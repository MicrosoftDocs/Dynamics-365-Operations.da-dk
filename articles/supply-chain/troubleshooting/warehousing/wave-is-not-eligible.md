---
title: Bølge er ikke berettiget til oprydning
description: Bølge er ikke berettiget til oprydning
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924321"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Bølge er ikke berettiget til oprydning

Fejlkode: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Bølge %1 er ikke berettiget til oprydning.

Du kan ikke rydde op i bølgedataene.  

## <a name="cause"></a>Årsag

Bølgen behandles i øjeblikket som angivet med en af følgende forhold:

- Feltet **Bølgestatus** er angivet til *Udfører*.
- Når du vælger **Batchjob** i gruppen **Bølge** under fanen **Bølge** i handlingsruden, er feltet **Status** ikke angivet til *Afsluttet*, *Fejl* eller *Annulleret*. Derfor kører der aktuelt et batchjob.

## <a name="resolution"></a>Løsning

Vælg **Batchjob** i gruppen **Bølge** under fanen **Bølge** i handlingsruden, og benyt derefter en af følgende fremgangsmåder:

- Hvis feltet **Status** er angivet til *Udfører*: Vælg **Vis opgaver** i gruppen **Batchjob** under fanen **Batchjob** i handlingsruden. Du kan følge status ved at opdatere siden **Batchopgaver**.
- Hvis feltet **Status** ikke er angivet til *Udfører*: Vælg **Skift status** i gruppen **Funktioner** under fanen **Batchjob** i handlingsruden. Vælg **Venter** i feltet *Vælg ny status*. Vælg derefter **OK**.
