---
title: Oversigt over konsolidering og eliminering
description: "Denne artikel indeholder generelle oplysninger om konsoliderings- og elimineringsprocessen. Den indeholder svar på nogle ofte stillede spørgsmål."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 3868605826e3c6f0714736ffa8630d1569e17d6f
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-and-elimination-overview"></a>Oversigt over konsolidering og eliminering

Denne artikel indeholder generelle oplysninger om konsoliderings- og elimineringsprocessen. Den indeholder svar på nogle ofte stillede spørgsmål.

Når du konsoliderer data, kombineres de økonomiske resultater for flere datterselskaber til ét konsolideret regnskab. Datterselskaber kan være i forskellige versioner eller systemer, de ejes måske ikke fuldt ud, og de kan bruge forskellige valutaer. Der er flere muligheder for konsolidering af data:

-   **Konsolider online** – Denne indstilling konsoliderer daglige saldi efter de valgte konti og dimensioner og gemmer dem i et konsolideret regnskab.
-   **Økonomirapportering** – Denne indstilling gør det muligt at konsolidere posteringer og saldi, og kan genereres når som helst. Der kan oprettes flere niveauer af hierarkier, og du kan få vist flere rapporteringsvalutaer.
-   **Konsolider med import** – Denne indstilling importerer saldi til et konsolideret regnskab.
-   **Eksportér virksomhedssaldi** – Denne indstilling leverer en eksportfil med virksomhedssaldi. Filen kan derefter importeres til andre forekomster eller systemer. Økonomirapportering kan også bruges til at eksportere saldi til en Microsoft Excel-fil.

Elimineringer kan rapporteres på flere måder:

-   Elimineringsregler kan oprettes i systemet og kan derefter behandles under konsolideringsprocessen eller via et elimineringsforslag. Reglerne kan bogføres for enhver virksomhed, der har **Brug til økonomisk eliminering** valgt i opsætningen af juridisk enhed.
-   Der kan oprettes et separat regnskab, som kan bruges til manuelt at bestemme og bogføre elimineringstransaktioner. Dette kan bruges i konsolideringsprocessen eller til økonomirapportering.
-   Konti og økonomiske dimensioner, der bruges til at bestemme intern aktivitet, kan filtreres ud fra en række- eller kolonnedefinition i økonomirapportering, og der kan bruges komplette detailudledningsfunktioner. En beregnet kolonne eller række kan derefter bruges til at fjerne kontiene og de økonomiske dimensioner fra den konsoliderede total.

Der er mange konsolideringsscenarier, og de enkelte metoder kan håndtere scenarierne på forskellige måder.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål
1.  Jeg foretrækker at bogføre elimineringer i en database. Hvilke muligheder har jeg?

Du har flere muligheder. Du kan bruge indstillingen **Konsolider online** og medtage elimineringer under processen eller som et forslag. Posteringerne bogføres i det konsoliderede regnskab. Du kan også have et separat regnskab, som du manuelt opretter elimineringerne i og derefter bruge dette regnskab i økonomirapportering eller i konsolideringsprocessen.

2.  Vi skal bruge vores konsoliderede resultater i flere rapporteringsvalutaer.

Indstillingen **Økonomirapportering** har ubegrænset rapporteringsvalutaer. Data oversættes under oprettelse af rapporten baseret på valutakurstype og den metode til valutaomregning, der er angivet i hovedkontoen. Indstillingen **Konsolider online** har imidlertid kun én rapporteringsvaluta, og der kræves et konsolideret regnskab for hver rapporteringsvaluta, hvis du bruger denne indstilling. Indstillingen **Økonomirapportering** er den anbefalede metode.

3.  Jeg vil have vist detaljer på transaktionsniveau for hvert regnskab.

Indstillingen **Økonomirapportering** er løsningen, fordi du kan få vist detaljer på transaktionsniveau for så mange virksomheder, som er medtaget i definitionen af rapporteringstræet.

4.  Vi bruger budgetplanlægning eller budgetstyring, og det skal konsolideres.
Indstillingen **Økonomirapportering** er løsningen til at konsolidere budgetplanlægnings- eller budgetkontroldata.

5.  Vores datterselskaber er spredt over hele verden, og vi har flere kontoplaner. Hvad er den bedste metode til konsolidering af vores data?

Du har flere muligheder, når du skal kunne håndtere flere kontoplaner. Du kan bruge indstillingen **Konsolider online** og derefter vælge at bruge enten den koncernkonto, der er defineret for hovedkontoen, eller en koncernkontogruppe. Du kan også bruge indstillingen **Økonomirapportering**, medtage flere links til de økonomiske dimensioner i rækkedefinitionen og tilknytte kontiene.

6.  Vi kræver flere niveauer af konsolidering. Med andre ord konsoliderer vi først vores europæiske datterselskaber til det britiske pund (GBP). Vi tager derefter disse data og konverterer det konsoliderede beløb til US dollar. Hvordan kan vi gøre det?

Når der kræves flere niveauer af konsolidering, og der bruges forskellige valutaer på hvert niveau, skal du bruge indstillingen **Konsolider online**. Der skal oprettes flere konsoliderede regnskaber, der har forskellige regnskabs- og rapporteringsvalutaer. Konsolideringen skal derefter køres flere gange. Indstillingen **Økonomirapportering** oversættes altid fra hver kildevirksomheds regnskabsvaluta til den valgte valuta.

7.  Vi har datterselskaber på et andet system. Hvordan kan vi konsolidere dem?

Brug indstillingen **Konsolider med import** for at hente saldiene til et konsolideret regnskab.

8.  Vi ejer ikke nogle af vores datterselskaber fuldt ud. Hvad er den bedste metode til konsolidering af dem?

Du har flere muligheder for delvist ejede datterselskaber. Ved hjælp af indstillingen **Økonomirapportering** kan du oprette en definition af rapporteringstræet og ejerskabet. Du kan også bruge en beregnet række eller kolonne til at repræsentere det delvist ejede beløb. Du kan endda vise minoritetsinteressen som en separat række i en rapport. Du kan også bruge indstillingen **Konsolider online**. Fanen **Juridiske enheder** har en kolonne, **Ejerskab**, hvor du kan definere den procentdel, der ejes af moderselskabet.

9.  Vores organisation skal vise konsolideringer efter virksomhedsenhed eller ønsker at bruge organisationshierarkier.

Indstillingen **Økonomirapportering** er løsningen. Organisationshierarkier, der er juridiske enheder eller økonomiske dimensioner i dem, kan rapporteres i Økonomirapportering. Du kan også oprette dine egne hierarkier med flere niveauer ved hjælp af en definition på et rapporteringstræ, der har en kombination af juridiske enheder og dimensionsværdier.

10. Vi har mere end én forekomst af systemet.

Ved at bruge indstillingen **Eksportér virksomhedssaldi** til at eksportere fra én forekomst og derefter bruge indstillingen **Konsolider med import** i den anden forekomst, kan du konsolidere dataene.


Yderligere oplysninger finder du i [revalution af valuta i et konsolideret regnskab](\finanicials\general-ledger\currency-revaluation-consolidation-company).

