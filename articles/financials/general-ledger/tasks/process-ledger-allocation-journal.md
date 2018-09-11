--- 
title: Behandle finansfordelingskladde
description: "Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d9caebc6004d0a513ab2c3947300d7dd6e283750
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="ee48b-103">Behandle finansfordelingskladde</span><span class="sxs-lookup"><span data-stu-id="ee48b-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee48b-104">Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans.</span><span class="sxs-lookup"><span data-stu-id="ee48b-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="ee48b-105">Før du kan oprette en fordelingskladde, skal der være mindst én aktiv finansfordelingsregel.</span><span class="sxs-lookup"><span data-stu-id="ee48b-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="ee48b-106">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ee48b-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ee48b-107">Gå til Finans > Fordelinger > Udfør fordelingsanmodning.</span><span class="sxs-lookup"><span data-stu-id="ee48b-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="ee48b-108">Klik på rullelisten i feltet Regel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ee48b-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ee48b-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ee48b-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ee48b-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="ee48b-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ee48b-111">Angiv en dato i feltet Pr. dato.</span><span class="sxs-lookup"><span data-stu-id="ee48b-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="ee48b-112">Fra-datoen er meget vigtig, hvis Finans er datakilden for reglen.</span><span class="sxs-lookup"><span data-stu-id="ee48b-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="ee48b-113">Denne dato bestemmer, hvilke finanssaldi der skal medtages til fordeling.</span><span class="sxs-lookup"><span data-stu-id="ee48b-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="ee48b-114">Vælg Stop i Nul-kildefeltet.</span><span class="sxs-lookup"><span data-stu-id="ee48b-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="ee48b-115">Derved standses fordelingsprocessen, og der vises en meddelelse, der angiver, at der er valgt et nul-kildebeløb.</span><span class="sxs-lookup"><span data-stu-id="ee48b-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="ee48b-116">Vælg "Kun forslag" i feltet Forslagsmuligheder.</span><span class="sxs-lookup"><span data-stu-id="ee48b-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="ee48b-117">Vælg Kun forslag for at gennemgå og eventuelt godkende resultatet i Fordelingskladder før bogføring af fordelingen til Finans.</span><span class="sxs-lookup"><span data-stu-id="ee48b-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="ee48b-118">Angiv en dato i feltet Finansposteringsdato.</span><span class="sxs-lookup"><span data-stu-id="ee48b-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="ee48b-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ee48b-119">Click OK.</span></span>
9. <span data-ttu-id="ee48b-120">Gå til Finans > Fordelinger > Fordelingskladder.</span><span class="sxs-lookup"><span data-stu-id="ee48b-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="ee48b-121">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="ee48b-121">Click Lines.</span></span>
11. <span data-ttu-id="ee48b-122">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="ee48b-122">Click Post.</span></span>
12. <span data-ttu-id="ee48b-123">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="ee48b-123">Click Post.</span></span>


