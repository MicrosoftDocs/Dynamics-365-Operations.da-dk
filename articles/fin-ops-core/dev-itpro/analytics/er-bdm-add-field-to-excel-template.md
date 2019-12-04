---
title: Tilføj nye felter til en skabelon for forretningsdokument i Microsoft Excel
description: Dette emne indeholder oplysninger om, hvordan du kan tilføje nye felter til en skabelon til forretningsdokument i Microsoft Excel ved hjælp af funktionen Styring af forretningsdokument.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d6e0f2c914b8d348ef6eac42557fb46c53df04a9
ms.sourcegitcommit: d16d370dab734e09312cb06711beca9cca52d4c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2809514"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="1443d-103">Tilføj nye felter til en skabelon for forretningsdokument i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="1443d-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1443d-104">Du kan tilføje nye felter til en skabelon, der bruges til at generere forretningsdokumenter i Microsoft Excel-format.</span><span class="sxs-lookup"><span data-stu-id="1443d-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="1443d-105">Disse felter kan tilføjes som pladsholdere, der bruges til at udfylde genererede dokumenter med de nødvendige oplysninger fra programmet.</span><span class="sxs-lookup"><span data-stu-id="1443d-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="1443d-106">For hvert felt, du tilføjer, kan du også angive en binding til datakilderne for at angive, hvilke programdata der skal indsættes i feltet, når skabelonen bruges til at generere forretningsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1443d-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="1443d-107">Hvis du vil vide mere om denne funktion, skal du fuldføre eksemplet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="1443d-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="1443d-108">I dette eksempel vises, hvordan du kan opdatere en skabelon for at udfylde de felter, der genereres i fritekstfakturaformler.</span><span class="sxs-lookup"><span data-stu-id="1443d-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="1443d-109">Konfigurer Styring af forretningsdokumenter til at redigere skabeloner</span><span class="sxs-lookup"><span data-stu-id="1443d-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="1443d-110">Da Styring af forretningsdokument (BDM) er bygget oven på [Oversigten over Elektronisk rapporteringsstrukturen (ER)](general-electronic-reporting.md), skal du konfigurere de krævede parametre ER og BDM, før du kan begynde at arbejde med BDM.</span><span class="sxs-lookup"><span data-stu-id="1443d-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="1443d-111">Log ind på forekomsten af Microsoft Dynamics 365 Finance som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="1443d-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="1443d-112">Fuldfør følgende trin i eksemplet i emnet [Oversigt over styring af forretningsdokumenter](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="1443d-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="1443d-113">Konfigurer ER-parametre.</span><span class="sxs-lookup"><span data-stu-id="1443d-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="1443d-114">Aktivér BDM.</span><span class="sxs-lookup"><span data-stu-id="1443d-114">Turn on BDM.</span></span>

<span data-ttu-id="1443d-115">Du kan nu begynde at bruge BDM til at redigere skabeloner til forretningsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1443d-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="1443d-116">Importer løsninger, der indeholder en skabelon</span><span class="sxs-lookup"><span data-stu-id="1443d-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="1443d-117">I eksemplet i denne procedure bruges den officielt publicerede ER-løsning.</span><span class="sxs-lookup"><span data-stu-id="1443d-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="1443d-118">Du skal importere ER-konfigurationerne for denne løsning i den aktuelle forekomst af Finance.</span><span class="sxs-lookup"><span data-stu-id="1443d-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="1443d-119">ER-formatkonfigurationen af **Fritekstfakturaen (Excel)** indeholder skabelonen for forretningsdokumenter i Excel, der kan redigeres ved hjælp af BDM.</span><span class="sxs-lookup"><span data-stu-id="1443d-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="1443d-120">Importer den seneste version af denne ER-formatkonfiguration fra Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="1443d-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="1443d-121">Varianter af den tilsvarende ER-datamodel og konfigurationer af ER-modeltilknytninger importeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="1443d-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="1443d-122">Du kan finde flere oplysninger om, hvordan du importerer ER-konfigurationer under [Administrere livscyklus for ER-konfiguration](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="1443d-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Siden for Delt LCS-aktivbibliotek](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="1443d-124">Rediger skabelonen for ER-løsningen</span><span class="sxs-lookup"><span data-stu-id="1443d-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="1443d-125">Log på som bruger med adgang til arbejdsområdet **Styring af forretningsdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="1443d-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="1443d-126">Åbn arbejdsområdet til **Styring af forretningsdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="1443d-126">Open the **Business document management** workspace.</span></span>

    ![Arbejdsområdet til Styring af forretningsdokumenter](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="1443d-128">Vælg skabelonen til **Fritekstfakturaer (Excel)** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1443d-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="1443d-129">I højre rude skal du vælge **Ny skabelon** for at oprette en ny skabelon, der er baseret på den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="1443d-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="1443d-130">I feltet **Titel** skal du angive **Fritekstfaktura (Excel) Contoso** som titlen på den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="1443d-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="1443d-131">Vælg **OK** for at bekræfte starten af redigeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1443d-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="1443d-132">Siden BDM-skabeloneditor vises.</span><span class="sxs-lookup"><span data-stu-id="1443d-132">The BDM template editor page appears.</span></span> <span data-ttu-id="1443d-133">Du kan bruge Microsoft Office 365 til at redigere den valgte skabelon online i det integrerede kontrolelement.</span><span class="sxs-lookup"><span data-stu-id="1443d-133">You can use Microsoft Office 365 to edit the selected template online in the embedded control.</span></span>

![Siden med BDM-skabeloneditor](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="1443d-135">Tilføj etiketten for et nyt felt til skabelonen</span><span class="sxs-lookup"><span data-stu-id="1443d-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="1443d-136">På siden med BDM-skabeloneditor skal du på Excel-båndet på fanen **Vis** vælge afkrydningsfelterne **Overskrifter og gitterlinjer** for den redigerbare Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="1443d-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Afkrydsningsfelterne Overskrifter og Gitterlinjer er markerede](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="1443d-138">Marker cellerne **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="1443d-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="1443d-139">På Excel-båndet under fanen **Startside** skal du vælge **Flet & Centrer** for at flette de markerede celler ind i en sammenflettet **E8:F8**-celle.</span><span class="sxs-lookup"><span data-stu-id="1443d-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="1443d-140">I den sammenflettede celle **E8:F8** skal du indtaste **URL-adressen**.</span><span class="sxs-lookup"><span data-stu-id="1443d-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="1443d-141">Vælg flettet celle **E7:F7**, vælg **Formatpensel**, og vælg derefter den sammenflettede celle **E8:F8** for at formatere den på samme måde som den flettede celle **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="1443d-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Etiketten "Nyt felt" er tilføjet til skabelonen](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="1443d-143">Formater skabelonen for at reservere plads til et nyt felt</span><span class="sxs-lookup"><span data-stu-id="1443d-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="1443d-144">På siden med BDM-skabeloneditor skal du vælge den sammenflettede celle **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="1443d-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="1443d-145">På Excel-båndet under fanen **Startside** skal du vælge **Flet & Centrer** for at flette de markerede celler ind i en sammenflettet **G8:H8**-celle.</span><span class="sxs-lookup"><span data-stu-id="1443d-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="1443d-146">Vælg flettet celle **G7:H7**, vælg **Formatpensel**, og vælg derefter den sammenflettede celle **G8:H8** for at formatere den på samme måde som den flettede celle **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="1443d-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Plads, der er reserveret til det nye felt](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="1443d-148">I afkrydsningsfeltet **Navn** skal du vælge **FirmaInfo**.</span><span class="sxs-lookup"><span data-stu-id="1443d-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="1443d-149">Intervallet **FirmaInfo** i den aktuelle Excel-skabelon indeholder alle de felter, der bruges til at udfylde overskriften i en genereret rapport med detaljer om det aktuelle firma som sælgende part.</span><span class="sxs-lookup"><span data-stu-id="1443d-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Interval for FirmaInfo er valgt](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="1443d-151">Tilføj et nyt felt til skabelonen</span><span class="sxs-lookup"><span data-stu-id="1443d-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="1443d-152">På siden **BDM-skabeloneditor** skal du i handlingsruden vælge **Vis format**.</span><span class="sxs-lookup"><span data-stu-id="1443d-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="1443d-153">I ruden **Skabelonstruktur** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="1443d-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1443d-154">Du skal justere den sektion i skabelonen, du vil bruge som et nyt felt.</span><span class="sxs-lookup"><span data-stu-id="1443d-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="1443d-155">Du har allerede gennemført denne justering ved at formatere den flettede celle **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="1443d-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Sådan tilføjer du et nyt felt til skabelonen](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="1443d-157">Vælg **Excel\Celle** for at tilføje et nyt felt som en celle i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1443d-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="1443d-158">Du kan vælge **Excel\Interval**, hvis du vil føje et nyt interval til skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1443d-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="1443d-159">Det angivne interval kan indeholde flere celler.</span><span class="sxs-lookup"><span data-stu-id="1443d-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="1443d-160">Du kan tilføje disse celler senere.</span><span class="sxs-lookup"><span data-stu-id="1443d-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="1443d-161">Bemærk, at skabelonkomponenten **FirmaInfo** automatisk vælges i ruden **Skabelonstruktur**, fordi det er det mest passende overordnede komponent i den aktuelle skabelonstruktur for det felt, du tilføjer.</span><span class="sxs-lookup"><span data-stu-id="1443d-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="1443d-162">I feltet **Excel-interval** skal du indtaste **FirmaURL_Værdi**.</span><span class="sxs-lookup"><span data-stu-id="1443d-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="1443d-163">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1443d-163">Select **OK**.</span></span>

    ![Feltet FirmaURL_Værdi tilføjes til skabelonstrukturen](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="1443d-165">I ruden **Skabelonstruktur** skal du vælge ellipseknappen (...) og dernæst vælge **Vis bindinger**.</span><span class="sxs-lookup"><span data-stu-id="1443d-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Vis valgte bindinger](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="1443d-167">I ruden **Skabelonstruktur** vises nu de datakilder, der er tilgængelige i det underliggende ER-format.</span><span class="sxs-lookup"><span data-stu-id="1443d-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="1443d-168">Vælg **FirmaInfo_værdi** som det felt, du har planer om at binde til en datakilde for det underliggende ER-format.</span><span class="sxs-lookup"><span data-stu-id="1443d-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="1443d-169">I sektionen **Datakilder** i ruden **Skabelonstruktur** skal du udvide **Model \> FakturaGrundlag \> FirmaInfo**.</span><span class="sxs-lookup"><span data-stu-id="1443d-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="1443d-170">Under **FirmaInfo** skal du vælge elementet **WebsiteURL**.</span><span class="sxs-lookup"><span data-stu-id="1443d-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Elementet WebsiteURL er valgt](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="1443d-172">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="1443d-172">Select **Bind**.</span></span>
11. <span data-ttu-id="1443d-173">I ruden **Skabelonstruktur** skal du vælge **Gem** og dernæst lukke siden med BDM-skabeloneditor.</span><span class="sxs-lookup"><span data-stu-id="1443d-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="1443d-174">I arbejdsområdet **Styring af forretningsdokumenter** vises den opdaterede skabelon på fanen **Skabelon** i højre rude.</span><span class="sxs-lookup"><span data-stu-id="1443d-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="1443d-175">Bemærk, at feltet **Status** for den redigerede skabelon er ændret til **Kladde** i gitteret, og at feltet **Revision** ikke længere er tomt.</span><span class="sxs-lookup"><span data-stu-id="1443d-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="1443d-176">Disse ændringer betyder, at processen for redigering af denne skabelon er startet.</span><span class="sxs-lookup"><span data-stu-id="1443d-176">These changes indicate that the process of editing this template has been started.</span></span>

![Redigeret skabelon i arbejdsområdet Styring af forretningsdokument](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="1443d-178">Gennemgå firmaindstillinger</span><span class="sxs-lookup"><span data-stu-id="1443d-178">Review company settings</span></span>

1.  <span data-ttu-id="1443d-179">Gå til **Organisationsadministration \> Organisationer \> Juridiske enheder**.</span><span class="sxs-lookup"><span data-stu-id="1443d-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="1443d-180">I oversigtspanelet **Kontaktinformation** skal du verificere, at firmaets URL-adresse er angivet.</span><span class="sxs-lookup"><span data-stu-id="1443d-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Firmaets URL-adresse angives på siden Juridiske enheder](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="1443d-182">Generer forretningsdokumenter for at teste den opdaterede skabelon</span><span class="sxs-lookup"><span data-stu-id="1443d-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="1443d-183">I programmets skal du ændre firmaet til **USMF** og gå til **Debitor \> Fakturaer \> Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="1443d-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="1443d-184">Vælg fakturaen **FTI-00000002**, og vælg derefter **Udskriftsstyring**.</span><span class="sxs-lookup"><span data-stu-id="1443d-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="1443d-185">I venstre rude skal du udvide **Modul - debitor \> Dokumenter \> Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="1443d-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="1443d-186">Under **Fritekstfaktura** skal du vælge niveauet for det **Originale dokument** for at angive, hvilke fakturaer der skal behandles.</span><span class="sxs-lookup"><span data-stu-id="1443d-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="1443d-187">I højre rude i feltet **Rapportformat** skal du vælge skabelonen **Fritekstfaktura (Excel) Contoso** for det angivne dokumentniveau.</span><span class="sxs-lookup"><span data-stu-id="1443d-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Skabelonen Fritekstfaktura (Excel) Contoso er valgt](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="1443d-189">Tryk på **Esc** for at lukke den aktuelle side.</span><span class="sxs-lookup"><span data-stu-id="1443d-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="1443d-190">Vælg **Udskriv \> Valgte**.</span><span class="sxs-lookup"><span data-stu-id="1443d-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="1443d-191">Hent det genererede dokument, og åbn det i Excel.</span><span class="sxs-lookup"><span data-stu-id="1443d-191">Download the generated document, and open it in Excel.</span></span>

    ![Fritekstfaktura i Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="1443d-193">Den ændrede skabelon bruges til at generere rapporten med fritekstfaktura for den valgte vare.</span><span class="sxs-lookup"><span data-stu-id="1443d-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="1443d-194">Hvis du vil analysere, hvordan denne rapport påvirkes af de ændringer, du har foretaget i skabelonen, skal du køre denne rapport i én programsession umiddelbart efter, at du har ændret skabelonen i en anden programsession.</span><span class="sxs-lookup"><span data-stu-id="1443d-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="1443d-195">Relaterede links</span><span class="sxs-lookup"><span data-stu-id="1443d-195">Related links</span></span>

[<span data-ttu-id="1443d-196">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="1443d-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="1443d-197">Oversigt over styring af forretningsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1443d-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="1443d-198">Designe en konfiguration til generering af rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="1443d-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
