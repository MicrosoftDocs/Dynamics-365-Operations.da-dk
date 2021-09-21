---
title: Tidligere igangværende job afsluttes, når delantal rapporteres for det sidste job
description: Når jeg bruger jobkortenheden til at rapportere en delmængde på det sidste job i en produktionsordre, vil alle tidligere job på den ordre, der har status som igangværende, automatisk blive afsluttet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475946"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Tidligere igangværende job afsluttes, når delantal rapporteres for det sidste job

## <a name="symptoms"></a>Symptomer

Når jeg bruger jobkortenheden til at rapportere en delmængde på det sidste job i en produktionsordre, vil alle tidligere job på den ordre, der har status som igangværende, automatisk blive afsluttet.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. På siden **Produktionsordrestandarder** under fanen **Færdigmelding** er der en indstilling med navnet **Slutmarker rute**. Hvis dette emne er angivet til *Ja*, bogføres en rutekortkladde, når en arbejder bruger jobkortenheden eller jobkortterminalen til at rapportere den sidste operation. I denne kladde markeres alle operationer som fuldført, og alle produktionsjob afsluttes. Når indstillingen **Slutmarker rute** er angivet til *Ja*, betragter systemet ikke den jobstatus, som arbejderen valgte, da denne rapporterede den sidste operation. Systemet overvejer heller ikke, om arbejderen rapporterer en fuld eller delvis mængde.
