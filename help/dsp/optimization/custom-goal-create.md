---
title: Création d’un objectif personnalisé
description: Création d’un objectif personnalisé
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Création d’un objectif personnalisé

>[!TIP]
>
>Pour obtenir des conseils sur la configuration de vos objectifs personnalisés, voir [ bonnes pratiques relatives à la création d’objectifs personnalisés.](custom-goal-best-practices.md)

1. Connectez-vous à Advertising Cloud Search à l’adresse (entreprises américaines) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (entreprises de tous les autres pays) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont été suivies, sont disponibles dans le produit et incluez un nom d’affichage :
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Recherchez la mesure et assurez-vous que **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.
   1. Si la mesure ne contient pas de valeur dans la colonne **[!UICONTROL Display Name]**, cliquez dans la cellule, saisissez le nom d’affichage, puis cliquez sur **[!UICONTROL Apply].**
1. Créez l’objectif personnalisé en tant qu’ *objectif* :
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Create objective].**
   1. Renseignez les paramètres de l&#39;objectif :
      1. Dans le champ **[!UICONTROL Change Objective Name]**, saisissez le nom de l&#39;objectif.

         Le nom de l&#39;objectif s&#39;affiche dans la liste [!UICONTROL Custom Goals] des paramètres du package Advertising Cloud DSP.

      1. Associez les propriétés à l’objectif :

         >[!NOTE]
         >
         > Toutes les propriétés de transaction suivies pour l’annonceur sont répertoriées par défaut dans la liste [!UICONTROL Available Properties].

         * Pour importer un fichier CSV avec des propriétés et leur poids, cliquez sur **[!UICONTROL Import]** et localisez le fichier à importer.

            Les propriétés importées doivent déjà exister pour l’annonceur ; les noms ne sont pas sensibles à la casse.

            Les propriétés importées remplaceront toutes les propriétés existantes spécifiées.

         * Pour spécifier manuellement la première propriété avec le poids par défaut (1), sélectionnez dans la liste de toutes les propriétés de transaction suivies pour l’annonceur.

         * Pour ajouter manuellement une autre propriété avec le poids par défaut (1), cliquez sur **[!UICONTROL +]** .

            >[!TIP]
            >
            > Pour rechercher une propriété dans la liste, saisissez une chaîne n’importe où dans le nom de la propriété.

         * Pour ajouter manuellement plusieurs propriétés, cliquez sur **[!UICONTROL Add Multiple Properties].** Pour chaque propriété à ajouter, cliquez sur le nom de la propriété dans la  [!UICONTROL Available Properties] colonne et faites-la glisser dans la  [!UICONTROL Added Properties] colonne. Lorsque vous avez terminé d’ajouter des propriétés, cliquez sur **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Pour rechercher une propriété dans la liste, saisissez une chaîne n’importe où dans le nom de la propriété dans le champ de saisie.
            >* Pour filtrer la liste afin d’exclure les propriétés qui sont exclues dans les rapports, sélectionnez l’option **[!UICONTROL Hide properties excluded from reports].**


         * (Lorsque l’objectif contient plusieurs propriétés) Pour modifier le poids d’une propriété par rapport aux autres propriétés de l’objectif, saisissez des valeurs dans le ou les champs **[!UICONTROL Weight]**.
      1. Au bas des paramètres, cliquez sur **[!UICONTROL Save]**.


Une fois que vous avez créé un objectif, vous pouvez l’affecter à un package Advertising Cloud DSP en tant qu’objectif personnalisé lorsque l’objectif d’optimisation est &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;.

>[!TIP]
>
>Pour des performances <!-- optimum? Or optimization won't happen at all w/out it? -->optimisées, les mesures combinées dans l’objectif personnalisé (objectif) doivent totaliser au moins 10 conversions par jour. Dans le cas contraire, la bonne pratique consiste à ajouter à l’objectif des événements de prise en charge supplémentaires (propriétés de transaction), tels que des pages de produit ou des démarrages d’application. Voir [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md) pour obtenir des instructions.

>[!MORELIKETHIS]
>
>* [À propos des objectifs personnalisés](custom-goal-about.md)
>* [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)

