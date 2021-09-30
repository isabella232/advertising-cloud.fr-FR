---
title: Filtres de pré-offre au niveau de l’emplacement et comment les utiliser
description: Référencez les filtres de pré-enchère au niveau de l’emplacement disponibles et découvrez comment les utiliser.
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: 75ec6f54271542d56e0d16fbb7aa92ebcf00d765
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Filtres de pré-offre au niveau de l’emplacement et comment les utiliser

| Filtre avant offre | Description | Quand utiliser ce filtre |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Définit un seuil de prédiction minimal pour la probabilité qu’une vente aux enchères entraîne un clic publicitaire. Par exemple, si vous définissez le seuil sur 0,1 %, vous n’enchérisserez pas lors d’une enchère, sauf si la probabilité prévue d’un clic est supérieure ou égale à 0,1 %.<br><br><b>Remarque :</b>  Les filtres sont appliqués avant les objectifs d’optimisation. Par conséquent, des filtres très stricts peuvent empêcher les dépenses. | Utilisez cette option lorsque vous disposez d’un objectif d’indicateur de performance clé minimal pour le taux de clics (CTR) et que vous ne souhaitez pas dépenser votre budget lorsque le CTR est inférieur au seuil. Ce filtre peut être très restrictif, il est donc important de définir des objectifs réalistes. Selon d’autres restrictions sur l’emplacement, un objectif de 0,03 à 0,07 % est généralement un bon point de départ. Vous pouvez l’optimiser au niveau du site, si nécessaire, afin d’améliorer les mesures.<br><br>Si votre objectif est d’atteindre un taux de clics minimal et le meilleur taux de clics possible, la configuration recommandée consiste à combiner un  [!UICONTROL Click Through Rate] filtre avec l’objectif d’optimisation &quot;[!UICONTROL Lowest CPM]&quot;. Si votre objectif est un CPM maximal sans avantage réel pour l’excès de performances et un CTR minimal, l’association d’un filtre [!UICONTROL Click Through Rate] avec l’objectif d’optimisation &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; peut s’avérer plus appropriée. |
| [!UICONTROL 100% Completion Rate] | Définit un taux d’achèvement minimal requis qui doit être atteint avant que vous n’enchériez sur une impression. | Utilisez ce filtre lorsque le principal objectif de la campagne est les taux d&#39;achèvement. Facteur dans d’autres paramètres de ciblage, mais 65 % est le pourcentage de départ recommandé. |
| [!UICONTROL Player Size - Adobe] | Définit la taille minimale requise du lecteur à l’aide des données d’Advertising Cloud DSP. Vous enchérirez sur une impression lorsque le seuil [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous effectuez une diffusion sur l’inventaire du lecteur d’épisodes complet à l’aide des données de DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Définit une taille minimale de lecteur requise, à l’aide des données de [!DNL Moat] ou [!DNL Integral Ad Science] ([!DNL IAS]). Vous enchérirez sur une impression lorsque le seuil [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous effectuez une diffusion sur l’inventaire complet du lecteur d’épisodes à l’aide des données [!DNL Moat] ou [!DNL IAS] de l’ensemble de la plateforme.<br><br><b>Remarque :</b> utilisez ce filtre uniquement lorsque la campagne est configurée pour utiliser  [!DNL Moat] ou  [!DNL IAS] des données. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Définit un pourcentage minimum de visibilité requis, à l’aide des valeurs et mesures de visibilité d’Advertising Cloud DSP. Vous proposerez une impression lorsque le seuil spécifié sera atteint.<br><br><b>Remarques :</b><ul><li>Si le paramètre [!UICONTROL Viewability Sensitivity] de la campagne est &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, la norme de mesure de la visibilité [!DNL Media Rating Council] (MRC) est utilisée pour la campagne. Si le paramètre [!UICONTROL Viewability Sensitivity] est &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, la [!DNL GroupM] norme de mesure de la visibilité est utilisée pour la campagne.</li><li>Les définitions des mesures d’Adobe diffèrent des définitions tierces. Il peut donc y avoir de légères incohérences avec les données tierces.</li></ul> | La bonne pratique consiste à correspondre à l’objectif d’optimisation et aux paramètres de filtre pré-enchère avec le paramètre [!UICONTROL Viewability Sensitivity] de la campagne. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)

