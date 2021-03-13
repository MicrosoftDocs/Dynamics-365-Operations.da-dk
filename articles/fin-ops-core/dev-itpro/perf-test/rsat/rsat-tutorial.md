---
title: Selvstudium til Regression Suite Automation Tool
description: I dette emne vises, hvordan du kan bruge værktøjet RSAT (Regression Suite Automation Tool). Det beskriver forskellige funktioner og indeholder eksempler, der bruger avanceret scripting.
author: robinarh
manager: AnnBe
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c4c0f9340085341ab60f97b55dacf36624e5f46
ms.sourcegitcommit: b337b647a1be4908fc361fb6d962e96a69f301a9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2021
ms.locfileid: "5036701"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Selvstudium til Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format.

Dette selvstudium gennemgår nogle af de avancerede funktioner i RSAT (Regression suite automation tool), herunder en demoopgave og beskriver strategi og centrale undervisningspunkter.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Vigtige funktioner i RSAT og Arbejdsrutineoptager

### <a name="validate-a-field-value"></a>Valider en feltværdi

RSAT giver dig mulighed for at medtage valideringstrin i din test case for at validere forventede værdier. Du kan få flere oplysninger om denne funktion i artiklen [Validere forventede værdier](rsat-validate-expected.md).

I følgende eksempel vises, hvordan du kan bruge denne funktion til at validere, om den disponible lagerbeholdning er større end 0 (nul).

1. I demodataene i **USMF**-firmaet skal du oprette en opgaveregistrering, der indeholder følgende trin:

    1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
    2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter en værdi på **1000** for feltet **Varenummer**.
    3. Vælg **Disponibel lagerbeholdning**.
    4. Brug Quick Filter til at finde poster. Du kan f.eks. filtrere efter værdien **1** for feltet **Lokation**.
    5. Markér den valgte række på listen.
    6. Kontroller, at værdien af feltet **I alt disponibelt** er **411,0000000000000000**.

2. Gem opgaveregistreringen som en **udviklerregistrering**, og knyt den til test casen i Azure Devops.
3. Føj testsagen til testplanen, og Indlæs testsagen i RSAT.
4. Åbn Excel-parameterfilen, og gå til fanen **TestCaseSteps**.
5. Hvis du vil kontrollere, om den disponible lagerbeholdning altid er større end **0**, skal du gå til trinnet **Valider I alt disponibelt** og ændre værdien fra **411** til **0**. Rediger værdien i feltet **Operator** fra et lighedstegn (**=**) til et større end-tegn (**\>**).
6. Gem og luk Excel-parameterfilen.
7. Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen Azure DevOps.

Hvis værdien af feltet **I alt disponibelt** for den angivne vare på lageret er større end 0 (nul), vil testene bestå, uanset den faktiske værdi for disponibel lagerbeholdning.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Gemte variabler og sammenkædning af test cases

En af nøglefunktionerne i RSAT er sammenkædning af test cases, dvs. en test kan overføre værdier til andre test. Du kan få flere oplysninger i artiklen [Kopiere variabler til sammenkædede test cases](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Afledt testsag

RSAT giver dig mulighed for at bruge den samme opgaveregistrering i flere test cases, hvilket gør det muligt at køre en opgave med forskellige datakonfigurationer. Du kan finde flere oplysninger i artiklen [Afledte test cases](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Validere beskeder og meddelelser

Denne funktion kan bruges til at validere, om der opstod en handling. Når der f.eks. oprettes, estimeres og derefter startes en produktionsordre, viser appen meddelelsen "Produktion – start" for at give dig besked om, at produktionsordren er startet.

![Beskeden Produktion – start](./media/use_rsa_tool_05.png)

Du kan validere denne meddelelse via RSAT ved at angive meddelelsesteksten under fanen **Meddelelsesvalidering** i Excel-parameterfilen for den relevante registrering.

![Fanen Meddelelsesvalidering](./media/use_rsa_tool_06.png)

Når testsagen er kørt, sammenlignes meddelelsen i Excel-parameterfilen med den viste meddelelse. Hvis meddelelserne ikke stemmer overens, vil testsagen mislykkes.

> [!NOTE]
> Du kan angive mere end én meddelelse under fanen **Meddelelsesvalidering** i Excel-parameterfilen. Meddelelserne kan også være fejl- eller advarselsmeddelelser i stedet for orienterende meddelelser.

### <a name="snapshot"></a>Øjebliksbillede

Denne funktion bruger skærmbilleder af de trin, der blev udført under opgaveregistreringen. Det er nyttigt i forbindelse med overvågning eller fejlfinding.

- Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og ændre værdien af det følgende element fra **falsk** til **sand**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Når du kører test casen, vil RSAT generere snapshots (billeder) af trinnene i afspilningsmappen i test cases i arbejdsbiblioteket. Hvis du bruger en ældre version af RSAT, gemmes billederne i **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, og der oprettes en separat mappe for hver testsag, der køres.

## <a name="assignment"></a>Tilknytning

### <a name="scenario"></a>Scenario

1. Produktdesigneren opretter et nyt, frigivet produkt.
2. Produktionschefen starter en produktionsordre for at bringe lagerniveauet op til to styk.
3. Produktionen starter og afslutter produktionsordren og kontrollerer, at det disponible antal er to styk.
4. Salgsteamet modtager en ordre på fire stykker af det nye produkt. Salgsgruppen opdaterer derfor nettokravene via den dynamiske plan. Da der ikke er mere tilgængelig kapacitet, er standardordrepolitikken indstillet til "køb i stedet for at fremstille". Derfor oprettes der et salgsforslag.
5. Køberen tilføjer en kreditor, autoriserer indkøbsordreforslaget og bekræfter derefter indkøbsordren.
6. Når de købte varer ankommer til butikken, søger butiksoperatøren efter den relaterede indkøbsordre og modtager varerne. Da ordren nu er fuldført, kan varer plukkes og pakkes i forhold til salgsordren.
7. Finans bogfører købsfakturaen og salgsfakturaen.

I følgende illustration vises flowet i dette scenarie.

![Flow for demoscenariet](./media/use_rsa_tool_14.png)

I følgende illustration vises hierarkiet af forretningsprocesserne for dette scenario i LCS Forretningsmodeldesigner.

![Forretningsprocesser til demoscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategi – vigtig læring

### <a name="data"></a>Data

- Sørg for, at du har repræsentative datamængder (en kopi af produktion/gyldne konfigurationsdata plus overførte data).
- Når du genererer nye data via en opgaveregistrering, skal du oprette testnavne, der ikke er i konflikt med eksisterende navne (brug f.eks. et præfisk såsom **RSATxxx**).
- Brug Azures funktion til genoprettelse af et bestemt tidspunkt for at køre test i miljøjer, der ikke er niveau 1, igen.
- Selvom du kan bruge Excel-funktionerne **VILKÅRLIG** og **NU** til at generere en entydig kombination, kræver det ret meget arbejde. Her er et eksempel.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Arbejdsrutineoptager

- Definer scenarierne, før du går i gang med at registrere. Et godt styret projekt har foruddefinerede testscenarier. Hvis du vil oprette en testsag, skal du overveje, hvor forudsigelige udfaldet af disse testsituationer er.
- Opdel registreringer, hvis de udføres af forskellige roller, eller hvis der er ventetiden eller en ekstern hændelse før næste trin.
- Undgå at vælge værdier på lister. Brug i stedet tekstformater som f.eks **FIFO**, **AudioRM** og **SiteWH**. Når du vælger på en liste, registreres placeringen af værdien på listen, ikke selve værdien. Hvis der føjes varer til listen, kan placeringen af værdien ændres. Derfor vil din registrering bruge en anden parameter, og resten af scenariet kan blive påvirket.
- Tænk over funktionsmåde for flere brugere. Antag f. eks. ikke, at din nyoprettede salgsordre altid skal vælges automatisk. Brug i stedet for altid filteret til at finde den rigtige rækkefølge.
- Brug funktionen Kopier i Opgaveregistrering til at gemme navnet på et nyoprettet produkt, så det kan bruges i sammenkædede testsager.
- Brug funktionen Valider i Opgaveregistrering til at angive kontrolpunkter, der bekræftet, at trinnene er blevet kørt korrekt.

### <a name="rsat"></a>RSAT

- Hvis du vil køre testen i et andet firma, kan du ændre firmaet under fanen **Generelt** i Excel-parameterfilen. Sørg for, at indstillinger og data er tilgængelige i netop det valgte firma.
- Du kan ændre testbrugeren under fanen **Generelt** i Excel-parameterfilen. Angiv e-mail-id'et for den bruger, der skal køre testsagen. På denne måde kan testsagen køres ved hjælp af sikkerhedstilladelserne for den angivne bruger.
- Hvis du vil vente, før testen startes, kan du definere en pause under fanen **Generelt** i Excel-parameterfilen. Denne pause kan bruges i et batchjob (f. eks. hvis en arbejdsgang skal køres, før næste trin kan udføres).

## <a name="advanced-scripting"></a>Avanceret scripting

### <a name="cli"></a>CLI

RSAT kan kaldes fra et **Kommandoprompt**- eller **PowerShell**-vindue.

> [!NOTE]
> Kontroller, at **TestRoot**-miljøvariablen er indstillet til RSAT-installationsstien. (Gå til Microsoft Windows, åbn **Kontrolpanel**, vælg **System og sikkerhed \> System \> Avancerede systemindstillinger**, og vælg derefter **Miljøvariabler**.)

1. Åbn et **Kommandoprompt**- eller **PowerShell**-vindue som administrator.
2. Naviger til RSAT-installationsmappen.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Vis alle kommandoer.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Viser hjælp om alle tilgængelige kommandoer og deres parametre.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valgfri parametre

`command`: Hvor ``[command]`` er en af de kommandoer, der er angivet nedenfor.

#### <a name="about"></a>om

Viser den aktuelle version.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Rydder skærmen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>hent

Downloader vedhæftede filer for den angivne testcase til outputmappen.
Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>download: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.
+ `output_dir`: Repræsenterer outputmappen. Biblioteket skal eksistere.

##### <a name="download-examples"></a>download: eksempler

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>rediger

Giver dig mulighed for at åbne parameterfilen i Excel-programmet og redigere den.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: påkrævede parametre

+ `excel_file`: Skal indeholde en fuldstændig sti til en eksisterende Excel-fil.

##### <a name="edit-examples"></a>edit: eksempler

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Opretter testkørsels- og -parameterfiler for det angivne testcase i outputmappen. Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.
+ `output_dir`: Repræsenterer outputmappen. Biblioteket skal eksistere.

##### <a name="generate-examples"></a>generate: eksempler

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

Genererer en ny testcase, der er afledt fra den leverede testcase. Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: påkrævede parametre

+ `parent_test_case_id`: Repræsenterer det overordnede testcase-id.
+ `test_plan_id`: Repræsenterer testplan-id'et.
+ `test_suite_id`: Repræsenterer testpakke-id'et.

##### <a name="generatederived-examples"></a>generatederived: eksempler

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Opretter kun testkørselsfilen for det angivne testcase i outputmappen. Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.
+ `output_dir`: Repræsenterer outputmappen. Biblioteket skal eksistere.

##### <a name="generatetestonly-examples"></a>generatetestonly: eksempler

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Opretter alle testcases for den angivne pakke i outputmappen. Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige testpakker. Brug en vilkårlig værdi fra første kolonne som en **test_suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: påkrævede parametre

+ `test_suite_name`: Repræsenterer testpakkenavnet.
+ `output_dir`: Repræsenterer outputmappen. Biblioteket skal eksistere.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: eksempler

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>help

Identisk med [?](#section) -kommandoen.

#### <a name="list"></a>listen

Viser alle tilgængelige testcases.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Viser alle tilgængelige testplaner.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Viser testcases for den angivne testpakke. Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker. Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: påkrævede parametre

+ `suite_name`: Navnet på den ønskede pakke.

##### <a name="listtestsuite-examples"></a>listtestsuite: eksempler

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Viser alle tilgængelige testpakker.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Afspiller en testcase ved hjælp af en Excel-fil.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: påkrævede parametre

+ `excel_file`: En fuld sti til Excel-filen. Filen skal eksistere.

##### <a name="playback-examples"></a>playback: eksempler

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Afspiller flere testcases på én gang. Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: påkrævede parametre

+ `test_case_id1`: Id for eksisterende testcase.
+ `test_case_id2`: Id for eksisterende testcase.
+ `test_case_idN`: Id for eksisterende testcase.

##### <a name="playbackbyid-examples"></a>playbackbyid: eksempler

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Afspiller mange testcases på én gang ved hjælp af Excel-filer.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: påkrævede parametre

+ `excel_file1`: Fuld sti til Excel-filen. Filen skal eksistere.
+ `excel_file2`: Fuld sti til Excel-filen. Filen skal eksistere.
+ `excel_fileN`: Fuld sti til Excel-filen. Filen skal eksistere.

##### <a name="playbackmany-examples"></a>playbackmany: eksempler

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Afspiller alle testcases fra den angivne testpakke.
Du kan bruge kommandoen ``listtestsuitenames`` til at få vist alle tilgængelige pakker. Brug en vilkårlig værdi fra første kolonne som **suite_name**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: påkrævede parametre

+ `suite_name`: Navnet på den ønskede pakke.

##### <a name="playbacksuite-examples"></a>playbacksuite: eksempler

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

Lukker programmet.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>upload

Uploader alle de filer, der hører til den angivne testpakke eller de angivne testcases.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: påkrævede parametre

+ `suite_name`: Alle de filer, der hører til den angivne testpakke, bliver uploadet.
+ `testcase_id`: Alle de filer, der hører til den eller de angivne testcases, bliver uploadet.

##### <a name="upload-examples"></a>upload: eksempler

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Uploader kun den optagne fil, der hører til de angivne testcases.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: påkrævede parametre

+ `testcase_id`: Den optagne fil, der hører til de angivne testcases, bliver uploadet.

##### <a name="uploadrecording-examples"></a>uploadrecording: eksempler

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Viser to måder at aktivere dette program på: en, der bruger en fil med standardindstillinger, en anden, der angiver en fil med indstillinger.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell-eksempler

#### <a name="run-a-test-case-in-a-loop"></a>Køre en testsag i en løkke

Du har et testscript, der opretter en ny kunde. Ved hjælp af scripting kan denne testsag køres i en løkke ved at gøre følgende data tilfældige, før hver enkelt gentagelse køres:

- Debitor-id
- Navn på debitor
- Debitors adresse

Kunde-id'et har formatet *ATCUS\<number\>*, hvor \<number\> er en værdi mellem **000000001** og **999999999**.

I følgende eksempel bruges en parameter, **start**, til at definere det første tal, der bruges. Er bruger en anden parameter, **nr**, til at det definere det antal kunder, der skal oprettes. For hver gentagelse ændres parametrene i Excel-parameterfilen ved hjælp af en UpdateCustomer-funktion. Derefter kaldes RSAT-kommandolinjen i en RunTestCase-funktion.

Åbn Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i admininistratortilstand, og indsæt følgende kode i det vindue, der hedder **Uden titel.ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Køre et script, der afhænger af data i Microsoft Dynamics 365

I følgende eksempel bruges et OData-kald (Open data Protocol) til at finde ordrestatussen for en indkøbsordre. Hvis status ikke er **faktureret**, kan du f.eks. kalde en RSAT-testsag, der bogfører fakturaen.

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
