---
title: Pourquoi les données du canal peuvent-elles varier entre Advertising Cloud et  [!DNL Marketing Channels]
description: Découvrez pourquoi les données de canal suivies par l’AMO ID peuvent différer des données de canal suivies par [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Pourquoi les données du canal peuvent-elles varier entre Advertising Cloud et [!DNL Marketing Channels]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

Une question courante des utilisateurs qui découvrent l’intégration des jeux de données Advertising Cloud et [!DNL Marketing Channels] est : &quot;Qu’est-ce qui provoque la variance des données entre l’AMO ID et [!DNL Marketing Channels] ?&quot; Ou, parfois, &quot;Pourquoi les données sont-elles rompues ? J’ai besoin que toutes les mesures correspondent dans les rapports.&quot; Heureusement, les incohérences n’indiquent pas que les données sont &quot;cassées&quot; et les incohérences sont attendues et même souhaitées. Examinons pourquoi l’intégration a été conçue de cette manière.

Les deux jeux de données présentent des cas d’utilisation Principaux différents :

* [!DNL Marketing Channels]: Le cas d’utilisation Principal pour  [!DNL Marketing Channels] consiste à comparer les données sur plusieurs canaux avec un modèle d’attribution commun. Les analystes peuvent utiliser la dimension [!UICONTROL Marketing Channel] pour obtenir des informations supplémentaires sur la manière dont les canaux interagissent les uns avec les autres. Ces informations peuvent vous aider à prendre des décisions de macroniveau sur la manière d’investir dans chaque canal et à obtenir des informations sur la manière dont les visiteurs de chaque canal interagissent avec le site web.

   La dimension [!DNL Analytics] [!UICONTROL Marketing Channel] est donc configurée pour capturer et suivre tous les canaux. [!DNL Marketing Channels] peut également être configuré pour capturer les affichages publicitaires et les clics publicitaires Advertising Cloud DSP, par rapport aux autres canaux marketing.

* Advertising Cloud AMO ID : Le Principal cas d’utilisation des données AMO ID d’Advertising Cloud consiste à alimenter les algorithmes d’offre avancés d’Advertising Cloud optimisés par [!DNL Adobe Sensei]. Les algorithmes prennent automatiquement des milliers de décisions d’offre de microniveau prises quotidiennement afin d’optimiser les dépenses publicitaires et d’atteindre les objectifs de la campagne [!DNL DSP] ou du portefeuille [!DNL Search]. Plus les algorithmes peuvent connecter les campagnes à des données de conversion, mieux ils peuvent prendre ces décisions d’offre.

   Pour collecter ces données, l’intégration [!DNL Analytics for Advertising Cloud] transmet des AMO ID bruts qui peuvent être traduits en codes de suivi des clics publicitaires et des affichages publicitaires dans la dimension AMO ID d’Adobe Analytics — qui est stockée sous la forme d’une variable personnalisée (eVar) ou d’une variable réservée (rVar). Les clics publicitaires pour d’autres canaux ne sont pas définis dans la dimension AMO ID. La dimension AMO ID ne peut donc pas effectuer le suivi des entrées à partir de ces autres canaux. Par conséquent, l’AMO ID persiste via les points d’entrée [!DNL Marketing Channes]l.

Pour plus d’informations sur les écarts de données possibles entre les données suivies par Advertising Cloud et les données suivies par [!DNL Analytics], voir &quot;[Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Écarts de données attendus  [!DNL Analytics] entre Advertising Cloud et](/help/integrations/analytics/data-variances.md)
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation d’Advertising Cloud ID pour  [!DNL Marketing Channels] créer des règles de traitement](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Utilisation des données Advertising Cloud](mc-ac-data.md)
>* [Vidéo : Reporting avec Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

