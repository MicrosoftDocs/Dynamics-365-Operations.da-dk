---
title: Bogføring af indirekte omkostning
description: Dette emne forklarer, hvordan du kan bogføre indirekte omkostninger, oprette omkostningsgrupper og føje noder til efterkalkulationsarket for indirekte omkostninger.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d7f4753f69d83d172993e1c9b04be2220fdf253f
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804604"
---
# <a name="indirect-cost-posting"></a>Bogføring af indirekte omkostning

Indirekte omkostninger er omkostninger, der ikke er direkte relateret til en enkelt aktivitet i produktionsprocessen. Eksempler på dette er administrative omkostninger som f.eks. medarbejderløn, regnskabsafdelingsomkostninger og faste omkostninger som f.eks. leje, forbrug og omkostninger til maskiner.

## <a name="calculating-indirect-costs"></a>Beregning af indirekte omkostninger

Microsoft Dynamics 365 Finance har ikke en automatisk måde at beregne satsen for indirekte omkostninger på. Du skal fastlægge dine indirekte omkostninger, oprette indirekte omkostningskoder og vedligeholde satsen for hver indirekte omkostning i efterkalkulationsarket.

Den nøjagtige proces, der bruges til at beregne indirekte omkostninger, kan variere en smule fra firma til firma. Den generelle proces består dog af følgende basistrin:

1. Opret en liste over indirekte omkostninger, der skal registreres i produktionen. Denne liste kan omfatte leje, administrative udgifter, regnskabsgebyrer og juridiske honorarer. Den bør ikke omfatte omkostninger til råmaterialer eller arbejdskraft, der registreres i produktionsruter.
2. Beregn summen af alle indirekte omkostninger. Du kan gruppere ensartede typer indirekte omkostninger eller holde dem adskilt. Hver indirekte omkostning, der konfigureres, kan have forskellige hovedkonti, der bruges til bogføring i finansmodulet.
3. Sammenlign de indirekte omkostninger med en faktor, der også kaldes absorptionsgrundlaget. Faktoren kan være alt, hvad du vælger. Her er nogle få almindelige eksempler:

    - Indtægter
    - Det samlede antal, der produceres
    - Opstillingstid
    - Procestid

    Du kan vælge den periode, du vil beregne de indirekte omkostninger for, f.eks. månedligt, kvartalsvist eller årligt. Summen af dine indirekte omkostninger og summen af faktoren skal være for samme tidsrum. Følgende formel bruges til beregning af den indirekte omkostningssats:

    *Indirekte omkostningssats* = *Samlede indirekte omkostningsudgifter* &divide; *Totalfaktor*

4. Opret indirekte omkostningsgrupper.
5. Konfigurer efterkalkulationsarket med satserne.
6. Vedligehold omkostningerne for de indirekte omkostninger i efterkalkulationsversionen.

> [!NOTE]
> Du kan bruge modulet **Omkostningsregnskab** til at akkumulere omkostninger og fastlægge dine faste omkostninger fra forskellige kilder, f.eks. produktion, projekter og finansmodulet. Du kan få flere oplysninger under [Driftsregnskab](/cost-accounting/cost-accounting-home-page.md).

> [!IMPORTANT]
> Forskellige myndigheder har udgivet vejledning til de omkostningstyper, der kan medtages som indirekte omkostninger eller faste omkostninger i omkostningerne for færdigvarer. Før du begynder at konfigurere indirekte omkostninger, anbefales det, at du kontrollerer det med din revisor og den lokale lovgivning for at sikre, at du overholder angivne standarder.

## <a name="create-cost-groups-for-indirect-costs"></a>Oprette omkostningsgrupper til indirekte omkostninger

Du skal oprette mindst én omkostningsgruppe for at kunne bruge indirekte omkostninger. Der er ingen grænser for, hvor mange omkostningsgrupper du kan have. Overvej, hvordan du beregner omkostningerne, og om der er forskellige satser for forskellige omkostningstyper. Din organisation producerer f.eks. fødevarer. Nogle råvarer og færdigvarer er tørvarer og har én indirekte omkostning til lager. Andre råvarer og færdigvarer er nedkølede og har højere indirekte omkostninger. I dette tilfælde kan du oprette to omkostningsgrupper: **Faste omkostninger til tørmateriale** og **Faste omkostninger til nedkølet materiale**.

Følg disse trin for at oprette en omkostningsgruppe til indirekte omkostninger.

1. Gå til **Produktionsstyring &gt; Konfiguration &gt; Ruter &gt; Kostprisgrupper**.
2. Vælg **Ny** for at oprette en gruppe.
3. Angiv et entydigt navn i feltet **Omkostningsgruppe** som f.eks. **MATOMK**.
4. Indtast i feltet **Navn** en beskrivelse af omkostningsgruppen som f.eks. **Faste materialeomkostninger**.
5. Vælg **Indirekte** i feltet **Kostprisgruppetype**.
6. Valgfrit: Vælg **Fast omkostning** eller **Variabel omkostning** i feltet **Funktionsmåde**.

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>Konfigurere efterkalkulationsarket til indirekte omkostninger

Når du har oprettet en eller flere kostprisgrupper, kan du konfigurere efterkalkulationsarket med indirekte omkostninger og definere beregningen. Det kan være en fordel at gruppere indirekte omkostninger i efterkalkulationsarket. Du kan gruppere indirekte omkostninger ved at oprette et valgfrit hoved i efterkalkulationsarket. Du skal oprette mindst én node for hver omkostningsgruppe i efterkalkulationsarket. For hver omkostningsgruppe for indirekte omkostninger kan du tilføje endnu en beregning af indirekte omkostninger.

### <a name="indirect-cost-node-types"></a>Nodetyper for indirekte omkostninger

I dette afsnit beskrives de forskellige typer noder til indirekte omkostninger.

#### <a name="surcharge"></a>Tillæg

**Tillæg** er en af de mest almindelige typer indirekte omkostninger. Den beregner en procentdel af omkostningen på absorptionsbasis af omkostninger i produktionsordren. Du kan definere absorptionsbasis ved at vælge de omkostningsgrupper, der er knyttet til materialerne eller tidskomponenterne i efterkalkulationsarket.

Der kan f.eks. blive lagt en tillægsafgift på 3 procent til produktionsomkostningerne for alle råvarer i en produktionsordre.

#### <a name="rate"></a>Sats

En indirekte omkostning af **Sats**-typen bruges til at føje et fast kostbeløb til produktionsordren fra en absorptionsbasis af omkostningerne i produktionsordren. Satsen kan baseres på en af tre undertyper:

- **Behandling** – Satsen er baseret på kørselstiden i ruten.
- **Konfiguration** – Satsen er baseret på konfigurationstiden i ruten.
- **Antal** – Satsen baseres på det producerede antal.

Du kan definere absorptionsbasis ved at vælge de omkostningsgrupper, der er knyttet til materialet eller tidskomponenterne i efterkalkulationsarket.

Et fast beløb på 2,00 USD føjes f.eks. til hver produktionsordre baseret på rutens kørselstid for kostprisgruppen til arbejdskraft på efterkalkulationsarket.

#### <a name="output-unit-based"></a>Baseret på outputenhed

En indirekte omkostning af typen **Baseret på outputenhed** beregnes ved at gange det beløb, der er angivet i oversigtspanelet **Sats** for efterkalkulationsarket af den valgte undertype. Du kan vælge antallet, vægten eller volumen for den færdige vare som multiplikator for den indirekte omkostning.

Du kan f.eks. bruge antallet til at beregne 1,50 USD af maskinafskrivning for hvert produceret antal. Som et andet eksempel kan du bruge volumen til at beregne 2,00 USD nedkølingsomkostninger for den plads, som færdigvaren fylder i kølerenhederne.

#### <a name="input-unit-based"></a>Baseret på inputenhed

En indirekte omkostning af typen **Baseret på inputenhed** beregnes ved at gange mængden af råvarer, der forbruges i en produktionsordre, med et beløb. Du kan bruge vægten eller volumen af input på produktionsordren til at beregne totalen. Du kan begrænse beregningen til et undersæt af materialer ved at vælge en eller flere kostprisgrupper i oversigtspanelet **Overtagelsesgrundlag** i efterkalkulationsarket.

Du kan f.eks. bruge volumen af input for en bestemt omkostningsgruppe, der er knyttet til kølervarer, til at lægge 1,00 USD til produktionsordren.

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>Oprette en totalnode for indirekte omkostninger i efterkalkulationsarket

Benyt følgende fremgangsmåde for at oprette en totalnode for indirekte omkostninger i efterkalkulationsarket.

1. Gå til **Omkostningsstyring &gt; Konfiguration af regnskabspolitikker for indirekte omkostninger &gt; Kostprisark**.
2. Vælg en node i træet, der repræsenterer omkostningerne for de varer, der er produceret.
3. Vælg **Ny** for at oprette en node.
4. Vælg **Total** i feltet **Vælg nodetype**.
5. Angiv et entydigt id for noden i feltet **Kode**, f.eks. **Faste produktionsomkostninger**.
6. Markér afkrydsningsfeltet **Sidehoved**.
7. Markér afkrydsningsfeltet **Total**.
8. Vælg **OK**.

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>Oprette en gruppenode for indirekte omkostninger i efterkalkulationsarket

Benyt følgende fremgangsmåde for at oprette en gruppenode for indirekte omkostninger i efterkalkulationsarket.

1. Gå til **Omkostningsstyring &gt; Konfiguration af regnskabspolitikker for indirekte omkostninger &gt; Kostprisark**.
2. Vælg den node i træet, som du vil oprette den indirekte omkostning under. Vælg f.eks. totalnoden for **Faste produktionsomkostninger**.
3. Vælg **Ny** for at oprette en node.
4. Vælg **Omkostningsgruppe** i feltet **Vælg nodetype**.
5. Angiv et entydigt id for noden i feltet **Kode**, f.eks. **TRANSP**.
6. Indtast en kort beskrivelse i feltet **Beskrivelse** som f.eks. **Fast transportomkostning**.
7. Vælg **OK**.
8. Vælg omkostningsgruppen i feltet **Omkostningsgruppe**, f.eks. **OMK1: Indirekte transportomkostninger**.

### <a name="create-a-surcharge-indirect-cost"></a>Oprette en indirekte omkostning for tillæg

Benyt følgende fremgangsmåde for at oprette en indirekte omkostning for tillæg i efterkalkulationsarket.

1. Gå til **Omkostningsstyring &gt; Konfiguration af regnskabspolitikker for indirekte omkostninger &gt; Kostprisark**.
2. Vælg den gruppenode for indirekte omkostning i træet, som du vil oprette den indirekte omkostning under. Vælg f.eks. totalnoden for **TRANSP - Fast transportomkostning**.
3. Vælg **Ny** for at oprette en node.
4. Vælg **Tillæg** i feltet **Vælg nodetype**.
5. Angiv et entydigt id for noden i feltet **Kode**, f.eks. **Tillæg for transport**.
6. Vælg **OK**.
7. I feltet **Undertype** skal du vælge **Total**.
8. I oversigtspanelet **Overtagelsesgrundlag** skal du vælge **Nyt** for at oprette en omkostningskode.
9. Vælg en omkostningsgruppe, der skal bruges til beregning af tillægsafgiften, i feltet **Kode**.
10. Valgfrit: Gentag trin 8 til 9 for hver ekstra omkostningsgruppe, du vil bruge til beregningen.
11. I oversigtspanelet **Tillæg** skal du vælge **Ny** for at oprette en sats.
12. Vælg den efterkalkulationsversion, hvor du vil tilføje tillægsafgiften, i feltet **Version**.
13. Valgfrit: Angiv et sted, som tillægsafgiften skal anvendes på, i feltet **Sted**.
14. I feltet **Procent** skal du angive den procentdel, der skal beregnes på produktionsordrer fra de omkostningsgrupper, der er defineret i oversigtspanelet **Overtagelsesgrundlag**.
15. I oversigtspanelet **Finanskonteringer** skal du vælge den hovedkonto, der skal bruges til felterne **Anslåede indirekte omkostninger, der er overtaget**, **Forkalkuleret omkostning til forbrugte indirekte omkostninger, IGVF**, **Indirekte omkostninger, der er overtaget** og **Omkostning til forbrugte indirekte omkostninger, IGVF**.
16. Valgfrit: Angiv de økonomiske dimensioner, der som standard skal indtastes i transaktioner, når de bogføres i finansmodulet, i oversigtspanelet **Økonomiske dimensioner**.

Den foregående fremgangsmåde viser, hvordan du opretter en indirekte omkostning af typen **Tillæg**. Tilsvarende trin bruges til at oprette andre typer indirekte omkostninger. I følgende afsnit beskrives forskellene for hver type.

#### <a name="rate"></a>Sats

- Vælg **Sats** i stedet for **Tillæg** i trin 4.
- I trin 7 skal du vælge **Behandling**, **Konfiguration** eller **Antal** i stedet for **Total**.
- I trin 11 skal du bruge oversigtspanelet **Sats** i stedet for oversigtspanelet **Tillæg**.
- I trin 14 skal du angive et beløb i feltet **Beløb** i stedet for en procent i feltet **Procent**.

#### <a name="output-unit-based"></a>Baseret på outputenhed

- I trin 4 skal du vælge **Baseret på outputenhed** i stedet for **Tillæg**.
- I trin 7 skal du vælge **Antal**, **Vægt** eller **Volumen** i stedet for **Total**.
- Spring trin 8 til og med 10 over.
- I trin 11 skal du bruge oversigtspanelet **Sats** i stedet for oversigtspanelet **Tillæg**.

#### <a name="input-unit-based"></a>Baseret på inputenhed

- I trin 4 skal du vælge **Baseret på inputenhed** i stedet for **Tillæg**.
- I trin 7 skal du vælge **Vægt** eller **Volumen** i stedet for **Total**.
- I trin 11 skal du bruge oversigtspanelet **Sats** i stedet for oversigtspanelet **Tillæg**.
