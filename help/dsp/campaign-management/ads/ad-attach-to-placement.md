---
title: Joindre une publicité à un emplacement
description: Découvrez comment joindre une publicité à un emplacement.
feature: Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 1%

---

# Joindre une publicité à un emplacement

## Joindre une nouvelle publicité à partir de la vue [!UICONTROL Ads]

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.
1. Cliquez sur le nom de la campagne.
1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.
1. En regard du nom de la publicité, cliquez sur **... >[!UICONTROL Add to Placements]**.
1. Dans l’écran Placer la publicité , effectuez l’une des opérations suivantes :
   * Pour créer un emplacement pour la publicité, procédez comme suit :
      1. Cliquez sur **[!UICONTROL Create New Placement]**.
      1. Saisissez les [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md), puis cliquez sur **[!UICONTROL Create Placement]**.
   * Pour ajouter la publicité à un ou plusieurs emplacements existants :
      1. Cliquez sur **[!UICONTROL Select a Placement].**
      1. Effectuez l’une des opérations suivantes :
         * Pour ajouter une publicité à la fois :
            1. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select].**
            1. (Facultatif) Pour chaque publicité supplémentaire à joindre, cliquez sur **[!UICONTROL Attach to Other Placement]**. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select].**
         * Pour joindre la publicité à 20 emplacements à la fois :
            1. Cochez la case en regard de **Sélection en bloc.&quot;
            1. Cochez la case en regard de chaque emplacement auquel joindre la publicité.
            1. Cliquez sur **[!UICONTROL Attach]**.
      1. Dans l’onglet Terminer et réviser , sélectionnez l’une des options suivantes :
         * Pour revenir à la vue Publicités, cliquez sur **[!UICONTROL I'm done for now]**.
         * Pour joindre la publicité à un autre emplacement, cliquez sur **[!UICONTROL Attach To Other Placement]**.

## Joindre une publicité nouvelle ou existante à partir de la vue [!UICONTROL Placements]

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.
1. Cliquez sur le nom de la campagne.
1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.
1. En regard du nom de l’emplacement, cliquez sur **... > [!UICONTROL Attach Ads].**
1. Dans l’écran [!UICONTROL Add Ad to Placement], effectuez l’une des opérations suivantes :
   * Pour créer une publicité, procédez comme suit :
      1. Cliquez sur **[!UICONTROL Create a New Ad]**.
      1. Renseignez les paramètres de publicité pour les [publicités audio](ad-settings-audio.md), la [télévision connectée](ad-settings-connected-tv.md), les [publicités display](ad-settings-display.md), les [publicités mobiles](ad-settings-mobile.md), les [publicités natives](ad-settings-native.md) ou [publicités preroll](ad-settings-pre-roll.md).
      1. Cliquez sur **[!UICONTROL Save & Submit for Review]**.

         La [révision de la publicité](ad-about.md) de la nouvelle publicité prend entre 24 et 48 heures et inclut des vérifications des catégories sensibles, la fonctionnalité de clic sur l’URL et le rendu de l’aperçu. La colonne [!UICONTROL Status] indique si DSP a approuvé la publicité. Les publicités rompues peuvent avoir un état en attente de plus de 24 à 48 heures, vous avez donc le temps de corriger les erreurs avant qu’elles ne soient rejetées.

         >[!NOTE]
         >
         >Votre publicité ne sera diffusée que si DSP et le SSP ont tous deux approuvé le contenu créatif. Chaque SSP possède ses propres exigences et processus d’approbation.
   * Pour sélectionner des publicités existantes :
      1. Cliquez sur **[!UICONTROL Select an Ad].**
      1. Spécifiez les publicités :
         * Pour ajouter une publicité à la fois :
            1. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select].**
            1. (Facultatif) Pour chaque publicité supplémentaire à joindre, cliquez sur **[!UICONTROL Add Another Ad]**. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select].**
         * Pour ajouter jusqu’à 20 publicités à la fois :
            1. Cochez la case en regard de **[!UICONTROL Bulk Select]**.&quot;
            1. Cochez la case en regard de chaque publicité à ajouter.
            1. Cliquez sur **[!UICONTROL Attach]**.
      1. (Facultatif) Pour remplacer la période de vol par défaut et la rotation des publicités pour des publicités spécifiques dans l’emplacement :
         1. Cliquez sur **[!UICONTROL Custom Schedule Ads]**.
         1. Effectuez l’une des opérations suivantes :
            * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis indiquez la date de début et la date de fin.
            * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne de publicité pour la colonne de vol.
            * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne de publicité pour la colonne de vol.
            * (Lorsque plusieurs publicités ont le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations sur le vol, puis saisissez le poids relatif de rotation de chaque publicité, en pourcentage.
Le poids total doit être égal à 100.
         1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.
         1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.
      1. Cliquez sur **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité](ad-create.md)
>* [Modifier une publicité](ad-edit.md)
>* [Liste des emplacements associés à une publicité](ad-list-placements.md)
>* [Modification de la planification des publicités pour un emplacement](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

