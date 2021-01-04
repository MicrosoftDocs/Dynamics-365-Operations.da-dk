---
title: Oprette leasingbøger
description: I dette emne beskrives de oplysninger, der vedligeholdes i leasingkartoteker. Leasingkartoteker indeholder de regnskabspolitikker, der bestemmer, hvordan en leasingaftale redegøres for i systemet.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441758"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="f75c3-104">Oprette leasingbøger</span><span class="sxs-lookup"><span data-stu-id="f75c3-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f75c3-105">Leasingkartoteker indeholder de regnskabspolitikker, der bestemmer, hvordan en leasingaftale redegøres for i systemet.</span><span class="sxs-lookup"><span data-stu-id="f75c3-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="f75c3-106">Ud over bogføring af kontant grundlag understøtter aktivleasing følgende standarder:</span><span class="sxs-lookup"><span data-stu-id="f75c3-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="f75c3-107">Almindeligt anerkendte regnskabsprincipper i USA (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="f75c3-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="f75c3-108">Accounting Standards Codification Topic 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="f75c3-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="f75c3-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="f75c3-109">ASC 840</span></span>
- <span data-ttu-id="f75c3-110">International Financial Reporting Standard 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="f75c3-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="f75c3-111">International bogholderi standard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="f75c3-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="f75c3-112">Du kan oprette et nyt leasingkartotek ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f75c3-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="f75c3-113">Gå til **Aktivleasing \> Konfiguration \> Leasingkartotek**.</span><span class="sxs-lookup"><span data-stu-id="f75c3-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="f75c3-114">Vælg **Ny** for at tilføje et kartotek.</span><span class="sxs-lookup"><span data-stu-id="f75c3-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="f75c3-115">Angiv følgende felter.</span><span class="sxs-lookup"><span data-stu-id="f75c3-115">Set the following fields.</span></span>

    | <span data-ttu-id="f75c3-116">Navn</span><span class="sxs-lookup"><span data-stu-id="f75c3-116">Name</span></span>                                     | <span data-ttu-id="f75c3-117">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f75c3-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="f75c3-118">Posteringslag</span><span class="sxs-lookup"><span data-stu-id="f75c3-118">Posting layer</span></span>                            | <span data-ttu-id="f75c3-119">Vælg det posteringslag, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="f75c3-119">Select the posting layer to use.</span></span> <span data-ttu-id="f75c3-120">Hvert enkelt kartotek, der er tilknyttet en leasingaftale, konfigureres for et bestemt posteringslag.</span><span class="sxs-lookup"><span data-stu-id="f75c3-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="f75c3-121">Hvert posteringslag har forskellige bogføringsformål.</span><span class="sxs-lookup"><span data-stu-id="f75c3-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="f75c3-122">Leasingtype</span><span class="sxs-lookup"><span data-stu-id="f75c3-122">Lease type</span></span>                               | <span data-ttu-id="f75c3-123">Vælg, om leasingaftalen skal klassificeres automatisk, eller om den skal foruddefineres som finansierings- eller driftsleasingaftale.</span><span class="sxs-lookup"><span data-stu-id="f75c3-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="f75c3-124">Regnskabsstruktur</span><span class="sxs-lookup"><span data-stu-id="f75c3-124">Accounting framework</span></span>                     | <span data-ttu-id="f75c3-125">Vælg den struktur, der er tilknyttet kartoteket.</span><span class="sxs-lookup"><span data-stu-id="f75c3-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="f75c3-126">Konfiguration af leasingperiode/brugstid</span><span class="sxs-lookup"><span data-stu-id="f75c3-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="f75c3-127">Systemet klassificerer leasingaftalen som finansiel, hvis leasingtypen er angivet til **Automatisk**, og hvis leasingperioden for aktivets brugstid er større end eller lig med den procent, der er defineret i dette felt.</span><span class="sxs-lookup"><span data-stu-id="f75c3-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="f75c3-128">Konfiguration af nutidsværdi/handelsværdi af aktiv</span><span class="sxs-lookup"><span data-stu-id="f75c3-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="f75c3-129">Angiv et heltal for at definere den tærskel, der bestemmer, hvilken leasingtype der skal bestemmes.</span><span class="sxs-lookup"><span data-stu-id="f75c3-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="f75c3-130">Hvis den nuværende værdi af fremtidige minimums leasingbetalinger er større end den brugerdefinerede værdi fra opsætningen af kartoteket, og hvis kartotekets leasingklassifikation er indstillet til automatisk, klassificerer systemet leasingaftalen som en finansieringsleasing.</span><span class="sxs-lookup"><span data-stu-id="f75c3-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="f75c3-131">Kortsigtet grænse</span><span class="sxs-lookup"><span data-stu-id="f75c3-131">Short-term threshold</span></span>                     | <span data-ttu-id="f75c3-132">Angiv det antal måneder, der skal bruges som tærskel for kortfristede leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="f75c3-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="f75c3-133">Hvis leasingperioden er mindre end eller lig med det antal måneder, du angiver her, klassificerer systemet leasingaftalen som en kortfristet leasingaftale, og den udskudte lejebehandling anvendes.</span><span class="sxs-lookup"><span data-stu-id="f75c3-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="f75c3-134">Grænseværdi for lav værdi</span><span class="sxs-lookup"><span data-stu-id="f75c3-134">Low value threshold</span></span>                      | <span data-ttu-id="f75c3-135">Angiv et beløb, der skal bruges som en tærskel for leasingaftaler med lav værdi.</span><span class="sxs-lookup"><span data-stu-id="f75c3-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="f75c3-136">Hvis aktivets rimelige værdi er mindre end eller lig med den værdi, du angiver her, klassificerer systemet leasingaftalen som en lavværdileasingaftale, og den udskudte lejebehandling anvendes.</span><span class="sxs-lookup"><span data-stu-id="f75c3-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="f75c3-137">Betal til kreditor</span><span class="sxs-lookup"><span data-stu-id="f75c3-137">Pay to vendor</span></span>                            | <span data-ttu-id="f75c3-138">Angiv denne indstilling til **Ja** for at tillade, at leasingbetalinger bogføres som en faktura til den kreditorkonto, der er angivet for hver leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="f75c3-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="f75c3-139">Når en leasingbetaling bogføres, vil kreditorkontoen blive krediteret.</span><span class="sxs-lookup"><span data-stu-id="f75c3-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="f75c3-140">Hvis denne indstilling er angivet til **Nej**, krediteres den konto, der er angivet for **Leasingbetaling**-bogføringstypen for siden **Leasingbogføringsparametre** i stedet.</span><span class="sxs-lookup"><span data-stu-id="f75c3-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
