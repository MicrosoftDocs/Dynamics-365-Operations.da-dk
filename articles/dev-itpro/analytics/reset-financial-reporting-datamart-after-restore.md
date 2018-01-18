---
title: "Nulstille datacenteret Økonomirapportering"
description: "Dette emne beskriver, hvordan du nulstiller datacenteret Økonomirapportering."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Nulstille datacenteret Økonomirapportering

[!include[banner](../includes/banner.md)]

I dette emne forklares, hvordan du nulstiller datacenteret Økonomirapportering for følgende versioner:

- Version 7.2.6.0 og nyere versioner af Økonomirapportering til Microsoft Dynamics 365 for Finance and Operations
- Version 7.0.10000.4 og nyere versioner af Økonomirapportering til Microsoft Dynamics 365 for Finance and Operations
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (lokal installation)

Hvis du vil have Økonomirapportering version 7.2.6.0 til Finance and Operations, kan du hente KB 4052514 fra <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Nulstille datacenteret Økonomirapportering for version 7.2.6.0 og nyere versioner af Økonomirapportering til Finance and Operations

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Nulstille datacenteret Økonomirapportering fra Rapportdesigner

> [!NOTE]
> Trinnene i denne proces understøttes i version 7.2.6.0 og nyere versioner af Økonomirapportering til Finance and Operations. Hvis du har en tidligere version, kan du kontakte supportteamet for at få hjælp.

Du skal muligvis nulstille datacenteret for økonomirapportering i bestemte scenarier. Du kan udføre denne opgave i Rapportdesigner-klienten. Her er nogle scenarier, hvor du muligvis skal nulstille datacenteret:

- Finance and Operations-databasen blev gendannet, men databasen for datacenteret blev ikke gendannet.
- Der vises forkerte data for en periode.
- Support råder dig til at nulstille datacenteret som en del af et fejlfindingstrin.

Nulstillingen af datacenteret bør kun udføres på tidspunkter, hvor mængden af data, der behandles i databasen, er lille. Økonomirapportering er ikke tilgængelig i forbindelse med nulstilling.

#### <a name="reset-the-data-mart"></a>Nulstil datacenteret

Når du vil nulstille datacenteret, skal du i menuen **Værktøjer** i Rapportdesigner vælge **Nulstil datacenter**. Den viste dialogboks har to sektioner: **Statistik** og **Nulstil**.

[![Dialogboksen Nulstil datacenter](./media/Reset-72.jpg)](./media/Reset-72.jpg)

##### <a name="integration-attempts"></a>Integrationsforsøg

Gitteret **Integrationsforsøg** viser, hvor mange gange systemet har forsøgt at integrere posteringer. Systemet fortsætter med at forsøge at integrere data i en periode på flere dage, hvis de første forsøg ikke lykkes. Du ved, at datacenteret skal nulstilles, hvis antallet af forsøg er 8 eller derover, og hvis der er mange dimensionskombinations- eller transaktionsposter. I så fald skal der ikke rapporteres om dataene.

##### <a name="data-status"></a>Datastatus

Gitteret **Datastatus** indeholder et øjebliksbillede af transaktionerne, kurserne og dimensionsværdierne i datacenteret. Et stort antal forældede poster angiver, at der er foretaget mange opdateringer af posterne. Det kan medføre længere rapportgenereringstider.

##### <a name="misaligned-main-account-categories"></a>Hovedkontokategorier, der ikke er justeret korrekt

Hvis du bruger en version, der er ældre end Økonomirapportering version 7.2.1 til Microsoft Dynamics 365 for Finance and Operations, kan du muligvis nulstille datacenteret, hvis du omdøber konti og flytter konti fra en kontokategori til en anden. Disse handlinger kan medføre, at hovedkontokategorier bliver justeret forkert. Feltet **Hovedkontokategorier, der ikke er justeret korrekt** viser, om du oplever dette problem.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Nulstille datacenteret i Økonomirapportering version 7.2.6.0 til Finance and Operations

Hvis du vil nulstille datacenteret i version 7.2.6.0 og tidligere versioner af Økonomirapportering til Finance and Operations, skal du i dialogboksen **Nulstil datacenter** markere afkrydsningsfeltet **Nulstil datacenter** og derefter vælger **OK**. Nulstil kun datacenteret under planlagt nedetid.

[![Afkrydsningsfeltet Nulstil datacenter](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Nulstil datacenteret, og vælg en årsag i Økonomirapportering version 7.3.0 til Microsoft Dynamics 365 for Finance and Operations

Hvis du konstaterer, at der kræves en nulstilling af datacenteret, kan du markere afkrydsningsfeltet **Nulstil datacenter** og derefter vælge en årsag i feltet **Årsag**. Følgende valgmuligheder er tilgængelige:

- **Manglende eller forkerte data** – Baseret på statistikken, har du konstateret, at der sandsynligvis mangler data. Før du fortsætter, anbefaler vi, at du samarbejder med Support om at bestemme den egentlige årsag.
- **Gendan database** – Finance and Operations-databasen blev gendannet, men databasen for datacenteret Økonomirapportering blev ikke gendannet.
- **Andet** – Du er ved at nulstille datacenteret af anden årsag. Hvis du mener, at der er et problem, kan du kontakte Support for at identificere det.

[![Nulstil datacenter](./media/Integration.png)](./media/Integration.png)

> [!NOTE]
> Kontroller, at alle opgaver i datacenteret har fuldført en oprindelige belastning, før du starter en nulstilling. Du kan kontrollere dette ved at søge efter en værdi i kolonnen Tidspunkt for seneste kørsel ved at vælge **Værktøjer** &gt; **Integrationsstatus**.

#### <a name="clear-users-and-companies"></a>Ryd brugere og firmaer

Marker afkrydsningsfeltet **Ryd brugere og firmaer**, hvis du har gendannet databasen, men derefter har foretaget ændringer af brugere eller virksomheder. Det skulle ikke være nødvendigt at markere dette afkrydsningsfelt ofte.

Når du er klar til at starte nulstillingsprocessen, skal du vælge **OK**. Du bliver bedt om at bekræfte, at du er klar til at starte processen. Bemærk, at Økonomirapportering ikke er tilgængelig under nulstillingen og den indledende dataintegration, der foretages bagefter.

Hvis du vil kontrollere status for integrationen, skal du vælge **Værktøjer** &gt; **Integrationsstatus** at se sidst integrationen blev kørt og status.

[![Få vist status for integrationen](./media/New-integration.PNG)](./media/New-integration.PNG)

> [!NOTE]
> Nulstillingen er afsluttet, når alle tilknytninger viser status for RanToCompletion, og der i vinduet Integrationsstatus står "Integration fuldført" i nederste venstre hjørne.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Nulstille datacenteret Økonomirapportering version 7.0.10000.4 og nyere versioner af Økonomirapportering til Finance and Operations

Hvis du på et tidspunkt vil gendanne din Finance and Operations-database fra en sikkerhedskopi eller kopiere databasen fra et andet miljø, skal du følge trinnene i dette afsnit for at prøve at sikre, at datacenteret Økonomirapportering bruger den gendannede Finance and Operations-database korrekt.

> [!NOTE]
> Trinene i processen understøttes for Microsoft Dynamics AX-programversion 7.0.1 (maj 2016) (programbuild 7.0.1265.23014 og Økonomirapportering build 7.0.10000.4) og nyere versioner. Hvis du har en tidligere version af Finance and Operations, skal du kontakte vores Support for at få hjælp.

### <a name="export-report-definitions"></a>Eksporter rapportdefinitioner

Følg først disse trin for at eksportere dine rapportdesign fra Rapportdesigneren.

1. I Reportdesigner skal du vælge **Regnskab** &gt; **Rapportkomponentgrupper**.
2. Vælg den rapportkomponentgruppe, der skal eksporteres, og vælg derefter **Eksportér**.

    > [!NOTE]
    > Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.

3. Vælg de rapportdefinitioner, der skal eksporteres:

    - Hvis du vil eksportere alle dine rapportdefinitioner og de tilknyttede rapportkomponenter, skal du vælge **Markér alt**.
    - Hvis du vil eksportere bestemte rapporter, rækker, kolonner, træer eller dimensionsopsætninger, skal du vælge den relevante fane og derefter vælge de elementer, der skal eksporteres. Tryk på og hold Ctrl-tasten nede for at vælge flere elementer under en fane. Når du vælger rapporter til eksport, vælges de tilknyttede rækker, kolonner, træer og dimensionsopsætninger.

4. Vælg **Eksportér**.
5. Angiv et filnavn, og vælg et sikkert sted, hvor du vil gemme de eksporterede rapportdefinitioner.
6. Vælg **Gem**.

Du kan kopiere eller overføre filen til et sikkert sted. På denne måde kan filen importeres til et andet miljø senere. Du kan finde oplysninger om, hvordan du bruger en Microsoft Azure-lagerkonto, i [Overfør data med AzCopy-kommandolinjeværktøjet](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Microsoft leverer ikke en lagerkonto som en del af din Finance and Operations-aftale. Du skal købe en lagerkonto eller bruge en lagerkonto fra et separat Azure-abonnement.

> [!WARNING]
> Vær opmærksom på funktionen af D-drevet på virtuelle Azure-maskiner (VM'er). Gem ikke permanent dine eksporterede rapportkomponentgrupper på drev D. Du kan finde flere oplysninger om midlertidige drev i [Om de midlertidige drev på virtuelle Windows Azure-maskiner](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Stop tjenester

Følgende Microsoft Windows-tjenester har åbne forbindelser til Finance and Operations-databasen. Derfor skal du bruge Microsoft Fjernskrivebord til at oprette forbindelse til alle computere i miljøet og derefter bruge services.msc til at stoppe disse tjenester.

- Tjenesten World Wide Web Publishing (på alle AOS-computere [Applikationsobjektservere])
- Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)
- Tjenesten Management Reporter 2012 Process (kun på Business Intelligence-computere [BI])

### <a name="reset"></a>Nulstil

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Download den nyeste MinorVersionDataUpgrade.zip-pakke

Download den nyeste MinorVersionDataUpgrade.zip-pakke. Du kan finde oplysninger om, hvordan du finder og henter den korrekte version af dataopgraderingspakken, under [Hent den nyeste installerbare dataopgraderingspakke](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). 

Der kræves ikke en opgradering for at hente pakken MinorVersionDataUpgrade.zip. Derfor skal du bare følge trinnene i afsnittet "Hent den nyeste installerbare dataopgraderingspakke" i det pågældende emne. Du kan springe alle de andre trin i emnet over.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Køre scripts mod Finance and Operations-databasen

Kør følgende scripts mod Finance and Operations-databasen (ikke mod Økonomirapportering-databasen):

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Disse scripts er med til at sikre, at brugerne, rollerne og indstillingerne for sporing af ændringer er korrekte.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Køre en Windows PowerShell-kommando for at nulstille databasen

På AOS-computeren skal du starte Microsoft Windows PowerShell som administrator og udføre følgende kommandoer for at nulstille integrationen mellem Finance and Operations og Økonomirapportering.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Her er en forklaring på parametrene i kommandoen **Reset-DatamartIntegration**:

- De gyldige værdier for **-Reason** er: **SERVICING**, **BADDATA** og **OTHER**.
- Parameteren **-ReasonDetail** er fri tekst.
- Årsagen og detaljer om årsagen registreres i telemetri/miljøovervågningen.

> [!NOTE]
> Når du har kørt kommandoerne, bliver du bedt om at angive **Y** for at bekræfte, at du vil nulstille databasen.

#### <a name="restart-services"></a>Genstart tjenester

Brug services.msc til at genstarte de tjenester, som du tidligere har stoppet:

- Tjenesten World Wide Web Publishing (på alle AOS-computere)
- Tjenesten Microsoft Dynamics 365 for Finance and Operations Batch Management (kun på ikke-private AOS-computere)
- Tjenesten Management Reporter 2012 Process (kun på BI-computere)

#### <a name="import-report-definitions"></a>Importer rapportdefinitioner

Importer dine rapportdesigns fra Reportdesigner ved hjælp af den fil, der blev oprettet under eksporten.

1. I Reportdesigner skal du vælge **Regnskab** &gt; **Rapportkomponentgrupper**.
2. Vælg den rapportkomponentgruppe, der skal eksporteres, og vælg derefter **Eksportér**.

    > [!NOTE]
    > Bemærk: I Finance and Operations understøttes kun én komponentgruppe, **Standard**.

3. Vælg komponenten **Standard**, og vælg derefter **Importer**.
4. Vælg den fil, der indeholder de eksporterede rapportdefinitioner, og vælg derefter **Åbn**.
5. Vælg de rapportdefinitioner, der skal importeres, i dialogboksen **Importér**:

    - Hvis du vil importere alle rapportdefinitionerne og de tilknyttede rapportkomponenter, skal du vælge **Markér alt**.
    - Hvis du vil importere bestemte rapporter, rækker, kolonner, træer eller dimensionsgrupper, skal du markere de rapporter, rækker, kolonner, træer eller dimensionsgrupper, der skal importeres.

6. Vælg **Importér**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Nulstille datacenteret Økonomirapportering til Finance and Operations (til det lokale miljø)

1. Bed alle brugere om at afslutte Reportdesigner og området Økonomirapportering i Finance and Operations.
2. Kør følgende script mod Økonomirapportering-databasen (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Afkort eller slet alle poster fra tabellen FINANCIALREPORTS i Finance and Operations-databasen (AXDB).
4. Afkort eller slet alle poster fra tabellen FINANCIALREPORTVERSION, hvis denne tabel finde i Finance and Operations-databasen. Hvis tabellen ikke findes i Finance and Operations-databasen, kan du springe dette trin over.
5. Kør scriptet **ResetDatamart.sql** mod Økonomirapportering-databasen. Dette script deaktiverer datacenterintegrationen, sletter alle data i datacenteret og genaktiverer derefter datacenterets dataintegration.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Efter nulstillingen kan du manuelt kontrollere genindlæsningen af dataene ved at køre følgende forespørgsel mod Økonomirapportering-databasen.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Bekræft, at alle rækker har en **LastRunTime**-værdi, og at **StateType** er indstillet til **5**. En **StateType**-værdi på **5** angiver, at dataene blev genindlæst korrekt. En værdi på **7** angiver en fejltilstand. Nogle gange har tilknytningen af organisationshierarkiet denne tilstand ved første kørsel. Dog skulle fejltilstanden blive afhjulpet automatisk.

