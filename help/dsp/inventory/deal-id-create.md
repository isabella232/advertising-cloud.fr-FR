---
title: Créer manuellement les détails de l’identifiant de transaction
description: Découvrez comment saisir manuellement les détails d’un ID de transaction.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: c2b83922ba5d4b40ad5a436f0ea052d051fb1d37
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Créer manuellement les détails de l’identifiant de transaction

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Deal ID]**.

1. Saisissez le [paramètres de transaction](deal-id-settings.md):

   1. Dans le [!UICONTROL Deal ID basics] , indiquez les détails de l’opération et les annonceurs qui peuvent accéder à l’opération. Pour les offres garanties, vous devez également spécifier les dates de vol prévues et le nombre estimé d&#39;impressions, à des fins de suivi uniquement.

      Vous pouvez suivre le rythme des offres garanties en incluant la colonne &quot;Calcul de l’impression PG&quot; dans la vue Inventaire > Transactions.

   1. (utilisateurs administrateurs uniquement) ; (facultatif) Dans le [!UICONTROL Technical] modifiez les paramètres par défaut si nécessaire.

   1. Cliquez sur **[!UICONTROL Save]**.

1. (Offres garanties uniquement) Sélectionnez les publicités à utiliser pour l’opération et créez un emplacement par défaut garanti par programmation (PG).

   Les emplacements PG par défaut garantissent que votre transaction renvoie toujours une offre pour chaque demande d’offre. Si vous ne créez pas d’emplacement PG par défaut, tous les emplacements qui ciblent l’opération ne placent pas d’offres à moins qu’ils ne soient correctement configurés. Vous devez toujours créer un emplacement PG par défaut. Dans le [!UICONTROL Placements] vue, les emplacements PG par défaut ont une [!UICONTROL Sub-type] valeur de colonne de &quot;[!UICONTROL PG Default].&quot;

   Vous pouvez éventuellement utiliser l’opération comme cible d’inventaire dans d’autres emplacements, mais vous devez les configurer correctement pour placer des offres.

   1. Dans le [!UICONTROL Ad & Campaign Selection] sélectionnez les publicités qui seront utilisées pour l’opération :

      1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner l’état d’une publicité pour filtrer les publicités.

      1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité à utiliser pour l’opération.

      1. Cliquez sur **[!UICONTROL Apply]**.
   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez la variable [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md), y compris le remplacement de l’offre par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération ; la modification de la période ; ou joindre d’autres publicités.

      L’opération est automatiquement ciblée dans la section Cibles de l’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.



Une fois l’opération créée, vous pouvez l’utiliser comme cible d’inventaire pour plusieurs emplacements.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise de transaction à l’éditeur pour vérification.

>[!TIP]
>
>* Dans le [!UICONTROL Inventory] > [!UICONTROL Deals] vue, [!UICONTROL Pacing & Budget] La colonne indique comment l’opération s’étend à la date de vol spécifiée et à l’objectif d’impression.
>
>* Si la diffusion est en sous-ou en trop-rythme, contactez votre éditeur pour ajuster le volume qu’elle envoie via l’offre.


>[!MORELIKETHIS]
>
>* [Paramètres d’ID de transaction manuelle](deal-id-settings.md)
>* [Configuration d’un contrat garanti programmatique](programmatic-guaranteed-set-up.md)
>* [Envoyer une publicité pour une transaction sécurisée par programmation [!DNL FreeWheel]](freewheel-submit.md)
>* [A propos des contrats garantis par programmation](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
