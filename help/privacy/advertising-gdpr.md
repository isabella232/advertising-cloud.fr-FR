---
title: Prise en charge de la publicité Adobe pour le Règlement général sur la protection des données
description: Découvrez les types de requêtes de données pris en charge, les valeurs de configuration et de champ requises, ainsi que des exemples de requêtes d’accès aux API utilisant des ID de produit hérités et des champs de données renvoyés.
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Prise en charge de la publicité Adobe pour le Règlement général sur la protection des données

*Pour [!DNL Adobe Advertising Search]; Adobe Advertising DSP; Adobe Advertising Creative; et Adobe Advertising DCO*

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez votre service juridique pour obtenir des conseils concernant le Règlement général sur la protection des données.

Le Règlement général sur la protection des données (RGPD), qui est entré en vigueur le 25 mai 2018, donne à tous les individus (personnes concernées) à l’intérieur des frontières de l’Union européenne (UE) le contrôle de leurs données personnelles et simplifie l’environnement réglementaire pour les affaires internationales. Cette loi s’applique à toutes les entreprises (contrôleurs de données) qui offrent des biens ou des services pour, surveiller le comportement ou collecter des données personnelles de personnes à l’intérieur des frontières de l’UE au moment du traitement de leurs données personnelles, quel que soit le lieu d’activité du contrôleur de données.

Adobe Experience Cloud agit en tant qu’entité de traitement des données pour toutes les données personnelles qu’il reçoit et stocke pour le compte de ses clients. En tant que contrôleur des données, vous déterminez les données personnelles qu’Adobe Experience Cloud traite et stocke pour vous.

Ce document décrit comment [!DNL Advertising Search]; publicité créative; DSP de publicité (Demand Side Platform); et [!DNL Advertising DCO] prendre en charge les droits d’accès et de suppression des données de vos sujets des données en vertu du RGPD à l’aide de l’API Adobe Experience Platform Privacy Service et de l’interface utilisateur du Privacy Service.

Pour plus d’informations sur ce que le RGPD signifie pour votre entreprise, voir [Le RGPD et votre entreprise](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Types de requête de données pris en charge pour Adobe Advertising

Adobe Experience Platform permet aux entreprises d’effectuer les tâches suivantes :

* Accédez aux données au niveau du cookie d’un sujet de données ou aux données au niveau de l’ID d’appareil (pour les publicités dans les applications mobiles) dans [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO].
* Suppression des données au niveau du cookie stockées dans [!DNL Search], [!DNL Creative], [!DNL DSP]ou [!DNL DCO] pour les sujets des données utilisant un navigateur ; ou supprimer des données au niveau de l’ID stockées dans [!DNL DSP] pour les sujets des données qui utilisent des applications sur des appareils mobiles.
* Vérifiez l’état d’une ou de toutes les requêtes existantes.

## Configuration requise pour envoyer des requêtes pour Adobe Advertising

Pour envoyer des demandes d’accès et de suppression de données pour Adobe Advertising, vous devez :

1. Déployez une bibliothèque JavaScript pour récupérer et supprimer les cookies des titulaires de données. La même bibliothèque, `AdobePrivacy.js`, est utilisé pour toutes les solutions Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Les requêtes envoyées à certaines solutions Adobe Experience Cloud ne nécessitent pas la bibliothèque JavaScript, mais les requêtes envoyées à Adobe Advertising le requièrent.

   Vous devez déployer la bibliothèque sur la page web à partir de laquelle vos titulaires de données peuvent envoyer des requêtes d’accès et de suppression, telles que le portail de confidentialité de votre entreprise. La bibliothèque vous aide à récupérer les cookies d’Adobe (ID d’espace de noms : `gsurferID`) afin que vous puissiez soumettre ces identités dans le cadre de demandes d’accès et de suppression via l’API Adobe Experience Platform Privacy Service.

   Lorsque le sujet des données demande la suppression de données personnelles, la bibliothèque supprime également le cookie du sujet des données du navigateur du sujet des données.

   >[!NOTE]
   >
   >La suppression des données personnelles est différente de l’exclusion, qui arrête le ciblage d’un utilisateur final avec des segments d’audience. Cependant, lorsqu’un sujet des données demande de supprimer des données personnelles de [!DNL Creative], [!DNL DSP]ou [!DNL DCO], la bibliothèque envoie également une requête à Adobe Advertising pour exclure le sujet de données du ciblage de segments. Pour les annonceurs qui utilisent [!DNL Search], nous vous recommandons de fournir aux sujets des données un lien vers [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), qui explique comment exclure le ciblage des segments ciblés.

1. Identifiez votre ID d’organisation Experience Cloud et assurez-vous qu’il est lié à vos comptes Advertising Adobe.

   Un ID d’organisation Experience Cloud est une chaîne alphanumérique de 24 caractères accompagnée de &quot;@AdobeOrg&quot;. Un ID d’organisation a été attribué à la plupart des clients Experience Cloud. Si votre équipe marketing ou votre administrateur système d’Adobes interne ne connaît pas l’ID d’organisation ou ne sait pas s’il a été configuré, contactez l’assistance clientèle d’Adobe à l’adresse gdprsupport@adobe.com. Vous aurez besoin de l’ID d’organisation pour envoyer des requêtes à l’API de confidentialité à l’aide de la variable `imsOrgID` espace de noms.

   >[!IMPORTANT]
   >
   >Contactez le représentant publicitaire Adobe de votre entreprise pour confirmer que tous les comptes Advertising Adobe de votre entreprise — y compris [!DNL DSP] des comptes ou des annonceurs, [!DNL Search] les comptes et [!DNL Creative] ou [!DNL DCO] comptes : sont liés à l’ID d’organisation Experience Cloud.

1. Utilisez l’une des méthodes suivantes : [API Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (pour les requêtes automatisées) ou la variable [Interface utilisateur du Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (pour les requêtes ad hoc) pour envoyer des requêtes d’accès et de suppression à Adobe Advertising pour le compte des sujets des données, et pour vérifier le statut des requêtes existantes.

   Pour les annonceurs qui disposent d’une application mobile pour interagir avec les sujets des données et lancer des campagnes avec DSP, vous devez télécharger les SDK mobiles prêts pour la confidentialité pour les Experience Cloud. Les SDK mobiles permettent aux contrôleurs de données de définir des indicateurs d’état d’exclusion, de récupérer l’identifiant de l’appareil du sujet de données (ID d’espace de noms : deviceID) et envoyer des requêtes à l’API du Privacy Service. Votre application mobile requiert un SDK version 4.15.0 ou supérieure.

   Lorsque vous soumettez une demande d’accès d’un sujet de données, l’API du Privacy Service renvoie les informations d’un sujet de données en fonction du cookie spécifié ou de l’ID d’appareil, que vous devez ensuite renvoyer au sujet de données.

   Lorsque vous soumettez une demande de suppression d’un sujet de données, l’ID de cookie ou l’ID d’appareil, ainsi que toutes les données sur les coûts, les clics et les recettes associés au cookie, sont supprimés du serveur.

   >[!NOTE]
   Si votre société dispose de plusieurs ID d’organisation Experience Cloud, vous devez envoyer des demandes d’API distinctes pour chacun d’eux. Vous pouvez toutefois adresser une requête d’API à plusieurs sous-solutions Adobe Advertising ([!DNL Search], [!DNL Creative], [!DNL DSP], et [!DNL DCO]), avec un compte par sous-solution.

Toutes ces étapes sont nécessaires pour Adobe Advertising. Pour plus d’informations à ce sujet et sur d’autres tâches connexes que vous devez effectuer à l’aide d’Adobe Experience Platform Privacy Service, et où trouver les éléments dont vous aurez besoin, voir [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Valeurs de champ requises dans les demandes JSON Adobe Advertising

&quot;contexte de l’entreprise&quot; :

* `"namespace": **imsOrgID**`
* `"value":` &lt;*votre valeur d’identifiant de l’organisation IMS*>

`"users":`

* `"key":` &lt;*généralement le nom du sujet de données*>

* `"action":` both `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (qui indique que la variable [!DNL adcloud] espace du cookie)

   * `"value":` &lt;*la valeur de l’ID de cookie du sujet de données réel telle qu’elle est extraite de`AdobePrivacy.js`*>

* `"include": **adCloud**` (qui est le produit Adobe qui s’applique à la requête)

* `"regulation": **gdpr**` (qui est la réglementation sur la confidentialité qui s’applique à la demande)

## Exemple de demande envoyée par le titulaire de données à l’aide d’un identifiant utilisateur Adobe Advertising récupéré `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## Champs de données renvoyés pour les demandes d’accès

Voici un exemple de réponse d’accès pour Adobe Advertising.

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
