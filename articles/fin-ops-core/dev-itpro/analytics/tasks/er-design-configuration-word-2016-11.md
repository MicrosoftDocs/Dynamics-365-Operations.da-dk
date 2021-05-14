---
title: Genbruge ER-konfigurationer med Excel-skabeloner til generering af rapporter i Word-format
description: Dette emne indeholder en beskrivelse af, hvordan rapportformater, der er designet til at generere rapporter som Excel-projektmapper, kan konfigureres til generering af rapporter som Word-dokumenter.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 413be634e80b87781444e1c1445c78691f4b4b0b
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944286"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="80ca0-103">Genbruge ER-konfigurationer med Excel-skabeloner til generering af rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="80ca0-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80ca0-104">Hvis du vil generere rapporter som Microsoft Word-dokumenter, kan du [konfigurere](../er-design-configuration-word.md) et nyt [elektronisk rapportering (ER)](../general-electronic-reporting.md)-[format](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="80ca0-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="80ca0-105">Du kan også genbruge et ER-format, der oprindeligt var designet til at generere rapporter som Excel-projektmapper.</span><span class="sxs-lookup"><span data-stu-id="80ca0-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="80ca0-106">I dette tilfælde skal du erstatte Excel-skabelonen med en Word-skabelon.</span><span class="sxs-lookup"><span data-stu-id="80ca0-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="80ca0-107">I nedenstående procedurer vises det, hvordan en bruger i rollen Systemadministrator eller rollen Elektronisk rapporteringsudvikler kan konfigurere et ER-format, så der genereres rapporter som Word-filer, ved at genbruge et ER-format, der er beregnet til at generere rapporter som Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="80ca0-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="80ca0-108">Disse procedurer kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="80ca0-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="80ca0-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="80ca0-109">Prerequisites</span></span>

<span data-ttu-id="80ca0-110">For at fuldføre disse procedurer skal du først følge trinnene i opgavevejledningen [Designe en konfiguration til generering af rapporter i OPENXML-format](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="80ca0-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="80ca0-111">Du skal downloade og gemme følgende skabeloner lokalt for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="80ca0-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="80ca0-112">Skabelon for betalingsrapport (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="80ca0-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [<span data-ttu-id="80ca0-113">Bundet skabelon for betalingsrapport (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="80ca0-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

<span data-ttu-id="80ca0-114">Disse procedurer er til en funktion, der er tilføjet i Dynamics 365 for Operations version 1611 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="80ca0-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="80ca0-115">Vælg den eksisterende ER-rapportkonfiguration</span><span class="sxs-lookup"><span data-stu-id="80ca0-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="80ca0-116">Gå i Dynamics 365 Finance til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="80ca0-117">Sørg for, at konfigurationsudbyderen **Litware, Inc.** er valgt som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="80ca0-118">Hvis den ikke er, skal du følge trinnene i opgavevejledningen [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="80ca0-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="80ca0-119">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="80ca0-120">Du skal genbruge den eksisterende ER-konfiguration, der er udviklet til at generere rapportoutput i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="80ca0-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="80ca0-121">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og vælge **Eksempel på regnearksrapport**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80ca0-122">I oversigtspanelet **Versioner** kan du redigere kladdeversionen af det valgte ER-format.</span><span class="sxs-lookup"><span data-stu-id="80ca0-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="80ca0-123">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-123">Select **Designer**.</span></span>
6. <span data-ttu-id="80ca0-124">Bemærk, at titlen på rodformatelementet på siden **Formatdesigner** angiver, at der aktuelt bruges en Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="80ca0-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Vælge den eksisterende konfiguration](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="80ca0-126">Gennemgå den downloadede Word-skabelon</span><span class="sxs-lookup"><span data-stu-id="80ca0-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="80ca0-127">Åbn skabelonfilen **SampleVendPaymDocReport.docx**, som du downloadede tidligere, i Word-skrivebordsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="80ca0-128">Sørg for, at skabelonen kun indeholder layoutet af det dokument, du vil generere som ER-output.</span><span class="sxs-lookup"><span data-stu-id="80ca0-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Word-skabelonlayoutet i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="80ca0-130">Erstatte Excel-skabelonen med Word-skabelonen og tilføje en brugerdefineret XML-del</span><span class="sxs-lookup"><span data-stu-id="80ca0-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="80ca0-131">Aktuelt bruges Excel-dokumentet som en skabelon til at generere outputtet i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="80ca0-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="80ca0-132">Du skal erstatte denne skabelon med Word-skabelonen SampleVendPaymDocReport.docx, som du downloadede tidligere.</span><span class="sxs-lookup"><span data-stu-id="80ca0-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="80ca0-133">Du skal også udvide Word-skabelonen ved at tilføje en brugerdefineret XML-del.</span><span class="sxs-lookup"><span data-stu-id="80ca0-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="80ca0-134">På siden **Formatdesigner** i Finans skal du under fanen **Format** vælge **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="80ca0-135">Vælg **Slet** på siden **Vedhæftede filer** for at fjerne den eksisterende Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="80ca0-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="80ca0-136">Vælg **Ja** for at bekræfte ændringen.</span><span class="sxs-lookup"><span data-stu-id="80ca0-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="80ca0-137">Vælg **Ny** \> **Fil**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80ca0-138">Du skal vælge en dokumenttype, der er [konfigureret](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parametrene, til at gemme skabeloner i ER-format.</span><span class="sxs-lookup"><span data-stu-id="80ca0-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="80ca0-139">Vælg **Gennemse**, og gå derefter til og vælg den **SampleVendPaymDocReport.docx**-fil, du har hentet tidligere.</span><span class="sxs-lookup"><span data-stu-id="80ca0-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="80ca0-140">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-140">Select **OK**.</span></span>
6. <span data-ttu-id="80ca0-141">Luk siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="80ca0-142">På siden **Formatdesigner** skal du i feltet **Skabelon** angive eller vælge filen **SampleVendPaymDocReport.docx** for at bruge denne Word-skabelon i stedet for den Excel-skabelon, der tidligere er brugt.</span><span class="sxs-lookup"><span data-stu-id="80ca0-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="80ca0-143">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-143">Select **Save**.</span></span>

    <span data-ttu-id="80ca0-144">I tillæg til at lagre konfigurationsændringer opdaterer handlingen **Gem** også den vedhæftede Word-skabelon.</span><span class="sxs-lookup"><span data-stu-id="80ca0-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="80ca0-145">Den hierarkiske struktur på det designede format føjes til det vedhæftede Word-dokument som en ny brugerdefineret XML-del med navnet **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="80ca0-146">Den vedhæftede Word-skabelon indeholder layoutet på det dokument, der genereres som ER-output, og den struktur af data, som ER udfylder i denne skabelon på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="80ca0-147">Bemærk, at titlen på rodformatelementet angiver, at der aktuelt bruges en Word-skabelon.</span><span class="sxs-lookup"><span data-stu-id="80ca0-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Erstatning af Excel-skabelonen med Word-skabelonen og tilføjelse af en brugerdefineret XML-del](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="80ca0-149">Vælg **Vedhæftede filer** under fanen **Formater**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="80ca0-150">Du kan nu knytte elementerne i den brugerdefinerede XML-del **Rapport** til indholdskontrolelementerne i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="80ca0-151">Hvis du har kendskab til design af Word-dokumenter som formularer, der indeholder [indholdskontrolelementer](/office/client-developer/word/content-controls-in-word), der er knyttet til elementer i [brugerdefinerede XML-dele](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), skal du fuldføre alle trin i den næste procedure for at oprette dokumentet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="80ca0-152">Du kan finde flere oplysninger under [Oprette formularer, som brugere udfylder eller udskriver i Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="80ca0-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="80ca0-153">Ellers skal du springe næste procedure over.</span><span class="sxs-lookup"><span data-stu-id="80ca0-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="80ca0-154">Hente et Word-dokument, der har en brugerdefineret XML-del, og udføre datatilknytning</span><span class="sxs-lookup"><span data-stu-id="80ca0-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="80ca0-155">I Finans skal du vælge **Åbn** på siden **Vedhæftede filer** for at downloade den valgte skabelon fra Finans og gemme den lokalt som et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="80ca0-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="80ca0-156">Åbn det dokument, du lige har downloadet, i Word-skrivebordsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="80ca0-157">Vælg **XML-tilknytningsrude** under fanen **Udvikler**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80ca0-158">Hvis fanen **Udvikler** ikke vises på båndet, skal du tilpasse båndet for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="80ca0-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="80ca0-159">Vælg i feltet **Brugerdefineret XML-del** i ruden **XML-tilknytning** den brugerdefinerede del **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="80ca0-160">Tilknyt elementerne i den valgte brugerdefinerede XML-del **Rapport** og indholdskontrolelementerne i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="80ca0-161">Gem det opdaterede Word-dokument lokalt som **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="80ca0-162">Gennemgå Word-skabelonen, hvor den brugerdefinerede XML-del er knyttet til indholdskontrolelementer</span><span class="sxs-lookup"><span data-stu-id="80ca0-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="80ca0-163">Åbn skabelonfilen **SampleVendPaymDocReportBounded.docx** i Word-skrivebordsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="80ca0-164">Sørg for, at skabelonen indeholder layoutet af det dokument, du vil generere som ER-output.</span><span class="sxs-lookup"><span data-stu-id="80ca0-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="80ca0-165">De indholdskontrolelementer, der bruges som pladsholdere for data, som ER indtaster i denne skabelon under kørslen, er baseret på de tilknytninger, der er konfigureret mellem elementer i den brugerdefinerede XML-del **Rapport** og indholdets kontrolelementer i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="80ca0-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Word-skabeloneksempel i skrivebordsprogrammet](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="80ca0-167">Uploade Word-skabelonen, hvor den brugerdefinerede XML-del er knyttet til indholdskontrolelementer</span><span class="sxs-lookup"><span data-stu-id="80ca0-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="80ca0-168">I Finans skal du vælge **Slet** på siden **Vedhæftede filer** for at fjerne den Word-skabelon, der ikke har tilknytninger mellem elementer i den brugerdefinerede XML-del **Rapport** og kontrolelementer til indhold.</span><span class="sxs-lookup"><span data-stu-id="80ca0-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="80ca0-169">Vælg **Ja** for at bekræfte ændringen.</span><span class="sxs-lookup"><span data-stu-id="80ca0-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="80ca0-170">Vælg **Ny** \> **Fil** for at tilføje en ny skabelonfil, der indeholder tilknytninger mellem elementer i den brugerdefinerede XML-del **Rapport** og kontrolelementer til indhold.</span><span class="sxs-lookup"><span data-stu-id="80ca0-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="80ca0-171">Du skal vælge en dokumenttype, der er [konfigureret](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) i ER-parametrene, til at gemme skabeloner i ER-format.</span><span class="sxs-lookup"><span data-stu-id="80ca0-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="80ca0-172">Vælg **Gennemse**, og gå til og vælg den **SampleVendPaymDocReportBounded.docx**-fil, du har hentet eller forberedt ved at gennemføre proceduren i afsnittet [Få Word med brugerdefineret XML-del til at udføre databindinger](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="80ca0-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="80ca0-173">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-173">Select **OK**.</span></span>
5. <span data-ttu-id="80ca0-174">Luk siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="80ca0-175">Vælg det dokument, du lige har hentet, i feltet **Skabelon** på siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="80ca0-176">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-176">Select **Save**.</span></span>
8. <span data-ttu-id="80ca0-177">Luk siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="80ca0-178">Markere det konfigurerede format som kørbart</span><span class="sxs-lookup"><span data-stu-id="80ca0-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="80ca0-179">Hvis du vil køre kladdeversionen af det format, der kan redigeres, skal du gøre det [kørbart](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="80ca0-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="80ca0-180">På siden **Konfigurationer** i handlingsruden i Finans skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="80ca0-181">I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="80ca0-182">Vælg **Rediger** for at gøre den aktuelle side redigerbar efter behov.</span><span class="sxs-lookup"><span data-stu-id="80ca0-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="80ca0-183">For den aktuelt valgte konfiguration af **Eksempel på regnearksrapport** skal du angive indstillingen **Kør kladde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="80ca0-184">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="80ca0-185">Køre formatet for at oprette output i Word-format</span><span class="sxs-lookup"><span data-stu-id="80ca0-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="80ca0-186">Gå i Finans til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="80ca0-187">Vælg **Linjer** i en betalingskladde, du indtastede tidligere.</span><span class="sxs-lookup"><span data-stu-id="80ca0-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="80ca0-188">Markér alle rækker i gitteret på siden **Kreditorbetalinger**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="80ca0-189">Vælg **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-189">Select **Payment status** \> **None**.</span></span>

    ![Betalinger til behandling på siden Kreditorbetalinger](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="80ca0-191">Vælg **Opret betalinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="80ca0-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="80ca0-192">Følg disse trin i den viste dialogboks:</span><span class="sxs-lookup"><span data-stu-id="80ca0-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="80ca0-193">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="80ca0-194">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="80ca0-195">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-195">Select **OK**.</span></span>

7. <span data-ttu-id="80ca0-196">Vælg **OK** i dialogboksen **Elektroniske rapporteringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="80ca0-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="80ca0-197">Det oprettede output vises i Word-format og indeholder oplysninger om de behandlede betalinger.</span><span class="sxs-lookup"><span data-stu-id="80ca0-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="80ca0-198">Analysér det genererede output.</span><span class="sxs-lookup"><span data-stu-id="80ca0-198">Analyze the generated output.</span></span>

    ![Genereret output i Word-format](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="80ca0-200">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="80ca0-200">Additional resources</span></span>

- [<span data-ttu-id="80ca0-201">Designe ny ER-konfiguration til generering af rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="80ca0-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="80ca0-202">Integrere billeder og figurer i de dokumenter, du opretter ved hjælp af ER</span><span class="sxs-lookup"><span data-stu-id="80ca0-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
