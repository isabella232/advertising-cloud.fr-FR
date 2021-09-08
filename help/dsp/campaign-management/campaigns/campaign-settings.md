---
title: Paramètres de campagne
description: Reportez-vous à la description des paramètres de campagne disponibles.
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Paramètres de campagne

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** nom de la campagne.

**[!UICONTROL Advertiser]:**  (Lecture seule pour les campagnes existantes) Annonceur (marque) applicable. Sélectionnez un annonceur existant ou créez-en un.

**[!UICONTROL Advertiser URL]:** page officielle de l’annonceur. Ce champ accélère le processus d’approbation des publicités avec les partenaires d’inventaire.

**[!UICONTROL Timezone]:**  (Lecture seule pour les campagnes existantes) Fuseau horaire pour la création de rapports et les offres.

**[!UICONTROL Customer PO]:**  (Facultatif) Commande d’achat d’un client pour la commande d’insertion/la commande d’achat.

**[Dates de campagne] :** dates de début et de fin de la campagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** indique s’il faut gérer les marges de la campagne :  *[!UICONTROL Yes]* ou  *[!UICONTROL No]* (valeur par défaut).

Lorsque vous choisissez *[!UICONTROL Yes],* indiquez le type et le montant de la marge :

* **[!UICONTROL Margin Type]:** type de marge. Vous ne pouvez pas modifier le type de marge une fois que vous avez activé la gestion des marges et enregistré l&#39;opération.

   * *[!UICONTROL Fixed]:*  (valeur par défaut) Permet à Advertising Cloud DSP de calculer automatiquement et de plafonner les dépenses en fonction d’un pourcentage de marge fixe du  [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* permet de gérer les marges vers le bas jusqu&#39;au niveau de placement en spécifiant un  [!UICONTROL Budget Reserve %] et  [!UICONTROL Gross Budget] pour chaque package et emplacement de l&#39;opération. Advertising Cloud DSP optimise en fonction de l’efficacité financière de chaque placement, sans garantir de marge spécifique. Utilisez cette option pour les commandes d’insertion composées de plusieurs éléments de ligne pour lesquels vous avez accepté de fournir un nombre fixe d’unités ou de types d’unités à un rythme fixe.

* **[!UICONTROL Fixed Margin %]:**  (Campagnes avec des marges fixes uniquement) Balises par défaut pour chaque ordre d’insertion,  <!-- impression? -->en pourcentage. Ce montant est déduit de la valeur [!UICONTROL Gross Budget] pour définir le budget net de l&#39;opération.

* **[!UICONTROL Budget Reserve %]:**  (Campagnes avec des marges fixes uniquement. (facultatif) réserve un pourcentage spécifié de  [!UICONTROL Gross Budget] comme protection. Ce montant est déduit de la valeur [!UICONTROL Gross Budget] pour définir le budget net de l&#39;opération.

**[!UICONTROL Gross Budget]:**  (Campagnes avec gestion des marges uniquement) Le budget brut de l’opération, avant l’application des ajustements marginaux spécifiés.

Vous pouvez éventuellement ajouter un budget brut quotidien, hebdomadaire ou mensuel supplémentaire :

1. Cliquez sur **[!UICONTROL Add an additional Gross Budget]**.

1. Saisissez le **[!UICONTROL Gross Budget]** et sélectionnez l&#39;intervalle de budget : *[!UICONTROL Daily],* *[!UICONTROL Weekly],* ou *[!UICONTROL Monthly]*.

Le budget net total, qui correspond au plafond de dépenses de l&#39;opération, est automatiquement calculé à partir des paramètres de la marge et est indiqué sous cette valeur.

**[!UICONTROL Budget]:**  (Campagnes sans gestion des marges) Budget global de l’opération.

**[!UICONTROL Estimated Tax Withholding]:** retient un pourcentage du total des dépenses par rapport aux frais publicitaires, aux frais de service publicitaire et/ou aux frais de données au niveau du compte pour les impôts locaux ou nationaux. Les taux sont des estimations à des fins de budget et de calendrier, de sorte que les taux d’imposition facturés peuvent varier.

Pour estimer les impôts à retenir :

1. Cliquez sur **[!UICONTROL Update rates here]**.

1. Spécifiez la valeur **[!UICONTROL Estimated tax rate]**, en pourcentage.

1. Cochez la case en regard de chaque type de taxe pour lequel vous souhaitez retenir des impôts. Les types de frais incluent :

   * *[!UICONTROL Include estimated tax - ads fee]:* s’applique à toutes les dépenses de médias Advertising Cloud DSP, y compris les taxes sur les frais de gestion de campagne.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* s’applique à toutes les dépenses relatives à Advertising Cloud DSP, à l’exception des médias et des données. Elle exclut les taxes pour les frais de gestion de campagne

   * *[!UICONTROL Include estimated tax - data fee]:* s’applique à toutes les données dépensées dans Advertising Cloud DSP.

1. Cliquez sur **[!UICONTROL Submit]**.

>[!NOTE]
>
>* Aux États-Unis, les États peuvent varier dans leur inclusion des taxes entre les publicités, les publicités et les données. Pour les organisations d’autres pays, incluez les trois catégories de taxes pour tenir compte de la TVA.
>
>* Vous pouvez également configurer ces valeurs dans les paramètres de frais du compte.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:**  (Lecture seule pour les campagnes existantes créées depuis le 22 juin 2020 ; non disponible pour les campagnes créées avant le 22 juin 2020) Niveau auquel Advertising Cloud ciblera les publicités et appliquera des limites de fréquence :  *Même* appareil pour cibler un appareil ou des  ** personnes pour cibler une personne sur tous leurs appareils connus.

**[!UICONTROL Device Graph]:**  (lecture seule pour les campagnes existantes) ; campagnes avec ciblage interpériphérique basé sur les personnes uniquement) Graphique d’appareil à utiliser pour le ciblage interpériphérique et la gestion des fréquences :

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible pour tous les annonceurs pour un ciblage entre appareils à 0,35 € par heure de visite pour les impressions diffusées à l’aide de la représentation graphique des  [!DNL LiveRamp] appareils (c’est-à-dire pour les appareils non trouvés dans les segments d’audience ciblés). Vous pouvez configurer le ciblage sur plusieurs appareils au niveau de l’emplacement.

   Cette option est également disponible pour tous les annonceurs, sans frais, pour la gestion des fréquences et la mesure d’attribution.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Disponible uniquement pour  [!DNL Device Co-op] les participants Adobe Experience Cloud sans frais supplémentaires.

>[!TIP]
>
>Si l’annonceur utilise également l’attribution entre appareils, la bonne pratique consiste à utiliser les mêmes paramètres graphiques d’appareil pour le ciblage et la gestion des fréquences que ceux spécifiés dans les paramètres d’attribution entre appareils de l’annonceur. Si vous sélectionnez une autre représentation graphique des appareils pour cette campagne, la création de rapports d’incohérences peut se produire.

**[!UICONTROL Frequency Cap]:**  (Facultatif) Le nombre de fois où un appareil ou une personne unique (en fonction de la valeur spécifiée  [!UICONTROL Cross Device Level]) recevra des publicités diffusées à partir de la campagne. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respectera le plafond de fréquence le plus strict de la hiérarchie de l&#39;opération.

**[!UICONTROL Packages]:**  [](/help/dsp/campaign-management/packages/package-about.md) les packages à inclure dans la campagne. Sélectionnez les packages existants et/ou créez des packages à inclure. Si vous créez des modules, reportez-vous à la description des [paramètres du module](/help/dsp/campaign-management/packages/package-settings.md) pour plus d’informations.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Les paramètres suivants activent uniquement les fonctionnalités de mesure et de création de rapports. L’optimisation des performances est exécutée uniquement au niveau du package et de l’emplacement.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:**  (Facultatif) Active la  [!DNL IAS] mesure et la création de rapports sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Measure On]:** inventaire sur lequel mesurer :  *[!UICONTROL Display and VPAID video inventory]* (valeur par défaut) ou  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >La visibilité des vidéos est mesurable sur l’inventaire VPAID uniquement.

* **[!UICONTROL IAS Account ID (AnID)]:** (annonceurs disposant de leurs propres  [!DNL IAS] comptes ; (facultatif) ID de  [!DNL IAS] compte de l’organisation, qui  [!DNL IAS] facturera directement pour l’utilisation.

* **[!UICONTROL IAS Team ID]:** (annonceurs disposant de leurs propres  [!DNL IAS] comptes ; (facultatif) Identifiant d’équipe pour le  [!DNL IAS] compte de l’organisation, qui  [!DNL IAS] facturera directement pour l’utilisation.  <!-- verify -->

**[!UICONTROL MOAT]:**  (Facultatif) Permet la  [!DNL MOAT] mesure et la création de rapports sur la visibilité, la fraude, la sécurité de la marque et la vérification de l’audience. Des frais supplémentaires s’appliquent.

#### Vérification de l’audience

**[!UICONTROL Nielsen]:**  (Facultatif) Active la  [!DNL Nielsen] mesure et la création de rapports de la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Target Gender]:** le genre à cibler :  *[!UICONTROL Both]* (valeur par défaut),  *[!UICONTROL Male]* ou  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** tranche d’âge à cibler. Utilisez les curseur gauche et droit pour réduire la plage selon vos besoins.

* **[!UICONTROL Target Country]:**  (facultatif) pays à cibler. [!DNL Nielsen] mesurera uniquement les impressions diffusées dans les pays pris en charge.

**[!UICONTROL comScore vCE]:**  (Facultatif) Active la  [!DNL Comscore validated Campaign Essentials (vCE)] mesure et la création de rapports de la vérification de l’audience, à l’aide des paramètres spécifiés. Des frais supplémentaires s’appliquent.

* **[!UICONTROL Target Gender]:** le genre à cibler :  *[!UICONTROL Both]* (valeur par défaut),  *[!UICONTROL Male]* ou  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** tranche d’âge à cibler. Utilisez les curseur gauche et droit pour réduire la plage selon vos besoins.

* **[!UICONTROL Target Country]:**  (facultatif) pays à cibler. [!DNL Comscore] mesurera uniquement les impressions diffusées dans les pays pris en charge.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:**  permet la mesure propriétaire et la création de rapports sur la visibilité à l’aide de la  [!DNL IAB Open Video Viewability (OpenVV)] technologie, en fonction du niveau de sensibilité spécifié :

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Gestion de campagne](campaign-about.md)
>* [Création d’une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)

