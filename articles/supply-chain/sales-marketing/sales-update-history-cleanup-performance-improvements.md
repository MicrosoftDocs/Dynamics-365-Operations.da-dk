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
ms.openlocfilehash: d4eeee3c1228b278fea07464f35946c295c5aea8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679049"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Forbedringer af ydeevnen for oprydning i salgshistorikken

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!-- GA with 10.0.24 -->

**Oprydning i salgshistorikken** kan tage lang tid, hvis den køres sjældent i miljøer med en stor mængde salgsopdateringer. I disse situationer kan funktionen til *forbedring af performance for salgshistorikken* hjælpe med at reducere varigheden af kørslen og forbedre pålideligheden.

Funktionen forbedrer det eksisterende oprydningsjob på følgende måder:

- Oprydningen opdeles i batches (du kan ændre batchstørrelsen via tilpasninger).
- Den kører i maksimalt 2 timer (du kan ændre varigheden via tilpasninger).
- Hvor det er muligt, bruges databasefunktionerne til at minimere låsning og til at undgå at forbinde transaktionstabeller under oprydning.

Når funktionen er aktiveret, køres **oprydningen af historikken for salgsopdatering** (**Salgs og marketing \> Periodiske opgaver \> Oprydning \> Oprydning af salgsopdateringhistorik**) som før, men med bedre ydeevne og højst 2 timer. Det betyder, at det kan være nødvendigt at køre flere gange for at rydde op i alle data for en bestemt tidsramme til tilbageholdelse.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Aktivere funktionen til forbedring af ydeevnen i oprydningssalgshistorik

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Salg og marketing*
- **Funktionsnavn:** *Forbedringer af ydeevnen i oprydningssalgshistorik*