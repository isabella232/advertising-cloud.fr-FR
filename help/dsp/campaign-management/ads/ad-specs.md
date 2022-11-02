---
title: Spécifications des publicités
description: Référencez les spécifications publicitaires générales et spécifiques à l’éditeur.
feature: DSP Ads
exl-id: 905dfd9b-e7a3-4eb6-988f-b49d4b282dd2
source-git-commit: b867ace878a0c1e6391476e267c9161e5ecea921
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---

# Spécifications des types de publicité pris en charge

## Publicités vidéo (preroll et CTV)

### Screens pris en charge

Les publicités sont diffusées par défaut sur les appareils de bureau, mobiles et de télévision connectés. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Serveurs publicitaires tiers pris en charge

Vous pouvez utiliser des feuilles de balises à partir de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service publicitaire](certified-ad-servers.md).&quot;

### Conditions requises pour les ressources vidéo haute définition (requis)

**Type de balise vidéo :** VPAID 2.0 JavaScript ou VAST (CTV). Toutes les unités publicitaires VPAID doivent respecter les conditions suivantes : [Spécification VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) comme défini par l’IAB (Interactive Advertising Bureau).

**Codec vidéo :** MP4/H.264

**Résolution :** 1280x720 pour 720p, 1920x1080 pour 1080p

**Débit :** 1 500 à 2 500 Kbit/s pour 720p, 2 500 à 3 500 Kbit/s pour 1 080p

**H.264 Profil/niveau :** High profile, niveau 3.1 pour 720p; Profil élevé, niveau 4.0 pour 1080p

**Taux d’images vidéo :** 29,970 ips (communément appelé 30 ips) pour les pays NTSC, 25 ips pour les pays PAL, 23,976 ips (communément appelé 24 ips) pour le contenu d’affichage de film

**Espace colorimétrique vidéo :** 4:2:0 sous-échantillonnage YUV Chroma

**Entrelacement vidéo :** Analyse progressive, c’est-à-dire non entrelacée. Pas de mouvement à l’intérieur du champ (cadres de fusion) ni d’entrelacement.

**Leaders (Slate) :** Non autorisé

**Codec audio :** AAC-LC ou HE-AACv1

**Débit audio :** 128-192 Kbit/s pour AAC-LC, 64-128 Kbit/s pour HE-AACv1

**Canal audio :** Mélange stéréo 2 canaux

**Taux d’échantillonnage audio :** 44,1 kHercules ou 48 kHercules, selon le matériau source

**Niveaux audio :** 24 LKFS (+/- 2,0 dB) aux États-Unis selon le ATSC A/85 ; 23 LUFS (+/- 1.0) dans l&#39;UE selon l&#39;EBU R128

#### Exigences supplémentaires de l’éditeur pour les publicités télévisées connectées

* **Réseau A+E :** Voir Réseau A+E [spécifications publicitaires](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Découverte :** Voir Découverte [spécifications publicitaires](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (y compris Hulu) :** Voir Disney&#39;s [spécifications publicitaires](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max :** Voir HBO Max [spécifications publicitaires](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal :**

   * [Vidéo numérique](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Piège](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramètre :** Voir Paramètres [spécifications publicitaires](https://www.paramount.com/digital-ads).

## Publicités affichées

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Types de fichiers pris en charge

**Image :** GIF, JPG/JPEG, PNG

**HTML5 :** Types de fichiers image : GIF, JPG/JPEG, PNG, SVG

### Conditions requises pour les ressources d’image (requis)

Universal Display est pris en charge.

**Tailles d’annonce recommandées :** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Serveurs d’annonces tiers pris en charge :** Vous pouvez utiliser des feuilles de balises à partir de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service publicitaire](certified-ad-servers.md).&quot;

## Publicités audio

### Screens pris en charge

Ordinateur de bureau, mobile, tablette, haut-parleurs intelligents et télévision connectée

### Serveurs publicitaires tiers pris en charge

Vous pouvez utiliser des feuilles de balises à partir de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service publicitaire](certified-ad-servers.md).&quot;

### Conditions requises pour les ressources audio (requis)

**Type de fichier :** MP3, OGG, AAC

**Leaders (ardoise) :**  Non autorisé

**Taille maximale du fichier :** 2 Mo

**Débit :** 128

**Longueur du fichier :** 0 à 60 s

#### Exigences supplémentaires pour les éditeurs

* **[!DNL iHeartRadio]**
   * Longueur : 5, 15, 30 ou 60 secondes
   * Type de fichier : MP3
   * Taille maximale du fichier : 320 Kbit/s
   * Volume : 44,1 kGHz

* **[!DNL Pandora]**
   * Longueur : 15 ou 30 secondes
   * Type de fichier : MP4 (in-app), MP3 (bureau)
   * Taille maximale du fichier : 2,2 Mo

* **[!DNL SoundCloud]**
   * Longueur : 6, 15 ou 30 secondes
   * Type de fichier : MP3
   * Taille maximale du fichier : 5 Mo

* **[!DNL Spotify]**
   * Longueur : Jusqu’à 30 secondes
   * Type de fichier : OGG
   * Taille maximale du fichier : 500 Mo
   * Volume : RMS normalisé à -14; dBFS pic normalisé à -0,2 dBFS

* **[!DNL TargetSpot]**
   * Longueur : 15, 30 ou 60 secondes
   * Type de fichier : MP3

* **[!DNL TuneIn]**
   * Longueur : 10, 15 ou 30 secondes
   * Type de fichier : MP3, OGG
   * Volume : 44,1 kGHz

### Conditions requises pour les bannières publicitaires d’accompagnement (facultatif)

**Tailles prises en charge :** 300x250, 500x500, 640x640, 1024x1024

#### Exigences supplémentaires pour les éditeurs

* **[!DNL iHeartRadio]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, SWF, HTML
   * Taille maximale du fichier : 2,2 Mo
   * Dimensions : 300x250

* **[!DNL Pandora]:**
   * Type de fichier : JPEG, GIF
   * Taille maximale du fichier : Taille : 100 Ko
   * Dimensions : 300x250 (mobile ou bureau) ou 500x500 (bureau)

* **[!DNL SoundCloud]:**
   * Type de fichier : JPG statique, PNG
   * Taille maximale du fichier : Moins de 400 Ko
   * Dimensions : 1 024 x 1 024

* **[!DNL Spotify]:**
   * Type de fichier : JPG statique, PNG
   * Taille maximale du fichier : 200 Ko
   * Dimensions : 300x250

* **[!DNL TuneIn]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, HTML
   * Taille maximale du fichier : 2 Mo
   * Dimensions : 300x250
 

## Publicités d’affichage natives

Chaque publicité peut inclure une image fixe ou un GIF mobile (paragraphe de film).

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Ressources requises pour tous les formats natifs du flux

#### Ressource image

**Résolution :** 600 x 600 pixels au minimum ; minimum recommandé de 1 200 x 627 px

**Type de fichier :** JPEG (image publicitaire ou image de couverture de publicité vidéo), GIF (cinemograph)

**Taille de fichier :** Moins de 1 Mo (l’image ne doit pas contenir de texte.)

#### Logo du annonceur

**Résolution :** 80x80px minimum ; Minimum recommandé 300 x 300 px

**Type de fichier :** JPEG ou PNG.

**Format :**  Rapport 1x1

>[!NOTE]
>
>Selon l’image sur laquelle il sera superposé, choisissez entre les ressources de logo claires ou sombres.

#### Texte/Copie

**Titre :** 200 caractères maximum ; 25 caractères recommandés

**Légende :** 200 caractères maximum ; 100 caractères recommandés

**Sponsorisé par :** 200 caractères maximum ; 30 caractères recommandés

**Appel à l&#39;action (MoPub uniquement) :** 15 caractères maximum

>[!NOTE]
>
>La mise en page finale est définie par l’éditeur au moment de l’exécution. Si une publicité dépasse le nombre de caractères recommandé, certains fournisseurs d’inventaire peuvent ne pas diffuser la publicité, ou l’éditeur ou le fournisseur de services de messagerie peut tronquer le texte.

#### URL de page d’entrée

URL de clic publicitaire avec des outils de suivi de clics facultatifs.

Conditions requises pour les outils de suivi des clics :

* Pixels de suivi d’impression tiers : Format d’URL d’image 1x1 uniquement

* Suivi JavaScript de visibilité : Pris en charge uniquement pour IAS ; Images 1x1 au format JS.append uniquement

* pixels de suivi des clics tiers : Redirection vers la landing page incorporée dans l’URL (redirection HTTP 302)

* Les outils de suivi des clics de la plateforme de gestion des données (DMP) avec 200 réponses ou plus ne sont pas pris en charge.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-multiple.md)
>* [Modifier une publicité](ad-edit.md)

