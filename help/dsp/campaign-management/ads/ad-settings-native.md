---
title: Paramètres des publicités natives
description: Consultez la description des paramètres d’annonce disponibles pour les annonces natives.
feature: Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Paramètres des publicités natives

## [!UICONTROL Upload or Select Creative]

*Nouvelles publicités vidéo (mais pas affichées uniquement)*

**[!UICONTROL Upload Audio]:** pour charger une ressource brute vers DSP. Lorsque vous sélectionnez cette option, procédez comme suit :

1. Cliquez sur **[!UICONTROL Choose File]** et localisez le fichier sur votre appareil ou votre réseau.
1. Saisissez le titre du fichier qui sera utilisé dans la vue [!UICONTROL Ads] et les rapports.
1. Cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** pour sélectionner tout élément créatif précédemment chargé au format correct dans le compte.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe.

**[!UICONTROL Ad Name]:** nom de la publicité. Le type de publicité (affichage natif) ou de titre vidéo (formats vidéo) est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : 15sec Native&quot;).

**[!UICONTROL Native Creative]:** image 1 200 x 627 pour optimiser la diffusion sur l’inventaire mobile. Pour les publicités vidéo, il s’agit de l’image affichée avant la lecture de la vidéo native. Cliquez sur **[!UICONTROL Browse]** et recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** titre attrayant qui attirera l’attention des visiteurs.

**[!UICONTROL Description]:** pour les publicités vidéo, il s’agit d’un bref résumé de la publicité. Pour les publicités affichées, il s’agit du corps de la publicité. La longueur maximale est de 100 caractères.

**[!UICONTROL Landing Page]:** URL à laquelle accède la visionneuse lorsqu’elle clique sur la publicité.

**[!UICONTROL Final Landing Page]:**  [!UICONTROL Landing Page] URL contenant les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL Sponsored By (Advertiser Name)]:** annonceur de la publicité.

**[!UICONTROL Call to Action]:**  (Facultatif) Étape que les visiteurs doivent effectuer une fois qu’ils ont vu cette publicité.

**[!UICONTROL Advertiser Logo]:**  (Facultatif) Logo de rapport 1:1 à inclure dans la publicité pour une plus grande reconnaissance de marque. Cliquez sur **[!UICONTROL Browse]** et recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

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
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

