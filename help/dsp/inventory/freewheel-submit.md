---
title: Envoyer une publicité pour une opération PG à [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une transaction garantie par un programme avec un éditeur sur [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 6cb41f3b-29e4-4feb-9c31-578ab40bd4f7
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Envoyer une publicité pour une transaction garantie par un programme à [!DNL Freewheel]

*Comptes avec la variable [!DNL FreeWheel] Autorisation garantie par programmation uniquement*

Une fois que [accepter une offre garantie par un programme avec un éditeur sur FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), y compris la sélection d’une publicité et la création de l’emplacement par défaut garanti par la programmation à utiliser pour l’opération, vous devez envoyer l’annonce à [!DNL Freewheel] pour approbation.

>[!PREREQUISITES]
>
>Contactez votre équipe de compte d’Adobe pour vous assurer que votre [!DNL DSP] compte autorisé à utiliser la variable [!DNL FreeWheel] workflow garanti par la programmation.

1. Copiez la clé publicitaire de la publicité utilisée avec le [!DNL Freewheel] deal :

   1. Cliquez sur le nom de la campagne.

   1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.

   1. Cliquez sur  **[!UICONTROL ...]>[!UICONTROL Edit]** en regard du nom de la publicité.

   1. Une fois les paramètres de publicité ouverts, copiez la clé publicitaire alphanumérique dans l’URL affichée dans la barre d’adresse du navigateur.

      Par exemple, dans l’URL suivante, la clé publicitaire est `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. Envoyer la publicité à [!DNL Freewheel]:

   1. Effectuez l’une des opérations suivantes :

      * En regard du nom de la publicité, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Sur la ligne de la transaction, cliquez sur ![Menu Options](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. Vérifiez l’ID de la transaction, puis saisissez la variable **[!UICONTROL Ad Key]** vous avez copié à l’étape 1, puis cliquez sur **[!UICONTROL Submit]**.

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérification de l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Présentation de la configuration de transactions garanties par la programmation dans [!DNL Freewheel]](freewheel-overview.md)
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Vérification de l’état des publicités pour [!DNL FreeWheel] Offres garanties par la programmation](freewheel-check-status.md)
>* [Codes d’erreur pour [!DNL Freewheel] Envois de publicités](freewheel-error-codes.md)

