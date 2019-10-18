---
title: Overføre ER-konfiguration til Lifecycle Services
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration af elektronisk rapportering (ER) og overføre den til Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 980ce00ae702ea0a3394efa15419e0f7b7dc2530
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182203"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="82a90-103">Overføre ER-konfiguration til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="82a90-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82a90-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny konfiguration af elektronisk rapportering (ER) og overføre den til Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="82a90-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="82a90-105">I dette eksempel skal du oprette en konfiguration og overføre den til LCS for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="82a90-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="82a90-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="82a90-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="82a90-107">Adgang til LCS er også nødvendig for at udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="82a90-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="82a90-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="82a90-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="82a90-109">Vælg "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="82a90-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="82a90-110">og indstil det som aktivt.</span><span class="sxs-lookup"><span data-stu-id="82a90-110">and set it as active.</span></span>
3. <span data-ttu-id="82a90-111">Klik på Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="82a90-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="82a90-112">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="82a90-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="82a90-113">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="82a90-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="82a90-114">Du skal oprette en konfiguration, der indeholder en eksempeldatamodel for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="82a90-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="82a90-115">Denne datakonfigurationsmodel overføres senere til LCS.</span><span class="sxs-lookup"><span data-stu-id="82a90-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="82a90-116">Skriv 'Eksempelmodelkonfiguration' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82a90-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="82a90-117">Eksempemodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="82a90-117">Sample model configuration</span></span>  
3. <span data-ttu-id="82a90-118">Skriv 'Eksempelmodelkonfiguration' i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="82a90-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="82a90-119">Eksempemodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="82a90-119">Sample model configuration</span></span>  
4. <span data-ttu-id="82a90-120">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="82a90-120">Click Create configuration.</span></span>
5. <span data-ttu-id="82a90-121">Klik på Modeldesigner.</span><span class="sxs-lookup"><span data-stu-id="82a90-121">Click Model designer.</span></span>
6. <span data-ttu-id="82a90-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="82a90-122">Click New.</span></span>
7. <span data-ttu-id="82a90-123">Skriv 'Indgangspunkt' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82a90-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="82a90-124">Indgangspunkt</span><span class="sxs-lookup"><span data-stu-id="82a90-124">Entry point</span></span>  
8. <span data-ttu-id="82a90-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="82a90-125">Click Add.</span></span>
9. <span data-ttu-id="82a90-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="82a90-126">Click Save.</span></span>
10. <span data-ttu-id="82a90-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="82a90-127">Close the page.</span></span>
11. <span data-ttu-id="82a90-128">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="82a90-128">Click Change status.</span></span>
12. <span data-ttu-id="82a90-129">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="82a90-129">Click Complete.</span></span>
13. <span data-ttu-id="82a90-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="82a90-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="82a90-131">Registrere et nyt lager</span><span class="sxs-lookup"><span data-stu-id="82a90-131">Register a new  repository</span></span>
1. <span data-ttu-id="82a90-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="82a90-132">Close the page.</span></span>
2. <span data-ttu-id="82a90-133">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="82a90-133">Click Repositories.</span></span>
    * <span data-ttu-id="82a90-134">Dette gør det muligt at åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="82a90-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="82a90-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="82a90-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="82a90-136">Her kan du tilføje et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="82a90-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="82a90-137">Vælg LCS i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="82a90-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="82a90-138">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="82a90-138">Click Create repository.</span></span>
6. <span data-ttu-id="82a90-139">Indtast eller vælg en værdi i feltet Projekt.</span><span class="sxs-lookup"><span data-stu-id="82a90-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="82a90-140">Vælg det ønskede LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="82a90-140">Select the desired LCS project.</span></span> <span data-ttu-id="82a90-141">Du skal have adgang til projektet.</span><span class="sxs-lookup"><span data-stu-id="82a90-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="82a90-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="82a90-142">Click OK.</span></span>
    * <span data-ttu-id="82a90-143">Udfyld en ny lagerpost.</span><span class="sxs-lookup"><span data-stu-id="82a90-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="82a90-144">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="82a90-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="82a90-145">Vælg LCS-lagerposten.</span><span class="sxs-lookup"><span data-stu-id="82a90-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="82a90-146">Bemærk, at et registreret lager er markeret af den aktuelle udbyder, dvs. at de eneste konfigurationer, der ejes af den pågældende udbyder, kan placeres på dette lager og derfor overføres til det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="82a90-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="82a90-147">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="82a90-147">Click Open.</span></span>
    * <span data-ttu-id="82a90-148">Åbn lageret for at få vist listen over ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="82a90-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="82a90-149">Den vil være tom, hvis dette projekt endnu ikke er blevet brugt til deling af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="82a90-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="82a90-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="82a90-150">Close the page.</span></span>
11. <span data-ttu-id="82a90-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="82a90-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="82a90-152">Overføre konfiguration til LCS</span><span class="sxs-lookup"><span data-stu-id="82a90-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="82a90-153">Klik på Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="82a90-153">Click Configurations.</span></span>
2. <span data-ttu-id="82a90-154">Vælg 'Eksempelmodelkonfiguration' i træet.</span><span class="sxs-lookup"><span data-stu-id="82a90-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="82a90-155">Vælg en oprettet konfiguration, der allerede er fuldført.</span><span class="sxs-lookup"><span data-stu-id="82a90-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="82a90-156">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="82a90-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="82a90-157">Vælg versionen af den valgte konfiguration med statussen 'Fuldført'.</span><span class="sxs-lookup"><span data-stu-id="82a90-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="82a90-158">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="82a90-158">Click Change status.</span></span>
5. <span data-ttu-id="82a90-159">Klik på Del.</span><span class="sxs-lookup"><span data-stu-id="82a90-159">Click Share.</span></span>
    * <span data-ttu-id="82a90-160">Konfigurationens status ændres fra 'Fuldført' til 'Delt', når den er udgivet i LCS.</span><span class="sxs-lookup"><span data-stu-id="82a90-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="82a90-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="82a90-161">Click OK.</span></span>
7. <span data-ttu-id="82a90-162">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="82a90-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="82a90-163">Vælg konfigurationsversionen 'med statussen 'Delt'.</span><span class="sxs-lookup"><span data-stu-id="82a90-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="82a90-164">Bemærk, at statussen for den valgte version er ændret fra 'Fuldført' til 'Delt'.</span><span class="sxs-lookup"><span data-stu-id="82a90-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="82a90-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="82a90-165">Close the page.</span></span>
9. <span data-ttu-id="82a90-166">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="82a90-166">Click Repositories.</span></span>
    * <span data-ttu-id="82a90-167">Dette gør det muligt at åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="82a90-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="82a90-168">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="82a90-168">Click Open.</span></span>
    * <span data-ttu-id="82a90-169">Vælg LCS-lageret, og åbn det.</span><span class="sxs-lookup"><span data-stu-id="82a90-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="82a90-170">Bemærk, at den valgte konfiguration vises som et aktiv for det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="82a90-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="82a90-171">Åbne LCS ved hjælp af https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="82a90-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="82a90-172">Åbn et projekt, der tidligere blev brugt til registrering af lageret, åbn 'Aktivbibliotek' for dette projekt, og udvid indholdet af aktivtypen 'GER-konfiguration' – den overførte ER-konfiguration vil være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="82a90-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="82a90-173">Bemærk, at den uploadede LCS-konfiguration kan importeres til en anden forekomst, hvis udbyderne har adgang til dette LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="82a90-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

