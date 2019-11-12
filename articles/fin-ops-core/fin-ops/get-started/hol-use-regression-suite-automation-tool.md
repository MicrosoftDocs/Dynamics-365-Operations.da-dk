---
title: Bruge Regression Suite Automation Tool
description: I dette emne vises, hvordan du kan bruge værktøjet RSAT (Regression Suite Automation Tool). Det beskriver forskellige funktioner og indeholder eksempler, der bruger avanceret scripting.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 9afa98156c58d10c19454430769a3d60343661dc
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550951"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Brug Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format. 

Dette selvstudium gennemgår nogle af de avancerede funktioner i RSAT (Regression suite automation tool), herunder en demoopgave og beskriver strategi og centrale undervisningspunkter.

## <a name="features-of-rsattask-recorder"></a>Funktioner i RSAT/Arbejdsrutineoptager

### <a name="validate-a-field-value"></a>Valider en feltværdi

Du kan finde flere oplysninger om denne funktion under [Oprette en ny opgaveregistrering, der har en valideringsfunktion](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Gemt variabel

Du kan finde flere oplysninger om denne funktion under [Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Afledt testsag

1. Åbn RSAT (Regression Suite Automation Tool), og vælg begge testsager, du har oprettet i [Konfigurere og installere selvstudium til Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).
2. Vælg **Ny \> Opret afledt testsag**.

    ![Kommandoen Opret afledt testsag i menuen Ny](./media/use_rsa_tool_01.png)

3. Du får vist en meddelelse, hvor det angives, at der oprettes en afledt test sag for hver valgt testsag i den aktuelle testpakke, og at hver afledt testsag vil have sin egen kopi af Excel-parameterfilen. Vælg **OK**.

    > [!NOTE]
    > Når du kører en afledt testsag, bruger den en opgaveregistrering af den overordnede test og dens egen kopi af Excel-parameterfilen. På denne måde kan du køre den samme test med forskellige parametre uden at skulle vedligeholde mere end én opgaveregistrering. En afledt testsag behøver ikke at være en del af samme testpakke som dens overordnede testsag.

    ![Meddelelsesboks](./media/use_rsa_tool_02.png)

    Der oprettes to ekstra afledte testsager, og afkrydsningsfeltet **Afledt?** er markeret for dem.

    ![Afledte testsager oprettet](./media/use_rsa_tool_03.png)

    Der oprettes automatisk en afledt testsag i Azure DevOps. Det er et underordnet element til testsagen **Opret et nyt produkt** og mærkes med et særligt nøgleord: **RSAT:DerivedTestSteps**. Disse testsager føjes også automatisk til testplanen i Azure DevOps.

    ![Nøgleordet RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Hvis de afledte testsager, der oprettes, af en eller anden årsag ikke har den rigtige ordre, skal du gå til Azure DevOps og omarrangere testsagerne i testpakken, så RSAT kan køre dem i den rigtige rækkefølge.

4. Vælg de afledte testsager, og vælg derefter **Rediger** for at åbne de tilhørende Excel-parameterfiler.
5. Rediger disse Excel-parameter filer på samme måde, som du redigerede de overordnede filer. Med andre ord skal du sikre dig, at produkt-id'et er angivet, så det genereres automatisk. Kontroller også, at den gemte variabel kopieres til de relevante felter.
6. Gå til fanen **Generelt** i begge Excel-parameterfiler, opdater værdien af feltet **Firma** til **USSI**, så de afledte testsager køres mod en anden juridisk enhed end den overordnede testsag. Hvis du vil køre testsagerne mod en bestemt bruger (eller den rolle, der er knyttet til en bestemt bruger), kan du opdatere værdien i feltet **Testbruger**.
7. Vælg **Kør**, og kontroller, at produktet er oprettet i både den juridiske enhed, USMF, og den juridiske enhed, USSI.

### <a name="validate-notifications"></a>Valider beskeder

Denne funktion kan bruges til at validere, om der opstod en handling. Når der f.eks. oprettes, estimeres og derefter startes en produktionsordre, viser appen meddelelsen "Produktion – start" for at give dig besked om, at produktionsordren er startet.

![Beskeden Produktion – start](./media/use_rsa_tool_05.png)

Du kan validere denne meddelelse via RSAT ved at angive meddelelsesteksten under fanen **Meddelelsesvalidering** i Excel-parameterfilen for den relevante registrering.

![Fanen Meddelelsesvalidering](./media/use_rsa_tool_06.png)

Når testsagen er kørt, sammenlignes meddelelsen i Excel-parameterfilen med den viste meddelelse. Hvis meddelelserne ikke stemmer overens, vil testsagen mislykkes.

> [!NOTE]
> Du kan angive mere end én meddelelse under fanen **Meddelelsesvalidering** i Excel-parameterfilen. Meddelelserne kan også være fejl- eller advarselsmeddelelser i stedet for orienterende meddelelser.

### <a name="validate-values-by-using-operators"></a>Valider værdier ved hjælp af operatorer

I tidligere versioner af RSAT kunne du kun validere værdier, hvis en kontrolværdi var lig med en forventet værdi. Den nye funktion giver dig mulighed for at validere, at en variabel ikke er lig med, er mindre end eller mere end en angivet værdi.

- Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), og ændre værdien i det følgende element fra **falsk** til **sand**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    I Excel-parameterfilen vises et nyt felt **Operator**.

    > [!NOTE]
    > Hvis du har brugt en ældre version af RSAT, skal du oprette nye Excel-parameterfiler.

    ![Feltet Operator](./media/use_rsa_tool_07.png)

I følgende eksempel vises, hvordan du kan bruge denne funktion til at validere, om den disponible lagerbeholdning er større end 0 (nul).

1. I demodataene i **USMF**-firmaet skal du oprette en opgaveregistrering, der indeholder følgende trin:

    1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
    2. Brug Quick Filter til at finde poster. Filtrer f.eks. efter en værdi på **1000** for feltet **Varenummer**.
    3. Vælg **Disponibel lagerbeholdning**.
    4. Brug Quick Filter til at finde poster. Du kan f.eks. filtrere efter værdien **1** for feltet **Lokation**.
    5. Markér den valgte række på listen.
    6. Kontroller, at værdien af feltet **I alt disponibelt** er **411,0000000000000000**.

2. Gem opgaveregistreringen i BPM-biblioteket i LCS, og synkroniser den med Azure DevOps.
3. Føj testsagen til testplanen, og Indlæs testsagen i RSAT.
4. Åbn Excel-parameterfilen. Under fanen **InventOnhandItem** kan du se afsnittet **Valider InventOnhandItem**, der indeholder feltet **operator**.

    ![Feltet Operator](./media/use_rsa_tool_08.png)

5. Hvis du vil validere, om den disponible lagerbeholdning altid vil være mere end 0, skal du ændre værdien af feltet **Værdi** fra **411** til **0** og værdien af feltet **Operator** fra et lighedstegn (**=**) til et større end tegn (**\>**).

    ![Værdierne i felterne Værdi og Operator ændres](./media/use_rsa_tool_09.png)

6. Gem og luk Excel-parameterfilen.
7. Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen Azure DevOps.

Hvis værdien af feltet **I alt disponibelt** for den angivne vare på lageret er større end 0 (nul), vil testene bestå, uanset den faktiske værdi for disponibel lagerbeholdning.

### <a name="generator-logs"></a>Generatorlogfiler

Denne funktion opretter en mappe, der indeholder logfilerne for de testsager, der er blevet kørt.

- Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), og ændre værdien i det følgende element fra **falsk** til **sand**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Når testsagerne er kørt, kan du finde logfilerne under **C:\\Brugere\\\<Brugernavn\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Mappen GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Hvis der var eksisterende testsager, før du ændrede værdien i. config-filen, oprettes der ikke logfiler for disse testsager, før du opretter nye testkørselsfiler.
> 
> ![Kommandoen Generér kun testkørselsfiler i menuen Ny](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Øjebliksbillede

Denne funktion bruger skærmbilleder af de trin, der blev udført under opgaveregistreringen.

- Hvis du vil bruge denne funktion, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**) og ændre værdien af det følgende element fra **falsk** til **sand**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Under **C:\\Brugere\\\<Brugernavn\>\\AppData\\Roaming\\regressionTool\\playback** oprettes der en separat mappe for hver testsag, der køres.

![Mappen til øjebliksbiller for en testsag](./media/use_rsa_tool_12.png)

I hver af disse mapper kan du finde øjebliksbilleder af de trin, der blev udført, mens testsagerne blev kørt.

![Øjebliksfiler](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>Tilknytning

### <a name="scenario"></a>Scenarie

1. Produktdesigneren opretter et nyt, frigivet produkt.
2. Produktionschefen starter en produktionsordre for at bringe lagerniveauet op til to styk.
3. Produktionen starter og afslutter produktionsordren og kontrollerer, at det disponible antal er to styk.
4. Salgsteamet modtager en ordre på fire stykker af det nye produkt. Salgsgruppen opdaterer derfor nettokravene via den dynamiske plan. Da der ikke er mere tilgængelig kapacitet, er standardordrepolitikken indstillet til "køb i stedet for at fremstille". Derfor oprettes der et salgsforslag.
5. Køberen tilføjer en kreditor, autoriserer indkøbsordreforslaget og bekræfter derefter indkøbsordren.
6. Når de købte varer ankommer til butikken, søger butiksoperatøren efter den relaterede indkøbsordre og modtager varerne. Da ordren nu er fuldført, kan varer plukkes og pakkes i forhold til salgsordren.
7. Finans bogfører købsfakturaen og salgsfakturaen.

I følgende illustration vises flowet i dette scenarie.

![Flow for demoscenariet](./media/use_rsa_tool_14.png)

I følgende illustration vises forretningsprocesserne for dette scenario i RSAT.

![Forretningsprocesser til demoscenariet](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategi – vigtig læring

### <a name="data"></a>Data

- Sørg for, at du har repræsentative datamængder (en kopi af produktion/gyldne konfigurationsdata plus overførte data).
- Når du genererer nye data via en opgaveregistrering, skal du oprette testnavne, der ikke er i konflikt med eksisterende navne (brug f.eks. et præfisk såsom **RSATxxx**).
- Brug Azures funktion til genoprettelse af et bestemt tidspunkt for at køre test i miljøjer, der ikke er niveau 1, igen.
- Selvom du kan bruge Excel-funktionerne **VILKÅRLIG** og **NU** til at generere en entydig kombination, kræver det ret meget arbejde. Her er et eksempel.

    ```
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

### <a name="command-line"></a>Kommandolinje

RSAT kan kaldes fra et **Kommandopropt**-vindue.

> [!NOTE]
> Kontroller, at **TestRoot**-miljøvariablen er indstillet til RSAT-installationsstien. (Gå til Microsoft Windows, åbn **Kontrolpanel**, vælg **System og sikkerhed \> System \> Avancerede systemindstillinger**, og vælg derefter **Miljøvariabler**.)

1. Åbn et **kommandopromptvindue** som administrator.
2. Kør værktøjet fra installationsmappen.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Vis alle kommandoer.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell-eksempler

#### <a name="run-a-test-case-in-a-loop"></a>Køre en testsag i en løkke

Du har et testscript, der opretter en ny kunde. Ved hjælp af scripting kan denne testsag køres i en løkke ved at gøre følgende data tilfældige, før hver enkelt gentagelse køres:

- Debitor-id
- Navn på debitor
- Debitors adresse

Kunde-id'et har formatet *ATCUS\<tal\>*, hvor \<tal\> er en værdi mellem **000000001** og **999999999**.

I følgende eksempel bruges en parameter, **start**, til at definere det første tal, der bruges. Er bruger en anden parameter, **nr**, til at det definere det antal kunder, der skal oprettes. For hver gentagelse ændres parametrene i Excel-parameterfilen ved hjælp af en UpdateCustomer-funktion. Derefter kaldes RSAT-kommandolinjen i en RunTestCase-funktion.

Åbn Microsoft Windows PowerShell Integrated Scripting Environment (ISE) i admininistratortilstand, og indsæt følgende kode i det vindue, der hedder**Uden titel.ps1**.

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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
