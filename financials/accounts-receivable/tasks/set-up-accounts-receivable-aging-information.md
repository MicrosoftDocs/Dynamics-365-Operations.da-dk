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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2e9f393acaa47d485a583b99ace459474f30be6a
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="eb630-103">Opsætte og generere aldersfordelte oplysninger om debitorer</span><span class="sxs-lookup"><span data-stu-id="eb630-103">Set up and generate accounts receivable aging information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb630-104">Denne guide hjælper dig med at oprette en definition af forældelsesperiode, aldersfordele kundesaldi og få vist saldi på listen Aldersfordelt saldo og siden Rykkere.</span><span class="sxs-lookup"><span data-stu-id="eb630-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="eb630-105">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="eb630-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="eb630-106">Opret en definition af forældelsesperioder</span><span class="sxs-lookup"><span data-stu-id="eb630-106">Create an aging period definition</span></span>
1. <span data-ttu-id="eb630-107">Gå til Kredit > Opsætning > Definitioner af forældelsesperioder.</span><span class="sxs-lookup"><span data-stu-id="eb630-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="eb630-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="eb630-108">Click New.</span></span>
3. <span data-ttu-id="eb630-109">Indtast en værdi i feltet Definition på forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="eb630-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="eb630-110">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="eb630-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eb630-111">Klik på Tilføj under for at indsætte en ny forældelsesperiode.</span><span class="sxs-lookup"><span data-stu-id="eb630-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="eb630-112">Indtast en beskrivelse, der skal vises i rapporter over forældelse, i feltet Periode.</span><span class="sxs-lookup"><span data-stu-id="eb630-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="eb630-113">Indtast et tal i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="eb630-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="eb630-114">Vælg en indstilling i feltet Interval.</span><span class="sxs-lookup"><span data-stu-id="eb630-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="eb630-115">Finansperiode svarer til perioden til finanskalenderen.</span><span class="sxs-lookup"><span data-stu-id="eb630-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="eb630-116">Dag, uge, måned, kvartal og år definerer størrelsen på intervallet efter datotype..</span><span class="sxs-lookup"><span data-stu-id="eb630-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="eb630-117">Ubegrænset vælger alle transaktioner før eller efter den forrige periode, alt efter om det er den første eller sidste periode.</span><span class="sxs-lookup"><span data-stu-id="eb630-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="eb630-118">Vælg en indstilling i feltet Aldersindikator.</span><span class="sxs-lookup"><span data-stu-id="eb630-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="eb630-119">Vælg perioden øverst i gitteret.</span><span class="sxs-lookup"><span data-stu-id="eb630-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="eb630-120">Opdater beskrivelsen for at beskrive den ældste periode i definitionen af forældelsesperioder</span><span class="sxs-lookup"><span data-stu-id="eb630-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="eb630-121">Angiv den nye beskrivelse af forældelsesperioden i feltet Periode.</span><span class="sxs-lookup"><span data-stu-id="eb630-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="eb630-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="eb630-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="eb630-123">Aldersfordel saldiene</span><span class="sxs-lookup"><span data-stu-id="eb630-123">Age the balances</span></span>
1. <span data-ttu-id="eb630-124">Gå til Kredit > Periodiske opgaver > Æld debitorsaldi.</span><span class="sxs-lookup"><span data-stu-id="eb630-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="eb630-125">I feltet Definition på forældelsesperiode skal du vælge den definition på forældelsesperiode, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="eb630-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="eb630-126">Du kan have ét aktivt øjebliksbillede for hver definition af forældelsesperioder.</span><span class="sxs-lookup"><span data-stu-id="eb630-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="eb630-127">Alle kunder behandles som standard.</span><span class="sxs-lookup"><span data-stu-id="eb630-127">All customers are processed by default.</span></span> <span data-ttu-id="eb630-128">Du kan bruge denne udvælgelse til at beregne en enkelt samlings kundepulje.</span><span class="sxs-lookup"><span data-stu-id="eb630-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="eb630-129">Vælg datoen fra den transaktion, du vil bruge til aldersfordelingen.</span><span class="sxs-lookup"><span data-stu-id="eb630-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="eb630-130">Vælg en "pr."-dato for aldersfordeling.</span><span class="sxs-lookup"><span data-stu-id="eb630-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="eb630-131">I dag er standard, men hvis du ændrer feltet til Valgt dato, kan du vælge den dato, du vil.</span><span class="sxs-lookup"><span data-stu-id="eb630-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="eb630-132">Du kan bruge Dags dato til batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="eb630-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="eb630-133">Udvid området Firma.</span><span class="sxs-lookup"><span data-stu-id="eb630-133">Expand the Company range.</span></span> <span data-ttu-id="eb630-134">Du kan vælge de firmaer, der skal medtages i øjebliksbilledet.</span><span class="sxs-lookup"><span data-stu-id="eb630-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="eb630-135">Det aktuelle firma er valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="eb630-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="eb630-136">Klik på OK for at behandle øjebliksbilledet.</span><span class="sxs-lookup"><span data-stu-id="eb630-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="eb630-137">Det vil tage et stykke tid, så vent på, at skyderen forsvinder, og kontrollér, om der er en meddelelse i Meddelelsescenter.</span><span class="sxs-lookup"><span data-stu-id="eb630-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="eb630-138">Få vist saldi på listen aldersfordelte saldi og på siden Rykker</span><span class="sxs-lookup"><span data-stu-id="eb630-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="eb630-139">Gå til Kredit > Rykkere > Aldersfordelte saldi.</span><span class="sxs-lookup"><span data-stu-id="eb630-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="eb630-140">Listesiden viser saldi for kunden.</span><span class="sxs-lookup"><span data-stu-id="eb630-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="eb630-141">Ikonet for aldersfordeling viser forældelsesperioden for den ældste transaktion.</span><span class="sxs-lookup"><span data-stu-id="eb630-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="eb630-142">Vælg en kunde med en saldo.</span><span class="sxs-lookup"><span data-stu-id="eb630-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="eb630-143">Udvid faktaboksen Aldersfordeling for at få vist de aldersfordelte saldi.</span><span class="sxs-lookup"><span data-stu-id="eb630-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="eb630-144">Definitionen af forældelsesperioden for faktaboksen hentes fra den definition af standardforældelsesperiode, som er angivet i parametrene.</span><span class="sxs-lookup"><span data-stu-id="eb630-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="eb630-145">Du kan ændre den ved hjælp af menuen Indsaml.</span><span class="sxs-lookup"><span data-stu-id="eb630-145">You can change it using the Collect menu.</span></span>  


