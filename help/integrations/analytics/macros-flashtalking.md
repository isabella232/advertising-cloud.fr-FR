---
title: Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Flashtalking] Balises publicitaires
description: Découvrez pourquoi et comment ajouter [!DNL Analytics for Advertising Cloud] des macros à [!DNL Flashtalking] balises publicitaires
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Flashtalking] Balises publicitaires

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Applicable à Advertising Cloud DSP uniquement*

Si vous utilisez des balises de publicité de [!DNL Flashtalking] pour vos annonces Advertising Cloud DSP, ajoutez les paramètres Analytics for Advertising Cloud aux URL de votre page d’entrée. Les paramètres permettent à Advertising Cloud d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Flashtalking] publicités display et vidéo pour les types suivants de [!DNL Analytics for Advertising Cloud] implémentations :

* **Les annonceurs qui utilisent la variable [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Code JavaScript implémenté sur leurs sites web**: Vous devriez voir certaines données de clics publicitaires dans Adobe Analytics à partir des publicités que vous achetez via Advertising Cloud, sans macros supplémentaires. Toutefois, pour capturer les données de clics publicitaires dans des navigateurs qui ne prennent pas en charge les cookies tiers et qui ne sont donc pas capturés par le code JavaScript, ajoutez les macros des sections suivantes à vos [!DNL Flashtalking] balises publicitaires.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque des cookies sont toujours disponibles. Une fois les cookies arrêtés par Advertising Cloud, la mise en oeuvre des macros suivantes est nécessaire.

* **Annonceurs dont les sites web n’utilisent pas la variable [!DNL Analytics for Advertising Cloud] Code JavaScript et s’appuient sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans données d’affichage publicitaire) : Les macros suivantes sont requises pour signaler l’activité des clics sur site provenant des publicités achetées via Advertising Cloud.

## Afficher les balises publicitaires

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[ftqs:[AdobeAMO]]
```

Exemple :  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![Exemple d&#39;un [!DNL Flashtalking] paramètres de balise publicitaire](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Balises de publicité vidéo

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exemple :  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![Exemple d&#39;un [!DNL Flashtalking] paramètres de balise publicitaire](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
