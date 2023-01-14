---
title: Questions fréquentes
description: xxx
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Questions fréquentes xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214 Par défaut, Adobe Analytics consigne tous les événements capturés dans chaque rapport. &quot;[!UICONTROL Unspecified]&quot; représentent des événements de remplissage de formulaire qui n’étaient pas connectés à Adobe Advertising. Par exemple, dans le rapport Plateforme publicitaire, les conversions organiques ou les conversions pilotées par une campagne par e-mail tombent dans &quot;non spécifié&quot;.

Vous pouvez utiliser le filtre pour supprimer les événements non spécifiés des rapports en supprimant la coche par l’option &quot;Inclure non spécifié (aucun)&quot;. <!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323 Placez les balises d’événement Analytics aux mêmes emplacements que les pixels Ad Cloud pour vous assurer que XXX correspond.

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q : Au cours de notre audit de sécurité interne, certaines fonctionnalités ont été signalées comme des problèmes de sécurité que nous avons activés lors de l’intégration d’Ad Cloud à notre installation Adobe Analytics existante.

L’intégration en question se trouve entre AdCloud et Adobe Audience Manager. Cette fonctionnalité augmente le taux de correspondance de l’identifiant visiteur entre AdCloud et Adobe Audience Manager. Pour ce faire, il envoie des requêtes réseau à pagead.l.doubleclick.net, star-mini.c10r.facebook.com et pug88000nf.pubmatic.com afin de déterminer si ces services possèdent un identifiant existant pour le visiteur qui peut être exploité. Il s’agit des requêtes réseau qui ont été marquées comme un risque de sécurité et qui se produisent pour tous les visiteurs du site.

Notre Auditor nous demande de désactiver cette fonctionnalité. Que se passe-t-il si nous bloquons ces demandes réseau ?

A : Nous avons vérifié avec notre produit et ils ont mentionné que les pixels en question ont pour but d’augmenter les taux de correspondance des cookies entre Ad Cloud, des partenaires d’inventaire/SSP spécifiques (par rapport à DSP) et AAM.  S’ils sont supprimés, le client peut voir un certain niveau de taux de correspondance diminué entre AAC/AAM et les partenaires d’inventaire pour lesquels les pixels respectifs sont destinés, mais il ne s’attend pas à ce qu’il soit substantiel.

Pour Ad Cloud Search, nous constatons que l’ID d’organisation Experience Cloud de l’annonceur est configuré pour Mathwork, mais que notre équipe produit ne voit pas la configuration de Mathwork pour activer les audiences dans Ad Cloud. Utilisez-vous Adobe Audience Manager pour envoyer des audiences vers Ad Cloud Search ? Si ce n’est pas le cas, la suppression de ces éléments n’aura aucun impact sur le workflow actuel. AAM l’assistance clientèle peut vous aider à supprimer ces pixels si vous ne souhaitez pas qu’ils soient déclenchés.

