---
title: Sammenlign lagerrapport over varepriser
description: Få mere at vide om, hvordan du opretter en rapport vedrørende sammenligning af lagerets varepriser og derefter gennemser og/eller eksporterer resultatet.
author: AndersGirke
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 80e376db3616af27d94ee55480cd2f56441db93b
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2020
ms.locfileid: "3072109"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="b1485-103">Sammenlign lagerrapport over varepriser</span><span class="sxs-lookup"><span data-stu-id="b1485-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1485-104">I dette emne forklares det, hvordan du kan køre en rapport over **Sammenligning af lagerets varepriser** og gøre outputtet digitalt tilgængeligt enten som en interaktiv side i Dynamics 365 Supply Chain Management eller som et eksporteret dokument i et af de flere tilgængelige formater.</span><span class="sxs-lookup"><span data-stu-id="b1485-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="b1485-105">Når du får vist rapporten i din browser, reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det layout, du har konfigureret.</span><span class="sxs-lookup"><span data-stu-id="b1485-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="b1485-106">Du kan sortere resultaterne, filtrere dem, gå mere i dybden i dataene og meget mere.</span><span class="sxs-lookup"><span data-stu-id="b1485-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="b1485-107">Rapportresultater gemmes i dataenheden **Sammenligning af varepriser**, som giver dig mulighed for at filtrere og eksportere resultaterne til et format som f.eks. CSV eller Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b1485-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="b1485-108">Rapporten **Sammenligning af varepriser på lageret** er nyttig, hvis afgangen indeholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="b1485-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="b1485-109">Outputtet indeholder f.eks. mange linjer, hvis du har mere end 40.000 varer, der har en afventende varepris i efterkalkulationsversionen.</span><span class="sxs-lookup"><span data-stu-id="b1485-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="b1485-110">Aktiver sammenligning af varepriser på lageret</span><span class="sxs-lookup"><span data-stu-id="b1485-110">Enable compare item prices storage</span></span>

<span data-ttu-id="b1485-111">Før du kan bruge denne funktion, skal du aktivere den i dit system.</span><span class="sxs-lookup"><span data-stu-id="b1485-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="b1485-112">Administratorer kan bruge indstillingerne [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="b1485-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="b1485-113">Her er funktionen angivet som:</span><span class="sxs-lookup"><span data-stu-id="b1485-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="b1485-114">**Modul** - Omkostningsstyring</span><span class="sxs-lookup"><span data-stu-id="b1485-114">**Module** - Cost management</span></span>
- <span data-ttu-id="b1485-115">**Funktionsnavn** - Sammenligning af varepriser på lager</span><span class="sxs-lookup"><span data-stu-id="b1485-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="b1485-116">Generér en rapport, der sammenligner varepriserne på lageret</span><span class="sxs-lookup"><span data-stu-id="b1485-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="b1485-117">Udfør følgende trin for at generere og gemme en rapport for **Sammenligning af varepriser på lageret**:</span><span class="sxs-lookup"><span data-stu-id="b1485-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="b1485-118">Gå til **Omkostningsstyring > Forespørgsler og rapporter > Forudbestemte omkostningsrapporter > Sammenligning af varepriser på lageret**.</span><span class="sxs-lookup"><span data-stu-id="b1485-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="b1485-119">Vælg **Ny** for at åbne ruden **Sammenligning af varepriser**.</span><span class="sxs-lookup"><span data-stu-id="b1485-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="b1485-120">Angiv følgende indstillinger for at definere, hvilke priser der skal sammenlignes i rapporten:</span><span class="sxs-lookup"><span data-stu-id="b1485-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="b1485-121">I oversigtspanelet **Parametre** kan du give rapporten et unikt **Navn** og bruge felterne i de sektionerne **Afventende priser til sammenligning** og **Priser, som anvendes sammenligning** til at definere, hvilke priser og datoer der skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="b1485-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="b1485-122">I oversigtspanelet **Poster, som skal medtages** skal du konfigurere filtre og begrænsninger for at definere, hvilke data der skal medtages i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b1485-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="b1485-123">På oversigtspanelet **Kør i baggrunden** skal du angive, hvornår og hvor ofte rapporten skal genereres.</span><span class="sxs-lookup"><span data-stu-id="b1485-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="b1485-124">Denne rapport udføres altid som en del af et batchjob.</span><span class="sxs-lookup"><span data-stu-id="b1485-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="b1485-125">Vælg **OK** for at anvende dine indstillinger og lukke ruden.</span><span class="sxs-lookup"><span data-stu-id="b1485-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="b1485-126">Når batchjobbet er fuldført, vises det på siden **Sammenligning af varepriser på lageret**.</span><span class="sxs-lookup"><span data-stu-id="b1485-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="b1485-127">Du er muligvis nødt til at opdatere siden for at se rapporten.</span><span class="sxs-lookup"><span data-stu-id="b1485-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="b1485-128">Udforsk rapporten med sammenligningen af varepriserne på lageret</span><span class="sxs-lookup"><span data-stu-id="b1485-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="b1485-129">Når du har genereret en rapport, kan du til enhver tid få vist og udforske den på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="b1485-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="b1485-130">Gå til **Omkostningsstyring > Forespørgsler og rapporter > Forudbestemte omkostningsrapporter > Sammenligning af varepriser på lageret**.</span><span class="sxs-lookup"><span data-stu-id="b1485-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="b1485-131">Vælg en rapport på listen.</span><span class="sxs-lookup"><span data-stu-id="b1485-131">Select a report from the list.</span></span>

1. <span data-ttu-id="b1485-132">Benyt en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="b1485-132">Do one of the following:</span></span>

    - <span data-ttu-id="b1485-133">Vælg **Oversigt** for at få en oversigt over dine rapportresultater.</span><span class="sxs-lookup"><span data-stu-id="b1485-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="b1485-134">Vælg **Visningsdetaljer** for at få en mere detaljeret visning af rapporten</span><span class="sxs-lookup"><span data-stu-id="b1485-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="b1485-135">Når den valgte visning åbner, kan du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="b1485-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="b1485-136">Vælge næsten enhver kolonneoverskrift for at sortere eller filtrere tabellen efter værdier i kolonnen på samme måde som de fleste standardformularer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b1485-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="b1485-137">Bemærk, at du ikke kan sortere eller filtrere kolonnen **Nettoprisændring %**, da det er et beregnet felt.</span><span class="sxs-lookup"><span data-stu-id="b1485-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="b1485-138">Vælg **Dimensionsvisning** for at åbne en rude, hvor du kan vælge, hvilken dimensionskolonne der skal medtages i formularen.</span><span class="sxs-lookup"><span data-stu-id="b1485-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="b1485-139">Angiv **Gem opsætning** til **Ja**, hvis du vil gemme disse indstillinger, så de bevares, næste gang du åbner rapporten.</span><span class="sxs-lookup"><span data-stu-id="b1485-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="b1485-140">Vælg **OK** for at anvende dine indstillinger og lukke.</span><span class="sxs-lookup"><span data-stu-id="b1485-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="b1485-141">Vælg en række i formularen, og vælg derefter **Vis detaljer** for at få vist flere oplysninger om den valgte vare.</span><span class="sxs-lookup"><span data-stu-id="b1485-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="b1485-142">Du vil kunne gå i dybden med dataene herfra.</span><span class="sxs-lookup"><span data-stu-id="b1485-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="b1485-143">Vælg en række i formularen, og vælg derefter **Vis sammenligningsdiagram** for at få vist en interaktiv grafisk repræsentation af resultaterne, som de relaterer til den valgte vare.</span><span class="sxs-lookup"><span data-stu-id="b1485-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="b1485-144">Du kan udforske disse resultater ved at vælge forskellige grafiske elementer i diagrammet og i diagramforklaringen.</span><span class="sxs-lookup"><span data-stu-id="b1485-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="b1485-145">Vælg en række i formularen, og vælg derefter **Vis beregningsdetaljer** for at få vist flere oplysninger om de beregninger, der er relateret til den valgte vare.</span><span class="sxs-lookup"><span data-stu-id="b1485-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="b1485-146">Du vil kunne gå i dybden med dataene herfra.</span><span class="sxs-lookup"><span data-stu-id="b1485-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="b1485-147">Eksporter rapporten med sammenligningen af varepriserne på lageret</span><span class="sxs-lookup"><span data-stu-id="b1485-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="b1485-148">Hver rapport, du opretter, gemmes i dataenheden **Sammenligning af varepriser**.</span><span class="sxs-lookup"><span data-stu-id="b1485-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="b1485-149">Du kan bruge standardfunktionerne til datastyring i Supply Chain Management til at eksportere data fra denne enhed til alle understøttede dataformater, herunder CSV eller Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b1485-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="b1485-150">Følgende er et eksempel på, hvordan du kan eksportere en rapport over **Sammenligning af varepriser på lageret**:</span><span class="sxs-lookup"><span data-stu-id="b1485-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="b1485-151">Gå til **Systemadministration > Arbejdsområder > Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="b1485-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="b1485-152">Klik på knappen **Eksporter** i sektionen **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="b1485-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="b1485-153">Siden **Eksportér** åbnes, som du kan bruge til at konfigurere eksportjobbet.</span><span class="sxs-lookup"><span data-stu-id="b1485-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="b1485-154">Start med at give dit job et **Gruppenavn**.</span><span class="sxs-lookup"><span data-stu-id="b1485-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="b1485-155">I sektionen **Valgte enheder** skal du vælge **Tilføj enhed** for at åbne en dialogboks, hvor du kan angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="b1485-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="b1485-156">**Enhedsnavn** - Vælg **Sammenligning af varepriser**.</span><span class="sxs-lookup"><span data-stu-id="b1485-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="b1485-157">**Målformat for data** - Vælg det format, du vil eksportere til.</span><span class="sxs-lookup"><span data-stu-id="b1485-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="b1485-158">Vælg **Tilføj** for at tilføje den nye række, og vælg derefter **Luk** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b1485-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="b1485-159">Normalt skal du eksportere én rapport ad gangen.</span><span class="sxs-lookup"><span data-stu-id="b1485-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="b1485-160">Det kan du gøre ved at oprette et **Filter** for den række, du lige har tilføjet til ruden **Forespørgsler**.</span><span class="sxs-lookup"><span data-stu-id="b1485-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="b1485-161">På den måde kan du definere, hvilke rapporter fra enheden **Sammenligning af varepriser**, du vil medtage i eksporten.</span><span class="sxs-lookup"><span data-stu-id="b1485-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="b1485-162">Angiv følgende filterindstillinger for at eksportere en enkelt rapport:</span><span class="sxs-lookup"><span data-stu-id="b1485-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="b1485-163">På fanen **Afgrænsning** skal du vælge **Tilføj** for at tilføje en ny række.</span><span class="sxs-lookup"><span data-stu-id="b1485-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="b1485-164">Angiv **Tabel** til **Sammenligning af varepriser**.</span><span class="sxs-lookup"><span data-stu-id="b1485-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="b1485-165">Angiv **Afledt tabel** til **Sammenligning af varepriser**.</span><span class="sxs-lookup"><span data-stu-id="b1485-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="b1485-166">Angiv **Felt** til det felt, du vil filtrere efter.</span><span class="sxs-lookup"><span data-stu-id="b1485-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="b1485-167">Normalt bruges **Udførelsesnavn** eller **Kørselstidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="b1485-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="b1485-168">Angiv **Kriterier** til værdien fra det valgte felt, som du vil søge efter (enten rapportens navn eller det tidspunkt, rapporten blev oprettet på).</span><span class="sxs-lookup"><span data-stu-id="b1485-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="b1485-169">Hvis det er nødvendigt, kan du tilføje flere rækker til tabellen **Afgrænsning**, indtil du entydigt har identificeret den rapport, du søger efter.</span><span class="sxs-lookup"><span data-stu-id="b1485-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="b1485-170">Vælg **OK** for at gemme dine indstillinger og lukke.</span><span class="sxs-lookup"><span data-stu-id="b1485-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="b1485-171">Vælg **Gem** for at gemme eksportindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="b1485-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="b1485-172">Åbn fanen **Eksportindstillinger**, og vælg **Eksporter nu** for at generere eksportfilen.</span><span class="sxs-lookup"><span data-stu-id="b1485-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="b1485-173">Siden **Udførelsesoversigt** åbnes, hvor du kan se statussen for eksportjobbet og en liste over de enheder, der er eksporteret.</span><span class="sxs-lookup"><span data-stu-id="b1485-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="b1485-174">Vælg enheden **Sammenligning af varepriser** i området **Status for behandling af enhed**, og vælg derefter **Hent fil** for at hente de data, der eksporteres fra den pågældende enhed.</span><span class="sxs-lookup"><span data-stu-id="b1485-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="b1485-175">Du kan finde flere oplysninger om, hvordan du bruger datastyring til at eksportere data i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="b1485-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
