---
title: Paramètres de publicité vidéo universelle
description: Reportez-vous à la description des paramètres d’annonce disponibles pour les publicités vidéo universelles.
feature: DSP Ads
source-git-commit: 2d344d2ae0438433eb679a5f31f471c2eac4fe26
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Paramètres de publicité vidéo universelle

*Fonctionnalité bêta ouverte*

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
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la variable [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : 30sec Universal Video&quot;).

**[!UICONTROL Show Controls]:** Où inclure des commandes vidéo pour la publicité : *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* ou *[!UICONTROL None]* (valeur par défaut).

**[!UICONTROL Preserve Aspect Ratio]:** Conserver les proportions de largeur et de hauteur de la vidéo (*[!UICONTROL Yes]*) ou pour étirer la vidéo afin de remplir l’espace disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant uniquement des balises VAST ; lecture seule) La balise VAST tierce que vous avez saisie en tant que source de la publicité avec les éléments nécessaires [Macros de suivi Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Wmode]:** Mode fenêtre : *[!UICONTROL window]*, *[!UICONTROL transparent]* ou *[!UICONTROL opaque]*. Si ce paramètre n’est pas applicable, laissez-le vide.

**[!UICONTROL Video Format]:** Le format du lecteur de publicités pour l’inventaire potentiel : *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* ou *[!UICONTROL VAST]*. La visibilité est toujours mesurée pour [!UICONTROL VPAID], mais [!UICONTROL VPAID & VAST] inclut un inventaire qui n’autorise pas la mesure de la visibilité. Tenez compte de cette distinction si les mesures de visibilité sont importantes pour votre campagne.

Utilisation *[!UICONTROL VAST]*, qui n’autorise pas la mesure de la visibilité, lorsque vous ciblez une télévision connectée ou un inventaire nécessitant strictement le format VAST uniquement (provenant généralement de sources d’approvisionnement telles que Google Ad Manager, Appnexus, SpotX et FreeWheeler).

**[!UICONTROL Clock Number]**: (Utilisé uniquement au Royaume-Uni ; disponible uniquement pour les utilisateurs autorisés) Identifiant unique utilisé pour s’assurer que la publicité appropriée est diffusée. Si ce paramètre n’est pas applicable, laissez-le vide.

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
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

