---
title: Oprette modeltilknytningskonfigurationer til elektronisk rapportering
description: Du kan bruge denne procedure til at designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcfc258e7fe364779fd77cc79413e8d5e871e214
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182686"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="55f8b-103">Oprette modeltilknytningskonfigurationer til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="55f8b-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55f8b-104">Du kan bruge denne procedure til at designe en ny modeltilknytningskonfiguration til elektronisk rapportering og bruge indbyggede ER-funktioner til effektive samlede beregninger.</span><span class="sxs-lookup"><span data-stu-id="55f8b-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="55f8b-105">I denne procedure skal du oprette en konfiguration til eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="55f8b-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="55f8b-106">Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="55f8b-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="55f8b-107">Disse trin kan udføres ved hjælp af ethvert datasæt.</span><span class="sxs-lookup"><span data-stu-id="55f8b-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="55f8b-108">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="55f8b-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="55f8b-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="55f8b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="55f8b-110">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="55f8b-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="55f8b-111">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="55f8b-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="55f8b-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="55f8b-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="55f8b-113">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="55f8b-113">Click Show filters.</span></span>
4. <span data-ttu-id="55f8b-114">Angiv filterværdien "Intrastat" i feltet "Navn", og brug filteroperatoren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="55f8b-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="55f8b-115">Anvend dette filter til at finde 'Intrastat'-datamodelkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="55f8b-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="55f8b-116">Denne model findes muligvis allerede i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="55f8b-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="55f8b-117">Hvis det er tilfældet, kan du springe over næste underordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="55f8b-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="55f8b-118">Hent den Intrastat-modelkonfiguration, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="55f8b-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="55f8b-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55f8b-119">Close the page.</span></span>
2. <span data-ttu-id="55f8b-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55f8b-120">Close the page.</span></span>
3. <span data-ttu-id="55f8b-121">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="55f8b-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="55f8b-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="55f8b-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55f8b-123">Vælg feltet Microsoft-udbyder.</span><span class="sxs-lookup"><span data-stu-id="55f8b-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="55f8b-124">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="55f8b-124">Click Repositories.</span></span>
    * <span data-ttu-id="55f8b-125">Klik på Lagre i feltet Microsoft-udbyder.</span><span class="sxs-lookup"><span data-stu-id="55f8b-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="55f8b-126">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="55f8b-126">Click Show filters.</span></span>
7. <span data-ttu-id="55f8b-127">Angiv filterværdien "ressourcer" i feltet "Typenavn", og brug filteroperatoren "indeholder".</span><span class="sxs-lookup"><span data-stu-id="55f8b-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="55f8b-128">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="55f8b-128">Click Open.</span></span>
9. <span data-ttu-id="55f8b-129">Vælg 'Intrastat model' i træet.</span><span class="sxs-lookup"><span data-stu-id="55f8b-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="55f8b-130">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="55f8b-130">Click Import.</span></span>
11. <span data-ttu-id="55f8b-131">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="55f8b-131">Click Yes.</span></span>
    * <span data-ttu-id="55f8b-132">Du har importeret den ER-modelkonfiguration, der indeholder den datamodel, du vil bruge til at undersøge, hvordan du kan bruge den nye ER-funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="55f8b-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="55f8b-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55f8b-133">Close the page.</span></span>
13. <span data-ttu-id="55f8b-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55f8b-134">Close the page.</span></span>
14. <span data-ttu-id="55f8b-135">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="55f8b-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="55f8b-136">Tilføj en ny modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="55f8b-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="55f8b-137">Vælg 'Intrastat model' i træet.</span><span class="sxs-lookup"><span data-stu-id="55f8b-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="55f8b-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="55f8b-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="55f8b-139">Skriv "Modeltilknytning baseret på datamodellen Intrastat" i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="55f8b-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="55f8b-140">Skriv 'Tilknytning af Intrastat-eksempel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="55f8b-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="55f8b-141">Tilknytning af Intrastat-eksempel</span><span class="sxs-lookup"><span data-stu-id="55f8b-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="55f8b-142">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="55f8b-142">Click Create configuration.</span></span>

