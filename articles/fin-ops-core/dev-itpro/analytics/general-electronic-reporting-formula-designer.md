---
title: Formeldesigner i elektronisk rapportering (ER)
description: Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43700d68587cebfb4f897c8a5b619dd4771cc439
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181306"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner i elektronisk rapportering (ER)

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge formler til at transformere data, så de opfylder kravene til dokumentets udførelse og formatering. Disse formler ligner formler i Microsoft Excel. Forskellige typer funktioner understøttes i formlerne: tekst, dato og klokkeslæt, matematisk logik, oplysninger, konvertering af datatypen og andre (domænespecifikke funktioner i virksomheden).

## <a name="formula-designer-overview"></a>Oversigt over formeldesigner

Elektronisk rapportering (ER) understøtter formeldesigneren. Derfor kan du på designtidspunktet konfigurere udtryk, der kan bruges til følgende opgaver under kørsel:

- Konverter data, der modtages fra en programdatabase, og som skal angives i en ER-datamodel, der er designet til at være datakilde for ER-formater. (F.eks. kan disse transformeringer kan omfatte filtrering, gruppering og datatypekonvertering).
- Formatere de data, der skal sendes til et genereret elektroniske dokument i overensstemmelse med det layout og betingelserne for et bestemt ER-format. (Formatering kan f.eks. udføres i overensstemmelse med det ønskede sprog eller kultur eller kodning).
- Styre processen til oprettelse af elektroniske dokumenter. (F.eks. kan udtrykkene aktivere eller deaktivere outputtet af bestemte elementer i formatet, afhængigt af behandlingen af data. De kan også afbryde processen med oprettelse af dokumentet eller udløse meddelelser til brugere).

Du kan åbne siden **Formeldesigner**, når du udfører en af følgende handlinger:

- Binder datakildeelementer til datamodelkomponenter.
- Binder datakildeelementer til formatkomponenter.
- Vedligeholder beregnede felter som en del af datakilder.
- Definerer synlighedsbetingelser for brugerinputparametre.
- Designer formatets transformeringer.
- Definerer aktivering af betingelserne for formatets komponenter.
- Definerer filnavne til formatets FILE-komponenter.
- Definerer betingelserne for proceskontrolvalideringer.
- Definerer meddelelsestekst for proceskontrolvalideringer.

## <a name="designing-er-formulas"></a>Design af ER-formler

### <a name="data-binding"></a>Databinding

ER-formeldesigneren kan bruges til at definere et udtryk, der transformerer data, der er modtaget fra datakilder, så data kan angives i dataforbrugeren under kørsel:

- Fra programdatakilder og kørselsparametre til en ER-datamodel
- Fra en ER-datamodel til et ER-format
- Fra programdatakilder og kørselsparametre til et ER-format

I følgende illustration vises et udtryk af denne type design. I dette eksempel afrunder udtrykket værdien af feltet **Intrastat.AmountMST** i Intrastat-tabellen til to decimaler og returnerer den afrundede værdi.

[![Databinding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

I følgende illustration vises, hvordan et udtryk af denne type kan bruges. I dette eksempel er resultatet af det designede udtryk angivet i **Transaction.InvoicedAmount**-komponenten af **momsrapporteringsmodellen**.

[![Databinding bruges](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

På kørselstidspunktet afrunder den designede formel **ROUND (Intrastat.AmountMST, 2)** værdien af feltet **AmountMST** for hver post i Intrastattabellen til to decimaler. Den indsætter derefter den afrundede værdi i komponenten **Transaction.InvoicedAmount** i datamodellen **Momsrapportering**.

### <a name="data-formatting"></a>Dataformatering

ER-formeldesigneren kan bruges til at definere et udtryk, der formaterer data, der er modtaget fra datakilder, så data kan sendes som en del af det genererende elektroniske dokument. Du har muligvis formatering, der skal anvendes som en typisk regel, der skal genbruges til et format. I så fald kan du introducere denne formatering én gang i formatkonfigurationen, som en navngivet transformering, der har et formateringsudtryk. Denne navngivne transformation kan sammenkædes med mange formatkomponenter, hvor outputtet skal været formateret i henhold til det formateringsudtryk, du oprettede.

I følgende illustration vises designet af en transformation af denne type. Dette eksempel på **TrimmedString**-transformation afkorter indgående data i af datatypen **Streng** ved at fjerne foranstillede og efterstillede mellemrum. Derefter returneres den afkortede strengværdi.

[![Transformation](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

I følgende illustration vises, hvordan en transformation af denne type kan bruges. I dette eksempel sender flere komponenter tekst som output til det generere elektroniske dokument på kørselstidspunktet. Alle disse formatkomponenter refererer til transformationen **TrimmedString** efter navn.

[![Transformation, der bruges](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Når formatkomponenter refererer til **TrimmedString-**-transformation (for eksempel **partyName**-komponenten i den foregående illustration), sendes tekst som output for at generere det elektroniske dokument. Denne tekst indeholder ikke foranstillede eller efterstillede mellemrum.

Hvis du har en formatering, der skal anvendes individuelt, kan den indføres som et individuelt udtryk for binding af en bestemt formatkomponent. I følgende illustration vises et udtryk af denne type. I dette eksempel er **partyType**-formatkomponenten bundet til datakilden via et udtryk, der konverterer indgående data fra feltet **Model.Company.RegistrationType** i datakilden til stor bogstavtekst. Udtrykket sender derefter teksten som output til det elektroniske dokument.

[![Anvende formatering på en enkelt komponent](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Kontrol af procesforløb

ER-formeldesigneren kan bruges til at definere udtryk, der styrer procesforløbet under generering af elektroniske dokumenter. Du kan udføre følgende opgaver:

- Definer betingelser, der bestemmer, hvornår en proces til oprettelse af dokumentet skal stoppes.
- Angiv udtryk, der opretter enten meddelelser til slutbrugeren om stoppede processer eller udløser en kørselslogbesked om, at processen fortsætter med oprettelse af rapporter.
- Angiv filnavne til oprettelse af elektroniske dokumenter, og kontrollér betingelserne for deres oprettelse.

Hver regel i kontrol af procesforløb udformet som en enkelt validering. I følgende illustration vises en validering af denne type. Her er en forklaring af konfigurationen i dette eksempel:

- Valideringen evalueres, når **INSTAT**-noden oprettes under generering af XML-filen.
- Hvis listen over transaktioner er tom, stopper valideringen kørselsprocessen og returnerer **FALSE**.
- Valideringen returnerer en fejlmeddelelse, der indeholder teksten til etiketten for SYS70894 på brugerens foretrukne sprog.

[![Validering](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER-formeldesigneren bruges også til at generere et filnavn til et genererende elektronisk dokument og styring af processen til oprettelse af en fil. I følgende illustration vises designet af en kontrol af procesforløb af denne type. Her er en forklaring af konfigurationen i dette eksempel:

- Listen over poster fra datakilden **model. Intrastat-** er opdelt i batches. Hver batch indeholder op til 1000 poster.
- Output opretter en zip-fil, der indeholder en fil i XML-format for hver batch, der blev oprettet.
- Et udtryk returnerer et filnavn til generering af elektroniske dokumenter ved at sammenkæde filnavnet og filtypenavnet. For den anden batch og alle efterfølgende batches indeholder filnavnet batch-ID som et suffiks.
- Et udtryk aktiverer (returnerer **TRUE**) processen med en filoprettelse for de eneste batches, der indeholder mindst én post.

[![Filstyring](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="documents-content-control"></a>Kontrol af dokumentindhold

Er-formeldesigneren kan bruges til at konfigurere udtryk, der styrer, hvilke data der placeres i genererede elektroniske dokumenter på kørselstidspunktet. Udtrykkene kan aktivere eller deaktivere outputtet af bestemte elementer i formatet, afhængigt af behandlingen af data og den konfigurerede logik. Disse udtryk kan angives for et enkelt formatelement i feltet **Aktiveret** under fanen **Tilknytning** på siden **Operationsdesigner** som en logisk betingelse, der returnerer den **booleske værdi**:

-   Når **Sand** returneres, udføres det aktuelle formatelement.
-   Når **Falsk** returneres, udføres det aktuelle formatelement ikke.

I følgende illustration vises udtryk af denne type (version **11.12.11** for den **ISO20022-kreditoverførsel (nr.)**-formatkonfiguration, der er leveret af Microsoft, er et eksempel). Formatkomponenten **XMLHeader** er konfigureret til at beskrive strukturen i en kreditoverførselsmeddelelse, der følger ISO 20022 XML-meddelelsesstandarderne. Formatkomponenten **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** er konfigureret til at føje til den genererede meddelelse, **Ustrd**-XML-elementet, og placere remitteringsoplysningerne i et ustruktureret format som tekst i følgende XML-elementer:

-   **PaymentNotes**-komponenten bruges til at udskrive tekst på betalingsnoter.
-   **DelimitedSequence**-komponenten udskriver kommaseparerede fakturanumre, der bruges til at afstemme den aktuelle kreditoverførsel.

[![Operationsdesigner](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes**- og **DelimitedSequence**-komponenterne er mærket ved hjælp af et spørgsmålstegn. Det betyder, at brugen af begge komponenter er betinget, baseret på følgende kriterier:

-   Defineret for komponenten **PaymentNote** muliggør udtrykket **@.PaymentsNotes < >""** (ved at returnere **TRUE**) udfyldningen af **Ustrd**-XML-elementet med teksten for betalingsnoter, når denne tekst til den aktuelle kreditoverførsel ikke er tom.

[![Operationsdesigner](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)

-   Defineret for komponenten **DelimitedSequence** muliggør udtrykket **@.PaymentsNotes=""** (ved at returnere **TRUE**) udfyldningen af **Ustrd**-XML-elementet, adskilt af komma, med fakturanumre, der bruges til at afstemme den aktuelle kreditoverførsel, når teksten i betalingsnoter til denne kreditoverførsel er tom.

[![Operationsdesigner](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)

Baseret på denne indstilling indeholder den genererede meddelelse for hver debitorbetaling, **Ustrd**-XML-elementet, enten tekst med betalingsnoter eller, når denne tekst er tom, tekst, der er adskilt af komma, fakturanumre, som bruges til at afstemme denne betaling.

### <a name="basic-syntax"></a>Grundlæggende syntaks

ER udtryk kan indeholde én eller flere af følgende elementer:

- Konstanter
- Operatorer
- Referencer
- Stier
- Funktioner

#### <a name="constants"></a>Konstanter

Når du designer udtryk, kan du bruge tekst og numeriske konstanter (værdier, der ikke beregnes). Den numeriske konstant **20** og strengkonstanten **"100"** anvendes f.eks. i udtrykket **VALUE ("100") + 20**, der returnerer den numeriske værdi **120**. Elektronisk rapportering (ER) understøtter escape-sekvenser. Derfor kan du angive en udtryksstreng, der skal håndteres anderledes. F.eks. returnerer udtrykket **"Leo Tolstoy ""Krig og fred"" Bind 1"** tekststrengen **Leo Tolstoy "Krig og fred" Bind 1**.

#### <a name="operators"></a>Operatorer

Følgende tabel viser de aritmetiske operatorer, du kan bruge til at udføre grundlæggende matematiske funktioner som addition, subtraktion, multiplikation og division.

| Operator | Betydning               | Eksempel |
|----------|-----------------------|---------|
| +        | Tilføjelse              | 1+2     |
| -        | Subtraktion, negation | 5-2, -1 |
| \*       | Multiplikation        | 7\*8    |
| /        | Afdeling              | 9/3     |

Følgende tabel viser de sammenligningsoperatorer, der understøttes. Du kan bruge disse operatorer til at sammenligne to værdier.

| Operator | Betydning                  | Eksempel    |
|----------|--------------------------|------------|
| =        | Lig                    | X=Y        |
| &gt;     | Større end             | X&gt;Y     |
| &lt;     | Mindre end                | X&lt;Y     |
| &gt;=    | Større end eller lig med | X&gt;=Y    |
| &lt;=    | Mindre end eller lig med    | X&lt;=Y    |
| &lt;&gt; | Ikke lig med             | X&lt;&gt;Y |

Du kan desuden bruge tegnet (&) som en operator til tekstsammenføjning. På denne måde kan du sammenføje eller sammenkæde en eller flere tekststrenge i et enkelt stykke tekst.

| Operatør | Betydning     | Eksempel                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Sammenkæde | "Intet at udskrive" & ":&nbsp;" & "Der blev ikke fundet nogen poster" |

##### <a name="operator-precedence"></a>Den prioriterede operatorrækkefølge

Den rækkefølge, som delene af et sammensat udtryk evalueres i, er vigtig. For eksempel er resultatet af udtrykket **1 + 4 / 2** forskelligt, afhængigt af om addition eller division udføres først. Du kan bruge parenteser til eksplicit at angive, hvordan et udtryk evalueres. Hvis du for eksempel vil angive, at addition skal udføres først, kan du ændre det foregående udtryk til **(1 + 4) / 2**. Hvis du ikke udtrykkelig angiver rækkefølgen af operationer i et udtryk, er rækkefølgen baseret på standardrangfølgen, der er tildelt de understøttede operatorer. Følgende tabel viser den prioritet, der er tildelt hver enkelt operator. Operatorer, der har højere prioritet (for eksempel 7), evalueres før operatorer, der har lavere prioritet (f.eks. 1).

| Prioritering | Operatorer      | Syntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                                   |
| 6          | Medlemsadgang  | … . …                                                                   |
| 5          | Funktionskald  | … ( … )                                                                 |
| 4          | Multiplikation | … \* …<br>… / …                                                         |
| 3          | Tilføjelse       | … + …<br>… - …                                                          |
| 2          | Sammenligning     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Separation     | … , …                                                                   |

Hvis et udtryk indeholder flere på hinanden følgende operatorer, der har samme prioritet, evalueres disse operationer fra venstre mod højre. For eksempel vil udtrykket **1 + 6 / 2 \* 3 &gt; 5** returnere **true**. Vi anbefaler, at du bruger parenteser til at angive den ønskede rækkefølge af operationer i udtryk, så det bliver nemmere at læse og vedligeholde udtrykkene eksplicit.

#### <a name="references"></a>Referencer

Alle datakilder for den aktuelle ER-komponent, der er tilgængelige under designet af et udtryk, kan bruges som navngivne referencer. (Den aktuelle ER-komponent kan være enten en model eller et format). For eksempel indeholder den aktuelle ER-datamodel datakilden **ReportingDate** datakilde, og denne datakilde returnerer en værdi af datatypen **DATETIME**. Denne værdi i det genererende dokument skal formateres korrekt ved at referere til datakilden i udtrykket på følgende måde: **DATETIMEFORMAT (ReportingDate, "dd-MM-åååå")**.

Alle tegn i navnet på en datakilde, der refereres til, som ikke repræsenterer et bogstav i alfabetet, skal indledes med et enkelt anførselstegn ('). Hvis navnet på en refererende datakilde indeholder mindst ét symbol, der ikke repræsenterer et bogstav i alfabetet, skal navnet stå i anførselstegn. (F.eks. kan disse ikke-alfabetiske symboler være tegnsætningstegn eller andre skriftlige symboler). Her er nogle eksempler:

- Datakilden **Today’s date & time** skal refereres til i et ER-udtryk som følger: **'Today''s date & time’**.
- Metoden **name()** i datakilden **Customers** skal refereres til i ER-udtryk som følger: **Customers.'name()'**.

Hvis metoderne i datakilder har parametre, bruges følgende syntaks til at kalde disse metoder:

- Hvis metoden **isLanguageRTL** i datakilden **System** har en **EN-US**-parameter af datatypen **String** skal denne metode refereres til i et ER-udtryk som **System.'isLanguageRTL'("EN-US")**.
- Anførselstegn er ikke påkrævede, når et metodenavn kun indeholder alfanumeriske symboler. Men de er obligatoriske til en metode for en tabel, hvis navnet indeholder kantede parenteser.

Når datakilden **System** føjes til en ER-tilknytning, der henviser til programklassen **Global**, returnerer udtrykket den booleske værdi **FALSE**. Det ændrede udtryk **System.' isLanguageRTL'("AR")** returnerer den booleske værdi **SAND**.

Du kan begrænse den måde, værdier sendes til parametrene på for denne type metode:

- Kun konstanter kan overføres til metoder af denne type. Værdierne af konstanter, der er defineret i designfasen.
- Kun primitive datatyper (basis) understøttes til parametrene for denne type. (De primitive datatyper er heltal, reelt tal, boolesk, streng og så videre).

#### <a name="paths"></a>Stier

Når et udtryk refererer til en struktureret datakilde, kan du bruge definitionen af stien til at vælge et bestemt primitivt element i datakilden. Tegnet en prik (.) bruges til at adskille de enkelte elementer i en struktureret datakilde. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, og denne datakilde returnerer en liste med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, og begge disse felter returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan derfor være udformet således: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funktioner

Det næste afsnit beskriver de funktioner, der kan bruges i ER-udtryk. Alle datakilder i udtrykskonteksten (aktuel ER-datamodel eller ER-format) samt konstanter kan bruges som parametre til opkaldsfunktioner i henhold til listen over argumenter for opkaldsfunktioner. Konstanter kan også bruges som parametre til kald af funktioner. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, og denne datakilde returnerer en liste med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, og begge disse felter returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan derfor være udformet således ved at bruge den indbyggede ER-afrundingsfunktion: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Understøttede funktioner

I følgende tabel beskrives de datamanipulationsfunktioner, du kan bruge til at designe ER-datamodeller og ER-rapporter. Listen over funktioner er ikke fast. Udviklere kan udvide den. Du kan se listen over funktioner, du kan bruge, ved at åbne ruden med funktioner i ER-formeldesigneren.

### <a name="date-and-time-functions"></a>Dato- og klokkeslætsfunktioner

| Funktion | Beskrivelse | Eksempel |
|----------|-------------|---------|
| ADDDAYS (datetime, dage) | Føj det angivne antal dage til den angivne date/time-værdi. | **ADDDAYS (NOW() 7)** returnerer datoen og klokkeslættet syv dage ud i fremtiden. |
| DATETODATETIME (dato) | Konverter den angivne datoværdi til en dato-/klokkeslætværdi. | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den aktuelle Finance and Operations-sessionsdato, 24. december 2015, som **12/24/2015 12:00:00 AM**. I dette eksempel er **CompInfo** en datakilde til ER af typen **Finance and Operations/tabel** og refererer til tabellen CompanyInfo. |
| NOW () | Returner aktuel dato og aktuelt klokkeslæt på programserver som en dato-/klokkeslætsværdi. | |
| TODAY () | Returner aktuel dato på programserver som en datoværdi. | |
| NULLDATE () | Returner en **null**-datoværdi. | |
| NULLDATETIME () | Returner en **null**-værdi for dato/klokkeslæt. | |
| DATETIMEFORMAT (datetime, format) | Konverter den angivne dato-/klokkeslætværdi til en streng i det angivne format. (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** returnerer den aktuelle dato på programserver, 24. december 2015, som **"24-12-2015"**, baseret på det angivne brugerdefinerede format. |
| DATETIMEFORMAT (datetime, format, kultur) | Konverter den angivne dato-/klokkeslætværdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** returnerer den aktuelle dato på programserver, 24. december 2015, som **"24.12.2015"**, i henhold til den valgte tyske kultur. |
| SESSIONTODAY () | Returner den aktuelle dato for programsession som en datoværdi. | |
| SESSIONNOW () | Returner aktuel dato og aktuelt klokkeslæt på programsession som en dato-/klokkeslætsværdi. | |
| DATEFORMAT (dato, format) | Returner en strenggengivelse af den angivne dato i det angivne format. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** returnerer den aktuelle programsessionsdato, 24. december 2015, som **"24-12-2015"**, baseret på det angivne brugerdefinerede format. |
| DATEFORMAT (dato, format, kultur) | Konverter den angivne datoværdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** returnerer den aktuelle programsessionsdato, 24. december 2015, som **"24.12.2015"**, i henhold til den valgte tyske kultur. |
| DAYOFYEAR (dato) | Returnerer en heltalsrepræsentation af antallet af dage mellem 1. januar og den angivne dato. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** returnerer **61**. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** returnerer **1**. |
| DAYS (dato 1, dato 2) | Returnere antallet af dage mellem den første angivne dato og den anden angivne dato. Returnerer en positiv værdi, når den første dato er senere end den anden dato, returnerer **0** (nul), når den første dato er lig med den anden dato eller returnerer en negativ værdi, når den første date er før den anden dato. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** returnerer **-1**. |

### <a name="data-conversion-functions"></a>Datakonverteringsfunktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| DATETODATETIME (dato) | Konverter den angivne datoværdi til en dato-/klokkeslætværdi. | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den aktuelle Finance and Operations-sessionsdato, 24. december 2015, som **12/24/2015 12:00:00 AM**. I dette eksempel er **CompInfo** en datakilde til ER af typen **Finance and Operations/tabel** og refererer til tabellen CompanyInfo. |
| DATEVALUE (streng, format) | Returner en datogengivelse af den angivne streng i det angivne format. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** returnerer datoen 21. december 2016 i overensstemmelse med det angivne brugerdefinerede format og standardprogrammets **EN-US** kultur. |
| DATEVALUE (streng, format, kultur) | Returner en datogengivelse af den angivne streng i det angivne format og den angivne kultur. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** returnerer datoen, 21. januar 2016, baseret på det angivne brugerdefinerede format og den angivne kultur. Men **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato. |
| DATETIMEVALUE (streng, format) | Returner en dato-/klokkseslætgengivelse af den angivne streng i det angivne format. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-åååå hh:mm:ss")** returnerer 2:55:00 AM den 21. december 2016, baseret på det angivne brugerdefinerede format og standardprogrammets **EN-US**-kultur. |
| DATETIMEVALUE (streng, format, kultur) | Returner en dato-/klokkeslætgengivelse af den angivne streng i det angivne format og den angivne kultur. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** returnerer 2:55:00 AM den 21. december 2016, baseret på det angivne brugerdefinerede format og den angivne kultur. Men **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** udløser en undtagelse for at informere brugeren om, at den angivne streng ikke genkendes som en gyldig dato/klokkeslæt. |

### <a name="list-functions"></a>Listefunktioner

<table>
<thead>
<tr>
<th>Funktion</th>
<th>Betegnelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (input, længde)</td>
<td>Opdeler den angivne inputstreng i understrenge, som hver især har den angivne længde. Returner resultatet som en ny liste.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> returnerer en ny liste, der består af to poster, der har et <strong>STRING</strong>-felt. Feltet i den første post indeholder teksten <strong>&quot;abc&quot;</strong>, og feltet i den anden post indeholder teksten <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr>
<td>SPLIT (input, afgrænser)</td>
<td>Opdeler den angivne inputstreng i understrenge baseret på den angivne afgrænser.</td>
<td><strong>SPLIT (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong> returnerer en ny liste, der består af tre poster, der har et <strong>STRING</strong>-felt. Feltet i den første post indeholder teksten <strong>&quot;X&quot;</strong>, feltet i den anden post indeholder teksten, &quot;&nbsp;&quot;, og feltet i den tredje post indeholder teksten <strong>&quot;y&quot;</strong>. Hvis afgrænsningstegnet er tomt, returneres en ny liste, der består af én post, der har et <strong>STRING</strong>-felt, der indeholder inputteksten. Hvis inputtet er tomt, returneres en ny tom liste.
Hvis hverken inputtet eller afgrænsningstegnet er angivet (null), opstår der en programundtagelse.</td>
</tr>
<tr>
<td>SPLITLIST (liste, antal)</td>
<td>Opdel den angivne liste i batches, som hver især indeholder det angivne antal poster. Returner resultatet som en ny liste over batches, der indeholder følgende elementer:
<ul>
<li>Batches som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle batchnummer (<strong>Batchnummer-</strong>komponent)</li>
</ul>
</td>
<td>I følgende illustration er der oprettet en <strong>Linjer</strong>-datakilde som en postliste over tre poster. Denne liste er opdelt i bundter, som hver indeholder op til to poster.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>I følgende illustration vises det designede formatlayout. I dette formatlayout er bindinger til datakilden <strong>Linjer</strong> oprettet for at generere outputtet i XML-format. Dette output viser individuelle noder for hvert parti og posterne i det.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>I følgende illustration vises resultatet, når det designede format køres.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (post 1 [, post 2, …])</td>
<td>Returner en ny liste, der oprettes ud fra de angivne argumenter.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> returnerer en tom post, hvor listen over felter indeholder alle felterne i postlisterne <strong>MainData</strong> og <strong>OtherData</strong>.</td>
</tr>
<tr>
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Returner en ny forenet liste, der oprettes ud fra lister med de angivne argumenter.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> returnerer en liste over seks poster, hvor ét felt af <strong>STRING</strong>-datatypen indeholder enkelte bogstaver.</td>
</tr>
<tr>
<td>ISEMPTY (liste)</td>
<td>Returnerer <strong>SAND</strong>, hvis den angivne liste ikke indeholder nogen elementer. Ellers returneres <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (liste)</td>
<td>Returner en tom liste ved hjælp af den angivne liste som kilde til listestrukturen.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af <strong>SPLIT</strong>-funktionen.</td>
</tr>
<tr>
<td>FIRST (liste)</td>
<td>Returner den første post i den angivne liste, hvis posten ikke er tom. Ellers udløses en undtagelse.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (liste)</td>
<td>Returner den første post i den angivne liste, hvis posten ikke er tom. Ellers returneres en <strong>null</strong>-post.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (liste)</td>
<td>Returner en liste, der kun indeholder det første element på en given liste.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (sti)</td>
<td>Denne funktion kører som en markering i hukommelsen. Den returner en ny, udlignet liste, der repræsenterer alle elementer, der svarer til den angivne sti. Stien skal defineres som en gyldig datakildesti for et datakildeelement af datatypen postliste. Dataelementer som strengen til stien og datoen bør udløse en fejl i designfasen i ER-udtryksgeneratoren.</td>
<td>Hvis du angiver <strong>SPLIT (&quot;abcdef&quot;, 2)</strong> som datakilde (DS), vil <strong>COUNT (ALLITEMS (DS.Value))</strong> returnere <strong>3</strong>.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (sti)</td>
<td>Denne funktion kører som en sammenkædet SQL-forespørgsel. Den returner en ny, udlignet liste, der repræsenterer alle elementer, der svarer til den angivne sti. Den angivne sti skal defineres som en gyldig datakildesti for et datakildeelement af datatypen postliste, og den skal indeholde mindst én relation. Dataelementer som strengen til stien og datoen bør udløse en fejl i designfasen i ER-udtryksgeneratoren.</td>
<td>Definer følgende datakilder i din modeltilknytning:
<ul>
<li><strong>CustInv</strong> (typen <strong>Tabelposter</strong>), som refererer til tabellen CustInvoiceTable</li> 
<li><strong>FilteredInv</strong> (typen <strong>Beregnet felt</strong>), som indeholder udtrykket <strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong></li>
<li><strong>JourLines</strong> (typen <strong>Beregnet felt</strong>), som indeholder udtrykket <strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong></li>
</ul>
<p>Når du kører din modeltilknytning for at kalde datakilden <strong>JourLines</strong>, udføres følgende SQL-sætning:</p>
VÆLG ... FRA CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3, HVOR...
</td>
</tr>
<tr>
<td>ORDERBY (liste [udtryk 1, udtryk, 2, ...])</td>
<td>Returnere den angivne liste, når den er sorteret i henhold til de angivne argumenter. Disse argumenter kan defineres som udtryk.</td>
<td>Hvis <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>ORDERBY (Vendors, Vendors.'name()')</strong> returnere en liste over kreditorer, der er sorteret efter navn i stigende rækkefølge.</td>
</tr>
<tr>
<td>REVERSE (liste)</td>
<td>Returner den angivne liste i omvendt rækkefølge.</td>
<td>Hvis <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()'))</strong> returnere en liste over leverandører, der er sorteret efter navn i faldende rækkefølge.</td>
</tr>
<tr>
<td>WHERE (liste, betingelse)</td>
<td>Returnere den angivne liste, når den er blevet filtreret i henhold til den angivne tilstand. Den angivne betingelse, anvendes på listen i hukommelsen. På denne måde adskiller funktionen <strong>WHERE</strong>, sig fra funktionen <strong>FILTER</strong> funktion.</td>
<td>Hvis <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> returnere en liste over blot de kreditorer, der tilhører kreditorgruppe 40.</td>
</tr>
<tr>
<td>ENUMERATE (liste)</td>
<td>Returner en ny liste, der består af optalte poster af den angivne liste og viser følgende elementer:
<ul>
<li>Angivne listeposter som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle postindeks (<strong>Tal-</strong>komponent)</li>
</ul>
</td>
<td>I følgende illustration er <strong>Enumerated</strong>-datakilden oprettet som en fasttekstliste over kreditorposter fra <strong>Vendors</strong>-datakilden, der henviser til VendTable-tabellen.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Følgende illustration viser formatet. I dette format oprettes databindinger for at generere outputtet i XML-format. Dette output viser individuelle leverandører som optalte noder.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>I følgende illustration vises resultatet, når det designede format køres.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (liste)</td>
<td>Returner antal poster på den angivne liste, hvis listen ikke er tom. Ellers returneres <strong>0</strong> (nul).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> returnerer <strong>2</strong>, fordi <strong>SPLIT</strong>-funktionen opretter en liste, der består af to poster.</td>
</tr>
<tr>
<td>LISTOFFIELDS (sti)</td>
<td>Returnerer en postliste, der er oprettet ud fra et argument i en af følgende typer:
<ul>
<li>Modelfasttekst</li>
<li>Formatfasttekst</li>
<li>Container</li>
</ul>
<p>Den liste, der oprettes, består af poster, der har følgende felter:</p>
<ul>
<li>Navn</li>
<li>Label</li>
<li>Betegnelse</li>
</ul>
På kørselstidspunktet returnerer felterne <strong>Label</strong> og <strong>Beskrivelse</strong> værdier, der er baseret på formatets sprogindstillinger.
</td>
<td>I følgende illustration introduceres en fasttekst i en datamodel.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Følgende illustration viser disse detaljer:</p>
<ul>
<li>Modelfastteksten indsættes i en rapport som en datakilde.</li>
<li>Et ER-udtryk bruger fastteksten med modellen som en parameter til funktionen <strong>LISTOFFIELDS</strong>.</li>
<li>En datakilde af postlistetypen indsættes i en rapport ved hjælp af det oprettede ER-udtryk.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Følgende eksempel viser de ER-formatelementer, der er bundet til datakilden af postlistetypen, der blev oprettet ved hjælp af funktionen <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>I følgende illustration vises resultatet, når det designede format køres.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Baseret på sprogindstillingerne til de overordnede FILE- og FOLDER-formatelementer, udfyldes oversat tekst til etiketter og beskrivelser i outputtet til ER-formatet.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (sti, sprog)</td>
<td>Returner en liste over poster, der er oprettet ud fra et argument, f.eks. en optælling af modellen, en optælling af format eller en container. Den liste, der oprettes, består af poster, der har følgende felter:
<ul>
<li>Navn</li>
<li>Label</li>
<li>Betegnelse</li>
<li>Er oversat</li>
</ul>
På kørselstidspunktet returnerer felterne <strong>Label</strong> og <strong>Beskrivelse</strong> værdier, der er baseret på formatets sprogindstillinger og det angivne sprog. Feltet <strong>Er oversat</strong> angiver, at feltet <strong>Etiket</strong> er oversat til det angivne sprog.
</td>
<td>Du bruger f.eks. datakildetypen <strong>Beregnet felt</strong> til at konfigurere datakilderne <strong>enumType_de</strong> og <strong>enumType_deCH</strong> for datamodeloptællingen <strong>enumType</strong>.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>I dette tilfælde skal kan du bruge følgende udtryk til at få etiketten til tællerværdien på tysk (Schweiz), hvis denne oversættelse er tilgængelig. Hvis oversættelsen til tysk (Schweiz) ikke er tilgængelig, er etiketten på tysk.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (liste, feltnavn, afgrænser)</td>
<td>Returnerer en streng, der består af sammenføjede værdier for det angivne felt fra den angivne liste. Værdierne er adskilt af et angivet separatortegn.</td>
<td>Hvis du angiver <strong>SPLIT(&quot;abc&quot; , 1)</strong> som en datakilde (DS), <strong>returnerer STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> <strong>&quot;a-b-c&quot;</strong>.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (liste, grænseværdi. grænsekilde)</td>
<td>Opdel den angivne liste i en ny liste over underordnede lister, og returner resultatet i indholdet af listen over poster. Parameteren for <strong>grænseværdi</strong> definerer værdien af grænsen for opdeling af den oprindelige liste. Parameteren for <strong>grænsekilde</strong> definerer det trin, som den samlede sum forøges med. Grænsen anvendes ikke på et enkelt element på den oprindelige liste, hvis grænsekilden overskrider den angivne grænse.</td>
<td>Følgende illustration viser et format. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Følgende illustration viser de datakilder, der bruges til formatet.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>I følgende illustration vises resultatet, når formatet køres. I så fald er outputtet en simpel liste over råvarer.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>I de følgende illustrationer er det samme format blevet justeret, så den repræsenterer listen over varegoder i batches, når et enkelt batch skal indeholde goder, og den samlede vægt ikke må overstige en grænse 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>I følgende illustration vises resultatet, når det justerede format køres.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Grænsen anvendes ikke på den sidste vare på den oprindelige liste, da værdien (11) af grænsekilden (vægt) overskrider den angivne grænse (9). Brug om nødvendigt enten funktionen <strong>WHERE</strong> eller udtrykket <strong>Aktiveret</strong> for det tilsvarende formatelement for at ignorere (springe over) underordnede lister under oprettelse af rapporten.</blockquote>
</td>
</tr>
<tr>
<td>FILTER (liste, betingelse)</td>
<td>Returner den angivne liste, når forespørgslen er blevet ændret til at filtrere i henhold til den angivne tilstand. Denne funktion adskiller sig fra funktionen <strong>WHERE</strong>, fordi den angivne betingelse anvendes på enhver ER-datakilde af typen <strong>Tabelposter</strong> på databaseniveau. Listen og betingelse kan defineres ved hjælp af tabeller og relationer.</td>
<td>Hvis <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>FILTER(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> returnere en liste over blot de kreditorer, der tilhører kreditorgruppe 40. Hvis <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til VendTable-tabellen, og hvis <strong>parmVendorBankGroup</strong> er konfigureret som en ER-datakilde, der returnerer en værdi af datatypen <strong>Streng</strong>, returnerer <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> en liste over kun de kreditorkonti, der tilhører en bestemt bankgruppe.</td>
</tr>
<tr>
<td>INDEKS (liste, indeks)</td>
<td>Denne funktion returnerer en post, der vælges af et bestemt numerisk indeks på listen. Der udløses en undtagelse, hvis indekset er uden for området for posterne på listen.</td>
<td>Hvis du angiver datakildens <strong>DS</strong> for typen <strong>Beregnet felt</strong>, og den indeholder udtrykket <strong>SPLIT ("A|B|C", “|”), 2</strong>, returnerer udtrykket <strong>DS.Value</strong> tekstværdien “B”. Udtrykket <strong>INDEX (SPLIT ("A|B|C", “|”), 2).Value</strong> returnerer også tekstværdien “B”.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logiske funktioner

| Funktion | Beskrivelse | Eksempel |
|----------|-------------|---------|
| CASE (udtryk, valgmulighed 1, resultat 1 \[, valgmulighed 2, resultat 2\] ... \[, standardresultat\]) | Evaluer den angivne udtryksværdi mod de angivne alternative valgmuligheder. Returner resultatet af den valgmulighed, der svarer til værdien af udtrykket. Ellers returneres det valgfri standardresultat, hvis der er angivet et standardresultat. (Standardresultatet er den sidste parameter, der ikke indledes med en valgmulighed). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "VINTER", "11", "VINTER", "12", "VINTER", "")** returnerer strengen **"VINTER"**, når den aktuelle programsessionsdato er mellem oktober og december. Ellers returneres en tom streng. |
| IF (betingelse, værdi 1, værdi 2) | Returner den først angivne værdi, når den angivne betingelse er opfyldt. Ellers returneres den anden angivne værdi. Hvis værdi 1 og 2 er poster eller postlister, har resultatet kun de felter, der findes på begge lister. | **IF (1 = 2, "betingelse er opfyldt", "betingelse er ikke opfyldt")** returnerer strengen **"betingelse er ikke opfyldt"**. |
| NOT (betingelse) | Returner den omvendte logiske værdi af den angivne betingelse. | **NOT (TRUE)** returnerer **FALSE**. |
| AND (betingelse 1\[, betingelse 2, ...\]) | Returnerer **TRUE**, hvis *alle* angivne betingelser er sande. Ellers returneres **FALSE**. | **AND (1=1, "a"="a")** returnerer **TRUE**. **AND (1=2, "a"="a")** returnerer **FALSE**. |
| OR (betingelse 1\[, betingelse 2, ...\]) | Returnerer **FALSE**, hvis *alle* angivne betingelser er falske. Returnerer **TRUE**, hvis *en af* de angivne betingelser er sande. | **OR (1=2, "a"="a")** returnerer **TRUE**. |
| VALUEIN (input, liste, listeelementudtryk) | Bestem, om det angivne input svarer til en værdi for et element på den angivne liste. Returnerer **TRUE**, hvis det angivne input svarer til resultatet af at køre det angivne udtryk for mindst én post. Ellers returneres **FALSE**. Parameteren **input** repræsenterer stien til et datakildeelement. Værdien af dette element bliver sammenlignet. Parameteren **liste** repræsenterer stien til et datakildeelement af postlistetypen som en liste over poster, der indeholder et udtryk. Værdien af dette element bliver sammenlignet med det angivne input. Argumentet **listeelementudtryk** repræsenterer et udtryk, der peger på eller indeholder et enkelt felt fra den angivne liste, som skal bruges til sammenligningen. | Du kan se eksempler i afsnittet [Eksempler: VALUEIN (input, liste, listeelementudtryk)](#examples-valuein-input-list-list-item-expression) nedenfor. |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Eksempler: VALUEIN (input, liste, listeelementudtryk)
Generelt oversættes funktionen **VALUEIN** oversættes til et sæt **OR**-betingelser:

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>Eksempel 1
Du kan definere følgende datakilde i din modeltilknytning: **Liste** (typen **Beregnet felt**). Denne datakilde indeholder udtrykket **SPLIT ("a,b,c",",")**.

Når en datakilde, der er konfigureret som udtrykket **VALUEIN ("B", List, List.Value)**, kaldes, returneres **TRUE**. I dette tilfælde oversættes funktionen **VALUEIN** til følgende sæt betingelser:

**(("B" = "a") eller ("B" = "b") eller ("B" = "c"))**, hvor **("B" = "b")** er lig med **TRUE**

Når en datakilde, der er konfigureret som udtrykket **VALUEIN ("B", List, LEFT(List.Value, 0))**, kaldes, returneres **FALSE**. I dette tilfælde oversættes funktionen **VALUEIN** til følgende betingelse:

**("B" = "")**, som ikke er lig med **TRUE**

Bemærk, at den øvre grænse for antallet af tegn i teksten i en sådan betingelse er 32.768 tegn. Du skal derfor ikke oprette datakilder, der kan overskride denne grænse på kørselstidspunktet. Hvis grænsen overskrides, stopper programmet med at køre, og der opstår en undtagelse. For eksempel kan denne situation opstå, hvis datakilden er konfigureret som **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)**, og **List1** og **List2** listerne indeholder en stor mængde poster.

I nogle tilfælde kan funktionen **VALUEIN** oversættes til en databasesætning ved hjælp af operatoren **EXISTS JOIN**. Dette problem opstår, når funktionen **FILTER** anvendes, og følgende betingelser er opfyldt:

- Indstillingen **Spørg efter forespørgsel** er deaktiveret for datakilden til den **VALUEIN**-funktion, der refererer til listen over poster. (Der bliver ikke anvendt yderligere betingelser på denne datakilde på kørselstidspunktet).
- Ingen indlejrede udtryk konfigureres for datakilden til den **VALUEIN**-funktion, der refererer til listen over poster.
- Et listeelement i **VALUEIN**-funktionen refererer til et felt (ikke et udtryk eller en metode) i den angivne datakilde.

Overvej at bruge denne indstilling i stedet for funktionen **WHERE** som beskrevet tidligere i dette eksempel.

##### <a name="example-2"></a>Eksempel 2

Du definerer følgende datakilder i din modeltilknytning:

- **In** (typen **Tabelposter**), som refererer til tabellen Intrastat
- **Port** (typen **Tabelposter**), som refererer til tabellen IntrastatPort

Når en datakilde, der konfigureret som udtrykket **FILTER (In, VALUEIN(In.Port, Port, Port.PortId)**, kaldes, genereres følgende SQL-sætning for at returnere filtrerede poster fra tabellen Intrastat:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

For **dataAreaId** felter genereres den endelige SQL-sætning ved hjælp af **IN**-operatoren.

##### <a name="example-3"></a>Eksempel 3

Du definerer følgende datakilder i din modeltilknytning:

- **Le** (typen **Beregnet felt**), som indeholder udtrykket **SPLIT ("DEMF,GBSI,USMF", ",")**
- **In** (typen **Tabelposter**), som refererer til Intrastat-tabellen, og som indstillingen **Intern** er aktiveret for

Når en datakilde, der er konfigureret som udtrykket **FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)**, kaldes, indeholder den endelige SQL-sætning følgende betingelse:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Matematiske funktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| ABS (tal) | Returner den absolutte værdi af det angivne tal. (Returnerer med andre ord tallet uden dets fortegn). | **ABS (-1)** returnerer **1**. |
| POWER (tal, potens) | Returnerer resultatet af at opløfte det angivne positive tal i den angivne potens. | **POWER (10, 2)** returnerer **100**. |
| NUMBERVALUE (streng, decimalseparator, ciffergrupperingsseparator) | Konverter den angivne streng til et tal. Den angivne decimalseparator bruges mellem heltallet og brøkdele af et decimaltal. Den angivne ciffergrupperingsseparator bruges som tusindseparator. | **NUMBERVALUE("1 234,56", ", " "")** returnerer værdien **1234.56**. |
| VALUE (streng) | Konverter den angivne streng til et tal. Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som et negativt fortegn. Udløs en undtagelse, hvis den angivne streng indeholder andre ikke-numeriske tegn. | **VALUE ("1 234,56")** medfører en undtagelse. |
| ROUND (tal, decimaler) | Returner det angivne tal, når det er afrundet til det angivne antal decimaler:<ul><li>Hvis værdien for parameteren **decimaler** er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.</li><li>Hvis værdien for parameteren **decimaler** er **0** (nul), afrundes det angivne tal til det nærmeste heltal.</li><li>Hvis værdien af parameteren **decimaler** er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.</li></ul> | **ROUND (1200.767. 2)** afrunder til to decimaler og returnerer **1200.77**. **ROUND (1200.767, -3)** afrunder til det nærmeste multiplum af 1.000 og returnerer **1000**. |
| ROUNDDOWN (tal, decimaler) | Returner det angivne tal, når det er nedrundet til det angivne antal decimaler.<blockquote>[!NOTE] Denne funktion fungerer ligesom **ROUND**, men den runder altid det angivne tal ned (mod nul).</blockquote> | **ROUNDDOWN (1200.767. 2)** afrunder ned til to decimaler og returnerer **1200.76**. **ROUNDDOWN (1700.767, -3)** afrunder ned til det nærmeste multiplum af 1.000 og returnerer **1000**. |
| ROUNDUP (tal, decimaler) | Returner det angivne tal, når det er rundet op til det angivne antal decimaler.<blockquote>[!NOTE] Denne funktion fungerer ligesom **ROUND**, men den runder altid det angivne tal op (væk fra nul).</blockquote> | **ROUNDUP (1200.763. 2)** afrunder op til to decimaler og returnerer **1200.77**. **ROUNDUP (1200.767, -3)** afrunder op til det nærmeste multiplum af 1.000 og returnerer **2000**. |

### <a name="data-conversion-functions"></a>Datakonverteringsfunktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| VALUE (streng) | Konverter den angivne streng til et tal. Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som et negativt fortegn. Udløs en undtagelse, hvis den angivne streng indeholder andre ikke-numeriske tegn. | **VALUE ("1 234,56")** medfører en undtagelse. |
| NUMBERVALUE (streng, decimalseparator, ciffergrupperingsseparator) | Konverter den angivne streng til et tal. Den angivne decimalseparator bruges mellem heltallet og brøkdele af et decimaltal. Den angivne ciffergrupperingsseparator bruges som tusindseparator. | **NUMBERVALUE ("1 234,56", ",", "")** returnerer **1234.56**. |
| INTVALUE (streng) | Returner en heltalsrepræsentation af den angivne streng. Eventuelle decimalpladser afkortes. | **INTVALUE ("100.77")** returnerer **100**. |
| INTVALUE (tal) | Returner en heltalsrepræsentation af det angivne tal. Eventuelle decimalpladser afkortes. | **INTVALUE (-100.77)** returnerer **-100**. |
| INT64VALUE (streng) | Returner en int64-repræsentation af den angivne streng. Eventuelle decimalpladser afkortes. | **INT64VALUE ("22565422744")** returnerer **22565422744**. |
| INT64VALUE (tal) | Returner en int64-repræsentation af det angivne tal. Eventuelle decimalpladser afkortes. | **INT64VALUE (22565422744.00)** returnerer **22565422744**. |

### <a name="record-functions"></a>Postfunktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| NULLCONTAINER (liste) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post.<blockquote>[!NOTE] Denne funktion er forældet. Brug **EMPTYRECORD** i stedet.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen. |
| EMPTYRECORD (post) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post.<blockquote>[!NOTE] En **null**-post er en post, hvor alle felter har en tom værdi. En tom værdi er **0** (nul) for tal, en tom streng for strenge, osv.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen. |

### <a name="text-functions"></a>Tekstfunktioner

<table>
<thead>
<tr>
<th>Funktion</th>
<th>Betegnelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (streng)</td>
<td>Returner den angivne streng, efter at den er konverteret til store bogstaver.</td>
<td><strong>UPPER(&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;EKSEMPEL&quot;</strong>.</td>
</tr>
<tr>
<td>LOWER (streng)</td>
<td>Returner den angivne streng, efter at den er konverteret til små bogstaver.</td>
<td><strong>LOWER (&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr>
<td>LEFT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra starten af den angivne streng.</td>
<td><strong>LEFT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;Eks&quot;</strong>.</td>
</tr>
<tr>
<td>RIGHT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra slutningen af den angivne streng.</td>
<td><strong>RIGHT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;pel&quot;</strong>.</td>
</tr>
<tr>
<td>MID (streng, startposition, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra startpositionen i den angivne streng.</td>
<td><strong>MID (&quot;Eksempel&quot;, 2, 3)</strong> returnerer <strong>&quot;kse&quot;</strong>.</td>
</tr>
<tr>
<td>LEN (streng)</td>
<td>Returner antallet af tegn i den angivne streng.</td>
<td><strong>LEN (&quot;Eksempel&quot;)</strong> returnerer <strong>6</strong>.</td>
</tr>
<tr>
<td>CHAR (tal)</td>
<td>Returner den streng af tegn, der refereres til af det angivne Unicode-tal.</td>
<td><strong>CHAR (255)</strong> returnerer <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE] Den streng, som denne funktion returnerer, afhænger af den kodning, der er valgt i det overordnede FILE-formatelement. Du kan finde listen over understøttede kodninger under <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodningsklasse</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (streng 1 [, streng 2, ...])</td>
<td>Returner alle angivne tekststrenge, efter at de er sat ind i én streng.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> returnerer <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE] Udtrykket <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> returnerer også <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (streng, mønster, erstatning)</td>
<td>Returner den angivne streng, når alle forekomster af tegn i det angivne strengmønster er blevet erstattet med tegn på den tilsvarende position i den angivne erstatningsstreng.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (streng, mønster, erstatning, almindeligt udtryksflag)</td>
<td>Når det angivne parameter for det <strong>almindelige udtryksflag</strong> er <strong>true</strong>, returneres den angivne streng, når den er blevet ændret ved at anvende det almindelige udtryk, der er angivet som <strong>mønsterargumentet</strong> for denne funktion. Dette udtryk bruges til at søge efter tegn, der skal erstattes. Tegn i det angivne <strong>erstatningsargument</strong> bruges til at erstatte tegn, der findes. Når den angivne parameter for det <strong>almindelige udtryksflag</strong> er <strong>false</strong>, fungerer denne funktion ligesom <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, true)</strong> anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>TEXT (input)</td>
<td>Returner det angivne input, når det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>Hvis serverens landestandard for Finance and Operations-forekomsten er defineret som <strong>EN-US</strong>, returnerer <strong>TEXT (NOW ())</strong> den aktuelle programsessionsdato, December 17, 2015 som tekststrengen <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> returnerer <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr>
<td>FORMAT (streng 1, streng 2[, streng 3, ...])</td>
<td>Returner den angivne streng, når den er blevet formateret ved at erstatte alle forekomster af <strong>%N</strong> med det <em>te</em> argument. Argumenterne er strenge. Hvis et argument ikke er angivet for en parameter, bliver parameteren returneret som <strong>&quot;%N&quot;</strong> i strengen. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>I følgende eksempel på <strong>PaymentModel</strong>-datakilden returneres listen over kundeposter via <strong>Customer</strong>-komponenten og behandlingens datoværdi via <strong>ProcessingDate</strong>-feltet.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>Datakilden <strong>PaymentModel</strong> i ER-format er designet til at generere en elektronisk fil til de valgte debitorer og er valgt som en datakilde og styrer procesforløbet. En undtagelse opstår for at give brugeren besked, når en bestemt debitor er spærret for den dato, hvor rapporten behandles. Den formel, der er udviklet til denne type behandlingskontrol, kan bruge følgende ressourcer:</p>
<ul>
<li>Etiket SYS70894, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong> &quot;Nothing to print&quot;</li>
<li><strong>For det danske sprog:</strong> &quot;Intet at udskrive&quot;</li>
</ul></li>
<li>Etiket SYS18389, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong> &quot;Debitor %1 er spærret for %2.&quot;</li>
<li><strong>For det tyske sprog: </strong> &quot;Debitor '%1' er spærret for %2.&quot;</li>
</ul></li>
</ul>
<p>Her er den formel, der kan udvikles:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Hvis en rapport behandles for debitoren <strong>Litware Retail</strong> den 17. december 2015 i den amerikanske kultur, <strong>EN-US</strong>, og på det amerikanske sprog, <strong>EN-US</strong>, returnerer denne formel følgende tekst, som kan præsenteres for slutbrugeren som en undtagelsesmeddelelse:</p>
<p>&quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Hvis den samme rapport behandles den 17. december 2015 for kunden <strong>Litware Retail</strong> med dansk kultur <strong>DA</strong> og sproget <strong>DA</strong>, returnerer formlen følgende tekst, der bruger et andet datoformat:</p>
<p>&quot;Intet at udskrive. Debitor 'Litware Retail' er spærret for 17.12.2015.&quot;</p>
<blockquote>[!NOTE] Følgende syntaks er anvendt i ER-formler for etiketter:
<ul>
<li><strong>For etiketter fra Finance and Operations-appressourcer:</strong> <strong>@&quot;X&quot;</strong>, hvor <strong>X</strong> er etiket-id'et i applikationsobjekttræet (AOT)</li>
<li><strong>For etiketter, der er placeret i ER-konfigurationer:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, hvor <strong>X</strong> er etiket-id i ER-konfigurationen</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (tal, format)</td>
<td>Returner en strenggengivelse af det angivne tal i det angivne format. (Oplysninger om understøttede formater finder du under <a href="https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx">standard</a> og <a href="https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx">brugerdefinerede</a>.) Konteksten, som denne funktion køres i, bestemmer den kultur, der bruges til at formatere tal.</td>
<td>For den amerikanske kultur vil <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> returnere <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> returnerer <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr>
<td>NUMBERFORMAT (tal, format, kultur)</td>
<td>Returner en strengrepræsentation af det angivne tal i det angivne format og den angivne kultur. (Oplysninger om understøttede formater finder du under <a href="https://docs.microsoft.com/dotnet/standard/base-types/standard-numeric-format-strings">standard</a> og <a href="https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings">brugerdefineret</a>.)</td>
<td><strong>NUMBERFORMAT (10/3, “F2”, "de")</strong> returnerer <strong>3,33</strong>, mens <strong>NUMBERFORMAT (10/3, “F2”, "en-us")</strong> returnerer <strong>3.33</strong>.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (tal, sprog, valuta, udskriv valutanavn, decimaltegn)</td>
<td>Returner det angivne nummer, når den er blevet skrevet helt ud (konverteret til tekststrenge) i det angivne sprog. Sprogkoden er valgfri. Når den er defineret som en tom streng, bruges sprogkoden for kørselskonteksten. (Sprogkoden for kørselskonteksten er defineret for en genererende mappe eller fil). Valutakoden er også valgfrie. Når den er defineret som en tom streng, bruges firmavalutaen.
<blockquote>[!NOTE] Flaget for parametrene <strong>udskriv valutanavn</strong> og <strong>decimaltegn</strong> analyseres kun for følgende sprogkoder: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> og <strong>RU</strong>. Desuden analyseres <strong>udskriv valutanavn</strong>-parameteren kun for virksomheder, hvor landets eller områdets kontekst understøtter afvigelse af valutanavne.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> returnerer <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> returnerer <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> returnerer <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr>
<td>PADLEFT (streng, længde, margentegn)</td>
<td>Returnerer en streng af den angivne længde, hvor begyndelsen af den angivne streng er udfyldt med de angivne tegn.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> returnerer tekststrengen <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr>
<td>TRIM (streng)</td>
<td>Returner den angivne streng, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Eksempel&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;på tekst&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> returnerer <strong>&quot;Eksempel på tekst&quot;</strong>.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (kildesti til fasttekstdata, labeltekst til fasttekstværdi)</td>
<td>Returnerer en værdi for den angivne kilde til fasttekstdata baseret på den angivne tekst i denne fasttekstlabel.</td>
<td>I følgende illustration introduceres fastteksten <strong>ReportDirection</strong> i en datamodel. Bemærk, at der er defineret etiketter for optællingsværdier.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Følgende illustration viser disse detaljer:</p>
<ul>
<li>Modelfastteksten <strong>ReportDirection</strong> indsættes i en rapport som en datakilde <strong>$Direction</strong>.</li>
<li>Et ER-udtryk <strong>$IsArrivals</strong> er designet til at bruge modelfastteksten som parameter for denne funktion. Værdien af dette udtryk er <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (input)</td>
<td>Konverter det angivne input fra datatypen <strong>Streng</strong> til et dataelement i datatypen <strong>GUID</strong>.<blockquote>[!NOTE] Til en omregning i modsat retning (dvs. konvertere angivet input fra datatypen <strong>GUID</strong> til et dataelement i datatypen <strong>Streng</strong>) kan du bruge funktionen <strong>TEXT()</strong>.</blockquote></td>
<td>Du definerer følgende datakilder i din modeltilknytning:
<ul>
<li><strong>myID</strong> (typen <strong>Beregnet felt</strong>), som indeholder udtrykket <strong>GUIDVALUE (&quot;AF5CCDAC F728-4609-8C8B-A4B30B0C0AA0&quot;)</strong></li>
<li><strong>Users</strong> (typen <strong>Tabelposter</strong>), som refererer til tabellen UserInfo</li>
</ul>
Når disse datakilder er defineret, kan du bruge et udtryk som <strong>FILTER (Users, Users.objectId = myID)</strong> til at filtrere tabellen UserInfo efter feltet <strong>objectId</strong> i datatypen <strong>GUID</strong>.
</td>
</tr>
<tr>
<td>JSONVALUE (id, sti)</td>
<td>Opdel data i JavaScript Object Notation (JSON)-format, som benyttes af den angivne sti til at udtrække en skalarværdi, der er baseret på det angivne id.</td>
<td>Datakilden <strong>$JsonField</strong> indeholder følgende data i JSON-format: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. For denne datakilde returnerer </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong> værdien <strong>7.3.1234.1</strong> fra datatypen <strong>Streng</strong>.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Datakonverteringsfunktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| TEXT (input) | Returner det angivne input, når det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst. For værdier af den **reelle** type er strengkonverteringen begrænset til to decimaler. | Hvis serverens landestandard for Finance and Operations-forekomsten er defineret som **EN-US**, returnerer **TEXT (NOW ())** den aktuelle Finance and Operations-sessionsdato, December 17, 2015 som tekststrengen **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** returnerer **"0.33"**. |
| QRCODE (streng) | Returnerer et QR-kodebillede (Quick Response-kode) i det binære base64-format for den angivne streng. | **QRCODE ("teksteksempel")** returnerer **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Dataindsamlingsfunktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Returnerer navnet på det aktuelle formats element. Returnerer en tom streng, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | Du kan få mere at vide om brugen af denne funktion i opgaveguiden **Bruge ER-data af formatoutput til optælling og sammenlægning** en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner. |
| SUMIFS (nøglestreng for sammenlægning, kriterieinterval 1-streng, kriterieværdi 1-streng \[,kriterieinterval 2-streng, kriterieværdi 2-streng, …\]) | Returnerer summen af værdierne, der blev indsamlet til XML-noder (med navn, der er defineret som en nøgle) under kørslen af formatet, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer **0** (nul) værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | |
| SUMIF (nøglestreng for sammenlægning, kriterieintervalstreng, kriterieværdistreng) | Returnerer summen af værdierne, der blev indsamlet til XML-noder (med navn, der er defineret som en nøgle) under kørslen af formatet, og som opfylder den angivne betingelse (et interval og en værdi). Returnerer **0** (nul) værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | |
| COUNTIFS (kriterieinterval 1-streng, kriterieværdi 1-streng \[, kriterieinterval 2-streng, kriterieværdi 2-streng, ...\]]) | Returnerer antal XML-noder, som blev indsamlet under kørslen af formatet, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer **0** (nul) værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | |
| COUNTIF (kriterieintervalstreng, kriterieværdistreng) | Returnerer antal XML-noder, som blev indsamlet under kørslen af formatet, og som opfylder den angivne betingelse (et interval og en værdi). Returnerer en **0** (nul) værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | |
| COLLECTEDLIST (kriterieinterval 1-streng, kriterieværdi 1-streng \[, kriterieinterval 2-streng, kriterieværdi 2-streng, ...\]) | Returnerer den liste over værdier, som blev indsamlet for XML-noder under kørslen af formatet, og som opfylder de angivne betingelser (et interval og en værdi). Returnerer en tom liste, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. | |

### <a name="other-business-domainspecific-functions"></a>Andre (forretningsdomænespecifikke) funktioner

| Funktion | Betegnelse | Eksempel |
|----------|-------------|---------|
| CONVERTCURRENCY (beløb, kildevaluta, målvaluta, dato, firma) | Konverter det angivne pengebeløb fra den angivne kildevaluta til den angivne målvaluta ved hjælp af indstillingerne for det angivne firma på den angivne dato. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** returnerer, hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for DEMF-firmaet. |
| ROUNDAMOUNT (tal, decimaler, afrundingsregel) | Afrund det angivne beløb i henhold til det angivne antal decimaler og den angivne afrundingsregel.<blockquote>[!NOTE] Afrundingsreglen skal angives som en værdi af **RoundOffType**-fasttekst.</blockquote> | Hvis **model.RoundOff**-parameter er indstillet til **Downward**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere værdien **1000.78**. Hvis **model.RoundOff**-parameter er indstillet til enten **Normal** eller **Oprunding**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere værdien **1000.79**. |
| CURCredRef (cifre) | Returner en kreditors reference, baseret på cifrene i det angivne fakturanummer. | **CURCredRef ("VEND-200002")** returnerer **"2200002"**. |
| MOD\_97 (cifre) | Returner en kreditors reference som et MOD97-udtryk, baseret på cifrene i det angivne fakturanummer. | **MOD\_97 ("VEND-200002")** returnerer **"20000285"**. |
| ISOCredRef (cifre) | Returner en ISO-kreditorreference, baseret på cifrene og bogstaverne i det angivne fakturanummer.<blockquote>[!NOTE] For at eliminere symboler fra alfabeter, der ikke er ISO-kompatible, skal inputparameteren oversættes, før den videresendes til denne funktion.</blockquote> | **ISOCredRef ("VEND-200002")** returnerer **"RF23VEND-200002"**. |
| CN\_GBT\_AdditionalDimensionID (streng, tal) | Hent yderligere det angivne økonomisk dimensions-id. I parameteren **streng** er dimensioner repræsenteret i denne streng som id'er, der er adskilt af kommaer. Parameteren **nummer** definerer nummerseriekoden for den ønskede dimension i strengen. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** returnerer **"CC"**. |
| GetCurrentCompany () | Returnerer en tekstrepræsentation af koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på. | **GETCURRENTCOMPANY ()** returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**. |
| CH\_BANK\_MOD\_10 (cifre) | Returner en kreditors reference som et MOD10-udtryk, baseret på cifrene i det angivne fakturanummer. | **CH\_BANK\_MOD\_10 ("VEND-200002")** returnerer **3**. |
| FA\_SUM (anlægsaktivkode, værdimodelkode, startdato, slutdato) | Returnerer den klargjorte datacontainer med anlægsaktivbeløb for den angivne periode. | **FA\_SUM ("COMP-000001", "Aktuel", Date1, Date2)** returnerer den forberedte datacontainer for anlægsaktivet **"COMP-000001"**, der har værdimodellen **"Aktuel"** i en periode fra **Date1** til **Date2**. |
| FA\_BALANCE (anlægsaktivkode, værdimodelkode, rapporteringsår, rapporteringsdato) | Returnerer den klargjorte datacontainer med saldoen for anlægsaktiv. Rapporteringsåret skal angives som en værdi af fastteksten **AssetYear**. | **FA\_SUM ("COMP-000001", "Aktuel", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** returnerer den forberedte datacontainer med saldi for anlægsaktivet **"COMP-000001"**, der har værdimodellen **"Aktuel"** for den aktuelle programsessionsdato. |
| TABLENAME2ID (streng) | Returnerer en heltalsrepræsentation af et tabel-Id for det angivne tabelnavn. | **TABLENAME2ID ("Intrastat")** returnerer **1510**. |
| ISVALIDCHARACTERISO7064 (streng) | Returnerer den booleske værdi **TRUE**, når den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN). I modsat fald returneres den booleske værdi **FALSE**. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** returnerer **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** returnerer **FALSE**. |
| NUMSEQVALUE (nummerseriekode, område, område-id) | Returnerer den nye genererede værdi for en nummerserie baseret på den angivne nummerseriekode, område og område-id. Området skal angives som en værdi af optællingen **ERExpressionNumberSequenceScopeType** (**Delt**, **Juridisk enhed** eller **Firma**). For området **Delt** skal du angive en tom streng som område-id'et. For områderne **Firma** og **Juridisk enhed** skal du angive firmakoden som område-id. For områderne **Firma** og **Juridisk enhed**, hvis du angiver en tom streng som område-id, bruges den aktuelle firmakode. | Du definerer følgende datakilder i din modeltilknytning:<ul><li>**enumScope** (**Dynamics 365 for Operations-optælling** type), som refererer til optællingen **ERExpressionNumberSequenceScopeType**</li><li>**NumSeq** (typen **Beregnet felt**), som indeholder udtrykket **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")**</li></ul>Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den **Gene\_1**-nummerserie, der er konfigureret for det firma, der leverer den kontekst, som ER-formatet køres under. |
| NUMSEQVALUE (nummerseriekode) | Returnerer den nye genererede værdi for en nummerserie baseret på den angivne nummerserie, området **Firma** og koden for det firma (som område-id), der leverer den kontekst, ER-formatet køres under. | Du kan definere følgende datakilde i din modeltilknytning: **NumSeq** (typen **Beregnet felt**). Denne datakilde indeholder udtrykket **NUMSEQVALUE ("Gene\_1")**. Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den **Gene\_1**-nummerserie, der er konfigureret for det firma, der leverer den kontekst, som ER-formatet køres under. |
| NUMSEQVALUE (nummerseriepost-id) | Returnerer den nye genererede værdi for en nummerserie baseret på post-id'et for den angivne nummerserie. | Du definerer følgende datakilder i din modeltilknytning:<ul><li>**LedgerParms** (typen **Tabel**), som refererer til tabellen LedgerParameters</li><li>**NumSeq** (typen **Beregnet felt**), som indeholder udtrykket **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)**</li></ul>Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den nummerserie, der er konfigureret i Finans-parametrene for det firma, der leverer den kontekst, som ER-formatet køres under. Denne nummerserie identificerer entydigt kladder og fungerer som et batchnummer, der knytter posteringerne sammen. |

### <a name="functions-list-extension"></a>Funktionslistens udvidelse

ER understøtter muligheden for at udvide listen over funktioner, der bruges i ER-udtryk. Der kræves en vis teknisk indsats for at gøre dette. Yderligere oplysninger finder du under [Udvidelse af listen over elektroniske rapporteringsfunktioner](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Udvide listen over elektroniske rapporteringsfunktioner (ER)](general-electronic-reporting-formulas-list-extension.md)