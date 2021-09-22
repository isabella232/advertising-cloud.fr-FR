---
title: Colonnes dans les feuilles de calcul téléchargées/téléchargées
description: Référencez les colonnes dans les feuilles de calcul AQ Excel téléchargées.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Colonnes dans les feuilles de calcul téléchargées/téléchargées

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> Dans une feuille de calcul téléchargée, toutes les colonnes modifiables sont surlignées en bleu.

| Section | Colonne | Description | Modifiable ? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Identifiant numérique de l’emplacement. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nom de l’emplacement. | Oui |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Toutes les étiquettes appliquées, pour la création de rapports. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Lien permettant d’ouvrir l’emplacement en mode d’édition. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | État de l’emplacement : *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Oui |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Type d’emplacement. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Le nom du package parent, le cas échéant. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Date de début de l’emplacement. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Date de fin de l’emplacement. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Si les tranches horaires sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<br><b>Remarque :</b> Pour vérifier le planning réel des tranches horaires, ouvrez les paramètres d’emplacement dans  [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Le budget de placement, s’il en existe un. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | L’intervalle de budget : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | L’objectif du paquet. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | La valeur cible de l’objectif. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indique si l’emplacement se déplace vers *[!UICONTROL Budget]* ou *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Offre maximale pour l’emplacement. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | Stratégie de remplissage de la plage pour l’emplacement : *[!UICONTROL evenly]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Tout critère de filtrage de pré-enchère à appliquer. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Si les règles d’offre (obsolètes) sont *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Limite de fréquence Principale pour l’emplacement au cours de la balise [!UICONTROL Frequency Cap Interval] spécifiée. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalle de la limite de fréquence Principale : *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Limite de fréquence secondaire de l’emplacement pendant la [!UICONTROL Secondary Frequency Cap Interval] spécifiée | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Type d’intervalle pour la limite de fréquence secondaire : *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. Le nombre applicable de semaines, jours, heures ou minutes est indiqué par la balise [!UICONTROL Secondary Frequency Cap Interval Value]. | Oui |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Le nombre de semaines, de jours, d’heures ou de minutes pour lesquelles la valeur [!UICONTROL Secondary Frequency Cap] s’applique. Par exemple, si la limite secondaire est de trois impressions par six heures, la valeur ici est <b>6&lt;/>. | Oui |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Nombre d’emplacements géographiques ciblés, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Les emplacements géographiques ciblés, séparés par des points-virgules, ou *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Nombre d’emplacements géographiques exclus ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Les emplacements géographiques exclus, séparés par des points-virgules, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | Nombre d’offres d’inventaire public ciblées, le cas échéant, spécifiées, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | Nombre d’offres d’inventaire public exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | Le nombre d’offres d’inventaire privé ciblées, le cas échéant, sont spécifiées, *[!UICONTROL All]* ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | Nombre d’offres d’inventaire privé exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Nombre d’offres [!UICONTROL On-Demand Inventory] ciblées, le cas échéant, *[!UICONTROL All]* ou *[!UICONTROL None]* ciblées. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | Nombre d’offres de stock à la demande exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Le type de trafic ciblé : *[!UICONTROL Website]* et/ou *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Si l’option Ciblage du stock pour exclure le trafic sortant est &lt;i[!UICONTROL >ON]* ou *[!UICONTROL OFF]*.<br>Les publicités sortantes apparaissent généralement au-dessus du contenu sous la forme d’une fenêtre contextuelle ou d’un contenu (dans l’expérience native), plutôt que sous la forme de publicités vidéo standard dans un lecteur vidéo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La qualité des sites à cibler : *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* ou *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | Le nombre de catégories de site ciblées, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | Le nombre de catégories de site exclues, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Les sites exclus, le cas échéant, sont spécifiés ou *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Les langues du site ciblées. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | Permet d’autoriser ou non la diffusion des publicités sur des sites non contrôlés : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | Le nombre de sites ciblés, le cas échéant, est spécifié ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Les audiences ciblées, le cas échéant, sont spécifiées ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Les audiences exclues, le cas échéant, sont spécifiées ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Si les [!DNL Comscore] segments démographiques sont activés pour l’emplacement (et d’autres emplacements dans la campagne) : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*. Cette fonction peut être activée uniquement pour les campagnes pour lesquelles la fonction [!DNL Audience Verification] est activée pour [!DNL Nielson] et/ou [!DNL Comscore].  Il entraîne des frais supplémentaires. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Permet d’étendre ou non le ciblage des publicités sur plusieurs appareils : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Inclus # | Le nombre de codes de rubrique ciblés, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | Nombre de codes de rubrique exclus, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | Nombre de cibles d’appareil ciblées, le cas échéant, ou *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Nombre de cibles d’appareil exclues, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Le nombre de fournisseurs de FAI ciblés, le cas échéant, est spécifié ou *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | Le nombre de fournisseurs de FAI exclus, le cas échéant, est spécifié ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | Nombre de filtres de sécurité de marque appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | Nombre de filtres de blocage de fraude pré-enchère appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | Nombre de filtres de visibilité avant offre appliqués, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Si le bloc de sécurité du site est activé ou non : *[!UICONTROL ON]* ou *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Nombre de pixels de suivi d’événement tiers associés à l’emplacement ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Nombre de pixels de suivi de conversion associés à l’emplacement ou *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Taux de frais tiers statique à suivre en tant que coût non facturable pour mille impressions, le cas échéant. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | Nombre de publicités associées à l’emplacement, le cas échéant, ou *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Les noms des publicités associées à l’emplacement, le cas échéant, sont joints ou *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [À propos de la correction des paramètres de positionnement d’une campagne à l’aide de feuilles de calcul](qa-about.md)
>* [Télécharger les paramètres de positionnement d’une campagne](qa-sheet-download.md)
>* [Télécharger les paramètres de positionnement d’une campagne](qa-sheet-upload.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

