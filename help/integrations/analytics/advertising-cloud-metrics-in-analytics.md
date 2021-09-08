---
title: Mesures Advertising Cloud dans Analysis Workspace
description: Mesures Advertising Cloud dans Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Mesures Advertising Cloud dans Analysis Workspace

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

>[!NOTE]
>
>* Advertising Cloud transmet quotidiennement les mesures et dimensions de trafic à [!DNL Analytics].
>* [!DNL Analytics] capture les clics publicitaires et les affichages publicitaires Advertising Cloud en temps réel.


## Mesures de trafic d’Advertising Cloud

>[!NOTE]
>
>Toutes les mesures de trafic Advertising Cloud dans [!DNL Analytics] commencent par &quot;AMO&quot;.

| Mesure de trafic | Description |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Nombre d’impressions Advertising Cloud. |
| [!UICONTROL AMO Clicks] | Nombre total de clics Advertising Cloud. |
| [!UICONTROL AMO Cost] | Les dépenses Advertising Cloud dans la devise de la suite de rapports. |
| [!UICONTROL AMO ID Instance] | Nombre de fois où l’Advertising Cloud ID est défini. |
| [!UICONTROL AMO Minutes Viewed] | Nombre de minutes pendant lesquelles une vidéo Advertising Cloud a été visionnée. |
| [!UICONTROL AMO Views] | Nombre de vues sur une publicité. Une vue est comptabilisée lorsque la visionneuse lance la vidéo Advertising Cloud. |
| [!UICONTROL AMO Views 25% Complete] | Nombre d’affichages pour lesquels au moins 25 % d’une vidéo Advertising Cloud a été visionnée. |
| [!UICONTROL AMO Views 50% Complete] | Nombre d’affichages pour lesquels au moins 50 % d’une vidéo Advertising Cloud a été visionnée. |
| [!UICONTROL AMO Views 75% Complete] | Nombre d’affichages pour lesquels au moins 75 % d’une vidéo Advertising Cloud a été visionnée. |
| [!UICONTROL AMO Views 100% Complete] | Nombre d’affichages pour lesquels 100 % d’une vidéo Advertising Cloud a été visionnée. |
| [!UICONTROL AMO Viewable Impressions] | Nombre d’impressions qui ont été mesurées pour être visibles en fonction de la configuration de l’emplacement. |
| [!UICONTROL AMO Not Viewable Impressions] | Nombre d’impressions qui n’étaient pas visibles. Cette valeur est calculée comme suit ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Nombre d’impressions diffusées pour lesquelles l’instrumentation de visibilité a été initialisée avec succès. Cette valeur est calculée en tant que (impressions instrumentées : nombre d’impressions non mesurables). |

## Mesures calculées personnalisées utiles pour Advertising Cloud

Pensez à créer les mesures suivantes pour vos données Advertising Cloud.

* Clics jusqu’à l’instance de page d’entrée ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]) : Il s’agit du pourcentage de personnes qui ont cliqué sur la publicité et l’ont affiché sur la page d’entrée.
* Taux mesurable ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Taux d’impression visible ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Coût par affichage ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Coût par clic ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Dimensions Advertising Cloud

>[!NOTE]
>
>Toutes les dimensions Advertising Cloud dans [!DNL Analytics] sont suivies de &quot;(AMO ID)&quot;.

| Dimension | Données Advertising Cloud applicables | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Advertising Cloud DSP ou nom du moteur de recherche |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] et  [!DNL Search] données | Nom du compte. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | RTB ([!DNL DSP]) ou nom du réseau publicitaire ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Nom de la campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Nom du package ([!DNL DSP]) ou du portefeuille ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Nom de l’emplacement. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Nom du groupe publicitaire. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Mot-clé. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Type de correspondance de recherche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Mot-clé et type de correspondance. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Type de publicité, par exemple `text`, `video`, `display` ou `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Type de publicité ([!DNL DSP]) ou titre de publicité ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Description de la publicité ([!DNL DSP]) ou corps de la publicité ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | URL affichée dans la publicité. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | URL de destination de la publicité. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] et  [!DNL Search] données | Indique si l’entrée de la page d’entrée était un affichage publicitaire ou un clic publicitaire. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Cible du produit d’une publicité avec une liste de produits. |

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Données dans Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

