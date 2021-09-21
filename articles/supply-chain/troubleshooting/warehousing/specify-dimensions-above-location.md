---
title: Der kan ikke frigives belastning for delantal med batch-over-hierarki
description: Når du bruger en vare med reservationshierarkiet fra batch-over, skal belastningslinjerne angive dimensionerne over lokationen, for at lageret kan fordeles.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475879"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Der kan ikke frigives belastning for delantal med batch-over-reservationshierarki

## <a name="symptoms"></a>Symptomer

Når du bruger en vare, der har et *batch over*-reservationshierarki, vil kommandoen **Frigiv til lagersted** på siden **Panelet Lastplanlægning** ikke fungere, hvis du prøver at frigive en last for en delmængde. Du modtager følgende fejlmeddelelse:

> For at blive tildelt en bølge skal lastlinjer angive dimensionerne over lokationen. Du kan tildele disse dimensioner ved at reservere og genoprette lastlinjen.

Men, hvis du bruger en vare, der har et *batch under*-reservationshierarki, kan du frigive en last for en delmængde fra siden **Panelet Lastplanlægning**.

## <a name="cause"></a>Årsag

Når en dimension er over **Lokation**-dimensionen i reservationshierarkiet, skal den angives før frigivelsen til lagerstedet. Lageret kan kun fordeles, hvis der ikke er huller i dimensionerne over lokationen.

## <a name="resolution"></a>Løsning

Sørg for, at alle dimensioner over **lokationen** er tildelt, ved at reservere og oprette belastningslinjen igen.
