---
title: Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]
description: Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---

# Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]

*Annonceurs avec Advertising Cloud DSP et Advertising Cloud Search*

Consultez les informations suivantes avant d’intégrer Advertising Cloud à Adobe Analytics.

## Conditions requises pour la création de rapports sur les données Advertising Cloud dans [!DNL Analytics]

* Service Experience Cloud Identity : `visitorAPI.js` version 2.0 ou ultérieure
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium]ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente du service Identity Experience Cloud avec prise en charge de CNAME, ainsi que la version la plus récente d’Analytics AppMeasurement pour JavaScript.

## Conditions requises pour le partage de segments Analytics avec Advertising Cloud

* Service Experience Cloud Identity : `visitorAPI.js` version 2.1 ou ultérieure
* Adobe Analytics : `!DNL appMeasurement.js` version 1.8 ou ultérieure

## Conditions requises pour la création de rapports [!DNL Analytics] Données dans Advertising Cloud

Fournissez les informations suivantes à l’équipe de mise en oeuvre d’Advertising Cloud :

* Le [!DNL Analytics] identifiant de suite de rapports qui sera utilisé pour la création de rapports sur l’activité de médias payants et pour alimenter l’activité du site à des fins d’optimisation et de création de rapports dans Advertising Cloud.
* ID d’organisation Experience Cloud de l’entreprise (ID d’organisation).

Vous trouverez ces deux identifiants sur la page [Écran récapitulatif du débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Écran récapitulatif des Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Données dans Advertising Cloud {#lookback-a4adc}

Parce que [!DNL Analytics] Les données sont envoyées à Advertising Cloud à des fins de création de rapports et d’optimisation. Elles sont soumises aux règles d’attribution, notamment aux intervalles de recherche en amont des impressions et des clics, configurés pour l’annonceur dans Advertising Cloud.

![paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Intervalle de recherche en amont des clics d’attribution Advertising Cloud : Nombre de jours après le premier clic au cours desquels le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; le maximum est de 90 jours
* Intervalle de recherche en amont des impressions d’attribution Advertising Cloud : Nombre de jours après une impression publicitaire au cours desquels l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; le maximum est de 30 jours

   >[!NOTE]
   >
   > L’intervalle de recherche en amont des impressions est spécifique à Advertising Cloud, et non [!DNL Analytics for Advertising Cloud], création de rapports.

Le [!DNL Analytics for Advertising Cloud] JavaScript utilise ces paramètres pour déterminer jusqu’où considérer comme valide une entrée d’affichage publicitaire ou de clic publicitaire sur le site. Pour plus d’informations sur la manière dont les affichages publicitaires et les clics publicitaires sont déterminés, voir &quot;[Advertising Cloud ID utilisés par Analytics](ids.md).&quot;

## Données Advertising Cloud dans [!DNL Analytics]

[!DNL Analytics] définit les Advertising Cloud ID (AMO ID) dans l’accès Analytics, sous réserve du paramètre de persistance de l’eVar de l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal Advertising Cloud et votre [!DNL Adobe] le gestionnaire de compte peut le modifier.

* [!DNL Analytics for Advertising Cloud] Expiration de l’eVar : 60 jours par défaut pour les AMO ID

>[!NOTE]
>
>Pour segmenter les données pour une autre période, vous pouvez : [configuration de segments personnalisés](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) avec différentes intervalles de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Affichage
* Vidéo
* Vidéo en ligne
* Native

Contactez votre [!DNL Adobe] gestionnaire de compte pour les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant l’implémentation

* Aucun coût supplémentaire n’est facturé pour cette intégration et les appels au serveur ne génèrent pas non plus de frais supplémentaires. [!DNL Analytics] ou les frais Advertising Cloud.

* [!DNL Analytics for Advertising Cloud] est indépendant du serveur de publicités : un affichage publicitaire ou un clic publicitaire peut survenir à partir de n’importe quel serveur d’annonces et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration ne transmet que [!DNL Analytics] événements standard et personnalisés vers Advertising Cloud pour optimiser l’offre des efforts publicitaires et des médias payants ultérieurs. Ça ne passe pas. [!DNL Analytics] segments, mesures calculées et eVars à Advertising Cloud pour l’optimisation des offres.

* Advertising Cloud crée des identifiants persistants dans [!DNL Analytics] en fonction de la dernière publicité sur laquelle l’utilisateur a cliqué ou visionné avant d’accéder au site, en fonction de la variable [fenêtres de recherche en amont des clics et des affichages publicitaires](#lookback-a4adc) configuré dans Advertising Cloud. Si un visiteur du site devait avoir les deux types d’interactions d’entrée sur le site dans son profil et que le clic se trouve dans la période de recherche arrière, l’identifiant de clic publicitaire du visiteur remplacerait l’identifiant d’affichage publicitaire pour la création de rapports sur le site.

* [!DNL Analytics for Advertising Cloud] le suivi des conversions dans Adobe Analytics utilise un intervalle de recherche en amont de suivi configurable (60 jours par défaut). Les rapports Advertising Cloud reflètent les conversions et l’engagement du site tout au long de cette période de recherche en amont de suivi.

* Tous les types d’annonces sont pris en charge. Cependant, tous les environnements d’annonces ne sont pas pris en charge.

   Par exemple, les publicités de télévision connectée (CTV) ne sont pas suivies car aucun clic n’est effectué dans CTV et aucune conversion ne peut avoir lieu sur le même appareil. Cependant, si la publicité est affichée dans un environnement de bureau, certaines données d’entrée de site d’affichage publicitaire peuvent être suivies.

* [!DNL Analytics] les conversions sont actuellement suivies et attribuées uniquement à un visiteur sur le même appareil.

* [!DNL Analytics for Advertising Cloud] ne prend pas en charge les conversions d’affichage publicitaire in-app.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation de transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois le service Identity Experience Cloud mis en oeuvre pour un site, les accès qui contiennent des données provenant de [!DNL Analytics] ou Advertising Cloud contient un ID supplémentaire.

Exemple : `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration des données précise, tous les appels Advertising Cloud utilisés par une [!DNL Analytics for Advertising Cloud] activité pour diffuser du contenu ou enregistrer la mesure d’objectif doit avoir une [!DNL Analytics] accès qui partage le même ID supplémentaire.

Lorsque vous résolvez les problèmes dans [!DNL Analytics], veillez à confirmer que l’ID supplémentaire est présent pour [!DNL Analytics] accès. Dans le [Débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html), cet identifiant s’affiche dans l’onglet Advertising Cloud sous la forme `sdid` .

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que la variable [!DNL Analytics for Target] intégration.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Code JavaScript pour Analytics pour Advertising Cloud](/help/integrations/analytics/javascript.md)

