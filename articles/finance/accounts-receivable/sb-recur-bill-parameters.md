---
title: Parametre for tilbagevendende kontraktfakturering
description: Denne artikel indeholder en forklaring på, hvordan du kan konfigurere standardværdierne for faktureringsplaner, der oprettes ved fakturering af tilbagevendende kontrakter. Det forklarer også, hvordan du opretter faktureringsplangrupper.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643997"
---
# <a name="recurring-contract-billing-parameters"></a>Parametre for tilbagevendende kontraktfakturering

Brug siden **Faktureringsparametre for tilbagevendende kontrakter** til at konfigurere standardværdierne for faktureringsplaner, der oprettes i forbindelse med fakturering af tilbagevendende kontrakter. Alle de faktureringsplaner, du opretter, bruger først disse standardværdier. Du kan dog ændre værdierne for hver faktureringsplan efter behov.

## <a name="general-tab"></a>Fanen Generelt

1. Vælg en faktureringsplangruppe i feltet **Faktureringsplangruppe** under fanen **Generelt** på siden **Faktureringsparametre for tilbagevendende kontrakter**. Du kan finde flere oplysninger om opsætning af faktureringsplangrupper i afsnittet [Fakturere plangrupper](#set-up-billing-schedule-groups) senere i denne artikel.
2. Vælg i feltet **Fratrædelsestype**, hvordan den endelige faktura beregnes, når en faktureringsplan afsluttes:

    - **Juster plan** – Afskære faktureringsplanen på fratrædelsesdatoen, rediger status for planen til **Sidste fakturering**, og juster den tilknyttede ventende plan ved at tilbagefør det beløb, der ikke længere skal genkendes. Hvis faktureringsstartdatoen ligger efter ophørsdatoen, fjernes de resterende faktureringsperioder.
    - **Resterende fakturering** – Føj et eventuelt restbeløb for faktureringsperioden til ophørsperioden, og ret status for linjen til **Sidste fakturering**, og opdater udskydelsesplanen. Hvis faktureringens startdato ligger efter ophørsdatoen, føjes det samlede beløb for alle resterende faktureringsperioder til faktureringsperioden, og de resterende faktureringsperioder fjernes.
    - **Ingen regulering** – Afslut faktureringsplanen på den angivne ophørsdato. Der foretages ingen justeringer af faktureringsplanen.

3. Vælg **Ingen** i feltet **Entydig planlægningstype** for at angive, at debitorer er begrænset til en enkelt faktureringsplan. Vælg **Pr. kunde** eller **Pr. slutbruger** for at angive, at kunder er begrænset til en entydig plan.
4. Hvis du vil justere linjerne i faktureringsplanen med slutningen af en måned, skal du angive indstillingen **Juster til måned** til **Ja**. Angiv det til **Nej** for at bruge trinvise datoer.
5. Angiv indstillingen **Forholdsmæssige delperioder** til **Ja** for at fordele faktureringsbeløb baseret på antallet af dage i perioden. Angiv det til **Nej**, hvis beløbet skal være det samme i hver faktureringsperiode, uanset antallet af dage.
6. Hvis du angiver indstillingen **Prorater delperioder** til **Ja**, skal du angive feltet **Prorationsmetode** til **Daglig** for at fordele beløbene baseret på antallet af dage i perioden. Indstil det til **Månedligt**, så det har et tilsvarende beløb hver måned.
7. Angiv, om nyoprettede faktureringsplaner som standard er på hold.

    > [!NOTE]
    > Hvis du vil fjerne hold i en faktureringsplan, skal brugeren være en del af en brugergruppe. Vælg **Fjern gruppeændring for hold-brugergruppe** for at konfigurere en brugergruppe, hvor indstillingen **Tillad fjernelse af hold** er aktiveret.

8. Vælg standardfakturaposteringstypen for nye faktureringsplaner i feltet **Fakturaposteringstype**.
9. Indstil indstillingen **Juster deltid til fakturering** til **Ja** for at justere den tilsvarende udskydelsesplan, så den bruger de samme datoer som faktureringsplanen. Angiv det til **Nej** for at bruge forskellige datoer.
10. Hvis du bruger funktionen til opdeling af omsætning, skal du angive indstillingen **Opret automatisk omsætningsopdeling** til **Ja**, når der føjes varer til en faktureringsplan. Afkrydsningsfeltet **Splitning af omsætning** markeres automatisk på faktureringsplanlinjen, hvis varen er konfigureret som en opdelt omsætningsvare. Angiv indstillingen **Nej**, hvis du manuelt vil markere afkrydsningsfeltet **Indtægtssplitning**.
11. Angiv indstillingen **Debitoropdeling** til **Ja**, hvis du vil tillade, at en faktureringsplan faktureres til forskellige debitorer. Når indstillingen er angivet til **Ja**, er indstillingen **Debitoropdelt** tilgængelig i faktureringsplanhovedet og faktureringsplanlinjen. 
12. Angiv felterne til oprettelse af salgsordrer:

    - Fakturaer kan konsolideres efter periode, debitor eller vare. Du kan angive en hvilken som helst kombination af **Ja** og **Nej**. Fakturaer kan også opdeles efter varegruppe.
    - Følgende indstillinger er tilgængelige for faktura:

        - **Opret salgsordre** - Opret kun salgsordren.
        - **Vis bogføringsfaktura** – Fakturer salgsordren, og åbn en side, hvor du kan bogføre fakturaen manuelt.
        - **Opret gebyrtekstfaktura** – Vælg denne indstilling, hvis du bruger fritekstfakturaer.
        - **Bogfør fakturaen automatisk** – Fakturer salgsordren, og bogfør den automatisk.

    - Angiv indstillingen **Føj faktureringsdatoer til indstillingen Varebeskrivelse** til **Ja**, hvis du vil tilføje en beskrivelse, der omfatter faktureringens startdato og slutdato.
    - Angiv indstillingen **Udelad nulforbrug** til **Ja** for at udelade faktureringsplanlinjer, der ikke har noget forbrug. Angiv det til **Nej**, hvis disse linjer skal medtages på salgsordren.
    - Angiv indstillingen **Udskriv ikke underordnede varer** til **Ja**, hvis du ikke vil udskrive de underordnede varer for en indtægtssplit på salgsordren. Den udskrevne faktura viser dog kun den overordnede vare. Hvis nettobeløbet for de (skjulte) underordnede varer er en sum på ikke nul, viser nettobeløbet på den overordnede linje en oversigt over de underordnede linjer. Angiv indstillingen **Nej** for at udskrive alle underordnede varer under den overordnede vare på salgsfakturaen.

12. Angiv felterne for support og fornyelse:

    - Angiv indstillingen **Automatisk aktivering af support og fornyelse** til **Ja**, hvis du automatisk vil bruge funktionen til support og fornyelse på en salgsordre.
    - Vælg standardniveauet for **support og fornyelse** i feltet Support og fornyelsesniveau.
    - Vælg mængden for support og fornyelse i feltet **Support og fornyelsesmængde**.
    - I feltet **Startdato for standardsupport og fornyelse** angive den dato, der skal bruges som standardstartdato for support og fornyelse:

        - **Transaktionsdato** – Brug transaktionsdatoen som startdato.
        - **Starten af den aktuelle måned** – Brug den første i den aktuelle måned som startdato.
        - **Starten af næste måned** – Brug den første i næste måned som startdato. Hvis transaktionsdatoen er den første, bruges transaktionsdatoen.
        - **Regel 15** – Hvis transaktionsdatoen er mellem den første og den 15. dag, skal du bruge den første i den aktuelle måned som startdato. Hvis transaktionsdatoen er den 16. dag eller senere i en måned, er den første i næste måned startdatoen.

    - Angiv indstillingen **Medtag rabat i beregning** til **Ja** for at medtage rabatbeløbet i beløbet for understøttelse eller fornyelse. Angiv det til **Nej** for at udelade rabatbeløbet.
    - I felterne **Supportfrekvens** og **Fornyelse** skal du vælge den frekvens, der skal bruges, når elementer for understøttelse og fornyelse føjes til en faktureringsplan: **Daglig**, **Månedlig**, **Kvartalsvis**, **Halvårlig** eller **Årlig**.
    - Angiv indstillingen **Juster efter varegruppe** til **Ja** for at justere start- og slutdatoerne for nye varer til eksisterende varer baseret på varegruppen.
    - Angiv indstillingen **Juster til næste ikke-fakturerede periode** til **Ja** for at bestemme justeringsdatoen for et fornyelseselement på basis af datoen for den næste ikke-fakturerede periode, efter at fornyelsen er startet.
    - Angiv indstillingen **Kopiér serienummer** til **Ja** for at kopiere varens serienummer fra den første salgsordrelinje til den tilsvarende faktureringsplanlinje.

13. Hvis du bruger eskalering i faktureringsplanen, skal du vælge den metode, der skal bruges til beregning af forbrugerprisindekset.
14. Angiv indstillingen **Spor prisændring** til **Ja**, hvis du vil registrere prisændringer på faktureringsplanlinjer. Hvis en faktureringsplanlinje ændres manuelt fra standard til flad, og en ny pris angives, spores revisionsoplysningerne på faktureringsplanlinjen. Angiv det til **Nej**, hvis du ikke vil spore disse ændringer.
15. Angiv, om poster som standard skal filtreres efter startdato eller slutdato på siden **Opret faktura**.
16. Hvis du bruger funktionen **Ikke-genereret omsætning**, skal du angive de indstillinger, der bruges:

    - Angiv indstillingen **Bogfør finanskladde** automatisk til **Ja**, hvis finanskladden skal oprettes og bogføres samtidigt. Angiv den til **Nej**, hvis du vil oprette finanskladden og derefter bogføre den manuelt.
    - Vælg det **standardkladdenavn**, der skal bruges, når finanskladden oprettes, i feltet Standardkladdenavn.
    - Vælg den **kortfristede ikke-fakturerede metode** i feltet Kortfristet metode, hvis du bruger en. Hvis du vælger **Ingen**, bruges funktionen på kort sigt ikke med ikke-frafaktureret omsætning. Vælg de **rulleperioder**, der altid skal bruges 12 måneder eller et **fast år** til at bruge det resterende regnskabsår.

17. Angiv de indstillinger, der skal bruges, når en faktureringsplan og dens linjer afsluttes:

    - **Udsted kredit** – Opret en kreditnota, når en faktureringsplan eller faktureringsplanlinje afsluttes.
    - **Kreditregulering** – Opret en kreditregulering for en faktureringsplan, når en linje afsluttes. Kreditreguleringen vises i en fremtidig faktureringsperiode for faktureringsplanen. Kreditreguleringen opdaterer fakturabeløbet for den næste faktureringsperiode, indtil kreditten er anvendt færdig på faktureringsplanen.
    - **Ingen kredit** – Opret ikke en kreditregulering eller kreditnota, når en faktureringsplan eller faktureringsplanlinje afsluttes. Denne indstilling er kun tilgængelig, når du bruger et ophør af typen **Ingen regulering** til at afslutte en faktureringsplan.
18. Når indstillingen **Én gang kan afsluttes med refusion** er angivet til **Nej**, og en faktureringsplan med faktureringsfrekvensen **Én gang** ændres status for faktureringsplanlinjen til **Fratrådt**, når faktureringsplanen er faktureret. Denne faktureringsplan kan ikke afsluttes, og der kan ikke udstedes kredit. Når indstillingen **Én gang kan afsluttes med refusion** er angivet til **Ja**, og en faktureringsplan med faktureringsfrekvensen **Én gang** kan have status **Aktiv**, når faktureringsplanen er faktureret. Faktureringsplanlinjen kan afsluttes, og en refusion behandles. 
19. Indstillingen **Beregn daglig**, der angives i parametre, angives som standard til masseafslutningssiden og dialogboksen til faktureringsoverskrift og afslutning. Den kan ændres under aftrædelsesprocessen. Når beløbet er angivet til **Ja**, beregnes ethvert refusionsbeløb ved hjælp af en dagssats. Når det er angivet til **Nej**, krediteres det på baggrund af fratrædelsesdatoen og faktureringshyppigheden. Hvis der f.eks. bruges månedlig frekvens, og faktureringsbeløbet er $100 pr. måned, er kreditbeløbet i trin af $100. Hvis faktureringsfrekvensen er engangshyppigheden, $0,00. Prorate skal angives dagligt til Ja for at få en refusion for engangsfaktureringsfrekvens. 
20. Angiv Indstillingen **Opret udsættelse for kredit** til **Ja** for at oprette en ny udskydelsesplan, hvis du krediterer en eksisterende udskydelsesplan. Lad indstillingen være angivet til **Nej** for at oprette kreditnotaen i den eksisterende udskydelsesplan.

## <a name="sequence-number-tab"></a>Fanen Sekvensnummer

Brug fanen **Sekvensnummer** på siden **faktureringsparametre for tilbagevendende kontrakter** til at angive standardværdien for faktureringsplannumre. Standardværdierne konfigureres på siden **Nummerserier** (**organisationsadministration \> Nummerserier \> Nummerserier**).

## <a name="set-up-billing-schedule-groups"></a>Konfigurer faktureringsplanlægningsgrupper

Brug siden **Faktureringsplangrupper** til at oprette en faktureringsplangruppe for fakturering af tilbagevendende kontrakter. Når der oprettes en ny faktureringsplan, og der anvendes en faktureringsplangruppe til den, angives de værdier, der er defineret på siden **Faktureringsplangrupper**, som standardværdier for faktureringsplanen. Du kan ændre alle standardværdierne for den specifikke faktureringsplan, du opretter. Du kan oprette flere faktureringsplangrupper og derefter tildele en af dem som standardfaktureringsplangruppe på siden **Faktureringsparametre for tilbagevendende kontrakter**.

Hvis du vil oprette en faktureringsplangruppe for fakturering af tilbagevendende kontrakter, skal du følge disse trin.

1. Vælg **Ny** på siden **Faktureringsplangrupper** for at oprette en faktureringsplangruppe.
2. Angiv et entydigt id til kreditorgruppen i feltet **Faktureringsplangruppe**.
3. Indtast en beskrivelse i feltet **Beskrivelse**.
4. I feltet **Faktureringsfrekvens** skal du angive, hvor ofte faktureringsplanen skal faktureres til en kunde: **Engangsfakturering**, **Daglig**, **Månedlig**, **Kvartalsvis**, **Halvårlig** eller **Årlig**.
5. Angiv et tal i feltet **Faktureringsinterval**. Angiv f.eks. feltet **Faktureringsfrekvens** til **Månedlig** og feltet **Faktureringsinterval** til **2**, så der faktureres hver anden måned.
6. Vælg standardprissætningsmetoden for varer i faktureringsplanen i feltet **Prissætningsmetode**.

    - **Standard** – Beregn enhedsprisen baseret på det angivne samlede antal, og brug standardprisen fra siden **Frigivne produkter** i Administration af produktoplysninger.
    - **Flad** – Anvend en flad pris, der er angivet på faktureringsplanlinjen.
    - **Lag** – Beregn enhedsprisen ved at bruge et fast antal til forskellige prise parenteser. Hvert lag skal udfyldes, før der fortsættes til det næste prissætnings parentes.
    - **Fladt lag** – Beregn enhedsprisen ved at bruge et fast antal og udvidede prisbeløb til forskellige prise parenteser. Den pris, der opkræves i en faktureringsperiode, bruger den udvidede pris, der svarer til det niveau, hvor faktureringsantallet findes.

7. Vælg varetypen for faktureringsgruppen i feltet **Varetype**:

    - **Standard** – Vælg denne værdi, hvis antallet er statisk.
    - **Brug** – Vælg denne værdi for varer af typen forbrug eller forbrug. Hvis du vælger denne værdi, skal du indstille feltet **Forbrugsaflæsningsindstilling** til **Læsning** for at angive værdien (læsningen) for en faktureringsperiode på en tæller eller enhed. Den forbrugte værdi beregnes på baggrund af den forrige faktureringsperiode og den aktuelle læsning, som du angiver.
    - **Milepæl** – Vælg denne værdi for at bruge funktionen Milepælsfakturering. Hvis du vælger denne værdi i feltet **Milepælsskabelon**, skal du vælge milepælsskabelonen, hvis du bruger en.
    - **Forbrug** – Vælg denne værdi for at angive den værdi, der forbruges i en faktureringsperiode.

8. Angiv indstillingen **Faktura særskilt** til **Ja** for at oprette en kombination af konsoliderede fakturaer og separate fakturaer for samme debitor. En kunde har f.eks. fem faktureringsplaner. Tre af dem konsolideres på en enkelt faktura, men hver af de to andre kræver en separat faktura. Angiv indstillingen **Nej** for kun at oprette én konsolideret faktura til debitoren.
9. Indstil **Forny automatisk** til **Ja** for automatisk at forny den tilbagevendende faktureringsplan til næste fakturaperiode, når fakturaen oprettes. Angiv **Nej** for at forny faktureringsplanen manuelt. Angiv, hvor mange linjer der skal tilføjes for hver fornyelse, i feltet **Linjer, der skal tilføjes pr. fornyelse**.
10. Angiv **eskaleringsindstillingen** til **Ja** for at anvende *eskaleringer* (prisstigninger) på de faktureringsplaner, der er tilknyttet denne faktureringsplangruppe.
