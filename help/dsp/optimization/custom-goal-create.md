---
title: Création d’un objectif personnalisé
description: Création d’un objectif personnalisé
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Création d’un objectif personnalisé

Vous pouvez créer des objectifs personnalisés sous la forme *objectifs* dans [!DNL Adobe Advertising Search].

Pour créer un objectif personnalisé, le compte DSP doit être associé à un [!DNL Search] avec le même ID d’organisation Adobe Experience Cloud, depuis le [!DNL Search] paramètres du client. Si votre compte DSP n’est pas lié à un [!DNL Search] , contactez votre [!DNL Adobe] l&#39;équipe du compte.

>[!TIP]
>
>Voir [bonnes pratiques pour la création d’objectifs personnalisés](custom-goal-best-practices.md) pour obtenir des conseils sur la configuration de vos objectifs personnalisés.

1. Se connecter [!DNL Adobe Advertising Search] at (entreprises américaines) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (sociétés dans tous les autres pays) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont été suivies, sont disponibles dans le produit et incluez un nom d’affichage :
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Recherchez la mesure et assurez-vous que la variable **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.
   1. Si la mesure ne contient pas de valeur dans la variable **[!UICONTROL Display Name]** , cliquez dans la cellule, saisissez le nom d’affichage, puis cliquez sur **[!UICONTROL Apply].**
1. Créez l’objectif personnalisé en tant que *objectif*:
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Create objective].**
   1. Renseignez les paramètres de l&#39;objectif :
      1. Dans le **[!UICONTROL Change Objective Name]** , saisissez le nom de l’objectif.

         Le nom de l’objectif s’affiche dans la [!UICONTROL Custom Goals] dans les paramètres du module DSP.

      1. Associez les propriétés à l’objectif :

         >[!NOTE]
         >
         > Toutes les propriétés de transaction suivies pour l’annonceur sont répertoriées par défaut dans la variable [!UICONTROL Available Properties] liste.

         * Pour importer un fichier CSV avec des propriétés et leur poids, cliquez sur **[!UICONTROL Import]** et localisez le fichier à importer.

            Les propriétés importées doivent déjà exister pour l’annonceur ; les noms ne sont pas sensibles à la casse.

            Les propriétés importées remplacent toutes les propriétés existantes spécifiées.

         * Pour spécifier manuellement la première propriété avec le poids par défaut (1), sélectionnez dans la liste de toutes les propriétés de transaction suivies pour l’annonceur.

         * Pour ajouter manuellement une autre propriété avec le poids par défaut (1), cliquez sur **[!UICONTROL +]** .

            >[!TIP]
            >
            > Pour rechercher une propriété dans la liste, saisissez une chaîne n’importe où dans le nom de la propriété.

         * Pour ajouter manuellement plusieurs propriétés, cliquez sur **[!UICONTROL Add Multiple Properties].** Pour chaque propriété à ajouter, cliquez sur le nom de la propriété dans la variable [!UICONTROL Available Properties] et faites-le glisser dans la [!UICONTROL Added Properties] colonne . Lorsque vous avez terminé d’ajouter des propriétés, cliquez sur **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Pour rechercher une propriété dans la liste, saisissez une chaîne n’importe où dans le nom de la propriété dans le champ de saisie.
            >* Pour filtrer la liste afin d’exclure les propriétés qui sont exclues dans les rapports, sélectionnez l’option . **[!UICONTROL Hide properties excluded from reports].**


         * (Lorsque l’objectif contient plusieurs propriétés) Pour modifier le poids d’une propriété par rapport aux autres propriétés de l’objectif, saisissez des valeurs dans la variable **[!UICONTROL Weight]** champ(s).
      1. Au bas des paramètres, cliquez sur **[!UICONTROL Save]**.


Une fois que vous avez créé un objectif, vous pouvez l’affecter à un module DSP en tant qu’objectif personnalisé lorsque l’objectif d’optimisation est &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Pour des performances optimales, les mesures combinées de l’objectif personnalisé (objectif) doivent totaliser au moins dix conversions par jour. Dans le cas contraire, la bonne pratique consiste à ajouter à l’objectif des événements de prise en charge supplémentaires (propriétés de transaction), tels que des pages de produit ou des démarrages d’application. Voir [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md) pour obtenir des instructions.

>[!MORELIKETHIS]
>
>* [À propos des objectifs personnalisés](custom-goal-about.md)
>* [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)

