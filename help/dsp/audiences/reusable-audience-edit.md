---
title: Modification d’une audience réutilisable
description: Découvrez comment modifier une audience réutilisable.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Modification d’une audience réutilisable

Lorsque vous modifiez une audience qui est utilisée dans n’importe quel emplacement ou autre audience réutilisable, les modifications sont immédiatement appliquées à ces emplacements et audiences.<!-- verify -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. Placez le curseur sur la ligne de l’audience et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les paramètres de l’audience de l’une des façons suivantes :

   >[!NOTE]
   >
   >Si vous modifiez la logique du segment d’audience, détaillée [données de taille d’audience](audience-about.md) est mis à jour dans le panneau de droite.

   * (Facultatif) Pour modifier la variable **[!UICONTROL Audience Name]** click ![Modifier](/help/dsp/assets/edit.png) en regard du nom de l’audience, saisissez un nom d’audience unique, puis cliquez sur **[!UICONTROL Apply]**.

   * (Facultatif) Pour modifier manuellement la logique de segment à l’aide des segments disponibles dans la variable [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], et [!UICONTROL Saved Audiences] onglets](audience-settings.md), procédez comme suit.

      * Pour ajouter un segment à un groupe de segments existant :
      1. Cliquez sur le groupe de segments dans le panneau de droite.

      1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

         *[!UICONTROL Exclude All]* n’est pas disponible pour le premier groupe de segments. Pour une audience qui ne comprend que des exclusions, définissez cette audience comme *[!UICONTROL Include Any]* puis, dans un emplacement, sélectionnez cette audience dans le menu Audiences exclues .

      1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

         Le groupe de segments est automatiquement mis à jour avec le nouveau segment.
   * Pour ajouter un nouveau groupe de segments :

      1. Cliquez sur **[!UICONTROL + New Group]** dans le panneau de droite.

      1. (Facultatif) Remplacez la logique entre le groupe précédent et le nouveau groupe par *[!UICONTROL And]* ou *[!UICONTROL Or]*, selon les besoins.

      1. Recherchez les segments du nouveau groupe dans le panneau de gauche, puis cochez les cases en regard des noms des segments.

      1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.
   * Pour utiliser la logique de segment d’une audience existante :

      1. Copiez la logique de segment de l’audience existante de l’une des façons suivantes :

         * Dans la vue Toutes les audiences, placez le curseur sur la ligne de l’audience, puis cliquez sur **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Dans les paramètres de l’audience existante, dans la partie supérieure du panneau de logique de segment, cliquez sur **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Dans un éditeur de texte, créez manuellement la logique de segment à l’aide des identifiants de segment alphanumériques et des [Syntaxe booléenne](audience-segment-logic-syntax.md)et copiez-le dans le presse-papiers.
      1. Cliquez sur **[!UICONTROL paste in an audience rule to begin building]**, collez la logique de segment existante dans le champ de saisie, puis cliquez sur **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Si l’audience comprend déjà une logique de segment, coller une nouvelle logique de segment remplace la logique existante.





1. Cliquez sur **[!UICONTROL Save]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Duplication d’une audience réutilisable](reusable-audience-duplicate.md)
>* [Affichage des détails sur une audience réutilisable](reusable-audience-view-details.md)
>* [Partage d’une audience réutilisable](reusable-audience-share.md)
>* [Exportation d’une audience réutilisable](reusable-audience-export.md)
>* [Copie de la clé de segment d’une audience réutilisable dans le Presse-papiers](reusable-audience-clipboard.md)
>* [Suppression d’une audience réutilisable](reusable-audience-delete.md)
>* [Paramètres d’audience](audience-settings.md)
>* [Syntaxe de la logique de segment d’audience](audience-segment-logic-syntax.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)

