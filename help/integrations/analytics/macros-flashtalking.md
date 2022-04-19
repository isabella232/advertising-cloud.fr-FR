---
title: Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Flashtalking] Balises publicitaires
description: Découvrez pourquoi et comment ajouter [!DNL Analytics for Advertising Cloud] des macros à [!DNL Flashtalking] balises publicitaires
feature: Integration with Adobe Analytics
source-git-commit: c95dc72fa42b47ecea0c27bd59a2df4cd9c20233
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Flashtalking] Balises publicitaires

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Applicable à Advertising Cloud DSP uniquement*

Si vous utilisez des balises de publicité de [!DNL Flashtalking] pour vos annonces Advertising Cloud DSP, ajoutez les paramètres Analytics for Advertising Cloud aux URL de votre page d’entrée. Enregistrement des paramètres `s_kwcid` et `ef_id` paramètres de chaîne de requête dans l’URL de la page d’entrée, ce qui permet à Advertising Cloud d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Flashtalking] publicités display et vidéo pour les types suivants de [!DNL Analytics for Advertising Cloud] implémentations :

* **Les annonceurs qui utilisent la variable [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Code JavaScript implémenté sur leurs sites web**: Le code JavaScript enregistre déjà la variable `s_kwcid` et `ef_id` paramètres de chaîne de requête. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le biais du code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque des cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

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
>* [Advertising Cloud ID utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
