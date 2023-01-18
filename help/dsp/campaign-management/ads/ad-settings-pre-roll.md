---
title: Paramètres de publicité preroll
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités preroll.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Paramètres de publicité preroll

## [!UICONTROL Insert Ad Tag]

*Nouvelles publicités uniquement*

**[!UICONTROL URL]:** URL de la balise VAST.

**[!UICONTROL Title]:** Titre du fichier, qui se trouve dans la propriété [!UICONTROL Ads] afficher et générer des rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la variable **[!UICONTROL Enter]** clé. Si la balise est valide, un fichier XML contenant `<VAST>` près du sommet.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type d’emplacement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la variable [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : 30sec Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Publicités preroll standard et pouvant être ignorées uniquement) Largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Publicités preroll standard et pouvant être ignorées uniquement) Hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

**[!UICONTROL Player X]:** Coordonnée X de l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Y]:** Coordonnée Y pour l’unité publicitaire. Conservez le paramètre par défaut.

**[!UICONTROL Player Width]:** Largeur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Ce champ est identique au champ **[!UICONTROL Width]** champ .

**[!UICONTROL Player Height]:** Hauteur de l’unité publicitaire entière. Cette option peut être verrouillée selon le type d’unité publicitaire sélectionné.

Il s’agit de la même chose que la variable **[!UICONTROL Height]** champ .

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou pour étirer la vidéo afin de remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité avec les éléments nécessaires [Macros de suivi des DSP publicitaires](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Wmode]:** (Pré-roll interactif uniquement) Mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Pré-roll interactif uniquement) Format du lecteur publicitaire pour l’inventaire potentiel : *[!UICONTROL VPAID]* ou *[!UICONTROL VPAID & VAST]*. La visibilité est toujours mesurée pour VPAID, mais VPAID &amp; VAST comprend un inventaire qui ne permet pas la mesure de la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

**[!UICONTROL Clock Number]**: (preroll interactif uniquement) ; utilisé uniquement au Royaume-Uni; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la publicité appropriée est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

### [!UICONTROL Pixel]

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur la variable *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** L’URL de l’image en pixels, au format approprié pour la variable [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications des publicités](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)

