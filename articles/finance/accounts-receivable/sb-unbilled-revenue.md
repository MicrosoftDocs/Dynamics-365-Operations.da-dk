---
title: Ikke-afregnet indtægt
description: Denne artikel indeholder en forklaring på, hvordan du konfigurerer varer og konti og bruger udskydelse af indtægter og udgifter i Abonnementsfakturering.
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
ms.openlocfilehash: b3fe58fc06df3f61433c8457b337ae895283e12b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879676"
---
# <a name="unbilled-revenue"></a>Ikke-afregnet indtægt

Denne artikel indeholder en beskrivelse af funktionen for ikke-faktureret omsætning, der giver dig mulighed for at medtage beløbene for hele faktureringsplaner i balancen. Disse beløb medtages på en konto for ikke-faktureret omsætning og en modkonto for ikke-faktureret omsætning, og kontrakten faktureres via afdrag.

## <a name="set-up-unbilled-revenue"></a>Opsætning af ikke-afregnet indtægt

Følg disse trin for at konfigurere ikke-afregnet indtægt.

- Felterne i sektionen **ikke-afregnet indtægt** angives automatisk på basis af værdierne på siden **Faktureringsparametre for tilbagevendende kontrakter**.
- Funktionen for ikke-faktureret omsætning kan bruges til varer, hvor feltet **Varetype** er angivet til **Standard**. Det kan også bruges udskydelse af varer. Hvis du vil bruge ikke-faktureret omsætning med kortfristede funktioner, skal du konfigurere de kortfristede indstillinger på siden **Faktureringsparametre for tilbagevendende kontrakter**.

Følg disse trin for at konfigurere varer, der ikke er afregnet indtægt for.

1. Vælg **Tilføj** på siden **Opsætning af ikke-genereret omsætning** under fanen **Varer**.
2. Vælg varekoden i **varekoden** på den nye linje.
3. Vælg varerelationen i feltet **Varerelation**.
4. Gentag disse trin for at tilføje flere linjer.
5. Vælg **Gem**.

Følg disse trin for at konfigurere konti, der ikke er afregnet indtægt for.

1. Vælg **Tilføj** på siden **Opsætning af ikke-genereret omsætning** under fanen **Konti**.
2. Vælg varekoden i **varekoden** på den nye linje.
3. Vælg varerelationen i feltet **Varerelation**.
4. Angiv kontiene for ikke-faktureret omsætning og ikke-fakturerede rabatbeløb for varen. Hvis du vil bruge kortfristede konti, skal du angive feltet **Kortfristede ikke-fakturerede metoder** til **Rulleperioder** eller **Faste perioder** på siden **Faktureringsparametrene for tilbagevendende kontrakter**.
5. Gentag disse trin for at tilføje flere linjer.
6. Vælg **Gem**.

## <a name="use-unbilled-revenue"></a>Brug ikke-afregnet indtægt

1. Opret en faktureringsplan på siden **Alle faktureringsplaner**.
2. Hvis varen endnu ikke er konfigureret til at bruge ikke-faktureret omsætning, skal du markere afkrydsningsfeltet **Ikke-faktureret omsætning** på faktureringsplanlægningslinjen.
3. Angiv indstillingen **Ikke-afregnet indtægt** til **Ja**. Gennemse, og rediger kontiene for ikke-faktureret omsætning og ikke-fakturerede rabatbeløb for varen.
4. I faktureringsplanen skal du under behandling af **ikke-faktureret omsætning** skal du vælge **Opret kladdepost** for at oprette den første kladdepost for ikke-faktureret omsætning. Dette trin skal fuldføres, før faktureringsplanen faktureres.
5. Når den første kladdepost er oprettet, skal du vælge **Opret faktura** for at oprette salgsordrer og bogføre fakturaerne for faktureringsplanerne.
6. Når fakturaerne er bogført, kan du gennemse revisionsoplysningerne under fanen **Fornyelser** på siden **Alle faktureringsplaner**.

### <a name="milestone-billing"></a>Milepælsfakturering

Milepælsfakturering fungerer med ikke-faktureret omsætning under følgende betingelser:

- Hvis den overordnede milepæl ikke er faktureret (afkrydsningsfeltet **Ikke-faktureret omsætning** er markeret), og de underordnede milepælsvarer faktureres (markeringen i afkrydsningsfeltet **Ikke-faktureret omsætning** er fjernet), skal start- og slutdatoerne for den overordnede vare angives. Disse datoer bruges til at oprette den første kladdepost.
- Hvis den overordnede milepæl ikke er faktureret (afkrydsningsfeltet **Ikke-faktureret omsætning** er ryddet), og de underordnede milepælsvarer faktureres (markeringen i afkrydsningsfeltet **Ikke-faktureret omsætning** er markeret), skal slutdatoen angives for de underordnede varer, du vil oprette indledende kladdepost for.

Hver underordnet milepælsvare kan behandles separat. Slutdatoerne kan angives, når du er klar til at oprette den første kladdepost.

> [!NOTE]
> Hvis den første kladdepostering for den overordnede milepælsvare eller underordnede varer allerede er oprettet, eller der er oprettet en faktura, kan start- og slutdatoerne ikke redigeres.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Ikke-faktureret omsætning med straight line-afdrag

Hvis du vil bruge ikke-faktureret omsætning med lineære udskydelsesplaner, skal du følge disse trin.

1. Opret en faktureringsplan på siden **Alle faktureringsplaner**.
2. Føj en vare til faktureringsplanlinjer.
3. Vælg **Udskydelser** for linjen.
4. Benyt følgende fremgangsmåde på siden **Transaktionsudskydelse**:

    1. Angiv indstillingen **Udskudt** til **Ja**.
    2. Rediger konti efter behov.
    3. Vælg **Lige linje** i sektionen **Planlæg**, og rediger andre værdier efter behov.
    4. Vælg **OK**.

5. Markér feltet **Ikke-afregnet indtægt** for linjen, og benyt derefter følgende fremgangsmåde:

    1. Angiv indstillingen **Ikke-afregnet indtægt** til **Ja**.
    2. Angiv kontiene for ikke-faktureret omsætning og ikke-fakturerede rabatbeløb for varen.

6. Vælg **Opret kladdepost** under **Behandling af ikke-faktureret omsætning** i faktureringsplanen. Alternativt kan du bruge siden **Massebehandling af ikke-genereret omsætning** til at oprette kladdeposten.
7. Udskydelsesplanen oprettes. Du kan gennemse oplysninger på siden **Alle udskydelsesplaner**. Når den er oprettet, kan du redigere forskellige værdier for linjeelementet i faktureringsplanen. Du kan f.eks. redigere enhedspris, antal eller datoer.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Ikke-frafaktureret omsætning med hændelsesbaserede hændelser

Hvis du vil bruge ikke-faktureret omsætning med hændelsesbaserede udskudte planer, skal du følge disse trin.

1. Opret en faktureringsplan på siden **Alle faktureringsplaner**.
2. Føj en vare til faktureringsplanlinjer.
3. Vælg **Udskydelser** for linjen.
4. Benyt følgende fremgangsmåde på siden **Transaktionsudskydelse**:

    1. Angiv indstillingen **Udskudt** til **Ja**.
    2. Rediger konti efter behov.
    3. Vælg **hændelsesbaseret**, **skabelon**, **fordelingstype** og **udløbskonto** i afsnittet **Planlæg**.
    4. Vælg **OK**.

5. Markér feltet **Ikke-afregnet indtægt** for linjen, og benyt derefter følgende fremgangsmåde:

    - Angiv indstillingen **Ikke-afregnet indtægt** til **Ja**.
    - Angiv kontiene for ikke-faktureret omsætning og ikke-fakturerede rabatbeløb for varen.

6. Vælg **Opret kladdepost** under **Behandling af ikke-faktureret omsætning** i faktureringsplanen. Alternativt kan du bruge siden **Massebehandling af ikke-genereret omsætning** til at oprette kladdeposten.
7. Udskydelsesplanen oprettes. Du kan gennemse oplysninger på siden **Alle udskydelsesplaner**. Når den er oprettet, kan du redigere forskellige værdier for linjeelementet i faktureringsplanen. Du kan f.eks. redigere enhedspris, antal eller datoer. Udskudt tidsplan genberegnes på basis af de nye værdier.

Fordelingerne genberegnes på basis af den valgte fordelingstype (**Procent**, **Færdiggørelsesgrad** eller **Lig med beløb**). For fordelingstypen **Variable beløb** genberegnes fordelingen på basis af den procent, der svarer til den initialværdi for hændelsen. Den oprindelige enhedspris er f.eks. $100,00, og procenten af initialværdien er $55,00 (55 procent). Hvis enhedsprisen ændres til $200,00, bliver det variable beløb for hændelsen $110,00 (stadig 55 procent).

> [!NOTE]
> Hvis det er registreres, at planlægningslinjerne er blevet udskudt, kan linjeelementet i faktureringsplanen ikke redigeres. Hvis du vil redigere linjeelementet, skal du først tilbageføre de genkendte linjer. Faktureringsplanlinjen kan nu opdateres.

### <a name="unbilled-revenue-and-top-billing"></a>Ikke-faktureret omsætning og topfakturering

Der angives en faktureringsplan for tre år, og fakturaerne faktureres én gang om året over en treårig periode. Hele kontraktbeløbet registreres på kontoen for ikke-faktureret omsætning, som de årlige fakturaer oprettes ud fra. Modkontoen er indtægts- eller udskudt omsætningskonto.

Bemærk, at topfakturering og ikke-faktureret omsætning ikke fungerer sammen, da der kan forekomme afstemningsproblemer i finansmodulet. På opsætningssiden **Varegruppe er** varegruppe A f.eks. konfigureret, så feltet **Antal øverste linjer** angives til **2**. Der tilføjes tre elementer på siden **Faktureringsplaner**. Alle tre varer tilhører varegruppe A. Når den første kladdepostering oprettes for funktionen for ikke-faktureret omsætning, behandles beløbet for alle tre varer til den ikke-fakturerede konto. Når fakturaen for faktureringsplanen oprettes, er det kun beløbene for de to øverste elementer, der medtages. Derfor stemmer fakturabeløbet ikke overens med det beløb, der blev behandlet på kontoen for ikke-faktureret omsætning, og der opstår afstemningsproblemer i finansmodulet.

Hvis du vil bruge ikke-faktureret omsætning, skal du lade siden til **opsætning af varegrupper** være tom eller konfigurere alle varegrupper, så feltet **Antal øverste linjer** angives til **0** (nul). Hvis du vil bruge topfakturering, er ingen handlinger for ikke-faktureret omsætning tilgængelige.

### <a name="examples"></a>Eksempler

Fra og med version 10.0.27 introduceres en ny konto, når der bruges ikke-genereret omsætning. Når den første proces til **oprettelse af kladdepostering** bogføres, udføres kreditten på en ny konto til modregning af ikke-bogført omsætning. Denne konto bruges i stedet for omsætningskontoen, da samme værdi skal tilbageføres, når faktureringsplanen faktureres. Hvis der opstår valutakurs- eller afrundingsdifferencer, kan de beløb, der beregnes under processen **Generér faktura**, være forskellige. Denne adfærd sikrer, at nettobeløbet på kontiene er 0 (nul).

Dette eksempel viser, hvordan du kan bruge ikke-faktureret omsætning til at anerkende hele beløbet i en kontrakt på statussen som ikke-genereret omsætning. Den anden side af posten er modkontoen for ikke-faktureret omsætning. Når du fakturerer debitoren, tilbageføres den ikke-fakturerede omsætning og modregnede ikke-fakturerede omsætning. Indtægtsføring sker enten på faktureringstidspunktet eller i overensstemmelse med den plan for indtægtsføring, der er konfigureret.

#### <a name="assumptions"></a>Forudsætninger

- Den 1. januar i det indeværende år underskriver en kunde en treårig kontrakt $390.
- Kontrakten omfatter to dele: licenser og en vedligeholdelsesaftale.
- Salgsprisen for licensgebyret betales $300, og kunden faktureres $100 1. januar hvert kontraktår. Licensgebyret $300 omsætning, når kontrakten underskrives.
- Salgsprisen for vedligeholdelsesgebyret betales $90, og kunden faktureres $30 1. januar hvert kontraktår. Det $90 vil blive udskudt, og $2,50 registreres hver måned i kontraktens levetid.
- Kunden faktureres i $130 i begyndelsen (1. januar) i hvert af kontraktens tre år.

#### <a name="steps"></a>Trin

1. Konfigurer de to frigivne varer som ikke-frafakturerede varer. Du kan bruge **Opsætning af ikke-afregnet indtægt** til at konfigurere varer og konti, der bruger ikke-genereret omsætning.
2. I dette eksempel udskydes vedligeholdelsesgebyret. Varen kræver udskydelsesskabelon, der er konfigureret på siden **Udskudte skabeloner**. Skabelonen har en **månedlig** periodefrekvens og en længden af en genkendelsesperiode på 36 måneder. Derfor er indtægten pr. måned $2,50.
3. På siden **Varer, der er udskudt som standard**, skal du angive feltet **Vedligeholdelsesgebyr** til **Vare, der kan udskydes**. Dette og det næste vil medføre, at vedligeholdelsesgebyrelementet udskydes, når den sælges eller medtages i en faktureringsplan.
4. Vælg **Udskudte standarder** \> **Skabelon**, og tilføj varen til vedligeholdelsesgebyret og den straight line-skabelon fra trin 2. Varen til vedligeholdelsesgebyret knyttes til en 36-måneders udsættelsesplan.
5. Opret en faktureringsplan, der omfatter de to ikke-fakturerede varer. Faktureringsplanen til kontrakten konfigureres med følgende varer:

    | Element | Igangsæt dato | Slutdato | Antal | Faktureringsfrekvens | Udskyd vare | Ikke-afregnet indtægt | Beskrivende tekst |
    |---|---|---|---|---|---|---|---|
    | Licens | 01. januar, CY | 31. december CY+2 | $100,00 | Årligt | Nej | Ja | Kunden faktureres $100,00 hvert år. Totalen $300,00 vil på forhånd blive registreret som ikke-faktureret omsætning på balancen og som indtægt i driftsopgørelsen. Hver faktura reducerer det ikke-fakturerede beløb. |
    | Vedligeholdelse | 01. januar, CY | 31. december CY+2 | $30,00 | Årligt | Ja | Ja | Kunden faktureres $30,00 hvert år. Totalen $90,00 vil på forhånd blive registreret som ikke-faktureret omsætning og udskudt indtægt på balancen. Hver faktura reducerer det ikke-fakturerede beløb. Den udskudte indtægt registreres en gang om måneden over 36 måneder. |

6. På siden **Alle faktureringsplaner** skal du bruge processen **Opret kladdepost** til at bogføre kontraktværdien på statussen som ikke-faktureret omsætning.

Der oprettes to kladdeposteringer, én for hver linje i faktureringsplanen.

| Ikke-afregnet indtægtskonto | Modkonto til ikke-faktureret indtægt | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| Ikke-afregnet indtægtskonto | | $300,00 | |
| | Modkonto til ikke-faktureret indtægt | | $300,00 |

| Ikke-afregnet indtægtskonto | Udskudt indtægt | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| Ikke-afregnet indtægtskonto | | $90,00 | |
| |Udskudt vedligeholdelsesindtægt | | $90,00 |

Den første kladdepostering bogføres på en konto for ikke-bogført omsætningsmodkonto, og den anden bogføres på en konto til udskudt omsætning. Hvis faktureringslinjen både har ikke-faktureret omsætning og udskudt omsætning, bruges kontoen til udskudt omsætning og ikke modkontoen for ikke-faktureret omsætning. Kontrakten kræver, at fakturaen for kunden oprettes ved begyndelsen af hvert år. Brug processen **Opret faktura** til at oprette fakturaen. Når fakturaen oprettes, oprettes følgende kladdeposteringer.

| Hovedkonto | Ikke-afregnet indtægtskonto | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| Modkonto til ikke-faktureret indtægt | | $100,00 | |
| | Ikke-afregnet indtægtskonto | | $100,00 |
| Debitor | | $100,00 | |
| | Omsætningskonto | | $100,00 |

| Hovedkonto | Ikke-afregnet indtægtskonto | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| Indtægtskonto for udskudt vedligeholdelse | | $30,00 | |
| | Ikke-afregnet indtægtskonto | | $30,00 |
| Debitor | | $30,00 | |
| | Indtægtskonto for udskudt vedligeholdelse | | $30,00 |

Denne kladdepost oprettes af fakturaer, der bogføres i begyndelsen af de næste to år. Nettobeløbet på kontoen for udskudt omsætning er 0 (nul), fordi der ikke er nogen afrundings- eller valutakursforskel. Den udskudte omsætning skal tilbageføres nøjagtigt, som den blev krediteret under processen **Opret kladdepost**. Da omsætningen stadig er udskudt og registreres senere, sker kreditten på kontoen for udskudt omsætning igen.

I sidste trin oprettes kladdeposten for indtægtsføring hver måned for at genkende indtægten af det udskudte vedligeholdelsesgebyr. Kladdeposten kan oprettes ved hjælp af siden **Behandling af genkendelse**. Alternativt kan den oprettes ved at vælge **Genkend** for linjerne på siderne **Udskudt plan**.

| Udskudt indtægtskonto | Omsætningskonto | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| Udskudt vedligeholdelsesindtægt | | $2,50 | |
| | Vedligeholdelsesindtægt | | $2,50 |

Denne kladdepost oprettes, hver gang der køres en registreringsproces for denne udskudte vare (i alt 36 gange).

#### <a name="short-term-fixed-year"></a>Kortsigtede: Fast år

Du kan bruge ikke-faktureret omsætning sammen med kortfristede funktioner, skal du konfigurere de **kortfristede indstillinger** på siden **Faktureringsparametre for tilbagevendende kontrakter**. I følgende eksempel vises de beregninger, der udføres, når ikke-faktureret omsætning bruges sammen med metoden for kortfristet ved et **fast år**.

Der oprettes en faktureringsplan med følgende kriterier:

- **Startdato:** 1. juni 2020
- **Slutdato:** 31 december 2021
- **Enhedspris:** $100
- **Frekvens:** Månedlig

På siden **Alle faktureringsplaner** oprettes den første kladdepost af processen **Opret kladdepost**. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $700
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $1.200

Fakturaen oprettes for faktureringsperioden fra 1. juni 2020 til og med 30. november 2020. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $100
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $1.200

Fakturaen oprettes for faktureringsperioden fra 1. december 2020 til og med 31. december 2020. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $1.200
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $0

#### <a name="short-term-rolling-periods"></a>Kortfrist: Rulleperioder

Du kan bruge ikke-faktureret omsætning sammen med kortfristede funktioner, skal du konfigurere de kortfristede indstillinger på siden **Faktureringsparametre for tilbagevendende kontrakter**. I følgende eksempel vises de beregninger, der udføres, når ikke-faktureret omsætning bruges sammen med **Rulleperioder** for kortfristet.

Der oprettes en faktureringsplan med følgende kriterier:

- **Startdato:** 1. juni 2020
- **Slutdato:** 31 december 2021
- **Enhedspris:** $100
- **Frekvens:** Månedlig

På siden **Alle faktureringsplaner** oprettes den første kladdepost af processen **Opret kladdepost**. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $1.200
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $700

Fakturaen oprettes for faktureringsperioden fra 1. juni 2020 til og med 30. november 2020. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $1.200
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $100

Fakturaen oprettes for faktureringsperioden fra 1. december 2020 til og med 31. december 2020. De aktuelle kort- og langfristede beløb beregnes på følgende måde:

- **Aktuelt kortsigtet ikke-faktureret omsætningsbeløb:** $1.200
- **Aktuelt langsigtet ikke-faktureret omsætningsbeløb:** $0

### <a name="items-with-revenue-allocation"></a>Varer med indtægtsfordeling

To elementer, der har forskellige faktureringsfrekvenser, føjes til en faktureringsplan. De bruger både ikke-faktureret omsætning og er varer, der kan afdrages.

- **Varenummer 1000:** Surface Pro 128 GB

    - **Faktureringsfrekvens:** En gang
    - **Enhedspris:** $1.500
    - **Enkeltstående salgspris:** $1.600
    - **Kontraktindtægt:** $1.465,26

- **Varenummer S0021:** Forsikring, der sælges sammen med varenummer 1000

    - **Faktureringsfrekvens:** Månedligt for 12 måneder
    - **Enhedspris:** $20 pr. måned
    - **Enkeltstående salgspris:** $25
    - **Kontraktindtægt:** $264,74

Da begge varer bruger ikke-faktureret omsætning og indtægtsfordeling, er det samlede kontraktbeløb på fornyelseslinjen 0 (nul). Kolonnen **Kontraktomsætning** tilføjes og viser omsætningsbeløbet for kontrakten.

I følgende tabel vises den første kladdepostering for varerne og fakturaen.

| Ikke-afregnet indtægtskonto | Udskudt indtægtskonto | Debetbeløb | Kreditbeløb |
|---|---|---|---|
| **Vare 1000 kladdepostering** | | | |
| Debet ikke-afregnet indtægtskonto (401250) | | $1.465,26 | |
| | Kreditudskudt indtægtskonto (250600) | | $1.465,26 |
| **Vare 0021 kladdepostering** | | | |
| Debet ikke-afregnet indtægtskonto (401250) | | $274,74 | |
| | Kreditudskudt indtægtskonto (250600) | | $274,74 |
| **Fakturaer** | | | |
| | Ikke-afregnet kreditindtægtskonto | | $1.465,26 |
| | Ikke-afregnet kreditindtægtskonto | | $274,74 |
| Debetkonto AR (130100) | | $1.488,16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Ændringer i faktureringsplanlinjen, faktureringsdetaljelinjen eller indtægtsfordelingen

Når enhedsprisen eller antallet ændres, skal kontraktomsætningsbeløbet for hver vare, der er en del af indtægtsfordelingen, opdateres. Kladdeposten genberegnes derfor.

Enhedsprisen for vare 1000 ændres f.eks. fra $1.500 til $1.600. I dette tilfælde genberegnes omsætningsbeløbet for kontrakten automatisk som $1.549,47. Kontraktomsætningen for varen S0021 genberegnes som $290,53.

Når de ændrede er bekræftet og bindende, tilbageføres de første kladdeposteringer for begge varer, og der oprettes nye kladdeposteringer:

- **Vare 1000:** Den oprindelige første kladdepost $1.465,26 tilbageføres. Der oprettes en ny sikkerhedslagerkladde for $1.549,47.
- **Vare S0021:** Den oprindelige første kladdepost $274,74 tilbageføres. Der oprettes en ny sikkerhedslagerkladde for $290,53.

#### <a name="termination"></a>Ophør

Vare S0021 har en startdato i januar 2020 og en slutdato i december 2020, men den ophører i juni 2020. Kontraktens omsætningsbeløb for begge varer skal genberegnes:

- **Vare 1000:** Kontraktomsætningen genberegnes som $1.567,67.
- **Vare S0021:** Kontraktomsætningen genberegnes som $124,00.

Der oprettes en reguleringskladdepost for den linje, der er afsluttet. Kladdeposten for den linje, der tilhører samme MEA-nummer (multiple element arrangement), tilbageføres, og der oprettes en ny kladdepost:

- **Vare 1000:** Den oprindelige første kladdepost $1.465,26 tilbageføres. Der oprettes en justeringslagerkladde for $1.549,47.
- **Vare S0021:** Den oprindelige første kladdepost $274,74 tilbageføres. Der oprettes en ny sikkerhedslagerkladde for $124,00.
