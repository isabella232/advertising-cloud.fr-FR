---
title: Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act &#58; Prise en charge de l’accès et de la suppression des données des consommateurs
description: Découvrez les types de requêtes de données pris en charge, les valeurs de configuration et de champ requises, ainsi que des exemples de requêtes d’accès aux API à l’aide d’ID de produit hérités et de champs de données renvoyés.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’accès et de la suppression des données des consommateurs

*Pour Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP et Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez votre service juridique pour obtenir des conseils concernant le California Consumer Privacy Act.

Le California Consumer Privacy Act (CCPA) est la nouvelle loi californienne sur la protection de la vie privée, qui est entrée en vigueur le 1er janvier 2020. Le CCPA accorde aux résidents de Californie de nouveaux droits concernant leurs informations personnelles et impose des responsabilités en matière de protection des données à certaines entités qui exercent des activités en Californie. Le CCPA accorde aux consommateurs le droit d’accéder à leurs informations personnelles et de les supprimer, ainsi que le droit de se désinscrire de certaines activités qualifiées de &quot;vente&quot; d’informations personnelles à un tiers.

En tant qu’entreprise, vous déterminerez les données personnelles que Adobe Experience Cloud traite et stocke pour vous.

En tant que fournisseur de services, Adobe Advertising Cloud fournit une assistance à votre entreprise pour qu’elle remplisse ses obligations en vertu du CCPA qui s’appliquent à l’utilisation des produits et services Advertising Cloud, y compris la gestion des demandes d’accès et de suppression des informations personnelles et la gestion des demandes de refus de vente des informations personnelles.

Ce document décrit comment Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) et [!DNL Media Optimizer DCO] — en tant que fournisseurs de services — soutiennent les droits des consommateurs à accéder et supprimer des informations personnelles à l’aide de l’Adobe [!DNL Experience Platform Privacy Service API] et [!DNL Privacy Service UI].

Pour plus d’informations sur la manière dont Advertising Cloud DSP prend en charge le droit des consommateurs de se désabonner de la vente des informations personnelles, voir [Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’exclusion des consommateurs](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

Pour plus d’informations sur les services de confidentialité Adobe pour le CCPA, consultez le [Centre de confidentialité des Adobes](https://www.adobe.com/privacy/ccpa.html).

## Types de requête de données pris en charge pour Advertising Cloud

Adobe Experience Platform permet aux entreprises d’effectuer les tâches suivantes :

* Accédez aux données au niveau du cookie d’un consommateur ou aux données au niveau de l’identifiant de l’appareil (pour les publicités dans les applications mobiles) dans [!DNL Search], [!DNL Creative], [!DNL DSP] ou [!DNL DCO].
* Supprimer les données au niveau du cookie stockées dans [!DNL Search], [!DNL Creative], [!DNL DSP] ou [!DNL DCO] pour les consommateurs utilisant un navigateur ; ou supprimez les données au niveau de l’ID stockées dans [!DNL DSP] pour les consommateurs qui utilisent des applications sur des périphériques mobiles.
* Vérifiez l’état d’une ou de toutes les requêtes existantes.

## Configuration requise pour envoyer des requêtes pour Advertising Cloud

Pour envoyer des demandes d’accès et de suppression des informations personnelles des consommateurs à partir d’Advertising Cloud, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer les cookies de votre client. La même bibliothèque `AdobePrivacy.js` est utilisée pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes envoyées à certaines solutions Adobe Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes envoyées à Advertising Cloud le nécessitent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos clients peuvent envoyer des requêtes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies d’Adobe (ID d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre de demandes d’accès et de suppression via [!DNL  Adobe Experience Platform Privacy Service API].

   Lorsque le client demande de supprimer des données personnelles, la bibliothèque supprime également le cookie du client du navigateur du client.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de l’exclusion, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un client demande de supprimer des données personnelles de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], la bibliothèque envoie également une demande à Advertising Cloud pour exclure le client du ciblage de segments. Pour les annonceurs disposant de [!DNL Search], nous vous recommandons de fournir à vos clients un lien vers [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), qui explique comment se désinscrire du ciblage de segments d’audience.

1. Identifiez votre identifiant de l&#39;organisation IMS et assurez-vous qu&#39;il est lié à vos comptes Advertising Cloud.

   Un identifiant de l’organisation IMS est une chaîne alphanumérique de 24 caractères accompagnée de &quot;@AdobeOrg&quot;. Un identifiant de l’organisation IMS a été attribué à la plupart des clients Adobe Experience Cloud. Si votre équipe marketing ou votre administrateur système d’Adobes interne ne connaît pas l’identifiant de l’organisation IMS de votre entreprise ou ne sait pas s’il a été configuré, contactez l’assistance clientèle Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’identifiant de l’organisation IMS pour envoyer des requêtes à l’API de confidentialité.

   >[!IMPORTANT]
   >
   >Contactez le représentant Advertising Cloud de votre entreprise pour confirmer que tous les comptes Advertising Cloud de votre organisation — y compris les comptes [!DNL DSP] ou les annonceurs, les comptes [!DNL Search] et les comptes [!DNL Creative] ou [!DNL DCO] — sont liés à votre ID d’organisation IMS.

1. Utilisez l’ [API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les requêtes automatisées) ou l’[interface utilisateur Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (pour les requêtes ad hoc) pour envoyer des requêtes d’accès et de suppression des informations personnelles à Advertising Cloud pour le compte des consommateurs et pour vérifier le statut des requêtes existantes.

   Pour les annonceurs qui disposent d’une application mobile pour interagir avec leurs clients et lancer des campagnes avec [!DNL DSP], vous devez télécharger les SDK mobiles prêts pour la confidentialité pour les Experience Cloud. Les SDK mobiles permettent aux entreprises de définir des indicateurs d’état d’exclusion, de récupérer l’identifiant d’appareil du consommateur (ID d’espace de noms : `deviceID`) et envoyer des requêtes à l’API du Privacy Service. Votre application mobile requiert un SDK version 4.15.0 ou supérieure.

   Lorsque vous envoyez une demande d’accès du consommateur, l’API du Privacy Service renvoie les informations du consommateur en fonction du cookie ou de l’identifiant d’appareil spécifié, que vous devez ensuite renvoyer au consommateur.

   Lorsque vous soumettez une demande de suppression de client, l’ID de cookie ou l’ID d’appareil, ainsi que toutes les données de coût, de clic et de recettes associées au cookie, sont supprimés du serveur.

   >[!NOTE]
   Si votre entreprise possède plusieurs identifiants d’organisation de service Adobe Experience Cloud Identity Management (identifiants d’organisation IMS), vous devez envoyer des requêtes d’API distinctes pour chacun d’eux. Vous pouvez toutefois adresser une requête d’API à plusieurs sous-solutions Advertising Cloud ([!DNL Search], [!DNL Creative], [!DNL DSP] et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour recevoir l’assistance d’Advertising Cloud. Pour plus d’informations à ce sujet et sur d’autres tâches connexes que vous devez effectuer à l’aide d’Adobe Experience Platform Privacy Service, et où trouver les éléments dont vous avez besoin, voir [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valeurs de champ requises dans les requêtes JSON Advertising Cloud

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;>votre valeur d’identifiant de l’organisation IMS *>*

&quot;users&quot; :

* `"key":` &lt;>généralement le nom du client *>*

* `"action":` ou  `**access**` ou  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique l’espace de cookie adcloud)

   * `"value":` &lt;>la valeur de l’ID de cookie du client réel, telle qu’elle est extraite de  `AdobePrivacy.js`*>*

* `"include": **adCloud**` (qui est le produit Adobe qui s’applique à la requête)

* `"regulation": **ccpa**` (qui est la réglementation sur la confidentialité qui s’applique à la demande)

## Exemple de demande envoyée par un client à l’aide d’un identifiant utilisateur Advertising Cloud récupéré dans AdobePrivacy.js

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## Champs de données renvoyés pour les demandes d’accès

Voici un exemple de réponse d’accès aux informations personnelles pour Advertising Cloud.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
