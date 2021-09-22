---
title: Paramètres des publicités mobiles
description: Consultez la description des paramètres d’annonce disponibles pour les annonces mobiles.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Paramètres des publicités mobiles

## [!UICONTROL Upload or Select Creative]

*Nouveaux formats de publicités vidéo mobiles uniquement*

**[!UICONTROL Vertical video]:**  (Non disponible lorsque  [!UICONTROL Custom Transcode] est sélectionné) Indique que la vidéo est verticale (mode portrait).

**[!UICONTROL Transcode to]:**  (certains utilisateurs, selon les autorisations) ; (facultatif) Formats que vous souhaitez inclure dans votre balise VAST lorsque l’éditeur a des exigences de fichier créatif spécifiques. Les formats acceptés par la plupart des éditeurs sont sélectionnés par défaut.

**[!UICONTROL Custom Transcode]:**  (utilisateurs bêta uniquement) ; non disponible lorsque la vidéo verticale est sélectionnée) ) Indique que la vidéo utilise un transcodage personnalisé. Si vous sélectionnez cette option, spécifiez le format de fichier, le débit vidéo, le zoom et les dimensions pour trois versions de transcodage personnalisées au maximum.

**[!UICONTROL XTrader]:**  (Certains utilisateurs, selon les autorisations) Indique que la vidéo utilise un ou plusieurs  [!DNL X_TRADER] flux.

**[!UICONTROL Upload Video]:** pour charger une ressource brute vers DSP. Lorsque vous sélectionnez cette option, procédez comme suit :

1. Cliquez sur **[!UICONTROL Choose File]** et localisez le fichier sur votre appareil ou votre réseau.
1. Saisissez le titre du fichier qui sera utilisé dans la vue [!UICONTROL Ads] et les rapports.
1. Cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** pour sélectionner tout élément créatif précédemment chargé au format correct dans le compte.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Certains types d’annonces) Pour entrer une balise VAST tierce contenant des ressources créatives et des pixels de suivi :

1. Cliquez sur ![flèche](/help/dsp/assets/compressed.png) en regard de **[!UICONTROL Advanced: VAST Tag URL]**.
1. Dans le champ **[!UICONTROL URL]** , saisissez l’URL de la balise VAST.
1. Saisissez **[!UICONTROL Title]** pour le fichier qui sera utilisé dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant `<VAST>` se trouve près du haut.

**[!UICONTROL Advanced: 3rd party Ad Tag]:**  (Certains types d’annonces) Pour entrer une balise d’annonce tierce contenant des ressources créatives et des pixels de suivi :

1. Cliquez sur ![flèche](/help/dsp/assets/compressed.png) en regard de **[!UICONTROL Advanced: #3rd party Ad Tag]**.
1. Saisissez **[!UICONTROL Ad Title]** pour le fichier qui sera utilisé dans la vue [!UICONTROL Ads] et les rapports.
1. Dans le champ **[!UICONTROL Ad Tag]** , saisissez la balise publicitaire.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Publicités d’affichage mobiles

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue Publicités et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : Gamer 300x250&quot;).

**\[Source de la publicité\]** : Si Advertising Cloud DSP diffuse la publicité (*[!UICONTROL Adobe served]*) ou si vous utilisez un serveur de publicités tiers (*[!UICONTROL 3rd party]*).

**[!UICONTROL Creative type]:**  (publicités servies par Adobe uniquement) Indique si la ressource est une  *[!UICONTROL Image]* ressource ou une  *[!UICONTROL HTML5]* ressource.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset] :**  (publicités servies par Adobe uniquement) fichier image ou fichier HTML5 compressé à charger, selon le type de création. Cliquez sur **[!UICONTROL Browse]** et recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:**  (annonces diffusées par Adobe uniquement) URL à laquelle accède la visionneuse lorsqu’elle clique sur la publicité.

**[!UICONTROL Final Click URL]:**  (publicités servies par Adobe uniquement ; lecture seule) L’URL de clic avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL Display Code]:**  (annonces tierces uniquement) URL de la ressource créative tierce. Tous les paramètres [timestamp] et [[timestamp]] seront remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:**  (Publicités tierces uniquement) URL de la ressource créative tierce, avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

### [!UICONTROL Basic]: Publicités vidéo

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue Publicités et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : 30sec Phone Preroll&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width] :** largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height] :** hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Player X]:** Coordonnée X de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** Coordonnée Y de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Il s’agit du même champ que le champ **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité :  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* ou  *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** indique s’il faut conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou étirer la vidéo pour remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:**  (Certains types d’annonces). Nombre de secondes nécessaires pour retarder l’affichage du bouton de fermeture.

**[!UICONTROL Click URL]:**  (annonces diffusées par Adobe uniquement) URL à laquelle accède la visionneuse lorsqu’elle clique sur la publicité.

**[!UICONTROL Final Click URL]:**  (publicités servies par Adobe uniquement ; lecture seule) Le  [!UICONTROL Click URL] avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL VAST Tag]:**  (publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que ressource créative.

**[!UICONTROL Final VAST Tag]:**  (publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que ressource créative avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL Wmode]:**  (Certains types d’annonces) Mode fenêtre :  *[!UICONTROL window]*,  *[!UICONTROL transparent]* ou  *[!UICONTROL opaque]*.

### [!UICONTROL Teaser]

*Formats de pression pour la lecture mobile pour les publicités DSP servies*

**[!UICONTROL Asset]:** l’image de teaser ou la ressource vidéo :

* Pour sélectionner votre propre image, cliquez sur **[!UICONTROL Choose File],** localisez le fichier sur votre appareil ou votre réseau, puis cliquez sur **[!UICONTROL Upload Image]**.

   Il est recommandé d’utiliser une image avec les mêmes dimensions que l’unité publicitaire.

* Pour sélectionner une image du contenu créatif, cliquez sur **[!UICONTROL Choose Thumbnail]**.

Conditions requises pour les teasers d’image statiques :

* Format : GIF, JPEG, PNG
* Taille de l’image : 300x250
* Taille de fichier : 50 Ko ou moins
* Recommandé : appel à l’action, image reconnaissable, logo de marque

Conditions requises pour les teasers vidéo :

* Type de fichier : MOV, MP4
* Taille de fichier : Moins de 2 Mo
* Durée : 7-10sec
* Recommandé : images reconnaissables, visages, raccourcis

### [!UICONTROL Overlays]

*Formats interactifs preroll et interactifs mobiles et d’appui-lecture pour les publicités DSP diffusées*

Les paramètres suivants s’appliquent à chaque superposition que vous créez ou modifiez.

**[!UICONTROL Asset]:**  (ressources brutes uniquement) ressource image de recouvrement. Le fichier doit être au format GIF, JPG ou PNG à une seule image et la taille maximale de l’image doit être inférieure à 2 Mo. Pour charger la ressource, cliquez sur **[!UICONTROL Browse]**, recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

>[!TIP]
>
>Voir [Bonnes pratiques pour la conception de superpositions](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  URL à laquelle accède la visionneuse lorsqu’elle clique sur une superposition pour votre publicité.

**[!UICONTROL X]:** coordonnée X pour la superposition. Sélectionnez la position de départ de la superposition, puis saisissez le nombre de pixels à partir de la position de départ (par exemple 10 px de centre). La bonne pratique consiste à utiliser *du centre*, ce qui empêche la superposition de se déplacer avec différentes tailles de lecteur sur les sites de publication.

**[!UICONTROL Y]:** coordonnée Y pour la superposition. Sélectionnez la position de départ de la superposition, puis saisissez le nombre de pixels à partir de la position de départ (par exemple, 10 px en haut). La bonne pratique consiste à spécifier une coordonnée *[!UICONTROL From Bottom]* ou *[!UICONTROL From Top],* selon la position à laquelle vous souhaitez que la superposition s’affiche sur la publicité.

**[!UICONTROL Layer]:** calque dans lequel la superposition apparaîtra. La vidéo et chaque superposition se trouvent dans des calques distincts.

* *[!UICONTROL 2 through 5]:* devant la vidéo mais derrière d’autres superpositions.

* *[!UICONTROL 1]:*  devant la vidéo.

* *[!UICONTROL 0]:* dans le même calque que la vidéo. La vidéo se rétrécit pour remplir l’espace restant. Non recommandé pour le défilement interactif.

* *[!UICONTROL -1]:* Derrière la vidéo.

* *[!UICONTROL -2 through -5]:* Derrière la vidéo mais devant d’autres superpositions.

* *[!UICONTROL Background]:* Derrière la vidéo et les autres superpositions. La superposition s’adapte à la largeur et à la hauteur complètes de la vidéo, et les proportions ne sont pas conservées.

### [!UICONTROL Endcap]

Obsolète

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type de publicité, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** si le pixel est un  *[!UICONTROL IMG URL]* (fichier image 1x1 pixel),  *[!UICONTROL HTML]* ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour la  [!UICONTROL Pixel Type]valeur spécifiée.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous aidera à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels :  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* ou  *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsolète

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Bonnes pratiques pour la conception de superpositions](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

