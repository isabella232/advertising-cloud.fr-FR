---
title: Utilisation d’Advertising Cloud ID pour créer des [!DNL Marketing Channels] règles
description: Découvrez comment utiliser les Advertising Cloud ID pour créer des règles de traitement pour  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Utilisation d’Advertising Cloud ID pour créer des règles de traitement [!DNL Marketing Channels]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

Vous pouvez utiliser des Advertising Cloud ID ([AMO ID et EF ID](../ids.md)) pour configurer les règles de traitement [!DNL Marketing Channels] dans Adobe Analytics. Utilisez des Advertising Cloud ID pour les règles spécifiques à vos campagnes Advertising Cloud.

## AMO ID dans les règles de traitement

L’AMO ID est le code de suivi Principal utilisé pour signaler les données Advertising Cloud dans [!DNL Analytics]. L’AMO ID est une concaténation de valeurs dynamiques gérées par l’Adobe afin de fournir un reporting granulaire dans [!DNL Analytics]. Il est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou rVar (AMO ID). L’AMO ID peut être défini dans [!DNL Analytics] de deux manières :

* Suivi des clics publicitaires : Advertising Cloud définit le paramètre de chaîne de requête `s_kwcid` dans un lien et [!DNL Analytics] sélectionne le paramètre à partir de l’URL de la page d’entrée lorsqu’un clic publicitaire se produit.
* Suivi des affichages publicitaires ([!DNL DSP] uniquement) : Le service Last Event détecte un affichage publicitaire côté serveur et envoie l’AMO ID à [!DNL Analytics]. Dans ce cas, l’URL ne contient pas de paramètre `s_kwcid`.

Les valeurs dynamiques des AMO ID indiquent le canal marketing qui a fait l’objet d’un suivi :

* Le préfixe de l’AMO ID peut être utilisé pour identifier le canal de niveau supérieur dans [!DNL Marketing Channels].

* Les expressions de caractères dans le corps de l’AMO ID indiquent un type de campagne plus spécifique.

* Le suffixe &quot;vt&quot; est présent pour le trafic d’affichage publicitaire [!DNL DSP] et peut être utilisé pour créer des canaux [!DNL DSP] de clic publicitaire et d’affichage publicitaire distincts.

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

La règle de traitement [!DNL Marketing Channels] pour le canal [!UICONTROL Paid Search] peut se présenter comme suit :

![Exemple de  [!UICONTROL Paid Search] règle](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La règle de traitement [!DNL Marketing Channels] pour le canal [!UICONTROL YouTube Video Ads] peut se présenter comme suit :

![Exemple de  [!UICONTROL YouTube Video Ads] règle](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Veillez à exécuter vos règles par ordre de précision. Si les deux règles ci-dessus s’exécutaient dans l’ordre, le trafic de publicité vidéo [!DNL YouTube] tomberait tous sous le canal [!UICONTROL Paid Search] car l’AMO ID commencerait tous les deux par &quot;AL!&quot;. et contiennent &quot;!ytv!&quot;.

## Identifiant EF dans les règles de traitement

L’AMO EF ID (EF ID) est le deuxième code de suivi utilisé dans l’intégration [!DNL Analytics for Advertising Cloud]. Son Principal objectif est de suivre et de transmettre des données d’événement [!DNL Analytics] dans Advertising Cloud. Chaque fois qu’un clic publicitaire ou un affichage publicitaire se produit, un identifiant EF unique est généré, même s’il s’agit exactement de la même publicité pour le même visiteur. L’identifiant EF n’est pas utilisé dans l’interface utilisateur de création de rapports [!DNL Analytics], car il dépasse généralement les 500 000 valeurs uniques par variable limite dans [!DNL Analytics], ce qui le rend inutilisable pour la création de rapports. Les mesures et métadonnées Advertising Cloud ne sont pas appliquées à l’identifiant EF ; elles sont appliquées uniquement à l’AMO ID. La granularité supplémentaire du suivi est requise pour l’optimisation des campagnes dans Advertising Cloud. Les deux identifiants sont donc requis.

Bien que la dimension Identifiant EF ne soit pas utilisée directement dans les rapports [!DNL Analytics], l’identifiant EF peut s’avérer utile pour créer des canaux marketing. Le suffixe d’identifiant EF indique le canal (affichage ou recherche) et si la visite a été pilotée par un clic publicitaire ou un affichage publicitaire. Le délimiteur dans l’identifiant EF est un deux-points, plutôt que le point d’exclamation dans l’AMO ID.

| Suffixe d’identifiant EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemples de règles de traitement qui utilisent l’identifiant EF

#### Afficher la règle de clic publicitaire

Créez un canal marketing d’affichage des clics publicitaires en capturant uniquement les clics publicitaires. Comme l’AMO ID est le même pour les clics publicitaires et les affichages publicitaires, cette règle utilise la variable EF ID et le paramètre de chaîne de requête `ef_id` .

Il arrive que les clics publicitaires fassent l’objet d’un suivi via l’URL (valeur par défaut). Dans d’autres cas, le suivi des clics publicitaires s’effectue via le service Last Event (Dernier événement) côté serveur. Par conséquent, l’URL ne contient pas le paramètre `ef_id` . La règle recherche donc les conditions dans lesquelles la variable EF ID ou le paramètre de chaîne de requête `ef_id` se termine par &quot;:d&quot;. Utilisez l’opérateur &quot;`Any`&quot; car vous souhaitez que cette règle soit déclenchée pour l’une ou l’autre des conditions.

![Exemple de règle de clic publicitaire](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Règle d’affichage publicitaire

Pour créer un canal d’affichage publicitaire, créez une règle dans laquelle l’identifiant EF se termine par &quot;:i&quot;. Comme le visiteur n’a pas cliqué sur la publicité, le suivi des affichages publicitaires n’inclut pas `ef_id` ou `s_kwcid` dans l’URL. Par conséquent, une seule condition est nécessaire.

![Exemple de règle d&#39;affichage publicitaire](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Pourquoi les données du canal peuvent-elles varier entre Advertising Cloud et [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Utilisation des données Advertising Cloud](mc-ac-data.md)
>* [Vidéo : Reporting avec Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)

