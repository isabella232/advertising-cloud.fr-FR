---
title: Paramètres du module
description: Voir la description des paramètres de package disponibles.
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Paramètres du module

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** nom du module. La longueur maximale est de 60 caractères.

**[!UICONTROL Description]:**  (facultatif) description du package.

**[!UICONTROL 3rd Party Billed Fees]:**  (Facultatif) Frais tiers statiques à suivre en tant que coût non facturable :

>[!NOTE]
>
>Les frais facturables sont pris en compte dans la mesure [!UICONTROL Net CPM].
* **[!UICONTROL CPM]:** coût par 1 000 impressions (CPM).

* **[!UICONTROL CPM Description]:** description des frais CPM.

Vous pouvez remplacer le paramètre de niveau package au [niveau d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:**  (lecture seule pour les modules existants) À quel niveau placer et limiter les emplacements dans le module :

* **[!UICONTROL Package level pacing]:** Cette stratégie de rythme fonctionne en effectuant un suivi et en plafonnant tous les emplacements inclus en tant que  *groupe*. Cette stratégie garantit que tous les emplacements d’un package donné sont optimisés de manière holistique, en répartissant les dépenses en fonction des performances et de l’échelle avec certains indicateurs clés de performance (IPC).

* **[!UICONTROL Placement level pacing]:**  Cette stratégie de rythme fonctionne en effectuant un suivi et en plafonnant tous les emplacements inclus  *individuellement*. La bonne pratique consiste à utiliser cette stratégie uniquement pour exécuter des marchés privés garantis.

**[!UICONTROL Flight Dates]:** date de début et date de fin du package.

Pour créer éventuellement des vols de fréquence variable pour le package, sélectionnez *[!UICONTROL *Activate Custom Flighting]** et configurez les vols personnalisés dans la section [!UICONTROL Flighting] ci-dessous. Une fois que vous avez activé le vol personnalisé et enregistré le package, vous ne pouvez pas désactiver le vol personnalisé.

>[!NOTE]
>
>* Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération. De plus, les dates de vols de tous les emplacements affectés à ce package doivent être incluses dans ces dates.
> * Vous ne pouvez pas modifier la date de début du module lorsque l’éclairage personnalisé est activé.


**[!UICONTROL Budget]:**  (Modules avec une fréquence au niveau des packages uniquement) Le plafond budgétaire brut et l’intervalle de budget.

Pour les packages avec un vol personnalisé, l’intervalle de budget est toujours *[!UICONTROL All time]*. Pour les packages sans vol personnalisé, spécifiez l’intervalle de budget : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:**  (Modules avec package et gestion dynamique des marges uniquement) Le budget brut maximum pour la durée du package.

**[!UICONTROL Optimization Goal]:**  (Modules avec un rythme au niveau du module uniquement) L’objectif d’optimisation du module. Consultez les descriptions de chaque objectif d’optimisation à l’adresse [Objectifs d’optimisation et Comment les utiliser](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:**  (Modules avec objectifs d’optimisation personnalisés uniquement)  [Objectif ](/help/dsp/optimization/custom-goal-about.md) personnalisé du module. Pour plus d’informations sur les bonnes pratiques relatives aux objectifs personnalisés et aux campagnes qui les utilisent, voir [Bonnes pratiques relatives à la création d’un objectif personnalisé](/help/dsp/optimization/custom-goal-best-practices.md) et [Bonnes pratiques relatives à la configuration des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:**  (Modules avec objectifs d’optimisation personnalisés uniquement) L’objectif du module. Ce paramètre permet de déterminer comment optimiser le module :

* *[!UICONTROL Prospecting]:* les packages de prospection se concentrent sur l&#39;acquisition de nouveaux clients.

* *[!UICONTROL Retargeting]:* les modules de reciblage se concentrent sur la réexposition des visiteurs ou clients précédents.

* *[!UICONTROL Other]:* Tous les autres usages.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:**  (Modules avec objectifs d’optimisation personnalisés uniquement) Autre module dont les données historiques sont utilisées comme entrée pour optimiser le module.

**[!UICONTROL Target]:**  (Modules avec une fréquence au niveau du module uniquement) Objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Frequency Cap]:**  (Modules avec une fréquence au niveau du module uniquement) Le nombre de fois où un appareil ou une personne unique (selon la valeur spécifiée  [!UICONTROL Cross Device Level]) peut être affiché dans les publicités à partir du module. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
>* Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respecte la limite de fréquence la plus stricte de la hiérarchie de l&#39;opération.
>* La bonne pratique consiste à définir des limites de fréquence pour la prospection et le reciblage au niveau du package.
> * Des plafonds de fréquence plus élevés se traduisent par des dépenses et des impressions plus élevées, mais une portée moindre. Les limites de fréquence plus basses se traduisent par des dépenses et des impressions plus faibles, mais une portée plus élevée.


**[!UICONTROL Pace on]:**  (Modules avec un espacement au niveau du module uniquement) Quel est le rythme basé sur :

* *[!UICONTROL Budget]:*  (Par défaut) Cette option permet d’effectuer autant d’impressions que possible dans le budget alloué du package.

* *[!UICONTROL Impressions]:* cette option livre des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte au cours d’un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *Tout le temps,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Pacing Fill Strategy]:**  (Modules avec une fréquence au niveau du package uniquement) Comment accélérer la diffusion et :

* *[!UICONTROL Even]* Effectue un espacement uniforme dans chaque vol, avec une cible de 50 % de la diffusion dans la première moitié du vol.

* *[!UICONTROL Slightly Ahead]:*  (valeur par défaut) accélère la diffusion, de sorte qu’elle se termine à 55-65 % à mi-chemin de la durée du vol.

* *[!UICONTROL Frontload]:* accélère la diffusion pour qu’elle soit de 65 à 75 % à mi-chemin du vol.

* *[!UICONTROL Aggressive Frontload]:* accélère la diffusion pour qu’elle soit de 75 à 85 % à mi-chemin du vol.

## [!UICONTROL Flighting]

(Modules avec une fréquence au niveau du module et avec &quot;[!UICONTROL Activate Custom Flighting]&quot; activé) Périodes de vol personnalisées dans la [!UICONTROL Flight Dates] globale spécifiée dans la section [!UICONTROL Goals & Budget].

Pour chaque vol, indiquez la date de début, la date de fin et le nombre cible d&#39;impressions. Pour ajouter un autre vol, cliquez sur **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de modules](package-about.md)
>* [Création d’un module](package-create.md)
>* [Modification d’un module](package-edit.md)
>* [Joindre un emplacement à un package](package-attach-placement.md)
>* [Questions fréquentes sur la gestion des campagnes](/help/dsp/campaign-management/campaign-management-faq.md)

