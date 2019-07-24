---
title: Få adgang til programmetadata ved hjælp af ER-konfiguration
description: Fremgangsmåden i dette emne forklarer, hvordan en Regulatory Configuration Service-bruger kan designe en ny elektronisk rapporteringsmodel (ER) ved hjælp af metadataene i Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727023"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="dc205-103">Få adgang til programmetadata ved hjælp af ER-konfiguration</span><span class="sxs-lookup"><span data-stu-id="dc205-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc205-104">Følgende trin beskriver, hvordan en Regulatory Configuration Service-bruger i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe en ny ER-modeltilknytning ved hjælp af metadataene i Dynamics 365 for Finance and Operations-applikationen.</span><span class="sxs-lookup"><span data-stu-id="dc205-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the metadata of the Dynamics 365 for Finance and Operations application.</span></span> <span data-ttu-id="dc205-105">Der opnås adgang til programmetadata ved hjælp af en ER-metadatakonfiguration, der indeholder et eksempel sæt af metadata for adgang til udenrigshandelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="dc205-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="dc205-106">Du skal først fuldføre RCS-trinnene i procedureemnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dc205-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="dc205-107">Derefter skal du i Finance and Operations udføre trinnene i emnet [(ER) Klargøre programmetadata, der skal bruges i RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="dc205-107">Then, in Finance and Operations, complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc205-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="dc205-108">Prerequisites</span></span>
1. <span data-ttu-id="dc205-109">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="dc205-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="dc205-110">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="dc205-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="dc205-111">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="dc205-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="dc205-112">Importere konfiguration af metadata</span><span class="sxs-lookup"><span data-stu-id="dc205-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="dc205-113">Klik på **Konfiguration af metadata**.</span><span class="sxs-lookup"><span data-stu-id="dc205-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="dc205-114">Importér den ER-metadatakonfiguration, der indeholder metadata fra det Finance and Operations-program, der er konfigureret til at generere elektroniske dokumenter for udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="dc205-114">Import the ER metadata configuration that contains metadata from the Finance and Operations application that is configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="dc205-115">Denne ER-konfiguration af metadata er blevet eksporteret som en XML-fil, mens trinnene i [(ER) Klargøre programmetadata, der skal bruges i RCS](prepare-application-metadata-rcs.md) blev fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc205-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="dc205-116">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="dc205-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="dc205-117">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="dc205-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="dc205-118">Klik på **Gennemse**, og vælg filen 'Udenrigshandelmetadata.xml'.</span><span class="sxs-lookup"><span data-stu-id="dc205-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="dc205-119">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc205-119">Click **OK**.</span></span> 
7. <span data-ttu-id="dc205-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc205-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="dc205-121">Oprette datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc205-121">Create data model configuration</span></span>
1. <span data-ttu-id="dc205-122">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="dc205-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="dc205-123">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc205-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="dc205-124">Skriv 'Udenrigshandelmodel' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="dc205-125">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="dc205-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="dc205-126">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dc205-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="dc205-127">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc205-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="dc205-128">Skriv "Rod" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="dc205-129">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dc205-129">Click **Add**.</span></span> 
9. <span data-ttu-id="dc205-130">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc205-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="dc205-131">Skriv 'Transaktion' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="dc205-132">Vælg **Liste over poster** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="dc205-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="dc205-133">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dc205-133">Click **Add**.</span></span> 
13. <span data-ttu-id="dc205-134">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc205-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="dc205-135">Skriv 'Varekode' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="dc205-136">Vælg **Streng** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="dc205-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="dc205-137">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dc205-137">Click **Add**.</span></span> 
17. <span data-ttu-id="dc205-138">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc205-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="dc205-139">Skriv 'Faktureret beløb' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="dc205-140">Vælg **Kommatal** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="dc205-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="dc205-141">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dc205-141">Click **Add**.</span></span> 
21. <span data-ttu-id="dc205-142">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc205-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="dc205-143">Skriv 'Dato' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="dc205-144">Vælg **Dato** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="dc205-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="dc205-145">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="dc205-145">Click **Add**.</span></span> 
25. <span data-ttu-id="dc205-146">Klik på **Rodreference**.</span><span class="sxs-lookup"><span data-stu-id="dc205-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="dc205-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc205-147">Click **OK**.</span></span> 
27. <span data-ttu-id="dc205-148">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc205-148">Click **Save**.</span></span> 
28. <span data-ttu-id="dc205-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc205-149">Close the page.</span></span> 
29. <span data-ttu-id="dc205-150">Klik på **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="dc205-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="dc205-151">Klik på **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="dc205-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="dc205-152">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc205-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="dc205-153">Oprette konfiguration af modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="dc205-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="dc205-154">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc205-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="dc205-155">Angiv 'Modeltilknytning baseret på datamodellen Udenrigshandelmodel' i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dc205-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="dc205-156">Skriv 'Tilknytning af udenrigshandel' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="dc205-157">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="dc205-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="dc205-158">Udvid sektionen **Forudsætninger**.</span><span class="sxs-lookup"><span data-stu-id="dc205-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="dc205-159">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="dc205-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="dc205-160">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dc205-160">Click **New**.</span></span> 
8. <span data-ttu-id="dc205-161">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dc205-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="dc205-162">Vælg **Konfiguration** i feltet **Type af forudsætningskomponent**.</span><span class="sxs-lookup"><span data-stu-id="dc205-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="dc205-163">Vælg konfiguration **Udenrigshandelmetadata**.</span><span class="sxs-lookup"><span data-stu-id="dc205-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="dc205-164">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc205-164">Click **Save**.</span></span> 
12. <span data-ttu-id="dc205-165">Vi har tilføjet referencen til version 1 af konfigurationen af 'Udenrigshandelmetadata'.</span><span class="sxs-lookup"><span data-stu-id="dc205-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="dc205-166">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="dc205-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="dc205-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc205-167">Close the page.</span></span> 
14. <span data-ttu-id="dc205-168">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dc205-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="dc205-169">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="dc205-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="dc205-170">Vælg **Dynamics 365 for Operations\Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="dc205-171">Klik på **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="dc205-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="dc205-172">Skriv 'Intrastat' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="dc205-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="dc205-173">Vælg **Intrastat** -tabelposter.</span><span class="sxs-lookup"><span data-stu-id="dc205-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="dc205-174">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc205-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc205-175">De eneste to tabeller blev tilbudt, da der kun blev føjet to tabeller til det sæt metadata, der bruges i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="dc205-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="dc205-176">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dc205-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="dc205-177">Udvid **Intrastat** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="dc205-178">Vælg **Intrastat\AmountMST** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="dc205-179">Udvid **Transaktion = Intrastat** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="dc205-180">Vælg **Transaktion = Intrastat\Faktureret beløb** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="dc205-181">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dc205-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="dc205-182">Vælg **Intrastat\TransDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="dc205-183">Vælg **Transaktion = Intrastat\Dato** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="dc205-184">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dc205-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="dc205-185">Udvid **Intrastat\>Relationer** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="dc205-186">Udvid **Intrastat\>Relationer\IntrastatCommodity** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="dc205-187">Vælg **Intrastat\>Relationer\IntrastatCommodity\Kode** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="dc205-188">Vælg **Transaktion = Intrastat\Varekode** i træet.</span><span class="sxs-lookup"><span data-stu-id="dc205-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="dc205-189">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="dc205-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="dc205-190">Klik på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="dc205-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc205-191">Vi har bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om programmetadata fra den ER-metadatakonfiguration, der henvises til.</span><span class="sxs-lookup"><span data-stu-id="dc205-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="dc205-192">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dc205-192">Click **Save**.</span></span> 
37. <span data-ttu-id="dc205-193">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc205-193">Close the page.</span></span> 
38. <span data-ttu-id="dc205-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc205-194">Close the page.</span></span> 
39. <span data-ttu-id="dc205-195">Når du har brug for at udvide det eksisterende sæt metadata, kan du gøre det i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dc205-195">When you need to extend the existing set of metadata, you can do it in Finance and Operations.</span></span> <span data-ttu-id="dc205-196">Du kan derefter eksportere den nye fuldførte version af ER-metadatakonfigurationen fra Finance and Operations, importere den til RCS og opdatere forudsætningerne for den konfigurerede konfiguration af modeltilknytning, der henviser til en ny version af importeret metadatakonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc205-196">Then you can export the new completed version of ER metadata configuration from Finance and Operation,s import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc205-197">Denne indlæsning af oplysninger om programmetadata er den eneste, der er tilgængelig for lokalt installerede programmer (når der bruges lokale virksomhedsdata (LBD) eller en lokal installationsmodel for Dynamics 365 for Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="dc205-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used for Dynamics 365 for Finance and Operations).</span></span>
        
