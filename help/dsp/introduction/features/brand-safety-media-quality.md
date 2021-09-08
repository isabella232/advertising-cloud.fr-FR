---
title: Sécurité des marques et qualité des médias
description: En savoir plus sur la sécurité de la marque et les fonctionnalités de qualité multimédia.
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Sécurité des marques et qualité des médias

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP fournit une suite de fonctionnalités de protection de la marque pour s’assurer que chacune de vos campagnes atteint des utilisateurs réels dans un environnement sécurisé.

Notre équipe de surveillance des fraudes travaille en étroite collaboration avec les principaux partenaires du secteur, tels que [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] et [!DNL WhiteOps], afin d’organiser soigneusement l’inventaire sur notre plateforme. Grâce à une gestion proactive de notre offre, DSP veille à ce que tous les annonceurs de la plate-forme soient protégés du trafic non humain (robots, robots d’indexation, trafic du centre de données et fraude) et à ne diffuser que dans des contextes sécurisés contre la marque.

En plus d’offrir une gestion centralisée de la qualité, nous pensons à donner aux annonceurs les moyens de concevoir les contrôles qui s’alignent sur leur marque. Adobe Advertising Cloud propose des intégrations avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] et [!DNL Peer39], afin que chaque annonceur puisse choisir le niveau de protection anti-fraude souhaité, le filtrage contextuel et le ciblage des mots-clés.

## Initiatives de qualité Advertising Cloud DSP

### Vérification de l’inventaire avec prise en charge de [!DNL Ads.txt]

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) est une initiative lancée par  [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en juin 2017 pour faciliter la représentation correcte des stocks sur le marché libre, combattant ainsi les sources illégitimes de trafic et d’usurpation de domaine. Les éditeurs et distributeurs participants déclarent publiquement les entreprises autorisées à vendre leur inventaire numérique et la nature de ces relations, en conservant une page `ads.txt` au niveau supérieur du domaine (par exemple `example.com/ads.txt`).

DSP prend en charge [!DNL ads.txt] en lisant le fichier `ads.txt` de chaque éditeur et en vous donnant la possibilité de n’acheter qu’auprès de vendeurs [!DNL ads.txt] vérifiés. Par exemple, en faisant correspondre les vendeurs auxquels nous accédons `nytimes.com` au fichier `ads.txt` du New York Times, nous pouvons identifier ceux qui sont légitimes et ceux qui ne le sont pas, et nous bloquerons les contrevenants si l&#39;emplacement est configuré pour acheter uniquement auprès de vendeurs vérifiés. <!-- can we actually mention NY Times? -->

Vous pouvez définir des [!DNL ads.txt] contrôles par défaut pour chaque annonceur<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) pour :

* acheter un stock à partir des vendeurs directs autorisés d’un domaine uniquement ;

* acheter un stock à partir des revendeurs directs et revendeurs autorisés d’un domaine uniquement ;

* donner la priorité à l’achat du stock à partir des revendeurs directs et revendeurs autorisés d’un domaine ;

* acheter un stock à tous les vendeurs ;

### Surveillance des fraudes sur les plateformes

DSP a créé des outils et des systèmes internes performants pour gérer la fraude sur notre plateforme, en partenariat avec des fournisseurs de pointe tels que [!DNL Whiteops] et [!DNL Integral Ad Science].

En outre, Adobe travaille en étroite collaboration avec [!DNL IAB] et [!DNL TAG] pour garantir un blocage des fraudes robuste et standard pour protéger nos annonceurs, en exploitant des outils tels que [!DNL ads.txt] (voir la section précédente), la [!DNL IAB] liste Robots et araignées et la [!DNL TAG] liste IP du centre de données.

Grâce à notre approche multidimensionnelle de la qualité, notre équipe surveille les anomalies et les schémas de trafic non valides, en assurant moins de 3 % de trafic non valide sur un inventaire protégé. Tout inventaire suspect, y compris les stocks sur des domaines spécifiques ou provenant d&#39;éditeurs ou de vendeurs spécifiques, est immédiatement bloqué sur l&#39;ensemble de la plateforme.

### Mappage, classement et catégorisation des stocks

Le mapping de l’inventaire est le processus détaillé de révision et d’intégration requis pour tous les nouveaux stocks avant de les ajouter à notre plateforme. Ce processus est conçu pour assurer la sécurité et la qualité de tous les inventaires sur DSP.

* **Mappage :**  notre équipe d’inventaire examine soigneusement chaque domaine, en évaluant des aspects tels que :

   * Sécurité des marques

   * Vérification du type d’annonce

   * Contenu générique, domaines en double et service de fausses publicités

* **Classement :** nous examinons la présence de la marque dans l’écosystème global afin de classer l’inventaire selon différents niveaux. Vous pouvez [cibler vos emplacements](/help/dsp/campaign-management/placements/placement-settings.md) sur ces niveaux pour le niveau de portée souhaité :

   * **[!UICONTROL T1]** - Nom de la marque, sites reconnaissables à l’échelle internationale

   * **[!UICONTROL T2]** - Sites d’une grande beauté, actualisés, sans contenu généré par l’utilisateur, et généralement peu reconnus au niveau mondial

   * **[!UICONTROL T3]** - Contenu généré par l’utilisateur et contenu de niche

* **Classification de site :** pour garantir un ciblage et un blocage faciles du contenu, nous balisons chaque propriété avec une catégorie de site définie par Advertising Cloud en fonction du contenu de la propriété. Vous pouvez [cibler ou exclure ces catégories de site pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md) en fonction des objectifs de placement.

### Prise en charge complète du blocage de site

Advertising Cloud DSP fournit à la fois une liste de sites bloqués globalement et la possibilité de créer des listes de sites bloqués personnalisées pour les annonceurs et les comptes.

#### Liste globale des sites bloqués d’Advertising Cloud DSP

Advertising Cloud DSP tient à jour une liste des sites bloqués globalement considérés comme dangereux pour l’exécution des publicités. Cette liste contient des sites présentant des contenus répréhensibles (tels que la haine ou la terreur) et des sites infectés par des robots, des faux preroll, des domaines discordants et d&#39;autres activités frauduleuses.

Dans le cadre de notre initiative de sécurité des marques (Brand Safety) visant à éradiquer les activités qui fraudent les publicitaires, tous les sites sont analysés à l’aide des mesures figurant dans la liste des sites bloqués du graphique. Tous les sites qui ne réussissent pas les contrôles de sécurité de la marque sont ajoutés à la liste des sites bloqués globalement. Étant donné qu’Advertising Cloud DSP gère cette liste de manière dynamique, les sites peuvent l’activer ou la désactiver à tout moment, en fonction des dernières analyses de sécurité de la marque.

Lorsque vous incluez un site sur la liste des sites bloqués globalement comme cible d’emplacement, le site est marqué d’un point d’exclamation rouge (!). Cela indique que les publicités ne s’exécuteront pas sur le site marqué.

#### Listes de sites bloqués au niveau du compte et des annonceurs

Les utilisateurs peuvent également gérer des listes de sites bloqués au niveau du compte et de l’annonceur<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, qui sont utilisées automatiquement pour tous les emplacements. La liste des sites bloqués de niveau inférieur est appliquée en plus de la liste des sites bloqués globalement.

## Intégrations tierces

### Filtrage contextuel

Le filtrage contextuel vous permet de cibler ou de bloquer des opportunités publicitaires en fonction du contexte de la page sur laquelle la publicité serait diffusée. Adobe propose un filtrage contextuel via des intégrations avec des fournisseurs de premier plan du secteur : [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] et [!UICONTROL G-rated Sites] sont des exemples de filtres actuels.

Vous pouvez définir des contrôles de filtre contextuel par défaut pour chaque annonceur<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo ](/help/dsp/assets/comscore-logo.png) ![ComscoreDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![Logo](/help/dsp/assets/ias-logo.png) ![Logo Integral Ad SciencePeer39](/help/dsp/assets/peer39-logo.png)

### Blocage des fraudes avant offre

Tirez parti de nos intégrations tierces avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] pour bloquer le trafic non humain de vos campagnes. Ces intégrations fournissent des fonctionnalités de blocage avant enchères leaders du secteur afin de minimiser le trafic général et sophistiqué non valide (GIVT et SIVT) dans vos campagnes.

Vous pouvez définir des contrôles par défaut de blocage de fraude avant offre pour chaque annonceur<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

Pour plus d’informations sur les fonctionnalités, contactez directement votre fournisseur préféré ou contactez votre gestionnaire de compte d’Adobe.

![Logo ](/help/dsp/assets/comscore-logo.png) ![ComscoreDoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![Logo](/help/dsp/assets/ias-logo.png) ![Logo Integral Ad SciencePeer39](/help/dsp/assets/peer39-logo.png)

### Visibilité avant offre {#pre-bid-viewability}

Les filtres de visibilité avant offre optimisés par nos partenaires de pointe [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) et [!DNL Integral Ad Science] permettent aux annonceurs de s’assurer que leurs campagnes correspondent aux objectifs de performances de visionnage souhaités pour l’ensemble de l’inventaire vidéo et d’affichage.

Vous pouvez définir des filtres de visibilité par défaut pour chaque annonceur<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo ](/help/dsp/assets/doubleverify-logo.png) ![DoubleVerify](/help/dsp/assets/oracle-advertising-logo.png) ![Logo Oracle AdvertisingLogo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Ciblage de rubrique

DSP ciblage de rubrique vous permet de cibler ou de bloquer des listes de mots-clés en exploitant nos partenaires contextuels de pointe [!DNL Comscore] et [!DNL Oracle Data Cloud] ([!DNL Grapeshot]).

Le ciblage des rubriques vous permet de vous assurer que vos publicités sont toujours diffusées dans un environnement qui s’aligne sur votre marque, que ce soit en bloquant des contenus nocifs ou en veillant à dépenser dans un contexte qui garantit un meilleur résultat.

Le ciblage des rubriques nécessite de créer des segments de rubrique directement avec [!DNL Comscore] ou [!DNL Grapeshot] (à l’aide de [!DNL Oracle Data Cloud]). Une fois créés dans la plateforme du partenaire, vous pouvez [cibler ou exclure un identifiant de segment dans la section[!UICONTROL  Audience Targeting] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité.

Pour commencer, contactez votre fournisseur préféré ou votre gestionnaire de compte d’Adobe.

![Logo Comscore ](/help/dsp/assets/comscore-logo.png) ![logoGrapeshot](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP s’est associé à [!DNL DoubleVerify] pour proposer sa solution de ciblage [!DNL Authentic Brand Safety], qui vous permet de créer un ensemble centralisé d’exigences de sécurité de marque à cibler sur toutes vos plateformes d’achat pour des raisons de cohérence.

Une fois que vous avez créé un segment de sécurité de marque [!DNL DoubleVerify] avec le ciblage nécessaire, vous pouvez l’utiliser dans DSP pour répliquer vos règles de blocage post-enchère avec pré-enchère dans les environnements web.

Vous pouvez spécifier un [!DNL DoubleVerify] identifiant de segment pour chaque annonceur<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [activer ou désactiver [!UICONTROL Authentic Brand Safety] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). DSP facture votre compte pour l’utilisation de l’identifiant de segment.

Pour plus d’informations sur les fonctionnalités, contactez directement [!DNL DoubleVerify] ou votre gestionnaire de compte d’Adobe.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
