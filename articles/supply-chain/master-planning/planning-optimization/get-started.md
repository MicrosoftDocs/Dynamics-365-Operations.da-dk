---
title: Introduktion til Planlægningsoptimering
description: I dette emne beskrives, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973470"
---
# <a name="get-started-with-planning-optimization"></a>Kom i gang med planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Som [tidligere annonceret](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) er planlægningsoptimering planlagt til at erstatte det eksisterende indbyggede varedisponeringsprogram.

Hvis du i øjeblikket bruger det indbyggede varedisponeringsprogram, skal du starte med at planlægge din migrering til planlægningsoptimering nu. Det er vigtigt at starte migreringsprocessen med det samme, fordi dine handlinger kan blive påvirket, når udfasning gennemtvinges. For at undgå problemer i sidste øjeblik, når udfasning gennemtvinges, anbefaler vi kraftigt, at du fuldfører migreringen før 1. december 2020. 

Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov. Planlægningsoptimeringsfunktionen er i øjeblikket ikke aktiveret som standard i Dynamics Lifecycle Services (LCS), så du har mulighed for at foretage din evaluering, før funktionen er slået til.

> [!NOTE]
> Du skal anmode om en undtagelse fra migrering til planlægningsoptimering, hvis din varedisponeringsproces ikke omfatter produktion (varedisponeringsgenererede produktionsordreforslag), og du har brug for det indbyggede varedisponeringsprogram ud over version 10.0.15. Startende med version 10.0.16 vises der en fejl i miljøer, når der køres indbygget varedisponering uden generering af produktionsordreforslag. Planlægningsoptimering skal bruges til alle nye installationer, der ikke genererer produktionsordreforslag under varedisponering. Ejere af eksisterende miljøer, der kører det indbyggede varedisponeringsprogram uden generering af produktionsordreforslag, modtager en mail med detaljer om undtagelsesprocessen. Det anbefales, at du arbejder med en partner for at evaluere og planlægge migreringen til planlægningsoptimering.

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
