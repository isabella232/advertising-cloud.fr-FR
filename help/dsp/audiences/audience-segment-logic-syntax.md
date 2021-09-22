---
title: Syntaxe de la logique de segment d’audience
description: Référencez la syntaxe que vous pouvez utiliser pour définir la logique pour les segments d’audience.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Syntaxe de la logique de segment d’audience

Lorsque vous créez des audiences réutilisables, vous pouvez définir manuellement la logique de segment à l’aide d’identifiants de segment alphanumériques et de la syntaxe suivante :

* () pour indiquer un groupe
* `||` pour  [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; pour [!DNL AND]
* ! pour [!DNL NOT] (exclude)

>[!NOTE]
>
>* Tous les groupes de segments spécifiés sont inclus, sauf s’ils sont précédés de ! (qui les exclut).


Par exemple, la logique suivante :

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

signifie (en anglais brut)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Dans les paramètres d’emplacement, vous pouvez utiliser des audiences enregistrées comme audiences à cibler explicitement ou comme audiences distinctes à exclure du ciblage. Assurez-vous que votre logique de segment reflète l’objectif pour lequel vous utiliserez l’audience.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Paramètres d’audience](audience-settings.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)

