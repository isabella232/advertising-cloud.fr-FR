---
title: Gestion de l’audience dans Advertising Cloud DSP
description: Découvrez les fonctionnalités de gestion de l’audience.
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 578651a458ffd505573df0e9a61e26bd2176ad17
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# Gestion de l’audience dans Advertising Cloud DSP

Dans Advertising Cloud DSP, vous pouvez créer et gérer des segments d’audience et des ensembles d’audiences, que vous pouvez utiliser comme cibles pour vos emplacements :

* Vous pouvez collecter vos propres données d’audience propriétaires en créant et en implémentant des segments. Vous pouvez ensuite recibler les utilisateurs du segment avec des publicités ou empêcher les utilisateurs du segment de recevoir des publicités. Vous pouvez créer les types de segments suivants :

   * [Segments personnalisés ](/help/dsp/audiences/custom-segment-create.md) pour effectuer le suivi des utilisateurs a) exposés aux publicités provenant de périphériques de bureau, mobiles et CTV, et b) qui visitent des pages web spécifiques.

   * [Segments d’opposition à la vente des informations personnelles du CCPA ](/help/dsp/audiences/ccpa-opt-out-segment-create.md) pour effectuer le suivi des ID d’utilisateurs provenant de demandes d’opposition à la vente des informations personnelles des clients sur votre site web, en vertu de la California Consumer Privacy Act (CCPA). Vous pouvez récupérer les rapports mensuels des identifiants d’utilisateur à partir des demandes d’opposition à la vente.

      Pour plus d’informations sur la prise en charge d’Advertising Cloud pour les demandes d’opposition à la vente des informations personnelles du CCPA, voir [Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’exclusion des consommateurs](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* Vous pouvez créer une bibliothèque d’audiences [réutilisables ](/help/dsp/audiences/reusable-audience-create.md). Les audiences enregistrées sont composées de l’un de vos segments d’audience disponibles et de l’une de vos autres audiences enregistrées. Toute modification apportée à une audience enregistrée est automatiquement appliquée à tous les emplacements qui ciblent ou excluent l’audience et à toutes les autres audiences qui incluent l’audience enregistrée.

   Les audiences enregistrées permettent aux planificateurs de médias de regrouper les audiences selon les besoins, en incluant et en excluant plusieurs segments à l’aide d’une logique booléenne complexe. La taille de chaque segment et la taille totale de l’audience sont indiqués au fur et à mesure que vous créez une audience. Les exécutants de Campaign peuvent alors simplement sélectionner une ou plusieurs audiences enregistrées comme cibles d’emplacement plutôt que de configurer manuellement les cibles d’audience pour chaque emplacement.

D’autres types d’audience sont également disponibles pour le ciblage des emplacements.

## Importation de segments de données propriétaires et tiers

Advertising Cloud DSP peut importer vos propres segments de données propriétaires à partir de votre plateforme de gestion des données (DMP) et les fournir à tout ensemble d’annonceurs, si nécessaire.

Advertising Cloud DSP peut également importer des segments tiers personnalisés, y compris des combinaisons complexes de segments tiers. Vous pouvez fournir les segments à n’importe quel groupe d’annonceurs, si nécessaire.

Pour plus d’informations, contactez votre gestionnaire de compte.

## Audiences disponibles en tant que cibles de placement

Vous pouvez cibler vos emplacements sur tous les types d’audiences suivants.

* Toutes les visionneuses d’audiences créées par l’utilisateur qui ont été enregistrées dans Advertising Cloud DSP.

* Tous les segments d’audience créés par l’utilisateur qui ont été créés dans Advertising Cloud DSP :

   * Segments personnalisés pour les utilisateurs qui ont consulté des pages web spécifiques et qui ont été exposés à des impressions de publicités spécifiques.

   * Segments d’audience d’opposition à la vente des informations personnelles du CCPA pour les utilisateurs qui ont soumis des demandes d’opposition à la vente des informations personnelles sur votre site web, en vertu du California Consumer Privacy Act (CCPA).

* Tous les segments de données propriétaires importés.

* Tous les segments de données tiers personnalisés importés.

* (Emplacements ciblant uniquement les États-Unis) [Tous les segments de données tiers disponibles pour les clients Advertising Cloud DSP de plus de 30 fournisseurs ](/help/dsp/audiences/third-party-data-providers.md), y compris [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast], et bien d’autres.

   Vous pouvez cibler des segments spécifiques, qui ciblent les utilisateurs en fonction des données d’audience (par exemple, les utilisateurs avec des données démographiques, des centres d’intérêt ou des intentions spécifiques et/ou des profils comportementaux). Vous pouvez naviguer par fournisseur de données et par catégorie, rechercher des segments par nom ou identifiant de segment, ou filtrer les résultats par fournisseur de données, taille totale des segments, nombre de navigateurs Web ou nombre d’appareils.

   Les segments tiers engendrent des frais supplémentaires, indiqués en regard de chaque nom de segment.

* (Publicitaires avec Adobe Experience Cloud, Adobe Audience Manager ou Adobe Analytics qui utilisent uniquement des balises de conversion JavaScript Advertising Cloud) Tous les segments d’audience propriétaires, de deuxième ou de troisième niveau disponibles créés dans Adobe Experience Cloud, créés dans Audience Manager ou publiés sur Adobe Experience Cloud à partir d’Audience Manager ou de [!DNL Analytics].

   Les tarifs d’utilisation des segments sont pré-négociés et ne sont pas visibles dans Advertising Cloud.  <!-- Verify -->

   Les segments de Adobe Experience Cloud sont disponibles environ une heure après leur création ou leur publication dans Adobe Experience Cloud. Les segments provenant directement de l’Audience Manager sont disponibles environ 24 heures après leur création. <!-- Verify all -->

   >[!NOTE]
   >
   >Pour plus d’informations sur la configuration et la collecte de données pour les segments dans ces solutions, consultez la documentation de [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html) et [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Données sur la taille de l’audience

Dans les paramètres d’audience enregistrés et les paramètres d’emplacement, vous pouvez afficher des données détaillées sur la taille de l’audience :

* La taille totale et principale de l’audience dédupliquée pour tous les segments sélectionnés et les audiences enregistrées s’affiche. Vous pouvez afficher les détails par type d’appareil (navigateur, mobile ou télévision connectée).

   ![la taille d’audience combinée ;](/help/dsp/assets/audience-size.png)

* Pour les segments individuels et les audiences enregistrées, la taille totale de l’audience et le CPM (le cas échéant) s’affichent en regard du nom du segment. Vous pouvez afficher plus de détails sur le segment, y compris la taille par type d’appareil (navigateur, mobile ou télévision connectée). Pour les audiences enregistrées, la taille totale est le total dédupliqué.

   ![la taille individuelle du segment ;](/help/dsp/assets/audience-size-segment.png)

## Audiences vues

### Vue Toutes les audiences

Dans la vue [!UICONTROL All Audiences], ou la bibliothèque d’audiences, vous pouvez enregistrer et gérer des audiences réutilisables, qui incluent des groupes de segments d’audience et même d’autres audiences enregistrées. Vous pouvez utiliser les audiences comme cibles pour plusieurs emplacements. Le nombre d’emplacements dans lesquels chaque audience est utilisée est indiqué en regard du nom de l’emplacement.

Vous pouvez modifier, cloner, supprimer, exporter ou partager n’importe quelle audience.

### Vue Segments

Dans la vue [!UICONTROL Segments], tous les utilisateurs peuvent créer des segments personnalisés supplémentaires.

La vue [!UICONTROL Segments] répertorie également les types de segments suivants :

* Tous les segments personnalisés créés par l’utilisateur sont disponibles pour l’utilisateur.

   Vous pouvez afficher les balises de suivi pour l’un des segments personnalisés que vous avez créés et les partager avec d’autres utilisateurs. Vous pouvez également modifier ou supprimer les segments personnalisés que vous avez créés.

   Vous ne pouvez pas modifier ni partager des segments personnalisés que d’autres utilisateurs ont partagés avec vous.

* Tous les segments propriétaires importés sont disponibles pour l’utilisateur.

   Vous ne pouvez pas modifier ni partager les segments propriétaires qui ont été partagés avec vous. Contactez votre gestionnaire de compte si vous devez partager des segments propriétaires avec d’autres utilisateurs.

* Tous les segments tiers personnalisés sont disponibles pour l’utilisateur.

   Vous ne pouvez pas modifier ni partager des segments tiers qui ont été partagés avec vous. Contactez votre gestionnaire de compte si vous devez partager des segments tiers avec d’autres utilisateurs.

>[!MORELIKETHIS]
>
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Paramètres d’audience](audience-settings.md)
>* [Syntaxe de la logique de segment d’audience](audience-segment-logic-syntax.md)
>* [Création et implémentation d’un segment personnalisé](custom-segment-create.md)
>* [Création et implémentation d’un  [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

