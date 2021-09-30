---
title: Fjernede eller udfasede platformfunktioner
description: Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.
author: sericks007
ms.date: 09/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 8910fc338f822e6b6b59acb0e6ee7a90db2b5007
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500103"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjernede eller udfasede platformfunktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="feature-deprecation-effective-august-2021"></a>Udfasning af funktioner, der træder i kraft i august 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-rapporter i Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** |   Alle aktiviteter og overvågning udføres internt af platformen via automatisering. Dette kræver ingen manuel handling.|
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | SQL-rapporter: Aktuelle DTU, Aktuelle DTU-detaljer, Hent lås-oplysninger, Oversigt over vejledning i aktuel plan, Hent liste over forespørgsels-id'er, Hent SQL-forespørgselsplan for bestemt plan-id, Hent forespørgselsplaner og udførelsesstatus, Hent begrænsningskonfiguration, Hent ventestatistik, Vis mest dyre forespørgsler |
| **Installationsindstilling**              | Skyinstallation: Påvirker Microsoft-administrerede produktionsmiljøer og sandkassemiljøer på niveau 2 til og med niveau 5. |
| **Status**                         | Udfaset: Planlagt dato for fjernelse i oktober 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-handlinger i LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi udfaser nogle SQL-handlinger i LCS.  |
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | SQL-aktioner: Oprette en planvejledning for at gennemtvinge plan-id, oprette en planvejledning for at tilføje tabeltip, fjerne planvejledning, deaktivere/aktivere sidelåse og låse eskalering, opdatere statistik for en tabel, gendanne indeks, oprette indeks |
| **Installationsindstilling**              | Skyinstallation: Påvirker Microsoft-administrerede produktionsmiljøer og sandkassemiljøer på niveau 2 til og med niveau 5. |
| **Status**                         | Udfaset: Planlagt dato for fjernelse i oktober 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Udfasning af funktioner, der træder i kraft i maj 2021

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globaliseringsportal i Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Vi udfaser globaliseringsportalen i LCS, da denne funktion er blevet erstattet af andre LCS-baserede tjenester. |
| **Erstattet af en anden funktion?**   | Ja, denne funktion erstattes af LCS [Problemsøgning](../lifecycle-services/issue-search-lcs.md) og [Dynamics-tjenesten til indsendelse af lovmæssige beskeder](../lcs-solutions/submit-localization-alerts.md). |
| **Produktområder, der er berørt**         | Globaliseringsportal i LCS|
| **Installationsindstilling**              | Skyinstallation |
| **Status**                         | Udfases: Planlagt dato for fjernelse i maj 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Funktionen er fjernet med ikrafttrædelsesdatoen 28. januar 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Batchjob til håndtering af defragmentering af SQL-indeks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Denne funktion er fjernet for at reducere de faste omkostninger ved drift, overvågning og vedligeholdelse af indeksstyringen af kunder. |
| **Erstattet af en anden funktion?**   | Fremadrettet vil indeksvedligeholdelsen blive udført af Microsoft-tjenester. Dette sker løbende, uden at det påvirker brugerworkloads. |
| **Produktområder, der er berørt**         | Finance and Operations-apps|
| **Installationsindstilling**              | Skyinstallation – påvirker Microsoft-administrerede produktionsmiljøer og sandkassemiljøer på niveau 2 til og med niveau 5. |
| **Status**                         | Denne funktion er fjernet. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.17 af Finance and Operations-apps


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Understøttelse af de seneste versioner af Visual Studio kræver ændringer af X++ udvidelserne til Visual Studio. Disse ændringer er ikke kompatible med Visual Studio 2015. |
| **Erstattet af en anden funktion?**   | Visual Studio 2017 erstatter Visual Studio 2015 som den installerede og påkrævede version. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Efter opdatering fjernes de forrige X++-værktøjer fra Visual Studio 2015, og de opdaterede værktøjer installeres ikke i Visual Studio 2015. Det påvirker ikke hostede builds. I forbindelse med build-virtuelle maskiner skal build-pipelinen (build-definitionen) opdateres manuelt for at ændre afhængigheden fra MSBuild 14.0 (Visual Studio 2015) til MSBuild 15.0 (Visual Studio 2017) som beskrevet i [Opdatere en ældre pipeline i Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Brugeravatar 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Brugeravataren, der vises i højre side af navigationslinjen, blev hentet ved hjælp af en API fra Dynamics 365-hovedkontrolelementet, der er frarådet. |
| **Erstattet af en anden funktion?**   | Brugerne vil i stedet se deres initialer i en cirkel på navigationslinjen. Det er den samme visual, der anvendes på udviklingsmaskiner. |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | Fjernet fra og med version 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Udfasning af Enterprise Portal (EP)  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Metadataartifakter, der er tilknyttet Dynamics AX 2012 Enterprise Portal (EP), er blevet frarådet, da EP aldrig blev understøttet i Finance and Operations-apps. |
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Alle EP-koder er planlagt til at blive fjernet i oktober 2021-versionen. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.15 af Finance and Operations-apps

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-understøttelse af Dynamics 365 udfases

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Internet Explorer 11-understøttelsen af alle Dynamics 365-produkter udfases fra december 2020, og Internet Explorer 11 understøttes ikke efter august 2021.<br><br>Dette vil påvirke kunder, der bruger Dynamics 365-produkter, som er udviklet til brug via en Internet Explorer 11-grænseflade. Efter august 2021 er Internet Explorer 11 ikke understøttet for sådanne Dynamics 365-produkter. |
| **Erstattet af en anden funktion?**   | Vi anbefaler, at kunderne overgår til Microsoft Edge.|
| **Produktområder, der er berørt**         | Alle Dynamics 365-produkter |
| **Installationsindstilling**              | Alt|
| **Status**                         | Udfases: Internet Explorer 11 understøttes ikke efter august 2021.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio-tilføjelsesprogram til anvendelse af hotfixes til metadata

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Metadata-hotfixes understøttes ikke længere i [One Version](../../fin-ops/get-started/one-version.md)-serviceopdateringer, der blev introduceret i juli 2018 med version 8.1. |
| **Erstattet af en anden funktion?**   | Individuelle hotfixes til metadata er ikke tilgængelige for understøttede versioner. Der anvendes i stedet kumulative kvalitetsopdateringer. |
| **Produktområder, der er berørt**         | Visual Studio-tilføjelsesprogrammer |
| **Installationsindstilling**              | Virtuelle maskiner til udvikling |
| **Status**                         | Med version 10.0.15 er tilføjelsesprogrammet ikke længere inkluderet i Visual Studio-værktøjerne. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.14 af Finance and Operations-apps

### <a name="online-users-page"></a>Siden Onlinebrugere 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Dette er en ældre side, der blev oprettet til forrige klient-/serverarkitektur. Oplysningerne på denne side er ikke altid nøjagtige, hvilket kan være forvirrende og vildledende. |
| **Erstattet af en anden funktion?**   | Vi vil angive en ny side i en senere opdatering.|
| **Produktområder, der er berørt**         | Systemadministration |
| **Installationsindstilling**              | Alt |
| **Status**                         | I oktober 2021 fjernes denne formular.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.13 af Finance and Operations-apps


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Brugerdefineret kode defineret i egenskaber for SSRS-rapport 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Generelt har brugerdefineret kode begrænsede fordele, men kræver væsentlige ressourcer og beregninger for at være understøttet. Brugerdefineret kode bruges primært af rapportforfattere til at kalde offentlige metoder fra en brugerdefineret kodeassembly. Den skybaserede tjeneste understøtter dog ikke referencer til brugerdefinerede assemblyer for SSRS-rapporter. |
| **Erstattet af en anden funktion?**   | Rapportforfattere kan vælge at fortsætte med at referere til offentlige .NET-API'er til handlinger for Matematik, Konvertering og Format fra et tekstfeltudtryk. Du kan finde flere oplysninger under [Føje kode til en rapport (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Produktområder, der er berørt**         | Undersæt af programrapportdesign, der er defineret i RDL, som indeholder brugerdefineret kode. |
| **Installationsindstilling**              | Alt |
| **Status**                         | Med version 10.0.13 begynder kompileren at udstede en advarsel for forekomster, hvor der registreres en brugerdefineret kode i en SSRS-rapportdefinition. Du kan løse problemet ved at åbne definitionen af rapportdesignet og fjerne alle brugerdefinerede kodeartefakter. Denne advarsel erstattes af en compilerfejl i en fremtidig opdatering.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Opgradering af tre jQuery-komponentbiblioteker 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Tre jQuery-komponentbiblioteker opdateres for at levere sikkerhedsrettelser og vedligeholde valuta.   
| **Erstattet af en anden funktion?**   | Følgende biblioteker bliver berørt: jQuery (til version 3.5.0 fra version 2.1.4), jQuery UI (til version 1.12.1 fra version 1.11.4), jQuery qTip (til version 3.0.3 fra 2.2.1). Der er leveret en migreringsvejledning online af jQuery.  |
| **Produktområder, der er berørt**         | Udvidede kontroller, specielt tilpasset JavaScript-kode, der udnytter de frarådede eller fjernede API'er |
| **Installationsindstilling**              | Alt |
| **Status**                         | Med version 10.0.13/Platform update 37 kan kunderne vælge at flytte til de seneste biblioteker ved at aktivere funktionen "Opgrader tre jQuery-komponentbiblioteker". Det bliver obligatorisk at flytte til de nye biblioteker med frigivelsen i april 2021 for at give tid til migrering af berørte API'er.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Eksisterende API for gitterkontrolelement/forceLegacyGrid()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Det eksisterende gitterkontrolelement erstattes af det nye gitterkontrolelement. |
| **Erstattet af en anden funktion?**   | Det [nye gitterkontrolelement](../..//fin-ops/get-started/grid-capabilities.md) |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | I version 10.0.13 er det nye gitterkontrolelement generelt tilgængeligt, og kunderne kan vælge at aktivere denne funktion. Det nye gitter vil være i brug som standard med frigivelsen i oktober 2021 og er forventes aktuelt at være obligatorisk i april 2022. Når det nye gitterkontrolelement bliver obligatorisk, vil **forceLegacyGrid()**-API ikke længere fungere. |

### <a name="personalization-without-saved-views"></a>Personlig tilpasning uden gemte visninger 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Undersystemet for personlig tilpasning er blevet fornyet med funktionen for gemte visninger, så det har bedre ydeevne og giver yderligere muligheder. |
| **Erstattet af en anden funktion?**   | Gemte visninger |
| **Produktområder, der er berørt**         | Webklient |
| **Installationsindstilling**              | Alt |
| **Status**                         | I version 10.0.13/Platform update 37 er funktionen til gemte visninger generelt tilgængelig, og kunderne kan vælge at aktivere denne funktion. Funktionen til gemte visninger bliver obligatorisk i oktober 2021-frigivelsen. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.12 af Finance and Operations-apps

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Udvidelser af gitter- eller gruppekontrolformularer, der indeholder ugyldige feltreferencer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Datagruppeegenskaben for gitter- eller gruppekontrolelementer bruges til automatisk at få vist alle felterne i en feltgruppe. En gitter- eller gruppekontrol, der tilføjes som en udvidelse, kan indeholde felter, der ikke længere er defineret i feltgruppen, eller den kan mangle felter, der er defineret i feltgruppen. Dette kan medføre en inkonsistent funktionsmåde på kørselstidspunktet. Platformsopdateringer til version 10.0.12 af Finance and Operations-apps kategoriserer nu dette problem som en *compileradvarsel*. Du kan løse dette problem ved at åbne formularudvidelsen og gemme den.
| **Erstattet af en anden funktion?**   | Denne compileradvarsel erstattes af en compilerfejl i en senere opdatering. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Der introduceres en compileradvarsel i platformsopdateringer til version 10.0.12 af Finance and Operations-apps. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Platformsopdateringer til version 10.0.11 af Finance and Operations-apps

### <a name="explicit-safe-lists-for-self-service-environments"></a>Eksplicitte sikre lister til selvbetjeningsmiljøer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Processen til flytning af IP til sikre lister er ændret. Selvbetjening understøtter ikke længere IP-sikre lister. |
| **Erstattet af en anden funktion?**   | Du kan finde flere oplysninger i [Konfiguration af betinget adgang til Azure Active Directory](/appcenter/general/configuring-aad-conditional-access).|
| **Produktområder, der er berørt**         | Sikkerhed |
| **Installationsindstilling**              | Sky |
| **Status**                         | Udfaset: Denne funktion er helt udfaset for installationer med selvbetjening. |

### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Understøttelse af de seneste versioner af Visual Studio kræver ændringer af X++ udvidelserne til Visual Studio. Disse ændringer er ikke kompatible med Visual Studio 2015. |
| **Erstattet af en anden funktion?**   | Visual Studio 2017 erstatter Visual Studio 2015 som den installerede og påkrævede version. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Virtuelle maskiner, der er udrullet på version 10.0.13 (platformsopdatering 37) eller nyere, indeholder Visual Studio 2017. Version 10.0.16 (platformsopdatering 40) er den endelige version med understøttelse af Visual Studio 2015. Virtuelle maskiner, der kun har Visual Studio 2015, kan ikke opdatere til version 10.0.17 (platformsopdatering 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper, der indeholder ugyldige feltreferencer

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Feltgrupper i tabellens metadatadefinitioner kan indeholde feltreferencer, der ikke er gyldige. Hvis disse feltgrupper er installeret, kan de medføre kørselsfejl i Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Platformopdatering 23 introducerede en *compileradvarsel*, der gjorde det muligt, at dette metadataproblem kunne rettes. Platformsopdateringer til version 10.0.11 af Finance and Operations-apps kategoriserer dette problem som en *compilerfejl*.<p>Følg disse trin for at løse dette problem.</p><ol><li>Fjern den ugyldige feltreference fra definitionen af tabelfeltgruppen.</li><li>Kompilér igen.</li><li>Kontrollér, at eventuelle fejl er løst.</li></ol> |
| **Erstattet af en anden funktion?**   | Denne compilerfejl erstatter permanent compileradvarslen.  |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Compileradvarslen er en compilerfejl i platformsopdateringer til version 10.0.11 af Finance and Operations-apps. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-licenser, der er oprettet ved hjælp af SHA1-hashing-algoritmen

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Den proces, man bruger til at oprette ISV-licenser (Independent Software Vendor), er blevet ændret. Du kan få flere oplysninger i afsnittet [Independent software vendor (ISV) licensing](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Erstattet af en anden funktion?**   | Ja. Brug Windows PowerShell til at oprette licenser. |
| **Produktområder, der er berørt**         | Visual Studio-udviklingsværktøjer |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: ISV-licenser, der er oprettet ved hjælp af SHA1-hashing-algoritmen. Denne algoritme er afhænger af certifikater, der er oprettet med hjælpeprogrammet MakeCert, og dette værktøj er udfaset.<br><br>Udfases: Brugen af SHA1 til sikkerheds- eller hashing-formål. SHA1 vil ophøre med at fungere i starten af 2021. Derfor bør den ikke længere bruges.<br><br>Fjernet: Understøttelse af TLS (Transport Layer Security) 1.0 og TLS 1.1 indgående eller udgående anmodninger. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Dette var et sikkerhedsproblem, fordi anmodningen om ændring kunne sendes til en ikke-tiltænkt bruger. Dette var også et anvendelighedsproblem, fordi den tvang brugeren til at afgøre, hvem der var arbejdsgangsigangsætteren og vælge dem manuelt.  |
| **Erstattet af en anden funktion?**   | Nej |
| **Produktområder, der er berørt**         | Arbejdsgang |
| **Installationsindstilling**              | Alt |
| **Status**                         | Rullelisten Brugervalg blev fjernet fra dialogboksen Ændring af anmodning i platformsopdatering 32. Anmodninger om ændring af anmodninger sendes efter hensigten automatisk til igangsætteren. Du kan finde flere oplysninger om denne funktion under [Handlinger i godkendelsesprocesser i arbejdsgang](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Link til integreret detaljeadgang understøttes ikke længere i sideinddelte dokumenter, der gengives af den skybaserede tjeneste 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Navigations URL-adresser, der er integreret i dokumenter, der er gengivet af tjenesten, kan indeholde følsomme virksomhedsdata. Vi fjerner understøttelse af link til integreret detaljeadgang i dokumenter som en sikkerhedsforanstaltning, der beskytter kundens data yderligere. Brugerne vil også få gavn af en forbedret ydeevne, når de opretter dokumenter interaktivt, som følge af denne ændring.  |
| **Erstattet af en anden funktion?**   | Ingen |
| **Produktområder, der er berørt**         | Rapportering |
| **Installationsindstilling**              | Alt |
| **Status**                         | Denne funktion fjernes aktivt fra tjenesten.<br><br>Den moderne klient tilbyder adskillige muligheder for at lave visninger, der omfatter automatisk genererede links, som kan hjælpe dig med at navigere i programmet. Sideinddelte dokumenter, der gengives af tjenesten, anbefales til ekstern kommunikation, der sendes via mail, arkiveres og udskrives for modtagere. Vi har forbedret oplevelsen af at få vist dokumenter direkte i browseren, som giver direkte adgang til lokale printere. Du kan finde flere oplysninger i [Vis PDF-dokumenter med en integreret fremviser](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
