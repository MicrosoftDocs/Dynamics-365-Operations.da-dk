---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 9c50000c98bdde2c9da43b3110686aa5d01e8081
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259214"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="790b3-103">Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien</span><span class="sxs-lookup"><span data-stu-id="790b3-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="790b3-104">Tilføjelsesprogrammet til elektronisk fakturering for Italien understøtter i øjeblikket muligvis ikke alle de funktioner, der er tilgængelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="790b3-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="790b3-105">Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien.</span><span class="sxs-lookup"><span data-stu-id="790b3-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="790b3-106">Det fører dig gennem de konfigurationstrin, der er landeafhængige i Regulatory Configuration Services (RCS) og i Finance.</span><span class="sxs-lookup"><span data-stu-id="790b3-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="790b3-107">Det fører dig også gennem processen til indsendelse af elektroniske fakturaer, der er oprettet i formatet **FatturaPA**, som er specifikt for Italien, og forklarer, hvordan du kan gennemgå resultaterne af behandlingen.</span><span class="sxs-lookup"><span data-stu-id="790b3-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="790b3-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="790b3-108">Prerequisites</span></span>

<span data-ttu-id="790b3-109">Før du udfører trinene i dette emne, skal du udføre trinnene i [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="790b3-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="790b3-110">RCS-opsætning</span><span class="sxs-lookup"><span data-stu-id="790b3-110">RCS setup</span></span>

<span data-ttu-id="790b3-111">Under RCS-opsætningen skal du udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="790b3-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="790b3-112">Importér e-faktureringsfunktionen til eksport af elektroniske fakturaer til kunder i formatet **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="790b3-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="790b3-113">Gennemse de formatkonfigurationer, der skal bruges til at oprette, sende og modtage svar om elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="790b3-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="790b3-114">Konfigurer de hændelser, der understøtter scenarierne for indsendelse af elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="790b3-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="790b3-115">Publicer e-faktureringsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="790b3-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="790b3-116">"E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="790b3-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="790b3-117">I dette tilfælde er eksporten af elektroniske fakturaer til kunder den e-faktureringsfunktion, du skal konfigurere.</span><span class="sxs-lookup"><span data-stu-id="790b3-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="790b3-118">Importere e-faktureringsfunktionen</span><span class="sxs-lookup"><span data-stu-id="790b3-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="790b3-119">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="790b3-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="790b3-120">I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="790b3-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="790b3-121">På siden med **e-faktureringsfunktioner** skal du vælge **Importér** for at importere e-faktureringsfunktionen fra det globale lager.</span><span class="sxs-lookup"><span data-stu-id="790b3-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="790b3-122">Hvis du ikke kan se listen over tilgængelige funktioner, skal du vælge **Synkroniser**.</span><span class="sxs-lookup"><span data-stu-id="790b3-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="790b3-123">Vælg funktionen **Eksport af e-fakturaer (IT)**, og vælg derefter **Importér**.</span><span class="sxs-lookup"><span data-stu-id="790b3-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Importere funktionen Eksport af e-fakturaer (IT)](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="790b3-125">Når du importerer funktionen **Eksport af e-fakturaer (IT)** fra det globale lager, importeres alle de indstillinger, der er beskrevet i de næste afsnit, også.</span><span class="sxs-lookup"><span data-stu-id="790b3-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="790b3-126">Oprette en ny version af funktionen Eksport af e-fakturaer (IT)</span><span class="sxs-lookup"><span data-stu-id="790b3-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="790b3-127">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="790b3-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Tilføje en ny version af e-faktureringsfunktionen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="790b3-129">Derefter skal du konfigurere de elektroniske rapporteringsformater (ER), der er knyttet til e-faktureringsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="790b3-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="790b3-130">På fanen **Konfigurationer** skal du vælge **Tilføj** for at administrere konfigurationsversionerne.</span><span class="sxs-lookup"><span data-stu-id="790b3-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Administrere konfigurationsversionerne for e-faktureringsfunktion](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="790b3-132">I dette trin tilføjer og konfigurerer du ER-formaterne for de forskellige filer, der bruges til at eksportere italienske e-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="790b3-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="790b3-133">I forbindelse med italienske FatturaPA-e-fakturaer kan du enten bruge følgende standardkonfigurationer eller de faktiske tilpassede konfigurationer, du bruger til e-fakturering:</span><span class="sxs-lookup"><span data-stu-id="790b3-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="790b3-134">Salgsfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="790b3-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="790b3-135">Projektfaktura (IT)</span><span class="sxs-lookup"><span data-stu-id="790b3-135">Project invoice (IT)</span></span>

    <span data-ttu-id="790b3-136">Når du opretter en e-faktureringsfunktion, der er afledt af en anden e-faktureringsfunktion, nedarves alle ER-formater fra den oprindelige funktion.</span><span class="sxs-lookup"><span data-stu-id="790b3-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="790b3-137">Vælg en specifik filkonfiguration for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="790b3-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="790b3-138">Vælg **Rediger** eller **Vis** for at åbne siden **Formatdesigner**.</span><span class="sxs-lookup"><span data-stu-id="790b3-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Åbne siden Formatdesigner](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="790b3-140">Du kan bruge siden **Formatdesigner** til at redigere og få vist filkonfigurationer for ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="790b3-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Siden Formatdesigner](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="790b3-142">Administrere funktionsopsætninger for e-fakturering</span><span class="sxs-lookup"><span data-stu-id="790b3-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="790b3-143">På siden med **e-faktureringsfunktioner** på fanen **Konfigurationer** skal du vælge **Tilføj**, **Slet** eller **Rediger** for at administrere funktionsopsætningerne for e-fakturering.</span><span class="sxs-lookup"><span data-stu-id="790b3-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Administrere funktionsopsætninger for e-fakturering](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="790b3-145">I dette trin konfigurerer du de hændelser, der gælder for elektroniske fakturaer, herunder oprettelse af XML-outputfiler i formatet **FatturaPA** og digital underskrivning (hvis det er nødvendigt).</span><span class="sxs-lookup"><span data-stu-id="790b3-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="790b3-146">Konfigurere funktionsopsætningen for Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="790b3-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="790b3-147">Vælg **Salgsfaktura** i kolonnen **Funktionsopsætning** på fanen **Konfigurationer** på siden med **e-faktureringsfunktioner**.</span><span class="sxs-lookup"><span data-stu-id="790b3-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="790b3-148">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="790b3-148">Select **Edit**.</span></span>
3. <span data-ttu-id="790b3-149">På siden **Opsætning af funktionsversion** skal du vælge fanen **Handlinger** for at administrere listen over handlinger.</span><span class="sxs-lookup"><span data-stu-id="790b3-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="790b3-150">Handlinger definerer en liste over handlinger, der skal køres i rækkefølge for at opnå fuld udførelse af hændelsen.</span><span class="sxs-lookup"><span data-stu-id="790b3-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Fanen Handlinger](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="790b3-152">Handlings-id</span><span class="sxs-lookup"><span data-stu-id="790b3-152">Action ID</span></span> | <span data-ttu-id="790b3-153">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="790b3-153">Action name</span></span>        | <span data-ttu-id="790b3-154">Handlingsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="790b3-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="790b3-155">1</span><span class="sxs-lookup"><span data-stu-id="790b3-155">1</span></span>         | <span data-ttu-id="790b3-156">Transformere document</span><span class="sxs-lookup"><span data-stu-id="790b3-156">Transform document</span></span> | <span data-ttu-id="790b3-157">Opret XML-filen til e-fakturaen i formatet **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="790b3-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="790b3-158">2</span><span class="sxs-lookup"><span data-stu-id="790b3-158">2</span></span>         | <span data-ttu-id="790b3-159">Underskriv dokument</span><span class="sxs-lookup"><span data-stu-id="790b3-159">Sign document</span></span>      | <span data-ttu-id="790b3-160">Anvend en digital underskrift på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="790b3-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="790b3-161">Vælg fanen **Anvendelighedsregler** for at få vist og vedligeholde anvendelighedsreglerne.</span><span class="sxs-lookup"><span data-stu-id="790b3-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="790b3-162">Anvendelighedsregler definerer den kontekst, som handlingen vil blive kørt i.</span><span class="sxs-lookup"><span data-stu-id="790b3-162">Applicability rules define the context where the action will be run.</span></span>

    ![Fanen Anvendelighedsregler](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="790b3-164">Vælg fanen **Variabler** for at få vist og vedligeholde variablerne.</span><span class="sxs-lookup"><span data-stu-id="790b3-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Fanen Variabler](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="790b3-166">Definer de offentlige variabler, der skal bruges til at køre handlingerne.</span><span class="sxs-lookup"><span data-stu-id="790b3-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="790b3-167">Konfigurere funktionsopsætningen for Projektfaktura</span><span class="sxs-lookup"><span data-stu-id="790b3-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="790b3-168">De trin og indstillinger, der kræves for at konfigurere funktionsopsætningen for **Projektfaktura**, minder meget om trinnene og indstillingerne for funktionsopsætningen for **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="790b3-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="790b3-169">Når du arbejder med projektfakturaer, kan du se procedurerne for salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="790b3-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="790b3-170">Tildele e-faktureringsfunktionen til miljøet</span><span class="sxs-lookup"><span data-stu-id="790b3-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="790b3-171">På siden med **e-faktureringsfunktioner** på fanen **Miljøer** skal du vælge **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="790b3-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="790b3-172">Vælg miljøet i feltet **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="790b3-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="790b3-173">I feltet **Gyldig fra** skal du vælge den dato, hvor miljøet skal være gyldigt.</span><span class="sxs-lookup"><span data-stu-id="790b3-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="790b3-174">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="790b3-174">Select **Enable**.</span></span> 

![Aktivere e-faktureringsmiljøet](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="790b3-176">Publicere e-faktureringsfunktionen</span><span class="sxs-lookup"><span data-stu-id="790b3-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="790b3-177">Du kan publicere e-faktureringsfunktionen ved at ændre versions status til **Fuldført** eller **Publiceret**.</span><span class="sxs-lookup"><span data-stu-id="790b3-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="790b3-178">Skifte versionsstatus til Fuldført</span><span class="sxs-lookup"><span data-stu-id="790b3-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="790b3-179">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="790b3-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="790b3-180">Vælg **Skift status \> Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="790b3-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="790b3-181">Skifte versionsstatus til Publiceret</span><span class="sxs-lookup"><span data-stu-id="790b3-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="790b3-182">På siden med **e-faktureringsfunktioner** på fanen **Versioner** skal du vælge den e-faktureringsfunktion, der har statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="790b3-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="790b3-183">Vælg **Skift status \> Publicer**.</span><span class="sxs-lookup"><span data-stu-id="790b3-183">Select **Change status \> Publish**.</span></span>

![Ændre status for e-faktureringsfunktionen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="790b3-185">Konfigurere integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance</span><span class="sxs-lookup"><span data-stu-id="790b3-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="790b3-186">Under opsætningen af Finance skal du udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="790b3-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="790b3-187">Importere ER-datamodellen, ER-datamodeltilknytningen og kontekstkonfigurationerne for FatturaPA-e-fakturaer.</span><span class="sxs-lookup"><span data-stu-id="790b3-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="790b3-188">Konfigurer det certifikat, der kræves for at kunne underskrive italienske e-fakturaer digitalt.</span><span class="sxs-lookup"><span data-stu-id="790b3-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="790b3-189">Importere ER-datamodellen, -datamodeltilknytningen og -formaterne</span><span class="sxs-lookup"><span data-stu-id="790b3-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="790b3-190">I arbejdsområdet **Elektronisk rapportering** skal du kontrollere, at konfigurationsudbyderen **Business Document Service** er angivet til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="790b3-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="790b3-191">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="790b3-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="790b3-192">Vælg **Globalt lager \> Åbn**.</span><span class="sxs-lookup"><span data-stu-id="790b3-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="790b3-193">Importér **Fakturamodel**, **Fakturamodeltilknytning** og **Debitorfakturakontekstmodel**.</span><span class="sxs-lookup"><span data-stu-id="790b3-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="790b3-194">Aktivere funktionen til eksport af elektroniske fakturaer til kunder for Italien</span><span class="sxs-lookup"><span data-stu-id="790b3-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="790b3-195">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="790b3-196">På fanen **Funktioner** skal du markere afkrydsningsfeltet **Aktiveret** i rækken for funktionsreferencen **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="790b3-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Aktivere funktionen FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="790b3-198">Konfigurere elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="790b3-198">Configure electronic documents</span></span>

1. <span data-ttu-id="790b3-199">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="790b3-200">Vælg **Tilføj** på fanen **Elektronisk dokument**, og angiv de tabeller, der skal bruges til oprettelse af italienske e-fakturaer:</span><span class="sxs-lookup"><span data-stu-id="790b3-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="790b3-201">**Tabelnavn:** Debitorfakturajournal</span><span class="sxs-lookup"><span data-stu-id="790b3-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="790b3-202">**Tabelnavn:** Projektfaktura</span><span class="sxs-lookup"><span data-stu-id="790b3-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="790b3-203">Definer en relateret dokumentkontekst for hver tabel:</span><span class="sxs-lookup"><span data-stu-id="790b3-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="790b3-204">Vælg **Debitorfakturakontekst** for **Debitorfakturajournal**.</span><span class="sxs-lookup"><span data-stu-id="790b3-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="790b3-205">Vælg **Projektfakturakontekst** for **Projektfaktura**.</span><span class="sxs-lookup"><span data-stu-id="790b3-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Konfigurere svartyper](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="790b3-207">Behandling af elektronisk faktura</span><span class="sxs-lookup"><span data-stu-id="790b3-207">Electronic invoice processing</span></span>

<span data-ttu-id="790b3-208">Under behandlingen i Finance skal du udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="790b3-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="790b3-209">Oprette italienske e-fakturaer ved hjælp af tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="790b3-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="790b3-210">Få vist logfilerne for udførelse, og gennemse resultaterne af behandlingen</span><span class="sxs-lookup"><span data-stu-id="790b3-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="790b3-211">Oprette elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="790b3-211">Generate electronic invoices</span></span>

<span data-ttu-id="790b3-212">Når du har aktiveret funktionen **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering** og aktiverer funktionen **IT00036**, kan den gamle Finance-proces til oprettelse af italienske e-fakturaer ikke længere bruges.</span><span class="sxs-lookup"><span data-stu-id="790b3-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="790b3-213">Den erstattes af den nye proces **Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="790b3-214">Du kan sende dokumenterne manuelt baseret på dit behov for e-fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="790b3-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="790b3-215">Før du fortsætter, skal du kontrollere, at den opsætning, der kræves til italienske e-fakturaer, blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="790b3-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="790b3-216">Du kan finde flere oplysninger i [Elektroniske fakturaer til kunder](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="790b3-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="790b3-217">Bemærk, at nogle af de opsætningstrin, der er beskrevet i dette emne, muligvis ikke er tilgængelige pga. aktivering af tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="790b3-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="790b3-218">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="790b3-219">Ved den første indsendelse af et dokument skal du angive indstillingen **Send dokumenter igen** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="790b3-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="790b3-220">Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="790b3-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="790b3-221">I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel**, hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.</span><span class="sxs-lookup"><span data-stu-id="790b3-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialogboksen Send elektroniske dokumenter](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="790b3-223">Filterforespørgsel</span><span class="sxs-lookup"><span data-stu-id="790b3-223">Filter query</span></span>

1. <span data-ttu-id="790b3-224">I dialogboksen **Forespørgsel** kan du konfigurere filtreringsbetingelserne for både salgsfakturaer og projektfakturaer eller lade betingelserne stå tomme for at medtage alle de fakturaer, der ikke er sendt.</span><span class="sxs-lookup"><span data-stu-id="790b3-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Konfigurere filterkriterier for indsendelse](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="790b3-226">Vælg **OK** for at lukke dialogboksen **Forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="790b3-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="790b3-227">Vælg **OK** for at sende de valgte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="790b3-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="790b3-228">[BEMÆRK!] I løbet af første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="790b3-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="790b3-229">Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="790b3-230">Få vist indsendelseslogge</span><span class="sxs-lookup"><span data-stu-id="790b3-230">View submission logs</span></span>

<span data-ttu-id="790b3-231">Du kan få vist indsendelseslogge for alle sendte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="790b3-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="790b3-232">Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="790b3-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="790b3-233">I feltet **Dokumenttype** skal du vælge **Debitorfakturajournal** eller **Projektfaktura** for at filtrere de nødvendige elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="790b3-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Vælge en dokumenttype for at få vist indsendelseslogge](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="790b3-235">Den værdi, der vises i kolonnen **Indsendelsesstatus**, repræsenterer status for indsendelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="790b3-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="790b3-236">Den angiver, om processen kørte som konfigureret, og om der skal udføres yderligere handlinger.</span><span class="sxs-lookup"><span data-stu-id="790b3-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="790b3-237">Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden for at få vist logoplysningerne for udførelse af indsendelsen.</span><span class="sxs-lookup"><span data-stu-id="790b3-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Få vist logoplysninger om indsendelse](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="790b3-239">I oversigtspanelet **Behandling af handlinger** kan du se udførelsesloggen for de handlinger, der er konfigureret i den funktionsversion, som blev konfigureret i RCS.</span><span class="sxs-lookup"><span data-stu-id="790b3-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="790b3-240">Kolonnen **Status** viser, om handlingen blev kørt korrekt.</span><span class="sxs-lookup"><span data-stu-id="790b3-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="790b3-241">I oversigtspanelet **Handlingsfiler** kan du se de midlertidige filer, der blev oprettet under udførelse af handlingerne.</span><span class="sxs-lookup"><span data-stu-id="790b3-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="790b3-242">Du kan vælge **Vis** for at downloade XML-outputfilen i formatet **FatturaPA** og få vis indholdet.</span><span class="sxs-lookup"><span data-stu-id="790b3-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="790b3-243">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="790b3-243">Related topics</span></span>

- [<span data-ttu-id="790b3-244">Oversigt over tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="790b3-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="790b3-245">Kom i gang med tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="790b3-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="790b3-246">Konfigurere tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="790b3-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]