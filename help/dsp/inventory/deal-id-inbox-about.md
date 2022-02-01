---
title: À propos de [!UICONTROL Deal ID Inbox]
description: En savoir plus sur les [!UICONTROL Deal ID inbox] qui vous permet d’accepter les offres privées que vous avez déjà négociées avec les éditeurs sur [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement connu sous le nom de [!DNL AdX]), and [!DNL Magnite DV+] (anciennement [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# À propos de [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] vous permet de configurer rapidement des offres qu’Advertising Cloud DSP a importées d’éditeurs par le biais de plateformes côté offre (SSP), afin que vous n’ayez pas à configurer chaque opération manuellement. Vous pouvez accepter les offres d’inventaire privé garanties et non garanties que vous avez déjà négociées avec les éditeurs sur [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement connu sous le nom de [!DNL AdX]), et [!DNL Magnite DV+] (anciennement [!DNL Rubicon]) de la variable [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP est le premier DSP à intégrer à la [!DNL FreeWheel] API.

Dans le [!UICONTROL Deal ID inbox], vous pouvez afficher les détails de l’opération à mesure que votre éditeur les voit, accélérer la configuration de l’opération et éviter les erreurs de saisie manuelle.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP actualise automatiquement tous les détails de la transaction tous les jours à 4 h 30 HNE. Il actualise également tous les [!DNL FreeWheel] offres et mises à jour des offres existantes à partir de [!DNL Google] et [!DNL Magnite DV+] par heure. Vous pouvez également actualiser manuellement les détails de l’opération pour renseigner à tout moment les nouvelles offres.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Pour les offres garanties par la programmation via [!DNL Google Authorized Buyers], vous devez effectuer au moins 90 % de votre budget, sinon votre compte ne pourra plus accéder à [!DNL Google] offres dans [!UICONTROL Deal ID inbox].

## Implémentation de [!UICONTROL Deal ID Inbox]

Pour recevoir vos offres dans la variable [!UICONTROL Deal ID inbox], vos comptes SSP doivent mapper le compte DSP de votre organisation à votre compte SSP. DSP partagera les noms de compte de l’organisation avec les SSP appropriés. Contactez votre [!DNL Adobe] l’équipe du compte pour obtenir des instructions.

Pendant les négociations de l’opération, demandez à l’éditeur d’envoyer l’opération à votre acheteur au lieu du compte DSP parent. L’identifiant de l’opération peut être un nom ou un identifiant, selon le SSP.

## Actions possibles sur vos transactions

* **Transactions de révision** pour vérifier que le SSP a envoyé l’éditeur, les dates de vol, le CPM et d’autres détails de transaction corrects. Si l’éditeur a commis une erreur, contactez-les en dehors de DSP afin qu’il puisse corriger et envoyer à nouveau l’opération.

* **Accepter des accords** après révision, et ils n’apparaîtront plus dans la variable [!UICONTROL Deal ID inbox]. Les offres acceptées sont répertoriées dans la section [!UICONTROL Inventory] > [!UICONTROL Deals] et sont prêts à cibler dans les emplacements des annonceurs.

* **Ignorer les transactions** qui ne sont pas nécessaires ou non sollicités. Les offres ignorées sont déplacées vers la variable [!UICONTROL Ignored Deals] dans l’onglet [!UICONTROL Deal ID inbox], qui sert d’archive. DSP n’alerte pas les SSP et les éditeurs lorsque vous ignorez une transaction.

* **Modifier les détails des offres déjà acceptées** de [!UICONTROL Inventory] > [!UICONTROL Deals] (pas dans la variable [!UICONTROL Deal ID inbox]). De même, lorsque les éditeurs envoient des modifications aux offres, les publicitaires sont chargés de mettre en oeuvre ces modifications dans [!UICONTROL Inventory] > [!UICONTROL Deals] car la variable [!UICONTROL Deal ID inbox] ne synchronise pas les modifications des SSP après la configuration des offres.

## Quels types d&#39;accords ne peuvent être acceptés ?

Lorsqu’une liste d’offres n’inclut pas une ![Accepter](/help/dsp/assets/accept.png) ou une [!UICONTROL Accept] , vous ne pouvez pas l’accepter à partir du [!UICONTROL Deal ID inbox]. Au lieu de cela, vous pouvez [créer manuellement les détails de l’ID de transaction ;](/help/dsp/inventory/deal-id-create.md).

Vous ne pouvez pas accepter les types d’offres suivants :

* [!DNL Google] des offres qui ne sont pas en dollars américains.

* [!DNL Magnite DV+] offres qui ne sont pas en USD

* [!DNL FreeWheel] des offres qui ne sont pas dans la devise de votre compte.

* Offres dont la date de fin est antérieure à aujourd’hui.

* Ancien [!DNL Magnite DV+] les contrats qui étaient qualifiés de &quot;types de médias multiples&quot;.

Les détails de l’accord incluent la raison pour laquelle l’accord n’est pas disponible.

>[!MORELIKETHIS]
>
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Présentation des fonctionnalités du stock](inventory-overview.md)

