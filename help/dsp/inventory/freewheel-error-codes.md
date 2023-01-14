---
title: Codes d’erreur pour [!DNL FreeWheel] Envois de publicités
description: Référencez les codes d’erreur renvoyés pour les envois d’annonces à [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 2eb93971-ba82-4de8-96c5-48524d628b70
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 2%

---

# Codes d’erreur pour [!DNL FreeWheel] Envois de publicités

Les messages d’erreur relatifs aux envois d’annonces ayant échoué peuvent provenir de DSP Advertising ou de [!DNL FreeWheel]. Les messages d’erreur s’affichent dans la [!UICONTROL API Response] dans la colonne [[!UICONTROL Freewheel Status] dialog](freewheel-check-status.md).

## Erreurs internes de la publicité DSP

| Message d’erreur | Description | Étapes suivantes |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] n’a pas encore répondu que l’envoi a réussi ou échoué. | Vérifiez à nouveau l’état dans 10 minutes. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] n’accepte pas les publicités britanniques sans numéros d’horloge attribués. | Attribuez un numéro d’horloge à la publicité, puis soumettez-la à nouveau. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Le transcodeur n’avait pas terminé de transcoder la publicité lorsque vous avez tenté d’envoyer la publicité. | Patientez dix minutes, puis renvoyez la publicité. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | L’accord soumis n’est pas configuré comme un accord garanti par la programmation. [!DNL FreeWheel] accepte uniquement les offres garanties. | Configurez l’ID d’opération en tant qu’opération garantie par un programme. La publicité est automatiquement envoyée à [!DNL FreeWheel] lorsque vous enregistrez l’emplacement par défaut garanti par la programmation à la fin du processus d’ID d’opération. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | L’ID de transaction envoyé n’existe pas ou n’est pas principal du côté de l’Adobe. | Assurez-vous que l’opération est principale, puis soumettez à nouveau l’annonce. |
| [!DNL \[public_id=]\&lt;deal>] n’existe pas | L’ID d’opération envoyé n’existe pas sur la variable [!DNL FreeWheel] fin. | Contactez votre [!DNL FreeWheel] représentant pour confirmer l’ID de transaction. |
| [!DNL Ad with identifier] \&lt;*nom de la publicité*\> [!DNL was not found.] | La clé publicitaire envoyée n’existe pas ou n’est pas principale du côté Adobe. | Recherchez la clé de publicité correcte, puis soumettez à nouveau la publicité. |
| [!DNL Pending Submission] | La soumission est toujours en attente. | Actualisez la page. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Erreurs d’API

| Code | Signification | Description | Étapes suivantes |
|--- |--- |--- |--- |
| 401 | Non autorisé | Informations d’accès incorrectes, manquantes ou non valides. | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 403 | Interdit | Le serveur a compris la demande mais refuse de l’autoriser. | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 404 | Introuvable | La ressource que vous avez demandée n’est pas disponible. Si l’ID créatif est introuvable dans l’opération du PUT, un 404 est renvoyé. | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 405 | Méthode non autorisée | Une requête d’une ressource a été effectuée à l’aide d’une méthode de requête non prise en charge par cette ressource (par exemple, en utilisant GET sur une méthode qui nécessite l’envoi de données par un POST ou en utilisant PUT sur une ressource en lecture seule). | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 408 | Délai d’expiration de la requête | Un délai d’expiration s’est produit pendant le traitement de cette requête. Les dépassements de délai sont généralement dus à des demandes simultanées d’accès exclusif à certaines ressources. | Soumettez à nouveau la demande lorsque vous recevez ce statut. Si le problème persiste, contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 422 | Entité non traitable | Ressource non valide. Cette erreur se produit lorsque le corps de la requête n’est pas valide ou que la ressource créée/mise à jour est non valide (par exemple, si l’ID de transaction est introuvable). Voir [Erreurs de l’API 422 de FreeWheel](#freewheel-422-errors) pour plus d’informations. | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |
| 500 | Erreur interne du serveur | Erreur du système API. | Contactez votre [!DNL Adobe] l&#39;équipe du compte. |

{style=&quot;table-layout:auto&quot;}

## [!DNL Freewheel] Erreurs API 422 {#freewheel-422-errors}

| Code | Code HTTP | Description |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Le format json des données de requête n’est pas valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_VALIDATION_FAILURE | 422 | Les données de requête ne comportent pas de champs obligatoires ou présentent un type de données non valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DEAL_INVALID | 422 | L&#39;accord est mal configuré ou n&#39;existe pas. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DEAL_GET_FAILURE | 422 | L&#39;accord n&#39;a pas été trouvé ou sa configuration a un problème. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | L’URL de création n’est pas valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Le créatif n’était pas lié aux noeuds des unités publicitaires de l’opération. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | Le créatif n&#39;a pas été mis à jour. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DSP_GET_FAILURE | 422 | Le DSP n&#39;existe pas dans le système. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | Le créatif n’a pas été dissocié des unités publicitaires. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Le créatif n&#39;a pas été supprimé. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | L’URL n’a pas été détectée. |
| DATA_ENTITY_NOT_FOUND | 422 | Le créatif n&#39;existe pas. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Présentation de la configuration de transactions garanties par la programmation dans [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Envoyer une publicité pour une transaction garantie par un programme à [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Vérification de l’état des publicités pour [!DNL FreeWheel] Offres garanties par la programmation](/help/dsp/inventory/freewheel-check-status.md)

