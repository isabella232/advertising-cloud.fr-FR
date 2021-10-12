---
title: À propos de [!UICONTROL Deal ID Inbox]
description: Découvrez la fonction [!UICONTROL Deal ID inbox], qui vous permet d’accepter les offres privées que vous avez déjà négociées avec les éditeurs sur  [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (anciennement [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# À propos de [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] vous permet de configurer rapidement des offres qu’Advertising Cloud DSP a importées des éditeurs via des plateformes côté offre (SSP) afin que vous n’ayez pas à configurer chaque opération manuellement. Vous pouvez accepter les offres d’inventaire privé garanties et non garanties que vous avez déjà négociées avec les éditeurs sur [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement [!DNL AdX]) et [!DNL Magnite DV+] (anciennement [!DNL Rubicon]) à partir du [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP est la première DSP à intégrer avec l’API [!DNL FreeWheel].

Dans la section [!UICONTROL Deal ID inbox], vous pouvez afficher les détails de l’opération à mesure que votre éditeur les voit, accélérer la configuration de l’opération et éviter les erreurs de saisie manuelle.

DSP actualise automatiquement tous les détails de la transaction tous les jours à 4 h 30 HNE. Il actualise également toutes les [!DNL FreeWheel] offres et met à jour les offres existantes toutes les heures de [!DNL Google] et [!DNL Magnite DV+]. Vous pouvez également actualiser manuellement les détails de l’opération pour renseigner à tout moment les nouvelles offres.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Pour les offres garanties par la programmation via [!DNL Google Authorized Buyers], vous devez exécuter au moins 90 % de votre budget, sinon votre compte perdra l’accès aux [!DNL Google] offres dans la section [!UICONTROL Deal ID inbox].

## Implémentation de [!UICONTROL Deal ID Inbox]

Pour recevoir vos offres dans [!UICONTROL Deal ID inbox], vos comptes SSP doivent mapper le compte DSP de votre organisation à votre compte SSP. DSP partagera les noms de compte de l’organisation avec les SSP appropriés. Contactez votre gestionnaire de compte d’Adobe pour obtenir des instructions.

Pendant les négociations de l’opération, demandez à l’éditeur d’envoyer l’opération à votre acheteur au lieu du compte DSP parent. L’identifiant de l’opération peut être un nom ou un identifiant, selon le SSP.

## Actions possibles sur vos transactions

* **Vérifiez** les conditions pour vérifier que le fournisseur de services de messagerie a envoyé l’éditeur, les dates de vol, le CPM et d’autres détails sur l’opération corrects. Si l’éditeur a commis une erreur, contactez-les en dehors de DSP afin qu’il puisse corriger et envoyer à nouveau l’opération.

* **Acceptez les** conditions après révision et elles n’apparaîtront plus dans le  [!UICONTROL Deal ID inbox]. Les offres acceptées sont répertoriées dans [!UICONTROL Inventory] > [!UICONTROL Deals] et sont prêtes à être ciblées dans les emplacements des annonceurs.

* **Ignorez** les transactions inutiles ou non sollicitées. Les offres ignorées sont déplacées vers l’onglet [!UICONTROL Ignored Deals] dans la balise [!UICONTROL Deal ID inbox], qui sert d’archive. DSP n’alerte pas les SSP et les éditeurs lorsque vous ignorez une transaction.

* **Modifiez les détails des** soldes déjà acceptés depuis  [!UICONTROL Inventory] >  [!UICONTROL Deals] (pas dans le  [!UICONTROL Deal ID inbox]). De même, lorsque les éditeurs envoient des modifications aux offres, les annonceurs sont chargés de mettre en oeuvre ces modifications dans [!UICONTROL Inventory] > [!UICONTROL Deals], car [!UICONTROL Deal ID inbox] ne synchronise pas les modifications des SSP une fois les offres configurées.

## Quels types d&#39;accords ne peuvent être acceptés ?

Lorsqu’une liste d’offres ne contient pas d’icône ![Accepter](/help/dsp/assets/accept.png) ou de bouton [!UICONTROL Accept], vous ne pouvez pas l’accepter à partir de la balise [!UICONTROL Deal ID inbox]. Vous pouvez à la place [créer manuellement les détails de l’ID de transaction](/help/dsp/inventory/deal-id-create.md).

Vous ne pouvez pas accepter les types d’offres suivants :

* [!DNL Google] des offres qui ne sont pas en dollars américains.

* [!DNL Magnite DV+] offres qui ne sont pas en USD

* [!DNL FreeWheel] des offres qui ne sont pas dans la devise de votre compte.

* Offres dont la date de fin est antérieure à aujourd’hui.

* Anciens [!DNL Magnite DV+] contrats qui étaient qualifiés de &quot;types de médias multiples&quot;.

Les détails de l’accord incluent la raison pour laquelle l’accord n’est pas disponible.

>[!MORELIKETHIS]
>
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Présentation des fonctionnalités du stock](inventory-overview.md)

