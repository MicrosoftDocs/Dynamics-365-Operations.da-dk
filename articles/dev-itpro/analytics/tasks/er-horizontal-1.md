--- 
title: "Designe formater til dynamisk at tilføje kolonnerne i Excel-rapporter som vandret udvidelige områder"
description: "Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 80cd2603ba5ee47f861077d75a955037ffbde96e
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="design-formats-to-dynamically-add-columns-to-excel-reports-as-horizontally-expandable-ranges"></a><span data-ttu-id="6be75-103">Designe formater til dynamisk at tilføje kolonnerne i Excel-rapporter som vandret udvidelige områder</span><span class="sxs-lookup"><span data-stu-id="6be75-103">Design formats to dynamically add columns to Excel reports as horizontally expandable ranges</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6be75-104">Følgende fremgangsmåde beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler af elektronisk rapportering, kan konfigurere et format for elektronisk indberetning (ER) for at generere rapporter som OPENXML-regnearksfiler (Excel), hvor de påkrævede kolonner kan oprettes dynamisk som områder, der kan udvides vandret.</span><span class="sxs-lookup"><span data-stu-id="6be75-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="6be75-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="6be75-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6be75-106">Du skal først udføre disse tre opgaveguider for at fuldføre disse trin:</span><span class="sxs-lookup"><span data-stu-id="6be75-106">To complete these steps, you must first complete these three task guides:</span></span> 

<span data-ttu-id="6be75-107">"ER Oprette en konfigurationsudbyder og markere den som aktiv"</span><span class="sxs-lookup"><span data-stu-id="6be75-107">“ER Create a configuration provider and mark it as active”</span></span>

<span data-ttu-id="6be75-108">"ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)"</span><span class="sxs-lookup"><span data-stu-id="6be75-108">“ER Use financial dimensions as a data source (Part 1: Design data model)”</span></span>

<span data-ttu-id="6be75-109">"ER Bruge økonomiske dimensioner som en datakilde (del 2: Modeltilknytning)"</span><span class="sxs-lookup"><span data-stu-id="6be75-109">“ER Use financial dimensions as a data source (Part 2: Model mapping)”</span></span>

<span data-ttu-id="6be75-110">Du skal hente og gemme en lokal kopi af skabelonen med et eksempel på en rapport findes her, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="6be75-110">You must also download and save a local copy of the template with a sample report found here, [https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 


<span data-ttu-id="6be75-111">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="6be75-111">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-report-configuration"></a><span data-ttu-id="6be75-112">Opret en ny rapportkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6be75-112">Create a new report configuration</span></span>
1. <span data-ttu-id="6be75-113">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6be75-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6be75-114">Vælg 'Eksempelmodel til økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-114">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6be75-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6be75-115">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="6be75-116">Skriv "Format baseret på eksempelmodellen for datamodellen Økonomiske dimensioner" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="6be75-116">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="6be75-117">Brug den model, der er oprettet i forvejen, som datakilde for den nye rapport.</span><span class="sxs-lookup"><span data-stu-id="6be75-117">Use the model created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="6be75-118">Skriv 'Eksempel på rapport med vandret områder, der kan udvides' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6be75-118">In the Name field, type 'Sample report with horizontally expandable ranges'.</span></span>
    * <span data-ttu-id="6be75-119">Eksempel på rapport med vandret områder, der kan udvides</span><span class="sxs-lookup"><span data-stu-id="6be75-119">Sample report with horizontally expandable ranges</span></span>  
6. <span data-ttu-id="6be75-120">Skriv 'Sådan opretter du Excel-output med dynamisk tilføjelse af kolonner' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6be75-120">In the Description field, type 'To make Excel output with dynamically adding columns'.</span></span>
    * <span data-ttu-id="6be75-121">Sådan opretter du Excel-output med dynamisk tilføjelse af kolonner</span><span class="sxs-lookup"><span data-stu-id="6be75-121">To make Excel output with dynamically adding columns</span></span>  
7. <span data-ttu-id="6be75-122">Vælg Post i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="6be75-122">In the Data model definition field, select Entry.</span></span>
8. <span data-ttu-id="6be75-123">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6be75-123">Click Create configuration.</span></span>

## <a name="design-the-report-format"></a><span data-ttu-id="6be75-124">Design rapportformatet</span><span class="sxs-lookup"><span data-stu-id="6be75-124">Design the report format</span></span>
1. <span data-ttu-id="6be75-125">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="6be75-125">Click Designer.</span></span>
2. <span data-ttu-id="6be75-126">Slå til/fra-knappen 'Vis detaljer' til.</span><span class="sxs-lookup"><span data-stu-id="6be75-126">Turn on the ‘Show details’ toggle button.</span></span>
3. <span data-ttu-id="6be75-127">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6be75-127">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="6be75-128">Klik på Importér fra Excel.</span><span class="sxs-lookup"><span data-stu-id="6be75-128">Click Import from Excel.</span></span>
5. <span data-ttu-id="6be75-129">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="6be75-129">Click Attachments.</span></span>
    * <span data-ttu-id="6be75-130">Importer rapportskabelonen.</span><span class="sxs-lookup"><span data-stu-id="6be75-130">Import the report’s template.</span></span> <span data-ttu-id="6be75-131">Brug den Excel-fil, du har downloadet til det.</span><span class="sxs-lookup"><span data-stu-id="6be75-131">Use Excel file that you downloaded for that.</span></span>  
6. <span data-ttu-id="6be75-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6be75-132">Click New.</span></span>
7. <span data-ttu-id="6be75-133">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="6be75-133">Click File.</span></span>
8. <span data-ttu-id="6be75-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6be75-134">Close the page.</span></span>
9. <span data-ttu-id="6be75-135">Indtast eller vælg en værdi i feltet Skabelon.</span><span class="sxs-lookup"><span data-stu-id="6be75-135">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="6be75-136">Vælg den downloadede skabelon.</span><span class="sxs-lookup"><span data-stu-id="6be75-136">Select the downloaded template.</span></span>  
10. <span data-ttu-id="6be75-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6be75-137">Click OK.</span></span>
    * <span data-ttu-id="6be75-138">Tilføj et nyt område for at oprette Excel-output dynamisk med så mange kolonner, som du har valgt (i formen for brugerdialogboksen) for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="6be75-138">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="6be75-139">Hver celle for hver kolonne repræsenterer navnet på en enkelt økonomisk dimension.</span><span class="sxs-lookup"><span data-stu-id="6be75-139">Each cell for every column will represent a single financial dimension’s name.</span></span>  
11. <span data-ttu-id="6be75-140">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="6be75-140">Click Add to open the drop dialog.</span></span>
12. <span data-ttu-id="6be75-141">Vælg "Excel\Range" i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-141">In the tree, select 'Excel\Range'.</span></span>
13. <span data-ttu-id="6be75-142">Skriv 'DimNames' i feltet Excel-interval.</span><span class="sxs-lookup"><span data-stu-id="6be75-142">In the Excel range field, type 'DimNames'.</span></span>
    * <span data-ttu-id="6be75-143">DimNames</span><span class="sxs-lookup"><span data-stu-id="6be75-143">DimNames</span></span>  
14. <span data-ttu-id="6be75-144">Vælg 'Vandret' i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="6be75-144">In the Replication direction field, select 'Horizontal'.</span></span>
15. <span data-ttu-id="6be75-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6be75-145">Click OK.</span></span>
16. <span data-ttu-id="6be75-146">Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-146">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
17. <span data-ttu-id="6be75-147">Klik på Flyt op.</span><span class="sxs-lookup"><span data-stu-id="6be75-147">Click Move up.</span></span>
18. <span data-ttu-id="6be75-148">Vælg 'Excel = "SampleFinDimWsReport"\Cell<DimNames>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-148">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<DimNames>'.</span></span>
19. <span data-ttu-id="6be75-149">Klik på Klip.</span><span class="sxs-lookup"><span data-stu-id="6be75-149">Click Cut.</span></span>
20. <span data-ttu-id="6be75-150">Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-150">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
21. <span data-ttu-id="6be75-151">Klik på Sæt ind.</span><span class="sxs-lookup"><span data-stu-id="6be75-151">Click Paste.</span></span>
22. <span data-ttu-id="6be75-152">Udvid 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-152">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
23. <span data-ttu-id="6be75-153">Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-153">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
24. <span data-ttu-id="6be75-154">Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-154">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
25. <span data-ttu-id="6be75-155">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-155">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
    * <span data-ttu-id="6be75-156">Tilføj et nyt område for at oprette Excel-output dynamisk med så mange kolonner, som du har valgt (i formen for brugerdialogboksen) for økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="6be75-156">Add a new range to dynamically create Excel output with as many columns as you selected (in the user dialog form) for financial dimensions.</span></span> <span data-ttu-id="6be75-157">Hver celle for hver kolonne repræsenterer en enkelt økonomisk dimensions værdi for de enkelte rapporteringstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="6be75-157">Each cell for every column will represent a single financial dimension’s value for each reporting transaction.</span></span>  
26. <span data-ttu-id="6be75-158">Klik på Tilføj et interval.</span><span class="sxs-lookup"><span data-stu-id="6be75-158">Click Add Range.</span></span>
27. <span data-ttu-id="6be75-159">Skriv 'DimValues' i feltet Excel-interval.</span><span class="sxs-lookup"><span data-stu-id="6be75-159">In the Excel range field, type 'DimValues'.</span></span>
    * <span data-ttu-id="6be75-160">DimValues</span><span class="sxs-lookup"><span data-stu-id="6be75-160">DimValues</span></span>  
28. <span data-ttu-id="6be75-161">Vælg 'Vandret' i feltet Replikeringsretning.</span><span class="sxs-lookup"><span data-stu-id="6be75-161">In the Replication direction field, select 'Horizontal'.</span></span>
29. <span data-ttu-id="6be75-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6be75-162">Click OK.</span></span>
30. <span data-ttu-id="6be75-163">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-163">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>'.</span></span>
31. <span data-ttu-id="6be75-164">Klik på Klip.</span><span class="sxs-lookup"><span data-stu-id="6be75-164">Click Cut.</span></span>
32. <span data-ttu-id="6be75-165">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-165">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
33. <span data-ttu-id="6be75-166">Klik på Sæt ind.</span><span class="sxs-lookup"><span data-stu-id="6be75-166">Click Paste.</span></span>
34. <span data-ttu-id="6be75-167">Udvid 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-167">In the tree, expand 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>

## <a name="map-format-elements-to-data-sources"></a><span data-ttu-id="6be75-168">Knyt formatelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="6be75-168">Map format elements to data sources</span></span>
1. <span data-ttu-id="6be75-169">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="6be75-169">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6be75-170">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-170">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6be75-171">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-171">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="6be75-172">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-172">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="6be75-173">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="6be75-174">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-174">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>'.</span></span>
7. <span data-ttu-id="6be75-175">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-175">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
8. <span data-ttu-id="6be75-176">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-176">Click Bind.</span></span>
9. <span data-ttu-id="6be75-177">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-177">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal'.</span></span>
10. <span data-ttu-id="6be75-178">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dimensionsdata: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
11. <span data-ttu-id="6be75-179">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-179">Click Bind.</span></span>
12. <span data-ttu-id="6be75-180">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-180">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>'.</span></span>
13. <span data-ttu-id="6be75-181">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Kredit: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
14. <span data-ttu-id="6be75-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-182">Click Bind.</span></span>
15. <span data-ttu-id="6be75-183">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-183">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>'.</span></span>
16. <span data-ttu-id="6be75-184">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Debet: Real' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
17. <span data-ttu-id="6be75-185">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-185">Click Bind.</span></span>
18. <span data-ttu-id="6be75-186">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-186">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>'.</span></span>
19. <span data-ttu-id="6be75-187">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Valuta: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
20. <span data-ttu-id="6be75-188">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-188">Click Bind.</span></span>
21. <span data-ttu-id="6be75-189">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-189">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>'.</span></span>
22. <span data-ttu-id="6be75-190">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Dato: Dato' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
23. <span data-ttu-id="6be75-191">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-191">Click Bind.</span></span>
24. <span data-ttu-id="6be75-192">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-192">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>'.</span></span>
25. <span data-ttu-id="6be75-193">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste\Bilag: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
26. <span data-ttu-id="6be75-194">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-194">Click Bind.</span></span>
27. <span data-ttu-id="6be75-195">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-195">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>'.</span></span>
28. <span data-ttu-id="6be75-196">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
29. <span data-ttu-id="6be75-197">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-197">Click Bind.</span></span>
30. <span data-ttu-id="6be75-198">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-198">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical'.</span></span>
31. <span data-ttu-id="6be75-199">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Transaktion: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
32. <span data-ttu-id="6be75-200">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-200">Click Bind.</span></span>
33. <span data-ttu-id="6be75-201">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-201">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>'.</span></span>
34. <span data-ttu-id="6be75-202">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste\Batch: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
35. <span data-ttu-id="6be75-203">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-203">Click Bind.</span></span>
36. <span data-ttu-id="6be75-204">Vælg 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-204">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical'.</span></span>
37. <span data-ttu-id="6be75-205">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Journal: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
38. <span data-ttu-id="6be75-206">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-206">Click Bind.</span></span>
39. <span data-ttu-id="6be75-207">Udvid 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-207">In the tree, expand 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
40. <span data-ttu-id="6be75-208">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste\Kode: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-208">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String'.</span></span>
41. <span data-ttu-id="6be75-209">Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-209">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>'.</span></span>
42. <span data-ttu-id="6be75-210">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-210">Click Bind.</span></span>
43. <span data-ttu-id="6be75-211">Vælg 'model: Data Eksempelmodel for datamodellen Økonomiske dimensioner\Dimensionsindstilling: Postliste' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-211">In the tree, select 'model: Data model Financial dimensions sample model\Dimensions setting: Record list'.</span></span>
44. <span data-ttu-id="6be75-212">Vælg 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-212">In the tree, select 'Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal'.</span></span>
45. <span data-ttu-id="6be75-213">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-213">Click Bind.</span></span>
46. <span data-ttu-id="6be75-214">Vælg 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-214">In the tree, select 'Excel = "SampleFinDimWsReport"\Cell<CompanyName>'.</span></span>
47. <span data-ttu-id="6be75-215">Vælg 'model: Eksempelmodel for datamodellen Økonomiske dimensioner\Firma: Streng' i træet.</span><span class="sxs-lookup"><span data-stu-id="6be75-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
48. <span data-ttu-id="6be75-216">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6be75-216">Click Bind.</span></span>
49. <span data-ttu-id="6be75-217">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6be75-217">Click Save.</span></span>
50. <span data-ttu-id="6be75-218">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6be75-218">Close the page.</span></span>


