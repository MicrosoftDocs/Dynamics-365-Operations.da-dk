---
title: Regression Suite Automation Tool-selvstudium
description: Denne artikel viser, hvordan du kan bruge værktøjet RSAT (Regression Suite Automation Tool). Det beskriver forskellige funktioner og indeholder eksempler, der bruger avanceret scripting.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a270398ddebef0f47a2c31b0ffb022e3df6489c7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277398"
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

2. Gem opgaveregistreringen som en **udviklerregistrering**, og knyt den til testsagen i Azure DevOps.
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

![Beskeden Produktion – start.](./media/use_rsa_tool_05.png)

Du kan validere denne meddelelse via RSAT ved at angive meddelelsesteksten under fanen **Meddelelsesvalidering** i Excel-parameterfilen for den relevante registrering.

![Fanen Meddelelsesvalidering.](./media/use_rsa_tool_06.png)

Når testsagen er kørt, sammenlignes meddelelsen i Excel-parameterfilen med den viste meddelelse. Hvis meddelelserne ikke stemmer overens, vil testsagen mislykkes.

> [!NOTE]
> Du kan angive mere end én meddelelse under fanen **Meddelelsesvalidering** i Excel-parameterfilen. Meddelelserne kan også være fejl- eller advarselsmeddelelser i stedet for orienterende meddelelser.

### <a name="snapshot"></a>Øjebliksbillede

Denne funktion bruger skærmbilleder af de trin, der blev udført under opgaveregistreringen. Det er nyttigt i forbindelse med overvågning eller fejlfinding.

- Hvis du vil bruge denne funktion, mens RSAT kører med brugergrænsefladen, skal du åbne filen **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Program Files (x86)\\Regression Suite Automation Tool**), og ændre værdien for det følgende element fra **falsk** til **sand**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Hvis du vil bruge denne funktion, mens RSAT kører med CLI (f.eks. Azure DevOps), skal du åbne filen **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** under RSAT-installationsmappen (f.eks. **C:\\Programfiler (x86)\\Regression Suite Automation Tool**), og ændre værdien for det følgende element fra **falsk** til **sand**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Når du kører testsager, genererer RSAT snapshots (billeder) af trinnene og gemmer dem i afspilningsmappen for testsager i arbejdsbiblioteket. I mappen ved navn **StepSnapshots** oprettes en separat undermappe. Denne mappe indeholder øjebliksbilleder for de testsager, der køres.

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

![Flow for demoscenariet.](./media/use_rsa_tool_14.png)

I følgende illustration vises hierarkiet af forretningsprocesserne for dette scenario i LCS Forretningsmodeldesigner.

![Forretningsprocesser til demoscenariet.](./media/use_rsa_tool_15.png)

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Viser alle kommandoer eller hjælp til en bestemt kommando sammen med de tilgængelige parametre.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Valgfri parametre

`command`: Hvor ``[command]`` er en af kommandoerne på den foregående liste.

#### <a name="about"></a>about

Viser versionen af den installerede RSAT.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Rydder skærmen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>download

Downloader vedhæftede filer (optagelses-, udførelses- og parameterfiler) for den angivne testsag fra Azure DevOps til outputmappen. Du kan bruge kommandoen ``list`` til at hente alle tilgængelige testsager og bruge enhver værdi fra den første kolonne som parameteren **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter downloadprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.

##### <a name="download-required-parameters"></a>download: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.

##### <a name="download-optional-parameters"></a>download: valgfrie parametre

+ `output_dir`: Repræsenterer arbejdsmappen for output. Mappen skal eksistere. Arbejdsmappen fra indstillingerne bruges, hvis denne parameter ikke er angivet.

##### <a name="download-examples"></a>download: eksempler

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Downloader vedhæftede filer (optagelses-, udførelses- og parameterfiler) for alle testsager i den angivne testpakke fra Azure DevOps til outputmappen. Du kan bruge kommandoen ``listtestsuitenames`` til at hente alle tilgængelige testpakker og bruge enhver værdi som parameteren **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter downloadprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/byid`: Denne parameter angiver, at den ønskede testpakke er identificeret med sit Azure DevOps-id i stedet for navnet på testpakken.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: påkrævede parametre

+ `test_suite_name`: Repræsenterer testpakkenavnet. Denne parameter er påkrævet, hvis /byid-switch **ikke** er angivet. Dette er navnet på Azure DevOps-testpakken.
+ `test_suite_id`: Repræsenterer testpakke-id'et. Denne parameter er påkrævet, hvis /byid-switch **er** angivet. Dette id er testpakkens Azure DevOps-id.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: valgfrie parametre

+ `output_dir`: Repræsenterer arbejdsmappen for output. Mappen skal eksistere. Arbejdsmappen fra indstillingerne bruges, hvis denne parameter ikke er angivet.

##### <a name="downloadsuite-examples"></a>downloadsuite: eksempler

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>edit

Giver dig mulighed for at åbne parameterfilen i Excel-programmet og redigere den.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: påkrævede parametre

+ `excel_file`: Skal indeholde en fuldstændig sti til en eksisterende Excel-fil.

##### <a name="edit-examples"></a>edit: eksempler

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Opretter testkørsels- og -parameterfiler for det angivne testcase i outputmappen. Du kan bruge kommandoen ``list`` til at få vist alle tilgængelige testcases. Brug en vilkårlig værdi fra første kolonne som en **test_case_id**-parameter.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter generetingsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/dllonly`: Generér kun testudførelsesfiler. Generér ikke Excel-parameterfilen igen.
+ `/keepcustomexcel`: Opgrader den eksisterende parameterfil. Regenerer også udførelsesfiler.

##### <a name="generate-required-parameters"></a>generate: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.

##### <a name="generate-optional-parameters"></a>generate: valgfrie parametre

+ `output_dir`: Repræsenterer arbejdsmappen for output. Mappen skal eksistere. Arbejdsmappen fra indstillingerne bruges, hvis denne parameter ikke er angivet.

##### <a name="generate-examples"></a>generate: eksempler

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Genererer en ny afledt testsag (underordnet testsag) fra den leverede testsag. Den nye testsag føjes også til den angivne testpakke. Du kan bruge kommandoen ``list`` til at hente alle tilgængelige testsager og bruge enhver værdi fra den første kolonne som parameteren **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter generetingsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.

##### <a name="generatederived-required-parameters"></a>generatederived: påkrævede parametre

+ `parent_test_case_id`: Repræsenterer det overordnede testcase-id.
+ `test_plan_id`: Repræsenterer testplan-id'et.
+ `test_suite_id`: Repræsenterer testpakke-id'et.

##### <a name="generatederived-examples"></a>generatederived: eksempler

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Opretter kun testkørselsfiler for den angivne testsag. Den genererer ikke Excel-parameterfilen. Filerne genereres i den angivne outputmappe. Du kan bruge kommandoen ``list`` til at hente alle tilgængelige testsager og bruge enhver værdi fra den første kolonne som parameteren **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter generetingsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: påkrævede parametre

+ `test_case_id`: Repræsenterer testcase-id'et.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: valgfrie parametre

+ `output_dir`: Repræsenterer arbejdsmappen for output. Mappen skal eksistere. Arbejdsmappen fra indstillingerne bruges, hvis denne parameter ikke er angivet.

##### <a name="generatetestonly-examples"></a>generatetestonly: eksempler

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Opretter testautomatiseringsfiler for alle testsager i den angivne testpakke. Du kan bruge kommandoen ``listtestsuitenames`` til at hente alle tilgængelige testpakker og bruge enhver værdi som parameteren **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter generetingsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/dllonly`: Generér kun testudførelsesfiler. Generér ikke Excel-parameterfilen igen.
+ `/keepcustomexcel`: Opgrader eksisterende parameterfil. Regenerer også udførelsesfiler.
+ `/byid`: Denne parameter angiver, at den ønskede testpakke er identificeret med sit Azure DevOps-id i stedet for navnet på testpakken.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: påkrævede parametre

+ `test_suite_name`: Repræsenterer testpakkenavnet. Denne parameter er påkrævet, hvis /byid-switch **ikke** er angivet. Dette er navnet på Azure DevOps-testpakken.
+ `test_suite_id`: Repræsenterer testpakke-id'et. Denne parameter er påkrævet, hvis /byid-switch **er** angivet. Dette id er testpakkens Azure DevOps-id.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: valgfrie parametre

+ `output_dir`: Repræsenterer arbejdsmappen for output. Mappen skal eksistere. Arbejdsmappen fra indstillingerne bruges, hvis denne parameter ikke er angivet.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: eksempler

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Identisk med [?](#section) -kommandoen.

#### <a name="list"></a>list

Viser alle tilgængelige testsager i den aktuelle testplan.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Viser alle tilgængelige testplaner.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Viser testcases for den angivne testpakke. Du kan bruge kommandoen ``listtestsuitenames`` til at hente alle tilgængelige testpakker og bruge enhver værdi fra listen som parameteren **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: påkrævede parametre

+ `test_suite_name`: Navnet på den ønskede pakke.

##### <a name="listtestsuite-examples"></a>listtestsuite: eksempler

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Viser testcases for den angivne testpakke.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: påkrævede parametre

+ `test_suite_id`: Id'et på den ønskede pakke.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: eksempler

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Viser alle testpakker i den aktuelle testplan.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Afspiller testsagen, der er knyttet til den angivne Excel-parameterfil. Denne kommando bruger eksisterende lokale automatiseringsfiler og downloader ikke filer fra Azure DevOps. Denne kommando understøttes ikke i POS-handelstestsager.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter afspilningsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/comments[="comment"]`: Angiv en brugerdefineret informationsstreng, der skal medtages i feltet **Kommentarer** i oversigts- og testresultatsiderne for Azure DevOps-testsagskørsler.

##### <a name="playback-required-parameters"></a>playback: påkrævede parametre

+ `excel_parameter_file`: Den fulde sti til en Excel-parameterfil. Filen skal eksistere.

##### <a name="playback-examples"></a>playback: eksempler

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Afspiller flere testsager på én gang. Testsagerne identificeres ved deres id. Denne kommando downloader filer fra Azure DevOps. Du kan bruge kommandoen ``list`` til at hente alle tilgængelige testsager og bruge enhver værdi fra den første kolonne som parameteren **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter afspilningsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/comments[="comment"]`: Angiv en brugerdefineret informationsstreng, der skal medtages i feltet **Kommentarer** i oversigts- og testresultatsiderne for Azure DevOps-testsagskørsler.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: påkrævede parametre

+ `test_case_id1`: Id for en eksisterende testsag.
+ `test_case_id2`: Id for en eksisterende testsag.
+ `test_case_idN`: Id for en eksisterende testsag.

##### <a name="playbackbyid-examples"></a>playbackbyid: eksempler

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Afspiller mange testsager på én gang. Testsagerne identificeres af Excel-parameterfilerne. Denne kommando bruger eksisterende lokale automatiseringsfiler og downloader ikke filer fra Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter afspilningsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/comments[="comment"]`: Angiv en brugerdefineret informationsstreng, der skal medtages i feltet **Kommentarer** i oversigts- og testresultatsiderne for Azure DevOps-testsagskørsler.

##### <a name="playbackmany-required-parameters"></a>playbackmany: påkrævede parametre

+ `excel_parameter_file1`: Den fulde sti til Excel-parameterfilen. Filen skal eksistere.
+ `excel_parameter_file2`: Den fulde sti til Excel-parameterfilen. Filen skal eksistere.
+ `excel_parameter_fileN`: Den fulde sti til Excel-parameterfilen. Filen skal eksistere.

##### <a name="playbackmany-examples"></a>playbackmany: eksempler

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Afspiller alle testsager fra en eller flere angivne testpakker. Hvis parameteren /local er angivet, bruges lokale vedhæftede filer til afspilning. Ellers downloades vedhæftede filer fra Azure DevOps. Du kan bruge kommandoen ``listtestsuitenames`` til at hente alle tilgængelige testpakker og bruge enhver værdi fra den første kolonne som parameteren **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: valgfrie parametre

+ `/updatedriver`: Hvis denne parameter er angivet, opdateres webbrowserens WebDriver efter behov, før afspilningsprocessen køres.
+ `/local`: Denne parameter angiver, at lokale vedhæftede filer skal bruges til afspilning i stedet for at downloade filer fra Azure DevOps.
+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter afspilningsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/comments[="comment"]`: Angiv en brugerdefineret informationsstreng, der skal medtages i feltet **Kommentarer** i oversigts- og testresultatsiderne for Azure DevOps-testsagskørsler.
+ `/byid`: Denne parameter angiver, at den ønskede testpakke er identificeret med sit Azure DevOps-id i stedet for navnet på testpakken.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: påkrævede parametre

+ `test_suite_name1`: Repræsenterer testpakkenavnet. Denne parameter er påkrævet, hvis /byid-switch **ikke** er angivet. Dette er navnet på Azure DevOps-testpakken.
+ `test_suite_nameN`: Repræsenterer testpakkenavnet. Denne parameter er påkrævet, hvis /byid-switch **ikke** er angivet. Dette er navnet på Azure DevOps-testpakken.
+ `test_suite_id1`: Repræsenterer testpakke-id'et. Denne parameter er påkrævet, hvis /byid-switch **er** angivet. Dette id er testpakkens Azure DevOps-id.
+ `test_suite_idN`: Repræsenterer testpakke-id'et. Denne parameter er påkrævet, hvis /byid-switch **er** angivet. Dette id er testpakkens Azure DevOps-id.

##### <a name="playbacksuite-examples"></a>playbacksuite: eksempler

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Kører alle testsager i den angivne Azure DevOps-testpakke.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: valgfrie parametre

+ `/retry[=seconds]`: Hvis denne parameter er angivet, og testsager blokeres af andre RSAT-forekomster, venter afspilningsprocessen i det angivne antal sekunder og forsøger derefter en gang til. Standardværdien for \[seconds\] er 120 sekunder. Uden denne parameter annulleres processen med det samme, hvis testsager er blokeret.
+ `/comments[="comment"]`: Angiv en brugerdefineret informationsstreng, der skal medtages i feltet **Kommentarer** i oversigts- og testresultatsiderne for Azure DevOps-testsagskørsler.
+ `/byid`: Denne parameter angiver, at den ønskede testpakke er identificeret med sit Azure DevOps-id i stedet for navnet på testpakken.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: påkrævede parametre

+ `test_suite_id`: Repræsenterer testpakke-id'et, som det findes i Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: eksempler

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Lukker programmet. Denne kommando kan kun bruges, når programmerne kører i interaktiv tilstand.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: eksempler

`quit`

#### <a name="upload"></a>upload

Uploader vedhæftede filer (optagelses-, kørsels- og parameterfiler), der tilhører en angivet testpakke eller testsager, til Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: påkrævede parametre

+ `test_suite_name`: Alle filer, der tilhører den angivne testpakke, bliver uploadet.
+ `test_case_id1`: Repræsenterer det første testsags-id, der skal uploades. Brug kun denne parameter, når der ikke er angivet et navn på en testpakke.
+ `test_case_idN`: Repræsenterer det sidste testsags-id, der skal uploades. Brug kun denne parameter, når der ikke er angivet et navn på en testpakke.

##### <a name="upload-examples"></a>upload: eksempler

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Uploader kun den optagelsesfil, der tilhører en eller flere angivne testsager, til Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: påkrævede parametre

+ `test_case_id1`: Repræsenterer det første testsags-id for den optagelse, der skal uploades til Azure DevOps.
+ `test_case_idN`: Repræsenterer det sidste testsags-id for den optagelse, der skal uploades til Azure DevOps.

##### <a name="uploadrecording-examples"></a>uploadrecording: eksempler

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Viser de tre brugsmåder for dette program.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Kørsel af programmet interaktivt:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Kørsel af programmet ved at angive en kommando:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Kørsel af programmet ved at angive en indstillingsfil:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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

```powershell
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
