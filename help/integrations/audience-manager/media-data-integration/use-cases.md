---
title: Cas d’utilisation
description: En savoir plus sur les cas d’utilisation pour le partage de vos données multimédia Advertising DSP avec Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 21d80cf6-f817-495a-bae4-fc9e44f1eda4
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Cas d’utilisation de la capture de données d’exposition aux médias dans Adobe Audience Manager

*Publicitaires avec DSP Advertising uniquement*

*Annonceurs avec une intégration Advertising-Adobe Audience Manager par Adobe uniquement*

Vous trouverez ci-dessous quelques façons de tirer parti de la capture de vos données d’exposition aux médias Advertising DSP <!-- ad impression data? --> en Audience Manager.

## Gestion de la récence et des fréquences

La capture des données d’impression dans Audience Manager vous permet d’améliorer votre gestion des fréquences en créant des segments d’utilisateurs qui ont été exposés à une publicité ou à une campagne spécifique. Vous pouvez utiliser ces segments pour le ciblage des publicités si vous souhaitez augmenter la fréquence ou pour la suppression des publicités si vous souhaitez limiter la fréquence.

Également avec l’Audience Manager [!DNL Segment Builder], vous pouvez appliquer des [contrôles de récence et de fréquence](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) à tout [caractéristiques basées sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) qui contiennent des signaux exploitables. Cela vous permet, par exemple, de limiter le nombre de fois où un utilisateur voit apparaître un élément créatif particulier dans une campagne multimédia. Lire &quot;[Suppression instantanée inter-périphérique](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; pour apprendre à le faire.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messagerie séquentielle

En capturant les données d’impression, vous pouvez créer un segment d’utilisateurs qui ont été exposés à une campagne ou à une publicité et utiliser ce segment pour la messagerie ou la suppression séquentielle. Vous pouvez, par exemple, recibler les utilisateurs qui ont vu des éléments créatifs `123` mais n’a pas cliqué ni converti en les affichant créatifs `456`.

Pour exécuter cet exemple en Audience Manager, procédez comme suit :<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Créez une caractéristique pour capturer les utilisateurs qui ont vu le contenu créatif.

   Par exemple, pour nommer la caractéristique `Creative Trait 123`, utilisez la règle de caractéristique suivante :

   `d_creative == 123 AND d_event == imp`

1. Créez une caractéristique pour capturer les utilisateurs qui cliquent ou convertissent.

   Par exemple, pour nommer cette caractéristique `Click and Converter`, utilisez la règle de caractéristique suivante :

   `d_event == click OR d_event=conv`

1. Créez un segment appelé `Retarget Users` pour renseigner les utilisateurs qui ont vu des éléments créatifs `123` mais n’a pas cliqué ni converti. Utilisez la règle de caractéristique suivante :

   `Creative Trait 123 AND NOT Click and Converter`

1. Mappage du segment `Retarget Users` vers une destination et cibler les utilisateurs de la destination avec des `456`.

## [!DNL Adobe Audience Analytics] et données d’exposition Campaign

Une fois que les données d’impression et de clic de campagne sont disponibles dans Audience Manager, vous pouvez créer des caractéristiques et des segments d’utilisateurs qui ont été exposés à une campagne ou à une tactique spécifique ou ont interagi avec celle-ci. Avec [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), les segments d’Audience Manager peuvent être synchronisés avec [!DNL Analytics] pour une analyse plus approfondie. Les cas d’utilisation potentiels sont les suivants :

* **Analyse des interactions entre DSP et [!DNL Adobe Advertising Search] publicités :** Le standard [[!DNL Analytics for Advertising] integration](/help/integrations/analytics/overview.md) ne fournit pas d’informations sur l’interaction entre DSP et [!DNL [!DNL Search]], car les deux canaux utilisent des AMO ID qui suivent les règles d’attribution AMO ID, pour lesquels un clic de recherche remplace un affichage publicitaire. En créant un segment d’exposition DSP dans Audience Manager, vous pouvez utiliser [!DNL Audience Analytics] pour analyser l’interaction entre DSP et [!DNL [!DNL Search]] publicités dans [!DNL Analytics].

* **Analyse des fréquences :** Vous pouvez créer des segments dans l’Audience Manager en fonction du nombre de fois où un utilisateur a été exposé à une publicité ou une campagne spécifique. Vous pouvez ensuite analyser les différents segments d’exposition dans Analytics afin de voir comment le comportement des utilisateurs change en fonction du nombre d’expositions DSP.

## [!DNL Audience Optimization Reports]

Vous pouvez tirer parti de [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) pour identifier les opportunités de performances potentielles pour les segments dans vos campagnes. Ces rapports combinent les données d’impression, de clics et de conversion de campagnes avec des mesures de segments afin d’informer les optimisations centrées sur les segments et d’offrir une combinaison efficace de canaux.

### Types de rapports d’Audience Optimization pertinents

| Rapport | Description |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Compare les segments mappés et non mappés en fonction des impressions et des taux de conversion. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Renvoie des données sur les impressions, les taux de clics publicitaires et les conversions pour un large éventail de dimensions publicitaires. |
| [[!UICONTROL Optimal Frequency] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Permet de découvrir l’équilibre optimal entre le nombre d’impressions diffusées et de conversions. Il vous permet d’ajuster le nombre d’impressions à afficher avant de commencer à voir des rendements décroissants. |
| [[!UICONTROL Unique User Reach] Rapport](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Graphique à bulles, dans lequel chaque bulle est dimensionnée en proportion directe du nombre d’utilisateurs uniques pour la dimension sélectionnée. |

### Considérations

* If [!DNL Audience Optimization Reports] Les utilisateurs disposent de contrôles d’accès en fonction du rôle (RBAC), puis [!DNL Adobe Customer Care] doit configurer un mappage entre l’identifiant publicitaire et le code d’intégration de la source de données d’Audience Manager de l’entreprise. Les utilisateurs administrateurs peuvent alors fournir des droits RBAC à différents utilisateurs.

* Rapports de conversion dans [!DNL Audience Optimization Reports] nécessite une configuration par l’utilisateur final. Les utilisateurs doivent renseigner les fichiers de métadonnées.

* [!DNL Audience Optimization Reports] ne prend pas en charge les modifications apportées aux métadonnées de campagne (telles que le nom de la campagne ou le nom de l’emplacement).

* Les clics sur les publicités de recherche sont inclus dans [!DNL Audience Optimization Reports] uniquement lorsqu’ils sont corrélés avec les impressions. En d’autres termes, les clics de recherche sont traités comme des conversions suite aux impressions. Par conséquent, de nombreux clics de recherche peuvent ne pas être inclus dans [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](overview.md)
>* [Collecte de données de clics et d’impressions à partir de campagnes Advertising DSP](collect.md)

