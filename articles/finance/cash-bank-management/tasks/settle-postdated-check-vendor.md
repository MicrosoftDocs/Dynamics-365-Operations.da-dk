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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d66caa83df693445c1b1d40ffdc11e8d10cf7426
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239621"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="c81c2-103">Udligne en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="c81c2-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c81c2-104">Udligne en fremdateret check, der er udstedt til en leverandør, når banken har clearet checkposteringen, når checken har været forfalden og ikke markeret af banken.</span><span class="sxs-lookup"><span data-stu-id="c81c2-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="c81c2-105">Gennemfør følgende procedurer, før du starter denne.</span><span class="sxs-lookup"><span data-stu-id="c81c2-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="c81c2-106">Oprette fremdaterede checks</span><span class="sxs-lookup"><span data-stu-id="c81c2-106">Set up postdated checks</span></span>

2) <span data-ttu-id="c81c2-107">Registrere og bogføre en fremdateret check for en kreditor</span><span class="sxs-lookup"><span data-stu-id="c81c2-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="c81c2-108">Rollen for denne procedure er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="c81c2-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="c81c2-109">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="c81c2-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="c81c2-110">Gå til Kreditor > Betalinger > Fremdaterede kreditorchecks.</span><span class="sxs-lookup"><span data-stu-id="c81c2-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="c81c2-111">Klik på Udlign.</span><span class="sxs-lookup"><span data-stu-id="c81c2-111">Click Settle.</span></span>
3. <span data-ttu-id="c81c2-112">Klik på Afregn clearingpostering.</span><span class="sxs-lookup"><span data-stu-id="c81c2-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="c81c2-113">Udlign kreditorkontoen for checktransaktionen.</span><span class="sxs-lookup"><span data-stu-id="c81c2-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="c81c2-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c81c2-114">Close the page.</span></span>
5. <span data-ttu-id="c81c2-115">Gå til Finans > Kladdeposteringer > Finanskladder.</span><span class="sxs-lookup"><span data-stu-id="c81c2-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="c81c2-116">Vælg "Alle" i feltet Vis.</span><span class="sxs-lookup"><span data-stu-id="c81c2-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="c81c2-117">Marker eller fjern markeringen i afkrydsningsfeltet Vis kun kladder, der er oprettet af brugeren.</span><span class="sxs-lookup"><span data-stu-id="c81c2-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="c81c2-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c81c2-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c81c2-119">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="c81c2-119">Click Lines.</span></span>
10. <span data-ttu-id="c81c2-120">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="c81c2-120">Click Voucher.</span></span>
11. <span data-ttu-id="c81c2-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c81c2-121">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]