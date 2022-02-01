---
title: Définition des emplacements et des publicités pour un identifiant de transaction
description: Découvrez comment utiliser une offre privée avec des emplacements et publicités supplémentaires.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 669cadcf-021b-4129-95d5-3d24af4a4b88
source-git-commit: 3e47fec28a17cb64de42309c0368293e1ef1cdea
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---

# Définition des emplacements et des publicités pour un identifiant de transaction

Pour les offres non garanties, vous pouvez spécifier l’opération en tant que cible d’inventaire pour les nouveaux emplacements du [!UICONTROL Placements] vue.

Pour les offres PG garanties par programmation, vous pouvez créer de nouveaux emplacements avec des publicités spécifiées à partir de la [!UICONTROL Deals] vue.

Vous pouvez également [Ajout de nouvelles publicités à des emplacements existants](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) à tout moment associé aux offres PG et non garanties.

## Définition d’une transaction non garantie comme cible d’inventaire pour un emplacement

* [Créez un emplacement à partir du [!UICONTROL Placements] view](/help/dsp/campaign-management/placements/placement-create.md). Dans le [!UICONTROL Inventory Targeting] , sélectionnez l’opération privée.

## Joindre des emplacements et des publicités à un contrat PG

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Sur la ligne de la transaction, cliquez sur  ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL attach a placement]**.

1. Dans le [!UICONTROL Ad & Campaign Selection] sélectionnez les publicités qui seront utilisées pour l’emplacement :

       1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner l’état d’une publicité pour filtrer les publicités.
       
       1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité qui sera utilisée pour l’opération.
       
       1. Cliquez sur **[!UICONTROL Apply]**.
   
   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez la variable [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md), y compris le remplacement de l’offre par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération ; la modification de la période ; ou joindre d’autres publicités.

      L’opération est automatiquement ciblée dans la section Cibles de l’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.


L’emplacement commencera à s’exécuter une fois que l’éditeur aura activé votre ID d’opération PG.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise de transaction à l’éditeur pour vérification.

>[!MORELIKETHIS]
>
>* [À propos du stock privé](private-inventory-about.md)
>* [Liste des emplacements et des publicités pour une transaction privée](/help/dsp/inventory/private-deal-view-placements.md)
>* [Créer manuellement les détails de l’identifiant de transaction](deal-id-create.md)
>* [Paramètres d’ID de transaction manuelle](deal-id-settings.md)
>* [Configuration d’un contrat garanti programmatique](programmatic-guaranteed-set-up.md)

