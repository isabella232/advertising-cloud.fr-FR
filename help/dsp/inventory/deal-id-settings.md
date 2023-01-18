---
title: Paramètres d’ID de transaction manuelle
description: Voir la description des paramètres des ID de transaction saisis manuellement.
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Paramètres d’ID de transaction manuelle

| Section | Paramètre | Description | Obligatoire | Modifiable |
|---------|-----------|-------------|----------|----------|
| [Détails de l’opération] | [!UICONTROL Deal name] | Le nom utilisé pour identifier votre [!UICONTROL Deal ID] dans le DSP de publicité. Saisissez un nom ou sélectionnez **[!UICONTROL Auto-name]** pour permettre DSP générer un nom basé sur les détails de l’opération.<br><br>Exemple de nom généré automatiquement : `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Oui | Oui |
|  | [!UICONTROL External deal ID] | Identifiant utilisé par votre éditeur et le fournisseur de services de messagerie pour identifier cette transaction. | Oui | Non |
|  | [!UICONTROL Publisher] | Nom de l’éditeur qui vend cet inventaire. | Oui | Non |
|  | [!UICONTROL SSP] | Plateforme côté offre (SSP) sur laquelle s’exécute cet accord. | Oui | Non |
|  | [!UICONTROL Media type] | Le type de média acheté lors de cette transaction : *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]* ou *[!UICONTROL Audio]*. Les options varient selon SSP.<br><br> Si l’accord autorise plusieurs types de médias, sélectionnez le type de média de l’emplacement par défaut lors de la création de l’accord. Plus tard, vous pouvez modifier la valeur ou vous pouvez simplement [joindre un nouvel emplacement avec le type de média supplémentaire](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Oui | Non |
|  | [!UICONTROL Deal type] | L&#39;engagement et la structure de prix de l&#39;accord :<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Vous et l’éditeur n’avez pas engagé de nombre fixe de diffusions d’impression. L&#39;accord spécifie le prix minimum pour l&#39;inventaire, bien que le CPM puisse fluctuer et augmenter selon les conditions du marché.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Vous et l’éditeur n’avez pas engagé de nombre fixe de diffusions d’impression. La tarification est à un taux fixe négocié.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Vous et l’éditeur avez convenu d’un nombre prédéfini d’impressions, de ciblage, de dates de vol et de prix fixe.<br><br><b>Remarque :</b> Les offres garanties exigent des dates de vol et un nombre spécifié d’impressions dans la variable [!UICONTROL Tracking] . Vous devez également créer un emplacement par défaut garanti par programme (PG) pour l’opération, et vous pouvez éventuellement utiliser l’opération pour d’autres emplacements à la place.</li></ul> | Oui | Non |
|  | [!UICONTROL CPM] | Le coût négocié par 1 000 impressions (CPM). | Oui | Oui |
|  | [Devise] | Devise de l’accord.<br><br>Tous les SSP acceptent des offres en USD. Lorsque le SSP accepte la devise de votre compte DSP, cette devise est également disponible. | Oui | Non |
|  | [!UICONTROL Billing method] | Tous les identifiants de transaction sont [!DNL Adobe]-financé et -facturtered. DSP paie tous les fournisseurs de médias disponibles en fonction de leur utilisation, gère les incohérences avec les fournisseurs et envoie une facture consolidée au compte. Cette option entraîne des frais supplémentaires, comme indiqué dans la carte de taux du compte. | Oui | Non |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Adresse électronique du compte utilisateur qui peut accéder à la transaction. | Non | Oui |
|  | [!UICONTROL Advertisers that can access this deal] | Les publicitaires spécifiques du compte qui peuvent accéder à cette transaction.<br><br><b>Remarque :</b> Vous pouvez partager l’opération avec les annonceurs dans des comptes supplémentaires de la [!UICONTROL Deals] vue. Sur la ligne de la transaction, cliquez sur **[!UICONTROL #]**, cliquez sur **[!UICONTROL share]**, puis partagez l’opération avec une adresse électronique. | Oui | Oui |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Les dates de début et de fin du trafic utilisant cette transaction. Ces dates sont destinées au suivi uniquement et n’ont aucune incidence sur la diffusion des publicités.<br><br><b>Conseil :</b> Dans le [!UICONTROL Inventory] > [!UICONTROL Deals] vue, [!UICONTROL Pacing & Budget] La colonne indique comment l’opération s’étend à la date de vol spécifiée et à l’objectif d’impression. Si la diffusion est en sous-ou en trop-rythme, contactez votre éditeur pour ajuster le volume qu’elle envoie via l’offre. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |
|  | [!UICONTROL Impressions] | (Facultatif pour les offres non garanties) Nombre estimé d’impressions que vous prévoyez d’exécuter à l’aide de cette opération. Cette valeur est fournie à des fins de suivi uniquement ; l’éditeur contrôle la diffusion de la publicité. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Créer manuellement les détails de l’identifiant de transaction](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [À propos du stock privé](private-inventory-about.md)

