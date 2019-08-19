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
ms.openlocfilehash: 6ed76f82532d43a3c05b60b12176fe851e327956
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846217"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="a77e6-103">Udligne posteringer mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="a77e6-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a77e6-104">Denne procedure viser, hvordan du udligner posteringer mellem finanskonti og annullerer en finansudligning.</span><span class="sxs-lookup"><span data-stu-id="a77e6-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="a77e6-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="a77e6-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="a77e6-106">Udligne postering mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="a77e6-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="a77e6-107">Gå til Finans > Periodiske opgaver > Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="a77e6-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="a77e6-108">Find den postering, du vil udligne, på listen.</span><span class="sxs-lookup"><span data-stu-id="a77e6-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="a77e6-109">Beløbssaldoen skal være nul.</span><span class="sxs-lookup"><span data-stu-id="a77e6-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="a77e6-110">Klik på Medtag.</span><span class="sxs-lookup"><span data-stu-id="a77e6-110">Click Include.</span></span>
4. <span data-ttu-id="a77e6-111">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="a77e6-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="a77e6-112">Annullere en finansudligning</span><span class="sxs-lookup"><span data-stu-id="a77e6-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="a77e6-113">Gå til Finans > Forespørgsler og rapporter > Råbalance.</span><span class="sxs-lookup"><span data-stu-id="a77e6-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="a77e6-114">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a77e6-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="a77e6-115">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="a77e6-115">Click Update.</span></span>
4. <span data-ttu-id="a77e6-116">Find den konto, der har den udlignede postering.</span><span class="sxs-lookup"><span data-stu-id="a77e6-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="a77e6-117">Klik på Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="a77e6-117">Click All transactions.</span></span>
6. <span data-ttu-id="a77e6-118">Brug et filter til nemt at finde posteringen på listen.</span><span class="sxs-lookup"><span data-stu-id="a77e6-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="a77e6-119">Klik på Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="a77e6-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="a77e6-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a77e6-120">In the list, mark the selected row.</span></span>

