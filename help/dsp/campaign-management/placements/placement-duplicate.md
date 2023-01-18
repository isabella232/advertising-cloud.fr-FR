---
title: Duplication de placements
description: Découvrez comment dupliquer un ou plusieurs emplacements.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Duplication de placements

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliquez un ou plusieurs emplacements pour créer des emplacements avec des paramètres similaires. Vous pouvez :

* Créer plusieurs doublons d’emplacements
* Dupliquer des emplacements dans les publicitaires et campagnes d’origine ou dans des emplacements différents
* (Pour les emplacements dupliqués dans les campagnes d’origine) Vous pouvez éventuellement dupliquer les publicités d’origine.
* Modifier l’état et les dates de vol des nouveaux emplacements

Voir &quot;[Ce qui n’est pas dupliqué](#placement-not-duplicated)&quot; pour une liste de paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Effectuez l’une des opérations suivantes :

   * Pour dupliquer un emplacement, cliquez sur  **[!UICONTROL ...]>[!UICONTROL Duplicate]** en regard du nom du module.

   * Pour dupliquer plusieurs emplacements :

      1. Cochez la case en regard de chaque emplacement à dupliquer.

      1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Duplicate]**.

1. Spécifiez les nouveaux paramètres d’emplacement :

   1. (Emplacements uniques) Saisissez le nouveau nom de l’emplacement.

   1. Dans le **[!UICONTROL Choose Package (Required)]** , sélectionnez le package parent ou **[!UICONTROL No package]*.

   1. (Facultatif) Modifiez les paramètres par défaut.

   Les paramètres s’appliquent à tous les emplacements sélectionnés.

   Par défaut, les nouveaux emplacements sont destinés au type de publicité d’origine, sont attribués aux annonceurs et campagnes d’origine, ont des horaires de vol commençant le jour en cours, sont suspendus et n’incluent pas les publicités d’origine.

   Lorsque vous créez plusieurs emplacements, les nouveaux noms d’emplacements sont ajoutés avec un nombre, dans l’ordre, à l’aide de la convention &lt;*original_placement_name #N*>, par exemple &quot;Mon emplacement #2.&quot;

1. Cliquez sur **[!UICONTROL Submit]**.

## Ce qui n’est pas dupliqué {#placement-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués sauf :

* Paramètres d’expérience
* (Si vous modifiez les dates de vol) Planification publicitaire personnalisée
* (Si vous ne joignez pas de publicités) Pondération et planification des publicités personnalisées
* Emplacements par défaut pour les offres (PG) garanties par programmation et emplacements pour [!UICONTROL Simple Ad Serving] transactions
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Niveau de placement [!DNL DoubleVerify Authentic Brand Safety] segments (qui remplacent les segments au niveau de l’annonceur)

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Création d’un emplacement](placement-create.md)
>* [Modifier un emplacement](placement-edit.md)
>* [Affichage du journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)

