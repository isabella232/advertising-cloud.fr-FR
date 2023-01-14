---
title: Création d’une source d’audience pour activer les audiences propriétaires
description: Découvrez comment créer une source pour importer des audiences dans votre compte ou un compte publicitaire.
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Création d’une source d’audience pour activer les audiences propriétaires

*Fonction bêta*

<!-- Will this remain for admin users/Adobe account teams only? -->

Créez une source pour importer des audiences dans votre compte DSP ou un compte publicitaire. Actuellement, vous pouvez importer des audiences depuis [la valeur [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Après avoir créé une source pour le [!DNL Real-Time CDP], vous devrez activer votre [!DNL Real-Time CDP] audiences via la destination Adobe Advertising DSP dans [!DNL Real-Time CDP] pour commencer à les importer. Voir [les étapes du workflow d’activation ;](source-about.md#workflow-sources).

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Cliquez sur [!UICONTROL Add Source].

1. Dans le [!UICONTROL Select a Type] sélectionnez le type de source.

   *[!UICONTROL RT-CDP]*: Ce type de source, pour [la valeur [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), est la seule option.

1. Spécifiez la variable [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Saisissez le reste [paramètres source](source-settings.md).

   Conserver une copie du [!UICONTROL Source Key] qui est généré. Vous aurez besoin de la valeur plus tard.

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans Experience Platform, créez une connexion de destination de DSP Advertising à l’aide du [!UICONTROL Source Key] qui a été généré dans les paramètres source DSP.

Pour obtenir des instructions sur l’activation de la connexion DSP destination, la sélection de segments et l’accès aux autorisations de contrôle, voir &quot;[Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Paramètres de la source d’audience](source-settings.md)
>* [À propos de l’activation de segments authentifiés à partir des sources d’audience](source-about.md)
>* [Activation des segments authentifiés à partir de partenaires d’identification durables](source-durable-id.md)<!-- title?-->
>* [Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)

