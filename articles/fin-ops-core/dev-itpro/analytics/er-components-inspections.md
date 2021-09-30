---
title: Inspicere den konfigurerede ER-komponent for at undgå kørselsproblemer
description: Dette emne forklarer, hvordan du inspicerer de konfigurerede ER-komponenter (elektronisk rapportering) for at forhindre kørselsproblemer, der kan opstå.
author: NickSelin
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a855619ebd1c41dc3ca583912f758ed8a8f9ceef
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488108"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Inspicere den konfigurerede ER-komponent for at undgå kørselsproblemer

[!include[banner](../includes/banner.md)]

Alle konfigurerede komponenter i ER-[format](general-electronic-reporting.md#FormatComponentOutbound) [(elektronisk rapportering)](general-electronic-reporting.md) og [modeltilknytnings](general-electronic-reporting.md#data-model-and-model-mapping-components)komponenter kan [valideres ](er-fillable-excel.md#validate-an-er-format)på designtidspunktet. Under denne validering foretages en konsistenskontrol for at forhindre kørselsproblemer, der kan opstå, f.eks. kørselsfejl og reduktion af ydeevnen. For hvert enkelt problem, der findes, angiver kontrollen stien til et problematisk element. I forbindelse med nogle problemer findes der en automatisk rettelse.

Som standard anvendes valideringen automatisk i følgende tilfælde for en ER-konfiguration, der indeholder de tidligere nævnte ER-komponenter:

- Du [importerer](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) en ny [version](general-electronic-reporting.md#component-versioning) af en ER-konfiguration til din forekomst af Microsoft Dynamics 365 Finance.
- Du ændrer [status](general-electronic-reporting.md#component-versioning) for den redigerbare ER-konfiguration fra **Kladde** til **Fuldført**.
- Du [rebaserer](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) en redigerbar ER-konfiguration ved at anvende en ny basisversion.

Du kan køre denne validering eksplicit. Vælg en af følgende tre muligheder, og følg de trin, der er angivet:

- Mulighed 1:

    1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
    2. Vælg den ønskede ER-konfiguration, der indeholder komponenten i ER-format eller komponten med ER-modeltilknytningen, i konfigurationstræet i venstre rude.
    3. I oversigtspanelet **Versioner** skal du vælge den ønskede version af den valgte ER-konfiguration.
    4. Vælg **Valider** i handlingsruden.

- Mulighed 2 for ER-format:

    1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
    2. Vælg den ønskede ER-konfiguration, der indeholder komponenten i ER-format, i konfigurationstræet i venstre rude.
    3. I oversigtspanelet **Versioner** skal du vælge den ønskede version af den valgte ER-konfiguration.
    4. Vælg **Designer** i handlingsruden.
    5. I handlingsruden på siden **Formatdesigner** skal du vælge **Valider**.

- Mulighed 3 for ER-modeltilknytning:

    1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
    2. Vælg den ønskede ER-konfiguration, der indeholder komponenten med ER-modeltilknytningen, i konfigurationstræet i venstre rude.
    3. I oversigtspanelet **Versioner** skal du vælge den ønskede version af den valgte ER-konfiguration.
    4. Vælg **Designer** i handlingsruden.
    5. Vælg **Designer** i handlingsruden på siden **Tilknytning af model til datakilde**.
    6. Vælg **Valider** i handlingsruden på siden **Modeltilknytningsdesigner**.

Hvis du vil springe valideringen over, når konfigurationen importeres, skal du følge disse trin.

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Valider konfiguration efter import** til **Nej**.

Hvis du vil springe valideringen over, når du ændrer eller rebaserer versions status, skal du følge disse trin.

1. Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. Angiv indstillingen **Spring validering over ved ændring eller rebasering af konfigurations status** til **Ja**.

ER bruger følgende kategorier til at gruppere inspektioner af konsistenskontrol:

- **Mulighed for udførelse** – Inspektioner, der registrerer kritiske problemer, der kan opstå på kørselstidspunktet. Disse problemer er hovedsageligt af typen **Fejl**. 
- **Ydeevne** – Inspektioner, der registrerer problemer, der kan medføre ineffektiv udførelse af konfigurerede ER-komponenter. Disse problemer er hovedsageligt af typen **Advarsel**.
- **Dataintegritet** – Inspektioner, der registrerer problemer, der kan medføre tab af data eller kørselsproblemer. Disse problemer er hovedsageligt af typen **Advarsel**.

## <a name="list-of-inspections"></a>Liste over inspektioner

I nedenstående tabel vises en oversigt over de inspektioner, ER tilbyder. Du kan finde flere oplysninger om disse inspektioner ved at bruge linkene i første kolonne til at gå til de relevante afsnit i dette emne. I disse afsnit forklares de komponenttyper, som ER tilbyder inspektion af, og hvordan du kan omkonfigurere ER-komponenter for at undgå problemer.

<table>
<thead>
<tr>
<th>Navn</th>
<th>Kategori</th>
<th>Niveau</th>
<th>Melding</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Typekonvertering</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Et udtryk af typen &lt;type&gt; kan ikke konverteres til et felt af typen &lt;type&gt;.</p>
<p><b>Kørselsfejl:</b> Undtagelse for type</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Typekompatibilitet</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Det konfigurerede udtryk kan ikke bruges som binding for elementet i det aktuelle format til en datakilde, da dette udtryk returnerer en værdi af datatypen &lt;type&gt;, der ligger uden for det område af datatyper, som understøttes af elementet i det aktuelle format af typen &lt;type&gt;.</p>
<p><b>Kørselsfejl:</b> Undtagelsestype</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Konfigurationselementet mangler</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Stien blev ikke fundet &lt;sti&gt;.</p>
<p><b>Kørselsfejl:</b> Der blev ikke fundet et element i konfigurations&lt;stien&gt;</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Mulighed for udførelse af et udtryk med FILTER-funktion</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Der kan ikke forespørges om FILTER-funktionens listeudtryk.</p>
<p><b>Kørselsfejl:</b> Filtrering understøttes ikke. Valider konfigurationen for at få flere oplysninger om dette.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Mulighed for udførelse af en GROUPBY-datakilde</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>Stien &lt;sti&gt; understøtter ikke forespørgsler.</td>
</tr>
<tr>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Funktionen Gruppér efter kan ikke udføres med forespørgslen.</p>
<p><b>Kørselsfejl:</b> Funktionen Gruppér efter kan ikke udføres med forespørgslen.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Mulighed for udførelse af en JOIN-datakilde</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>Kan ikke joinforbinde en &lt;sti&gt; til en liste, der ikke er et filter i en forespørgsel.</p>
<p><b>Kørselsfejl:</b> Den joinforbundne funktion skal være et filterudtryk. Det beregnede felt er kaldt forkert.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Funktionen FILTER foretrækkes frem for WHERE</a></td>
<td>Ydeevne</td>
<td>Advarsel!</td>
<td>Det foretrækkes at bruge funktionen FILTER til udtrykket frem for WHERE fra et ydeevneperspektiv. Vælg Ret for at erstatte den automatisk.</td>
</tr>
<tr>
<td><a href='#i8'>Funktionen ALLITEMSQUERY foretrækkes frem for ALLITEMS</a></td>
<td>Ydeevne</td>
<td>Advarsel!</td>
<td>Det foretrækkes at bruge funktionen ALLITEMSQUERY til udtrykket frem for ALLITEMS fra et ydeevneperspektiv. Vælg Ret for at erstatte den automatisk.</td>
</tr>
<tr>
<td><a href='#i9'>Overvejelse i forbindelse med sager med tom liste</a></td>
<td>Mulighed for udførelse</td>
<td>Advarsel!</td>
<td>
<p>Liste&lt;stien&gt; indeholder ikke kontrol af, om sagen har en tom liste. Det kan resultere i en fejl på kørselstidspunktet. Tilføj kontrol af, om sagen har en tom liste.</p>
<p><b>Kørselsfejl:</b> Listen er tom på &lt;stien&gt;</p>
<p><b><a href='#i9a'>Potentielt problem</a>:</b> Linjen udfyldes én gang, mens en datakilde, som den er udfyldt fra, indeholder flere poster</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Mulighed for udførelse af et udtryk med FILTER-funktion (cachelagring)</a></td>
<td>Mulighed for udførelse</td>
<td>Fejl</td>
<td>
<p>FILTER-funktionen kan ikke anvendes på den valgte type datakilde. En datakilde af tabelposttypen kan kun anvendes, hvis den ikke er cachelagret, og der ikke er tilføjet indlejrede datakilder manuelt.</p>
<p><b>Kørselsfejl:</b> Filtrering understøttes ikke. Valider konfigurationen for at få flere oplysninger om dette.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Manglende binding</a></td>
<td>Mulighed for udførelse</td>
<td>Advarsel!</td>
<td>
<p>Stien &lt;sti&gt; har ingen binding til datakilder, når den bruger modellens tilknytning.</p>
<p><b>Kørselsfejl:</b> Stien &lt;sti&gt; er ikke bundet</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Ikke sammenkædet skabelon</a></td>
<td>Dataintegritet</td>
<td>Advarsel!</td>
<td>Filens &lt;navn&gt; er ikke kædet sammen med nogen filkomponenter og fjernes, når status for konfigurationsversion er ændret.</td>
</tr>
<tr>
<td><a href='#i13'>Ikke synkroniseret format</a></td>
<td>Dataintegritet</td>
<td>Advarsel!</td>
<td>Det definerede navn &lt;komponentnavn&gt; findes ikke i Excel-arket &lt;arknavn&gt;</td>
</tr>
<tr>
<td><a href='#i14'>Ikke synkroniseret format</a></td>
<td>Dataintegritet</td>
<td>Advarsel!</td>
<td>
<p>&lt;Kodet kontrol af Word-indhold&gt; kode findes ikke i Word-skabelonfilen</p>
<p><b>Kørselsfejl:</b> &lt;Kodet kontrol af Word-indhold&gt; kode findes ikke i Word-skabelonfilen.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Ingen standardtilknytning</a></td>
<td>Dataintegritet</td>
<td>Fejl</td>
<td>
<p>Der findes mere end én modeltilknytning for datamodellen for &lt;modelnavnet (rodbeskrivelsen)&gt; i konfigurationers &lt;konfigurationsnavne adskilt af komma&gt;. Angiv en af konfigurationerne som standard</p>
<p><b>Kørselsfejl:</b> Der findes mere end én modeltilknytning for datamodellen for &lt;modelnavnet (rodbeskrivelsen)&gt; i konfigurationer &lt;konfigurationsnavne adskilt af komma&gt;. Angiv en af konfigurationerne som standard.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Uoverensstemmende indstilling af komponenter i sidehoved eller sidefod</a></td>
<td>Dataintegritet</td>
<td>Fejl</td>
<td>
<p>Sidehoveder/sidefødder (&lt;komponenttype: sidehoved eller sidefod&gt;) er uoverensstemmende</p>
<p><b>Kørsel:</b> Den sidste konfigurerede komponent bruges under kørsel, hvis kladdeversionen af det konfigurerede ER-format udføres.</p>
</td>
</tr>
<tr>
<td><a href='#i17'>Uoverensstemmende indstilling af sidekomponent</a></td>
<td>Dataintegritet</td>
<td>Fejl</td>
<td>Der er mere end to områdekomponenter uden replikering. Fjern unødvendige komponenter.</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Typekonvertering

ER undersøger, om datatypen for et datamodelfelt er kompatibel med datatypen for et udtryk, der er konfigureret som binding for dette felt. Hvis datatyperne ikke er kompatible, opstår der en valideringsfejl i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at ER ikke kan konvertere et udtryk af typen A til et felt af typen B.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere komponenterne af typerne ER-datamodeller og ER-modeltilknytninger samtidigt.
2. Tilføj et felt med navnet **X** i datamodeltræet, og vælg **Heltal** som datatype.

    ![X-felt og datatypen Heltal, der er føjet til datatilstandstræet på siden Datamodel.](./media/er-components-inspections-01.png)

3. I ruden **Datakilder** for modeltilknytning skal du tilføje en datakilde af typen **Beregnet felt**.
4. Navngiv den nye datakilde **Y**, og konfigurer den, så den indeholder udtrykket `INTVALUE(100)`.
5. Bind **X** til **Y**.
6. I datamodeldesigneren skal du ændre datatypen for **X**-feltet fra **Heltal** til **Int64**.
7. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**.

    ![Validere den redigerbare modeltilknytningskomponent på siden Modeltilknytningsdesigner.](./media/er-components-inspections-01.gif)

8. Vælg **Valider** for at inspicere modeltilknytningskomponenten for den valgte ER-konfiguration på siden **Konfigurationer**.

    ![Inspektion af modeltilknytningskomponenten på siden Konfigurationer.](./media/er-components-inspections-01a.png)

9. Bemærk, at der opstår en valideringsfejl. Meddelelsen angiver, at værdien af den typen **Heltal**, som udtrykket `INTVALUE(100)` i **Y**-datakilden returnerer, ikke kan gemmes i datamodelfeltet **X** af typen **Int64**.

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre et format, der er konfigureret til at bruge modeltilknytningen.

![Kørselsfejl på siden Formatdesigner.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Opdater datamodelstrukturen ved at ændre datatypen for datamodelfeltet, så den svarer til datatypen for det udtryk, der er konfigureret til bindingen af det pågældende felt. I det foregående eksempel skal datatypen for feltet **X** ændres tilbage til **Heltal**.

#### <a name="option-2"></a>Indstilling 2

Opdater modeltilknytningen ved at ændre udtrykket for den datakilde, der er bundet til datamodelfeltet. I det foregående eksempel skal udtrykket for datakilden **Y** ændres til `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Typekompatibilitet

ER undersøger, om datatypen for et formatelement er kompatibel med datatypen for et udtryk, der er konfigureret som binding for det pågældende formatelement. Hvis datatyperne ikke er kompatible, opstår der en valideringsfejl i ER-operationsdesigneren. Den meddelelse, du modtager, angiver, at det konfigurerede udtryk ikke kan bruges som binding for elementet i det aktuelle format til en datakilde, da udtrykket returnerer en værdi af datatypen A, der ligger uden for området af de datatyper, som understøttes af elementet i det aktuelle format af typen B.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere komponenterne af typerne ER-datamodel og ER-format samtidigt.
2. Tilføj et felt med navnet **X** i datamodeltræet, og vælg **Heltal** som datatype.
3. Tilføj et formatelement af typen **Numerisk** i formatstrukturtræet.
4. Navngiv det nye formatelement **Y**. Vælg **Heltal** som datatype i feltet **Numerisk type**.
5. Bind **X** til **Y**.
6. Skift datatypen for **Y**-formatelementet fra **Heltal** til **Int64** i formatstrukturtræet.
7. Vælg **Valider** for at inspicere den redigerbare formatkomponent på siden **Formatdesigner**.

    ![Validere typekompatibilitet på siden Formatdesigner.](./media/er-components-inspections-02.gif)

8. Bemærk, at der opstår en valideringsfejl. Meddelelsen angiver, at det konfigurerede udtryk kun kan acceptere **Int64**-værdier. Derfor kan værdien af **X**-datamodelfeltet for typen **Heltal** ikke angives i formatelementet **Y**.

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Opdater formatstrukturen ved at ændre datatypen for formatelementet **Numerisk**, så den svarer til datatypen for det udtryk, du har konfigureret til bindingen af det pågældende element. I det foregående eksempel skal værdien **Numerisk type** for formatelementet **X** ændres tilbage til **Heltal**.

#### <a name="option-2"></a>Indstilling 2

Opdater formattilknytningen for formatelementet **X** ved at ændre udtrykket fra `model.X` til `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Konfigurationselementet mangler

ER kontrollerer, om bindingsudtrykkene kun indeholder datakilder, der er konfigureret i den redigerbare ER-komponent. For alle bindinger, der indeholder en datakilde, som mangler i den redigerbare ER-komponent, opstår der en valideringsfejl i ER-operationsdesigneren eller i ER-modeltilknytningsdesigneren.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere komponenterne af typerne ER-datamodeller og ER-modeltilknytninger samtidigt.
2. Tilføj et felt med navnet **X** i datamodeltræet, og vælg **Heltal** som datatype.

    ![Datamodeltræ med feltet X og datatypen Heltal på siden Datamodel.](./media/er-components-inspections-01.png)

3. I ruden **Datakilder** for modeltilknytning skal du tilføje en datakilde af typen **Beregnet felt**.
4. Navngiv den nye datakilde **Y**, og konfigurer den, så den indeholder udtrykket `INTVALUE(100)`.
5. Bind **X** til **Y**.
6. Slet datakilden **Y** i ruden **Datakilder** i modeltilknytningsdesigneren.
7. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**.

    ![Inspektion af den redigerbare ER-modeltilknytningskomponent på siden Modeltilknytningsdesigner.](./media/er-components-inspections-03.gif)

8. Bemærk, at der opstår en valideringsfejl. Meddelelsen angiver, at bindingen af datamodelfeltet **X** indeholder den sti, der refererer til datakilden **Y**, men denne datakilde blev ikke fundet.

### <a name="automatic-resolution"></a>Automatisk løsning

Vælg **Ophæv binding** for at løse dette problem automatisk ved at fjerne den manglende datakildebinding.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Ophæv bindingen af datamodelfeltet **X** for at stoppe henvisningen til den ikke-eksisterende **Y**-datakilde.

#### <a name="option-2"></a>Indstilling 2

I ruden **Datakilder** i ER-modeltilknytningsdesigneren skal du tilføje datakilden **Y** igen.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Mulighed for udførelse af et udtryk med FILTER-funktion

Den indbyggede ER-funktion [FILTER](er-functions-list-filter.md) bruges til at få adgang til programtabeller, visninger eller dataenheder ved at foretage et enkelt SQL-kald for at hente de nødvendige data som en liste over poster. En datakilde af typen **Postliste** bruges som argument for denne funktion og angiver programkilden for kaldet. ER kontrollerer, om der kan oprettes en direkte SQL-forespørgsel til en datakilde, der refereres til i `FILTER`-funktionen. Hvis der ikke kan oprettes en direkte forespørgsel, opstår der en valideringsfejl i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at det ER-udtryk, der inkluderer `FILTER`-funktionen, ikke kan køres på kørselstidspunktet.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
4. Tilføj en datakilde af typen **Beregnet felt**.
5. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at udtrykket `FILTER(Vendor, Vendor.AccountNum="US-101")` i datakilden **Kreditor** kan forespørges.
7. Rediger datakilden **Kreditor** ved at tilføje et indlejret felt af typen **Beregnet felt** for at få det relevante kreditorkontonummer.
8. Navngiv det nye indlejrede felt **$AccNumber**, og konfigurer det, så det indeholder udtrykket `TRIM(Vendor.AccountNum)`.
9. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at udtrykket `FILTER(Vendor, Vendor.AccountNum="US-101")` i datakilden **Kreditor** kan forespørges.

    ![Kontrollere, at udtrykket kan forespørges på siden Modeltilknytningsdesigner.](./media/er-components-inspections-04.gif)

10. Bemærk, at der opstår en valideringsfejl, fordi datakilden **Kreditor** indeholder et indlejret felt af typen **Beregnet felt**, der ikke tillader, at udtrykket i datakilden **FilteredVendor** oversættes til den direkte SQL-sætning.

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre et format, der er konfigureret til at bruge modeltilknytningen.

![Der opstår kørselsfejl, når du kører det redigerbare format på siden Formatdesigner.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

I stedet for at føje et indlejret felt af typen **Beregnet felt** til datakilden **Kreditor**, skal du føje det indlejrede felt **$AccNumber** til datakilden **FilteredVendor** og konfigurere det, så det indeholder udtrykket `TRIM(FilteredVendor.AccountNum)`. På denne måde kan udtrykket `FILTER(Vendor, Vendor.AccountNum="US-101")` køres på SQL-niveau og beregne det indlejrede felt **$AccNumber** bagefter.

#### <a name="option-2"></a>Indstilling 2

Rediger udtrykket i datakilden **FilteredVendor** fra `FILTER(Vendor, Vendor.AccountNum="US-101")` til `WHERE(Vendor, Vendor.AccountNum="US-101")`. Det anbefales ikke, at du ændrer udtrykket for en tabel, der har en stor mængde data (transaktionstabel), fordi alle poster hentes, og valg af de nødvendige poster sker i hukommelsen. Denne fremgangsmåde kan derfor forårsage dårlig ydeevne. Yderligere oplysninger finder du i [ER-funktionen WHERE](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Mulighed for udførelse af en GROUPBY-datakilde

Datakilden **GROUPBY** opdeler forespørgselsresultatet i grupper af poster, normalt med det formål at foretage en eller flere sammenlægninger af hver gruppe. Alle **GROUPBY**-datakilder kan konfigureres, så de køres enten på databaseniveau eller i hukommelsen. Når en **GROUPBY**-datakilde konfigureres, så den køres på databaseniveau, kontrollerer ER, om der kan oprettes en direkte SQL-forespørgsel til en datakilde, der henvises til i den pågældende datakilde. Hvis der ikke kan oprettes en direkte forespørgsel, opstår der en valideringsfejl i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at den konfigurerede **GROUPBY**-datakilde ikke kan køres på kørselstidspunktet.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Trans**. I feltet **Tabel** skal du vælge **VendTrans** for at angive, at denne datakilde skal anmode om tabellen VendTrans.
4. Tilføj en datakilde af typen **Gruppér efter**.
5. Navngiv den nye datakilde **GroupedTrans**, og konfigurer den på følgende måde:

    - Vælg datakilden **Trans** som den postkilde, der skal grupperes.
    - Vælg **Forespørgsel** i feltet **Udførselssted** for at angive, at du vil køre denne datakilde på databaseniveau.

    ![Konfigurere datakilden på siden Rediger 'Gruppér efter'-parametre.](./media/er-components-inspections-05a.gif)

6. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at den konfigurerede datakilde **GroupedTrans** kan forespørges.
7. Rediger datakilden **Trans** ved at tilføje et indlejret felt af typen **Beregnet felt** for at få det relevante kreditorkontonummer.
8. Navngiv den nye datakilde **$AccNumber**, og konfigurer den, så den indeholder udtrykket `TRIM(Trans.AccountNum)`.

    ![Konfigurere datakilden på siden Modeltilknytningsdesigner.](./media/er-components-inspections-05a.png)

9. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at den konfigurerede datakilde **GroupedTrans** kan forespørges.

    ![Validering af ER-modeltilknytningskomponenten, og kontrol af den GroupedTrans-datakilde kan forespørges, på siden Modeltilknytningsdesigner.](./media/er-components-inspections-05b.png)

10. Bemærk, at der opstår en valideringsfejl, fordi datakilden **Trans** indeholder et indlejret felt af typen **Beregnet felt**, der ikke tillader, at kaldet til datakilden **GroupedTrans** oversættes til den direkte SQL-sætning.

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre et format, der er konfigureret til at bruge modeltilknytningen.

![Der opstår kørselsfejl, når advarslen ignoreres på siden Formatdesigner.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

I stedet for at føje et indlejret felt af typen **Beregnet felt** til datakilden **Trans**, skal du tilføje det indlejrede felt **$AccNumber** for elementet **GroupedTrans.lines** for datakilden **GroupedTrans** og konfigurere det, så det indeholder udtrykket `TRIM(GroupedTrans.lines.AccountNum)`. På denne måde kan datakilden **GroupedTrans** køres på SQL-niveau og beregne det indlejrede felt **$AccNumber** bagefter.

#### <a name="option-2"></a>Indstilling 2

Rediger værdien i feltet **Udførselssted** for datakilden **GroupedTrans** fra **Forespørgsel** til **I hukommelsen**. Det anbefales ikke, at du ændrer værdien for en tabel, der har en stor mængde data (transaktionstabel), fordi alle poster hentes, og gruppering og aggregering sker i hukommelsen. Denne fremgangsmåde kan derfor forårsage dårlig ydeevne.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Mulighed for udførelse af en JOIN-datakilde

Datakilden [JOIN](er-join-data-sources.md) kombinerer poster fra to eller flere databasetabeller baseret på relaterede felter. Alle **JOIN**-datakilder kan konfigureres, så de køres enten på databaseniveau eller i hukommelsen. Når en **JOIN**-datakilde konfigureres, så den køres på databaseniveau, kontrollerer ER, om der kan oprettes en direkte SQL-forespørgsel til datakilder, der henvises til i den pågældende datakilde. Hvis der ikke kan oprettes en direkte SQL-forespørgsel med mindst én henvist datakilde, opstår der en valideringsfejl i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at den konfigurerede **JOIN**-datakilde ikke kan køres på kørselstidspunktet.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
4. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
5. Navngiv den nye datakilde **Trans**. I feltet **Tabel** skal du vælge **VendTrans** for at angive, at denne datakilde skal anmode om tabellen VendTrans.
6. Tilføj en datakilde af typen **Beregnet felt** som det indlejrede felt for datakilden **Kreditor**.
7. Navngiv den nye datakilde **FilteredTrans**, og konfigurer den, så den indeholder udtrykket `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Tilføj en datakilde af typen **Join**.
9. Navngiv den nye datakilde **JoinedList**, og konfigurer den på følgende måde:

    1. Tilføj datakilden **Kreditor** som det første sæt poster, der skal joinforbindes.
    2. Tilføj datakilden **Vendor.FilteredTrans** som det andet sæt poster, der skal joinforbindes. Vælg **INNER** som type.
    3. Vælg **Forespørgsel** i feltet **Udfør** for at angive, at du vil køre denne datakilde på databaseniveau.

    ![Konfigurere datakilden på siden Joinforbindelsesdesigner.](./media/er-components-inspections-06a.gif)

10. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at den konfigurerede datakilde **JoinedList** kan forespørges.
11. Rediger udtrykket for datakilden **Vendor.FilteredTrans** fra `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` til `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**, og kontroller, at den konfigurerede datakilde **JoinedList** kan forespørges.

    ![Validering af den redigerbare modeltilknytningskomponent, og kontrol af, at datakilden JoinedList kan forespørges, på siden Modeltilknytningsdesigner.](./media/er-components-inspections-06b.png)

13. Bemærk, at der opstår valideringsfejl, fordi udtrykket for datakilden **Vendor.FilteredTrans** ikke kan oversættes til det direkte SQL-kald. Derudover gør det direkte SQL-kald det ikke muligt at oversætte kaldet for datakilden **JoinedList** til den direkte SQL-sætning.

    ![Kørselsfejl på grund af mislykket validering af datakilden JoinedList på siden Modeltilknytningsdesigner.](./media/er-components-inspections-06c.png)

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre et format, der er konfigureret til at bruge modeltilknytningen.

![Køre det redigerbare format på siden Formatdesigner.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Skift udtrykket for datakilden **Vendor.FilteredTrans** fra `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` tilbage til `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, som advarslen foreslår.

![Updateret udtryk for datakilde på siden Modeltilknytningsdesigner.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Indstilling 2

Rediger værdien i feltet **Udfør** for datakilden **JoinedList** fra **Forespørgsel** til **I hukommelsen**. Det anbefales ikke, at du ændrer værdien for en tabel, der har en stor mængde data (transaktionstabel), fordi alle poster hentes, og joinforbindelse foregår i hukommelsen. Denne fremgangsmåde kan derfor forårsage dårlig ydeevne. Der vises en valideringsadvarsel, som oplyser dig om denne risiko.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Funktionen FILTER foretrækkes frem for WHERE

Den indbyggede ER-funktion [FILTER](er-functions-list-filter.md) bruges til at få adgang til programtabeller, visninger eller dataenheder ved at foretage et enkelt SQL-kald for at hente de nødvendige data som en liste over poster. Funktionen [WHERE](er-functions-list-where.md) henter alle poster fra den givne kilde og vælger poster i hukommelsen. En datakilde af typen **Postliste** bruges som argument for begge funktioner og angiver en kilde til hentning af poster. ER kontrollerer, om der kan oprettes et direkte SQL-kald til en datakilde, der refereres til i **WHERE**-funktionen. Hvis der ikke kan oprettes et direkte kald, vises der en valideringsadvarsel i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, anbefaler, at du bruger funktionen **FILTER** i stedet for funktionen **WHERE** for at øge effektiviteten.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Trans**. I feltet **Tabel** skal du vælge **VendTrans** for at angive, at denne datakilde skal anmode om tabellen VendTrans.
4. Tilføj en datakilde af typen **Beregnet felt** som det indlejrede felt for datakilden **Kreditor**.
5. Navngiv den nye datakilde **FilteredTrans**, og konfigurer den, så den indeholder udtrykket `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
7. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
8. Tilføj en datakilde af typen **Beregnet felt**.
9. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**.

    ![Inspicere den redigerbare ER-modeltilknytningskomponent på siden Modeltilknytningsdesigner.](./media/er-components-inspections-07a.png)

11. Bemærk, at valideringsadvarsler anbefaler, at du bruger funktionen **FILTER** i stedet for funktionen **WHERE** for datakilderne **FilteredVendor** og **FilteredTrans**.

    ![Anbefaling at bruge funktionen FILTER i stedet for funktionen WHERE på siden Modeltilknytningsdesigner.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Vælg **Ret** for automatisk at erstatte funktionen **WHERE** med funktionen **FILTER** i udtrykket for alle datakilder, der vises i gitteret under fanen **Advarsler** for denne type inspektion.

Du kan også vælge rækken for en enkelt advarsel i gitteret og derefter vælge **Ret markeret**. I dette tilfælde ændres udtrykket automatisk i den datakilde, der er nævnt i den valgte advarsel.

![Vælge Ret for automatisk at erstatte funktionen WHERE med funktionen FILTER på siden Modeltilknytningsdesigner.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Manuel løsning

Du kan manuelt justere udtrykkene for alle datakilderne i valideringsgitteret ved at erstatte funktionen **WHERE** med funktionen **FILTER**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Funktionen ALLITEMSQUERY foretrækkes frem for ALLITEMS

De indbyggede ER-funktioner [ALLITEMS](er-functions-list-allitems.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md) returnerer en flad værdi i **Postliste**, der består af en liste over poster, som repræsenterer alle elementer, som svarer til den angivne sti. ER kontrollerer, om der kan oprettes et direkte SQL-kald til en datakilde, der refereres til i **ALLITEMS**-funktionen. Hvis der ikke kan oprettes et direkte kald, vises der en valideringsadvarsel i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, anbefaler, at du bruger funktionen **ALLITEMSQUERY** i stedet for funktionen **ALLITEMS** for at øge effektiviteten.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
4. Tilføj en datakilde af typen **Beregnet felt** for at få poster for flere kreditorer.
5. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Tilføj en datakilde af typen **Beregnet felt** for at få transaktioner for alle filtrerede kreditorer.
7. Navngiv den nye datakilde **FilteredVendorTrans**, og konfigurer den, så den indeholder udtrykket `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**.

    ![Inspektion af den redigerbare modeltilknytningskomponent på siden Modeltilknytningsdesigner.](./media/er-components-inspections-08a.png)

9. Bemærk, at der opstår en valideringsadvarsel. I meddelelsen anbefales det, at du bruger funktionen **ALLITEMSQUERY** i stedet for funktionen **ALLITEMS** for datakilden **FilteredVendorTrans**.

    ![Anbefaling at bruge funktionen ALLITEMSQUERY i stedet for funktionen ALLITEMS på siden Modeltilknytningsdesigner.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Vælg **Ret** for automatisk at erstatte funktionen **ALLITEMS** med funktionen **ALLITEMSQUERY** i udtrykket for alle datakilder, der vises i gitteret under fanen **Advarsler** for denne type inspektion.

Du kan også vælge rækken for en enkelt advarsel i gitteret og derefter vælge **Ret markeret**. I dette tilfælde ændres udtrykket automatisk i den datakilde, der er nævnt i den valgte advarsel.

![Vælg Ret på Siden Modeltilknytningsdesigner.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Manuel løsning

Du kan manuelt justere udtrykkene for alle de datakilder, der nævnes i valideringsgitteret, ved at erstatte funktionen **ALLITEMS** med funktionen **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Overvejelse i forbindelse med sager med tom liste

Du kan konfigurere din ER-format- eller -modeltilknytningskomponent, så den får feltværdien for en datakilde til typen **Postliste**. ER kontrollerer, om designet overvejer det tilfælde, hvor en datakilde, der kaldes, ikke indeholder poster (dvs. den er tom), for at forhindre kørselsfejl, når en værdi hentes fra et felt i en post, der ikke findes.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere komponenterne af typerne ER-datamodel, ER-modeltilknytning og ER-format samtidigt.
2. Tilføj et rodelement med navnet **Root3** i datamodeltræet.
3. Rediger elementet **Root3s** ved at tilføje et indlejret element af typen **Postliste**.
4. Navngiv det nye indlejrede element **Kreditor**.
5. Rediger elementet **Kreditor** på følgende måde:

    - Tilføj et indlejret felt af typen **Streng**, og giv det navnet **Name**.
    - Tilføj et indlejret felt af typen **Streng**, og giv det navnet **AccountNumber**.

    ![Tilføje indlejrede felter på siden Datamodel.](./media/er-components-inspections-09a.png)

6. I ruden **Datakilder** for modeltilknytning skal du tilføje en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
7. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
8. Tilføj en datakilde af typen **Generelt \\ Brugerinputparameter** for at søge efter en kreditorkonto i kørselsdialogboksen.
9. Navngiv den nye datakilde **RequestedAccountNum**. Angiv **Kreditors kontonummer** i feltet **Etiket**. Behold standardværdien i feltet **Navn på operationsdatatype**, **Beskrivelse**.
10. Tilføj en datakilde af typen **Beregnet felt** for at filtrere en kreditor, der forespørges om.
11. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bind datamodelelementerne til konfigurerede datakilder på følgende måde:

    - Bind **FilteredVendor** til **Kreditor**.
    - Bind **FilteredVendor.AccountNum** til **Vendor.AccountNumber**.
    - Bind **FilteredVendor.'name()'** til **Vendor.Name**.

    ![Binde datamodelelementer på siden Modeltilknytningsdesigner.](./media/er-components-inspections-09b.png)

13. Tilføj følgende elementer i formatstrukturtræet for at generere et udgående dokument i XML-format, der indeholder kreditoroplysningerne:

    1. Tilføj rod-XML-elementet **Sætning**.
    2. Tilføj det indlejrede XML-element **Part** for XML-elementet **Sætning**.
    3. Tilføj følgende indlejrede XML-attributter for XML-elementet **Part**:

        - Navn
        - AccountNum

14. Bind formatelementer til de angivne datakilder på følgende måde:

    - Bind formatelementet **Sætning\\Part\\Name** til datakildefeltet **model.Vendor.Name**.
    - Bind formatelementet **Sætning\\Part\\AccountNum** til datakildefeltet **model.Vendor.AccountNumber**.

15. Vælg **Valider** for at inspicere den redigerbare formatkomponent på siden **Formatdesigner**.

    ![Validere de formatelementer, du har bundet til datakilder på siden Formatdesigner.](./media/er-components-inspections-09c.png)

16. Bemærk, at der opstår en valideringsfejl. Meddelelsen angiver, at der muligvis udløses en fejl for de konfigurerede formatkomponenter **Sætning\\Part\\Name** og **Sætning\\Part\\AccountNum** på kørselstidspunktet, hvis listen `model.Vendor` er tom.

    ![Valideringsfejl, der giver besked om en mulig fejl i de konfigurerede formatkompontenter.](./media/er-components-inspections-09d.png)

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen. Vælg **Kør** for at køre formatet, og vælg kontonummeret for en kreditor, der ikke findes. Da den ønskede kreditor ikke findes, vil listen `model.Vendor` være tom (dvs. at den ikke indeholder nogen poster).

![Kørselsfejl, fordi det opstod under kørsel af formattilknytningen.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Du kan vælge **Ophæv binding** for den valgte række i gitteret under fanen **Advarsler**. Den binding, der peges på i kolonnen **Sti**, fjernes automatisk fra formatelementerne.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Du kan binde formatelementet **Sætning\\Part\\Name** til datakildeelementet `model.Vendor`. På kørselstidspunktet kalder denne binding først datakilden `model.Vendor`. Når `model.Vendor` returnerer en tom postliste, køres de indlejrede formatelementer ikke. Derfor forekommer der ingen valideringsadvarsler for denne formatkonfiguration.

![Binde formatelementet til datakildeelementet på siden Formatdesigner.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Indstilling 2

Skift bindingen for formatelementet **Sætning\\Part\\Name** fra `model.Vendor.Name` til `FIRSTORNULL(model.Vendor).Name`. Den opdaterede binding konverterer betinget den første post i datakilden `model.Vendor` typen **Postliste** til en ny datakilde af typen **Post**. Den nye datakilde indeholder det samme sæt felter.

- Hvis mindst én post er tilgængelig i datakilden `model.Vendor`, udfyldes felterne i den pågældende post med værdierne fra felterne i den første post i datakilden `model.Vendor`. I dette tilfælde returnerer den opdaterede binding kreditorens navn.
- Ellers udfyldes alle felter i den post, der oprettes, med standardværdien for datatypen i det pågældende felt. I dette tilfælde returneres den tomme streng som standardværdi for datatypen **Streng**.

Derfor forekommer der ingen valideringsadvarsler for **Sætning\\Part\\Name**, når det er bundet til udtrykket `FIRSTORNULL(model.Vendor).Name`.

![Ændret binding løser valideringsadvarsler på siden Formatdesigner.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Indstilling 3

Hvis du eksplicit vil angive de data, der er angivet i et genereret dokument, når datakilden `model.Vendor` af typen **Postliste** ikke returnerer poster (teksten **Ikke tilgængelig** i dette eksempel), skal du ændre bindingen af formatelementet **Sætning\\Part\\Name** fra `model.Vendor.Name` til `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Du kan også bruge udtrykket `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Yderligere overvejelser

I inspektionen får du også en advarsel om et andet potentielt problem. Efterhånden som du binder formatelementerne **Sætning\\Part\\Name** og **Sætning\\Part\\AccountNum** til de rette felter for datakilden `model.Vendor` af typen **Postliste**, køres disse bindinger og henter værdierne for de rette felter for den første i datakilden `model.Vendor`, hvis denne liste ikke er tom.

Da du ikke har bundet formatelementet **Sætning\\Part** til datakilden `model.Vendor`, vil elementet **Sætning\\Part** ikke blive gentager for hver post i datakilden `model.Vendor` under formatudførelse. Et genereret dokument vil i stedet kun blive udfyldt med oplysninger fra den første post på listen over poster, hvis den pågældende liste indeholder flere poster. Der kan derfor være et problem, hvis formatet er beregnet til at udfylde et genereret dokument med oplysninger om alle kreditorer fra datakilden `model.Vendor`. Du kan løse dette problem ved at binde elementet **Sætning\\Part** til datakilden `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Mulighed for udførelse af et udtryk med FILTER-funktion (cachelagring)

Flere indbyggede ER-funktioner, herunder [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md), bruges til at få adgang til programtabeller, visninger eller dataenheder ved at foretage et enkelt SQL-kald for at hente de nødvendige data som en liste over poster. En datakilde af typen **Postliste** bruges som argument for hver af disse funktioner og angiver en programkilde for kaldet. ER kontrollerer, om der kan oprettes et direkte SQL-kald til en datakilde, der refereres til i en af disse funktioner. Hvis der ikke kan oprettes et direkte kald, fordi datakilden var markeret som [cachelagret](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), opstår der en valideringsfejl i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at det ER-udtryk, der indeholder en af disse funktioner, ikke kan køres på kørselstidspunktet.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-modeltilknytningskomponenten.
2. Tilføj en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
3. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
4. Tilføj en datakilde af typen **Generelt \\ Brugerinputparameter** for at søge efter en kreditorkonto i kørselsdialogboksen.
5. Navngiv den nye datakilde **RequestedAccountNum**. Angiv **Kreditors kontonummer** i feltet **Etiket**. Behold standardværdien i feltet **Navn på operationsdatatype**, **Beskrivelse**.
6. Tilføj en datakilde af typen **Beregnet felt** for at filtrere en kreditor, der forespørges om.
7. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Markér den konfigurerede **Kreditor**-datakilde som cachelagret.

    ![Konfigurere modeltilknytningskomponenten på siden Modeltilknytningsdesigner.](./media/er-components-inspections-10a.gif)

9. Vælg **Valider** for at inspicere den redigerbare modeltilknytningskomponent på siden **Modeltilknytningsdesigner**.

    ![Validere den FILTER-funktion, der er anvendt på datakilden for den cachelagrede kreditor, på siden Modeltilknytningsdesigner.](./media/er-components-inspections-10a.png)

10. Bemærk, at der opstår en valideringsfejl. Meddelelsen angiver, at funktionen **FILTER** ikke kan anvendes på den cachelagrede **Kreditor**-datakilde.

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre formatet.

![Der opstod kørselsfejl under kørsel af formattilknytningen på siden Formatdesigner.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution&quot;></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name=&quot;manual-resolution&quot;></a>Manuel løsning

#### <a name=&quot;option-1&quot;></a>Indstilling 1

Fjern flaget **Cache** fra datakilden **Kreditor**. Datakilden **FilteredVendor** bliver derefter eksekverbar, men datakilden **Kreditor**, der refereres til i tabellen VendTable, åbnes, hver gang datakilden **FilteredVendor** kaldes.

#### <a name=&quot;option-2&quot;></a>Indstilling 2

Rediger udtrykket i datakilden **FilteredVendor** fra `FILTER(Vendor, Vendor.AccountNum=&quot;US-101")` til `WHERE(Vendor, Vendor.AccountNum="US-101")`. I dette tilfælde åbnes datakilden **Kreditor**, der refereres til i tabellen VendTable, kun under det første opkald fra datakilden **Kreditor**. Valg af poster sker dog i hukommelsen. Denne fremgangsmåde kan derfor forårsage dårlig ydeevne.

## <a name="missing-binding"></a><a id="i11"></a>Manglende binding

Når du konfigurerer en ER-formatkomponent, tilbydes ER-basisdatamodellen som standarddatakilde for ER-formatet. Når det konfigurerede ER-formatet køres, bruges [standardmodeltilknytningen](er-country-dependent-model-mapping.md) for basismodellen til at udfylde datamodellen med programdata. ER-formatdesigneren viser en advarsel, hvis du binder et formatelement til et datamodelelement, der ikke er bundet til en datakilde i den modeltilknytning, der aktuelt er valgt som standardmodeltilknytning for det redigerbare format. Denne bindingstype kan ikke køres på kørselstidspunktet, fordi det format, der køres, ikke kan udfylde et bundet element med programdata. Derfor opstår der en fejl på kørselstidspunktet.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere komponenterne af typerne ER-datamodel, ER-modeltilknytning og ER-format samtidigt.
2. Tilføj et rodelement med navnet **Root3** i datamodeltræet.
3. Rediger elementet **Root3s** ved at tilføje et nyt indlejret element af typen **Postliste**.
4. Navngiv det nye indlejrede element **Kreditor**.
5. Rediger elementet **Kreditor** på følgende måde:

    - Tilføj et indlejret felt af typen **Streng**, og giv det navnet **Name**.
    - Tilføj et indlejret felt af typen **Streng**, og giv det navnet **AccountNumber**.

    ![Føje indlejrede felter til kreditorelementet på siden Datamodel.](./media/er-components-inspections-11a.png)

6. I ruden **Datakilder** for modeltilknytning skal du tilføje en datakilde af typen **Dynamics 365 for Operations \\ Tabelposter**.
7. Navngiv den nye datakilde **Kreditor**. I feltet **Tabel** skal du vælge **VendTable** for at angive, at denne datakilde vil anmode om tabellen VendTable.
8. Tilføj en datakilde af typen **Generelt \\ Brugerinputparameter** for at forespørge om en kreditorkonto i kørselsdialogboksen.
9. Navngiv den nye datakilde **RequestedAccountNum**. Angiv **Kreditors kontonummer** i feltet **Etiket**. Behold standardværdien i feltet **Navn på operationsdatatype**, **Beskrivelse**.
10. Tilføj en datakilde af typen **Beregnet felt** for at filtrere en kreditor, der forespørges om.
11. Navngiv den nye datakilde **FilteredVendor**, og konfigurer den, så den indeholder udtrykket `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Bind datamodelelementerne til konfigurerede datakilder på følgende måde:

    - Bind **FilteredVendor** til **Kreditor**.
    - Bind **FilteredVendor.AccountNum** til **Vendor.AccountNumber**.

    > [!NOTE]
    > Datamodelfeltet **Vendor.Name** forbliver ubundet.

    ![Datamodelelementer, der er bundet til konfigurerede datakilder, og et datatilstandselement, der forbliver på siden Modeltilknytningsdesigner.](./media/er-components-inspections-11b.png)

13. Tilføj følgende elementer i formatstrukturtræet for at generere et udgående dokument i XML-format, der indeholder oplysningerne om de kreditorer, der forespørges om:

    1. Tilføj rod-XML-elementet **Sætning**.
    2. Tilføj det indlejrede XML-element **Part** for XML-elementet **Sætning**.
    3. Tilføj følgende indlejrede XML-attributter for XML-elementet **Part**:

        - Navn
        - AccountNum

14. Bind formatelementerne til de angivne datakilder på følgende måde:

    - Bind formatelementet **Sætning\\Part** til datakildeelementet `model.Vendor`.
    - Bind formatelementet **Sætning\\Part\\Name** til datakildefeltet **model.Vendor.Name**.
    - Bind formatelementet **Sætning\\Part\\AccountNum** til datakildefeltet **model.Vendor.AccountNumber**.

15. Vælg **Valider** for at inspicere den redigerbare formatkomponent på siden **Formatdesigner**.

    ![Validere ER-formatkomponenten på siden Formatdesigner.](./media/er-components-inspections-11c.png)

16. Bemærk, at der opstår en valideringsadvarsel. Meddelelsen angiver, at datakildefeltet **model.Vendor.Name** ikke er bundet til nogen datakilde i den modeltilknytning, der er konfigureret til at blive brugt af formatet. Formatelementet **Sætning\\Part\\Name** udfyldes muligvis ikke ved kørsel, og der kan forekomme en kørselsundtagelse.

    ![Validere ER-formatkomponenten på siden Formatdesigner.](./media/er-components-inspections-11d.png)

I følgende illustration vises den kørselsfejl, der opstår, hvis du ignorerer advarslen og vælger **Kør** for at køre formatet.

![Kørsel af det redigerbare format på siden Formatdesigner.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Rediger den konfigurerede modeltilknytning ved at føje en binding til datakildefeltet **model.Vendor.Name**.

#### <a name="option-2"></a>Indstilling 2

Rediger det konfigurerede format ved at fjerne en binding for formatelementet **Sætning\\Part\\Name**.

## <a name="not-linked-template"></a><a id="i12"></a>Ikke sammenkædet skabelon

Når du [manuelt](er-fillable-excel.md#manual-entry) konfigurerer en ER-formatkomponent for at bruge en skabelon til at generere et udgående dokument, skal du tilføje elementet **Excel\\Fil** manuelt, tilføje den ønskede skabelon som en vedhæftet fil til den redigerbare komponent og markere den vedhæftede fil i det tilføjede **Excel\\Fil**-element. På denne måde angiver du, at det tilføjede element vil udfylde den valgte skabelon på kørselstidspunktet. Når du konfigurerer en version af formatkomponenten i **Kladde** [Status](general-electronic-reporting.md#component-versioning), kan du føje flere skabeloner til den redigerbare komponent og derefter vælge hver skabelon i elementet **Excel\\Fil** for at køre ER-formatet. På denne måde kan du se, hvordan de forskellige skabeloner udfyldtes på kørselstidspunktet. Hvis du har skabeloner, der ikke er valgt i nogen **Excel\\Fil**-elementer, advarer ER-formatdesigneren dig om, at disse skabeloner slettes fra den version af ER-formatkomponenten, der kan redigeres, når dens status ændres fra **Kladde** til **Fuldført**.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-formatkomponenten.
2. Tilføj elementet **Excel\\Fil** i formatstrukturtræet.
3. I det **Excel\\Fil**-element, du lige har tilføjet, kan du tilføje en Excel-projektmappefil, **A.xlsx**, som en vedhæftet fil. Brug den dokumenttype, der er konfigureret i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), til at angive lagringen af ER-formatskabeloner.
4. I **Excel\\Fil**-elementet skal du tilføje en anden Excel-projektmappefil, **B.xlsx**, som en vedhæftet fil. Brug den samme dokumenttype, der bruges til projektmappefilen A.
5. Vælg projektmappefilen A i elementet **Excel\\Fil**.
6. Vælg **Valider** for at inspicere den redigerbare formatkomponent på siden **Formatdesigner**.

    ![Validere den redigerbare formatkomponent i projektmappefilen på siden Formatdesigner.](./media/er-components-inspections-12a.gif)

7. Bemærk, at der opstår en valideringsadvarsel. Meddelelsen angiver, at projektmappefilen B.xlsx ikke er kædet sammen med nogen komponenter, og at den fjernes, når status for konfigurationsversionen ændres.

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

Rediger det konfigurerede format ved at fjerne alle skabeloner, der ikke er sammenkædet med et **Excel\\Fil**-element.

## <a name="not-synced-format"></a><a id="i13"></a>Ikke synkroniseret format

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent for at bruge en Excel-skabelon til at generere et udgående dokument, kan du tilføje elementet **Excel\\Fil** manuelt, tilføje den ønskede skabelon som en vedhæftet fil til den redigerbare komponent og markere den vedhæftede fil i det tilføjede **Excel\\Fil**-element. På denne måde angiver du, at det tilføjede element vil udfylde den valgte skabelon på kørselstidspunktet. Da den tilføjede Excel-skabelon er designet eksternt, kan det redigerbare ER-format indeholde Excel-navne, der mangler i den tilføjede skabelon. ER-formatdesigneren advarer dig om eventuelle uoverensstemmelser mellem egenskaberne for de ER-formatelementer, der refererer til navne, som ikke er medtaget i den tilføjede Excel-skabelon.

Følgende fremgangsmåde viser, hvordan dette problem kan opstå.

1. Start med at konfigurere ER-formatkomponenten.
2. Tilføj **Excel\\Fil**-elementet **Rapport** i formatstrukturtræet.
3. I det **Excel\\Fil**-element, du lige har tilføjet, kan du tilføje en Excel-projektmappefil, **A.xlsx**, som en vedhæftet fil. Brug den dokumenttype, der er konfigureret i [ER-parametrene](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), til at angive lagringen af ER-formatskabeloner.

    > [!IMPORTANT]
    > Kontrollér, at den tilføjede Excel-projektmappe ikke indeholder navnet **ReportTitle**.

4. Tilføj følgende **Excel\\Celle**-element **Titel** som et indlejret element i elementet **Rapport**. I feltet **Excel-interval** skal du indtaste **ReportTitle**.
5. Vælg **Valider** for at inspicere den redigerbare formatkomponent på siden **Formatdesigner**.

    ![Validere de indlejrede elementer og felter på siden Formatdesigner.](./media/er-components-inspections-13a.png)

6. Bemærk, at der opstår en valideringsadvarsel. Meddelelsen angiver, at navnet **ReportTitle** ikke findes på arket **Ark1** i den Excel-skabelon, du bruger.

    ![Valideringsadvarsel om, at navnet ReportTitle ikke findes på Ark1 i Excel-skabelonen.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Rediger det konfigurerede format ved at fjerne alle de elementer, der refererer til de Excel-navne, som mangler i skabelonen.

#### <a name="option-2"></a>Indstilling 2

[Opdater](er-fillable-excel.md#template-import) det redigerbare ER-format ved at importere en Excel-skabelon. Strukturen af det redigerbare ER-format [synkroniseres](modify-electronic-reporting-format-reapply-excel-template.md) med strukturen af den importerede Excel-skabelon.

### <a name="additional-consideration"></a>Yderligere overvejelser

Hvis du vil vide, hvordan formatstrukturen kan synkroniseres med en ER-skabelon i skabeloneditoren for [styring af forretningsdokumenter](er-business-document-management.md), skal du se [Opdatere strukturen for en forretningsdokumentskabelon](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Ikke synkroniseret med et Word-skabelonformat

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent for at bruge en Word-skabelon til at generere et udgående dokument, kan du tilføje elementet **Excel\\Fil** manuelt, tilføje den ønskede Word-skabelon som en vedhæftet fil til den redigerbare komponent og markere den vedhæftede fil i det tilføjede **Excel\\Fil**-element.

> [!NOTE]
> Når Word-dokumentet er vedhæftet, viser ER-formatdesigneren det element, der kan redigeres, som **Word\\Fil**.

På denne måde angiver du, at det tilføjede element vil udfylde den valgte skabelon på kørselstidspunktet. Da den tilføjede Word-skabelon er designet eksternt, kan det redigerbare ER-format indeholde Word-navne, der mangler i den tilføjede skabelon. ER-formatdesigneren advarer dig om eventuelle uoverensstemmelser mellem egenskaberne for de ER-formatelementer, der refererer til navne, som ikke er medtaget i den tilføjede Word-skabelon.

Du kan se et eksempel på, hvordan dette problem kan forekomme, under [Konfigurere det format, der kan redigeres, hvis du vil udelade oversigtsafsnittet](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Rediger det konfigurerede format ved at slette formlen **Fjernet** fra det formatelement, der nævnes i valideringsadvarslen.

#### <a name="option-2"></a>Indstilling 2

Rediger brug af Word-skabelonen ved at [tilføje](er-design-configuration-word-suppress-controls.md#tag-control) den påkrævede mærkat til det relevante indhold i Word-kontrolelementet.

## <a name="no-default-mapping"></a><a id="i15"></a>Ingen standardtilknytning

Når den [Manglende bindende](#i11) inspektion udføres, evalueres de inspicerede format bindinger i forhold til bindingerne fra den relevante modeltilknytningskomponent. Da du kan importere [flere](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER-modeltilknytningskonfigurationer til din finansforekomst, og hver konfiguration kan indeholde den relevante modeltilknytningskomponent, skal du vælge én konfiguration som standardkonfiguration. Ellers vil der forekomme en undtagelse, når du prøver at køre, redigere eller validere det inspicerede ER-format, og du vil modtage følgende meddelelse: "Der findes mere end én modeltilknytning for \<model name (root descriptor)\> datamodellen i konfigurationerne \<configuration names separated by comma\>. Angiv en af konfigurationerne som standard."

Du kan se et eksempel på, hvordan dette problem kan forekomme, og hvordan det kan rettes, under [Administrer flere afledte tilknytninger for en enkelt modelrod](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Uoverensstemmende indstilling af komponenter i sidehoved eller sidefod

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til at bruge en Excel-skabelon til at generere et udgående dokument, kan du tilføje komponenten **Excel\\overskrift** for at indsætte overskrifter øverst i et regneark i en Excel-projektmappe. Du kan også tilføje komponenten **Excel\\sidefod**, hvis du vil udfylde sidefødder nederst i et regneark. For hver komponent i **Excel\\sidehoved** eller **Excel\\sidefod**, du tilføjer, skal du angive de **Sidehoved-/sidefod**-egenskaber, der skal angive de sider, komponenten skal føres for. Da du kan konfigurere flere komponenter i **Excel\\sidehoved** eller **Excel\\sidefod** til en komponent i et enkelt **ark**, og du kan generere forskellige sidehoveder eller sidefødder til forskellige typer sider i et Excel-regneark, skal du konfigurere en enkelt komponent i **Excel\\sidehoved** eller **Excel\\sidefod** for en bestemt værdi af egenskaben for udseende som **sidehoved/sidefod**. Hvis der er konfigureret mere end én komponent i **Excel\\sidehoved** eller **Excel\\sidefod** til en bestemt værdi af egenskaben for **sidehovedets/sidefodens udseende**, opstår der en valideringsfejl, og du modtager følgende fejlmeddelelse: "Sidehoveder/sidefødder (&lt;komponenttype: sidehoved eller sidefod&gt;) er uoverensstemmende."

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Rediger det konfigurerede format ved at slette en af de uoverensstemmende komponenter **Excel\\sidehoved** eller **Excel\\sidefod**.

#### <a name="option-2"></a>Indstilling 2

Rediger værdien for egenskaben for udseendet af **sidehovedet eller sidefoden** for en af de uoverensstemmende komponenter i **Excel\\sidehoved** eller **Excel\\sidefod**.

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>Uoverensstemmende indstilling af sidekomponent

Når du [konfigurerer](er-fillable-excel.md) en ER-formatkomponent til at bruge en Excel-skabelon til at generere et udgående dokument, kan du tilføje **Excel\\-side** komponenten for at sideopdele et genereret dokument ved at bruge ER-formler. For hver **Excel\\-side**-komponent, du tilføjer, kan du tilføje mange indlejrede [område](er-fillable-excel.md#range-component)-komponenter og stadig være kompatibel med følgende [struktur](er-fillable-excel.md#page-component-structure):

- Den første indlejrede **Område**-komponent kan konfigureres, så egenskaben **Replikeringsretning** angives til **Ingen replikering**. Dette område bruges til at oprette sidehoveder i genererede dokumenter.
- Du kan tilføje mange andre indlejrede **område**-komponenter, hvor egenskaben **Replikeringsretning** er angivet som **Lodret**. Disse områder bruges til at udfylde genererede dokumenter.
- Den sidste indlejrede **Område**-komponent kan konfigureres, så egenskaben **Replikeringsretning** angives til **Ingen replikering**. Dette område bruges til at oprette sidefodsfødder i genererede dokumenter og til at tilføje de nødvendige sideskift.

Hvis du ikke følger denne struktur for et ER-format i ER-formatdesigneren på designtidspunktet, opstår der en valideringsfejl, og du modtager følgende fejlmeddelelse: "Der er mere end to områdekomponenter uden replikering. Fjern unødvendige komponenter."

### <a name="automatic-resolution"></a>Automatisk løsning

Det er ikke muligt at løse dette problem automatisk.

### <a name="manual-resolution"></a>Manuel løsning

#### <a name="option-1"></a>Indstilling 1

Rediger det konfigurerede format ved at ændre egenskaben **Replikeringsretning** for alle uoverensstemmende **Excel\\-område**-komponenter.

## <a name="additional-resources"></a>Yderligere ressourcer

[ER-funktionen ALLITEMS](er-functions-list-allitems.md)

[ER-funktionen ALLITEMSQUERY](er-functions-list-allitemsquery.md)

[ER-funktionen INT64VALUE](er-functions-conversion-int64value.md)

[ER-funktionen INTVALUE](er-functions-conversion-intvalue.md)

[ER-funktionen FILTER](er-functions-list-filter.md)

[ER-funktionen WHERE](er-functions-list-where.md)

[Bruge JOIN-datakilder til at hente data fra flere programtabeller i ER-modeltilknytninger](er-join-data-sources.md)

[Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md)

[Oversigt over styring af forretningsdokumenter](er-business-document-management.md)

[Skjule Word-indhold i genererede rapporter](er-design-configuration-word-suppress-controls.md)

[Administrere flere afledte tilknytninger for en enkelt modelrod](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
