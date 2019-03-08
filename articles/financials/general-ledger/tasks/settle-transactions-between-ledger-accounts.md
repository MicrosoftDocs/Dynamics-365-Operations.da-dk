---
title: Udligne posteringer mellem finanskonti
description: Denne procedure viser, hvordan du udligner posteringer mellem finanskonti og annullerer en finansudligning.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "325819"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="eb18a-103">Udligne posteringer mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="eb18a-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb18a-104">Denne procedure viser, hvordan du udligner posteringer mellem finanskonti og annullerer en finansudligning.</span><span class="sxs-lookup"><span data-stu-id="eb18a-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="eb18a-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="eb18a-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="eb18a-106">Udligne postering mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="eb18a-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="eb18a-107">Gå til Finans > Periodiske opgaver > Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="eb18a-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="eb18a-108">Find den postering, du vil udligne, på listen.</span><span class="sxs-lookup"><span data-stu-id="eb18a-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="eb18a-109">Beløbssaldoen skal være nul.</span><span class="sxs-lookup"><span data-stu-id="eb18a-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="eb18a-110">Klik på Medtag.</span><span class="sxs-lookup"><span data-stu-id="eb18a-110">Click Include.</span></span>
4. <span data-ttu-id="eb18a-111">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="eb18a-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="eb18a-112">Annullere en finansudligning</span><span class="sxs-lookup"><span data-stu-id="eb18a-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="eb18a-113">Gå til Finans > Forespørgsler og rapporter > Råbalance.</span><span class="sxs-lookup"><span data-stu-id="eb18a-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="eb18a-114">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="eb18a-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="eb18a-115">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="eb18a-115">Click Update.</span></span>
4. <span data-ttu-id="eb18a-116">Find den konto, der har den udlignede postering.</span><span class="sxs-lookup"><span data-stu-id="eb18a-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="eb18a-117">Klik på Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eb18a-117">Click All transactions.</span></span>
6. <span data-ttu-id="eb18a-118">Brug et filter til nemt at finde posteringen på listen.</span><span class="sxs-lookup"><span data-stu-id="eb18a-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="eb18a-119">Klik på Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="eb18a-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="eb18a-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="eb18a-120">In the list, mark the selected row.</span></span>

