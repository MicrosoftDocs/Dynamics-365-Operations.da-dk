---
title: Kreditorrabatter
description: "Dette emne indeholder en oversigt over de mest almindelige opgaver, du vil udføre, når du arbejder med kreditorrabatter. Kreditorrabatter hjælpe virksomheder med bedre at styre deres leverandørrabatprogrammer ved at automatisere de opgaver, der kræves for at administrere, spore og gøre krav på rabatter, der er opnået."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TAMVendRebateAgreement
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 2012
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ae5ee60238b951779c7790870e6c6adfba55d7d
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-rebates"></a>Kreditorrabatter
[!include[banner](../includes/banner.md)]

Kreditorrabatter hjælpe virksomheder med bedre at styre deres leverandørrabatprogrammer ved at automatisere de opgaver, der kræves for at administrere, spore og gøre krav på rabatter, der er opnået.

Dette emne indeholder en oversigt over de mest almindelige opgaver, du vil udføre, når du arbejder med kreditorrabatter. Oversigten omfatter følgende opgaver:

- Gennemgå detaljer om en rabataftale
- Identificere ordrer, der er berettiget til rabatter, og oprette rabatkrav.
- Gennemse og godkende krav.

## <a name="audience-and-purpose"></a>Målgruppe og formål

Oplysningerne i dette emne er beregnet til forretningsbeslutningstagere i større virksomheder, f.eks. i stillinger som indkøbschef, regnskabsdirektør (CFO) og regnskabschef, der har følgende ansvarsområder:

- Forhandle leverandørpris, rabat og rabataftaler.
- Administrere personale, der behandler rabatkrav og opkræver betalinger.
- Bestille lagervarer til de bedst mulige priser.

Personer i disse stillinger har brug for måder til at opnå forskellige mål. Her er nogle eksempler:

- Fleksibel tilpasning af forskellige typer leverandørkampagneprogrammer og rabatbetingelser.
- Reducer den administrative byrde og de fejl, der er knyttet til overvågningen af ydeevnen for kampagner og behandlingen af krav.
- Forbedre likviditetsbudgetteringen ved at periodisere fremtidige tilgodehavender.
- Få et kvantificeret grundlag for løbende og fremtidige forhandlinger med leverandører om rabatter.

## <a name="review-details-of-a-vendor-rebate-agreement"></a>Gennemgå detaljer om en leverandørrabataftale
En leverandørrabataftale registreres i en kontrakt med en leverandør, der angiver de aftalte vilkår og betingelser, hvor firmaet er berettiget til en monetær belønning mod at nå forud angivne købsmål. Leverandørrabataftaler registreres på siden **Rabataftaler**.

Du åbner siden **Kreditorrabataftaler** ved at vælge **Indkøb og forsyning** &gt; **Kreditorrabatter** &gt; **Rabataftaler**.

![Købsaftale](media/purchase-agreement.PNG)

På siden **Kreditorrabataftaler** kan du få vist detaljer om de betingelser, der er aftalt i en leverandøraftale.

Aftalens overskrift angiver de generelle betingelser, der berettiget et firma til rabatter. Når den er aktiv angiver oplysningerne i hovedet, at en kreditor giver en rabat, når der købes et specifikt produkt i et specifikt antal. I hovedet, kan du også angive indstillingen for måleenheden for rabat og datoberegningstypen.

- Under fanen **Generelt** kan du i feltet **Indstillingen Måleenhed for rabat** du definere om måleenheden skal være en betingelse for, at indkøbsordrelinjen berettiger til rabatkrav. 

    - **Konvertere** – En indkøbsordrelinje, der er berettiget til en leverandørrabat i henhold til rabataftalen. Du modtager en rabat, uanset den måleenhed, der gælder for linjen.
    - **Nøjagtigt match** – For at opnå en rabat skal en indkøbslinje have den samme måleenhed, der er angivet i aftalen.

- Under fanen **Generelt** i feltet **Beregningsdatotype**, skal du vælge den dato, der bruges til at bestemme, om indkøbet forekommer i rabataftalens gyldighedsperiode.

    - **Oprettet den** – Brug oprettelsesdatoen for indkøbsordren.
    - **Ønsket levering** – Brug den ønskede leveringsdato.

På aftalelinjer kan du angive leverandørrabataftalen mere detaljeret.

- I feltet **Opsaml indkøb efter**, kan du angive beregningen af rabatkravet. Beløbet kan angives til at afhænge af en periode (af uge, måned, år, levetid eller en tilpasset periode). Værdien **Faktura** angiver, at et rabatkrav skal bestemmes, hver gang en indkøbsordrelinje faktureres.
- I feltet **Taget fra** kan du angive grundlaget for beregning af rabatten.

    - **Brutto**– rabatten beregnes ud fra varens bruttopris.
    - **Netto** – rabatten beregnes ud fra varens nettopris (prisen efter andre rabatter er blevet anvendt).

- Felterne **Periodiseringskonto for rabatprogram** og **Udgiftskonto for rabatprogram** angiver kontonumre, der skal modtage periodiserede rabatbeløb i mellemstadiet mellem godkendelse og behandling.
- Når indstillingen **Godkendelse kræves** er angivet til **Ja**, skal rabatkravet godkendes, før det kan periodiseres eller udbetales.
- Feltet **Linjeskifttype for rabat** angiver grundlaget for rabatterne.

    - **Antal** – rabatterne er baseret på mængde.
    - **Beløb** – rabatterne er beløbsbaserede.

- På oversigtspanelet **Linjer** kan du se, hvordan forskellige antal niveauer kan konfigureres til at tildele forskellige rabatter. I den forrige illustration angiver felterne **Fra værdi** og **Til værdi** f.eks., at en produktmængde mellem 10 og 19 enheder giver ret til en rabat på USD 15 pr. enhed.

    > [!NOTE]
    > Værdien **Fra værdi** er inklusiv, mens værdien **Til værdi** er eksklusiv. F.eks. er feltet **Linjeskifttype for rabat** angivet til **Antal**, og du indtaster **1** i feltet **Fra værdi** og **3** i feltet **Til værdi**. I så fald gælder rabatbeløbet, når du køber én eller to varer, men ikke, når du køber tre varer.

- I feltet **Status for godkendelsesarbejdsgang** angiver værdien **Godkendt**, at aftalen kan anvendes til indkøbsordrer, der opfylder betingelserne i aftalen.

## <a name="identify-orders-that-qualify-for-rebates-and-generate-rebate-claims"></a>Identificere ordrer, der er berettiget til rabatter, og oprette rabatkrav

Når indkøbsordrer afgives til en leverandør, som firmaet har en rabataftale med, identificerer programmet alle fremtidige leverandørkreditbetalinger. Hvis indkøbsordrerne er kvalificerede til en rabat, genereres et rabatkrav for hver ordrelinje, så snart en købsfaktura er blevet bogført. Processen er automatisk. Du kan senere kan gennemse de forventede rabatter og se virkningen af disse rabatter på produktets omkostninger og overskudsgrad.

### <a name="view-details-of-rebates-that-are-applied-to-a-purchase-order-line-per-the-vendor-rebate-agreement"></a>Få vist detaljer om rabatter, der anvendes på en indkøbsordrelinje pr. leverandørrabataftale
1. På siden **Indkøbsordre** skal du vælge en ordrelinje, og derefter vælge **Indkøbsordrelinje** &gt; **Vis** &gt; **Prisdetaljer**.
2. På siden **Prisdetaljer** skal du vælge oversigtspanelet **Rabatter**.

Rabatoplysningerne vises også i feltet **Kreditorrabat** i sektionen **Forkalkulation af avance** på siden **Prisdetaljer**.

> [!NOTE]
> På siden **Indkøbs- og forsyningsparametre** under fanen **Priser** skal du kontrollere, at indstillingen **Aktivér prisdetaljer** er angivet til **Ja**. Hvis indstillingen er angivet til **Nej**, kan du ikke få vist rabatterne.

## <a name="review-and-approve-claims"></a>Gennemse og godkende krav
Krav til rabat, der genereres, repræsenterer de fremtidige betalinger, der kan forventes fra leverandøren. Før der udstedes en kreditnota til leverandøren, ønsker ejeren af aftalen typisk at gennemse krav og godkende dem. Bemærk dog, at status for et krav bestemmer, om kravet er klar til at gennemgå godkendelsesprocessen.

### <a name="the-status-of-claims-and-the-effect-on-the-approval-process"></a>Status for krav og effekten på godkendelsesprocessen
Når der oprettes et krav, angives dets status som **Skal beregnes**, hvis rabatten tildeles på kumulativt grundlag, eller **Beregnet**, hvis rabatten tildeles pr. faktura. Hvis status for et krav er **Skal beregnes**, skal kravet gennemgå en beregningsproces, der håndteres af funktionen Opsaml. Kun de krav, der har status som **Beregnet** skal indgå i godkendelsesprocessen.

> [!NOTE]
> Hvis indstillingen **Godkendelse kræves** på en kreditorrabataftale er angivet til **Nej**, får de krav, der genereres, status som **Godkendt**. Godkendelsen er obligatorisk for de krav, der er tildelt på kumulativt grundlag.

### <a name="approve-claims-and-view-postings-and-invoice-details"></a>Godkende krav, og få vist posteringer og fakturaoplysninger
Når krav er blevet godkendt, kan de behandles af Kreditor (A/P). Der genereres automatisk en kreditnota (kreditorfaktura) for beløbet i rabatkravet. Kreditbeløbet kan derefter føjes til kreditorsaldoen og A/P-teamet kan medtage den i den almindelige udligningsproces.

1. Vælg **Indkøb og forsyning** &gt; **Kreditorrabatter** &gt; **Rabatkrav** for at åbne et rabatkrav.
2. Luk rabatkravet.
3. Markér kravet, og vælge derefter **Godkend** i handlingsruden.
4. På anmodningssiden i feltet **Kreditor** skal du vælge den kreditor, du har tilladelse til at modtage en rabat, fra, og derefter vælge **OK**.

    En rabatperiodiseringskladde bogføres for kravsbeløbet. Denne bogføring debiterer kontoen Periodiserede kreditorrabattilgodehavender med den forventede kreditorkredit og krediterer mellemkontoen Periodiserede modtagne kreditorrabatter med den forventede gevinst.

    ![Melding](media/message.png)

5. Markér linjen på rabatlisten, og vælg derefter **Rabatposter** i handlingsruden for at få vist og navigere til kladdebatchnummeret for denne bogføring med rabatperiodisering.

    For at flytte kravene til den almindelige A/P-proces skal A/P-medarbejderen nu afslutte håndteringen af rabatkravet ved at køre funktionen Behandl.

6. I handlingsruden skal du vælge **Behandl** og derefter vælge **Filtrér**. I feltet **Kriterier** til feltet **Kreditorkonto** skal du vælge den kreditor, der skal behandles rabatkrav for, vælge andre relevante filtre og derefter vælge **OK**.

    Meddelelseslinjerne og det faktum, at status ændres til **Fuldført**, angiver, at der er opstået følgende hændelser:

    - En kladdepost til periodisering af rabat har tilbageført det tidligere midlertidige beløb for periodisering af konti for tilgodehavender og udgifter.
    - En kreditorfaktura (kreditnota) for rabatbeløbet er blevet oprettet.

        > [!NOTE]
        > Indstillingen af feltet **Manuel fakturabogføring** under fanen **Rabatprogram** på siden **Indkøbs- og forsyningsparametre** bestemmer, om en kreditorfaktura bogføres manuelt eller automatisk som en del af processen til behandling af krav.

    - Når kreditorfakturaen bogføres, enten automatisk eller manuelt, debiteres kreditorens kreditorkonto, og kontoen Modtagne rabatter og fradrag krediteres.

        > [!NOTE] 
        > Kontonummeret for Modtagne rabatter og fradrag er angivet for den indkøbskategori, der bruges på købsfakturalinjen for rabatten. Indkøbskategorien er omvendt angivet under fanen **Rabatprogram** på siden **Indkøbs- og forsyningsparametre**.

7. Markér linjen på rabatlisten, og vælg derefter **Rabatposter** i handlingsruden for at få vist og navigere til kladdebatchnummeret for denne bogføring med rabatperiodisering og også kreditorfakturanummeret.
8. Vælg linjen for kreditorfakturaposteringen, og vælg derefter **Kreditorfaktura** i handlingsruden. Hvis kreditorfakturaen er bogført, vises fakturajournalen. Ellers kan du se kreditorfakturaen som en ventende kreditorfaktura, der kræver manuel postering.

    Fakturalinjen angiver detaljer om kreditorfakturaen for indkøbskategorien **Provisioner og rabatter** .

9. På siden **Alle leverandører** skal du vælge den leverandør, du modtager en rabat fra, og derefter vælge **Transaktioner** i handlingsruden. Find linjen for fakturaen. Rabatbeløbet er nu blevet føjet til kreditorsaldoen.

## <a name="summary"></a>Resumé
Processen til håndtering af kreditorrabatter omfatter flere manuelle sporingsopgaver, der ofte er langsommelige. Ved at automatisere disse opgaver, kan funktionen til styring af kreditorrabatten hjælpe dig med at komme igennem følgende processer:

- Generering af præcise rabatkrav
- Periodisering af det forventede tilgodehavende og den midlertidige gevinst i Finans
- Opdatering af kreditorsaldoen og resultatopgørelsen med den ydelse, der er forfaldent

