---
title: À propos de la gestion des publicités dans Advertising Cloud DSP
description: En savoir plus sur la gestion des publicités.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: ff0e153344f8245ff217cc8b2b276184dd7422b5
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# À propos de la gestion des publicités dans Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP prend en charge la diffusion de publicités par le biais de balises de service de publicités tierces (telles que Google, Flashtalking ou Sizmek) pour divers types d’annonces et le chargement direct de ressources pour les annonces d’affichage natives. Vous pouvez charger des balises tierces individuellement ou par lot. Les téléchargements en masse utilisent des feuilles de balises partenaires ou un modèle de balise en bloc.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Une fois vos publicités configurées, vous devrez joindre chaque publicité à un emplacement, qui inclut les paramètres de ciblage (tels que la géographie, l’audience, le périphérique et le ciblage d’inventaire) qui contrôleront la manière dont votre campagne sera diffusée. Vous pouvez joindre une publicité à un ou plusieurs emplacements.

## Types de publicité disponibles {#ad-types}

Tous les types d’annonces suivants sont disponibles dans Advertising Cloud DSP. Pour obtenir des spécifications complètes de chaque type d’annonce, reportez-vous à la section [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf).

* **Publicités audio (tierces uniquement)**: Les publicités audio sont lues entre le contenu des sites d’éditeurs numériques et peuvent être exécutées de manière autonome sous la forme de fichiers audio ou avec des bannières d’accompagnement. L’audio est le meilleur moyen d’accroître la notoriété de la marque et d’interagir avec les publics en ligne. Indicateurs de performance clés pour l’inclusion audio [!UICONTROL Completion Rate] et [!UICONTROL Cost per Completion].

* **Publicités affichées (tierces uniquement)**: Les publicités affichées sont des images animées ou statiques affichées dans les navigateurs web ou dans les applications. En cliquant sur l’unité publicitaire, l’utilisateur accède à un site ou à un microsite de marque. L’affichage est le meilleur outil utilisé pour générer des CPM efficaces, augmenter l’association des messages, ajouter des points de contact de marque ou de produit supplémentaires et faire descendre les utilisateurs dans l’entonnoir d’achat. Les indicateurs de performance clés pour l’affichage incluent [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions], et [!UICONTROL Cost per Conversion]. DSP prend en charge un large éventail de tailles de bannières publicitaires.

* **Mobile Ads (tiers uniquement)**: Les publicités Mobile peuvent être au format vidéo preroll (VAST, MRAID) ou d’affichage standard. La vidéo preroll de Mobile peut être lue automatiquement ou cliquer pour être lue. Elle est préférable pour atteindre les visionneuses sur plusieurs écrans. L’affichage standard de Mobile est une image statique affichée sur les navigateurs web mobiles ou dans les applications. Il est préférable de l’utiliser pour compléter les achats de vidéos numériques, générer l’association des messages et ajouter des points de contact de marque ou de produit supplémentaires. Les publicités Mobile peuvent également fonctionner comme des prises de vue en plein écran ou comme des spots mobiles, qui sont des publicités mobiles à fort impact en plein écran et qui sont les mieux utilisées pour développer la notoriété de la marque pour les audiences mobiles et générer des conversions.

* **Publicités d’affichage natives (propriétaires uniquement)**: Les publicités natives sont prises en charge dans un format d’affichage standard. Les annonces natives incluent un titre et/ou un titre, une description, un logo et une image. Les éléments d’annonce sont combinés et rendus pour correspondre au style de page de l’éditeur afin que l’annonce se fonde avec le contenu organique de l’éditeur et entraîne un engagement plus important. L’option native est la mieux utilisée pour la sensibilisation à la marque et pour stimuler les taux d’affichage et d’engagement des audiences grâce à la publicité conviviale destinée aux visiteurs. Les indicateurs clés de performance incluent : [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions], et [!UICONTROL Cost Per Conversion].

* **Publicités preroll (tiers uniquement)**: Les publicités preroll (VAST et VPAID) sont affichées avant le contenu vidéo Premium et offrent une expérience de visionneuse immersive et attrayante. La vidéo preroll peut être interactive, contenir des fonctions multimédias enrichies et inclure des superpositions, des roulements et des appels à l’action. Les indicateurs de performances clés des publicités vidéo preroll incluent : [!UICONTROL Video Completion Rate] et [!UICONTROL Viewability Rate].

* **Publicités TV connectées (tiers uniquement)**: Les publicités télévisées connectées sont affichées avant et pendant le contenu vidéo de la télévision de qualité supérieure. L’inventaire de toutes les télévisions connectées s’exécute sur les appareils télévisés, ce qui signifie que la vidéo est lue automatiquement dans un environnement en arrière-plan plein écran que les téléspectateurs ne peuvent pas ignorer. La télévision connectée est le format vidéo numérique le plus proche des publicités télévisées. Les indicateurs de performances clés de la télévision connectée incluent : [!UICONTROL Completion Rate].

## Approbations publicitaires Advertising Cloud DSP

Lorsque vous créez une publicité, Advertising Cloud DSP la examine pour les catégories sensibles, cliquez sur la fonctionnalité URL et prévisualisez le rendu.

Au départ, un point rouge apparaît dans la variable [!UICONTROL Status] colonne . Le processus de révision prend normalement 24 à 48 heures. Cependant, une publicité interrompue peut avoir un état en attente pendant plus de 48 heures, vous avez donc le temps de corriger les erreurs avant le rejet de la publicité. Les publicités refusées incluent une raison de rejet.

Lorsque DSP approuve une publicité, un point vert s’affiche dans la colonne État.

![indicateur de validation dans [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Votre publicité ne sera diffusée que si DSP et le SSP ont tous deux approuvé le contenu créatif. Chaque SSP possède ses propres exigences et processus d’approbation.

>[!MORELIKETHIS]
>
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-multiple.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)

