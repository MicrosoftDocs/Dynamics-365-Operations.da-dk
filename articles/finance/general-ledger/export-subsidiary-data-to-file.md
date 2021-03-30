---
title: Eksporter datterselskabsdata til filer
description: Dette emne forklarer, hvordan du forbereder eksport af data fra Microsoft Dynamics 365 Finance og derefter importerer dem til en konsolideret juridisk enhed.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205493"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="4180f-103">Eksporter datterselskabsdata til filer</span><span class="sxs-lookup"><span data-stu-id="4180f-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4180f-104">Brug siden **Eksport** (**Systemadministration \> Arbejdsområder \> Import/eksport**) til at forberede eksport af datterselskabsdata til filer, der derefter kan importeres til en konsolideret juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="4180f-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="4180f-105">Yderligere oplysninger om import- og eksportprocesser i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="4180f-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="4180f-106">Opret en juridisk enhed til brug i konsolideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="4180f-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="4180f-107">Du kan finde flere oplysninger om at oprette juridiske enheder i [Oprette juridisk enhed](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="4180f-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="4180f-108">Du kan finde flere oplysninger i [Forberede en juridisk enhed til brug i konsolideringsprocessen](prepare-company-for-consolidation.md) og [Konfigurere en juridisk enhed til konsolidering](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="4180f-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="4180f-109">Gå til **Konsolideringer \> Eksporter firmasaldi**.</span><span class="sxs-lookup"><span data-stu-id="4180f-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="4180f-110">På siden **Eksporter firmasaldi** skal du angive detaljerne om konsolideringen under fanen **Kriterium** ved at angive følgende felter.</span><span class="sxs-lookup"><span data-stu-id="4180f-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="4180f-111">Felt</span><span class="sxs-lookup"><span data-stu-id="4180f-111">Field</span></span>                             | <span data-ttu-id="4180f-112">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="4180f-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="4180f-113">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="4180f-113">Main account</span></span>                      | <span data-ttu-id="4180f-114">Angiv de konti, der skal konsolideres.</span><span class="sxs-lookup"><span data-stu-id="4180f-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="4180f-115">Hvis du vil medtage alle konti, skal du lade dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="4180f-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="4180f-116">Brug koncernkonto</span><span class="sxs-lookup"><span data-stu-id="4180f-116">Use consolidation account</span></span>         | <span data-ttu-id="4180f-117">Hvis du har angivet koncernkonti, skal du angive denne indstilling til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4180f-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="4180f-118">Vælg koncernkonto fra</span><span class="sxs-lookup"><span data-stu-id="4180f-118">Select consolidation account from</span></span> | <span data-ttu-id="4180f-119">Vælg enten **Hovedkonto** eller **Konsolideringskontogruppe**.</span><span class="sxs-lookup"><span data-stu-id="4180f-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="4180f-120">Koncernkontogruppe</span><span class="sxs-lookup"><span data-stu-id="4180f-120">Consolidation account group</span></span>       | <span data-ttu-id="4180f-121">Vælg en koncernkontogruppe, du vil klassificere koncernkontoen efter.</span><span class="sxs-lookup"><span data-stu-id="4180f-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="4180f-122">Konsolideringsperiode</span><span class="sxs-lookup"><span data-stu-id="4180f-122">Consolidation period</span></span>              | <span data-ttu-id="4180f-123">Angiv "fra" og "til" datointerval til konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="4180f-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="4180f-124">Medtag faktiske beløb</span><span class="sxs-lookup"><span data-stu-id="4180f-124">Include actual amounts</span></span>            | <span data-ttu-id="4180f-125">Angiv denne indstilling til **Ja**, hvis du vil medtage faktiske beløb.</span><span class="sxs-lookup"><span data-stu-id="4180f-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="4180f-126">Medtag budgetbeløb</span><span class="sxs-lookup"><span data-stu-id="4180f-126">Include budget amounts</span></span>            | <span data-ttu-id="4180f-127">Angiv denne indstilling til **Ja**, hvis du vil medtage budgetbeløb i konsolideringer.</span><span class="sxs-lookup"><span data-stu-id="4180f-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="4180f-128">Budgetmodeller</span><span class="sxs-lookup"><span data-stu-id="4180f-128">Budget models</span></span>                     | <span data-ttu-id="4180f-129">Angiv den budgetmodel, der skal medtages.</span><span class="sxs-lookup"><span data-stu-id="4180f-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="4180f-130">Angiv på fanen **Økonomiske dimensioner** detaljerne i konsolideringen.</span><span class="sxs-lookup"><span data-stu-id="4180f-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="4180f-131">Angiv de økonomiske dimension, der skal overføres fra transaktionerne i datterselskabskontiene til transaktionerne i den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="4180f-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="4180f-132">Vælg de økonomiske dimensioner i oversigten .</span><span class="sxs-lookup"><span data-stu-id="4180f-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="4180f-133">Identificer den korrekte specifikation for hver økonomisk dimension, der konsolideres.</span><span class="sxs-lookup"><span data-stu-id="4180f-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="4180f-134">De tilgængelige indstillinger omfatter **Dimension**, **Gruppedimension**, **Regnskab** og **Konto**.</span><span class="sxs-lookup"><span data-stu-id="4180f-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4180f-135">Med indstillingen **Gruppedimension** kan du definere den dimensionsværdi, der bruges af den gruppe af firmaer, der konsolideres.</span><span class="sxs-lookup"><span data-stu-id="4180f-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="4180f-136">Angiv den segmentrækkefølge, der skal konsolideres i.</span><span class="sxs-lookup"><span data-stu-id="4180f-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="4180f-137">På fanen **Juridiske enheder** skal du følge disse trin for at angive den juridiske enhed, der skal eksporteres:</span><span class="sxs-lookup"><span data-stu-id="4180f-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="4180f-138">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4180f-138">Select **New**.</span></span>
    2. <span data-ttu-id="4180f-139">Angiv den juridiske enhed i feltet **Juridisk kildeenhed**.</span><span class="sxs-lookup"><span data-stu-id="4180f-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="4180f-140">Hvis samme kriterier gælder for flere datterselskaber, der er i samme database, kan du overføre data fra disse datterselskaber til separate eksportfiler i en enkelt handling:</span><span class="sxs-lookup"><span data-stu-id="4180f-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="4180f-141">Opret en linje for hver juridisk datterselskabsenhed, hvis konti skal eksporteres til filer.</span><span class="sxs-lookup"><span data-stu-id="4180f-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="4180f-142">Disse filer importeres senere til den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="4180f-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="4180f-143">For hvert datterselskab skal du angive navnet på datterselskabet og navnet på den eksportfil, der oprettes under eksportjobbet.</span><span class="sxs-lookup"><span data-stu-id="4180f-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="4180f-144">I feltet **Kontotype til omregningsdifferencer** skal du vælge **Drift og tab** eller **Balance**.</span><span class="sxs-lookup"><span data-stu-id="4180f-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="4180f-145">Angiv et filnavn til den eksportfil, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="4180f-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="4180f-146">Vælg **OK** for at køre eksporten.</span><span class="sxs-lookup"><span data-stu-id="4180f-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="4180f-147">Når eksporten er fuldført, modtager du en meddelelse, der viser antallet af poster, der er gemt i hver fil.</span><span class="sxs-lookup"><span data-stu-id="4180f-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="4180f-148">Derefter kan du importere filerne til den konsoliderede juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="4180f-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]