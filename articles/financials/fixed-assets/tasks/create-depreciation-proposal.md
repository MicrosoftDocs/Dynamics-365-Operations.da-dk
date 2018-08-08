--- 
title: Oprette et afskrivningsforslag
description: "Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ab5264a0f2c03655a3e8f23344f5233c1bfb6515
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="6b0b5-103">Oprette et afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="6b0b5-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b0b5-104">Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="6b0b5-105">Denne opgave bruger USMF-demofirmaet og rollen revisor.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="6b0b5-106">Opret afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="6b0b5-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="6b0b5-107">Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="6b0b5-108">Klik på rullelisten i feltet Kladdenavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6b0b5-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6b0b5-110">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="6b0b5-111">Markér indstillingen Opsummer afskrivning, hvis du vil opsummere månedlige afskrivninger på én kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="6b0b5-112">Hvis Til dato-værdien f.eks. er 31. marts 2015, genereres følgende beskrivelse: "Afskrivning siden 31. januar 2015".</span><span class="sxs-lookup"><span data-stu-id="6b0b5-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="6b0b5-113">Derefter indstilles feltet Dato på de foreslåede kladdelinjer til 31. marts 2015.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="6b0b5-114">Afskrivningsforslaget kan filtreres efter aktiv, aktivgruppe eller andre kriterier ved hjælp af parameteren Filter.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="6b0b5-115">Når du bruger Opret anskaffelses- eller afskrivningsforslag til formen anlægsaktiver, kan du foreslå afskrivning i batch.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="6b0b5-116">Dette anbefales til større forslag, der vil bruge flere systemressourcer.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="6b0b5-117">Hvis du vælger batchindstillingen, kan du stadig fuldføre andre opgaver samtidig.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="6b0b5-118">Når du foreslår afskrivning på denne måde, beregnes afskrivningen for værdimodeller for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="6b0b5-119">Klik på Opret kladde.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="6b0b5-120">Gennemse afskrivningsposter.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-120">Review depreciation entries</span></span>
1. <span data-ttu-id="6b0b5-121">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="6b0b5-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6b0b5-123">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-123">Click Lines.</span></span>
4. <span data-ttu-id="6b0b5-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="6b0b5-124">Click Post.</span></span>


