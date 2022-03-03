---
title: Der kan ikke oprettes en belastningslinje pga. ugyldige lagerdimensioner
description: Når du forsøger at frigive en retursalgsordre til lagerstedet, kan du få vist en fejl om ugyldige lagerdimensioner. Fjern disse fra ordrelinjen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119206"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Der kan ikke oprettes en belastningslinje for en retursalgsordre pga. ugyldige lagerdimensioner

## <a name="symptoms"></a>Symptomer

Du får vist følgende fejlmeddelelse, når du forsøger at frigive en retursalgsordre til lagerstedet:

> Du kan ikke oprette en lastlinje for denne ordrelinje, fordi den indeholder lagerdimensioner, der er ugyldige. Du kan ikke referere til lagerdimensioner, der findes under lokationsdimensionen i reservationshierarkiet. Fjern de ugyldige dimensioner fra ordrelinjen.

## <a name="resolution"></a>Løsning

Desværre understøtter produktet ikke lastbehandling af en salgsreturproces. Derfor kan du ikke frigive retursalgsordren til lagerstedet.

På salgsordretransaktioner kan du ikke referere til lagerdimensioner, der findes under dimensionen **Lokation** i reservationshierarkiet. Løsningen er at fjerne de ugyldige dimensioner fra ordrelinjen.
