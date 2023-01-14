---
title: Présentation de [!DNL Analytics for Advertising]
description: Présentation de [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Présentation de [!DNL Analytics for Advertising]

*Annonceurs avec DSP Advertising et[!DNL Advertising Search]*

[!DNL Analytics for Advertising] intègre Adobe Analytics et Adobe Advertising afin d’étendre et d’améliorer les fonctionnalités de chaque produit.

L’intégration permet aux annonceurs de suivre les interactions de site par clic publicitaire et affichage publicitaire dans leurs [!DNL Analytics] , ce qui permet aux marques de voir comment leurs dépenses publicitaires conduisent à l’engagement sur le site et à des objectifs commerciaux essentiels.

En outre, Adobe Advertising peut accéder aux vastes données propriétaires qui [!DNL Analytics] collecte à l’aide de [!DNL Analytics] balises déjà présentes sur le site. Cela permet une gestion plus robuste des parcours, un remarketing propriétaire et des rapports sur les sites de médias payants. Adobe Advertising peut utiliser la variable [!DNL Analytics] données pour l’optimisation des dépenses et des offres.

Lorsqu&#39;elle est correctement employée, [!DNL Analytics for Advertising] brouille les lignes entre deux rôles traditionnels : la gestion des parcours publicitaires (l’acte d’envoyer des utilisateurs sur le site par le biais de publicités) et la compréhension de cet engagement par le biais de web analytics.

Principaux avantages :

* Envoyer [!DNL Analytics] segments directement à Adobe Advertising pour le remarketing de site propriétaire.
* Utilisation [!DNL Analytics] événements personnalisés et standard en tant que signaux de conversion pour optimiser la publicité multimédia payante.
* Profitez de [!DNL Analytics] Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites.
* Permettre une collaboration plus étroite entre les analystes web et les équipes de médias payants.
* Utiliser des identifiants d’affichage publicitaire et de clic publicitaire Adobe persistants dans [!DNL Analytics] pour comprendre l’engagement du site.
* Améliorez les rapports multimédia payants traditionnels dans Analysis Workspace avec des mesures personnalisées, des dimensions personnalisées et l’activité du site impossible à réaliser lors de l’exportation de données ou de pixels vers des serveurs d’annonces ou d’autres DSP.
* Profitez de [!DNL Analytics] code déjà présent sur votre site web pour le suivi et l’optimisation dans Adobe Advertising.

>[!TIP]
>
> Regardez une [présentation vidéo de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Utilisation d’Analytics pour les rapports sur les médias payants

[!DNL Analytics for Advertising] améliore les rapports et les informations sur la manière dont votre publicité entraîne le comportement du site en vous permettant d’effectuer les opérations suivantes :

* Utiliser des identifiants d’affichage publicitaire et de clic publicitaire Adobe persistants dans [!DNL Analytics] pour comprendre l’engagement du site.
* Profitez d’Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites. Vous pouvez accéder aux données de dimension et d’événement de média payant, qui incluent les noms d’entité de campagne de publicité d’Adobe (jusqu’aux emplacements et publicités) et leurs mesures associées, telles que les clics, les impressions et les coûts.

Pour utiliser [!DNL Analytics] en tant qu’outil de reporting multimédia payant, votre entreprise a besoin d’une connexion Experience Cloud avec accès à Analysis Workspace. Votre équipe Adobe Advertising vous aidera à mapper vos données Adobe Advertising à des suites de rapports individuelles dans Analysis Workspace. Vous pouvez envoyer des données Adobe Advertising à n’importe quelle suite de rapports, mais vous devez connaître les suites de rapports qui ont été mappées à Adobe Advertising et celles qui ne l’ont pas fait. Selon la suite de rapports, cela peut modifier les données signalées.

[Adobe des identifiants publicitaires dans [!DNL Analytics]](ids.md) fonctionne comme les autres eVars, avec une expiration personnalisée et persistante. Par défaut, l’intervalle de recherche en amont des attributions est défini sur 60 jours pendant la mise en oeuvre d’Adobe Advertising. Pour modifier ce paramètre, utilisez les [!DNL Adobe] l&#39;équipe du compte.

Les dimensions Adobe Advertising sont ajoutées avec le suffixe &quot;(AMO ID)&quot; (par exemple, &quot;Type de publicité (AMO ID)&quot;). Voir &quot;[Adobe des mesures publicitaires dans Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; pour une liste des dimensions disponibles.

>[!NOTE]
>
> Lorsque vous affichez des données Advertising Adobe (ou tout jeu de données) dans [!DNL Analytics], sachez que les mesures et les rapports sont basés sur les règles définies dans [!DNL Analytics]. Les données peuvent être différentes de celles que vous voyez dans d’autres systèmes de création de rapports, tels que les rapports sur les serveurs de publicités, [!DNL DSP] rapports ou rapports de moteur de recherche. Pour comprendre les différences de données entre les [!DNL Analytics], vous devez savoir à quel moment les données d’eVar expirent, ce qui définit une visite, ce qui est considéré comme une attribution Dernière touche par rapport à une attribution persistante totale, et d’autres facteurs. Pour plus d’informations, voir [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md).

## Utilisation d’Analytics pour alimenter les campagnes et Portfolios publicitaires Adobe

Sans nécessiter de pixels supplémentaires, [!DNL Analytics for Advertising] permet une meilleure optimisation et une segmentation plus facile de l’audience en envoyant deux signaux principaux à Adobe Advertising :

* Mesures de conversion à utiliser comme signaux d’offre :
   * mesures standard, telles que [!UICONTROL Revenue] et [!UICONTROL Cart Views].
   * les mesures d’engagement du site, telles que les mesures de pages vues et de visites.
   * mesures de recettes personnalisées.
   * mesures de recettes réservées.
* Segments créés dans [!DNL Analytics] et publié sur Experience Cloud.

   Vous pouvez utiliser [!DNL Analytics] segments pour le reciblage de site propriétaire dans [!DNL DSP] et des annonces de référencement payant.

   ([!DNL Search] uniquement) Les annonceurs avec [!DNL Analytics] mais aucune Audience Manager ne peut également créer des audiences basées sur des balises de site web Google (listes de remarketing) et des audiences de correspondance de clients (listes de clients) à partir de [!DNL Analytics] segments partagés avec Experience Cloud.

### Mesures de conversion de site en tant que signaux d’offre

Vous pouvez utiliser vos événements standard et personnalisés depuis [!DNL Analytics] pour créer des objectifs pondérés dans Adobe Advertising. Les objectifs informent les décisions d’offre pour votre [!DNL DSP] packages et portefeuilles de recherche.

>[!NOTE]
>
> Vous ne pouvez pas mapper les mesures calculées à partir de [!DNL Analytics] dans Adobe Advertising.

Votre équipe de publicité d’Adobe vous aidera à identifier et à mapper les événements qui s’appliquent aux performances de médias payants dans Adobe Advertising, où ils apparaîtront dans [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Voir &quot;[Mesures Analytics dans Adobe Advertising](analytics-data-in-advertising-cloud.md)&quot; pour une liste de mesures disponibles.

### Segments Analytics pour le reciblage de site

Adobe Advertising peut ingérer [!DNL Analytics] segments à des fins de remarketing pour les DSP publicitaires et [!DNL Search] publicités utilisant l’intégration d’audiences Experience Cloud natives entre [!DNL Analytics] et Experience Cloud.

Pour accéder au [!DNL Analytics] segments, un compte publicitaire doit disposer de la variable [Service d’ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) activée. Lorsque le service d’ID est activé, tous les segments Experience Cloud (y compris les segments créés dans [!DNL Analytics] et publiés sur des Experience Cloud, des segments créés dans Adobe Audience Manager, des segments créés dans Experience Cloud à l’aide du [!DNL People core service], et les segments créés dans Adobe Experience Platform et envoyés à Adobe Advertising par Audience Manager) deviennent disponibles dans Adobe Advertising dès qu’ils sont traités.

[!DNL Analytics] sont disponibles sous 24 heures et sont mises à jour quotidiennement.

Pour plus d’informations sur le service Audiences Experience Cloud, voir [Audiences Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemples d’utilisation de l’intégration

### Utilisation des données Adobe Advertising dans Analysis Workspace

Pour savoir comment utiliser vos données Adobe Advertising pour créer des rapports visuels dans Analysis Workspace, visionnez la vidéo &quot;[Présentation de Workspace et de la création de rapports](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Création de tableaux de bord Adobe Advertising

Pour savoir comment effectuer le suivi de vos données Adobe Advertising par rapport à vos objectifs dans Analysis Workspace, visionnez la vidéo &quot;[Création de tableaux de bord Advertising Adobe avec Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Utilisation de l’identifiant publicitaire Adobe pour l’analyse des entrées sur le site

Pour découvrir comment créer un rapport d’entrée sur le site Adobe Advertising afin de surveiller les influences &quot;jour de la semaine, heure de la journée, navigateur et géographique&quot;, visionnez la vidéo &quot;[Créer des rapports d’entrée sur le site Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vidéo : Introduction à [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe des identifiants publicitaires utilisés par Analytics](ids.md)
>* [Code JavaScript pour Analytics pour la publicité](/help/integrations/analytics/javascript.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md)
>* [Adobe des mesures publicitaires dans Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Données dans Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

