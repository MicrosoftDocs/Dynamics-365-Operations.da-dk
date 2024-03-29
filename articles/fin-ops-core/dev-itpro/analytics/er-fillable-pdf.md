---
title: Designe konfigurationer til elektronisk rapportering for at udfylde PDF-skabeloner
description: Denne artikel indeholder oplysninger om, hvordan du kan designe et elektronisk rapporteringsformat (ER) for at udfylde en PDF-skabelon.
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 4056c2b9442e26a0e1c99e6155a3cd605d222974
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283307"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Designe konfigurationer til elektronisk rapportering for at udfylde PDF-skabeloner

[!include[banner](../includes/banner.md)]

Procedurerne i denne artikel er eksempler, der viser, hvordan en bruger i rollen **Systemadministrator** eller **Udvikler til elektronisk rapportering** kan konfigurere et elektronisk rapporteringsformat (ER), der genererer rapporter som PDF-filer ved at bruge PDF-dokumenter, der skal udfyldes, som rapportskabeloner. Disse trin kan udføres i ethvert regnskab af Dynamics 365 Finance eller Regulatory Configuration Services (RCS).

## <a name="prerequisites"></a>Forudsætninger

Før du går i gang, skal du have en af følgende adgangstyper, afhængigt af hvilken tjeneste du bruger til at fuldføre procedurerne i denne artikel:

- Adgang til Finance for en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

- Adgang til RCS for en af følgende roller:

    - Udvikler til elektronisk rapportering
    - Funktionel konsulent i elektronisk rapportering
    - Systemadministrator

Du skal også fuldføre proceduren [Opret konfigurationsudbydere og marker dem som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Til sidst skal du downloade følgende filer.

| Indholdsbeskrivelse                       | Filnavn                                     |
|-------------------------------------------|-----------------------------------------------|
| Skabelon til den første side i rapporten | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Skabelon til andre sider i rapporten    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| ER-eksempelformat - PDF                          | [Intrastat report (PDF).version.1.1.xml](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| ER-eksempelformat - Excel                          | [Intrastat (import from Excel).version.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Eksempeldatasæt                            | [Intrastat sample data.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Designe formatkonfigurationen

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Få adgang til listen over de konfigurationer, der leveres af Microsoft

1. Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.
2. Sørg for, at provideren **Litware, Inc.** er tilgængelig og markeret som aktiv.
3. Vælg feltet for **Microsoft**-udbyderen, vælg **Lagre**.

    > [!NOTE]
    > Hvis der allerede findes et lager af **LCS** typen, kan du springe de resterende trin i denne procedure over.

4. Vælg **Tilføj**.
5. I rulledialogboksen i feltgruppen **Konfigurationslagertype** skal du vælge indstillingen **LCS**.
6. Vælg **Opret lager**.
7. Vælg **OK**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Få de modelkonfigurationer, der leveres af Microsoft

1. Til venstre på siden **Konfigurationslagre** skal du vælge knappen **Vis filtre** (symbolet for tragten).
2. Tilføj et filter med værdien **LCS** i feltet **Type**, og brug operatoren **begynder med**.
3. Vælg **Anvend**.
4. Vælg **Åbn**.
5. Vælg **Intrastat-model** i træet.
6. I oversigtspanelet **Versioner** skal du vælge version **1**.

    > [!NOTE]
    > Hvis knappen **Importer** i oversigtspanelet **Versioner** ikke er tilgængelig, kan du springe de resterende trin i denne procedure over.

7. Vælg **Importér**.
8. Vælg **Ja** for at bekræfte importen af den valgte version af modelkonfigurationen **Intrastat-model**.

### <a name="create-a-new-format-configuration"></a>Opret en ny formatkonfiguration

1. I arbejdsområdet **Elektronisk rapportering** skal du vælge feltet **Rapporteringskonfigurationer**.
2. Vælg **Intrastat-model** i træet.
3. Vælg **Opret konfiguration**.

    > [!NOTE]
    > Hvis knappen **Opret konfiguration** ikke er tilgængelig, skal du aktivere designtilstand på siden **Elektroniske rapporteringsparametre**, der kan åbnes fra arbejdsområdet **Elektronisk rapportering**.

4. Vælg indstillingen **Format, der er baseret på datamodellen Intrastat** i feltgruppen **Ny** i rulledialogboksen.
5. I feltet **Navn** skal du skrive **Intrastat-rapport (PDF)**.
6. I feltet **Beskrivelse** skal du skrive **Intrastat-rapport i PDF-format**.

    > [!NOTE]
    > Den aktive konfigurationsudbyder indsættes automatisk. Denne udbyder vil kunne vedligeholde denne konfiguration. Selvom andre udbydere kan bruge denne konfiguration, vil de ikke kunne vedligeholde den.

7. Valgfrit: I feltet **Formattype** kan du vælge et bestemt format for et elektronisk dokument. Hvis du vælger **PDF**, opretter ER Operations-designeren kun formatelementer på designtidspunktet, der gælder for dokumenter, der genereres i PDF-format (**PDF\Fil**, **PDF\PDF-fletning** osv.). Hvis du ikke udfylder dette felt, bliver der angivet et format for det elektroniske dokument på designtidspunktet i ER Operations-designeren, hvor der tilføjes et første format-element. Hvis du f.eks. tilføjer **Excel\File** som det første formatelement, viser ER Operations-designer kun de formatelementer, der gælder for dokumenter, der genereres i Excel-format (**Excel\Cell**, **Excel\Range** osv.). format.
8. Vælg **Opret konfiguration**.

Der oprettes en ny ER-formatkonfiguration Du kan bruge kladdeversionen af denne konfiguration til at gemme den ER-formatkomponent, der er beregnet til at generere elektroniske dokumenter i PDF-format.

### <a name="design-the-format-of-an-electronic-document"></a>Designformatet for et elektronisk dokument

I det ER-format, du har oprettet, kan du nu designe det ER-format, der opretter **Intrastat-kontrol**-rapporten, i PDF-format. Den første side i denne rapport skal vise en oversigt over rapporten og detaljer om de udenlandske handelstransaktioner, der indberettes om. De andre sider skal kun vise detaljer om de udenlandske handelstransaktioner, der indberettes om. Da de genererede rapportsider skal have forskellige layout, bliver de to forskellige skabeloner i PDF-format brugt i ER-formatet.

Åbn de PDF-skabeloner, du har hentet, i en PDF-fremviser. Bemærk, at hver skabelon indeholder flere felter, der skal udfyldes. I hver skabelon vises detaljer om udenlandske handelstransaktioner som 42 rækker, der hver har ni felter. Rækkenummeret vises i slutningen af hvert felts navn (f.eks. **Dato 1**...**Dato 42** og **Vare 1**...**Vare 42**).

Følgende illustration viser PDF-skabelonen til den første side i rapporten.

![Skabelon 1.](media/rcs-ger-filloutpdf-template1.png)

Følgende illustration viser PDF-skabelonen til de øvrige sider i rapporten.

![Skabelon 2.](media/rcs-ger-filloutpdf-template2.png)

1. På siden **Konfigurationer** skal du vælge **Designer**.
2. Vælg **Tilføj rod**.
3. Vælg **PDF \> PDF-fletning** i træet i rulledialogboksen.

    Når du vælger **PDF-fletning**-elementet som rodelement for formatet, bliver alle PDF-dokumenter, der genereres på kørselstidspunktet, flettet til et enkelt endeligt PDF-dokument. Hvis du kun har brug for én PDF-skabelon til at oprette alle de nødvendige dokumenter ved hjælp af det ER-format, som du designer, skal du vælge **PDF-fil** som rodelementet.

4. I feltet **Navn** skal du skrive **Output**.
5. Vælg **Brugerindstilling** i feltet **Sprogindstillinger**. Rapporten genereres på det sprog, som den bruger, der kører den, bruger.
6. Vælg **Brugerindstilling** i feltet **Indstillinger for kultur**. Værdier og datoer, der vises på siderne i rapporten, formateres ud fra den foretrukne landestandard for den bruger, der kører rapporten.
7. Vælg **OK**.
8. I handlingsruden under fanen **Importér** skal du vælge **Importér fra PDF**.

    Når et PDF-dokument, der kan udfyldes, importeres som skabelon til dette ER-format, oprettes automatisk alle de nødvendige ER-formatelementer (elementerne **PDF-fil**, **Feltgruppe** og **Felter**) i det format, der designet, baseret på strukturen i det PDF-dokument, der importeres.

9. Vælg **Gennemse**. Naviger til og vælg filen **IntrastatReportTemplate1.pdf**, som du hentede tidligere, som en forudsætning.
10. Vælg **OK**.

    Den valgte fil indlæses, og feltet **Skabelon** i dialogboksen **Importer fra PDF** udfyldes.

11. Angiv indstillingen **Gruppefelter** til **Ja**. Hvis det valgte PDF-dokument indeholder en eller flere feltgrupper, bruges de til at gruppere de ER-formatelementer, der oprettes. Der oprettes et formatelement af typen **Feltgruppe** til dette formål.

    Hvis denne indstilling er sat til **Nej**, oprettes de påkrævede ER-formatelementer som en simpel liste over elementer, der indlejres under det **PDF-fil**-format, der oprettes.

12. Vælg **OK**.

    ![Dialogboksen Importér fra PDF.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Udvid **Output** i træet.

    Bemærk, at **PDF-fil**-komponenten er blevet oprettet automatisk for at administrere oprettelsen af den første side i den rapport, der genereres på kørselstidspunktet.

14. Udvid **Output \> PDF-fil** i træet.

    Bemærk, at den strukturerede liste over formatelementer er blevet oprettet automatisk i dette ER-format baseret på strukturen i det PDF-dokument, der kan udfyldes, og som du tidligere har importeret.

15. Vælg **Output \> PDF-fil** i træet.
16. I feltet **Navn** skal du skrive **Side 1**.

    Dette formatelement bruges til at oprette den første side i **Intrastat-kontrol**-rapporten. På denne side vises en oversigt over rapporten og oplysninger om udenlandske handelstransaktioner.

    Hvis du ikke udfylder feltet **Sprogindstillinger**, vil indstillingen **Sprogindstillinger** for det overordnede **PDF-fletning**-element bestemme sproget i den rapport, der genereres, ved hjælp af dette formatelement. Du kan vælge en anden værdi for at tilsidesætte indstillingen af det overordnede element.

    Hvis du ikke udfylder feltet **Indstillinger for kultur**, vil indstillingen **Indstillinger for kultur** for det overordnede **PDF-fletning**-element bestemme landestandarden i den rapport, der genereres, ved hjælp af dette formatelement. Landestandarden bestemmer formatet af værdier og datoer på siderne i rapporten. Du kan vælge en anden værdi for at tilsidesætte indstillingen af det overordnede element.

17. Vælg fanen **Importer** i handlingsruden. Bemærk, at knappen **Opdater fra PDF** er blevet tilgængelig for det valgte formatelement, **PDF-fil**.

    Du kan bruge denne knap til at importere den opdaterede PDF-skabelon til det redigerede format. Når den opdaterede PDF-skabelon importeres, ændres listen over formatelementer tilsvarende:

    - I forbindelse med nye felter i den opdaterede PDF-skabelon oprettes der nye formatelementer i det redigerede ER-format.
    - Hvis den opdaterede PDF-skabelon ikke længere indeholder felter, der svarer til eksisterende formatelementer i det redigerede ER-format, slettes disse formatelementer fra ER-formatet.

18. Vælg **Vedhæftede filer** under fanen **Formater**.

    Bemærk, at det importerede PDF-dokument vedhæftes til det redigerede ER-format.

    ![Visning af vedhæftet PDF-fil.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Fortsæt med at designe dette format ved at importere den anden PDF-skabelon, idet du føjer nødvendige bindinger til datakilder osv.
20. Vælg **Gem**.
21. Luk siden.
22. Vælg **Slet**.
23. Vælg **Ja**.

Hvis du vil vide, hvordan nye formatelementer af typen **PDF-fletning**, **PDF-fil**, **Feltgruppe** og **Felt** kan bruges til at oprette dokumenter i PDF-format, kan du importere og analysere ER-eksempelformatet.

### <a name="import-the-format-configuration"></a>Importere formatkonfigurationen

Derefter skal du importere det ER-eksempelformat, som du tidligere har hentet, for at generere **Intrastat-kontrol**-rapporten i PDF-format. Den første side i rapporten skal vise en oversigt over rapporten og detaljer om de udenlandske handelstransaktioner, der indberettes om. De andre sider skal kun vise detaljer om de udenlandske handelstransaktioner, der indberettes om.

1. Vælg **Exchange \> Indlæs fra XML-fil** på siden **Konfigurationer**.
2. Vælg **Gennemse**. Naviger til og vælg filen **Intrastat report (PDF).version.1.1.xml**, som du hentede tidligere, som en forudsætning.
3. Vælg **OK**.

## <a name="analyze-the-format-configuration"></a>Analysere formatkonfigurationen

### <a name="format-layout"></a>Formatlayout

1. På siden **Konfigurationer** skal du i træet vælge **Intrastat-model \> Intrastat-rapport (PDF)**.
2. Vælg **Designer**.
3. Vælg **Vis detaljer**.
4. Udvid **Output: PDF-fletning** i træet.

    Bemærk, at dette ER-format indeholder to **PDF-fil**-elementer, som bruger hver sin PDF-skabelon. Én skabelon bruges til at oprette den første side i rapporten i PDF-format, og den anden skabelon bruges til at oprette de andre sider.

5. I træet skal du udvide **Output: PDF-fletning \> side 1: PDF-fil (IntrastatReportTemplate1)**.
6. I træet skal du udvide **Output: PDF-fletning \> Side N: PDF-fil (IntrastatReportTemplate2)**.

    Bemærk, at strukturen i de indlejrede formateringselementer for de to **PDF-fil**-elementer også varierer, fordi indholdet af de to PDF-skabeloner afviger fra hinanden.

### <a name="format-mapping"></a>Formattilknytning

1. Vælg fanen **Tilknytning** på siden **Formatdesigner**.
2. Udvid **Sideopdeling \> Sider** i træet.

    ![Formeldesignerside, hvor modeltræet er udvidet.](media/rcs-ger-filloutpdf-reviewformat.png)

    Bemærk følgende oplysninger:

    - Formatelementet **Output \> Side 1** af typen **PDF-fil** er ikke bundet til nogen datakilde, og udtrykket **Aktiveret** for dette formatelement er tomt. På kørselstidspunktet vil **IntrastatReportTemplate1** PDF-skabelonen derfor kun blive udfyldt én gang, når der genereres et individuelt PDF-dokument.
    - Formatelementet **Output \> Side N** af typen **PDF-fil** er bundet til **Paging.PageN**-datakilden af typen **Postliste**, og udtrykket **Aktiveret** for dette formatelement er tomt. På kørselstidspunktet vil **IntrastatReportTemplate2** PDF-skabelonen derfor kun blive udfyldt for hver post fra listen over bundne poster, når der genereres et individuelt PDF-dokument.
    - Da formatelementerne **Side 1: PDF-fil** og **Side N: PDF-fil** er underordnede i forhold til **Output: PDF-fletning**-formatelementet, flettes alle PDF-dokumenter, der er udfyldt, i et enkelt endeligt PDF-dokument.
    - Datakilderne **Paging.Page1** og **Paging.PageN** konfigureres som filtre for poster fra datakilden **Paging.Pages**. Denne datakilde er konfigureret til at opdele hele sættet af udenlandske handelstransaktioner i batches. Hver batch indeholder op til 42 poster. Følgende ER-udtryk bruges til at opdele transaktionerne i batches:

        SPLITLIST(Totals.CommodityRecord,42)

    - Datakilden **Paging.Pages** indeholder elementet **Paging.Pages.Enumerated**, der returnerer detaljerne for hver post, der er medtaget i et batch. Disse oplysninger omfatter postens rækkefølge i det aktuelle batch (feltet **Paging.Pages.Enumerated.Number**). Feltet **Paging.Pages.Enumerated.Number** bruges i **Navn** udtrykket i **PDF-felt**-formatelementer til dynamisk generering af et feltnavn, der er baseret på transaktionsnummeret i en batch. Det genererede feltnavn bruges derefter til at udfylde det korrekte PDF-felt i den PDF-skabelon, der bruges.
    - **Output \> Side N \> Detaljer 2** formatelementet af typen **PDF-gruppe** er bundet til **Paging.PageN.Enumerated** datakilden (eller **\@.Enumerated**, hvis visningstilstanden **Relativ sti** bruges) af typen **Liste over poster**. Derfor vil de indlejrede elementer i denne PDF-gruppe blive udfyldt for hver post fra listen over bundne poster på kørselstidspunktet. På denne måde oprettes de enkelte PDF-linjer stort set, når for hvert N'te af 42 poster af **Paging.PageN.Enumerated**-listen følgende PDF-felter er udfyldt: Dato N, Retning N, Vare N osv. I denne henseende svarer funktionsmåden i dette **Feltgruppe**-formatelement derfor til funktionsmåden for formatelementerne **XML \> Sekvens** og **Tekst \> Sekvens**.

3. Udvid **Output \> Side N \> Detaljer 2** i træet.
4. Vælg **Output \> Side N \> Detaljer 2 \> PageFooter** i træet.

    Bemærk, at **Navn** attributten for dette formatelement er defineret som **PageFooter**. Bemærk også, at **Navn** udtrykket for formatelementet er tomt.

5. Vælg **Output \> Side N \> Detaljer 2 \> Rettelse 1** i træet.

    Bemærk, at **Navn** attributten for dette formatelement er defineret som **Rettelse 1**. Bemærk også, at **Navn** udtrykket for formatelementet er defineret som **Paging.FldName("Correction",\@.Number)**.

![Formatdesigner, hvor der er valgt en tilknytning.](media/rcs-ger-filloutpdf-reviewformat2.png)

Bemærk, at **Felt**-formatelementet bruges til at udfylde et individuelt felt i et PDF-dokument, der kan udfyldes, som er defineret som en skabelon for det overordnede **PDF-fil**-formatelement. Bindingen af **PDF-fil**-formatelementet eller de indlejrede elementer, hvis det har indlejrede elementer, angiver den værdi, der er angivet i tilsvarende PDF-felter. Der kan bruges forskellige egenskaber for **Felt**-formatelementet til at angive, hvilket PDF-felt der skal udfyldes af et individuelt formatelement:

- Attributten **Navn** for formatelementet under fanen **Format**
- Udtrykket **Navn** for formatelementet under fanen **Tilknytning**

Da begge egenskaber er valgfri for et **Felt** formatelement, anvendes følgende regler til at angive PDF-destinationsfeltet:

- Hvis attributten **Navn** er tom, og **Navn** udtrykket returnerer en tom streng på kørselstidspunktet, udløses der en undtagelse på kørselstidspunktet for at give brugeren besked om, at et PDF-felt ikke kan findes i den PDF-skabelon, der bruges til at udfylde PDF-dokumentet.
- Hvis attributten **Navn** er defineret, og **Navn** udtrykket er tomt, er det PDF-felt, der har det samme navn som attributten **Navn** i formatelementet, udfyldt.
- Hvis attributten **Navn** er defineret, og **Navn** udtrykket er konfigureret, er det PDF-felt, der har det samme navn som den værdi, der returneres af udtrykket **Navn** i formatelementet, udfyldt.

> [!NOTE]
> Når et afkrydsningsfelt i PDF-skabelonen ikke tilhører en gruppe afkrydsningsfelter, vises det i det redigerbare ER-format som et **Feltelement**, der er indlejret under **PDF-fil**. Denne type PDF-afkrydsningsfelt kan angives som markeret på følgende måder:
>
> - Når det tilsvarende **Felt**-formatelement er bundet til et datakildefelt med datatypen *[Boolesk](er-formula-supported-data-types-primitive.md#boolean)*, der har værdien **Sand**.
> - Når det tilsvarende **Felt**-formatelement indeholder et indlejret **Streng**-formatelement, der er bundet til et datakildefelt, der har tekstværdien **1**, **Sand** eller **Ja**
>
> Skabelonen kan indeholde en gruppe afkrydsningsfelter, hvor der kun kan markeres ét afkrydsningsfelt ad gangen. Disse afkrydsningsfelter vises i en PDF-skabelon som flere formfelter af typen *AFKRYDSNINGSFELT*. Hvert felt har samme navn, men en anden eksportværdi. Når du importerer skabelonen til det redigerbare ER-format, vil hvert afkrydsningsfelt være repræsenteret i formatets hierarkiske struktur som et element i **afkrydsningsfeltgruppen**, der er indlejret under samme element i **afkrydsningsfeltgruppen**. Navnet på gruppeelementet **afkrydsningsfeltet** vil være lig med navnet på afkrydsningsfeltfelterne i PDF-skabelonen. Navnet på hvert **afkrydsningsfelt** vil være lig med eksportværdien for tilsvarende afkrydsningsfeltfelt i PDF-skabelonen.
>
> Du kan kun knytte et element for **afkrydsningsfeltgruppen** afkrydsningsfelt til et datakildefelt af typen *Boolesk*.

## <a name="run-the-format-configuration"></a>Køre formatkonfigurationen

### <a name="import-the-format-configuration"></a>Importere formatkonfigurationen

Derefter skal du indlæse ER-eksempelformatet **Intrastat (import fra Excel)**. Dette format er beregnet til at opdele en brugervalgt Microsoft Excel-projektmappe, der simulerer udenlandske handelstransaktioner.

1. Vælg **Exchange \> Indlæs fra XML-fil** på siden **Konfigurationer**.
2. Vælg **Gennemse**. Naviger til og vælg filen **Intrastat (import from Excel).version.1.1.xml**, som du hentede tidligere, som en forudsætning.
3. Vælg **OK**.
4. Vælg **Intrastat-model \> Intrastat (import fra Excel)** i træet.
5. Vælg **Rediger**.
6. Vælg **Ja** i indstillingen **Standard for modeltilknytning**.

    > [!NOTE]
    > Hvis du tidligere har valgt **Ja** i indstillingen **Standard for modeltilknytning** for **Intrastatmodel**-konfigurationen eller en anden konfiguration, der er indlejret under **Intrastat-model**-konfigurationen, skal du sætte denne indstilling til **Nej**.

    Når indstillingen **Standard for modeltilknytning** er sat til **Ja**, tildeles det importerede **Intrastat (import fra** Excel) ER-format som standarddatakilde til **Intrastat-rapport (PDF)**-formatkonfigurationen. Når konfiguration af formatet **Intrastat-rapport (PDF)** køres, simulerer indholdet af den Excel-projektmappe, der fortolkes af **Intrastat (import fra Excel)** ER-formatet, de udenlandske handelstransaktioner, der skal rapporteres. Følgende illustration viser et eksempel på en Excel-projektmappe.

    ![Excel-projektmappe, der indeholder eksempeldata.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Køre formatkonfigurationen

1. På siden **Konfigurationer** skal du i træet vælge **Intrastat-model \> Intrastat-rapport (PDF)**.
2. Vælg **Kør**.
3. Vælg **Gennemse**. Naviger til og vælg filen **Intrastat sample data.xlsx**, som du hentede tidligere, som en forudsætning.
4. Vælg **OK**.
5. I feltet **Rapportretning** skal du vælge **Begge** for at udfylde alle posteringer fra den importerede Excel-projektmappe i den PDF-rapport, der genereres.
6. Vælg **OK**.
7. Gennemse det PDF-dokument, som genereres.

I følgende illustration vises et eksempel på den første side i den rapport, der genereres.

![Første side i den genererede rapport.](media/rcs-ger-filloutpdf-generatedreport.png)

I følgende illustration vises et eksempel på en anden side i den rapport, der genereres.

![Anden side i den genererede rapport.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="limitations"></a>Begrænsninger

Navnene på felterne, der kan udfyldes, skal være entydige i den PDF-formular, som du planlægger at bruge som rapportskabelon. For hvert af disse felter oprettes et individuelt formatelement med det tilsvarende navn i det redigerbare ER-format, når der importeres en PDF-formular. Hvis en PDF-formular indeholder flere felter med samme navn, oprettes der et enkelt formatelement for de felter, der ikke tillader, at de udfyldes individuelt under kørslen.

## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

### <a name="when-i-run-the-er-format-to-generate-a-report-in-pdf-format-why-do-i-get-the-following-errors--cannot-handle-iref-streams-the-current-implementation-of-pdfsharp-cannot-handle-this-pdf-feature-introduced-with-acrobat-6-and-a-pdf-name-must-start-with-a-slash-"></a>Når jeg kører ER-formatet for at generere en rapport i PDF-format, hvorfor får jeg følgende fejl: **Kan ikke håndtere iref-streams. Den aktuelle implementering af PDFSharp kan ikke håndtere denne PDF-funktion, der introduceres med Acrobat 6.** og **Et PDF-navn skal starte med skråstreg (/).**

ER-strukturen bruger version 1.5 af PDFSharp-biblioteket til at generere disse PDF-rapporter. Nogle funktioner i PDF 1.5 (Adobe Reader 6.0) er endnu ikke implementeret i dette bibliotek. Derfor kan PDFSharp endnu ikke åbne nogle filer, der er markeret som **for PDF 1.5 eller højere** og kan resultere i de modtagne fejl. Brug en af følgende løsninger på dette problem:

-   Når du bruger din egen PDF-skabelon: Nedgrader skabelonen til en tidligere version af Adobe, og start med at bruge en ny skabelon i dit ER-format.
-   Når du bruger en ER-formatskabelon, der er delt med dig af en anden konfigurationsudbyder som del af en ER-løsning: Kontakt ejeren af denne ER-løsning, og angiv en beskrivelse af problemet.
-   Når du bruger den softwareproducentløsning, der indeholder en tidligere version af biblioteket PDFSharp: Kontakt ejeren af løsningen, og foreslå en opgradering til den nyere PDFSharp-version.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Designe en ER-konfiguration til generering af rapporter i OPENXML-format (november 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Designe ER-konfigurationer til at generere rapporter i Word-format](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
