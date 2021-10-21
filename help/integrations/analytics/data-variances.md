---
title: Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud
description: Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '3282'
ht-degree: 0%

---

# Écarts de données attendus entre [!DNL Analytics] et Advertising Cloud

*Annonceurs avec intégration Advertising Cloud-Adobe Analytics uniquement*

Les annonceurs qui utilisent la variable [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> l’intégration effectue le suivi de la publicité payante via Advertising Cloud et Adobe Analytics. Lorsque vous effectuez le suivi de médias, de campagnes et de canaux via plusieurs systèmes, les mêmes jeux de données de différents systèmes correspondent rarement entièrement. Ce document explique comment vous devriez vous attendre à ce que les données des médias qui font l’objet d’un trafic via Advertising Cloud soient comparées aux données des différents systèmes dans lesquels les médias sont suivis dans . [!DNL Analytics].

>[!NOTE]
>
>Ce document est axé sur Advertising Cloud et Analytics, mais de nombreux points clés peuvent également être transférés à d’autres solutions de suivi.

## Différences d’attribution dans des rapports similaires

### Fenêtres de recherche en amont et modèles d’attribution potentiellement différents

Le [!DNL Analytics for Advertising Cloud] l’intégration utilise deux variables (eVars ou rVars \[eVars réservées]\) pour capturer la variable [EF ID et AMO ID](ids.md). Ces variables sont configurées avec un seul intervalle de recherche en amont (l’heure à laquelle les clics publicitaires et les affichages publicitaires sont attribués) et un modèle d’attribution. Sauf indication contraire, les variables sont configurées pour correspondre à l’intervalle de recherche en amont des clics par défaut au niveau de l’annonceur et au modèle d’attribution dans Advertising Cloud.

Cependant, les intervalles de recherche en amont et les modèles d’attribution peuvent être configurés dans Analytics (via les eVars) et dans Advertising Cloud. De plus, dans Advertising Cloud, le modèle d’attribution peut être configuré non seulement au niveau de l’annonceur (pour l’optimisation des offres), mais également dans les vues de données et les rapports individuels (à des fins de création de rapports uniquement). Par exemple, une organisation peut préférer utiliser le modèle d’attribution de distribution uniforme pour l’optimisation, mais utiliser l’attribution Dernière touche pour les rapports dans Advertising Cloud DSP ou [!DNL Search]. La modification des modèles d’attribution modifie le nombre de conversions attribuées.

Si un intervalle de recherche en amont des rapports ou un modèle d’attribution est modifié dans un produit et non dans l’autre, les mêmes rapports de chaque système affichent des données distinctes :

* **Exemple d’incohérences dues à des intervalles de recherche en amont différents :**

   Supposons qu’Advertising Cloud dispose d’une période de recherche en amont des clics de 60 jours et que [!DNL Analytics] a une période de recherche arrière de 30 jours. Supposons également qu’un utilisateur se rende sur le site par le biais d’une publicité qui fait l’objet d’un suivi Advertising Cloud, quitte le site, puis revient le 45e jour et effectue une conversion. Advertising Cloud attribuera la conversion à la visite initiale, car la conversion s’est produite dans l’intervalle de recherche en amont de 60 jours. [!DNL Analytics], toutefois, ne peut pas attribuer la conversion à la visite initiale, car la conversion s’est produite après l’expiration de l’intervalle de recherche en amont de 30 jours. Dans cet exemple, Advertising Cloud signale un nombre de conversions plus élevé que [!DNL Analytics] le cas échéant.

   ![Exemple de conversion attribuée dans Advertising Cloud mais pas [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Exemple d’incohérences causées par différents modèles d’attribution :**

   Supposons qu’un utilisateur interagisse avec trois annonces Advertising Cloud différentes avant la conversion, avec les recettes comme type de conversion. Si un rapport Advertising Cloud utilise un modèle de distribution uniforme pour l’attribution, il attribuera les recettes de manière uniforme sur toutes les publicités. If [!DNL Analytics] utilise toutefois le modèle d’attribution Dernière touche , puis il attribuera les recettes à la dernière publicité. Dans l’exemple suivant, Advertising Cloud attribue 10 USD sur les 30 USD des recettes capturées à chacune des trois publicités, alors que [!DNL Analytics] attribue tous les 30 USD de recettes à la dernière publicité affichée par l’utilisateur. Lorsque vous comparez des rapports d’Advertising Cloud et [!DNL Analytics], vous pouvez vous attendre à voir l’impact de la différence dans l’attribution.

   ![Différentes recettes attribuées à Advertising Cloud et [!DNL Analytics] en fonction de différents modèles d’attribution](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La bonne pratique consiste à utiliser les mêmes intervalles de recherche en amont et modèle d’attribution dans Advertising Cloud et [!DNL Analytics]. Travaillez avec votre [!DNL Adobe] le gestionnaire de compte, si nécessaire, pour identifier les paramètres actuels et conserver la synchronisation des configurations.

Ces mêmes concepts s’appliquent à tout autre canal, tel que les canaux qui utilisent des intervalles de recherche en amont différents ou des modèles d’attribution.

#### Différentes fenêtres de recherche en amont pour le suivi des affichages publicitaires {#impression-lookback}

Dans Advertising Cloud, l’attribution est basée sur les clics et les impressions, et vous pouvez configurer différents intervalles de recherche en amont pour les clics et les impressions. Dans [!DNL Analytics], toutefois, l’attribution est basée sur les clics publicitaires et les affichages publicitaires et vous n’avez pas la possibilité de définir différentes fenêtres d’attribution pour les clics publicitaires et les affichages publicitaires ; le suivi de chaque commence à la visite initiale du site. Une impression peut se produire le même jour ou plusieurs jours avant qu’un affichage publicitaire ne se produise, ce qui peut avoir un impact sur l’endroit où la fenêtre d’attribution commence dans chaque système.

En règle générale, la majorité des conversions d’affichages publicitaires se produisent assez rapidement pour que les deux systèmes attribuent du crédit. Cependant, certaines conversions peuvent se produire en dehors de l’intervalle de recherche en amont des impressions Advertising Cloud, mais dans la variable [!DNL Analytics] intervalle de recherche en amont; de telles conversions sont attribuées à l’affichage publicitaire dans [!DNL Analytics] mais pas à l’impression dans Advertising Cloud.

Dans l’exemple suivant, supposons qu’un visiteur ait reçu une publicité le jour 1, qu’il ait effectué une visite d’affichage publicitaire (c’est-à-dire qu’il a visité la page d’entrée de la publicité sans avoir cliqué auparavant sur la publicité) le jour 2 et qu’il ait été converti le jour 45. Dans ce cas, Advertising Cloud effectuerait le suivi de l’utilisateur des jours 1 à 14 (à l’aide d’une recherche en amont de 14 jours), [!DNL Analytics] effectuent le suivi de l’utilisateur à partir des jours 2 à 61 (à l’aide d’une recherche en amont de 60 jours), et la conversion le jour 45 est attribuée à la publicité dans [!DNL Analytics] mais pas dans Advertising Cloud.

![Exemple de conversion d’affichage publicitaire attribuée dans [!DNL Analytics] mais pas Advertising Cloud](/help/integrations/assets/a4adc-viewthrough-example.png)

Une autre cause d’incohérences est que, dans Advertising Cloud, vous pouvez affecter des conversions d’affichage publicitaire à une *poids d’affichage publicitaire* qui est relatif au poids attribué à une conversion basée sur les clics. La pondération d’affichage publicitaire par défaut est de 40 %, ce qui signifie qu’une conversion d’affichage publicitaire est comptabilisée comme 40 % de la valeur d’une conversion basée sur les clics. [!DNL Analytics] ne fournit aucune pondération des conversions d’affichage publicitaire de ce type. Ainsi, par exemple, une commande de recettes de 100 USD capturée dans [!DNL Analytics] sera réduite à 40 USD dans Advertising Cloud si vous utilisez le poids d’affichage publicitaire par défaut, soit une différence de 60 USD.

Tenez compte de ces différences lors de la comparaison des conversions d’affichage publicitaire entre Advertising Cloud et [!DNL Analytics] rapports.

#### Modèles d’attribution disponibles

| Attribution Advertising Cloud | [!DNL Analytics] Attribution | Affectation eVar/rVar |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Ne pas utiliser* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>Pour l’affectation linéaire, [!DNL Analytics] Attribue les événements de succès de manière égale à toutes les valeurs d’eVar au cours d’une seule visite. Par conséquent, utilisez l’attribution linéaire avec une expiration eVar de &quot;Visite&quot;. Toutefois, pour la publicité, l’utilisation de l’attribution linéaire conduit à une attribution qui n’est pas vraiment linéaire et à des rapports moins que idéaux. Par exemple, si un visiteur interagit avec trois publicités avant de procéder à la conversion au cours de trois visites distinctes, seule la publicité vue lors de la dernière visite est attribuée à la conversion, et non aux trois publicités.
>
>En outre, le fait de basculer l’attribution de conversion vers ou depuis &quot;Linéaire&quot; empêche l’affichage des données historiques, ce qui peut entraîner des données erronées dans les rapports. Par exemple, l’affectation linéaire peut diviser les recettes entre plusieurs valeurs d’eVar différentes. Si vous définissez l’attribution sur &quot;Le plus récent&quot;, 100 % de ces recettes sont associées à la valeur unique la plus récente. Cette association peut vous mener à des conclusions incorrectes.
>
>Pour éviter toute confusion, [!DNL Analytics] rend les données historiques indisponibles dans l’interface de création de rapports. Vous pouvez afficher les données historiques si vous redéfinissez le paramètre d’attribution initial de l’eVar, bien que vous ne devriez pas modifier les paramètres d’attribution de l’eVar simplement pour accéder aux données historiques. Adobe recommande d’utiliser un nouvel eVar lorsque vous souhaitez appliquer un nouveau paramètre d’attribution pour les données déjà en cours d’enregistrement, plutôt que de modifier les paramètres d’attribution pour un eVar qui dispose déjà d’une quantité significative de données historiques.

Voir une liste de [!DNL Analytics] les modèles d’attribution et leurs définitions à l’adresse [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Si vous êtes connecté à Advertising Cloud, vous trouverez une liste de modèles d’attribution à l’adresse
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Attribution de date d’événement dans Advertising Cloud

Dans Advertising Cloud, vous pouvez signaler les données de conversion soit par date de clic/événement associé (date de l’événement de clic ou d’impression), soit par date de transaction (date de conversion). Le concept de rapport de date de clic/d’événement n’existe pas dans [!DNL Analytics]; toutes les conversions suivies dans [!DNL Analytics] sont signalés par date de transaction. Par conséquent, une même conversion peut être signalée avec des dates différentes dans Advertising Cloud et [!DNL Analytics]. Prenons l’exemple d’un utilisateur qui clique sur une publicité le 1er janvier et effectue une conversion le 5 janvier. Si vous affichez les données de conversion par date d’événement dans Advertising Cloud, la conversion sera signalée le 1er janvier, lorsque le clic a eu lieu. Dans [!DNL Analytics], la même conversion sera signalée le 5 janvier.

![Exemple de conversion attribuée à des dates différentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution dans [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] reporting](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) vous permet de configurer des règles pour identifier différents canaux marketing en fonction des différents aspects des informations sur les accès. Vous pouvez effectuer le suivi des canaux trackés par Advertising Cloud ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], et [!UICONTROL Paid Search]) as [!DNL Marketing Channels] en utilisant la variable `ef_id` paramètre de chaîne de requête pour identifier le canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Cependant, même si la variable [!DNL Marketing Channels] Les rapports peuvent effectuer le suivi des canaux Advertising Cloud, les données peuvent ne pas correspondre aux rapports Advertising Cloud pour plusieurs raisons. Pour plus d’informations, reportez-vous aux sections suivantes.

>[!NOTE]
>
> Les concepts de base suivants s’appliquent également à tout suivi multicanal qui implique des campagnes non suivies dans Advertising Cloud, comme le [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (également appelée Dimension &quot;Code de suivi&quot; ou &quot;eVar 0&quot;) et suivi personnalisé en eVar.

### Modèles d’attribution potentiellement différents dans [!DNL Marketing Channels]

Le plus [!DNL Marketing Channels] les rapports sont configurés avec [!UICONTROL Last Touch] l’attribution, pour laquelle le dernier canal marketing détecté se voit attribuer 100 % de la valeur de conversion. Utilisation de différents modèles d’attribution pour la variable [!DNL Marketing Channels] les rapports et les rapports Advertising Cloud entraîneront des incohérences dans les conversions attribuées.

### Une fenêtre de recherche en amont potentiellement différente dans [!DNL Marketing Channels]

L’intervalle de recherche en amont pour [!DNL Marketing Channels] peuvent être personnalisés. Dans Advertising Cloud, l’intervalle de recherche en amont des clics est configurable, bien qu’une période de 60 jours fixe soit courante. Si les deux produits utilisent des intervalles de recherche en amont différents, vous pouvez vous attendre à des incohérences de données.

### Différente attribution de canaux dans [!DNL Marketing Channels]

Les rapports Advertising Cloud capturent uniquement les médias payants qui transitent par Advertising Cloud (recherche payante de publicités Advertising Cloud Search et affichage pour les publicités Advertising Cloud DSP), alors que [!DNL Marketing Channels] Les rapports peuvent effectuer le suivi de tous les canaux numériques. Cela peut entraîner une incohérence dans le canal pour lequel une conversion est attribuée.

Par exemple, les canaux de recherche payante et de recherche naturelle ont souvent une relation symbiotique, dans laquelle chaque canal s’aide l’autre. Le [!DNL Marketing Channels] Le rapport attribuera certaines conversions à la recherche naturelle, ce qui n’est pas le cas d’Advertising Cloud, car il ne suit pas la recherche naturelle.

Prenons également le cas d’un client qui consulte une publicité display, clique sur une publicité de recherche payante, clique dans un message électronique, puis passe une commande de 30 USD. Même si Advertising Cloud et [!DNL Marketing Channels] toutes deux utilisent le modèle d’attribution Dernière touche, la conversion sera toujours attribuée différemment à chacune d’elles. Advertising Cloud n’a pas accès au [!UICONTROL Email] , de sorte qu’il créditerait la recherche payante pour la conversion. [!DNL Marketing Channels], cependant, a accès aux trois canaux, de sorte qu’il créditerait [!UICONTROL Email] pour la conversion.

![Exemple d’attribution de conversion différente dans Advertising Cloud ou [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Pour plus d’informations sur les raisons pour lesquelles les mesures peuvent varier, voir &quot;[Pourquoi les données du canal peuvent-elles varier entre Advertising Cloud et [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Différences de données dans Adobe Analytics [!DNL Paid Search Detection]

Le [hérité [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) fonctionnalité dans [!DNL Analytics] permet aux entreprises de [définir des règles pour effectuer le suivi du trafic de recherche payante et organique ;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) pour les moteurs de recherche spécifiés. Le [!DNL Paid Search Detection] les règles utilisent à la fois une chaîne de requête et le domaine référent pour identifier le trafic de recherche payante et naturelle. Le [!DNL Paid Search Detection] les rapports font partie du groupe de [Méthodes de recherche](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) qui expirent lorsqu’un événement spécifié (tel qu’un passage en caisse) se produit ou que la visite se termine.

Voici l’interface permettant de créer une [!DNL Paid Search Detection] ensemble de règles :

![Exemple de règle Détection de recherche payante définie dans [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Le résultat [!DNL Paid Search Detection] Les rapports incluent [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], et [!UICONTROL Natural Search Keywords] rapports.

Notez les deux restrictions suivantes avec les données dans [!DNL Paid Search Detection] rapports :

* Le [!UICONTROL Paid Search Keywords] et [!UICONTROL Natural Search Keywords] Les rapports affichent les requêtes de recherche identifiées par les URL de référence, et non les mots-clés sur lesquels les utilisateurs enchèrent. Advertising Cloud et [!DNL Analytics] Les rapports affichent les mots-clés réels. ne vous attendez donc pas à ce qu’ils s’alignent sur la variable [!DNL Paid Search Detection] rapports sur les mots-clés.

* Lorsque la variable [!DNL Paid Search Detection] a été créée à l’origine, la requête de recherche d’origine (la chaîne de caractères saisie par l’utilisateur dans la barre de recherche du moteur de recherche) était plus facilement accessible aux annonceurs via l’URL de référence. Aujourd’hui, les moteurs de recherche obscurcissent en grande partie la requête et la variable [!DNL Paid Search Detection] les rapports sur les mots-clés ont une valeur limitée, car la plupart des données de requête sont sous &quot;non spécifié&quot;.

   Avec [!DNL Analytics for Advertising Cloud], les publicitaires peuvent toujours effectuer le suivi des mots-clés payants dans [!DNL Analytics]. Le domaine référent informe le moteur de recherche du moteur de recherche qui a généré le trafic. Puisque les informations de compte spécifiques à l’annonceur ne sont pas liées au domaine référent, tout le trafic est répertorié sous le moteur de recherche. Les annonceurs disposant de plusieurs comptes dans le même moteur de recherche doivent se référer à Advertising Cloud ou [!DNL Analytics] création de rapports pour la création de rapports spécifiques au compte.

### Pourquoi configurer [!DNL Paid Search Detection]?

Le [!DNL Paid Search Detection] Les rapports vous permettent d’identifier le trafic de recherche naturelle dans la variable [[!DNL Analytics Marketing Channels] rapports](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html). La séparation du trafic de recherche payante et du trafic de recherche naturelle est un excellent moyen de comprendre la valeur que la recherche naturelle apporte à l’écosystème marketing complet.

## Validation des données de clic publicitaire pour [!DNL Analytics for Advertising Cloud] {#data-validation}

Pour votre intégration, vous devez valider vos données de clics publicitaires afin de vous assurer que toutes les pages de votre site effectuent correctement le suivi des clics publicitaires.

Dans [!DNL Analytics], l’une des méthodes les plus simples de validation [!DNL Analytics for Advertising Cloud] le suivi permet de comparer les clics aux instances à l’aide de la mesure calculée &quot;Clics jusqu’aux instances AMO ID&quot;, calculée comme suit :

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] représente le nombre de fois où les AMO ID (`s_kwcid` ) sont suivis sur le site. Chaque fois qu’un utilisateur clique sur une publicité, une `s_kwcid` est ajouté à l’URL de la landing page. Le nombre de [!UICONTROL AMO ID Instances]est donc analogue au nombre de clics et peut être validé par rapport aux clics publicitaires réels. Nous constatons généralement un taux de correspondance de 80 % pour [!DNL Search] et un taux de correspondance de 30 % pour [!DNL DSP] trafic (lorsqu’il est filtré pour inclure uniquement les clics publicitaires) [!UICONTROL AMO ID Instances]). La différence d’attentes entre la recherche et l’affichage peut s’expliquer par le comportement de trafic attendu. La recherche capture l’intention et, en tant que telle, les utilisateurs ont généralement l’intention de cliquer sur les résultats de la recherche à partir de leur requête. Toutefois, les utilisateurs qui voient un affichage ou une publicité vidéo en ligne sont plus susceptibles de cliquer dessus involontairement, puis de rebondir à partir du site ou de quitter la nouvelle fenêtre qui se charge avant le suivi de l’activité de page.

Dans les rapports Advertising Cloud, vous pouvez comparer de la même manière les clics aux instances à l’aide de la variable[!UICONTROL ef_id_instances]&quot; au lieu de [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Bien que vous vous attendiez à un taux de correspondance élevé entre l’AMO ID et l’EF ID, ne vous attendez pas à une parité de 100 %, car l’AMO ID et l’EF ID suivent fondamentalement différentes données, et cette différence peut entraîner de légères différences dans le total [!UICONTROL AMO ID Instances] et [!UICONTROL EF ID Instances]. Si le total [!UICONTROL AMO ID Instances] in [!DNL Analytics] différer de [!UICONTROL EF ID Instances] Dans Advertising Cloud, en revanche, de plus de 1 %, contactez votre [!DNL Adobe] gestionnaire de compte pour obtenir de l’aide.

Pour plus d’informations sur l’AMO ID et l’EF ID, voir [Advertising Cloud ID utilisés par Analytics](ids.md).

Voici un exemple d’espace de travail permettant d’effectuer le suivi des clics vers des instances.

![Exemple d’espace de travail pour le suivi des clics vers des instances](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Comparaison de jeux de données dans [!DNL Analytics for Advertising Cloud] Contre dans Advertising Cloud

Le [AMO ID](ids.md) (paramètre de chaîne de requête s_kwcid) est utilisé pour la création de rapports dans [!DNL Analytics], et la variable [EF ID](ids.md) est utilisé pour la création de rapports dans Advertising Cloud. Comme il s’agit de valeurs distinctes, il est possible qu’une valeur soit corrompue ou non ajoutée à la page d’entrée.

Par exemple, supposons que nous ayons la page d’entrée suivante :

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

où l’identifiant EF est &quot;`test_ef_id`&quot; et l’AMO ID est &quot;`test_amo_id`.&quot;

Si une redirection côté site se produit, l’URL peut se présenter comme suit :

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

où l’identifiant EF est &quot;`test_ef_id`&quot; et l’AMO ID est &quot;`test_amo_id#redirectAnchorTag`.&quot;

Dans cet exemple, l’ajout de la balise d’ancrage ajoute des caractères inattendus à l’AMO ID, ce qui entraîne la présence d’une valeur qu’Analytics ne reconnaît pas. Cet AMO ID ne serait pas classé et les conversions qui y sont associées tomberaient sous &quot;[!UICONTROL unspecified]&quot; ou &quot;[!UICONTROL none]&quot; dans [!DNL Analytics] rapports.

Heureusement, même si des problèmes comme celui-ci sont communs, ils ne génèrent généralement pas un fort pourcentage d&#39;incohérences. Cependant, si vous constatez une différence importante entre les AMO ID dans [!DNL Analytics] et les identifiants EF dans Advertising Cloud, contactez votre [!DNL Adobe] gestionnaire de compte pour obtenir de l’aide.

## Autres considérations relatives aux mesures

### Différence entre les clics et les visites {#clicks-vs-visits}

Elles semblent similaires, mais les clics et les visites représentent des données différentes :

* **Cliquez sur :** [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une publicité sur le site web d’un éditeur.

* **Visite :** [!DNL Analytics] définit une [visite](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) sous la forme d’une série de pages vues par un utilisateur, se terminant par selon l’un de plusieurs critères, comme 30 minutes d’inactivité.

Par définition, un clic peut conduire à plusieurs visites.

Examinez l’exemple suivant : Les utilisateurs 1 et 2 accèdent tous deux à un site en cliquant sur une publicité Advertising Cloud. L’utilisateur 1 affiche quatre pages, puis quitte le site pour la journée. Le clic initial se traduit donc par une visite. L’utilisateur 2 consulte deux pages, quitte un déjeuner de 45 minutes, revient, affiche deux autres pages, puis quitte le site ; dans ce cas, le clic initial génère deux visites.

![Exemple de différence entre clics et visites](/help/integrations/assets/a4adc-visits-example.png)

### Différence entre les clics et les clics publicitaires

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Les clics et les clics publicitaires sont deux mesures différentes :

* **Cliquez sur :** [!DNL DSP] ou le moteur de recherche enregistre un clic lorsqu’un visiteur clique sur une publicité sur le site web d’un éditeur.

* **Clics publicitaires :** [!DNL Analytics] enregistre un clic publicitaire lorsque le visiteur arrive sur le site web de destination, que la page d’entrée se charge et que la variable [!DNL Analytics] La requête au bas de la page envoie les données à [!DNL Analytics].

Les clics et les clics publicitaires peuvent varier sensiblement en raison de clics publicitaires accidentels. Nous avons constaté que la plupart des clics sur les publicités affichées sont accidentels. Ces visiteurs accidentels ont cliqué sur le bouton Précédent avant le chargement de la page d’entrée. [!DNL Analytics] ne peut pas enregistrer de clic publicitaire. Cela est particulièrement vrai pour les annonces sur lesquelles un clic accidentel est plus probable, comme les annonces mobiles, les publicités vidéo et les publicités qui remplissent l’écran et qui doivent être fermées avant que l’utilisateur puisse afficher la page.

Les sites chargés sur des périphériques mobiles sont également moins susceptibles de générer des clics publicitaires en raison de largeurs de bande plus faibles ou de la puissance de traitement disponible, ce qui entraîne un chargement plus long des landing pages. Il n’est pas rare que 50 à 70 % des clics ne génèrent pas de clics publicitaires. Dans les environnements mobiles, la différence peut atteindre 90 % en raison de la combinaison d’un navigateur plus lent et de la plus grande probabilité que l’utilisateur clique accidentellement sur la publicité lors du défilement de la page ou de la tentative de fermeture de la publicité.

Les données de clic peuvent également être enregistrées dans des environnements qui ne peuvent pas enregistrer les clics publicitaires avec les mécanismes de suivi actuels (tels que les clics vers ou depuis une application mobile) ou pour lesquels l’annonceur a déployé une seule approche de suivi (par exemple, avec l’approche JavaScript d’affichage publicitaire, les navigateurs qui bloquent les cookies tiers effectuent le suivi des clics, mais pas des clics publicitaires). Adobe recommande vivement de déployer les méthodes de suivi des URL de clics et des affichages publicitaires JavaScript pour optimiser la couverture des clics publicitaires pouvant faire l’objet d’un suivi.

### Utilisation des mesures de trafic Advertising Cloud pour les Dimensions non Advertising Cloud

Advertising Cloud fournit à Analytics [mesures de trafic spécifiques aux publicités et dimensions associées provenant de DSP et de la recherche](advertising-cloud-metrics-in-analytics.md). Les mesures fournies par Advertising Cloud s’appliquent uniquement aux dimensions Advertising Cloud spécifiées et les données ne sont pas disponibles pour les autres dimensions dans [!DNL Analytics].

Par exemple, si vous affichez la variable [!UICONTROL AMO Clicks] et [!UICONTROL AMO Cost] mesures par compte, qui est une dimension Advertising Cloud, vous verrez alors le total [!UICONTROL AMO Clicks] et [!UICONTROL AMO Cost] par compte.

![Exemple de mesures Advertising Cloud dans un rapport utilisant une dimension Advertising Cloud](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Toutefois, si vous affichez la variable [!UICONTROL AMO Clicks] et [!UICONTROL AMO Cost] mesures par une dimension sur la page (telle que Page), pour laquelle Advertising Cloud ne fournit pas de données, puis la variable [!UICONTROL AMO Clicks] et [!UICONTROL AMO Cost] pour chaque page sera zéro (0).

![Exemple de mesures Advertising Cloud dans un rapport utilisant une dimension non prise en charge](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Utilisation [!UICONTROL AMO ID Instances] comme substitut des clics avec des Dimensions non Advertising Cloud

Puisque vous ne pouvez pas utiliser [!UICONTROL AMO Clicks] avec les dimensions sur site, vous pouvez rechercher un équivalent aux clics. Vous pouvez être tenté d’utiliser les visites comme substitut, mais elles ne sont pas la meilleure option, car chaque visiteur peut avoir plusieurs visites. (Voir[Différence entre les clics et les visites](#clicks-vs-visits).&quot; Nous vous recommandons plutôt d’utiliser [!UICONTROL AMO ID Instances]: nombre de captures de l’AMO ID. while [!UICONTROL AMO ID Instances] ne correspondra pas [!UICONTROL AMO Clicks] exactement, il s’agit de la meilleure option pour mesurer le trafic de clics sur le site. Pour plus d’informations, voir[Validation des données pour [!DNL Analytics for Advertising Cloud]](#data-validation).&quot;

![Exemple d&#39;un [!UICONTROL AMO ID Instances] au lieu de [!UICONTROL AMO Clicks] pour une dimension non prise en charge](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Mesures Advertising Cloud dans Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Données dans Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Pourquoi les données peuvent varier entre Advertising Cloud et [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

