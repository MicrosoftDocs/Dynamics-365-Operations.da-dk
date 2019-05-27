---
title: Udligne en fremdateret check fra en debitor
description: Du kan udligne en fremdateret check, efter at checken er clearet af banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cefaac99a1ce5aa777f4f62456c3248045cc27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565989"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="d0c87-103">Udligne en fremdateret check fra en debitor</span><span class="sxs-lookup"><span data-stu-id="d0c87-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0c87-104">Du kan udligne en fremdateret check, efter at checken er clearet af banken.</span><span class="sxs-lookup"><span data-stu-id="d0c87-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="d0c87-105">Denne økonomiske bevægelse clearer også posteringen på en mellemkonto for den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="d0c87-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="d0c87-106">Følgende opgaver skal være fuldført, før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="d0c87-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="d0c87-107">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="d0c87-107">Set up postdated checks</span></span>

2) <span data-ttu-id="d0c87-108">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="d0c87-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="d0c87-109">Rollen for denne opgaveguide er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="d0c87-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="d0c87-110">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d0c87-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d0c87-111">Gå til Kredit og inkasso > Forespørgsler og rapporter > Betalinger > Fremdaterede debitorchecks.</span><span class="sxs-lookup"><span data-stu-id="d0c87-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="d0c87-112">Klik på Udlign.</span><span class="sxs-lookup"><span data-stu-id="d0c87-112">Click Settle.</span></span>
3. <span data-ttu-id="d0c87-113">Klik på Afregn clearingpostering.</span><span class="sxs-lookup"><span data-stu-id="d0c87-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="d0c87-114">Udlign debitorkontoen for checktransaktionen.</span><span class="sxs-lookup"><span data-stu-id="d0c87-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="d0c87-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d0c87-115">Close the page.</span></span>
5. <span data-ttu-id="d0c87-116">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="d0c87-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="d0c87-117">Vælg en indstilling i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="d0c87-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="d0c87-118">Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.</span><span class="sxs-lookup"><span data-stu-id="d0c87-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="d0c87-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d0c87-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d0c87-120">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="d0c87-120">Click Lines.</span></span>
10. <span data-ttu-id="d0c87-121">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="d0c87-121">Click Voucher.</span></span>
11. <span data-ttu-id="d0c87-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d0c87-122">Close the page.</span></span>

