---
title: Design et ER-format til generering af en rapport i Excel-format med integrerede billeder i sidehoveder eller sidefødder
description: Dette emne forklarer, hvordan du bruger elektronisk rapportering (ER) til at generere forretningsdokumenter, der har billeder og figurer integreret i sidehoveder og sidefødder.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3f3f77a9e6104a31995c9ee398504982fe43ac9e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323769"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Design et ER-format til generering af en rapport i Excel-format med integrerede billeder i sidehoveder eller sidefødder

[!include[banner](../includes/banner.md)]

Dette emne forklarer, hvordan en bruger med rollen Systemadministrator eller Funktionel konsulent i elektronisk rapportering kan udføre disse opgaver:

- Konfigurer parametre for strukturen [Elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md).
- Importer ER-[konfigurationer](general-electronic-reporting.md#Configuration), der [leveres](general-electronic-reporting.md#Provider) af Microsoft, og som bruges til at generere [fritekstfakturaer](../../../finance/accounts-receivable/create-free-text-invoice-new.md), baseret på en [skabelon](er-fillable-excel.md#excel-file-component) i Microsoft Excel-format.
- Opret en [brugerdefineret](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) version af en standardkonfiguration af ER-format, der leveres af Microsoft.
- Rediger den brugerdefinerede ER-formatkonfiguration, så den genererer en rapport over fritekstfakturaer med et firmalogobillede i sidefoden.

Procedurerne i dette emne kan fuldføres i **USMF**-firmaet. Der kræves ingen kodning. Før du begynder, skal du hente og gemme følgende fil.

| Betegnelse        | Filnavn |
|--------------------|-----------|
| Billede af firmalogo | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Indhold

- [Konfigurere den juridiske enhed](#ConfigureLegalEntity)
- [Konfigurere ER-strukturen](#ConfigureFramework)

    - [Konfigurere ER-parametre](#ConfigureParameters)
    - [Aktivere en udbyder af ER-konfigurationer](#ActivateProvider)

        - [Gennemse listen over udbydere af ER-konfigurationer](#ReviewProvidersList)
        - [Tilføje en ny udbyder af ER-konfigurationer](#AddProvider)
        - [Aktivere ny udbyder af ER-konfigurationer](#ActivateAddedProvider)

- [Importere standardkonfigurationer af ER-format](#ImportERSolution1)

    - [Importere standardkonfigurationer af ER](#ImportERFormat)
    - [Gennemse de importerede ER-konfigurationer](#ReviewImportedERSolution)

- [Udskrive en fritekstfaktura ved hjælp af standard ER-format](#PrintInvoice1)

    - [Opsætning af udskriftsstyring](#ConfigurePrintManagement1)
    - [Udskriv en fritekstfaktura](#ProcessInvoice1)

- [Tilpasse standard-ER-formatet](#CustomizeProvidedFormat)

    - [Oprette et brugerdefineret format](#DeriveProvidedFormat)
    - [Redigere brugerdefineret format](#ConfigureDerivedFormat)
    - [Markere det brugerdefineret format som kørbart](#MarkFormatRunnable)

- [Udskrive en fritekstfaktura ved hjælp af det brugerdefinerede ER-format](#PrintInvoice2)

    - [Opsætning af udskriftsstyring](#ConfigurePrintManagement2)
    - [Udskriv en fritekstfaktura](#ProcessInvoice2)

- [Yderligere ressourcer](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Konfigurere den juridiske enhed

1. Gå til **Organisationsadministration** \> **Organisationer** \> **Juridiske enheder**.
2. Vælg **Skift** på siden **Juridiske enheder** i oversigtspanelet **Billede af rapportfirmalogo**.
3. Vælg **Gennemse** i dialogboksen **Vælg billedfil**, og vælg den **firmalogo.png**, du hentede tidligere.
4. Vælg **Gem**, og luk derefter siden **Juridiske enheder**.

![Billede af firmalogo, der er valgt på siden Juridiske enheder.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurere ER-strukturen

Som bruger i rollen Funktionel konsulent i elektronisk rapportering skal du konfigurere det minimale sæt med ER-parametre, før du kan begynde at bruge ER-strukturen til at designe en brugerdefineret version af standard-ER-formatet.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurere ER-parametre

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .
4. På fanen **Vedhæftede filer** kan du angive følgende parametre:

    - I feltet **Konfigurationer** skal du vælge typen **Fil** for **USMF**-virksomheden.
    - I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.

Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivere en udbyder af ER-konfigurationer

Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer. Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål. Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.

> [!NOTE]
> Kun ejeren af en ER-konfiguration, der kan redigere konfigurationen. Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Gennemse listen over udbydere af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse. Gennemse indholdet af denne side. Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Tilføje en ny udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.
3. På siden **Konfigurationsudbydere** skal du vælge **Ny**.
4. I feltet **Navn** skal du angive **Litware, Inc.**
5. I feltet **Internetadresse** skal du angive `https://www.litware.com`.
6. Vælg **Gem**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere ny udbyder af ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.

Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Importere standardkonfigurationer af ER-format

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Importere standardkonfigurationer af ER

Hvis du vil føje standard-ER-konfigurationerne til din aktuelle forekomst af Dynamics 365 Finance, skal du importere dem fra det ER-[lager](general-electronic-reporting.md#Repository), der er konfigureret for den pågældende forekomst.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for **Microsoft**-udbyderen.
3. På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**. Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), skal du følge godkendelsesvejledningen.
4. På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **Fritekstfaktura (Excel)**.
5. I oversigtspanelet **Versioner** skal du vælge den nyeste version (f.eks. **240.112**) for den valgte ER-formatkonfiguration.
6. Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.

![Importere ER-betalingsformatet på siden Konfigurationslager.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Gennemse de importerede ER-konfigurationer

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel**.
4. Bemærk, at der ud over det valgte **Fritekstfaktura (Excel)** ER-format, blev importeret andre påkrævede ER-konfigurationer. Kontroller, at følgende ER-konfigurationer er tilgængelige i konfigurationstræet:

    - **Fakturamodel** – Denne konfiguration indeholder den datamodel, der repræsenterer datastrukturen for fakturaforretningsdomænet.
    - **Tilknytning af fakturamodel** – Denne konfiguration indeholder den modeltilknytning ER-komponent, der beskriver, hvordan datamodellen udfyldes med applikationsdata under kørsel.
    - **Fritekstfaktura (Excel)** – Denne konfiguration indeholder komponenterne til format og formattilknytning af ER. Formatkomponenten angiver rapportlayoutet baseret på en skabelon i Excel-format. Komponenten til formattilknytning indeholder modeldatakilden og angiver, hvordan denne datakilde bruges til at udfylde rapportlayoutet på kørselstidspunktet.

![Importerede ER-konfigurationer på siden Konfigurationer.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Udskrive en fritekstfaktura ved hjælp af standard ER-format

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Opsætning af udskriftsstyring

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På **Fritekstfaktura**-siden vælges **FTI-00000002**-fakturaen, og vælg derefter **udskriftsstyring** i gruppen **Udskriftsstyring** i handlingsruden under fanen **Faktura**.
3. På opsætningssiden **Udskriftsstyring** skal du udvide **Modul – debitor \> Dokumenter \> Fritekstfaktura**, og derefter vælge **Oprindeligt\<Default\>** element.
4. Vælg **Fritekstfaktura (Excel)** i feltet **Rapportformat**.
5. Vælg tasten **Esc** for at forlade opsætningssiden **Udskriftsstyring** og vende tilbage til siden **Fritekstfaktura**.

![Indstillinger for udskriftsstyring til en fritekstfaktura i standard ER-format på opsætningssiden udskriftsstyring.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Udskriv en fritekstfaktura

1. På **Fritekstfaktura**-siden tjekkes, at **FTI-00000002**-fakturaen er valgt, og vælg derefter i handlingsruden under fanen **Faktura** i gruppen **Dokument** vælges **Udskriv** \> **Valgt**.
2. Hent den genererede faktura i Excel-format, og åbn den for at få forhåndsvisning.
3. Bemærk, at sidefoden i den genererede faktura i overensstemmelse med strukturen i Excel-skabelonen for det angivne ER-format indeholder oplysninger om det aktuelle sidetal og det samlede antal sider i rapporten.

![Genereret fritekstfaktura.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Tilpasse standard-ER-formatet

I eksemplet i dette afsnit kan du bruge ER-konfigurationerne fra Microsoft til at generere en fritekstfaktura i Excel-format. Du skal dog tilføje en tilpasning for at placere et firmalogobillede i sidefoden på genererede fakturaer.

I dette tilfælde skal du som repræsentant for Litware, Inc. oprette (aflede) en ny standard-ER-formatkonfiguration, der er baseret på Microsoft-leveret af **Fritekstfaktura (Excel)**-konfiguration.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Oprette et brugerdefineret format

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Fakturamodel** og derefter vælge **Fritekstfaktura (Excel)**. Litware, Inc. vil bruge den importerede version (f.eks. **240.112**) af denne ER-formatkonfiguration som basis for den brugerdefinerede version.
3. Vælg **Opret konfiguration** for at åbne dialogboksen med rullemenu. Brug denne dialogboks til at oprette en ny konfiguration for et brugerdefineret betalingsformat.
4. I feltet **Ny** skal du vælge indstillingen **Afledt fra navn: Fritekstfaktura (Excel), Microsoft**.
5. Vælg **Fritekstfaktura (Excel) brugerdefineret** i feltet **Navn**.
6. Vælg **Opret konfiguration**.

![Oprettelse af en konfiguration til et brugerdefineret betalingsformat i dialogboksen Opret konfiguration.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Version 240.112.1 af den **Fritekstfaktura (Excel) brugerdefineret** ER-formatkonfiguration oprettes. Denne version har [statussen](general-electronic-reporting.md#component-versioning) **Kladde** og kan redigeres. Det aktuelle indhold af det brugerdefinerede ER-format svarer til indholdet af det format, der er leveret af Microsoft.

![Ny version af den redigerbare ER-konfiguration på siden Konfigurationer.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Redigere brugerdefineret format

Konfigurer dit brugerdefinerede format, så der vises et firmalogobillede i sidefoden på hver side i rapporten.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **Fritekstfaktura (Excel) brugerdefineret**.
3. I oversigtspanelet **Versioner** skal du vælge version **240.112.1** for den valgte konfiguration.
4. Vælg **Designer**.
5. På siden **Formatdesigner** skal du vælge **Vis detaljer** for at få vist flere oplysninger om formatelementerne.
6. Udvid og gennemse følgende elementer:

    - Elementet **Fritekstfaktura** af typen **Excel**. Dette element bruges til at generere en faktura i Excel-projektmappeformat.
    - Elementet **Fritekstfaktura \\ Faktura** af typen **Ark**. Dette element bruges til at generere et regneark i den genererede Excel-projektmappe.
    - Elementet **Fritekstfaktura \\ Faktura \\ Sidefod** af typen **Sidefod**. Dette element bruges til at udfylde en fakturafod.

7. Vælg elementet **Fritekstfaktura \\ Faktura \\ Sidefod**.

    ![Sidefodselementet i ER-operationsdesigneren.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Hver sidefod i en genereret faktura indeholder oplysninger om det aktuelle sidetal og det samlede antal sider i rapporten. Som du kan se, indeholder elementet i **Fritekstfaktura \\ Faktura \\ Sidefod** ingen underordnede elementer. Derfor er den Excel-skabelon, der bruges, konfigureret til at vise sidefodsdetaljer i midten af hver rapports sidefod.

8. Vælg **Tilføj**, og vælg derefter typen **Excel \\ Billede** for det formatelement, du vil tilføje:

    1. Vælg **Højre** i feltet **Justering**.
    2. Vælg **Relative** i feltet **Skaler højde**.
    3. Angiv **70** i feltet **Skala i procent**.
    4. Vælg **OK**.

        > [!NOTE]
        > Elementet **Excel \\ Billede** bruges til at tilføje et firmalogobillede og justere det i højre side af sidefoden.

    ![Egenskaber for billedelementet i dialogboksen Komponentegenskaber.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Vælg det **billedelement**, du netop har tilføjet, i formatstrukturtræet til venstre, og udvid derefter **modeldatakilden** under fanen **Tilknytning**.
10. Udvid **model.Betaling** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo**, og derefter **model.InvoiceBase.CompanyInfo.Logo**. Datakildefeltet for [containertypen](er-formula-supported-data-types-composite.md#container) viser firmaets logobillede som medieindhold.
11. Vælg **Bind**. Elementet **Billedeformat** er nu bundet til datakildefeltet **model.InvoiceBase.CompanyInfo.Logo**. Under kørsel vil der derfor blive sat et firmalogobillede i sidefoden på genererede fakturaer.

    ![Elementet Billedeformat er nu bundet til datakildefeltet model.InvoiceBase.CompanyInfo.Logo i ER-operationsdesigner.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Vælg **Gem**, og luk derefter siden **Designer**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Markere det brugerdefineret format som kørbart

Nu, hvor den første version af det brugerdefinerede format er blevet oprettet og har statussen **Kladde**, kan du køre formatet til testformål. Hvis du vil køre rapporten, skal du behandle en kreditorbetaling ved hjælp af den betalingsmåde, der refererer til det brugerdefinerede ER-format. Som standard er det kun versioner, der har statussen **Fuldført** eller **Delt** der [tages i betragtning](general-electronic-reporting.md#component-versioning), når du kalder et ER-format fra applikationen. Denne funktionsmåde er med til at forhindre, at ER-formater med uafsluttede design bliver brugt. Men når det gælder dine testkørsler, kan du tvinge programmet til at bruge den version af dit ER-format, der har statussen **Kladde**. På denne måde kan du justere den aktuelle formatversion, hvis der kræves ændringer. Du kan finde flere oplysninger under [Anvendelighed](electronic-reporting-destinations.md#applicability).

Hvis du vil bruge kladdeversionen af et ER-format, skal du eksplicit markere ER-formatet.

1. Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.
2. På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
3. I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.
4. Vælg **Rediger** for at gøre den aktuelle side redigerbar, og derefter, i konfigurationstræet i venstre rude, skal du vælge **Fritekstfaktura (Excel) brugerdefineret**.
5. Angiv indstillingen **Kør kladde** til **Ja**.

![Markere det brugerdefinerede format som kørbart på siden Varianter.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Udskrive en fritekstfaktura ved hjælp af det brugerdefinerede ER-format

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Opsætning af udskriftsstyring

1. Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På **Fritekstfaktura**-siden vælges **FTI-00000002**-fakturaen, og vælg derefter **udskriftsstyring** i gruppen **Udskriftsstyring** i handlingsruden under fanen **Faktura**.
3. På opsætningssiden **Udskriftsstyring** skal du udvide **Modul - debitor** \> **Dokumenter** \> **Fritekstfaktura** og derefter vælge **Oprindeligt** **\<Default\>** element.
4. Vælg **Fritekstfaktura (Excel) Brugerdefineret** i feltet **Rapportformat**.
5. Vælg **Esc** for at forlade opsætningssiden **Udskriftsstyring** og vende tilbage til siden **Fritekstfaktura**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Udskriv en fritekstfaktura

1. På **Fritekstfaktura**-siden tjekkes, at **FTI-00000002**-fakturaen er valgt, og vælg derefter i handlingsruden under fanen **Faktura** i gruppen **Dokument** vælges **Udskriv** \> **Valgt**.
2. Hent den genererede faktura i Excel-format, og åbn den for at få forhåndsvisning.
3. Bemærk, at sidefoden i den genererede faktura i overensstemmelse med strukturen i det tilpassede ER-format indeholder et firmalogobillede samt oplysninger om rapportens sidefod.

![Genereret fritekstfaktura med et firmalogobillede i sidefoden.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Yderligere ressourcer

- [Designe en konfiguration til at generere dokumenter i Excel-format](er-fillable-excel.md)
- [Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md)
