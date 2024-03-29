---
title: Tilgængelige budgetmidler
description: Denne artikel introducerer funktionen for budgetmidler og indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetstyring for at optimere administrationen af organisationens økonomiske ressourcer.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898234"
---
# <a name="budget-funds-available"></a>Tilgængelige budgetmidler

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel introducerer funktionen for budgetmidler og indeholder oplysninger, der kan hjælpe dig med at konfigurere budgetstyring for at optimere administrationen af organisationens økonomiske ressourcer.

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
