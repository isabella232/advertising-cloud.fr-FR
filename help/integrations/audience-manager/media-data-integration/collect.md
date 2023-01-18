---
title: Collecte de données de clics et d’impressions à partir de campagnes Advertising DSP
description: Découvrez comment capturer des impressions basées sur des cookies et des événements de clic à partir de publicités Advertising DSP à l’aide de pixels d’Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Collecte de données Media Exposure à partir de campagnes Advertising DSP

*Publicitaires avec DSP Advertising uniquement*

*Annonceurs avec une intégration Advertising-Adobe Audience Manager par Adobe uniquement*

Ce document explique comment baliser les publicités Advertising DSP pour capturer des événements d’impression et de clic basés sur des cookies à l’aide de pixels d’Audience Manager, ainsi que des tâches supplémentaires nécessaires à l’utilisation des données.

Les pixels d’événement ne capturent pas les événements qui se produisent dans des environnements sans cookie, tels que les applications mobiles et la télévision connectée (CTV).

## Étape 1 : Configuration d’une source de données dans Audience Manager {#set-up-data-source}

Dans Audience Manager, créez une [source de données](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) pour les données d’impression DSP et de clic. Inclure l’ID de source de données [dans chaque balise d’événement](#implement-dsp-pixels) afin que tous les événements suivis soient attribués à la source de données.

>[!NOTE]
> Il est possible de collecter toutes les données d’impression et de clic pour les campagnes publicitaires s’exécutant sur plusieurs DSP au sein d’une seule source de données.

## Étape 2 : Implémentation des pixels d’événement d’impression et de clic sur les pages web {#implement-dsp-pixels}

Les annonceurs peuvent créer et implémenter des balises d’événement pour leurs propres marques. Si nécessaire, contactez votre consultant Adobe Audience Manager ou votre [!DNL Adobe] gestionnaire de compte pour l’assistance.

>[!NOTE]
>
>Si votre entreprise utilise [!DNL Analytics] suivi, il se peut que vous n’ayez pas besoin d’un suivi des clics d’Audience Manager. Adobe Analytics capture les signaux de clics et peut les envoyer à l’Audience Manager via [transfert côté serveur](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Syntaxe des pixels

Les pixels d’événement doivent inclure les paramètres suivants.

**Pixels de suivi d’impression :**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec [paramètres supplémentaires facultatifs](#parameters) précédé du préfixe `&`

**pixels de suivi des clics :**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

avec [paramètres supplémentaires facultatifs](#parameters) précédé du préfixe `&`

Où :

* `[Audience Manager customer domain]` est le nom de domaine qui enverra des événements d’impression ou de clic à [!DNL Adobe].

* `[source id]` est l’identifiant de la variable [source de données](#set-up-data-source) dans laquelle vous allez suivre DSP données d’impression et de clic.

* `[redirect URL]` est l’URL de redirection codée en double. Si vous utilisez un outil de codage en ligne, tel que www.urlencoder.org, exécutez la chaîne via l’encodeur et codez à nouveau le résultat.

* `${TM_CAMPAIGN_ID_NUM}` est l’identifiant de campagne numérique dans DSP. Si vous souhaitez coder en dur un identifiant de campagne individuel au lieu d’utiliser la macro DSP, localisez l’identifiant dans les paramètres de la campagne.

* Chaque [parameter](#key-value-pairs) est précédé du préfixe `&` et est au format `d_parameter=parameter_id`où `parameter` est remplacé par la paire clé-valeur du nouveau champ. Exemple : `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Paramètres comme paires clé-valeur {#parameters}

**Format :**  `d_parameter=parameter_id`

    où :
    
    * le paramètre est précédé du préfixe `&amp;`
    
    * `parameter` est remplacé par la paire clé-valeur du nouveau champ.
    
    Exemple : `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Les deux types de pixels peuvent contenir des paramètres supplémentaires sous la forme *paires clé-valeur* pour collecter des caractéristiques ou fournir des métadonnées de campagne (un nom d’emplacement ou un nom de campagne, par exemple) pour d’autres rapports. Une paire clé-valeur se compose de deux éléments connexes : a *key*, qui est une constante qui définit le jeu de données, et une *value*, qui est une variable qui appartient au jeu.

Dans la paire clé-valeur, la variable valeur peut être soit un identifiant codé en dur, soit un identifiant codé en dur. *macro*, qui est une petite unité de code autonome remplacée dynamiquement par les valeurs correspondantes lors du chargement de la balise publicitaire pour le suivi de campagne et d’utilisateur. Pour les paramètres relatifs aux campagnes, vous pouvez utiliser [Macros DSP](/help/dsp/campaign-management/macros.md) au lieu d’utiliser des macros d’Audience Manager pour envoyer les attributs de campagne avec les données d’impression ou de clic correspondantes à l’Audience Manager, en utilisant un seul pixel sur toutes les publicités. Les macros DSP que vous insérez dans les pixels de l’événement doivent être des valeurs appropriées pour les paires clé-valeur que vous incluez dans les pixels. Par exemple, pour la variable `d_placement` clé, vous utiliseriez la macro DSP `${TM_PLACEMENT_ID_NUM}` comme valeur pour capturer les identifiants d’emplacement générés par la macro Adobe Advertising.

Pour obtenir la liste des macros prises en charge par Audience Manager pour les pixels d’événement d’impression, voir &quot;[Capture des données d’impression de campagne via des appels de pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Pour obtenir la liste des macros prises en charge par Audience Manager pour les pixels d’événement de clic, voir &quot;[Capture des données de clic de campagne via des appels de pixel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* La bonne pratique consiste à inclure les identifiants de campagne, d’emplacement, de contenu créatif (publicitaire) et de site afin que vous puissiez utiliser les attributs de campagne pour créer des caractéristiques d’Audience Manager.
>* Pour créer des rapports d’Audience Optimization, des paramètres supplémentaires sont requis.
>* Dans les paires clé-valeur, remplacez les valeurs par la valeur appropriée. [Macros DSP](/help/dsp/campaign-management/macros.md) vous pouvez donc utiliser un seul pixel pour toutes les publicités dans toutes les campagnes. Par exemple, modifiez `d_campaign=[%campaignID%]`to `d_campaign=${TM_CAMPAIGN_ID_NUM}` pour capturer les identifiants de campagne générés par la macro Adobe Advertising.
>* Si nécessaire, vous pouvez créer vos propres paramètres avec des valeurs codées en dur. Exemple : `d_DSP=AdCloud`


Exemple de pixel d&#39;événement d&#39;impression :

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Où ajouter les pixels

#### Pixel de suivi d’impression

Joindre un pixel de suivi d’événement d’impression à toutes les publicités dans votre [!DNL DSP] campagnes. Vous pouvez le faire à l’un des emplacements suivants :

* Au niveau de l’emplacement, qui applique le pixel par défaut à toutes les publicités de l’emplacement. Dans la section Suivi des paramètres de placement, ajoutez le pixel dans la balise [[!UICONTROL Event pixels] field](/help/dsp/campaign-management/placements/placement-settings.md).

* Au niveau de la publicité, qui remplace tous les pixels d’événement de niveau placement. Dans les paramètres de publicité, [créez un pixel d’événement sur la [!UICONTROL Pixel] tab](/help/dsp/campaign-management/ads/ad-edit.md).

* (Pour les publicités sur un serveur de publicités tiers) Au niveau de la publicité dans le serveur de publicités.

#### Pixel de suivi des clics

Dans le serveur de publicités, insérez le pixel d’événement de clic (avec l’URL codée ajoutée) partout où vous insérez normalement l’URL de clic publicitaire de la publicité.

## Étape 3 : Tâches après mise en oeuvre

Une fois les balises d’événement implémentées, les données sont transmises aux serveurs de collecte de données d’Audience Manager. Effectuez les tâches suivantes avant de pouvoir utiliser les données dans les rapports.

### Créez un [!DNL Amazon S3] Intervalle et source de données

Une fois vos données stockées sur les serveurs d’Audience Manager, vous devez créer une [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]), puis une source de données, à laquelle toutes les données de pixel seront envoyées. Contactez votre conseiller en Audience Manager ou [Assistance clientèle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) si vous avez besoin d&#39;aide.

### Création de caractéristiques d’Audience Manager et de segments

Vos données d’événement seront transférées dans l’Audience Manager en tant que [signaux inutilisés](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Création manuelle [caractéristiques basées sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) à partir des données ingérées, puis créez des [segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) en utilisant ces caractéristiques, avant de pouvoir utiliser les données dans les rapports.

Exemple de caractéristique qui renseigne les données au niveau de l’utilisateur pour les utilisateurs exposés à un contenu créatif spécifique dans DSP :

1. Identifiez l’événement comme `d_event = imp`.
1. Identifiez l’ID de création dans la campagne DSP, puis mappez-le à la caractéristique en tant que `d_creative=[Creative ID]`.

![Écran de création de caractéristiques](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Macros DSP](/help/dsp/campaign-management/macros.md)
>* [Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](overview.md)
>* [Cas d’utilisation](use-cases.md)

