---
title: Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager
description: Découvrez comment utiliser les pixels d’événement d’Audience Manager pour capturer les données de niveau impression et de clic des campagnes Advertising Cloud DSP
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager

*Annonceurs avec Advertising Cloud DSP uniquement*

*Annonceurs avec intégration Advertising Cloud-Adobe Audience Manager uniquement*

Les clients Advertising Cloud DSP disposant de Adobe Audience Manager peuvent utiliser les pixels d’événement d’Audience Manager pour capturer les données au niveau de l’impression et les données au niveau des clics des campagnes DSP. Les pixels d’événement envoient les données sous forme de signaux exploitables à l’Audience Manager. Ces signaux permettent différents cas d’utilisation DSP, tels qu’une segmentation plus poussée, une gestion des fréquences, des analyses marketing et des informations sur les rapports.

DSP ne vous charge pas d&#39;envoyer ces signaux à l&#39;Audience Manager. Cependant, vous payez les coûts standard d’ingestion des Audiences Manager en fonction des appels au serveur, selon votre contrat d’Audience Manager. L’Audience Manager supprime les événements en double qui sont suivis de deux manières différentes, de sorte que chaque événement ne soit chargé qu’une seule fois.

>[!NOTE]
>
> Audience Manager prend également en charge la capture de données à partir de fichiers journaux de serveur d’annonces, ce qui offre moins de flexibilité. Ce processus n’est pas traité dans cette documentation.

## Avantages Principal

* DSP données de campagne sont transmises en Audience Manager en temps réel et vous pouvez les utiliser pour créer des caractéristiques basées sur des règles que vous utilisez pour définir des segments.

* Les segments sont disponibles pour le ciblage immédiatement après la qualification des caractéristiques utilisateur et des segments, ce qui renforce les efforts de ciblage en temps réel.

* Vous pouvez exploiter les données de campagne pour des cas d’utilisation tels que la limitation de la fréquence dans les créatifs, le reciblage des utilisateurs qui ont été exposés à des campagnes précédentes et l’analyse du comportement et des points d’entrée du site en aval.

* Les données agrégées offrent une vue unifiée des performances de campagne, permettent d’identifier les chemins de conversion personnalisés et peuvent être utilisés pour améliorer la séquence d’événements qui mènent à des conversions par le biais de l’Audience Manager. [!DNL Audience Optimization Reports] ou au moyen d’une [[!DNL Audience Analytics] intégration avec Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Suivi des données

Les pixels d’impression d’Audience Manager et d’événement de clic sont basés sur des cookies. Les pixels ne capturent pas les événements qui se produisent dans des environnements sans cookie, tels que les applications mobiles et la télévision connectée (CTV).

### Pixels de suivi d’impression

L’Audience Manager effectue le suivi des données d’impression pour une publicité lorsque vous associez un pixel de suivi d’événement transparent de 1xl à la publicité. Le pixel d’événement est chargé chaque fois que la publicité est diffusée à un utilisateur et chargée par le navigateur web. Le pixel est chargé à partir d’un sous-domaine spécifique au client de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), qui est un domaine hérité pour l’Audience Manager et qui contient des paramètres en tant que paires clé-valeur. L’appel d’événement collecte les données d’impression et de conversion et les envoie aux serveurs de collecte de données d’Audience Manager.

### Pixels de suivi des clics

L’Audience Manager effectue le suivi des clics de la même manière que les impressions, sauf qu’elle ne charge pas le pixel d’événement transparent chaque fois que la publicité est diffusée. Au lieu de cela, les données de clic sont suivies dans l’URL de clic publicitaire de la publicité. La publicité pointe vers un sous-domaine spécifique au client de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), qui est un domaine hérité à des fins d’Audience Manager, pour traitement par les serveurs de collecte de données d’Audience Manager. Le serveur redirige ensuite l’utilisateur vers la page d’entrée prévue. L’URL contient des paramètres en tant que paires clé-valeur.

>[!NOTE]
>
>Si votre entreprise utilise [!DNL Analytics] suivi, il se peut que vous n’ayez pas besoin d’un suivi des clics d’Audience Manager. Adobe Analytics capture les signaux de clics et peut les envoyer à l’Audience Manager via [transfert côté serveur](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Collecte de données de clics et d’impressions à partir des campagnes Advertising Cloud DSP](collect.md)
>* [Cas d’utilisation](use-cases.md)

