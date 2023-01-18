---
title: Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising]
description: Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising]

*Annonceurs avec DSP Advertising et[!DNL Advertising Search]*

Consultez les informations suivantes avant d’intégrer Adobe Advertising à Adobe Analytics.

## Conditions requises pour la création de rapports sur les données Advertising d’Adobe dans [!DNL Analytics]

* L’une des options suivantes :
   * SDK Web Adobe Experience Platform : `alloy.js`
   * Service Experience Cloud Identity : `visitorAPI.js` version 2.0 ou ultérieure
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente de chaque bibliothèque.

## Conditions requises pour le partage de segments Analytics avec Adobe Advertising

* Service Experience Cloud Identity : `visitorAPI.js` version 2.1 ou ultérieure
* Adobe Analytics : `!DNL appMeasurement.js` version 1.8 ou ultérieure

## Conditions requises pour la création de rapports [!DNL Analytics] Données dans Adobe Advertising

Fournissez les informations suivantes à l’équipe de mise en oeuvre d’Adobe Advertising :

* Le [!DNL Analytics] Identifiant de suite de rapports qui sera utilisé pour la création de rapports sur l’activité de médias payants et pour alimenter l’activité du site à des fins d’optimisation et de création de rapports dans Adobe Advertising
* ID d’organisation Experience Cloud de l’entreprise (ID d’organisation).

Vous trouverez ces deux identifiants sur la page [Onglet Résumé du débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Écran récapitulatif des Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Données dans Adobe Advertising {#lookback-a4adc}

Parce que [!DNL Analytics] Les données sont envoyées à Adobe Advertising pour la création de rapports et l’optimisation, les données sont soumises aux règles d’attribution, y compris les intervalles d’impression et de recherche en amont des clics, qui sont configurés pour l’annonceur dans Adobe Advertising.

![Paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe de l’intervalle de recherche en amont des clics d’attribution : Nombre de jours après le premier clic au cours desquels le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; le maximum est de 90 jours
* Adobe de l’intervalle de recherche en amont des impressions d’attribution : Nombre de jours après une impression publicitaire au cours desquels l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; le maximum est de 30 jours

   >[!NOTE]
   >
   > L’intervalle de recherche en amont des impressions est spécifique à Adobe Advertising, et non [!DNL Analytics for Advertising], création de rapports.

Le [!DNL Analytics for Advertising] JavaScript utilise ces paramètres pour déterminer jusqu’où considérer comme valide une entrée d’affichage publicitaire ou de clic publicitaire sur le site. Pour plus d’informations sur la manière dont les affichages publicitaires et les clics publicitaires sont déterminés, voir &quot;[Adobe des identifiants publicitaires utilisés par Analytics](ids.md).&quot;

## Adobe des données Advertising dans [!DNL Analytics]

[!DNL Analytics] définit les identifiants de publicité Adobe (AMO ID) dans l’accès Analytics, sous réserve du paramètre de persistance de l’eVar de l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal Adobe Advertising et votre [!DNL Adobe] l’équipe du compte peut la modifier.

* [!DNL Analytics for Advertising] Expiration de l’eVar : 60 jours par défaut pour les AMO ID

>[!NOTE]
>
>Pour segmenter les données pour une autre période, vous pouvez : [configuration de segments personnalisés](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) avec différentes intervalles de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Affichage
* Vidéo
* Vidéo en ligne
* Native

Contactez votre [!DNL Adobe] équipe de compte pour les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant l’implémentation

* L’équipe de mise en oeuvre d’Adobe Advertising configurera l’intégration.

* Aucun coût supplémentaire n’est facturé pour cette intégration et les appels au serveur ne génèrent pas non plus de frais supplémentaires. [!DNL Analytics] ou les frais de publicité d’Adobe.

* [!DNL Analytics for Advertising] est indépendant du serveur de publicités : un affichage publicitaire ou un clic publicitaire peut survenir à partir de n’importe quel serveur d’annonces et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration ne transmet que [!DNL Analytics] événements standard et personnalisés pour Adobe de la publicité afin d’optimiser l’offre des médias payants et des efforts publicitaires ultérieurs. Ça ne passe pas. [!DNL Analytics] segments, mesures calculées et eVars pour Adobe de la publicité pour l’optimisation des offres.

* Adobe Advertising crée des identifiants persistants dans [!DNL Analytics] en fonction de la dernière publicité sur laquelle l’utilisateur a cliqué ou visionné avant d’accéder au site, en fonction de la variable [fenêtres de recherche en amont des clics et des affichages publicitaires](#lookback-a4adc) configuré dans Adobe Advertising. Si un visiteur du site devait avoir les deux types d’interactions d’entrée sur le site dans son profil et que le clic se trouve dans la période de recherche arrière, l’identifiant de clic publicitaire du visiteur remplacerait l’identifiant d’affichage publicitaire pour la création de rapports sur le site.

* [!DNL Analytics for Advertising] le suivi des conversions dans Adobe Analytics utilise un intervalle de recherche en amont de suivi configurable (60 jours par défaut). Les rapports de publicité Adobe reflètent les conversions et l’engagement du site tout au long de cette période de recherche en amont de suivi.

* Tous les types d’annonces sont pris en charge. Cependant, tous les environnements d’annonces ne sont pas pris en charge.

   Par exemple, les publicités de télévision connectée (CTV) ne sont pas suivies car aucun clic n’est effectué dans CTV et aucune conversion ne peut avoir lieu sur le même appareil. Cependant, si la publicité est affichée dans un environnement de bureau, certaines données d’entrée de site d’affichage publicitaire peuvent être suivies.

* [!DNL Analytics] les conversions sont actuellement suivies et attribuées uniquement à un visiteur sur le même appareil.

* [!DNL Analytics for Advertising] ne prend pas en charge les conversions d’affichage publicitaire in-app.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation de transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois le service Identity Experience Cloud mis en oeuvre pour un site, les accès qui contiennent des données provenant de [!DNL Analytics] ou Adobe Advertising contient un ID supplémentaire.

Exemple : `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration des données précise, tous les appels Adobe Advertising utilisés par une [!DNL Analytics for Advertising] activité pour diffuser du contenu ou enregistrer la mesure d’objectif doit avoir une [!DNL Analytics] accès qui partage le même ID supplémentaire.

Lorsque vous résolvez les problèmes dans [!DNL Analytics], veillez à confirmer que l’ID supplémentaire est présent pour [!DNL Analytics] accès. Dans le [Débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), vous pouvez voir cet identifiant dans l’onglet Adobe Advertising en tant que `sdid` .

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que la variable [!DNL Analytics for Target] intégration.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Code JavaScript pour Analytics pour la publicité](/help/integrations/analytics/javascript.md)

