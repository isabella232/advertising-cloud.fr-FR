---
title: '''[!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobe Advertising'
description: Découvrez comment utiliser [!DNL Adobe] [!DNL Audience Analytics] pour les cas d’utilisation publicitaire
feature: Integration with Adobe Audience Manager
exl-id: e05ba560-d3d5-4024-b1ba-956e878a2578
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) est une intégration entre Adobe Audience Manager et Adobe Analytics qui permet aux clients d’Audience Manager d’envoyer des segments vers [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Les clients Adobe Advertising peuvent en bénéficier en utilisant [!DNL Audience Analytics]. L’intégration vous permet d’effectuer les opérations suivantes :

* Envoi direct des données d’exposition Adobe Advertising à [!DNL Analytics] pour déterminer l’impact de l’activité d’entonnoir supérieur sur l’activité de site en aval.

* Déterminez les canaux marketing et les points d’entrée du site à partir des publicités haut de l’entonnoir.

* Calculez l’intégration avec [!DNL Analytics for Advertising] pour incorporer des segments démographiques tiers à partir de [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) avec [!DNL Analytics for Advertising] pour plus d’informations sur les profils utilisateur.

   [!DNL Audience Marketplace] donne accès aux flux de données tiers avec des modèles d’abonnement &quot;Activation&quot;, qui permettent aux acheteurs d’envoyer des données vers une destination. Si les données sont utilisées dans une [!DNL Analytics] destination, les frais d’activation ne sont pas appliqués.

* (Publicitaires avec Advertising DSP) Ajoutez des segments d’exposition supplémentaires pour des informations de gestion de parcours holistique.

   Les DSP publicitaires peuvent envoyer des données d’exposition à l’Audience Manager sous forme de signaux exploitables par le biais de l’implémentation de Adobe Experience Platform ou des pixels de suivi d’impression d’Audience Manager. Transfert des mêmes données vers [!DNL Analytics] permet une analyse avancée des données. Voir &quot;[Présentation de l’intégration des données Adobe Advertising Media avec Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; pour plus d’informations.

Pour plus d’informations sur [!DNL Audience Analytics], y compris ses conditions préalables et son workflow, voir &quot;[Audience Analytics - Aperçu](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemples d’utilisation [!DNL Audience Analytics] Données avec données Adobe Advertising

Vous trouverez ci-dessous des exemples d’utilisation des données combinées dans les [!DNL Analytics] [!DNL Analysis Workspace].

### Afficher l’impact de l’activité Entonnoir supérieur sur l’activité en aval

Utilisez les segments d’exposition à l’Audience Manager pour voir l’impact de l’activité du site entonnoir supérieur sur l’activité du site en aval. Insérez des identifiants de macro ou de publicité d’Adobe dans vos pixels de suivi pour suivre l’impact à un niveau détaillé, du niveau de la campagne au niveau du site sur lequel l’utilisateur a été exposé.

Principaux avantages :

* Suivi de l’exposition par type d’entonnoir/de publicité et utilisation [!DNL Audience Analytics] pour déterminer les taux d’entrée et le chevauchement avec la phase suivante du parcours client.

* Déterminez l’impact de l’activité d’entonnoir supérieur sur l’activité de site en aval.

* Connexion [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> et [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> pour déterminer un parcours holistique du site.

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Afficher l’impact de l’activité entonnoir supérieur sur l’activité du site en aval](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Utilisation [!DNL Audience Analytics] Données de segment tierces pour l’analyse du profil utilisateur

Utilisez des segments d’Audience Manager tiers pour une analyse plus approfondie de la manière dont les utilisateurs interagissent avec votre site. Vous pouvez utiliser ces informations pour déterminer les nouvelles audiences tierces pour lesquelles activer les médias, en fonction de la manière dont les profils des segments tiers interagissent avec les indicateurs de performances clés des sites des campagnes multimédia.

>[!TIP]
> Utilisation de l’Audience Manager `Audiences ID` et `Audiences Name` dimensions dans [!DNL Analytics], comme toute autre dimension qui [!DNL Analytics] collecte des données.

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Utilisation de segments tiers pour enrichir l’analyse des profils utilisateur](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe des intégrations Advertising avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

