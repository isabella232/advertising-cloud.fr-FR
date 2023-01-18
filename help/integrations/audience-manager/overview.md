---
title: Adobe des intégrations Advertising avec Adobe Audience Manager
description: Découvrez les différentes façons dont Adobe Advertising peut échanger des données avec Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe des intégrations Advertising avec Adobe Audience Manager

Vous pouvez intégrer Adobe Advertising à l’Audience Manager de différentes manières.

## Synchroniser l’Audience Manager et d’autres [!DNL Adobe] Segments pour le ciblage des publicités

[!DNL Search] et DSP peuvent extraire des métadonnées, des données de hiérarchie et des données d’audience uniques pour l’ensemble de l’Audience Manager d’un annonceur ou d’une agence et d’autres [!DNL Adobe] audiences. Cette connexion unique est disponible uniquement pour les marketeurs qui utilisent Adobe Advertising. Voir &quot;[Importation de segments Adobe Audience Manager pour le ciblage des publicités](/help/integrations/audience-manager/import-audiences.md).&quot;

### Utilisation de l’Audience Manager et d’autres [!DNL Adobe] Segments à créer [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Publicitaires inscrits avec [!DNL Advertising Search] only*

Dans [!DNL [!DNL Search]], vous pouvez créer [!DNL Google Ads] Les clients Google correspondent aux audiences provenant d’ID d’utilisateur qui utilisent vos segments d’Audience Manager existants qui ont [!UICONTROL Adobe Media Optimizer (HTTP)] et [!UICONTROL Adobe Media Optimizer Batch Destination] comme destinations. ([!DNL Media Optimizer] est un ancien nom de [!DNL [!DNL Search]].) Cela inclut les segments Adobe Analytics publiés sur Adobe Experience Cloud et les segments créés dans Adobe Experience Cloud à l’aide de la variable [!DNL People core service]. Pour plus d’informations, voir l’aide intégrée au produit dans [!DNL [!DNL Search]].

[Audiences de correspondance client provenant d’ID utilisateur](https://support.google.com/google-ads/answer/9199250) fonctionne comme les audiences basées sur des balises de site web, mais un ID non lié aux PII est attribué aux membres d’audience uniques pour des avantages distincts par rapport aux audiences standard basées sur les balises de client et de site web.

Pour créer les ID utilisateur nécessaires, vous devez utiliser une balise JavaScript Adobe Advertising <!-- with a user ID parameter -->sur vos sites web. Contactez votre [!DNL [!DNL Search]] équipe du compte pour plus d’informations.

![processus de création de segments](/help/integrations/assets/ad_search_user_id_pic.png)

Une fois que vous avez créé les audiences, vous pouvez les utiliser dans [!DNL Google Ads] campagnes en tant que [cibles ou exclusions au niveau de la campagne ou du groupe publicitaire](#audience-manager-targets).

### Utilisation de l’Audience Manager et d’autres [!DNL Adobe] Segments pour cibler ou exclure des publicités {#audience-manager-targets}

* (Annonceurs inscrits avec [!DNL] [!DNL Search]]) Vous pouvez utiliser n’importe quelle [!DNL Google Ads] audiences qui étaient [créé à l’aide de [!DNL Adobe] segments](#audience-manager-google-audiences) comme cibles ou exclusions au niveau de la campagne ou du groupe publicitaire dans votre [!DNL Google Ads] campagnes.

* (Publicitaires avec DSP) Vous pouvez utiliser votre [!DNL Adobe] segments comme cibles pour vos emplacements publicitaires. Vous pouvez éventuellement inclure les segments dans les audiences réutilisables, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements.

* (Publicitaires avec Advertising Creative) Vous pouvez utiliser votre [!DNL Adobe] segments comme cibles pour des créatifs spécifiques dans vos expériences publicitaires.

>[!NOTE]
>
>Pour plus d’informations sur la création d’audiences dans l’Audience Manager et l’Experience Cloud [!DNL Audience Library] , ainsi que des cas d’utilisation courants pour différents types d’audience, voir &quot;[Options de création d’audiences](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Envoi DSP données d’exposition multimédia à l’Audience Manager

*Publicitaires avec DSP uniquement*

DSP clients Adobe Audience Manager peuvent capturer des données provenant de campagnes publicitaires à l’aide d’appels de pixel vers Audience Manager. Vous pouvez ensuite utiliser les données de campagne pour créer des caractéristiques basées sur des règles, que vous pouvez utiliser pour définir de nouveaux segments afin d’activer divers cas d’utilisation DSP, tels qu’une segmentation plus avancée, la gestion des fréquences, les analyses marketing et les informations sur les rapports.

Voir &quot;[Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; pour plus d’informations.

## Obtenir des informations plus riches sur l’activité du site avec Audience Analytics

Adobe des clients Advertising avec [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) Vous pouvez envoyer à la fois des données suivies par Adobe Advertising et des segments d’Audience Manager vers [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Pour plus d’informations, voir[[!DNL Adobe][!DNL Audience Analytics] pour les clients Adobe Advertising](/help/integrations/audience-manager/audience-analytics.md).&quot;
