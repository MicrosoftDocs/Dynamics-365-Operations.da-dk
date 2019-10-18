---
title: Oprette periodiseringsskemaer
description: Dette emne forklarer, hvordan du opretter et periodiseringsskema.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: e8f8cf8546187ae1c65d4966887e1c5842dff431
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175352"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="06591-103">Oprette periodiseringsskemaer</span><span class="sxs-lookup"><span data-stu-id="06591-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06591-104">Dette emne forklarer, hvordan du opretter et periodiseringsskema.</span><span class="sxs-lookup"><span data-stu-id="06591-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="06591-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="06591-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="06591-106">Gå til **Navigationsrude > Moduler > Finans > Konfiguration af kladde > Periodiseringsskemaer**.</span><span class="sxs-lookup"><span data-stu-id="06591-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="06591-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="06591-107">Select **New**.</span></span>
3. <span data-ttu-id="06591-108">Skriv en værdi i feltet **Periodiseringsidentifikation**.</span><span class="sxs-lookup"><span data-stu-id="06591-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="06591-109">Skriv en værdi i feltet **Beskrivelse af periodiseringsskema**.</span><span class="sxs-lookup"><span data-stu-id="06591-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="06591-110">I feltet **Debet** skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="06591-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="06591-111">Den hovedkonto, der defineres, erstatter debethovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="06591-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="06591-112">I feltet **Kredit** skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="06591-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="06591-113">Den hovedkonto, der defineres, erstatter kredithovedkontoen på kladdebilagslinjen, og det bruges også til tilbageførsel af den udelukkelse, der er baseret på posteringer til periodisering af finans.</span><span class="sxs-lookup"><span data-stu-id="06591-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="06591-114">I feltet **Bilag** skal du vælge, hvordan bilaget skal bestemmes, når transaktionerne bogføres.</span><span class="sxs-lookup"><span data-stu-id="06591-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="06591-115">I feltet **Beskrivelse** skal du skrive en værdi for at beskrive de transaktioner, der skal bogføres.</span><span class="sxs-lookup"><span data-stu-id="06591-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="06591-116">I feltet **Periodefrekvens** skal du vælge, hvor ofte transaktionerne skal finde sted.</span><span class="sxs-lookup"><span data-stu-id="06591-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="06591-117">Angiv et tal i feltet **Antal forekomster pr. periode**.</span><span class="sxs-lookup"><span data-stu-id="06591-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="06591-118">I feltet **Bogfør transaktioner** skal du vælge, hvornår transaktionerne skal bogføres, f.eks. **Månedligt**.</span><span class="sxs-lookup"><span data-stu-id="06591-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

