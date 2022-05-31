---
title: À propos de l’activation de segments authentifiés à partir des sources d’audience
description: Découvrez comment ingérer des segments propriétaires à partir d’une plateforme de données client.
feature: DSP Audiences
source-git-commit: aac60e8fddce1db3d0101a617fca3af970043648
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# À propos de l’activation de segments authentifiés à partir des sources d’audience

<!-- Doesn't specifically explain what you can do in our UI -->
*Fonction bêta*

Advertising Cloud DSP peut ingérer des segments propriétaires composés de signaux authentifiés créés dans une plateforme de données client (CDP). Vous pouvez utiliser les segments ingérés comme cibles pour vos emplacements.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP est intégré à la fonction [la valeur [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform.

Dans [!DNL Real-time CDP], *destinations* sont des connexions à des plateformes de données externes qui permettent une activation transparente des données. Par exemple, vous pouvez utiliser des destinations pour activer vos relations client connues (telles que des adresses électroniques hachées) pour la publicité ciblée dans des formats numériques pris en charge par DSP.

Pour plus d’informations sur les destinations, voir l’Experience Platform [Guide des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), y compris un aperçu du produit, des instructions pour [création d’espaces de travail de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) et [création de connexions à destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), et [activation des données vers les destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Processus d’utilisation de l’intégration DSP avec [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Autoriser DSP traduire les segments de données client en [!DNL LiveRamp RampIDs]](source-durable-id.md) qui sont reconnaissables dans un environnement admissible.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Création d’une source d’audience](source-create.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire.

1. [Configurez une [!DNL Real-Time CDP] connexion de destination dans l’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).<!-- Verify URL once it's published. -->

Pour obtenir une assistance supplémentaire, contactez votre [!DNL Adobe] équipe de compte ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Activation des segments authentifiés à partir de partenaires d’identification durables](source-durable-id.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Présentation du catalogue des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)

