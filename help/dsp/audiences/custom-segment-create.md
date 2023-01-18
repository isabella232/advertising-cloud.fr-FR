---
title: Création et implémentation d’un segment personnalisé
description: Découvrez comment créer et implémenter un segment personnalisé pour effectuer le suivi des utilisateurs exposés aux publicités ou des utilisateurs qui visitent vos pages web.
feature: DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Création et implémentation d’un segment personnalisé

Vous pouvez collecter vos propres données d’audience propriétaires en créant et en implémentant un segment DSP personnalisé. Vous pouvez utiliser ce segment pour effectuer le suivi a) des utilisateurs exposés aux publicités provenant de périphériques de bureau, mobiles et CTV, et b) des utilisateurs qui visitent des pages web spécifiques. Vous pouvez ensuite recibler les utilisateurs du segment avec des publicités supplémentaires ou empêcher les utilisateurs du segment de recevoir des publicités supplémentaires.

>[!NOTE]
>
>Pour effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, en vertu de la California Consumer Privacy Act (CCPA), créez une [Segment d’exclusion de la vente du CCPA](ccpa-opt-out-segment-create.md).

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]**.

   1. Pour le **[!UICONTROL Segment Type]**, sélectionnez *[!UICONTROL Custom]*.

   1. Saisissez le **[!UICONTROL Segment Window]**: nombre de jours pendant lesquels le cookie d’un utilisateur reste dans le segment.

      La fenêtre par défaut est de 45 jours. Saisissez une valeur comprise entre 1 (1) et 365.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez des balises pour effectuer le suivi du segment, selon les besoins :

   1. Revenir à **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get Pixel]**.

      * Pour effectuer le suivi des visiteurs de bureau et mobiles sur une page web :

         1. Copiez la balise de suivi des pages vues, étiquetée &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Fournissez la balise au contact de l’annonceur ou du site web pour le déploiement.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.
      * Pour effectuer le suivi des utilisateurs exposés à une unité publicitaire sur des appareils de bureau, mobiles ou CTV :

         1. Copiez la balise de suivi d’impression, étiquetée &quot;[!UICONTROL Desktop or mobile ads].&quot;


1. Ajoutez la balise au [!UICONTROL Pixel] pour chaque publicité appropriée ou au [!UICONTROL Event Pixels] de la section [[!UICONTROL Tracking] paramètres pour chaque emplacement approprié](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Une fois qu’une balise de suivi est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!TIP]
>
>Suivez la taille du segment lorsque les utilisateurs sont suivis.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Modifier les informations sur le segment](segment-edit.md)
>* [Suppression d’un segment](segment-delete.md)
>* [Affichage des pixels de suivi pour un segment](segment-view-pixels.md)
>* [Partage ou arrêt du partage d’un segment](segment-share.md)
>* [Créez et implémentez une [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

