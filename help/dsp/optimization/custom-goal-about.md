---
title: À propos des objectifs personnalisés
description: Découvrez les objectifs personnalisés pour définir vos événements de succès dans des modules optimisés pour le CPA le plus bas ou le ROAS le plus élevé.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# À propos des objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque module qui utilise les objectifs d’optimisation &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; doit inclure un objectif personnalisé qui permettra d’atteindre l’objectif d’optimisation général. Vous pouvez créer des objectifs personnalisés sous la forme *objectifs* in [!DNL Adobe Advertising Search].

![objectifs personnalisés](/help/dsp/assets/objective-goals.png)

Chaque objectif personnalisé comprend une ou plusieurs mesures, ou *propriétés de transaction* et les poids relatifs de ces propriétés de transaction. Les propriétés de transaction disponibles incluent toutes les mesures suivies à l’aide du pixel de conversion Adobe Advertising et par le biais d’Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] les dimensions et les segments ne sont pas disponibles pour l’optimisation Adobe Advertising.
>* Pour utiliser les événements Analytics dans DSP, utilisez [!DNL Adobe] l’équipe du compte pour configurer une intégration au niveau de l’annonceur.
>* [!DNL Analytics] les événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`


Supposons, par exemple, que trois mesures (propriétés de transaction) soient pertinentes pour un module spécifique dans l’une de vos campagnes : &quot;Téléchargement PDF&quot; d’une valeur de 20 USD, &quot;Inscription par e-mail&quot; d’une valeur de 30 USD et &quot;Confirmation de commande&quot; d’une valeur de 40 USD. Si vous souhaitez donner du poids en fonction de la valeur monétaire ponctuelle de l’action du client, le poids relatif des propriétés est de 1, 2 et 1,5.

Voir [bonnes pratiques pour la création d’objectifs personnalisés](custom-goal-best-practices.md) pour obtenir des conseils sur la configuration de vos objectifs personnalisés.

Une fois que [créer un objectif personnalisé ;](custom-goal-create.md), vous pouvez [l’affecter à un module](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide d’Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Création d’un objectif personnalisé](custom-goal-create.md)
>* [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)

