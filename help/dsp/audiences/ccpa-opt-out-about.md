---
title: A propos [!UICONTROL CCPA Opt-out-of-Sale] Segments et rapports
description: Découvrez comment créer des segments pour effectuer le suivi des identifiants à partir des demandes d’opposition à la vente des informations personnelles (CCPA) et comment récupérer des rapports sur les identifiants.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# A propos [!UICONTROL CCPA Opt-out-of-Sale] Segments et rapports

Vous pouvez effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, en vertu de la California Consumer Privacy Act (CCPA), en procédant comme suit : [création et mise en oeuvre d’un segment d’exclusion de la vente des informations personnelles (CCPA)](ccpa-opt-out-segment-create.md). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

## Rapports d’exclusion de la vente aux consommateurs

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients ont envoyés pour les demandes d’exclusion de la vente pour le compte. Les données consolident les demandes capturées à l’aide des segments d’opposition à la vente des informations personnelles (CCPA) qui ont été créés dans DSP et les envois effectués via l’API du Privacy Service.  Les rapports sont générés le premier de chaque mois pour le mois précédent. Par exemple, la liste mensuelle des utilisateurs pour juin est disponible le 1er juillet.

Chaque rapport est disponible sous la forme d’un fichier texte de données séparées par des tabulations compressé au format GZIP. Les identifiants utilisateur capturés dans les segments d’opposition à la vente des informations personnelles (CCPA) sont identifiés par le segment et par l’annonceur.

Vous pouvez [récupérer les liens vers les rapports mensuels ;](ccpa-opt-out-segment-report-retrieve.md) qui ont été créés au cours des trois derniers mois, soit à partir de DSP, soit à l’aide de la DSP [!DNL Trafficking API]. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support pour le California Consumer Privacy Act : Prise en charge de l’exclusion des clients](/help/privacy/ccpa-opt-out-of-sale.md)
>* [Créez et implémentez une [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Récupération des rapports d’exclusion de la vente pour les consommateurs](ccpa-opt-out-segment-report-retrieve.md)
>* [À propos de la gestion de l’audience](audience-about.md)

