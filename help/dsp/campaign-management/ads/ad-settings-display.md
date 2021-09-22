---
title: Paramètres d’affichage des publicités
description: Consultez la description des paramètres d’annonce disponibles pour les annonces affichées.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Paramètres d’affichage des publicités

Les paramètres suivants concernent les publicités standard. Vous pouvez également diffuser des publicités vidéo &quot;cliquer pour lire&quot; pour les publicités display, mais nous vous déconseillons de le faire car peu d’éditeurs les prennent en charge.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:**  (lecture seule) type de publicité que vous créez, qui correspond au type de placement auquel la publicité peut être jointe. Par défaut, il est défini sur *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : Gamer 300x250&quot;).

**\[Source de la publicité\]** : Si Advertising Cloud DSP diffuse la publicité (*[!UICONTROL Adobe served]*) ou si vous utilisez un serveur de publicités tiers (*[!UICONTROL 3rd party]*).

**[!UICONTROL This is an expandable Banner]:**  (Publicités tierces uniquement) Indique que la publicité est une bannière publicitaire extensible. Les paramètres d’extension associés déterminent l’inventaire à acheter. Veillez donc à ce qu’ils reflètent le comportement de l’annonce.

**[!UICONTROL Expansion Method]:**  (bannières publicitaires extensibles tierces uniquement) si la bannière se développe sur  *[!UICONTROL Click]* ou  *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:**  (bannières publicitaires extensibles tierces uniquement) Direction dans laquelle la publicité se développe :  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]* ou  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:**  (bannières publicitaires extensibles tierces uniquement) Fournisseur certifié pour lequel la publicité est disponible :  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]* ou  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:**  (annonces tierces uniquement) URL de la ressource créative tierce. Tous les paramètres [timestamp] et [[timestamp]] seront remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:**  (Publicités tierces uniquement) URL de la ressource créative tierce, avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

**[!UICONTROL Creative type]:**  (publicités servies par Adobe uniquement) Indique si la ressource est une  *[!UICONTROL Image]* ressource ou une  *[!UICONTROL HTML5]* ressource.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset] :**  (publicités servies par Adobe uniquement) fichier image ou fichier HTML5 compressé à charger, selon le type de création. Cliquez sur **[!UICONTROL Browse]** et recherchez le fichier sur votre périphérique ou réseau, puis cliquez sur **[!UICONTROL Upload]** ou **[!UICONTROL Upload Image]**.

**[!UICONTROL Ad Size]:** largeur et hauteur de la publicité. Il doit s’agir d’une [taille d’affichage standard prise en charge](/help/dsp/assets/ad-specs.pdf). Vous pouvez saisir manuellement la taille de la publicité avant de la télécharger ou saisir une valeur [!UICONTROL Display Code]. Si vous ne saisissez pas la taille de la publicité, les dimensions de la balise publicitaire ou de publicité chargée sont automatiquement saisies en lecture seule. Notez que la publicité affichée ne sera pas enregistrée si les dimensions ne se trouvent pas dans l’affichage standard sous forme de tailles, par exemple 301x250 au lieu de 300x250.

>[!IMPORTANT]
>
> La taille de l’annonce déclarée dans les champs largeur et hauteur sera mise en correspondance avec les demandes d’offre entrantes. Vous pouvez rencontrer des problèmes de diffusion si les dimensions de l’annonce ne correspondent pas à la taille de l’annonce déclarée.

**[!UICONTROL Click URL]:**  (annonces diffusées par Adobe uniquement) URL à laquelle accède la visionneuse lorsqu’elle clique sur la publicité.

**[!UICONTROL Final Click URL]:**  (publicités servies par Adobe uniquement ; lecture seule) Le  [!UICONTROL Click URL] avec les  [macros de suivi ](/help/dsp/campaign-management/macros.md) Advertising Cloud DSP nécessaires insérées, le cas échéant.

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
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

