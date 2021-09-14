---
title: Macros Advertising Cloud DSP
description: Référencez les macros disponibles pour le suivi général et pour effectuer le suivi des clics sur les publicités tierces.
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: e0166dbad4fec41fdc64a65cb3a8ac97496c681f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Macros Advertising Cloud DSP

Une macro est une courte commande ou un raccourci pour une instruction et suit généralement le format `${MACRO_NAME}`. Le serveur de publicités Advertising Cloud DSP exécute les macros lorsque la publicité est diffusée ou fait l’objet d’un clic.

Les macros sont le plus souvent utilisées lors du trafic de métadonnées ou de code créatif tiers et personnalisés (tels que les pixels tiers).

## Macros de suivi générales

Utilisez des macros de suivi générales pour tous les types de balises et d’annonces afin de transmettre des données spécifiques, selon les besoins.

| Macro | Description |
| --------------- | ---------------------- |
| `${USER_ID}` | Identifiant utilisateur pour tous les types d’appareils. |
| `${TM_RANDOM}` | Mise en cache : un nombre aléatoire compris entre 1 et 1000000 |
| `${TM_PLACEMENT_ID_NUM}` | ID d’emplacement |
| `${TM_SITE_URL_URLENC}` | L’URL transmise dans la demande d’offre ; encodé URL |
| `${TM_SITE_DOMAIN_URLENC}` | Le sous-domaine de page analysé à partir de l’URL dans la demande d’offre ; encodé URL |

{style=&quot;table-layout:auto&quot;}

## Macros de clic pour les publicités tierces

Pour effectuer un suivi précis des clics pour les publicités à l’aide de balises d’affichage tierces, DSP nécessite une macro de clic d’affichage. Une seule version de la macro est requise ; la macro appropriée dépend du type de balise.

| Macro | Description |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | URL de redirection qui permet aux serveurs d’annonces de suivre et compter les clics publicitaires dans la plateforme |
| `${TM_CLICK_URL_URLENC}` | URL de redirection qui permet aux serveurs de publicités nécessitant un codage URL de suivre et de comptabiliser les clics publicitaires dans la plateforme |

{style=&quot;table-layout:auto&quot;}

DSP insère automatiquement les macros de clic publicitaire dans une balise d’affichage lorsque vous :

* Exporter des balises publicitaires à partir d’un partenaire de serveur de publicités Advertising Cloud <!-- [Needs PM confirmation.] -->
* Chargement en masse de balises publicitaires [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] directement dans DSP

Si une macro de clic est manquante lors de la création d’une publicité display, DSP affiche un message d’avertissement vous invitant à insérer manuellement la macro de clic d’affichage appropriée dans la zone appropriée de la balise.

>[!MORELIKETHIS]
>
>* [Paramètres de publicité audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Paramètres des publicités télévisées connectées](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Paramètres d’affichage des publicités](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Paramètres des publicités mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Paramètres des publicités natives](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Paramètres de publicité preroll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

