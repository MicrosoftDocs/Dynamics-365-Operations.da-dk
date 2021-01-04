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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441624"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="5966c-103">Udligne en fremdateret check fra en debitor</span><span class="sxs-lookup"><span data-stu-id="5966c-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5966c-104">Du kan udligne en fremdateret check, efter at checken er clearet af banken.</span><span class="sxs-lookup"><span data-stu-id="5966c-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="5966c-105">Denne økonomiske bevægelse clearer også posteringen på en mellemkonto for den fremdaterede check.</span><span class="sxs-lookup"><span data-stu-id="5966c-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="5966c-106">Følgende opgaver skal være fuldført, før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="5966c-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="5966c-107">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="5966c-107">Set up postdated checks</span></span>

2) <span data-ttu-id="5966c-108">Registrere og bogføre en fremdateret check for en debitor</span><span class="sxs-lookup"><span data-stu-id="5966c-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="5966c-109">Rollen for denne opgaveguide er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="5966c-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="5966c-110">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="5966c-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="5966c-111">Gå til Kredit og inkasso > Forespørgsler og rapporter > Betalinger > Fremdaterede debitorchecks.</span><span class="sxs-lookup"><span data-stu-id="5966c-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="5966c-112">Klik på Udlign.</span><span class="sxs-lookup"><span data-stu-id="5966c-112">Click Settle.</span></span>
3. <span data-ttu-id="5966c-113">Klik på Afregn clearingpostering.</span><span class="sxs-lookup"><span data-stu-id="5966c-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="5966c-114">Udlign debitorkontoen for checktransaktionen.</span><span class="sxs-lookup"><span data-stu-id="5966c-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="5966c-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5966c-115">Close the page.</span></span>
5. <span data-ttu-id="5966c-116">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="5966c-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="5966c-117">Vælg en indstilling i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="5966c-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="5966c-118">Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.</span><span class="sxs-lookup"><span data-stu-id="5966c-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="5966c-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="5966c-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="5966c-120">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="5966c-120">Click Lines.</span></span>
10. <span data-ttu-id="5966c-121">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="5966c-121">Click Voucher.</span></span>
11. <span data-ttu-id="5966c-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5966c-122">Close the page.</span></span>

