---
title: Envoyer une publicité pour une transaction PG à [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une offre garantie par un programme auprès d’un éditeur sur FreeWheel.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Envoyer une publicité pour une transaction garanti programmatique à FreeWheel

*Comptes avec l’autorisation  [!DNL FreeWheel] Programmatic Guaranteed uniquement*

Une fois que vous avez [accepté une offre garantie par un programme avec un éditeur sur FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), y compris la sélection d’une publicité et la création de l’emplacement par défaut garanti par un programme à utiliser pour l’opération, vous devez envoyer la publicité à FreeWheel pour approbation.

>[!PREREQUISITES]
>
>Contactez votre équipe de compte d’Adobe pour vous assurer que votre compte [!DNL DSP] est autorisé à utiliser le workflow garanti par la programmation [!DNL FreeWheel].

1. Copiez la clé publicitaire de la publicité utilisée avec l’offre FreeWheel :

   1. Cliquez sur le nom de la campagne.

   1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.

   1. Cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]** en regard du nom de la publicité.

   1. Une fois les paramètres de publicité ouverts, copiez la clé publicitaire alphanumérique dans l’URL affichée dans la barre d’adresse du navigateur.

      Par exemple, dans l’URL suivante, la clé publicitaire est `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. Envoyez la publicité à FreeWheel :

   1. Dans la vue [!UICONTROL Deals], recherchez l’opération.

   1. Dans la ligne de la transaction, cliquez sur ![Menu Options](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]**.

   1. Vérifiez l’ID de la transaction, saisissez la balise **[!UICONTROL Ad Key]** que vous avez copiée à l’étape 1, puis cliquez sur **[!UICONTROL Submit]**.

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérifiez l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Présentation de la configuration de contrats sécurisés par programmation dans FreeWheel](freewheel-overview.md)
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Vérification de l’état des publicités  [!DNL FreeWheel] pour les transactions garanties par programmation](freewheel-check-status.md)
>* [Codes d’erreur pour les envois d’annonce FreeWheel](freewheel-error-codes.md)

