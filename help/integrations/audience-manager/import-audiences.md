---
title: Importation de segments Adobe Audience Manager pour le ciblage des publicités
description: Découvrez comment importer votre [!DNL Adobe] Audiences dans les DSP publicitaires et la recherche à l’aide de Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 08a40148-b7d2-442b-81e8-f3aec4fca7df
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Importation de segments Adobe Audience Manager pour le ciblage des publicités

DSP de publicité et [!DNL Advertising Search] peut extraire des métadonnées, des données hiérarchiques et des données d’audience uniques pour l’ensemble du contenu d’un annonceur ou d’une agence ; [!DNL Adobe] audiences<!-- segments or audiences? Standardize terms per AAM's docs -->. Cela inclut les données pour :

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés dans Adobe Experience Cloud

* Les segments créés dans Adobe Experience Cloud à l’aide de la variable [!DNL People core service]

* Segments créés dans Adobe Experience Platform et envoyés à Adobe Advertising par Audience Manager

Pour accéder à [!DNL Adobe] audiences dans DSP ou [!DNL Creative], vous devez importer les audiences dans DSP. Pour accéder à [!DNL Adobe] audiences dans [!DNL [!DNL Search]], vous devez importer les audiences dans [!DNL [!DNL Search]].

## Conditions préalables

* L’annonceur doit implémenter [la valeur [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) version 2.0 ou ultérieure. Le [!DNL Identity Service] fournit un identifiant universel et permanent qui identifie vos visiteurs dans toutes les solutions Experience Cloud.

   La mise en oeuvre comprend l’ajout de la variable [!DNL Identity service] code vers chaque page web des sites de l’annonceur.

* L’organisation doit être [activé pour les services Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) et disposer d’un Experience Cloud [!DNL Organization ID] (anciennement appelée [!DNL IMS org ID]).

   Le [!UICONTROL Organization ID] permet aux entreprises disposant de plusieurs produits Adobe Experience Cloud de partager des données entre certains produits.

* (Publicitaires avec [!DNL Analytics]) L’annonceur doit [implémenter [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) version 1.6.4 ou ultérieure.

* Les visiteurs du site web de l’annonceur n’incluent pas un volume élevé de [!DNL Apple Safari] utilisateurs.

* (Recommandé lorsque l’annonceur utilise à la fois l’Audience Manager et [!DNL Analytics]) Pour réduire les appels à chaque page web, supprimez l’Audience Manager existante. [!DNL Data Integration Library] code pour la collecte de données et activation du transfert côté serveur pour chaque [!DNL Analytics] suite de rapports à la place. Pour plus d’informations, voir[Transfert côté serveur - Aperçu](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Recommandé) Pour des taux de correspondance plus élevés, envoyez uniquement des données de site web propriétaires à Adobe Advertising. Si l’annonceur rassemble des données tierces ou hors ligne d’un système de gestion de la relation client, les fuites de données peuvent réduire les taux de correspondance.

## Importation d’audiences d’Audience Manager dans DSP

### Procédure d’importation d’audiences dans DSP

Le [!DNL Adobe] les équipes des opérations de compte et de données effectuent les étapes suivantes.

1. Le [!DNL Adobe] l’équipe du compte doit configurer le paramètre au niveau de l’annonceur &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. Le [!DNL Adobe] l’équipe du compte doit envoyer une requête ;<!-- Submit a request as a JIRA task? --> à l’équipe des opérations de données<!-- implementation team? --> pour importer les segments d’Audience Manager de l’entreprise à l’aide de l’intégration de l’API native d’Advertising DSP.

### Quels changements entraînent l’Audience Manager ?

L’API automatiquement :

* Crée deux destinations DSP en Audience Manager :

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Mappe les deux destinations à tous les segments d’Audience Manager, ce qui permet à l’Audience Manager de partager les segments avec le compte publicitaire DSP associé au même Experience Cloud. [!DNL Organization ID] utilisé pour l’Audience Manager. <!-- Verify -->

   L’organisation peut éventuellement supprimer les segments inutiles des destinations dans l’Audience Manager.

* Ajoute le pixel de synchronisation des cookies d’échange suivant au conteneur d’Audience Manager de l’entreprise afin d’améliorer la portée des campagnes client :

   * Adobe d’AdCloud : 411 (standard et automatique dans le cadre de [!DNL Identity Service] version 2.0. Organisations avec [!DNL Identity Service] Les versions antérieures à la version 2.0 doivent ajouter ce pixel à leur conteneur d’Audience Manager.

## Importation des audiences d’Audience Manager dans [!DNL Search]

### Procédure d’importation d’audiences dans [!DNL Search]

[!DNL Adobe] Le personnel effectue la plupart ou la totalité des étapes suivantes.

1. Le [!DNL Adobe] l’équipe du compte doit envoyer une demande à l’équipe des opérations de données pour configurer une intégration entre [!DNL Search] et Audience Manager. Inclure les noms des segments d’Audience Manager que vous souhaitez exporter vers [!DNL Search].

1. Dans Audience Manager, configurez les destinations pour [!DNL Search]:

   1. Créez deux nouvelles destinations : `[!UICONTROL Adobe Media Optimizer (HTTP)]` et `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] est un ancien nom de [!DNL Search].

   1. Spécifiez les segments pour chacune des destinations.

      Avec le [!UICONTROL Automatically map all current and future segments] , tous les segments sont mappés et synchronisés quotidiennement.

      Le [!UICONTROL Manually map segments] vous permet de mapper manuellement les segments à synchroniser avec la destination du lot (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Aucun segment ne doit être mappé manuellement à la destination HTTP.

1. Within [!DNL Search], soit le [!DNL Search] l’équipe de mise en oeuvre ou un utilisateur disposant du rôle de gestionnaire client d’accès direct doit lancer l’importation à partir de [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Vous devez entrer l’Experience Cloud de l’organisation. [!DNL Organization ID] ([!DNL IMS org ID]). L’ID doit être identique à celui utilisé pour le compte d’Audience Manager de l’organisation.

### Quels changements entraînent l’Audience Manager ?

L’organisation verra deux [!DNL Search] destinations dans l’Audience Manager :

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Synchronisation des données

L&#39;import initial prend environ 24 heures. Après l’importation initiale, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Où trouver vos segments synchronisés

### Dans DSP

Dans DSP, les noms de segment sont organisés par taxonomie de l’Audience Manager et disponibles avec les décomptes d’adhésion de segment correspondants dans :

* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Sur le [!UICONTROL Adobe Segments] de l’onglet [!UICONTROL Audience Targeting] .

* Dans [paramètres d’audience](/help/dsp/audiences/audience-settings.md): Sur le [!UICONTROL Adobe Segments] .

### Dans Advertising Creative

Dans [!DNL Creative], les segments sont disponibles dans les paramètres de l’expérience pour les noeuds cibles.

### Dans [!DNL Advertising Search]

Dans [!DNL [!DNL Search]], les segments sont disponibles lorsque vous créez une [!DNL Google] audience utilisant la variable [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; de [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Pour chaque [!DNL Google] audience que vous créez, [!DNL Google] fournit la taille de l’audience.

>[!MORELIKETHIS]
>
>* [Adobe des intégrations Advertising avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

