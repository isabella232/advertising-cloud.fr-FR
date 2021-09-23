---
title: À propos des rapports In-Platform
description: Découvrez les données du rapport incluses dans les vues de gestion de campagne.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: df462aac1da30c1ebe9e1bb8afd8546d79432fde
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# À propos des rapports In-Platform

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Les vues de gestion de campagne incluent des données de rapport complètes. Les rapports disponibles vous aident à identifier les packages et emplacements performants et ceux qui nécessitent votre attention. Les boutons d’action rapide vous rendent également plus productif.

## Liste de toutes les campagnes

La vue [!UICONTROL Campaigns] s’ouvre sur une liste de toutes les campagnes de votre compte. La ligne [!UICONTROL Subtotals] indique la somme ou la valeur moyenne de chaque mesure sur toutes les lignes visibles.

![Liste des campagnes](/help/dsp/assets/campaigns-list.png)

Par défaut, chaque ligne de campagne comprend les mesures de fréquence et de diffusion. Les mesures de rythme incluent [!UICONTROL Gross Spend (Lifetime)], qui inclut une jauge des dépenses réelles sur la cible par rapport aux dépenses prévues sur la cible pour tous les modules de la campagne, afin que vous puissiez identifier les campagnes sous-performantes d’un seul coup d’oeil. Vous pouvez éventuellement [modifier le mode Colonne](column-view-change.md) ou même [créer un mode Colonne personnalisé](column-view-create.md).

Vous pouvez également [personnaliser les tableaux de données](campaign-data-views-about.md) de manière supplémentaire et [filtrer les données visibles](campaign-data-filter.md).

Pour afficher une campagne plus en détail, cliquez sur son nom.

## Reporting de campagne unique

Au sein d’une campagne, vous pouvez filtrer les données en fonction de l’entité de campagne : [!UICONTROL Packages], [!UICONTROL Placements] et [!UICONTROL Ads]. Vous pouvez également [filtrer les données visibles](campaign-data-filter.md) afin d’inclure uniquement les modules, emplacements ou annonces que vous souhaitez voir.

![Onglets des entités de Campaign](/help/dsp/assets/campaign-subtabs.png)

Dans chaque onglet d’entité, chaque ligne comprend des mesures de fréquence et de diffusion, par défaut, mais vous pouvez [modifier le mode Colonne](column-view-change.md) ou même [créer un mode Colonne personnalisé](column-view-create.md) à appliquer à tous les sous-onglets de la campagne. Vous pouvez également [personnaliser les tableaux de données](campaign-data-views-about.md) de différentes manières. Chaque tableau de données comprend une ligne [!UICONTROL Subtotals], qui indique la somme ou la valeur moyenne de chaque mesure sur toutes les lignes visibles.

Pour chaque campagne, vous pouvez également personnaliser les graphiques de tendance de série temporelle avec trois mesures, disponibles dans chaque vue d’entité. Par défaut, les données de [!UICONTROL Net Spend], [!UICONTROL Impressions] et [!UICONTROL Net CPM] sont incluses dans des graphiques distincts (graphiques en courbes). Vous pouvez éventuellement modifier les mesures.

![graphiques de tendances distincts pour trois mesures](/help/dsp/assets/trend-chart-separate.png)

Vous pouvez également, si vous le souhaitez, superposer les trois mesures afin de détecter facilement les anomalies et les domaines dans lesquels améliorer l’échelle ou les performances.

![graphique des tendances avec superposition](/help/dsp/assets/trend-chart.png)

Vous pouvez [personnaliser les graphiques de tendances](campaign-data-visualization-manage.md) par campagne, et les mêmes mesures sont conservées dans tous les graphiques de tendances de la campagne.

### Inspecteur de placement

Pour chaque emplacement, vous pouvez [ouvrir une (vue détaillée [!UICONTROL Inspector])](placement-details-view.md), qui inclut les données détaillées suivantes :

* **[!UICONTROL Sites]:** tous les sites sur lesquels l’emplacement a eu des impressions.

   L’onglet [!UICONTROL Sites] comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage en colonnes standard et personnalisées disponibles sur la page principale, ainsi qu’un bouton [!UICONTROL Exclude] dans chaque ligne afin que vous puissiez rapidement exclure un site de l’emplacement.

* **[!UICONTROL Ads]:** toutes les publicités de l’emplacement.

   L’onglet [!UICONTROL Ads] comprend des fonctions de recherche et de filtrage, les mêmes options standard et personnalisées d’affichage des colonnes disponibles sur la page principale et des boutons d’action rapide dans chaque ligne, tels que [!UICONTROL Pause] (afin que vous puissiez rapidement suspendre une publicité).

* **[!UICONTROL Frequency]:** données pour chaque niveau de fréquence des publicités pour l’emplacement, notamment :
   * le niveau de fréquence des publicités (par exemple &quot;1&quot; pour toutes les instances où les utilisateurs ont vu une publicité une fois) ;
   * le nombre unique estimé d’appareils/navigateurs ou de personnes (selon la valeur [!UICONTROL Cross Device Level] spécifiée pour l’emplacement) qui ont reçu des impressions au niveau de fréquence spécifié.
   * nombre estimé d’impressions au niveau de fréquence spécifié
   * la fréquence moyenne estimée pour le niveau de fréquence spécifié. Cette valeur est égale à (Impressions estimées)/(Uniques estimées).

![Inspecteur de placement](/help/dsp/assets/placement-inspector-sites.png)

Vous pouvez exporter les données de l’onglet [!UICONTROL Sites], [!UICONTROL Ads] ou [!UICONTROL Frequency] vers le dossier de téléchargement par défaut de votre navigateur sous la forme d’un rapport au format XLSM.

### Autres types de rapports au niveau des campagnes

Pour d’autres ventilations de données, consultez [les pages de création de rapports au niveau de la campagne héritées](/help/dsp/campaign-management/campaigns/campaign-view-report.md) à partir de [!UICONTROL Campaigns Classic]. Le rapport hérité comprend des sections sur les données [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] et [!UICONTROL Audience Performance].

>[!MORELIKETHIS]
>
>* [Affichage des sites, publicités et détails de fréquence d’un emplacement](placement-details-view.md)
>* [À propos des vues de données de campagne](campaign-data-views-about.md)
>* [Création d’un mode Colonnes personnalisé](column-view-create.md)
>* [Modification du mode Colonnes](column-view-change.md)
>* [Gestion des visualisations des données](campaign-data-visualization-manage.md)
>* [Exporter des données à partir d’une vue de gestion de campagne](campaign-export-data.md)
>* [Affichage d’un rapport détaillé pour une campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

