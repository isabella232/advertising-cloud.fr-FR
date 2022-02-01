---
title: '[!UICONTROL Simple Ad Serving] Paramètres de transaction'
description: En savoir plus sur les paramètres disponibles pour [!UICONTROL Simple Ad Serving] les offres.
feature: DSP Simple Ad Serving
source-git-commit: 22f5d8279fadfcf79e2cd41566321f423d63eb16
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Paramètres de transaction

## Nouveau [!UICONTROL Simple Ad Serving] Offres

### [!UICONTROL Select Ad Source]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Type de média pour cette affaire : *[!UICONTROL Video],* *[!UICONTROL Display],* ou *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Nom de l’éditeur qui vend cet inventaire. Recherchez un éditeur en saisissant au moins les deux premiers caractères du nom. Pour ajouter un éditeur qui n’est pas répertorié, contactez votre [!DNL Adobe] gestionnaire de compte. |
| **[!UICONTROL Advertiser]** | Un seul annonceur sur le compte qui peut accéder à cette offre. Sélectionnez également l&#39;opération et (éventuellement) le kit dans lequel l&#39;opération est disponible. |
| **[!UICONTROL Media Quality Assessment?]** | (Certains utilisateurs) Permet à la publicité de s’exécuter sur un autre DSP pour la vérification tierce. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | La seule option est *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nouvelles offres uniquement) Indique si :<ul><li>*[!UICONTROL Create New]:* Pour créer une publicité pour cette opération.</li><li>*[!UICONTROL Select Ads]:* Pour utiliser une publicité existante pour cette opération.</li></ul> |
| **[!UICONTROL Ad Type]** | Type d’annonce pour cette opération. Si vous allez créer de nouvelles publicités pour l’opération, incluez la taille ou la durée de la publicité, selon vos besoins. Les options disponibles varient en fonction du type de média. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(Lorsque vous utilisez des publicités existantes) Publicités à inclure dans l’offre. Cochez la case en regard de chaque publicité à inclure.

### [!UICONTROL Select & Upload [Media Type]]

(Nouvelles publicités uniquement) Screens pour créer une [publicité propriétaire](/help/dsp/campaign-management/ads/ad-create.md) ou [publicité tierce](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Le coût par millier d’impressions (CPM), tel qu’il est reflété dans la carte de taux de votre contrat. Contactez votre [!DNL Adobe] gestionnaire de compte pour cette valeur. <br><br>Indiquez également la devise de l’opération. Tous les utilisateurs peuvent sélectionner USD ou, si le SSP prend en charge d’autres devises, la devise du compte DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Facultatif) Des frais tiers statiques à suivre en tant que coût non facturable et la devise de l’opération.<br><br>Tous les utilisateurs peuvent sélectionner USD ou, si le SSP prend en charge d’autres devises, la devise du compte DSP. **REMARQUE :** Les frais facturables sont reflétés dans la variable [!UICONTROL Net CPM] mesure. |
| **[!UICONTROL Third Party Fee Description]** | (Facultatif) Description des frais tiers. |
| **[!UICONTROL Flight Dates]** | Les dates de début et de fin du trafic utilisant cette transaction. Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération. Les balises de publicité renvoient une réponse uniquement pendant le vol spécifié.<br><br> La bonne pratique consiste à créer une campagne de diffusion d’annonces simple distincte d’une durée d’un an et à y créer des pixels de suivi. |
| **[!UICONTROL Impressions]** | (Facultatif) Nombre estimé d’impressions que vous prévoyez d’exécuter à l’aide de cette opération. Cette valeur est utilisée à des fins de suivi uniquement et pour marquer les diffusions lorsque les objectifs de diffusion sont atteints ; l’éditeur contrôle la diffusion réelle de l’annonce. La bonne pratique consiste à saisir un grand nombre d’impressions afin de garder la balise principale dans DSP afin qu’elle puisse être renouvelée ou étendue si nécessaire. |
| **[!UICONTROL Deal Name]** | Nom de l’opération. Saisissez un nom ou sélectionnez *[!UICONTROL Auto Generate Deal Name]* pour permettre DSP générer un nom basé sur les détails de l’opération.<br><br>Exemple de nom généré automatiquement : `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Lecture seule) Publicités faisant partie de l’offre. Pour modifier une publicité, cliquez sur son nom. Pour supprimer une publicité de l’opération, cliquez sur **[!UICONTROL X]** en regard du nom de la publicité. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [A propos [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Créez un [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [Affichage des pixels de suivi d’événement pour un événement [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)

