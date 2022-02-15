---
title: Code JavaScript pour [!DNL Analytics for Advertising Cloud]
description: Code JavaScript pour [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 7bf8f3524954b17d9da336a2210a098bf571399e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Code JavaScript pour [!DNL Analytics for Advertising Cloud]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Annonceurs avec Advertising Cloud DSP uniquement*

Pour Advertising Cloud DSP, la variable [!DNL Analytics for Advertising Cloud] l’intégration effectue le suivi des interactions de site avec les affichages publicitaires et les clics publicitaires. Les visites des clics publicitaires sont suivies par le code Adobe Analytics standard sur vos pages web ; la valeur [!DNL Analytics] Le code capture les paramètres AMO ID et EF ID dans l’URL de la page d’entrée et les suit dans leurs eVars réservées respectives. Vous pouvez effectuer le suivi des visites d’affichage publicitaire en déployant un fragment de code JavaScript dans vos pages web.

Lors de la première page vue d’une visite sur le site, le code JavaScript Advertising Cloud vérifie si le visiteur a déjà vu ou cliqué sur une publicité. Si l’utilisateur a déjà accédé au site par le biais d’un clic publicitaire ou n’a pas vu de publicité, le visiteur est ignoré. Si le visiteur a vu une publicité et n’est pas entré sur le site par le biais d’un clic publicitaire au cours de la [intervalle de recherche en amont des clics](/help/integrations/analytics/prerequisites.md#lookback-a4adc) défini dans Advertising Cloud, le code JavaScript Advertising Cloud (a) utilise la variable [Service d’ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) pour générer un ID supplémentaire (`SDID`) ou b) utilise Adobe Experience Platform [!DNL Web SDK] `generateRandomID` pour générer une `[!DNL StitchID]`. L’un ou l’autre des identifiants est utilisé pour associer les données d’Advertising Cloud à l’accès Adobe Analytics du visiteur. Adobe Analytics interroge ensuite Advertising Cloud pour connaître l’AMO ID et l’EF ID associés à l’exposition publicitaire. Les identifiants AMO ID et EF sont ensuite renseignés dans leurs eVars respectives. Ces valeurs persistent pendant une période donnée (60 jours par défaut).

[!DNL Analytics] envoie des mesures de trafic sur le site (telles que les pages vues, les visites et la durée de la visite), et toute [!DNL Analytics] événements personnalisés ou standard pour Advertising Cloud toutes les heures, à l’aide de l’identifiant EF comme clé. Ces [!DNL Analytics] les mesures sont ensuite exécutées via le système d’attribution Advertising Cloud pour connecter les conversions à l’historique des clics et des expositions.

>[!NOTE]
>
>La logique de suivi JavaScript Advertising Cloud se produit côté Adobe et n’a donc pratiquement aucun impact sur le temps de chargement de la page.
>
>En revanche, la logique de la variable [!DNL DCM] connecteur de données vers [!DNL Analytics] (en utilisant [!DNL Google Campaign Manager 360]) pour Advertising Cloud DSP se produit côté client. L’assemblage côté client ralentit le chargement de la page et augmente le risque de perte de données. Cela se produit car la variable [!DNL Analytics] JavaScript doit effectuer un ping [!DNL DoubleClick] et attendez [!DNL DoubleClick] pour transmettre les dernières données de clic/impression à [!DNL Analytics]. Lorsque la variable [!DNL DSP] l’équipe configure les [!DNL DCM] connecteur de données, vous devez spécifier la durée pendant laquelle vous souhaitez retarder la page.

## Déploiement du code JavaScript

La bibliothèque JavaScript se compose de deux lignes qui permettent [!DNL Analytics] et Advertising Cloud pour communiquer entre eux. Si la variable [!DNL Analytics for Advertising Cloud] l’intégration a été effectuée pendant la mise en oeuvre d’Advertising Cloud. Vous avez alors reçu ce code avec des instructions sur la manière de le déployer.

**(Mises en oeuvre qui utilisent le service Identity Experience Cloud `visitorAPI.js` code)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**(Mises en oeuvre qui utilisent l’Experience Platform [!DNL Web SDK] `alloy.js`code)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Emplacement du code

Le [!DNL Analytics for Advertising Cloud] La fonction JavaScript doit se trouver après le service d’ID Experience Cloud, mais avant votre code Analytics App Measurement, de sorte que l’ID supplémentaire (`SDID`) ou `[!DNL StitchID]` peut être inclus dans votre appel Analytics.

![Emplacement du code](/help/integrations/assets/a4adc-code-placement.png)

### Validation du déploiement du code

Vous pouvez effectuer la validation à l’aide de n’importe quel outil de renifleur de paquets (tel que [!DNL Charles], [!DNL Fiddler]ou [!DNL Chrome Developer Tools]) en comparant les valeurs des quatre identifiants entre la requête envoyée à Advertising Cloud et la requête envoyée à [!DNL Analytics], comme indiqué ci-dessous.

#### Comment confirmer le code avec [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Ouvrir [!DNL Chrome Developer Tools] et cliquez sur le bouton **Réseau** .

1. Charger une page de site web qui contient le [!DNL Analytics for Advertising Cloud] JavaScript.

1. Filtrez les [!UICONTROL Network] par onglet `last` et passez en revue deux lignes :

   ![Filtrage en dernier](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La première ligne correspond à l’appel à la bibliothèque JavaScript et est intitulée `last-event-tag-latest.min.js`.
   * La deuxième ligne correspond à l’appel envoyant la demande à Advertising Cloud. Il commence comme suit : `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Si vous ne voyez pas l’appel à Advertising Cloud, il se peut qu’il ne s’agisse pas de la première page vue de votre visite. À des fins de test, vous pouvez supprimer le cookie afin que l’appel suivant soit la première page vue de la visite correspondante :

      1. Dans l’onglet Application , recherchez la variable `adcloud` et vérifiez que le cookie contient `_les_v` (dernière visite) avec la valeur de `y` et un horodatage d’époque UTC qui expire dans 30 minutes.
      1. Supprimez la variable `ad cloud` et actualisez la page.

1. (Mises en oeuvre qui utilisent le service Identity Experience Cloud `visitorAPI.js` (code) Filtrer sur `/b/ss` pour voir l’accès Analytics.

   ![Filtrage sur `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Mises en oeuvre qui utilisent l’Experience Platform [!DNL Web SDK] `alloy.js`(code) Filtrer sur `/interact` pour vérifier que la charge utile de requête au réseau Edge contient `advertisingStitchID`.

   ![Filtrage sur `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Comparez les valeurs d’identifiant entre les deux accès. Toutes les valeurs seront incluses dans les paramètres de chaîne de requête, à l’exception de l’identifiant de suite de rapports dans l’accès Analytics, qui est le chemin d’accès à l’URL immédiatement après `/b/ss/`.

   | ID | Paramètre Analytics | Edge Network | Paramètre Advertising Cloud |
   | --- | --- | --- | --- |
   | Organisation IMS Experience Cloud | `mcorgid` |  | `_les_imsOrgid` |
   | ID de données supplémentaire | sdid |  | `_les_sdid` |
   | Identifiant d’assemblage | stitchId | `advertisingStitchID` sous le `_adcloud` property |  |
   | Suite de rapports Analytics | La valeur après `/b/ss/` |  | `_les_rsid` |
   | Identifiant visiteur Experience Cloud | mid |  | `_les_mid` |

   Si les valeurs d’identifiant correspondent, l’implémentation JavaScript est confirmée. Advertising Cloud enverra la variable [!DNL Analytics] server les détails du suivi des clics publicitaires ou des affichages publicitaires s’ils existent.

#### Comment confirmer le code avec [!DNL Adobe Experience Cloud Debugger]

1. Ouvrez le [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) sur votre page d’accueil.
1. Accédez au [!UICONTROL Network] .
1. Dans le [!UICONTROL Solutions Filter] barre d’outils, cliquez sur [!UICONTROL Advertising Cloud] et [!UICONTROL Analytics].
1. Dans le [!UICONTROL Request URL – Hostname] ligne de paramètre, localisez `lasteventf-tm.everesttech.net`.
1. Dans le [!UICONTROL Request – Parameters] , vérifiez les signaux générés, comme à l’étape 3 de &quot;[Comment confirmer le code avec [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Mises en oeuvre qui utilisent le service Identity Experience Cloud `visitorAPI.js` (code) Assurez-vous que la variable `Sdid` correspond au paramètre `Supplemental Data ID` dans le filtre Adobe Analytics.
   * (Mises en oeuvre qui utilisent l’Experience Platform [!DNL Web SDK] `alloy.js`(code) Assurez-vous que la valeur de la variable `advertisingStitchID` correspond au paramètre `Sdid` envoyé à l’Experience Platform Edge Network.
   * Si le code n’est pas généré, vérifiez que le cookie Advertising Cloud a été supprimé dans la variable [!UICONTROL Application] . Une fois supprimé, actualisez la page et répétez le processus.

   ![Audit [!DNL Analytics for Advertising Cloud] Code JavaScript dans [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]](prerequisites.md)

