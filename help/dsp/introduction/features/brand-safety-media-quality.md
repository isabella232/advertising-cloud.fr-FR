---
title: Sécurité des marques et qualité des médias
description: En savoir plus sur la sécurité de la marque et les fonctionnalités de qualité multimédia.
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 0%

---

# Sécurité des marques et qualité des médias

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP fournit une suite de fonctionnalités de protection de la marque pour s’assurer que chacune de vos campagnes atteint des utilisateurs réels dans un environnement sécurisé.

Notre équipe de surveillance des fraudes travaille en étroite collaboration avec les principaux partenaires de l’industrie, tels que [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)], et [!DNL WhiteOps], pour organiser soigneusement l’inventaire sur notre plateforme. Grâce à une gestion proactive de notre offre, DSP veille à ce que tous les annonceurs de la plate-forme soient protégés du trafic non humain (robots, robots d’indexation, trafic du centre de données et fraude) et à ne diffuser que dans des contextes sécurisés contre la marque.

En plus d’offrir une gestion centralisée de la qualité, nous pensons à donner aux annonceurs les moyens de concevoir les contrôles qui s’alignent sur leur marque. Adobe Advertising Cloud offre des intégrations avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud], et [!DNL Peer39], en veillant à ce que chaque annonceur puisse choisir le niveau de protection anti-fraude souhaité, le filtrage contextuel et le ciblage des mots-clés.

## Initiatives de qualité Advertising Cloud DSP

### Vérification de l’inventaire avec [!DNL Ads.txt] Assistance

[[!DNL Ads.txt], qui signifie [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) est une initiative lancée par la [!DNL Interactive Advertising Bureau] ([!DNL IAB]) en juin 2017 afin de faciliter la représentation adéquate des stocks sur le marché ouvert, et de lutter ainsi contre les sources illégitimes de trafic et d’usurpation de domaine. Les éditeurs et les distributeurs participants déclarent publiquement les entreprises autorisées à vendre leur inventaire numérique et la nature de ces relations, en maintenant une `ads.txt` au niveau supérieur du domaine (par exemple `example.com/ads.txt`).

Prise en charge des DSP [!DNL ads.txt] en lisant les `ads.txt` et vous donner la possibilité d’acheter uniquement auprès d’un [!DNL ads.txt] vendeurs. Par exemple, en faisant correspondre les vendeurs, nous voyons accéder aux `nytimes.com` au New York Times&#39; `ads.txt` , nous pouvons identifier celles qui sont légitimes et celles qui ne le sont pas, et nous bloquerons les contrevenants si l&#39;emplacement est configuré pour n&#39;acheter qu&#39;auprès de vendeurs vérifiés. <!-- can we actually mention NY Times? -->

Vous pouvez définir la valeur par défaut [!DNL ads.txt] contrôles pour chaque annonceur<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement ;](/help/dsp/campaign-management/placements/placement-settings.md) à :

* acheter un stock à partir des vendeurs directs autorisés d’un domaine uniquement ;

* acheter un stock à partir des revendeurs directs et revendeurs autorisés d’un domaine uniquement ;

* donner la priorité à l’achat du stock à partir des revendeurs directs et revendeurs autorisés d’un domaine ;

* acheter un stock à tous les vendeurs ;

### Surveillance des fraudes sur les plateformes

DSP a créé des outils et des systèmes internes performants pour gérer la fraude sur notre plateforme, en partenariat avec des fournisseurs de pointe tels que [!DNL Whiteops] et [!DNL Integral Ad Science].

En outre, Adobe travaille en étroite collaboration avec [!DNL IAB] et [!DNL TAG] pour garantir un blocage robuste et standard des fraudes pour protéger nos annonceurs, en exploitant des outils tels que [!DNL ads.txt] (voir la section précédente), la variable [!DNL IAB] la liste des robots et araignées, ainsi que la liste [!DNL TAG] Liste IP du centre de données.

Grâce à notre approche multidimensionnelle de la qualité, notre équipe surveille les anomalies et les schémas de trafic non valides, en assurant moins de 3 % de trafic non valide sur un inventaire protégé. Tout inventaire suspect, y compris les stocks sur des domaines spécifiques ou provenant d&#39;éditeurs ou de vendeurs spécifiques, est immédiatement bloqué sur l&#39;ensemble de la plateforme.

### Mappage, classement et catégorisation des stocks

Le mapping de l’inventaire est le processus détaillé de révision et d’intégration requis pour tous les nouveaux stocks avant de les ajouter à notre plateforme. Ce processus est conçu pour assurer la sécurité et la qualité de tous les inventaires sur DSP.

* **Mappage :** Notre équipe chargée de l’inventaire examine attentivement chaque domaine en évaluant des aspects tels que :

   * Sécurité des marques

   * Vérification du type d’annonce

   * Contenu générique, domaines en double et service de fausses publicités

* **Mosaïque :** Nous examinons la présence de la marque dans l’écosystème global pour classer l’inventaire selon différents niveaux. Vous pouvez [cibler vos emplacements](/help/dsp/campaign-management/placements/placement-settings.md) à ces niveaux pour le niveau de portée souhaité :

   * **[!UICONTROL T1]** - Nom de la marque, sites reconnaissables à l’échelle internationale

   * **[!UICONTROL T2]** - Sites d’une grande beauté, actualisés, sans contenu généré par l’utilisateur, et généralement peu reconnus au niveau mondial

   * **[!UICONTROL T3]** - Contenu généré par l’utilisateur et contenu de niche

* **Classification de site :** Pour faciliter le ciblage et le blocage du contenu, nous balisons chaque propriété avec une catégorie de site définie par Advertising Cloud en fonction du contenu de la propriété. Vous pouvez [cibler ou exclure ces catégories de site pour chaque emplacement ;](/help/dsp/campaign-management/placements/placement-settings.md) en fonction des objectifs de placement.

### Prise en charge complète du blocage de site

Advertising Cloud DSP fournit à la fois une liste de sites bloqués globalement et la possibilité de créer des listes de sites bloqués personnalisées pour les annonceurs et les comptes.

#### Liste globale des sites bloqués d’Advertising Cloud DSP {#global-blocked-sites}

Advertising Cloud DSP tient à jour une liste des sites bloqués globalement considérés comme dangereux pour l’exécution des publicités. Cette liste contient des sites présentant des contenus répréhensibles (tels que la haine ou la terreur) et des sites infectés par des robots, des faux preroll, des domaines discordants et d&#39;autres activités frauduleuses.

Dans le cadre de notre initiative de sécurité des marques (Brand Safety) visant à éradiquer les activités qui fraudent les publicitaires, tous les sites sont analysés à l’aide des mesures figurant dans la liste des sites bloqués du graphique. Tous les sites qui ne réussissent pas les contrôles de sécurité de la marque sont ajoutés à la liste des sites bloqués globalement. Étant donné qu’Advertising Cloud DSP gère cette liste de manière dynamique, les sites peuvent l’activer ou la désactiver à tout moment, en fonction des dernières analyses de sécurité de la marque.

Lorsque vous incluez un site sur la liste des sites bloqués globalement comme cible d’emplacement, le site est marqué d’un point d’exclamation rouge (!). Cela indique que les publicités ne s’exécuteront pas sur le site marqué.

#### Listes de sites bloqués au niveau du compte et des annonceurs

Les utilisateurs peuvent également gérer des listes de sites bloqués au niveau du compte et de l’annonceur<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, qui sont utilisées automatiquement pour tous les emplacements. La liste des sites bloqués de niveau inférieur est appliquée en plus de la liste des sites bloqués globalement.

## Intégrations tierces

### Filtrage contextuel

Le filtrage contextuel vous permet de cibler ou de bloquer des opportunités publicitaires en fonction du contexte de la page sur laquelle la publicité serait diffusée. Adobe propose un filtrage contextuel via des intégrations avec des fournisseurs de premier plan du secteur : [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39]. Exemples de filtres actuels : [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics], et [!UICONTROL G-rated Sites].

Vous pouvez définir des contrôles de filtre contextuel par défaut pour chaque annonceur.<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement ;](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Blocage des fraudes avant offre

Tirez parti de nos intégrations tierces avec [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39] pour bloquer le trafic non humain de vos campagnes. Ces intégrations fournissent des fonctionnalités de blocage avant enchères leaders du secteur afin de minimiser le trafic général et sophistiqué non valide (GIVT et SIVT) dans vos campagnes.

Vous pouvez définir des contrôles par défaut de blocage des fraudes avant offre pour chaque annonceur.<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement ;](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

Pour plus d’informations sur les fonctionnalités, contactez directement votre fournisseur préféré ou contactez votre [!DNL Adobe] l&#39;équipe du compte.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png) ![Logo Peer39](/help/dsp/assets/peer39-logo.png)

### Visibilité avant offre {#pre-bid-viewability}

Filtres de visibilité avant offre optimisés par nos partenaires de pointe [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]), et [!DNL Integral Ad Science] permettent aux annonceurs de s’assurer que leurs campagnes correspondent aux objectifs de performances de visionnage souhaités dans l’inventaire des vidéos et des affichages.

Vous pouvez définir des filtres de visibilité par défaut pour chaque annonceur.<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [personnaliser les paramètres de chaque emplacement ;](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer lorsque vous utilisez cette fonction.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png) ![Logo Oracle Advertising](/help/dsp/assets/oracle-advertising-logo.png) ![Logo Integral Ad Science](/help/dsp/assets/ias-logo.png)

### Ciblage de rubrique

DSP ciblage de rubrique vous permet de cibler ou de bloquer des listes de mots-clés en exploitant nos partenaires contextuels de pointe [!DNL Comscore] et [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). Le ciblage des rubriques vous permet de vous assurer que vos publicités sont toujours diffusées dans un environnement qui s’aligne sur votre marque, que ce soit en bloquant des contenus nocifs ou en veillant à dépenser dans un contexte qui garantit un meilleur résultat.

Le ciblage des rubriques nécessite de créer des segments de rubrique personnalisés directement avec [!DNL Comscore] ou [!DNL Grapeshot] (en utilisant [!DNL Oracle Data Cloud]). Une fois créés dans la plateforme partenaire, vous pouvez [cibler ou exclure un identifiant de segment dans la variable [!UICONTROL Audience Targeting] section pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité.

Pour créer des segments de rubrique personnalisés :

* Pour créer une [!DNL Comscore] et créer des segments personnalisés, vous pouvez demander une connexion pour [!DNL Activation Segment Manager] at [https://agents.comscore.com](https://agents.comscore.com). Voir [[!DNL Comscore] centre d’aide](https://comscoreactivation.zendesk.com/hc/) pour obtenir des instructions complètes sur la configuration de segments personnalisés. Les frais pour les segments personnalisés sont visibles dans [!DNL Segment Manager] lors de leur création.

* Pour commencer à utiliser [!DNL Oracle Data Cloud], contactez [!DNL Oracle Data Cloud] ou [!DNL Adobe] l&#39;équipe du compte.

![Logo Comscore](/help/dsp/assets/comscore-logo.png) ![Logo du graphique](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP s’est associé à [!DNL DoubleVerify] pour offrir ses [!DNL Authentic Brand Safety] la solution de ciblage, qui vous permet de créer un ensemble centralisé d’exigences de sécurité de la marque à cibler sur toutes vos plateformes d’achat pour des raisons de cohérence.

Une fois que vous avez créé une [!DNL DoubleVerify] segment de sécurité de la marque avec le ciblage nécessaire, vous pouvez l’utiliser dans DSP pour répliquer vos règles de blocage post-enchère avec pré-enchère dans les environnements web.

Vous pouvez définir une [!DNL DoubleVerify] identifiant de segment pour chaque annonceur<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->, puis éventuellement [activer ou désactiver [!UICONTROL Authentic Brand Safety] pour chaque emplacement](/help/dsp/campaign-management/placements/placement-settings.md). DSP facture votre compte pour l’utilisation de l’identifiant de segment.

Pour plus d’informations sur les fonctionnalités, contactez [!DNL DoubleVerify] directement ou contactez votre [!DNL Adobe] l&#39;équipe du compte.

![Logo DoubleVerify](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
