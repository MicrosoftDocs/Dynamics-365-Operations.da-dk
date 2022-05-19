---
title: Ofte stillede spørgsmål vedrørende Økonomirapportering
description: Dette emne indeholder svar på nogle ofte stillede spørgsmål om Økonomirapportering.
author: jinniew
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5e0702864815c630f35e3f5b753ece1cb1daa71
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722290"
---
# <a name="financial-reporting-faq"></a>Ofte stillede spørgsmål vedrørende Økonomirapportering

Dette emne indeholder svar på ofte stillede spørgsmål om Økonomirapportering.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvordan begrænser jeg adgangen til en rapport ved hjælp af sikkerhedstræet?

I følgende eksempel vises, hvordan du kan begrænse adgangen til en rapport ved hjælp af sikkerhedstræet.

USMF-demofirmaet indeholder rapporten **Finansbalance**, som ikke alle brugere af Økonomirapportering bør have adgang til. Du kan bruge sikkerhedstræet til at begrænse adgangen til en enkelt rapport, så kun specifikke brugere kan få adgang til rapporten.

1. Log på Financial Reporter Report Designer.
2. Vælg **Fil \> Ny \> Trædiagramdefinition** for at oprette en ny trædiagramdefinition.
3. Tryk to gange (eller dobbeltklik) på linjen **Oversigt** i kolonnen **Enhedssikkerhed**.
4. Vælg **Brugere og Grupper**.
5. Vælg de brugere eller grupper, der kræver adgang til rapporten.
6. Vælg **Gem**.
7. Tilføj den nye trædefinition i rapportdefinitionen.
8. Vælg **Indstilling** i trædefinitionen. Vælg derefter **Medtag alle enheder** under **Valg af rapporteringsenhed**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvordan identificerer jeg, hvilke konti der ikke svarer til mine saldi?

Når du har en rapport, der ikke har tilsvarende saldi, kan du bruge følgende procedurer til at identificere hver konto og afvigelse.

### <a name="in-financial-reporter-report-designer"></a>I Financial Reporter Report Designer

1. Opret en ny rækkedefinition.
2. Vælg **Rediger \> Indsæt rækker fra dimensioner**.
3. Vælg **MainAccount**.
4. Vælg **OK**.
5. Gem rækkedefinitionen.
6. Opret en ny kolonnedefinition.
7. Opret en ny rapportdefinition.
8. Vælg **Indstillinger**, og fjern markering af denne indstilling.
9. Opret rapporten. 
10. Eksporter rapporten til Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>I Dynamics 365 Finance

1. Gå til **Finans \> Forespørgsler og rapporter \> Råbalance**.
2. Angiv følgende felter:

    - **Fra dato** – Angiv startdatoen for regnskabsåret.
    - **Til dato** – Angiv den dato, rapporten skal genereres for.
    - **Økonomisk dimension** – Angiv dette felt til **Hovedkontosæt**.

3. Vælg **Beregn**.
4. Eksporter rapporten til Excel.

Du skal nu kunne kopiere data fra Excel-rapporten i Financial Reporter til rapporten **Råbalance**, så du kan sammenligne kolonnerne **Ultimosaldo**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Når jeg designer en rapport i Report Designer, eller når jeg opretter en økonomisk rapport, får jeg følgende meddelelse: "Operationen kunne ikke fuldføres pga. problemer i dataproviderstrukturen." Hvordan skal jeg svare?

Meddelelsen angiver, at der opstod et problem, da systemet forsøgte at hente økonomiske metadata fra datacentret, mens du brugte Økonomirapportering. Du kan løse dette problem på to måder:

- Gennemse dataintegrationsstatus ved at gå til **Værktøjer \> Integrationsstatus** i Report Designer. Hvis integrationen ikke er fuldført, skal du vente, indtil den er fuldført. Derefter skal du prøve at gentage det, du var i gang med, da du modtog meddelelsen.
- Kontakt Support for at identificere og arbejde dig gennem problemet. Der kan være uoverensstemmende data i systemet. Supportteknikere kan hjælpe dig med at identificere dette problem på serveren og finde de specifikke data, der muligvis skal opdateres.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Hvordan påvirker valget af historisk satsoversættelse rapportens ydeevne?

Den historiske kurs bruges typisk med overført overskud, ejendom, udstyr og egenkapital. Den historiske kurs kan være påkrævet på baggrund af retningslinjerne fra FASB (Financial Accounting Standards Board) eller almindeligt anerkendte regnskabsprincipper (GAAP). Du kan finde flere oplysninger under [Valutaegenskaber i regnskabsaflæggelse](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Hvor mange valutakurstyper findes der?

Der findes tre typer:

- **Aktuel kurs** – Denne type bruges typisk ved statuskonti. Det kaldes normalt *valutakursen på stedet* og kan være kursen den sidste dag i måneden eller en anden foruddefineret dato.
- **Gennemsnitskurs** – Denne type bruges typisk til resultatopgørelseskonti (driftskonti). Du kan konfigurere gennemsnitssatsen til enten at angive et simpelt gennemsnit eller et vægtet gennemsnit.
- **Historisk kurs** - Denne type bruges typisk med overført overskud, ejendom, udstyr og egenkapital. Disse konti kan være obligatoriske i henhold til retningslinjer fra FASB eller GAAP.

## <a name="how-does-historical-currency-translation-work"></a>Hvordan fungerer omregning af historisk valuta?

Satserne er specifikke for posteringsdatoen. Derfor oversættes hver enkelt postering individuelt baseret på den nærmeste valutakurs.

Ved historisk valutaomregning kan de foruddefinerede periodesaldi bruges i stedet for individuelle posteringsoplysninger. Denne funktionsmåde er forskellig fra funktionaliteten for aktuel satsoversættelse.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Hvordan påvirker historisk valutaoversættelse ydeevnen?

Når de data, der vises i rapporterne, opdateres, kan der ske en forsinkelse, fordi beløb skal genberegnes ved at kontrollere posteringsoplysningerne. Denne forsinkelse udløses, hver gang satserne opdateres eller flere posteringer bogføres. Hvis der f.eks. konfigureres tusindvis af konti til historikoversættelse flere gange om dagen, kan der komme en forsinkelse på op til en time, før dataene i rapporten opdateres. Hvis der derimod er et mindre antal specifikke konti, kan procestiden for opdateringer af rapportdata reduceres til minutter eller mindre.

Når der genereres rapporter ved hjælp af valutaomregning for konti af typen Historisk type, vil der ligeledes blive foretaget en ekstra beregning pr. postering. Afhængigt af antallet af konti kan den tid, der oprettes for rapporter, være mere end dobbelt så mange.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Hvad er de forkalkuleret datacenterintegrationsintervaller?

Financial Reporter bruger 16 opgaver til at kopiere data fra Dynamics 365 Finance til Financial Reporter-databasen. Følgende tabel indeholder disse 16 opgaver og viser det interval, der angiver, hvor ofte hver opgave køres. Intervallerne kan ikke ændres.

| Navn                                                       | Interval | Tidsmåling for interval |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 Kontokategorier til kontokategori            | 41       | Minutter         |
| AX 2012 Konti til konto                                | 7        | Minutter         |
| AX 2012 Virksomheder til virksomhed                               | 300      | Sekunder         |
| AX 2012 Virksomheder til organisation                          | 23       | Minutter         |
| AX 2012 Dimensionskombinationer til dimensionskombination    | 1        | Minutter         |
| AX 2012 Dimensionsværdier til dimensionsværdi                | 11       | Minutter         |
| AX 2012 Dimensioner til dimension                            | 31       | Minutter         |
| AX 2012 Valutakurser til valutakurs                    | 17       | Minutter         |
| AX 2012 Regnskabsår til regnskabsår                        | 13       | Minutter         |
| AX 2012 Finanstransaktioner til fakta                | 1        | Minutter         |
| AX 2012 Organisationshierarkier til træ                   | 3,600    | Sekunder         |
| AX 2012 Scenarier til scenarie                              | 29       | Minutter         |
| AX 2012 Transaktionstypekvalifikatorer til faktatypekvalifikatorer | 19       | Minutter         |
| Vedligeholdelsesopgave                                           | 1        | Minutter         |
| MR-rapportdefinitioner til AX7 økonomiske rapporter             | 45       | Sekunder         |
| MR-rapportversioner til AX Regnskabsrapportversioner         | 45       | Sekunder         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
