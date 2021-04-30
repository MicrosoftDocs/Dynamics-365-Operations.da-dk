---
title: Justere et ER-format for at oprette et brugerdefineret elektronisk dokument
description: Dette emne forklarer, hvordan du justerer et elektronisk rapporteringsformat (ER) fra Microsoft og opretter et brugerdefineret elektronisk dokument.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60b318ab03bc1bb47517a206e8b2afd9c13cf273
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891713"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="7cb0b-103">Justere et ER-format for at oprette et brugerdefineret elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="7cb0b-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7cb0b-104">Procedurerne i dette emne forklarer, hvordan en bruger med rollen Systemadministrator eller Funktionel konsulent i elektronisk rapportering kan udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="7cb0b-105">Konfigurer parametre for den [Elektroniske rapporteringsstruktur (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="7cb0b-106">Importer ER-konfigurationer, der leveres af Microsoft, og som bruges til at generere en betalingsfil, mens en [kreditorbetaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) behandles.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="7cb0b-107">Opret en brugerdefineret version af en standardkonfiguration af ER-format, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="7cb0b-108">Rediger den brugerdefinerede konfigurationen af ER-format, så det genererer betalingsfiler, der opfylder kravene i en bestemt bank.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="7cb0b-109">Anvend de ændringer, der er foretaget i konfiguration af standard-ER-formatet, i konfigurationen af det brugerdefinerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="7cb0b-110">Alle de følgende procedurer kan udføres i **GBSI**-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="7cb0b-111">Der kræves ingen kodning.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-111">No coding is required.</span></span>

- [<span data-ttu-id="7cb0b-112">Konfigurere ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="7cb0b-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="7cb0b-113">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="7cb0b-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="7cb0b-114">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="7cb0b-115">Gennemse listen over udbydere af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="7cb0b-116">Tilføje en ny udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="7cb0b-117">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="7cb0b-118">Importere standardkonfigurationer af ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="7cb0b-119">Importere standardkonfigurationer af ER</span><span class="sxs-lookup"><span data-stu-id="7cb0b-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="7cb0b-120">Gennemse de importerede ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="7cb0b-121">Klargøre en kreditorbetaling til behandling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="7cb0b-122">Tilføj bankoplysninger for kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="7cb0b-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="7cb0b-123">Angive en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="7cb0b-124">Behandle kreditorbetaling ved hjælp af standard-ER-formatet</span><span class="sxs-lookup"><span data-stu-id="7cb0b-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="7cb0b-125">Konfigurere den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="7cb0b-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="7cb0b-126">Behandle en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="7cb0b-127">Tilpasse standard-ER-formatet</span><span class="sxs-lookup"><span data-stu-id="7cb0b-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="7cb0b-128">Oprette et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="7cb0b-129">Redigere et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="7cb0b-130">Markere et brugerdefineret format som kørbart</span><span class="sxs-lookup"><span data-stu-id="7cb0b-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="7cb0b-131">Behandle kreditorbetaling ved hjælp af det brugerdefinerede ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="7cb0b-132">Konfigurere den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="7cb0b-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="7cb0b-133">Behandle en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="7cb0b-134">Importere nye version af standardkonfigurationer af ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="7cb0b-135">Importere nye version af standardkonfigurationer af ER</span><span class="sxs-lookup"><span data-stu-id="7cb0b-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="7cb0b-136">Gennemse de importerede ER-formatkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="7cb0b-137">Anvende ændringerne i den nye version af et importeret format i et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="7cb0b-138">Fuldføre den aktuelle kladdeversion af et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="7cb0b-139">Basere et brugerdefineret format på en ny basisversion</span><span class="sxs-lookup"><span data-stu-id="7cb0b-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="7cb0b-140">Behandle kreditorbetaling ved hjælp af et ER-format med ny base</span><span class="sxs-lookup"><span data-stu-id="7cb0b-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="7cb0b-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="7cb0b-142">Konfigurere ER-strukturen</span><span class="sxs-lookup"><span data-stu-id="7cb0b-142">Configure the ER framework</span></span>

<span data-ttu-id="7cb0b-143">Som bruger i rollen Funktionel konsulent i elektronisk rapportering skal du konfigurere det minimale sæt med ER-parametre, før du kan begynde at bruge ER-strukturen til at designe en brugerdefineret version af standard-ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="7cb0b-144">Konfigurere ER-parametre</span><span class="sxs-lookup"><span data-stu-id="7cb0b-144">Configure ER parameters</span></span>

1. <span data-ttu-id="7cb0b-145">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-146">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="7cb0b-147">På siden **Parametre til elektronisk rapportering** under fanen **Generelt** skal du vælge **Ja** i indstillingen **Aktiver designtilstand** .</span><span class="sxs-lookup"><span data-stu-id="7cb0b-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="7cb0b-148">På fanen **Vedhæftede filer** kan du angive følgende parametre:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="7cb0b-149">I feltet **Konfigurationer** skal du vælge typen **Fil** for **USMF**-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="7cb0b-150">I felterne **Jobarkiv**, **Midlertidig**, **Grundlag** og **Andre** skal du vælge typen **Fil**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="7cb0b-151">Du kan finde flere oplysninger om ER-parametre under [Konfigurere ER-strukturen](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="7cb0b-152">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="7cb0b-153">Alle ER-konfigurationer, der tilføjes, er markeret som ejet af en udbyder af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="7cb0b-154">Den udbyder af ER-konfigurationer, der aktiveres i arbejdsområdet **Elektronisk rapportering**, bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="7cb0b-155">Du skal derfor aktivere en udbyder af ER-konfigurationer i arbejdsområdet **Elektronisk rapportering**, før du begynder at tilføje eller redigere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="7cb0b-156">Det er kun ejeren af en ER-konfiguration, der kan redigere den.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="7cb0b-157">Før du kan redigere en ER-konfiguration, skal den relevante udbyder af ER-konfiguration aktiveres i arbejdsområdet **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="7cb0b-158">Gennemse listen over udbydere af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="7cb0b-159">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-160">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="7cb0b-161">På siden **Tabel over konfigurationsudbydere** har hver udbyderpost et entydigt navn og en entydig URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="7cb0b-162">Gennemse indholdet af denne side.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-162">Review the contents of this page.</span></span> <span data-ttu-id="7cb0b-163">Hvis der allerede findes en post for **Litware, Inc.** (`https://www.litware.com`), skal du springe den næste procedure over, [Tilføje en ny udbyder af ER-konfigurationer](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="7cb0b-164">Tilføje en ny udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="7cb0b-165">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-166">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Konfigurationsudbydere** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="7cb0b-167">På siden **Konfigurationsudbydere** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="7cb0b-168">I feltet **Navn** skal du angive **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="7cb0b-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="7cb0b-169">I feltet **Internetadresse** skal du angive `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="7cb0b-170">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="7cb0b-171">Aktivere en udbyder af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="7cb0b-172">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-173">Gå til siden **Lokaliseringskonkfigurationer**, og vælg feltet **Litware, Inc.** i sektionen **Konfigurationsudbydere**, og vælg derefter **Angiv som aktive**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="7cb0b-174">Få flere oplysninger om udbydere af ER-konfigurationer under [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="7cb0b-175">Importere standardkonfigurationer af ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="7cb0b-176">Importere standardkonfigurationer af ER</span><span class="sxs-lookup"><span data-stu-id="7cb0b-176">Import the standard ER configurations</span></span>

<span data-ttu-id="7cb0b-177">Hvis du vil føje standard-ER-konfigurationerne til din aktuelle forekomst af Microsoft Dynamics 365 Finance, skal du importere dem fra det ER-[lager](general-electronic-reporting.md#Repository), der er konfigureret for den pågældende forekomst.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="7cb0b-178">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-179">På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="7cb0b-180">På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="7cb0b-181">Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="7cb0b-182">På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="7cb0b-183">I oversigtspanelet **Versioner** skal du vælge version **1.1** for den valgte ER-formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="7cb0b-184">Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Siden Konfigurationslager](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="7cb0b-186">Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="7cb0b-187">Gennemse de importerede ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="7cb0b-188">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-189">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7cb0b-190">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="7cb0b-191">Bemærk, at der ud over det valgte **BACS (Storbritannien)**-format, blev importeret andre krævede ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="7cb0b-192">Kontroller, at følgende ER-konfigurationer er tilgængelige i konfigurationstræet:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="7cb0b-193">**Betalingsmodel** – denne konfiguration indeholder den [datamodel](general-electronic-reporting.md#data-model-and-model-mapping-components), der repræsenterer datastrukturen for betalingsforretningsdomænet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="7cb0b-194">**Tilknytning af betalingsmodel 1611** – denne konfiguration indeholder den [modeltilknytning](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-komponent, der beskriver, hvordan datamodellen udfyldes med applikationsdata under kørsel.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="7cb0b-195">**BACS (Storbritannien)** – denne konfiguration indeholder [format](general-electronic-reporting.md#FormatComponentOutbound) og formattilknytnings-ER-komponenter.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="7cb0b-196">Formatkomponenten angiver rapportlayoutet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-196">The format component specifies the report layout.</span></span> <span data-ttu-id="7cb0b-197">Komponenten til formattilknytning indeholder modeldatakilden og angiver, hvordan rapportlayoutet angives ved hjælp af denne datakilde på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Siden Konfigurationer](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="7cb0b-199">Klargøre en kreditorbetaling til behandling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="7cb0b-200">Tilføje bankoplysninger for kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="7cb0b-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="7cb0b-201">Du skal tilføje bankoplysninger for en kreditorkonto, som der vil blive henvist til senere i en registreret betaling.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="7cb0b-202">Gå til **Kreditor** \> **Kreditorer** \> **Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="7cb0b-203">På siden **Alle kreditorer** skal du vælge kreditorkontoen **GB_SI_000001**, og derefter skal du i handlingsruden på fanen **Kreditor** i gruppen **Konfigurer** vælge **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="7cb0b-204">På siden **Kreditorbankkonti** skal du vælge **Ny** og angive derefter følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="7cb0b-205">Angiv **GBP OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="7cb0b-206">Vælg **BankGBP** i feltet **Bankgrupper**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="7cb0b-207">Angiv **202015** i feltet **Bankkontonummer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="7cb0b-208">I feltet **SWIFT-kode** skal du angive <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="7cb0b-209">I feltet **IBAN** skal du angive **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="7cb0b-210">I feltet **Registreringsnummer** skal du beholde standardværdien <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Siden Kreditorbankkonti](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="7cb0b-212">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-212">Select **Save**.</span></span>
5. <span data-ttu-id="7cb0b-213">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-213">Close the page.</span></span>
6. <span data-ttu-id="7cb0b-214">På siden **Alle kreditorer** skal du åbne kreditorkontoen **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="7cb0b-215">På siden Kreditordetaljer skal du vælge **Rediger** for at gøre siden redigerbare, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="7cb0b-216">I oversigtspanelet **Betaling** skal du i feltet **Bankkonto** vælge **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Siden Kreditordetaljer](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="7cb0b-218">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-218">Select **Save**.</span></span>
10. <span data-ttu-id="7cb0b-219">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="7cb0b-220">Angive en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-220">Enter a vendor payment</span></span>

<span data-ttu-id="7cb0b-221">Du skal angive en ny kreditorbetaling ved hjælp af et [betalingsforslag](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-221">You must enter a new vendor payment by using a [payment proposal](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).</span></span>

1. <span data-ttu-id="7cb0b-222">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="7cb0b-223">På siden **Kreditorbetalingskladde** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="7cb0b-224">Vælg **VendPay** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="7cb0b-225">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-225">Select **Lines**.</span></span>
5. <span data-ttu-id="7cb0b-226">Vælg **Betalingsforslag** \> **Opret betalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="7cb0b-227">I dialogboksen **Kreditorbetalingsforslag** skal du konfigurere betingelser, der kun filtrerer efter poster for kreditorkontoen **GB_SI_000001**, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="7cb0b-228">Marker linjen for fakturaen **00000007_Inv**, og vælg derefter **Opret betaling**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Dialogboksen Kreditorbetalingsforslag](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="7cb0b-230">Kontroller, at den angivne betaling er konfigureret til at bruge den **elektroniske** betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Side med leverandørbetalinger](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="7cb0b-232">Behandle kreditorbetaling ved hjælp af standard-ER-formatet</span><span class="sxs-lookup"><span data-stu-id="7cb0b-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="7cb0b-233">Konfigurere den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="7cb0b-233">Set up the electronic payment method</span></span>

<span data-ttu-id="7cb0b-234">Du skal konfigurere den elektroniske betalingsmåde, så den bruger den importeret ER-formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="7cb0b-235">Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="7cb0b-236">Gå til siden **Betalingsmetoder – kreditorer**, og vælg den **elektroniske** betalingsmetode i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="7cb0b-237">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-237">Select **Edit**.</span></span>
4. <span data-ttu-id="7cb0b-238">I oversigtspanelet **Filformater** til at angive indstillingen **Generelt elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="7cb0b-239">I feltet **Eksportér formatkonfiguration** skal du vælge formatkonfigurationen **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Betalingsmåder – kreditorside](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="7cb0b-241">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="7cb0b-242">Behandle en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-242">Process a vendor payment</span></span>

1. <span data-ttu-id="7cb0b-243">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="7cb0b-244">På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du tilføjede tidligere, og derefter vælge **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="7cb0b-245">Vælg **Generer betalinger** på siden **Kreditorbetalinger**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="7cb0b-246">I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="7cb0b-247">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="7cb0b-248">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="7cb0b-249">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-249">Select **OK**.</span></span>
6. <span data-ttu-id="7cb0b-250">I dialogboksen **Parametre til elektronisk rapportering** skal du angive indstillingen **Udskriv kontrolrapport** til **Ja** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Siden med dialogboksen Parametre til elektronisk rapportering](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="7cb0b-252">Ud over betalingsfilen kan du nu oprette kontrolrapporten.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="7cb0b-253">Hent zip-filen, og udtræk derefter følgende filer fra den:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="7cb0b-254">Kontrolrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-254">The control report in Excel format</span></span>
    - <span data-ttu-id="7cb0b-255">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-255">The payment file in TXT format</span></span>

        <span data-ttu-id="7cb0b-256">Bemærk, at i overensstemmelse med [strukturen](#PositionRoutingNumber) i det angivne ER-format starter betalingslinjen i den genererede fil med det registreringsnummer, der blev [defineret](#DefineRoutingNumber) for den konfigurerede bankkonto.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="7cb0b-258">Tilpasse standard-ER-formatet</span><span class="sxs-lookup"><span data-stu-id="7cb0b-258">Customize the standard ER format</span></span>

<span data-ttu-id="7cb0b-259">I eksemplet, der vises i dette afsnit, bruger du de ER-konfigurationer, der leveres af Microsoft, til at generere kreditorbetalingsfiler i BACS-format, men du skal tilføje en tilpasning for at understøtte kravene til en bestemt bank.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="7cb0b-260">Det er også en god ide at opgradere det brugerdefinerede format, når nye versioner af ER-konfigurationer bliver tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="7cb0b-261">Du vil dog være i stand til at opgradere til den laveste omkostning.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="7cb0b-262">I dette tilfælde skal du som repræsentant for Litware, Inc. oprette (aflede) en ny standard-ER-formatkonfiguration ved at bruge konfigurationen leveret af **BACS (Storbritannien)** Microsoft som basis.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="7cb0b-263">Oprette et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-263">Create a custom format</span></span>

1. <span data-ttu-id="7cb0b-264">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7cb0b-265">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="7cb0b-266">Litware, Inc. vil bruge version 1.1 af denne ER-formatkonfiguration som basis for den brugerdefinerede version.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="7cb0b-267">Vælg **Opret konfiguration** for at åbne dialogboksen med rullemenu.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="7cb0b-268">Du kan bruge denne dialogboks til at oprette en ny konfiguration for et brugerdefineret betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="7cb0b-269">I feltet **Ny** skal du vælge indstillingen **Afledt fra navn: BACS (Storbritannien), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="7cb0b-270">Angiv **BACS (UK – brugerdefineret )** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Dialogboks til rulleliste Opret konfiguration](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="7cb0b-272">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-272">Select **Create configuration**.</span></span>

<span data-ttu-id="7cb0b-273">Version 1.1.1 af **BACS (UK – brugerdefineret)** ER-formatkonfiguration er oprettet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="7cb0b-274">Denne version har [statussen](general-electronic-reporting.md#component-versioning) **Kladde** og kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="7cb0b-275">Det aktuelle indhold af det brugerdefinerede ER-format svarer til indholdet af det format, der er leveret af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Siden Konfigurationer](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="7cb0b-277">Redigere et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-277">Edit a custom format</span></span>

<span data-ttu-id="7cb0b-278">Du skal konfigurere det brugerdefinerede format, så det opfylder de bankspecifikke krav.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="7cb0b-279">En bank kan f.eks. kræve, at betalingsfiler, der genereres, omfatter EU-koden til SWIFT-koden (Society for Worldwide Interbank Financial Telecommunication) for den bank, der er tildelt agentrollen i den behandlede kreditorbetaling.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="7cb0b-280">SWIFT-koder er internationale bankkoder, der identificerer specifikke banker verden over.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="7cb0b-281">De kaldes også BIC'er (Bank Identifier Codes).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="7cb0b-282">SWIFT-koden skal indeholde 11 tegn, og den skal angives i begyndelsen af hver betalingslinje i en genereret betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="7cb0b-283">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7cb0b-284">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (UK brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="7cb0b-285">I oversigtspanelet **Versioner** skal du vælge version **1.1.1** for den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="7cb0b-286">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-286">Select **Designer**.</span></span>
5. <span data-ttu-id="7cb0b-287">På siden **Formatdesigner** skal du vælge **Vis detaljer** for at få vist flere oplysninger om formatelementerne.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="7cb0b-288">Udvid og gennemse følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="7cb0b-289">Elementet **BACSReportsFolder** typen **Mappe**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="7cb0b-290">Dette element bruges til at oprette output i ZIP-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="7cb0b-291">Elementet **Fil** for typen **Fil**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="7cb0b-292">Dette element bruges til at oprette en betalingsfil i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="7cb0b-293">Elementet **Transaktioner** for typen **Rækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="7cb0b-294">Dette element bruges til at oprette en enkelt betalingslinje i en betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="7cb0b-295">Elementet **Transaktion** for typen **Rækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="7cb0b-296">Dette element bruges til at oprette individuelle felter for en enkelt betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="7cb0b-297">Vælg elementet **Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-297">Select the **transaction** element.</span></span>

    ![Transaktionselementet i ER-operationsdesigneren](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="7cb0b-299">Den leverede rapport konfigureres, så <a id="PositionRoutingNumber"></a>alle betalingslinjer starter med bankens registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="7cb0b-300">Formatelementet **vendBankRouteNum** bruges til dette formål.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="7cb0b-301">Vælg **Tilføj**, og vælg derefter typen **Tekst\\Streng** for det formatelement, du vil tilføje:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="7cb0b-302">I feltet **Navn** skal du angive **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="7cb0b-303">Angiv **11** i feltet **Minimumlængde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="7cb0b-304">Angiv **11** i feltet **Maksimumlængde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="7cb0b-305">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cb0b-306">Elementet **vendBankSWIFT** bruges til at angive SWIFT-koden for en kreditors bank i genererede filer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="7cb0b-307">Vælg **vendBankSWIFT** i formattræstrukturen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="7cb0b-308">Vælg **Flyt op** for at flytte det valgte formatelement et niveau op.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="7cb0b-309">Gentag dette trin, indtil elementet **vendBankSWIFT** er det <a id="PositionSWIFTCode"></a>første element under det overordnede element **transaktion**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT som det første element under transaktion i ER-operationsdesigner](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="7cb0b-311">Mens **vendBankSWIFT** stadig er markeret i formatets strukturtræ, skal du vælge fanen **Tilknytning** og derefter udvide datakilden **model**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="7cb0b-312">Udvid **model.Payment** \> **model.Payment.CreditorAgent**, og vælg datakildefeltet **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="7cb0b-313">Dette datakildefelt viser SWIFT-koden for en kreditorbank, der er tildelt agentrollen i den behandlede kreditorbetaling.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="7cb0b-314">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-314">Select **Bind**.</span></span> <span data-ttu-id="7cb0b-315">Formatelementet **VendBankSWIFT** er nu bundet sammen med datakildefeltet **model.Payment.CreditorAgent.BICFI**, så SWIFT-koderne angives i genererede betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![vendBankSWIFT-formatelement, der er bundet til datakildefeltet model.Payment.CreditorAgent.BICFI, er i ER-operationsdesigner](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="7cb0b-317">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-317">Select **Save**.</span></span>
15. <span data-ttu-id="7cb0b-318">Luk designersiden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="7cb0b-319">Markere et brugerdefineret format som kørbart</span><span class="sxs-lookup"><span data-stu-id="7cb0b-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="7cb0b-320">Nu, hvor den første version af det brugerdefinerede format er blevet oprettet og har statussen **Kladde**, kan du køre den til testformål.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="7cb0b-321">Hvis du vil køre rapporten, skal du behandle en kreditorbetaling ved hjælp af den betalingsmåde, der refererer til det brugerdefinerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="7cb0b-322">Som standard er det kun versioner, der har statussen **Fuldført** eller **Delt** der [tages i betragtning](general-electronic-reporting.md#component-versioning), når du kalder et ER-format fra applikationen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="7cb0b-323">Denne funktionsmåde er med til at forhindre, at ER-formater med uafsluttede design bliver brugt.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="7cb0b-324">Men når det gælder dine testkørsler, kan du tvinge programmet til at bruge den version af dit ER-format, der har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="7cb0b-325">På denne måde kan du justere den aktuelle formatversion, hvis der kræves ændringer.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="7cb0b-326">Du kan finde flere oplysninger under [Anvendelighed](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="7cb0b-327">Hvis du vil bruge kladdeversionen af et ER-format, skal du eksplicit markere ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="7cb0b-328">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7cb0b-329">På siden **Konfigurationer** i handlingsruden skal du under fanen **Konfigurationer** i gruppen **Avancerede indstillinger** vælge **Brugerparametre**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="7cb0b-330">I dialogboksen **Brugerparametre** skal du angive indstillingen **Kørselsindstillinger** til **Ja** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="7cb0b-331">Vælg **Rediger** for at gøre den aktuelle side redigerbar efter behov.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="7cb0b-332">Vælg **BACS (UK brugerdefineret)** i konfigurationstræet i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="7cb0b-333">Angiv indstillingen **Kør kladde** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Indstillingen Kør kladde på siden Konfigurationer](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="7cb0b-335">Behandle kreditorbetaling ved hjælp af det brugerdefinerede ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="7cb0b-336">Konfigurere den elektroniske betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="7cb0b-336">Set up the electronic payment method</span></span>

<span data-ttu-id="7cb0b-337">Du skal konfigurere den elektroniske betalingsmåde, så det brugerdefinerede ER-format bruges til at behandle kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="7cb0b-338">Gå til **Kreditor** \> **Opsætning af betaling** \> **Betalingsmåder**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="7cb0b-339">Gå til siden **Betalingsmetoder – kreditorer**, og vælg den **elektroniske** betalingsmetode i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="7cb0b-340">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-340">Select **Edit**.</span></span>
4. <span data-ttu-id="7cb0b-341">I oversigtspanelet **Filformat** til at angive indstillingen **Generelt elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="7cb0b-342">I feltet **Eksportér formatkonfiguration** skal du vælge formatkonfigurationen **BACS (UK brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Betalingsmåder – kreditorside](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="7cb0b-344">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="7cb0b-345">Behandle en kreditorbetaling</span><span class="sxs-lookup"><span data-stu-id="7cb0b-345">Process a vendor payment</span></span>

1. <span data-ttu-id="7cb0b-346">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="7cb0b-347">På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="7cb0b-348">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-348">Select **Lines**.</span></span>
4. <span data-ttu-id="7cb0b-349">Gå til siden **Kreditorbetalinger**, og vælg **Betalingsstatus** \> **Ingen** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="7cb0b-350">Vælg **Generer betaling**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="7cb0b-351">I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="7cb0b-352">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="7cb0b-353">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="7cb0b-354">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-354">Select **OK**.</span></span>
8. <span data-ttu-id="7cb0b-355">I dialogboksen **Parametre til elektronisk rapportering** skal du angive indstillingen **Udskriv kontrolrapport** til **Ja** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7cb0b-356">Ud over betalingsfilen kan du kun oprette kontrolrapporten.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="7cb0b-357">Hent zip-filen, og udtræk derefter følgende filer fra den:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="7cb0b-358">Kontrolrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-358">The control report in Excel format</span></span>
    - <span data-ttu-id="7cb0b-359">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-359">The payment file in TXT format</span></span>

        <span data-ttu-id="7cb0b-360">Bemærk, at betalingslinjen i den genererede fil nu [starter](#PositionSWIFTCode) med den SWIFT-kode, der blev [angivet](#DefineSWIFTCode) for bankkontoen for den kreditor, hvor betalingen er behandlet, i overensstemmelse med strukturen i det brugerdefinerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="7cb0b-362">Importere nye version af standardkonfigurationer af ER-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="7cb0b-363">I eksemplet, der vises i dette afsnit, modtager du en meddelelse om vidensdatabaseartikel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="7cb0b-364">Denne besked oplyser dig om den nye version af ER-formatet **BACS (Storbritannien)**, der er udgivet af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="7cb0b-365">Ud over kontrolrapporten lader denne nye version brugere oprette betalingsadviseringsrapporten og rapporten over mødenotater, mens en kreditorbetaling behandles.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="7cb0b-366">Det er en funktion, du vil blive glad for.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="7cb0b-367">Importere nye version af standardkonfigurationer af ER</span><span class="sxs-lookup"><span data-stu-id="7cb0b-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="7cb0b-368">Hvis du vil tilføje nye versioner af ER-konfigurationerne til den aktuelle Finans-forekomst, skal du importere dem fra ER-[lageret](general-electronic-reporting.md#Repository), som du har konfigureret.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="7cb0b-369">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-370">På siden **Lokaliseringskonfigurationer** skal du i sektionen **Konfigurationsudbydere** vælge feltet **Microsoft** og derefter vælge **Lagre** for at få vist listen over lagre for Microsoft-udbyderen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="7cb0b-371">På siden **Konfigurationslagre** skal du vælge lageret for **Global**-typen og derefter vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="7cb0b-372">Hvis du bliver bedt om at angive godkendelse for at oprette forbindelse til Regulatory Configuration Service, skal du følge godkendelsesvejledningen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="7cb0b-373">På siden **Konfigurationslager** skal du i konfigurationstræet i venstre rude vælge formatkonfigurationen **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="7cb0b-374">I oversigtspanelet **Versioner** skal du vælge version **3.3** for den valgte ER-formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="7cb0b-375">Vælg **Importér** for at hente den valgte version fra Global-lageret til den aktuelle Finans-forekomst.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Siden Konfigurationslager](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="7cb0b-377">Hvis du har problemer med at få adgang til det [globale lager](er-download-configurations-global-repo.md), kan du i stedet [hente konfigurationer](download-electronic-reporting-configuration-lcs.md) fra LCS i stedet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="7cb0b-378">Gennemse de importerede ER-formatkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="7cb0b-379">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-380">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7cb0b-381">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="7cb0b-382">I oversigtspanelet **Versioner** skal du vælge version **3.3**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="7cb0b-383">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-383">Select **Designer**.</span></span>
6. <span data-ttu-id="7cb0b-384">Gå til siden **Formatdesigner**, udvid formatelementet **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="7cb0b-385">Bemærk, at version 3.3 indeholder det formatelementet **PaymentAdviceReport**, der bruges til at generere en betalingsadviseringsrapport, når en kreditorbetaling behandles.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![PaymentAdviceReport-formatet i ER-operationsdesigneren](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="7cb0b-387">Luk designersiden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="7cb0b-388">Anvende ændringerne i den nye version af et importeret format i et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="7cb0b-389">Fuldføre den aktuelle kladdeversion af et brugerdefineret format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="7cb0b-390">Hvis du vil beholde den aktuelle tilstand for det brugerdefinerede format, skal du fuldføre kladdeversion 1.1.1 ved at ændre dens status fra **Kladde** til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="7cb0b-391">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7cb0b-392">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Rapporteringskonfigurationer** i sektionen **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7cb0b-393">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (Storbritannien)** og derefter vælge **BACS (UK brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="7cb0b-394">I oversigtspanelet **Versioner** skal du vælge **Skift status** \> **Fuldfør** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="7cb0b-395">Statussen for version 1.1.1 ændres fra **Kladde** til **Fuldført**, og versionen bliver skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="7cb0b-396">Der er tilføjet en ny redigerbar version, 1.1.2, som har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="7cb0b-397">Du kan bruge denne version til at foretage yderligere ændringer i det brugerdefinerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="7cb0b-398">Basere et brugerdefineret format på en ny basisversion</span><span class="sxs-lookup"><span data-stu-id="7cb0b-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="7cb0b-399">Hvis du vil begynde at bruge den nye funktionalitet i version 3.3 af formatet **BACS (Storbritannien)** i tilpasningen, skal du ændre den grundlæggende konfigurationsversion for den brugerdefinerede konfiguration, **BACS (Storbritannien)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="7cb0b-400">Denne proces kaldes [rebasering](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="7cb0b-401">I stedet for version 1.1 af **BACS (Storbritannien)** skal du bruge version 3.3.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="7cb0b-402">Gå til **Organisationsadministration** \> **Elektronisk rapportering** \> **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="7cb0b-403">På siden **Konfigurationer** skal du i konfigurationstræet i venstre rude udvide **Betalingsmodel** og derefter vælge **BACS (UK brugerdefineret)**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="7cb0b-404">I oversigtspanelet **Versioner** skal du vælge version **1.1.2** og derefter **Rebasér**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="7cb0b-405">I dialogboksen **Rebasér** skal du i feltet **Målversion** vælge version **3.3** af basiskonfiguration for at anvende den som den ny base og bruge den til at opdatere konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialogboksen Rebasér](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="7cb0b-407">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-407">Select **OK**.</span></span>
6. <span data-ttu-id="7cb0b-408">Bemærk, at nummeret på kladdeversionen er ændret fra **1.1.2** til **3.3.2**, så den afspejler ændringen i basisversionen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="7cb0b-409">Når den brugerdefinerede version og en ny basisversion flettes, kan der blive registreret nogle konflikter på grund af formatændringer, der ikke kan flettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Rebaseret konfiguration med konflikter på siden Konfigurationer](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="7cb0b-411">Hvis der registreres konflikter, skal de løses manuelt i formatdesigneren.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="7cb0b-412">I oversigtspanelet **Versioner** skal du vælge version **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="7cb0b-413">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-413">Select **Designer**.</span></span>
9. <span data-ttu-id="7cb0b-414">Gå til siden **Formatdesigner**, og vælg en post med en rebaseringskonflikt i oversigtspanelet **Detaljer**, og vælg derefter **Anvend basisværdi**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Rebaserer konfliktpost i ER-operationsdesigner](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="7cb0b-416">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-416">Select **Save**.</span></span>

    <span data-ttu-id="7cb0b-417">Posten for rebaseringskonflikten skal ikke længere vises i oversigtspanelet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikt er løst i ER-operationsdesigner](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="7cb0b-419">Du har løst konflikten ved at bekræfte, at version 3 af basismodellen skal bruges i dette ER-format.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="7cb0b-420">Udvid **BACSReportsFolder** \> **fil** \> **transaktioner** \> **transaktion**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="7cb0b-421">Under fanen **Tilknytning** kan du se, at version 3.3.2 i det brugerdefinerede ER-format indeholder både din tilpasning (formatelementet **vendBankSWIFT** og dets binding) og den nye funktionalitet i version 3.3 af basis-ER-formatet, der blev angivet af Microsoft (elementformatet **PaymentAdviceReport** sammen med de indlejrede elementer og konfigurerede bindinger).</span><span class="sxs-lookup"><span data-stu-id="7cb0b-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="7cb0b-422">Med blot nogle få klik med musen har du indført ændringerne af en ny basisversion ved at flette dem med tilpasningen.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Flettet format i ER-operationsdesigner](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="7cb0b-424">Luk designersiden.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="7cb0b-425">Rebaseringshandling kan fortrydes.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-425">The rebase action is reversible.</span></span> <span data-ttu-id="7cb0b-426">Hvis du vil annullere denne rebasering, skal du vælge version **1.1.1** af formatet **BACS (UK brugerdefineret)** i oversigtspanelet **Versioner** og derefter vælge **Hent denne version**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="7cb0b-427">Version 3.3.2 vil derefter blive omnummereret til 1.1.2, og indholdet af kladdeversion 1.1.2 vil svare til indholdet af version 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="7cb0b-428">Behandle kreditorbetaling ved hjælp af et ER-format med ny base</span><span class="sxs-lookup"><span data-stu-id="7cb0b-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="7cb0b-429">Gå til **Kreditor** \> **Betalinger** \> **Betalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="7cb0b-430">På siden **Kreditorbetalingskladde** skal du vælge den betalingskladde, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="7cb0b-431">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-431">Select **Lines**.</span></span>
4. <span data-ttu-id="7cb0b-432">Gå til siden **Kreditorbetalinger**, og vælg **Betalingsstatus** \> **Ingen** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="7cb0b-433">Vælg **Generer betaling**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="7cb0b-434">I dialogboksen **Opret betalinger** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="7cb0b-435">Vælg **Elektronisk** i feltet **Betalingsmåde**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="7cb0b-436">Vælg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="7cb0b-437">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-437">Select **OK**.</span></span>
8. <span data-ttu-id="7cb0b-438">I dialogboksen **Parametre til elektronisk rapportering** skal du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="7cb0b-439">Angiv indstillingen **Udskriv kontrolrapport** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="7cb0b-440">Angiv indstillingen **Udskriv betalingsadvisering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialogboksen Parametre til elektronisk rapportering](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="7cb0b-442">Ud over betalingsfilen kan du nu generere både kontrolrapporten og betalingsadviseringsrapporten.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="7cb0b-443">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-443">Select **OK**.</span></span>
10. <span data-ttu-id="7cb0b-444">Hent zip-filen, og udtræk derefter følgende filer fra den:</span><span class="sxs-lookup"><span data-stu-id="7cb0b-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="7cb0b-445">Kontrolrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-445">The control report in Excel format</span></span>
    - <span data-ttu-id="7cb0b-446">Betalingsadviseringsrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-446">The payment advice report in Excel format</span></span>

        ![Betalingsadviseringsrapport i Excel-format](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="7cb0b-448">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="7cb0b-448">The payment file in TXT format</span></span>

        <span data-ttu-id="7cb0b-449">Bemærk, at betalingslinjen i den genererede fil starter med den SWIFT-kode, der blev angivet for bankkontoen for den kreditor, hvor betalingen er behandlet.</span><span class="sxs-lookup"><span data-stu-id="7cb0b-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="7cb0b-451">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7cb0b-451">Additional resources</span></span>

- [<span data-ttu-id="7cb0b-452">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="7cb0b-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7cb0b-453">Hente ER-konfigurationer fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7cb0b-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="7cb0b-454">Hente ER/konfigurationer fra det globale lager til Konfigurationstjenesten</span><span class="sxs-lookup"><span data-stu-id="7cb0b-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]