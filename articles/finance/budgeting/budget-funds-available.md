---
title: Tilgængelige budgetmidler
description: Dette emne introducerer funktionen for budgetmidler og indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetstyring for at optimere administrationen af organisationens økonomiske ressourcer.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891306"
---
# <a name="budget-funds-available"></a>Tilgængelige budgetmidler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne introducerer funktionen for budgetmidler og indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetstyring for at optimere administrationen af organisationens økonomiske ressourcer.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Udvidet beregningsfunktionen for disponible budgetmidler

Med funktionen **Spor kun beløb i beregningen af disponible budgetmidler** kan du spore de underliggende tabeller til budgetstyring for dokumenttyper og tilstande baseret på indstillingerne fra siden **Definer budgetstyringsparametre**.

Visse indstillinger for budgetstyringskonfiguration skal have bestemte indstillinger, for at funktionen kan fungere korrekt. Disse indstillinger vælges eller ryddes under fanen **Tilgængelige budgetmidler** på siden **Definer budgetstyringsparametre**. Følgende tabel viser de indstillinger, der kræves til funktionen for disponible budgetmidler.

| Hvis denne indstilling er valgt | Skal denne indstilling også være valgt |
| ------------------------- | -------------------------------- |
| Budgetreservationer for budgetreservationer | Budgetreservationer for behæftelser *og* faktiske udgifter |
| Budgetreservation for behæftelser | Faktiske udgifter |
| Budgetreservationer for behæftelser med dokumenter af typen Indkøbsrekvisition | Budgetreservationer for budgetreservationer |

Denne funktion påvirker kun nye dokumenter. Beløbene for eksisterende dokumenter spores og vises fortsat i forespørgslerne til budgetstyringsstatistik, indtil en indstilling for budgetmidler, der er til rådighed, ændres, og den nye budgetstyringskonfiguration er aktiveret. På dette tidspunkt fjernes budgetsporingsdata for dokumenter, der blev fjernet fra beregningen af disponible budgetmidler.

Det anbefales, at du lader indstillingen **Ikke-bogførte faktiske udgifter** være ryddet. Hvis feltet er markeret, udføres der en tidskrævende budgetstyringsberegning på ikke-bogførte dokumenter, f.eks. ventende kreditorfakturaer.
