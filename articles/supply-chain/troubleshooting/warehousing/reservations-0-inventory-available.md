---
title: Kan ikke foretage lagerreservationer, fordi 0,00 er tilgængelige
description: Du får vist en fejl, hvor systemet ikke kan foretage reservationer, fordi der kun er 0,00 tilgængelige på lageret. Dette problem skyldes sandsynligvis åbent arbejde.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475935"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Systemet kan ikke foretage lagerreservationer, fordi 0,00 er tilgængelige i lageret

## <a name="symptoms"></a>Symptomer

Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner. Du kan modtage følgende fejlmeddelelse:

> Fysisk disponibel sted=%1, lagersted=%2, lagerstatus=tilgængelig, batchnummer=%3, ejer=%4: %5 kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret.

## <a name="resolution"></a>Løsning

Dette problem skyldes sandsynligvis åbent arbejde. Du skal enten fuldføre arbejdet eller modtage uden arbejdsoprettelse. Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet. Disse transaktioner kan f.eks. være åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.
