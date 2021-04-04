---
title: Redigere modeller og tilknytninger til at generere dokumenter, der har programdata
description: I dette emne forklares det, hvordan du designer konfigurationer af rapportering for at generere et elektronisk dokument og opdatere programdata. (Del 2 – Generere dokumenter).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567086"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="e4a21-104">Redigere modeller og tilknytninger til at generere dokumenter, der har programdata</span><span class="sxs-lookup"><span data-stu-id="e4a21-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4a21-105">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 2: Generere dokumenter)".</span><span class="sxs-lookup"><span data-stu-id="e4a21-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="e4a21-106">I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="e4a21-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="e4a21-107">I denne procedure skal redigere du ER-konfigurationerne for at begynde at bruge dem til at generere elektroniske dokumenter og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="e4a21-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="e4a21-108">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="e4a21-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e4a21-109">Disse trin kan udføres ved hjælp af DEMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="e4a21-110">Rediger datamodel</span><span class="sxs-lookup"><span data-stu-id="e4a21-110">Modify data model</span></span>
1. <span data-ttu-id="e4a21-111">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e4a21-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e4a21-112">Vælg 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="e4a21-113">Du skal udvide brugen af datamodellen.</span><span class="sxs-lookup"><span data-stu-id="e4a21-113">You will extend how you use the data model.</span></span> <span data-ttu-id="e4a21-114">Ud over at bruge den som datakilde for at generere Intrastat-rapporten, bruges datamodellen til at indsamle oplysninger om Intrastat-rapporteringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="e4a21-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="e4a21-115">Oplysningerne bruges derefter til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="e4a21-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="e4a21-116">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="e4a21-116">Click Designer.</span></span>
4. <span data-ttu-id="e4a21-117">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e4a21-118">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="e4a21-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="e4a21-119">Skriv 'Til opdatering af programdata' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="e4a21-120">Til opdatering af programdata</span><span class="sxs-lookup"><span data-stu-id="e4a21-120">For application data update</span></span>  
7. <span data-ttu-id="e4a21-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-121">Click Add.</span></span>
8. <span data-ttu-id="e4a21-122">Vælg 'Til opdatering af programdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="e4a21-123">Det nye rodelement tilføjes for at angive det dataflow, der skal bruges til at flytte data fra Intrastat-rapporten (brugt som datakilde) til programtabellerne (opdateringsdestinationen).</span><span class="sxs-lookup"><span data-stu-id="e4a21-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="e4a21-124">Bemærk, at de forskellige rodelementer skal bruges til at hente data, der bogføres i det udgående dokument, og til at hente data fra det dokument, der bruges til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="e4a21-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="e4a21-125">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="e4a21-126">Skriv 'Arkivoverskrift' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="e4a21-127">Arkivoverskrift</span><span class="sxs-lookup"><span data-stu-id="e4a21-127">Archive header</span></span>  
11. <span data-ttu-id="e4a21-128">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="e4a21-129">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-129">Click Add.</span></span>
    * <span data-ttu-id="e4a21-130">Eftersom du skal oprette en post for hver Intrastat-rapport, der oprettes, skal du oprette et nyt element til den.</span><span class="sxs-lookup"><span data-stu-id="e4a21-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="e4a21-131">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e4a21-132">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e4a21-133">Filnavn</span><span class="sxs-lookup"><span data-stu-id="e4a21-133">File name</span></span>  
15. <span data-ttu-id="e4a21-134">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="e4a21-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-135">Click Add.</span></span>
17. <span data-ttu-id="e4a21-136">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e4a21-137">Skriv "Antal linjer" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="e4a21-138">Antal linjer</span><span class="sxs-lookup"><span data-stu-id="e4a21-138">Number of lines</span></span>  
19. <span data-ttu-id="e4a21-139">Vælg "Heltal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="e4a21-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-140">Click Add.</span></span>
    * <span data-ttu-id="e4a21-141">Tilføj dette element for at repræsenterer antallet af Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="e4a21-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="e4a21-142">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e4a21-143">Skriv 'Arkivér linjer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="e4a21-144">Arkivér linjer</span><span class="sxs-lookup"><span data-stu-id="e4a21-144">Archive lines</span></span>  
23. <span data-ttu-id="e4a21-145">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="e4a21-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-146">Click Add.</span></span>
    * <span data-ttu-id="e4a21-147">Tilføj dette element for at repræsenterer listen over Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="e4a21-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="e4a21-148">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e4a21-149">Skriv "Beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="e4a21-150">Beløb</span><span class="sxs-lookup"><span data-stu-id="e4a21-150">Amount</span></span>  
27. <span data-ttu-id="e4a21-151">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="e4a21-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-152">Click Add.</span></span>
29. <span data-ttu-id="e4a21-153">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e4a21-154">Skriv 'Varepost-id' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="e4a21-155">Varepost-id</span><span class="sxs-lookup"><span data-stu-id="e4a21-155">Commodity rec id</span></span>  
31. <span data-ttu-id="e4a21-156">Vælg 'Int64' i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="e4a21-157">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-157">Click Add.</span></span>
33. <span data-ttu-id="e4a21-158">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="e4a21-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e4a21-159">Skriv 'Varenummer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="e4a21-160">varenummer</span><span class="sxs-lookup"><span data-stu-id="e4a21-160">Item number</span></span>  
35. <span data-ttu-id="e4a21-161">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="e4a21-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="e4a21-162">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-162">Click Add.</span></span>
37. <span data-ttu-id="e4a21-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4a21-163">Click Save.</span></span>
38. <span data-ttu-id="e4a21-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e4a21-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="e4a21-165">Rediger modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="e4a21-165">Modify model mapping</span></span>
1. <span data-ttu-id="e4a21-166">Udvid 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="e4a21-167">Vælg 'Intrastat (model)\Intrastat (tilknytning)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="e4a21-168">Rediger den eksisterende modeltilknytning for at begynde at bruge den til opdateringen af programdata og arkivere Intrastat-rapporteringsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="e4a21-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="e4a21-169">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="e4a21-169">Click Designer.</span></span>
4. <span data-ttu-id="e4a21-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e4a21-170">Click New.</span></span>
5. <span data-ttu-id="e4a21-171">Skriv 'Opdater arkiv' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="e4a21-172">Opdater arkiv</span><span class="sxs-lookup"><span data-stu-id="e4a21-172">Update archive</span></span>  
6. <span data-ttu-id="e4a21-173">Vælg 'Til destination' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="e4a21-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="e4a21-174">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4a21-174">Click Save.</span></span>
    * <span data-ttu-id="e4a21-175">Denne nye tilknytning angiver det dataflow, der skal bruges til at flytte data (Intrastat-rapporteringsdetaljer) fra datamodellen til programtabellerne (opdateringsdestinationen).</span><span class="sxs-lookup"><span data-stu-id="e4a21-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="e4a21-176">Bemærk, at en anden models rodelementer skal bruges til at hente data fra programmet til rapporteringsprocessen og derefter bruge dataene fra datamodellen til programdataopdateringen.</span><span class="sxs-lookup"><span data-stu-id="e4a21-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="e4a21-177">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="e4a21-177">Click Designer.</span></span>
9. <span data-ttu-id="e4a21-178">Vælg 'Datamodel\Datamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="e4a21-179">Tilføj den krævede datakilde.</span><span class="sxs-lookup"><span data-stu-id="e4a21-179">Add the required data source.</span></span> <span data-ttu-id="e4a21-180">Dette er den datamodel, der indeholder oplysninger om de rapporterede Intrastat-transaktioner, der skal arkiveres.</span><span class="sxs-lookup"><span data-stu-id="e4a21-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="e4a21-181">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="e4a21-181">Click Add root.</span></span>
11. <span data-ttu-id="e4a21-182">Skriv 'model' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="e4a21-183">model</span><span class="sxs-lookup"><span data-stu-id="e4a21-183">model</span></span>  
12. <span data-ttu-id="e4a21-184">Angiv eller vælg værdien 'Til opdatering af programdata' i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="e4a21-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="e4a21-185">Til opdatering af programdata</span><span class="sxs-lookup"><span data-stu-id="e4a21-185">For application data update</span></span>  
13. <span data-ttu-id="e4a21-186">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e4a21-186">Click OK.</span></span>
14. <span data-ttu-id="e4a21-187">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="e4a21-188">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="e4a21-189">Vælg 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="e4a21-190">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="e4a21-190">Click Add.</span></span>
    * <span data-ttu-id="e4a21-191">Datakilden skal tilføjes, fordi du skal optælle Intrastat-posteringer, der er rapporteret til arkivering.</span><span class="sxs-lookup"><span data-stu-id="e4a21-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="e4a21-192">Skriv 'Optalte linjer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="e4a21-193">Optalte linjer</span><span class="sxs-lookup"><span data-stu-id="e4a21-193">Enumerated lines</span></span>  
19. <span data-ttu-id="e4a21-194">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="e4a21-194">Click Edit formula.</span></span>
20. <span data-ttu-id="e4a21-195">Vælg 'Liste\ENUMERATE' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="e4a21-196">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="e4a21-196">Click Add function.</span></span>
22. <span data-ttu-id="e4a21-197">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="e4a21-198">Udvid 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="e4a21-199">Vælg 'model\Arkivér overskrift\Arkivér linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="e4a21-200">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e4a21-200">Click Add data source.</span></span>
26. <span data-ttu-id="e4a21-201">Angiv 'ENUMERATE(model.'Arkivér overskrift.'Arkivér linjer)' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e4a21-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="e4a21-202">ENUMERATE(model. 'Arkivoverskrift'.' Arkivér linjer)</span><span class="sxs-lookup"><span data-stu-id="e4a21-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="e4a21-203">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4a21-203">Click Save.</span></span>
28. <span data-ttu-id="e4a21-204">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e4a21-204">Close the page.</span></span>
29. <span data-ttu-id="e4a21-205">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e4a21-205">Click OK.</span></span>
30. <span data-ttu-id="e4a21-206">Klik på Tilføj destination.</span><span class="sxs-lookup"><span data-stu-id="e4a21-206">Click Add destination.</span></span>
    * <span data-ttu-id="e4a21-207">Tilføj programtabeller som krævede destinationer, der skal opdateres for at arkivere oplysninger om rapporterede Intrastat-transaktioner.</span><span class="sxs-lookup"><span data-stu-id="e4a21-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="e4a21-208">Skriv 'Arkiv' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e4a21-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="e4a21-209">Arkivér</span><span class="sxs-lookup"><span data-stu-id="e4a21-209">Archive</span></span>  
32. <span data-ttu-id="e4a21-210">Gå til feltet Tabelnavn, og skriv 'IntrastatArchiveGeneral'.</span><span class="sxs-lookup"><span data-stu-id="e4a21-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="e4a21-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="e4a21-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="e4a21-212">Behold posthandlingen "Indsæt", så du kan tilføje poster under arkiveringen af detaljer for hver Intrastat-rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="e4a21-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="e4a21-213">Vælg Ja i feltet Postinfolog.</span><span class="sxs-lookup"><span data-stu-id="e4a21-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="e4a21-214">Vælg Ja for at få oplysninger om problemer med programdataopdateringen.</span><span class="sxs-lookup"><span data-stu-id="e4a21-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="e4a21-215">Vælg Ja i feltet Undlad validering af posthandling.</span><span class="sxs-lookup"><span data-stu-id="e4a21-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="e4a21-216">Vælg Ja for at forhindre valideringsfejl for det tomme felt 'Id for Intrastat-arkiv'.</span><span class="sxs-lookup"><span data-stu-id="e4a21-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="e4a21-217">Dette sker, når der er tilføjet poster, baseret på rækkefølgen af talindstillinger, der er konfigureret for denne tabel i formularen Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="e4a21-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="e4a21-218">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e4a21-218">Click OK.</span></span>
    * <span data-ttu-id="e4a21-219">Bind elementer i den tilføjede datakilde (den filtrerede model, der er baseret på det valgte rodelement) til elementer fra den tilføjede destination.</span><span class="sxs-lookup"><span data-stu-id="e4a21-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="e4a21-220">Udvid 'Arkivér' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="e4a21-221">Udvid 'Arkivér\<Relationer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="e4a21-222">Udvid 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="e4a21-223">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Beløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="e4a21-224">Udvid 'model\Arkivér overskrift\Optalte linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="e4a21-225">Udvid 'model\Arkivér overskrift\Optalte linjer\Værdi' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="e4a21-226">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="e4a21-227">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-227">Click Bind.</span></span>
44. <span data-ttu-id="e4a21-228">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Vare(IntrastatCommodity)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="e4a21-229">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varepost-id' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="e4a21-230">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-230">Click Bind.</span></span>
47. <span data-ttu-id="e4a21-231">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Varenummer(ItemId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="e4a21-232">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varenummer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="e4a21-233">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-233">Click Bind.</span></span>
50. <span data-ttu-id="e4a21-234">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Linjenummer(LineNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="e4a21-235">Vælg 'model\Arkivér overskrift\Optalte linjer\Nummer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="e4a21-236">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-236">Click Bind.</span></span>
53. <span data-ttu-id="e4a21-237">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="e4a21-238">Vælg 'model\Arkivér overskrift\Optalte linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="e4a21-239">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-239">Click Bind.</span></span>
56. <span data-ttu-id="e4a21-240">Vælg 'Arkivér\Filnavn(FileName)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="e4a21-241">Vælg 'model\Arkivér overskrift\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="e4a21-242">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-242">Click Bind.</span></span>
59. <span data-ttu-id="e4a21-243">Vælg 'Arkivér\Antal linjer(NumberOfLines)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="e4a21-244">Vælg 'model\Arkivér overskrift\Antal linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="e4a21-245">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-245">Click Bind.</span></span>
62. <span data-ttu-id="e4a21-246">Vælg 'Arkivér' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="e4a21-247">Vælg 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="e4a21-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="e4a21-248">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="e4a21-248">Click Bind.</span></span>
65. <span data-ttu-id="e4a21-249">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e4a21-249">Click Save.</span></span>
66. <span data-ttu-id="e4a21-250">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e4a21-250">Close the page.</span></span>
67. <span data-ttu-id="e4a21-251">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e4a21-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]