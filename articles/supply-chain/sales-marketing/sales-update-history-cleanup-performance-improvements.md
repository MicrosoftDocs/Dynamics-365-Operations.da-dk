---
title: Forbedringer af ydeevnen for oprydning i salgshistorikken
description: I dette emne beskrives funktionen til forbedring af performance for salgshistorikken, og hvordan den aktiveres.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985905"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Forbedringer af ydeevnen for oprydning i salgshistorikken

[!include [banner](../includes/banner.md)]

**Oprydning i salgshistorikken** kan tage lang tid, hvis den køres sjældent i miljøer med en stor mængde salgsopdateringer. I disse situationer kan funktionen til *forbedring af performance for salgshistorikken* hjælpe med at reducere varigheden af kørslen og forbedre pålideligheden.

Funktionen forbedrer det eksisterende oprydningsjob på følgende måder:

- Oprydningen opdeles i batches (du kan ændre batchstørrelsen via tilpasninger).
- Den kører i maksimalt 2 timer (du kan ændre varigheden via tilpasninger).
- Hvor det er muligt, bruges databasefunktionerne til at minimere låsning og til at undgå at forbinde transaktionstabeller under oprydning.

Når funktionen er aktiveret, køres **oprydningen af historikken for salgsopdatering** (**Salgs og marketing \> Periodiske opgaver \> Oprydning \> Oprydning af salgsopdateringhistorik**) som før, men med bedre ydeevne og højst 2 timer. Det betyder, at det kan være nødvendigt at køre flere gange for at rydde op i alle data for en bestemt tidsramme til tilbageholdelse.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>Aktivere funktionen til forbedring af ydeevnen for oprydning af salgshistorik

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Salg og marketing*
- **Funktionsnavn:** *Forbedringer af ydeevnen i oprydningssalgshistorik*
