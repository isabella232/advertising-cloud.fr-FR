---
title: Solutions multi-appareils
description: En savoir plus sur les fonctionnalités multi-appareils.
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---

# Solutions multi-appareils

Intégrations Advertising Cloud DSP avec [!DNL LiveRamp] et [!DNL Adobe Device Co-op] vous permettent d’étendre votre audience à tous les appareils connus d’une personne, et pas seulement aux appareils suivis par votre marque. Les intégrations permettent également de limiter les fréquences et de mesurer l’attribution sur tous les appareils.

Lorsque vous utilisez un graphique d’appareil basé sur les personnes pris en charge, vous pouvez :

* Faire correspondre les audiences sur les canaux et les appareils pour diffuser des publicités aux personnes et aux ménages, plutôt qu’aux appareils.
* Équilibrer l’exposition en comprenant et en plafonnant la fréquence entre les individus.
* Stratégies de test qui exposent ou convertissent des audiences sur plusieurs canaux ou appareils.

## Avantages de chaque représentation graphique des appareils

* [!DNL Adobe Device Co-op]:
   * Fournit un pool d’inclusion des données déterministes et probabilistes des annonceurs Adobes participants
   * Fournit des connexions d’ID de cookie fiables optimisées par les visiteurs web de bureau et mobiles
   * Inclut principalement des données provenant des États-Unis et du Canada
   * Sans frais d’utilisation

* [!DNL LiveRamp] Device Graph :
   * Fournit un pool de données déterministes, y compris les données client hors ligne.
   * Offre une couverture égale entre les ID de cookie et les ID d’appareils mobiles
   * Inclut principalement des données provenant des États-Unis
   * Est gratuit pour le plafonnement des fréquences et la mesure d’attribution
   * Le prix de l’impression étendue (impressions diffusées uniquement en utilisant la variable [!DNL LiveRamp] Graphique d’appareil plutôt que sur les appareils trouvés dans les segments d’audience ciblés)

      Le taux est répercuté sur votre carte de taux de compte.

## Gestion des fréquences basée sur les personnes

La gestion des fréquences basée sur les personnes vous permet de spécifier des limites de fréquence au niveau de la personne, plutôt qu’au niveau de l’appareil, pour un véritable contrôle de l’exposition aux médias.

### Activation de la gestion des fréquences basée sur les personnes

* **Campagnes :** Lorsque vous créez une campagne, vous pouvez spécifier une [!UICONTROL Cross-Device Level] . Activer &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; et sélectionnez une représentation graphique des appareils. Le graphique d’appareil spécifié est utilisé pour le ciblage entre appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes au niveau de la campagne, du package et de l’emplacement. Les limites de fréquence s’appliquent à tous les périphériques connus d’une personne.

Pour plus d’informations, voir [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Une fois une campagne enregistrée, vous ne pouvez pas la modifier. [!UICONTROL Cross Device Level] .

* **Packages :**  Vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau du package. DSP respectera le plafond de fréquence le plus strict de la hiérarchie de l&#39;opération.

* **Emplacements :** Vous pouvez éventuellement définir des limites de fréquence supplémentaires au niveau de l’emplacement. DSP respectera le plafond de fréquence le plus strict de la hiérarchie de l&#39;opération.

## Ciblage basé sur les personnes

Le ciblage basé sur les personnes vous permet de trouver des clients sur les ordinateurs de bureau et les appareils mobiles.

### Activation du ciblage basé sur les personnes

* **Campagnes :** Lorsque vous créez une campagne, vous pouvez spécifier une [!UICONTROL Cross-Device Level] . Activer &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot; et sélectionnez une représentation graphique des appareils. Le graphique d’appareil spécifié est utilisé pour le ciblage entre appareils au niveau de l’emplacement et pour la gestion des fréquences basée sur les personnes.

Pour plus d’informations, voir [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Emplacements :** Lorsque vous sélectionnez des cibles d’audience pour un emplacement dans une campagne avec une représentation graphique spécifique des appareils, une [!UICONTROL Cross-Device Targeting] permet d’étendre le ciblage sur tous les appareils connus d’une personne (selon la représentation graphique des appareils spécifiée dans les paramètres de campagne), y compris sur les appareils qui ne figurent pas dans les segments spécifiés.

### Configuration des rapports pour le ciblage basé sur les personnes

Vous pouvez inclure les mesures suivantes dans les rapports personnalisés :

* **Impressions étendues :** (Dans la variable [!UICONTROL Build Your Report] sous [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) Le volume d’impressions incrémentielles diffusées en utilisant une représentation graphique des appareils (qui est introuvable dans les segments d’audience d’origine). Cette mesure est également utilisée pour calculer les frais applicables associés à l’utilisation d’une représentation graphique des appareils tiers.

   Pour déterminer le coût de vos impressions étendues au cours d’une période, exécutez un rapport personnalisé qui comprend la variable [!UICONTROL Extended Impressions] puis multipliez le nombre total d’impressions étendues par 0,00035 $ (0,35/1000 impressions).

   Le coût agrégé est également inclus dans la variable [!UICONTROL Billable Other Net Spend] (sous [!UICONTROL Metrics] > [!UICONTROL Spend]), bien que cette mesure inclut également d’autres frais de campagne que vous avez peut-être ajoutés.

* **Device Graph :** (Dans la variable [!UICONTROL Build Your Report] sous [!UICONTROL Dimensions] > [!UICONTROL Campaign]) Graphique d’appareil sélectionné pour une campagne, un package ou un emplacement spécifique.

## Mesure d’attribution basée sur les personnes

*Annonceurs avec suivi des conversions Advertising Cloud uniquement*

Avec l’attribution basée sur les personnes, vous pouvez attribuer des conversions qui ont eu lieu sur un appareil différent de celui sur lequel l’exposition au média s’est produite. La mesure d’attribution basée sur les personnes est disponible dans DSP, Advertising Cloud Search et Advertising Cloud Creative pour les annonceurs qui ont implémenté des pixels de conversion Advertising Cloud sur leurs sites.

### Activation de la mesure d’attribution basée sur les personnes

Si vous souhaitez activer la mesure d’attribution entre appareils, contactez votre [!DNL Adobe] l&#39;équipe du compte. Pour [!DNL Adobe Device Co-op] , vous devrez fournir vos [!DNL Adobe Device Co-op] le contrat et l’ID d’organisation de votre Experience Cloud (anciennement appelé [!DNL IMS org ID]).

Pour savoir si un compte publicitaire est configuré pour utiliser un graphique d’appareil pour la mesure d’attribution :

1. Dans le menu principal, cliquez sur **[!UICONTROL Settings]>[!UICONTROL Advertiser]**.
1. Placez le curseur sur la ligne de l’annonceur et cliquez sur **[!UICONTROL Edit]**.
1. Dans le [!UICONTROL Integrations] dans les paramètres de l’annonceur, voir si la variable [!UICONTROL Cross-Device Attribution] est principal.

   Pour les intégrations principales, la représentation graphique des appareils est indiquée.

### Configuration des rapports de conversion pour l’attribution des conversions entre appareils

#### Paramètres du rapport de conversion

Lorsqu’un graphique d’appareil est activé pour la mesure d’attribution, la variable [!UICONTROL Conversion] Le rapport comprend un [!UICONTROL Cross-Device Breakout] qui vous permet d’inclure jusqu’à trois colonnes distinctes pour chaque mesure de conversion, notamment :

* &lt;*Conversion*>[!UICONTROL (tp)]: Inclut le nombre total de conversions (nombre total de personnes), qui comprend à la fois les conversions sur le même appareil et les conversions sur plusieurs appareils (le cas échéant). Dans le rapport, &quot;[!UICONTROL (tp)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(tp)).

* &lt;*Conversion*>[!UICONTROL (sd)]: (Facultatif) Inclut uniquement les conversions pour lesquelles un seul appareil a été suivi dans le chemin de conversion. Dans le rapport, &quot;[!UICONTROL (sd)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(sd)).

* &lt;*Conversion*>[!UICONTROL (xd)]: (Facultatif) Inclut uniquement les conversions pour lesquelles plusieurs appareils ont été suivis dans le chemin de conversion. Dans le rapport, &quot;[!UICONTROL (xd)]&quot; est ajouté au nom de la mesure de conversion, au type de règle et aux types de conversion dans le chemin de conversion (par exemple, &quot;Réponses(le)(tl)(xd)).

#### Interprétation du rapport de conversion

Si vous triez le pourcentage total de conversions qui sont multi-appareils ([!UICONTROL (xd)]/[!UICONTROL (tl)]) de haut en bas, vous comprendrez ce qui génère des conversions entre appareils supérieures à la moyenne. Vous pouvez l’utiliser pour informer votre stratégie de création ou de ciblage afin de mettre en correspondance la messagerie et l’investissement des canaux avec le comportement des utilisateurs.

* Modules : découvrez les modules qui génèrent le plus de conversions totales et ceux qui présentent un pourcentage élevé de conversions entre appareils. Cela peut vous aider à comprendre où dépenser.

* Emplacements : comparez les performances et l’attribution des emplacements (par exemple, une publicité web mobile peut générer des conversions sur un ordinateur de bureau). Sans graphique d’appareil pour l’attribution, vous pouvez ignorer l’impact d’un emplacement web mobile sur les conversions de bureau, ou il peut être masqué si la majorité de vos utilisateurs se convertissent sur ordinateur et non sur le web mobile.

* Publicités : découvrez les publicités qui génèrent le plus de conversions et quantifiez leur valeur et leur impact sur les navigateurs web et les environnements d’applications mobiles.

* Sites : optimisez les sites d’un site à l’autre plutôt que d’exclure complètement les sites manuellement. Si un site web génère des conversions entre appareils, vous pouvez voir sur quels appareils ce comportement se produit.

* Offres - Améliorez l’optimisation manuelle en vérifiant quelles offres d’inventaire offrent des conversions entre appareils, puis en décidant si vous devez étendre votre ciblage afin d’inclure davantage de périphériques et de canaux dans ces offres.

>[!MORELIKETHIS]
>
>* [Paramètres des rapports](/help/dsp/reports/report-settings.md)
>* [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

