---
title: Affichage des rapports de diagnostic de placement
description: Découvrez comment diagnostiquer les problèmes de configuration et de fréquence d’emplacement.
feature: DSP Placements
exl-id: d64406b6-83b5-4ae7-984c-98610fc1ee40
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Affichage des rapports de diagnostic de placement

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Les outils suivants peuvent vous aider à diagnostiquer les problèmes de configuration et de fréquence de placement une fois qu’une campagne est active :

* **[!UICONTROL Change Log]:** affiche les modifications apportées aux paramètres d’emplacement clés, tels que le nom, l’état et l’offre maximale. Chaque entrée comprend la date et le nom d’utilisateur de la personne qui a apporté la modification.
* **[!UICONTROL Ad Approvals]:** indique si les fournisseurs de stock ont approuvé ou refusé les publicités. Vous pouvez éventuellement modifier l’état d’une publicité (par exemple, suspendre une publicité rejetée) ou ouvrir les paramètres de la publicité.
* **[!UICONTROL Non Bids]:** Indique pourquoi DSP n’a pas enchéri sur l’emplacement.

1. Ouvrez le rapport Diagnostics :
   1. Ouvrez les paramètres de placement :
      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.
      1. Cliquez sur le nom de la campagne, puis sur **[!UICONTROL Placements]**.
      1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.
   1. Dans le coin supérieur droit, cliquez sur ![Diagnostics de placement](/help/dsp/assets/placement-diagnostics.png) ou **[!UICONTROL Diagnostic]**.
1. Effectuez l’une des opérations suivantes :
   * Pour afficher le journal des modifications :
      1. Cliquez sur **[!UICONTROL Change Log]**.
      1. (Facultatif) Filtrez les résultats du rapport :
         * Dans le menu de dates, remplacez la période du rapport par défaut 14 derniers jours par une autre période (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* ou *[!UICONTROL Last 1 year]*).
         * Dans le menu de gauche, filtrez le rapport selon un nom d’utilisateur spécifique.
         * Dans le menu de droite, filtrez le rapport selon un paramètre d’emplacement spécifique.
   * Pour consulter le statut des validations publicitaires :
      1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Ad Approvals]**.
      1. (Facultatif) Pour suspendre ou activer la publicité, cliquez sur le commutateur d’état (![commutateur d’état](/help/dsp/assets/status-switch.png)) dans la colonne Publicité.
      1. (Facultatif) Pour ouvrir les paramètres d’une publicité, cliquez sur **[!UICONTROL View Ad]** en regard de la publicité.
   * Pour savoir pourquoi DSP n’a pas enchéri sur l’emplacement :
      1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Non Bids]**.
      1. (Facultatif) Pour modifier la période, cliquez dans le champ de date et sélectionnez une autre date ou période.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [À propos des rapports In-Platform](campaign-reports-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

