---
title: Configuration de tests A/B pour les annonces Advertising Cloud DSP dans Adobe Target
description: Découvrez comment configurer un test A/B dans [!DNL Target] pour vos publicités DSP.
source-git-commit: 465f3c18a7d85d54bca5ff2f565694a9b211a7ed
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour les annonces Advertising Cloud DSP

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Annonceurs avec Advertising Cloud DSP uniquement*

Adobe Advertising Cloud DSP et Adobe Target permettent aux marketeurs de proposer plus facilement une expérience personnalisée et connectée à l’aide de médias payants et de messages sur site. En partageant des signaux entre les deux produits, vous pouvez :

* Diminuez les taux de chute du site en liant l’exposition publicitaire des clients DSP campagnes à leurs expériences sur site.

* Créez des tests A/B en mettant en miroir les expériences sur site avec les messages publicitaires à l’aide des données d’exposition Adobe Audience Manager et des audiences Target cliquer pour alimenter.

* Mesurez l’impact de la messagerie unifiée sur un effet élévateur objectif sur site à l’aide de visualisations simples dans Adobe Analytics pour [!DNL Target].

Consultez les sections suivantes pour connaître les conditions préalables et pour obtenir des instructions sur la configuration du suivi des clics publicitaires et des affichages publicitaires, implémenter le partage de signal entre DSP et [!DNL Target] et configurer une activité de test A/B, puis [!DNL Analytics] Analysis Workspace pour afficher les données de test.

Si vous avez d’autres questions, contactez adcloud_support@adobe.com.

## Conditions préalables

Ce cas pratique nécessite les produits et intégrations suivants :

* [!DNL Target]

* [[!DNL Analytics] pour Advertising Cloud](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (requise pour les tests d’affichage publicitaire uniquement)

## Étape 1 : Configuration de la structure de clic publicitaire {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Structure du clic publicitaire](/help/integrations/assets/target-ct-framework.png)

Lorsque vous ajoutez DSP macros à une URL de clic publicitaire (l’URL affichée lorsqu’un utilisateur clique sur une publicité et atteint la page d’entrée), DSP capture automatiquement la clé d’emplacement en incluant ```${TM_PLACEMENT_ID}``` dans l’URL du clic publicitaire. Cette macro capture la clé d’emplacement alphanumérique et non l’identifiant d’emplacement numérique.

![URL de clic publicitaire ajoutée à l’URL de la page d’entrée](/help/integrations/assets/target-ct-url.jpg)

### Ajout DSP macros à vos URL de clic publicitaire

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Dans le cas de Google Campaign Manager 360 ou d’une conversation par Flash, mettez à jour manuellement l’URL du clic publicitaire pour chaque publicité afin d’inclure les macros requises pour capturer les variables AMO ID. Les variables AMO ID sont utilisées pour envoyer des données de clic à Adobe Analytics et pour partager des clés de placement pour les tests A/B. Consultez les pages suivantes pour obtenir des instructions :

* [Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Flashtalking] Balises publicitaires](/help/integrations/analytics/macros-flashtalking.md)

* [Ajouter [!DNL Analytics for Advertising Cloud] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)

Contactez votre équipe de compte DSP et le groupe de solutions Advertising (aac-advertising-solutions-group@adobe.com) pour récupérer la clé d’emplacement requise et finaliser la configuration, et pour vous assurer que chaque URL de clic publicitaire est renseignée avec la clé d’emplacement.

## Étape 2 : Configuration de la structure d’affichage publicitaire à l’aide de l’Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Structure d’affichage publicitaire](/help/integrations/assets/targetr-vt-framework.png)

En ajoutant un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et paramètres d’emplacement, vous pouvez créer un segment de test pour d’autres opportunités de test d’affichage publicitaire.

1. Implémentez un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et DSP paramètres d’emplacement.

   Pour obtenir des instructions, voir[Collecte de données d’exposition multimédia à partir des campagnes Advertising Cloud DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Veillez à ajouter [Macros DSP](/help/dsp/campaign-management/macros.md) pour capturer toutes les données que le pixel d’événement d’impression doit transmettre, y compris `${TM_PLACEMENT_ID_NUM}` pour l’identifiant d’emplacement numérique.

   >[!NOTE]
   >
   >Les URL de suivi des clics incluent la variable `${TM_PLACEMENT_ID}` pour la clé d’emplacement alphanumérique, au lieu de `${TM_PLACEMENT_ID_NUM}` pour l’identifiant d’emplacement numérique.

1. Configurez un segment d’Audience Manager à partir des données d’impression DSP :

   1. Accédez à **Audience Manager** > **Données d’audience** > **Signaux**, puis sélectionnez la variable **Rechercher** dans le coin supérieur gauche.

   1. Saisissez le **Clé** et **Valeur** pour le signal qui détermine à quel niveau les utilisateurs du segment sont regroupés. Utilisez une [clé prise en charge](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) avec une valeur qui correspond à une macro que vous avez ajoutée au pixel d’événement d’impression d’Audience Manager.

      Par exemple, pour regrouper des utilisateurs pour un emplacement spécifique, utilisez la variable `d_placement` clé. Pour la valeur, utilisez un identifiant de placement numérique réel (tel que 2501853 dans la capture d’écran ci-dessus) capturé par la macro DSP. `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Si le champ Nombre total affiche le nombre d’utilisateurs pour la paire clé-valeur, ce qui indique que le pixel a été placé correctement et que les données circulent, vous pouvez passer à l’étape suivante.
   ![Signaux de recherche](/help/integrations/assets/target-am-signals.png)

1. [Création d’une caractéristique basée sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) pour la création de segments dans Audience Manager.

   1. Nommez la caractéristique afin qu’elle soit facilement identifiable dans les activités de test. Stockez la caractéristique dans le dossier de votre choix.

   1. Dans la **Source de données** menu déroulant, sélectionnez **Ad Cloud**.

   1. Dans le Générateur d’expression, ajoutez ```d_event``` dans le champ Clé et ```imp``` dans le **Valeur** champ, sélectionnez **Ajouter une règle**, puis enregistrez la caractéristique.

   ![Capture d’écran d’une caractéristique basée sur des règles](/help/integrations/assets/target-am-trait.png)

1. Configurez un segment de test dans Audience Manager :

   1. Dans la partie supérieure de la page, accédez à **Données d’audience** > **Caractéristiques** et recherchez le nom complet de la caractéristique. Cochez la case en regard du nom de la caractéristique, puis cliquez sur **Créer un segment**.

   1. Nommez le segment, sélectionnez `Ad Cloud` comme la propriété **Source de données**, puis enregistrez le segment.

      L’Audience Manager divise automatiquement le segment en une population témoin qui reçoit l’expérience de page d’entrée standard et un groupe de test qui a reçu une expérience personnalisée sur site.
   ![Capture d’écran d’un segment de test](/help/integrations/assets/target-am-segment.png)

## Étape 3 : Configuration d’une activité de test A/B dans Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

Les instructions suivantes présentent des informations relatives au cas d’utilisation DSP. Pour obtenir des instructions complètes, voir[Création d’un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html.&quot;

1. [Connexion à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. Dans la **Activités** liste, cliquez sur **Création d’une activité** > **Test A/B**.

   ![Création d’une activité de test A/B](/help/integrations/assets/target-create-ab.png)

1. Dans le **Entrée dans l’URL d’activité*** , saisissez l&#39;URL de la landing page pour le test.

   ![Saisir le champ URL d’activité](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Vous pouvez utiliser plusieurs URL pour tester l’entrée du site vue publicitaire. Pour plus d’informations, voir[Activité multi-page](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Vous pouvez facilement identifier les entrées principales par URL de page en créant un [Rapport d’entrée sur le site](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) dans Analytics.

1. Dans le **Objectif** , saisissez la mesure de succès du test.

   >[!NOTE]
   >
   >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target]et que la suite de rapports correcte est sélectionnée.

1. Définissez la variable **Priorité** to `High` ou `999` afin d’éviter les conflits lorsque les utilisateurs du segment de test reçoivent une expérience sur site incorrecte.

1. Within **Paramètres de création de rapports**, sélectionnez la variable **Nom de la société** et **Suite de rapports** connecté à votre compte DSP.

   Pour obtenir des conseils supplémentaires sur la création de rapports, voir &quot;[Bonnes pratiques et dépannage de la création de rapports](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. Dans le **Période** , saisissez les dates de début et de fin appropriées pour le test.

1. Ajoutez des audiences à l’activité :

   1. Choisissez la [segment précédemment créé en Audience Manager pour tester les audiences d’affichage publicitaire](#view-through-framework).

      ![Ajout d’audiences à l’activité](/help/integrations/assets/target-create-ab-audiences.png)

   1. Sélectionner **Pages du site** > **Page d’entrée** > **Requête**, puis saisissez la clé de placement DSP dans le champ **Valeur** pour utiliser les paramètres de chaîne de requête Target pour les audiences de clics publicitaires.

      ![Capture d’écran d’une audience de clics ciblés](/help/integrations/assets/target-click-audience.jpg)

1. Pour le **Méthode d’affectation du trafic**, sélectionnez **Manuel (par défaut)** et fractionner l’50/50 de l’audience.

1. Enregistrez l’activité.

1. Utilisation [!DNL Target] [Compositeur d’expérience visuelle](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) pour apporter des modifications de conception au modèle de landing page de test A/B.

   * Expérience A : Ne modifiez pas ce contenu, car il s’agit de l’expérience de page d’entrée par défaut/contrôle sans personnalisation.

   * Expérience B : Utilisez la variable [!DNL Target] interface utilisateur pour personnaliser le modèle de landing page en fonction des ressources incluses dans le test (titres, copie, positionnement des boutons et éléments créatifs, par exemple).
   >[!NOTE]
   >
   >Par exemple, contactez votre équipe de compte pour des cas d’utilisation de test créatif pour les tests créatifs.

## Étape 4 : Configurez vos [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des [!DNL Target] activités basées sur [!DNL Analytics] mesures de conversion et segments d’audience, puis mesurer les résultats à l’aide de [!DNL Analytics] comme source de création de rapports. Toute la création de rapports et la segmentation pour cette activité est basée sur [!DNL Analytics] collecte de données.

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers les instructions de mise en oeuvre, voir &quot;[Adobe Analytics comme source de création de rapports pour Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurez les [!DNL Analytics for Target] Panneau

Dans Analysis Workspace, configurez la variable [!DNL Analytics for Target panel] pour analyser votre [!DNL Target] activités et expériences. Gardez à l’esprit les recommandations et informations importantes suivantes concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique à la campagne, au package ou à l’emplacement Advertising Cloud pour lequel le test a été exécuté. Utilisez des visualisations récapitulatives pour afficher les mesures Advertising Cloud dans le même rapport que les performances du test Target.

* Définir la priorité de l’utilisation des mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Comprenez que les mesures multimédia agrégées provenant d’Advertising Cloud (telles que les impressions, les clics et les coûts) ne peuvent pas être associées aux mesures Target.

#### Dimensions

Les dimensions suivantes se rapportent à [!DNL Analytics for Target]:

* **Activités Target**: Nom du test A/B

* **Expériences Target**: Noms des expériences de page d’entrée utilisées dans l’activité

* **Activité Target** > **Expérience**: Nom de l’activité et nom de l’expérience dans la même ligne

### Dépannage d’Analytics pour [!DNL Target] Données

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même SDID (Supplemental Data ID) est utilisé pour Target et Analytics. Vous pouvez vérifier les valeurs du SDID à l’aide de la variable [Débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) sur la page d’entrée sur laquelle la campagne entraîne des utilisateurs.

[Valeurs SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page d’entrée, vérifiez que a) le nom d’hôte affiché dans l’Adobe Debugger sous Solutions > Target correspond à b) le serveur de suivi affiché dans la section [!DNL Target] pour l’activité (sous Objectifs et paramètres > Paramètres de création de rapports).

   [!DNL Analytics For Target] nécessite une [!DNL Analytics] serveur de suivi à envoyer dans les appels à partir de [!DNL Target] au [!DNL Modstats] serveur de collecte de données pour Analytics.&lt;!— simplement &quot;vers Analytics ?&quot;>

[Valeur Hostname dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Autres lectures

* [Intégration de Target à Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Explique comment configurer les rapports Target dans Analysis Workspace.
* [Présentation des tests A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Décrit les activités de test A/B que vous pouvez utiliser avec DSP publicités.
* [Offres et expériences](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Expressions [!DNL Target] outils permettant de déterminer le contenu sur site auquel DSP utilisateurs de test sont exposés.
* [Signaux, caractéristiques et segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Définit certains des outils d’Audience Manager qui peuvent vous aider à DSP les tests d’affichage publicitaire.
* [Présentation d’Analytics pour Advertising Cloud](https://experienceleague.adobe.com/docs/advertising-cloud/integrations/analytics/overview.html) - Introduit Analytics for Advertising Cloud, qui vous permet de suivre les interactions de site par clics publicitaires et affichages publicitaires dans vos instances Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->