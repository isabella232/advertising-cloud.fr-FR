---
title: Bonnes pratiques pour créer un objectif personnalisé
description: Découvrez les bonnes pratiques pour créer des objectifs personnalisés afin de définir vos événements de succès.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: 7cb39998041d151ece7809adc8a2e872b922e5fc
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Bonnes pratiques pour créer un objectif personnalisé

## Objectifs personnalisés avec une seule propriété

Les exemples suivants montrent comment configurer des objectifs qui ciblent une seule propriété (mesure).

### Exemple pour une campagne avec le[!UICONTROL Highest ROAS - Custom Goal]&quot;Objectif d’optimisation

Si l’objectif de votre campagne est les recettes ([!UICONTROL Highest ROAS - Custom Goal]), votre objectif personnalisé (objectif) comprend le paramètre &quot;[!UICONTROL Revenue]&quot; avec un poids d’un (1).

![exemple d’un objectif personnalisé ROAS avec une seule propriété](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de un équivaut à une valeur de un pour chaque $1 de recettes suivi.
>
> Par exemple, une conversion de 250 $ avec un poids de 1 est signalée comme étant de 250 $. Si la mesure de conversion se voit attribuer un poids de 0,5, la conversion de 250 $ est signalée comme étant de 125 $ dans Advertising Cloud (Conversion de 250 $ * 0,5). [!UICONTROL Property Weight] = 125 $).

### Exemple pour une campagne avec le[!UICONTROL Lowest CPA - Custom Goal]&quot;Objectif d’optimisation

Si l’objectif de votre campagne est le coût par acquisition le plus faible et qu’il ne nécessite qu’un seul événement de succès, vous allez inclure cette mesure (dans l’exemple suivant, &quot;Envoi de demande&quot;). La bonne pratique consiste à définir le poids sur un (1).

![exemple d’un objectif personnalisé CPA avec une seule propriété](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de un équivaut à une valeur de un pour chaque conversion suivie.
>
> Par exemple, si 10 conversions d’envoi de demande sont suivies, 10 conversions d’envoi de demande sont signalées.  Si la mesure de conversion se voit attribuer un poids de 0,5, les 10 conversions sont signalées comme étant de cinq (5) dans Advertising Cloud (10 conversions * 0,5). [!UICONTROL Property Weight] = 5).

## Objectifs personnalisés avec plusieurs propriétés

Il existe deux scénarios dans lesquels vous utiliseriez plusieurs propriétés dans un objectif personnalisé :

* L’objectif de votre campagne comporte plusieurs événements de succès. Par exemple, vous êtes peut-être publicitaire pour plusieurs actions sur site et toutes sont attribuées à votre objectif de CPA. L’exemple d’objectif suivant comprend trois propriétés distinctes (téléchargement de PDF, contact avec nous et inscription par e-mail), chacune d’elles ayant un poids d’une (1), qui indique à la variable [!DNL Adobe Sensei] que chacune des propriétés a une importance égale. Si vous incluez des propriétés dont les coûts ou l’importance sont variables, vous pouvez ajuster leur poids relatif en conséquence.

   ![exemple d’un objectif personnalisé avec plusieurs propriétés](/help/dsp/assets/custom-goal-multiple-properties.png)

* La propriété unique de votre objectif personnalisé n’atteint pas le minimum de 10 conversions par jour requis pour des performances optimisées. Cela peut se produire en raison de dépenses journalières minimales ou d’un nombre limité de conversions naturelles. L’ajout de propriétés de prise en charge supplémentaires à l’objectif personnalisé peut vous aider à atteindre le seuil de 10 conversions par jour. Dix événements de prise en charge peuvent aider un kit à atteindre le seuil de 10/jours, même si chaque poids est inférieur à un (1). Mais vous n’aurez peut-être pas besoin d’ajouter autant d’événements.

   Lorsque vous ajoutez des propriétés de prise en charge à un objectif personnalisé, pondérez-les en fonction de leur importance relative par rapport à l’événement de succès principal et gardez à l’esprit la quantité de points de données. Cela permet à l’algorithme Adobe Sensei d’équilibrer plusieurs propriétés et d’optimiser en fonction de votre objectif.

   L’exemple d’objectif suivant comprend trois propriétés, chacune ayant un poids différent : Envoi de l’application = 1, Démarrage de l’application = 0,1 et Page d’entrée des annonceurs = 0,01. Cela signifie que chaque conversion d’envoi de l’application a la même valeur pour votre entreprise qu’une moyenne de 10 conversions de démarrage de l’application et 100 conversions de page d’entrée des annonceurs.

   ![exemple d’un objectif personnalisé avec plusieurs propriétés](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Si, à la place, vous aviez pondéré les visites de page d’entrée de manière égale par rapport aux envois d’application, le nombre naturellement plus élevé de visites de page d’entrée pourrait dépasser votre objectif et augmenter le nombre de visites de page d’entrée.<!--reword-->

>[!MORELIKETHIS]
>
>* [À propos des objectifs personnalisés](custom-goal-about.md)
>* [Création d’un objectif personnalisé](custom-goal-create.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)

