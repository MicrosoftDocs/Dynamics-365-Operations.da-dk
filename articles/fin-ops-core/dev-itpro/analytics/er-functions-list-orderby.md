---
title: ER-funktionen ORDERBY
description: Dette emne indeholder oplysninger om, hvordan funktionen ORDERBY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075168"
---
# <a name="orderby-er-function"></a>ER-funktionen ORDERBY

[!include [banner](../includes/banner.md)]

Funktionen `ORDERBY` returnerer den angivne liste som en *Postliste*-værdi, efter at den er sorteret i henhold til de angivne argumenter. Disse argumenter kan defineres som udtryk.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntaks 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntaks 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Denne syntaks understøttes i Microsoft Dynamics 365 Finance version 10.0.25 og nyere.

## <a name="arguments"></a>Argumenter

`location`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Den placering, hvor sorteringen skal køres. Der findes følgende gyldige indstillinger:

- "Query"
- "InMemory"

`list`: *[Postliste](er-formula-supported-data-types-composite.md#record-list)*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`expression 1`: *Felt*

Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til. Det felt, der refereres til, skal være et felt af den primitive datatype. Dette argument skal udfyldes.

`expression N`: *Felt*

Den gyldige sti til et felt i datakilden, som `list`-argumentet for den kaldte funktion refererer til. Det felt, der refereres til, skal være et felt af den primitive datatype. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Liste over poster*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

### <a name="syntax-1"></a>Syntaks 1

Datasortering udføres altid i hukommelsen på programserveren. Du kan finde flere detaljer i [eksempel 1](#example-1).

### <a name="syntax-2"></a>Syntaks 2

### <a name="sorting-in-memory"></a>Sortering i hukommelsen

Når argumentet `location` angives som **InMemory**, udføres datasortering i hukommelsen på en programserver. Du kan finde flere detaljer i [eksempel 2](#example-2).

### <a name="sorting-in-database"></a>Sortering i database

Når argumentet `location` angives som **Query**, udføres datasortering på databaseniveau. I dette tilfælde skal argumentet `list` pege på en af følgende datakilder for [elektronisk rapportering (ER)](general-electronic-reporting.md), der angiver den programkilde, som en direkte databaseforespørgsel kan oprettes for:

- Datakilde af typen *Tabelposter*
- Relation af en datakilde af typen *Tabelposter*
- Datakilde af typen *Beregnet felt*

Argumenterne `expression 1` og `expression N` skal pege på felter for en ER-datakilde, der angiver de relevante felter i programkilden, som en direkte databaseforespørgsel også kan oprettes for.

Hvis der ikke kan oprettes en direkte databaseforespørgsel, opstår der en [valideringsfejl](er-components-inspections.md#i18) i ER-modeltilknytningsdesigneren. Den meddelelse, du modtager, angiver, at det ER-udtryk, der inkluderer `ORDERBY`-funktionen, ikke kan køres på kørselstidspunktet.

Hvis du vil opnå en bedre ydeevne, anbefales det, at du bruger indstillingen **Query**, når sorteringen konfigureres for programdatakilder, der kan indeholde det store antal poster (f.eks. til tabeller i transaktionsapplikationer).

> [!NOTE]
> Selve `ORDEBY`-funktionen kan ikke oversættes til en direkte databaseforespørgsel. Derfor kan der ikke forespørges på en ER-datakilde, der indeholder denne funktion. Det kan heller ikke bruges i området for ER-funktioner som [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md), hvor der kun kan bruges datakilder, der kan forespørges.

Yderligere oplysninger finder du i [eksempel 3](#example-3) og [eksempel 4](#example-4).

### <a name="comparability"></a>Sammenlignelighed

Da SQL-databaseprogrammet og finansprogramserveren kan bruge en anden rangeringsværdi for et enkelt tegn, kan sorteringsresultatet af samme postliste variere, når et [strengfelt](er-formula-supported-data-types-primitive.md#string) bruges til sortering. Du kan finde flere detaljer i [eksempel 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Eksempel 1: Standardudførelse i hukommelsen

Hvis du indtaster datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("C|B|A", "|")`, returnerer udtrykket `FIRST( ORDERBY( DS, DS. Value)).Value` tekstværdien **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Eksempel 2: Eksplicit udførelse i hukommelsen

Hvis **Vendor** er konfigureret som en datakilde af typen *Tabelposter*, der henviser til tabellen **VendTable**, vil både udtrykket `ORDERBY (Vendor, Vendor.'name()')` og `ORDERBY ("InMemory", Vendor, Vendor.'name()')` returnere en liste over leverandører, der er sorteret efter navn i stigende rækkefølge.

Når du konfigurerer udtrykket i `ORDERBY ("Query", Vendor, Vendor.'name()')` i ER-modeltilknytningsdesigneren, opstår der en [valideringsfejl](er-components-inspections.md#i8) på designtidspunktet, fordi stien `Vendor.'name()'` refererer til en programmetode, der har logik, der ikke kan oversættes til en direkte databaseforespørgsel.

## <a name="example-3-database-query"></a><a name="example-3"></a>Eksempel 3: Databaseforespørgsel

Hvis **TaxTransaction** er konfigureret som en ER-datakilde af *Tabelpost*-typen, der henviser til tabellen **TaxTrans**, sorterer udtrykket `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` poster på programdatabaseniveau og returnerer en liste over momsposteringer, der er sorteret efter momskode i stigende rækkefølge.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Eksempel 4: Datakilder, der kan forespørges på

Hvis **TaxTransaction** er konfigureret som en ER-datakilde for *Tabelpost*-typen, der henviser til tabellen **TaxTrans**, kan ER-datakilden  **TaxTransactionFiltered** konfigureres, så den indeholder udtrykket `FILTER(TaxTransaction, TaxCode="VAT19")`, der skal hente posteringer for en angivet momskode. Da den konfigurerede **TaxTransactionFiltered** ER-datakilde kan forespørges, kan udtrykket `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` konfigureres til at returnere listen over filtrerede momsposteringer, der sorteres efter posteringsdato i stigende rækkefølge.

Hvis du konfigurerer **TaxTransactionOrdered** som en ER-datakilde af typen *Beregnet felt*, som indeholder udtrykket `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)`, og en ER-datakilde af typen *Beregnet felt*, der indeholder udtrykket `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, opstår der en [valideringsfejl](er-components-inspections.md#i18) på designtidspunktet i ER-modeltilknytningsdesigneren. Denne fejl opstår, fordi det første argument for funktionen [FILTER](er-functions-list-filter.md#usage-notes) skal henvise til en ER-datakilde, der kan forespørges på, men den **TaxTransactionOrdered**-datakilde, der indeholder funktionen `ORDERBY`, kan ikke forespørges.

## <a name="example-5-comparability"></a><a name="example-5"></a>Eksempel 5: Sammenlignelighed

### <a name="prerequisites"></a>Forudsætninger

1. Angiv **DS1**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `SPLIT ("D1|_D2|D3", "|")`.
2. Åbn siden **[Økonomiske dimensionsværdier](../../../finance/general-ledger/financial-dimensions.md)**, og vælg dimensionen **CostCenter**.
3. Angiv følgende dimensionsværdier: **D1**, **\_D2** og **D3**.

### <a name="sorting-in-memory"></a>Sortering i hukommelsen

1. Konfigurer **DS2**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Bemærk, at udtrykket `FIRST(DS2).Value` returnerer tekstværdien **"D1"**, udtrykket `INDEX(DS2, COUNT(DS2)).Value` returnerer tekstværdien **"\_D2"**, og udtrykket `STRINGJOIN(DS2, DS2.Value, "|")` returnerer tekstværdien **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>Sortering i database

1. Angiv datakilden **DS3** af typen *Tabelposter*, som refererer til enheden **FinancialDimensionValueEntity**.
2. Konfigurer **DS4**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Konfigurer **DS5**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `ORDERBY(DS4, DS4.DimensionValue)`.
4. Bemærk, at udtrykket `FIRST(DS5).Value` returnerer tekstværdien **"\_D2"**, udtrykket `INDEX(DS5, COUNT(DS5)).Value` returnerer tekstværdien **"D3"**, og udtrykket `STRINGJOIN(DS5, DS5.Value, "|")` returnerer tekstværdien **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
