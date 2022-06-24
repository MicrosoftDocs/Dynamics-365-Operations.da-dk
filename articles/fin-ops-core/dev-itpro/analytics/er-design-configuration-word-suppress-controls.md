---
title: Skjule Word-indhold i genererede rapporter
description: Denne artikel forklarer, hvordan du konfigurerer et ER-format (Elektronisk rapportering) til generering af rapporter som Microsoft Word-filer, hvor indholdskontroller tilsidesættes.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: e11b697b78c89a1758fa9e81c901bd29fe281539
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882107"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Skjule Word-indhold i genererede rapporter

[!include [banner](../includes/banner.md)]

Hvis du vil oprette Microsoft Word-rapporter som dokumenter, skal du designe en skabelon til rapporterne som et Word-dokument. Denne skabelon skal indeholde Word-indholdskontrolelementer som pladsholdere for data, der udfyldes under kørslen. Hvis du vil bruge et Word-dokument som skabelon til rapporter i Word-format, kan du [konfigurere](er-design-configuration-word.md) en ny [Elektronisk rapport (ER)](general-electronic-reporting.md) [som løsning](er-quick-start1-new-solution.md). Løsningen skal omfatte en ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder en ER-formatkomponent. Dette ER-format skal være konfigureret, så det bruger den designede skabelon til generering af rapporter.

I version 10.0.6 og senere af Dynamics 365 Finance kan du konfigurere formler i dit ER-format for at udelade visse Word-indholdskontrolelementer i genererede dokumenter.

I følgende fremgangsmåde forklares det, hvordan en bruger, der er tildelt rollen Systemadministrator eller Funktionel konsulent for elektronisk rapportering, kan konfigurere et ER-format, der genererer rapporter som Word-filer og deaktiverer nogle af indholdets kontrolelementer i de genererede rapporter, der er konfigureret ved hjælp af en Word-skabelon.

Disse trin kan udføres i GBSI-virksomheden.

## <a name="prerequisites"></a>Forudsætninger

Du skal først udføre disse trin i vejledningen for at fuldføre disse trin:

- [Designe en konfiguration til generering af rapporter i OPENXML-format](./tasks/er-design-reports-openxml-2016-11.md)
- [Genbruge Elektronisk rapporteringskonfigurationer med Excel-skabeloner til generering af rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)

Når du fuldfører trinnene i disse opgavevejledninger, forberedes følgende elementer:

- Et **eksempel-regneark** i ER-format, der er konfigureret til generering af et dokument i Word-format
- En [kladdeversion](general-electronic-reporting.md#component-versioning) af **eksempel-regneark** i ER-format, der er markeret som **Kørbar**
- En **elektronisk** betalingsmåde, der er konfigureret til at bruge **eksempelregnearksrapport** i ER-format til behandling af kreditorbetalinger

Du skal downloade og gemme følgende skabelon lokalt for eksempelrapporten:

- [Bundet Skabelon2 for betalingsrapport (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Gennemgå den downloadede Word-skabelon

1. Åbn skabelonfilen **SampleVendPaymDocReportBounded2.docx**, som du downloadede tidligere, i Word-skrivebordsprogrammet.
2. Kontrollér, at skabelonfilen indeholder en oversigtssektion, der viser de samlede betalingsbeløb for hver valutakode, der er opfyldt ved de behandlede betalinger.

    - Oversigtssektionen findes i en separat tabel i Word-dokumentet.
    - Den første række i denne tabel indeholder tabelkolonnerne som afsnitsoverskrift.
    - Den anden række i denne tabel indeholder den gentagende indholdskontrol som afsnitsdetaljer.
    - Dette indholdskontrolelement knyttes til feltet **SummaryLines** i den brugerdefinerede **rapport** XML-del for rapporten.
    - På baggrund af denne tilknytning er indholdskontrollen knyttet til elementet **SummaryLines** i det redigerbare ER-format.

    > [!NOTE]
    > Den gentagende indholdskontrol mærkes med nøglen til **SummaryLines**, der svarer til feltet i den brugerdefinerede XML-del, som den er tilknyttet.

    ![Word-skabelon eller layout.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Vælg den eksisterende ER-rapportkonfiguration

I følgende fremgangsmåde kan du genbruge den eksisterende ER-konfiguration, som du konfigurerede, da du fuldførte trinnene i de tidligere nævnte opgavevejledninger.

1. Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Vælg **Rapporteringskonfigurationer**.
3. På siden **Konfigurationer** skal du i konfigurationstræet udvide **Betalingsmodel** og vælge **Eksempel på regnearksrapport**.
4. Vælg **Designer** for at redigere kladdeversionen af det valgte ER-format.

## <a name="replace-the-current-template-with-the-new-template"></a>Erstat den aktuelle skabelon med den nye skabelon

Aktuelt bruges filen SampleVendPaymDocReportBounded.docx som en skabelon til at generere outputtet i Word-format. I følgende trin skal du udskifte denne Word-skabelon med en ny Word-skabelon SampleVendPaymDocReportBounded2.docx, som du downloadede tidligere.

1. På siden **Formatdesigner** skal du vælge **Tilknyttede filer**.
2. Vælg **Slet** på siden **Vedhæftede filer** for at fjerne den eksisterende skabelon.
3. Vælg **Ja** for at bekræfte sletningen.
4. Vælg **Ny** \> **Fil**.
5. Vælg **Gennemse**, og gå derefter til og vælg den **SampleVendPaymDocReportBounded2.docx**-fil, du har hentet tidligere.
6. Vælg **OK**.
7. Luk siden **Vedhæftede filer**.
8. På siden **Formatdesigner** i feltet **Skabelon** skal du angive **SampleVendPaymDocReportBounded2.docx**-filen.

## <a name="run-the-format-to-create-word-output"></a>Kør formatet for at oprette Word-output

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. På siden **Kreditor** på fanen **Liste** skal du vælge alle betalingerne.
3. Vælg **Betalingsstatus** \> **Ingen**.
4. Vælg **Opret betalinger**.
5. Vælg **Elektronisk** i feltet **Betalingsmåde**.
6. Vælg **GBSI OPER** i feltet **Bankkonto**.
7. Vælg **OK**.
8. Vælg **OK** i dialogboksen **Elektroniske rapportparametre**, og analyser det genererede output.

    ![Betalinger til behandling på siden Kreditorbetalinger.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Outputtet vises i Word-format og indeholder oversigtsafsnittet.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Konfigurere det format, der kan redigeres, for at udelade oversigtsafsnittet

Hvis du vil udelade oversigtssektionen i et genereret dokument på baggrund af anmodningen fra en bruger, der kører dette ER-format, skal du redigere det er-format, der kan redigeres.

1. Gå til **Elektronisk administration** \> **Arbejdsområde** \> **Elektronisk rapportering**, og åbn kladdeversionen af ER-formatet til redigering.
2. Vælg **Rapporteringskonfigurationer**. 
3. På siden **Configurations** skal du i konfigurationstræet udvide **Betalingsmodel** \> **Eksempel på regnearksrapport**.
4. Vælg **Designer**.
5. Udvid **Word** på siden **Formatdesigner** , og vælg **SummaryLines**.
6. Under fanen **Tilknytning** kan du tilføje en ny datakilde for at bede brugeren under kørslen om, hvorvidt oversigtssektionen skal udelades:

    1. Vælg **Tilføj rod**.
    2. I dialogboksen **Tilføj datakilde** skal du vælge parameteren **Generelt\Brugerinput** for at åbne dialogboksen **Egenskaber for brugerinputparameter for datakilder**.
    3. I feltet **Navn** skal du angive **uipSuppress**.
    4. I feltet **Etiket** skal du angive sektionen **Ignorer oversigt**.
    5. Vælg eller angiv **NoYes** i feltet **Operationsdatatype**.
    6. Vælg **OK**.

7. Tilføj en ny datakilde til **NoYes**-ansøgningsfastteksttype:

    1. Vælg **Tilføj rod**.
    2. I dialogboksen **Tilføj datakilde** skal du vælge **Dynamics 365 for Operations\Fasttekst** for at åbne dialogboksen **'Fasttekst'-egenskaber for datakilde**.
    3. Angiv **enumNoYes** i feltet **Navn**.
    4. I feltet **Etiket** skal du angive sektionen **Ignorer indstillinger**.
    5. Vælg eller angiv **NoYes** i feltet **Operationsdatatype**.
    6. Vælg **OK**.

8. For det valgte Element i **SummaryLines**-format skal du konfigurere den formel, der skal angive, hvornår det Word-indholdskontrol, der er tilknyttet det valgte formatelement, skal udelades:

    1. Under fanen **Tilknytning** i sektionen **Fjernet** skal du vælge **Rediger** for at åbne siden **[Formeldesigner](general-electronic-reporting-formula-designer.md)**.
    2. I feltet **Formel** skal du angive formlen `uipSuppress = enumNoYes.Yes`.
    3. Vælg **Gem**, og luk derefter siden **Formeldesigner**.

        > [!NOTE]
        > Denne formel anvendes på et genereret dokument, **når alle andre formatelementer er kørt**. For at kunne anvende denne formel findes en Word-indholdskontrol, der er kodet som et formatelement, som formlen er konfigureret til (**SummaryLines** i dette tilfælde) findes i et genereret dokument. Dette indhold fjernes derefter helt sammen med den række i Word-tabellen, det indeholder. Detaljerækken i oversigtssektionen fjernes fra det oprettede dokument.
        >
        > På designtid kan du konfigurere formlen **Fjernet** for et formatelement, selvom der ikke er nogen indholdskontrol i den Word-skabelon, du bruger, et mærkat, der svarer til navnet på et formatelement, som egenskaben **Fjernet** er konfigureret til. Når du validerer formatet på designtid, modtager du en [advarsel](er-components-inspections.md#i14) om denne uoverensstemmelse.
        >
        > Under kørslen er en undtagelse vigtigt, hvis der ikke er noget indholdskontrol i den Word-skabelon, du bruger, et mærkat, der svarer til navnet på det formatelement, som egenskaben **Fjernet** er konfigureret for.

    4. På fanen **Tilknytning** i sektionen **Fjernet** skal du angive indstillingen **Med overordnet** til **Ja**.

        > [!NOTE]
        > Du skal angive denne indstilling til **Ja** for at fjerne hele Word-tabellen som det overordnede objekt for den række, der indeholder oplysninger om oversigtssektionen. Hvis du angiver denne indstilling til **Nej**, forbliver afsnitsoverskriften i det oprettede dokument.

9. Vælg **Gem** for at gemme ændringer til det redigerbare format.

    ![Genereret output i Word-format.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Kør tilpasset format for at oprette Word-output

1. Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. Vælg den betalingskladde, du har oprettet, og vælg derefter **Linjer**.
3. Markér på siden **Kreditorbetalinger** alle rækker, og vælg derefter **Betalingsstatus** \> **Ingen**.
4. Vælg **Opret betalinger**.
5. Vælg **Elektronisk** i feltet **Betalingsmåde**.
6. Vælg **GBSI OPER** i feltet **Bankkonto**.
7. Vælg **OK**.
8. I dialogboksen **Parametre for elektronisk rapport** skal du vælge **Ja** i feltet **Ignorer oversigt**.
9. Vælg **OK**, og analyser det genererede output.

    ![Genereret output i Word-format.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Bemærk, at outputtet ikke indeholder samlesektionen, fordi det er blevet undertrykt.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Designe en konfiguration til generering af rapporter i OPENXML-format](./tasks/er-design-reports-openxml-2016-11.md)
- [Designe ny ER-konfiguration til generering af rapporter i Word-format](er-design-configuration-word.md)
- [Genbruge Elektronisk rapporteringskonfigurationer med Excel-skabeloner til generering af rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)
- [Inspicere den konfigurerede ER-komponent for at undgå kørselsproblemer](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
