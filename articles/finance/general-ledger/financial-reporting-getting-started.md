---
title: Oversigt over økonomirapportering
description: Denne artikel beskriver, hvor du kan få adgang til økonomirapportering i Microsoft Dynamics 365 Finance, og hvordan du bruger funktionerne til økonomirapportering.
author: aprilolson
ms.date: 06/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2c31e8b8b8022e5dfdb1f8dc4836d3d95174078
ms.sourcegitcommit: d9d111d7420ca8f1071689afe38a1ccf4b8051f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/21/2022
ms.locfileid: "9033654"
---
# <a name="get-started-with-financial-reporting"></a>Start her med økonomirapportering 

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvor du kan få adgang til økonomirapportering, og hvordan du bruger funktionerne til økonomirapportering. Det indeholder også en beskrivelse af eksisterende standardøkonomirapporter.

## <a name="enable-financial-reporting"></a>Aktivere økonomirapportering
Hvis du vil bruge økonomirapporteringstjenesten for din organisation, skal en Lifecycle Services-administrator (LCS) aktivere denne tjeneste på LCS-portalen for din organisation. Hvis der ikke er klargjort økonomirapportering i dit miljø, skal du kontakte din LCS-administrator for at aktivere tjenesten. 

## <a name="accessing-financial-reporting"></a>Adgang til økonomirapportering

Du kan finde menuen **Financial reporting** følgende steder:

- **Finans** > **Forespørgsler og rapporter**
- **Budgettering** > **Forespørgsler og rapporter** > **Grundlæggende budgettering**
- **Budgettering** > **Forespørgsler og rapporter** > **Budgetplanlægning**
- **Budgettering** > **Forespørgsler og rapporter** > **Budgetstyring**
- Konsolideringer

Hvis du vil oprette og generere økonomiske rapporter for en juridisk enhed, skal du angive følgende oplysninger for den pågældende juridiske enhed:

- Regnskabskalender
- Ledger
- Kontoplan
- Valuta
- Bogfør en postering på mindst én konto
- MainAccount vises i kolonnen **Valgt** på siden **Opsætning af Financial Reporting** (**Finans > Finansopsætning > Opsætning af Financial Reporting**)

## <a name="granting-security-access-to-financial-reporting"></a>Tildele sikkerhedsadgang til Financial Reporting

Funktionerne til økonomisk rapportering er tilgængelige for brugere, der har de nødvendige rettigheder og pligter tildelt via deres sikkerhedsroller. I følgende afsnit vises disse rettigheder og pligter samt de tilknyttede roller.

### <a name="duties"></a>Opgaver

| Navn på pligt                            | Betegnelse                                                             | AOT-navn                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Opretholde sikker økonomirapportering | Oprethold sikkerhed i økonomirapportering, og udfør administrative opgaver. | FinancialReportsSecurityMaintain |
| Ajourføre økonomiske rapporter            | Udarbejd og vedligehold økonomiske rapporter.                                  | FinancialReportsMaintain         |
| Generere økonomiske rapporter            | Generér og opdater økonomiske rapporter.                                 | FinancialReportsGenerate         |
| Gennemgå driftsregnskaber          | Gennemgå og analyser driftsregnskaber.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Rettigheder

| Rettighedsetiket                       | Betegnelse                                                             | AOT-navn                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Opretholde sikker økonomirapportering | Oprethold sikkerhed i økonomirapportering, og udfør administrative opgaver. | FinancialReportsSecuritySystemMaintain |
| Ajourføre økonomiske rapporter            | Udarbejd og vedligehold økonomiske rapporter.                                  | FinancialReportsMaintainReports  |
| Generere økonomiske rapporter            | Generér og opdater økonomiske rapporter.                                 | FinancialReportsGenerateReports  |
| Vis økonomiske rapporter                | Vis økonomiske rapporter.                                                 | FinancialReportsView             |

### <a name="roles"></a>Roller

| Rettighedsetiket                       | Programadgangsrettighed                                  | Roller                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Opretholde sikker økonomirapportering | Opretholde sikker økonomirapportering | Sikkerhedsadministrator                                                          |
| Ajourføre økonomiske rapporter            | Ajourføre økonomiske rapporter            | Regnskabschef, Regnskabsansvarlig, Finansinspektør, Budgetchef |
| Generere økonomiske rapporter            | Generere økonomiske rapporter            | Administrerende direktør, regnskabsdirektør, bogholder                                                            |
| Vis økonomiske rapporter                | Gennemgå driftsregnskaber          | Ingen tildelt                                                                   |

Når en bruger er tilføjet, eller en rolle er ændret, bør brugeren kunne få adgang til Financial Reporting inden for få minutter. 

> [!NOTE]
> Rollen sysadmin føjes til alle roller i Financial Reporting.

## <a name="report-deletions-and-expirations"></a>Rapportér sletninger og udløbsdatoer

Brugere, der genererer en rapport, kan slette deres egne rapporter. Brugere med pligten **Ajourføring af sikker økonomirapportering** kan slette andres rapporter. 

Begrebet udløbsdato blev introduceret i version 10.0.8. En ny påkrævet funktion aktiveres på siden **Alle** i arbejdsområdet til administration af funktioner. Funktionen **Opbevaringspolitikker for økonomiske rapporter** indeholder følgende ændringer:
* Nyligt genererede rapporter markeres automatisk som havende en udløbsdato på 90 dage fra det tidspunkt, hvor de genereres.
* Alle eksisterende rapporter fra før funktionen blev installeret, får en udløbsperiode på 90 dage. Datoen kan blive vist som tom i en kort periode frem til tjenesten økonomirapportering kører, en rapport genereres, og tjenesten udfører opdateringen til eksisterende rapporter med en tom udløbsdato. 
* Brugere med **Ajourføring af sikker økonomirapportering** har adgang til denne funktionalitet. Enhver bruger i pligten **Ajourføring af økonomiske rapporter**, som er blevet tildelt rettigheden **Ajourføring af udløb af økonomiske rapporter**, vil også have mulighed for at ændre udløbsperioden. I øjeblikket er der to tilbageholdelsesmuligheder: 

    * Et udløb på 90 dage.
    * En mulighed for at indstille, at rapporten aldrig skal udløbe.

Når der vælges en udløbsdato som f.eks. 90 dage, anvendes den 90 dage fra dags dato. Dette er en anden funktion end de 90 dage fra den oprindelige oprettelsesdato, der blev angivet, da rapporten blev genereret. 

Yderligere indstillinger vil blive medtaget i fremtidige funktioner. Udløbet på 90 dage er standard, og brugere med de rette tilladelser kan tilsidesætte standarden på listesiden **Økonomirapporter**.

## <a name="default-reports"></a>Standardrapporter

Økonomirapportering indeholder 22 økonomiske standardrapporter. Hver rapport bruger standardhovedkontokategorierne: Du kan bruge disse rapporter, som de er, eller du kan bruge dem som udgangspunkt til dine behov for økonomirapportering. Disse standardrapporter omfatter ud over de traditionelle regnskaber, resultatopgørelsen og balancen, rapporter, der viser de forskellige typer økonomiske rapporter, du kan oprette. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Standardrapport                                                                                         | Beskrivelse                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12-måneders rullende enkelt kolonne resultatopgørelse – standard | Få vist en organisations rentabilitet for de sidste 12 måneder i en enkelt kolonne.                                                                                                                                                                                                                                      |
| 12-måneders tendensresultatopgørelse – standard                 | Få vist en organisations rentabilitet for hver af de sidste 12 måneder. Disse 12 måneder kan spænde over mere end ét regnskabsår.                                                                                                                                                                                             |
| Faktisk vs. budget – standard                                | Få vist detaljerede saldooplysninger for alle konti for det oprindelige budget, og sammenlign det reviderede budget med faktiske oplysninger, der har en afvigelse.                                                                                                                                                                          |
| Revisionsoplysninger – standard                                  | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser debet- og kreditsaldi i rapporteringsvalutaen og den lokale valuta, sammen med yderligere posteringsoplysninger som bruger-id, den bruger, der senest har ændret data, datoen for den seneste ændring og kladde-id'et. |
| Saldoliste – standard                                   | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser start- og ultimosaldi og debet- og kreditsaldi for indeværende periode og år til dato samt yderligere posteringsoplysninger som f.eks. bilaget.                                                                    |
| Balance – standard                                   | Få vist organisationens økonomiske situation for året.                                                                                                                                                                                                                                                             |
| Balancen og resultatopgørelsen side om side – standard | Få vist organisationens økonomiske situation og indtjening for året ved siden af hinanden.                                                                                                                                                                                                                              |
| Pengestrøm – projekt                                       | Få indblik i de kontanter, der går ind og ud af organisationen.                                                                                                                                                                                                                                   |
| Detaljeret JE- og TB-revision – standard                      | Få vist startsaldo og aktivitetsoplysninger for alle konti.                                                                                                                                                                                                                                                      |
| [Detaljeret råbalance – standard](trial-balance-financial-reports.md)| Få vist oplysninger om saldoen for alle konti, der har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.                                                                                                                                  |
| Tre år kvartalsvise tendens for udgifter – standard             | Få indblik i udgifter for de seneste 12 kvartaler i de foregående tre år.                                                                                                                                                                                                                                   |
| Finansielle overskrifter JE- og TB-revision – standard            | Få vist en oversigt over finansielle overskrifter for saldi og aktivitet for aktivet, ansvar, ejerens egenkapital, indtægter, udgifter, gevinst eller tab.                                                                                                                                                                           |
| [Resultatopgørelse – standard](income-statement-financial-report.md)| Få vist organisationens rentabilitet for den aktuelle periode og år til dato.                                                                                                                                                                                                                                   |
| Finansposteringsliste – standard                        | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser debet- og kreditsaldi sammen med t yderligere posteringsoplysninger såsom posteringsdato, kladdenummer, bilag, typen og sporingsnummer.                                                                            |
| Nøgletal – standard                                          | Få vist soliditet, rentabilitet og efektivitetsnøgletal for organisationen for året.                                                                                                                                                                                                                           |
| Rullende 12 måneders udgifter – standard                       | Få indblik i udgifter for hvert af de seneste 12 måneder. Disse 12 måneder kan spænde over mere end ét regnskabsår.                                                                                                                                                                                                       |
| Rullende kvartal resultatopgørelse – standard               | Få vist organisationens rentabilitet på kvartalsvist grundlag for det seneste år og år til dato.                                                                                                                                                                                                                   |
| Parallel balance – standard                      | Få vist organisationens økonomiske situation for året. Denne rapport viser aktiver og passiver og egenkapital ved siden af hinanden.                                                                                                                                                                                |
| [Råbalanceoversigt – standard](trial-balance-financial-reports.md)| Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.                                                                                                                                                                  |
| [Årlig råbalanceoversigt – standard](trial-balance-financial-reports.md)| Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.                                                                                                                           |
| Ugentligt salg og rabatter – standard                     | Få indblik i salg og rabatter for hver uge i en måned. Denne rapport omfatter fire uger totalt.                                                                                                                                                                                                              |
| Tilgængelige budgetmidler - standard                         | Se en detaljeret sammenligning af det reviderede budget, faktiske udgifter, budgetreservationer og disponible budgetmidler for alle konti                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Startøkonomirapporter

Når du vælger menuen **Financial Reporting**, vises listen over økonomiske standardrapporter for firmaet. Du kan derefter åbne eller redigere en rapport. Vælg navnet på rapporten for at åbne en af standardrapporterne. Første gang en rapport åbnes, genereres den automatisk for den foregående måned. For eksempel, hvis du åbner en rapport for første gang i august 2019, oprettes rapporten for 31. juli 2019. Når en rapport er åben, kan du begynde at udforske den ved at foretage detailudledning for bestemte data og ændre rapportindstillinger.

## <a name="creating-and-modifying-financial-reports"></a>Oprettelse og redigering af økonomiske rapporter

Du kan oprette en ny rapport eller ændre en eksisterende rapport på listen over økonomiske rapporter. Hvis du har de nødvendige tilladelser, kan du oprette en ny økonomirapport ved at vælge **Ny** i handlingsruden. Et rapportdesignerprogram overføres til din enhed. Du kan oprette den nye rapport, når rapportdesigneren er startet. Når du har gemt den nye rapport, vises den på listen over økonomiske rapporter. Listen viser kun rapporter, der er oprettet for det firma, du bruger i Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Rapporteringstrædefinitioner

En af de komponenter, der bruges til at oprette økonomirapporter, er en definition af rapporteringstræet. En rapporteringstrædefinition hjælper med at definere strukturen og hierarkiet i din organisation. Det er en krydsdimensionale hierarkisk struktur, der er baseret på de størrelsesmæssige relationer i dine økonomiske data. Den giver oplysninger på rapporteringsenhedsniveau og på oversigtsniveau for alle enheder i træet.

Du kan oprette et ubegrænset antal rapporteringstræer for at få vist virksomhedens data på forskellige måder. Hvert rapporteringsræ kan indeholde alle kombinationer af afdelinger og summeringsenheder, men en rapportdefinition kan kun knyttes til ét rapporteringstræ ad gangen. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Opdatere versionen af Økonomirapportering via slipstreaming

Finans- og driftsapps opdateres hver måned. Økonomirapportering bliver dog ikke nødvendigvis opdateret i samme tempo. Kunderne har desuden flere valgmuligheder, når de implementerer opdateringer til Finans- og driftsapps. Opdateringer af Økonomirapportering installeres automatisk. Økonomirapportering har en angivet version, der forbruges i et kundemiljø, når der implementeres en serviceopdatering, når nedetiden startes, eller når kundens miljø er i vedligeholdelsestilstand. Denne proces kaldes *slipstreaming* eller *true-up*, fordi alle kundeimplementeringen er konfigureret til samme version af Økonomirapportering.

Du kan finde ændringer, der udgives i de enkelte versioner, i [Nyheder eller ændringer i Dynamics 365 Finance](../../finance/get-started/whats-new-home-page.md). Platformsopdateringer og fejlrettelser findes i afsnittet "Yderligere ressourcer" nederst på siden for hver version.

Den valgte slipstreamede version er en gennemset og valideret version af Økonomirapportering, der er klar til produktion. Den er kompatibel med alle tidligere eller fremtidige versioner af Dynamics 365 Finance. Økonomirapportering kan f.eks. være på den seneste 10.0.19 build, mens kunden stadig bruger programversion 10.0.16.

> [!NOTE]
> Det eneste tilfælde, hvor kunderne kan flytte til en tidligere version (et nedgraderingsscenario), forekommer, hvis Microsoft stopper en true-up-udrulning på grund af et problem. Så snart en rettelse er tilgængelig, vil den blive anvendt automatisk.

Slipstream-processen er fuldautomatisk og kræver ingen kundehandling. Tre topologier forbruger slipstream, hver på en lidt anden måde:

- **I det lokale miljø** – Implementering i det lokale miljø understøtter ikke slipstream og true-up.
- **Infrastruktur som en service (IaaS)** – Slipstream-logikken anvendes under alle operationer, der forsøger at opdatere Økonomirapportering. Det omfatter binære opdateringer eller udsendelser, der indeholder binære opdateringer.
- **Selvbetjening** – Alle operationer, der kræver nedetid for Økonomirapportering, anvender slipstream-logikken:

    - Binære opdateringer eller udsendelser, der indeholder binære opdateringer
    - S-programrettelse eller anden nedetid for infrastrukturen
    - AOT-pakkeudrulninger

## <a name="troubleshooting-issues-opening-report-designer"></a>Fejlfinding af problemer med at åbne Report Designer

Der er nogle få almindelige problemer, der kan forårsage problemer, når du åbner Report Designer. Disse problemer og de trin, der skal løses, er som følger.

Problem 1: Report Designer starter ikke, når du vælger **Ny** eller **Rediger**.

* I Internet Explorer skal du vælge **Indstillinger** og derefter vælge **Internetindstillinger**. Vælg fanen **Sikkerhed**. Vælg websteder, du har tillid til, og vælg derefter **Websteder**. I **Føj dette websted til zone** skal du angive "\*\.dynamics.com" (uden anførselstegn) og derefter vælge **Tilføj**. 
* I Internet Explorer skal du vælge **Indstillinger** og derefter vælge **Internetindstillinger**. Vælg fanen **Sikkerhed**. Vælg websteder, du har tillid til. I området, der er angivet med Sikkerhedsniveau for denne zone, skal du ændre indstillingen til **Mellem-Lav**.
* Deaktiver blokering af pop op-vinduer i din browser.
* Der kræves arbejdsstationer for at installere Microsoft .NET Framework 4.7.2 eller nyere. Denne version af Microsoft .NET Framework kan hentes og installeres fra [Microsoft Download Center](https://dotnet.microsoft.com/download/dotnet-framework/net472).
* Hvis du bruger Chrome-browseren, skal du installere en ClickOnce-udvidelse for at hente Report Designer-klienten. Hvis du kører Chrome i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand. Du kan finde flere oplysninger om Chrome ClickOnce-udvidelsen i [Systemkrav til skyinstallationer](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Hvis du bruger Microsoft Edge med en Chrome-browser, behøver du ikke installere en ClickOnce-udvidelse til Edge Chromium. Du skal dog aktivere ClickOnce-indstillingen for at hente rapportdesigner-klienten. Hvis du kører i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand.

    1. Åbn en ny browser i Microsoft Edge.
    2. Angiv **edge://flags**, og vælg **Enter**.
    3. Søg efter indstillingen **ClickOnce Support**, eller brug dette direkte link: **edge://flags/#edge-click-once**.
    4. Angiv indstillingen i rullemenuen til **Aktiveret**.
    5. Vælg **Genstart browser**.

Problem 2: Brugeren har ikke fået tildelt de krævede tilladelser til at bruge Financial Reporting. 

* Hvis du vil kontrollere, om brugeren ikke har tilladelse, skal vælge **Ja** på fejlen "Der kan ikke oprettes forbindelse til Financial Reporting-serveren. Vælg Ja, hvis du vil fortsætte, og angiv en anden serveradresse." Vælg derefter **Test forbindelse**. Hvis du ikke har rettigheder, vises en meddelelse med teksten "forbindelsesforsøg mislykkedes. Brugeren har ikke de rette tilladelser til at oprette forbindelse til serveren. Kontakt din systemadministrator."
* De nødvendige rettigheder vises ovenfor i [Tildele sikkerhedsadgang til Financial Reporting](#granting-security-access-to-financial-reporting). Sikkerhed i Financial Reporting er baseret på disse rettigheder. Du har ikke adgang til dem, medmindre du har fået tildelt disse rettigheder (eller en anden sikkerhedsrolle, der omfatter disse rettigheder). 
* Integrationsopgaven **Firmaets brugere – udbyder til firma** (som også er ansvarlig for og kendt som brugerintegration) kører i et 5-minutters interval. Det kan tage op til 10 minutter, før eventuelle ændringer af tilladelser træder i kraft i Økonomirapportering. 

    Hvis en anden bruger kan åbne Report Designer, skal du vælge **Funktioner** og derefter vælge **Integrationsstatus**. Kontrollér, at integrationstilknytningen "Firmaets bruger – udbyder til firma" kører korrekt, fordi du er tildelt tilladelse til at bruge Økonomirapportering. 

* Det kan være muligt, at en anden fejl har forhindret **Dynamics-bruger til Økonomirapportering-brugerintegration** i at afslutte. Eller er det muligt, at en Datamart-nulstilling er blevet startet og endnu ikke fuldført, eller at der er opstået en anden systemfejl. Prøv at køre processen igen senere. Hvis problemet fortsætter, skal du kontakte din systemadministrator.

Problem 3: Du kan fortsætte efter logonsiden til **ClickOnce Report Designer**, men ikke fuldføre logon i Report Designer. 

* Den tid, der er angivet på din lokale computer, når du angiver dine logonoplysninger, skal være inden for fem minutter efter tiden på serveren til Økonomirapportering. Hvis der er en forskel på mere end fem minutter, vil systemet ikke tillade logon. 
* Hvis tiden på computeren afviger fra tiden på Financial Reporting-serveren, anbefales du at aktivere indstillingen i Windows, så computerens tid indstilles automatisk. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Fejlfinding af Report Designer-problemer med Logbog

Du kan bruge Logbog til at analysere nogle af de problemer, der opstår, når du bruger Financial Reporting. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Hvad sker der, når du har forbindelsesproblemer med Financial Reporting? 

Her er nogle trin, du kan udføre for at gøre din samtale med Microsofts support mere effektiv og give dig en hurtigere løsning. 
 
De følgende trin gennemgår processen til aktivering af meddelelser i Logbog til Financial Reporting. De logfiler, som Logbog genererer, hjælper supportteknikere med at identificere kilden til forbindelsesproblemet hurtigt. Send kopier af disse logfiler sammen med din supportanmodning, når du kontakter support.


1. Kopiér RegisterETW.zip-filen til klientarbejdsstationen (helst Desktop), og udtræk [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122).
2. Sørg for, at Windows Logbog er lukket.
3. Åbn en kommandoprompt for Administrator PowerShell, og gå til den mappe, hvor RegisterETW.ps1 er placeret.
4. Kør følgende kommando: .\RegisterETW.ps1

    Et vellykket output i PowerShell bekræftes med meddelelsen **Fuldført RegisterETW-script**.

    Åbn logbogen igen, og du vil nu se disse logfiler under **Microsoft > Dynamics**:

    * MR-Client
    * MR-DVT
    * MR-Integration
    * MR-Logger
    * MR-Reporting
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Genskab problemet i Report Designer.
6. Eksportér MR-Logger-hændelserne ved hjælp af Logbog.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Fejlfinding af problemer med forbindelse til Financial Reporting

Problem: Du modtager fejlen "Det er ikke muligt at oprette forbindelse til Financial Reporting-serveren".

* Undersøg, om problemet opstår i webbrowserne Chrome og Edge.
* Hvis problemet kun forekommer i én browser, kan det være ClickOnce-problemet. 
* Når du får fejlmeddelelsen om forbindelsen, skal du vælge **Test** for at teste forbindelsen for at se, hvilken meddelelse der vises. 
* Problemet kan være resultatet af en anden bruger, der ikke har adgang til Financial Reporting. Hvis en bruger ikke har adgang, modtager brugeren en meddelelse om, at den ikke har rettigheder.
* Hvis der opstår problemer i flere browsere, skal du kontrollere, at uret på din arbejdsstation er angivet til Automatisk.
* Sammen med en bruger, der har sikkerhedsadministratorrettigheder i Dynamics 365 Finance og administratorrettigheder til netværksdomænet kan du logge på din arbejdsstation for at se, om der er forbindelse. Hvis de kan oprette forbindelse, kan problemet være relateret til netværkstilladelser.
* På arbejdsstationen skal du midlertidigt deaktivere firewallen. Hvis du derefter kan oprette forbindelse til Report Designer, er problemet i din firewall. Du kan løse problemet sammen med din organisations it-afdeling.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Vis økonomiske rapporter](view-financial-reports.md)
- [Rapportering af trædefinitioner i økonomiske rapporter](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
