---
title: Bruge stregkodedatakilder til at generere stregkodebilleder
description: Dette emne forklarer, hvordan du kan bruge stregkodedatakilder til at generere stregkodebilleder.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: a5a396080d8b5dd4c2ed9a0eb15c1286e8799ebf
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323946"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Bruge stregkodedatakilder til at generere stregkodebilleder

[!include[banner](../includes/banner.md)]

Du kan bruge den [elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md) til at designe ER-formatkomponenter, som du kan køre for at generere elektroniske og printbare udgående dokumenter, som du skal bruge. Hvis du vil oprette et udgående dokument i Microsoft Office-format, skal du angive rapportens layout ved enten at bruge et Microsoft Excel-dokument eller et Microsoft Word-dokument som rapportskabelon. I [ER-operationsdesigneren](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) kan du vedhæfte et Excel- eller Word-dokument som skabelon til et ER-format. Følgende navngivne elementer i den vedhæftede skabelon er knyttet til elementerne i den konfigurerede formatkomponent:

- Indholdskontrolelementer i Word
- Navngivne ark, områder, celler, figurer og billeder i Excel

De navngivne elementer bruges som pladsholdere for data, der er angivet i et genereret dokument, når der køres et ER-format. ER-formatelementer er knyttet til datakilder. Disse datakilder angiver de data, der skal indtastes i de genererede dokumenter på kørselstidspunktet. Du kan finde flere oplysninger under [Integrer billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md).

ER understøtter nu datakildetypen **Stregkode**. Derfor kan du nu generere et billede, der repræsenterer stregkoden for angivet tekst. Når du konfigurerer et ER-format, kan du angive datakilderne for **Stregkode**-typen for at generere stregkodebilleder. Du kan derefter føje disse billeder til de genererede forretningsdokumenter, f.eks. ordrer, fakturaer, følgesedler og kvitteringer. Du kan også føje dem til forskellige typer etiketter, f.eks. produkt- og hyldelabels, emballage og forsendelsesetiketter.

Følgende pladsholdere kan bruges i rapportskabeloner til at angive stregkodebilleder:

- Kontrolelement til [billedindhold](/office/client-developer/word/content-controls-in-word) for Word
- [Billede](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)-objekt i Excel

Ved at bruge en datakilde af **Stregkode**-typen kan du generere stregkoder i følgende formater:

- Endimensionale stregkoder:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Intelligent email
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Todimensionale stregkoder:

    - Aztec
    - Datamatrix
    - QR-kode

Når du konfigurerer en **Stregkode** som datakilde, kan du definere specifikke gengivelsesparametre, der bruges til at generere et billede:

- **Bredde** – Angiv stregkodens bredde i pixel. En værdi på **0** (nul) angiver, at standardbredden bruges. Betydningen kan variere for forskellige formater.
- **Højde** – Angiv stregkodens højde i pixel. En værdi på **0** (nul) angiver, at standardhøjden bruges. Betydningen kan variere for forskellige formater.
- **Margen** – Angiv størrelsen på stregkodens margen i pixel. Margenen er det område på hver side af stregkoden, der skal holdes klart (stillezone). En værdi på **0** (nul) angiver, at standardmargen bruges. Betydningen kan variere for forskellige formater.
- **Outputindhold** – Angiv værdien til **Ja** for at generere et stregkodebillede, der indeholder de kodede oplysninger som tekst. Standardværdien er **Nej**.
- **Kodning** – Angiv den type tegn, der er kodet i det genererede stregkodebillede. Som standard bruges **UTF-8** som kodning.

> [!IMPORTANT]
> Når du tilføjer en ny **Stregkode**-datakilde, skal du placere den under et andet element (container) som et indlejret element.
>
> Når du binder en **Stregkode**-datakilde til et celleelement i et format, og celleelementet repræsenterer enten et Word-indholdskontrolelement eller et Excel-billede, vises datakilden i denne binding som en funktion, der har en enkelt parameter af **Streng**-typen. Du skal bruge denne parameter til at angive den tekst, der skal omdannes til et stregkodebillede, og som læses, når en genereret stregkode scannes.

Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Eksempel: Generér en betalingscheck, der indeholder en stregkode, som koder betalingsbeløbet.

I dette eksempel vises, hvordan en bruger i rollen **Systemadministrator** eller **Funktionel konsulent i elektronisk rapportering** kan konfigurere et ER-format, der indeholder en skabelon, der bruges til at generere et udgående dokument i Excel-format, der indeholder en stregkode. Her vises en oversigt over de trin, der er involveret.

1. [Fuldfør forudsætningerne](#ExamplePrerequisites).
2. [Aktivér en konfigurationsudbyder](#ExampleProvider).
3. [Importér den leverede ER-løsning](#ExampleImportSolution).
4. [Opret en betalingscheck](#ExampleGenerateCheque).
5. [Gennemgå den genererede betalingscheck](#ExampleReviewGeneratedCheque).
6. [Rediger formatet af den leverede ER-løsning](#ExampleModifyFormat).

    1. [Anvend en ny checkskabelon](#ExampleModifyFormatApplyTemplate).
    2. [Tilføj en ny stregkodedatakilde](#ExampleModifyFormatAddDataSource).
    3. [Bind et nyt formatelement](#ExampleModifyFormatBindFormatElement).
    4. [Gør den ændrede version tilgængelig for testkørsler](#ExampleModifyFormatMakeVersionAvailable).

        1. [Fuldfør den ændrede formatversion](#CompleteToRun).
        2. [Gør kladdeversionen tilgængelig for brug](#MarkToRun).

7. [Opret en betalingscheck](#ExampleGenerateCheque2).
8. [Konverter den genererede check til PDF](#ExampleConvertToPDF).

I dette eksempel skal du bruge den leverede ER-løsning, der er konfigureret til at generere betalingschecks. Denne løsning genererer betalingschecks, hvor betalingsbeløbet skrives både som et tal og som tekst. Du skal redigere denne ER-løsning, så checken også omfatter en genereret stregkode, hvor betalingsbeløbet er kodet og kan læses med en stregkodescanner.

Disse trin kan fuldføres i firmaet **USMF** i Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Fuldfør forudsætningerne

For at fuldføre dette eksempel skal du have adgang til USMF-firmaet i Finans i en af følgende roller:

- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Hvis du endnu ikke har fuldført eksemplet i emnet [Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md), skal du hente følgende konfigurationer af ER-eksempelløsningen.

| Indholdsbeskrivelse         | Filnavn                   |
|-----------------------------|-----------------------------|
| ER-datamodelkonfiguration | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)      |
| Konfiguration af ER-format     | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |

Hent desuden følgende Excel-fil, der indeholder den ændrede skabelon for den leverede ER-løsning.

| Indholdsbeskrivelse | Filnavn                 |
|---------------------|---------------------------|
| Rapportskabelon     | [Checkskabelon Excel.xlsx](https://download.microsoft.com/download/3/b/d/3bd3b944-da8f-43b4-8533-3c1292a4c3ef/CheckTemplateExcel.xlsx) |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Aktivere en konfigurationsudbyder

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** i sektionen **Konfigurationsudbydere** skal du kontrollere, at [konfigurationsudbyderen](general-electronic-reporting.md#Provider) for eksempelfirmaet **Litware, Inc.** er vist, og at den er markeret som aktiv. Hvis den ikke er angivet, eller hvis den ikke er markeret som aktiv, skal du følge trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Angivelse af eksempelfirmaet til aktivt på siden Lokaliseringskonfigurationer.](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Importér den leverede ER-løsning

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. Hvis konfigurationen **Model til check** på siden **Konfigurationer** ikke er tilgængelig i konfigurationstræet, skal du følge disse trin for at importere ER-datamodelkonfigurationen:

    1. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
    2. Vælg **Gennemse** i dialogboksen, find og vælg filen **Model for cheques.xml**, og vælg derefter **OK**.

4. Hvis konfigurationen **Checkudskrivningsformat** ikke er tilgængelig i konfigurationstræet, skal du følge disse trin for at importere ER-formatkonfigurationen:

    1. Vælg **Exchange** \> **Indlæs fra XML-fil** i handlingsruden.
    2. Vælg **Gennemse** i dialogboksen, find og vælg filen **Cheques printing format.xml**, og vælg derefter **OK**.

5. Udvid **Model for checks** i konfigurationstræet.
6. Gennemse listen over importerede ER-konfigurationer i konfigurationstræet.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Opret en betalingscheck

1. Gå til **Kontant- og bankstyring** \> **Bankkonti** \> **Bankkonti**.
2. Vælg kontoen **USMF OPER** på siden **Bankkonti**.
3. På siden med bankkontooplysninger i handlingsruden skal du under fanen **Opsætning** vælge **Check** i gruppen **Layout**.
4. Vælg **Rediger** på siden **Checklayout**.
5. Brug oversigtspanelet **Generelt** til at angive indstillingen **Generisk elektronisk eksportformat** til **Ja**.
6. Vælg det **Checkudskrivningsformat**, som du tidligere har importeret, i feltet **Eksportér formatkonfiguration**.
7. Vælg **Udskriv prøve** i handlingsruden.
8. Angiv indstillingen af **Omsætteligt checkformat** til **Ja** i dialogboksen, og vælg derefter **OK**.

    ![Checklayout - dialogboksen Udskriv prøve.](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Gennemgå den genererede betalingscheck

- Åbn den genererede check i Excel.
2. Gennemgå den genererede check.

    ![Genereret betalingscheck i Excel.](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Rediger formatet af den leverede ER-løsning

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Anvend en ny checkskabelon

Du kan bruge det stationære Excel-program til at åbne filen **Checkskabelon Excel.xlsx**, som du tidligere har importeret. Bemærk, at denne skabelon adskiller sig fra den skabelon, du brugte til at generere en betalingscheck i den leverede ER-løsning. Desuden indeholder den et **AmountBarcode**-element til stregkodebilledet.

![AmountBarcode-element i Excel-skabelonen.](./media/er-barcode-data-source-cheque2.png)

Du skal nu redigere ER-løsningen og derefter [genanvende](modify-electronic-reporting-format-reapply-excel-template.md) den ændrede skabelon.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model for checks** og vælge **Checkudskrivningsformat**.
4. Vælg **Designer** i handlingsruden.
5. I ER-operationsdesigneren skal du vælge fanen **Tilknytning** i højre side af siden og derefter vælge **Udvid/skjul** i ruden med formattræ til venstre.
6. Bemærk, at alle celleformatelementer er bundet til de relevante datakilder.

    ![Binding af celleformatelementer til datakilder i ER-operationsdesigneren.](./media/er-barcode-data-source-cells-bound.png)

7. Vælg fanen **Format** i højre side af siden.
8. Vælg ellipsen (**...**) i handlingsruden, og vælg derefter **Importér**.
9. Vælg **Opdater fra Excel** i gruppen **Import**, og vælg derefter **Opdater skabelon**.
10. Gå til filen **Checkskabelon Excel.xlsx**, der er gemt på din computer, i dialogboksen, markér den, og vælg derefter **OK** for at bekræfte, at den valgte skabelon skal anvendes.
11. Vælg fanen **Tilknytning** i højre side af siden og derefter **Udvid/skjul** i ruden med formattræ til venstre.
12. Bemærk, at **AmountBarcode**-celleelementet er blevet føjet til formatet. Dette element er knyttet til det **AmountBarcode**-element, der er føjet til den ændrede Excel-skabelon som en pladsholder for et stregkodebillede.

    ![AmountBarcode-celleelement er føjet til formatet i ER-operationsdesigneren.](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Tilføj en ny stregkodedatakilde

Derefter skal du tilføje en ny datakilde til **Stregkode**-typen.

1. I ER-operationsdesigneren skal du under fanen **Tilknytning** i højre side af siden vælge datakilden **Udskriv**.
2. Vælg **Tilføj**, og vælg derefter **Stregkode** som datakildetypen i gruppen **Funktioner**.

    ![Valg af stregkode som datakildetype.](./media/er-barcode-data-source-add.png)

3. I dialogboksen skal du angive **Stregkode** i feltet **Navn**.
4. I **Stregkodeformat** skal du vælge **Kode 128**.
5. Angiv **500** i feltet **Bredde**.
6. Vælg **OK**.

    ![Dialogboksen Egenskaber for datakilde.](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Bind et nyt formatelement

Derefter skal du binde det nye formatelement til den datakilde, du lige har tilføjet.

1. I ER-operationsdesigneren skal du under fanen **Tilknytning** i højre side af siden vælge datakilden **print\\barcode**.
2. Vælg celleelementet **AmountBarcode** i ruden med formattræet til venstre , og vælg derefter **Bind**.
3. Vælg **Vis detaljer** i handlingsruden.
4. Bemærk, at fordi **Stregkode**-datakilden er repræsenteret i bindingen som en funktion, der indeholder en enkelt parameter, er navnet på det bundne formatelement automatisk blevet brugt som argument for parameteren.

    ![Oplysninger om stregkodedatakilden i ER-operationsdesigneren.](./media/er-barcode-data-source-bind1.png)

5. Vælg **Rediger formel** for at justere bindingen.

    Du ønsker ikke, at navnet på celleelementet skal returneres. Derfor skal du konfigurere et udtryk, der returnerer tekst, der indeholder det betalingsbeløbet for den aktuelle check. Da det overordnede **ChequeLiness**-område er bundet til **model.cheques**-datakilden, er det skyldige beløb for den aktuelle check tilgængeligt i feltet **model.cheques.attributes.amount** for **Reel**-datatypen.

6. I feltet **Formel** skal du angive **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Vælg **Gem**, og luk derefter [ER-formeldesigneren](general-electronic-reporting-formula-designer.md).
8. Bemærk, at bindingen er blevet justeret.

    ![Reguleret binding i ER-operationsdesigneren.](./media/er-barcode-data-source-bind2.png)

9. Vælg **Gem**, og luk derefter ER-operationsdesigneren.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Gør den ændrede version tilgængelig for testkørsler

Som standard bruges de eneste versioner, der har statussen **Fuldført** og **Delt**, når du kører et ER-format.

Hvis du har færdiggjort dine ændringer, kan du fuldføre arbejdet med den aktuelle kladdeversion og gøre dine ændringer tilgængelige til brug. Du kan finde instruktioner i afsnittet [Fuldfør den ændrede formatversion](#CompleteToRun) nedenfor.

Hvis du vil fortsætte med at arbejde med den aktuelle kladdeversion, men du skal bruge den til at oprette checks, skal du eksplicit angive, at du vil bruge kladdeversionen af det format, der skal udføres. Du kan finde instruktioner i afsnittet [Gør kladdeversionen tilgængelig for brug](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Fuldfør den ændrede formatversion

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Model for checks** og vælge **Checkudskrivningsformat**.
4. I oversigtspanelet **Versioner** skal du vælge den post, der har statussen **Kladde**.
5. Vælg **Skift status**, og vælg derefter **Fuldført**.
6. Vælg **OK** i dialogboksen.

Status for den aktuelle version er ændret fra **Kladde** til **Fuldført**, og der oprettes en ny version med status **Kladde**. Du kan bruge denne nye kladdeversion til at anvende yderligere ændringer.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Gør kladdeversionen tilgængelig for brug

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
4. Angiv indstillingen af **Indstillingen Kør** til **Ja** i dialogboksen, og vælg derefter **OK**.
5. I konfigurationstræet skal du udvide **Model for checks** og vælge **Checkudskrivningsformat**.
6. Angiv indstillingen **Kør kladde** til **Ja**.
7. Vælg **Gem**.

Kladdeversionen af det valgte format er markeret som tilgængelig til brug, når det valgte format køres.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Opret en betalingscheck

1. Gå til **Kontant- og bankstyring** \> **Bankkonti** \> **Bankkonti**.
2. Vælg kontoen **USMF OPER** på siden **Bankkonti**.
3. På siden med bankkontooplysninger i handlingsruden skal du under fanen **Opsætning** vælge **Check** i gruppen **Layout**.
4. Vælg **Udskriv prøve** i handlingsruden på siden **Checklayout**.
5. Angiv indstillingen af **Omsætteligt checkformat** til **Ja** i dialogboksen.
6. Vælg **OK**.
7. Gennemgå den genererede check. Bemærk, at der er genereret en stregkode for at kode det skyldige beløb på checken.

    ![Genereret betalingscheck med stregkode i Excel.](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Der udløses en undtagelse, hvis argumentet for en **Stregkode**-datakilde ikke overholder de relevante krav, der er specifikke for stregkodeformatet. Når **Stregkode**-datakilden kaldes for at oprette en [EAN-8](https://wikipedia.org/wiki/EAN-8)-stregkode for den leverede tekst, udløses der f.eks. en undtagelse, hvis længden af teksten overstiger syv tegn.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Konverter den genererede check til PDF

Som beskrevet i emnet [Generere FTI-formularer, der kan udskrives](er-generate-printable-fti-forms.md#finland) kan du bruge en særlig skrifttype til oprettelse af stregkoder i et genereret dokument. I dette tilfælde kan yderligere transformationer af det genererede dokument afhænge af tilgængeligheden af den pågældende skrifttype i transformationsmiljøet. Hvis du f.eks. forsøger at konvertere et dokument til PDF-format eller se det i et miljø, hvor skrifttypen mangler, gengives stregkoderne ikke korrekt.

Men når du bruger **Stregkode**-datakilden til at producere stregkoder, afhænger gengivelsen af disse stregkoder ikke af nogen skrifttyper. Derfor kan du nemt konvertere dokumenter, der indeholder stregkoderne, til PDF-format. I følgende illustration vises eksemplet på en genereret betalingscheck, der er [konverteret](electronic-reporting-destinations.md#OutputConversionToPDF) til et PDF-dokument baseret på indstillingen af den konfigurerede ER-[destination](electronic-reporting-destinations.md).

![Forhåndsvisning af PDF-dokument med betalingscheck.](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Begrænsninger

> [!NOTE]
> Nogle typer stregkoder, der genereres, har et fast højde-bredde-forhold. Denne funktionsmåde giver mening, hvis du har slået funktionen **Aktivér brug af EPPlus-bibliotek i elektronisk rapporteringsstruktur** til, så den kan arbejde med Excel-dokumenter i ER. I dette tilfælde indsættes et billede i en pladsholder, der har et låst højde-bredde-forhold. Når dimensionerne for en pladsholder i en skabelon svarer til forholdet af et billede, der er indsat, tilpasses størrelsen på et reelt billede i et genereret dokument måske for at bevare det krævede højde-bredde-forhold. Hvis du vil forhindre tilpasning af billedstørrelsen, skal du bruge en pladsholder, der har et forventet højde-bredde-forhold.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk rapportering](general-electronic-reporting.md)
- [Destinationer for elektronisk rapportering](electronic-reporting-destinations.md)
- [Formelsprog i elektronisk rapportering](er-formula-language.md)
- [Funktionen NUMBERFORMAT](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
