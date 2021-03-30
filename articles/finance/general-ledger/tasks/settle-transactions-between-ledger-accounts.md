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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222089"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="abcf2-103">Udligne posteringer mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="abcf2-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abcf2-104">Denne procedure viser, hvordan du udligner posteringer mellem finanskonti og annullerer en finansudligning.</span><span class="sxs-lookup"><span data-stu-id="abcf2-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="abcf2-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="abcf2-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="abcf2-106">Udligne postering mellem finanskonti</span><span class="sxs-lookup"><span data-stu-id="abcf2-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="abcf2-107">Gå til Finans > Periodiske opgaver > Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="abcf2-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="abcf2-108">Find den postering, du vil udligne, på listen.</span><span class="sxs-lookup"><span data-stu-id="abcf2-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="abcf2-109">Beløbssaldoen skal være nul.</span><span class="sxs-lookup"><span data-stu-id="abcf2-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="abcf2-110">Klik på Medtag.</span><span class="sxs-lookup"><span data-stu-id="abcf2-110">Click Include.</span></span>
4. <span data-ttu-id="abcf2-111">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="abcf2-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="abcf2-112">Annullere en finansudligning</span><span class="sxs-lookup"><span data-stu-id="abcf2-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="abcf2-113">Gå til Finans > Forespørgsler og rapporter > Råbalance.</span><span class="sxs-lookup"><span data-stu-id="abcf2-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="abcf2-114">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="abcf2-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="abcf2-115">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="abcf2-115">Click Update.</span></span>
4. <span data-ttu-id="abcf2-116">Find den konto, der har den udlignede postering.</span><span class="sxs-lookup"><span data-stu-id="abcf2-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="abcf2-117">Klik på Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="abcf2-117">Click All transactions.</span></span>
6. <span data-ttu-id="abcf2-118">Brug et filter til nemt at finde posteringen på listen.</span><span class="sxs-lookup"><span data-stu-id="abcf2-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="abcf2-119">Klik på Finansudligninger.</span><span class="sxs-lookup"><span data-stu-id="abcf2-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="abcf2-120">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="abcf2-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]