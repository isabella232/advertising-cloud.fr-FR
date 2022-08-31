---
title: Paramètres d’emplacement
description: Voir la description des paramètres d’emplacement disponibles.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: 04586c87f134deaa9a28f57d6f7587f023fd217a
workflow-type: tm+mt
source-wordcount: '3304'
ht-degree: 0%

---

# Paramètres d’emplacement

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Nom de l’emplacement.

>[!TIP]
>Utilisez une convention d’affectation des noms adaptée à votre situation. Une convention d’affectation des noms suggérée est &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** État de l’emplacement : *[!UICONTROL Active]* (valeur par défaut) ou *[!UICONTROL Paused]*.

>[!TIP]
>La bonne pratique consiste à suspendre l’emplacement jusqu’à ce que vous soyez prêt à le lancer.

**[!UICONTROL Details]:** (Lecture seule) Le type de publicité applicable, le compte qui crée ou crée l’emplacement et la campagne parente. Pour afficher plus de détails, cliquez sur **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Ouvre une liste de modèles d’emplacement existants. Pour renseigner automatiquement les paramètres de ciblage à partir d’un modèle :

1. Effectuez l’une des opérations suivantes :

   * Pour réutiliser toute la cible depuis un modèle, cochez la case en regard du nom du modèle.

   * Pour réutiliser des types de cible individuels à partir d’un modèle, développez le nom du modèle et cochez la case en regard des types de cible que vous souhaitez réutiliser.

1. Cliquez sur **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Formats des publicités vidéo uniquement) Durée de la publicité et/ou spécifications de la publicité, qui sont utilisées pour calculer la projection des prévisions sur la droite. Les champs varient en fonction du type de publicité.

**[!UICONTROL Placement tags]:** (Facultatif) Mots-clés ou surnoms pour vous aider à localiser cet emplacement.

## Objectifs

**[!UICONTROL Package]:** (Facultatif) Un package auquel l’emplacement est affecté. Cliquez sur ![Modifier](/help/dsp/assets/edit.png) pour sélectionner un package existant ou créer un nouveau package. Lorsque vous affectez l’emplacement à un module, la variable [!UICONTROL Goals] mise à jour de la section avec les dates de vol, l’objectif de diffusion et le budget du kit.

**[!UICONTROL Flight Dates]:** Date de début et date de fin de l’emplacement. Les publicités approuvées peuvent être exécutées pendant le vol lorsque l’emplacement est principal et affecté à un principal package ou campagne.

Les dates du kit (le cas échéant) ou de la campagne sont renseignées automatiquement par défaut.

>[!NOTE]
>
>* Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération et dans les dates de vol du kit.


### Emplacements affectés aux modules avec un suivi au niveau du module

**[!UICONTROL Placement Funding]:** Comment budgéter l’emplacement :

* *[!UICONTROL Optimize based on performance]:* Contrôle le budget au niveau du package.
* *[!UICONTROL Set a fixed budget cap]:* Permet de définir un budget d’emplacement quotidien, hebdomadaire, mensuel ou à tout moment. Saisissez une valeur et la durée (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** Le maximum pour payer 1 000 impressions.

**[!UICONTROL Placement Pre-bid Filters]:** Jusqu’à cinq seuils d’indicateurs clés de performance (tels qu’une mesure de visibilité minimale ou un taux de clics) qui doivent être atteints pour que la soumission se produise. Vous pouvez utiliser des filtres avant offre comme tactiques d’optimisation, mais vous devez comprendre que chaque règle peut limiter les opportunités sur lesquelles cet emplacement peut enchérir. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtrage.
1. Cliquez sur **[!UICONTROL Save]**.

Consultez les descriptions de chaque filtre de pré-offre à l’adresse &quot;[Filtres de pré-offre au niveau de l’emplacement et comment les utiliser](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Tous les autres emplacements

**[!UICONTROL Budget Goal]:** Le budget plafond brut et l’intervalle de budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Placements dans les opérations avec gestion des marges uniquement) Le plafond budgétaire brut et l&#39;intervalle de budget (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  Objectif d’optimisation du module. Consultez les descriptions de chaque objectif d’optimisation à l’adresse &quot;[Objectifs d’optimisation et utilisation](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Objectif cible, utilisé pour effectuer le suivi des performances.

>[!NOTE]
>
>Ce champ n’est qu’une référence et n’est pas utilisé pour la prise de décision.

**[!UICONTROL Pace on]:** Sur quoi sera fondé le rythme :

* **[!UICONTROL Budget goal]:** (Par défaut) Cette option permet d’envoyer autant d’impressions que possible dans le budget alloué.

* **[!UICONTROL Impressions]:** Cette option permet de délivrer des impressions jusqu’à ce qu’une quantité spécifiée soit atteinte au cours d’un intervalle spécifié. Lorsque vous sélectionnez cette option, indiquez le nombre d’impressions et l’intervalle : *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* ou *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Le maximum pour payer 1 000 impressions.

**[!UICONTROL Pacing Fill Strategy]:** (Modules avec une fréquence au niveau du module uniquement) Comment accélérer la diffusion des publicités :

* *[!UICONTROL Even]:* (Par défaut) Effectue un espacement uniforme de la diffusion à chaque vol, avec une cible de 50 % de la diffusion dans la première moitié du vol.

* *[!UICONTROL Frontload]:* Accélère la diffusion de sorte qu’elle soit de 65 à 75 % complète à mi-chemin du vol.

* *[!UICONTROL Aggressive Frontload]:* Accélère la diffusion de sorte qu’elle soit complète à 75 à 85 % à mi-chemin du vol.

**[!UICONTROL Placement Pre-bid Filters]:** (Facultatif) Jusqu’à cinq filtres doivent être remplis pour que l’offre puisse avoir lieu. Vous pouvez utiliser des filtres avant offre comme tactiques d’optimisation, mais gardez à l’esprit que chaque règle peut limiter les opportunités sur lesquelles cet emplacement peut enchérir. Pour ajouter ou modifier des filtres :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour ajouter un filtre :
      1. Cliquez sur **[!UICONTROL Add Filter]**.
      1. En regard de **[!UICONTROL Only bid if]**, sélectionnez une mesure, puis saisissez une valeur.
   * Pour supprimer un filtre, cliquez sur **[!UICONTROL X]** dans la ligne de filtrage.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Facultatif) Emplacements spécifiques dans lesquels inclure ou exclure des publicités à l’emplacement. Si vous ne spécifiez aucun emplacement, tous les emplacements sont ciblés.

>[!NOTE]
>
>Les emplacements de ville et de zone desservie ne sont pas disponibles pour les emplacements Roku.

Pour spécifier des emplacements :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour inclure ou exclure un pays, un État, une ville, une zone desservie, un district législatif fédéral ou un district législatif d’État :
      1. Sélectionnez le type d’emplacement dans la colonne de gauche.
      1. (Si nécessaire) Cliquez sur un emplacement pour le développer.
      1. En regard de l’emplacement, cliquez sur *[!UICONTROL Include]* pour l’inclure en tant que cible ou *[!UICONTROL Exclude]* pour l’exclure en tant que cible.
   * Pour rechercher un code postal et inclure ou exclure tous les résultats sélectionnés :
      1. Cliquez sur **[!UICONTROL Search Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez le nom de la ville, puis cliquez sur ![Modifier](/help/dsp/assets/search.png).
      1. Cliquez sur le résultat de recherche approprié.
      1. Cliquez sur *[!UICONTROL Include All]* inclure tous les emplacements comme cibles ou *[!UICONTROL Exclude All]* pour exclure tous les emplacements en tant que cibles.
   * Pour saisir ou coller des codes postaux et les inclure ou les exclure tous :
      1. Cliquez sur **[!UICONTROL Paste Postal Code]**.
      1. Sélectionnez le pays.
      1. Saisissez ou collez jusqu’à 1 000 codes postaux.
Insérez un code postal par ligne ou saisissez plusieurs valeurs séparées par des virgules ou des onglets.
      1. Cliquez sur *[!UICONTROL Include All]* inclure tous les emplacements comme cibles ou *[!UICONTROL Exclude All]* pour exclure tous les emplacements en tant que cibles.
   * Pour supprimer un emplacement du [!UICONTROL Included] ou [!UICONTROL Excluded] liste, cliquez sur **[!UICONTROL X]** en regard de l’emplacement dans la colonne de droite.
1. Cliquez sur **[!UICONTROL Done]**.

>[!NOTE]
>
>* Tous les pays ne disposent pas d’emplacements de code postal ou d’État.
>* La zone de marché désignée, les districts législatifs fédéraux et les districts législatifs de l’État ne sont disponibles que pour les États-Unis.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Sources d’inventaire à inclure ou à exclure en tant que cibles. Pour la plupart des types d’emplacements, tous les types d’inventaire et toutes les sources pour chaque type sont inclus par défaut. Pour [!DNL Roku] emplacements, vous devez spécifier le type d’inventaire et les sources. Vous pouvez choisir parmi les types de stock suivants :

* [!UICONTROL Public]: (Tous les types d’emplacements, à l’exception de Roku) Tous les stocks d’échange ouverts auxquels Advertising Cloud a accès. Vous pouvez inclure et exclure l’inventaire public.

   Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer une recherche par nom de flux, clé de flux ou balise de caractéristique sélectionnée.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Vos offres privées existantes (ou celles existantes [!DNL Roku] offres [!DNL Roku] emplacements) avec les éditeurs que vous avez configurés dans DSP. Vous pouvez inclure, mais pas exclure, l’inventaire public.

   Vous pouvez rechercher la liste par mot-clé, clé, identifiant de transaction ou balise personnalisée.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Tous [premium, non garanti [!UICONTROL On Demand] stock](/help/dsp/inventory/on-demand-inventory-about.md) (ou [!UICONTROL On Demand] [!DNL] Offres Roku pour [!DNL Roku] emplacements) auxquels vous vous êtes abonné [!DNL DSP]. Vous pouvez inclure et exclure [!UICONTROL On Demand] inventaire.

   Vous pouvez afficher la liste par source ou par flux. Lorsque vous affichez la liste par flux, vous pouvez effectuer des recherches par nom de flux, clé de flux ou par région d’éditeur, balise de catégorie ou balise de caractéristique sélectionnée.

Pour définir le ciblage des stocks :

* Pour exclure un type de stock, décochez la case en regard de son nom.
* Pour cibler un type de stock :
   1. Cochez la case en regard du nom du type de stock.
   1. (Facultatif) Modifiez les sources pour inclure :
      1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] et [!UICONTROL On Demand] inventory) Click *[!UICONTROL *View by Source]** ou **[!UICONTROL View by Feed]** pour modifier la manière dont les sources sont répertoriées.
      1. (Le cas échéant) Filtrez l’inventaire selon vos besoins.
      1. Indiquez les sources à inclure et à exclure :
         * Pour inclure un [!UICONTROL Public] ou [!UICONTROL On Demand] source, cliquez sur **[!UICONTROL Include]** en regard du nom de la source.
         * À inclure [!UICONTROL Private] sources :
            * Pour inclure tout le stock dans une transaction, cliquez sur **[!UICONTROL Include all]** en regard du nom de l’opération.
            * Pour inclure une source de stock individuelle, développez le nom de l’opération, puis cochez la case en regard du nom de la source.
         * Pour exclure une [!UICONTROL Public] ou [!UICONTROL On ] source, cliquez sur **[!UICONTROL Exclude]** en regard du nom de la source.
   1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage à l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Save & Export]**.
   1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>Si vous vous êtes abonné à [!UICONTROL On Demand] mais ne parvient pas à localiser les éditeurs ou les offres à cibler, puis à vérifier l’état des offres. Pour plus d’informations sur les états, voir [A propos [!DNL On Demand] Inventaire Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Emplacements de vidéos uniquement) Exclut le trafic sortant.

Les publicités sortantes apparaissent généralement au-dessus du contenu sous la forme d’une fenêtre contextuelle ou d’un contenu (dans l’expérience native), plutôt que sous la forme de publicités vidéo standard dans un lecteur vidéo.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Types de trafic à cibler. Les options incluent **[!UICONTROL Websites]** et **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponible lorsque **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) La qualité des sites à cibler. Les niveaux 1 à 3 sont tous sécurisés pour la marque et ont été testés et approuvés par l’équipe de mappage DSP.

* *[!UICONTROL Tier 1]:* Sites et applications haut de gamme reconnaissables au plan national.
* *[!UICONTROL Tier 2]:* Cible le niveau 1, ainsi que les sites et applications de qualité moins connus que le niveau 1.
* *[!UICONTROL Tier 3]:* Cible les niveaux 1 à 2, ainsi que les sites et applications légitimes et sécurisés pour la marque qui répondent à un public de niche. Utilisez le niveau 3 pour la portée ou les achats de ciblage de données.
* *[!UICONTROL All Sites]:* Cible les niveaux 1 à 3 et le nouvel inventaire qui n’a pas été analysé ni classé, que vous pouvez utiliser pour sa portée.

>[!NOTE]
>
>L’inventaire est spécifique aux unités publicitaires de l’emplacement.

>[!TIP]
>
>Pour les campagnes de performances, la bonne pratique consiste à sélectionner *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Facultatif) disponible lorsque **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Catégories de site au sein des niveaux de site sélectionnés pour inclure ou exclure (mais pas les deux) en tant que cibles. Effectuez un choix parmi les listes de sites verticales que Advertising Cloud a mises en correspondance en fonction de l’objet du site :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les catégories de site à inclure ou à exclure :
   * Pour inclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Include categories]**.
      1. Cochez la case en regard de chaque catégorie à cibler.
   * Pour exclure des catégories de site :
      1. Cliquez sur **[!UICONTROL Exclude categories]**.
      1. Cochez la case en regard de chaque catégorie à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage à l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Facultatif) disponible lorsque **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Sites à exclure. Vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Pour rechercher un site :
      1. Cliquez sur **[!UICONTROL Search]**.
      1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
      1. Dans les résultats de recherche, sélectionnez les sites à exclure :
         * Pour exclure un site individuel, cochez la case en regard de celui-ci.
         * (Lorsque plus de 50 résultats sont disponibles) Pour exclure les 50 premiers résultats, cliquez sur **[!UICONTROL Exclude these 50]**. Pour exclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Exclude these \<*NN *\>]**.
   * Pour saisir les noms de domaine :
      1. Cliquez sur **[!UICONTROL Paste]**.
      1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
      1. Cliquez sur **[!UICONTROL Exclude All]**.
1. Cliquez sur **[!UICONTROL Done]** quand tu as fini.

>[!NOTE]
>
>* Des listes de sites bloqués au niveau du compte et de l’annonceur sont également appliquées, en plus d’Advertising Cloud DSP [liste de sites bloqués globalement](/help/dsp/introduction/features/brand-safety-media-quality.md), qui inclut les sites considérés comme dangereux pour les publicités.
>* Les listes de sites bloqués remplacent toujours les listes de sites ciblés. Si un emplacement exclut et inclut la même cible pour une publicité, la cible est exclue.


**[!UICONTROL Language]:** (Facultatif) Une seule langue à cibler.

**[!UICONTROL Site List Preview]:** (Lecture seule) Tous les sites ciblés et bloqués pour l’emplacement.

Vous pouvez éventuellement exporter la liste des sites ciblés et bloqués sous la forme d’un fichier CSV (valeurs séparées par des virgules). Pour exporter la liste, cliquez sur **[!UICONTROL Export full site list]**, puis ouvrez ou enregistrez le fichier selon la procédure normale de votre navigateur.

**[!UICONTROL Allow unscreened sites]:** (Emplacements d’affichage standard uniquement) Active la diffusion publicitaire sur des sites non contrôlés. Lorsque l’emplacement cible l’inventaire privé, cette option peut diffuser des publicités sur les sites bloqués.

**[!UICONTROL Paste list of targeted sites]:** Permet de cibler des sites spécifiques uniquement. Lorsque vous activez cette option, les autres options de ciblage de site sont désactivées.

**[!UICONTROL Sites]:** (Disponible lorsque **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*) Sites à cibler. Vous pouvez rechercher et sélectionner des sites, ou saisir ou coller des noms de domaine :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les sites :
   * Pour rechercher un site :
      1. Cliquez sur **[!UICONTROL Search]**.
      1. Saisissez un mot-clé, sélectionnez un niveau de site et/ou sélectionnez une catégorie de site.
      1. Dans les résultats de recherche, sélectionnez les sites à inclure :
         * Pour exclure un site individuel, cochez la case en regard de celui-ci.
         * (Lorsque plus de 50 résultats sont disponibles) Pour inclure les 50 premiers résultats, cliquez sur **[!UICONTROL Include these 50]**. Pour inclure tous les résultats de la recherche, cliquez sur **[!UICONTROL Include these \<*NN *\>]**.
   * Pour saisir les noms de domaine :
      1. click **[!UICONTROL Paste]**.
      1. Entrez un ou plusieurs noms de domaine sur des lignes distinctes.
      1. Cliquez sur **[!UICONTROL Include All]**.
1. Cliquez sur **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Toute cible d’audience pour l’emplacement, y compris [segments tiers, segments propriétaires, segments d’Adobe, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et principale de l’audience dédupliquée pour tous les segments sélectionnés et les audiences enregistrées s’affiche également. Vous pouvez sélectionner une audience existante, créer une audience que vous pourrez réutiliser ultérieurement ou sélectionner des segments d’audience spécifiques :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez l’audience.
* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Included Audiences], puis sélectionnez **[!UICONTROL + Create Audience]**. Pour obtenir des instructions, voir [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.
* Pour sélectionner des segments d’audience spécifiques, cliquez sur **[!UICONTROL Select segments for this placement only]**. Sélectionnez la logique du segment ; pour obtenir des instructions, reportez-vous à l’étape 6 de &quot;[Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md).&quot; Lorsque vous avez terminé, cliquez sur **Enregistrer**.

**[!UICONTROL Excluded Audiences]:** Toutes les audiences à exclure pour l’emplacement, y compris les audiences avec [segments tiers, segments propriétaires, segments d’Adobe, segments personnalisés et audiences enregistrées](/help/dsp/audiences/audience-settings.md). La taille totale et principale de l’audience dédupliquée pour toutes les audiences exclues s’affiche également. Vous pouvez sélectionner une audience existante ou créer une nouvelle audience que vous pourrez réutiliser ultérieurement :

* Pour sélectionner une audience existante, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez l’audience.
* Pour créer une audience, cliquez sur ![Sélectionner](/help/dsp/assets/chevron-down.png) en regard de [!UICONTROL Excluded Audiences], puis sélectionnez **+ Créer une audience**. Pour obtenir des instructions, voir [Création d’une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md), en commençant par l’étape 3.

**[!UICONTROL Cross Device Targeting]:** (Disponible lorsque vous sélectionnez au moins un segment ou une audience et que la variable [campaign est configuré pour le ciblage multi-appareils basé sur les personnes](/help/dsp/campaign-management/campaigns/campaign-settings.md). Permet d’étendre le ciblage sur tous les appareils connus d’une personne (selon la représentation graphique des appareils spécifiée dans les paramètres de la campagne), même sur les appareils qui ne figurent pas dans les segments spécifiés. Les frais peuvent s&#39;appliquer en fonction du graphique spécifié pour l&#39;opération. Actuellement, les données de Device Graph ne sont disponibles qu’en Amérique du Nord.

**[!UICONTROL Placement Cap]:** (Facultatif) Le nombre de fois où un appareil ou une personne unique (en fonction de la variable [!UICONTROL Cross Device Level] pour la campagne) seront diffusées des publicités à partir de l’emplacement. Les options incluent *[!UICONTROL Unlimited]* ou un montant spécifique par jour, semaine ou mois.

>[!NOTE]
>
> Vous pouvez définir des limites de fréquence aux niveaux de la campagne, du kit et de l’emplacement. DSP respectera le plafond de fréquence le plus strict de la hiérarchie de l&#39;opération.

**[!UICONTROL Secondary Cap]:** (Facultatif) disponible lorsque vous incluez une valeur numérique [!UICONTROL Placement Cap]) Une limitation supplémentaire dans les limites de la limite de placement Principale. Sélectionnez le nombre d’impressions et la période (3 par 12 heures, par exemple).

**[!UICONTROL Day Parting]:** (Facultatif) Jours spécifiques de la semaine et heure d’exécution des publicités. Pour définir des intervalles de créneaux horaires :
1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Sélectionnez le fuseau horaire applicable.
1. Spécifiez les intervalles :
   * Pour sélectionner un intervalle prédéfini, cliquez sur l’un des boutons de l’intervalle. Les options incluent *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* ou *[!UICONTROL Prime]* (primetime).
   * Pour sélectionner manuellement un intervalle, cliquez à l’intérieur d’une cellule, puis faites-le glisser pour sélectionner l’intervalle.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Facultatif) disponible pour les annonceurs configurés avec [!DNL Comscore] et [!DNL Grapeshot] segments) Noms ou identifiants de segments spécifiques provenant de [!DNL Comscore] et [!DNL Grapeshot] à inclure en tant que cibles. Des frais supplémentaires peuvent s’appliquer pour cette fonctionnalité. Pour activer cette fonction et configurer des segments de rubrique, contactez votre [!DNL Adobe] l&#39;équipe du compte.

Pour spécifier le ciblage de rubrique :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les segments à cibler :
   1. Dans la colonne de gauche, sélectionnez le partenaire (*[!UICONTROL Comscore]* ou *[!UICONTROL Grapeshot]*).
   1. Dans le champ de saisie, saisissez les noms ou les identifiants de segment.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de rubrique vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

>[!TIP]
>
>* Le ciblage de rubrique limite l’inventaire sur lequel l’emplacement peut enchérir. Par conséquent, utilisez le ciblage de rubrique pour seulement un faible pourcentage de votre achat global.
>
>* Configurez tout ciblage négatif dans le segment sur [!DNL Comscore] ou [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Facultatif) Des informations spécifiques sur les appareils, notamment les types d’appareils, les fabricants, les systèmes d’exploitation, les navigateurs et les types de connectivité, à inclure et exclure en tant que cibles. Pour spécifier le ciblage des périphériques :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les détails de l’appareil à inclure et à exclure :
   1. Dans la colonne de gauche, sélectionnez la catégorie.
   1. Spécifiez le ciblage :
      * Pour inclure une valeur, cliquez sur **[!UICONTROL Include]** en regard du nom de la valeur.
      * Pour exclure une valeur, cliquez sur **[!UICONTROL Exclude]** en regard du nom de la valeur.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage du périphérique à l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Facultatif) Des fournisseurs d’accès à Internet spécifiques (FAI) à inclure ou à exclure (mais pas les deux) comme cibles. Pour spécifier le ciblage des FAI :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Spécifiez les FAI à inclure ou à exclure :
   * Pour inclure des FAI :
      1. Cliquez sur **[!UICONTROL Include ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à cibler.
   * Pour exclure les FAI :
      1. Cliquez sur **[!UICONTROL Exclude ISPs]**.
      1. (Facultatif) Filtrez la liste par mot-clé.
      1. Cochez la case en regard de chaque FAI à exclure.
1. (Facultatif) Pour télécharger un fichier CSV contenant les informations de ciblage du FAI vers l’emplacement de téléchargement de votre navigateur, cliquez sur **[!UICONTROL Export]**.
1. Cliquez sur **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Types de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39] filtres contextuels à appliquer. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour de nouveaux emplacements, mais vous pouvez modifier les paramètres :

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types de contexte d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39]:

   * **Ciblez les sites qui :** (Facultatif) Un ou plusieurs types d’attributs d’inventaire à cibler par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL ComScore]:

   * **Bloquer les sites qui sont :** (Facultatif) Un ou plusieurs types d’attributs d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Facultatif) Degré de contenu adulte pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Alcohol Content]:** (Facultatif) Le degré de contenu d’alcool pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (valeur par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Pre-bid fraud blocking]:** Types de sites à bloquer en fonction du trafic frauduleux et des activités suspectes mesurées par [!DNL DoubleVerify], [!DNL Integral Ad Science], et [!DNL Peer39]. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour de nouveaux emplacements, mais vous pouvez modifier les paramètres :

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Par défaut, bloque tout le trafic non valide à 100 %, y compris le trafic sur les appareils mis en jonction, pour les nouveaux emplacements. Des frais supplémentaires peuvent s’appliquer.

   * **[!UICONTROL Also block sites with]:** (Facultatif) Un niveau supplémentaire de fraude et de trafic non valide qui entraînera DSP bloquer les publicités par défaut :  *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas le trafic supplémentaire), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Facultatif) Un ou plusieurs types de fraude qui entraîneront DSP bloquer les publicités par défaut : *[!UICONTROL Fraud]* (qui bloque tous les sites escroqués), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*, et/ou *[!UICONTROL Fraud: Zero Ads]*. Des frais supplémentaires peuvent s’appliquer.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Facultatif) Un type d’activité suspecte sur un site web ou une application qui DSP par défaut bloquer les publicités : *[!UICONTROL None]* (la valeur par défaut, qui ne bloque pas les publicités basées sur des activités suspectes), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Ads.txt filtering]:**

Quel niveau de [Ads.txt](https://iabtechlab.com/ads-txt-about/) le filtrage pré-enchère à utiliser en utilisant la liste des vendeurs numériques autorisés de chaque éditeur. La valeur par défaut au niveau de l’annonceur est sélectionnée pour les nouveaux emplacements, mais vous pouvez modifier les paramètres :

* *[!UICONTROL Opt out of ads.txt (default)]*: Pour acheter des stocks à tous les vendeurs.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Pour donner la priorité à l’achat du stock auprès des revendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]*: Acheter un inventaire uniquement auprès des revendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]*: Pour acheter des stocks uniquement auprès des vendeurs directs autorisés d’un domaine.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Les annonceurs configurés avec la variable [!UICONTROL DoubleVerify Authentic Brand Safety] Option) Active [!DNL DoubleVerify Authentic Brand Safety], qui bloque les impressions après l’offre à l’aide des règles de sécurité de marque personnalisées configurées pour l’identifiant de segment spécifié. DSP facture votre compte pour l’utilisation de l’identifiant de segment spécifié dans les paramètres de l’annonceur.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] emplacements) Fournisseurs tiers de suivi approuvés par [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], et [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Facultatif) Pixels de suivi d’événements tiers qui seront joints par défaut à toutes les nouvelles publicités de l’emplacement. Pour spécifier les pixels d’événement :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, cochez la case dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Renseignez les informations suivantes :
         * **[!UICONTROL Pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous aide à identifier facilement le pixel.
         * **[!UICONTROL Pixel event fires on]:** Événement qui déclenche le déclenchement du pixel. Les événements disponibles varient en fonction du type de publicité.
         * **[!UICONTROL Pixel type]:** Si le pixel est un *[!UICONTROL IMG URL]* (fichier image 1x1 pixel), *[!UICONTROL HTML]* ou *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** URL de l’image de pixel.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Facultatif) Pixels de suivi des conversions qui seront joints par défaut à toutes les nouvelles publicités de l’emplacement. Pour spécifier les pixels de conversion :

1. Cliquez sur ![Modifier](/help/dsp/assets/edit.png).
1. Effectuez l’une des opérations suivantes :
   * Pour sélectionner un pixel existant, cochez la case dans la ligne de pixel.
   * Pour créer un pixel :
      1. Cliquez sur **[!UICONTROL Create]**.
      1. Renseignez les informations suivantes :
         * **[!UICONTROL Conversion pixel name]:** Nom du pixel ; la longueur maximale est de 500 caractères. Utilisez un nom qui vous aide à identifier facilement le pixel.
         * **[!UICONTROL Conversion category]:** Type de conversion.
         * **[!UICONTROL Impression conversion window]:** Nombre de jours après une impression publicitaire au cours desquels l’impression peut être attribuée à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Click conversion window]:** Nombre de jours après un clic publicitaire pendant lesquels le clic peut être attribué à une conversion. La valeur par défaut est de 30 jours.
         * **[!UICONTROL Notes]:** (Facultatif) Une description ou d’autres informations sur le pixel.
      1. Cliquez sur **[!UICONTROL Create and attach]**.
      1. Implémentez le pixel de conversion sur les pages web appropriées :
         1. Dans le menu principal, accédez à **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. Dans la ligne de pixel, cliquez sur **[!UICONTROL edit]**.
         1. Copiez la ou les valeurs dans la variable [!UICONTROL HTML Tag] et [!UICONTROL Flash Tag] le cas échéant, pour fournir les informations au contact de l’annonceur ou du site web.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.
   1. Cliquez sur **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Facultatif) Taux de frais tiers statique qui doit être suivi comme un coût non facturable pour 1 000 impressions. Le cas échéant, la valeur par défaut au niveau du package est automatiquement appliquée pour les nouveaux emplacements, sauf si vous saisissez une autre valeur.

>[!NOTE]
>
>Les frais facturables sont reflétés dans la variable [!UICONTROL Net CPM] mesure.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Création d’un emplacement](placement-create.md)
>* [Modifier un emplacement](placement-edit.md)
>* [Raccourcis clavier](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Questions fréquentes à propos de Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

