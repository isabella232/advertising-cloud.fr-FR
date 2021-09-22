---
title: Création et implémentation d’un segment personnalisé
description: Découvrez comment créer et implémenter un segment personnalisé pour effectuer le suivi des utilisateurs exposés aux publicités ou des utilisateurs qui visitent vos pages web.
feature: DSP Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Création et implémentation d’un segment personnalisé

Vous pouvez collecter vos propres données d’audience propriétaires en créant et en implémentant un segment Advertising Cloud personnalisé. Vous pouvez utiliser ce segment pour effectuer le suivi a) des utilisateurs exposés aux publicités provenant de périphériques de bureau, mobiles et CTV, et b) des utilisateurs qui visitent des pages web spécifiques. Vous pouvez ensuite recibler les utilisateurs du segment avec des publicités supplémentaires ou empêcher les utilisateurs du segment de recevoir des publicités supplémentaires.

>[!NOTE]
>
>Pour effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la California Consumer Privacy Act (CCPA), créez un [segment d’opposition à la vente des informations personnelles du CCPA](ccpa-opt-out-segment-create.md).

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]** unique.

   1. Pour le [!UICONTROL Segment Type], sélectionnez **[!UICONTROL Custom]**.

   1. Entrez la fenêtre Segment, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans le segment.

      La fenêtre par défaut est de 45 jours. Saisissez une valeur comprise entre 1 (1) et 365.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez des balises pour effectuer le suivi du segment, selon les besoins :

   1. Revenez à **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   2. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get pixel]**.

      * Pour effectuer le suivi des visiteurs de bureau et mobiles sur une page web :

         1. Copiez la balise de suivi des pages vues, qui est étiquetée &quot;[!UICONTROL Desktop or mobile websites]&quot;.

         1. Fournissez la balise au contact de l’annonceur ou du site web pour le déploiement.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.
      * Pour effectuer le suivi des utilisateurs exposés à une unité publicitaire sur des appareils de bureau, mobiles ou CTV :

         1. Copiez la balise de suivi d’impression, qui est étiquetée &quot;[!UICONTROL Desktop or mobile ads]&quot;.

         1. Ajoutez la balise à l’onglet [!UICONTROL Pixel] pour n’importe quelle publicité. <!-- I'll add cross-reference to ad settings later. -->


Une fois qu’une balise de suivi est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!TIP]
>
>Suivez la taille du segment lorsque les utilisateurs sont suivis.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Création et implémentation d’un  [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Paramètres d’audience](audience-settings.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
