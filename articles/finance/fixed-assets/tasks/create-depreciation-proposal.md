---
title: Oprette et afskrivningsforslag
description: Dette emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslå afskrivning for anlægsaktiver.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013c768c8a016f399a27b1488ad0d5b339fdf7cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813573"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="c6be1-103">Oprette et afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="c6be1-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6be1-104">Dette emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslå afskrivning for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="c6be1-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="c6be1-105">Denne opgave bruger USMF-demofirmaet og rollen revisor.</span><span class="sxs-lookup"><span data-stu-id="c6be1-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="c6be1-106">Oprette et afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="c6be1-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="c6be1-107">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="c6be1-108">Vælg en indstilling på rullelisten i feltet **Kladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="c6be1-109">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="c6be1-110">Vælg indstillingen **Opsummer afskrivning**, hvis du vil opsummere månedlige afskrivninger på én kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="c6be1-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="c6be1-111">Hvis Til dato-værdien f.eks. er 31. marts 2015, genereres følgende beskrivelse: "Afskrivning siden 31. januar 2015".</span><span class="sxs-lookup"><span data-stu-id="c6be1-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="c6be1-112">Derefter indstilles feltet **Dato** på de foreslåede kladdelinjer til 31. marts 2015.</span><span class="sxs-lookup"><span data-stu-id="c6be1-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="c6be1-113">Afskrivningsforslaget kan filtreres efter aktiv, aktivgruppe eller andre kriterier ved hjælp af parameteren **Filter**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="c6be1-114">Når du bruger formen **Opret anskaffelses- eller afskrivningsforslag til anlægsaktiver**, kan du foreslå afskrivning i batch.</span><span class="sxs-lookup"><span data-stu-id="c6be1-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="c6be1-115">Dette anbefales til større forslag, der vil bruge flere systemressourcer.</span><span class="sxs-lookup"><span data-stu-id="c6be1-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="c6be1-116">Hvis du vælger batchindstillingen, kan du stadig fuldføre andre opgaver samtidig.</span><span class="sxs-lookup"><span data-stu-id="c6be1-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="c6be1-117">Når du foreslår afskrivning på denne måde, beregnes afskrivningen for værdimodeller for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="c6be1-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="c6be1-118">Vælg **Opret kladde**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="c6be1-119">Gennemse afskrivningsposter.</span><span class="sxs-lookup"><span data-stu-id="c6be1-119">Review depreciation entries</span></span>
1. <span data-ttu-id="c6be1-120">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c6be1-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c6be1-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c6be1-122">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-122">Select **Lines**.</span></span>
4. <span data-ttu-id="c6be1-123">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="c6be1-123">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]