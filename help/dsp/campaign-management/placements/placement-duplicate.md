---
title: Duplication de placements
description: Découvrez comment dupliquer un ou plusieurs emplacements.
feature: Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Duplication de placements

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliquez un ou plusieurs emplacements pour créer des emplacements avec des paramètres similaires. Vous pouvez :

* Créer plusieurs doublons d’emplacements
* Dupliquer des emplacements dans les publicitaires et campagnes d’origine ou dans des emplacements différents
* (Pour les emplacements dupliqués dans les campagnes d’origine) Vous pouvez éventuellement dupliquer les publicités d’origine.
* Modifier l’état et les dates de vol des nouveaux emplacements

Voir &quot;[Ce qui n’est pas dupliqué](#placement-not-duplicated)&quot; pour obtenir la liste des paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.
1. Cliquez sur le nom de la campagne.
1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.
1. Effectuez l’une des opérations suivantes :
   * Pour dupliquer un emplacement, cliquez sur **[!UICONTROL ...]>[!UICONTROL Duplicate]** en regard du nom du package.
   * Pour dupliquer plusieurs emplacements :
      1. Cochez la case en regard de chaque emplacement à dupliquer.
      1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Duplicate]**.
1. Spécifiez les nouveaux paramètres d’emplacement :
   1. (Emplacements uniques) Saisissez le nouveau nom de l’emplacement.
   1. Dans le menu **[!UICONTROL Choose Package (Required)]**, sélectionnez le package parent ou **[!UICONTROL No package]*.
   1. (Facultatif) Modifiez les paramètres par défaut.

   Les paramètres s’appliquent à tous les emplacements sélectionnés.

   Par défaut, les nouveaux emplacements sont destinés au type de publicité d’origine, sont attribués aux annonceurs et campagnes d’origine, ont des horaires de vol commençant le jour en cours, sont suspendus et n’incluent pas les publicités d’origine.

   Lorsque vous créez plusieurs emplacements, les nouveaux noms d’emplacement sont ajoutés avec un nombre, en séquence, à l’aide de la convention &quot;a0/>original_placement_name #N&lt;a1/&quot;, comme &quot;Mon emplacement #2&quot;.**

1. Cliquez sur **[!UICONTROL Submit]**.

## Ce qui n’est pas dupliqué {#placement-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués sauf :

* Paramètres d’expérience
* (Si vous modifiez les dates de vol) Planification publicitaire personnalisée
* (Si vous ne joignez pas de publicités) Pondération et planification des publicités personnalisées
* Emplacements par défaut pour les offres garanties par programmation (PG) et emplacements pour les offres [!UICONTROL Simple Ad Serving]
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Segments de niveau emplacement [!DNL DoubleVerify Authentic Brand Safety] (qui remplacent les segments de niveau annonceur)

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Création d’un emplacement](placement-create.md)
>* [Modifier un emplacement](placement-edit.md)
>* [Paramètres d’emplacement](placement-settings.md)

