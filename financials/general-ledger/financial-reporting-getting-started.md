---
title: "Økonomirapportering"
description: "I dette emne beskrives, hvor du kan få adgang til økonomirapportering i Microsoft Dynamics 365 for Operations, og hvordan du bruger funktionerne til økonomirapportering. Den indeholder en beskrivelse af de økonomirapporter, der findes."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Økonomirapportering

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvor du kan få adgang til økonomirapportering i Microsoft Dynamics 365 for Operations, og hvordan du bruger funktionerne til økonomirapportering. Den indeholder en beskrivelse af de økonomirapporter, der findes.

<a name="accessing-financial-reporting"></a>Adgang til økonomirapportering
-----------------------------

Du kan finde menuen **Økonomirapportering** følgende steder i Microsoft Dynamics 365 for Operations:

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
| Opretholde sikker økonomirapportering | Oprethold sikkerhed omkring økonomisk rapportering, og udfør administrative opgaver. | FinancialReportsSecurityMaintain |
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

## <a name="default-reports"></a>Standardrapporter
Økonomirapportering indeholder 22 økonomiske standardrapporter. Hver rapport bruger standardkategorier for hovedkonti i Microsoft Dynamics 365 for Operations. Du kan bruge disse rapporter, som de er, eller du kan bruge dem som udgangspunkt til dine behov for økonomirapportering. Disse standardrapporter omfatter ud over de traditionelle regnskaber, resultatopgørelsen og balancen, rapporter, der viser de forskellige typer økonomiske rapporter, du kan oprette. Hver rapport i den følgende tabel er kædet til en Office-Mix-præsentation om rapporten.

| Standardrapport                                                                                         | Betegnelse                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12-måneders rullende enkelt kolonne resultatopgørelse – standard](https://mix.office.com/watch/76kc7bm3wnt1) | Få vist en organisations rentabilitet for de sidste 12 måneder i en enkelt kolonne.                                                                                                                                                                                                                                      |
| [12-måneders tendensresultatopgørelse – standard](https://mix.office.com/watch/12brmfge5p8r)                 | Få vist en organisations rentabilitet for hver af de sidste 12 måneder. Disse 12 måneder kan spænde over mere end ét regnskabsår.                                                                                                                                                                                             |
| [Faktisk vs. budget – standard](https://mix.office.com/watch/fi439lkwr0no)                                | Få vist detaljerede saldooplysninger for alle konti for det oprindelige budget, og sammenlign det reviderede budget med faktiske oplysninger, der har en afvigelse.                                                                                                                                                                          |
| [Revisionsoplysninger – standard](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser debet- og kreditsaldi i rapporteringsvalutaen og den lokale valuta, sammen med yderligere posteringsoplysninger som bruger-id, den bruger, der senest har ændret data, datoen for den seneste ændring og kladde-id'et. |
| [Saldoliste – standard](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser start- og ultimosaldi og debet- og kreditsaldi for indeværende periode og år til dato samt yderligere posteringsoplysninger som f.eks. bilaget.                                                                    |
| [Balance – standard](https://mix.office.com/watch/zkgq0u7visw9)                                   | Få vist organisationens økonomiske situation for året.                                                                                                                                                                                                                                                             |
| [Balancen og resultatopgørelsen side om side – standard](https://mix.office.com/watch/zkgq0u7visw9) | Få vist organisationens økonomiske situation og indtjening for året ved siden af hinanden.                                                                                                                                                                                                                              |
| [Pengestrøm – projekt](https://mix.office.com/watch/jd3go9pz6390)                                       | Få indblik i de kontanter, der går ind og ud af organisationen.                                                                                                                                                                                                                                   |
| [Detaljeret JE- og TB-revision – standard](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Få vist startsaldo og aktivitetsoplysninger for alle konti.                                                                                                                                                                                                                                                      |
| [Detaljeret råbalance – standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Få vist oplysninger om saldoen for alle konti, der har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.                                                                                                                                  |
| [Tre år kvartalsvise tendens for udgifter – standard](https://mix.office.com/watch/gwm4zu7tmtj8)             | Få indblik i udgifter for de seneste 12 kvartaler i de foregående tre år.                                                                                                                                                                                                                                   |
| [Finansielle overskrifter JE- og TB-revision – standard](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Få vist en oversigt over finansielle overskrifter for saldi og aktivitet for aktivet, ansvar, ejerens egenkapital, indtægter, udgifter, gevinst eller tab.                                                                                                                                                                           |
| [Resultatopgørelse – standard](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Få vist organisationens rentabilitet for den aktuelle periode og år til dato.                                                                                                                                                                                                                                   |
| [Finansposteringsliste – standard](https://mix.office.com/watch/19h9v2rmh48vy)                        | Få vist detaljerede saldooplysninger for alle konti. Denne rapport viser debet- og kreditsaldi sammen med t yderligere posteringsoplysninger såsom posteringsdato, kladdenummer, bilag, typen og sporingsnummer.                                                                            |
| [Nøgletal – standard](https://mix.office.com/watch/b08hfc5h92me)                                          | Få vist soliditet, rentabilitet og efektivitetsnøgletal for organisationen for året.                                                                                                                                                                                                                           |
| [Rullende 12 måneders udgifter – standard](https://mix.office.com/watch/iywod5qmqhz7)                       | Få indblik i udgifter for hvert af de seneste 12 måneder. Disse 12 måneder kan spænde over mere end ét regnskabsår.                                                                                                                                                                                                       |
| [Rullende kvartal resultatopgørelse – standard](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Få vist organisationens rentabilitet på kvartalsvist grundlag for det seneste år og år til dato.                                                                                                                                                                                                                   |
| [Parallel balance – standard](https://mix.office.com/watch/zkgq0u7visw9)                      | Få vist organisationens økonomiske situation for året. Denne rapport viser aktiver og passiver og egenkapital ved siden af hinanden.                                                                                                                                                                                |
| [Råbalanceoversigt – standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.                                                                                                                                                                  |
| [Årlig råbalanceoversigt – standard](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Få vist saldooplysninger for alle konti, der har start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år.                                                                                                                           |
| [Ugentligt salg og rabatter – standard](https://mix.office.com/watch/112ng0hy5de0j)                     | Få indblik i salg og rabatter for hver uge i en måned. Denne rapport omfatter fire uger totalt.                                                                                                                                                                                                              |
| [Tilgængelige budgetmidler - standard](https://mix.office.com/watch/15hcpezcbx7tv)                         | Se en detaljeret sammenligning af det reviderede budget, faktiske udgifter, budgetreservationer og disponible budgetmidler for alle konti                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Startøkonomirapporter
Når du klikker på menuen **Økonomirapportering**, vises listen over økonomiske standardrapporter for firmaet. Du kan derefter åbne eller redigere en rapport. Vælg navnet på rapporten for at åbne en af standardrapporterne. Første gang en rapport åbnes, genereres den automatisk for den foregående måned. For eksempel, hvis du åbner en rapport for første gang i august 2016, oprettes rapporten for 31. juli 2016. Når en rapport er åben, kan du begynde at udforske den ved at foretage detailudledning for bestemte data og ændre rapportindstillinger.

## <a name="creating-and-modifying-financial-reports"></a>Oprettelse og redigering af økonomiske rapporter
Du kan oprette en ny rapport eller ændre en eksisterende rapport på listen over økonomiske rapporter. Hvis du har de nødvendige tilladelser, kan du oprette en ny økonomirapport ved at klikke på **Ny** i handlingsruden. Et rapportdesignerprogram overføres til din enhed. Du kan oprette den nye rapport, når rapportdesigneren er startet. Når du har gemt den nye rapport, vises den på listen over økonomiske rapporter. Listen viser kun rapporter, der er oprettet for det firma, du har brugt i Microsoft Dynamics 365 for Operations. Du kan finde flere oplysninger om processen til oprettelse og redigering af økonomirapporter i Dynamics 365 for Operations i disse [blogindlæg](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) fra bloggen Dynamics Financial Reporting. **Bemærk!** Den computer, du henter rapportdesignerklienten ned på, skal have version 4.6.2 af Microsoft.NET Framework installeret. Denne version af Microsoft .NET Framework kan hentes og installeres [her](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at hente rapportdesigner-klienten. Hvis du kører i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen er aktiveret til incognito-tilstand. Du kan også redigere en rapport, der vises på listen over økonomiske rapporter. Når området omkring rapportnavnet er markeret, skal du klikke på **Rediger** i handlingsruden. Rapportdesignerprogrammet starter.

<a name="see-also"></a>Se også
--------

[Vis økonomirapporter](view-financial-reports.md)

[Dynamics Financial Reporting-blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




