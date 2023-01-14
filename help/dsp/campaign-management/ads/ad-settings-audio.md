---
title: Paramètres de publicité audio
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités audio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Paramètres de publicité audio

## [!UICONTROL Insert Ad Tag]

*Nouvelles publicités uniquement*

**[!UICONTROL URL]**: URL de la balise VAST.

**[!UICONTROL Title]**: Nom du fichier qui sera utilisé dans la variable [!UICONTROL Ads] afficher et générer des rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la variable **[!UICONTROL Enter]** clé. Si la balise est valide, un fichier XML contenant `<VAST>` près du sommet.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type d’emplacement auquel la publicité peut être jointe. Par défaut, la valeur *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la variable [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : Audio 30sec&quot;).

**[!UICONTROL Ad Duration]:** Longueur du fichier audio. Il est automatiquement défini comme [!UICONTROL 15] ou [!UICONTROL 30], selon l’unité publicitaire sélectionnée.

Ce champ peut être affiché ou non, selon les permissions du compte.

**[!UICONTROL VAST Tag]:** (Publicités utilisant uniquement des balises VAST) Une URL pour une source publicitaire tierce. Assurez-vous que la balise VAST comprend uniquement des fichiers de médias audio.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant uniquement des balises VAST) URL de la source publicitaire tierce avec les [Macros de suivi des DSP publicitaires](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Select Rate]:** (Utilisateurs avec autorisation uniquement) Taux négocié à l’avance et facturés par l’intermédiaire de l’Adobe, ou l’un des taux que vous avez négociés et dont la facturation sera effectuée par l’intermédiaire du fournisseur. Pour ajouter un taux, contactez votre [!DNL Adobe] l&#39;équipe du compte.

### Pixel

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction des besoins de suivi pour l’annonce individuelle.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur la variable *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si le pixel est un *[!UICONTROL IMG UR]L* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le type de pixel spécifié.

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aide à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications des publicités](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)

