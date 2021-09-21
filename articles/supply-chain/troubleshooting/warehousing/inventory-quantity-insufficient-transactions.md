---
title: Lagerantallet kan ikke opdateres på grund af utilstrækkelige posteringer
description: Lagerantal -1% kan ikke opdateres, fordi der ikke er nok lagertransaktioner til vare %2, de har de angivne dimensioner.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475855"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Lagerantallet kan ikke opdateres på grund af utilstrækkelige posteringer

## <a name="symptoms"></a>Symptomer

Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner. Du kan modtage følgende fejlmeddelelse:

> Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2 med dimensionsstørrelse=%3, farve=%4, tillæg=%5, sted=%6, lagersted=%7, lokation=%8, lagerstatus=tilgængelig, nummerplade=%9, batchnummer=%10 for reference-id %11 på parti-id %12.

## <a name="resolution"></a>Løsning

Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet. Disse transaktioner kan f.eks. have åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.
