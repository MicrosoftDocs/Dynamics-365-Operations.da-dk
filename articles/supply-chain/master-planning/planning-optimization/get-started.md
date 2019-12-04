---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773923"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Introduktion til Planlægningsoptimering

Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Microsoft Dynamics 365 Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov. Funktionen Planlægningsoptimering er som standard ikke slået til i Dynamics Lifecycle Services (LCS). Derfor har du mulighed for at foretage evalueringen, før den aktiveres.

Til sidst erstatter Planlægningsoptimering det eksisterende indbyggede planlægningsprogram Supply Chain Management.

Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer. Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Licenser

Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.

### <a name="install-the-add-in"></a>Installer tilføjelsesprogrammet

Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management. Du kan få adgang til tilføjelsesprogrammet fra dit LCS projekt og slå Planlægningsoptimeringsfunktionen til fra brugergrænsefladen til Supply Chain Management (UI).

1. Log på LCS, og åbn det ønskede miljø.
1. Gå til **Alle detaljer**.
1. Vælg **Vedligehold**, eller rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.
1. Vælg **Installer et nyt tilføjelsesprogram**.
1. Vælg **Planlægningsoptimering**.
1. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
1. Vælg **Installer**.

### <a name="planning-optimization-integration"></a>Integration af Planlægningsoptimering

Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Integration af Planlægningsoptimering** \> **Integrationsparametre**.

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

## <a name="related-resources"></a>Tilknyttede ressourcer

[Vilkår og betingelser for forhåndsvisning](https://go.microsoft.com/fwlink/?linkid=2015274)

[Oversigt over Planlægningsoptimering](planning-optimization-overview.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)
