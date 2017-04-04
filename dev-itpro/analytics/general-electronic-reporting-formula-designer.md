---
title: Formeldesigner i elektronisk rapportering
description: "Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge Microsoft Excel-lignende formler for datatransformation, der opfylder kravene til dette dokuments udførelse og formatering. Forskellige typer funktioner understøttes - tekst, dato og klokkeslæt, matematiske, logiske samt oplysninger, konverteringen af datatypen og andre (domæne-specifikke funktioner i virksomheden)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Formeldesigner i elektronisk rapportering

Dette emne beskriver, hvordan du bruger formeldesigneren i elektronisk rapportering (ER). Når du designer et format til et bestemt elektronisk dokument i ER, kan du bruge Microsoft Excel-lignende formler for datatransformation, der opfylder kravene til dette dokuments udførelse og formatering. Forskellige typer funktioner understøttes - tekst, dato og klokkeslæt, matematiske, logiske samt oplysninger, konverteringen af datatypen og andre (domæne-specifikke funktioner i virksomheden).

<a name="formula-designer-overview"></a>Oversigt over formeldesigner
-------------------------

Elektronisk rapportering (ER) understøtter formeldesigneren. Derfor kan du på designtidspunktet konfigurere udtryk, der kan bruges til følgende opgaver under kørsel:

-   Transformere data, der er modtaget fra en Microsoft Dynamics 365 for Operations-database, der skal udfyldes på en ER-datamodel, der er designet til at være datakilde til ER-formater (filtrering, gruppering, konvertering af datatyper osv.).
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

-   Fra Dynamics 365 for Operations-datakilder og kørselsparametre til ER-datamodel.
-   Fra en ER-datamodel til et ER-format.
-   Fra Dynamics 365 for Operations-datakilder og kørselsparametre til ER-format.

I følgende illustration vises et udtryk af denne type design. I dette eksempel returnerer udtrykket værdien af feltet **Intrastat.AmountMST** i Dynamics 365 for Operations-tabellen **Intrastat**, når værdien er blevet afrundet til to decimaler. [![billede-udtryk-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) i følgende illustration vises, hvordan du kan bruge et udtryk af denne type. I dette eksempel er resultatet af udtrykket designet udfyldes i de **Transaction.InvoicedAmount** komponent af det **skat rapporteringsmodellen** datamodel. [![billede-udtryk-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) på kørselstidspunktet, udviklet formlen **ROUND (Intrastat.AmountMST 2)**, afrundes værdien af den **AmountMST** felt for hver post i den **Intrastat** tabel med to decimaler, og udfylde den afrundede værdi til den **Transaction.InvoicedAmount** komponent af den **skatteindberetning** datamodel.

### <a name="data-formatting"></a>Dataformatering

ER-formeldesigneren kan bruges til at definere et udtryk, der formaterer data, der er modtaget fra datakilder, så data kan sendes som en del af det genererende elektroniske dokument. Hvis der er formatering, der skal anvendes som en typisk regel, der skal genbruges til et format, kan du introducere formateringen én gang i en formatkonfiguration som en navngivet transformering, der har et formateringsudtryk. Senere kan denne navngivne transformation sammenkædes med mange formatkomponenter, hvis output skal formateres i henhold til det oprettede udtryk. I følgende illustration vises designet af en transformation af denne type. Dette eksempel på **TrimmedString**-transformation tager indgående data i **Streng**-datatypen og afkorter foranstillede og efterstillede mellemrum, når den returnerer en strengværdi. [![billede-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) i følgende illustration vises, hvordan du kan bruge en transformering af denne type. I dette eksempel finder du flere formatkomponenter, som sender tekst som output til det genererende elektroniske dokument på kørselstidspunktet til **TrimmedString**-transformationen efter navn. [![billede-transformation-forbrug](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) når format-komponenter finder du den ** TrimmedString ** transformation (for eksempel det **partyName** komponent i den foregående illustration) dette sender tekst som output til at generere dokumentet. Teksten indeholder ikke foranstillede eller efterstillede mellemrum. Hvis du har en formatering, der skal anvendes individuelt, kan den indføres som et individuelt udtryk for binding af en bestemt formatkomponent. I følgende illustration vises et udtryk af denne type. I dette eksempel er **partyType**-formatkomponenten bundet til datakilden via et udtryk, der konverterer indgående data fra feltet **Model.Company.RegistrationType** i datakilden til stor bogstavtekst og sender teksten som output til det elektroniske dokument. [![billede binding med formlen](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Kontrol af procesforløb

ER-formeldesigneren kan bruges til at definere udtryk, der styrer procesforløbet under generering af dokumenter. Du kan gøre følgende:

-   Definer betingelser, der bestemmer, hvornår en proces til oprettelse af dokumentet skal stoppes.
-   Angiv udtryk, der opretter enten meddelelser til slutbrugeren om stoppede processer eller udløser en kørselslogbesked om, at processen fortsætter med oprettelse af rapporter.
-   Angiv filnavne til oprettelse af dokumenter, og kontrollér betingelserne for deres oprettelse.

Hver regel i kontrol af procesforløb udformet som en enkelt validering. I følgende illustration vises en validering af denne type. Her er en forklaring af konfigurationen i dette eksempel:

-   Valideringen evalueres, når **INSTAT**-noden oprettes i den genererende XML-fil.
-   Hvis listen over transaktioner er tom, stopper valideringen kørselsprocessen og returnerer **FALSE**.
-   Valideringen returnerer en fejlmeddelelse, der indeholder teksten til etiketten for SYS70894 på brugerens foretrukne sprog.

[![Validering af billede](./media/picture-validation.jpg)](./media/picture-validation.jpg) det ER formlen designer kan også bruges til at angive et filnavn til en generere elektroniske dokument og styre processen til oprettelse af filen. I følgende illustration vises designet af en kontrol af procesforløb af denne type. Her er en forklaring af konfigurationen i dette eksempel:

-   listen over poster fra datakilden **model.Intrastat-** opdeles i batches, der indeholder op til 1.000 poster hver.
-   Output opretter en zip-fil, der indeholder en fil i XML-format for hver batch, der blev oprettet.
-   Et udtryk returnerer et filnavn til generering af elektroniske dokumenter ved at sammenkæde filnavnet og filtypenavnet. For den anden batch og alle efterfølgende batches indeholder filnavnet batch-ID som et suffiks.
-   Et udtryk aktiverer (returnerer **TRUE**) processen med en filoprettelse for de eneste batches, der indeholder mindst én post.

[![kontrolelementet billede-fil](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Grundlæggende syntaks

ER udtryk kan indeholde én eller flere af følgende elementer:

-   Konstanter
-   Operatorer
-   Referencer
-   Stier
-   Funktioner

#### <a name="constants"></a>Konstanter

Du kan bruge tekst og numeriske konstanter (værdier, der ikke beregnes) i udformningen af udtryk. For eksempel udtryk ** værdi ("100") + 20 ** bruges numeriske konstant 20 og streng konstant "100", og returnerer en numerisk værdi **120**. Escape-sekvenser understøttes i ER-formeldesigneren, så du kan angive den del af udtryksstrengen, der skal håndteres anderledes. F.eks. returnerer udtrykket **"Leo Tolstoy ""Krig og fred"" Bind 1"** tekststrengen **Leo Tolstoy "Krig og fred" Bind 1**.

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

Den rækkefølge, som delene af et sammensat udtryk evalueres i, er vigtig. For eksempel er resultatet af udtrykket ** 1 + 4 / 2 ** varierer, afhængigt af om handlingen tilsætning, eller division operationen udføres først. Du kan bruge parenteser til eksplicit at angive, hvordan et udtryk evalueres. Du kan for eksempel for at angive, at addition skal udføres først, ændre det foregående udtryk til **(1 + 4) / 2**. Hvis rækkefølgen af operationer, der skal udføres i et udtryk, ikke er udtrykkeligt defineret, er rækkefølgen baseret på standardrangfølgen, der er tildelt de understøttede operatorer. Følgende tabeller viser operatorerne og den prioritet, der er tildelt hver enkelt. Operatorer, der har højere prioritet (for eksempel 7), evalueres før operatorer, der har lavere prioritet (f.eks. 1).

| Prioritering | Operatorer      | Syntaks                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                    |
| 6          | Medlemsadgang  | … . …                                                    |
| 5          | Funktionskald  | … ( … )                                                  |
| 4          | Multiplikation | … \* … … / …                                             |
| 3          | Tilføjelse       | … + … … - …                                              |
| 2          | Sammenligning     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Separation     | … , …                                                    |

Operatorer på samme linje har samme prioritet. Hvis et udtryk indeholder mere end én af disse operatorer, skal det evalueres de fra venstre mod højre. For eksempel udtrykket **1 + 6 / 2 \*3 &gt;5** returnerer **true**. Vi anbefaler, at du bruger parenteser til at angive den ønskede rækkefølge i evalueringen af udtryk, så det bliver nemmere at læse og vedligeholde udtrykkene eksplicit.

#### <a name="references"></a>Referencer

Alle datakilder for den aktuelle ER-komponent (en model eller et format), der er tilgængelige under designet af et udtryk, kan bruges som navngivne referencer. For eksempel indeholder den aktuelle ER-datamodel datakilden **ReportingDate**, der returnerer værdien af datatypen **DATETIME**. Denne værdi i generere dokumentet skal formateres korrekt, kan du referere til datakilden i udtrykket på følgende måde: **DATETIMEFORMAT (ReportingDate, "dd-MM-ÅÅÅÅ")** alle tegn i navnet på en selvrefererende datakilde, der ikke repræsenterer et bogstav i alfabetet skal indledes med et enkelt anførselstegn ('). Hvis navnet på en selvrefererende datakilde indeholder mindst ét symbol, der ikke repræsenterer et bogstav i alfabetet (for eksempel, tegnsætningstegn eller andre skriftlige symboler), skal navnet stå i anførselstegn. Her er nogle eksempler:

-   Datakilden **Today’s date & time** skal refereres til i ER-udtryk som følger: **'Today''s date & time’**
-   Metoden **name()** i datakilden **Customers** skal refereres til i ER-udtryk som følger: **Customers.'name()'**

#### <a name="path"></a>Sti

Når et udtryk refererer til en struktureret datakilde, kan du bruge definitionen af stien til at vælge et bestemt primitivt element i datakilden. Tegnet en prik (.) bruges til at adskille de enkelte elementer i en struktureret datakilde. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, der returnerer listen med poster. Poststrukturen** InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, der returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan defor være udformet således: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funktioner

Det næste afsnit beskriver de funktioner, der kan bruges i ER-udtryk. Alle datakilder i udtrykskonteksten (aktuel ER-datamodel eller ER-format) samt konstanter kan bruges som parametre til opkaldsfunktioner i henhold til listen over opkaldsfunktionsargumenter. For eksempel indeholder den aktuelle ER-datamodel datakilden **InvoiceTransactions**, der returnerer listen med poster. Poststrukturen** InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, der returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan derfor være udformet således ved at bruge den indbyggede ER-afrundingsfunktion: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Understøttede funktioner
I følgende tabel beskrives de datamanipulationsfunktioner, du kan bruge til at designe ER-datamodeller og ER-rapporter. Denne liste over funktioner er ikke fast og kan udvides af udviklere. Du kan se listen over funktioner, du kan bruge, i ruden med funktioner i ER-formeldesigneren.

### <a name="date-and-time-functions"></a>Dato- og klokkeslætsfunktioner

| Funktion                                   | Beskrivelse                                                                                                                                                                                                                                                                                                                                                      | Eksempel                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datetime, dage)                   | Føj det angivne antal dage til den angivne datetime-værdi.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW() 7)** returnerer datoen og klokkeslættet syv dage ud i fremtiden.                                                                                                                                                                                                                            |
| DATETODATETIME (dato)                      | Konverter den angivne datoværdi til en datetime-værdi.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. ' getCurrentDate()')** returnerer den aktuelle Dynamics 365 i forbindelse med sessionsdatoen, 12/24/2015, som **24/12/2015 12:00:00 AM**. I dette eksempel er **CompInfo** en datakilde til ER af typen **Dynamics 365 for Operations/tabel**, der refererer til tabellen CompanyInfo. |
| NOW ()                                     | Returner aktuel Dynamics 365 for Operations-dato og -klokkeslæt på programserver som en dato- og klokkeslætsværdi.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Returner aktuel Dynamics 365 for Operations-serverdato som en datoværdi.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Returner en **null**-datoværdi.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Returner en **null**-datetime-værdi.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datetime, format)          | Konverter den angivne datetime-værdi til en streng i det angivne format. (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** returnerer den aktuelle Dynamics 365 for Operations-programserverdato, 12/24/2015, som **"24-12-2015"**, i overensstemmelse med det angivne brugerdefinerede format.                                                                                                          |
| DATETIMEFORMAT (datetime, format, kultur) | Konverter den angivne datetime-værdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** returnerer den aktuelle Dynamics 365 for Operations-programserverdato, 12/24/2015, som **"24.12.2015"**, i henhold til den valgte tyske kultur.                                                                                                             |
| SESSIONTODAY ()                            | Returnerer aktuel Dynamics 365 for Operations-sessionsdato som en datoværdi.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Returnerer aktuel Dynamics 365 for Operations-sessionsdato og -klokkeslæt som en dato- og klokkeslætsværdi.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (dato, format)                  | Returnerer strengværdi af dato ved brug af det angivne format.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** returnerer den aktuelle Dynamics 365 for Operations-sessionsdato, 12/24/2015, som "**24-12-2015**" i overensstemmelse med det angivne brugerdefinerede format.                                                                                                                      |
| DATEFORMAT (dato, format, kultur)         | Konverter den angivne datoværdi til en streng i det angivne format og den angivne [kultur](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Oplysninger om understøttede formater finder du under [standard](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) og [brugerdefineret](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** returnerer den aktuelle Dynamics 365 for Operations-sessionsdato, 12/24/2015, som **"24.12.2015"** i henhold til den valgte tyske kultur.                                                                                                                       |

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
<td><strong>OPDEL (&quot;abcd&quot;, 3)</strong> returnerer en ny liste, der består af to poster, der har en <strong>streng</strong> felt. Feltet i den første post, der indeholder teksten, <strong>&quot;abc&quot;</strong>, og feltet i den anden post, der indeholder teksten, <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (liste, antal)</td>
<td>Opdel den angivne liste i batches, som hver især indeholder det angivne antal poster. Returner resultatet som en ny liste over batches, der indeholder følgende elementer:
<ul>
<li>Batches som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle batchnummer (<strong>Batchnummer-</strong>komponent)</li>
</ul></td>
<td>I følgende eksempel bliver <strong>Linjer</strong>-datakilde oprettet som en postliste med tre poster, der er opdelt i batches, der hver især indeholder op til to poster. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Viser designet format layoutet, hvor bindinger til de <strong>linjer</strong> datakilden er oprettet for at generere output i XML-format, som præsenterer enkelte noder for hvert parti og posterne i den. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Følgende er resultatet af at køre formatet designet. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (post 1 [, post 2,...])</td>
<td>Returner en ny liste, der oprettes ud fra de angivne argumenter.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> returnerer en tom post, hvor listen over felter indeholder alle felterne i postlisterne <strong>MainData</strong> og <strong>OtherData</strong>.</td>
</tr>
<tr class="even">
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Returner en ny forenet liste, der oprettes ud fra lister med de angivne argumenter.</td>
<td><strong>LISTJOIN (OPDELE (&quot;abc&quot;, 1), OPDELTE (&quot;def&quot;, 1))</strong> returnerer listen over seks poster, hvor en i den <strong>streng</strong> datatype, der indeholder enkelt bogstaver.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (liste)</td>
<td>Returnerer <strong>TRUE</strong>, hvis den angivne liste ikke indeholder nogen elementer. Ellers returneres <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (liste)</td>
<td>Returner en tom liste ved hjælp af den angivne liste som kilde til listestrukturen.</td>
<td><strong>EMPTYLIST (OPDELE (&quot;abc&quot;, 1))</strong> returnerer en ny tom liste, der har samme struktur som i den liste, der er returneret af <strong>OPDELE</strong> funktion.</td>
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
<td>Hvis du angiver <strong>opdelt (&quot;abcdef&quot;, 2)</strong> som datakilde (DS), <strong>antal (ALLITEMS (DS. Værdi))</strong> returnerer <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (liste [udtryk 1, udtryk, 2, ...])</td>
<td>Returner den angivne liste sorteret efter de angivne argumenter, der kan defineres som udtryk.</td>
<td>Når <strong>Vendor </strong>er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong> ORDERBY (Vendors, Vendors.'name()')</strong> returnere en liste over kreditorer, der er sorteret efter navn i stigende rækkefølge.</td>
</tr>
<tr class="even">
<td>REVERSE (liste)</td>
<td>Returner den angivne liste i omvendt rækkefølge.</td>
<td>Når <strong>Vendor </strong>er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong> returnere en liste over kreditorer, der er sorteret efter navn i faldende rækkefølge.</td>
</tr>
<tr class="odd">
<td>WHERE (liste, betingelse)</td>
<td>Returner den angivne liste, der er filtreret efter den angivne betingelse. I modsætning til <strong>FILTER</strong>-funktionen, den bliver den angivne betingelse anvendt på listen i hukommelsen.</td>
<td>Når <strong>leverandør</strong> er konfigureret som en ER-datakilde, der henviser til tabellen VendTable <strong>hvor (kreditorer, Vendors.VendGroup = &quot;40&quot;)</strong> returnerer en liste over kreditorer, der tilhører kreditorgruppen 40.</td>
</tr>
<tr class="even">
<td>ENUMERATE (liste)</td>
<td>Returner en ny liste, der består af optalte poster af den angivne liste og viser følgende elementer:
<ul>
<li>Angivne listeposter som almindelige lister (<strong>Værdi-</strong>komponent)</li>
<li>Det aktuelle postindeks (<strong>Tal-</strong>komponent)</li>
</ul></td>
<td>I følgende eksempel er <strong>Enumerated</strong>-datakilden oprettet som en fasttekstliste over kreditorposter fra <strong>Vendors</strong>-datakilden, der henviser til <strong>VendTable</strong>-tabellen. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Her er formatet, hvor der oprettes databindinger til at generere output i XML-format, som præsenterer enkelte kreditorer som optalt noder. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Dette er resultatet af at køre formatet designet. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (liste)</td>
<td>Returner antal poster på den angivne liste, hvis listen ikke er tom. Ellers returneres <strong>0</strong> (nul).</td>
<td><strong>COUNT (OPDELE (&quot;abcd&quot;, 3))</strong> returnerer <strong>2</strong>, da den <strong>OPDELE</strong> funktion opretter en liste, der består af to poster.</td>
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
</ul><ph id="t1">
< en href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> i følgende eksempel vises de elementer, der ER format, der er bundet til datakilden af post på listetype, som blev oprettet ved hjælp af funktionen LISTOFFIELDS. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Er resultatet af kørslen designet format. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Note:</strong> Translated tekst til etiketter og beskrivelser er udfyldt til ER format-output i overensstemmelse med de sprogindstillinger, der er konfigureret til overordnede fil og mappe formateringselementer.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (liste, feltnavn, afgrænser)</td>
<td>Returnerer strengen sammenføjede værdier for et felt fra en liste, der er adskilt med det valgte afgrænsningstegn.</td>
<td>Hvis du har angivet SPLIT("abc", 1) som en datakilde-DS, vil udtrykket STRINGJOIN (DS, DS.Value, ":") returnere "a:b:c"</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (liste, grænseværdi. grænsekilde)</td>
<td>Opdeler den angivne liste i en ny liste over underordnede lister og returnerer resultatet i indholdet af listen over poster. Parameteren for grænseværdi angiver værdien af grænsen for at opdele den oprindelige liste. Parameteren for grænsekilde angiver det trin, hvor den samlede sum forøges. Grænsen anvendes ikke på et enkelt element på listen, når grænsekilden overskrider den angivne grænse.</td>
<td>Følgende eksempel viser formatet, der bruger datakilder. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Dette er resultatet format udførelsen, der præsenterer den flade liste med råvare elementer. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>i følgende eksempel vises det samme format, der blev reguleret for at vise listen over råvare elementer i bundter, når et parti skal indeholde varer med den samlede vægt, der ikke bør overstige grænsen på 9. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Er resultatet af kørslen regulerede format. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Bemærk:</strong> grænsen anvendes ikke på det sidste element på listen oprindelse, som værdien af den tilladte kilde (vægt) (11) overskrider den angivne grænse (9). Brug enten funktionen <strong>WHERE</strong> eller <strong>Aktiveret</strong>-udtrykket for det tilsvarende formatelement for at ignorere (springe over) underordnede lister under oprettelsen af rapporten (om nødvendigt).</td>
</tr>
<tr class="odd">
<td>FILTER (liste, betingelse)</td>
<td>Returnerer den angivne liste, der er filtreret efter den angivne betingelse ved at ændre forespørgslen. I modsætning til funktionen <strong>WHERE</strong>, anvendes den angivne betingelse på databaseniveau til en ER-datakilde af typen tabelposter.</td>
<td>FILTER (kreditorer, Vendors.VendGroup = &quot;40&quot;) returnerer listen over kun kreditorer, der tilhører gruppen af leverandører "40" Når <strong>leverandør</strong> er konfigureret som ER datakilde, der henviser til den <strong>VendTable</strong> tabel</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Logiske funktioner

| Funktion                                                                                | Betegnelse                                                                                                                                                                                                                                                                     | Eksempel                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SAG (udtryk, valgmulighed 1, resultat 1 \[, 2, skal du følge 2\] ... \[, standard resultat\]) | Evaluer den angivne udtryksværdi mod de angivne alternative valgmuligheder. Returner resultatet af den valgmulighed, der er lig med værdien af udtrykket. Ellers returneres det eventuelt angivne standardresultat (den sidste parameter, der ikke indledes med en valgmulighed). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "VINTER", "11", "VINTER", "12", "VINTER", "")** returnerer strengen **"VINTER"**, når den aktuelle Dynamics 365 for Operations-sessionsdato er mellem oktober og december. Ellers returneres en tom streng. |
| IF (betingelse, værdi 1, værdi 2)                                                        | Returner den angivne værdi 1, når den angivne betingelse er opfyldt. Ellers Returner værdien 2. Hvis værdi 1 og 2 er poster eller registrere lister, har resultatet kun de felter, der findes på begge lister.                                                                     | **IF (1 = 2, "betingelse er opfyldt", "betingelse er ikke opfyldt")** returnerer strengen **"betingelse er ikke opfyldt"**.                                                                                                                                                      |
| NOT (betingelse)                                                                         | Returner den omvendte logiske værdi af den angivne betingelse.                                                                                                                                                                                                                   | **NOT (TRUE)** returnerer **FALSE**.                                                                                                                                                                                                                            |
| OG (betingelse 1\[, betingelse 2... \])                                                 | Returnerer **TRUE**, hvis *alle *angivne betingelser er sande. Ellers returneres **FALSE**.                                                                                                                                                                                            | **AND (1=1, "a"="a")** returnerer **TRUE**. **AND (1=2, "a"="a")** returnerer **FALSE**.                                                                                                                                                                           |
| ELLER (betingelse 1\[, betingelse 2... \])                                                  | Returnerer **FALSE**, hvis *alle *angivne betingelser er falske. Returnerer **TRUE**, hvis *en af *de angivne betingelser er sande.                                                                                                                                                                 | **OR (1=2, "a"="a")** returnerer **TRUE**.                                                                                                                                                                                                                      |

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
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> returnerer værdien <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (streng)</td>
<td>Konverter den angivne streng til et tal. Komma og punktum (.) betragtes som decimalseparator og en indledende bindestreg (-) bruges som negativt fortegn. Udløs en undtagelse, hvis der findes andre ikke-numeriske tegn i den angivne streng.</td>
<td><strong>VÆRDI (&quot;1 234,56&quot;)</strong> medfører en undtagelse.</td>
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

### <a name="record-functions"></a>Postfunktioner

| Funktion             | Beskrivelse                                                                                                                                                                                                                                     | Eksempel                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (liste) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post. **Bemærk: **Denne funktion er forældet. Brug **EMPTYRECORD** i stedet.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen. |
| EMPTYRECORD (post) | Returner en **null**-post, der har samme struktur som den angivne postliste eller post. **Bemærk:** A **null** post er en post, hvor alle felter har en tom værdi (**0**\[nul\] for tal, en tom streng for strenge, og så videre). | **EMPTYRECORD (SPLIT ("abc", 1))** returnerer en ny tom post, der har samme struktur som den liste, der er returneret af **SPLIT**-funktionen.   |

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
<td><strong>ØVERSTE (&quot;prøve&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (streng)</td>
<td>Returner den angivne streng konverteret til små bogstaver.</td>
<td><strong>LAVERE (&quot;prøve&quot;)</strong> returnerer <strong>&quot;eksempel&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra starten af den angivne streng.</td>
<td><strong>VENSTRE (&quot;prøve&quot;, 3)</strong> returnerer <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (streng, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra slutningen af den angivne streng.</td>
<td><strong>HØJRE (&quot;prøve&quot;, 3)</strong> returnerer <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (streng, startposition, antallet af tegn)</td>
<td>Returner det angivne antal tegn fra startpositionen i den angivne streng.</td>
<td><strong>MID (&quot;prøve&quot;, 2, 3)</strong> returnerer <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (streng)</td>
<td>Returner antallet af tegn i den angivne streng.</td>
<td><strong>LEN (&quot;prøve&quot;)</strong> returnerer <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (tal)</td>
<td>Returner den streng af tegn, der refereres til af det angivne Unicode-tal.</td>
<td><strong>CHAR (255)</strong> returnerer <strong>&quot;ÿ&quot;</strong>. <strong>Bemærk:</strong> Den returnerede streng afhænger af den kodning, der er valgt i det overordnede FILE-formatelement. Listen over understøttede kodninger findes i emnet <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodningsklasse</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (streng 1 [, streng 2, ...])</td>
<td>Returner alle angivne tekststrenge, der er sat ind i én streng.</td>
<td><strong>SAMMENKÆDE (&quot;abc&quot;, &quot;def&quot;)</strong> returnerer <strong>&quot;abcdef&quot;</strong>. <strong>Bemærk:</strong> udtrykket <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> returnerer også <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (streng, mønster, erstatning)</td>
<td>Returner den angivne streng, hvor alle forekomster af tegn i det angivne strengmønster erstattes med tegn på den tilsvarende position i den angivne erstatningsstreng.</td>
<td><strong>Oversæt (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (streng, mønster, erstatning, almindeligt udtryksflag)</td>
<td>Når det angivne udtryksflag er <strong>true</strong>, returneres den angivne streng, som er blevet ændret ved at anvende det almindelige udtryk, der er angivet som et mønsterargument for denne funktion. Dette udtryk bruges til at søge efter tegn, der skal erstattes. Tegn i det angivne erstatningsargument bruges til at erstatte tegn, der findes. Når det angivne udtryksflag er <strong>false</strong>, fungerer denne funktion ligesom <strong>TRANSLATE</strong>.</td>
<td>  <strong>Erstat (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, SAND)</strong> gælder et regulært udtryk, der fjerner alle ikke-numeriske tegn, symboler og returnerer <strong>&quot;19234564971&quot;</strong>. <strong>Erstat (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, FALSK)</strong> erstatter mønsteret <strong>&quot;cd&quot;</strong> med strengen <strong>&quot;GH&quot;</strong> og returnerer <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (input)</td>
<td>Returner det angivne input, som er konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard til den aktuelle forekomst af 365 for Operations. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>Hvis den Dynamics 365 for operationer forekomst serverens landestandard er defineret som <strong>EN-US</strong>, <strong>tekst (nu ())</strong> returnerer den aktuelle Dynamics 365 i forbindelse med sessionsdatoen, 12/17/2015 som tekststrengen <strong>&quot;17/12/2015 07:59:23 AM&quot;</strong>. <strong>TEKST (1/3)</strong> returnerer <strong>&quot;0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (streng 1, streng 2[, streng 3, ...])</td>
<td>Returner den angivne streng, som er formateret ved at erstatte alle forekomster af <strong>%N</strong> med det <em>n</em>te argument. Argumenterne er strenge. Hvis et argument ikke er angivet for en parameter, parameteren, der returneres som <strong>&quot;%N&quot;</strong> i strengen. For værdier af den <strong>reelle</strong> type er strengkonverteringen begrænset til to decimaler.</td>
<td>I dette eksempel på <strong>PaymentModel</strong>-datakilden returneres listen over kundeposter via <strong>Customer</strong>-komponenten og behandlingens datoværdi via <strong>ProcessingDate</strong>-feltet. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>I formatet ER, der er designet til at generere en elektronisk fil til de valgte debitorer, <strong>PaymentModel</strong> er valgt som en datakilde og styrer procesforløbet. En undtagelse opstår for slutbrugerne, når en bestemt debitor er spærret for den dato, når rapporten behandles. Den formel, der er udviklet til denne type behandlingskontrol, kan bruge følgende ressourcer:
<ul>
<li>Dynamics 365 for Operations-label SYS70894, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong>&quot;intet at udskrive&quot;</li>
<li><strong>For sproget, DE:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Dynamics 365 for Operations-label SYS18389, som har følgende tekst:
<ul>
<li><strong>For det amerikanske sprog:</strong>&quot;debitor %1 er spærret for %2.&quot;</li>
<li><strong>For sproget, DE:</strong>&quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Her er den formel, der kan udvikles: FORMAT (sammenkædning (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model. ProcessingDate, &quot;d&quot;)) Hvis en rapport er udført for den <strong>Litware Detailkunden</strong> på 17 December 2015 i den <strong>EN-US</strong> kultur og <strong>EN-US</strong> sprog, denne formel returnerer følgende tekst, som kan præsenteres som en meddelelse til brugeren: &quot;intet at udskrive. Kunden Litware Retail stoppes 17/12/2015.&quot; Hvis den samme rapport behandles det<strong> Litware Detailkunden</strong> på 17 December 2015 i den <strong>DE</strong> kultur og <strong>DE</strong> sprog, denne formel returnerer følgende tekst, der bruger et andet klokkeslætsformat: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Bemærk: </strong>ER-formler for etiketter anvender følgende syntaks:
<ul>
<li><strong>For etiketter fra Dynamics 365 til operationsressourcer:</strong> <strong>@&quot;X&quot;</strong>, hvor X er label-ID i applikationsobjekttræet (AOT)</li>
<li><strong>For etiketter, der er placeret i konfigurationer ER:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, hvor X er label-ID i konfigurationen, der ER</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (tal, format)</td>
<td>Returner strenggengivelsen af det angivne tal i det angivne format. (Oplysninger om understøttede formater finder du under <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standard</a> og <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">brugerdefinerede</a>.) Denne funktion køres i konteksten bestemmer den kultur, der bruges til at formatere tal.</td>
<td>For den amerikanske kultur, <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> returnerer <strong>&quot;45,00%&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> returnerer <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (tal, sprog, valuta, udskriv valutanavn, decimaltegn)</td>
<td>Returnerer tallet skrevet helt ud (konverteret) til tekststrenge i det definerede sprog. Sprogkoden er valgfri: Når den er defineret som en tom streng, bruges den løbende sammenhængs sprogkode (defineret for en genererende mappe eller fil) i stedet. Valutakoden er valgfri. Når den er defineret som en tom streng, bruges firmavalutaen. Bemærk, at <strong>Udskriv valutanavn</strong>-parameter og <strong>Decimaltegn</strong>-parameter kun analyseres for følgende sprogkoder: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Bemærk, at <strong>Udskriv valutanavn</strong>-parameter kun analyseres for Dynamics 365 for Operations-virksomheder med landets kontekst, der understøtter valutaafvigelse.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, FALSK, 2) returnerer "One tusinde to hundrede tredive fire og 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, FALSK, 0) returnerer "St dwadzieścia" NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, der er angivet til true, 2) returnerer "Сто двадцать евро 21 евроцент"</td>
</tr>
<tr class="odd">
<td>PADLEFT (streng, længde, margentegn)</td>
<td>Returnerer en streng af en angivet længde, hvor begyndelsen af den aktuelle streng er udfyldt med de angivne tegn.</td>
<td>PADLEFT ("1234", 10, " ") returnerer tekststrengen "      1234"</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Dataindsamlingsfunktioner

Funktion

Betegnelse

Eksempel

FORMATELEMENTNAME ()

Returnerer navnet på det aktuelle formats element. Returnerer en tom streng, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.

Se opgaveguiden **Bruge ER-data af formatoutput til optælling og sammenlægning** (en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger**) til at lære mere om brugen af disse funktioner.

REGNEARKSFUNKTIONERNE (nøgle streng til sammenlægning, Kriteriestrengen Område1, kriterier værdi1 streng \[, kriterier område2 streng, værdi2 Kriteriestrengen,... \])

Returnerer summen af værdierne i noder (med navn, der er defineret som en nøgle) af XML, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput **for de aktuelle filer er slået fra.

SUMIF (nøglestreng for sammenlægning, kriterieintervalstreng, kriterieværdistreng)

Returnerer summen af værdierne i noder (med navn, der er defineret som en nøgle) af XML, som er blevet indsamlet under denne kørsel af format, og som opfylder den angivne betingelse (interval og værdi). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.

TÆL (kriterier Område1 streng, kriterier værdi1 streng \[, kriterier område2 streng, værdi2 Kriteriestrengen,... \])

Returnerer antal XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval- og værdipar). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.

COUNTIF (kriterieintervalstreng, kriterieværdistreng)

Returnerer antal XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder den angivne betingelse (interval og værdi). Returnerer nul værdi, når flaget **Detaljer om indsamlingsoutput** for de aktuelle filer er slået fra.

COLLECTEDLIST (kriterier Område1 streng, kriterier værdi1 streng \[, kriterier område2 streng, værdi2 Kriteriestrengen,... \])

Returnerer en liste over værdier af XML-noder, som er blevet indsamlet under denne kørsel af format, og som opfylder de angivne betingelser (interval og værdi). Returnerer en tom liste, når flaget **Detaljer om indsamlingsoutput **for de aktuelle filer er slået fra.

### <a name="other-business-domainspecific-functions"></a>Andre (forretningsdomænespecifikke) funktioner

| Funktion                                                                         | Betegnelse                                                                                                                                                                                                                                                        | Eksempel                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (beløb, kildevaluta, målvaluta, dato, firma)        | Konverter det angivne pengebeløb fra kildevalutaen til målvalutaen ved hjælp af indstillingerne for det angivne Dynamics 365 for Operations-firma på den angivne dato.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")** returnerer, hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for DEMF-firmaet.                                                                                                                                  |
| ROUNDAMOUNT (tal, decimaler, afrundingsregel)                                       | Afrund det angivne beløb i henhold til den angivne afrundingsregel og det angivne antal decimaler. **Bemærk:** Afrundingsreglen skal angives som en værdi af Dynamics 365 for Operations **RoundOffType**-fasttekst.                          | Hvis de **model. RoundOff** parameter er indstillet til *** Downward ***, **ROUNDAMOUNT (1000.787, 2, model. RoundOff)** returnerer værdien **1000.78**. Hvis **model.RoundOff**-parameter er indstillet til enten **Normal** eller **Oprunding**, vil **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** returnere værdien **1000.79**. |
| CURCredRef (cifre)                                                              | Returner en kreditors reference, baseret på cifrene i det angivne fakturanummer.                                                                                                                                                                                  | **CURCredRef ("VEND-200002")** returnerer **"2200002"**.                                                                                                                                                                                                                                                         |
| MOD\_97 (cifre)                                                                 | Returner en kreditors reference som et MOD97-udtryk, baseret på cifrene i det angivne fakturanummer.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** returnerer **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (cifre)                                                              | Returner en ISO-kreditors reference, baseret på cifrene og bogstaverne i det angivne fakturanummer. **Bemærk: **For at eliminere symboler fra alfabeter, der ikke er ISO-kompatible, skal inputparameteren oversættes, før den videresendes til denne funktion. | **ISOCredRef ("VEND-200002")** returnerer **"RF23VEND-200002"**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (streng, nummer)                                  | Hent yderligere økonomisk dimensions-id Dimensioner er repræsenteret i denne streng som id'er, der er adskilt af kommaer. Tal definerer nummerseriekode til den ønskede dimension i denne streng.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA, BB, CC, DD, EE, FF, GG, HH", 3) returnere "CC"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Returnerer koden for den aktuelt registrerede virksomhed.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (cifre)                                                       | Returnerer en kreditors reference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer.                                                                                                                                                                      | CH\_BANK\_MOD\_returnerer 3, 10 ("VEND-200002")                                                                                                                                                                                                                                                                   |
| Anlæg\_SUM (faste aktiver koden, model værdikode, startdato, slutdato)               | Returnerer den klargjorte datacontainer med anlægsaktivbeløb for en periode.                                                                                                                                                                                         | Anlæg\_SUM ("COMP 000001", "Strøm", dato1, dato2) returnerer objektbeholderen forberedte data for anlægsaktivet "COMP 000001" med værdimodellen "Strøm" i en periode fra dato1 til dato2.                                                                                                                        |
| Anlæg\_BALANCE (faste anlæg-koden, værdi model, rapporteringsår, datoen for rapportering) | Returnerer den klargjorte datacontainer med saldi for anlægsaktiver. Rapporteringsår skal angives som en værdi af Dynamics-365 for Operations-fastteksten **AssetYear**.                                                                                           | Anlæg\_SUM ("COMP 000001", "Strøm", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) returnerer den forberedte data beholder af saldi for anlægsaktivet "COMP-000001" med værdimodellen "Strøm" på de aktuelle 365 for operationer sessionsdatoen.                                                                |

### <a name="functions-list-extension"></a>Funktionslistens udvidelse

ER understøtter muligheden for at udvide listen over funktioner, der bruges i ER-udtryk. Der kræves en vis teknisk indsats for at gøre dette. Yderligere oplysninger finder du under [Udvidelse af listen over elektroniske rapporteringsfunktioner](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Se også
--------

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Udvide listen over elektroniske rapporteringsfunktioner (ER)](general-electronic-reporting-formulas-list-extension.md)


