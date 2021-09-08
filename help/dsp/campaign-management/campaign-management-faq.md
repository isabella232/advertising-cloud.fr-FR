---
title: Questions fréquentes sur la gestion des campagnes
description: En savoir plus sur la gestion des campagnes, notamment la période de latence des modifications et ce qui se passe lorsque vous apportez des modifications au budget pendant un vol.
feature: Packages, Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Questions fréquentes sur la gestion des campagnes

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latence de la définition des modifications

* Lorsque vous modifiez un emplacement ou un paramètre de package, quand la modification prendra-t-elle effet ?

   Les modifications de paramètres prennent généralement effet immédiatement, mais peuvent prendre jusqu’à 12 heures.

   Si c’est le dernier jour de livraison, apportez des modifications plus tôt dans la journée afin que DSP dispose de suffisamment de temps pour recalibrer le kit en fonction des modifications. Par exemple, si vous passez de l’espacement régulier à l’espacement de la charge frontale, DSP doit réévaluer la façon dont elle répartira les dépenses tout au long du reste du vol. N&#39;effectuez pas ce genre de changement si vous n&#39;avez qu&#39;une heure pour livrer le dernier jour du vol.

## Mises à jour du budget en milieu de vol

* Lorsque vous modifiez un emplacement, combien de temps DSP-il nécessaire pour réaffecter le budget du package ?

   L’affectation du budget est basée sur les performances des placements, qui sont évaluées à l’aide d’une moyenne de 14 jours. Les modifications apportées à un emplacement entraînent des modifications de l’allocation du budget uniquement lorsqu’elles entraînent des changements de performances pendant la moyenne de 14 jours.

   Lorsque les performances changent, DSP réaffecte le budget de package entre les emplacements en conséquence lors du prochain cycle d&#39;optimisation du budget, qui se produit vers minuit (00:00) dans le fuseau horaire de la campagne.

* Comment le budget est-il réalloué lorsqu’un emplacement est supprimé d’un package et ajouté à un autre package ?

   L’historique des dépenses d’un emplacement est attaché à l’emplacement et l’accompagne d’un package à l’autre.

   Lorsque vous supprimez un emplacement d’un package, celui-ci n’a plus aucun historique des dépenses de l’emplacement. Le budget de package devient (budget de package - budget de placement supprimé) / intervalle de temps restant en vol. Le budget du package est ensuite alloué aux emplacements restants dans le package.

   De même, si vous ajoutez le même emplacement à un autre package, DSP considère l’historique de dépenses de l’emplacement lorsqu’il alloue le budget pour tous les emplacements du nouveau package.

* Comment le rythme des packages change-t-il le dernier jour d’un vol ?

   Le dernier jour d&#39;un vol, la journée est réduite de 24 heures à 23 heures afin que le budget de la formule ne soit pas dépassé. En outre, la stratégie de remplissage du package passe automatiquement à &quot;[!UICONTROL Frontload]&quot;, même s’il est défini sur &quot;[!UICONTROL even]&quot;. Cela signifie que 65 % du budget quotidien doit être affecté avant 11h30 heure de l’Est.

>[!MORELIKETHIS]
>
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Bonnes pratiques pour configurer des campagnes de performances](/help/dsp/optimization/campaign-best-practices-performance.md)

