---
title: 'Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’exclusion de la vente par les consommateurs'
description: Découvrez la prise en charge de la capture des demandes d’opposition à la vente des consommateurs.
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: adb3118d291d110e653a62cc1a323410b1a596b2
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---

# Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’exclusion de la vente par les consommateurs

*Pour Adobe Advertising Cloud Demand Side Platform*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez votre service juridique pour obtenir des conseils concernant le California Consumer Privacy Act.

Le California Consumer Privacy Act (CCPA) est la nouvelle loi californienne sur la protection de la vie privée, qui est entrée en vigueur le 1er janvier 2020. Le CCPA accorde aux résidents de Californie de nouveaux droits concernant leurs informations personnelles et impose des responsabilités en matière de protection des données à certaines entités qui exercent des activités en Californie. Le CCPA accorde aux consommateurs le droit d’accéder à leurs données et de les supprimer ainsi que le droit de se désinscrire de certaines activités qualifiées de &quot;vente&quot; d’informations personnelles à un tiers.

En tant qu’entreprise, vous déterminerez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

En tant que fournisseur de services, Adobe Advertising Cloud fournit une assistance à votre entreprise pour qu’elle remplisse ses obligations en vertu du CCPA qui s’appliquent à l’utilisation des produits et services Advertising Cloud, y compris la gestion des demandes de clients d’accès et de suppression des informations personnelles et la gestion des demandes de clients de se désabonner de la vente des informations personnelles.

Ce document décrit comment Adobe Advertising Cloud Demand Side Platform (DSP), en tant que fournisseur de services, soutient le droit du consommateur de se désinscrire de la &quot;vente&quot; des &quot;informations personnelles&quot;, car chaque terme est défini par le CCPA. Elle comprend des informations sur la manière de communiquer les demandes d’opposition à la vente à Advertising Cloud et de récupérer les rapports des demandes d’opposition à la vente de votre entreprise.

Pour plus d’informations sur la façon dont Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) et Media Optimizer DCO prennent en charge les droits d’accès et de suppression des informations personnelles des clients, voir [Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’accès et de la suppression des données des consommateurs](/help/privacy/ad-cloud-ccpa-access-delete.md).

Pour plus d’informations sur les services de confidentialité Adobe pour le CCPA, reportez-vous à la section [Centre de traitement des données personnelles des Adobes](https://www.adobe.com/privacy/ccpa.html).

## Communication de demandes d’opposition à la vente aux consommateurs à Advertising Cloud

Vous pouvez communiquer les demandes d’opposition à la vente des consommateurs à l’aide de l’une des méthodes suivantes :

* un segment d’opposition à la vente des informations personnelles créé dans Advertising Cloud DSP
* API Adobe Experience Platform Privacy Service

### Méthode 1 : Communication des demandes d’opposition à la vente des informations personnelles du CCPA à l’aide d’une [!UICONTROL CCPA Opt-Out-of-Sale] Segment dans Advertising Cloud DSP

>[!NOTE]
>
>Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

1. Connectez-vous au compte de l’annonceur dans Advertising Cloud DSP à l’adresse [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Créez un segment d’opposition à la vente des informations personnelles (CCPA) et implémentez le pixel de segment pour capturer les demandes d’opposition.](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Méthode 2 : Communication des demandes d’opposition à la vente des informations personnelles du CCPA à l’aide de l’API Adobe Experience Platform Privacy Service

*Les annonceurs ont affecté un Adobe Experience Cloud [!DNL Organization ID] ([!DNL IMS Org ID]) uniquement*

1. Déployez une bibliothèque JavaScript pour récupérer les cookies de votre client. La même bibliothèque, `AdobePrivacy.js`, est utilisé pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes envoyées à certaines solutions Adobe Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes envoyées à Advertising Cloud le nécessitent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des demandes d’opposition à la vente, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies d’Adobe (ID d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre de demandes d’opposition à la vente via l’API Adobe Experience Platform Privacy Service.

1. Identifiez votre identifiant de l&#39;organisation IMS et assurez-vous qu&#39;il est lié à vos comptes Advertising Cloud.

   Un identifiant de l’organisation IMS est une chaîne alphanumérique de 24 caractères annexée avec @AdobeOrg. Un identifiant de l’organisation IMS a été attribué à la plupart des clients Adobe Experience Cloud. Si votre équipe marketing ou votre administrateur système d’Adobes interne ne connaît pas l’identifiant de l’organisation IMS de votre entreprise ou ne sait pas s’il a été configuré, contactez l’assistance clientèle Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’identifiant de l’organisation IMS pour envoyer des requêtes à l’API de confidentialité.

   >[!IMPORTANT]
   >
   >Contactez le représentant Advertising Cloud de votre entreprise pour confirmer que tous les comptes Advertising Cloud de votre entreprise — y compris [!DNL DSP] des comptes ou des annonceurs, [!DNL Search] les comptes et [!DNL Creative] ou [!DNL DCO] comptes : sont liés à votre identifiant de l’organisation IMS.

1. Utilisez l’API Adobe Experience Platform Privacy Service pour [envoi de demandes d’exclusion de la vente](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) à Advertising Cloud pour le compte des consommateurs et pour vérifier le statut des requêtes existantes.

   Consultez l’ Annexe ci-dessous pour obtenir un exemple de demande d’opposition à la vente.

   >[!NOTE]
   Si votre entreprise possède plusieurs identifiants d’organisation de service Adobe Experience Cloud Identity Management (identifiants d’organisation IMS), vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois adresser une requête d’API à plusieurs sous-solutions Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP], et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour recevoir l’assistance d’Advertising Cloud. Pour plus d’informations à ce sujet et sur d’autres tâches connexes que vous devez effectuer à l’aide d’Adobe Experience Platform Privacy Service, et où trouver les éléments dont vous aurez besoin, voir [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Récupération des rapports des consommateurs qui ont soumis des demandes d’exclusion de la vente

Advertising Cloud génère des rapports mensuels sur les identifiants que les clients ont envoyés pour les demandes d’exclusion de la vente pour le compte. Chaque rapport est disponible sous la forme d’un fichier texte de données séparées par des tabulations compressé au format GZIP. Les données consolident les demandes capturées à l’aide des segments d’opposition à la vente des CCPA qui ont été créés dans Advertising Cloud DSP et les envois effectués via l’API du Privacy Service. Les identifiants utilisateur capturés dans les segments d’opposition à la vente des informations personnelles (CCPA) sont identifiés par le segment et par l’annonceur. Les rapports sont générés le premier de chaque mois pour le mois précédent. Par exemple, la liste mensuelle des utilisateurs pour juin est disponible le 1er juillet.

Vous pouvez récupérer les liens vers les rapports mensuels créés au cours des trois mois précédents, depuis Advertising Cloud DSP ou à l’aide d’Advertising Cloud. [!DNL Trafficking API]. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

### Méthode 1 : Récupération des rapports d’exclusion de la vente par les consommateurs dans Advertising Cloud DSP

1. Connectez-vous au compte de l’annonceur dans Advertising Cloud DSP à l’adresse [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Récupération des rapports](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Méthode 2 : Récupération des rapports d’exclusion de la vente par les consommateurs à l’aide d’Advertising Cloud [!DNL Trafficking API]

Cette fonctionnalité est disponible pour les organisations qui utilisent la variable [!DNL Trafficking API]. Consultez la documentation relative à la [!DNL Trafficking API] pour plus d’informations.

Si votre entreprise n’utilise pas la variable [!DNL Trafficking API] mais est intéressé par plus d’informations, contactez votre [!DNL Adobe] gestionnaire de compte.

## Annexe : Exemple [!UICONTROL CCPA Opt-Out-of-Sale] Demande d’utilisateurs d’API Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

où :

* `"namespace": "AdCloud"` indique que la variable `AdCloud` espace de cookie et la valeur correspondante est l’ID de cookie du client tel qu’il est récupéré à partir de `AdobePrivacy.js`
* `"include": ["AdCloud"]` indique que la demande s’applique à Advertising Cloud
