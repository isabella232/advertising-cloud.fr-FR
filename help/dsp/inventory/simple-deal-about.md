---
title: A propos [!UICONTROL Simple Ad Serving]
description: En savoir plus sur [!UICONTROL Simple Ad Serving] traite à l’aide de pixels de suivi d’événement.
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# A propos [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fournit une diffusion publicitaire et des rapports garantis et non décidés pour un éditeur spécifié et un seul type d’annonce à l’aide d’un seul emplacement dédié. Utilisation [!DNL Simple Ad Serving] lorsque votre éditeur ne peut pas exécuter votre transaction via des identifiants d’opération. L’éditeur gère l’ensemble du ciblage, du rythme et de la limitation du budget, ainsi que la limitation de la fréquence. Exécutez ces transactions via des pixels de suivi d’événement.

Avec [!UICONTROL Simple Ad Serving], chaque publicité est diffusée directement par l’éditeur (serveur de site) et DSP fournit un pixel de suivi d’événement à envoyer à l’éditeur, qui doit mettre en oeuvre le pixel et le trafic des publicités DSP. Selon le type d’inventaire, les pixels d’événement mesurent les événements d’impression, de clic publicitaire et de lecture vidéo.

Les types d’annonces suivants sont disponibles :

* version preroll standard de bureau
* tablette et preroll Mobile standard
* preroll standard de la télévision connectée
* display
* audio

Vous pouvez créer un [!UICONTROL Simple Ad Serving] deal [!UICONTROL Inventory] > [!UICONTROL Deals] vue. DSP génère automatiquement un emplacement avec le sous-type &quot;[!DNL Simple ad serving]&quot; pour la publicité. L’emplacement cible l’opération, mais n’autorise pas de ciblage, de budget ni de limitation de la fréquence supplémentaires. Vous ne pouvez modifier que certains des paramètres de la transaction, tels que le nom de la transaction, le CPM, les impressions et les dates de vol.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] les emplacements ne sont pas conformes aux fonds utilisables du compte ni aux budgets de campagne et de package. Cependant, les dépenses sont suivies et comptabilisées dans ces budgets. Même lorsque le CPM est de 0 $, les données d’événement sont toujours suivies.

>[!MORELIKETHIS]
>
>* [Créez un [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [Modifier [!UICONTROL Simple Ad Serving] Paramètres de transaction](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] Paramètres](simple-deal-settings.md)
>* [Afficher un rapport détaillé pour une transaction](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
