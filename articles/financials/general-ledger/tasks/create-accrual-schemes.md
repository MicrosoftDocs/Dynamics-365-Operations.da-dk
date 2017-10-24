--- 
title: Oprette periodiseringsskemaer
description: "Denne opgaveguide gennemgår oprettelse af en periodiseringsskema."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="96fef-103">Oprette periodiseringsskemaer</span><span class="sxs-lookup"><span data-stu-id="96fef-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96fef-104">Denne opgaveguide gennemgår oprettelse af en periodiseringsskema.</span><span class="sxs-lookup"><span data-stu-id="96fef-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="96fef-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="96fef-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="96fef-106">Gå til Finans > Kladdeopsætning > Periodiseringsskemaer.</span><span class="sxs-lookup"><span data-stu-id="96fef-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="96fef-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="96fef-107">Click New.</span></span>
3. <span data-ttu-id="96fef-108">Skriv en værdi i feltet Periodiseringsidentifikation.</span><span class="sxs-lookup"><span data-stu-id="96fef-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="96fef-109">Skriv en værdi i feltet Beskrivelse af periodiseringsskema.</span><span class="sxs-lookup"><span data-stu-id="96fef-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="96fef-110">I feltet Debet skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="96fef-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="96fef-111">Den hovedkonto, der defineres, erstatter debethovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="96fef-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="96fef-112">I feltet Kredit skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="96fef-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="96fef-113">Den hovedkonto, der defineres, erstatter kredithovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="96fef-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="96fef-114">I feltet Bilag skal du vælge, hvordan bilaget skal bestemmes, når transaktionerne bogføres.</span><span class="sxs-lookup"><span data-stu-id="96fef-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="96fef-115">I feltet Beskrivelse skal du skrive en værdi for at beskrive de transaktioner, der skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="96fef-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="96fef-116">I feltet Periodefrekvens skal du vælge, hvor ofte transaktionerne skal finde sted.</span><span class="sxs-lookup"><span data-stu-id="96fef-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="96fef-117">Angiv et tal i feltet Antal forekomster pr. periode.</span><span class="sxs-lookup"><span data-stu-id="96fef-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="96fef-118">I feltet Bogfør transaktioner skal du vælge, hvornår transaktionerne skal bogføres, f.eks. Månedligt.</span><span class="sxs-lookup"><span data-stu-id="96fef-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


