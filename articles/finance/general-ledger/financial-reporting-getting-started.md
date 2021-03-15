---
title: Oversigt over økonomirapportering
description: I dette emne beskrives, hvor du kan få adgang til økonomirapportering i Microsoft Dynamics 365 Finance, og hvordan du bruger funktionerne til økonomirapportering.
author: aprilolson
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24d57982981ca7b72e43c086ace381e420acb06c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975680"
---
# <a name="get-started-with-financial-reporting"></a>Introduktion til Financial Reporting 

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvor du kan få adgang til økonomirapportering, og hvordan du bruger funktionerne til økonomirapportering. Det indeholder også en beskrivelse af eksisterende standardøkonomirapporter.

<a name="accessing-financial-reporting"></a>Adgang til økonomirapportering
-----------------------------

Du kan finde menuen **Financial reporting** følgende steder:

-   **Finans** &gt; **Forespørgsler og rapporter**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Grundlæggende budgettering**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Budgetplanlægning**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Budgetstyring**
-   Konsolideringer

Hvis du vil oprette og generere økonomiske rapporter for en juridisk enhed, skal du angive følgende oplysninger for den pågældende juridiske enhed:

-   Regnskabskalender
-   Ledger
-   Kontoplan
-   Valuta
-   Bogfør en postering på mindst én konto
-   MainAccount vises i kolonnen Valgt i **Finans > Finansopsætning > Opsætning af Financial Reporting**

## <a name="granting-security-access-to-financial-reporting"></a>Tildele sikkerhedsadgang til Financial Reporting
Funktionerne til økonomisk rapportering er tilgængelige for brugere, der har de nødvendige rettigheder og pligter tildelt via deres sikkerhedsroller. I følgende afsnit vises disse rettigheder og pligter samt de tilknyttede roller.

### <a name="duties"></a>Opgaver

| Navn på pligt                            | Beskrivelse                                                             | AOT-navn                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Opretholde sikker økonomirapportering | Oprethold sikkerhed omkring økonomisk rapportering, og udfør administrative opgaver. | FinancialReportsSecurityMaintain |
| Ajourføre økonomiske rapporter            | Udarbejd og vedligehold økonomiske rapporter.                                  | FinancialReportsMaintain         |
| Generere økonomiske rapporter            | Generér og opdater økonomiske rapporter.                                 | FinancialReportsGenerate         |
| Gennemgå driftsregnskaber          | Gennemgå og analyser driftsregnskaber.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Rettigheder

| Rettighedsetiket                       | Beskrivelse                                                             | AOT-navn                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Opretholde sikker økonomirapportering | Oprethold sikkerhed omkring økonomisk rapportering, og udfør administrative opgaver. | FinancialReportsSecuritySystemMaintain |
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

Når en bruger er tilføjet, eller en rolle er ændret, bør brugeren kunne få adgang til økonomirapportering inden for få minutter. 

> [!NOTE]
> Rollen sysadmin føjes til alle roller i Financial Reporting.

## <a name="report-deletions-and-expirations"></a>Rapportér sletninger og udløbsdatoer
Brugere, der genererer en rapport, kan slette deres egne rapporter. Brugere med pligten **Ajourføring af sikker økonomirapportering** kan slette andres rapporter. 

Begrebet udløbsdato blev introduceret i version 10.0.8. En ny påkrævet funktion aktiveres på siden **Alle** i arbejdsområdet til administration af funktioner. Funktionen **Opbevaringspolitikker for økonomiske rapporter** indeholder følgende ændringer:
* Nyligt genererede rapporter markeres automatisk som havende en udløbsdato på 90 dage fra det tidspunkt, hvor de genereres.
* Alle eksisterende rapporter fra før funktionen blev installeret, får en udløbsperiode på 90 dage. Datoen kan blive vist som tom i en kort periode frem til tjenesten regnskabsrapportering kører, en rapport genereres, og tjenesten udfører opdateringen til eksisterende rapporter med en tom udløbsdato. 
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


## <a name="troubleshooting-issues-opening-report-designer"></a>Fejlfinding af problemer med at åbne Report Designer
Der er nogle få almindelige problemer, der kan forårsage problemer, når du åbner Report Designer. Disse problemer og de trin, der skal løses, er som følger.

Problem 1: Report Designer starter ikke, når du vælger **Ny** eller **Rediger**.

* I Internet Explorer skal du vælge **Indstillinger** og derefter vælge **Internetindstillinger**. Vælg fanen **Sikkerhed**. Vælg websteder, du har tillid til, og vælg derefter **Websteder**. I **Føj dette websted til zone** skal du angive "\*\.dynamics.com" (uden anførselstegn) og derefter vælge **Tilføj**. 
* I Internet Explorer skal du vælge **Indstillinger** og derefter vælge **Internetindstillinger**. Vælg fanen **Sikkerhed**. Vælg websteder, du har tillid til. I området, der er angivet med Sikkerhedsniveau for denne zone, skal du ændre indstillingen til **Mellem-Lav**.
* Deaktiver blokering af pop op-vinduer i din browser.
* Der kræves arbejdsstationer for at installere Microsoft .NET Framework 4.6.2 eller nyere. Denne version af Microsoft .NET Framework kan hentes og installeres fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345).
* Hvis du bruger Chrome-browseren, skal du installere en ClickOnce-udvidelse for at hente Report Designer-klienten. Hvis du kører Chrome i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand. Du kan finde flere oplysninger om Chrome ClickOnce-udvidelsen i [Systemkrav til skyinstallationer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements).
* Hvis du bruger Microsoft Edge med en Chrome-browser, behøver du ikke installere en ClickOnce-udvidelse til Edge Chromium. Du skal dog aktivere ClickOnce-indstillingen for at hente rapportdesigner-klienten. Hvis du kører i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand.
     1. Åbn en ny browser i Microsoft Edge.
     2. Angiv **edge://flags**, og vælg **Enter**.
     3. Søg efter indstillingen **ClickOnce Support**, eller brug dette direkte link: **edge://flags/#edge-click-once**.
     4. Angiv indstillingen i rullemenuen til **Aktiveret**.
     5. Vælg **Genstart browser**.

Problem 2: Brugeren har ikke fået tildelt de krævede tilladelser til at bruge Financial Reporting. 

* Hvis du vil kontrollere, om brugeren ikke har tilladelse, skal **Ja** på fejlen "Der kunne ikke oprettes forbindelse til serveren til Financial Reporting. Vælg Ja, hvis du vil fortsætte, og angiv en anden serveradresse. " Vælg derefter **Test forbindelse**. Hvis du ikke har rettigheder, vises en meddelelse med teksten "forbindelsesforsøg mislykkedes. Brugeren har ikke de rette tilladelser til at oprette forbindelse til serveren. Kontakt din systemadministrator."
* De nødvendige rettigheder vises ovenfor i [Tildele sikkerhedsadgang til Financial Reporting](#granting-security-access-to-financial-reporting). Sikkerhed i Financial Reporting er baseret på disse rettigheder. Du har ikke adgang til dem, medmindre du har fået tildelt disse rettigheder (eller en anden sikkerhedsrolle, der omfatter disse rettigheder). 
* Integrationsopgaven **Firmaets brugere – udbyder til firma** (som også er ansvarlig for og kendt som brugerintegration) kører i et 5-minutters interval. Det kan tage op til 10 minutter, før eventuelle ændringer af tilladelser træder i kraft i Financial Reporting. 
  Hvis en anden bruger kan åbne Report Designer, skal du vælge **Funktioner** og derefter vælge **Integrationsstatus**. Kontroller, at integrationstilknytningen "Firmaets bruger – udbyder til firma" kører korrekt, fordi du er tildelt tilladelse til at bruge Financial Reporting. 
* Det kan være muligt, at en anden fejl har forhindret **Dynamics-bruger til Financial Reporting-brugerintegration** i at afslutte. Eller er det muligt, at en Datamart-nulstilling er blevet startet og endnu ikke fuldført, eller at der er opstået en anden systemfejl. Prøv at køre processen igen senere. Hvis problemet fortsætter, skal du kontakte din systemadministrator.

Problem 3: Du kan fortsætte efter logonsiden til ClickOnce Report Designer, men de ikke fuldføre logon i Report Designer. 

* Den tid, der er angivet på din lokale computer, når du angiver dine logonoplysninger, skal være inden for fem minutter efter tiden på serveren til Financial Reporting. Hvis der er en forskel på mere end fem minutter, vil systemet ikke tillade logon. 
* I dette tilfælde anbefales det, at du aktiverer Windows-indstillingen til automatisk at indstille pc'ens tid. 

## <a name="additional-resources"></a>Yderligere ressourcer
- [Vis økonomiske rapporter](view-financial-reports.md)
- [Rapportering af trædefinitioner i økonomiske rapporter](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]