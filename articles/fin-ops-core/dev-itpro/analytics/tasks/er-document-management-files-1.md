---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 1: Forbedret datamodel)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til at bruge dokumentstyringsfiler (vedhæftede filer) i ER-output. (Del 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b265c9af0635e6c9fb6295f7e8e4e353b2a5ba5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754932"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="aeef6-104">ER Brug dokumentstyringsfiler i formatoutput (del 1: Forbedret datamodel)</span><span class="sxs-lookup"><span data-stu-id="aeef6-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aeef6-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="aeef6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="aeef6-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="aeef6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="aeef6-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="aeef6-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="aeef6-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="aeef6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="aeef6-109">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="aeef6-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="aeef6-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="aeef6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="aeef6-111">Sørg for, at udbyderen 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="aeef6-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="aeef6-112">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="aeef6-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="aeef6-113">Vælg udbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="aeef6-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="aeef6-114">.</span><span class="sxs-lookup"><span data-stu-id="aeef6-114">provider.</span></span>
3. <span data-ttu-id="aeef6-115">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="aeef6-115">Click Repositories.</span></span>

    <span data-ttu-id="aeef6-116">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="aeef6-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="aeef6-117">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="aeef6-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="aeef6-118">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="aeef6-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="aeef6-119">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="aeef6-119">Click Create repository.</span></span>
7. <span data-ttu-id="aeef6-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="aeef6-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="aeef6-121">Hent de konfigurationer for kundefakturamodelle, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="aeef6-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="aeef6-122">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="aeef6-122">Click Show filters.</span></span>
2. <span data-ttu-id="aeef6-123">Anvend følgende filtre: Angiv filterværdien "Operationsressourcer" i feltet "Navn" ved hjælp af filteroperatoren "starter med". Angiv filterværdien "" i feltet "Beskrivelse" ved hjælp af filteroperatoren "starter med"</span><span class="sxs-lookup"><span data-stu-id="aeef6-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="aeef6-124">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="aeef6-124">Click Show filters.</span></span>
4. <span data-ttu-id="aeef6-125">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="aeef6-125">Click Open.</span></span>
5. <span data-ttu-id="aeef6-126">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="aeef6-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="aeef6-127">Vælg modelkonfigurationen 'Debitorfakturamodel' for at importere den.</span><span class="sxs-lookup"><span data-stu-id="aeef6-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="aeef6-128">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="aeef6-128">Click Import.</span></span>

    <span data-ttu-id="aeef6-129">Klik på Importer for version 1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aeef6-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="aeef6-130">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="aeef6-130">Click Yes.</span></span>
8. <span data-ttu-id="aeef6-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aeef6-131">Close the page.</span></span>
9. <span data-ttu-id="aeef6-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aeef6-132">Close the page.</span></span>
10. <span data-ttu-id="aeef6-133">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="aeef6-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="aeef6-134">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="aeef6-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="aeef6-135">Opret den afledte model for at understøtte adgang til filerne fra Dokumentstyring.</span><span class="sxs-lookup"><span data-stu-id="aeef6-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="aeef6-136">Du vil oprette vores egen konfiguration af kundens fakturamodel, der er afledt af den konfiguration, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aeef6-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="aeef6-137">Du skal bruge denne konfiguration til at implementere adgang til filerne fra Dokumentstyring og gøre dem tilgængelige for elektroniske dokumenter, som du opretter ud fra denne model.</span><span class="sxs-lookup"><span data-stu-id="aeef6-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="aeef6-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="aeef6-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="aeef6-139">Skriv 'Afled fra navn: Debitorfakturamodel, Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="aeef6-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="aeef6-140">Skriv "Debitorfakturamodel (brugerdefineret)" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="aeef6-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="aeef6-141">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="aeef6-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]