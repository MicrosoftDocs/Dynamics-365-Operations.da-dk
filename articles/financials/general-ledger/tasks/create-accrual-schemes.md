---
title: Oprette periodiseringsskemaer
description: Denne opgaveguide gennemgår oprettelse af en periodiseringsskema.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ae55000a5cf1593d057d940dc3dbbf9e5cb3f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834874"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="891db-103">Oprette periodiseringsskemaer</span><span class="sxs-lookup"><span data-stu-id="891db-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="891db-104">Denne opgaveguide gennemgår oprettelse af en periodiseringsskema.</span><span class="sxs-lookup"><span data-stu-id="891db-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="891db-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="891db-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="891db-106">Gå til Finans > Kladdeopsætning > Periodiseringsskemaer.</span><span class="sxs-lookup"><span data-stu-id="891db-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="891db-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="891db-107">Click New.</span></span>
3. <span data-ttu-id="891db-108">Skriv en værdi i feltet Periodiseringsidentifikation.</span><span class="sxs-lookup"><span data-stu-id="891db-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="891db-109">Skriv en værdi i feltet Beskrivelse af periodiseringsskema.</span><span class="sxs-lookup"><span data-stu-id="891db-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="891db-110">I feltet Debet skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="891db-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="891db-111">Den hovedkonto, der defineres, erstatter debethovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="891db-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="891db-112">I feltet Kredit skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="891db-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="891db-113">Den hovedkonto, der defineres, erstatter kredithovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="891db-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="891db-114">I feltet Bilag skal du vælge, hvordan bilaget skal bestemmes, når transaktionerne bogføres.</span><span class="sxs-lookup"><span data-stu-id="891db-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="891db-115">I feltet Beskrivelse skal du skrive en værdi for at beskrive de transaktioner, der skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="891db-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="891db-116">I feltet Periodefrekvens skal du vælge, hvor ofte transaktionerne skal finde sted.</span><span class="sxs-lookup"><span data-stu-id="891db-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="891db-117">Angiv et tal i feltet Antal forekomster pr. periode.</span><span class="sxs-lookup"><span data-stu-id="891db-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="891db-118">I feltet Bogfør transaktioner skal du vælge, hvornår transaktionerne skal bogføres, f.eks. Månedligt.</span><span class="sxs-lookup"><span data-stu-id="891db-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>

