---
title: Ad Specifications
description: Reference general and publisher-specific ad specifications.
feature: DSP Ads
source-git-commit: 2110a30cf41a5cc091ec6224a7cbaf9b170ef1db
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Specifications for Supported Ad Types

## Video Ads (Pre-Roll and CTV)

### Supported Screens

Ads are delivered by default on desktop, mobile, and connected TV devices. Device targeting is available to adjust delivery.

### Supported Third-Party Ad Servers

[!DNL DCM][!DNL Flashtalking][!DNL Innovid][!DNL Sizmek] [](certified-ad-servers.md)

### Requirements for High-Definition Video Assets (Required)

**** [](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf)

****

****

****

****

****

****:2:

**** No intra-field motion (blending frames) or interlacing.

****

****

****

****

****

****

#### Additional Publisher Requirements for Connected TV Ads

* ****[](https://advertising.hulu.com/ad-products/video-commercial/)

* ****

   * ESPN Livestreaming:

      ****
      ****
      ****
      ****

   * Full-episode programming (FEP): ESPN, ABC, Freeform, Nat Geo, and FX

      * ****

         ****

         ****

         ****

      * ****

         ****

         ****

         ****

## Display Ads

### Supported Screens

Ads are delivered by default on desktop and mobile devices. Device targeting is available to adjust delivery.

### Supported File Types

****

****

### Requirements for Image Assets (Required)

Universal Display is supported.

****

****[!DNL DCM][!DNL Flashtalking][!DNL Innovid][!DNL Sizmek] [](certified-ad-servers.md)

## Audio Ads

### Supported Screens

Desktop, Mobile, Tablet, Smart Speakers, and Connected TV

### Supported Third-Party Ad Servers

[](certified-ad-servers.md)

### Requirements for Audio Assets (Required)

****

****

****

****

****

#### Additional Publisher Requirements

* **[!DNL Spotify]**
   * Length: Up to 30 seconds
   * File type: OGG
   * Maximum file size: 500MB
   * Volume: RMS normalized to -14; dBFS peak normalized to -0.2 dBFS

* **[!DNL SoundCloud]**
   * Length: 6, 15, or 30 seconds
   * File type: MP3
   * Maximum file size: 5 MB

* **[!DNL Pandora]**
   * Length: 15 or 30 seconds
   * File type: MP4 (in-app), MP3 (desktop)
   * Maximum file size: 2.2 MB

* **[!DNL TuneIn]**
   * Length: 10, 15, or 30 seconds
   * File type: MP3, OGG
   * Volume: 44.1 kHz

* **[!DNL iHeartRadio]**
   * Length: 5, 15, 30 or 60 seconds
   * File type: MP3
   * Maximum file size: 320 kbps
   * Volume: 44.1 kHz

* **[!DNL TargetSpot]**
   * Length: 15, 30 or 60 seconds
   * File type: MP3

### Requirements for Companion Banner Ads (Optional)

****

#### Additional Publisher Requirements

* **[!DNL Spotify]:**
   * File type: Static JPG, PNG
   * Maximum file size: 200 KB
   * Dimensions: 300x250

* **[!DNL SoundCloud]:**
   * File type: Static JPG, PNG
   * Maximum file size: Under 400 KB
   * Dimensions: 1024x1024

* **[!DNL Pandora]:**
   * File type: JPEG, GIF
   * Maximum file size: Size: 100 KB
   * Dimensions: 300x250 (mobile or desktop), or 500x500 (desktop)

* **[!DNL TuneIn]:**
   * File type: JPEG, JPG, PNG, GIF, HTML
   * Maximum file size: 2 MB
   * Dimensions: 300x250

* **[!DNL iHeartRadio]:**
   * File type: JPEG, JPG, PNG, GIF, SWF, HTML
   * Maximum file size: 2.2 MB
   * Dimensions: 300x250
 

## Native Display Ads

Each ad can include either a still image or a moving GIF (cinemagraph).

### Supported Screens

Ads are delivered by default on desktop and mobile devices. Device targeting is available to adjust delivery.

### Required Assets for All Native In-Feed Formats

#### Image Asset

****

****

****

#### Advertiser Logo

****

****

****

>[!NOTE]
>
>Depending on the image over which it will overlayed, choose between light or dark logo assets.

#### Text/Copy

****

****

****

****

>[!NOTE]
>
>The final layout is defined by the publisher at runtime. If an ad exceeds the recommended character count, some inventory providers may not to deliver the ad, or the publisher or SSP may truncate the text.

#### Landing Page URL

The clickthrough URL with optional click trackers.

Requirements for click trackers:

* Third-party impression-tracking pixels: 1x1 image URL format only

* Viewability JavaScript trackers: Supported for IAS only; 1x1 images in JS.append format only

* Third-party click-tracking pixels: Must redirect to the landing page embedded in the URL (HTTP 302 redirect)

* Data management platform (DMP) click trackers with 200 or more responses aren&#39;t supported.

>[!MORELIKETHIS]
>
>* [](ad-about.md)
>* [](ad-create.md)
>* [](ad-create-multiple.md)
>* [](ad-edit.md)

