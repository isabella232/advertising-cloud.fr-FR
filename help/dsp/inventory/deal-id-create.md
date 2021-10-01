---
title: Créer manuellement les détails de l’identifiant de transaction
description: Découvrez comment saisir manuellement les détails d’un ID de transaction.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 7e2a52e7b0d91f9206cd6e9a6ffb41a8399abf00
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Créer manuellement les détails de l’identifiant de transaction

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Deal ID]**.

1. Saisissez les [paramètres de transaction](deal-id-settings.md) :

   1. Dans la section [!UICONTROL Deal ID basics], indiquez les détails de la transaction et les annonceurs qui peuvent accéder à la transaction. Pour les offres garanties, vous devez également spécifier les dates de vol prévues et l’estimation des impressions, à des fins de suivi uniquement.

   1. (utilisateurs administrateurs uniquement) ; (facultatif) Dans la section [!UICONTROL Technical], modifiez les paramètres par défaut selon vos besoins.

   1. Cliquez sur **[!UICONTROL Save]**.

1. (Offres garanties uniquement) Sélectionnez les publicités qui seront utilisées pour l’opération et créez un emplacement garanti par programme par défaut.

   Les emplacements PG par défaut garantissent que votre transaction renverra toujours une offre pour chaque demande d’offre. Si vous ne créez pas d’emplacement PG par défaut, tous les emplacements qui ciblent l’opération ne placeront pas d’offres à moins qu’ils ne soient correctement configurés. Vous devez toujours créer un emplacement PG par défaut. Dans la vue [!UICONTROL Placements], les emplacements PG par défaut ont une valeur de colonne [!UICONTROL Sub-type] de &quot;[!UICONTROL PG Default]&quot;.

   Vous pouvez éventuellement utiliser l’opération comme cible d’inventaire dans d’autres emplacements, mais vous devez les configurer correctement pour placer des offres.

   1. Dans les paramètres [!UICONTROL Ad & Campaign Selection], sélectionnez les publicités qui seront utilisées pour l’opération :

      1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner l’état d’une publicité pour filtrer les publicités.

      1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité qui sera utilisée pour l’opération.

      1. Cliquez sur **[!UICONTROL Apply]**.
   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez les [paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md), y compris en remplaçant l’offre par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération. la modification de la période ; ou joindre d’autres publicités.

      L’opération est automatiquement ciblée dans la section Cibles de l’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.



Une fois l’opération créée, vous pouvez l’utiliser comme cible d’inventaire pour plusieurs emplacements.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise de transaction à l’éditeur pour vérification.

>[!TIP]
>
>* Dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals] , la colonne [!UICONTROL Pacing & Budget] indique comment l’opération se déroule selon la date de vol et l’objectif d’impression spécifiés.
>
>* Si la diffusion est en sous-ou en trop-rythme, contactez votre éditeur pour ajuster le volume qu’elle envoie via l’offre.


>[!MORELIKETHIS]
>
>* [Paramètres d’ID de transaction manuelle](deal-id-settings.md)
>* [Configuration d’un contrat garanti programmatique](programmatic-guaranteed-set-up.md)
>* [Envoyer une publicité pour une transaction sécurisée par programmation [!DNL FreeWheel]](freewheel-submit.md)
>* [A propos des contrats garantis par programmation](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](private-deal-attach-placements.md)-->