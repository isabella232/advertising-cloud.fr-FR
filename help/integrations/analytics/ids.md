---
title: Adobe des identifiants publicitaires utilisés par [!DNL Analytics]
description: Adobe des identifiants publicitaires utilisés par [!DNL Analytics]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---

# Adobe des identifiants publicitaires utilisés par [!DNL Analytics]

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

*Applicable au DSP de publicité et[!DNL Advertising Search]*

Adobe Advertising utilise deux identifiants pour le suivi des performances sur site : la valeur *EF ID* et le *AMO ID*.

Lorsqu’une impression publicitaire se produit, Adobe Advertising crée les valeurs AMO ID et EF ID et les stocke. Lorsqu’un visiteur qui a vu une publicité arrive sur le site sans cliquer sur une publicité, [!DNL Analytics] appelle ces valeurs à partir d’Adobe Advertising via le [!DNL Analytics for Advertising] Code JavaScript. Pour le trafic d’affichage publicitaire, [!DNL Analytics] génère un ID supplémentaire (`SDID`), qui est utilisé pour associer l’EF ID et l’AMO ID à [!DNL Analytics]. Pour le trafic de clics publicitaires, ces identifiants sont inclus dans l’URL de la page d’entrée à l’aide de la variable `s_kwcid` et `ef_id` paramètres de chaîne de requête.

Adobe Advertising fait la distinction entre un clic publicitaire ou une entrée d’affichage publicitaire sur le site web selon les critères suivants :

* Une entrée d’affichage publicitaire est capturée lorsqu’un utilisateur se rend sur le site après avoir affiché une publicité, mais sans cliquer dessus. [!DNL Analytics] enregistre un affichage publicitaire si deux conditions sont remplies :
   * Le visiteur ne dispose d’aucun clic publicitaire pour une [!DNL DSP] ou [!DNL Search] pendant la [intervalle de recherche en amont des clics](#lookback-a4adc).
   * Le visiteur a vu au moins une [!DNL DSP] pendant la [intervalle de recherche en amont des impressions](#lookback-a4adc). La dernière impression est transmise comme affichage publicitaire.
* Une entrée de clic publicitaire est capturée lorsqu’un visiteur du site clique sur une publicité avant d’accéder au site. [!DNL Analytics] capture un clic publicitaire lorsque l’une des conditions suivantes se produit :
   * L’URL comprend un identifiant EF et un AMO ID, ajoutés à l’URL de la page d’entrée par Adobe Advertising.
   * L’URL ne contient aucun code de suivi, mais le code JavaScript Adobe Advertising détecte un clic au cours des deux dernières minutes.

![Basé sur les vues Adobe Advertising [!DNL Analytics] integration](/help/integrations/assets/a4adc-view-through-process.png)

*Figure 1 : Basé sur les vues Adobe Advertising [!DNL Analytics] integration*

![Clic Adobe Advertising basé sur une URL [!DNL Analytics] integration](/help/integrations/assets/a4adc-click-through-process.png)

*Figure 2 : Clic Adobe Advertising basé sur une URL [!DNL Analytics] integration*

## Adobe des ID EF Advertising

L’identifiant EF est un jeton unique utilisé par Adobe Advertising pour associer une activité à une exposition sur les clics ou publicités en ligne. L’identifiant EF est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou la dimension rVar (eVar réservé) (identifiant EF de publicité Adobe) et suit chaque clic ou exposition publicitaire au niveau du navigateur ou de l’appareil individuel. Les EF ID agissent principalement comme clés d’envoi [!DNL Analytics] données à Adobe Advertising pour la création de rapports et l’optimisation des offres dans Adobe Advertising.

### Format d’identifiant EF

>[!NOTE]
>
>Les identifiants EF sont sensibles à la casse. Si [!DNL Analytics] l’implémentation force le suivi des URL à être en minuscules, puis Adobe Advertising ne reconnaît pas l’identifiant EF. Cela aura un impact sur les offres et les rapports Adobe Advertising, mais n’aura aucun impact sur les rapports Adobe Advertising dans [!DNL Analytics].

#### [!DNL Google Ads] annonces de recherche

```{gclid}:G:s```

où :

* `gclid` est la valeur [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### Publicités de recherche Microsoft Advertising

```{msclkid}:G:s```

où :

* `msclkid` est la valeur [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (&quot;s&quot; pour la recherche).

#### Afficher des publicités et des annonces de recherche sur d’autres moteurs de recherche

```<Adobe Advertising visitor ID>:<timestamp>:<channel type>```

où :

* &lt;*Identifiant visiteur Adobe Advertising*> est un identifiant unique par visiteur (tel que UmKVaABCkJ0mDt). Également appelé *ID de surfeur*.

* &lt;*timestamp*> correspond à l’heure au format YYYYMMDHHMMSS (par exemple, 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19):25:33).

* &lt;*type de canal*> est le type de canal responsable du clic ou de l’exposition :

   * `d` pour un clic sur une publicité DSP (clic publicitaire)
   * `i` pour une impression d’une publicité DSP (affichage publicitaire)
   * `s` pour un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple `EF `ID : WcmibgAAAHJK1RyY:1551968087687:d

### La Dimension d’identifiant EF dans [!DNL Analytics]

Dans [!DNL Analytics] rapports, vous pouvez rechercher les données d’identifiant EF en recherchant la variable [!UICONTROL EF ID] et en utilisant la dimension [!UICONTROL EF ID Instance] mesure.

Les identifiants EF sont soumis à la limite d’identifiant unique de 500 000 dans Analysis Workspace. Une fois la valeur de 500 000 atteinte, tous les nouveaux codes de suivi sont signalés sous le titre d’un élément de ligne &quot;[!UICONTROL Low Traffic].&quot; En raison de la possibilité d’une fidélité de création de rapports manquante, les identifiants EF ne sont pas classés et vous ne devez pas les utiliser pour les segments ou la création de rapports dans [!DNL Analytics].

## Adobe des AMO ID

L’AMO ID effectue le suivi de chaque combinaison d’annonces unique à un niveau moins granulaire et est utilisé pour [!DNL Analytics] classification des données et ingestion de mesures publicitaires (telles que les impressions, les clics et les coûts) provenant d’Adobe Advertising. L’AMO ID est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou la dimension rVar (AMO ID) et est utilisée exclusivement pour la création de rapports dans [!DNL Analytics].

L’AMO ID est également appelé `s_kwcid`, qui est parfois prononcé en tant que &quot;[!DNL the squid].&quot;

### Format AMO ID pour [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

où :

* &lt;*Identifiant de canal*> peut être :

   * `AC` = DSP de publicité
   * `AL` pour [!DNL Advertising Search]

* &lt;*Identifiant de publicité*> est utilisé comme identifiant unique généré par la publicité par un Adobe. Il sert de clé pour traduire les métadonnées d’entité Adobe Advertising en métadonnées lisibles. [!DNL Analytics] dimensions.

* &lt;*Identifiant de référencement*> est un identifiant unique généré par la publicité Adobe pour un emplacement. Il sert de clé pour traduire les métadonnées d’entité Adobe Advertising en métadonnées lisibles. [!DNL Analytics] dimensions.

Exemple d’AMO ID : AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Format AMO ID pour [!DNL Search]

AMO ID pour [!DNL Search] suivent un format distinct pour chaque moteur de recherche. Le format de tous les moteurs de recherche commence par ce qui suit :

```AL!{userid}!{sid}```

où :

* `AL` est l’identifiant de canal du réseau publicitaire.
* `{userid}` est l’identifiant utilisateur numérique unique attribué par Adobe Advertising à l’annonceur.
* `{sid}` est l’identifiant numérique utilisé par Adobe Advertising pour le réseau publicitaire spécifié, tel que `3` pour [!DNL Google Ads] ou `10` pour [!DNL Microsoft Advertising].

Vous trouverez ci-dessous les formats AMO ID complets pour quelques réseaux publicitaires. Pour les formats AMO ID pour d’autres réseaux publicitaires, contactez votre [!DNL Adobe] l&#39;équipe du compte.

Format AMO ID pour [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

où :

* `{creative}` est la valeur [!DNL Google Ads] identifiant numérique unique du créatif.
* `{matchtype}` est le type de correspondance du mot-clé qui a déclenché la publicité : `e` pour exact, `p` pour l’expression, ou `b` pour large.
* `{placement}` est le nom de domaine du site web sur lequel l’utilisateur a cliqué sur la publicité. Une valeur est disponible pour les publicités des campagnes ciblées par emplacement et pour les publicités des campagnes ciblées par mot-clé qui s’affichent sur les sites de contenu.
* `{network}` indique le réseau à partir duquel le clic s’est produit :  `g` pour [!DNL Google] recherche (pour les annonces ciblées par mot-clé uniquement), `s` pour un partenaire de recherche (pour les annonces ciblées par mot-clé uniquement) ou `d` pour le réseau d’affichage (pour les annonces ciblées par mot-clé ou les annonces ciblées par emplacement).
* `{keyword}` est le mot-clé spécifique qui a déclenché votre publicité (sur les sites de recherche) ou le mot-clé correspondant le mieux (sur les sites de contenu).

Format AMO ID pour [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

où :

* `{AdId}` est la valeur [!DNL Microsoft Advertising] identifiant numérique unique du créatif.
* `{OrderItemId}` est la valeur [!DNL Microsoft Advertising] ID numérique du mot-clé.

### Dimension AMO ID dans [!DNL Analytics]

Dans les rapports Analytics, vous pouvez rechercher des données AMO ID en recherchant la variable [!UICONTROL AMO ID] et en utilisant la dimension [!UICONTROL AMO ID Instance] mesure. Le [!UICONTROL AMO ID] La dimension contient toutes les valeurs AMO ID capturées, tandis que la variable [!UICONTROL AMO ID Instance] mesure indique la fréquence de capture d’une valeur AMO ID par le site. Par exemple, si la même publicité de recherche a fait l’objet de quatre clics mais qu’Analytics a suivi sept entrées de site, [!UICONTROL AMO ID Instance] serait de sept (7) et [!UICONTROL Clicks] serait quatre (4).

Pour tout rapport ou audit dans [!DNL Analytics], la bonne pratique consiste à utiliser l’AMO ID avec son instance correspondante. Pour plus d’informations, voir[Validation des données pour [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; dans &quot;Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising.&quot;

## À propos des classifications Analytics

Dans [!DNL Analytics], un [classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) est un élément de métadonnées d’un code de suivi donné, tel qu’un compte, une campagne ou une publicité. Adobe Advertising classe les données Advertising d’Adobe brutes à l’aide de classifications afin que vous puissiez afficher les données de différentes manières (par exemple, par type de publicité ou par campagne) lors de la génération des rapports. Les classifications constituent la base du reporting Adobe Advertising dans [!DNL Analytics] et peut être utilisé avec les mesures AMO, telles que [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], et [!UICONTROL AMO Clicks], ainsi que des événements personnalisés et standard sur site tels que [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], et [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md)

