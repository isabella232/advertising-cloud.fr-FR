---
title: Adobe des mesures publicitaires dans Analysis Workspace
description: Adobe des mesures publicitaires dans Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe des mesures publicitaires dans Analysis Workspace

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

>[!NOTE]
>
>* Adobe Advertising transmet les mesures et dimensions de trafic à [!DNL Analytics] tous les jours.
>* [!DNL Analytics] capture les clics publicitaires et les affichages publicitaires Adobe en temps réel.


## Mesures de trafic d’Adobe Advertising

>[!NOTE]
>
>Toutes les mesures de trafic Adobe Advertising dans [!DNL Analytics] commencez par &quot;AMO&quot;.

| Mesure de trafic | Description |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Nombre d’impressions de publicité Adobe. |
| [!UICONTROL AMO Clicks] | Nombre total de clics publicitaires d’Adobe. |
| [!UICONTROL AMO Cost] | Dépense de publicité Adobe dans la devise de la suite de rapports. |
| [!UICONTROL AMO ID Instance] | Nombre de fois où l’identifiant publicitaire Adobe est défini. |
| [!UICONTROL AMO Minutes Viewed] | Nombre de minutes pendant lesquelles une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO Views] | Nombre de vues sur une publicité. Une vue est comptabilisée lorsque la visionneuse lance la vidéo Adobe Advertising. |
| [!UICONTROL AMO Views 25% Complete] | Nombre d’affichages pour lesquels au moins 25 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO Views 50% Complete] | Nombre d’affichages pour lesquels au moins 50 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO Views 75% Complete] | Nombre d’affichages pour lesquels au moins 75 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO Views 100% Complete] | Nombre d’affichages pour lesquels 100 % d’une vidéo Adobe Advertising a été visionnée. |
| [!UICONTROL AMO Viewable Impressions] | Nombre d’impressions qui ont été mesurées pour être visibles en fonction de la configuration de l’emplacement. |
| [!UICONTROL AMO Not Viewable Impressions] | Nombre d’impressions qui n’étaient pas visibles. Cette valeur est calculée comme suit : ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Nombre d’impressions diffusées pour lesquelles l’instrumentation de visibilité a été initialisée avec succès. Cette valeur est calculée en tant que (impressions instrumentées : nombre d’impressions non mesurables). |

## Mesures calculées personnalisées utiles pour Adobe Advertising

Envisagez de créer les mesures suivantes pour vos données Adobe Advertising.

* Clics jusqu’à l’instance de page d’entrée ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]) : Il s’agit du pourcentage de personnes qui ont cliqué sur la publicité et l’ont affiché sur la page d’entrée.
* Taux mesurable ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Taux d’impression visible ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Coût par affichage ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Coût par clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Dimensions Adobe Advertising

>[!NOTE]
>
>Toutes les dimensions Adobe Advertising dans [!DNL Analytics] sont suivis de &quot;(AMO ID)&quot;.

| Dimension | Données Adobe Advertising applicables | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] et [!DNL Search] data | DSP de publicité ou nom du moteur de recherche |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] et [!DNL Search] data | Nom du compte. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] et [!DNL Search] data | RTB ([!DNL DSP]) ou le nom du réseau publicitaire ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Nom de la campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Le package ([!DNL DSP]) ou portefeuille ([!DNL Search]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Nom de l’emplacement. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Nom du groupe publicitaire. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Mot-clé. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Type de correspondance de recherche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Mot-clé et type de correspondance. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Le type d’annonce, tel que `text`, `video`, `display`ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Type de publicité ([!DNL DSP]) ou titre de publicité ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Description de la publicité ([!DNL DSP]) ou du corps de la publicité ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | URL affichée dans la publicité. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | URL de destination de la publicité. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] et [!DNL Search] data | Indique si l’entrée de la page d’entrée était un affichage publicitaire ou un clic publicitaire. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Cible du produit d’une publicité avec une liste de produits. |

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Données dans Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)

