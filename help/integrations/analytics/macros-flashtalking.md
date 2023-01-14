---
title: Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires
description: Découvrez pourquoi et comment ajouter [!DNL Analytics for Advertising] des macros à [!DNL Flashtalking] balises publicitaires
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: 04b57aec29e2d737bc33375614137543bead240c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

*Applicable aux DSP Advertising uniquement*

Si vous utilisez des balises de publicité de [!DNL Flashtalking] pour vos annonces Advertising DSP, ajoutez les paramètres Analytics for Advertising aux URL de votre page d’entrée. Enregistrement des paramètres `s_kwcid` et `ef_id` paramètres de chaîne de requête dans l’URL de la page d’entrée, ce qui permet à Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Flashtalking] publicités display et vidéo pour les types suivants de [!DNL Analytics for Advertising] implémentations :

* **Les annonceurs qui utilisent la variable [!DNL Adobe] [!DNL Analytics for Advertising] Code JavaScript implémenté sur leurs sites web**: Le code JavaScript enregistre déjà la variable `s_kwcid` et `ef_id` paramètres de chaîne de requête. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le biais du code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque des cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

* **Annonceurs dont les sites web n’utilisent pas la variable [!DNL Analytics for Advertising] Code JavaScript et s’appuient sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans données d’affichage publicitaire) : Les macros suivantes sont requises pour signaler l’activité de clics sur site provenant des publicités que vous achetez via Adobe Advertising.

## Afficher les balises publicitaires

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[ftqs:[AdobeAMO]]
```

Exemple :  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Balises de publicité vidéo

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exemple :  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Adobe des identifiants publicitaires utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)

