---
title: Start her med planlægningsoptimering
description: Denne artikel beskriver, hvordan du kommer i gang med at bruge funktionen Planlægningsoptimering.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 629a84135434ad79f8397649ee9a4a62e49751d9
ms.sourcegitcommit: 14a27b776befbc6793390f97e8fb0279c0ea18c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/15/2022
ms.locfileid: "9295922"
---
# <a name="get-started-with-planning-optimization"></a>Kom i gang med planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Som [tidligere annonceret](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) er planlægningsoptimering planlagt til at erstatte det eksisterende indbyggede varedisponeringsprogram.

Hvis du i øjeblikket bruger det indbyggede varedisponeringsprogram, skal du starte med at planlægge din migrering til planlægningsoptimering nu. Det er vigtigt at starte med det samme, da det ellers kan have indflydelse på dine handlinger, når afskrivning gennemtvinges (selvom gennemtvingelse ikke er planlagt i øjeblikket). Vi opfordrer dig på det kraftigste til at fuldføre overflytningen, så snart Planlægningsoptimering understøtter de funktioner, du skal bruge, så du kan begynde at få fordel af de mange forbedringer af ydeevnen og andre nye egenskaber, der leveres af den nye tjeneste.

Funktionen Planlægningsoptimering understøtter i øjeblikket ikke alle de funktioner, der er tilgængelige i det planlægningsprogram, der er indbygget i Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt i Planlægningsoptimering, opfylder dine behov. Planlægningsoptimeringsfunktionen er i øjeblikket ikke aktiveret som standard i Dynamics Lifecycle Services (LCS), så du har mulighed for at foretage din evaluering, før funktionen er slået til.

> [!NOTE]
> Du skal anmode om en undtagelse fra migrering til planlægningsoptimering, hvis din varedisponeringsproces ikke omfatter produktion (varedisponeringsgenererede produktionsordreforslag), og du har brug for det indbyggede varedisponeringsprogram ud over version 10.0.15. Startende med version 10.0.16 vises der en fejl i miljøer, når der køres indbygget varedisponering uden generering af produktionsordreforslag. Planlægningsoptimering skal bruges til alle nye installationer, der ikke genererer produktionsordreforslag under varedisponering. Ejere af eksisterende miljøer, der kører det indbyggede varedisponeringsprogram uden generering af produktionsordreforslag, modtager en mail med detaljer om undtagelsesprocessen. Det anbefales, at du arbejder med en partner for at evaluere og planlægge migreringen til planlægningsoptimering.

Før du slår Planlægningsoptimering til, anbefales det på det kraftigste, at du evaluerer resultaterne af analysen af om Planlægningsoptimering passer. Du kan finde flere oplysninger under [Analyse af om Planlægningsoptimering passer](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Tilgængelighed

Planlægningsoptimering er i øjeblikket tilgængelig i følgende geografiske Azure-områder: USA, Canada, Brasilien, Europa, Frankrig, Storbritannien, Australien, Asien og Stillehavsområdet, Japan og Indien. Hvis du forsøger at installere tilføjelsesprogrammet fra et andet geografisk område, vil LCS vise en meddelelse om, at dette geografiske område ikke understøttes. Yderligere oplysninger om Azure-geografi og de relaterede områder finder du i [Azure-geografiske områder](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Bemærk, at planlægningsoptimering ikke understøtter lokale installationer af Dynamics 365 Supply Chain Management.

## <a name="licensing"></a>Licensering

Hvis du kan køre varedisponering ved hjælp af din aktuelle licens, behøver du ikke købe en ekstra licens for at begynde at bruge Planlægningsoptimering.

## <a name="install-and-enable-planning-optimization"></a>Installere og aktivere Planlægningsoptimering

Hvis du vil bruge Planlægningsoptimering, skal du sikre dig, at systemet har alle de nødvendige forudsætninger på plads, og derefter aktivere licensnøglen og installere tilføjelsesprogrammet Planlægningsoptimering til Dynamics 365 Supply Chain Management.

### <a name="prerequisites"></a>Forudsætninger

Før du installerer tilføjelsesprogrammet Planlægningsoptimering, skal følgende forudsætninger være opfyldt:

- Du skal køre Supply Chain Management i et LCS-aktiveret miljø med høj tilgængelighed på niveau 2 eller højere (ikke et OneBox-miljø) i Dynamics 365 Supply Chain Management version 10.0.7 eller nyere. Hvis du forsøger at installere tilføjelsesprogrammet i et OneBox-miljø, fuldføres installationen ikke, og du skal annullere installationen.

- Systemet skal være konfigureret til Power Platform-integration. Du kan finde flere oplysninger under [Microsoft Power Platform-integration med programmer til finans og drift](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Aktivere licensen til Planlægningsoptimering

Hvis du vil bruge Planlægningsoptimering, skal du aktivere dens konfigurationsnøgle. Benyt følgende fremgangsmåde:

1. Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.
1. Markér afkrydsningsfeltet For **Planlægningsoptimering** under fanen **Konfigurationsnøgler**.
1. Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>Installere tilføjelsesprogrammet Planlægningsoptimering

Du skal installere tilføjelsesprogrammet fra dit LCS-projekt og derefter slå funktionen Planlægningsoptimering til fra brugergrænsefladen i Supply Chain Management.

Sådan installerer du tilføjelsesprogrammet Planlægningsoptimering:

1. Log på LCS, og åbn det ønskede miljø.
1. Gå til **Alle detaljer**.
1. Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.
1. Vælg **Installer et nyt tilføjelsesprogram**.
1. Vælg **Planlægningsoptimering**.
1. Følg installationsvejledningen, og accepter vilkårene og betingelserne.
1. Vælg **Installer**.
1. I oversigtspanelet **Tilføjelsesprogrammer for miljø** skulle du kunne se, at Planlægningsoptimering er ved at blive installeret.
1. Efter nogle minutter bør **Installerer** blive ændret til **Installeret** (du skal muligvis opdatere siden). Når den er installeret, er du klar til at aktivere Planlægningsoptimering i Dynamics 365 Supply Chain Management.

Det vigtigste formål med at installere tilføjelsesprogrammet Planlægningsoptimering er at forbinde tjenesten og miljøet. Derfor skal du installere tilføjelsesprogrammet separat på hvert miljø, hvor du vil bruge Planlægningsoptimering, uanset hvilken kode der flyttes mellem miljøerne.

## <a name="integrate-planning-optimization-with-your-system"></a>Integrere Planlægningsoptimering med dit system

Hvis du vil konfigurere, om tilføjelsesprogrammet til Planlægningsoptimering skal bruges til varedisponering, skal du gå til **Varedisponering** \> **Opsætning** \> **Parametre for Planlægningsoptimering**.

### <a name="connection-status"></a>Forbindelsesstatus

Forbindelsesstatussen angiver den aktuelle status for forbindelsen mellem Supply Chain Management og tjenesten Planlægningsoptimering. I følgende tabel vises de mulige værdier.

| Forbindelsesstatus | Beskrivelse | Kan Planlægningsoptimering anvendes? |
|---|---|---|
| Tilsluttet | Der er oprettet en forbindelse mellem Planlægningsoptimeringstjenesten og Supply Chain Management. | Ja |
| Forbindelse aktiveres | En anmodning om at aktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang. | Nej |
| Forbindelse afbrudt | Der er ingen forbindelse til Planlægningsoptimeringstjenesten. Forbindelsen kan slås til fra LCS, som beskrevet tidligere i denne artikel. | Nej |
| Forbindelse deaktiveres | En anmodning om at deaktivere forbindelsen til Planlægningsoptimeringstjenesten er i øjeblikket i gang. | Nej |
| Henter status | Systemet venter på statusoplysninger fra Planlægningsoptimeringstjenesten. | Nej |

### <a name="the-use-planning-optimization-option"></a>Indstillingen Brug Planlægningsoptimering

Indstillingen af indstillingen **Brug Planlægningsoptimering** bestemmer, hvilket planlægningsprogram der bruges til varedisponering:

- **Ja** – Planlægningsoptimering bruges til varedisponering.
- **Nej** – Det indbyggede planlægningsprogram for Supply Chain Management bruges til varedisponering.

Denne indstilling gælder for alle juridiske enheder (firmaer). Det er ikke muligt at bruge planlægningsoptimering i visse juridiske enheder og den indbyggede varedisponering i andre juridiske enheder.

> [!NOTE]
> Hvis de eksisterende planlægningsbatchjob, der blev oprettet til det indbyggede planlægningsprogram for Supply Chain Management, udløses mens indstillingen **Brug Planlægningsoptimering** er angivet til **Ja**, vil disse job ikke blive udført.

### <a name="integration-with-the-setup"></a>Integration med opsætningen

Hvis Planlægningsoptimering er aktiveret, foretages varedisponering ved hjælp af tilføjelsesprogrammet Planlægningsoptimering. I dette tilfælde påvirkes resultaterne af og funktionerne for varedisponering.

## <a name="additional-resources"></a>Yderligere ressourcer

[Vilkår og betingelser for forhåndsvisning](https://go.microsoft.com/fwlink/?linkid=2015274)

[Oversigt over planlægningsoptimering](planning-optimization-overview.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

