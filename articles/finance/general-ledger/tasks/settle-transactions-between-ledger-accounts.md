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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144668"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="63d49-103">Udligne posteringer mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="63d49-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63d49-104">Denne procedure viser, hvordan du udligner posteringer mellem finanskonti og annullerer en finansudligning.</span><span class="sxs-lookup"><span data-stu-id="63d49-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="63d49-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="63d49-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="63d49-106">Udligne postering mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="63d49-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="63d49-107">Gå til Finans > Periodiske opgaver > Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="63d49-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="63d49-108">Find den postering, du vil udligne, på listen.</span><span class="sxs-lookup"><span data-stu-id="63d49-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="63d49-109">Beløbssaldoen skal være nul.</span><span class="sxs-lookup"><span data-stu-id="63d49-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="63d49-110">Klik på Medtag.</span><span class="sxs-lookup"><span data-stu-id="63d49-110">Click Include.</span></span>
4. <span data-ttu-id="63d49-111">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="63d49-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="63d49-112">Annullere en finansudligning</span><span class="sxs-lookup"><span data-stu-id="63d49-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="63d49-113">Gå til Finans > Forespørgsler og rapporter > Råbalance.</span><span class="sxs-lookup"><span data-stu-id="63d49-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="63d49-114">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="63d49-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="63d49-115">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="63d49-115">Click Update.</span></span>
4. <span data-ttu-id="63d49-116">Find den konto, der har den udlignede postering.</span><span class="sxs-lookup"><span data-stu-id="63d49-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="63d49-117">Klik på Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="63d49-117">Click All transactions.</span></span>
6. <span data-ttu-id="63d49-118">Brug et filter til nemt at finde posteringen på listen.</span><span class="sxs-lookup"><span data-stu-id="63d49-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="63d49-119">Klik på Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="63d49-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="63d49-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="63d49-120">In the list, mark the selected row.</span></span>

