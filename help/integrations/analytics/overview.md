---
title: Présentation de [!DNL Analytics for Advertising Cloud]
description: Présentation de [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Présentation de [!DNL Analytics for Advertising Cloud]

*Annonceurs avec Advertising Cloud DSP et Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] intègre Adobe Analytics et Adobe Advertising Cloud pour étendre et améliorer les fonctionnalités de chaque produit.

L’intégration permet aux annonceurs de suivre les interactions de site par clic publicitaire et affichage publicitaire dans leurs [!DNL Analytics] , ce qui permet aux marques de voir comment leurs dépenses publicitaires conduisent à l’engagement sur le site et à des objectifs commerciaux essentiels.

En outre, Advertising Cloud peut accéder aux vastes données propriétaires qui [!DNL Analytics] collecte à l’aide de [!DNL Analytics] balises déjà présentes sur le site. Cela permet une gestion plus robuste des parcours, un remarketing propriétaire et des rapports sur les sites de médias payants. Advertising Cloud peut utiliser la variable [!DNL Analytics] données pour l’optimisation des dépenses et des offres.

Lorsqu&#39;elle est correctement employée, [!DNL Analytics for Advertising Cloud] brouille les lignes entre deux rôles traditionnels : la gestion des parcours publicitaires (l’acte d’envoyer des utilisateurs sur le site par le biais de publicités) et la compréhension de cet engagement par le biais de web analytics.

Principaux avantages :

* Envoyer [!DNL Analytics] segments directement vers Advertising Cloud pour le remarketing de site propriétaire.
* Utilisation [!DNL Analytics] événements personnalisés et standard en tant que signaux de conversion pour optimiser la publicité multimédia payante.
* Profitez de [!DNL Analytics] Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites.
* Permettre une collaboration plus étroite entre les analystes web et les équipes de médias payants.
* Utiliser les identifiants d’affichage et de clic publicitaire Advertising Cloud persistants dans [!DNL Analytics] pour comprendre l’engagement du site.
* Améliorez les rapports multimédia payants traditionnels dans Analysis Workspace avec des mesures personnalisées, des dimensions personnalisées et l’activité du site impossible à réaliser lors de l’exportation de données ou de pixels vers des serveurs d’annonces ou d’autres DSP.
* Profitez de [!DNL Analytics] code déjà présent sur votre site web pour le suivi et l’optimisation dans Advertising Cloud.

>[!TIP]
>
> Regardez une [présentation vidéo de [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Utilisation d’Analytics pour les rapports sur les médias payants

[!DNL Analytics for Advertising Cloud] améliore les rapports et les informations sur la manière dont votre publicité entraîne le comportement du site en vous permettant d’effectuer les opérations suivantes :

* Utiliser les identifiants d’affichage et de clic publicitaire Advertising Cloud persistants dans [!DNL Analytics] pour comprendre l’engagement du site.
* Profitez d’Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites. Vous pouvez accéder aux données de dimension et d’événement de média payant, qui incluent les noms des entités de campagne Advertising Cloud (jusqu’aux emplacements et publicités) et leurs mesures associées, telles que les clics, les impressions et les coûts.

Pour utiliser [!DNL Analytics] en tant qu’outil de reporting multimédia payant, votre entreprise a besoin d’une connexion Experience Cloud avec accès à Analysis Workspace. Votre équipe Advertising Cloud vous aidera à mapper vos données Advertising Cloud à des suites de rapports individuelles dans Analysis Workspace. Vous pouvez envoyer des données Advertising Cloud à n’importe quelle suite de rapports, mais vous devez connaître les suites de rapports qui ont été mappées à Advertising Cloud et celles qui ne l’ont pas fait. Selon la suite de rapports, cela peut modifier les données signalées.

[Advertising Cloud ID dans [!DNL Analytics]](ids.md) fonctionne comme les autres eVars, avec une expiration personnalisée et persistante. Par défaut, l’intervalle de recherche en amont des attributions est défini sur 60 jours pendant la mise en oeuvre d’Advertising Cloud. Pour modifier ce paramètre, utilisez les [!DNL Adobe] l&#39;équipe du compte.

Les dimensions Advertising Cloud sont ajoutées avec le suffixe &quot;(AMO ID)&quot; (par exemple, &quot;Type de publicité (AMO ID)&quot;). Voir &quot;[Mesures Advertising Cloud dans Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; pour une liste des dimensions disponibles.

>[!NOTE]
>
> Lorsque vous affichez des données Advertising Cloud (ou tout autre jeu de données) dans [!DNL Analytics], sachez que les mesures et les rapports sont basés sur les règles définies dans [!DNL Analytics]. Les données peuvent être différentes de celles que vous voyez dans d’autres systèmes de création de rapports, tels que les rapports sur les serveurs de publicités, [!DNL DSP] rapports ou rapports de moteur de recherche. Pour comprendre les différences de données entre les [!DNL Analytics], vous devez savoir à quel moment les données d’eVar expirent, ce qui définit une visite, ce qui est considéré comme une attribution Dernière touche par rapport à une attribution persistante totale, et d’autres facteurs. Pour plus d’informations, voir [Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud](data-variances.md).

## Utilisation d’Analytics pour optimiser les campagnes et les Portfolios Advertising Cloud

Sans nécessiter de pixels supplémentaires, [!DNL Analytics for Advertising Cloud] permet une meilleure optimisation et une segmentation plus facile de l’audience en envoyant deux signaux principaux à Advertising Cloud :

* Mesures de conversion à utiliser comme signaux d’offre :
   * mesures standard, telles que [!UICONTROL Revenue] et [!UICONTROL Cart Views].
   * les mesures d’engagement du site, telles que les mesures de pages vues et de visites.
   * mesures de recettes personnalisées.
   * mesures de recettes réservées.
* Segments créés dans [!DNL Analytics] et publié sur Experience Cloud.

   Vous pouvez utiliser [!DNL Analytics] segments pour le reciblage de site propriétaire dans [!DNL DSP] et des annonces de référencement payant.

   (Advertising Cloud Search uniquement) Annonceurs avec [!DNL Analytics] mais aucune Audience Manager ne peut également créer des audiences basées sur des balises de site web Google (listes de remarketing) et des audiences de correspondance de clients (listes de clients) à partir de [!DNL Analytics] segments partagés avec Experience Cloud.

### Mesures de conversion de site en tant que signaux d’offre

Vous pouvez utiliser vos événements standard et personnalisés depuis [!DNL Analytics] pour créer des objectifs pondérés dans Advertising Cloud. Les objectifs informent les décisions d’offre pour votre [!DNL DSP] packages et portefeuilles de recherche.

>[!NOTE]
>
> Vous ne pouvez pas mapper les mesures calculées à partir de [!DNL Analytics] dans Advertising Cloud.

Votre équipe Advertising Cloud vous aidera à identifier et à mapper les événements qui s’appliquent aux performances de médias payants dans Advertising Cloud, où ils apparaîtront dans [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Voir &quot;[Mesures Analytics dans Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot; pour une liste de mesures disponibles.

### Segments Analytics pour le reciblage de site

Advertising Cloud peut ingérer [!DNL Analytics] segments à des fins de remarketing pour Advertising Cloud DSP et [!DNL Search] publicités utilisant l’intégration d’audiences Experience Cloud natives entre [!DNL Analytics] et Experience Cloud.

Pour accéder au [!DNL Analytics] segments, un compte publicitaire doit disposer de la variable [Service d’ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) activée. Lorsque le service d’ID est activé, tous les segments Experience Cloud (y compris les segments créés dans [!DNL Analytics] et publiés sur des Experience Cloud, des segments créés dans Adobe Audience Manager, des segments créés dans Experience Cloud à l’aide du [!DNL People core service], et les segments créés dans Adobe Experience Platform et envoyés à Advertising Cloud par Audience Manager) deviennent disponibles dans Advertising Cloud dès qu’ils sont traités.

[!DNL Analytics] sont disponibles sous 24 heures et sont mises à jour quotidiennement.

Pour plus d’informations sur le service Audiences Experience Cloud, voir [Audiences Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Exemples d’utilisation de l’intégration

### Utilisation des données Advertising Cloud dans Analysis Workspace

Pour savoir comment utiliser vos données Advertising Cloud pour créer des rapports visuels dans Analysis Workspace, visionnez la vidéo &quot;[Présentation de Workspace et de la création de rapports](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Création de tableaux de bord Advertising Cloud

Pour savoir comment effectuer le suivi de vos données Advertising Cloud par rapport à vos objectifs dans Analysis Workspace, visionnez la vidéo &quot;[Création de tableaux de bord Advertising Cloud avec Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Utilisation de l’Advertising Cloud ID pour l’analyse des entrées sur le site

Pour voir comment créer un rapport d’entrée sur le site Advertising Cloud afin de surveiller les influences jour de la semaine, heure de la journée, navigateur et géographique, visionnez la vidéo &quot;[Création de rapports d’entrée sur le site Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Vidéo : Introduction à [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud ID utilisés par Analytics](ids.md)
>* [Code JavaScript pour Analytics pour Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud](data-variances.md)
>* [Mesures Advertising Cloud dans Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Données dans Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

