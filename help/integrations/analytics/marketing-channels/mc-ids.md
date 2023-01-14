---
title: Utilisation d’identifiants Adobe Advertising pour créer [!DNL Marketing Channels] Règles
description: Découvrez comment utiliser des identifiants Adobe Advertising pour créer des règles de traitement pour [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Utilisation d’identifiants Adobe Advertising pour créer [!DNL Marketing Channels] Règles de traitement

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

Vous pouvez utiliser des identifiants Adobe Advertising ([AMO ID et EF ID](../ids.md)) pour configurer [!DNL Marketing Channels] règles de traitement dans Adobe Analytics. Utilisez des identifiants Adobe Advertising pour les règles spécifiques à vos campagnes Adobe Advertising.

## AMO ID dans les règles de traitement

L’AMO ID est le code de suivi Principal utilisé pour signaler les données Advertising d’Adobe dans [!DNL Analytics]. L’AMO ID est une concaténation de valeurs dynamiques gérées par Adobe pour fournir des rapports granulaires dans [!DNL Analytics]. Il est stocké dans une [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou de la dimension rVar (AMO ID). L’AMO ID peut être défini dans [!DNL Analytics] de deux manières :

* Suivi des clics publicitaires : Adobe Advertising définit la variable `s_kwcid` paramètre de chaîne de requête dans un lien, et [!DNL Analytics] récupère le paramètre de l’URL de la page d’entrée lorsqu’un clic publicitaire se produit.
* Suivi des affichages publicitaires ([!DNL DSP] Uniquement) : Le service Last Event détecte un affichage publicitaire côté serveur et envoie l’AMO ID à [!DNL Analytics]. Dans ce cas, l’URL ne contient pas de `s_kwcid` .

Les valeurs dynamiques des AMO ID indiquent le canal marketing qui a fait l’objet d’un suivi :

* Le préfixe de l’AMO ID peut être utilisé pour identifier le canal de niveau supérieur dans [!DNL Marketing Channels].

* Les expressions de caractères dans le corps de l’AMO ID indiquent un type de campagne plus spécifique.

* Le suffixe &quot;vt&quot; est présent pour [!DNL DSP] trafic d’affichage publicitaire et peut être utilisé pour créer des clics publicitaires et des affichages publicitaires distincts [!DNL DSP] canaux.

Le reste de l’AMO ID peut être ignoré.

| AMO ID | Canal | Logique de règle |
|--------|---------|--------------------|
| AL ! (préfixe) | [!UICONTROL Paid Search] | Commence par |
| AC ! (préfixe) | [!UICONTROL DSP] | Commence par |
| !g ! (body) | [!UICONTROL Google Search] | Contient |
| !s ! (body) | [!UICONTROL Search Partner] | Contient |
| !d ! (body) | [!UICONTROL Display Network] | Contient |
| !u ! (body) | [!UICONTROL Smart Shopping Campaign] | Contient |
| !ytv ! (body) | [!UICONTROL YouTube Video Ad] | Contient |
| !yts ! (body) | [!UICONTROL YouTube Search Ad] | Contient |
| !vp ! (body) | [!UICONTROL Google Video Partners] | Contient |
| !vt (suffixe) | [!UICONTROL DSP View-through] | Se termine par |

### Exemples de règles de traitement qui utilisent l’AMO ID

Le [!DNL Marketing Channels] règle de traitement pour la [!UICONTROL Paid Search] channel peut se présenter comme suit :

![Exemple d’un [!UICONTROL Paid Search] règle](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Le [!DNL Marketing Channels] règle de traitement pour la [!UICONTROL YouTube Video Ads] channel peut se présenter comme suit :

![Exemple d’un [!UICONTROL YouTube Video Ads] règle](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Veillez à exécuter vos règles par ordre de précision. Si les deux règles ci-dessus s’exécutaient dans l’ordre, la variable [!DNL YouTube] le trafic des publicités vidéo tomberait tous sous [!UICONTROL Paid Search] car AMO ID commencerait tous les deux par &quot;AL!&quot; et contiennent &quot;!ytv!&quot;.

## Identifiant EF dans les règles de traitement

L’AMO EF ID (EF ID) est le deuxième code de suivi utilisé dans la variable [!DNL Analytics for Advertising] intégration. Son Principal objectif est de suivre et de transmettre des [!DNL Analytics] données d’événement dans Adobe Advertising. Chaque fois qu’un clic publicitaire ou un affichage publicitaire se produit, un identifiant EF unique est généré, même s’il s’agit exactement de la même publicité pour le même visiteur. L’identifiant EF n’est pas utilisé dans la variable [!DNL Analytics] l’interface utilisateur de création de rapports, car elle dépasse généralement la limite de 500 000 valeurs uniques par variable dans [!DNL Analytics], ce qui le rend inutilisable pour la création de rapports. Les mesures et métadonnées Adobe Advertising ne sont pas appliquées à l’identifiant EF ; elles sont appliquées uniquement à l’AMO ID. La granularité supplémentaire du suivi est requise pour l’optimisation des campagnes dans Adobe Advertising. Les deux identifiants sont donc requis.

Bien que la dimension Identifiant EF ne soit pas utilisée directement dans [!DNL Analytics] , l’identifiant EF peut s’avérer utile pour créer des canaux marketing. Le suffixe d’identifiant EF indique le canal (affichage ou recherche) et si la visite a été pilotée par un clic publicitaire ou un affichage publicitaire. Le délimiteur dans l’identifiant EF est un deux-points, plutôt que le point d’exclamation dans l’AMO ID.

| Suffixe d’identifiant EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemples de règles de traitement qui utilisent l’identifiant EF

#### Afficher la règle de clic publicitaire

Créez un canal marketing d’affichage des clics publicitaires en capturant uniquement les clics publicitaires. Comme l’AMO ID est le même pour les clics publicitaires et les affichages publicitaires, cette règle utilise la variable EF ID et la variable `ef_id` paramètre de chaîne de requête.

Il arrive que les clics publicitaires fassent l’objet d’un suivi via l’URL (valeur par défaut). Dans d’autres cas, le suivi des clics publicitaires s’effectue via le service Last Event (Dernier événement) côté serveur. Par conséquent, l’URL ne contient pas le paramètre `ef_id` . La règle recherche donc les conditions dans lesquelles la variable EF ID ou la variable `ef_id` le paramètre de chaîne de requête se termine par &quot;:d&quot;. Utilisez le`Any`&quot;, car vous souhaitez que cette règle soit déclenchée pour l’une ou l’autre des conditions.

![Exemple de règle de clic publicitaire](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Règle d’affichage publicitaire

Pour créer un canal d’affichage publicitaire, créez une règle dans laquelle l’identifiant EF se termine par &quot;:i&quot;. Comme le visiteur n’a pas cliqué sur la publicité, le suivi des affichages publicitaires n’inclut pas la variable `ef_id` ou `s_kwcid` dans l’URL. Par conséquent, la règle ne nécessite qu’une seule condition.

![Exemple de règle d&#39;affichage publicitaire](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Pourquoi les données de canal peuvent-elles varier entre la publicité Adobe et [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec Adobe des données Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation [!DNL Marketing Channels] pour la création de rapports Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe des identifiants publicitaires utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)

