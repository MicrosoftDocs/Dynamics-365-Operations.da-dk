---
title: Udligne en fremdateret check for en kreditor
description: Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144229"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="0fa18-103">Udligne en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="0fa18-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fa18-104">Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken.</span><span class="sxs-lookup"><span data-stu-id="0fa18-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="0fa18-105">Gennemfør følgende procedurer, før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="0fa18-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="0fa18-106">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="0fa18-106">Set up postdated checks</span></span>

2) <span data-ttu-id="0fa18-107">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="0fa18-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="0fa18-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="0fa18-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="0fa18-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="0fa18-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="0fa18-110">Gå til Kreditor > Betalinger > Fremdaterede kreditorchecks.</span><span class="sxs-lookup"><span data-stu-id="0fa18-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="0fa18-111">Klik på Udlign.</span><span class="sxs-lookup"><span data-stu-id="0fa18-111">Click Settle.</span></span>
3. <span data-ttu-id="0fa18-112">Klik på Afregn clearingpostering.</span><span class="sxs-lookup"><span data-stu-id="0fa18-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="0fa18-113">Udlign kreditorkontoen for checktransaktionen.</span><span class="sxs-lookup"><span data-stu-id="0fa18-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="0fa18-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fa18-114">Close the page.</span></span>
5. <span data-ttu-id="0fa18-115">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="0fa18-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="0fa18-116">Vælg "Alle" i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="0fa18-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="0fa18-117">Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.</span><span class="sxs-lookup"><span data-stu-id="0fa18-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="0fa18-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0fa18-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0fa18-119">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="0fa18-119">Click Lines.</span></span>
10. <span data-ttu-id="0fa18-120">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="0fa18-120">Click Voucher.</span></span>
11. <span data-ttu-id="0fa18-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0fa18-121">Close the page.</span></span>

