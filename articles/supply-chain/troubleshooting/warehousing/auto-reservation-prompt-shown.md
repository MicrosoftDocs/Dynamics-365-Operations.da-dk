---
title: Prompten til automatisk reservation vises med tilgængelig lagerbeholdning
description: Når du bruger den samme vare på et lagersted, hvor lagerprocesser ikke er aktiveret, vises prompten for automatisk reservation. Angiv alle dimensionerne over lokationen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475941"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Prompten til automatisk reservation af batchnummer vises også selv med tilgængelig lagerbeholdning

## <a name="symptoms"></a>Symptomer

Når du bruger en vare, der har et *batch over*-reservationshierarki på et lagersted, hvor der ikke er aktiveret lagerstedsprocesser, og automatisk reservation er aktiveret, vises prompten for automatisk reservation af et batchnummer, også selvom der kun er ét tilgængeligt batch til plukning.

Men når du bruger den samme vare på et lagersted, hvor lagerprocesser er aktiveret, vises prompten for automatisk reservation ikke.

## <a name="resolution"></a>Løsning

Hvis et reservationshierarki defineres som *batch over* eller *serie over*, skal den dimension, der refereres til (**Batchnummer** eller **Serienummer**), altid angives ved behovsordrer. Lagerstedsprocesserne kan muligvis fuldføre oplysningerne, hvis der er et enkelt batch- eller serienummer tilgængeligt. Men da lagerstedet ikke er aktiveret for lagerstedsprocesser, skal brugeren altid angive alle dimensionerne over **Lokation**.
