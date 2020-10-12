---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887258"
---
# <a name="get-started-with-planning-optimization"></a>Introduktion til Planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov. Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS). Derfor har du mulighed for at foretage evalueringen, før den aktiveres.

Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.

Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer. Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Tilgængelighed
Planlægningsoptimering er i øjeblikket tilgængelig i følgende Azure-områder: USA, Canada, Europa, Storbritannien og Australien. Hvis du forsøger at installere tilføjelsesprogrammet fra et andet geografisk område, vil LCS vise en meddelelse om, at dette geografiske område ikke understøttes.

Bemærk, at planlægningsoptimering ikke understøtter lokale installationer af Dynamics 365 Supply Chain Management.

### <a name="licensing"></a>Licensering

Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.

### <a name="install-the-add-in"></a>Installer tilføjelsesprogrammet

Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management. Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).

> [!NOTE]
> Behovet for planlægningsoptimering er et LCS-aktiveret miljø med høj tilgængelighed på niveau 2 eller højere (ikke et Onebox-miljø) i Dynamics 365 Supply Chain Management, version 10.0.7 eller nyere. Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke, og du skal annullere installationen.

1. Log på LCS, og åbn det ønskede miljø.
1. Gå til **Alle detaljer**.
1. Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.
1. Vælg **Installer et nyt tilføjelsesprogram**.
1. Vælg **Planlægningsoptimering**.
1. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
1. Vælg **Installer**.
1. I oversigtspanelet **Tilføjelsesprogrammer for miljø** kan du se, at Planlægningsoptimering er ved at blive installeret.
1. Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden). Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.

### <a name="planning-optimization-integration"></a>Integration af Planlægningsoptimering

Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.

#### <a name="connection-status"></a>Forbindelsesstatus

Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering. I følgende tabel vises de mulige værdier.

| Forbindelsesstatus | Beskrivelse | Kan Planlægningsoptimering anvendes? |
|---|---|---|
| Tilsluttet | Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management. | Ja |
| Forbindelse aktiveres | En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang. | Nr. |
| Forbindelse afbrudt | Der er ingen forbindelse til Planlægningsoptimeringstjenesten. Forbindelsen kan slås til fra LCS, som beskrevet tidligere i dette emne. | Nr. |
| Forbindelse deaktiveres | En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang. | Nr. |
| Henter status | Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten. | Nr. |

#### <a name="the-use-planning-optimization-option"></a>Indstillingen Brug Planlægningsoptimering

Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:

- **Ja** – Planlægningsoptimering bruges til varedisponering.
- **Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.

> [!NOTE]
> Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.

### <a name="integration-with-the-setup"></a>Integration med opsætningen

Hvis forhåndsvisningen af Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet for Planlægningsoptimering. I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.

## <a name="additional-resources"></a>Yderligere ressourcer

[Vilkår og betingelser for forhåndsvisning](https://go.microsoft.com/fwlink/?linkid=2015274)

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
