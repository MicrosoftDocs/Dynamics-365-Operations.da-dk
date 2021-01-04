---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6d15a79a359b3c708b2b33893d700377a57c3eb7
ms.sourcegitcommit: cfd84321fba38e02e270d361df369a536a48efa3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2020
ms.locfileid: "4512228"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="2ee66-103">Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico</span><span class="sxs-lookup"><span data-stu-id="2ee66-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="2ee66-104">Tilføjelsesprogrammet til elektronisk fakturering for Mexico understøtter i øjeblikket muligvis ikke alle de funktioner, der er tilgængelige i CFDI-dokumentet (Comprobante Fiscal Digital por Internet) og i den relaterede integrering i Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2ee66-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="2ee66-105">Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico.</span><span class="sxs-lookup"><span data-stu-id="2ee66-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="2ee66-106">Det fører dig gennem de konfigurationstrin, der er landeafhængige i Regulatory Configuration Services (RCS) og i Finance.</span><span class="sxs-lookup"><span data-stu-id="2ee66-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="2ee66-107">Det fører også dig gennem de trin, du skal følge i Finance for at sende CFDI-fakturaer via tjenesten, og det forklarer, hvordan du kan gennemse behandlingsresultaterne og statussen for CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ee66-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="2ee66-108">Prerequisites</span></span>

<span data-ttu-id="2ee66-109">Før du udfører trinene i dette emne, skal du udføre trinnene i [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="2ee66-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="2ee66-110">RCS-opsætning</span><span class="sxs-lookup"><span data-stu-id="2ee66-110">RCS setup</span></span>

<span data-ttu-id="2ee66-111">Under RCS-opsætningen skal du udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="2ee66-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="2ee66-112">Importér e-faktureringsfunktionen til behandling af CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="2ee66-113">Gennemse de formatkonfigurationer, der skal bruges til at oprette, sende og modtage svar om CFDI-fakturaer og til at sende og modtage svar om annullering.</span><span class="sxs-lookup"><span data-stu-id="2ee66-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="2ee66-114">Konfigurer de hændelser, der understøtter scenarierne for CFDI-fakturaindsendelse.</span><span class="sxs-lookup"><span data-stu-id="2ee66-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="2ee66-115">Publicer e-faktureringsfunktionen for CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="2ee66-116">"E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="2ee66-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="2ee66-117">I dette tilfælde er CFDI-fakturaer (MX) den e-faktureringsfunktion, du skal konfigurere.</span><span class="sxs-lookup"><span data-stu-id="2ee66-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="2ee66-118">Importere e-faktureringsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2ee66-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="2ee66-119">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="2ee66-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="2ee66-120">I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="2ee66-121">På siden med **e-faktureringsfunktioner** skal du vælge **Importér** for at importere funktionen **CFDI-fakturaer (MX)** fra det globale lager.</span><span class="sxs-lookup"><span data-stu-id="2ee66-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2ee66-122">Hvis du ikke kan se funktionen på listen, skal du vælge **Synkroniser** og derefter gentage trin 3.</span><span class="sxs-lookup"><span data-stu-id="2ee66-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![Importere funktionen CFDI-fakturaer (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="2ee66-124">Når du importerer funktionen **CFDI-fakturaer (MX)** fra det globale lager, importeres alle funktionsindstillinger, herunder konfigurationer og handlinger, også.</span><span class="sxs-lookup"><span data-stu-id="2ee66-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="2ee66-125">Oprette en ny version af funktionen MX (CFDI fakturaer)</span><span class="sxs-lookup"><span data-stu-id="2ee66-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="2ee66-126">Du kan oprette en ny version, hvis f.eks. URL-adresser skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="2ee66-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="2ee66-127">Du kan finde flere oplysninger i [CFDI for e-fakturering](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="2ee66-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="2ee66-128">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Tilføje en ny version af e-faktureringsfunktionen](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="2ee66-130">Opdatere konfigurationsversionen</span><span class="sxs-lookup"><span data-stu-id="2ee66-130">Update the configuration version</span></span>

1. <span data-ttu-id="2ee66-131">På siden med **e-faktureringsfunktioner** under **Konfigurationer** skal du vælge **Tilføj** eller **Slet** for at administrere konfigurationsversionerne (filkonfigurationer for ER-format).</span><span class="sxs-lookup"><span data-stu-id="2ee66-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Administrere konfigurationer for e-faktureringsfunktion](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="2ee66-133">Når du opretter en ny version, nedarves alle konfigurationer fra den senest publicerede version.</span><span class="sxs-lookup"><span data-stu-id="2ee66-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="2ee66-134">Der kræves følgende konfigurationer for at behandle CFDI-fakturaer:</span><span class="sxs-lookup"><span data-stu-id="2ee66-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="2ee66-135">CFDI-faktura (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="2ee66-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="2ee66-136">Import af CFDI-svarmeddelelse</span><span class="sxs-lookup"><span data-stu-id="2ee66-136">CFDI response message import</span></span>
    - <span data-ttu-id="2ee66-137">Import af CFDI-fejllog</span><span class="sxs-lookup"><span data-stu-id="2ee66-137">CFDI error log import</span></span>
    - <span data-ttu-id="2ee66-138">Anmodning om CFDI-annullering (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="2ee66-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="2ee66-139">CFDI-faktura (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="2ee66-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="2ee66-140">Vælg en konfigurationsversion på listen, og vælg derefter **Rediger** eller **Vis** for at åbne siden **Formatdesigner**, hvor du kan redigere eller få vist konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Åbne siden Formatdesigner](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="2ee66-142">Du kan bruge siden **Formatdesigner** til at redigere og få vist filkonfigurationer for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="2ee66-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="2ee66-143">Du kan finde flere oplysninger i [Oprette konfigurationer for elektroniske dokumenter](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="2ee66-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Siden Formatdesigner](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="2ee66-145">Administrere funktionsopsætninger for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="2ee66-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="2ee66-146">På siden med **e-faktureringsfunktioner** på fanen **Konfigurationer** skal du vælge **Tilføj**, **Slet** eller **Rediger** for at administrere funktionsopsætningerne for e-fakturering.</span><span class="sxs-lookup"><span data-stu-id="2ee66-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Administrere funktionsopsætninger for e-fakturering](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="2ee66-148">Hvis du vil sende CFDI-fakturaer til autorisation (oprette XML-filen, sende XML-filen og behandle svaret), kræves funktionsopsætningen for **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="2ee66-149">Hvis du vil sende en CFDI-fakturaannullering, kræves der funktionsopsætninger for **Annullering** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="2ee66-150">Konfigurere funktionsopsætningen for Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="2ee66-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="2ee66-151">Vælg **Salgsfaktura** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="2ee66-152">Vælg **Rediger** for at konfigurere handlinger, anvendelighedsregler og variabler.</span><span class="sxs-lookup"><span data-stu-id="2ee66-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Redigere funktionsopsætningen for e-fakturering](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="2ee66-154">På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="2ee66-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="2ee66-155">Handlinger definerer en liste over handlinger, der skal køres i rækkefølge for at opnå fuld udførelse af hændelsen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Fanen Handlinger](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="2ee66-157">Handlings-id</span><span class="sxs-lookup"><span data-stu-id="2ee66-157">Action ID</span></span> | <span data-ttu-id="2ee66-158">Handling</span><span class="sxs-lookup"><span data-stu-id="2ee66-158">Action</span></span>                   | <span data-ttu-id="2ee66-159">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="2ee66-159">Action name</span></span>                                  | <span data-ttu-id="2ee66-160">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="2ee66-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="2ee66-161">1</span><span class="sxs-lookup"><span data-stu-id="2ee66-161">1</span></span>         | <span data-ttu-id="2ee66-162">Transformere document</span><span class="sxs-lookup"><span data-stu-id="2ee66-162">Transform document</span></span>       | <span data-ttu-id="2ee66-163">Oprette CFDI-e-faktura uden digital underskrift</span><span class="sxs-lookup"><span data-stu-id="2ee66-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="2ee66-164">Opret CFDI-e-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="2ee66-165">2</span><span class="sxs-lookup"><span data-stu-id="2ee66-165">2</span></span>         | <span data-ttu-id="2ee66-166">Underskriv dokument</span><span class="sxs-lookup"><span data-stu-id="2ee66-166">Sign document</span></span>            | <span data-ttu-id="2ee66-167">Underskrive digital</span><span class="sxs-lookup"><span data-stu-id="2ee66-167">Digital sign</span></span>                                 | <span data-ttu-id="2ee66-168">Underskriv e-fakturaen digitalt til indsendelse.</span><span class="sxs-lookup"><span data-stu-id="2ee66-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="2ee66-169">3</span><span class="sxs-lookup"><span data-stu-id="2ee66-169">3</span></span>         | <span data-ttu-id="2ee66-170">Kalde mexicansk PAC-tjeneste</span><span class="sxs-lookup"><span data-stu-id="2ee66-170">Call Mexican PAC service</span></span> | <span data-ttu-id="2ee66-171">Sende CFDI-e-faktura</span><span class="sxs-lookup"><span data-stu-id="2ee66-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="2ee66-172">WCF-klienten (Windows Communication Foundation) sender CFDI-e-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="2ee66-173">4</span><span class="sxs-lookup"><span data-stu-id="2ee66-173">4</span></span>         | <span data-ttu-id="2ee66-174">Behandle svar</span><span class="sxs-lookup"><span data-stu-id="2ee66-174">Process response</span></span>         | <span data-ttu-id="2ee66-175">Analysere svar fra webtjeneste</span><span class="sxs-lookup"><span data-stu-id="2ee66-175">Analyze web service response</span></span>                 | <span data-ttu-id="2ee66-176">Analysér svaret fra webtjenesten, og returner fejlloggen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="2ee66-177">Konfigurere URL-adressen til mexicanske PAC-webtjenester</span><span class="sxs-lookup"><span data-stu-id="2ee66-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="2ee66-178">På siden **Opsætning af funktionsversion** på fanen **Handlinger** på oversigtspanelet **Handlinger** skal du vælge **Kald mexicansk PAC-tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="2ee66-179">På oversigtspanelet **Parametre** i feltet **URL-adresse** skal du angive URL-adressen til webtjenesten til CFDI-fakturaindsendelse.</span><span class="sxs-lookup"><span data-stu-id="2ee66-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="2ee66-180">Brug samme fremgangsmåde for at opdatere URL-adressen til handlingen **Kald mexicansk PAC-tjeneste** for funktionsopsætningerne for **Annuller** og **Anmodning om annullering**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="2ee66-181">Tildele kladdeversionen til et e-faktureringsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ee66-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="2ee66-182">På siden med **e-faktureringsfunktioner** på fanen **Miljøer** skal du vælge **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="2ee66-183">Vælg miljøet i feltet **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="2ee66-184">I feltet **Gyldig fra** skal du vælge den dato, hvor miljøet skal være gyldigt.</span><span class="sxs-lookup"><span data-stu-id="2ee66-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="2ee66-185">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-185">Select **Enable**.</span></span>

![Aktivere et e-faktureringsmiljø](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="2ee66-187">Skifte versionsstatus til Fuldført</span><span class="sxs-lookup"><span data-stu-id="2ee66-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="2ee66-188">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="2ee66-189">Vælg **Skift status \> Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="2ee66-190">Skifte versionsstatus til Publiceret</span><span class="sxs-lookup"><span data-stu-id="2ee66-190">Change the version status to Published</span></span>

- <span data-ttu-id="2ee66-191">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Skift status \> Publicer**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="2ee66-192">Publicere e-faktureringsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2ee66-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="2ee66-193">På siden med **e-faktureringsfunktioner** skal du vælge fanen **Versioner** for at administrere statussen for funktionen **CFDI-fakturaer (MX)**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="2ee66-194">Vælg **Skift status** for at ændre funktionens status.</span><span class="sxs-lookup"><span data-stu-id="2ee66-194">Select **Change status** to change the status of the feature.</span></span>

![Ændre status for e-faktureringsfunktionen](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="2ee66-196">Konfigurere integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance</span><span class="sxs-lookup"><span data-stu-id="2ee66-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="2ee66-197">Hvis du vil konfigurere tilføjelsesprogrammet til elektronisk fakturering i Finance, skal du fuldføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="2ee66-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="2ee66-198">Importér ER-datamodellen, ER-datamodeltilknytningen og de formater, der kræves til CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="2ee66-199">Konfigurer svartyper for opdatering af CFDI-fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="2ee66-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="2ee66-200">Disse svartyper bruges til svaret fra den autoriserede certificeringsudbyderserver (PAC).</span><span class="sxs-lookup"><span data-stu-id="2ee66-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="2ee66-201">Importere ER-datamodellen, ER-datamodeltilknytningen og kontekstkonfigurationerne for CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="2ee66-202">Log på Finance.</span><span class="sxs-lookup"><span data-stu-id="2ee66-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="2ee66-203">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="2ee66-204">Kontrollér, at denne konfigurationsudbyder er angivet til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="2ee66-205">Du kan finde flere oplysninger om, hvordan du angiver en udbyder til **Aktiv**, i [Oprette konfigurationsudbydere og markere dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="2ee66-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="2ee66-206">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="2ee66-207">Vælg **Globalt lager \> Åbn**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="2ee66-208">Importér **Fakturamodel**, **Fakturamodeltilknytning**, **CFDI-fakturaformat (MX)**, **CFDI-fakturaformat for anmodning om annullering (MX)** og **CFDI fakturaformat for annullering (MX)**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="2ee66-209">Aktivere funktionen til behandling af CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="2ee66-210">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="2ee66-211">På fanen **Funktioner** skal du markere afkrydsningsfeltet **Aktivér** i rækkerne for funktionsreferencerne **MX-00010** og **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Aktivere funktionerne til behandling af CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="2ee66-213">Importere ER-konfigurationer og konfigurere svartyper for opdatering af CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="2ee66-214">Importér ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="2ee66-214">Import ER configurations</span></span>

1. <span data-ttu-id="2ee66-215">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="2ee66-216">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="2ee66-217">Vælg **Globalt lager \> Åbn**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="2ee66-218">Importér **Svarmeddelelsesmodel**, **Import af CFDI-fejllog (MX)** og **Import af CFDI-svarmeddelelse (MX)**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="2ee66-219">Konfigurere svartyper</span><span class="sxs-lookup"><span data-stu-id="2ee66-219">Set up the response types</span></span>

1. <span data-ttu-id="2ee66-220">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="2ee66-221">Vælg **Tilføj** på fanen **Elektronisk dokument**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="2ee66-222">Angiv debitorfakturajournalen, og vælg derefter projektfakturaen i feltet **Tabelnavn**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="2ee66-223">Definer en relateret dokumentkontekst for hver tabel:</span><span class="sxs-lookup"><span data-stu-id="2ee66-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="2ee66-224">Angiv en **Debitorfakturakontekst** for **Debitorfakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="2ee66-225">Angiv en **Projektfakturakontekst** for **Projektfaktura**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="2ee66-226">Vælg **Svartyper** for at konfigurere de svartyper, der kan returneres fra tilføjelsesprogrammet til elektronisk fakturering, og som er medtaget i en debitorfakturajournal eller projektfaktura.</span><span class="sxs-lookup"><span data-stu-id="2ee66-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="2ee66-227">Vælg **Ny**, og vælg derefter **Svar** i feltet **Svartype**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="2ee66-228">Vælg **Afventer** i feltet **Indsendelsesstatus**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="2ee66-229">I feltet **Modeltilknytning** skal du vælge **Format til import af svarmeddelelse – modeltilknytning fra svarmeddelelse**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="2ee66-230">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-230">Select **Save**.</span></span>
9. <span data-ttu-id="2ee66-231">Vælg **Ny**, og vælg derefter **ResponseData** i feltet **Svartype**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="2ee66-232">Vælg **Afventer** i feltet **Indsendelsesstatus**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="2ee66-233">I **Modeltilknytning** skal du vælge **Format til dataimport af CFDI-svar (detaljer) – dataimport af svar**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="2ee66-234">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="2ee66-235">Behandle elektroniske fakturaer i Finance</span><span class="sxs-lookup"><span data-stu-id="2ee66-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="2ee66-236">Du kan udføre følgende opgaver under behandlingen af CFDI-fakturaer i Finance ved hjælp af tilføjelsesprogrammet til elektronisk fakturering:</span><span class="sxs-lookup"><span data-stu-id="2ee66-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="2ee66-237">Send CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="2ee66-238">Få vist loggene for udførelse af indsendelse.</span><span class="sxs-lookup"><span data-stu-id="2ee66-238">View the submission execution logs.</span></span>
- <span data-ttu-id="2ee66-239">Send annulleringen af en CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="2ee66-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="2ee66-240">Sende CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-240">Submit CFDI invoices</span></span>

<span data-ttu-id="2ee66-241">Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering**, kan processen **Eksportér/importér elektronisk faktura** (**Debitor \> Fakturaer \> E-fakturaer**) ikke længere bruges til at sende CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="2ee66-242">Den erstattes af den nye proces **Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="2ee66-243">Før du bruger den nye proces **Send elektroniske dokumenter**, skal du kontrollere, at den opsætning, der kræves til mexicanske e-fakturaer, blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="2ee66-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="2ee66-244">Du kan finde flere oplysninger i [CFDI-layoutversion 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="2ee66-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="2ee66-245">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="2ee66-246">Ved den første indsendelse af et dokument skal du altid angive indstillingen **Send dokumenter igen** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="2ee66-247">Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="2ee66-248">I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel**, hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="2ee66-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Sende et CFDI-dokument](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="2ee66-250">I løbet af første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="2ee66-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="2ee66-251">Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="2ee66-252">Få vist indsendelseslogge</span><span class="sxs-lookup"><span data-stu-id="2ee66-252">View submission logs</span></span>

<span data-ttu-id="2ee66-253">Du kan få vist indsendelseslogge for alle sendte dokumenter eller kun for ét sendt dokument.</span><span class="sxs-lookup"><span data-stu-id="2ee66-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="2ee66-254">Få vist alle indsendelseslogge</span><span class="sxs-lookup"><span data-stu-id="2ee66-254">View all submission logs</span></span>

<span data-ttu-id="2ee66-255">Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering**, bliver en ny side tilgængelig, hvor du kan følge op på processen for indsendelse af dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2ee66-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="2ee66-256">Du kan bruge denne side til at få vist indsendelseslogge for alle sendte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2ee66-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="2ee66-257">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="2ee66-258">I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** for at filtrere de nødvendige elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="2ee66-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Vælge en dokumenttype for at få vist indsendelseslogge](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="2ee66-260">Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Få vist logoplysninger om indsendelse](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="2ee66-262">Oplysningerne i indsendelseslogge er opdelt mellem tre oversigtspaneler:</span><span class="sxs-lookup"><span data-stu-id="2ee66-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="2ee66-263">**Behandling af handlinger** – I dette oversigtspanel vises udførelsesloggen for de handlinger, der er konfigureret i den funktionsversion, som blev konfigureret i RCS.</span><span class="sxs-lookup"><span data-stu-id="2ee66-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="2ee66-264">Kolonnen **Status** viser, om handlingen blev kørt korrekt.</span><span class="sxs-lookup"><span data-stu-id="2ee66-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="2ee66-265">**Handlingsfiler** – I dette oversigtspanel vises de midlertidige filer, der blev oprettet under udførelse af handlingerne.</span><span class="sxs-lookup"><span data-stu-id="2ee66-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="2ee66-266">Du kan vælge **Vis** for at downloade og få vist filen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="2ee66-267">**Handlingslog for behandling** – I dette oversigtspanel vises resultaterne af kommunikationen mellem tilføjelsesprogrammet til elektronisk fakturering og destinationswebtjenesten.</span><span class="sxs-lookup"><span data-stu-id="2ee66-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="2ee66-268">Den viser også, hvad der blev returneret af behandlingen fra webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="2ee66-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="2ee66-269">Kolonnen **Fejlkode** viser den returkode, der blev returneret af autorisationswebtjenesten.</span><span class="sxs-lookup"><span data-stu-id="2ee66-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="2ee66-270">Når den afsendte CFDI-faktura er godkendt, opdateres statussen til **Godkendt**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="2ee66-271">Få vist indsendelseslogge fra CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="2ee66-272">Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering**, kan du også få vist indsendelsesloggene fra CFDI-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2ee66-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="2ee66-273">Gå til **Debitor \> Forespørgsler og rapporter \> CFDI (elektroniske fakturaer)**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="2ee66-274">Vælg en CFDI-faktura, der blev sendt, efter at funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2ee66-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="2ee66-275">Vælg **Log for elektronisk dokument** på fanen **Historik** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2ee66-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Få vist indsendelseslogge fra CFDI-fakturaer](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="2ee66-277">Knappen **Historik** er tilgængelig for CFDI-fakturaer, der blev sendt, før funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2ee66-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="2ee66-278">Knappen **Historik** er ikke tilgængelig for CFDI-fakturaer, der blev sendt, efter at funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2ee66-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="2ee66-279">Sende annullering af CFDI-fakturaer</span><span class="sxs-lookup"><span data-stu-id="2ee66-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="2ee66-280">Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering**, kan den gamle proces til annullering af CFDI-fakturaer ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="2ee66-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="2ee66-281">Den erstattes af en ny annulleringsproces, der er indlejret på siden **Indsendelseslog for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="2ee66-282">Gå til **Debitor \> Forespørgsler og rapporter \> CFDI (elektroniske fakturaer)**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="2ee66-283">Hvis CFDI-fakturaen har statussen **Godkendt**, skal du vælge **Funktioner \> Annuller CFDI**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="2ee66-284">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="2ee66-285">Vælg CFDI-fakturaen, og vælg derefter **Funktioner \> Send relaterede indsendelser**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="2ee66-286">Angiv en beskrivelse af den relaterede indsendelse, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="2ee66-287">Få vist alle indsendelseslogge for annullering</span><span class="sxs-lookup"><span data-stu-id="2ee66-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="2ee66-288">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="2ee66-289">I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** for kun at filtrere efter debitorfakturajournaldokumenter.</span><span class="sxs-lookup"><span data-stu-id="2ee66-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="2ee66-290">Vælg CFDI-fakturaen, og vælg derefter **Forespørgsler \> Relateret indsendelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2ee66-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="2ee66-291">På siden **Relaterede indsendelser** vises alle relaterede indsendelser og deres indsendelsesstatus for en bestemt CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="2ee66-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="2ee66-292">I følgende illustration repræsenterer den første linje den indsendelse, der anmodede om godkendelse af CFDI-fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="2ee66-293">Den anden linje repræsenterer den indsendelse, der annullerede den pågældende CFDI-faktura.</span><span class="sxs-lookup"><span data-stu-id="2ee66-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Få vist alle indsendelseslogge for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="2ee66-295">Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.</span><span class="sxs-lookup"><span data-stu-id="2ee66-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Få vist alle oplysninger om indsendelseslogge for annullering](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="2ee66-297">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="2ee66-297">Privacy notice</span></span>
<span data-ttu-id="2ee66-298">Aktivering af funktionerne MX-00010 og MX-00016 (CFDI-faktura og CFDI-annullering) kan kræve, at der sendes begrænsede data, som omfatter organisationens momsregistrerings-id.</span><span class="sxs-lookup"><span data-stu-id="2ee66-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="2ee66-299">Dette vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer til denne skattemyndighed i det foruddefinerede format, der kræves til integration med myndighedernes webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="2ee66-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="2ee66-300">En administrator kan aktivere og deaktivere funktionerne MX-00010 og MX-00016 (CFDI-faktura og CFDI-annullering) ved at gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="2ee66-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="2ee66-301">Vælg fanen **Funktioner**, vælg de rækker, der indeholder funktionerne MX-00010 og MX-00016, og foretag derefter det relevante valg.</span><span class="sxs-lookup"><span data-stu-id="2ee66-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="2ee66-302">De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="2ee66-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="2ee66-303">Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den lande- eller områdespecifikke funktion.</span><span class="sxs-lookup"><span data-stu-id="2ee66-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ee66-304">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2ee66-304">Additional resources</span></span>

- [<span data-ttu-id="2ee66-305">Oversigt over tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="2ee66-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="2ee66-306">Kom i gang med tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="2ee66-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="2ee66-307">Konfigurere tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="2ee66-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
