---
title: Utilisation de [!DNL Roku] l’inventaire
description: 'Découvrez DSP partenariat avec des emplacements spécifiques à  [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Utilisation de l’inventaire [!DNL Roku]

Advertising Cloud DSP fournit des fonctionnalités uniques pour la publicité sur [!DNL Roku].

## Le partenariat Advertising Cloud DSP et [!DNL Roku]

Roku et Advertising Cloud DSP ont un partenariat unique qui correspond à vos audiences [!DNL DSP] à [!DNL Roku] ID pour le ciblage d’audience déterministe 1:1 sur l’inventaire [!DNL Roku].

En dehors de la DSP de Roku (OneView), Advertising Cloud DSP a un accès unique à ces fonctionnalités de ciblage. Advertising Cloud DSP est également la seule DSP autorisée à mesurer l’offre [!DNL Roku] à côté de tous les autres inventaires de télévisions connectées (CTV). Étant donné que [!DNL Roku] ne partage pas tous les signaux RTB et pixel d’impression standard, aucun autre DSP ne peut cibler ou mesurer sur l’offre CTV vendue sur Roku.

## [!DNL Roku] Options d’inventaire

Vous pouvez : a) configurer des ID d’opération privés directement avec [!DNL Roku], puis saisir les données d’ID d’opération dans DSP ou b) accéder à la [!DNL On Demand] Galerie pour vous abonner aux profils [!DNL Roku] :

>[!NOTE]
>
>[!DNL Roku] L&#39;inventaire n&#39;est pas disponible sur les marchés ouverts et les bourses.

* Pour vos offres privées, vous allez [configurer des informations sur les ID d’opération dans DSP](/help/dsp/inventory/deal-id-create.md), puis cibler &quot;[!UICONTROL Roku Network – Audience]&quot; et &quot;[!UICONTROL The Roku Channel – Audience]&quot; dans des emplacements [!DNL Roku].<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Vous pouvez [vous abonner à la  [!DNL Roku] inventory within the [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md) suivante, puis cibler toutes les offres approuvées à des [!DNL Roku] emplacements :

   * &quot;[!UICONTROL Roku Network – Audience]&quot; pour l’inventaire dans l’écosystème [!DNL Roku] avec des partenaires de contenu de qualité, tels que [!DNL The CW], [!DNL ABC] et [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; pour le contenu de l’application [!DNL Roku] détenue et gérée (O&amp;O).

### Avantages de la personnalisation des marchés privés avec [!DNL Roku]

Les offres privées vous permettent de personnaliser les paramètres de l’opération en fonction de vos besoins.

* **Tarifs négociés :** travaillez avec l’équipe  [!DNL Roku] commerciale pour négocier et structurer un accord qui répond aux besoins de votre campagne.

* **Priorité d’échelle :** les marchés privés (PMP) reçoivent une priorité plus élevée que les marchés toujours actifs (tels que les  [!DNL On Demand] offres).

* **Gestion des fréquences :** le plafond  [!DNL Roku] par défaut est d’une (1) publicité par 30 minutes par utilisateur, mais vous pouvez personnaliser le plafond par heure, jour, semaine, mois ou période de vol complète.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Ciblage des données :** [!DNL Roku]  les audiences sont créées à partir de signaux de  [!DNL Roku] périphérique et de télévision, de données suivies par  [!DNL The Roku Channel] (comme l’affinité du genre TV, le comportement de la télévision en continu et l’état d’abonnement au câble) et de données supplémentaires provenant du système de gestion de la relation  [!DNL Roku] client (CRM).

* **[!DNL Roku]Ciblage de contenu :** les offres privées peuvent cibler les applications par genre, application de la liste bloquée d’application, événements saisonniers et de tentpôle, et elles ne s’affichent  [!DNL The Roku Channel] que dans .

## [!DNL Roku] Emplacements

Dans DSP campagnes, vous allez [créer des  [!DNL Roku] emplacements spécifiques](/help/dsp/campaign-management/placements/placement-create.md) à l’aide du type d’emplacement &quot;[!UICONTROL Connected TV (Roku)]&quot;. Vous allez inclure des [!DNL Roku] emplacements dans des modules spécifiques à [!DNL Roku] avec des objectifs définis.

Chaque emplacement [!DNL Roku] doit cibler au moins une [!DNL Roku] opération ou source. Pour tirer parti de la correspondance d’audience unique de DSP avec [!DNL Roku], incluez un ou plusieurs segments d’audience pouvant être mis en correspondance avec le jeu de données déterministe [!DNL Roku] (opt-in).

### [!DNL Roku]Fournisseurs de suivi tiers approuvés

[!DNL Roku] les emplacements peuvent inclure des pixels d’événement tiers et des pixels de conversion provenant des fournisseurs suivants :   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal],  [!DNL Oracle],  [!DNL Placed],  [!DNL Polk],  [!DNL Research Now],, et.

### Bonnes pratiques par stratégie de placement

Vous trouverez ci-dessous les pratiques recommandées pour les emplacements spécifiques à [!DNL Roku].

Pour optimiser la portée incrémentielle :

* Supprimez les audiences exposées sur [!DNL Roku O&O] en excluant les audiences que vous avez déjà atteintes à l’aide de [!DNL The Roku Channel].

* Supprimez les audiences exposées sur [!DNL All Roku] en excluant les audiences que vous avez déjà atteintes sur la plateforme [!DNL Roku].

Pour la configuration la plus rapide :

* Ciblez les offres existantes et permanentes pour [!DNL The Roku Channel] dans [[!DNL On Demand] Inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md) afin d’accéder rapidement à l’ [!DNL Roku] inventaire détenu et exploité.
* Ciblez les offres existantes et toujours actives pour [!DNL Roku Network] dans [[!DNL On Demand] Inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md) afin d’atteindre rapidement l’échelle sur la plateforme [!DNL Roku].

Pour une échelle maximale :

* Personnalisez un [!DNL Roku] marché privé pour accéder en priorité à l’offre [!DNL Roku] à un prix négocié.

>[!MORELIKETHIS]
>
>* [Créer manuellement les détails de l’identifiant de transaction](/help/dsp/inventory/deal-id-create.md)
> * [Abonner et demander l’accès  [!DNL On Demand] aux offres d’inventaire Premium](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Création d’un emplacement](/help/dsp/campaign-management/placements/placement-create.md)

