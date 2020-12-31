---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 1: Forbedret datamodel)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b82c63c572cc946737ba54deb10a03dc437c01b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681815"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="56a5e-103">ER Brug dokumentstyringsfiler i formatoutput (del 1: Forbedret datamodel)</span><span class="sxs-lookup"><span data-stu-id="56a5e-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56a5e-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="56a5e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="56a5e-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="56a5e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="56a5e-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="56a5e-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="56a5e-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="56a5e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="56a5e-108">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="56a5e-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="56a5e-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="56a5e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="56a5e-110">Sørg for, at udbyderen 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="56a5e-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="56a5e-111">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="56a5e-111">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="56a5e-112">Vælg udbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="56a5e-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="56a5e-113">.</span><span class="sxs-lookup"><span data-stu-id="56a5e-113">provider.</span></span>
3. <span data-ttu-id="56a5e-114">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="56a5e-114">Click Repositories.</span></span>

    <span data-ttu-id="56a5e-115">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="56a5e-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="56a5e-116">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="56a5e-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="56a5e-117">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="56a5e-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="56a5e-118">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="56a5e-118">Click Create repository.</span></span>
7. <span data-ttu-id="56a5e-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="56a5e-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="56a5e-120">Hent de konfigurationer for kundefakturamodelle, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="56a5e-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="56a5e-121">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="56a5e-121">Click Show filters.</span></span>
2. <span data-ttu-id="56a5e-122">Anvend følgende filtre: Angiv filterværdien "Operationsressourcer" i feltet "Navn" ved hjælp af filteroperatoren "starter med". Angiv filterværdien "" i feltet "Beskrivelse" ved hjælp af filteroperatoren "starter med"</span><span class="sxs-lookup"><span data-stu-id="56a5e-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="56a5e-123">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="56a5e-123">Click Show filters.</span></span>
4. <span data-ttu-id="56a5e-124">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="56a5e-124">Click Open.</span></span>
5. <span data-ttu-id="56a5e-125">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="56a5e-125">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="56a5e-126">Vælg modelkonfigurationen 'Debitorfakturamodel' for at importere den.</span><span class="sxs-lookup"><span data-stu-id="56a5e-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="56a5e-127">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="56a5e-127">Click Import.</span></span>

    <span data-ttu-id="56a5e-128">Klik på Importer for version 1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="56a5e-128">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="56a5e-129">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="56a5e-129">Click Yes.</span></span>
8. <span data-ttu-id="56a5e-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="56a5e-130">Close the page.</span></span>
9. <span data-ttu-id="56a5e-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="56a5e-131">Close the page.</span></span>
10. <span data-ttu-id="56a5e-132">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="56a5e-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="56a5e-133">Vælg 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="56a5e-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="56a5e-134">Opret den afledte model for at understøtte adgang til filerne fra Dokumentstyring.</span><span class="sxs-lookup"><span data-stu-id="56a5e-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="56a5e-135">Du vil oprette vores egen konfiguration af kundens fakturamodel, der er afledt af den konfiguration, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56a5e-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="56a5e-136">Du skal bruge denne konfiguration til at implementere adgang til filerne fra Dokumentstyring og gøre dem tilgængelige for elektroniske dokumenter, som du opretter ud fra denne model.</span><span class="sxs-lookup"><span data-stu-id="56a5e-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="56a5e-137">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="56a5e-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="56a5e-138">Skriv 'Afled fra navn: Debitorfakturamodel, Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="56a5e-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="56a5e-139">Skriv "Debitorfakturamodel (brugerdefineret)" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="56a5e-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="56a5e-140">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="56a5e-140">Click Create configuration.</span></span>

