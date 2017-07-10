---
title: Test af overgang under opgradering
description: "Dette emne forklarer, hvordan du kan teste de opgaver, der forekommer, når du har deaktiveret AX 2012, men før du aktiverer Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: da-dk
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Test af overgang under opgradering

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Overgang* er det udtryk, der bruges til den endelige proces for at få et nyt system aktivt. Denne overgangsproces består af de opgaver, der forekommer, når Microsoft Dynamics AX 2012 er deaktiveret, men før Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, er aktiveret. Formålet med testen af opgraderingsovergang er at afprøve overgangsprocessen for at sikre en problemfri oplevelse for alle, der er involveret i løbet af den faktiske overgang til aktivering.

Der findes to primære arbejdsstrømme i løbet af en overgang:

- **Teknisk arbejdsstrøm** – Denne arbejdsstrøm omfatter processen til udførelse af dataopgradering. Virksomheden gennemtvinger en grænse for mængden af nedetid, der er tilladt. I denne nedetid vil hverken AX 2012 eller Finance and Operations være tilgængelig. Denne arbejdsstrøm skal eventuelt tilpasse dataopgraderingsproceduren for at imødekomme en virksomheds nedetidsgrænse.
- **Funktionel arbejdsstrøm** – Denne arbejdsstrøm omfatter de konfigurationsopgaver, der skal udføres, når dataopgraderingen er fuldført. Alle disse opgaver skal dokumenteres og kvantificeres, og en ressource skal tildeles, fordi både den funktionelle arbejdsstrøm og den tekniske arbejdsstrøm skal indpasses i virksomhedens nedetidsgrænse.

I følgende illustration vises den overordnede proces for overgang til aktivering, som den sker i produktionsmiljøet.

![Overgangsproces](./media/cutover_1.png)

Denne overgangsproces adskiller sig fra en grundlæggende dataopgradering i et sandkassemiljø på følgende måder:

- AX 2012-databasen kopieres ikke, men bliver kun sikkerhedskopieret, og derefter ændres den oprindelige database. Denne metode er hurtigere, og sikkerhedskopien kan tilbageføres, hvis tilbageførslen er påkrævet.
- Da produktionsmiljøet for Finance and Operations har begrænset adgang, bliver de opgaver, der tidligere blev udført på sandkasseforekomsten af AOS (applikationsobjektserver), nu udført af Microsoft DSE-teamet. Disse opgaver omfatter download og import af filen bacpac og kørsel af pakken MajorversionDataUpgrade.zip.
- Vi har tilføjet følgende opgaver:

    - Udfør en røgtest.
    - Fuldfør konfigurationsopgaver for programmet. Dette trin kan være stort, afhængig af de funktioner, der bruges. I dette trin konfigurerer det funktionelle team nye programfunktioner, så de er klar til brug i det opgraderede system.
    - Tillad brugere igen. Fortæl din brugerbase, at opgraderingen er fuldført, og at de kan bruge systemet igen.

## <a name="technical-workstream"></a>Teknisk arbejdsstrøm

Den tekniske arbejdsstrøm involverer forskellige tekniske teammedlemmer: databaseadministratoren (DBA), AX 2012-systemadministratoren, serveradministratorer og udviklere, der er fortrolig med AX 2012 og Finance and Operations. Dette emne forklarer, hvilke opgaver der involverer hvilke roller.

Under overgangstesten har det tekniske team fokus på ydeevne og pålidelighedstest af dataopgraderingen for at sikre, at den overholder virksomhedens nedetidsgrænse. Mange elementer af hardware og software er involveret i denne proces. Nogle af disse elementer er lokale, mens andre er i Microsoft-skyen. Desuden er mange elementer i brugerdefineret programkode og standardkode involveret. Resultatet af denne test skal være tillid til overgangsprocessen for dit miljø.

### <a name="turn-off-the-ax-2012-aos-instances"></a>Deaktiver AX 2012 AOS-forekomsterne

Denne opgave involverer systemadministratoren for AX 2012 og serveradministratorer.

Der skal valideres følgende områder:

- **Batchjob, der kører på tidspunktet for overgangen** – Et langvarigt batchjob, der allerede er begyndt at køre, forhindrer systemet i at stoppe. Planlæg fremad, så du kan stoppe AOS-forekomster på det ønskede tidspunkt. Det være nødvendigt at planlægge batches, så de er fuldført nogen tid, før du kan deaktivere AX 2012.
- **Integrerede systemer** – Du har muligvis andre systemer, der er integreret med AX 2012-miljøet. I tidsplanen for at deaktivere AX 2012 skal du tage højde for disse systemer. Eksempelvis skal du muligvis deaktivere de integrerede systemer et stykke tid, før du kan deaktivere selve AX 2012, så alle resterende startede transaktioner kan fuldføres. Kravene til integrerede systemer varierer betydeligt fra virksomhed til virksomhed. Derfor skal dit team af eksperter planlægge dette scenarie uafhængigt af hinanden.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Opret en sikkerhedskopi af AX 2012-databasen

Dette involverer databaseadministratoren. Sikkerhedskopien vil blive brugt, hvis der kræves en tilbagerulning. Den bruges også som et referencepunkt, der opbevares i en periode, og viser computerens tilstand på tidspunktet for overgangen.

Der skal valideres følgende områder:

- Få konkret timing af sikkerhedskopieringen.
- Juster indstillinger for sikkerhedskopiering, der bruges (for eksempel komprimering sammenlignet med ikke-komprimering), for at sikre den hurtigst mulige sikkerhedskopiering.

### <a name="export-the-database-to-bacpac"></a>Eksportér databasen til bacpac

Dette involverer databaseadministratoren. Resultatet af denne opgave er eksportfilen, der vil blive overført til Microsoft Azure for det nye system.

Der skal valideres følgende områder:

- Få konkret timing af sikkerhedskopieringen.
- Optimer eksporten for at sikre den hurtigst mulige oplevelse. Optimering kan omfatte følgende opgaver:

    - Du kan måle systemressourcer under eksport, f.eks. CPU, disk-i/o og hukommelse.
    - Hvis der findes flaskehalse i ressourcerne, kan du oprette en plan for at løse dem. Normalt vil du afhjælpe disse flaskehalse ved at tildele flere af den nødvendige ressource.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Overfør bacpac-filen til lagring i Azure

Denne opgave involverer databaseadministratoren eller serveradministratorer. I denne opgave flyttes filen bacpac til Azure.

Der skal valideres følgende områder:

- Vælg den computer, der skal bruges til overførsel, og sørg for, at søgeværktøjet til Azure.datalageret er konfigureret og klar til brug.
- Få konkret timing af overførslen ved at måle den flere gange. Overførselstiden varierer afhængigt af hastigheden på forbindelsen til internettet og den geografiske beliggenhed af Azure-datacenteret i forhold til din adresse.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>Hent og importér filen bacpac til Azure SQL-databasen

Når denne opgave forekommer under udgivelsen, udføres den af Microsoft DSE-teamet. Under overgangstesten involverer den dog databaseadministratoren. Resultatet af denne opgave er eksportfilen, der vil blive overført til Azure for det nye system.

Der skal valideres følgende områder:

- Få konkret timing af importprocessen.
- Optimer eksporten for at sikre den hurtigst mulige oplevelse. Optimering kan omfatte følgende opgaver:

    - Mål systemressourcer under eksport. Her er nogle eksempler:

        - **På AOS-computeren:** CPU, disk-i/o og hukommelse
        - **På forekomsten af Azure SQL-databasen:** SQL-databasens gennemløb (DTU). Du kan overvåge Azure SQL DTU fra Microsoft SQL Server Management Studio på AOS-computeren ved at kigge på systemvisningen sys.dm_resource_stats.

    - Hvis der findes flaskehalse i ressourcerne, kan du oprette en plan for at løse dem. Normalt vil du afhjælpe disse flaskehalse ved at tildele flere af den nødvendige ressource. Da denne computer har Microsoft som vært, skal du sende en anmodning til Microsoft om at øge ressourcer, hvis du identificerer, at de er en flaskehals.

### <a name="run-the-majorversiondataupgradezip-package"></a>Kør pakken MajorVersiondataUpgrade.zip

Når denne opgave forekommer under udgivelsen, udføres den af Microsoft DSE-teamet. Under overgangstesten involverer den dog udviklerne. I denne opgave konverteres den gamle databasestruktur til strukturen i det nye system.

Processen til databasesynkronisering kører som en del af denne opgave. Databasesynkronisering kan tage lang tid i nogle situationer, f.eks. når et grupperet indeks er ændret på en tabel, fordi denne handling er krævende i SQL.

Vi anbefaler, at du først udfører din analyse og fejlfindingsprocessen i et udviklingsmiljø. I et sandkassemiljø er fejlfindings- og analysemulighederne mere begrænset. Målet er at have få eller ingen af de problemer, der skal løses, når du foretager test af overgang.

Der skal valideres følgende områder:

- Få konkret timing af importprocessen.
- Optimer processen for at sikre den hurtigst mulige oplevelse. Optimering kan omfatte følgende opgaver:

    - Overvåg ydeevnen af individuelle opgraderingsscripts gennem tabellen ReleaseUpdateScriptsExecution.
    - Juster scripts for at optimere ydeevnen. Denne opgave kræver muligvis, at du tilpasser et scripts X++-kode for at optimere den til dit datasæt.
    - Overvåg Azure SQL DTU ved hjælp af Microsoft Dynamics Lifecycle Services (LCS) eller systemvisningen sys.dm_resources_stats i Management Studio. Hvis ressourcer er udnyttet maksimalt, skal du muligvis anmode om et højere databaseniveau fra Microsoft DSE-teamet.

### <a name="roll-back-to-ax-2012"></a>Tilbagefør til AX 2012

Formålet med denne opgave er at gendanne databasen ved hjælp af den sikkerhedskopi, der blev foretaget, da AX 2012 blev slået fra, og derefter aktivere AX 2012 igen. Tilstanden for integrerede systemer skal muligvis også gendannes. Men da integrerede systemer varierer fra virksomhed til virksomhed, skal du planlægge dette scenarie uafhængigt, baseret på dine særlige omstændigheder. Selvom det er usandsynligt, at du skal tilbageføre, er det vigtigt, at du har en proces, der er testet, hvis du får brug for den.

## <a name="functional-workstream"></a>Funktionel arbejdsstrøm

Efter dataopgraderingen kræves flere konfigurationsopgaver i det nye miljø. Formålet med denne arbejdsstrøm er at dokumentere og kvantificere alle konfigurationsopgaver og tildele hver opgave en ressource for at sikre, at disse opgaver kan udføres sammen med den tekniske arbejdsstrøm under nedetiden.

Funktionelle opgaver omfatter typisk ændring af værdierne for specifikke systemparametre eller andre konfigurationsdata. Disse opgaver identificeres via det fuldt funktionelle testgennemløb, som er en anden aktivitet end overgangstesten. Når en opgave af denne type er identificeret, skal den gennemgås sammen med den funktionelle ressource og udvikleren.

Større ændringer kan kræve, at der skrives et nyt tilpasset script til dataopdatering under dataopgraderingen. Den funktionelle ressource kan dog manuelt køre mindre ændringer via det nye system efter opgradering af data.

Større ændringer, der har nye dataopgraderingsscripts, skal testes. Derfor skal en eller flere yderligere gentagelser af pakken MajorVersionDataUpgrade.zip køres. Det er vigtigt, at du opvejer omkostningen ved at køre pakken igen i forhold til omkostningen ved manuel indtastning af data.

For hver manuelle ændring skal der tilføjes en opgave i planlægningsdokumentet for overgang. Denne opgave skal vise følgende oplysninger:

-   Hvad er opgaven, og hvad skal gøres?
-   Hvem skal gøre det?
-   Hvor lang tid tager det?

