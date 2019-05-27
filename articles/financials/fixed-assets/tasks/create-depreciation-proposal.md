---
title: Opret afskrivningsforslag
description: Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549529"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="ffb05-103">Opret afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="ffb05-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffb05-104">Denne procedure emne beskriver, hvordan batchafskrivningsforslag fungerer, og det forklares, hvordan du foreslår afskrivning for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="ffb05-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="ffb05-105">Denne opgave bruger USMF-demofirmaet og rollen revisor.</span><span class="sxs-lookup"><span data-stu-id="ffb05-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="ffb05-106">Opret afskrivningsforslag</span><span class="sxs-lookup"><span data-stu-id="ffb05-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="ffb05-107">Gå til Anlægsaktiver > Kladdeposteringer > Opret afskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="ffb05-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="ffb05-108">Klik på rullelisten i feltet Kladdenavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ffb05-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ffb05-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb05-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ffb05-110">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="ffb05-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ffb05-111">Markér indstillingen Opsummer afskrivning, hvis du vil opsummere månedlige afskrivninger på én kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="ffb05-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="ffb05-112">Hvis Til dato-værdien f.eks. er 31. marts 2015, genereres følgende beskrivelse: "Afskrivning siden 31. januar 2015".</span><span class="sxs-lookup"><span data-stu-id="ffb05-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="ffb05-113">Derefter indstilles feltet Dato på de foreslåede kladdelinjer til 31. marts 2015.</span><span class="sxs-lookup"><span data-stu-id="ffb05-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="ffb05-114">Afskrivningsforslaget kan filtreres efter aktiv, aktivgruppe eller andre kriterier ved hjælp af parameteren Filter.</span><span class="sxs-lookup"><span data-stu-id="ffb05-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="ffb05-115">Når du bruger Opret anskaffelses- eller afskrivningsforslag til formen anlægsaktiver, kan du foreslå afskrivning i batch.</span><span class="sxs-lookup"><span data-stu-id="ffb05-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="ffb05-116">Dette anbefales til større forslag, der vil bruge flere systemressourcer.</span><span class="sxs-lookup"><span data-stu-id="ffb05-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="ffb05-117">Hvis du vælger batchindstillingen, kan du stadig fuldføre andre opgaver samtidig.</span><span class="sxs-lookup"><span data-stu-id="ffb05-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="ffb05-118">Når du foreslår afskrivning på denne måde, beregnes afskrivningen for værdimodeller for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="ffb05-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="ffb05-119">Klik på Opret kladde.</span><span class="sxs-lookup"><span data-stu-id="ffb05-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="ffb05-120">Gennemse afskrivningsposter.</span><span class="sxs-lookup"><span data-stu-id="ffb05-120">Review depreciation entries</span></span>
1. <span data-ttu-id="ffb05-121">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="ffb05-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="ffb05-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ffb05-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ffb05-123">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="ffb05-123">Click Lines.</span></span>
4. <span data-ttu-id="ffb05-124">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="ffb05-124">Click Post.</span></span>

