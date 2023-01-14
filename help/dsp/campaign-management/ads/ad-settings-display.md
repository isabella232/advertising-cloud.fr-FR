---
title: Paramètres d’affichage des publicités
description: Consultez la description des paramètres d’annonce disponibles pour les annonces affichées.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Paramètres d’affichage des publicités

Les paramètres suivants concernent les publicités standard.

## [!UICONTROL Ad Options]

### De base

**[!UICONTROL Ad Type]:** (Lecture seule) Type de publicité que vous créez, qui correspond au type d’emplacement auquel la publicité peut être jointe. Par défaut, la valeur *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Nom de la publicité. Le titre de la ressource est utilisé par défaut, mais vous pouvez le modifier.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez la publicité à un emplacement, dans la variable [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que l’aperçu du produit Vacances) : Gamer 300x250&quot;).

**\[Source de publicité\]**: (Lecture seule) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Publicités tierces uniquement) Indique que la publicité est une bannière extensible. Les paramètres d’extension associés déterminent l’inventaire à acheter. Veillez donc à ce qu’ils reflètent le comportement de l’annonce.

**[!UICONTROL Expansion Method]:** (Publicités de bannière extensible tierces uniquement) Indique si la bannière s’étend sur *[!UICONTROL Click]* ou *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Bannières publicitaires extensibles tierces uniquement) La direction dans laquelle la publicité se développe : *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* ou *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Bannières publicitaires extensibles tierces uniquement) Fournisseur certifié pour lequel la publicité est disponible : *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* ou *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Publicités tierces uniquement) URL de la ressource créative tierce. Quelconque [timestamp] et [[timestamp]] seront remplacés par des valeurs réelles.

**[!UICONTROL Final Display Code]:** (Publicités tierces uniquement) URL de la ressource créative tierce, avec les [Macros de suivi des DSP publicitaires](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Ad Size]:** Largeur et hauteur de la publicité. Il doit s’agir d’une [taille d’affichage standard prise en charge](ad-specs.md). Vous pouvez saisir manuellement la taille de la publicité avant de la télécharger ou saisir une [!UICONTROL Display Code]. Si vous ne saisissez pas la taille de la publicité, les dimensions de la balise publicitaire ou de publicité chargée sont automatiquement saisies en lecture seule. Notez que la publicité affichée ne sera pas enregistrée si les dimensions ne se trouvent pas dans l’affichage standard sous forme de tailles, par exemple 301x250 au lieu de 300x250.

>[!IMPORTANT]
>
> La taille de l’annonce déclarée dans les champs largeur et hauteur sera mise en correspondance avec les demandes d’offre entrantes. Vous pouvez rencontrer des problèmes de diffusion si les dimensions de l’annonce ne correspondent pas à la taille de l’annonce déclarée.

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
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Spécifications des publicités](ad-specs.md)
>* [Macros DSP](/help/dsp/campaign-management/macros.md)

