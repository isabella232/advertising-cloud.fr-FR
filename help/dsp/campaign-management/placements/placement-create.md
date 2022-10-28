---
title: Création d’un emplacement
description: Découvrez comment créer un emplacement.
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 1%

---

# Création d’un emplacement

>[!TIP]
>
>Créez des emplacements en fonction d’objectifs de campagne spécifiques ou de besoins de création de rapports.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne dans laquelle l&#39;emplacement sera inclus.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**. Dans le [!UICONTROL Placement Types] dans le menu, cliquez sur le type d’emplacement.

   Le type d’emplacement détermine le type d’annonce que l’emplacement peut inclure.

1. Saisissez le [paramètres de placement](placement-settings.md):

   1. Spécifiez la variable [!UICONTROL Basics] paramètres.

   1. Dans le [!UICONTROL Goals] , spécifiez la variable [!UICONTROL Gross Budget] et, éventuellement, spécifier des objectifs d’emplacement supplémentaires.

      Certains champs ont des valeurs par défaut que vous pouvez remplacer.

      Si le module auquel l’emplacement est affecté a une fréquence au niveau du module, vos objectifs et paramètres de fréquence refléteront les paramètres du module.

   1. (Facultatif) Dans le [!UICONTROL Geo-Targeting] , réduisez les emplacements inclus ou exclus.

      Si vous n’identifiez pas des emplacements spécifiques, tous les emplacements sont ciblés.

      >[!NOTE]
      >
      >Les emplacements de ville et de zone desservie ne sont pas disponibles pour les emplacements Roku.

   1. Dans le [!UICONTROL Inventory Targeting] , réduisez les sources d’inventaire à inclure ou à exclure.

      Pour la plupart des types d’emplacements, tous les types d’inventaire et toutes les sources pour chaque type sont inclus par défaut. Pour [!DNL Roku] emplacements, vous devez spécifier le type d’inventaire et les sources.

   1. (Facultatif) Dans le [!UICONTROL Site Targeting] , limitez les sites à cibler et spécifiez les sites à exclure.

   1. (Facultatif) Dans le [!UICONTROL Audience Targeting] section :

      1. Circonscrivez le public. Cela inclut la sélection des segments d’audience à cibler dans l’emplacement.

         Pour [!DNL] Emplacements Roku, vous pouvez tirer parti des [L’audience unique de DSP avec [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) en incluant un ou plusieurs segments d’audience pouvant être mis en correspondance avec la variable [!DNL Roku] Jeu de données déterministes (opt-in).
   1. (Pour les campagnes avec un ciblage au niveau des personnes ; (facultatif) Lorsque l’emplacement cible une ou plusieurs audiences spécifiques, activez le ciblage interpériphérique basé sur les personnes pour l’emplacement.

      Le ciblage multi-appareils basé sur les personnes est fourni par [!DNL LiveRamp] utilisation des données américaines uniquement. Le service est disponible pour tous les annonceurs à 0,35 CPM pour les impressions diffusées à l’aide de la variable [!DNL LiveRamp] Device Graph (c’est-à-dire, pour les appareils introuvables dans les segments d’audience ciblés).

   1. (Facultatif) Dans le [!DNL Brand Safety and Media Targeting] , appliquez des restrictions de sécurité à la marque pour vos emplacements.

   1. (Facultatif) Dans le [!DNL Tracking] , saisissez des pixels d’événement tiers ou des pixels de conversion pour les publicités de l’emplacement.

      >[!NOTE]
      >
      >([!DNL Roku] emplacements) Fournisseurs de pixels tiers approuvés par [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], et [!DNL Research Now].


1. Cliquez sur **[!UICONTROL Create Placement]**.

1. (Facultatif) Joindre des publicités à l’emplacement :

   1. Cliquez sur **[!UICONTROL Attach an ad]**.

   1. Effectuez l’une des opérations suivantes :
   * Pour créer une publicité, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Create a New Ad].**

      1. Spécifiez les paramètres de publicité pour [annonces audio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [télévision connectée](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [publicités display](/help/dsp/campaign-management/ads/ad-settings-display.md), [annonces mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [annonces natives](/help/dsp/campaign-management/ads/ad-settings-native.md)ou [publicités preroll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md).

      1. Cliquez sur **[!UICONTROL Save & Submit for Review]**.

      1. (Facultatif) Pour chaque publicité supplémentaire que vous souhaitez créer pour l’emplacement, cliquez sur **[!UICONTROL Attach Another Ad]**, puis répétez les étapes 1 à 3.

      1. Si vous ne joignez aucune publicité existante, cliquez sur **[!UICONTROL I'm done for now]**.
   * Pour joindre des publicités existantes dans la campagne :

      1. Cliquez sur **[!UICONTROL Select an Ad]**.
      1. Effectuez l’une des opérations suivantes :
         * Pour ajouter une publicité à la fois :
            1. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select].**
            1. (Facultatif) Pour chaque publicité supplémentaire à joindre, cliquez sur **[!UICONTROL Attach Another Ad]**, puis répétez le processus.
         * Pour ajouter jusqu’à 20 publicités à la fois :
            1. Cochez la case située au-dessus de la liste des publicités.
            1. Cochez la case en regard de chaque publicité à ajouter.
            1. Cliquez sur **[!UICONTROL Attach]**.
            1. En regard du nom de la publicité, cliquez sur **[!UICONTROL Select]**.
      1. (Facultatif) Pour remplacer la période de vol par défaut et la rotation des publicités pour des publicités spécifiques dans l’emplacement :
         1. Cliquez sur **[!UICONTROL Custom Schedule Ads]**.

         1. Effectuez l’une des opérations suivantes :

            * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis spécifiez la date de début et la date de fin.

            * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne publicitaire de la colonne &quot;vol&quot;.

            * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne publicitaire de la colonne &quot;vol&quot;.

            * (Lorsque plusieurs publicités ont le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations sur le vol, puis saisissez le poids relatif de rotation de chaque publicité, sous forme de pourcentage.

               Le poids total doit être égal à 100.
         1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.

         1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.




>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier un emplacement](placement-edit.md)
>* [Modification de la planification des publicités pour un emplacement](placement-edit-ad-schedule.md)
>* [Mettre en pause ou activer un emplacement](placement-pause-activate.md)
>* [Affichage du journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
>* [Raccourcis clavier](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Résolution des problèmes de performances](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vidéo : Création d’un emplacement d’affichage standard](https://video.tv.adobe.com/v/340454)

