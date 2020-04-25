---
title: Oversigt over økonomirapportering
description: I dette emne beskrives, hvor du kan få adgang til økonomirapportering i Microsoft Dynamics 365 Finance, og hvordan du bruger funktionerne til økonomirapportering. Den indeholder en beskrivelse af de økonomirapporter, der findes.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01fcc7c4f3e1eb7aadfc93b120cd57e62077d0c0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249054"
---
# <a name="financial-reporting-overview"></a>Oversigt over økonomirapportering

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvor du kan få adgang til økonomirapportering, og hvordan du bruger funktionerne til økonomirapportering. Det indeholder også en beskrivelse af eksisterende standardøkonomirapporter.

<a name="accessing-financial-reporting"></a>Adgang til økonomirapportering
-----------------------------

Du kan finde menuen **Økonomirapportering** følgende steder:

-   **Finans** &gt; **Forespørgsler og rapporter**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Grundlæggende budgettering**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Budgetplanlægning**
-   **Budgettering** &gt; **Forespørgsler og rapporter** &gt; **Budgetstyring**
-   Konsolideringer

Hvis du vil oprette og generere økonomiske rapporter for en juridisk enhed, skal du angive følgende oplysninger for den pågældende juridiske enhed:

-   Regnskabskalender
-   Finans
-   Kontoplan
-   Valuta

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

Når en bruger er tilføjet, eller en rolle er ændret, bør brugeren kunne få adgang til økonomirapportering inden for få minutter. **Bemærk!** Rollen sysadmin føjes til alle roller i økonomirapportering.

## <a name="report-deletions-and-expirations"></a>Rapportér sletninger og udløbsdatoer
Brugere, der genererer en rapport, kan slette deres egne rapporter. Brugere med pligten **Ajourføring af sikker økonomirapportering** kan slette andres rapporter. 

Fra og med udgivelse 10.0.7 er begrebet udløbsdatoer blevet introduceret. En ny obligatorisk funktion vil blive aktiveret i arbejdsområdet administration af funktioner. Denne funktion indeholder følgende ændringer:
* Nyligt genererede rapporter markeres automatisk som havende en udløbsdato på 90 dage fra det tidspunkt, hvor de genereres
* Alle eksisterende rapporter fra før funktionen blev installeret, får en udløbsperiode på 90 dage. Datoen kan blive vist som tom i en kort periode frem til tjenesten regnskabsrapportering kører, en rapport genereres, og tjenesten udfører opdateringen til eksisterende rapporter med en tom udløbsdato. 
* Brugere med **Ajourføring af sikker økonomirapportering** har adgang til denne funktionalitet. Enhver bruger i pligten **Ajourføring af økonomiske rapporter**, som er blevet tildelt rettigheden **Ajourføring af udløb af økonomiske rapporter**, vil også have mulighed for at ændre udløbsperioden. I øjeblikket er der to tilbageholdelsesmuligheder til rådighed - 
  * et udløb på 90 dage
  * en mulighed for at indstille, at rapporten aldrig skal udløbe

Når der vælges en udløbsfrist på 90 dage, løber de 90 dage fra i dag, hvilket er forskelligt fra de 90 dage fra den oprindelige generationsdato, der er angivet under generering af rapporter. 

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
| Detaljeret råbalance – standard                         | Få vist oplysninger om saldoen for alle konti, der har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.                                                                                                                                  |
| Tre år kvartalsvise tendens for udgifter – standard             | Få indblik i udgifter for de seneste 12 kvartaler i de foregående tre år.                                                                                                                                                                                                                                   |
| Finansielle overskrifter JE- og TB-revision – standard            | Få vist en oversigt over finansielle overskrifter for saldi og aktivitet for aktivet, ansvar, ejerens egenkapital, indtægter, udgifter, gevinst eller tab.                                                                                                                                                                           |
| Resultatopgørelse – standard                                | Få vist organisationens rentabilitet for den aktuelle periode og år til dato.                                                                                                                                                                                                                                   |
| Finansposteringsliste – standard                        | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser debet- og kreditsaldi sammen med t yderligere posteringsoplysninger såsom posteringsdato, kladdenummer, bilag, typen og sporingsnummer.                                                                            |
| Nøgletal – standard                                          | Få vist soliditet, rentabilitet og efektivitetsnøgletal for organisationen for året.                                                                                                                                                                                                                           |
| Rullende 12 måneders udgifter – standard                       | Få indblik i udgifter for hvert af de seneste 12 måneder. Disse 12 måneder kan spænde over mere end ét regnskabsår.                                                                                                                                                                                                       |
| Rullende kvartal resultatopgørelse – standard               | Få vist organisationens rentabilitet på kvartalsvist grundlag for det seneste år og år til dato.                                                                                                                                                                                                                   |
| Parallel balance – standard                      | Få vist organisationens økonomiske situation for året. Denne rapport viser aktiver og passiver og egenkapital ved siden af hinanden.                                                                                                                                                                                |
| Råbalanceoversigt – standard                          | Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.                                                                                                                                                                  |
| Årlig råbalanceoversigt – standard           | Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.                                                                                                                           |
| Ugentligt salg og rabatter – standard                     | Få indblik i salg og rabatter for hver uge i en måned. Denne rapport omfatter fire uger totalt.                                                                                                                                                                                                              |
| Tilgængelige budgetmidler - standard                         | Se en detaljeret sammenligning af det reviderede budget, faktiske udgifter, budgetreservationer og disponible budgetmidler for alle konti                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Startøkonomirapporter
Når du klikker på menuen **Økonomirapportering**, vises listen over økonomiske standardrapporter for firmaet. Du kan derefter åbne eller redigere en rapport. Vælg navnet på rapporten for at åbne en af standardrapporterne. Første gang en rapport åbnes, genereres den automatisk for den foregående måned. For eksempel, hvis du åbner en rapport for første gang i august 2016, oprettes rapporten for 31. juli 2016. Når en rapport er åben, kan du begynde at udforske den ved at foretage detailudledning for bestemte data og ændre rapportindstillinger.

## <a name="creating-and-modifying-financial-reports"></a>Oprettelse og redigering af økonomiske rapporter
Du kan oprette en ny rapport eller ændre en eksisterende rapport på listen over økonomiske rapporter. Hvis du har de nødvendige tilladelser, kan du oprette en ny økonomirapport ved at klikke på **Ny** i handlingsruden. Et rapportdesignerprogram overføres til din enhed. Du kan oprette den nye rapport, når rapportdesigneren er startet. Når du har gemt den nye rapport, vises den på listen over økonomiske rapporter. Listen viser kun rapporter, der er oprettet for det firma, du bruger i Finance. 

> [!NOTE] 
> Den computer, du henter rapportdesignerklienten ned på, skal have version 4.6.2 af Microsoft .NET Framework installeret. Denne version af Microsoft .NET Framework kan hentes og installeres fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345). Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at hente rapportdesigner-klienten. Hvis du kører i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand. Du kan også redigere en rapport, der vises på listen over økonomiske rapporter. Når området omkring rapportnavnet er markeret, skal du klikke på **Rediger** i handlingsruden. Rapportdesignerprogrammet starter.

## <a name="additional-resources"></a>Yderligere ressourcer
- [Se økonomiske rapporter](view-financial-reports.md)



