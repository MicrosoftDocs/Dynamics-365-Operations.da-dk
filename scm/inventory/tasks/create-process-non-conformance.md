---
title: Oprette og behandle en overensstemmelse
description: "Brug denne procedure til at udføre uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: da-dk
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="ad812-103">Oprette og behandle en overensstemmelse</span><span class="sxs-lookup"><span data-stu-id="ad812-103">Create and process a conformance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad812-104">Brug denne procedure til at udføre uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="ad812-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="ad812-105">Du kan køre denne registrering i demofirmaet USMF, og du kan bruge de foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="ad812-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="ad812-106">Denne procedure udføres typisk af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="ad812-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="ad812-107">Som en forudsætning skal du køre opgaveregistreringen "Inspicer kvaliteten af varer".</span><span class="sxs-lookup"><span data-stu-id="ad812-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="ad812-108">For at behandle godkendelse af en uoverensstemmelse skal den bruger, der kører opgavregistreringen, have en "Navn"-værdi tildelt på siden Brugere.</span><span class="sxs-lookup"><span data-stu-id="ad812-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="ad812-109">For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="ad812-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ad812-110">Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="ad812-110">Select a quality order</span></span>
1. <span data-ttu-id="ad812-111">Gå til Kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="ad812-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="ad812-112">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad812-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ad812-113">Vælg den kvalitetsordre, der blev oprettet ud fra opgaveregistreringen "Kontrollere kvaliteten af varer".</span><span class="sxs-lookup"><span data-stu-id="ad812-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="ad812-114">Oprette en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="ad812-114">Create a nonconformance</span></span>
1. <span data-ttu-id="ad812-115">Klik på Forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="ad812-115">Click Inquiries.</span></span>
2. <span data-ttu-id="ad812-116">Klik på Uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="ad812-116">Click Non conformances.</span></span>
3. <span data-ttu-id="ad812-117">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ad812-117">Click New.</span></span>
4. <span data-ttu-id="ad812-118">Klik på rullelisten i feltet Problemtype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ad812-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ad812-119">Vælg det problem, der blev fundet under inspektionsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ad812-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="ad812-120">Klik på rullelisten i feltet Problemtype for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ad812-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ad812-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ad812-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ad812-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad812-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ad812-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ad812-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="ad812-124">Godkende/afvise en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="ad812-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="ad812-125">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="ad812-125">Click Functions.</span></span>
2. <span data-ttu-id="ad812-126">Klik på Godkend uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="ad812-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="ad812-127">I dette eksempel skal du godkende uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="ad812-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="ad812-128">Godkendte uoverensstemmelser kan være tilknytte til relaterede operationer at registrere arbejde, der udføres som en del af håndteringen af uoverensstemmelsen og, som i denne opgaveregistrering, behandlingen af korrektionshåndtering.</span><span class="sxs-lookup"><span data-stu-id="ad812-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="ad812-129">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="ad812-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="ad812-130">Opret en korrektionshandling</span><span class="sxs-lookup"><span data-stu-id="ad812-130">Create a correction action</span></span>
1. <span data-ttu-id="ad812-131">Klik på Rettelser.</span><span class="sxs-lookup"><span data-stu-id="ad812-131">Click Corrections.</span></span>
2. <span data-ttu-id="ad812-132">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ad812-132">Click New.</span></span>
3. <span data-ttu-id="ad812-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad812-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ad812-134">Klik på rullelisten i feltet Personalenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ad812-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ad812-135">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ad812-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ad812-136">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="ad812-136">Click Select.</span></span>
7. <span data-ttu-id="ad812-137">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="ad812-137">Click Attach.</span></span>
    * <span data-ttu-id="ad812-138">Oprette en note om korrektionen.</span><span class="sxs-lookup"><span data-stu-id="ad812-138">Create a note about the correction.</span></span> <span data-ttu-id="ad812-139">I dette eksempel er handlingen at kontakte leverandøren for at diskutere uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="ad812-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="ad812-140">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ad812-140">Click New.</span></span>
9. <span data-ttu-id="ad812-141">Klik på Notat.</span><span class="sxs-lookup"><span data-stu-id="ad812-141">Click Note.</span></span>
    * <span data-ttu-id="ad812-142">Bemærk, at afhængigt af opsætningen af rapporten kan forskellige dokumenttyper udskrives på de rapporter, der er relateret til uoverensstemmelsesstyring.</span><span class="sxs-lookup"><span data-stu-id="ad812-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="ad812-143">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ad812-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="ad812-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad812-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="ad812-145">Vedligehold en korrektion</span><span class="sxs-lookup"><span data-stu-id="ad812-145">Maintain a correction</span></span>
1. <span data-ttu-id="ad812-146">Klik på Marker som fuldført.</span><span class="sxs-lookup"><span data-stu-id="ad812-146">Click Mark complete.</span></span>
2. <span data-ttu-id="ad812-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ad812-147">Click OK.</span></span>
3. <span data-ttu-id="ad812-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad812-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="ad812-149">Luk en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="ad812-149">Close a nonconformance</span></span>
1. <span data-ttu-id="ad812-150">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="ad812-150">Click Functions.</span></span>
2. <span data-ttu-id="ad812-151">Klik på Luk uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="ad812-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="ad812-152">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="ad812-152">Click Yes.</span></span>
4. <span data-ttu-id="ad812-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad812-153">Close the page.</span></span>
5. <span data-ttu-id="ad812-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ad812-154">Close the page.</span></span>

