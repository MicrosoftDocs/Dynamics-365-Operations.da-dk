---
title: Redigere modeller og tilknytninger til at generere dokumenter, der har programdata
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 2 - Generere dokumenter)".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "361929"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="6e549-103">Redigere modeller og tilknytninger til at generere dokumenter, der har programdata</span><span class="sxs-lookup"><span data-stu-id="6e549-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e549-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 2: Generere dokumenter)".</span><span class="sxs-lookup"><span data-stu-id="6e549-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="6e549-105">I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="6e549-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="6e549-106">I denne procedure skal redigere du ER-konfigurationerne for at begynde at bruge dem til at generere elektroniske dokumenter og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="6e549-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="6e549-107">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="6e549-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="6e549-108">Disse trin kan udføres ved hjælp af DEMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="6e549-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="6e549-109">Rediger datamodel</span><span class="sxs-lookup"><span data-stu-id="6e549-109">Modify data model</span></span>
1. <span data-ttu-id="6e549-110">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6e549-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6e549-111">Vælg 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="6e549-112">Du skal udvide brugen af datamodellen.</span><span class="sxs-lookup"><span data-stu-id="6e549-112">You will extend how you use the data model.</span></span> <span data-ttu-id="6e549-113">Ud over at bruge den som datakilde for at generere Intrastat-rapporten, bruges datamodellen til at indsamle oplysninger om Intrastat-rapporteringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6e549-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="6e549-114">Oplysningerne bruges derefter til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="6e549-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="6e549-115">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="6e549-115">Click Designer.</span></span>
4. <span data-ttu-id="6e549-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="6e549-117">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="6e549-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="6e549-118">Skriv 'Til opdatering af programdata' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="6e549-119">Til opdatering af programdata</span><span class="sxs-lookup"><span data-stu-id="6e549-119">For application data update</span></span>  
7. <span data-ttu-id="6e549-120">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-120">Click Add.</span></span>
8. <span data-ttu-id="6e549-121">Vælg 'Til opdatering af programdata' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="6e549-122">Det nye rodelement tilføjes for at angive det dataflow, der skal bruges til at flytte data fra Intrastat-rapporten (brugt som datakilde) til programtabellerne (opdateringsdestinationen).</span><span class="sxs-lookup"><span data-stu-id="6e549-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="6e549-123">Bemærk, at de forskellige rodelementer skal bruges til at hente data, der bogføres i det udgående dokument, og til at hente data fra det dokument, der bruges til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="6e549-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="6e549-124">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6e549-125">Skriv 'Arkivoverskrift' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="6e549-126">Arkivoverskrift</span><span class="sxs-lookup"><span data-stu-id="6e549-126">Archive header</span></span>  
11. <span data-ttu-id="6e549-127">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="6e549-128">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-128">Click Add.</span></span>
    * <span data-ttu-id="6e549-129">Eftersom du skal oprette en post for hver Intrastat-rapport, der oprettes, skal du oprette et nyt element til den.</span><span class="sxs-lookup"><span data-stu-id="6e549-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="6e549-130">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="6e549-131">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="6e549-132">Filnavn</span><span class="sxs-lookup"><span data-stu-id="6e549-132">File name</span></span>  
15. <span data-ttu-id="6e549-133">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="6e549-134">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-134">Click Add.</span></span>
17. <span data-ttu-id="6e549-135">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="6e549-136">Skriv "Antal linjer" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="6e549-137">Antal linjer</span><span class="sxs-lookup"><span data-stu-id="6e549-137">Number of lines</span></span>  
19. <span data-ttu-id="6e549-138">Vælg "Heltal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="6e549-139">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-139">Click Add.</span></span>
    * <span data-ttu-id="6e549-140">Tilføj dette element for at repræsenterer antallet af Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="6e549-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="6e549-141">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="6e549-142">Skriv 'Arkivér linjer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="6e549-143">Arkivér linjer</span><span class="sxs-lookup"><span data-stu-id="6e549-143">Archive lines</span></span>  
23. <span data-ttu-id="6e549-144">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="6e549-145">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-145">Click Add.</span></span>
    * <span data-ttu-id="6e549-146">Tilføj dette element for at repræsenterer listen over Intrastat-posteringer, der rapporteres i den aktuelle rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="6e549-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="6e549-147">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="6e549-148">Skriv "Beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="6e549-149">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e549-149">Amount</span></span>  
27. <span data-ttu-id="6e549-150">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="6e549-151">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-151">Click Add.</span></span>
29. <span data-ttu-id="6e549-152">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="6e549-153">Skriv 'Varepost-id' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="6e549-154">Varepost-id</span><span class="sxs-lookup"><span data-stu-id="6e549-154">Commodity rec id</span></span>  
31. <span data-ttu-id="6e549-155">Vælg 'Int64' i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="6e549-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-156">Click Add.</span></span>
33. <span data-ttu-id="6e549-157">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="6e549-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="6e549-158">Skriv 'Varenummer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="6e549-159">varenummer</span><span class="sxs-lookup"><span data-stu-id="6e549-159">Item number</span></span>  
35. <span data-ttu-id="6e549-160">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="6e549-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="6e549-161">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-161">Click Add.</span></span>
37. <span data-ttu-id="6e549-162">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6e549-162">Click Save.</span></span>
38. <span data-ttu-id="6e549-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6e549-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="6e549-164">Rediger modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="6e549-164">Modify model mapping</span></span>
1. <span data-ttu-id="6e549-165">Udvid 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="6e549-166">Vælg 'Intrastat (model)\Intrastat (tilknytning)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="6e549-167">Rediger den eksisterende modeltilknytning for at begynde at bruge den til opdateringen af programdata og arkivere Intrastat-rapporteringsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="6e549-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="6e549-168">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="6e549-168">Click Designer.</span></span>
4. <span data-ttu-id="6e549-169">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6e549-169">Click New.</span></span>
5. <span data-ttu-id="6e549-170">Skriv 'Opdater arkiv' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="6e549-171">Opdater arkiv</span><span class="sxs-lookup"><span data-stu-id="6e549-171">Update archive</span></span>  
6. <span data-ttu-id="6e549-172">Vælg 'Til destination' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="6e549-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="6e549-173">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6e549-173">Click Save.</span></span>
    * <span data-ttu-id="6e549-174">Denne nye tilknytning angiver det dataflow, der skal bruges til at flytte data (Intrastat-rapporteringsdetaljer) fra datamodellen til programtabellerne (opdateringsdestinationen).</span><span class="sxs-lookup"><span data-stu-id="6e549-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="6e549-175">Bemærk, at en anden models rodelementer skal bruges til at hente data fra programmet til rapporteringsprocessen og derefter bruge dataene fra datamodellen til programdataopdateringen.</span><span class="sxs-lookup"><span data-stu-id="6e549-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="6e549-176">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="6e549-176">Click Designer.</span></span>
9. <span data-ttu-id="6e549-177">Vælg 'Datamodel\Datamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="6e549-178">Tilføj den krævede datakilde.</span><span class="sxs-lookup"><span data-stu-id="6e549-178">Add the required data source.</span></span> <span data-ttu-id="6e549-179">Dette er den datamodel, der indeholder oplysninger om de rapporterede Intrastat-transaktioner, der skal arkiveres.</span><span class="sxs-lookup"><span data-stu-id="6e549-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="6e549-180">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="6e549-180">Click Add root.</span></span>
11. <span data-ttu-id="6e549-181">Skriv 'model' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="6e549-182">model</span><span class="sxs-lookup"><span data-stu-id="6e549-182">model</span></span>  
12. <span data-ttu-id="6e549-183">Angiv eller vælg værdien 'Til opdatering af programdata' i feltet Definition.</span><span class="sxs-lookup"><span data-stu-id="6e549-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="6e549-184">Til opdatering af programdata</span><span class="sxs-lookup"><span data-stu-id="6e549-184">For application data update</span></span>  
13. <span data-ttu-id="6e549-185">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e549-185">Click OK.</span></span>
14. <span data-ttu-id="6e549-186">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="6e549-187">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="6e549-188">Vælg 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="6e549-189">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="6e549-189">Click Add.</span></span>
    * <span data-ttu-id="6e549-190">Datakilden skal tilføjes, fordi du skal optælle Intrastat-posteringer, der er rapporteret til arkivering.</span><span class="sxs-lookup"><span data-stu-id="6e549-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="6e549-191">Skriv 'Optalte linjer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="6e549-192">Optalte linjer</span><span class="sxs-lookup"><span data-stu-id="6e549-192">Enumerated lines</span></span>  
19. <span data-ttu-id="6e549-193">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="6e549-193">Click Edit formula.</span></span>
20. <span data-ttu-id="6e549-194">Vælg 'Liste\ENUMERATE' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="6e549-195">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="6e549-195">Click Add function.</span></span>
22. <span data-ttu-id="6e549-196">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="6e549-197">Udvid 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="6e549-198">Vælg 'model\Arkivér overskrift\Arkivér linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="6e549-199">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="6e549-199">Click Add data source.</span></span>
26. <span data-ttu-id="6e549-200">Angiv 'ENUMERATE(model.'Arkivér overskrift.'Arkivér linjer)' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="6e549-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="6e549-201">ENUMERATE(model. 'Arkivoverskrift'.' Arkivér linjer)</span><span class="sxs-lookup"><span data-stu-id="6e549-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="6e549-202">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6e549-202">Click Save.</span></span>
28. <span data-ttu-id="6e549-203">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6e549-203">Close the page.</span></span>
29. <span data-ttu-id="6e549-204">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e549-204">Click OK.</span></span>
30. <span data-ttu-id="6e549-205">Klik på Tilføj destination.</span><span class="sxs-lookup"><span data-stu-id="6e549-205">Click Add destination.</span></span>
    * <span data-ttu-id="6e549-206">Tilføj programtabeller som krævede destinationer, der skal opdateres for at arkivere oplysninger om rapporterede Intrastat-transaktioner.</span><span class="sxs-lookup"><span data-stu-id="6e549-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="6e549-207">Skriv 'Arkiv' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6e549-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="6e549-208">Arkivér</span><span class="sxs-lookup"><span data-stu-id="6e549-208">Archive</span></span>  
32. <span data-ttu-id="6e549-209">Gå til feltet Tabelnavn, og skriv 'IntrastatArchiveGeneral'.</span><span class="sxs-lookup"><span data-stu-id="6e549-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="6e549-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="6e549-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="6e549-211">Behold posthandlingen "Indsæt", så du kan tilføje poster under arkiveringen af detaljer for hver Intrastat-rapporteringsproces.</span><span class="sxs-lookup"><span data-stu-id="6e549-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="6e549-212">Vælg Ja i feltet Postinfolog.</span><span class="sxs-lookup"><span data-stu-id="6e549-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="6e549-213">Vælg Ja for at få oplysninger om problemer med programdataopdateringen.</span><span class="sxs-lookup"><span data-stu-id="6e549-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="6e549-214">Vælg Ja i feltet Undlad validering af posthandling.</span><span class="sxs-lookup"><span data-stu-id="6e549-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="6e549-215">Vælg Ja for at forhindre valideringsfejl for det tomme felt 'Id for Intrastat-arkiv'.</span><span class="sxs-lookup"><span data-stu-id="6e549-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="6e549-216">Dette sker, når der er tilføjet poster, baseret på rækkefølgen af talindstillinger, der er konfigureret for denne tabel i formularen Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="6e549-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="6e549-217">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e549-217">Click OK.</span></span>
    * <span data-ttu-id="6e549-218">Bind elementer i den tilføjede datakilde (den filtrerede model, der er baseret på det valgte rodelement) til elementer fra den tilføjede destination.</span><span class="sxs-lookup"><span data-stu-id="6e549-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="6e549-219">Udvid 'Arkivér' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="6e549-220">Udvid 'Arkivér\<Relationer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="6e549-221">Udvid 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="6e549-222">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Beløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="6e549-223">Udvid 'model\Arkivér overskrift\Optalte linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="6e549-224">Udvid 'model\Arkivér overskrift\Optalte linjer\Værdi' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="6e549-225">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="6e549-226">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-226">Click Bind.</span></span>
44. <span data-ttu-id="6e549-227">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Vare(IntrastatCommodity)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="6e549-228">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varepost-id' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="6e549-229">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-229">Click Bind.</span></span>
47. <span data-ttu-id="6e549-230">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Varenummer(ItemId)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="6e549-231">Vælg 'model\Arkivér overskrift\Optalte linjer\Værdi\Varenummer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="6e549-232">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-232">Click Bind.</span></span>
50. <span data-ttu-id="6e549-233">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail\Linjenummer(LineNumber)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="6e549-234">Vælg 'model\Arkivér overskrift\Optalte linjer\Nummer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="6e549-235">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-235">Click Bind.</span></span>
53. <span data-ttu-id="6e549-236">Vælg 'Arkivér\<Relationer\IntrastatArchiveDetail' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="6e549-237">Vælg 'model\Arkivér overskrift\Optalte linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="6e549-238">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-238">Click Bind.</span></span>
56. <span data-ttu-id="6e549-239">Vælg 'Arkivér\Filnavn(FileName)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="6e549-240">Vælg 'model\Arkivér overskrift\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="6e549-241">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-241">Click Bind.</span></span>
59. <span data-ttu-id="6e549-242">Vælg 'Arkivér\Antal linjer(NumberOfLines)' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="6e549-243">Vælg 'model\Arkivér overskrift\Antal linjer' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="6e549-244">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-244">Click Bind.</span></span>
62. <span data-ttu-id="6e549-245">Vælg 'Arkivér' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="6e549-246">Vælg 'model\Arkivér overskrift' i træet.</span><span class="sxs-lookup"><span data-stu-id="6e549-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="6e549-247">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="6e549-247">Click Bind.</span></span>
65. <span data-ttu-id="6e549-248">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6e549-248">Click Save.</span></span>
66. <span data-ttu-id="6e549-249">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6e549-249">Close the page.</span></span>
67. <span data-ttu-id="6e549-250">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6e549-250">Close the page.</span></span>

