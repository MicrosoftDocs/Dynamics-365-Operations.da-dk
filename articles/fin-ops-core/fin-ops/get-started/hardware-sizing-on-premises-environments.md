---
title: Krav til tilpasning af hardware til lokale miljøer
description: Krav til tilpasning af hardware til lokale miljøer
author: sericks007
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: b89135cd9e951e690e53c1b4bf98dfcb03f2d652
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694463"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Krav til tilpasning af hardware til lokale miljøer

[!include [banner](../includes/banner.md)]

Før du begynder at tilpasse hardware og infrastruktur til et lokalt miljø, skal du sætte dig ind i [Systemkrav til skyinstallationer](system-requirements.md) og læse [Vejledning til installation og implementering](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) for at få en ordentlig forståelse af den underliggende struktur.

> [!NOTE]
> Vær særligt opmærksom på best practices for opsætning af systemet for at opnå optimal ydelse.

Når du har gennemgået dokumentationen, kan du begynde at vurdere dit antal af transaktioner og samtidige brugere og tilpasse dit miljø baseret på det gennemsnitlige systemgennemløb.

## <a name="factors-that-affect-sizing"></a>Faktorer, der påvirker kapacitet

Alle faktorer, der er vist i følgende illustration, skal tages i betragtning, når du vurderer hardwarens størrelse eller kapacitet. Jo mere detaljerede oplysninger, der indsamles, desto mere præcist kan du bestemme størrelsen. Hvis du vurderer hardwarestørrelsen uden understøttende data, bliver resultatet næppe nøjagtigt. Det absolutte minimumkrav for de nødvendige data er spidsbelastningen pr. transaktionslinje pr. time.

[![Tilpasning af hardware til lokale miljøer](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Set fra venstre mod højre er den første og vigtigste faktor, der er nødvendig for at anslå den korrekte størrelse, er en transaktionsprofil eller transaktionsbeskrivelse. Det er vigtigt altid at finde spidsbelastningen for transaktionsvolumen pr. time. Hvis der er flere perioder med spidsbelastning, skal disse perioder defineres korrekt.

Efterhånden som du forstår i, hvilken belastning der har indflydelse på infrastrukturen, skal du også have en mere detaljeret forståelse af disse faktorer:

- **Transaktioner** – Transaktioner har typisk visse toppe i dagens/ugens løb. Dette afhænger hovedsageligt af transaktionstypen. Tids- og udgiftsposter topper normalt én gang om ugen, mens salgordreposteringer ofte foregår samlet via integration eller kommer lidt efter lidt i løbet af dagen.
- **Antal samtidige brugere** – Antallet af samtidige brugere er den næstvigtigste faktor ved tilpasning af størrelse. Du kan ikke få pålidelige størrelsesestimater, der er baseret på antallet af samtidige brugere, så hvis du kun har disse data til rådighed, skal du anslå et omtrentligt antal og derefter genoverveje dette, når du har flere data. En nøjagtig definition af samtidige brugere indebærer, at:

    - Navngivne brugere ikke er samtidige brugere.
    - Samtidige brugere altid er et undersæt af navngivne brugere. 
    - Spidsbelastning definerer den maksimale samtidighed ved størrelsestilpasning.

    Kriterier for samtidige brugere er, at brugeren opfylder alle følgende kriterier:

    - Er logget på.
    - Arbejder med transaktioner/forespørgsler på tidspunktet for optælling.
    - Ikke en inaktiv session.

- **Datakomposition** – Dette drejer sig primært om, hvordan systemet bliver indstillet og konfigureret. F.eks. hvor mange juridiske enheder, du skal have, hvor mange varer, hvor mange styklisteniveauer, og hvor kompleks konfigurationen af sikkerheden bliver. Hver af disse faktorer kan påvirke ydeevnen en lille smule, så disse faktorer kan blive udlignet ved hjælp af intelligent valgmuligheder, når det drejer sig om infrastruktur.
- **Udvidelser** – Tilpasninger kan være simple eller komplekse. Antallet af tilpasninger og arten af kompleksitet og forbrug har varierende indflydelse på størrelsen af den nødvendige infrastruktur. For komplekse tilpasninger anbefales det at foretage en evaluering af ydeevnen for at sikre, at de ikke kun testes for effektiviteten, men også gør det lettere at forstå infrastrukturbehovene. Dette er endnu vigtigere, når udvidelserne ikke er kodet i overensstemmelse med best practices for ydeevne og skalerbarhed.
- **Rapportering og analyser** – Disse faktorer omfatter typisk kørsel af komplekse forespørgsler i de forskellige databaser i systemet. Når du ved kørsel af dyre rapporter forstår og kan reducere hyppigheden, kan du også bedre forstå virkningen af dem.
- **Løsninger fra tredjepart** – For disse løsninger, f.eks. fra softwareproducenter, gælder samme implikationer og anbefalinger som for udvidelser.

## <a name="sizing-your-environment"></a>Tilpasse størrelsen af dit miljø

For at kende kravene til størrelsestilpasning skal du kende det maksimale antal transaktioner, som du har brug for at behandle. De fleste hjælpesystemer, som Management Reporter eller SSRS, er mindre missionskritiske. Derfor fokuseres der oftest på AOS og SQL Server i dette dokument.

> [!NOTE]
> Generelt udskaleres beregningsniveauerne og skal være konfigureret som N + 1, dvs. at hvis du beregner tre AOS, skal du tilføje en fjerde AOS. Databaseniveauet skal konfigureres i en Always On-opsætning med høj tilgængelighed.

## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Størrelsestilpasning

- 3K og 15K transaktionslinjer pr. time, pr. processorkerne på DB-server.
- Typisk AOS-til-SQL-kerneforhold 3:1 for den primære SQL Server. Ekstra kerner er påkrævet, baseret på den valgte højtilgængelighedskonfiguration.

    - Behandling af handlinger, der trækker meget på databasen, kan sætte dette tilbage til 2:1.

- Følgende faktorer påvirker variationer:

    - Aktuelt anvendte parameterindstillinger.
    - Udvidelsesniveauer.
    - Brug af flere funktioner, f.eks. databaselog og påmindelser. Ekstremt omfang af databaselogning reducerer yderligere gennemløbet pr. time pr. processorkerne under 3K linjer.
    - Kompleksiteten af datasammensætningen – En simpel kontoplan kontra en detaljeret kontoplan f.eks. har konsekvenser for gennemløbet.
    - Transaktionsbeskrivelse.
    - 2 GB til 16 GB hukommelse for hver kerne.
    - Ekstra databaser på DB-server som f.eks. Management Reporter og SSRS-databaser.
    - Temp DB = 15 % af DB størrelse, med lige så mange filer som fysiske processorer.
    - SAN-størrelse og -gennemløb baseret på det samlede antal/brug af samtidige transaktioner.

### <a name="high-availability"></a>Høj tilgængelighed

Vi anbefaler altid at benytte SQL Server i en klynge- eller spejlingskonfiguration. Den sekundære SQL-node skal have det samme antal kerner, som den primære node.

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)

Du kan finde oplysninger om tilpasning af AD FS i [Dokumentationen til AD FS-serverkapacitet](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Du kan finde et [størrelsestilpasningsregneark](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) til planlægning af antallet af forekomster i installationen.

## <a name="aos-online-and-batch"></a>AOS (Online og batch)

### <a name="sizing"></a>Størrelsestilpasning

- Tilpasning efter antal/brug af transaktioner

    - 2K til 6K linjer pr. processorkerne
    - 16 GB pr. forekomst
    - Standardpakke – 4-24 kerner
    - 10-15 Enterprise-brugere pr. processorkerne
    - 15-25 Activity-brugere pr. processorkerne
    - 25-50 teammedlemmer pr. processorkerne

- Batch

    - 1 til 4 batchtråde pr. processorkerne
    - Størrelse baseret på en beskrivelse af batchvindue

- Bemærk, at AOS, Datastyring og Batch er i den samme rolle i Service Fabric. Du skal tilpasse størrelsen for disse tre arbejdsbyrder samlet og ikke adskille dem som i Microsoft Dynamics AX 2012.
- De samme variationsfaktorer som for SQL Server gælder her.

### <a name="high-availability"></a>Høj tilgængelighed

- Sørg for at have mindst 1 til 2 flere AOS'er tilgængelig, end du beregner.
- Sørg for at have mindst 3 til 4 tilgængelige virtuelle værter.

## <a name="management-reporter"></a>Management Reporter

I de fleste tilfælde bør de anbefalede minimumkrav med to noder være velegnet, medmindre anvendelsesomfanget er særlig stort. Kun i tilfælde med ekstraordinær stor anvendelse har du brug for mere end to noder. Skaler efter behov.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services

I versionen til almindelig tilgængelighed kan kun én SSRS-node installeres. Overvåg SSRS-noden under test, og øg antallet af kerner, der er tilgængelige for SSRS, på grundlag af behovet. Sørg for at have en forudkonfigureret sekundær node på en virtuel vært, som er forskellig fra SSRS VM'en. Det er vigtigt, hvis der er et problem med den virtuelle maskine, der er vært for SSRS, eller den virtuelle vært. Hvis det er tilfældet, skal den udskiftes.

## <a name="environment-orchestrator"></a>Miljø-Orchestrator

Tjenesten Orchestrator er den tjeneste, der styrer installationen og den relaterede kommunikation med LCS. Denne tjeneste installeres som den primære Service Fabric-tjeneste og kræver mindst tre VM'er. Tjenesten er placeret sammen med Service Fabric Orchestration-tjenesterne. Dette og skal tilpasses klyngens spidsbelastning. Du kan finde flere oplysninger i [Planlægge og forberede enkeltstående Service Fabric-klyngeinstallation](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="virtualization-and-oversubscription"></a>Virtualisering og overtegning

Missionskritiske tjenester som AOS skal hostes på virtuelle værter, der har dedikerede ressourcer – kerner, hukommelse og diskplads.
