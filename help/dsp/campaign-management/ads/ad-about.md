---
title: À propos de la gestion des publicités dans Advertising Cloud DSP
description: En savoir plus sur la gestion des publicités.
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# À propos de la gestion des publicités dans Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP offre deux façons de diffuser vos publicités :

* Advertising Cloud DSP diffusera vos publicités gratuitement lorsque vous chargez vos propres ressources (telles que les bannières d’affichage, les ressources vidéo, les fichiers audio ou les URL) directement vers DSP. Pour les ressources DSP diffusées, vous avez accès à des fonctionnalités supplémentaires, telles que des superpositions.

* Si vous utilisez un serveur de publicités tiers (Google, Flashtalking ou Sizmek, par exemple), vous pouvez charger vos balises de diffusion de publicités tierces sur DSP individuellement ou en bloc. La fonction de chargement en masse requiert que vous ayez : a) téléchargé des feuilles de balises DoubleClick et Flashtalking ou b) téléchargé un modèle, saisi vos balises dans le modèle, puis chargé à nouveau le modèle.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Une fois vos publicités configurées, vous devrez joindre chaque publicité à un emplacement, qui inclut les paramètres de ciblage (tels que la géographie, l’audience, le périphérique et le ciblage d’inventaire) qui contrôleront la manière dont votre campagne sera diffusée. Vous pouvez joindre une publicité à un ou plusieurs emplacements.

## Types de publicité disponibles

* Audio
* Télévision connectée
* Affichage
* Mobile
* Native
* Pre-Roll

Pour plus d’informations sur ces types d’annonces, voir [Types d’annonces disponibles](ad-types.md) et [Spécifications d’annonces](/help/dsp/assets/ad-specs.pdf) complètes.

## Fonctionnalités publicitaires spéciales

Les fonctionnalités suivantes sont disponibles uniquement pour les publicités DSP.

### Bannières d’accompagnement

Les bannières d’accompagnement sont diffusées avec les [publicités preroll](ad-settings-pre-roll.md) ou (avec certains éditeurs) [publicités audio](ad-settings-audio.md) et peuvent contribuer à renforcer l’association entre les marques et les messages.

>[!NOTE]
>
>* Les éditeurs n’autorisent pas tous les bannières d’entreprise. Les éditeurs qui autorisent les bannières compagnons ne garantissent pas les impressions de bannières compagnons.
>* Les bannières d’accompagnement issues de balises publicitaires tierces peuvent ne pas toujours être disponibles pour la prévisualisation.


Vous pouvez charger votre propre ressource de bannière d’accompagnement ou charger une balise d’iFrame ou de bannière de script tierce à partir d’un partenaire de service d’annonces tiers certifié.

### Recouvrements

Les superpositions permettent d’appliquer une valorisation de marque persistante à toute la vidéo et peuvent générer des clics supplémentaires. La fonction de superposition est disponible pour les [publicités preroll interactives](ad-settings-pre-roll.md) et pour les [publicités mobiles dans des formats interactifs et d’appui-lecture](ad-settings-mobile.md).

Voir [Bonnes pratiques pour la conception de superpositions](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Teasers

Un teaser est une image accrocheuse qui permet à la visionneuse de lire une publicité. Les teasers s’appliquent uniquement aux formats d’annonce de type &quot;appuyer pour lire&quot; mobile.

## Approbations publicitaires Advertising Cloud DSP

Lorsque vous créez une publicité, Advertising Cloud DSP la examine pour les catégories sensibles, cliquez sur la fonctionnalité URL et prévisualisez le rendu.

Au départ, un point rouge s’affiche dans la colonne [!UICONTROL Status]. Le processus de révision prend normalement 24 à 48 heures. Cependant, une publicité interrompue peut avoir un état en attente pendant plus de 48 heures, vous avez donc le temps de corriger les erreurs avant le rejet de la publicité. Les publicités refusées incluent une raison de rejet.

Lorsque DSP approuve une publicité, un point vert s’affiche dans la colonne État.

![Indicateur de validation en  [!UICONTROL Status] colonne](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Votre publicité ne sera diffusée que si DSP et le SSP ont tous deux approuvé le contenu créatif. Chaque SSP possède ses propres exigences et processus d’approbation.

>[!MORELIKETHIS]
>
>* [Créer une publicité](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-third-party.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)

