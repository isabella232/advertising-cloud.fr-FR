---
title: Advertising Cloud ID utilisés par [!DNL Analytics]
description: Advertising Cloud ID utilisés par [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising Cloud ID utilisés par [!DNL Analytics]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Applicable à Advertising Cloud DSP et Advertising Cloud Search*

Advertising Cloud utilise deux identifiants pour le suivi des performances sur site : la valeur *EF ID* et le *AMO ID*.

Lorsqu’une impression de publicité se produit, Advertising Cloud crée les valeurs AMO ID et EF ID et les stocke. Lorsqu’un visiteur qui a vu une publicité arrive sur le site sans cliquer sur une publicité, [!DNL Analytics] appelle ces valeurs à partir d’Advertising Cloud via la fonction [!DNL Analytics for Advertising Cloud] Code JavaScript. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), qui est utilisé pour associer l’EF ID et l’AMO ID à [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page d’entrée à l’aide de la variable `s_kwcid` et `ef_id` paramètres de chaîne de requête.

Advertising Cloud fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web selon les critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur se rend sur le site après avoir affiché une publicité, mais sans cliquer dessus. [!DNL Analytics] enregistre un affichage publicitaire si deux conditions sont remplies :
   * Le visiteur ne dispose d’aucun clic publicitaire pour une [!DNL DSP] ou [!DNL Search] pendant la [intervalle de recherche en amont des clics](#lookback-a4adc).
   * Le visiteur a vu au moins une [!DNL DSP] pendant la [intervalle de recherche en amont des impressions](#lookback-a4adc). La dernière impression est transmise comme affichage publicitaire.
* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une publicité avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :
   * L’URL comprend un EF ID et un AMO ID, ajoutés à l’URL de la page d’entrée par Advertising Cloud.
   * L’URL ne contient aucun code de suivi, mais le code JavaScript Advertising Cloud détecte un clic au cours des deux dernières minutes.

![Basé sur les vues Advertising Cloud [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Basé sur les vues Advertising Cloud [!DNL Analytics] integration*

![Clic Advertising Cloud basé sur une URL [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : Clic Advertising Cloud basé sur une URL [!DNL Analytics] integration*

## Advertising Cloud EF ID

L’identifiant EF est un jeton unique utilisé par Advertising Cloud pour associer l’activité à une exposition aux clics ou publicités en ligne. L’identifiant EF est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou de la dimension rVar (eVar réservé) (Advertising Cloud EF ID) et effectue le suivi de chaque clic ou exposition publicitaire au niveau du navigateur ou de l’appareil. Les EF ID agissent principalement comme clés d’envoi [!DNL Analytics] données à Advertising Cloud pour la création de rapports et l’optimisation des offres dans Advertising Cloud.

### Format d’identifiant EF

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

où :

* &lt;*Identifiant visiteur Advertising Cloud*> est un identifiant unique par visiteur (tel que UmKVaABCkJ0mDt). Également appelé *ID de surfeur*.

* &lt;*timestamp*> correspond à l’heure au format YYYYMMDHHMMSS (par exemple, 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19):25:33).

* &lt;*type de canal*> est le type de canal responsable du clic ou de l’exposition :

   * `d` pour un clic sur une publicité DSP (clic publicitaire)
   * `i` pour une impression d’une publicité DSP (affichage publicitaire)
   * `s` pour un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple `EF `ID : WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Les identifiants EF sont sensibles à la casse. Si [!DNL Analytics] l’implémentation force le suivi des URL en minuscules, puis Advertising Cloud ne reconnaît pas l’identifiant EF. Cela aura un impact sur les offres Advertising Cloud et la création de rapports, mais n’aura aucun impact sur la création de rapports Advertising Cloud dans [!DNL Analytics].

### La Dimension d’identifiant EF dans [!DNL Analytics]

Dans [!DNL Analytics] rapports, vous pouvez rechercher les données d’identifiant EF en recherchant la variable [!UICONTROL EF ID] et en utilisant la dimension [!UICONTROL EF ID Instance] mesure.

Les identifiants EF sont soumis à la limite d’identifiant unique de 500 000 dans Analysis Workspace. Une fois la valeur de 500 000 atteinte, tous les nouveaux codes de suivi sont signalés sous le titre d’un élément de ligne &quot;[!UICONTROL Low Traffic].&quot; En raison de la possibilité d’une fidélité de création de rapports manquante, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou la création de rapports dans [!DNL Analytics].

## Advertising Cloud AMO ID

L’AMO ID effectue le suivi de chaque combinaison d’annonces unique à un niveau moins granulaire et est utilisé pour [!DNL Analytics] classification des données et ingestion de mesures publicitaires (telles que les impressions, les clics et les coûts) à partir d’Advertising Cloud. L’AMO ID est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou la dimension rVar (AMO ID) et est utilisée exclusivement pour la création de rapports dans [!DNL Analytics].

L’AMO ID est également appelé `s_kwcid`, qui est parfois prononcé en tant que &quot;[!DNL the squid].&quot;

### Format AMO ID pour [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

où :

* &lt;*Identifiant de canal*> peut être :

   * `AC` = Advertising Cloud DSP
   * `AL` pour Advertising Cloud Search

* &lt;*Identifiant de publicité*> est utilisé comme identifiant unique généré par Advertising Cloud pour une publicité. Il sert de clé pour traduire les métadonnées d’entité Advertising Cloud en métadonnées lisibles. [!DNL Analytics] dimensions.

* &lt;*Identifiant de référencement*> est un identifiant unique généré par Advertising Cloud pour un emplacement. Il sert de clé pour traduire les métadonnées d’entité Advertising Cloud en métadonnées lisibles. [!DNL Analytics] dimensions.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

Exemple d’AMO ID : AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Format AMO ID pour [!DNL Search]

AMO ID pour [!DNL Search] suivent un format distinct pour chaque moteur de recherche. Le format de tous les moteurs de recherche commence par ce qui suit :

```AL!{ef_userid}!{ef_sid}```

où :

* `AL` est l’identifiant de canal pour le canal de recherche.
* `{ef_userid}` est l’identifiant utilisateur numérique unique attribué par Advertising Cloud à l’annonceur.
* `{ef_sid}` est l’identifiant numérique utilisé par Advertising Cloud pour le moteur de recherche spécifié, tel que `3` pour [!DNL Google Ads] ou `10` pour [!DNL Microsoft Advertising].

Vous trouverez ci-dessous les formats AMO ID complets pour quelques moteurs de recherche. Pour connaître les formats AMO ID des autres moteurs de recherche, contactez votre [!DNL Adobe] l&#39;équipe du compte.

Format AMO ID pour [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

où :

* `{creative}` est la valeur [!DNL Google Ads] identifiant numérique unique du créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité : `e` pour exact, `p` pour l’expression, ou `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel l’utilisateur a cliqué sur la publicité. Une valeur est disponible pour les publicités des campagnes ciblées par emplacement et pour les publicités des campagnes ciblées par mot-clé qui s’affichent sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic s’est produit :  `g` pour [!DNL Google] recherche (pour les annonces ciblées par mot-clé uniquement), `s` pour un partenaire de recherche (pour les annonces ciblées par mot-clé uniquement) ou `d` pour le réseau d’affichage (pour les annonces ciblées par mot-clé ou les annonces ciblées par emplacement).
* `{keyword}` est le mot-clé spécifique qui a déclenché votre publicité (sur les sites de recherche) ou le mot-clé correspondant le mieux (sur les sites de contenu).

Format AMO ID pour [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

où :

* `{AdId}` est la valeur [!DNL Microsoft Advertising] identifiant numérique unique du créatif.
* `{OrderItemId}` est la valeur [!DNL Microsoft Advertising] ID numérique du mot-clé.

### Dimension AMO ID dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez rechercher des données AMO ID en recherchant la variable [!UICONTROL AMO ID] et en utilisant la dimension [!UICONTROL AMO ID Instance] mesure. Le [!UICONTROL AMO ID] La dimension contient toutes les valeurs AMO ID capturées, tandis que la variable [!UICONTROL AMO ID Instance] mesure indique la fréquence de capture d’une valeur AMO ID par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instance] serait de sept (7) et [!UICONTROL Clicks] serait quatre (4).

Pour tout rapport ou audit dans [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir[Validation des données pour [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; dans &quot;Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud.&quot;

## À propos des classifications Analytics

Dans [!DNL Analytics], un [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées d’un code de suivi donné, tel qu’un compte, une campagne ou une publicité. Advertising Cloud classe les données Advertising Cloud brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par exemple, par type d’annonce ou campagne) lors de la génération des rapports. Les classifications constituent la base des rapports Advertising Cloud dans [!DNL Analytics] et peut être utilisé avec les mesures AMO, telles que [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], et [!UICONTROL AMO Clicks], ainsi qu’avec les événements personnalisés et standard sur site tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud](data-variances.md)

