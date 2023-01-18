---
title: Création et implémentation d’un segment d’opt-out de vente du CCPA
description: Découvrez comment créer et mettre en oeuvre un segment pour effectuer le suivi des identifiants d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs.
feature: CCPA, DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Création et implémentation d’un segment d’opt-out de vente du CCPA

Vous pouvez créer un segment pour effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, en vertu du California Consumer Privacy Act (CCPA). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

>[!NOTE]
>
>* Pour plus d’informations sur la manière de communiquer les demandes d’opposition à la vente du CCPA à Adobe Advertising à l’aide de l’API Adobe Experience Platform Privacy Service, voir [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* Pour effectuer le suivi des utilisateurs qui visitent des pages web à des fins non liées au suivi des événements d’opposition à la vente des informations personnelles (CCPA), ainsi que des utilisateurs exposés à des publicités provenant d’ordinateurs de bureau, de périphériques mobiles et de télévisions, créez une [segment personnalisé](/help/dsp/audiences/custom-segment-create.md).


1. Créez le segment :

   1. Dans le menu principal, cliquez sur **Audiences > Segments**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]**.

      Nom de segment recommandé : &quot;&lt;*Nom de votre annonceur*> - Droit d’opposition (opt-out) à la vente (par exemple, &quot;Acme - CCPA - Droit d’opposition à la vente&quot;)

   1. Pour le [!UICONTROL Segment Type], sélectionnez **[!UICONTROL CCPA Opt-out of sale]**.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez une balise pixel pour effectuer le suivi du segment :

   1. Revenir à **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. Sur la ligne de segment, placez le curseur sur le nouveau segment, puis cliquez sur **[!UICONTROL Get pixel]**.

   1. Copiez le pixel de l’image (en commençant par `<img src="https://rtd-tm.everesttech.net"`) pour collecter les identifiants des visiteurs de bureau et mobiles sur une page web.

   1. Fournissez la balise au contact de l’annonceur ou du site web pour le déploiement à l’aide du mécanisme utilisé par l’entreprise pour suivre les demandes d’opposition à la vente des informations personnelles (telles que l’utilisation d’une plateforme de gestion du consentement) de la CCPA.

      Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.

      Une fois le pixel implémenté, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

      Bien que la logique et le choix de l’implémentation dépendent de l’annonceur, voici un exemple de la manière dont un annonceur peut déclencher le pixel :

      1. Un consommateur arrive sur la page d&#39;accueil de l&#39;annonceur.
      1. Le consommateur trouve et clique sur le bouton &quot;Option de désinscription (opt-out) du CCPA&quot; de l’annonceur.
      1. Le consommateur reçoit une liste des prestataires avec lesquels l&#39;annonceur travaille.
      1. Le consommateur coche la case pour refuser de vendre des données à Adobe Advertising.

         Cette action déclenche le déclenchement du pixel et la collecte de l’ID de cookie du consommateur dans le paramètre spécifié[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Support pour le California Consumer Privacy Act : Prise en charge de l’exclusion des clients](/help/privacy/ccpa-opt-out-of-sale.md)
>* [A propos [!UICONTROL CCPA Opt-out-of-Sale] Segments et rapports](ccpa-opt-out-about.md)
>* [Récupération des rapports d’exclusion de la vente pour les consommateurs](ccpa-opt-out-segment-report-retrieve.md)
>* [Création et implémentation d’un segment personnalisé](custom-segment-create.md)
>* [À propos de la gestion de l’audience](audience-about.md)

