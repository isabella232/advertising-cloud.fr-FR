---
title: Paramètres des publicités télévisées connectées
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités télévisées connectées.
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Paramètres des publicités télévisées connectées

## [!UICONTROL Upload or Select Creative]

*Nouvelles publicités uniquement*

**[!UICONTROL Upload Audio]:** pour charger une ressource brute vers DSP. Lorsque vous sélectionnez cette option, procédez comme suit :

1. Cliquez sur **[!UICONTROL Choose File]** et localisez le fichier sur votre appareil ou votre réseau.
1. Saisissez le titre du fichier qui sera utilisé dans la vue [!UICONTROL Ads] et les rapports.
1. Cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** pour sélectionner tout élément créatif précédemment chargé au format correct dans le compte.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Certains types d’annonces) Pour entrer une balise VAST tierce contenant des ressources créatives et des pixels de suivi :

1. Cliquez sur ![flèche](/help/dsp/assets/compressed.png) en regard de **[!UICONTROL Advanced: VAST Tag URL]**.
1. Dans le champ **[!UICONTROL URL]** , saisissez l’URL de la balise VAST.
1. Saisissez **[!UICONTROL Title]** pour le fichier qui sera utilisé dans la vue Publicités et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant `<VAST>` se trouve près du haut.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : CTV 30s&quot;).

**[!UICONTROL Width | Ad Unit Width]:** largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Height | Ad Unit Height]:** hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Player X]:** Coordonnée X de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** Coordonnée Y de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité :  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* ou  *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** indique s’il faut conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL Click URL]:**  (annonces diffusées par Adobe uniquement) URL à laquelle accède la visionneuse lorsqu’elle clique sur la publicité.

**[!UICONTROL Final Click URL]:**  (publicités servies par Adobe uniquement ; lecture seule) Le  [!UICONTROL Click URL] avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL VAST Tag]:**  (publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité.

**[!UICONTROL Final VAST Tag]:**  (publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL Clock Number]**: (Utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la publicité appropriée est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type de publicité, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** si le pixel est un  *[!UICONTROL IMG URL]* (fichier image 1x1 pixel),  *[!UICONTROL HTML]* ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image de pixel, au format approprié pour le type de pixel spécifié.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous aidera à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels :  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* ou  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

