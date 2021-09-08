---
title: Code JavaScript pour [!DNL Analytics for Advertising Cloud]
description: Code JavaScript pour [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Code JavaScript pour [!DNL Analytics for Advertising Cloud]

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

*Annonceurs avec Advertising Cloud DSP uniquement*

Pour Advertising Cloud DSP, l’intégration [!DNL Analytics for Advertising Cloud] effectue le suivi des interactions de site affichant et affichant les clics publicitaires. Les visites des clics publicitaires sont suivies par le code Adobe Analytics standard sur vos pages web ; le code [!DNL Analytics] capture les paramètres AMO ID et EF ID dans l’URL de la page d’entrée et les suit dans leurs eVars réservées respectives. Vous pouvez effectuer le suivi des visites d’affichage publicitaire en déployant deux lignes de code JavaScript dans vos pages web.

Lors de la première page vue d’une visite sur le site, le code JavaScript Advertising Cloud vérifie si le visiteur a déjà vu ou cliqué sur une publicité. Si l’utilisateur a déjà accédé au site par le biais d’un clic publicitaire ou n’a pas vu de publicité, le visiteur est ignoré. Si le visiteur a vu une publicité et n’est pas entré sur le site par un clic publicitaire au cours de l’[intervalle de recherche en amont des clics](/help/integrations/analytics/prerequisites.md#lookback-a4adc) défini dans Advertising Cloud, le code JavaScript Advertising Cloud utilise le [service d’identification Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html) pour générer un ID supplémentaire (`SDID`), utilisé pour associer les données d’Advertising Cloud à l’accès Adobe Analytics du visiteur. Adobe Analytics interroge ensuite Advertising Cloud pour connaître l’AMO ID et l’EF ID associés à l’exposition publicitaire. Les identifiants AMO ID et EF sont ensuite renseignés dans leurs eVars respectives. Ces valeurs persistent pendant une période donnée (60 jours par défaut).

[!DNL Analytics] envoie toutes les heures des mesures de trafic du site (telles que les pages vues, les visites et la durée de la visite) et tout événement  [!DNL Analytics]  personnalisé ou standard à Advertising Cloud, à l’aide de l’identifiant EF comme clé. Ces [!DNL Analytics] mesures s’exécutent ensuite par le biais du système d’attribution Advertising Cloud pour connecter les conversions à l’historique des clics et des expositions.

>[!NOTE]
>
>La logique de suivi JavaScript Advertising Cloud se produit côté Adobe et n’a donc pratiquement aucun impact sur le temps de chargement de la page.
>
>En revanche, la logique du connecteur de données [!DNL DCM] vers [!DNL Analytics] (à l’aide de [!DNL Google Campaign Manager 360]) pour Advertising Cloud DSP se fait côté client. L’assemblage côté client ralentit le chargement de la page et augmente le risque de perte de données. Cela se produit car le code JavaScript [!DNL Analytics] doit envoyer un ping [!DNL DoubleClick] et attendre que [!DNL DoubleClick] transfère les dernières données de clic/impression vers [!DNL Analytics]. Lorsque votre équipe [!DNL DSP] configure le connecteur de données [!DNL DCM], vous devez indiquer la durée pendant laquelle vous souhaitez retarder la page.

## Déploiement du code JavaScript

La bibliothèque JavaScript se compose de deux lignes qui permettent à [!DNL Analytics] et à Advertising Cloud de communiquer entre eux. Si l’intégration [!DNL Analytics for Advertising Cloud] a été effectuée pendant la mise en oeuvre d’Advertising Cloud, vous avez reçu ce code avec des instructions sur la manière de le déployer.

Si vous ne disposez pas déjà du code, contactez l’équipe d’assistance d’Advertising Cloud.

### Emplacement du code

La fonction JavaScript [!DNL Analytics for Advertising Cloud] doit se trouver après le service d’ID Experience Cloud, mais avant votre code Analytics App Measurement, de sorte que l’ID supplémentaire (`SDID`) puisse être inclus dans votre appel Analytics.

![Emplacement du code](/help/integrations/assets/a4adc-code-placement.png)

### Validation du déploiement du code

Vous pouvez effectuer la validation à l’aide de n’importe quel type d’outil de renifleur de paquets (tel que [!DNL Charles], [!DNL Fiddler] ou [!DNL Chrome Developer Tools]) en comparant les valeurs des quatre identifiants entre la requête envoyée à Advertising Cloud et la requête envoyée à [!DNL Analytics], comme indiqué ci-dessous.

#### Comment confirmer le code avec [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Ouvrez [!DNL Chrome Developer Tools] et cliquez sur l’onglet **Réseau**.
1. Chargez une page de site web qui contient le code JavaScript [!DNL Analytics for Advertising Cloud].
1. Filtrez l’onglet [!UICONTROL Network] par `last` et passez en revue deux lignes :

   ![Filtrage en dernier](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * La première ligne correspond à l’appel à la bibliothèque JavaScript et est intitulée `last-event-tag-latest.min.js`.
   * La deuxième ligne correspond à l’appel envoyant la demande à Advertising Cloud. Il commence comme suit : `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Si vous ne voyez pas l’appel à Advertising Cloud, il se peut qu’il ne s’agisse pas de la première page vue de votre visite. À des fins de test, vous pouvez supprimer le cookie afin que l’appel suivant soit la première page vue de la visite correspondante :

      1. Dans l’onglet Application , recherchez le cookie `adcloud` et vérifiez que le cookie contient `_les_v` (dernière visite) avec une valeur `y` et un horodatage d’époque UTC qui expire dans 30 minutes.
      1. Supprimez le cookie `ad cloud` et actualisez la page.
1. Filtrez sur `/b/ss` pour afficher l’accès Analytics.

   ![Filtrage sur  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. Comparez les valeurs d’identifiant entre les deux accès. Toutes les valeurs seront incluses dans les paramètres de chaîne de requête, à l’exception de l’identifiant de suite de rapports dans l’accès Analytics, qui est le chemin d’accès à l’URL immédiatement après `/b/ss/`.

   | ID | Paramètre Analytics | Paramètre Advertising Cloud |
   |--- |--- |--- |
   | Organisation IMS Experience Cloud | `mcorgid` | `_les_imsOrgid` |
   | ID de données supplémentaire | sdid | `_les_sdid` |
   | Suite de rapports Analytics | La valeur après `/b/ss/` | `_les_rsid` |
   | Identifiant visiteur Experience Cloud | mid | `_les_mid` |

   Si les valeurs d’identifiant correspondent, l’implémentation JavaScript est confirmée. Advertising Cloud enverra au serveur [!DNL Analytics] les détails de suivi des clics publicitaires ou des affichages publicitaires s’ils existent.

#### Comment confirmer le code avec [!DNL Adobe Experience Cloud Debugger]

1. Ouvrez la [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) sur votre page d’accueil.
1. Accédez à l’onglet [!UICONTROL Network] .
1. Dans la barre d’outils [!UICONTROL Solutions Filter], cliquez sur [!UICONTROL Advertising Cloud] et [!UICONTROL Analytics].
1. Dans la ligne de paramètre [!UICONTROL Request URL – Hostname], recherchez `lasteventf-tm.everesttech.net`.
1. Sur la ligne [!UICONTROL Request – Parameters*] , vérifiez les signaux générés, comme à l’étape 3 de &quot;[Comment confirmer le code avec [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * Vérifiez que le paramètre `SDID` correspond à la valeur `Supplemental Data ID` du filtre Adobe Analytics.
   * Si le code n’est pas généré, vérifiez que le cookie Advertising Cloud a été supprimé dans l’onglet [!UICONTROL Application]. Une fois supprimé, actualisez la page et répétez le processus.

   ![Audit du code  [!DNL Analytics for Advertising Cloud] JavaScript dans  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Conditions préalables et informations clés relatives à la mise en oeuvre [!DNL Analytics for Advertising Cloud]](prerequisites.md)

