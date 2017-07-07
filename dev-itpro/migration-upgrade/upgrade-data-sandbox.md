---
title: "Opgradering af data i et sandkassemiljø"
description: "Dette emne forklarer, hvordan du udfører en opgradering af data fra AX 2012 til Dynamics 365 for Finance and Operations i et sandkassemiljø."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
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
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: da-dk
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Opgradering af data i et sandkassemiljø

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Resultatet af denne opgave er en opgraderet database, du kan bruge i et sandkassemiljø. Et sandkassemiljø er et miljø, hvor forretningsbrugere og funktionelle teammedlemmer kan validere programmets funktionalitet. Disse funktioner omfatter tilpasninger og de data, der blev overført fra Microsoft Dynamics AX 2012.

Vi anbefaler, at du kører processen til opgradering af data i et udviklingsmiljø, før du kører den i et delt sandkassemiljø, da denne metode hjælper med at reducere den samlede tid, der kræves til en opgradering af data, der lykkes. Yderligere oplysninger finder du i [Dataopgradering i et udviklingsmiljø](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Oversigt over opgraderingsprocessen for sandkassedata

Før du begynder at opgradere dataene i et sandkassemiljø, har du allerede opgraderede data i et udviklingsmiljø, som beskrevet i [Dataopgradering i et udviklingsmiljø](prepare-data-upgrade.md). De to processer er næsten ens. Den væsentligste forskel er, at et sandkassemiljø bruger Microsoft Azure SQL-databasen til lagring af data, mens et udviklingsmiljø bruger Microsoft SQL Server. Denne tekniske forskel i databaselaget kræver, at du redigerer proceduren for dataopgraderingen lidt i et sandkassemiljø, da en sikkerhedskopi fra AX 2012-databaseforekomsten ikke kan gendannes i SQL-databasen.

![Opgraderingsproces for sandkassedata](./media/data-upgrade-sandbox.png)

Her er de overordnede trin i opgraderingsprocessen.

1. Opret en kopi af AX 2012-databasen. Det anbefales kraftigt, at du bruger en kopi, da du skal slette nogle objekter i den kopi, der skal eksporteres.
2. Eksportér den kopierede database til en bacpac-fil ved hjælp af et gratis værktøj til SQL Server, der hedder SQLPackage.exe. Dette værktøj indeholder en særlig type sikkerhedskopi af databasen, der kan importeres til SQL-databasen.
3. Overfør bacpac-filen til lagring i Azure.
4. Hent filen bacpac til AOS-computeren (applikationsobjektserver) i sandkassemiljøet, og importér den derefter ved hjælp af SQLPackage.exe. Derefter skal du køre et script i den importerede database for at nulstille SQL-databasebrugere.
5. Kør pakken MajorVersionDataUpgrade.zip for at køre dataopgraderingen i databasen, der er importeret.

## <a name="create-a-copy-of-the-ax-2012-database"></a>Opret en kopi af AX 2012-databasen

Du skal oprette en kopi af AX 2012-databasen, du opgraderer, fordi du skal slette nogle objekter fra databasen. Disse objekter omfatter alle brugere med Microsoft Windows-godkendelse. Disse ændringer gør den ændrede database ubrugelig for AX 2012. I dette trin opretter du en kopi af databasen og sletter disse objekter.

Dette trin skal udføres af databaseadministratoren (DBA) eller en person, der har lignende viden og erfaring.

Du kan oprette en databasekopi ved at tage en sikkerhedskopi af den oprindelige database og gendanne den under et nyt navn. Sørg for, at der er ledig plads til begge databaser. Du kan oprette kopien på en anden server. Versionen af SQL Server-forekomsten, der kører databasen, er ikke vigtig.

Her er et eksempel på den kode, der opretter en databasekopi. Du skal redigere dette eksempel, så det afspejler dine specifikke databasenavne.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Når kopien er oprettet, kan du køre følgende script i Transact-SQL (T-SQL) mod den.
TODO 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Eksportere den kopierede database til en bacpac-fil

Eksportér den kopierede database til en bacpac-fil ved hjælp værktøjet SQLPackage.exe. Dette trin skal udføres af databaseadministratoren eller et teammedlem, som har tilsvarende kendskab.

Det er meget vigtigt, at du installerer den nyeste version af SQL Server Management Studio, før du starter dette trin. Selvom SQLPackage findes i tidligere versioner af Management Studio, fungerer den ikke korrekt for dette trin, medmindre du først installerer den nyeste version.

Dette trin er vigtigt, fordi eksporten skal ske igen under nedetiden inden udgivelsen. Her er nogle tip:

- Processen bacpac er meget input/output- og CPU-krævende. Derfor skal du køre eksporten på en kraftig maskine.
- SQLPackage skal køres lokalt på den computer, der er vært for databasen. SQLPackage må ikke køres på en lokal bærbar computer, som du forbinder med databasecomputeren, fordi denne proces også er netværkskrævende.

Åbn derefter vinduet **Kommandoprompt** som administrator, og kør følgende kommandoer.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Her er en forklaring på parametrene:

- **ssn** (kildeservernavnet) – Navnet på den SQL Server, der skal eksporteres fra. For vores proces skal denne parameter altid angives til **localhost**.
- **sdn** (kildedatabasenavn) – Navnet på databasen, der skal eksporteres.
- **tf** (destinationsfil) – Stien til og navnet på den fil, der skal eksporteres til. Mappen skal eksistere i forvejen, men filen oprettes af processen.
- **/p:CommandTimeout** – Timeoutværdien pr. forespørgsel. Denne parameter giver mulighed for, at større tabeller eksporteres uden at nå timeout.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Overfør bacpac-filen til lagring i Azure

Overfør din bacpac-fil til lagring i Azure. Se UsingStorageExplorer.docx TODO

### <a name="import-the-bacpac-file-into-sql-database"></a>Importér bacpac-filen til SQL-databasen

Under dette trin importerer du den eksporterede bacpac-fil til den forekomst af SQL-databasen, der bruges i dit sandkassemiljø. Du skal først installere den nyeste version af Management Studio på din AOS-sandkassecomputer. Du skal derefter importere filen ved hjælp af værktøjet SQLPackage.exe.

Du skal udføre disse opgaver direkte på AOS-computeren i dit sandkassemiljø, da der er firewallregler, der begrænser adgang til forekomsten af SQL-databasen. Ved hjælp af AOS-computeren kan du dog få adgang.

Du skal have den nyeste version af Management Studio, før du starter importen, ligesom ved eksporttrin. Dette trin virker ikke, hvis du har en ældre version.

Af hensyn til ydeevnen anbefales det, at du anbringer filen bacpac på drev D på AOS-computeren. På virtuelle Azure-maskiner er drev D en fysisk disk, der typisk har højere ydeevne end andre tilgængelige diske.

Åbn vinduet **Kommandoprompt** som administrator, og kør følgende kommandoer.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Her er en forklaring på parametrene:

- **tsn** (målservernavn) – Navnet på den SQL Azure-server, du skal importere til. Navnet findes i LCS. Giv det suffikset **. database.windows.net**.
- **tdn** (måldatabasenavn) – Navnet på databasen, der skal importeres til. Databasen må ikke allerede findes. Importprocessen opretter den.
- **sf** (kildefil) – Stien til og navnet på den fil, der skal importeres fra.
- **tp** (måladgangskode) – SQL adgangskoden for destinationsforekomsten af SQL-databasen.
- **tu** (målbruger) – SQL-brugernavnet for destinationsforekomsten af SQL-databasen. Vi anbefaler, at du bruger **sqladmin**. Du kan hente denne brugers adgangskode fra LCS-projektet.
- **/p:CommandTimeout** – Timeoutværdien pr. forespørgsel. Denne parameter giver mulighed for, at større tabeller eksporteres uden at nå timeout.
- **/p:DatabaseServiceObjective** – Serviceniveauet på den database, der oprettes. Du kan undersøge værdien for den eksisterende database ved hjælp af Management Studio. Højreklik på databasen, og vælg derefter **Egenskaber**.

Når du har kørt kommandoerne, modtager du følgende advarsel. Du kan blot ignorere den.

![Sandkassefejl](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Kør pakken MajorVersionDataUpgrade.zip

Kør datapakken med opgradering, der kan installeres som beskrevet i [Opgradere data i udviklings-, demonstrations- eller sandkassemiljøer](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Opgrader en kopi af databasen i et udviklingsmiljø

Det er nyttigt at opgradere den samme database i et udviklingsmiljø. Hvis du har en kopi af databasen, der er tilgængelig for udviklingsmiljøer, bliver det meget lettere at undersøge fejl, der findes i det opgraderede sandkassemiljø.

