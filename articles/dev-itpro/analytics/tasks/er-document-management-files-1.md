--- 
title: Forberede datamodeller til at bruge dokumentstyringsfiler i ER-output
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
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
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="504a3-103">Forberede datamodeller til at bruge dokumentstyringsfiler i ER-output</span><span class="sxs-lookup"><span data-stu-id="504a3-103">Prepare data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="504a3-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="504a3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="504a3-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="504a3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="504a3-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="504a3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="504a3-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="504a3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="504a3-108">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="504a3-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="504a3-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="504a3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="504a3-110">Sørg for, at udbyderen 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="504a3-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="504a3-111">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="504a3-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="504a3-112">Vælg udbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="504a3-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="504a3-113">.</span><span class="sxs-lookup"><span data-stu-id="504a3-113">provider.</span></span>
3. <span data-ttu-id="504a3-114">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="504a3-114">Click Repositories.</span></span>
    * <span data-ttu-id="504a3-115">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="504a3-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="504a3-116">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="504a3-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="504a3-117">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="504a3-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="504a3-118">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="504a3-118">Click Create repository.</span></span>
7. <span data-ttu-id="504a3-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="504a3-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="504a3-120">Hent de konfigurationer for kundefakturamodelle, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="504a3-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="504a3-121">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="504a3-121">Click Show filters.</span></span>
2. <span data-ttu-id="504a3-122">Anvend følgende filtre: Angiv filterværdien "Operationsressourcer" i feltet "Navn" ved hjælp af filteroperatoren "starter med". Angiv filterværdien "" i feltet "Beskrivelse" ved hjælp af filteroperatoren "starter med"</span><span class="sxs-lookup"><span data-stu-id="504a3-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="504a3-123">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="504a3-123">Click Show filters.</span></span>
4. <span data-ttu-id="504a3-124">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="504a3-124">Click Open.</span></span>
5. <span data-ttu-id="504a3-125">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="504a3-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="504a3-126">Vælg modelkonfigurationen 'Debitorfakturamodel' for at importere den.</span><span class="sxs-lookup"><span data-stu-id="504a3-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="504a3-127">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="504a3-127">Click Import.</span></span>
    * <span data-ttu-id="504a3-128">Klik på Importer for version 1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="504a3-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="504a3-129">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="504a3-129">Click Yes.</span></span>
8. <span data-ttu-id="504a3-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="504a3-130">Close the page.</span></span>
9. <span data-ttu-id="504a3-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="504a3-131">Close the page.</span></span>
10. <span data-ttu-id="504a3-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="504a3-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="504a3-133">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="504a3-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="504a3-134">Opret den afledte model for at understøtte adgang til filerne fra Dokumentstyring.</span><span class="sxs-lookup"><span data-stu-id="504a3-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="504a3-135">Du vil oprette vores egen konfiguration af kundens fakturamodel, der er afledt af den konfiguration, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="504a3-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="504a3-136">Du skal bruge denne konfiguration til at implementere adgang til filerne fra Dokumentstyring og gøre dem tilgængelige for elektroniske dokumenter, som du opretter ud fra denne model.</span><span class="sxs-lookup"><span data-stu-id="504a3-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="504a3-137">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="504a3-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="504a3-138">Skriv 'Afled fra navn: Debitorfakturamodel, Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="504a3-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="504a3-139">Skriv "Debitorfakturamodel (brugerdefineret)" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="504a3-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="504a3-140">Debitorfakturamodel (brugerdefineret)</span><span class="sxs-lookup"><span data-stu-id="504a3-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="504a3-141">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="504a3-141">Click Create configuration.</span></span>


