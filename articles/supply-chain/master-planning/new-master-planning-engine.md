---
title: Migrering til planlægningsoptimering for varedisponering
description: Dette emne giver oplysninger om det nye varedisponeringsprogram, Planlægningsoptimering, og om migrering fra det eksisterende program.
author: ChristianRytt
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9590213ef73f7623aff10d4c8ee3efbea0e7984b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823451"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migrering til planlægningsoptimering for varedisponering

[!include [banner](../includes/banner.md)]

Det indbyggede varedisponeringsprogram er planlagt til at blive forældet (udfaset, frarådes). Det erstattes af tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management. Dette emne giver oplysninger om virkningen af nye og eksisterende installationer. Det indeholder oplysninger om nødvendige handlinger.

Planlægningsoptimering giver dig mulighed for at beregne varedisponering udenfor Supply Chain Management og dens Azure SQL-database. De fordele, der er tilknyttet funktionen Planlægningsoptimering, omfatter forbedret ydeevne og minimeret påvirkning af SQL-databasen under kørsel af varedisponeringen. Da hurtige planlægningskørsler kan udføres selv i kontortiden, kan planlæggerne reagere øjeblikkeligt på ændringer i behov eller parametre.

Du kan finde flere oplysninger om Planlægningsoptimering under [Oversigt over Planlægningsoptimering](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Forældelse af det eksisterende varedisponeringsprogram

Microsoft er i gang med at gøre det indbyggede planlægningsprogram forældet til fordel for Planlægningsoptimering. Denne ændring påvirker alle skymiljøer. Lokale installationer påvirkes ikke. I version 10.0.16 og nyere vil du få vist en fejlmeddelelse, hvis du kører den indbyggede varedisponering uden at generere produktionsordreforslag. Men varedisponeringskørslen vil dog gennemføres uanset fejlmeddelelsen.

Yderligere oplysninger om forældelse af det indbyggede planlægningsprogram finder du i [Fjernede eller udfasede funktioner i Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Migrering, meddelelser og undtagelser

Ejere af eksisterende miljøer, der kører det indbyggede varedisponeringsprogram uden generering af produktionsordreforslag, modtager en mail med detaljer om undtagelsesprocessen. Det anbefales, at du arbejder med en partner for at evaluere og planlægge migreringen til planlægningsoptimering.

Som nævnt vil du i version 10.0.16 og nyere du få vist en fejlmeddelelse, hvis du kører den indbyggede varedisponering uden at generere produktionsordreforslag. Denne fejlmeddelelse indeholder vejledning om migrering og instruktioner i at anmode om en undtagelse.

### <a name="new-deployments"></a>Nye installationer

Planlægningsoptimering skal betragtes som standard for varedisponeringsprogrammet ved alle nye installationer i skyen. Planlægningsoptimering skal generelt bruges til alle nye installationer, der ikke genererer produktionsordreforslag under varedisponering. Hvis en ny installation afhænger af funktionalitet, som Planlægningsoptimering ikke understøtter i øjeblikket, kan du anmode om en undtagelse, så du kan fortsætte med at bruge det indbyggede varedisponeringsprogram.

### <a name="existing-deployments"></a>Eksisterende installationer

Ejere af eksisterende skybaserede installationer, der afhænger af varedisponering, skal planlægge at migrere til Planlægningsoptimering. Hvis din implementering afhænger af funktionalitet, som Planlægningsoptimering ikke understøtter i øjeblikket, kan du anmode om en undtagelse, så du kan fortsætte med at bruge det indbyggede varedisponeringsprogram.

Til miljøer, der i øjeblikket bruger varedisponeringsprocesser, der bliver forældede, sender Microsoft en mail til miljøadministratoren. Denne mail indeholder oplysninger om de handlinger, der kræves for at overføre produktet eller anmode om en undtagelse.

## <a name="the-exception-process"></a>Undtagelsesprocessen

Du kan anmode om en undtagelse, hvis du skal fortsætte med at bruge det indbyggede varedisponeringsprogram, fordi dine forretningsprocesser er meget afhængige af mindst én funktion, der aktuelt ikke er implementeret i Planlægningsoptimering. Du kan se en oversigt over tilgængelige funktioner i [Analyse af tilpasning af planlægningsoptimering](planning-optimization/planning-optimization-fit-analysis.md).

I øjeblikket er undtagelser fra migrering til Planlægningsoptimering kun relevante, hvis din varedisponeringsproces ikke omfatter produktion (dvs. varedisponeringsgenererede produktionsordreforslag), og du har brug for det indbyggede varedisponeringsprogram ud over version 10.0.15.

Når de påkrævede funktioner bliver tilgængelige, vil Microsoft give en frist, indtil undtagelsen udløber. Miljøadministratoren vil blive informeret, når de påkrævede funktioner er blevet tilgængelige, og fristen er påbegyndt.

> [!NOTE]
> Du kan kun anmode om en undtagelse for produktionsmiljøer, ikke for sandkassemiljøer. Hvis du har brug for at deaktivere undtagelsesfejlen i Planlægningsoptimering i et sandkassemiljø på en infrastruktur som en service (IaaS), skal du køre den SQL-forespørgsel, der er indeholdt i [Sandkassemiljøer](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandkassemiljøer

Kan jeg bruge indbygget varedisponering på mit sandkassemiljø? Har jeg brug for en undtagelse?

**Svar:** Undtagelser er normalt ikke relevante for sandkassemiljøer, fordi undtagelsesfejlen i Planlægningsoptimering ikke forhindrer det indbyggede varedisponeringsprogram i at køre korrekt. Men hvis fejlmeddelelsen bliver forstyrrende for dig, kan du deaktivere den i et IaaS-sandkassemiljø (ikke Service Fabric) ved at køre følgende forespørgsel på din database:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Lokale miljøer

Mit miljø er lokalt. Har jeg brug for en undtagelse?

**Svar:** Nej. Der kræves ikke en undtagelse i lokale miljøer. Du kan fortsætte med at bruge den indbyggede varedisponering. Din miljøadministrator vil blive underrettet, hvis der kræves en handling.

### <a name="production-scenarios"></a>Produktionsscenarier

Vi bruger produktionsordreforslag, men jeg er bekymret for, hvad der sker, når vi opgraderer til version 10.0.16. Skal jeg gøre noget?

**Svar:** Du skal ikke være bekymret. Du kan fortsætte med at bruge den indbyggede varedisponering i version 10.0.16. Det anbefales dog, at du evaluerer, om migrering til Planlægningsoptimering kan starte med den aktuelle funktionalitet. Vi anbefaler også, at du holder dig informeret om nye funktioner.

### <a name="email-from-microsoft"></a>Mail fra Microsoft

Vores miljøadministrator har modtaget en mail fra Microsoft. Denne mail angiver, at vi skal migrere til Planlægningsoptimering eller anmode om en undtagelse. Skal jeg gøre noget?

**Svar:** Ja. Dit miljø vil blive påvirket, hvis du ikke følger instruktionerne i mailen. Du kan enten migrere til Planlægningsoptimering inden den angivne dato eller anmode om en undtagelse ved hjælp af linket i mailen. Dette link åbner et spørgeskema. Når du har udfyldt og indsendt dette spørgeskema, vil du modtage et svar via mail. Selvom denne proces er manuel, forsøger Microsoft at svare i løbet af en uge, efter at spørgeskemaet er afsendt.

### <a name="error-messages"></a>Fejlmeddelelser

Jeg bruger version 10.0.16 eller nyere, og jeg får vist følgende fejlmeddelelse, når jeg kører varedisponering. Er varedisponering blokeret?

> Du får vist denne fejlmeddelelse, fordi det indbyggede varedisponeringsprogram blev brugt til scenarier, der understøttes af Planlægningsoptimering. Du bør migrere til Planlægningsoptimering nu, da den aktuelt indbyggede varedisponering udfases. Bemærk, at denne varedisponeringskørsel blev fuldført korrekt.
>
> Hvis din migrering har en stærk afhængighed i forhold til ventende funktioner, kan du anmode om en undtagelse for fortsat at bruge det indbyggede varedisponeringsprogram.
>
> Udfyld følgende spørgeskema for at komme i gang, og hvis det er relevant, skal du anmode om undtagelse fra migrering til Planlægningsoptimering.

**Svar:** Nej, varedisponering er ikke blokeret. Din varedisponeringskørsel blev fuldført korrekt, og du kan bruge resultatet på normal vis. Men hvis du vil undgå at modtage denne fejlmeddelelse under fremtidige varedisponeringskørsler, skal du enten migrere til Planlægningsoptimering med det samme eller anmode om en undtagelse ved hjælp af linket i fejlmeddelelsen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]