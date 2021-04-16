---
title: Skjule Word-indhold i genererede rapporter
description: Dette emne forklarer, hvordan du konfigurerer et ER-format (Elektronisk rapportering) til generering af rapporter som Microsoft Word-filer, hvor indholdskontroller tilsidesættes.
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
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753594"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="c675e-103">Skjule Word-indhold i genererede rapporter</span><span class="sxs-lookup"><span data-stu-id="c675e-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c675e-104">Hvis du vil oprette Microsoft Word-rapporter som dokumenter, skal du designe en skabelon til rapporterne som et Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="c675e-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="c675e-105">Denne skabelon skal indeholde Word-indholdskontrolelementer som pladsholdere for data, der udfyldes under kørslen.</span><span class="sxs-lookup"><span data-stu-id="c675e-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="c675e-106">Hvis du vil bruge et Word-dokument som skabelon til rapporter i Word-format, kan du [konfigurere](er-design-configuration-word.md) en ny [Elektronisk rapport (ER)](general-electronic-reporting.md) [som løsning](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="c675e-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="c675e-107">Løsningen skal omfatte en ER-[konfiguration](general-electronic-reporting.md#Configuration), der indeholder en ER-[formatkomponent](general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="c675e-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c675e-108">Dette ER-format skal være konfigureret, så det bruger den designede skabelon til generering af rapporter.</span><span class="sxs-lookup"><span data-stu-id="c675e-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="c675e-109">I version 10.0.6 og senere af Dynamics 365 Finance kan du konfigurere formler i dit ER-format for at udelade visse Word-indholdskontrolelementer i genererede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="c675e-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="c675e-110">I følgende fremgangsmåde forklares det, hvordan en bruger, der er tildelt rollen Systemadministrator eller Funktionel konsulent for elektronisk rapportering, kan konfigurere et ER-format, der genererer rapporter som Word-filer og deaktiverer nogle af indholdets kontrolelementer i de genererede rapporter, der er konfigureret ved hjælp af en Word-skabelon.</span><span class="sxs-lookup"><span data-stu-id="c675e-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="c675e-111">Disse trin kan udføres i GBSI-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="c675e-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c675e-112">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="c675e-112">Prerequisites</span></span>

<span data-ttu-id="c675e-113">Du skal først udføre disse trin i vejledningen for at fuldføre disse trin:</span><span class="sxs-lookup"><span data-stu-id="c675e-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="c675e-114">Designe en konfiguration til generering af rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="c675e-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="c675e-115">Genbruge Elektronisk rapporteringskonfigurationer med Excel-skabeloner til generering af rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="c675e-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="c675e-116">Når du fuldfører trinnene i disse opgavevejledninger, forberedes følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="c675e-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="c675e-117">Et **eksempel-regneark** i ER-format, der er konfigureret til generering af et dokument i Word-format</span><span class="sxs-lookup"><span data-stu-id="c675e-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="c675e-118">En [kladdeversion](general-electronic-reporting.md#component-versioning) af **eksempel-regneark** i ER-format, der er markeret som **Kørbar**</span><span class="sxs-lookup"><span data-stu-id="c675e-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="c675e-119">En **elektronisk** betalingsmåde, der er konfigureret til at bruge **eksempelregnearksrapport** i ER-format til behandling af kreditorbetalinger</span><span class="sxs-lookup"><span data-stu-id="c675e-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="c675e-120">Du skal downloade og gemme følgende skabelon lokalt for eksempelrapporten:</span><span class="sxs-lookup"><span data-stu-id="c675e-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="c675e-121">Bundet Skabelon2 for betalingsrapport (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="c675e-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="c675e-122">Gennemgå den downloadede Word-skabelon</span><span class="sxs-lookup"><span data-stu-id="c675e-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="c675e-123">Åbn skabelonfilen **SampleVendPaymDocReportBounded2.docx**, som du downloadede tidligere, i Word-skrivebordsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="c675e-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="c675e-124">Kontrollér, at skabelonfilen indeholder en oversigtssektion, der viser de samlede betalingsbeløb for hver valutakode, der er opfyldt ved de behandlede betalinger.</span><span class="sxs-lookup"><span data-stu-id="c675e-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="c675e-125">Oversigtssektionen findes i en separat tabel i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="c675e-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="c675e-126">Den første række i denne tabel indeholder tabelkolonnerne som afsnitsoverskrift.</span><span class="sxs-lookup"><span data-stu-id="c675e-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="c675e-127">Den anden række i denne tabel indeholder den gentagende indholdskontrol som afsnitsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c675e-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="c675e-128">Dette indholdskontrolelement knyttes til feltet **SummaryLines** i den brugerdefinerede **rapport** XML-del for rapporten.</span><span class="sxs-lookup"><span data-stu-id="c675e-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="c675e-129">På baggrund af denne tilknytning er indholdskontrollen knyttet til elementet **SummaryLines** i det redigerbare ER-format.</span><span class="sxs-lookup"><span data-stu-id="c675e-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c675e-130">Den gentagende indholdskontrol mærkes med nøglen til **SummaryLines**, der svarer til feltet i den brugerdefinerede XML-del, som den er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="c675e-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word-skabelon eller layout](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="c675e-132">Vælg den eksisterende ER-rapportkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c675e-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="c675e-133">I følgende fremgangsmåde kan du genbruge den eksisterende ER-konfiguration, som du konfigurerede, da du fuldførte trinnene i de tidligere nævnte opgavevejledninger.</span><span class="sxs-lookup"><span data-stu-id="c675e-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="c675e-134">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c675e-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c675e-135">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="c675e-136">På siden **Konfigurationer** skal du i konfigurationstræet udvide **Betalingsmodel** og vælge **Eksempel på regnearksrapport**.</span><span class="sxs-lookup"><span data-stu-id="c675e-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="c675e-137">Vælg **Designer** for at redigere kladdeversionen af det valgte ER-format.</span><span class="sxs-lookup"><span data-stu-id="c675e-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="c675e-138">Erstat den aktuelle skabelon med den nye skabelon</span><span class="sxs-lookup"><span data-stu-id="c675e-138">Replace the current template with the new template</span></span>

<span data-ttu-id="c675e-139">Aktuelt bruges filen SampleVendPaymDocReportBounded.docx som en skabelon til at generere outputtet i Word-format.</span><span class="sxs-lookup"><span data-stu-id="c675e-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="c675e-140">I følgende trin skal du udskifte denne Word-skabelon med en ny Word-skabelon SampleVendPaymDocReportBounded2.docx, som du downloadede tidligere.</span><span class="sxs-lookup"><span data-stu-id="c675e-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="c675e-141">På siden **Formatdesigner** skal du vælge **Tilknyttede filer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="c675e-142">Vælg **Slet** på siden **Vedhæftede filer** for at fjerne den eksisterende skabelon.</span><span class="sxs-lookup"><span data-stu-id="c675e-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="c675e-143">Vælg **Ja** for at bekræfte sletningen.</span><span class="sxs-lookup"><span data-stu-id="c675e-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="c675e-144">Vælg **Ny** \> **Fil**.</span><span class="sxs-lookup"><span data-stu-id="c675e-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="c675e-145">Vælg **Gennemse**, og gå derefter til og vælg den **SampleVendPaymDocReportBounded2.docx**-fil, du har hentet tidligere.</span><span class="sxs-lookup"><span data-stu-id="c675e-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="c675e-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c675e-146">Select **OK**.</span></span>
7. <span data-ttu-id="c675e-147">Luk siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="c675e-148">På siden **Formatdesigner** i feltet **Skabelon** skal du angive **SampleVendPaymDocReportBounded2.docx**-filen.</span><span class="sxs-lookup"><span data-stu-id="c675e-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="c675e-149">Kør formatet for at oprette Word-output</span><span class="sxs-lookup"><span data-stu-id="c675e-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="c675e-150">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="c675e-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="c675e-151">På siden **Kreditor** på fanen **Liste** skal du vælge alle betalingerne.</span><span class="sxs-lookup"><span data-stu-id="c675e-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="c675e-152">Vælg **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="c675e-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="c675e-153">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="c675e-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="c675e-154">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="c675e-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="c675e-155">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="c675e-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="c675e-156">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c675e-156">Select **OK**.</span></span>
8. <span data-ttu-id="c675e-157">Vælg **OK** i dialogboksen **Elektroniske rapportparametre**, og analyser det genererede output.</span><span class="sxs-lookup"><span data-stu-id="c675e-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Betalinger til behandling på siden Kreditorbetalinger](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="c675e-159">Outputtet vises i Word-format og indeholder oversigtsafsnittet.</span><span class="sxs-lookup"><span data-stu-id="c675e-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="c675e-160">Konfigurere det format, der kan redigeres, for at udelade oversigtsafsnittet</span><span class="sxs-lookup"><span data-stu-id="c675e-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="c675e-161">Hvis du vil udelade oversigtssektionen i et genereret dokument på baggrund af anmodningen fra en bruger, der kører dette ER-format, skal du redigere det er-format, der kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="c675e-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="c675e-162">Gå til **Elektronisk administration** \> **Arbejdsområde** \> **Elektronisk rapportering**, og åbn kladdeversionen af ER-formatet til redigering.</span><span class="sxs-lookup"><span data-stu-id="c675e-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="c675e-163">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="c675e-164">På siden **Configurations** skal du i konfigurationstræet udvide **Betalingsmodel** \> **Eksempel på regnearksrapport**.</span><span class="sxs-lookup"><span data-stu-id="c675e-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="c675e-165">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-165">Select **Designer**.</span></span>
5. <span data-ttu-id="c675e-166">Udvid **Word** på siden **Formatdesigner** , og vælg **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="c675e-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="c675e-167">Under fanen **Tilknytning** kan du tilføje en ny datakilde for at bede brugeren under kørslen om, hvorvidt oversigtssektionen skal udelades:</span><span class="sxs-lookup"><span data-stu-id="c675e-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="c675e-168">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="c675e-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="c675e-169">I dialogboksen **Tilføj datakilde** skal du vælge parameteren **Generelt\Brugerinput** for at åbne dialogboksen **Egenskaber for brugerinputparameter for datakilder**.</span><span class="sxs-lookup"><span data-stu-id="c675e-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="c675e-170">I feltet **Navn** skal du angive **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="c675e-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="c675e-171">I feltet **Etiket** skal du angive sektionen **Ignorer oversigt**.</span><span class="sxs-lookup"><span data-stu-id="c675e-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="c675e-172">Vælg eller angiv **NoYes** i feltet **Operationsdatatype**.</span><span class="sxs-lookup"><span data-stu-id="c675e-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="c675e-173">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c675e-173">Select **OK**.</span></span>

7. <span data-ttu-id="c675e-174">Tilføj en ny datakilde til **NoYes**-ansøgningsfastteksttype:</span><span class="sxs-lookup"><span data-stu-id="c675e-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="c675e-175">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="c675e-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="c675e-176">I dialogboksen **Tilføj datakilde** skal du vælge **Dynamics 365 for Operations\Fasttekst** for at åbne dialogboksen **'Fasttekst'-egenskaber for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="c675e-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="c675e-177">Angiv **enumNoYes** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c675e-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="c675e-178">I feltet **Etiket** skal du angive sektionen **Ignorer indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c675e-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="c675e-179">Vælg eller angiv **NoYes** i feltet **Operationsdatatype**.</span><span class="sxs-lookup"><span data-stu-id="c675e-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="c675e-180">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c675e-180">Select **OK**.</span></span>

8. <span data-ttu-id="c675e-181">For det valgte Element i **SummaryLines**-format skal du konfigurere den formel, der skal angive, hvornår det Word-indholdskontrol, der er tilknyttet det valgte formatelement, skal udelades:</span><span class="sxs-lookup"><span data-stu-id="c675e-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="c675e-182">Under fanen **Tilknytning** i sektionen **Fjernet** skal du vælge **Rediger** for at åbne siden **[Formeldesigner](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="c675e-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="c675e-183">I feltet **Formel** skal du angive formlen `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="c675e-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="c675e-184">Vælg **Gem**, og luk derefter siden **Formeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="c675e-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c675e-185">Denne formel anvendes på et genereret dokument, **når alle andre formatelementer er kørt**.</span><span class="sxs-lookup"><span data-stu-id="c675e-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="c675e-186">For at kunne anvende denne formel findes en Word-indholdskontrol, der er kodet som et formatelement, som formlen er konfigureret til (**SummaryLines** i dette tilfælde) findes i et genereret dokument.</span><span class="sxs-lookup"><span data-stu-id="c675e-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="c675e-187">Dette indhold fjernes derefter helt sammen med den række i Word-tabellen, det indeholder.</span><span class="sxs-lookup"><span data-stu-id="c675e-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="c675e-188">Detaljerækken i oversigtssektionen fjernes fra det oprettede dokument.</span><span class="sxs-lookup"><span data-stu-id="c675e-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="c675e-189">På designtid kan du konfigurere formlen **Fjernet** for et formatelement, selvom der ikke er nogen indholdskontrol i den Word-skabelon, du bruger, et mærkat, der svarer til navnet på et formatelement, som egenskaben **Fjernet** er konfigureret til.</span><span class="sxs-lookup"><span data-stu-id="c675e-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="c675e-190">Når du validerer formatet på designtid, modtager du en [advarsel](er-components-inspections.md#i14) om denne uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="c675e-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="c675e-191">Under kørslen er en undtagelse vigtigt, hvis der ikke er noget indholdskontrol i den Word-skabelon, du bruger, et mærkat, der svarer til navnet på det formatelement, som egenskaben **Fjernet** er konfigureret for.</span><span class="sxs-lookup"><span data-stu-id="c675e-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="c675e-192">På fanen **Tilknytning** i sektionen **Fjernet** skal du angive indstillingen **Med overordnet** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c675e-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c675e-193">Du skal angive denne indstilling til **Ja** for at fjerne hele Word-tabellen som det overordnede objekt for den række, der indeholder oplysninger om oversigtssektionen.</span><span class="sxs-lookup"><span data-stu-id="c675e-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="c675e-194">Hvis du angiver denne indstilling til **Nej**, forbliver afsnitsoverskriften i det oprettede dokument.</span><span class="sxs-lookup"><span data-stu-id="c675e-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="c675e-195">Vælg **Gem** for at gemme ændringer til det redigerbare format.</span><span class="sxs-lookup"><span data-stu-id="c675e-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Genereret output i Word-format](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="c675e-197">Kør tilpasset format for at oprette Word-output</span><span class="sxs-lookup"><span data-stu-id="c675e-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="c675e-198">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="c675e-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="c675e-199">Vælg den betalingskladde, du har oprettet, og vælg derefter **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="c675e-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="c675e-200">Markér på siden **Kreditorbetalinger** alle rækker, og vælg derefter **Betalingsstatus** \> **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="c675e-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="c675e-201">Vælg **Opret betalinger**.</span><span class="sxs-lookup"><span data-stu-id="c675e-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="c675e-202">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="c675e-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="c675e-203">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="c675e-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="c675e-204">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c675e-204">Select **OK**.</span></span>
8. <span data-ttu-id="c675e-205">I dialogboksen **Parametre for elektronisk rapport** skal du vælge **Ja** i feltet **Ignorer oversigt**.</span><span class="sxs-lookup"><span data-stu-id="c675e-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="c675e-206">Vælg **OK**, og analyser det genererede output.</span><span class="sxs-lookup"><span data-stu-id="c675e-206">Select **OK**, and analyze the generated output.</span></span>

    ![Genereret output i Word-format](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="c675e-208">Bemærk, at outputtet ikke indeholder samlesektionen, fordi det er blevet undertrykt.</span><span class="sxs-lookup"><span data-stu-id="c675e-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c675e-209">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c675e-209">Additional resources</span></span>

- [<span data-ttu-id="c675e-210">Designe en konfiguration til generering af rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="c675e-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="c675e-211">Designe ny ER-konfiguration til generering af rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="c675e-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="c675e-212">Genbruge Elektronisk rapporteringskonfigurationer med Excel-skabeloner til generering af rapporter i Word-format</span><span class="sxs-lookup"><span data-stu-id="c675e-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="c675e-213">Inspicere den konfigurerede ER-komponent for at undgå kørselsproblemer</span><span class="sxs-lookup"><span data-stu-id="c675e-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]