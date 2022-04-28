---
title: Udskydelsestransaktioner i abonnementsfakturering
description: Dette emne beskriver de forskellige transaktioner, der kan bruges i udskydelsestransaktioner som en del af indtægts- og udgiftsudskydelser i Abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f66c538afc732caf3faed3cfea6c695ff7f16273
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2022
ms.locfileid: "8558090"
---
# <a name="deferral-default-transactions"></a>Standardtransaktioner for udskydelse

Dette emne beskriver de transaktioner, der giver mulighed for indtægts- og udgiftsudskydelser. Udskydelsesplaner er altid baseret på og afhænger af et oprindelige dokument eller en faktureringsplan. Udskydelsesplaner oprettes på basis af standarder og kan ikke angives eller oprettes separat.

## <a name="sales-order-transaction-deferral"></a>Udskydelse af salgsordretransaktion

Brug siden **Udskydelser** eller **Opret kreditnota** til at angive eller redigere udskydelsesparametrene for en salgsordrelinje.

> [!NOTE]
> Når en salgsordre oprettes ud fra en faktureringsplan, er alle værdierne på siden **Udskydelser** eller **Opret kreditnota** skrivebeskyttet, og udskydelsesparametrene kan ikke redigeres. Hvis du vil redigere værdierne, skal du bruge siden **Rediger tidsplan**.

### <a name="edit-deferral-options"></a>Redigere indstillinger for udskydelse

Hvis du vil redigere indstillingerne for udskydelse af en linje, skal du følge disse trin.

1. Opret en salgsordretransaktion.
2. Vælg linjen, og vælg derefter **Udskydelser**.
3. På siden **Transaktionsudskydelse** skal indstillingen **Udskudt** angives til **Ja**. Hvis det er nødvendigt, kan du redigere andre felter.
4. Vælg **Eksempel** for at få vist udskydelsesplanen.
5. Hvis du har foretaget ændringer i transaktionsudskydelsen, skal du vælge **OK** og vende tilbage til transaktionssiden.
6. Bekræfte og bogføre transaktionen.

Når transaktionen er bogført, skal du åbne siden **Alle udskydelsesplaner** for at få vist udskydelsesplanen.

### <a name="create-a-credit-note"></a>Oprette en kreditnota

Følg disse trin for at oprette en kreditnota.

1. Opret en salgsordretransaktion.
2. Vælg den vare, du vil oprette en kreditnota for, i sektionen **Salgsordrelinjer**.
3. Vælg **Salgsordrelinje** \> **Ny**, og vælg derefter **Kreditnota**.
4. Vælg **Udskydelser**.
5. Angiv indstillingen **Juster eksisterende plan** til **Ja** for varen på siden **Udskydelse af salgsordretransaktion**.
6. Vælg den udskydelsesplan, som du vil anvende kreditnotaen på, i feltet **Reguleret plan**.
7. Opdater felterne **Genberegn dato** og **Slutdato** efter behov.
8. Vælg **OK**.
9. Afslut bogføring af salgsordretransaktionen.

### <a name="purchase-orders-and-purchase-invoices"></a>Indkøbsordrer og indkøbsfakturaer

Hvis du vil bruge udskydelsesfunktionen til en indkøbsordre, skal du først generere fakturaen. Brug derefter siden **Ventende kreditorfakturaer** til at redigere eller tilføje udskydelsesvarer. Du kan ikke redigere eller tilføje udskydelser direkte i en indkøbsordre.

1. Brug siden **Ventende kreditorfakturaer** til at angive en kreditorfaktura.

    Når du angiver en linje, angives udskydelsen automatisk til den vare eller indkøbskategori, du vælger. Denne udskydelse er baseret på konfigurationen af udskydelse på siden **Standardudskydelser**. Udskydelsen kan redigeres eller tilføjes på fordelingsniveau.

3. Vælg **Finans \> Fordel beløb** på indkøbslinjen.
4. For hvert fordelingsbeløb skal du vælge **Udskydelser**. Når fakturaen bogføres, oprettes der en udskydelsesplan for hver fordeling, som en udskydelse er angivet til.

### <a name="tax"></a>Moms

I nogle tilfælde kan momsbeløbet være helt eller delvist ikke-refunderbart. Hvis momsbeløbet på en udskydningslinje, indeholder et beløb, der ikke kan refunderes, medtages det momsbeløb, der ikke kan refunderes, i udskydningsplanens beløb, når fakturaen bogføres.

### <a name="variance"></a>Afvigelse

Hvis beløbet på kreditorfakturalinjen afviger fra beløbet på indkøbsordrelinjen, oprettes der afvigelsesfordelinger. Hvis linjen udskydes, angives finanskontoen for disse fordelinger til udskydningskontoen, og beløbene medtages i udskydningsplanens beløb, når fakturaen bogføres. Disse fordelinger kaldes **Prisafvigelse** og **Omkostningsafvigelse**.

### <a name="general-journals-and-invoice-journals"></a>Finanskladder og fakturakladder

Du kan bruge siden **Udskydelser** til at angive udskydelsesparametrene for en kladdebilagslinje. Du kan også få en forhåndsvisning af udskydelsesplanen for lineære udskydelser. Når du angiver en linje, angives udskydelsen automatisk på baggrund af opsætningen af udskydelseskonti på siden **Standardudskydelser**. Du kan manuelt ændre udskydelsesindstillingerne for de enkelte linjer. Når kladdebilaget bogføres, oprettes udskydelsesplanen.

#### <a name="post-and-transfer"></a>Bogfør og overfør

Hvis du vil bogføre kladdebilaget, skal du bruge kommandoen **Bogfør og overfør**. Udskydelsesindstillingerne følger den linje, som bilaget gælder for. For bilag, der ikke indeholder fejl, oprettes der en udskydelsesplan, hvis det er udskudt. For et bilag, der indeholder en fejl og overføres, overføres eventuelle udskydelsesindstillinger også med det.

#### <a name="tax"></a>Moms

I nogle tilfælde kan momsbeløbet være helt eller delvist ikke-refunderbart. Hvis momsbeløbet på en udskydningslinje, indeholder et beløb, der ikke kan refunderes, medtages det momsbeløb, der ikke kan refunderes, i udskydningsplanens beløb, når fakturaen bogføres.

## <a name="free-text-invoice-transaction-deferral"></a>Transaktionsudskydelse af fritekstfaktura

Du kan bruge siden **Udskydelser** til at angive udskydelsesparametrene for en fordeling af fritekstfakturalinje. Når en fordeling er angivet, angives udskydelsen automatisk på baggrund af udskydelsesindstillingerne på siden **Standardudskydelser**.

## <a name="fields"></a>Felter

Siden **Transaktionsudskydelse** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Udskudt | <p>Angiv, om linjen er en udskydelse:</p><ul><li>**Ja** – Linjen er en udskydelse.</li><li>**Nej** – Linjen er ikke en udskydelse.</li></ul><p>Når denne indstilling er angivet til **Ja**, er indstillingen **Juster eksisterende plan** ikke tilgængelig. For varer og gebyrer, der allerede er angivet som udskudt, angives denne indstilling til **Ja**. For varer og gebyrer, der ikke som standard er angivet som udskudt, skal du angive denne indstilling til **Ja**.</p> |
| Juster eksisterende tidsplan | <p>Angiv, om linjen er en regulering af en eksisterende udskydelsesplan:</p><ul><li>**Ja** – Den nye salgslinje er en regulering af en eksisterende udskydelsesplan. I dette tilfælde kan du vælge en udskydelsesplan i feltet **Reguleret plan**.</li><li>**Nej** – Den nye salgslinje er ikke en regulering af en eksisterende udskydelsesplan.</li></ul><p>Når denne indstilling er angivet til **Ja**, er indstillingen **Udskudt** ikke tilgængelig.</p> |
| Justeret tidsplan | <p>Vælg den udskydelsesplan, som linjen justerer. Alle værdier på siden opdateres derefter med værdierne fra den oprindelige udskydelsesplan. Disse værdier kan ikke redigeres.</p><p>Feltet er kun tilgængeligt, når indstillingen **Juster eksisterende plan** er angivet til **Ja**.</p> |
| Genberegningsdato | <p>Angiv startdatoen for den periode, hvorfra du vil genberegne restbeløbet. Standarddatoen er datoen for den næste ikke-anerkendte periode.</p><p>Feltet er kun tilgængeligt, når indstillingen **Juster eksisterende plan** er angivet til **Ja**.</p> |
| Slutdato | <p>Afhængigt af typen af udskydelse kan slutdatoen muligvis ikke opdateres:</p><ul><li>Angiv den nye slutdato for planen for en lineær udskydelse. Standardværdien er den eksisterende slutdato for udskydelsesplanen.</li><li>Angiv slutdatoen for kredithændelseslinjen for en hændelsesbaseret udskydelse. Denne dato kan være tom.</li></ul><p>Feltet er kun tilgængeligt, når indstillingen **Juster eksisterende plan** er angivet til **Ja**.</p> |
| Faktureringsplannummer | <p>Nummeret på faktureringsplanen.</p><p>Dette felt er kun tilgængeligt for faktureringsplaner for tilbagevendende kontrakter.</p> |
| Reguleringsmetode for udskydelse | <p>Metoden til udskudt regulering. Værdien svarer til værdien på siden **Behandling af masseafslutning** for faktureringsplanen for den tilbagevendende kontrakt.</p><p>Dette felt er kun tilgængeligt for faktureringsplaner for tilbagevendende kontrakter.</p> |
| **Konti - Indtægter** | |
| Udskydelseskonto | <p>Udskydelseskontoen, som er den bogføringskonto, der vises på siden **Salgsordre**.</p><p>Hvis linjen ikke er udskudt, er dette felt tomt. I så fald er bogføringskontoen standardindtægtskontoen.</p> |
| Føringskonto | <p>Angiv den konto, der bruges, når en udskydelse er anerkendt. Denne konto skal være en anden end udskydelseskontoen.</p><p>Når indstillingen **Udskudt** først angives til **Ja**, kopieres de dimensionsværdier, der bruges i udskydelseskontoen, til føringskontoen. Hvis dimensionen i udskydelseskontoen ikke findes for føringskontoen, ignoreres den.</p> |
| Første føringskonto | <p>Vælg kontoen til den første indtægtsføring. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| Føringsmodkonto | <p>Vælg modkontoen til indtægtsføring. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| **Konti - Rabat** | Dette afsnit vises kun for udskudte varer. Det er skjult for udskudte gebyrer. |
| Udskydelseskonto | <p>Angiv kontonummeret for rabatudskydelse. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Rabatudskydelse** er angivet til **Separat plan for rabat** på siden **Udskydelsesparametre for indtægt og udgift**, og der anvendes en rabat på linjen.</p> |
| Føringskonto | <p>Angiv føringskontonummeret for rabat. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Rabatudskydelse** er angivet til **Separat plan for rabat** på siden **Udskydelsesparametre for indtægt og udgift**, og der anvendes en rabat på linjen.</p> |
| Første føringskonto | <p>Vælg kontoen til den første rabatføring. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**, og der anvendes en rabat på linjen.</p> |
| Føringsmodkonto | <p>Vælg modkontoen til indtægtsføring. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**, og der anvendes en rabat på linjen.</p> |
| **Konti – Forbrug** | Dette afsnit vises kun for udskudte varer. Det er skjult for udskudte gebyrer. |
| Udskydelseskonto | <p>Angiv kontonummeret for forbrugsudskydelse.</p><p>For standardprodukter oprettes der to udskydelsesplaner:</p><ul><li>**Standardsalg** – En indtægtstidsplan, der har en kreditsaldo. I dette tilfælde skal du vælge forbrugsudskydelseskontoen.</li><li>**Forbrug** – En udgiftsplan for forbrug (vareforbrug \[COGS)\], der har en debetsaldo. I dette tilfælde skal du vælge forbrugsføringsskontoen.</li></ul><p>Når fakturaen bogføres, bogføres forbrugsbeløbet på den angivne forbrugsudskydelseskonto. Disse felter er ikke tilgængelige for servicevarer.</p> |
| Føringskonto | Angiv kontonummeret for forbrugsføring. |
| Første føringskonto | <p>Angiv kontoen til det første forbrugsføringsbeløb. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| Føringsmodkonto | <p>Angiv kontoen til det første modbeløb til forbrugsføring. Standardværdien er fra siden **Standardudskydelser**.</p><p>Dette felt er kun tilgængeligt, når feltet **Bogføringsmetode for udskydelse** er angivet til **Drift** på siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| **Tidsplan** | |
| Tidsplantype | <p>Vælg udskydelsesplantypen: **Lineær** (standard) eller **Hændelsesbaseret**.</p><p>De indstillinger, der vises på siden, er baseret på den planlægningstype for udskydelse, som du vælger.</p><p>Hvis standardskabelonen er angivet på siden **Udskydelsesstandarder** for transaktionslinjen, er udskydelsesplantypen baseret på den valgte skabelontype.</p> |
| **Tidsplan - Lineær** | |
| Konsolider tidligere perioder | <p>Angiv, om du vil konsolidere udskydelsesplanlinjer for tidligere perioder:</p><ul><li>**Ja** – Konsolider udskydelsesplanlinjer for tidligere perioder.</li><li>**Nej** – Konsolider ikke udskydelsesplanlinjer for tidligere perioder.</li></ul><p>Standardværdien er fra siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| Ens pr. periode | <p>Angiv, om antallet af dage i hver periode er ens eller varierer efter periode:</p><ul><li>**Ja** – Hver periode har samme antal dage.</li><li>**Nej** – Perioder har ikke samme antal dage.</li></ul><p>Når denne indstilling er angivet til **Nej**, tages der hensyn til antallet af dage i en periode, når beløbet i hver periode for en udskydelsesplan beregnes.</p><p>Standardværdien er fra siden **Udskydelsesparametre for indtægt og udgift**.</p> |
| Planlæg fra skabelon | <p>Angiv, om udskydelsesplanen oprettes på basis af en skabelon eller en slutdato:</p><ul><li>**Ja** – Udskydelsesplanen oprettes på basis af en skabelon.</li><li>**Nej** – Udskydelsesplanen oprettes på basis af en slutdato.</li></ul> |
| Skabelon | Vælg udskydelsesskabelonen. |
| Tilsidesættelsesstartdato | <p>Angiv, om startdatoen skal tilsidesættes:</p><ul><li>**Ja** – Tilsidesæt startdatoen med den dato, du angiver i feltet **Startdato**.</li><li>**Nej** – Startdatoen er reglen **Standardstartdato for udskydelse**, der anvendes på den fakturadato, der er angivet på siden **Bogføring af faktura**. Denne regel kan angives på siden **Udskydelsesparametre for indtægt og udgift**.</li></ul> |
| Startdato for udskydelse | Angiv udskydelsens startdato. Standardværdien er transaktionsdatoen. |
| Slutdato for udskydelse | <p>Slutdatoen for udskydelsen.</p><p>Denne dato beregnes automatisk ud fra udskydelsesskabelonen. Hvis der ikke er valgt en skabelon, skal du angive datoen manuelt.</p> |
| **Tidsplan - Hændelsesbaseret** | |
| Skabelon | <p>Vælg den hændelsesbaserede skabelon. Dette felt er valgfrit.</p><p>Hvis du vælger en skabelon, overskriver værdierne i skabelonen alle hændelsesbaserede data og hændelseslinjer.</p> |
| Fordelingstype | <p>Vælg fordelingstypen for hændelseslinjerne:</p><ul><li>**Variable beløb** – Der angives et specifikt fordelingsbeløb for hver linje.</li><li>**Lige store beløb** – Beløbet fordeles ligeligt på hver linje.</li><li>**Procent** – Et beløb tildeles på basis af den procentværdi, der er angivet for hver linje.</li><li>**Færdiggørelsesgrad** – En akkumuleret færdiggørelsesværdi angives til hver linje.</li><p>**Variabelt antal** – Der angives et specifikt fordelingsantal for hver linje.</li></ul><p>**Bemærk:** Hvis du vil vælge **Færdiggørelsesgrad**, skal datoerne være i stigende rækkefølge.</p> |
| **Opret separate hændelser pr. enhed** | |
| Beskrivelse | <p>Angiv, om hændelserne skal adskilles pr. enhed:</p><ul><li>**Ja** – Adskil hændelseslinjerne, så der er én linje pr. antal.<p>Der er f.eks. tre hændelseslinjer, og fakturaen har et antal på fire. I dette tilfælde indeholder den resulterende udskydelseskalender 12 linjer.</p></li><li>**Nej** – Adskil ikke hændelseslinjerne.</li></ul> |
| Udløbskonto | <p>Vælg den konto, der bruges til registrerede udløbne linjer. Du kan vælge kontoen, når udskydelseskalenderen er oprettet.</p><p>Hvis der er angivet en udløbsdato for en hændelse, går føringsbeløbet til udløbskontoen i stedet for føringsskontoen under føringsprocessen.</p> |
| **Tidsplan - Hændelsesbaserede linjer** | |
| Beskrivelse | En beskrivelse af hændelsen. |
| Slutdato for udskydelse | <p>Vælg hændelsens slutdato.</p><p>**Bemærk:** Hvis du vælger en slutdato, ryddes feltet **Udløbsdato**. Du kan ikke både bruge en slutdato og en udløbsdato.</p> |
| Udløbsdato | <p>Vælg hændelsens udløbsdato.</p><p>**Bemærk:** Hvis du vælger en slutdato, ryddes feltet **Udløbsdato**. Du kan ikke både bruge en slutdato og en udløbsdato.</p> |
| Quantity | <p>Angiv fordelingsantallet. Standardværdien for alle linjer er **0** (nul). Hvis du opdaterer antallet, skal det samlede antal for alle linjer være lig med eller mindre end det antal, der er angivet for linjevaren på salgsordren.</p><p>Dette felt er kun tilgængeligt, når feltet **Fordelingstype** er angivet til **Variabelt antal**.</p><p>Hvis antallet af linjevaren på salgsordren ændres, så det er mindre end det oprindelige antal, og fakturaen oprettes, oprettes der færre hændelsesbaserede linjer. Det samlede tildelte antal må ikke overstige det antal, der er angivet i den oprindelige salgsordre eller faktureringsplan.</p> |
| Fordelingsprocent | <p>Angiv fordelingsprocenten. Hvis feltet **Fordelingstype** er angivet til **Procent** eller **Færdiggørelsesgrad**, kan du manuelt angive en procent. Ellers beregnes den automatisk.</p><p>Hvis feltet **Fordelingstype** er angivet til **Procent**, skal de samlede procentsatser være lig med 100.</p> |
| Beløb | <p>Angiv fordelingsbeløbet. Hvis feltet **Fordelingstype** er angivet til **Variable beløb** eller **Færdiggørelsesgrad**, kan du manuelt angive et beløb.</p><p>Hvis feltet **Fordelingstype** er angivet til **Færdiggørelsesgrad**, og du angiver et beløb her, beregnes værdien i feltet **Færdiggørelsesprocent** automatisk.</p><p>På grund af afrunding svarer det beregnede beløb muligvis ikke præcist til det, der angives manuelt. Hvis du skal bruge et nøjagtigt beløb, skal du angive feltet **Fordelingstype** til **Variable beløb**.</p> |
| Færdiggørelsesprocent | <p>Angiv færdiggørelsesgraden. Værdien skal være mellem 0 (nul) og 100.</p><p>Dette felt er kun tilgængeligt, når feltet **Fordelingstype** er angivet til **Færdiggørelsesgrad**.</p> |
| Færdiggørelsesbeløb | <p>Den beregnede total for alle linjer udskydelseskalenderen.</p><p>Hvis feltet **Fordelingstype** er angivet til **Færdiggørelsesgrad**, kan du manuelt angive et beløb. I dette tilfælde beregnes værdien i feltet **Færdiggørelsesprocent** baseret på det beløb, du angiver.</p><p>På grund af afrunding svarer det beregnede beløb muligvis ikke præcist til det, der angives manuelt.</p><p>Dette felt er kun tilgængeligt, når feltet **Fordelingstype** er angivet til **Færdiggørelsesgrad**.</p> |
| Registrer ved bogføring | <p>Angiv, om linjen registreres automatisk, så snart transaktionen bogføres:</p><ul><li>**Markeret** – Linjen registreres automatisk, så snart transaktionen bogføres.</li><li>**Ryddet** – Linjen registreres ikke, så snart transaktionen bogføres.</li></ul> |
| Føringskonto | <p>Angiv føringskontoen for hændelsen, hvis kontoen er forskellig fra den konto, der bruges til hele udskydelsesplanen.</p><p>Du kan bruge dette felt sammen med indstillingen **Registrer ved bogføring**.</p> |
