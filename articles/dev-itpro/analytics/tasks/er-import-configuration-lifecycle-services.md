---
title: Importere ER-konfiguration fra Lifecycle Services
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551316"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="1ea79-103">Importere ER-konfiguration fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="1ea79-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ea79-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1ea79-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="1ea79-105">I dette eksempel skal du vælge den ønskede version af ER-konfigurationen og importere den til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, fordi ER-konfigurationer deles af firmaer.</span><span class="sxs-lookup"><span data-stu-id="1ea79-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="1ea79-106">For at fuldføre disse trin, skal du først fuldføre trinnene i proceduren "Overføre en ER-konfiguration til Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="1ea79-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="1ea79-107">Adgang til LCS er også nødvendig for at udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="1ea79-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="1ea79-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="1ea79-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1ea79-109">Klik på Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1ea79-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="1ea79-110">Slette en delt version af datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="1ea79-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="1ea79-111">Vælg 'Eksempelmodelkonfiguration' i træet.</span><span class="sxs-lookup"><span data-stu-id="1ea79-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="1ea79-112">Den første version af en eksempeldatamodelkonfiguration, der er oprettet og udgivet til LCS under proceduren "Overføre en ER-konfiguration til Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="1ea79-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="1ea79-113">I denne procedure vil du slette denne version af ER-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="1ea79-114">Denne version af en eksempeldatamodelkonfiguration importeres senere fra LCS.</span><span class="sxs-lookup"><span data-stu-id="1ea79-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="1ea79-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ea79-116">Vælg den konfigurationsversion, der har statussen 'Delt'.</span><span class="sxs-lookup"><span data-stu-id="1ea79-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="1ea79-117">Denne status angiver, at konfigurationen er blevet publiceret til LCS.</span><span class="sxs-lookup"><span data-stu-id="1ea79-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="1ea79-118">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="1ea79-118">Click Change status.</span></span>
4. <span data-ttu-id="1ea79-119">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="1ea79-119">Click Discontinue.</span></span>
    * <span data-ttu-id="1ea79-120">Skift status for den valgte version fra 'Delt' til 'Annulleret' for at gøre den tilgængelig for sletning.</span><span class="sxs-lookup"><span data-stu-id="1ea79-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="1ea79-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1ea79-121">Click OK.</span></span>
6. <span data-ttu-id="1ea79-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ea79-123">Vælg den konfigurationsversion, der har statussen 'Annulleret'.</span><span class="sxs-lookup"><span data-stu-id="1ea79-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="1ea79-124">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="1ea79-124">Click Delete.</span></span>
8. <span data-ttu-id="1ea79-125">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="1ea79-125">Click Yes.</span></span>
    * <span data-ttu-id="1ea79-126">Bemærk, at kun kladdeversion 2 af den valgte datamodelkonfiguration er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="1ea79-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="1ea79-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1ea79-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="1ea79-128">Importere en delt version af datamodelkonfiguration fra LCS</span><span class="sxs-lookup"><span data-stu-id="1ea79-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="1ea79-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1ea79-130">Åbn listen over lagre for konfigurationsudbyderen</span><span class="sxs-lookup"><span data-stu-id="1ea79-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="1ea79-131">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1ea79-131">configuration provider.</span></span>  
2. <span data-ttu-id="1ea79-132">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="1ea79-132">Click Repositories.</span></span>
3. <span data-ttu-id="1ea79-133">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="1ea79-133">Click Open.</span></span>
    * <span data-ttu-id="1ea79-134">Vælg LCS-lageret, og åbn det.</span><span class="sxs-lookup"><span data-stu-id="1ea79-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="1ea79-135">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1ea79-136">Vælg den første version af 'Eksempelmodelkonfiguration' på versionslisten.</span><span class="sxs-lookup"><span data-stu-id="1ea79-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="1ea79-137">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="1ea79-137">Click Import.</span></span>
6. <span data-ttu-id="1ea79-138">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="1ea79-138">Click Yes.</span></span>
    * <span data-ttu-id="1ea79-139">Bekræft importen af den valgte version fra LCS.</span><span class="sxs-lookup"><span data-stu-id="1ea79-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="1ea79-140">Bemærk, at meddelelsen (over formen) bekræfter fuldførelsen af importen af den valgte version.</span><span class="sxs-lookup"><span data-stu-id="1ea79-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="1ea79-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1ea79-141">Close the page.</span></span>
8. <span data-ttu-id="1ea79-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1ea79-142">Close the page.</span></span>
9. <span data-ttu-id="1ea79-143">Klik på Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1ea79-143">Click Configurations.</span></span>
10. <span data-ttu-id="1ea79-144">Vælg 'Eksempelmodelkonfiguration' i træet.</span><span class="sxs-lookup"><span data-stu-id="1ea79-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="1ea79-145">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1ea79-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1ea79-146">Vælg den konfigurationsversion, der har statussen 'Delt'.</span><span class="sxs-lookup"><span data-stu-id="1ea79-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="1ea79-147">Bemærk, at den delte version 1 af den valgte datamodelkonfiguration nu også er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="1ea79-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

