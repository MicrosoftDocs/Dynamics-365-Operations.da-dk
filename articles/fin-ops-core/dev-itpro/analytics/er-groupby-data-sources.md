---
title: Gruppere poster og aggregere beregninger ved hjælp af GROUPBY-datakilder
description: I dette emne beskrives, hvordan du kan bruge datakilder af GROUPBY-typen i elektronisk rapportering (ER).
author: NickSelin
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075623"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Gruppere poster og aggregere beregninger ved hjælp af GROUPBY-datakilder

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Under konfiguration af [ER-modeltilknytninger](general-electronic-reporting.md) eller -formater kan du [tilføje](#AddMmDataSource2) nødvendige datakilder af **GroupBy**-typen.

På designtidspunktet er en **GroupBy**-datakilde konfigureret til at identificere følgende elementer:

- En [basisdatakilde](#BaseDataSource), der indeholder poster, som skal grupperes under kørsel
- [Grupperingsfelter](#GroupingFields) i basisdatakilden, som bruges til postgruppering under kørsel
- [Aggregatfunktioner](#AggregateFunctions), der angiver de aggregatberegninger, der skal udføres for hver opdaget gruppe under kørslen

Under kørsel grupperer en konfigureret **GroupBy**-datakilde poster, der har samme værdier i grupperingsfelterne, og returnerer en liste over poster. Hver post repræsenterer en enkelt gruppe. Datakilden viser for hver gruppe de feltværdier, som de første poster er grupperet efter, værdierne i de beregnede aggregatfunktioner og listen over poster i den basisdatakilde, der tilhører gruppen.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Aggregatfunktioner

Under kørslen udføres hver aggregatberegning for hver gruppe af poster. Denne beregning udføres ved at bruge værdien på et enkelt felt eller et udtryk i posterne i en datakilde, der blev valgt til gruppering i den redigerbare datakilde af typen **GroupBy**. Følgende aggregatfunktioner understøttes i øjeblikket:

- **AVG** – Denne funktion returnerer gennemsnittet af værdierne i en gruppe. Den kan kun bruges i forbindelse med numeriske felter.
- **COUNT** – Denne funktion returnerer antallet af elementer, der blev fundet i en gruppe.
- **Min** – Denne funktion returnerer minimumværdien mellem værdierne i en gruppe.
- **Max** – Denne funktion returnerer maksimumværdien mellem værdierne i en gruppe.
- **SUM** – Denne funktion returnerer summen af alle værdierne i en gruppe. Den kan kun bruges i forbindelse med numeriske felter.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Sted for udførelse

Når du redigerer en **GroupBy**-datakilde og angiver den basisdatakilde, der indeholder de poster, der skal grupperes, registrerer systemet automatisk den mest effektive [placering](#ExecutionLocation) til udførelsen af den pågældende **GroupBy**-datakilde. Hvis der [kan forespørges](er-functions-list-filter.md#usage-notes) på basisdatakilden (dvs. hvis den kan køres på databaseniveau), angives programdatabasen også som udførelsessted for den **GroupBy**-datakilde, der kan redigeres. Ellers angives programserverens hukommelse som udførelsesplacering.

Du kan manuelt ændre den automatisk registrerede udførelsesplacering ved at vælge den placering, der gælder for den konfigurerede datakilde. Hvis den udførelsesplacering, der er valgt, ikke kan anvendes, vil der blive udløst en [valideringsfejl](er-components-inspections.md#i5) i forbindelse med design.

> [!TIP]
> Det anbefales, at du bruger databaseplaceringen til at gruppere datakilder, der viser et stort antal poster.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Hukommelsesforbrug

Hvis en **GroupBy**-datakilde køres i hukommelsen, bruges programserverens hukommelse som standard til at gemme poster fra den basisdatakilde, der tilhører hver af de fundne grupper, som poster i en enkelt gruppe. For at reducere forbruget af hukommelse kan du udelade lagring af poster for **GroupBy**-datakilder, hvis de er konfigureret til kun at beregne aggregerede funktioner, og deres gruppes poster ikke bruges under kørslen. På denne måde kan du reducere forbruget af hukommelse ved at aktivere funktionen **Reducer hukommelsesforbruget i ER, når gruppering af poster kun bruges til at beregne aggregeringer** i arbejdsområdet **Funktionsstyring**.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternativer

Lignende aggregeringer kan beregnes ved hjælp af [forskellige](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) typer datakilder eller indbyggede ER-funktioner.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet nedenfor.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Eksempel: Gruppere poster og aggregere beregninger ved hjælp af en GROUPBY-datakilde

Dette eksempel viser, hvordan en bruger med rollen Systemadministrator eller Funktionel konsulent for elektronisk rapportering kan konfigurere em ER-modeltilknytning, der har en **GROUPBY**-datakilde, som bruges til at beregne aggregatfunktioner og gruppere poster. Denne modeltilknytning bruges til at udskrive kontrolrapporten, når Intrastat-opgørelsen genereres. Denne rapport giver dig mulighed for at gennemgå rapporterede Intrastat-transaktioner.

Procedurerne i dette eksempel kan fuldføres for **DEMF**-firmaet i Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Forberede eksempeldata

Du skal først sørge for, at du har Intrastat-transaktioner til rapportering på **Intrastat**-siden. Du skal have posteringer for forskellige transportkoder, da du skal gruppere posteringer efter feltet **Transport** i dette eksempel.

![Forberede Intrastat-posteringer på Intrastat-siden.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at designe en ER-modeltilknytning.

### <a name="import-the-standard-er-format-configuration"></a>Importere standardkonfigurationen af ER-format

Følg trinnene i [Importere standardkonfigurationen af ER-format](er-quick-start2-customize-report.md#ImportERSolution1) for at føje ER-standardkonfigurationerne til den aktuelle forekomst af Dynamics 365 Finance. Importér version 1 af konfigurationen **Intrastat-model** fra lageret.

### <a name="create-a-custom-data-model-configuration"></a>Oprette en brugerdefineret datamodelkonfiguration

Benyt fremgangsmåden i [Tilføje en brugerdefineret datamodelkonfiguration](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) for manuelt at tilføje en ny **Intrastat-model (Litware)** som ER-datamodelkonfiguration, som du udleder af den importerede **Intrastat-modelkonfiguration**.

### <a name="configure-a-custom-data-model-component"></a>Konfigurere en brugerdefineret datamodelkomponent

Følg disse trin for at foretage de nødvendige ændringer af den afledte **Intrastat-model (Litware)**-datamodel, så den kan bruges til at vise transportkoder, der indeholder de nødvendige oplysninger.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet vælge **Intrastat-model (Litware)**.
3. Vælg **Designer**.
4. Vælg **Intrastat** i modeltræet på siden **Datamodeldesigner**.
5. Vælg **Ny** for at tilføje en ny indlejret node for den valgte **Intrastat**-node. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. I feltet **Navn** skal du angive **Transport**.
    2. Vælg **Liste over poster** i feltet **Varetype**.
    3. Vælg **Tilføj** for at tilføje en ny node.

6. Vælg **Ny** for at tilføje en ny indlejret node til den **Transport**-node, du netop har tilføjet. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. Angiv **Kode** i feltet **Navn**.
    2. Vælg **Streng** i feltet **Varetype**.
    3. Vælg **Tilføj** for at tilføje en ny node.

7. Vælg **Ny** for at tilføje endnu en indlejret node til **Transport**-noden. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. I feltet **Navn** skal du angive **TotalInvoicedAmount**.
    2. Vælg **Kommatal** i feltet **Varetype**.
    3. Vælg **Tilføj** for at tilføje en ny node.

8. Vælg **Ny** for at tilføje endnu en indlejret node til **Transport**-noden. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. Angiv **NumberOfTransactions** i feltet **Navn**.
    2. Vælg **Heltal** i feltet **Elementtype**.
    3. Vælg **Tilføj** for at tilføje en ny node.

9. Vælg **Ny** for at tilføje endnu en indlejret node til **Transport**-noden. Udfør følgende fremgangsmåde i rulledialogboksen til tilføjelse af en datamodelnode:

    1. I feltet **Navn** skal du angive **Transaktion**.
    2. Vælg **Liste over poster** i feltet **Varetype**.
    3. Vælg **Tilføj** for at tilføje en ny node.

10. Vælg **Skift varereference** for den **Transaktion**-node, du netop har tilføjet, i oversigtspanelet **Node**.
11. Vælg **CommodityRecord** i datamodeltræet i dialogboksen **Skift varereference**. Vælg derefter **OK**.

![Konfigureret datamodel i ER-datamodeldesigneren.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Fuldføre designet af den brugerdefinerede datamodel

Udfør trinnene i [Fuldføre designet af datamodellen](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) for at færdiggøre designet af den afledte datamodel **Intrastat-model (Litware)**.

### <a name="create-a-new-model-mapping-configuration"></a>Oprette en ny konfiguration af modeltilknytning

Benyt fremgangsmåden i [Oprette en ny konfiguration af modeltilknytning](er-quick-start1-new-solution.md#CreateModelMapping) for manuelt at tilføje en ny **Intrastat-eksempeltilknytning** som ER-modelkonfiguration for den afledte **Intrastat-model (Litware)**-konfiguration.

### <a name="add-a-new-model-mapping-component"></a>Tilføje en ny modeltilknytningskomponent

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet udvide konfigurationen **Intrastat-model**.
3. Vælg konfigurationen **Tilknytning af Intrastat-eksempel**.
4. Vælg **Designer** for at åbne listen over tilknytninger.
5. Vælg **Slet** for at fjerne den eksisterende tilknytningskomponent.
6. Vælg **Ny** for at tilføje en ny komponent.
7. I feltet **Definition** skal du vælge **Intrastat**.
8. Angiv **Intrastat-tilknytning** i feltet **Navn**.
9. Vælg **Designer** for at konfigurere den nye tilknytning.

### <a name="design-the-added-model-mapping-component"></a>Designe den tilføjede komponent til modeltilknytning

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Tilføje en datakilde for at få adgang til en programtabel

Du skal konfigurere datakilder for at få adgang til de programtabeller, der indeholder detaljerne om Intrastat-transaktioner.

1. Vælg **Dynamics 365 for Operations\\Tabelposter** på siden **Modeltilknytningsdesigner** i ruden **Datakildetyper**.
2. Vælg **Tilføj rod** i ruden **Datakilder** for at tilføje en ny datakilde, der skal bruges til at få adgang til **Intrastat**-tabellen. Hver post i **Intrastat**-tabellen repræsenterer en enkelt Intrastat-transaktion.
3. Angiv **Transaktion** i feltet **Navn** i dialogboksen **Egenskaber for datakilde**.
4. Indtast **Intrastat** i feltet **Tabel**.
5. Vælg **OK** for at tilføje den nye datakilde.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Føje en datakilde til gruppering af Intrastat-posteringer

Konfigurer en **GroupBy**-datakilde for at gruppere Intrastat-posteringer og beregne aggregatfunktioner.

1. Vælg **Funktioner\\Gruppér efter** i ruden **Datakildetyper** på siden **Modeltilknytningsdesigner**.
2. Vælg **Tilføj rod** i ruden **Datakilder** for at tilføje en ny datakilde, der skal bruges til at gruppere Intrastat-transaktioner og beregne aggregatfunktioner.
3. Angiv **TransportRecord** i feltet **Navn** i dialogboksen **Egenskaber for datakilde**.
4. Vælg **Rediger gruppér efter** for at konfigurere grupperingsbetingelser.
5. På siden **Rediger 'Gruppér efter'-parametre** på listen over datakilder i højre rude skal du vælge datakilden **Transaktion** og udvide den.
6. Vælg **Føj felt til \> Hvad skal grupperes** for at angive, at datakilden **Transaktion** er valgt som <a name="BaseDataSource">basisdatakilde</a> for den konfigurerede **GroupBy**-datakilde. Posterne i datakilden **Transaktion** grupperes, og feltværdierne i denne datakilde bruges til beregninger i aggregatfunktioner.
7. Markér feltet **Transaktion\Transport**, og vælg derefter **Føj felt til \> Feltet Grupperet** for at angive,at **Transport**-feltet for basisdatakilden er valgt som <a name="GroupingFields">grupperingskriterium</a> for den konfigurerede **GroupBy**-datakilde. Det vil sige, at posterne i datakilden **Transaktion** grupperes på basis af værdien i feltet **Transport**. Alle poster i den konfigurerede **GroupBy**-datakilde vil repræsentere en enkelt transportkode, der findes i poster i basisdatakilden.
8. Markér feltet **Transaction\AmountMST**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Føj felt til \> Aggregatfelter** for at angive, at der skal beregnes en <a name="AggregateFunctions">aggregatfunktion</a> for dette felt.
    2. Vælg funktionen **Sum** i feltet **Metode** i den post, der er føjet til det valgte felt **Transaction\AmountMST** i ruden **Aggregeringer**.
    3. I feltet **Navn** skal du angive **TotalInvoicedAmount**.

    Disse indstillinger angiver, at for hver transportgruppe beregnes det samlede beløb i feltet **Transaction\AmountMST**.

9. Markér feltet **Transaction\RecId**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Føj felt til \> Aggregatfelter** for at angive, at der skal beregnes en aggregatfunktion for dette felt.
    2. Vælg funktionen **Antal** i feltet **Metode** i den post, der er føjet til det valgte felt **Transaction\RecId** i ruden **Aggregeringer**.
    3. I feltet **Navn** skal du angive **NumberOfTransactions**.

    Disse indstillinger angiver, at for hver transportgruppe beregnes antallet af transaktioner i gruppen.

10. Vælg **Gem**.
11. Gennemgå <a name="ExecutionLocation">udførelsesparametrene</a> for den datakilde, der kan redigeres. Bemærk, at **Automatisk søgning** er valgt automatisk i feltet **Udførselssted**, og feltet **Udførelse ved** indeholder værdien **SQL**. Disse indstillinger angiver, at den valgte **Transaktion**-basisdatakilde i øjeblikket kan forespørges på, og du kan køre den **GroupBy**-datakilde, der kan redigeres, på databaseniveau.
12. Åbn opslaget for feltet **Udførselssted** for at gennemse listen over tilgængelige værdier. Bemærk, at du kan vælge **Forespørgsel** eller **I hukommelse** for at tvinge denne **GroupBy**-datakilde til at blive kørt på databaseniveau eller i programserverens hukommelse.
13. Vælg **Gem**, og luk derefter siden **Rediger 'Gruppér efter'-parametre**.
14. Vælg **OK** for at udføre indstillingerne for **GroupBy**-datakilden.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>Binde GroupBy-datakilden til datamodelfelter

Bind den konfigurerede datakilde til felterne i datamodellen for at angive, hvordan datamodellen skal udfyldes med programdata under kørsel.

1. Udvid noden **Transport** på siden **Modeltilknytningsdesigner** i ruden **Datamodel**.
2. Udvid datakilden **TransportRecord** i ruden **Datakilder**.
3. Tilføj en binding for at vise listen over fundne transportgrupper:

    1. Vælg **Transport** i ruden **Datamodel**.
    2. Vælg datakilden **TransportRecord** i ruden **Datakilder**.
    3. Vælg **Bind**.

4. Tilføj en binding for at vise transportkoden for hver fundne transportgruppe:

    1. Vælg datamodelelementet **Transport.Code**.
    2. Vælg det grupperede felt **TransportRecord.grouped.TransportMode**.
    3. Vælg **Bind**.

5. Tilføj en binding for at vise værdierne af beregnede aggregatfunktioner for hver opdaget transportgruppe:

    1. Vælg datamodelelementet **Transport.NumberOfTransactions**.
    2. Vælg det aggregerede felt **TransportRecord.aggregated.NumberOfTransactions**.
    3. Vælg **Bind**.
    4. Vælg datamodelelementet **Transport.TotalInvoicedAmount**.
    5. Vælg det aggregerede felt **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Vælg **Bind**.

6. Tilføj en binding, der viser transaktionsposter, der tilhører hver af de fundne transportgrupper:

    1. Vælg datamodelelementet **Transport.Transaction**.
    2. Vælg feltet **TransportRecord.lines**.
    3. Vælg **Bind**.

    Du kan fortsætte med at konfigurere bindinger for de indlejrede elementer i datamodelelementet **Transport.Transaction** og datakildefeltet **TransportRecord.lines** for at vise oplysninger om Intrastat-posteringer, der tilhører hver enkelt opdaget transportgruppe, under kørslen.

![Konfigureret modeltilknytning i ER-modeltilknytningsdesigneren.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Foretage fejlfinding af den tilføjede komponent til modeltilknytning

Brug [ER-datakildefejlfindingen](er-debug-data-sources.md) til at teste den konfigurerede modeltilknytning.

1. Vælg **Start fejlfinding** på siden **Modeltilknytningsdesigner**.
2. I ruden til venstre på siden **Foretag fejlfinding af datakilder** skal du vælge datakilden **TransportRecord** og derefter vælge **Læs alle poster**.
3. Udvid datakilden **TransportRecord**, og benyt derefter følgende fremgangsmåde:

    1. Vælg datakilden **TransportRecord.grouped.TransportMode**.
    2. Vælg **Hent værdi**.
    3. Vælg datakilden **TransportRecord.grouped.NumberOfTransactions**.
    4. Vælg **Hent værdi**.
    5. Vælg datakilden **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Vælg **Hent værdi**.

4. Vælg **Udvid alle** i højre rude.

Datakilden **TransportRecord** viser to poster og præsenterer to transportkoder. Antallet af posteringer og det samlede fakturerede beløb beregnes for hver transportkode.

> [!NOTE]
> Tilgangen "lazy reading" (afslappet lægning) bruges, når en **GroupBy**-datakilde kaldes for at optimere databasekald. Derfor beregnes nogle af feltværdierne i en **GroupBy**-datakilde kun i ER-datakilders fejlfindingsprogram, når de er bundet til datamodelfelter.

![Resultater af fejlfinding af datakilden på siden Foretag fejlfinding af datakilder.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Er der nogen måde at beregne samlede totaler på, når gruppetotalerne beregnes?

Ja. Hvis du vil beregne samlede totaler, skal du konfigurere en anden **GroupBy**-datakilde, hvor den **GroupBy**-datakilde, du tidligere konfigurerede, bruges som basisdatakilde. I følgende illustration vises datakilden **Totaler** for typen **GroupBy**, som bruges til at beregne den samlede **SUM**-funktion på baggrund af **SUM**-aggregeringen af **TransportRecord**-datakilden for typen **GroupBy**.

![Datakilden Totaler i ER-modeltilknytningsdesigneren.](./media/er-groupby-data-sources-configure-model-mapping2.png)

I følgende illustration vises resultaterne af fejlfinding af datakilden **Totaler**.

![Resultater af fejlfinding af datakilden Totaler på siden Foretag fejlfinding af datakilder.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Fejlfinde datakilder for et udført ER-format for at analysere dataflow og -transformering](er-debug-data-sources.md)
- [Bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
