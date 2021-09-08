---
title: Présentation de la configuration des contrats PG dans FreeWheel
description: 'Découvrez les conditions préalables et les étapes supplémentaires nécessaires à l’exécution de publicités pour des offres garanties par programmation avec les éditeurs sur FreeWheel. '
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Présentation de la configuration de contrats sécurisés par programmation dans FreeWheel

La configuration d’offres garanties par la programmation avec les éditeurs sur FreeWheel nécessite des autorisations et des étapes supplémentaires.

>[!PREREQUISITES]
>
>Contactez votre équipe de compte d’Adobe pour vous assurer que votre compte [!DNL DSP] dispose des autorisations suivantes.
>
>1. Autorisation d’utiliser le workflow garanti par la programmation [!DNL FreeWheel], qui est nécessaire pour envoyer une publicité pour une offre garantie par la programmation à [!DNL FreeWheel].
>
>1. (Si vous travaillez avec des éditeurs britanniques qui ont besoin d’un numéro d’horloge avec chaque publicité) Autorisation d’inclure des numéros d’horloge dans vos publicités.


## Workflow

1. Créez une publicité avec le type de média spécifié dans l’opération.

   Pour certains éditeurs britanniques, vous devez inclure un numéro d’horloge Clearcast dans votre publicité.

1. [Acceptez l’](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) ID de transaction que vous avez déjà négocié avec un éditeur sur FreeWheel à l’aide de la boîte de réception Deal ID.

   Une fois que vous avez accepté l’offre, suivez les invites à 1) sélectionnez la publicité à utiliser pour l’offre et 2) créez un emplacement par défaut garanti par programme pour diffuser l’annonce.

1. [Envoyer la publicité à FreeWheel](freewheel-submit.md)

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérifiez l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Envoyer une publicité pour une transaction garanti programmatique à FreeWheel](freewheel-submit.md)
>* [Vérification de l’état des publicités  [!DNL FreeWheel] pour les transactions garanties par programmation](freewheel-check-status.md)
>* [Codes d’erreur pour les envois d’annonce FreeWheel](freewheel-error-codes.md)

