---
title: Behandle finansfordelingskladde
description: I dette emne beskrives, hvordan du behandler en fordelingsanmodning i Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144953"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="7c161-103">Behandle finansfordelingskladde</span><span class="sxs-lookup"><span data-stu-id="7c161-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c161-104">I dette emne beskrives, hvordan du behandler en fordelingsanmodning.</span><span class="sxs-lookup"><span data-stu-id="7c161-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="7c161-105">Brug siden Udfør fordelingsanmodning til at oprette en fordelingskladde, der kan gennemses og godkendes før postering i Finans, eller bogføres direkte i Finans.</span><span class="sxs-lookup"><span data-stu-id="7c161-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="7c161-106">Før du kan oprette en fordelingskladde, skal der være mindst én aktiv finansfordelingsregel.</span><span class="sxs-lookup"><span data-stu-id="7c161-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="7c161-107">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7c161-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7c161-108">Gå til **Moduler > Finans > Fordelinger > Udfør fordelingsanmodning** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="7c161-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="7c161-109">I feltet **Regel** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="7c161-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="7c161-110">Angiv en dato i feltet **Pr. dato**.</span><span class="sxs-lookup"><span data-stu-id="7c161-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="7c161-111">**Pr. dato** er meget vigtig, når Finans er datakilden for reglen.</span><span class="sxs-lookup"><span data-stu-id="7c161-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="7c161-112">Denne dato bestemmer, hvilke finanssaldi der skal medtages til fordeling.</span><span class="sxs-lookup"><span data-stu-id="7c161-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="7c161-113">Vælg **Stop** i **Nul-kilde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7c161-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="7c161-114">Derved standses fordelingsprocessen, og der vises en meddelelse, der angiver, at der er valgt et nul-kildebeløb.</span><span class="sxs-lookup"><span data-stu-id="7c161-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="7c161-115">Vælg **Kun forslag** i feltet **Forslagsmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="7c161-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="7c161-116">Vælg **Kun forslag** for at gennemgå og eventuelt godkende resultatet i Fordelingskladder før bogføring af fordelingen til Finans.</span><span class="sxs-lookup"><span data-stu-id="7c161-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="7c161-117">Angiv en dato i feltet Finansposteringsdato.</span><span class="sxs-lookup"><span data-stu-id="7c161-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="7c161-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c161-118">Select **OK**.</span></span>
7. <span data-ttu-id="7c161-119">Gå til **Moduler > Finans > Fordelinger > Fordelingskladder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="7c161-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="7c161-120">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7c161-120">Select **Lines**.</span></span>
9. <span data-ttu-id="7c161-121">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="7c161-121">Select **Post**.</span></span>
10. <span data-ttu-id="7c161-122">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="7c161-122">Select **Post**.</span></span>

