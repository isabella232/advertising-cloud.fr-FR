---
title: Paramètres de publicité preroll
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités preroll.
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Paramètres de publicité preroll

## [!UICONTROL Upload or Select Creative]

*Nouvelles publicités uniquement*

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

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : 30sec Preroll&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width] :**  (Publicités preroll standard et pouvant être ignorées uniquement) Largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height] :**  (Publicités preroll standard et pouvant être ignorées uniquement) Hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

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

**[!UICONTROL Wmode]:**  (preroll interactif uniquement) Mode fenêtre :  *[!UICONTROL window]*,  *[!UICONTROL transparent]* ou  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:**  (preroll interactif uniquement) Format du lecteur publicitaire pour l’inventaire potentiel :  *[!UICONTROL VPAID]* ou  *[!UICONTROL VPAID & VAST]*. La visibilité est toujours mesurée pour VPAID, mais VPAID &amp; VAST comprend un inventaire qui ne permet pas la mesure de la visibilité. Gardez cela à l’esprit si les mesures de visibilité sont importantes pour votre campagne.

**[!UICONTROL Clock Number]**: (preroll interactif uniquement) ; utilisé uniquement au Royaume-Uni; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la publicité appropriée est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Companion]

*Publicités DSP uniquement*

Vous pouvez éventuellement joindre jusqu’à trois bannières d’accompagnement à une publicité. La bonne pratique consiste à joindre des bannières d’accompagnement, si possible.

>[!NOTE]
>
> Les éditeurs n’autorisent pas tous les bannières d’entreprise. Les éditeurs qui autorisent les bannières compagnons ne garantissent pas les impressions de bannières compagnons.
> Les bannières d’accompagnement issues de balises publicitaires tierces peuvent ne pas toujours être disponibles pour la prévisualisation.

**\[Case à cocher\] :** inclut la bannière compagnon spécifiée avec la publicité. Si la case est désactivée, la bannière compagnon n’est pas incluse.

**\[Banner Size\] :**  taille de bannière compagnon :  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*, qui est la taille de publicité la plus courante et recommandée pour toutes les publicités ;  *[!UICONTROL 300x60 (Small Banner)]*; ou  *[!UICONTROL 728x90 (Leaderboard)]*, qui est une taille d’annonce moins commune.

**\[Source\] :**  si vous téléchargez votre propre ressource de bannière d’accompagnement ou à l’aide d’une balise tierce.

**Ressource :**  (ressources brutes uniquement) ressource de bannière compagnon. Cliquez sur **[!UICONTROL Browse]** et recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

**Balise publicitaire]:[!UICONTROL ** (Publicités utilisant des balises VAST uniquement) Une URL vers une source de bannière compagnon tierce.

**[!UICONTROL Final Ad Tag]:**  (Publicités utilisant uniquement des balises VAST) URL d’une source source de bannière compagnon tierce avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

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

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** événement qui déclenche le déclenchement du pixel. Pour ce type de publicité, utilisez des pixels qui se déclenchent sur *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** si le pixel est un  *[!UICONTROL IMG URL]* (fichier image 1x1 pixel),  *[!UICONTROL HTML]* ou  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour la  [!UICONTROL Pixel Type]valeur spécifiée.

**[!UICONTROL Pixel Name]:** nom du pixel. Utilisez un nom qui vous aidera à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** fournisseur de pixels :  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* ou  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Bonnes pratiques pour la conception de superpositions](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

