---
title: Designe et ER-format til sideinddeling af genererede dokumenter i Excel
description: Dette emne forklarer, hvordan du designer en et elektronisk rapporteringsformat (ER), der sideinddeler et genereret dokument i Microsoft Excel.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: ce29225c4bce24adc2abefc3d3d6f20774852af4
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488333"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Designe et ER-format til sideinddeling af genererede dokumenter i Excel

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan en bruger i rollen Systemadministrator eller Funktionel konsulent i elektronisk rapportering kan konfigurere et [ER-format (elektronisk rapportering)](general-electronic-reporting.md), så der genereres udgående dokumenter i Microsoft Excel og administreres sideinddeling af dokumenter.

I dette eksempel skal du redigere det ER-format, der leveres af Microsoft, og som bruges til at udskrive kontrolrapporten, når Intrastat-opgørelsen [genereres](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Denne rapport giver dig mulighed for at observere rapporterede Intrastat-transaktioner. Dine ændringer vil give dig mulighed for at administrere sideinddelingen af kontrolrapporter, der genereres.

Procedurerne i dette emne kan fuldføres i **DEMF**-firmaet. Der kræves ingen kodning. Før du begynder, skal du hente og gemme følgende filer.

| Betegnelse       | Filnavn |
|-------------------|-----------| 
| Rapportskabelon 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Rapportskabelon 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Konfigurere ER-strukturen

Følg trinnene i [Konfigurere ER-strukturen](er-quick-start2-customize-report.md#ConfigureFramework) for at konfigurere det minimale sæt af ER-parametre. Du skal fuldføre denne opsætning, før du begynder at bruge ER-strukturen til at designe en tilpasset version af et ER-standardformat.

## <a name="import-the-standard-er-format-configuration"></a>Importere standardkonfigurationen af ER-format

Følg trinnene i [Importere standardkonfigurationen af ER-format](er-quick-start2-customize-report.md#ImportERSolution1) for at føje ER-standardkonfigurationerne til den aktuelle forekomst af Dynamics 365 Finance. Importér version **1.9** af **Intrastat-rapportens** formatkonfiguration. Basisversion 1 af **Intrastat-modellens** konfiguration importeres automatisk fra lageret.

## <a name="customize-the-standard-er-format"></a>Tilpasse standard-ER-formatet

### <a name="create-the-custom-er-format"></a>Oprette det brugerdefinerede ER-format

I dette scenario er du repræsentant for Litware, Inc. som aktuelt er valgt som den aktive ER-konfigurationsudbyder. Du skal oprette en ny ER-formatkonfiguration ved at bruge **Intrastat-rapport**-konfigurationen som basis.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Intrastat-model** og vælge **Intrastat-rapport**. Litware, Inc. vil bruge version 1.9 af denne ER-formatkonfiguration som basis for den brugerdefinerede version.
3. Vælg **Opret konfiguration** for at åbne dialogboksen med rullemenu. Du kan bruge denne dialogboks til at oprette en ny konfiguration for et brugerdefineret betalingsformat.
4. I feltet **Ny** skal du vælge indstillingen **Afledt fra navn: Intrastat-rapport, Microsoft**.
5. I feltet **Navn** skal du angive **Intrastat-rapport Litware**.
6. Vælg **Opret konfiguration** for at oprette det nye format.

Version 1.9.1 af **Intrastat-rapport Litware** ER-formatkonfiguration er oprettet. Denne version har [statussen](general-electronic-reporting.md#component-versioning) **Kladde** og kan redigeres. Det aktuelle indhold af det brugerdefinerede ER-format svarer til indholdet af det format, der er leveret af Microsoft.

### <a name="make-the-custom-format-runnable"></a>Gøre det brugerdefineret format kørbart

Nu, hvor den første version af det brugerdefinerede format er blevet oprettet og har statussen **Kladde**, kan du køre formatet til testformål. Hvis du vil køre rapporten, skal du behandle en kreditorbetaling ved hjælp af den betalingsmåde, der refererer til det brugerdefinerede ER-format. Som standard er det kun versioner, der har statussen **Fuldført** eller **Delt** der [tages i betragtning](general-electronic-reporting.md#component-versioning), når du kalder et ER-format fra applikationen. Denne funktionsmåde er med til at forhindre, at ER-formater med uafsluttede design bliver brugt. Men når det gælder dine testkørsler, kan du tvinge programmet til at bruge den version af dit ER-format, der har statussen **Kladde**. På denne måde kan du justere den aktuelle formatversion, hvis der kræves ændringer. Du kan finde flere oplysninger under [Anvendelighed](electronic-reporting-destinations.md#applicability).

Hvis du vil bruge kladdeversionen af et ER-format, skal du eksplicit markere ER-formatet.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.
4. Vælg **Rediger** for at gøre den aktuelle side redigerbar efter behov.
5. Vælg **Intrastat-rapport Litware** i konfigurationstræet i ruden til venstre.
6. Angiv indstillingen **Kør kladde** til **Ja**, og vælg derefter **Gem**.

    ![Indstillingen Kør kladde på siden Konfigurationer.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Konfigurere udenrigshandelsparametre for at bruge det tilpassede ER-format

Følg disse trin for at konfigurere parametre for udenrigshandel, så du kan bruge det brugerdefinerede format.

1. Gå til **Moms** \> **Konfiguration** \> **Udenrigshandel** \> **Udenrigshandelsparametre**.
2. På siden **Parametre for udenrigshandel** skal du i feltet **Tilknytning af filformat** vælge **Intrastat-rapport Litware** i oversigtspanelet **Elektronisk rapportering**.
3. Vælg **Intrastat-rapport Litware** i feltet **Rapportformattilknytning**.
4. Vælg **Gem**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Konfigurere det brugerdefinerede format til at bruge den hentede rapportskabelon

### <a name="review-the-first-downloaded-excel-template"></a>Gennemse den første hentede Excel-skabelon

1. Åbn skabelonfilen **ERIntrastatReportDemo1.xlsx**, som du downloadede tidligere, i Excel-skrivebordsprogrammet.
2. Kontrollér, at skabelonen indeholder navngivne områder, som du kan bruge til at oprette rapporthoved, rapportdetaljer og sidefodsafsnit i genererede dokumenter.

    ![Layout af Excel-skabelon 1 i skrivebordsprogrammet.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Erstat den aktuelle Excel-skabelon i det brugerdefinerede ER-format

Du skal føje en ny Excel-skabelon til det brugerdefinerede ER-format.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Intrastat-model** \> **Intrastat-rapport** og vælge konfigurationen **Intrastat-rapport Litware**.
3. Vælg **Designer**.
4. I handlingsruden på siden **Formatdesigner** skal du vælge **Vis detaljer**.
5. Kontrollér, at komponenten til **Intrastat: Excel**-rodformat er valgt, og vælg derefter **Opdater fra Excel** under fanen **Import** i handlingsruden i gruppen **Import**.
6. Vælg **Opdater skabelon** i dialogboksen **Opdater fra Excel**.
7. I dialogboksen **Åbn** skal du gå til og vælge filen **ERIntrastatReportDemo1.xlsx**, du hentede tidligere, og vælge **Åbn**.
8. Vælg **OK**.
9. Vælg **Gem**.

![Formatstruktur i ER-formatdesigneren, når den nye Excel-skabelon er tilføjet.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Ændre databindingen for at få vist varebeskrivelsen i en genereret rapport

1. Vælg fanen **Tilknytning** på siden **Formatdesigner**.
2. Udvid **Intrastat** \> **Rapportlinjer**, og vælg komponenten **Varekode**.
3. Vælg **Rediger formel**.
4. Skift bindingsformel fra `@.CommodityCode` til `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Vælg **Gem**.

![Konfigureret binding til visning af varebeskrivelsen i ER-formatdesigneren.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Generere en kontrolrapport til Intrastat-opgørelse

Du skal først sørge for, at du har Intrastat-transaktioner til rapportering på **Intrastat**-siden.

![Transaktioner på Intrastat-siden.](./media/er-paginate-excel-reports-transactions1.gif)

Brug derefter det brugerdefinerede ER-format til at generere kontrolrapporten til Intrastat-opgørelsen.

1. Gå til **Moms** \> **Opgørelser** \> **Udenrigshandel** \> **Intrastat**.
2. Vælg **Output** \> **Rapport** i handlingsruden på siden **Intrastat**.
3. Benyt følgende fremgangsmåde i dialogboksen **Intrastat-rapport** for at køre rapporten:

    1. Angiv felterne **Fra dato** og **Til dato** for at medtage specifikke Intrastat-transaktioner i rapporten.
    2. Angiv indstillingen **Generér fil** til **Nej**.
    3. Angiv indstillingen **Generer rapport** til **Ja**.
    4. Vælg **OK**.

4. Download og gem det dokument, der er oprettet.
5. Åbn dokumentet i Excel, og gennemgå det.

    ![Genereret Excel-dokument i skrivebordsprogrammet.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Konfigurere det brugerdefinerede format til sideinddeling af genererede dokumenter

### <a name="review-the-second-downloaded-excel-template"></a>Gennemse den anden hentede Excel-skabelon

1. Åbn skabelonfilen **ERIntrastatReportDemo2.xlsx**, som du downloadede tidligere, i Excel.
2. Sammenlign skabelonen med **ERIntrastatReportDemo1.xlsx**-skabelonen, og kontrollér, at den indeholder flere nye Excel-navne for at oprette og udfylde sidespecifikke sektioner i genererede dokumenter:

    - Området **ReportPageHeader** tilføjes for at oprette sidehoveder.
    - Området **ReportPageFooter** tilføjes for at oprette sidefødder.
    - Cellen **ReportPageFooter\_PageLines** er konfigureret til at vise antallet af transaktioner pr. side.
    - Cellen **ReportPageFooter\_PageAmount** er konfigureret til at vise det samlede beløb af transaktioner pr. side.
    - Cellen **ReportPageFooter\_PageWeight** er konfigureret til at vise den samlede vægt af transaktioner pr. side.
    - Cellen **ReportPageFooter\_RunningCounterLines** er konfigureret til at vise den løbende tæller for transaktioner fra starten af rapporten til den aktuelle side.
    - Cellen **ReportPageFooter\_RunningTotalAmount** er konfigureret til at vise den løbende beløbstotal for alle transaktioner fra starten af rapporten til den aktuelle side.
    - Cellen **ReportPageFooter\_RunningTotalWeight** er konfigureret til at vise den løbende vægttotal for alle transaktioner fra starten af rapporten til den aktuelle side.

    ![Layout af Excel-skabelon 2 i skrivebordsprogrammet.](./media/er-paginate-excel-reports-template2a.gif)

    Cellen **CommodityCode** i denne skabelon er konfigureret til at ombryde celletekst. Da rækken med transaktionsoplysninger er konfigureret, så den automatisk passer til en rækkes højde, skal hele rækkens højde ændres automatisk, når teksten i cellen **CommodityCode** ombrydes.

    ![CommodityCode-celle, der er konfigureret til at ombryde celletekst.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Gentage erstatningen af den aktuelle Excel-skabelon i det brugerdefinerede ER-format

1. Følg trinnene i afsnittet [Erstatte den aktuelle Excel-skabelon i det brugerdefinerede ER-format](#replace-template) i dette emne. I trin 7 skal du dog vælge **ERIntrastatReportDemo2.xlsx**-filen.
2. På siden **Formatdesigner** skal du udvide **Intrastat**.
3. Navngiv de [Område](er-fillable-excel.md#range-component)-formatkomponenter, der er føjet til det redigerbare ER-format for at synkronisere strukturen med strukturen i den anvendte Excel-skabelon:

    1. Vælg den **Område**-komponent, der er tilknyttet Excel-navnet **ReportPageHeader**.
    2. Angiv **Rapportsidehoved** i feltet **Navn** under fanen **Format**.
    3. Vælg den **Område**-komponent, der er tilknyttet Excel-navnet **ReportPageFooter**.
    4. Angiv **Rapportsidefod** i feltet **Navn** under fanen **Format**.

4. Vælg **Gem**.

![Formatstruktur i ER-formatdesigneren, når den nye Excel-skabelon er erstattet.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Ændre formatstrukturen for at implementere sideinddeling af dokument

1. Vælg **Intrastat**-rodkomponenten i formattræet i venstre rude på siden **Formatdesigner**.
2. Vælg **Tilføj**.
3. Vælg [Side](er-fillable-excel.md#page-component)-komponenten i gruppen af **Excel**-komponenter i dialogboksen **Tilføj**.
4. I dialogboksen **Komponentegenskaber** skal du i feltet **Navn** angive **Rapportside**. Vælg derefter **OK**.
5. Hvis du vil bruge **Rapportsidehoved**-komponenten som sidehoved på hver genereret side, skal du følge disse trin:

    1. Vælg komponenten **Rapportsidehoved**, og vælg derefter **Klip**.
    2. Vælg komponenten **Rapportside**, og vælg derefter **Sæt ind**.
    3. Udvid **Rapportside**.
    4. Hvis du vil tvinge **Side**-komponenten til at [betragte](er-fillable-excel.md#page-component-structure) dette område som sidehoved, skal du vælge **Rapportsidehoved** og derefter vælge **Ingen replikering** i feltet **Replikeringsretning** under fanen **Format**.

6. Hvis du vil sideinddele et genereret dokument, så indholdet på rapportlinjerne tages i betragtning, skal du følge disse trin:

    1. Vælg komponenten **Rapportlinjer**, og vælg derefter **Klip**.
    2. Vælg komponenten **Rapportside**, og vælg derefter **Sæt ind**.

7. Hvis du vil medtage rapportsidefoden efter rapportlinjer, men før den sidste sidefod, skal du følge disse trin:

    1. Vælg komponenten **Rapportsidefod**, og vælg derefter **Klip**.
    2. Vælg komponenten **Rapportside**, og vælg derefter **Sæt ind**.

8. Hvis du vil bruge **Rapportsidefod**-komponenten som sidefod på hver genereret side, skal du følge disse trin:

    1. Vælg komponenten **Rapportsidefod**, og vælg derefter **Klip**.
    2. Vælg komponenten **Rapportside**, og vælg derefter **Sæt ind**.
    3. Hvis du vil tvinge **Side**-komponenten til at [betragte](er-fillable-excel.md#page-component-structure) dette område som sidefod, skal du vælge **Rapportsidefod** og derefter vælge **Ingen replikering** i feltet **Replikeringsretning** under fanen **Format**.

![Formatstruktur i ER-formatdesigneren, når sideinddeling af dokument er implementeret.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Tilføje datakilder for at beregne sidefodstotaler

Du skal konfigurere nye datakilder for at beregne sidetotalen, den løbende tæller og værdier for løbende total og for at få dem vist i sidefodssektionen. Det anbefales, at du bruger [Dataindsamling](er-data-collection-data-sources.md) som datakilder til dette formål.

1. Vælg fanen **Tilknytning** på siden **Formatdesigner**.
2. Vælg **Tilføj rod**, og følg derefter følgende fremgangsmåde:

    1. Vælg **Tom container** i sektionen **Generelt** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Total** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for tom container**.
    3. Vælg **OK**.

3. Vælg datakilden **Total**, vælg **Tilføj**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Tom container** i sektionen **Generelt** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Side** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for tom container**.
    3. Vælg **OK**.

4. Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:

    1. Vælg **Tom container** i sektionen **Generelt** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Løbende** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for tom container**.
    3. Vælg **OK**.

5. Vælg datakilden **Total.Page**, vælg **Tilføj**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Beløb** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    3. Vælg **Kommatal** i feltet **Varetype**.
    4. Angiv indstillingen **Indsaml alle værdier** til **Ja**.
    5. Vælg **OK**.

6. Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:

    1. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Vægt** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    3. Vælg **Kommatal** i feltet **Varetype**.
    4. Angiv indstillingen **Indsaml alle værdier** til **Ja**.
    5. Vælg **OK**.

7. Vælg datakilden **Total.Running**, vælg **Tilføj**, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Beløb** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    3. Vælg **Kommatal** i feltet **Varetype**.
    4. Angiv feltet **Indsaml alle værdier** til **Ja**.
    5. Vælg **OK**.

8. Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:

    1. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Vægt** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    3. Vælg **Kommatal** i feltet **Varetype**.
    4. Angiv feltet **Indsaml alle værdier** til **Ja**.
    5. Vælg **OK**.

9. Vælg **Tilføj** igen, og følg derefter følgende fremgangsmåde:

    1. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
    2. Angiv **Linjer** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
    3. Vælg **Heltal** i feltet **Elementtype**.
    4. Angiv feltet **Indsaml alle værdier** til **Ja**.
    5. Vælg **OK**.

10. Vælg **Gem**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Tilføje datakilder for at kontrollere synlighed af sidefod

Hvis du har planer om at kontrollere synlighed af sidefod, og du ikke planlægger at medtage sidefoden på den sidste side, hvis den indeholder transaktioner, skal du konfigurere en ny datakilde for at beregne den påkrævede løbende tæller.

1. Vælg fanen **Tilknytning** på siden **Formatdesigner**.
2. Vælg **Total.Running** som datakilde, og vælg **Tilføj**.
3. Vælg **Dataindsamling** i sektionen **Funktioner** i dialogboksen **Tilføj datakilde**.
4. Angiv **Linjer2** i feltet **Navn** i dialogboksen **Egenskaber for datakilde for dataindsamling**.
5. Vælg **Heltal** i feltet **Elementtype**.
6. Angiv indstillingen **Indsaml alle værdier** til **Ja**.
7. Vælg **OK**.
8. Vælg **Gem**.

![Tilføjede datakilder i ER-formatdesigneren.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Konfigurere bindinger til indsamling af totalværdier

1. På siden **Formatdesigner** skal du udvide komponenten **Rapportlinjer** i formattræet og vælge den indlejrede **Fakturaværdi**-komponent.
2. Vælg **Rediger formel**.
3. Skift bindingsformel fra `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` til `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Udover at placere beløbsværdien i en Excel-celle for hver gentagen transaktion indsamler denne binding værdien i datasamlingen **Total.Page.Amount** for datakilden.

4. Vælg den indlejrede **Vægt**-komponent.
5. Vælg **Rediger formel**.
6. Skift bindingsformel fra `@.'$RoundedWeight'` til `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Udover at placere vægtværdien i en Excel-celle for hver gentagen transaktion indsamler denne binding værdien i **Total.Page.Weight**-datakilden.

![Konfigurerede bindinger til indsamling af totalværdier i ER-formatdesigneren.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Konfigurere bindinger til at udfylde sidefodstotaler

1. På siden **Formatdesigner** skal du i formattræet udvide komponenten **Rapportsidefod**, vælge den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_PageAmount**, og derefter følge disse trin:

    1. Vælg elementet **Total.Page.Amount.Sum()** i datakildetræet i højre rude.
    2. Vælg **Bind**.
    3. Vælg **Rediger formel**.
    4. Opdater formlen til `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Du skal angive argumentet for denne funktion som **Falsk** for at beholde de indsamlede data for den aktuelle side, da disse data er nødvendige for at beregne den løbende beløbstotal, det samlede antal linjer pr. side og linjetælleren.

2. Vælg den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_PageWeight**, i formattræet, og benyt derefter følgende fremgangsmåde:

    1. Vælg elementet **Total.Page.Weight.Sum()** i datakildetræet i højre rude.
    2. Vælg **Bind**.
    3. Vælg **Rediger formel**.
    4. Opdater formlen til `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Konfigurere bindinger til at udfylde løbende sidetotaler

1. På siden **Formatdesigner** skal du i formattræet udvide komponenten **Rapportsidefod**, vælge den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_RunningTotalAmount**, og derefter følge disse trin:

    1. Vælg elementet **Total.Running.Amount.Collect()** i datakildetræet i højre rude.
    2. Vælg **Bind**.
    3. Vælg **Rediger formel**.
    4. Opdater formlen til `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > Operanden `Total.Running.Amount.Sum(false)` returnerer den tidligere indsamlede løbende beløbstotal. Operanden `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` returnerer det samlede beløb på den aktuelle side. Du skal angive argumentet for den indlejrede funktion for den anden operand som **Sand** for at nulstille dataindsamlingen `Total.Page.Amount`, så snart denne værdi sættes i den løbende indsamling af total `Total.Running.Amount`. Det angivne argument skal starte med at opsamle den næste sidetotal fra en værdi på 0 (nul).
    >
    > Funktionen `Total.Running.Amount.Sum(false)` kaldes for at angive den løbende beløbstotal i Excel-cellen **ReportPageFooter\_RunningTotalAmount** på den aktuelle side.

2. Vælg den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_RunningTotalWeight**, i formattræet, og benyt derefter følgende fremgangsmåde:

    1. Vælg elementet **Total.Running.Weight.Collect()** i datakildetræet i højre rude.
    2. Vælg **Bind**.
    3. Vælg **Rediger formel**.
    4. Opdater formlen til `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Konfigurere bindinger til at udfylde løbende sidetæller

1. På siden **Formatdesigner** skal du i formattræet udvide komponenten **Rapportsidefod** og vælge den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_RunningCounterLines**.
2. Vælg **Rediger formel**.
3. Tilføj formlen `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Denne formel returnerer antallet af indsamlede beløbsværdier for hele rapporten. Dette antal svarer til antallet af transaktioner, der er blevet gentaget på det aktuelle tidspunkt. Samtidig indsamler formlen den returnerede værdi i samlingen **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Konfigurere bindinger til at udfylde sidefodstælleren

1. På siden **Formatdesigner** skal du i formattræet udvide komponenten **Rapportsidefod** og vælge den indlejrede **Område**-komponent, der henviser til Excel-cellen **ReportPageFooter\_PageLines**.
2. Vælg **Rediger formel**.
3. Tilføj formlen `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Denne formel beregner antallet af transaktioner på den aktuelle side som forskellen mellem antallet af transaktioner, der er indsamlet i **Total.Page.Amount.Result** for hele rapporten, og antallet af transaktioner, der er gemt på dette stadie i **Total.Running.Lines.Sum**. Da antallet af transaktioner for den aktuelle side er gemt i **Total.Running.Lines** i bindingen af **Område**-komponenten, der henviser til Excel-cellen **ReportPageFooter\_RunningCounterLines**, er antallet af transaktioner på den aktuelle side endnu ikke medtaget. Derfor er denne difference lig med antallet af transaktioner på den aktuelle side.

![Konfigurerede bindinger til udfyldelse af sidefodstælleren i ER-formatdesigneren.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Konfigurere komponentsynlighed

Du kan ændre synligheden af sidehovedet og sidefoden på en bestemt side i et genereret dokument for at skjule følgende elementer:

- Sidehovedet på første side, da rapporthovedet allerede indeholder kolonneoverskrifter
- Sidehovedet på enhver side, der ikke indeholder transaktioner, som kan forekomme på den sidste side
- Sidefoden på enhver side, der ikke indeholder transaktioner, som kan forekomme på den sidste side

Hvis du vil ændre synligheden, skal du opdatere egenskaben **Aktiveret** for komponenterne **Rapportsidehoved** og **Rapportsidefod**.

1. På siden **Formatdesigner** skal du udvide komponenten **Rapportside** i formattræet, vælge den indlejrede **Rapportsidehoved**-komponent og derefter følge disse trin:

    1. Vælg **Rediger** i feltet **Aktiveret**.
    2. På siden **Formeldesigner** skal du i feltet **Formel** angive følgende udtryk:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Vælg den indlejrede **Rapportsidefod**-komponent i formattræet, og benyt derefter følgende fremgangsmåde:

    1. Vælg **Rediger** i feltet **Aktiveret**.
    2. På siden **Formeldesigner** skal du i feltet **Formel** angive følgende udtryk:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Konstruktionen `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` bruges til at beregne antallet af transaktioner på den aktuelle side. Konstruktionen `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` bruges til at føje antallet af transaktioner på den aktuelle side til samlingen for korrekt at håndtere synligheden af næste sidefod.
    >
    > Samlingen `Total.Running.Lines` kan ikke genbruges her, da basiskomponentens **Aktiverede** egenskab behandles **efter** bindingerne for indlejrede komponenter. Når egenskaben **Aktiveret** er behandlet, er `Total.Running.Lines`-samlingen allerede steget med antallet af transaktioner på den aktuelle side.

3. Vælg **Gem**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Generere en kontrolrapport til Intrastat-opgørelse (opdateret)

1. Du skal først sørge for, at du har 24 transaktioner på **Intrastat**-siden. Gentag trinnene i afsnittet [Generere en kontrolrapport til Intrastat-opgørelse](#generate-intrastat-control-report) i dette emne for at generere og gennemse kontrolrapporten.

    Alle transaktioner vises på første side. Sidetotalerne og -tællerne svarer til rapporttotalerne og -tællerne. Sidehovedets område er skjult på den første side, da rapporthovedet allerede indeholder kolonneoverskrifter. Sidehovedet og sidefoden skjules på den anden side, da den pågældende side ikke indeholder transaktioner.

    ![Genereret Excel-dokument i skrivebordsprogram.](./media/er-paginate-excel-reports-document2.gif)

2. Opdater to transaktioner på **Intrastat**-siden ved at ændre **Varenummer**-koden fra **D00006** til **L0010**. Bemærk, at produktnavnet for den nye vare, **Aktivt højttalerpar**, er længere end produktnavnet for den oprindelige vare, **Standardhøjttaler**. Denne situation fremtvinger tekstombrydning i den tilsvarende celle i det genererede dokument. Sideinddeling af dokument og siderelateret opsummering og optælling skal nu opdateres. Gentag trinnene i afsnittet [Generere en kontrolrapport til Intrastat-opgørelse](#generate-intrastat-control-report) for at generere og gennemse kontrolrapporten.

    Aktuelt vises transaktioner på to sider, og sidetotaler og tællere beregnes korrekt. Sidehovedområdet skjules korrekt på den første side og kan ses på den anden side. Sidefoden er synlig på begge sider, fordi de indeholder transaktioner.

    ![Opdateret genereret Excel-dokument i skrivebordsprogrammet.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Er det muligt at se, hvornår den sidste side behandles af komponenten Sideformat?

Komponenten **Side** [viser ikke](er-fillable-excel.md#page-component-limitations) oplysninger om nummeret på den behandlede side og det samlede antal sider i et genereret dokument. Du kan dog konfigurere [ER-formler](er-formula-language.md), så du kan genkende den sidste side. Her er et eksempel:

- Beregn det samlede antal transaktioner, der allerede er blevet behandlet, ved hjælp af komponenten **Rapportside**. Du kan foretage denne beregning med formlen `COUNT(Total.Page.Amount.Result)`. 
- Beregn det samlede antal transaktioner, der skal behandles, på grundlag af den `model.CommodityRecord`-binding, der er konfigureret for komponenten **Rapportlinjer**. Du kan foretage denne beregning med formlen `COUNT(model.CommodityRecord)`.
- Sammenlign to tal for at genkende den sidste side. Hvis begge værdier er ens, genereres den sidste side.

> [!NOTE]
> Det anbefales, at du kun bruger denne fremgangsmåde, når den **Aktiverede** egenskab for **Rapportlinjer**-komponenten ikke indeholder en formel, der kan returnere [Falsk](er-formula-supported-data-types-primitive.md#boolean) under kørslen for nogle af de gentagne [poster](er-formula-supported-data-types-composite.md#record) på den bundne [Liste over poster](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Yderligere ressourcer

- [Designe en konfiguration til at generere dokumenter i Excel-format](er-fillable-excel.md)
- [Bruge datakilder for DATAINDSAMLING i elektroniske rapporteringsformater (ER)](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
