---
title: Genbruge ER-konfigurationer med Excel-skabeloner til generering af rapporter i Word-format
description: Dette emne indeholder en beskrivelse af, hvordan rapportformater, der er designet til at generere rapporter som Excel-projektmapper, kan konfigureres til generering af rapporter som Word-dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 769913fd0344eb276b3b1bd055255272ca5dfffd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092710"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Genbruge ER-konfigurationer med Excel-skabeloner til generering af rapporter i Word-format

[!include [banner](../../includes/banner.md)]

Hvis du vil generere rapporter som Microsoft Word-dokumenter, kan du [konfigurere](../er-design-configuration-word.md) et nyt [elektronisk rapportering (ER)](../general-electronic-reporting.md)-[format](../general-electronic-reporting.md#FormatComponentOutbound). Du kan også genbruge et ER-format, der oprindeligt var designet til at generere rapporter som Excel-projektmapper. I dette tilfælde skal du erstatte Excel-skabelonen med en Word-skabelon.

I nedenstående procedurer vises det, hvordan en bruger i rollen Systemadministrator eller rollen Elektronisk rapporteringsudvikler kan konfigurere et ER-format, så der genereres rapporter som Word-filer, ved at genbruge et ER-format, der er beregnet til at generere rapporter som Excel-filer.

Disse procedurer kan udføres i GBSI-virksomheden.

## <a name="prerequisites"></a>Forudsætninger

For at fuldføre disse procedurer skal du først følge trinnene i opgavevejledningen [Designe en konfiguration til generering af rapporter i OPENXML-format](er-design-reports-openxml-2016-11.md).

Du skal downloade og gemme følgende skabeloner lokalt for eksempelrapporten:

- [Skabelon for betalingsrapport (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Bundet skabelon for betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Disse procedurer er til en funktion, der er tilføjet i Dynamics 365 for Operations version 1611 (november 2016).

## <a name="select-the-existing-er-report-configuration"></a>Vælg den eksisterende ER-rapportkonfiguration

1. Gå i Dynamics 365 Finance til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.
2. Sørg for, at konfigurationsudbyderen **Litware, Inc.** er valgt som **Aktiv**. Hvis den ikke er, skal du følge trinnene i opgavevejledningen [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).
3. Vælg **Rapporteringskonfigurationer**. Du skal genbruge den eksisterende ER-konfiguration, der er udviklet til at generere rapportoutput i OPENXML-format.
4. På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og vælge **Eksempel på regnearksrapport**.

    > [!NOTE]
    > I oversigtspanelet **Versioner** kan du redigere kladdeversionen af det valgte ER-format.

5. Vælg **Designer**.
6. Bemærk, at titlen på rodformatelementet på siden **Formatdesigner** angiver, at der aktuelt bruges en Excel-skabelon.

![Vælge den eksisterende konfiguration](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Gennemgå den downloadede Word-skabelon

1. Åbn skabelonfilen **SampleVendPaymDocReport.docx**, som du downloadede tidligere, i Word-skrivebordsprogrammet.
2. Sørg for, at skabelonen kun indeholder layoutet af det dokument, du vil generere som ER-output.

![Word-skabelonlayoutet i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Erstatte Excel-skabelonen med Word-skabelonen og tilføje en brugerdefineret XML-del

Aktuelt bruges Excel-dokumentet som en skabelon til at generere outputtet i OPENXML-format. Du skal erstatte denne skabelon med Word-skabelonen SampleVendPaymDocReport.docx, som du downloadede tidligere. Du skal også udvide Word-skabelonen ved at tilføje en brugerdefineret XML-del.

1. På siden **Formatdesigner** i Finans skal du under fanen **Format** vælge **Vedhæftede filer**.
2. Vælg **Slet** på siden **Vedhæftede filer** for at fjerne den eksisterende Excel-skabelon. Vælg **Ja** for at bekræfte ændringen.
3. Vælg **Ny** \> **Fil**.

    > [!NOTE]
    > Du skal vælge en dokumenttype, der er [konfigureret](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parametrene, til at gemme skabeloner i ER-format.

4. Vælg **Gennemse**, og gå derefter til og vælg den **SampleVendPaymDocReport.docx**-fil, du har hentet tidligere.
5. Vælg **OK**.
6. Luk siden **Vedhæftede filer**.
7. På siden **Formatdesigner** skal du i feltet **Skabelon** angive eller vælge filen **SampleVendPaymDocReport.docx** for at bruge denne Word-skabelon i stedet for den Excel-skabelon, der tidligere er brugt.
8. Vælg **Gem**.

    I tillæg til at lagre konfigurationsændringer opdaterer handlingen **Gem** også den vedhæftede Word-skabelon. Den hierarkiske struktur på det designede format føjes til det vedhæftede Word-dokument som en ny brugerdefineret XML-del med navnet **Rapport**. Den vedhæftede Word-skabelon indeholder layoutet på det dokument, der genereres som ER-output, og den struktur af data, som ER udfylder i denne skabelon på kørselstidspunktet.

9. Bemærk, at titlen på rodformatelementet angiver, at der aktuelt bruges en Word-skabelon.

    ![Erstatning af Excel-skabelonen med Word-skabelonen og tilføjelse af en brugerdefineret XML-del](../media/er-design-configuration-word-2016-11-image03.gif)

10. Vælg **Vedhæftede filer** under fanen **Formater**.

Du kan nu knytte elementerne i den brugerdefinerede XML-del **Rapport** til indholdskontrolelementerne i Word-dokumentet.

Hvis du har kendskab til design af Word-dokumenter som formularer, der indeholder [indholdskontrolelementer](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), der er knyttet til elementer i [brugerdefinerede XML-dele](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), skal du fuldføre alle trin i den næste procedure for at oprette dokumentet. Du kan finde flere oplysninger under [Oprette formularer, som brugere udfylder eller udskriver i Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Ellers skal du springe næste procedure over.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Hente et Word-dokument, der har en brugerdefineret XML-del, og udføre datatilknytning

1. I Finans skal du vælge **Åbn** på siden **Vedhæftede filer** for at downloade den valgte skabelon fra Finans og gemme den lokalt som et Word-dokument.
3. Åbn det dokument, du lige har downloadet, i Word-skrivebordsprogrammet.
4. Vælg **XML-tilknytningsrude** under fanen **Udvikler**.

    > [!NOTE]
    > Hvis fanen **Udvikler** ikke vises på båndet, skal du tilpasse båndet for at tilføje den.

5. Vælg i feltet **Brugerdefineret XML-del** i ruden **XML-tilknytning** den brugerdefinerede del **Rapport**.
6. Tilknyt elementerne i den valgte brugerdefinerede XML-del **Rapport** og indholdskontrolelementerne i Word-dokumentet.
7. Gem det opdaterede Word-dokument lokalt som **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Gennemgå Word-skabelonen, hvor den brugerdefinerede XML-del er knyttet til indholdskontrolelementer

1. Åbn skabelonfilen **SampleVendPaymDocReportBounded.docx** i Word-skrivebordsprogrammet.
2. Sørg for, at skabelonen indeholder layoutet af det dokument, du vil generere som ER-output. De indholdskontrolelementer, der bruges som pladsholdere for data, som ER indtaster i denne skabelon under kørslen, er baseret på de tilknytninger, der er konfigureret mellem elementer i den brugerdefinerede XML-del **Rapport** og indholdets kontrolelementer i Word-dokumentet.

![Word-skabeloneksempel i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Uploade Word-skabelonen, hvor den brugerdefinerede XML-del er knyttet til indholdskontrolelementer

1. I Finans skal du vælge **Slet** på siden **Vedhæftede filer** for at fjerne den Word-skabelon, der ikke har tilknytninger mellem elementer i den brugerdefinerede XML-del **Rapport** og kontrolelementer til indhold. Vælg **Ja** for at bekræfte ændringen.
2. Vælg **Ny** \> **Fil** for at tilføje en ny skabelonfil, der indeholder tilknytninger mellem elementer i den brugerdefinerede XML-del **Rapport** og kontrolelementer til indhold.

    > [!NOTE]
    > Du skal vælge en dokumenttype, der er [konfigureret](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parametrene, til at gemme skabeloner i ER-format.

3. Vælg **Gennemse**, og gå til og vælg den **SampleVendPaymDocReportBounded.docx**-fil, du har hentet eller forberedt ved at gennemføre proceduren i afsnittet [Få Word med brugerdefineret XML-del til at udføre databindinger](#get-word-doc).
4. Vælg **OK**.
5. Luk siden **Vedhæftede filer**.
6. Vælg det dokument, du lige har hentet, i feltet **Skabelon** på siden **Formatdesigner**.
7. Vælg **Gem**.
8. Luk siden **Formatdesigner**.

## <a name="mark-the-configured-format-as-runnable"></a>Markere det konfigurerede format som kørbart

Hvis du vil køre kladdeversionen af det format, der kan redigeres, skal du gøre det [kørbart](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. På siden **Konfigurationer** i handlingsruden i Finans skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.
2. I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.
3. Vælg **Rediger** for at gøre den aktuelle side redigerbar efter behov.
4. For den aktuelt valgte konfiguration af **Eksempel på regnearksrapport** skal du angive indstillingen **Kør kladde** til **Ja**.
5. Vælg **Gem**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Køre formatet for at oprette output i Word-format

1. Gå i Finans til **Kreditor** \> **Betalinger** \> **Betalingskladde**.
2. Vælg **Linjer** i en betalingskladde, du indtastede tidligere.
3. Markér alle rækker i gitteret på siden **Kreditorbetalinger**.
4. Vælg **Betalingsstatus** \> **Ingen**.

    ![Betalinger til behandling på siden Kreditorbetalinger](../media/er-design-configuration-word-2016-11-image05.png)

5. Vælg **Opret betalinger** i handlingsruden.
6. Følg disse trin i den viste dialogboks:

    1. Vælg **Elektronisk** i feltet **Betalingsmåde**.
    2. Vælg **GBSI OPER** i feltet **Bankkonto**.
    3. Vælg **OK**.

7. Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.
8. Det oprettede output vises i Word-format og indeholder oplysninger om de behandlede betalinger. Analysér det genererede output.

    ![Genereret output i Word-format](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Yderligere ressourcer

- [Designe ny ER-konfiguration til generering af rapporter i Word-format](../er-design-configuration-word.md)
- [Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]