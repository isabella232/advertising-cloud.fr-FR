---
title: Gestion de campagne dans Advertising Cloud DSP - Aperçu
description: Découvrez la hiérarchie et les composants de la gestion de campagne.
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gestion de campagne dans Advertising Cloud DSP - Aperçu

Les campagnes Advertising Cloud DSP présentent la hiérarchie suivante :

* Campagne
   * Package(s)
      * Emplacement(s)
         * Publicités
            * Creative(s)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) Les campagnes sont le cadre général des environnements de vol. Chaque campagne est configurée avec un annonceur, des dates de début et de fin, un budget global, une option de ciblage multi-appareils et un plafond de fréquence par défaut, ainsi que des options de reporting pour la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience. Tous les paramètres au niveau de l&#39;opération s&#39;appliquent automatiquement à chaque package et emplacement de l&#39;opération.

## [!UICONTROL Packages]

Chaque campagne peut contenir un ou plusieurs [packages](/help/dsp/campaign-management/packages/package-about.md), dont chacun comprend un ensemble d’emplacements.

Utilisez les packages pour regrouper des emplacements à diffuser selon un budget défini, un objectif de performance et une stratégie de fréquence personnalisée. DSP optimise les packages en transférant les budgets vers les emplacements les plus performants du package. Vous pouvez organiser les packages par format d’emplacement, type de stock, fournisseur de données, persona ou toute autre caractéristique reconnaissable.

Les packages sont facultatifs, mais recommandés.

## [!UICONTROL Placements]

Un [emplacement](/help/dsp/campaign-management/placements/placement-about.md) stocke les paramètres de ciblage pour une ou plusieurs publicités du même type de publicité. Vous pouvez créer un emplacement pour une campagne ou un package unique, puis lui affecter des publicités.

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) Incluez des ressources de création et des URL de suivi. Vous pouvez soit charger vos ressources créatives et DSP diffuseront gratuitement les publicités qui les utilisent, soit charger des balises de diffusion de publicités tierces.

Une fois vos publicités configurées, vous devrez joindre chaque publicité à un emplacement. Vous pouvez joindre une seule publicité à un ou plusieurs emplacements.

Toutes les publicités principales et approuvées d’un emplacement principal dans une principale campagne peuvent être exécutées en fonction des paramètres de ciblage de l’emplacement.

## [!UICONTROL Creatives]

Vous pouvez télécharger des fichiers audio et vidéo à utiliser dans les publicités pour des campagnes spécifiées.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

Vous pouvez immédiatement créer une publicité à l’aide de l’élément créatif chargé ou vous pouvez en créer une ultérieurement à partir de la vue Créatifs ou Publicités.

>[!MORELIKETHIS]
>
>* [Gestion de campagne](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [À propos de la gestion de modules](/help/dsp/campaign-management/packages/package-about.md)
>* [À propos de la gestion des emplacements](/help/dsp/campaign-management/placements/placement-about.md)
>* [A propos de la gestion des publicités](/help/dsp/campaign-management/ads/ad-about.md)
>* [Liste de contrôle de Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [À propos des rapports In-Platform](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [À propos des vues de données de campagne](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

