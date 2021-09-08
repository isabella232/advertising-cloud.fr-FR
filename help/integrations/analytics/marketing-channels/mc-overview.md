---
title: Principes fondamentaux de [!DNL Marketing Channels]
description: Découvrez les informations clés sur  [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] les utilisateurs doivent comprendre.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Principes fondamentaux de [!DNL Analytics Marketing Channels]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

Cette page présente des informations clés sur [!DNL Analytics Marketing Channels] que les utilisateurs de [!DNL Analytics for Advertising Cloud] doivent comprendre.

Pour obtenir une documentation complète sur [!DNL Marketing Channels], voir &quot;[Prise en main de [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html)&quot;.

## Présentation de [!DNL Marketing Channels]

[!DNL Marketing Channels] sont une fonctionnalité clé d’Adobe Analytics. [!DNL Marketing Channels] les rapports indiquent comment les clients accèdent à votre site web par le biais de la fenêtre de création de rapports et comment chaque canal impacte les recettes ou le comportement sur site.

Prenons l’exemple suivant d’un parcours entre plusieurs visites. Chaque visite sur votre site web est indiquée par le canal marketing à partir duquel le visiteur est entré. La première visite, également appelée canal Première touche, est Email. L’affichage lors de la deuxième visite est un canal participant et la recherche naturelle est considérée comme le canal Dernière touche. Si vous utilisez [!UICONTROL Last Touch Attribution] dans [!UICONTROL Attribution IQ], la recherche naturelle recevra un crédit complet pour l’événement de conversion de 250 $. À l’aide du service d’ID Experience Cloud, vous pouvez associer ces visites individuelles pour afficher un parcours par un seul visiteur.

![Exemple de parcours de conversion entre visites dans les canaux marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

En utilisant des règles de traitement [!UICONTROL Marketing Channels], vous pouvez créer des ensembles de logiques afin de déterminer les canaux qui pilotent le trafic et de suivre chaque canal lorsque les utilisateurs se rendent sur votre site. Par exemple, le canal [!UICONTROL Email] est indiqué par un code de suivi unique généré lors du clic qui, lorsqu’il est consigné par Adobe Analytics, classe la visite comme provenant d’une campagne de marketing par e-mail.

## Règles de traitement et définition des canaux marketing

Chaque fois qu’un utilisateur se rend sur un site web, il le fait par le biais d’une URL sur laquelle il a cliqué ou directement tapé dans la barre d’adresse. Lorsque l’utilisateur accède au site web, [!DNL Analytics] effectue le suivi des informations qui peuvent être utilisées pour déterminer le canal qui a conduit la visite.

Souvent, les spécialistes du marketing ajoutent des codes de suivi de paramètre de chaîne de requête aux URL de canal pour faciliter le suivi de l’impact du canal sur leur site. Vous pouvez configurer des règles de traitement [!DNL Marketing Channels] pour écouter les paramètres et valeurs de suivi spécifiques afin de déterminer le canal sans suivi supplémentaire. Par exemple, si toutes les URL de campagne par e-mail suivent le format `www.adobe.com?cid=email…` (où l’URL contient le paramètre de chaîne de requête et la valeur `cid=email`), vous pouvez créer une règle pour écouter ce code de suivi et pour regrouper la visite dans le canal [!UICONTROL Email].

Les autres canaux ne disposent pas de chemins d’URL pouvant faire l’objet d’un suivi et nécessitent une logique plus poussée pour l’identification. Par exemple, [!UICONTROL Earned Social], dans lequel un utilisateur clique sur un lien qu’un autre utilisateur a partagé de manière organique sur un réseau social, est un canal important à suivre. Cependant, le spécialiste du marketing n’a aucun moyen d’ajouter un code de suivi de paramètre de chaîne de requête à l’URL partagée. Dans ce cas, vous pouvez créer une règle de traitement pour écouter le domaine référent des réseaux sociaux ciblés et l’absence de codes de suivi payants pour déterminer le canal. Les visites qui répondent à ces exigences font ensuite l’objet d’un suivi en tant que réseaux sociaux gagnés dans le rapport Canaux marketing .

Adobe recommande de travailler avec votre équipe d’analyse pour créer un ensemble complet de règles de traitement [!DNL Marketing Channels] afin d’effectuer le suivi de tous les canaux pertinents pour votre entreprise. Cela vous permet de créer de puissants rapports d’attribution.

Pour comprendre comment Advertising Cloud peut contribuer aux signaux nécessaires à la création de canaux marketing personnalisés, voir &quot;[Utilisation d’identifiants publicitaires pour créer [!DNL Marketing Channels] des règles](mc-ids.md)&quot;.

>[!MORELIKETHIS]
>
>* [Utilisation d’Advertising Cloud ID pour  [!DNL Marketing Channels] créer des règles de traitement](mc-ids.md)
>* [Pourquoi les données du canal peuvent-elles varier entre Advertising Cloud et [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Utilisation des données Advertising Cloud](mc-ac-data.md)
>* [Vidéo : Reporting avec Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Présentation de [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

