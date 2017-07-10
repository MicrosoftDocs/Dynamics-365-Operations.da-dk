---
title: Formeldesigner i elektronisk rapportering
description: "Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge Microsoft Excel-lignende formler for datatransformation, der opfylder kravene til dette dokuments udførelse og formatering. Forskellige typer funktioner understøttes: tekst, dato og klokkeslæt, matematisk logik, oplysninger, konvertering af datatypen og andre (domænespecifikke funktioner i virksomheden)."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 655a6fd99c0688b13c31c79f3322a287f902e7f1
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formeldesigner i elektronisk rapportering

[!include[banner](../includes/banner.md)]


Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge Microsoft Excel-lignende formler for datatransformation, der opfylder kravene til dette dokuments udførelse og formatering. Forskellige typer funktioner understøttes: tekst, dato og klokkeslæt, matematisk logik, oplysninger, konvertering af datatypen og andre (domænespecifikke funktioner i virksomheden).

<a name="formula-designer-overview"></a>Oversigt over formeldesigner
-------------------------

Elektronisk rapportering (ER) understøtter formeldesigneren. Derfor kan du på designtidspunktet konfigurere udtryk, der kan bruges til følgende opgaver under kørsel:

-   Transformere data, der er modtaget fra en Microsoft Dynamics 365 for Finance and Operations-database, der skal udfyldes på en ER-datamodel, der er designet til at være datakilde til ER-formater (filtrering, gruppering, konvertering af datatyper osv.).
-   Formatere data, der skal sendes til et genererende elektronisk dokument i henhold til layout og betingelser for et bestemt ER-format (i henhold til ønsket sprog eller kultur, kodning osv.).
-   Styre processen til generering af elektronisk dokument (aktivering/deaktivering af output af visse formatelementer, afhængigt af behandling af data, afbrydelse af dokumentoprettelse, afsendelse af meddelelser for slutbrugere osv.).

Derfor kan siden i formeldesigneren åbnes, når du gør følgende:

-   Binder datakildeelementer til datamodelkomponenter.
-   Binder datakildeelementer til formatkomponenter.
-   Vedligeholder beregnede felter som en del af datakilder.
-   Definerer synlighedsbetingelser for brugerinputparametre.
-   Designer formatets transformeringer.
-   Definerer aktivering af betingelserne for formatets komponenter.
-   Definerer filnavne til formatets FILE-komponenter.
-   Definerer betingelserne for proceskontrolvalideringer.
-   Definerer meddelelsestekst for proceskontrolvalideringer.

## <a name="designing-er-formulas"></a>Design af ER-formler
### <a name="data-binding"></a>Databinding

ER-formeldesigneren kan bruges til at definere et udtryk, der transformerer data, der er modtaget fra datakilder, så data kan udfyldes i forbrugernes data under kørsel:

-   Fra Finance and Operations-datakilder og kørselsparametre til ER-datamodel.
-   Fra en ER-datamodel til et ER-format.
-   Fra Finance and Operations-datakilder og kørselsparametre til ER-format.

I følgende illustration vises et udtryk af denne type design. I dette eksempel returnerer udtrykket værdien af feltet **Intrastat.AmountMST** i Finance and Operations-tabellen **Intrastat**, når værdien er blevet afrundet til to decimaler. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) I følgende illustration vises, hvordan et udtryk af denne type kan bruges. I dette eksempel er resultatet af det designede udtryk udfyldt i **Transaction.InvoicedAmount**-komponenten af **momsrapporteringsmodellen**. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) På kørselstidspunktet vil den designede formel **ROUND (Intrastat.AmountMST, 2)** afrunde værdien af feltet **AmountMST** for hver post i tabellen **Intrastat** til to decimaler og udfylde den afrundede værdi i komponenten **Transaction.InvoicedAmount** i datamodellen **Momsrapportering**.

### <a name="data-formatting"></a>Dataformatering

ER-formeldesigneren kan bruges til at definere et udtryk, der formaterer data, der er modtaget fra datakilder, så data kan sendes som en del af det genererende elektroniske dokument. Hvis der er formatering, der skal anvendes som en typisk regel, der skal genbruges til et format, kan du introducere formateringen én gang i en formatkonfiguration som en navngivet transformering, der har et formateringsudtryk. Senere kan denne navngivne transformation sammenkædes med mange formatkomponenter, hvis output skal formateres i henhold til det oprettede udtryk. I følgende illustration vises designet af en transformation af denne type. Dette eksempel på **TrimmedString**-transformation tager indgående data i **Streng**-datatypen og afkorter foranstillede og efterstillede mellemrum, når den returnerer en strengværdi. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) I følgende illustration vises, hvordan en transformation af denne type kan bruges. I dette eksempel finder du flere formatkomponenter, som sender tekst som output til det genererende elektroniske dokument på kørselstidspunktet til **TrimmedString**-transformationen efter navn. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Når formatkomponenter refererer til **TrimmedString**-transformation (for eksempel **partyName**-komponenten i den foregående illustration), sendes tekst som output for at generere dokumentet. Teksten indeholder ikke foranstillede eller efterstillede mellemrum. Hvis du har en formatering, der skal anvendes individuelt, kan den indføres som et individuelt udtryk for binding af en bestemt formatkomponent. I følgende illustration vises et udtryk af denne type. I dette eksempel er **partyType**-formatkomponenten bundet til datakilden via et udtryk, der konverterer indgående data fra feltet **Model.Company.RegistrationType** i datakilden til stor bogstavtekst og sender teksten som output til det elektroniske dokument. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Kontrol af procesforløb

ER-formeldesigneren kan bruges til at definere udtryk, der styrer procesforløbet under generering af dokumenter. Du kan gøre følgende:

-   Definer betingelser, der bestemmer, hvornår en proces til oprettelse af dokumentet skal stoppes.
-   Angiv udtryk, der opretter enten meddelelser til slutbrugeren om stoppede processer eller udløser en kørselslogbesked om, at processen fortsætter med oprettelse af rapporter.
-   Angiv filnavne til oprettelse af dokumenter, og kontrollér betingelserne for deres oprettelse.

Hver regel i kontrol af procesforløb udformet som en enkelt validering. I følgende illustration vises en validering af denne type. Her er en forklaring af konfigurationen i dette eksempel:

-   Valideringen evalueres, når **INSTAT**-noden oprettes i den genererende XML-fil.
-   Hvis listen over transaktioner er tom, stopper valideringen kørselsprocessen og returnerer **FALSE**.
-   Valideringen returnerer en fejlmeddelelse, der indeholder teksten til etiketten for SYS70894 på brugerens foretrukne sprog.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) Eksempel på validering ER-formeldesigneren bruges også til at angive et filnavn til et genererende elektronisk dokument og styring af processen til oprettelse af en fil. I følgende illustration vises designet af en kontrol af procesforløb af denne type. Her er en forklaring af konfigurationen i dette eksempel:

-   listen over poster fra datakilden **model.Intrastat-** opdeles i batches, der indeholder op til 1.000 poster hver.
-   Output opretter en zip-fil, der indeholder en fil i XML-format for hver batch, der blev oprettet.
-   Et udtryk returnerer et filnavn til generering af elektroniske dokumenter ved at sammenkæde filnavnet og filtypenavnet. For den anden batch og alle efterfølgende batches indeholder filnavnet batch-ID som et suffiks.
-   Et udtryk aktiverer (returnerer **TRUE**) processen med en filoprettelse for de eneste batches, der indeholder mindst én post.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grundlæggende syntaks

ER udtryk kan indeholde én eller flere af følgende elementer:

-   Konstanter
-   Operatorer
-   Referencer
-   Stier
-   Funktioner

#### <a name="constants"></a>Konstanter

Du kan bruge tekst og numeriske konstanter (værdier, der ikke beregnes) i udformningen af udtryk. Den numeriske konstant 20 og strengkonstanten "100" anvendes f.eks. i udtrykket **VALUE ("100") + 20**, der returnerer den numeriske værdi **120**. Escape-sekvenser understøttes i ER-formeldesigneren, så du kan angive den del af udtryksstrengen, der skal håndteres anderledes. F.eks. returnerer udtrykket **"Leo Tolstoy ""Krig og fred"" Bind 1"** tekststrengen **Leo Tolstoy "Krig og fred" Bind 1**.

#### <a name="operators"></a>Operatorer

Følgende tabel viser de aritmetiske operatorer, du kan bruge til at udføre grundlæggende matematiske funktioner som addition, subtraktion, division og multiplikation.

| Operatør | Betydning              | Eksempel |
|----------|----------------------|---------|
| +        | Tilføjelse             | 1+2     |
| -        | Subtraktion Negation | 5-2 -1  |
| \*       | Multiplikation       | 7\*8    |
| /        | Afdeling             | 9/3     |

I følgende tabel vises de sammenligningsoperatorer, der også understøttes, og som du kan bruge til at sammenligne to værdier.

| Operatør | Betydning                  | Eksempel    |
|----------|--------------------------|------------|
| =        | Lig                    | X=Y        |
| &gt;     | Større end             | X&gt;Y     |
| &lt;     | Mindre end                | X&lt;Y     |
| &gt;=    | Større end eller lig med | X&gt;=Y    |
| &lt;=    | Mindre end eller lig med    | X&lt;=Y    |
| &lt;&gt; | Ikke lig med             | X&lt;&gt;Y |

Du kan desuden bruge et og-tegn (&) som en sammenkædningsoperator, der sammensætter eller sammenføjer en eller flere tekststrenge i et enkelt stykke tekst.

| Operatør | Betydning     | Eksempel                                        |
|----------|-------------|------------------------------------------------|
| &        | Sammenkæde | "Intet at udskrive" & ": " & "Der blev ikke fundet nogen poster" |

#### <a name="operator-precedence"></a>Den prioriterede operatorrækkefølge

Den rækkefølge, som delene af et sammensat udtryk evalueres i, er vigtig. For eksempel er resultatet af udtrykket **1 + 4 / 2** forskelligt, afhængigt af om addition eller division udføres først. Du kan bruge parenteser til eksplicit at angive, hvordan et udtryk evalueres. Du kan for eksempel for at angive, at addition skal udføres først, ændre det foregående udtryk til **(1 + 4) / 2**. Hvis rækkefølgen af operationer, der skal udføres i et udtryk, ikke er udtrykkeligt defineret, er rækkefølgen baseret på standardrangfølgen, der er tildelt de understøttede operatorer. Følgende tabeller viser operatorerne og den prioritet, der er tildelt hver enkelt. Operatorer, der har højere prioritet (for eksempel 7), evalueres før operatorer, der har lavere prioritet (f.eks. 1).

| Prioritering | Operatorer      | Syntaks                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                    |
| 6          | Medlemsadgang  | … . …                                                    |
| 5          | Funktionskald  | … ( … )                                                  |
| 4          | Multiplikation | … \* … … / …                                             |
| 3          | Tilføjelse       | … + … … - …                                              |
| 2          | Sammenligning     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Separation     | … , …                                                    |

Operatorer på samme linje har samme prioritet. Hvis et udtryk indeholder mere end én af disse operatorer, skal det evalueres de fra venstre mod højre. For eksempel vil udtrykket **1 + 6 / 2 \* 3 &gt; 5** returnere **true**. Vi anbefaler, at du bruger parenteser til at angive den ønskede rækkefølge i evalueringen af udtryk, så det bliver nemmere at læse og vedligeholde udtrykkene eksplicit.

#### <a name="references"></a>Referencer

Alle datakilder for den aktuelle ER-komponent (en model eller et format), der er tilgængelige under designet af et udtryk, kan bruges som navngivne referencer. For eksempel indeholder den aktuelle ER-datamodel datakilden **ReportingDate**, der returnerer værdien af datatypen **DATETIME**. Denne værdi i det genererende dokument skal formateres korrekt ved at referere til datakilden i udtrykket på følgende måde: **DATETIMEFORMAT (ReportingDate, "dd-MM-åååå")** Alle tegn i navnet på en refererende datakilde, der ikke repræsenterer et bogstav i alfabetet, skal indledes med et enkelt anførselstegn ('). Hvis navnet på en refererende datakilde indeholder mindst ét symbol, der ikke repræsenterer et bogstav i alfabetet (for eksempel tegnsætningstegn eller andre skriftlige symboler), skal navnet stå i anførselstegn. Her er nogle eksempler:

-   Datakilden **Today’s date & time** skal refereres til i ER-udtryk som følger: **'Today''s date & time’**
-   Metoden **name()** i datakilden **Customers** skal refereres til i ER-udtryk som følger: **Customers.'name()'**

Bemærk, at følgende syntaks bruges til at kalde Dynamics 365 for Operations-datakilder med parametre:

- Der skal refereres til metoden isLanguageRTL for datakilden System med en EN-US parameter af datatypen streng i et ER-udtryk på følgende måde: System.'isLanguageRTL'("EN-US").
- Anførselstegn er ikke obligatoriske, når et metodenavn kun indeholder alfanumeriske symboler. De er obligatoriske for en metode for en tabel, når navnet indeholder kantede parenteser.

Når systemdatakilden føjes til en ER-tilknytning, der henviser til programklassen Global i Dynamics 365 for Operations, returnerer udtrykket den booleske værdi FALSE. Det ændrede udtryk System.’ isLanguageRTL'("AR") returnerer den booleske værdi TRUE.

Bemærk, at videresendelse til sådanne metodeparametre kan defineres med følgende begrænsninger:

- Kun konstanter kan sendes til disse metoder, hvis værdi defineres i designfasen.
- Kun primitive (basis)-datatyper understøttes for disse parametre (heltal, reelt tal, boolesk, streng osv.).

#### <a name="path"></a>Sti

Når et udtryk refererer til en struktureret datakilde, kan du bruge definitionen af stien til at vælge et bestemt primitivt element i datakilden. Tegnet en prik (.) bruges til at adskille de enkelte elementer i en struktureret datakilde. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, der returnerer listen med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, der returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan defor være udformet således: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funktioner

Det næste afsnit beskriver de funktioner, der kan bruges i ER-udtryk. Alle datakilder i udtrykskonteksten (aktuel ER-datamodel eller ER-format) samt konstanter kan bruges som parametre til opkaldsfunktioner i henhold til listen over opkaldsfunktionsargumenter. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, der returnerer listen med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, der returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan derfor være udformet således ved at bruge den indbyggede ER-afrundingsfunktion: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Understøttede funktioner
I følgende tabel beskrives de datamanipulationsfunktioner, du kan bruge til at designe ER-datamodeller og ER-rapporter. Denne liste over funktioner er ikke fast og kan udvides af udviklere. Du kan se listen over funktioner, du kan bruge, i ruden med funktioner i ER-formeldesigneren.

### <a name="date-and-time-functions"></a>Dato- og klokkeslætsfunktioner

| Funktion                                   | Beskrivelse                                                                                                                                                                                                                                                                                                                                                      | Eksempel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datetime, dage)                   | Føj det angivne antal dage til den angivne datetime-værdi.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW() 7)** returnerer datoen og klokkeslættet syv dage ud i fremtiden.                                                                                                                                                                                                                            |
| DATETODATETIME (dato)                      | Konverter den angivne datoværdi til en datetime-værdi.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den aktuelle Finance and Operations-sessionsdato, 24-12-2015, som **12/24/2015 12:00:00 AM**. I dette eksempel er **CompInfo** en datakilde til ER af typen **Finance and Operations/tabel**, der refererer til tabellen CompanyInfo. |
| NOW ()                                     | Returner aktuel Finance and Operations-dato og -klokkeslæt på programserver som en dato- og klokkeslætsværdi.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Returner aktuel Finance and Operations-dato og -klokkeslæt på programserver som en datoværdi.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Returner en **null**-datoværdi.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Returner en **null**-datetime-værdi.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datetime, format)          | Konverter den angivne datetime-værdi til en streng i det angivne format. (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** returnerer den aktuelle Finance and Operations-programserverdato, 24-12-2015, som **"24-12-2015"**, i overensstemmelse med det angivne brugerdefinerede format.                                                                                                          |
| DATETIMEFORMAT (datetime, format, kultur) | Konverter den angivne datetime-værdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** returnerer den aktuelle Finance and Operations-programserverdato, 24-12-2015, som **"24.12.2015"**, i henhold til den valgte tyske kultur.                                                                                                             |
| SESSIONTODAY ()                            | Returnerer aktuel Dynamics 365 for Finance and Operations-sessionsdato som datoværdi.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Returnerer aktuel Dynamics 365 for Finance and Operations-sessionsdato og -klokkeslæt som en dato- og klokkeslætsværdi.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (dato, format)                  | Returnerer strengværdi af dato ved brug af det angivne format.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** returnerer den aktuelle Dynamics 365 for Finance and Operations-sessionsdato, 24-12-2015, som "**24-12-2015**" i overensstemmelse med det angivne brugerdefinerede format.                                                                                                                      |
| DATEFORMAT (dato, format, kultur)         | Konverter den angivne datoværdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** returnerer den aktuelle Finance and Operations-sessionsdato, 24-12-2015, som **"24.12.2015"**, i henhold til den valgte tyske kultur.                                                                                                                       |
| DAYOFYEAR (dato)              | Returnerer heltalsrepræsentationen af antallet af dage mellem 1. januar og den angivne dato.       | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** returnerer **61**.
**DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** returnerer **1**.                                                                                                                       |

**Datakonverteringsfunktioner**

| Funktion                                   | Betegnelse                                                                                                                                                                                                                                                                                                                                                      | Eksempel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATETODATETIME (dato)                 | Konverter den angivne datoværdi til en datetime-værdi.           | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den aktuelle Finance and Operations-sessionsdato, 24-12-2015, som **12/24/2015 12:00:00 AM**. I dette eksempel er **CompInfo** en datakilde til ER af typen **Finance and Operations/tabel**, der refererer til tabellen **CompanyInfo**.                                                                                                                       |
| DATEVALUE (streng, format)              | Returnerer datovisning af en streng ved hjælp af et angivet format.       | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** returnerer datoen 12/21/2016 i overensstemmelse med det angivne brugerdefinerede format og standardprogrammets **EN-US** kultur.                                                                                                                       |
| DATEVALUE (streng, format, kultur)              | Returnerer datovisningen af en streng ved hjælp af et angivet format og en angivet kultur.       | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “IT”)** returnerer datoen 01/21/2016 i overensstemmelse med det angivne brugerdefinerede format og kultur. Der udløses en undtagelse for dette funktionskald, **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", “EN-US”)**, med besked om, at en given streng ikke genkendes som en gyldig dato.                                                                                                                       |
| DATETIMEVALUE (streng, format)              | Returnerer datetime-visning af en streng ved hjælp af et angivet format.       | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** returnerer den 21. december 2016 kl. 14:55:00 i overensstemmelse med de angivne brugerdefinerede format og standard programmets **EN-US** kultur.                                                                                                                       |
| DATETIMEVALUE (streng, format, kultur)              | Returnerer datetime-visningen af en streng ved hjælp af et angivet format og en angivet kultur.       | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “IT”)** returnerer den 21. december 2016 kl. 14:55:00 i overensstemmelse med et angivet brugerdefineret format og kultur. Der udløses en undtagelse for dette funktionskald, **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", “EN-US”)**, med besked om, at en given streng ikke genkendes som gyldig dato og klokkeslæt.                                                                                                                       |
### <a name="list-functions"></a>Listefunktioner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Betegnelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (input, længde)</td>
<td>Opdeler den angivne inputstreng i understrenge, som hver især har den angivne længde. Returner resultatet som en ny liste.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> returnerer en ny liste, der består af to poster, der har et <strong>STRING</strong>-felt. Feltet i den første post indeholder teksten <strong>&quot;abc&quot;</strong>, og feltet i den anden post indeholder teksten <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (liste, antal)</td>
<td>Opdel den angivne liste i batches, som hver især indeholder det angivne antal poster. Returner resultatet som en ny liste over batches, der indeholder følgende elementer:
<ul>
<li>Batches som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle batchnummer (<strong>Batchnummer-</strong>komponent)</li>
</ul></td>
<td>I følgende eksempel bliver <strong>Linjer</strong>-datakilde oprettet som en postliste med tre poster, der er opdelt i batches, der hver især indeholder op til to poster. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> Her er det designede formatlayout, hvor bindinger til <strong>Linjer</strong>-datakilden er oprettet for at generere output i XML-format, som præsenterer enkelte noder for hver batch og posterne i den. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> Følgende er resultatet af at køre det designede format. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (post 1 [, post 2,...])</td>
<td>Returner en ny liste, der oprettes ud fra de angivne argumenter.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> returnerer en tom post, hvor listen over felter indeholder alle felterne i postlisterne <strong>MainData</strong> og <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Returner en ny forenet liste, der oprettes ud fra lister med de angivne argumenter.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> returnerer listen over seks poster, hvor et felt af <strong>STRING</strong>-datatypen indeholder enkelte bogstaver.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (liste)</td>
<td>Returnerer <strong>TRUE</strong>, hvis den angivne liste ikke indeholder nogen elementer. Ellers returneres <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (liste)</td>
<td>Returner en tom liste ved hjælp af den angivne liste som kilde til listestrukturen.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> returnerer en ny tom liste, der har samme struktur som den liste, der er returneret af <strong>SPLIT</strong>-funktionen.</td>
</tr>
<tr class="odd">
<td>FIRST (liste)</td>
<td>Returner den første post i den angivne liste, hvis posten ikke er tom. Ellers udløses en undtagelse.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (liste)</td>
<td>Returner den første post i den angivne liste, hvis posten ikke er tom. Ellers returneres en <strong>null</strong>-post.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (liste)</td>
<td>Returner en liste, der kun indeholder det første element på en given liste.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (sti)</td>
<td>Returner en ny, udlignet liste, der repræsenterer alle elementer, der svarer til den angivne sti. Stien skal defineres som en gyldig datakildesti til et datakildeelement af datatypen postliste. Stien til streng-, dato- og andre dataelementer bør udløse en fejl i designfasen i ER-udtryksgeneratoren.</td>
<td>Hvis du angiver <strong>SPLIT (&quot;abcdef&quot;, 2)</strong> som datakilde (DS), vil <strong>COUNT (ALLITEMS (DS.Value))</strong> returnere <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (liste [udtryk 1, udtryk, 2, ...])</td>
<td>Returner den angivne liste sorteret efter de angivne argumenter, der kan defineres som udtryk.</td>
<td>Når <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>ORDERBY (Vendors, Vendors.'name()')</strong> returnere en liste over kreditorer, der er sorteret efter navn i stigende rækkefølge.</td>
</tr>
<tr class="even">
<td>REVERSE (liste)</td>
<td>Returner den angivne liste i omvendt rækkefølge.</td>
<td>Når <strong>Vendor</strong>er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> returnere en liste over kreditorer, der er sorteret efter navn i faldende rækkefølge.</td>
</tr>
<tr class="odd">
<td>WHERE (liste, betingelse)</td>
<td>Returner den angivne liste, der er filtreret efter den angivne betingelse. I modsætning til <strong>FILTER</strong>-funktionen, den bliver den angivne betingelse anvendt på listen i hukommelsen.</td>
<td>Når <strong>Vendor</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> returnere en liste over kreditorer, der tilhører kreditorgruppe 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (liste)</td>
<td>Returner en ny liste, der består af optalte poster af den angivne liste og viser følgende elementer:
<ul>
<li>Angivne listeposter som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle postindeks (<strong>Tal-</strong>komponent)</li>
</ul></td>
<td>I følgende eksempel er <strong>Enumerated</strong>-datakilden oprettet som en fasttekstliste over kreditorposter fra <strong>Vendors</strong>-datakilden, der henviser til <strong>VendTable</strong>-tabellen. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Her er formatet, hvor der oprettes databindinger for at generere output i XML-format, som præsenterer enkelte kreditorer som fasttekstnoder. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> Dette er resultatet af at køre det designede format. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (liste)</td>
<td>Returner antal poster på den angivne liste, hvis listen ikke er tom. Ellers returneres <strong>0</strong> (nul).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> returnerer <strong>2</strong>, fordi <strong>SPLIT</strong>-funktionen opretter en liste, der består af to poster.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (sti)</td>
<td>Returnerer en postliste, der er oprettet ud fra et argument i en af følgende typer:
<ul>
<li>Modelfasttekst</li>
<li>Formatfasttekst</li>
<li>Container</li>
</ul>
Den oprettede liste består af poster med følgende felter:
<ul>
<li>Navn</li>
<li>Etiket</li>
<li>Betegnelse</li>
</ul>
Felterne Label og Beskrivelse returnerer på kørselstidspunktet værdier baseret på formatets sprogindstillinger.</td>
<td>Følgende eksempel viser den fasttekst, der er introduceret i en datamodel. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Følgende eksempel viser:
<ul>
<li>Modelfasttekst, der er indsat i en rapport som en datakilde.</li>
<li>ER-udtryk, der er designet til at bruge modelfasttekst som parameter for denne funktion.</li>
<li>Datakilde til postlistetype, der er indsat i en rapport ved hjælp af det oprettede ER-udtryk.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> Følgende eksempel viser de ER-formatelementer, der er bundet til datakilden af post listetypen, som blev oprettet ved hjælp af funktionen LISTOFFIELDS.<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Dette er resultatet af kørslen designformatet.<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Bemærk!</strong> Oversat tekst til labels og beskrivelser er udfyldt til ER-formatoutput i overensstemmelse med de sprogindstillinger, der er konfigureret til overordnede FILE- og FOLDER-formatelementer.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (liste, feltnavn, afgrænser)</td>
<td>Returnerer strengen sammenføjede værdier for et felt fra en liste, der er adskilt med det valgte afgrænsningstegn.</td>
<td>Hvis du har angivet SPLIT("abc", 1) som en datakilde-DS, vil udtrykket STRINGJOIN (DS, DS.Value, ":") returnere "a:b:c"</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (liste, grænseværdi. grænsekilde)</td>
<td>Opdeler den angivne liste i en ny liste over underordnede lister og returnerer resultatet i indholdet af listen over poster. Parameteren for grænseværdi angiver værdien af grænsen for at opdele den oprindelige liste. Parameteren for grænsekilde angiver det trin, hvor den samlede sum forøges. Grænsen anvendes ikke på et enkelt element på listen, når grænsekilden overskrider den angivne grænse.</td>
<td>Følgende eksempel viser formatet, der bruger datakilder. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Dette er resultatformatudførelsen, der præsenterer den flade liste med varer.<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>I følgende eksempel vises det samme format, der blev reguleret for at vise listen over varer i batches, når et enkelt batch skal indeholde varer med den samlede vægt, der ikke bør overstige grænsen på 9.<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Dette er resultatet af kørslen af det regulerede format. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Bemærk!</strong> Grænsen anvendes ikke på det sidste element på den oprindelse liste, da værdien (11) af grænsekilden (vægt) overskrider den angivne grænse (9). Brug enten funktionen <strong>WHERE</strong> eller <strong>Aktiveret</strong>-udtrykket for det tilsvarende formatelement for at ignorere (springe over) underordnede lister under oprettelsen af rapporten (om nødvendigt).</td>
</tr>
<tr class="odd">
<td>FILTER (liste, betingelse)</td>
<td>Returnerer den angivne liste, der er filtreret efter den angivne betingelse ved at ændre forespørgslen. I modsætning til funktionen <strong>WHERE</strong>, anvendes den angivne betingelse på databaseniveau til en ER-datakilde af typen tabelposter.</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) returnerer listen over ene leverandører tilhørende leverandørgruppe “40”, når <strong>Vendor</strong> er konfigureret som ER-datakilde, der refererer til tabellen <strong>VendTable</strong></td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logiske funktioner

| Funktion                                                                                | Betegnelse                                                                                                                                                                                                                                                                     | Eksempel                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (udtryk, valgmulighed 1, resultat 1 \[, valgmulighed 2, resultat 2\] ... \[, standardresultat\]) | Evaluer den angivne udtryksværdi mod de angivne alternative valgmuligheder. Returner resultatet af den valgmulighed, der er lig med værdien af udtrykket. Ellers returneres det eventuelt angivne standardresultat (den sidste parameter, der ikke indledes med en valgmulighed). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")** returnerer strengen **"VINTER"**, når den aktuelle Finance and Operations-sessionsdato er mellem oktober og december. Ellers returneres en tom streng. |
| IF (betingelse, værdi 1, værdi 2)                                                        | Returner den angivne værdi 1, når den angivne betingelse er opfyldt. Ellers returneres værdi 2. Hvis værdi 1 og 2 er poster eller postlister, har resultatet kun de felter, der findes på begge lister.                                                                     | **IF (1 = 2, "betingelse er opfyldt", "betingelse er ikke opfyldt")** returnerer strengen **"betingelse er ikke opfyldt"**.                                                                                                                                                      |
| NOT (betingelse)                                                                         | Returner den omvendte logiske værdi af den angivne betingelse.                                                                                                                                                                                                                   | **NOT (TRUE)** returnerer **FALSE**.                                                                                                                                                                                                                            |
| AND (betingelse 1\[, betingelse 2, ...\])                                                 | Returnerer **TRUE**, hvis *alle *angivne betingelser er sande. Ellers returneres **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** returnerer **TRUE**. **AND (1=2, "a"="a")** returnerer **FALSE**.                                                                                                                                                                           |
| OR (betingelse 1\[, betingelse 2, ...\])                                                  | Returnerer **FALSE**, hvis *alle *angivne betingelser er falske. Returnerer **TRUE**, hvis *en af *de angivne betingelser er sande.                                                                                                                                                                 | **OR (1=2, "a"="a")** returnerer **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matematiske funktioner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (tal)</td>
<td>Returnerer den absolutte værdi af det angivne tal (tallet uden dets fortegn).</td>
<td><strong>ABS (-1)</strong> returnerer <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (tal, potens)</td>
<td>Returnerer resultatet af at opløfte det angivne positive tal i den angivne potens.</td>
<td><strong>POWER (10, 2)</strong> returnerer <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (streng, decimalseparator, ciffergrupperingsseparator)</td>
<td>Konverter den angivne streng til et tal. Det angivne symbol, der bruges til at adskille heltal og brøkdele af et decimaltal, og den angivne tusindtalsseparator bruges også.</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot; &quot; &quot;)</strong> returnerer værdien <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (streng)</td>
<td>Konverter den angivne streng til et tal. Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som negativt fortegn. Udløs en undtagelse, hvis der findes andre ikke-numeriske tegn i den angivne streng.</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> medfører en undtagelse.</td>
</tr>
<tr class="odd">
<td>ROUND (tal, decimaler)</td>
<td>Returner det angivne tal, der er afrundet til det angivne antal decimaler:
<ul>
<li>Hvis den angivne decimalværdi er større end 0 (nul), afrundes det angivne tal til det angivne antal decimaler.</li>
<li>Hvis den angivne decimalværdi er 0 (nul), afrundes det angivne tal til det nærmeste heltal.</li>
<li>Hvis den angivne decimalværdi er mindre end 0 (nul), afrundes det angivne tal mod venstre til decimalpunktet.</li>
</ul></td>
<td><strong>ROUND (1200.767. 2)</strong> afrunder til to decimaler og returnerer <strong>1200.77</strong>. <strong>ROUND (1200.767, -3)</strong> afrunder til det nærmeste multiplum af 1.000 og returnerer <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (tal, decimaler)</td>
<td>Returner det angivne tal, der er afrundet ned (mod nul) til det angivne antal decimaler. <strong>Bemærk:</strong> Denne funktion fungerer ligesom <strong>ROUND</strong>, men den runder altid det angivne tal ned.</td>
<td><strong>ROUNDDOWN (1200.767. 2)</strong> afrunder ned til to decimaler og returnerer <strong>1200.76</strong>. <strong>ROUNDDOWN (1700.767, -3)</strong> afrunder ned til det nærmeste multiplum af 1.000 og returnerer <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (tal, decimaler)</td>
<td>Returner det angivne tal, der er afrundet op (væk fra nul) til det angivne antal decimaler. <strong>Bemærk:</strong> Denne funktion fungerer ligesom <strong>ROUND</strong>, men den runder altid det angivne tal op.</td>
<td><strong>ROUNDUP (1200.763. 2)</strong> afrunder op til to decimaler og returnerer <strong>1200.77</strong>. <strong>ROUNDUP (1200.767, -3)</strong> afrunder op til det nærmeste multiplum af 1.000 og returnerer <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

**Datakonverteringsfunktioner**

| Funktion             | Betegnelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| VALUE (streng) | Konverter den angivne streng til et tal. Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som et negativt fortegn. Der udløses en undtagelse, hvis der findes andre ikke-numeriske tegn i den angivne streng.                                                                                  | **VALUE ("1 234,56")** medfører en undtagelse.   |
| NUMBERVALUE (streng, decimalseparator, ciffergrupperingsseparator) | Konverter den angivne streng til et tal. Det angivne symbol, der bruges til at adskille heltal og brøkdele af et decimaltal, og den angivne tusindtalsseparator bruges også.                                                                                  | **NUMBERVALUE("1 234,56", ", " "")** returnerer værdien **1234.56**.    |
| INTVALUE (streng) | Returnerer en heltalsrepræsentation af en streng. Eventuelle decimaldele afkortes.                                                                                  | **INTVALUE ("100.77")** returnerer **100**. |
| INTVALUE (tal) | Returnerer en heltalsrepræsentation af et tal. Eventuelle decimaldele afkortes.                                                                                  | **INTVALUE (-100.77)** returnerer **-100**. |
| INT64VALUE (streng) | Returnerer en int64-repræsentation af en streng. Eventuelle decimaldele afkortes.                                                                                  | **INT64VALUE (“22565422744”)** returnerer **22565422744**. |
| INT64VALUE (tal) | Returnerer en int64-repræsentation af et tal. Eventuelle decimaldele afkortes.                                                                                  | **INT64VALUE (22565422744.00)** returnerer **22565422744**. |



### <a name="record-functions"></a>Postfunktioner

| Funktion             | Betegnelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (liste) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post. **Bemærk:** Denne funktion er forældet. Brug **EMPTYRECORD** i stedet.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen. |
| EMPTYRECORD (post) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post. **Bemærk:** En **null**-post er en post, hvor alle felter har en tom værdi (**0** \[nul\] for tal, en tom streng for strenge osv). | **EMPTYRECORD (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen.   |

### <a name="text-functions"></a>Tekstfunktioner

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (streng)</td>
<td>Returner den angivne streng konverteret til store bogstaver.</td>
<td><strong>UPPER(&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;EKSEMPEL&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (streng)</td>
<td>Returner den angivne streng konverteret til små bogstaver.</td>
<td><strong>LOWER (&quot;Eksempel&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra starten af den angivne streng.</td>
<td><strong>LEFT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;Eks&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra slutningen af den angivne streng.</td>
<td><strong>RIGHT (&quot;Eksempel&quot;, 3)</strong> returnerer <strong>&quot;pel&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (streng, startposition, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra startpositionen i den angivne streng.</td>
<td><strong>MID (&quot;Eksempel&quot;, 2, 3)</strong> returnerer <strong>&quot;kse&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (streng)</td>
<td>Returner antallet af tegn i den angivne streng.</td>
<td><strong>LEN (&quot;Eksempel&quot;)</strong> returnerer <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (tal)</td>
<td>Returner den streng af tegn, der refereres til af det angivne Unicode-tal.</td>
<td><strong>CHAR (255)</strong> returnerer <strong>&quot;ÿ&quot;</strong>. <strong>Bemærk:</strong> Den returnerede streng afhænger af den kodning, der er valgt i det overordnede FILE-formatelement. Listen over understøttede kodninger findes i emnet <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodningsklasse</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (streng 1 [, streng 2, ...])</td>
<td>Returner alle angivne tekststrenge, der er sat ind i én streng.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> returnerer <strong>&quot;abcdef&quot;</strong>. <strong>Bemærk:</strong> Udtrykket <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> returnerer også <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (streng, mønster, erstatning)</td>
<td>Returner den angivne streng, hvor alle forekomster af tegn i det angivne strengmønster erstattes med tegn på den tilsvarende position i den angivne erstatningsstreng.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (streng, mønster, erstatning, almindeligt udtryksflag)</td>
<td>Når det angivne udtryksflag er <strong>true</strong>, returneres den angivne streng, som er blevet ændret ved at anvende det almindelige udtryk, der er angivet som et mønsterargument for denne funktion. Dette udtryk bruges til at søge efter tegn, der skal erstattes. Tegn i det angivne erstatningsargument bruges til at erstatte tegn, der findes. Når det angivne udtryksflag er <strong>false</strong>, fungerer denne funktion ligesom <strong>TRANSLATE</strong>.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, true)</strong> anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (input)</td>
<td>Returner det angivne input, som er konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard til den aktuelle forekomst af Finance and Operations. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>Hvis serverens landestandard for Finance and Operations-forekomsten er defineret som <strong>EN-US</strong>, returnerer <strong>TEXT (NOW ())</strong> den aktuelle Finance and Operations-sessionsdato, 12/17/2015 som tekststrengen <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> returnerer <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (streng 1, streng 2[, streng 3, ...])</td>
<td>Returner den angivne streng, som er formateret ved at erstatte alle forekomster af <strong>%N</strong> med det <em>n</em>te argument. Argumenterne er strenge. Hvis et argument ikke er angivet for en parameter, bliver parameteren returneret som <strong>&quot;%N&quot;</strong> i strengen. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>I dette eksempel på <strong>PaymentModel</strong>-datakilden returneres listen over kundeposter via <strong>Customer</strong>-komponenten og behandlingens datoværdi via <strong>ProcessingDate</strong>-feltet. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> Datakilden <strong>PaymentModel</strong> i ER-format er designet til at generere en elektronisk fil til de valgte debitorer og er valgt som en datakilde og styrer procesforløbet. En undtagelse opstår for slutbrugerne, når en bestemt debitor er spærret for den dato, når rapporten behandles. Den formel, der er udviklet til denne type behandlingskontrol, kan bruge følgende ressourcer:
<ul>
<li>Finance and Operations-label SYS70894, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong> &quot;Nothing to print&quot;</li>
<li><strong>For det danske sprog:</strong> &quot;Intet at udskrive&quot;</li>
</ul></li>
<li>Finance and Operations-label SYS18389, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong> &quot;Customer %1 is stopped for %2&quot;.</li>
<li><strong>For det danske sprog:</strong> &quot;Debitor '%1' er spærret for %2.&quot;</li>
</ul></li>
</ul>
Her er den formel, der kan udvikles: FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)). Hvis en rapport er behandlet for <strong>debitoren Litware Retail</strong> den 17. december 2015 i den <strong>amerikanske</strong> kultur og på det <strong>amerikanske</strong> sprog, vil denne formel returnere følgende tekst, som kan præsenteres som en meddelelse til slutbrugeren: &quot;Nothing to print. Customer Litware Retail is stopped for 12/17/2015.&quot; Hvis den samme rapport behandles den 17. december 2015 for <strong>Kunden Litware Retail</strong> med <strong>dansk</strong> kultur og <strong>dansk</strong> sprog, returnerer formlen følgende tekst, der bruger et andet datoformat: &quot;Intet at udskrive. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Bemærk!</strong> Følgende syntaks anvendes i ER-formler for etiketter:
<ul>
<li><strong>For etiketter fra Finance and Operations-ressourcer:</strong> <strong>@&quot;X&quot;</strong>, hvor X er etiket-id'et i applikationsobjekttræet (AOT)</li>
<li><strong>For etiketter, der er placeret i ER-konfigurationer:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, hvor X er etiket-id i ER-konfigurationen</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (tal, format)</td>
<td>Returner strenggengivelsen af det angivne tal i det angivne format. (Oplysninger om understøttede formater finder du under <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standard</a> og <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">brugerdefinerede</a>.) Konteksten, som denne funktion køres i, bestemmer den kultur, der bruges til at formatere tal.</td>
<td>For den amerikanske kultur vil <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong> returnere <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> returnerer <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (tal, sprog, valuta, udskriv valutanavn, decimaltegn)</td>
<td>Returnerer tallet skrevet helt ud (konverteret) til tekststrenge i det definerede sprog. Sprogkoden er valgfri: Når den er defineret som en tom streng, bruges den løbende sammenhængs sprogkode (defineret for en genererende mappe eller fil) i stedet. Valutakoden er valgfri. Når den er defineret som en tom streng, bruges firmavalutaen. Bemærk, at <strong>Udskriv valutanavn</strong>-parameter og <strong>Decimaltegn</strong>-parameter kun analyseres for følgende sprogkoder: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Bemærk, at <strong>Udskriv valutanavn</strong>-parameter kun analyseres for Finance and Operations-virksomheder med landets kontekst, der understøtter valutaafvigelse.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) returnerer "One Thousand Two Hundred Thirty Four and 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) returnerer “Sto dwadzieścia” NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) returnerer “Сто двадцать евро 21 евроцент”</td>
</tr>
<tr class="odd">
<td>PADLEFT (streng, længde, margentegn)</td>
<td>Returnerer en streng af en angivet længde, hvor begyndelsen af den aktuelle streng er udfyldt med de angivne tegn.</td>
<td>PADLEFT ("1234", 10, " ") returnerer tekststrengen "      1234"</td>
</tr>
<tr class="even">
<td>TRIM (streng)</td>
<td>Returnerer den givne tekst efter afkortning af foranstillede og efterstillede mellemrum og fjerner flere mellemrum mellem ord. </td>
<td><strong>TRIM ("Teksteksempel")</strong> returnerer <strong>"Teksteksempel".</strong></td>
=======
<td>GETENUMVALUEBYNAME (kildesti til fasttekstdata, labeltekst til fasttekstværdi)</td>
<td>Returnerer en værdi for en bestemt kilde til fasttekstdata efter angivet tekst i denne fasttekstlabel.</td>
<td>Følgende eksempel viser fastteksten ReportDirection introduceret i en datamodel. Bemærk, at der er defineret etiketter for optællingsværdier.
Følgende eksempler viser:
<ul><li>Modelfastteksten <strong>ReportDirection</strong>, der er indsat i en rapport som en datakilde <strong>$Direction</strong>.</li>
<li>ER-udtrykket <strong>$IsArrivals</strong>, der er designet til at bruge modelfasttekst som parameter for denne funktion. Værdien af dette udtryk er <strong>TRUE</strong></li></ul></td>
</tr>
</tbody>
</table>

**Datakonverteringsfunktioner**

| Funktion             | Betegnelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| TEXT (input) | Returner det angivne input, som er konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard til den aktuelle forekomst af Finance and Operations.
For værdier af den reelle type er strengkonverteringen begrænset til to decimaler.| Hvis serverens landestandard for Finance and Operations-forekomsten er defineret som **EN-US, TEXT (NOW ())**, returneres den aktuelle Finance and Operations-sessionsdato, 12/17/2015, som tekststrengen **12/17/2015 07:59:23 AM**.
**TEXT (1/3) returnerer "0.33"**. |
| QRCODE (streng) | Returnerer et QR-kodebillede i det binære base64-format for en given streng. | **QRCODE ("teksteksempel")** returnerer **U2FtcGxlIHRleHQ =**.   |

### <a name="data-collection-functions"></a>Dataindsamlingsfunktioner

| Funktion             | Betegnelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATELEMENTNAME () | Returnerer navnet på det aktuelle formats element. Returnerer en tom streng, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.| Se opgaveguiden **Bruge ER-data af formatoutput til optælling og sammenlægning** (en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger**) til at lære mere om brugen af disse funktioner. |
| SUMIFS (nøglestreng for sammenlægning, kriterieinterval 1-streng, kriterieværdi 1-streng \[,kriterieinterval 2-streng, kriterieværdi 2-streng, …\]) |Returnerer summen af værdierne i noder (med navn, der er defineret som en nøgle) af XML, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra. |            |
| SUMIF (nøglestreng for sammenlægning, kriterieintervalstreng, kriterieværdistreng) | Returnerer summen af værdierne i noder (med navn, der er defineret som en nøgle) af XML, som er blevet indsamlet under denne kørsel af format, og som opfylder den angivne betingelse (interval og værdi). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.|           |
| COUNTIFS (kriterieinterval 1-streng, kriterieværdi 1-streng \[, kriterieinterval 2-streng, kriterieværdi 2-streng, ...\]]) | Returnerer antal XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.|     |
| COUNTIF (kriterieintervalstreng, kriterieværdistreng) | Returnerer antal XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder den angivne betingelse (interval og værdi). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.|          |
| COLLECTEDLIST (kriterieinterval 1-streng, kriterieværdi 1-streng \[, kriterieinterval 2-streng, kriterieværdi 2-streng, ...\]) | Returnerer en liste over værdier af XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval og værdi). Returnerer en tom liste, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.|               |   




### <a name="other-business-domainspecific-functions"></a>Andre (forretningsdomænespecifikke) funktioner

| Funktion                                                                         | Betegnelse                                                                                                                                                                                                                                                        | Eksempel                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (beløb, kildevaluta, målvaluta, dato, firma)        | Konverter det angivne pengebeløb fra kildevalutaen til målvalutaen ved hjælp af indstillingerne for det angivne Finance and Operations-firma på den angivne dato.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** returnerer, hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for DEMF-firmaet.                                                                                                                                  |
| ROUNDAMOUNT (tal, decimaler, afrundingsregel)                                       | Afrund det angivne beløb i henhold til den angivne afrundingsregel og det angivne antal decimaler. **Bemærk:** Afrundingsreglen skal angives som en værdi af Finance and Operations **RoundOffType**-fasttekst.                          | Hvis **model.RoundOff**-parameter er indstillet til ****Downward****, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere værdien **1000.78**. Hvis **model.RoundOff**-parameter er indstillet til enten **Normal** eller **Oprunding**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere værdien **1000.79**. |
| CURCredRef (cifre)                                                              | Returner en kreditors reference, baseret på cifrene i det angivne fakturanummer.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** returnerer **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (cifre)                                                                 | Returner en kreditors reference som et MOD97-udtryk, baseret på cifrene i det angivne fakturanummer.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** returnerer **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (cifre)                                                              | Returner en ISO-kreditors reference, baseret på cifrene og bogstaverne i det angivne fakturanummer. **Bemærk:** For at eliminere symboler fra alfabeter, der ikke er ISO-kompatible, skal inputparameteren oversættes, før den videresendes til denne funktion. | **ISOCredRef ("VEND-200002")** returnerer **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (streng, tal)                                  | Hent yderligere økonomisk dimensions-id Dimensioner er repræsenteret i denne streng som id'er, der er adskilt af kommaer. Tal definerer nummerseriekode til den ønskede dimension i denne streng.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) returnerer “CC”                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Returnerer tekstrepræsentation af en kode for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.                                                                                                                                                                                                                    | **GETCURRENTCOMPANY ()** returnerer **USMF** for en bruger, der er logget på Finance and Operations-firmaet **Contoso Entertainment System USA**.                                                                                                                                                                                                                                                                                                              |
| CH\_BANK\_MOD\_10 (cifre)                                                       | Returnerer en kreditors reference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") returnerer 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (anlægsaktivkode, værdimodelkode, startdato, slutdato)               | Returnerer den klargjorte datacontainer med anlægsaktivbeløb for en periode.                                                                                                                                                                                         | FA\_SUM ("COMP 000001", “Aktuel”, Dato1, Dato2) returnerer den forberedte datacontainer for anlægsaktivet "COMP-000001" med værdimodellen "Aktuel" i en periode fra Dato1 til Dato2.                                                                                                                        |
| FA\_BALANCE (anlægsaktivkode, værdimodelkode, rapporteringsår, rapporteringsdato) | Returnerer den klargjorte datacontainer med saldi for anlægsaktiver. Rapporteringsår skal angives som en værdi af Finance and Operations-fastteksten **AssetYear**.                                                                                           | FA\_SUM ("COMP 000001", "Aktuel", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) returnerer den forberedte datacontainer af saldi for anlægsaktivet "COMP-000001" med værdimodellen "Aktuel" på den aktuelle 365 for Finance and Operations-sessionsdato.                                                                |
| TABLENAME2ID (streng)                                                       | Returnerer heltalsrepræsentation af et tabel-Id for et bestemt tabelnavn.                                                                                                                                                                      | **TABLENAME2ID ("Intrastat")** returnerer **1510**.                                                                                                                                                                                                                                                                   |
| ISVALIDCHARACTERISO7064 (streng)                                                       | Returnerer en boolesk værdi **TRUE**, når en given streng repræsenterer et gyldigt internationale bankkontonummer (IBAN). Returnerer ellers den booleske værdi **FALSE**.                                                                                                                                                                      | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")** returnerer **TRUE**. **ISVALIDCHARACTERISO7064 ("AT61")** returnerer **FALSE**.                                                                                                                                                                                                                                                                   |

### <a name="functions-list-extension"></a>Funktionslistens udvidelse

ER understøtter muligheden for at udvide listen over funktioner, der bruges i ER-udtryk. Der kræves en vis teknisk indsats for at gøre dette. Yderligere oplysninger finder du under [Udvidelse af listen over elektroniske rapporteringsfunktioner](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Se også
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Udvide listen over elektroniske rapporteringsfunktioner (ER)](general-electronic-reporting-formulas-list-extension.md)




