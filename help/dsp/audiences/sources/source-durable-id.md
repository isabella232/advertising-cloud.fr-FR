---
title: 'Activation des segments authentifiés à partir de partenaires d’ID durables '
description: Découvrez comment activer des audiences authentifiées par le biais d’une solution d’ID durable.
feature: DSP Audiences
source-git-commit: 8550b539676588c3a6bc07abe088b38bd4251725
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Activation des segments authentifiés à partir de partenaires d’ID durables

*Fonction bêta*

Pour activer les audiences authentifiées par le biais d’une solution d’ID durable dans Advertising Cloud DSP, vos segments doivent être traduits en [!DNL RampIDs], qui sont reconnaissables dans un environnement admissible. Pour ce faire, vous pouvez effectuer l’une des opérations suivantes :

* Utilisation de l’intégration DSP avec la [!DNL Adobe Real-Time Customer Data Profile (CDP)] et le [!DNL Adobe-LiveRamp Retrieval API].

* Envoi manuel de segments authentifiés à DSP à partir du [!DNL LiveRamp] [!DNL Connect] tableau de bord.

## Tâches

1. Pour chaque option, contactez `adcloud-support@adobe.com` pour activer les paramètres suivants dans DSP, ce qui vous permettra de cibler les segments authentifiés dans DSP campagnes une seule fois. [toutes les étapes du workflow d’activation sont terminées](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] configuration de campagne avant le partage de segments à partir de [!DNL Real-Time CDP].

   1. Au niveau du compte &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Utilisateurs partageant manuellement des segments authentifiés depuis [!DNL LiveRamp]) Effectuez les étapes suivantes dans la section [!DNL LiveRamp] [!DNL Connect] tableau de bord :

   1. Activation de la mosaïque de destination **[!DNL AAC API 1P Onboarding]**.

   1. Définir [!DNL Identifier Settings] to **[!DNL Ramp ID]** uniquement.

      ![Paramètres d’identifiant](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facultatif) Si vous souhaitez toujours recevoir des identifiants basés sur des cookies, créez une seconde [!DNL AAC API 1P Onboarding] mosaïque de destination avec &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; et &quot;[!DNL AAID]&quot; sélectionné.

## Bonnes pratiques relatives aux tests et à la validation des données

* **Cible [!DNL RampID]segments basés sur des cookies et segments basés sur des cookies dans des campagnes distinctes.**

   * Les paramètres de Campaign ne permettent de prioriser qu’un seul identifiant.

   * Actuellement, [!DNL RampIDs] ne peuvent pas être récupérés pendant les événements sur site. Cela signifie que certains objectifs personnalisés, tels que le CPA le plus bas et le RSDP, ne sont pas disponibles avec l’utilisation de segments authentifiés. Utilisez les segments basés sur des cookies uniquement si vous disposez d’un IPC de performances restrictif.

* **Créez un emplacement dans les deux [!DNL RampID] et des campagnes basées sur des cookies.**

   * Ciblage des segments partagés à partir de [!DNL LiveRamp] en utilisant le processus d’activation du segment standard.

   * Collaborez avec votre équipe d’assistance Advertising Cloud pour valider la distribution correcte des données.

Pour en savoir plus sur l’intégration DSP avec [!DNL LiveRamp], contactez `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>*[À propos de l’activation de segments authentifiés à partir des sources d’audience](source-about.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)

