---
title: Pourquoi les données de canal peuvent-elles varier entre la publicité Adobe et [!DNL Marketing Channels]
description: Découvrez pourquoi les données de canal suivies par l’AMO ID peuvent différer des données de canal suivies par [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Pourquoi les données de canal peuvent-elles varier entre la publicité Adobe et [!DNL Marketing Channels]

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

Une question courante des utilisateurs qui apprennent l’intégration de la publicité Adobe et [!DNL Marketing Channels] Les jeux de données sont &quot;Ce qui provoque la variance des données entre l’AMO ID et [!DNL Marketing Channels]?&quot; Ou, parfois, &quot;Pourquoi les données sont-elles rompues ? J’ai besoin que toutes les mesures correspondent dans les rapports.&quot; Heureusement, les incohérences n’indiquent pas que les données sont &quot;cassées&quot; et les incohérences sont attendues et même souhaitées. Examinons pourquoi l’intégration a été conçue de cette manière.

Les deux jeux de données présentent des cas d’utilisation Principaux différents :

* [!DNL Marketing Channels]: Le cas d’utilisation Principal pour [!DNL Marketing Channels] est utilisé pour comparer les données de plusieurs canaux à un modèle d’attribution commun. Les analystes peuvent utiliser la variable [!UICONTROL Marketing Channel] pour obtenir des informations supplémentaires sur la manière dont les canaux interagissent les uns avec les autres. Ces informations peuvent vous aider à prendre des décisions de macroniveau sur la manière d’investir dans chaque canal et à obtenir des informations sur la manière dont les visiteurs de chaque canal interagissent avec le site web.

   Le [!DNL Analytics] [!UICONTROL Marketing Channel] est donc configurée pour capturer et suivre tous les canaux. [!DNL Marketing Channels] peut également être configuré pour capturer les affichages publicitaires et les clics publicitaires DSP par rapport aux autres canaux marketing.

* Adobe Advertising AMO ID : Le cas d’utilisation Principal des données AMO ID Adobe Advertising consiste à alimenter les [!DNL Adobe Sensei]Algorithmes d’enchères optimisés. Les algorithmes prennent automatiquement des milliers de décisions d’offre de microniveau prises quotidiennement afin d’optimiser les dépenses publicitaires et d’atteindre les objectifs de la variable [!DNL DSP] ou la variable [!DNL Search] portfolio. Plus les algorithmes peuvent connecter les campagnes à des données de conversion, mieux ils peuvent prendre ces décisions d’offre.

   Pour collecter ces données, la variable [!DNL Analytics for Advertising] l’intégration transmet des AMO ID bruts qui peuvent être traduits en codes de suivi des clics publicitaires et des affichages publicitaires dans la dimension AMO ID d’Adobe Analytics, qui est stockée sous la forme d’une variable personnalisée (eVar) ou d’une variable réservée (rVar). Les clics publicitaires pour d’autres canaux ne sont pas définis dans la dimension AMO ID. La dimension AMO ID ne peut donc pas effectuer le suivi des entrées à partir de ces autres canaux. En conséquence, l’AMO ID persiste pendant la [!DNL Marketing Channels] points d’entrée.

Pour plus d’informations sur les écarts de données possibles entre les données suivies par Adobe Advertising et [!DNL Analytics]données trackées, voir &quot;[Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation d’identifiants Adobe Advertising pour créer [!DNL Marketing Channels] Règles de traitement](mc-ids.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec Adobe des données Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation [!DNL Marketing Channels] pour la création de rapports Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

