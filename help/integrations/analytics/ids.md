---
title: Advertising Cloud ID utilisés par [!DNL Analytics]
description: Advertising Cloud ID utilisés par [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Advertising Cloud ID utilisés par [!DNL Analytics]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Applicable à Advertising Cloud DSP et Advertising Cloud Search*

Advertising Cloud utilise deux identifiants pour le suivi des performances sur site :  l’identifiant EF et l’identifiant AMO.

Lorsqu’une impression de publicité se produit, Advertising Cloud crée les valeurs AMO ID et EF ID et les stocke. Lorsqu’un visiteur qui a vu une publicité arrive sur le site sans cliquer sur une publicité, [!DNL Analytics] appelle ces valeurs à partir d’Advertising Cloud par le biais du code JavaScript [!DNL Analytics for Advertising Cloud]. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), utilisé pour associer l’ID EF et l’AMO à [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page d’entrée à l’aide des paramètres de chaîne de requête `s_kwcid` et `ef_id` .

Advertising Cloud fait la distinction entre une entrée de clic publicitaire ou d’affichage publicitaire sur le site web selon les critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur se rend sur le site après avoir affiché une publicité, mais sans cliquer dessus. [!DNL Analytics] enregistre un affichage publicitaire si deux conditions sont remplies :
   * Le visiteur n’a aucun clic publicitaire pour une publicité [!DNL DSP] ou [!DNL Search] au cours de l’[intervalle de recherche en amont des clics](#lookback-a4adc).
   * Le visiteur a vu au moins une publicité [!DNL DSP] au cours de la [période de recherche en amont des impressions](#lookback-a4adc). La dernière impression est transmise comme affichage publicitaire.
* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une publicité avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :
   * L’URL comprend un EF ID et un AMO ID, ajoutés à l’URL de la page d’entrée par Advertising Cloud.
   * L’URL ne contient aucun code de suivi, mais le code JavaScript Advertising Cloud détecte un clic au cours des deux dernières minutes.

![ [!DNL Analytics] Intégration basée sur les vues Advertising Cloud](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 :  [!DNL Analytics] Intégration basée sur les vues Advertising Cloud*

![ [!DNL Analytics] Intégration d’Advertising Cloud basée sur des clics URL](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 :  [!DNL Analytics] Intégration d’Advertising Cloud basée sur des clics URL*

## Advertising Cloud EF ID

L’identifiant EF est un jeton unique utilisé par Advertising Cloud pour associer l’activité à une exposition aux clics ou publicités en ligne. L’identifiant EF est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (eVar réservé) (Advertising Cloud EF ID) et suit chaque clic ou exposition publicitaire au niveau du navigateur ou de l’appareil. Les EF ID agissent principalement comme des clés pour envoyer des données [!DNL Analytics] à Advertising Cloud afin de générer des rapports et d’optimiser les offres dans Advertising Cloud.

### Format d’identifiant EF

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

où :

* &lt;>Identifiant visiteur Advertising Cloud *> est un identifiant unique par visiteur (par exemple, EuhKVaABCkJ0mDt).* Également appelé *ID de surfeur*.

* &lt;>timestamp *> est l’heure au format YYYMMDHHMMSS (par exemple, 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19:25:33).*

* &lt;>type de canal *> est le type de canal responsable du clic ou de l’exposition :*

   * `d` pour un clic sur une publicité DSP (clic publicitaire)
   * `i` pour une impression d’une publicité DSP (affichage publicitaire)
   * `s` pour un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple `EF `ID : WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Les identifiants EF sont sensibles à la casse. Si une mise en oeuvre de [!DNL Analytics] force le suivi des URL en minuscules, Advertising Cloud ne reconnaît pas l’identifiant EF. Cela aura un impact sur les offres et les rapports Advertising Cloud, mais n’aura aucun impact sur les rapports Advertising Cloud dans [!DNL Analytics].

### Dimension d’identifiant EF dans [!DNL Analytics]

Dans les rapports [!DNL Analytics], vous pouvez rechercher des données d’identifiant d’EF en recherchant la dimension [!UICONTROL EF ID] et en utilisant la mesure [!UICONTROL EF ID Instance].

`EF IDs` sont soumises à la limite de 500 000 identifiants uniques dans Analysis Workspace. Une fois la valeur de 500 000 atteinte, tous les nouveaux codes de suivi sont signalés sous le titre d’un élément de ligne &quot;[!UICONTROL Low Traffic]&quot;. En raison de la fidélité potentielle des rapports, les `EF IDs` ne sont pas classifiés et vous ne devez pas les utiliser pour les segments ou les rapports dans [!DNL Analytics].

## Advertising Cloud AMO ID

L’AMO ID effectue le suivi de chaque combinaison de publicités unique à un niveau moins granulaire et est utilisé pour la classification des données [!DNL Analytics] et l’ingestion de mesures publicitaires (telles que les impressions, les clics et les coûts) depuis Advertising Cloud. L’AMO ID est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID) et est utilisé exclusivement pour la création de rapports dans [!DNL Analytics].

L’AMO ID est également appelé `s_kwcid`, parfois appelé &quot;calamar&quot;.

### Format AMO ID pour [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

où :

* &lt;>ID de canal *> peut être :*

   * `AC` = Advertising Cloud DSP
   * `AL` pour Advertising Cloud Search

* &lt;>ID de publicité&#x200B;*> est utilisé comme identifiant unique généré par Advertising Cloud pour une publicité.* Il sert de clé pour traduire les métadonnées d’entité Advertising Cloud en dimensions [!DNL Analytics] lisibles.

* &lt;>Identifiant de référencement *> est un identifiant unique généré par Advertising Cloud pour un emplacement.* Il sert de clé pour traduire les métadonnées d’entité Advertising Cloud en dimensions [!DNL Analytics] lisibles.

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

Les AMO ID pour [!DNL Search] suivent un format distinct pour chaque moteur de recherche. Le format de tous les moteurs de recherche commence par ce qui suit :

```AL!{ef_userid}!{ef_sid}```

où :

* `AL` est l’identifiant de canal pour le canal de recherche.
* `{ef_userid}` est l’identifiant utilisateur numérique unique attribué par Advertising Cloud à l’annonceur.
* `{ef_sid}` est l’identifiant numérique utilisé par Advertising Cloud pour le moteur de recherche spécifié, tel que  `3` pour  [!DNL Google Ads] ou  `10` pour  [!DNL Microsoft Advertising].

Vous trouverez ci-dessous les formats AMO ID complets pour quelques moteurs de recherche. Pour connaître les formats AMO ID des autres moteurs de recherche, contactez votre gestionnaire de compte Adobe.

Format AMO ID pour [!DNL Google Ads] :

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

où :

* `{creative}` est l’identifiant numérique  [!DNL Google Ads] unique de l’élément créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité :  `e` pour exact,  `p` pour expression ou  `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel l’utilisateur a cliqué sur la publicité. Une valeur est disponible pour les publicités des campagnes ciblées par emplacement et pour les publicités des campagnes ciblées par mot-clé qui s’affichent sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic s’est produit :   `g` pour  [!DNL Google] la recherche (pour les annonces ciblées par mot-clé uniquement),  `s` pour un partenaire de recherche (pour les annonces ciblées par mot-clé uniquement) ou  `d` pour le réseau d’affichage (pour les annonces ciblées par mot-clé ou par emplacement).
* `{keyword}` est le mot-clé spécifique qui a déclenché votre publicité (sur les sites de recherche) ou le mot-clé correspondant le mieux (sur les sites de contenu).

Format AMO ID pour [!DNL Microsoft Advertising] :

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

où :

* `{AdId}` est l’identifiant numérique  [!DNL Microsoft Advertising] unique de l’élément créatif.
* `{OrderItemId}` est l’identifiant  [!DNL Microsoft Advertising] numérique du mot-clé.

### Dimension AMO ID dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez rechercher des données AMO ID en recherchant la dimension [!UICONTROL AMO ID] et en utilisant la mesure [!UICONTROL AMO ID Instance]. La dimension [!UICONTROL AMO ID] héberge toutes les valeurs AMO ID capturées, tandis que la mesure [!UICONTROL AMO ID Instance] indique la fréquence à laquelle une valeur AMO ID a été capturée par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics, mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instance] correspondrait à sept (7) et [!UICONTROL Clicks] à quatre (4).

Pour tout rapport ou audit dans [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir &quot;[Validation des données pour [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; dans &quot;Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud&quot;.

## À propos des classifications Analytics

Dans [!DNL Analytics], une [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est une donnée de métadonnées pour un code de suivi donné, tel que Compte, Campagne ou Publicité. Advertising Cloud classe les données Advertising Cloud brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par exemple, par type d’annonce ou campagne) lors de la génération des rapports. Les classifications constituent la base des rapports Advertising Cloud dans [!DNL Analytics] et peuvent être utilisées avec les mesures AMO, telles que [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions] et [!UICONTROL AMO Clicks], ainsi qu’avec les événements personnalisés et standard sur site tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Écarts de données attendus  [!DNL Analytics] entre Advertising Cloud et](data-variances.md)

