---
title: '"[!DNL Adobe][!DNL Audience Analytics] pour les clients Advertising Cloud"'
description: Découvrez comment utiliser [!DNL Adobe][!DNL Audience Analytics] pour les cas d’utilisation publicitaire
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] pour les clients Advertising Cloud

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) est une intégration entre Adobe Audience Manager et Adobe Analytics qui permet aux clients d’Audience Manager d’envoyer des segments vers [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Les clients Advertising Cloud peuvent en bénéficier en utilisant [!DNL Audience Analytics]. L’intégration vous permet d’effectuer les opérations suivantes :

* Envoi direct des données d’exposition Advertising Cloud à [!DNL Analytics] pour déterminer l’impact de l’activité d’entonnoir supérieur sur l’activité de site en aval.

* Déterminez les canaux marketing et les points d’entrée du site à partir des publicités haut de l’entonnoir.

* Calculez l’intégration avec [!DNL Analytics for Advertising Cloud] pour incorporer des segments démographiques tiers à partir de [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) avec [!DNL Analytics for Advertising Cloud] pour plus d’informations sur les profils utilisateur.

   [!DNL Audience Marketplace] donne accès aux flux de données tiers avec des modèles d’abonnement &quot;Activation&quot;, qui permettent aux acheteurs d’envoyer des données vers une destination. Si les données sont utilisées dans une [!DNL Analytics] destination, les frais d’activation ne sont pas appliqués.

* (Publicitaires avec Advertising Cloud DSP) Ajoutez des segments d’exposition supplémentaires pour obtenir des informations de gestion de parcours globale.

   Advertising Cloud DSP peut envoyer des données d’exposition à l’Audience Manager sous forme de signaux exploitables par le biais de l’implémentation de Adobe Experience Platform ou des pixels de suivi des impressions de l’Audience Manager. Transfert des mêmes données vers [!DNL Analytics] permet une analyse avancée des données. Voir &quot;[Présentation de l’intégration des données multimédias Advertising Cloud avec Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; pour plus d’informations.

Pour plus d’informations sur [!DNL Audience Analytics], y compris ses conditions préalables et son workflow, voir &quot;[Audience Analytics - Aperçu](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Exemples d’utilisation [!DNL Audience Analytics] Données avec données Advertising Cloud

Vous trouverez ci-dessous des exemples d’utilisation des données combinées dans les [!DNL Analytics] [!DNL Analysis Workspace].

### Afficher l’impact de l’activité Entonnoir supérieur sur l’activité en aval

Utilisez les segments d’exposition à l’Audience Manager pour voir l’impact de l’activité du site entonnoir supérieur sur l’activité du site en aval. Incluez des identifiants de macro Advertising Cloud ou tiers dans vos pixels de suivi pour suivre l’impact à un niveau détaillé, du niveau de la campagne au niveau du site sur lequel l’utilisateur a été exposé.

Principaux avantages :

* Suivi de l’exposition par type d’entonnoir/de publicité et utilisation [!DNL Audience Analytics] pour déterminer les taux d’entrée et le chevauchement avec la phase suivante du parcours client.

* Déterminez l’impact de l’activité d’entonnoir supérieur sur l’activité de site en aval.

* Connexion [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> et [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> pour déterminer un parcours holistique du site.

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
>* [Intégrations Advertising Cloud à Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

