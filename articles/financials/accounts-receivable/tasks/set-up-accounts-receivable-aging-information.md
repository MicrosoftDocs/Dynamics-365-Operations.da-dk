--- 
title: "Opsætte og generere aldersfordelte oplysninger om debitorer"
description: "Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere."
author: mikefalkner
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 738df67c45b2e88f56ba0dffa7da19cbce6306b7
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="14ae2-103">Opsætte og generere aldersfordelte oplysninger om debitorer</span><span class="sxs-lookup"><span data-stu-id="14ae2-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14ae2-104">Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere.</span><span class="sxs-lookup"><span data-stu-id="14ae2-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="14ae2-105">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="14ae2-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="14ae2-106">Opret en definition af forældelsesperioder</span><span class="sxs-lookup"><span data-stu-id="14ae2-106">Create an aging period definition</span></span>
1. <span data-ttu-id="14ae2-107">Gå til Kredit > Opsætning > Definitioner af forældelsesperioder.</span><span class="sxs-lookup"><span data-stu-id="14ae2-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="14ae2-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="14ae2-108">Click New.</span></span>
3. <span data-ttu-id="14ae2-109">Indtast en værdi i feltet Definition på forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="14ae2-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="14ae2-110">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="14ae2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="14ae2-111">Klik på Tilføj under for at indsætte en ny forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="14ae2-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="14ae2-112">Indtast en beskrivelse, der skal vises i rapporter over forældelse, i feltet Periode.</span><span class="sxs-lookup"><span data-stu-id="14ae2-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="14ae2-113">Indtast et tal i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="14ae2-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="14ae2-114">Vælg en indstilling i feltet Interval.</span><span class="sxs-lookup"><span data-stu-id="14ae2-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="14ae2-115">Finansperiode svarer til perioden til finanskalenderen.</span><span class="sxs-lookup"><span data-stu-id="14ae2-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="14ae2-116">Dag, uge, måned, kvartal og år definerer størrelsen på intervallet efter datotype..</span><span class="sxs-lookup"><span data-stu-id="14ae2-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="14ae2-117">Ubegrænset vælger alle transaktioner før eller efter den forrige periode, alt efter om det er den første eller sidste periode.</span><span class="sxs-lookup"><span data-stu-id="14ae2-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="14ae2-118">Vælg en indstilling i feltet Aldersindikator.</span><span class="sxs-lookup"><span data-stu-id="14ae2-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="14ae2-119">Vælg perioden øverst i gitteret.</span><span class="sxs-lookup"><span data-stu-id="14ae2-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="14ae2-120">Opdater beskrivelsen for at beskrive den ældste periode i definitionen af forældelsesperioder</span><span class="sxs-lookup"><span data-stu-id="14ae2-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="14ae2-121">Angiv den nye beskrivelse af forældelsesperioden i feltet Periode.</span><span class="sxs-lookup"><span data-stu-id="14ae2-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="14ae2-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="14ae2-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="14ae2-123">Aldersfordel saldiene</span><span class="sxs-lookup"><span data-stu-id="14ae2-123">Age the balances</span></span>
1. <span data-ttu-id="14ae2-124">Gå til Kredit > Periodiske opgaver > Æld debitorsaldi.</span><span class="sxs-lookup"><span data-stu-id="14ae2-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="14ae2-125">I feltet Definition på forældelsesperiode skal du vælge den definition på forældelsesperiode, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="14ae2-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="14ae2-126">Du kan have ét aktivt øjebliksbillede for hver definition af forældelsesperioder.</span><span class="sxs-lookup"><span data-stu-id="14ae2-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="14ae2-127">Alle kunder behandles som standard.</span><span class="sxs-lookup"><span data-stu-id="14ae2-127">All customers are processed by default.</span></span> <span data-ttu-id="14ae2-128">Du kan bruge denne udvælgelse til at beregne en enkelt samlings kundepulje.</span><span class="sxs-lookup"><span data-stu-id="14ae2-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="14ae2-129">Vælg datoen fra den transaktion, du vil bruge til aldersfordelingen.</span><span class="sxs-lookup"><span data-stu-id="14ae2-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="14ae2-130">Vælg en "pr."-dato for aldersfordeling.</span><span class="sxs-lookup"><span data-stu-id="14ae2-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="14ae2-131">I dag er standard, men hvis du ændrer feltet til Valgt dato, kan du vælge den dato, du vil.</span><span class="sxs-lookup"><span data-stu-id="14ae2-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="14ae2-132">Du kan bruge Dags dato til batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="14ae2-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="14ae2-133">Udvid området Firma.</span><span class="sxs-lookup"><span data-stu-id="14ae2-133">Expand the Company range.</span></span> <span data-ttu-id="14ae2-134">Du kan vælge de firmaer, der skal medtages i øjebliksbilledet.</span><span class="sxs-lookup"><span data-stu-id="14ae2-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="14ae2-135">Det aktuelle firma er valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="14ae2-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="14ae2-136">Klik på OK for at behandle øjebliksbilledet.</span><span class="sxs-lookup"><span data-stu-id="14ae2-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="14ae2-137">Det vil tage et stykke tid, så vent på, at skyderen forsvinder, og kontrollér, om der er en meddelelse i Meddelelsescenter.</span><span class="sxs-lookup"><span data-stu-id="14ae2-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="14ae2-138">Få vist saldi på listen aldersfordelte saldi og på siden Rykker</span><span class="sxs-lookup"><span data-stu-id="14ae2-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="14ae2-139">Gå til Kredit > Rykkere > Aldersfordelte saldi.</span><span class="sxs-lookup"><span data-stu-id="14ae2-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="14ae2-140">Listesiden viser saldi for kunden.</span><span class="sxs-lookup"><span data-stu-id="14ae2-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="14ae2-141">Ikonet for aldersfordeling viser forældelsesperioden for den ældste transaktion.</span><span class="sxs-lookup"><span data-stu-id="14ae2-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="14ae2-142">Vælg en kunde med en saldo.</span><span class="sxs-lookup"><span data-stu-id="14ae2-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="14ae2-143">Udvid faktaboksen Aldersfordeling for at få vist de aldersfordelte saldi.</span><span class="sxs-lookup"><span data-stu-id="14ae2-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="14ae2-144">Definitionen af forældelsesperioden for faktaboksen hentes fra den definition af standardforældelsesperiode, som er angivet i parametrene.</span><span class="sxs-lookup"><span data-stu-id="14ae2-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="14ae2-145">Du kan ændre den ved hjælp af menuen Indsaml.</span><span class="sxs-lookup"><span data-stu-id="14ae2-145">You can change it using the Collect menu.</span></span>  


