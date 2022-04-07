---
title: Créer plusieurs publicités tierces
description: Découvrez comment créer plusieurs publicités tierces à la fois.
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Créer plusieurs publicités tierces

Vous pouvez créer jusqu’à 500 annonces tierces à la fois en chargeant des balises qui pointent vers des ressources de création hébergées sur des serveurs de publicités tiers. Vous pouvez inclure des pixels de suivi pour les annonces.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Vous pouvez transférer l’une des options suivantes : [!DNL DoubleClick] et [!DNL Flashtalking] des feuilles de balises ou un fichier renseigné manuellement à l’aide du modèle fourni.

>[!TIP]
>
> La bonne pratique consiste à utiliser des publicités tierces diffusées en toute sécurité via HTTPS. Les URL diffusées à l’aide de HTTPS commencent par &quot;https&quot;.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne dans laquelle la publicité sera incluse.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**. Dans la section Types de publicité du menu, cliquez sur **[!UICONTROL Bulk upload ads]**.

1. Sélectionnez le serveur publicitaire sur lequel la publicité est hébergée : *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* ou *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] et [!DNL Flashtalking] publicités) Sélectionnez le type de balise à utiliser pour chaque ressource vidéo et chaque ressource d’affichage. Les options disponibles varient en fonction du serveur de publicités.

1. (Publicités sur tous les serveurs de publicités, à l’exception de [!DNL DoubleClick] et [!DNL Flashtalking]) Cliquez sur **[!UICONTROL Download this template]** pour télécharger un modèle dans [!DNL Microsoft Excel] format de feuille de calcul (XLSX), que vous pouvez renseigner avec des données de publicité et enregistrer localement. Les colonnes requises incluent [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag], et [!UICONTROL Ad Types].

1. Cliquez sur **[!UICONTROL Upload]** et sélectionnez un fichier aux formats .xlsx ou .xls sur votre appareil ou votre réseau.

   Pour [!DNL DoubleClick] et [!DNL Flashtalking] publicités, téléchargez des feuilles de balises non modifiées à partir du serveur d’annonces. Pour les autres serveurs d’annonces, utilisez le modèle que vous avez téléchargé à l’étape 3.

1. Une fois le transfert terminé, cliquez sur **[!UICONTROL Start Building Ads]**.

1. Vérifiez les détails et l’état de chaque publicité :

   1. Vérifiez l’état de chaque publicité, en fonction des contrôles de validation sur la balise chargée.
   1. (Facultatif) Effectuez l’une des opérations suivantes pour chaque publicité :
      * Pour prévisualiser une publicité, cliquez sur ![play](/help/dsp/assets/play.png) dans la ligne publicitaire.
      * Pour modifier les détails de la publicité, cliquez sur ![edit](/help/dsp/assets/edit.png), modifiez les détails, puis cliquez sur **Enregistrer**.
      * Pour supprimer une publicité, cliquez sur **[!UICONTROL X]** dans la ligne publicitaire.

1. Cliquez sur **[!UICONTROL Create *N *Publicités]**.

1. Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Done]**.

   * (Si une publicité est refusée ; (facultatif) Pour modifier l’enregistrement de la publicité et la soumettre de nouveau pour révision :
      1. Cliquez sur le nom de la publicité.
      1. Modifiez les paramètres de la publicité.
      1. Cliquez sur **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Spécifications des publicités](/help/dsp/assets/ad-specs.pdf)
>* [Créer une publicité unique](ad-create.md)
>* [Vidéo : Comment télécharger en bloc des balises publicitaires tierces](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

