---
title: Paramètres du compte Advertiser
description: Voir la description des paramètres de l’annonceur disponibles.
source-git-commit: d7afcc2200adc41e583d21712226cb25f35aab66
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Paramètres du compte Advertiser

*Non disponible pour les utilisateurs en lecture seule*

## [!UICONTROL General] Paramètres

**[!UICONTROL Advertiser Name]:** Nom de l’annonceur.

**[!UICONTROL Category]:** La catégorie dans laquelle l’entreprise de l’annonceur fonctionne. La catégorie est communiquée aux éditeurs lorsque vous enchérissez sur l’inventaire. Veillez à choisir une catégorie qui s&#39;aligne sur vos publicités, sinon les éditeurs peuvent rejeter vos publicités.

>[!NOTE]
>
>Si vous sélectionnez *[!UICONTROL Other]*, l’annonceur ne pourra pas accéder à DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Page d’accueil de l’annonceur ou URL du site web principal (en commençant par `http://` ou `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Nouveaux comptes publicitaires uniquement) met tous les flux d’échange privés configurés pour le compte DSP de l’organisation à la disposition de l’annonceur.

### [!UICONTROL Adobe IMS IDs]

Les annonceurs qui disposent de produits Adobe Experience Cloud supplémentaires peuvent partager des données sur certains produits à l’aide de l’identifiant unique de l’entreprise pour l’Experience Cloud. Vous pouvez configurer des intégrations de produits spécifiques dans le [!UICONTROL Integrations] .

**[!UICONTROL Account IMS org and ID]:** (Publicitaires disposant de produits Experience Cloud supplémentaires sous licence via un compte Experience Cloud avec plusieurs annonceurs ; (facultatif) ID d’organisation Experience Cloud de l’annonceur.

**[!UICONTROL Advertiser IMS org and ID]:** (Annonceurs disposant de licences directes pour des produits Experience Cloud supplémentaires ; (facultatif) ID d’organisation Experience Cloud de l’annonceur.

### [!UICONTROL Integrations]

(Facultatif) Produits Experience Cloud supplémentaires liés au compte DSP. Les produits doivent être associés au même ID d’organisation Experience Cloud que celui fourni dans la variable [!UICONTROL Adobe IMS IDs] .

**[!UICONTROL Attribution services]> [!UICONTROL Adobe Media Optimizer]:** (Publicitaires avec Advertising Cloud Search ou qui utilisent des pixels de conversion Advertising Cloud) A [!DNL Search] compte avec lequel DSP échangera des données d’attribution.

**[!UICONTROL Report suites]> [!UICONTROL Adobe Analytics]:** (Publicitaires avec Adobe Analytics ; facultatif ; s’applique uniquement aux données collectées à l’aide des balises de suivi de conversion Advertising Cloud qui incluent une variable [!DNL EF Redirect] et jeton uniquement) Un ou plusieurs [!DNL Analytics] suites de rapports auxquelles DSP enverra les données collectées auprès des éditeurs et des partenaires côté offre. Analytics enverra également les données qu’il collecte du site du client à DSP.

Pour que les données s’affichent dans les suites de rapports, la variable [!DNL Search] paramètre au niveau de l’annonceur sur &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; doit être activé. En outre, le [!DNL Analytics] doit être configuré pour recevoir des données d’Advertising Cloud.

>[!WARNING]
>
>Si vous supprimez une suite de rapports précédemment liée, DSP n’échangera plus de données avec cette suite. Vous pouvez vous attendre à voir les fluctuations des données.

Pour plus d’informations sur l’intégration à [!DNL Analytics], voir &quot;[Présentation de [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]> [!UICONTROL Adobe Analytics Cloud]:** (Publicitaires avec Adobe Audience Manager ou Adobe Analytics ; (facultatif) une Audience Manager ou [!DNL Analytics] compte à partir duquel DSP extrait les métadonnées de segment, les données de hiérarchie et les données d’audience uniques pour toutes les audiences d’Adobe de l’annonceur. Cela inclut les données pour :

* Segments d’Audience Manager
* [!DNL Analytics] segments publiés sur Adobe Experience Cloud
* Les segments créés dans Adobe Experience Cloud à l’aide de la variable [!DNL People core service]
* Segments créés dans Adobe Experience Platform et envoyés à Advertising Cloud par Audience Manager

La synchronisation initiale prend environ 24 heures. Ensuite, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Paramètres

Vous pouvez éventuellement configurer des cibles par défaut pour les nouveaux emplacements de l’annonceur. Les utilisateurs peuvent remplacer les cibles par défaut pour tout nouvel emplacement.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Pays par défaut pour le géociblage de chaque emplacement. Les utilisateurs peuvent modifier le pays et configurer un ciblage géographique plus spécifique pour chaque emplacement.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Les audiences ou segments à supprimer par défaut. Les utilisateurs peuvent modifier les exclusions pour chaque emplacement.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Types de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39] filtres contextuels à appliquer. Vous pouvez remplacer les paramètres au niveau de l’annonceur au niveau de l’ [niveau de placement](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types de contexte d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Facultatif) Un ou plusieurs types d’attributs d’inventaire à cibler par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types d’attributs d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Facultatif) Degré de contenu adulte pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Alcohol Content]:** (Facultatif) Le degré de contenu d’alcool pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Types de sites à bloquer en fonction du trafic frauduleux et des activités suspectes mesurées par [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39]. Vous pouvez remplacer les paramètres au niveau de l’annonceur au niveau de l’ [niveau de placement](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Par défaut, bloque tout le trafic non valide à 100 %, y compris le trafic sur les appareils détournés, pour les nouveaux emplacements. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Also block sites with]:** (Facultatif) Un niveau supplémentaire de fraude et de trafic non valide qui entraînera DSP bloquer les publicités par défaut :  *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas le trafic supplémentaire), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types de fraude qui entraîneront DSP bloquer les publicités par défaut : *[!UICONTROL Fraud]* (qui bloque tous les sites escroqués), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, et/ou *[!UICONTROL Fraud: Zero Ads]*. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Facultatif) Un type d’activité suspecte sur un site web ou une application qui DSP par défaut bloquer les publicités : *[!UICONTROL None]* (la valeur par défaut, qui ne bloque pas les publicités basées sur des activités suspectes), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Des frais supplémentaires peuvent s’appliquer.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Par défaut, quel niveau de [[!DNL Ads.txt] filtrage pré-enchère](https://iabtechlab.com/ads-txt-about/) à utiliser en exploitant les [!DNL Authorized Digital Sellers] list :
* *[!UICONTROL Opt out of ads.txt (default)]*: Pour acheter des stocks à tous les vendeurs.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Pour donner la priorité à l’achat du stock auprès des revendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]*: Acheter un inventaire uniquement auprès des revendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]*: Pour acheter des stocks uniquement auprès des vendeurs directs autorisés d’un domaine.

Vous pouvez remplacer le paramètre au niveau de l’annonceur à l’adresse [niveau de placement](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Par défaut, active un filtre post-offre en temps réel pour s’assurer que les publicités sont diffusées sur les sites ciblés par l’annonceur. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] clients uniquement ; (facultatif) Identifiant du segment de sécurité de la marque associé à la variable [!DNL DoubleVerify] compte .

**[!UICONTROL Enable Authentic Brand Safety]:** (Facultatif) Par défaut, la fonction active [!DNL DoubleVerify] Authentification de sécurité des marques, qui bloque les impressions après l’offre à l’aide des règles de sécurité de marque personnalisées configurées pour l’identifiant de segment spécifié. DSP facture votre compte pour l’utilisation de l’identifiant de segment.

Vous pouvez remplacer le paramètre au niveau de l’annonceur au niveau de l’emplacement.

>[!MORELIKETHIS]
>
>* [Création d’un compte Advertiser](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
