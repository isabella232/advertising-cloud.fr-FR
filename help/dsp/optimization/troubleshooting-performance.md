---
title: Résolution des problèmes de performances
description: Référencez les problèmes de performances courants et voyez comment les résoudre.
feature: Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Résolution des problèmes de performances

| Problème | Cause possible | Actions à entreprendre |
| --- | --- | --- |
| Pas de dépenses en placement | L’emplacement n’inclut pas les publicités et/ou celles-ci ne sont pas principales. | Vérifiez que toutes les publicités attendues sont jointes à l’emplacement et qu’elles sont approuvées et principales.<br><br>Voir également si l’emplacement inclut un planning de publicité personnalisé, qui peut limiter la période d’envol de chaque publicité. Pour afficher la planification des publicités pour un emplacement à partir de la vue Emplacements, cliquez sur **[!UICONTROL ...]>[!UICONTROL Ad schedule]** en regard du nom de l’emplacement. |
|  | Les dates affectées ne se trouvent pas dans les dates de vol configurées. | Vérifiez que les dates de vol sont valides au niveau de la campagne, du package et de l’emplacement &#x200B;. |
|  | L&#39;objectif du budget a été atteint et/ou n&#39;est pas assez élevé. | Vérifiez les paramètres du budget aux niveaux de l&#39;opération, du kit et de l&#39;emplacement. |
|  | Le compte n&#39;a pas assez de financement. | Pour vérifier si votre compte est financé de manière adéquate, accédez à **[!UICONTROL Settings]>[!UICONTROL Account]** et observez le montant de [!UICONTROL Usable Funds]. Si vous devez ajouter d’autres fonds, contactez votre gestionnaire de compte d’Adobe. |
|  | Aucun inventaire n’est disponible. | Vérifiez si les sources d’inventaire spécifiées ([!UICONTROL Public], [!UICONTROL Private] ou [!UICONTROL On Demand]) sont les suivantes :<ul><li>Configurez correctement.</li><li>Principale et via des enchères.</li><li>Compatible avec la publicité et le type d’emplacement applicables.</li></ul><br>Si les sources d’inventaire sont toutes valides et principales, ciblez d’autres sources d’inventaire ou toutes les sources d’inventaire lorsque cela est possible. |
|  | Aucun utilisateur n’est disponible. | Vérifiez que les cibles d’audience spécifiées incluent suffisamment d’utilisateurs principaux. Dans le cas contraire, développez les cibles en ajoutant davantage d’audiences. |
| Faibles dépenses en placement | La section [!UICONTROL Non Bids] du rapport de diagnostic du placement indique les raisons possibles pour lesquelles l’emplacement n’a pas enchéri. | [Consultez le  [!UICONTROL Non Bids] ](/help/dsp/campaign-management/reports/placement-diagnostics.md) rapport pour comprendre pourquoi l’emplacement n’a pas enchéri.   <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | L’emplacement utilise des [filtres avant offre](/help/dsp/campaign-management/placements/placement-settings.md) qui limitent les offres. | Réduisez les seuils des filtres avant enchère de 5 % afin d’évaluer l’équilibre entre les dépenses et les performances. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres avant offre, les zones géographiques, l’inventaire et les audiences, peut limiter de manière cumulée les enchères et les dépenses. |
|  | Le placement a un taux de victoire faible. | Augmentez le [!UICONTROL Max Bid] pour améliorer le taux de victoire.<br><br><b>REMARQUE : </b> Les prix du stock peuvent varier en fonction du ciblage de l’emplacement.<br><br>Un taux de 10% de gain est considéré comme sain. |
|  | Un petit nombre d’inventaire est disponible. | Si possible, ciblez d’autres sources d’inventaire ou toutes les sources d’inventaire.<br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres avant offre, les zones géographiques, l’inventaire et les audiences, peut limiter de manière cumulée les enchères et les dépenses. |
|  | Un petit nombre d’utilisateurs est disponible. | Vérifiez que les cibles d’audience spécifiées incluent suffisamment d’utilisateurs principaux. Dans le cas contraire, développez les cibles en ajoutant davantage d’audiences.<br><br>Gardez à l’esprit que l’utilisation de plusieurs cibles d’emplacement, telles que les filtres avant offre, les zones géographiques, l’inventaire et les audiences, peut limiter de manière cumulée les enchères et les dépenses. |
|  | Le package comprend un grand nombre d’emplacements principaux. | Réduisez le nombre de principaux emplacements dans le package ou augmentez le budget global du package.<br><br>Si le package comporte de nombreux emplacements mais pas assez de budget, DSP peut ne pas être en mesure d’allouer suffisamment de budget à chaque emplacement. Chaque placement doit avoir la possibilité de dépenser au moins 2 USD/jour. Par exemple, si votre kit a un budget de 10 USD/jour, il est préférable d’inclure cinq emplacements ou moins. &#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md)

