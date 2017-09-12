--- 
title: Udligne en fremdateret check for en kreditor
description: "Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ac3fcad40e2d71dbde5fab8d1aa77cbfa879cdb1
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="dcf0b-103">Udligne en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="dcf0b-103">Settle a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcf0b-104">Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="dcf0b-105">Gennemfør følgende procedurer, før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="dcf0b-106">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="dcf0b-106">Set up postdated checks</span></span>

2) <span data-ttu-id="dcf0b-107">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="dcf0b-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="dcf0b-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="dcf0b-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="dcf0b-110">Gå til Kreditor > Betalinger > Fremdaterede kreditorchecks.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="dcf0b-111">Klik på Udlign.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-111">Click Settle.</span></span>
3. <span data-ttu-id="dcf0b-112">Klik på Afregn clearingpostering.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="dcf0b-113">Udlign kreditorkontoen for checktransaktionen.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="dcf0b-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-114">Close the page.</span></span>
5. <span data-ttu-id="dcf0b-115">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="dcf0b-116">Vælg "Alle" i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="dcf0b-117">Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="dcf0b-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dcf0b-119">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-119">Click Lines.</span></span>
10. <span data-ttu-id="dcf0b-120">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-120">Click Voucher.</span></span>
11. <span data-ttu-id="dcf0b-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dcf0b-121">Close the page.</span></span>


