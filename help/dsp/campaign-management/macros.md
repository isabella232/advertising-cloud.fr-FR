---
title: Macros sur les DSP publicitaires
description: Référencez les macros disponibles pour le suivi général et pour effectuer le suivi des clics sur les publicités tierces.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Macros sur les DSP publicitaires

Une macro est une courte commande ou un raccourci pour une instruction et suit généralement le format `${MACRO_NAME}`. Les macros incluses dans le code créatif ou les URL de clic publicitaire se développent en une chaîne de code plus longue que le serveur d’annonces peut comprendre. Le serveur de publicités DSP exécute les macros lorsque la publicité est diffusée ou fait l’objet d’un clic.

Les macros de serveur d’annonces sont utiles pour transmettre des informations importantes à DSP ou à des serveurs d’annonces tiers. Les macros sont le plus souvent utilisées lors du trafic de métadonnées ou de code créatif tiers et personnalisés (tels que les pixels tiers).

Vous pouvez insérer manuellement une macro n’importe où, par exemple dans une balise VAST, dans n’importe quelle URL ou dans un pixel d’événement DSP ou tiers. Cependant, chaque client DSP et partenaire a un format de balise publicitaire différent et les macros doivent être insérées dans différents emplacements de la balise en conséquence. Chaque fois que vous travaillez avec un nouveau client ou partenaire, demandez-lui de la documentation sur l’emplacement où insérer les macros dans leurs balises publicitaires DSP trafic.

## Macros de suivi générales

Utilisez des macros de suivi générales pour tous les types de balises et d’annonces afin de transmettre des données spécifiques, selon les besoins.

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | ID du compte. | entier |
| `${TM_AD_ID}` | Clé publicitaire (adKey). | string |
| `${TM_AD_ID_NUM}` | Identifiant de publicité. | entier |
| `${TM_ADVERTISER_ID}` | Identifiant de l’annonceur. | entier |
| `${TM_CAMPAIGN_ID}` | Clé de la campagne. | string |
| `${TM_CAMPAIGN_ID_NUM}` | Identifiant de campagne. | entier |
| ` ${TM_CLICK_URL}` | L’URL de redirection, qui permet aux serveurs d’annonces de suivre et de comptabiliser les clics publicitaires. Lorsque la publicité est diffusée, si l’utilisateur clique dessus, la macro est activée et le clic est enregistré et comptabilisé à des fins de création de rapports. | string |
| ` ${TM_CLICK_URL_URLENC}` | URL de redirection codée, qui permet aux serveurs d’annonces de suivre et de comptabiliser les clics publicitaires. Lorsque la publicité est diffusée, si l’utilisateur clique dessus, la macro est activée et le clic est enregistré et comptabilisé à des fins de création de rapports. N’utilisez pas cette macro à moins que vous ne créiez des publicités tierces et que votre fournisseur ne nécessite pas de codage d’URL. | string |
| `${TM_FEED_ID}` | Clé de l’emplacement du média (feedKey). | string |
| `${TM_FEED_ID_NUM}` | L’identifiant de l’emplacement du média. | entier |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Clé de site de l’emplacement. Requis pour [!DNL AppsFlyer] cliquez sur trackers pour les annonces d’installation d’applications mobiles.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | Clé d’emplacement (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | L’ID d’emplacement. | entier |
| `${TM_RANDOM}` | Mise en cache : un nombre aléatoire compris entre 1 et 1000000. | long |
| `${TM_SESSION_ID}` | Identifiant de la session, qui correspond à une récupération unique de la balise publicitaire. | string |
| `${TM_SITE_DOMAIN_URLENC}` | Le sous-domaine de page analysé à partir de l’URL dans la demande d’offre ; Codé URL. Non pris en charge pour les annonces &quot;in-banner&quot; et &quot;click-to-play&quot;. | string |
| ` ${TM_SITE_NAME}` | Nom du site de l’emplacement. | string |
| `${TM_SITE_URL_URLENC}` | L’URL transmise dans la demande d’offre ; Codé URL. Non pris en charge pour les annonces &quot;in-banner&quot; et &quot;click-to-play&quot;. | string |
| `${TM_SITE_ID_NUM}` | Identifiant du site pour l’emplacement. | entier |
| `${TM_TIMESTAMP}` | Horodatage Unix indiquant le nombre de secondes écoulées depuis minuit (00:00 UTC) le 1er janvier 1970. | long |
| ` ${TM_VIDEO_DURATION}` | Durée de la vidéo publicitaire en secondes. | entier |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros spécifiques à Mobile

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) Identifiant de la plateforme, qui correspond au système d’exploitation de l’appareil :<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` lorsque la plateforme n’est pas l’une des options ci-dessus</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Nom du modèle de l’appareil, codé en URL. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Environnement dans lequel la publicité a été diffusée :<ul><li>`a` = application mobile</li><li>`b` = site web mobile</li></ul> | string (`a` ou `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) Identifiant de la plateforme, qui correspond au système d’exploitation de l’appareil :<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` lorsque la plateforme n’est pas l’une des options ci-dessus</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Type d’appareil sur lequel la publicité était visionneuse :<ul><li>`TAB` = tablette</li><li>`PHN` = mobile</li><li>`computer` = ordinateur</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Si l’utilisateur a désactivé le suivi publicitaire :<ul><li>`1` (Indicateur DNT = 1) = l’utilisateur a exercé son droit d’opposition au suivi des publicités</li><li>`0` (Indicateur DNT = 0) = l’utilisateur s’est abonné au suivi des publicités</li></ul> | entier (`0` ou `1`) |
| `${TM_BUNDLE}` | Le [!DNL iOS] ou [!DNL Android] ID de lot de la boutique d’applications. Exemples : com.zynga.wwf2.free ou id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indique si l’enchérisseur détermine que la demande d’offre provient de l’Union européenne et requiert l’application du RGPD :<ul><li>`1` = Le RGPD doit être appliqué</li><li>`0` = Le RGPD ne doit pas être appliqué</li></ul>`gdpr_consent=${GDPR_CONSENT}` est la valeur de consentement transmise par le partenaire fournisseur dans la demande d’offre entrante :<ul><li>Dans la plupart des cas, il s’agit d’une chaîne de consentement encodée en base64url, ou daisybit (par exemple : BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMBkIDIgM0AgOJxAnQA)</li><li>`0` = aucun consentement</li><li>`1` = consentement</li></ul> | daisybit ou integer |

{style=&quot;table-layout:auto&quot;}

## Macros de clic pour les publicités tierces

Pour effectuer un suivi précis des clics pour les publicités à l’aide de balises d’affichage tierces, DSP nécessite une macro de clic d’affichage. Une seule version de la macro est requise ; la macro appropriée dépend du type de balise.

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | URL de redirection qui permet aux serveurs d’annonces de suivre et de comptabiliser les clics publicitaires dans la plateforme. | string |
| `${TM_CLICK_URL_URLENC}` | URL de redirection qui permet aux serveurs de publicités nécessitant un codage URL de suivre et de comptabiliser les clics publicitaires dans la plateforme. | string |

{style=&quot;table-layout:auto&quot;}

DSP insère automatiquement les macros d’affichage des clics dans une balise d’affichage tierce lorsque vous :

* Exportation des balises publicitaires à partir d’un partenaire de serveur de publicités <!-- [Needs PM confirmation.] -->
* Chargement en masse [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] balises publicitaires directement dans DSP

Si une macro de clic est manquante lors de la création d’une publicité display, DSP affiche un message d’avertissement vous invitant à insérer manuellement la macro de clic d’affichage appropriée dans la zone appropriée de la balise.

## Dépannage des erreurs de macro

Lorsque vous ajoutez des macros à votre code, veillez à utiliser la syntaxe exacte de la macro. Lors de la validation des macros, DSP vérifie que la macro correspond exactement à l’une des macros valides.

Des erreurs sont générées si des caractères sont manquants au début ou à la fin du nom de la macro. Par exemple, un message d’erreur s’affiche si :

* Vous oubliez un ou plusieurs caractères au début du nom de la macro, tels que `${`. Si vous n’incluez pas la syntaxe complète, l’entrée n’est pas reconnue comme macro valide.
* La macro ne se termine pas par un jeu de caractères valide, tel que `}`.

>[!MORELIKETHIS]
>
>* [Paramètres de publicité audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Paramètres des publicités télévisées connectées](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Paramètres d’affichage des publicités](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Paramètres des publicités mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Paramètres des publicités natives](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Paramètres de publicité preroll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Paramètres de publicité vidéo universelle](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

