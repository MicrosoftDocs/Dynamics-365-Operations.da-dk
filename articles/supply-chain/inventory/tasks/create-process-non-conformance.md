---
title: Oprette og behandle en overensstemmelse
description: Dette emne forklarer, hvordan du udfører uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d012af1924e9eedee41f46de6c253d009cb52d2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145703"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="cd3d8-103">Oprette og behandle en overensstemmelse</span><span class="sxs-lookup"><span data-stu-id="cd3d8-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd3d8-104">Dette emne forklarer, hvordan du udfører uoverensstemmelsesstyring baseret på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="cd3d8-105">Du kan køre denne registrering i demofirmaet USMF, og du kan bruge de foreslåede værdier.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="cd3d8-106">Denne procedure udføres typisk af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="cd3d8-107">Som en forudsætning skal du følge instruktionerne i [Inspicere varers kvalitet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="cd3d8-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="cd3d8-108">For at behandle godkendelse af en uoverensstemmelse skal den bruger, der kører opgavregistreringen, have en "Navn"-værdi tildelt på siden Brugere.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="cd3d8-109">For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="cd3d8-110">Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="cd3d8-110">Select a quality order</span></span>
1. <span data-ttu-id="cd3d8-111">I navigationsruden skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.**</span><span class="sxs-lookup"><span data-stu-id="cd3d8-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="cd3d8-112">Vælg på listen den kvalitetsordre, der blev oprettet i [Inspicere varers kvalitet](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="cd3d8-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="cd3d8-113">Oprette en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="cd3d8-113">Create a nonconformance</span></span>
1. <span data-ttu-id="cd3d8-114">Gå til handlingsruden, og vælg **Forespørgsler**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="cd3d8-115">Vælg **Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="cd3d8-116">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-116">Select **New**.</span></span>
4. <span data-ttu-id="cd3d8-117">Vælg det problem, der blev fundet i inspektionsprocessen, i rullemenuen til feltet **Problemtype**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="cd3d8-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="cd3d8-119">Godkende/afvise en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="cd3d8-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="cd3d8-120">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-120">Select **Functions**.</span></span>
2. <span data-ttu-id="cd3d8-121">Vælg **Godkend uoverensstemmelsen**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="cd3d8-122">I dette eksempel skal du godkende uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="cd3d8-123">Godkendte uoverensstemmelser kan være tilknyttet relaterede operationer for at registrere arbejde, der udføres som en del af håndteringen af uoverensstemmelsen og, som i dette emne, behandlingen af korrektionshåndtering.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="cd3d8-124">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="cd3d8-125">Opret en korrektionshandling</span><span class="sxs-lookup"><span data-stu-id="cd3d8-125">Create a correction action</span></span>
1. <span data-ttu-id="cd3d8-126">Vælg **Rettelser**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="cd3d8-127">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-127">Select **New**.</span></span>
3. <span data-ttu-id="cd3d8-128">Vælg den ønskede post fra rullemenuen i feltet **Personalenummer** i den nye række.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="cd3d8-129">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-129">Click **Select**.</span></span>
5. <span data-ttu-id="cd3d8-130">Vælg **Vedhæft**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-130">Select **Attach**.</span></span> <span data-ttu-id="cd3d8-131">Oprette en note om korrektionen.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-131">Create a note about the correction.</span></span> <span data-ttu-id="cd3d8-132">I dette eksempel er handlingen at kontakte leverandøren for at diskutere uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="cd3d8-133">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-133">Select **New**.</span></span>
7. <span data-ttu-id="cd3d8-134">Vælg **Note**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-134">Select **Note**.</span></span> <span data-ttu-id="cd3d8-135">Afhængigt af opsætningen af rapporten kan forskellige dokumenttyper udskrives på de rapporter, der er relateret til uoverensstemmelsesstyring.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="cd3d8-136">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="cd3d8-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="cd3d8-138">Vedligehold en korrektion</span><span class="sxs-lookup"><span data-stu-id="cd3d8-138">Maintain a correction</span></span>
1. <span data-ttu-id="cd3d8-139">Vælg **Markér som fuldført**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="cd3d8-140">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-140">Select **OK**.</span></span>
3. <span data-ttu-id="cd3d8-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="cd3d8-142">Luk en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="cd3d8-142">Close a nonconformance</span></span>
1. <span data-ttu-id="cd3d8-143">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-143">Select **Functions**.</span></span>
2. <span data-ttu-id="cd3d8-144">Vælg **Luk uoverensstemmelsen**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="cd3d8-145">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-145">Select **Yes**.</span></span>
4. <span data-ttu-id="cd3d8-146">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="cd3d8-146">Close the pages.</span></span>
