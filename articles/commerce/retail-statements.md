---
title: Detailopgørelser
description: I dette emne beskrives, hvordan opgørelser oprettes og bogføres.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022028"
---
# <a name="retail-statements"></a><span data-ttu-id="e2d19-103">Detailopgørelser</span><span class="sxs-lookup"><span data-stu-id="e2d19-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2d19-104">I Dynamics 365 Commerce bruges processen til bogføring af opgørelsen til at redegøre for de transaktioner, der opstår i Cloud POS eller MPOS (Modern POS).</span><span class="sxs-lookup"><span data-stu-id="e2d19-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="e2d19-105">Opgørelsesbogføringsprocessen bruger distributionsplanen til at trække en række POS-transaktioner til Headquarters-klienten (HQ).</span><span class="sxs-lookup"><span data-stu-id="e2d19-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="e2d19-106">De parametre, der er defineret på siden **Commerce-parametre** og **Butikker**, bruges til at vælge de transaktioner, der trækkes til hver enkelt opgørelse.</span><span class="sxs-lookup"><span data-stu-id="e2d19-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="e2d19-107">Følgende illustration viser til opgørelsesbogføringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="e2d19-108">I denne proces overføres transaktioner, der er registreret i POS, til klienten ved hjælp af Commerce-planlægger.</span><span class="sxs-lookup"><span data-stu-id="e2d19-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="e2d19-109">Når klienten modtager transaktionerne, kan du oprette, beregne og bogføre transaktionsopgørelsen for butikken.</span><span class="sxs-lookup"><span data-stu-id="e2d19-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="e2d19-110">[![Opgørelsesbogføringsproces](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="e2d19-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="e2d19-111">Oprettelse og bogføring af opgørelser</span><span class="sxs-lookup"><span data-stu-id="e2d19-111">Creating and posting statements</span></span>

<span data-ttu-id="e2d19-112">Du kan oprette en opgørelse manuelt eller ved at bruge batchprocesser, som du opretter, så de køres regelmæssigt i løbet af dagen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="e2d19-113">I begge tilfælde bruges følgende trin til at oprette og bogføre opgørelser.</span><span class="sxs-lookup"><span data-stu-id="e2d19-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="e2d19-114">Oprette opgørelsen</span><span class="sxs-lookup"><span data-stu-id="e2d19-114">Create the statement</span></span>

<span data-ttu-id="e2d19-115">Dette trin identificerer den butik, som opgørelsen oprettes til manuelt.</span><span class="sxs-lookup"><span data-stu-id="e2d19-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="e2d19-116">Hvis du konfigurerer en batchproces, kan du automatisk oprette opgørelser til alle butikker på basis af en plan, som du definerer.</span><span class="sxs-lookup"><span data-stu-id="e2d19-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="e2d19-117">Beregne opgørelsen</span><span class="sxs-lookup"><span data-stu-id="e2d19-117">Calculate the statement</span></span>

<span data-ttu-id="e2d19-118">I dette trin vælges transaktionslinjer på baggrund af kriterier, der er defineret for hver butik på siderne **Commerce-parametre** og **Butikker**.</span><span class="sxs-lookup"><span data-stu-id="e2d19-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="e2d19-119">På disse sider kan du definere kriterierne og angive, hvordan transaktionerne skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="e2d19-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="e2d19-120">Du kan bruge siden **Transaktioner** til at få vist en liste over de transaktioner, der er medtaget i opgørelsen, før du beregner opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="e2d19-121">Ved beregningen af opgørelsen bruges kasseoptællinger fra kasseapparaterne som optalt beløb.</span><span class="sxs-lookup"><span data-stu-id="e2d19-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="e2d19-122">Du kan også angive det optalte beløb manuelt.</span><span class="sxs-lookup"><span data-stu-id="e2d19-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="e2d19-123">Opgørelsen viser differencen mellem salgsbeløbet for transaktionerne og det faktisk optalte beløb for alle betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="e2d19-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="e2d19-124">Opgørelsen vil kun blive bogført, hvis denne difference er mindre end den maksimale bogføringsdifference, der er defineret for butikken.</span><span class="sxs-lookup"><span data-stu-id="e2d19-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d19-125">Opgørelsesberegningsprocessen bruger den globale nummerserie.</span><span class="sxs-lookup"><span data-stu-id="e2d19-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="e2d19-126">Når du beregner en opgørelse, omfatter beregningen følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="e2d19-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="e2d19-127">For det valgte datointerval skal du markere de transaktioner, der ikke er medtaget i en tidligere opgørelsesberegning.</span><span class="sxs-lookup"><span data-stu-id="e2d19-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="e2d19-128">Beregn de samlede beløb, der blev tilbudt i de valgte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="e2d19-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="e2d19-129">Resultaterne vises i opgørelseslinjerne afhængigt af opgørelsesmetoden:</span><span class="sxs-lookup"><span data-stu-id="e2d19-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="e2d19-130">Hvis opgørelsesmetoden er **Sum**, oprettes der en linje for hver betalingsmetode i de valgte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="e2d19-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="e2d19-131">Hvis opgørelsesmetoden er **Personale**, oprettes der en linje for hver betalingsmetode i transaktioner, der er udført af den valgte medarbejder.</span><span class="sxs-lookup"><span data-stu-id="e2d19-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="e2d19-132">Hvis opgørelsesmetoden er **POS-klient**, oprettes der en linje for hver betalingsmetode i transaktioner, der blev udført i det valgte register.</span><span class="sxs-lookup"><span data-stu-id="e2d19-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="e2d19-133">Hvis opgørelsesmetoden er **Skift**, oprettes der en linje for hver betalingsmetode i transaktioner, der blev udført under et skift.</span><span class="sxs-lookup"><span data-stu-id="e2d19-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="e2d19-134">Hvis afkrydsningsfeltet **Opdel efter opgørelsesmetode** er markeret på siden **Butikker**, oprettes en separat opgørelse ud fra den værdi, der er valgt i feltet **Opgørelsesmetode**.</span><span class="sxs-lookup"><span data-stu-id="e2d19-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="e2d19-135">Hvis der er åbent i din butik til efter midnat, kan du bogføre opgørelsesbogføringen, så den er baseret på slutningen på forretningsdagen i stedet for udløbet af kalenderdagen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="e2d19-136">På siden **Butikker** i oversigtspanelet **Opgørelse/ultimo** skal du i feltet **Afslutning på forretningsdag** angive det tidspunkt, hvor den sidste transaktion skal registreres for at blive medtaget i opgørelsen af forretningsdagen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="e2d19-137">Markér afkrydsningsfeltet **Bogfør som arbejdsdag** for at bogføre transaktioner inden for samme forretningsdag.</span><span class="sxs-lookup"><span data-stu-id="e2d19-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="e2d19-138">Når opgørelsen bogføres, kan transaktioner, der er registreret inden for samme forretningsdag, medtages på den samme salgsordre, selvom nogle transaktioner forekommer før midnat og nogle transaktioner efter midnat.</span><span class="sxs-lookup"><span data-stu-id="e2d19-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="e2d19-139">Eksempel: Bogfør en opgørelse for en forretningsdag, der strækker sig over to kalenderdage</span><span class="sxs-lookup"><span data-stu-id="e2d19-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="e2d19-140">En butik er åben mellem 8:00 og 3:00, og feltet **Bogfør som arbejdsdag** er markeret i butikkens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2d19-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="e2d19-141">Den 31. maj bogfører butikken transaktioner mellem 8:00 og midnat.</span><span class="sxs-lookup"><span data-stu-id="e2d19-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="e2d19-142">Butikken posterer også transaktioner mellem 12:01 og 3:00 den 1. juni.</span><span class="sxs-lookup"><span data-stu-id="e2d19-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="e2d19-143">Når butikken bogfører sin opgørelse ved afslutningen af forretningsdagen, indeholder den salgsordre, der oprettes, alle transaktioner, der er registreret i åbningstiden mellem kl. 08:00 og kl. 03:00, selvom transaktionerne fandt sted på datoer, d. 31. maj og d. 1. juni.</span><span class="sxs-lookup"><span data-stu-id="e2d19-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="e2d19-144">Hvis afkrydsningsfeltet **Bogfør som arbejdsdag** ikke er markeret for den samme butik, oprettes der separate salgsordrer, når butikken bogfører sin opgørelse ved afslutningen af forretningsdagen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="e2d19-145">Én salgsordre, der indeholder de transaktioner, der er registreret mellem åbningstiderne mellem kl. 08.00 og midnat d. 31, maj, og en anden salgsordre, der indeholder de transaktioner, der er registreret i forretningstiden mellem kl. 12:01 og kl. 03:00 d. 1. juni.</span><span class="sxs-lookup"><span data-stu-id="e2d19-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="e2d19-146">Før du kan oprette opgørelser, skal du lukke skiftene i opgørelsesperioden.</span><span class="sxs-lookup"><span data-stu-id="e2d19-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="e2d19-147">Bogføre opgørelsen</span><span class="sxs-lookup"><span data-stu-id="e2d19-147">Post the statement</span></span>

<span data-ttu-id="e2d19-148">Når du bogfører en opgørelse, oprettes der salgsordrer og fakturaer for salg i opgørelsen.</span><span class="sxs-lookup"><span data-stu-id="e2d19-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="e2d19-149">Salg efter princippet "kontant og afhentet" er samlet på én salgsordre og faktureret til den standardkunde, der er knyttet til butikken.</span><span class="sxs-lookup"><span data-stu-id="e2d19-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="e2d19-150">Salg, for hvilket der blev føjet en kunde til transaktionen i POS, genererer separate salgsordrer og fakturaer – én for hver entydig kunde.</span><span class="sxs-lookup"><span data-stu-id="e2d19-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="e2d19-151">Der oprettes automatisk betalingskladder for betalingerne i opgørelsen, og lageret opdateres for POS-butikken.</span><span class="sxs-lookup"><span data-stu-id="e2d19-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>