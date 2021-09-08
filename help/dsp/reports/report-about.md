---
title: À propos des rapports personnalisés
description: Découvrez les options de création manuelle de rapports personnalisés ou d’utilisation de modèles de rapports préconfigurés.
feature: Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# À propos des rapports personnalisés

Les rapports personnalisés vous permettent de personnaliser le contenu et la remise des données de votre rapport à l’aide des dimensions de campagne (comme l’annonceur, l’emplacement, les sites ou les zones géographiques) et des mesures qui vous intéressent le plus. Vous pouvez effectuer l’une des opérations suivantes :

* Configurez complètement les rapports de performances de campagne à un niveau granulaire.
* Choisissez parmi des modèles de rapport préconfigurés et personnalisez-les éventuellement davantage.

Vous pouvez générer les rapports une seule fois ou programmer leur génération quotidienne, hebdomadaire ou mensuelle à 03h00 dans le fuseau horaire spécifié. Une fois un rapport généré, une notification est envoyée à chaque destinataire spécifié, avec un lien de téléchargement du fichier.

>[!NOTE]
>
>Vous pouvez également afficher les données à la demande à tous les niveaux d’une campagne (campagne, package, emplacement ou publicité) [dans la vue de gestion de campagne appropriée](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Types de rapports disponibles

* **[!UICONTROL Custom]:** Ce rapport est un modèle vierge que vous pouvez utiliser pour créer votre propre rapport personnalisé à l’aide de la plupart des dimensions et mesures. [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo] et  [!UICONTROL Site] les rapports sont des variantes de ce modèle avec des colonnes et des dimensions présélectionnées pour leurs cas d’utilisation respectifs.

* Modèles de rapport préconfigurés

   * **[!UICONTROL Billing]:** utilisez ce rapport pour comprendre les mesures de facturation clés, telles que les mesures de dépenses pour la facturation des médias par campagne.

      >[!NOTE]
      >
      >Ce rapport contient des données sur le segment de facturation. Si une impression diffusée par un utilisateur ou un appareil appartient à plusieurs segments, un seul segment facturable est crédité de l’impression.

   * **[!UICONTROL Conversion]:** utilisez ce rapport pour comprendre les performances de vos campagnes en fonction des mesures de conversion capturées à l’aide du suivi de conversion Advertising Cloud. Ce rapport comprend l’attribution multipoint.

   * **[!UICONTROL Device]:** utilisez ce modèle prérenseigné pour afficher les mesures clés par dimensions liées à l’appareil.

   * **[!UICONTROL Frequency (by Impression)]:** Utilisez ce rapport pour comprendre la distribution des impressions affichées pour les visionneuses uniques (par exemple, le nombre de visionneuses uniques qui ont vu une impression, deux impressions, trois impressions, etc.). Les données sont disponibles par emplacement ou campagne.

      >[!NOTE]
      >
      >* Les données sont disponibles après le 1er mars 2019.
      >* La fréquence est estimée sur la base d&#39;un échantillonnage de données.
      >* Pour certains inventaires, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi des fréquences. Ce rapport inclut uniquement les impressions pour lesquelles un identifiant d’appareil était disponible.


   * **[!UICONTROL Frequency (by App/Site)]:** Utilisez ce rapport pour déterminer le nombre d’utilisateurs uniques auxquels ont accédé l’application ou le site. Vous pouvez également voir le nombre d’utilisateurs uniques auxquels vous avez accédé par le biais d’une application ou d’un site spécifique (&quot;utilisateurs uniques distincts&quot;).

      >[!NOTE]
      >
      >* Les données sont disponibles après le 15 novembre 2018.
      >* Pour certains inventaires privés, les éditeurs ne transmettent pas d’identifiant d’appareil, ce qui empêche le suivi des fréquences.


   * **[!UICONTROL Geo]**: Utilisez ce modèle prérenseigné pour afficher les mesures clés par dimensions géographiques.

   * **[!UICONTROL Margin]:** Utilisez ce rapport pour afficher les mesures clés telles que les marges, les bénéfices et les autres mesures de dépenses par campagne ou emplacement.

   * **[!UICONTROL Segment]:** utilisez ce modèle prérenseigné pour afficher les mesures clés par segment.

      >[!NOTE]
      >
      >* Ce rapport est destiné à montrer les performances de différents segments ciblés. Elle utilise des données d’adhésion au segment. Lorsqu’une impression est diffusée sur une personne ou un appareil appartenant à deux segments ciblés ou plus, ce rapport comprend une ligne pour chaque segment. Pour cette raison, les totaux de ce rapport peuvent ne pas correspondre à la diffusion réelle.
      >* Les mesures de conversion et les données d’objectif personnalisées pour les segments sont disponibles après le 2 août 2019. Toutes les autres données relatives aux segments sont disponibles à compter du 1er juin 2018.


   * **[!UICONTROL Site]:** par défaut, comprend les mesures standard, le total des dépenses nettes des médias et le total des dépenses nettes facturables par site.

## Rapports inter-comptes {#cross-account-reporting}

Toute organisation disposant de plusieurs comptes DSP peut éventuellement activer des données inter-comptes dans des rapports personnalisés, en fonction des besoins de l’organisation. Par exemple, vous pouvez donner au compte A l’accès aux données du compte B et au compte B l’accès aux données du compte C (mais pas au compte A). Pour activer et configurer cette fonction, contactez votre gestionnaire de compte.

Une fois la fonction activée pour votre organisation, vous pouvez [filtrer](report-settings.md) l’un des types de rapports suivants par compte :  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] et [!UICONTROL Conversion].

Les paramètres de votre compte à l’adresse [!UICONTROL Settings] > [!UICONTROL Account] indiquent a) les autres comptes dont les données sont disponibles pour votre compte et b) les autres comptes qui peuvent accéder aux données de votre compte.

>[!MORELIKETHIS]
>
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Paramètres des rapports personnalisés](/help/dsp/reports/report-settings.md)
>* [À propos des rapports In-Platform](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)

