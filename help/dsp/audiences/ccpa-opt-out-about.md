---
title: À propos des [!UICONTROL CCPA Opt-out-of-Sale] segments et des rapports
description: Découvrez comment créer des segments pour effectuer le suivi des identifiants à partir des demandes d’opposition à la vente des informations personnelles (CCPA) et comment récupérer des rapports sur les identifiants.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# À propos des [!UICONTROL CCPA Opt-out-of-Sale] segments et des rapports

Vous pouvez effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la Loi sur la protection des données des consommateurs (CCPA) de Californie, en [créant et en implémentant un segment d’opposition à la vente des informations personnelles du CCPA](ccpa-opt-out-segment-create.md). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

Une fois la balise de pixel de segment implémentée, Advertising Cloud commence à collecter un pool d’identifiants pour le compte de l’annonceur.

## Rapports d’exclusion de la vente aux consommateurs

Advertising Cloud génère des rapports mensuels sur les identifiants que les clients ont envoyés pour les demandes d’exclusion de la vente pour le compte. Les données consolident les demandes capturées à l’aide des segments d’opposition à la vente des CCPA qui ont été créés dans Advertising Cloud DSP et les envois effectués via l’API du Privacy Service.  Les rapports sont générés le premier de chaque mois pour le mois précédent. Par exemple, la liste mensuelle des utilisateurs pour juin est disponible le 1er juillet.

Chaque rapport est disponible sous la forme d’un fichier texte de données séparées par des tabulations compressé au format GZIP. Les identifiants utilisateur capturés dans les segments d’opposition à la vente des informations personnelles (CCPA) sont identifiés par le segment et par l’annonceur.

Vous pouvez [récupérer les liens vers les rapports mensuels](ccpa-opt-out-segment-report-retrieve.md) créés au cours des trois mois précédents, soit depuis Advertising Cloud DSP, soit en utilisant la balise [!DNL Trafficking API] Advertising Cloud. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

>[!MORELIKETHIS]
>
>* [Prise en charge de Adobe Advertising Cloud pour le California Consumer Privacy Act : Prise en charge de l’exclusion des clients](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Création et implémentation d’un  [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Récupération des rapports d’exclusion de la vente pour les consommateurs](ccpa-opt-out-segment-report-retrieve.md)
>* [À propos de la gestion de l’audience](audience-about.md)

