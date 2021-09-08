---
title: Conditions préalables et informations clés pour la mise en oeuvre de  [!DNL Analytics for Advertising Cloud]
description: Conditions préalables et informations clés pour la mise en oeuvre de  [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Conditions préalables et informations clés pour la mise en oeuvre de [!DNL Analytics for Advertising Cloud]

*Annonceurs avec Advertising Cloud DSP et Advertising Cloud Search*

Consultez les informations suivantes avant d’intégrer Advertising Cloud à Adobe Analytics.

## Conditions requises pour la création de rapports sur les données Advertising Cloud dans [!DNL Analytics]

* Service Experience Cloud Identity : `visitorAPI.js` version 2.0 ou ultérieure
* Toute version d’Adobe Analytics (y compris [!DNL Prime], [!DNL Premium] ou [!DNL Ultimate])
* Adobe Analytics : `appMeasurement.js` version 2.1 ou ultérieure

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente du service Identity Experience Cloud avec prise en charge de CNAME, ainsi que la version la plus récente d’Analytics AppMeasurement pour JavaScript.

## Conditions requises pour le partage de segments Analytics avec Advertising Cloud

* Service Experience Cloud Identity : `visitorAPI.js` version 2.1 ou ultérieure
* Adobe Analytics : `!DNL appMeasurement.js` version 1.8 ou ultérieure

## Exigences pour les rapports [!DNL Analytics] données dans Advertising Cloud

Fournissez les informations suivantes à l’équipe de mise en oeuvre d’Advertising Cloud :

* Identifiant de la suite de rapports [!DNL Analytics] qui sera utilisé pour la création de rapports sur l’activité de médias payants et pour alimenter l’activité du site à des fins d’optimisation et de création de rapports dans Advertising Cloud
* ID d’organisation Experience Cloud de l’entreprise (ID d’organisation).

Vous trouverez ces deux ID dans l’écran [Résumé du débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Écran récapitulatif des Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Données dans Advertising Cloud {#lookback-a4adc}

Les données [!DNL Analytics] étant envoyées à Advertising Cloud pour la création de rapports et l’optimisation, elles sont soumises aux règles d’attribution, notamment les intervalles d’impression et de recherche en amont des clics, qui sont configurés pour l’annonceur dans Advertising Cloud.

![paramètres de l’intervalle de recherche en amont au niveau de l’annonceur dans Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Intervalle de recherche en amont des clics d’attribution Advertising Cloud : Nombre de jours après le premier clic au cours desquels le clic peut être attribué à une conversion. Par défaut, cette valeur est de 60 jours ; le maximum est de 90 jours
* Intervalle de recherche en amont des impressions d’attribution Advertising Cloud : Nombre de jours après une impression publicitaire au cours desquels l’impression peut être attribuée à une conversion. Par défaut, cette valeur est de 14 jours ; le maximum est de 30 jours

   >[!NOTE]
   >
   > L’intervalle de recherche en amont des impressions est spécifique aux rapports Advertising Cloud, et non [!DNL Analytics for Advertising Cloud].

Le code JavaScript [!DNL Analytics for Advertising Cloud] utilise ces paramètres pour déterminer jusqu’où considérer comme valide une entrée d’affichage publicitaire ou de clic publicitaire sur le site. Pour plus d’informations sur la manière dont les affichages publicitaires et les clics publicitaires sont déterminés, voir &quot;[Advertising Cloud IDs Used by Analytics](ids.md)&quot;.

## Données Advertising Cloud dans [!DNL Analytics]

[!DNL Analytics] définit les Advertising Cloud ID (AMO ID) dans l’accès Analytics, sous réserve du paramètre de persistance de l’eVar de l’annonceur, qui s’applique à la fois aux clics publicitaires et aux affichages publicitaires. Le paramètre de persistance est configuré sur le serveur principal Advertising Cloud et votre gestionnaire de compte d’Adobe peut le modifier.

* [!DNL Analytics for Advertising Cloud] Expiration de l’eVar : 60 jours par défaut pour les AMO ID

>[!NOTE]
>
>Pour segmenter les données pour une période différente, vous pouvez [configurer des segments personnalisés](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) avec différentes intervalles de recherche en amont dans Analysis Workspace.

## Environnements publicitaires pris en charge

* Rechercher
* Affichage
* Vidéo
* Vidéo en ligne
* Native

Contactez votre gestionnaire de compte Adobe pour connaître les derniers environnements publicitaires pris en charge dans chaque canal.

## Informations à connaître avant l’implémentation

* Aucun coût supplémentaire n’est facturé pour cette intégration et les appels au serveur ne génèrent pas non plus de [!DNL Analytics] ou de frais Advertising Cloud supplémentaires.

* [!DNL Analytics for Advertising Cloud] est indépendant du serveur de publicités : un affichage publicitaire ou un clic publicitaire peut survenir à partir de n’importe quel serveur d’annonces et les identifiants appropriés sont générés lors de l’entrée sur le site.

* L’intégration transmet uniquement les [!DNL Analytics] événements standard et personnalisés à Advertising Cloud afin d’optimiser l’offre des efforts publicitaires et des médias payants ultérieurs. Il ne transmet pas de segments [!DNL Analytics], de mesures calculées et d’eVars à Advertising Cloud pour l’optimisation des offres.

* Advertising Cloud crée des identifiants persistants dans [!DNL Analytics] en fonction de la dernière publicité sur laquelle l’utilisateur a cliqué ou consultée avant d’entrer sur le site, en fonction des [intervalles de recherche en amont des clics et affichages publicitaires](#lookback-a4adc) configurés dans Advertising Cloud. Si un visiteur du site devait avoir les deux types d’interactions d’entrée sur le site dans son profil et que le clic se trouve dans la période de recherche arrière, l’identifiant de clic publicitaire du visiteur remplacerait l’identifiant d’affichage publicitaire pour la création de rapports sur le site.

* [!DNL Analytics for Advertising Cloud] le suivi des conversions dans Adobe Analytics utilise un intervalle de recherche en amont de suivi configurable (60 jours par défaut). Les rapports Advertising Cloud reflètent les conversions et l’engagement du site tout au long de cette période de recherche en amont de suivi.

* Tous les types d’annonces sont pris en charge. Cependant, tous les environnements d’annonces ne sont pas pris en charge.

   Par exemple, les publicités de télévision connectée (CTV) ne sont pas suivies car aucun clic n’est effectué dans CTV et aucune conversion ne peut avoir lieu sur le même appareil. Cependant, si la publicité est affichée dans un environnement de bureau, certaines données d’entrée de site d’affichage publicitaire peuvent être suivies.

* [!DNL Analytics] les conversions sont actuellement suivies et attribuées uniquement à un visiteur sur le même appareil.

* [!DNL Analytics for Advertising Cloud] ne prend pas en charge les conversions d’affichage publicitaire in-app.

* Le suivi des affichages publicitaires n’est pas pris en charge pour les annonceurs qui utilisent une implémentation de transfert côté serveur de [!DNL Analytics].

### ID supplémentaire

Une fois le service Identity Experience Cloud mis en oeuvre pour un site, les accès qui contiennent des données de [!DNL Analytics] ou d’Advertising Cloud contiennent un ID supplémentaire.

Exemple : `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Pour une intégration des données exacte, tous les appels Advertising Cloud utilisés par une activité [!DNL Analytics for Advertising Cloud] pour diffuser du contenu ou enregistrer la mesure d’objectif doivent avoir un accès [!DNL Analytics] correspondant partageant le même ID supplémentaire.

Lorsque vous effectuez un dépannage dans [!DNL Analytics], veillez à confirmer que l’ID supplémentaire est présent pour les accès [!DNL Analytics]. Dans [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html), vous pouvez voir cet ID dans l’onglet Advertising Cloud comme paramètre `sdid`.

>[!NOTE]
>
> Cette implémentation fonctionne de la même manière que l’intégration [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Code JavaScript pour Analytics pour Advertising Cloud](/help/integrations/analytics/javascript.md)

