---
title: Paramètres de publicité audio
description: Reportez-vous à la description des paramètres de publicité disponibles pour les publicités audio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Paramètres de publicité audio

## [!UICONTROL Upload or Select Creative]

*Nouvelles publicités uniquement*

**[!UICONTROL Upload Audio]:** Pour charger une ressource brute vers DSP. Lorsque vous sélectionnez cette option, procédez comme suit :

1. Cliquez sur **[!UICONTROL Choose File]** et localisez le fichier sur votre appareil ou votre réseau.
1. Saisissez un titre pour le fichier qui sera utilisé dans le champ [!UICONTROL Ads] afficher et générer des rapports.
1. Cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Pour sélectionner tout élément créatif précédemment chargé au format correct dans le compte.

**[!UICONTROL Advanced: VAST Tag URL]:** Pour entrer une balise VAST tierce contenant des ressources créatives et des pixels de suivi :

1. Cliquez sur ![flèche](/help/dsp/assets/compressed.png) en regard de **[!UICONTROL Advanced: VAST Tag URL]**.
1. Dans le **[!UICONTROL URL]** , saisissez l’URL de la balise VAST.
1. Saisissez un **[!UICONTROL Title]** pour le fichier , qui sera utilisé dans la variable [!UICONTROL Ads] afficher et générer des rapports.

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

**[!UICONTROL Click URL]:** (Publicités utilisant des ressources brutes et avec des bannières d’affichage uniquement) ; (facultatif) URL à laquelle accède la visionneuse lorsqu’elle clique sur une bannière d’affichage accompagnant votre publicité.

**[!UICONTROL Final Click URL]:** (Publicités utilisant des ressources brutes et avec des bannières d’affichage uniquement) ; lecture seule) La variable [!UICONTROL Click URL] avec les [Macros de suivi Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL VAST Tag]:** (Publicités utilisant uniquement des balises VAST) Une URL pour une source publicitaire tierce. Assurez-vous que la balise VAST comprend uniquement des fichiers de médias audio.

**[!UICONTROL Final VAST Tag]:** (Publicités utilisant uniquement des balises VAST) URL de la source publicitaire tierce avec les [Macros de suivi Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Select Rate]:** (Utilisateurs avec autorisation uniquement) Taux négocié à l’avance et facturés par l’intermédiaire de l’Adobe, ou l’un des taux que vous avez négociés et dont la facturation sera effectuée par l’intermédiaire du fournisseur. Pour ajouter un taux, contactez votre [!DNL Adobe] gestionnaire de compte.

### [!UICONTROL Companion]

*Publicités DSP uniquement*

Vous pouvez éventuellement joindre jusqu’à trois bannières d’accompagnement à une publicité. La bonne pratique consiste à joindre des bannières d’accompagnement, si possible.

>[!NOTE]
>
>* Les éditeurs n’autorisent pas tous les bannières d’entreprise. Les éditeurs qui autorisent les bannières compagnons ne garantissent pas les impressions de bannières compagnons.
>* Les bannières d’accompagnement issues de balises publicitaires tierces peuvent ne pas toujours être disponibles pour la prévisualisation.


**\[Case à cocher\] :** Inclut la bannière compagnon spécifiée avec la publicité. Si la case est désactivée, la bannière compagnon n’est pas incluse.

**\[Banner Size\] :** Taille de bannière compagnon : *[!UICONTROL 300x250]* (utilisé pour [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud], et [!DNL TuneIn]), *[!UICONTROL 640x640]* (utilisé pour [!DNL Spotify), or *1024x1024]* (utilisé pour [!DNL SoundCloud]).

**\[Source\] :** Source de la ressource de bannière compagnon :

* *[!UICONTROL Upload My Own Asset]:* Pour charger votre propre ressource.
* *[!UICONTROL Use a Third Party Tag]:* Pour saisir une balise d’iFrame ou de script provenant d’un partenaire tiers certifié de service publicitaire.

Utilisez une balise tierce lorsque vous souhaitez effectuer le suivi des impressions de bannière compagnon tierce.

**[!UICONTROL Asset]:** (Ressources brutes uniquement) La ressource de bannière compagnon, au format GIF, JPG ou PNG. Cliquez sur **[!UICONTROL Browse]** Recherchez le fichier sur votre appareil ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Ressources brutes uniquement) URL à laquelle accède la visionneuse lorsqu’elle clique sur la bannière compagnon de la publicité. Il peut inclure une redirection des clics à l’aide d’un pixel de suivi des clics tiers.

**[!UICONTROL Final Click URL]:** (ressources brutes uniquement) ; en lecture seule) L’URL de clic avec les [Macros de suivi Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

**[!UICONTROL Ad Tag]:** (Publicités utilisant uniquement des balises publicitaires tierces) Balise d’iFrame ou de bannière de script pour une source de bannière compagnon tierce. Il doit provenir d’un partenaire de service publicitaire tiers certifié.

**[!UICONTROL Final Ad Tag]:** (Publicités utilisant des balises publicitaires tierces uniquement) La balise publicitaire avec le [Macros de suivi Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insérés, le cas échéant.

### Pixel

Tous les pixels de suivi d’événement existants pour l’emplacement sont automatiquement joints. Vous pouvez désolidariser des pixels existants et créer de nouveaux pixels si nécessaire, en fonction de vos besoins de suivi.

Les paramètres suivants s’appliquent à chaque pixel que vous créez ou modifiez.

**[!UICONTROL Integration Event]:** Événement qui déclenche le déclenchement du pixel. Pour ce type d’annonce, utilisez des pixels qui se déclenchent sur la variable *[!UICONTROL Impression]* ou *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Si le pixel est un *[!UICONTROL IMG UR]L* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de l’image en pixels, au format approprié pour le type de pixel spécifié.

**[!UICONTROL Pixel Name]:** Nom du pixel. Utilisez un nom qui vous aidera à identifier facilement le pixel.

**[!UICONTROL Pixel Provider]:** Fournisseur de pixels : *[!UICONTROL None]*, *[!UICONTROL Nielsen]* ou *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Types de publicité disponibles](ad-types.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Macros Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

