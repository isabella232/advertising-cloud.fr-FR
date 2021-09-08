---
title: Configuration d’un contrat garanti programmatique
description: Découvrez comment configurer un contrat PG garanti par programmation que vous avez négocié avec un éditeur.
feature: Private Inventory, Deal IDs, Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuration d’un contrat garanti programmatique

*[Plateformes côté offre prises en charge uniquement](programmatic-guaranteed-about.md)*

Après avoir négocié une transaction (PG) garantie par un programme avec un éditeur pris en charge, vous pouvez configurer l’opération dans DSP en utilisant la commande [!DNL Deal ID inbox] ou en saisissant manuellement les détails de l’opération.

>[!NOTE]
>
> Pour les offres PG, l’éditeur gère l’intégralité des opérations d’ajustement du budget, de limitation du budget et de ciblage. Tous les SSP qui autorisent PG par DSP confirment que l’éditeur peut configurer la limitation du budget.
>
> La configuration d’offres garanties par la programmation avec les éditeurs sur [!DNL FreeWheel] nécessite des autorisations et des étapes supplémentaires. Pour plus d’informations, voir &quot;[Présentation de la configuration des transactions garanties par programmation dans  [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Configurez une transaction sécurisée programmatique à l’aide de [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Il s’agit de la méthode préférée pour [!DNL FreeWheel], [!DNL Google Authorized Buyers] et [!DNL Rubicon].

1. [Acceptez l&#39;accord](deal-id-inbox-accept.md).

1. Après avoir enregistré l’opération, sélectionnez les publicités qui seront utilisées pour l’opération et créez un emplacement par défaut garanti par programmation (PG), comme vous y êtes invité.

   La création d’un emplacement PG par défaut pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

   * Si vous acceptez une seule transaction, vous êtes automatiquement redirigé vers le workflow de création d’emplacements par défaut PG.

      Tous les [!DNL FreeWheel] marchés sont proposés comme un seul accord.

   * Si vous acceptez une proposition avec plusieurs ID de transaction PG, identifiez chaque emplacement par défaut PG que vous devez créer. Une fois tous les emplacements requis créés, le bouton Continuer est activé.

1. (Facultatif) Ciblez l’opération PG dans des emplacements supplémentaires non PG.

## Configuration manuelle d’une transaction sécurisée par programmation

Utilisez cette méthode pour tous les autres SSP.

1. [Configurez manuellement les détails](deal-id-create.md) de l’ID de transaction.

1. Une fois l’opération enregistrée, sélectionnez les publicités qui seront utilisées pour l’opération et créez un emplacement par défaut PG, comme vous y êtes invité.

   La création d’un emplacement par défaut PG pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

1. (Facultatif) Ciblez l’opération PG dans des emplacements supplémentaires non PG.

>[!MORELIKETHIS]
>
>* [A propos des contrats garantis par programmation](programmatic-guaranteed-about.md)
>* [Conseils pour négocier un accord garanti programmatique](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envoyer une publicité pour une transaction sécurisée par programmation [!DNL FreeWheel]](freewheel-submit.md)
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Créer manuellement les détails de l’identifiant de transaction](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [Présentation des fonctionnalités du stock](inventory-overview.md)

