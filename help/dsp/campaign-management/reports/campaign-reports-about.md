---
title: À propos des rapports In-Platform
description: Découvrez les données du rapport incluses dans les vues de gestion de campagne.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 093902d577cc4af3bb18bbeddc640fe284d3a179
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# À propos des rapports In-Platform

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Les vues de gestion de campagne incluent des données de rapport complètes. Les rapports disponibles vous aident à identifier les packages et emplacements performants et ceux qui nécessitent votre attention. Les boutons d’action rapide vous rendent également plus productif.

## Vue Toutes les campagnes

Le [!UICONTROL Campaigns] La vue s’ouvre sur un ensemble de graphiques de données de performances et une liste de toutes les campagnes de votre compte.

### Affichage du graphique {#chart-view}

Vous pouvez [personnaliser les graphiques de tendance des séries temporelles ;](campaign-data-visualization-manage.md) pour toutes les campagnes à l’aide de trois mesures. Par défaut, les données pour [!UICONTROL Net Spend], [!UICONTROL Impressions], et [!UICONTROL Net CPM] sont inclus dans des graphiques distincts (graphiques en courbes). Vous pouvez éventuellement modifier les mesures. Pour activer les données horaires dans les graphiques de tendance de série temporelle, définissez votre sélection de date sur un seul jour ([!UICONTROL Today], [!UICONTROL Yesterday]ou un jour spécifique).

![graphiques de tendances distincts pour trois mesures](/help/dsp/assets/trend-chart-separate.png)

Vous pouvez également, si vous le souhaitez, superposer les trois mesures afin de détecter facilement les anomalies et les domaines dans lesquels améliorer l’échelle ou les performances.

![graphique des tendances avec superposition](/help/dsp/assets/trend-chart.png)

### Vue Tableau

![Liste des campagnes](/help/dsp/assets/campaigns-list.png)

Par défaut, chaque ligne de campagne comprend les mesures de fréquence et de diffusion. Les mesures de fréquence incluent [!UICONTROL Gross Spend (Lifetime)], qui inclut une jauge des dépenses réelles sur cible par rapport aux dépenses prévues sur cible pour tous les modules de la campagne, afin que vous puissiez identifier les campagnes sous-performantes d’un seul coup d’oeil. Vous pouvez [modification du mode Colonnes](column-view-change.md) ou même [création d’un affichage de colonne personnalisé](column-view-create.md).

Vous pouvez également [personnaliser les tableaux de données ;](campaign-data-views-about.md) par d’autres moyens et [filtrer les données visibles](campaign-data-filter.md).

Pour afficher une campagne plus en détail, cliquez sur son nom.

## Reporting de campagne unique {#single-campaign-reporting}

Au sein d’une campagne, vous pouvez filtrer les données en fonction de l’entité de campagne : [!UICONTROL Packages], [!UICONTROL Placements], et [!UICONTROL Ads]. Vous pouvez également [filtrer les données visibles](campaign-data-filter.md) pour inclure uniquement les modules, emplacements ou annonces que vous souhaitez afficher.

![Onglets des entités de Campaign](/help/dsp/assets/campaign-subtabs.png)

### Affichage du graphique

Pour chaque campagne, vous pouvez : [personnaliser les graphiques de tendance des séries temporelles ;](campaign-data-visualization-manage.md) avec trois mesures, disponibles dans chaque vue d’entité. Les mêmes mesures sont conservées dans tous les graphiques de tendance de la campagne.

Voir [Section &quot;Affichage du graphique&quot; sur les mesures entre campagnes](#chart-view) pour plus d’informations.

### Vue Tableau

Dans chaque onglet d’entité, chaque ligne comprend par défaut des mesures de fréquence et de diffusion, mais vous pouvez [modification du mode Colonnes](column-view-change.md) ou même [création d’un affichage de colonne personnalisé](column-view-create.md) pour appliquer à tous les sous-onglets de la campagne. Vous pouvez également [personnaliser les tableaux de données ;](campaign-data-views-about.md) par d’autres moyens. Chaque tableau de données comprend une [!UICONTROL Subtotals] qui affiche soit la somme, soit la valeur moyenne de chaque mesure sur toutes les lignes visibles.

### Emplacement [!UICONTROL Inspector] {#placement-inspector}

Pour chaque emplacement, vous pouvez : [ouvrir une (vue détaillée) [!UICONTROL Inspector])](placement-details-view.md), qui comprend les données détaillées suivantes :

* **[!UICONTROL Sites]:** Tous les sites sur lesquels l’emplacement a eu des impressions.

   Le [!UICONTROL Sites] comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage en colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi qu’un [!UICONTROL Exclude] de chaque ligne afin que vous puissiez exclure rapidement un site de l’emplacement.

* **[!UICONTROL Ads]:** Toutes les publicités de l’emplacement.

   Le [!UICONTROL Ads] comprend les fonctions de recherche et de filtrage, les mêmes options d’affichage en colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi que des boutons d’action rapide dans chaque ligne, tels que [!UICONTROL Pause] (afin que vous puissiez rapidement suspendre une publicité).

* **[!UICONTROL Frequency]:** Données pour chaque niveau de fréquence publicitaire de l’emplacement, notamment :
   * le niveau de fréquence des publicités (par exemple &quot;1&quot; pour toutes les instances où les utilisateurs ont vu une publicité une fois) ;
   * le nombre estimé unique d’appareils/navigateurs ou de personnes (en fonction des [!UICONTROL Cross Device Level] pour la campagne) qui a reçu des impressions au niveau de fréquence spécifié
   * nombre estimé d’impressions au niveau de fréquence spécifié
   * la fréquence moyenne estimée pour le niveau de fréquence spécifié. Cette valeur est égale à (Impressions estimées)/(Uniques estimées).

* **[!UICONTROL Inventory]:** Informations sur toutes les offres ciblées par l’emplacement.

   Le [!UICONTROL Inventory] permet de résoudre rapidement les problèmes en affichant les statistiques de performances, telles que [!UICONTROL Auctions], [!UICONTROL Bids], et [!UICONTROL Win Rate]. L’onglet comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage en colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi que des boutons d’action rapide dans chaque ligne, y compris [!UICONTROL Edit], [!UICONTROL View Report], et [[!UICONTROL Auction Insights] pour résoudre d’autres problèmes](/help/dsp/inventory/private-deal-auction-insights.md).

#### Dépannage de l’inventaire

| Problème | Cause possible | Actions à entreprendre |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L’éditeur n’a pas commencé à envoyer de requêtes d’offre. | Contactez l’éditeur pour activer l’opération. |
|  | L’opération a été mal configurée, par exemple en saisissant un identifiant d’opération externe incorrect. | Confirmez les détails de l’opération et modifiez-la. |
| [!UICONTROL Auctions but no Bids] | Le ciblage de l’emplacement ne correspond pas aux requêtes d’offre entrantes pour l’opération. <br><br> Par exemple, un emplacement peut cibler une zone géographique qui n’est pas éligible à l’opération. | Modifiez les cibles d’emplacement selon les besoins afin d’éviter les non-correspondances de ciblage. |
|  | L’emplacement ne comporte pas de publicité principale avec le type de média requis pour l’opération. | Créez et joignez une publicité avec le type de média approprié à l’emplacement. |
|  | Le placement n&#39;a pas le budget adéquat. | Augmentez le budget d’emplacement afin d’autoriser l’enchère sur les requêtes entrantes. |
|  | Les dates de vol de placement ne chevauchent pas les dates de remise de l’impression pour l’opération. | Modifiez les dates de vol de l’emplacement selon les besoins. |
| [!UICONTROL Low Win Rate] | L’offre maximale de l’emplacement (plancher ou fixe) est inférieure au minimum requis par l’offre. | Augmenter le [!UICONTROL Max Bid] selon les besoins. |
|  | L’emplacement utilise des filtres avant offre qui limitent l’offre. | Réduisez les seuils des filtres pré-enchère pour autoriser plus d’offres. |
|  | Le ciblage de l’audience pour l’emplacement est trop restrictif. | Vérifiez si les cibles d’audience spécifiées disposent de suffisamment d’utilisateurs principaux et développez l’audience si possible. |

![Inspecteur de placement](/help/dsp/assets/placement-inspector.png)

Vous pouvez exporter les données du [!UICONTROL Sites], [!UICONTROL Ads]ou [!UICONTROL Frequency] dans le dossier de téléchargement par défaut de votre navigateur sous la forme d’un rapport au format XLSM.

### Autres types de rapports au niveau des campagnes

Pour d’autres ventilations de données, voir [les pages de création de rapports au niveau de la campagne ;](/help/dsp/campaign-management/campaigns/campaign-view-report.md). Le <!--legacy --> le rapport comprend des sections sur [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], et [!UICONTROL Audience Performance] data.

>[!MORELIKETHIS]
>
>* [Affichage des sites, publicités et détails de fréquence d’un emplacement](placement-details-view.md)
>* [À propos des vues de données de campagne](campaign-data-views-about.md)
>* [Création d’un mode Colonnes personnalisé](column-view-create.md)
>* [Modification du mode Colonnes](column-view-change.md)
>* [Gestion des visualisations des données](campaign-data-visualization-manage.md)
>* [Exportation de données à partir d’une vue Campaign Management](campaign-export-data.md)
>* [Affichage d’un rapport détaillé pour une campagne](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

