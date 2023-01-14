---
title: Utilisation [!DNL Roku] Inventaire
description: En savoir plus sur DSP partenariat avec [!DNL Roku], y compris les options d’inventaire, les fournisseurs tiers approuvés de suivi et les bonnes pratiques pour [!DNL Roku]emplacements spécifiques.
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Utilisation [!DNL Roku] Inventaire

Advertising DSP fournit des fonctionnalités uniques pour la publicité sur [!DNL Roku].

## DSP et [!DNL Roku] Partenariat

Roku et DSP ont un partenariat unique qui correspond à votre [!DNL DSP] audiences vers [!DNL Roku] ID pour le ciblage d’audience déterministe 1:1 sur [!DNL Roku] inventaire.

En dehors de la DSP de Roku (OneView), la DSP publicitaire a un accès unique à ces fonctionnalités de ciblage. La DSP publicitaire est également le seul DSP autorisé à mesurer [!DNL Roku] offre en regard de tous les autres inventaires de télévision connectée (CTV). Parce que [!DNL Roku] ne partage pas tous les signaux RTB et pixel d’impression standard, aucun autre DSP ne peut cibler ou mesurer sur l’ensemble de l’offre CTV vendue sur Roku.

## [!DNL Roku] Options d’inventaire

Vous pouvez soit (a) configurer des ID d’opération privés directement avec [!DNL Roku] puis saisissez les données d’ID de transaction dans DSP ou b) rendez-vous sur la page [!DNL On Demand] Galerie pour vous abonner à [!DNL Roku] profils :

>[!NOTE]
>
>[!DNL Roku] L&#39;inventaire n&#39;est pas disponible sur les marchés ouverts et les bourses.

* Pour vos affaires privées, [configurer des informations sur les ID de transaction dans DSP](/help/dsp/inventory/deal-id-create.md) et ensuite cibler &quot;[!UICONTROL Roku Network – Audience]&quot; et &quot;[!UICONTROL The Roku Channel – Audience]&quot; dans [!DNL Roku] emplacements.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Vous pouvez [abonnez-vous à ce qui suit [!DNL Roku] inventaire dans [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md), puis ciblez l’un des accords approuvés dans [!DNL Roku] emplacements :

   * &quot;[!UICONTROL Roku Network – Audience]&quot; pour l’inventaire dans la [!DNL Roku] écosystème avec des partenaires de contenu de qualité, tels que [!DNL The CW], [!DNL ABC], et [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; pour [!DNL Roku] contenu d’application détenu et exploité (O&amp;O).

### Avantages de la personnalisation des marchés privés avec [!DNL Roku]

Les offres privées vous permettent de personnaliser les paramètres de l’opération en fonction de vos besoins.

* **Tarifs négociés :** Utilisation de la fonction [!DNL Roku] l’équipe commerciale pour négocier et structurer un accord qui répond aux besoins de votre campagne.

* **Priorité des échelles :** Les marchés privés (PMP) reçoivent une priorité plus élevée que les offres toujours actives (telles que les offres [!DNL On Demand] offres).

* **Gestion des fréquences :** Le [!DNL Roku] la limite de fréquence par défaut est d’une (1) publicité par 30 minutes par utilisateur, mais vous pouvez la personnaliser par heure, jour, semaine, mois ou période de vol complète.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Ciblage de données :** [!DNL Roku] les audiences sont créées à partir de [!DNL Roku] signaux d’appareil et de télévision, données suivies par [!DNL The Roku Channel] (par exemple, l’affinité du genre TV, le comportement de la télévision en continu et l’état de l’abonnement au câble) et des données supplémentaires provenant de [!DNL Roku] système de gestion de la relation client (CRM).

* **[!DNL Roku]Ciblage de contenu :** Les offres privées peuvent cibler des applications par genre, application de la liste bloquée d’application, événements saisonniers et de tentpôle et programmes dans [!DNL The Roku Channel] uniquement.

## [!DNL Roku] Emplacements

Dans DSP campagnes, [create [!DNL Roku]Emplacements spécifiques](/help/dsp/campaign-management/placements/placement-create.md) en utilisant le type d’emplacement &quot;[!UICONTROL Connected TV (Roku)].&quot; Inclure [!DNL Roku] emplacements dans [!DNL Roku]des modules spécifiques avec des objectifs définis.

Chaque [!DNL Roku] l’emplacement doit cibler au moins un [!DNL Roku] transaction ou source. Pour utiliser la correspondance d’audience unique de DSP avec [!DNL Roku], incluez un ou plusieurs segments d’audience pouvant être mis en correspondance avec la variable [!DNL Roku] Jeu de données déterministes (opt-in).

### [!DNL Roku]Fournisseurs de suivi tiers approuvés

[!DNL Roku] les emplacements peuvent inclure des pixels d’événement tiers et des pixels de conversion provenant des fournisseurs suivants :  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], et [!DNL Research Now].

### Bonnes pratiques par stratégie de placement

Voici les pratiques recommandées pour [!DNL Roku]emplacements spécifiques.

Pour optimiser la portée incrémentielle :

* Supprimer les audiences exposées sur [!DNL Roku O&O] en excluant les audiences que vous avez déjà atteintes à l’aide de [!DNL The Roku Channel].

* Supprimer les audiences exposées sur [!DNL All Roku] en excluant les audiences que vous avez déjà atteintes dans la variable [!DNL Roku] plateforme.

Pour la configuration la plus rapide :

* Cibler des offres existantes et toujours actives pour [!DNL The Roku Channel] in [[!DNL On Demand] Inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md) pour un accès rapide [!DNL Roku] inventaire détenu et exploité.
* Cibler des offres existantes et toujours actives pour [!DNL Roku Network] in [[!DNL On Demand] Inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md) pour obtenir rapidement une échelle [!DNL Roku] plateforme.

Pour une échelle maximale :

* Personnalisation d’une [!DNL Roku] marché privé pour un accès prioritaire à [!DNL Roku] offre à un prix négocié.

>[!MORELIKETHIS]
>
>* [Créer manuellement les détails de l’identifiant de transaction](/help/dsp/inventory/deal-id-create.md)
> * [Abonner et demander l’accès à [!DNL On Demand] Premium Offres d’inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Création d’un emplacement](/help/dsp/campaign-management/placements/placement-create.md)

