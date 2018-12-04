---
title: Administration af handelsrabat
description: Dette emne indeholder beskrivelser af administration af handelsrabat til Microsoft Dynamics 365 for Finance and Operations.
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c3794535cf9230389d7da3f9dbde010e5c48cf2f
ms.openlocfilehash: 907d59f850d8d761e2dd4e04bd288a696f00964d
ms.contentlocale: da-dk
ms.lasthandoff: 08/17/2018

---

# <a name="trade-allowance-management"></a>Administration af handelsrabat

[!include [banner](../includes/banner.md)]

Administration af handelsrabat hjælper virksomheder med at håndtere kampagneprogrammer, der tilbyder monetære belønninger i form af "præstationsløn" til de detailhandelskunder, som når mængde- og funktionsmæssige mål. Funktionens egenskaber er udviklet til virksomheder, der fokuserer på omfattende processer til fremme af fortjeneste, fra budgettering og fordeling af kampagnemidler til opsætning af rabatkontrakt, kravoprettelse og -behandling, betalingsprocesser og endelig til analyse af kampagneeffektivitet.


Denne artikel giver en bred oversigt over funktionen til administration af handelsrabat, så du kan få et indblik i de opgaver, der typisk skal udføres ved administration af et kampagneprogram. Forskellige typer brugere, der har ansvaret for drift og beslutningstagning, forventes at bruge denne funktion til at opnå deres respektive mål:

- Tildele skønsmæssige midler til valgte konti og konfigurere handelsrabataftaler for kampagner, baseret på tilbagefaktureringer og betalinger af engangsbeløb (for en aftalt tjeneste)
- Køre de aftalte kampagnekontrakter via igangværende salg og generering af tilbagefaktureringskrav
- Beregning, godkendelse og behandling af de genererede krav og overførsel af dem til Debitor som fradrag for udligning af betaling
- Afstemning af kundens delbetalinger med det fradrag, der er forfaldent
- Registrere brugen af markedsføringsmidlerne og rentabilitet og effektivitet af evalueringsprogram

## <a name="audience-and-purpose"></a>Målgruppe og formål

Oplysningerne i dette dokument er beregnet til forretningsbeslutningstagere i større virksomheder, f.eks. i stillinger som indkøbschef, regnskabsdirektør (CFO) og regnskabschef, der har følgende ansvarsområder:

- Budgetter på højt niveau og fordelingen af midler
- Planlægge og analysere salgskampagner
- Administration af personale, der behandler tilbagefaktureringskrav, kører betalinger på baggrund af merchandizinghændelser og udligner delbetalinger og fradrag

Personer i disse roller har brug for måder til at nå disse mål:

- Forbedret anvendelse af markedsføringsmidler.
- Fleksibel tilpasning af forskellige typer kampagneprogrammer og rabatter.
- Reducer den administrative byrde og de fejl, der er knyttet til overvågningen af ydeevnen for kampagner og behandlingen af krav.
- Forbedre likviditetsbudgetteringen ved at periodisere fremtidige passiver.
- Få et kvantificeret grundlag for løbende og fremtidige forhandlinger med kunder om kampagner.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Markedsføringsmidler og handelsrabataftale

En handelsrabat er et incitamentsprogram, hvor der tilbydes monetære belønninger i form af præstationsløn til kunder, der når målene for bestemte mængder og/eller funktionsmæssige mål. Markedsføringsmidler er budgetterede udgifter. På denne måde kan salgsfremmende kampagner hentes.

### <a name="promotional-fund"></a>Markedsføringsmidler

Midler, der er fordelt på handelsrabataftaler, registreres på siden **Midler**. Du kan åbne siden **Midler** ved at vælge **Salgs og marketing** \> **Handelsrabatter** \> **Midler** \> **Midler**.

![Siden Midler](./media/trade-allowance-management-funds-page.png "Siden Midler")

På siden **Midler** kan du få vist detaljer om markedsføringsmidler.

Oversigtspanelet **Generelt** viser den periode, midlet gælder i, og det budgetterede beløb. Når midlerne skal fordeles til markedsføringsaftalen, skal feltet **Status** have værdien **Godkendt**.

Oversigtspanelet **kunder** viser kundehierarkiet. Du kan vælge de kunder, som er mål for midlerne, ved at trække dem, så de er under **Fondskunder**. Dette oversigtspanel viser også, hvordan det samlede beløb i midlerne er fordelt.

Oversigtspanelet **Varer** viser de varer, der er inkluderet i markedsføringen.

### <a name="trade-allowance-agreement"></a>Aftale om handelsrabat

Når definitionen af midler er på plads, er næste trin i planlægning af markedsføringen at registrere markedsføringskontrakter (som kaldes handelsrabataftale), tildele midler og definere præstationsmål for hver merchandizinghændelse.

Rabathandelsaftaler registreres på siden **Aftaler om handelsrabat**. Du kan åbne siden **Aftaler om handelsrabat** ved at vælge **Salg og marketing** \> **Handelsrabatter** \> **Aftaler om handelsrabat**.

![Siden Aftaler om handelsrabat](./media/trade-allowance-management-agreements-page.png "Siden Aftaler om handelsrabat")

#### <a name="header"></a>Hoved

Vælg **Hoved** for at skifte til Overskriftsvisning.

Felterne **Ordre til** og **Ordre fra** i oversigtspanelet **Generelt** definerer den periode, hvor aftalen er gyldig. Godkendelsesstatus **Godkendt internt** for aftalen angiver, at aftalen endnu ikke er gyldig og ikke kan anvendes under behandling af salgsordrer.

Sektionen **Analyse** i oversigtspanelet **Generelt** indeholder vigtige felter, der definerer de mængder og omkostninger, der bruges til evaluering af markedsføringen:

- Feltet **Basisenheder** angiver antallet af produkter, der skal sælges til de valgte kunder, før kampagnen anvendes.
- Værdien **Beregnet afsendelsesantal** beregnes ud fra værdien **Løft i procent**, der er en stigning i planlagte mål for kampagnen.
- Feltet **Handelsrabatomkostninger** beregnes baseret på antallet af de forskellige hændelser i handelsrabataftalen.

I oversigtspanelet **Kunder** kan du på listen til venstre vælge og få vist kundegrupper, der er konfigureret som foruddefinerede hierarkier. Du kan derefter vælge hele hierarkiet eller bestemte konti som mål for rabataftalen.

I oversigtspanelet **Varer**, f.eks. oversigtspanelet **Varer** på siden **Midler**, føjes produkter til aftalen for at tilknytte dens salg med den rabat, der blev aftalt.

Du kan se de markedsføringsmidler, der er tilknyttet denne kontrakt, i oversigtspanelet **Midler**. Du kan også få vist kontraktens hændelsesomkostningsfordeling. En hændelsesomkostningsfordeling på 100 % betyder, at denne kampagne vil blive finansieret udelukkende fra én finansieringskilde. En kampagne kan også udnytte flere midler og kan bruge identisk eller differentieret procentvis fordeling.

#### <a name="lines"></a>Linjer

Vælg derefter **Linjer** for at skifte til visningen Linjer.

Fanen **Merchandizinghændelser** viser de typer af hændelser, der er omfattet af en aftale. Der er tre typer: tilbagefakturering, engangsbeløb og uden for faktura.

Når du vælger merchandizinghændelsen og derefter vælge fanen **Beløb**, findes oplysninger om hændelsen.

![Linjer til handelsrabataftale](./media/trade-allowance-management-agreements-lines.png "Linjer til handelsrabataftale")

I sektionen **Handelsrabatlinjer** skal du angive antal- eller beløbsområder, som kunden skal opnå, for at definitioner kan opnå belønninger.

Hvis merchandizinghændelsen er af typen **Tilbagefakturer**, definerer den øverste sektion under fanen **Beløb** de regler, som tilbagefaktureringen skal anvendes, genereres og betales under. Reglerne kan for eksempel angive følgende betingelser for tilbagefaktureringskravet:

- Det er baseret på oprettelsesdatoen for salgsordren (værdien i **Beregningsdatotype** er **Oprettet**).
- Det beregnes ud fra salgsordrelinjens beløb før rabatter, ikke nettobeløbet, som omfatter rabatter (værdien **Taget fra** er **Brutto**).
- Det er baseret på mængden af de solgte varer, ikke beløbet (værdien **Linjeskifttype for rabat** er **Antal**).
- Det beregnes for hver periode i en måned (værdien **Opsaml salg efter** er **Måned**). 
- Det udlignes som et fradrag, ikke ved hjælp af Kreditor (værdien **Betalingstype** er **Debitorfradrag**).

Hvad angår merchandizinghændelsen af typen **Engangsbeløb** viser fanen **Beløb** det antal, der skal udbetales til kunden i form af et fradrag, når kunden opnår specifikke mål. Godkendelsesstatus **Åben** angiver, at engangsbeløbet endnu ikke er betalt.

Hvis du vil anvende aftalen på salgsordrer, der opfylder betingelserne i aftalen, skal aftalens status være **Bekræftet**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Foretage salg efter den planlagte merchandisinghændelse og generere tilbagefaktureringskrav

Når du opretter en salgsordre, der indeholder linjer, der opfylder kravene i aftalen, kan du få vist relaterede oplysninger på siden **Salgsordre** ved at vælge **Salgsordrelinje** \> **Visning** \> **Prisdetaljer**.

På siden **Prisdetaljer** i oversigtspanelet **Rabatter** kan salgsassistenten se en tilbagefakturering fra den gyldige handelsrabataftale (rabatprogram-id'et er vist) og det samlede beløb, der anvendes på linjen. Beløbet vises også i feltet **Rabatbeløb** i sektionen **Forkalkulation af avance** på siden **Prisdetaljer**.

Når salgsfakturaen bogføres, oprettes der et tilsvarende tilbagefaktureringskrav for hver fakturalinje.

> [!NOTE]
> Hvis du vil se siden **Prisdetaljer**, skal du på siden **Debitorparametre** under fanen **Priser** markere afkrydsningsfeltet **Aktiver prisdetaljer**. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Behandle krav og sende dem som fradrag til debitor

De næste trin i processen til håndtering af tilbagefaktureringer er at gennemse, beregne, godkende krav og derefter konvertere dem til fradrag.

Tilbagefaktureringspanelet er der, hvor ejeren af kampagneaftalen med jævne mellemrum gennemgår og behandler de krav, der genereres. Det er også der, hvor debitoradministratoren konverterer de godkendte krav til fradrag eller egentlige betalinger, afhængigt af betalingsmetoden for kravet.

På siden **Tilbagefaktureringspanel** kan du gennemse kravlinjerne. Hvis kravene har status **Skal genberegnes**, skal de genberegnes for eventuelle kumulative virkninger.

### <a name="recalculate-claims"></a>Genberegne krav

Hvis du vil genberegne krav, skal du i handlingsruden vælge **Opsaml**. Derefter skal du i dialogboksen **Opsaml rabatter** vælge debitoren.

Som følge af genberegningen genererer programmet nye krav i forbindelse med beløbene for at regulere de oprindelige krav til de kvalificerende beløb pr. enhed. Der genereres et reguleringskrav for hver enkelt kombination af en kunde, en vare, en valuta, en måleenhed, lagerdimensioner, økonomiske dimensioner og en momsgruppe. Disse reguleringskrav har samme reference til salgsordren og fakturanummeret som de krav, der skal reguleres (dvs. de krav, der oprindeligt blev oprettet fra salgsdokumentet). I modsætning til de oprindelige krav har reguleringskravet ikke værdier i de felter, der beskriver den oprindelige salgsordrelinjes beløb og antal.

Når genberegningen er fuldført, ændres status for kravene til **Beregnet**. Hvis du vil godkende kravene, skal du i handlingsruden vælge **Godkend**.

### <a name="process-claims-and-pass-them-to-ar"></a>Behandle krav og sende dem til Debitor

Kravene er nu klar til Debitor-behandling. For at behandle dem skal du i handlingsruden vælge **Behandl**. 

Under behandlingen af kravene ændres status til **Marker**, hvilket angiver, at en kladdepost (den kladde, der bogføres, er rabatperiodiseringskladden, som angivet i Debitor-parametrene) har forårsaget, at følgende hændelser er opstået: 

- Kravene er blevet overført til den midlertidige debitorsaldo som fradrag.
- Rabatperiodiseringskontoen er blevet krediteret som en repræsentation af det fremtidige passiv for kunden.
- Rabatudgiftskontoen er blevet debiteret, så du kan genkende de omkostninger, der er påløbet i forbindelse med salg.

For at fuldføre processen skal medarbejder nu håndtere de periodiserede fradrag i Debitor ved at overføre dem til kundesaldoen som en kreditnota (passiv). 

Start opgaven ved i handlingsruden på siden **Kunde** at vælge **Indsaml** \> **Udlign posteringer**. Vælg derefter på siden **Udligne posteringer** **Funktioner** \> **Tilbagefaktureringsprogram**. Denne rabatside viser alle tilbagefaktureringskrav, der tidligere er blevet behandlet.

Hvis du vil oprette en kreditnota, skal du markere afkrydsningsfeltet **Marker** for alle linjer og derefter vælge **Funktioner** \> **Opret kreditnota**.

Ved oprettelse af kreditnota bogføres en kladde. (Den kladde, der bogføres, er debitorforbrugskladden, som angivet i Debitor-parametre). Derfor er det reelle passivbeløb (kredit) blevet flyttet til debitorsaldoen. Fra et økonomisk perspektiv indebærer denne situation, at følgende hændelser er opstået:

- Kundens debitorkonto er blevet krediteret.
- Rabatperiodiseringskontoen er blevet debiteret.

For at godkende merchandisinghændelsen af typen **Engangsbeløb** skal du vælge hændelsen på siden **Aftaler om handelsrabat**, og derefter under fanen **Beløb** skal du vælge **Godkend**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Udligne det fradrag, der skal betales, og kundedelbetalingen ved hjælp af fradragspanelet

Ofte vælge kunderne delbetalinger af valgte fakturaer i forventning om tilbagefaktureringer. For at forhindre problemer med afstemningen af betalinger i fremtiden registrerer medarbejderen i Debitor disse delbetalinger som fradrag, når han eller hun registrerer de faktiske debitorbetalinger. Derefter kan disse debitorfradrag nemt udlignes i fradragspanelet mod de kravbeløb, som er forfaldne fra firmaet.

Hvis du vil registrere en kundes delbetaling i betalingskladden, skal du vælge **Debitor** \> **Betalinger** \> **Betalingskladde** og oprette en ny betalingskladde. Derefter skal du i handlingsruden vælge **Fradrag**. På siden **Fradrag** kan du oprette og spore det beløb, der blev betalt som delbetaling.

Den ansvarlige for indsamlingen bliver nu også ansvarlig for udligning af den åbne kreditnotapostering og delbetalingsposteringen mod hinanden i fradragspanelet.

For at administrere fradrag skal du vælge **Salg og marketing** \> **Handelsrabatter** \> **Fradrag** \> **Fradragspanel**. Den øverste del af siden indeholder linjer, der repræsenterer delbetalingerne fra kunden. Den nederste del af siden indeholder kundens åbne kreditposteringer. 

Markér fradragslinjen, hvis du vil udligne fradrag i forhold til den åbne postering, og markér derefter linjen under fanen Åbne posteringer. Klik på Vedligehold > Afstem i handlingsruden.

Status for de oprindelige krav er nu indstillet til **Fuldført**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Analysere effektiviteten af kampagnen og forbruget af midler

For at få et overblik over programmets vigtigste statistikker og brug af midler kan du bruge flere rapporter og analytiske visninger, der er tilgængelige i Administration af handelsrabat.

På siden **Handelsrabataktivitet** viser fanen **Oversigt** de vigtigste oplysninger om handelsrabataftalen. De andre faner viser mere specifikke oplysninger om de tilknyttede dokumenter, betalinger og andre hændelser, der er knyttet til programmet.

Fanen **Oversigt** viser det samlede antal produkter, der er solgt under kampagnen, det salgsbeløb, der er faktureret, og de tilbagefaktureringer og beløb, der er betalt.

Fanen **Kreditter for tilbagefakturering** indeholder oplysninger om individuelle tilbagefaktureringer, der er blevet krediteret til kunden.

For at få en mere analytisk oversigt over de forskellige performancemålinger for kampagnen kan du bruge analysevisningen. Du kan gå til analysevisningen ved at klikke på **Salg og marketing** \> **Handelsrabatter** \> **Aftaler om handelsrabat**. Klik på fanen **Analyse** i handlingsruden.  

For at få en mere analytisk oversigt over de forskellige performancemålinger for kampagnen kan du bruge analysevisningen. Du kan gå til analysevisningen ved at klikke på **Salg og marketing** \> **Handelsrabatter** \> **Aftaler om handelsrabat**. Klik på fanen **Analyse** i handlingsruden. 


