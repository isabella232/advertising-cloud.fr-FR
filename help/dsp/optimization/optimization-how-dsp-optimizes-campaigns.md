---
title: Optimisation des campagnes par DSP
description: Découvrez comment DSP optimise les packages dans vos campagnes.
feature: Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Optimisation des campagnes par DSP

Cette page décrit comment le moteur d’optimisation Advertising Cloud DSP, optimisé par [!DNL Adobe Sensei], optimise les modules de vos campagnes. Pour obtenir des conseils et des astuces sur l’optimisation manuelle de vos campagnes, contactez votre gestionnaire de compte Adobe. <!-- add link to trading playbook if we add it to help -->

Les objectifs d’optimisation des packages fonctionnent à deux niveaux :

* Pour chaque package : DSP alloue le budget à chaque emplacement dans le package en fonction des performances de l’emplacement par rapport à l’indicateur de performance clé sélectionné.

* Pour chaque emplacement/mise aux enchères dans le kit : DSP calcule la valeur en temps réel des indicateurs de performance clés économiques pour chaque enchère, puis utilise cette valeur pour déterminer l’offre.

   >[!NOTE]
   >
   >La valeur économique peut être fortement pondérée en fonction de la qualité des dépenses d&#39;un placement. Si un placement est derrière son objectif de dépense, il sera alors autorisé à acheter des enchères de moindre qualité. Si un placement atteint facilement son objectif de dépense, il se concentrera sur des enchères de meilleure qualité.

## Optimisation des packages

DSP peut optimiser votre diffusion de deux manières fondamentales, avec 20 variations disponibles pour correspondre à votre objectif de performances spécifique. Vous pouvez choisir entre :

* Définir la priorité du taux de performance

* Donner la priorité à l’équilibrage de l’efficacité des coûts avec le taux de performance

Voir [Objectifs d’optimisation et Comment les utiliser](optimization-goals.md) pour déterminer quel objectif d’optimisation vous aidera à atteindre vos IPC.

### Packages qui donnent la priorité au taux de performance

Pour les objectifs d’optimisation qui donnent la priorité au taux de performance, DSP prédit les performances de chaque enchère et toujours les offres à l’offre maximale. [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], etc. sont des exemples d’objectifs d’optimisation applicables.

Ce mode d’optimisation fonctionne bien si :

* Vous connaissez déjà le niveau de CPM effectif/acceptable (par exemple, une référence historique).

* Vous êtes prêt à ajuster manuellement la balise [!UICONTROL Max Bid] de chaque emplacement si vous rencontrez des problèmes de mise à l’échelle.

* Vous privilégiez l&#39;échelle par rapport à l&#39;efficacité.

#### Logique de traitement {#pacing-logic-performance}

* Si les dépenses suivent le rythme, les enchères deviendront plus sélectives, de sorte que vous n&#39;enchérisserez que sur les enchères prédites à des taux de performance élevés.

* Si les dépenses sont en retard, les enchères deviendront moins sélectives, de sorte que vous enchérisserez sur les enchères prédites avoir des taux de performance plus bas afin de rattraper l&#39;objectif de rythme.

#### Effacement de l’ombrage du prix/de l’offre {#clearing-price-performance}

Après avoir exécuté la logique de rythme, DSP exécute l’offre proposée par le biais d’un modèle de prévision de prix de compensation. Si la prévision indique que l’offre peut être réduite avec une baisse minimale du taux de victoire, l’offre est décrémentée selon la prévision.

### Packages qui donnent la priorité à l’équilibrage de l’efficacité des coûts avec le taux de performance

Pour certains objectifs d’optimisation, DSP prédit les performances de chaque enchère et ajuste automatiquement les prix de l’offre, sans dépasser la valeur [!UICONTROL Max Bid] d’un emplacement. [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], etc. sont des exemples d’objectifs d’optimisation applicables.

#### Logique de traitement {#pacing-logic-balanced}

* Si les dépenses suivent le rythme, DSP deviennent alors plus sensibles aux prix, offrant des montants plus bas pour échanger le taux de victoire avec le plan de rattrapage.

* Si une mesure de performance est également en cours d’équilibrage (tous les objectifs sauf [!UICONTROL Lowest CPM]), l’indicateur de performance clé prédit est fusionné dans le montant de l’offre. Par conséquent, vous proposez une offre plus élevée pour les enchères qui devraient être plus performantes selon le &quot;coût par&quot;.

* Si les dépenses sont en retard, DSP devient moins sensible aux prix et propose des montants plus élevés, jusqu&#39;à [!UICONTROL Max Bid], pour équilibrer le taux de victoire avec le plan de rythme.

#### Effacement de l’ombrage du prix/de l’offre {#clearing-price-balanced}

Après avoir exécuté la logique de rythme, DSP exécute l’offre proposée par le biais d’un modèle de prévision de prix de compensation. Si la prévision indique que l’offre peut être réduite avec une baisse minimale du taux de victoire, l’offre est décrémentée selon la prévision.

## Optimisation du placement

Les filtres de pré-enchère de placement constituent la méthode la plus stricte pour garantir des performances élevées. DSP utilise des filtres de pré-enchère de manière stratégique sur différents types d’annonces afin d’atteindre des objectifs de performances à l’échelle des emplacements dans chaque module. Vous pouvez utiliser des filtres avant offre simultanément avec une optimisation au niveau du package ou indépendamment.

>[!NOTE]
>
>Les filtres de pré-enchères disponibles varient en fonction du type de publicité. Par exemple, pour un emplacement d’affichage standard, vous pouvez filtrer par taux de clics publicitaires et visibilité, mais pas par taux d’achèvement.

Voir [Filtres de pré-offre de niveau emplacement et Comment les utiliser](optimization-pre-bid-filters.md) pour déterminer quel filtre de pré-offre vous aidera à atteindre vos IPC.

>[!MORELIKETHIS]
>
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Filtres de pré-offre au niveau de l’emplacement et comment les utiliser](optimization-pre-bid-filters.md)
>* [Résolution des problèmes de performances](/help/dsp/optimization/troubleshooting-performance.md)

