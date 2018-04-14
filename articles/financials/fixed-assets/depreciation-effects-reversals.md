---
title: "Virkninger af afskrivninger med tilbageførsler"
description: "I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 786fad1ced1d6d4608b9852c300824ff4f795362
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="34907-103">Virkninger af afskrivninger med tilbageførsler</span><span class="sxs-lookup"><span data-stu-id="34907-103">Depreciation effects with reversals</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="34907-104">I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion.</span><span class="sxs-lookup"><span data-stu-id="34907-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="34907-105">Du kan tilbageføre anlægsaktivposteringer og de transaktioner, der er knyttet til et anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="34907-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="34907-106">Du kan også annullere en tilbageført postering.</span><span class="sxs-lookup"><span data-stu-id="34907-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="34907-107">Du kan tilbageføre eller tilbagekalde en transaktion, der ikke er den seneste transaktion, som er bogført i modellen for aktivet.</span><span class="sxs-lookup"><span data-stu-id="34907-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="34907-108">Du skal først afgøre, om der er blevet bogført nogen afskrivningsposteringer efter den postering, du vil tilbageføre.</span><span class="sxs-lookup"><span data-stu-id="34907-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="34907-109">Det skyldes, at afskrivning ikke genberegnes, når du tilbagefører en postering.</span><span class="sxs-lookup"><span data-stu-id="34907-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="34907-110">Afskrivningen vil derfor ofte blive overvurderet eller undervurderet efter tilbageførslen, som det fremgår af eksemplerne.</span><span class="sxs-lookup"><span data-stu-id="34907-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="34907-111">Hvis du vil sikre, at afskrivningen er korrekt, når du tilbagefører en postering, skal du ikke fortsætte med tilbageførslen, hvis du modtager en besked om, at afskrivningen ikke genberegnes.</span><span class="sxs-lookup"><span data-stu-id="34907-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="34907-112">Du skal i stedet først tilbageføre den afskrivningspostering, der blev bogført efter den postering, du prøvede at tilbageføre, og derefter fortsætte med tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="34907-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="34907-113">Du bliver ikke advaret om genberegning af afskrivningen, og du kan fortsætte med tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="34907-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="34907-114">I nedenstående eksempler vises de beregninger, der forekommer, hvis du fortsætter efter advarslen uden først at tilbageføre afskrivningsposteringerne.</span><span class="sxs-lookup"><span data-stu-id="34907-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="34907-115">Eksempel 1: Afskrivningen overvurderes</span><span class="sxs-lookup"><span data-stu-id="34907-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="34907-116">Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="34907-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="34907-117">I dette eksempel overvurderes afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="34907-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="34907-118">Posteringshistorik for aktiv</span><span class="sxs-lookup"><span data-stu-id="34907-118">Asset transaction history</span></span>

| <span data-ttu-id="34907-119">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-119">Date</span></span>       | <span data-ttu-id="34907-120">Posttype</span><span class="sxs-lookup"><span data-stu-id="34907-120">Transaction type</span></span>                                                          | <span data-ttu-id="34907-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="34907-122">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-122">January 1</span></span>  | <span data-ttu-id="34907-123">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="34907-123">Acquisition</span></span>                                                               | <span data-ttu-id="34907-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-124">59,000.00</span></span>                                 |
| <span data-ttu-id="34907-125">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-125">January 1</span></span>  | <span data-ttu-id="34907-126">Anskaffelsesregulering</span><span class="sxs-lookup"><span data-stu-id="34907-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="34907-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-127">1,000.00</span></span>                                  |
| <span data-ttu-id="34907-128">31. januar</span><span class="sxs-lookup"><span data-stu-id="34907-128">January 31</span></span> | <span data-ttu-id="34907-129">Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="34907-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="34907-130">1.000,00Beregning: Bogført værdi (59.000 + 1.000) / Antal resterende afskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="34907-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="34907-131">Tilbageførselshandling</span><span class="sxs-lookup"><span data-stu-id="34907-131">Reversal action</span></span>

| <span data-ttu-id="34907-132">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-132">Date</span></span>      | <span data-ttu-id="34907-133">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="34907-133">Transaction type</span></span>                | <span data-ttu-id="34907-134">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="34907-135">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-135">January 1</span></span> | <span data-ttu-id="34907-136">Tilbageførsel af anskaffelsesregulering</span><span class="sxs-lookup"><span data-stu-id="34907-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="34907-137">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="34907-138">Virkning af afskrivning</span><span class="sxs-lookup"><span data-stu-id="34907-138">Depreciation effect</span></span>

| <span data-ttu-id="34907-139">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-139">Date</span></span>        | <span data-ttu-id="34907-140">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="34907-140">Transaction type</span></span>        | <span data-ttu-id="34907-141">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34907-142">28. februar</span><span class="sxs-lookup"><span data-stu-id="34907-142">February 28</span></span> | <span data-ttu-id="34907-143">Afskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="34907-143">Depreciation (proposal)</span></span> | <span data-ttu-id="34907-144">983,05Beregning: Bogført værdi (59.000 - 1.000 afskrivning) / Antal resterende afskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="34907-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="34907-145">Afskrivningen er overvurderet med 16,95 (1.000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="34907-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="34907-146">Eksempel 2: Afskrivningen undervurderes</span><span class="sxs-lookup"><span data-stu-id="34907-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="34907-147">Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="34907-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="34907-148">I dette eksempel undervurderes afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="34907-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="34907-149">Posteringshistorik for aktiv</span><span class="sxs-lookup"><span data-stu-id="34907-149">Asset transaction history</span></span>

| <span data-ttu-id="34907-150">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-150">Date</span></span>       | <span data-ttu-id="34907-151">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="34907-151">Transaction type</span></span>                                                          | <span data-ttu-id="34907-152">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="34907-153">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-153">January 1</span></span>  | <span data-ttu-id="34907-154">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="34907-154">Acquisition</span></span>                                                               | <span data-ttu-id="34907-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-155">59,000.00</span></span>                                   |
| <span data-ttu-id="34907-156">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-156">January 1</span></span>  | <span data-ttu-id="34907-157">Nedskrivningsregulering</span><span class="sxs-lookup"><span data-stu-id="34907-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="34907-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-158">1,000.00</span></span>                                    |
| <span data-ttu-id="34907-159">31. januar</span><span class="sxs-lookup"><span data-stu-id="34907-159">January 31</span></span> | <span data-ttu-id="34907-160">Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="34907-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="34907-161">966,67Beregning: Bogført værdi (59.000 - 1.000) / Antal resterende afskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="34907-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="34907-162">Tilbageførselshandling</span><span class="sxs-lookup"><span data-stu-id="34907-162">Reversal action</span></span>

| <span data-ttu-id="34907-163">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-163">Date</span></span>      | <span data-ttu-id="34907-164">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="34907-164">Transaction type</span></span>               | <span data-ttu-id="34907-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="34907-166">1. januar</span><span class="sxs-lookup"><span data-stu-id="34907-166">January 1</span></span> | <span data-ttu-id="34907-167">Tilbageførsel af nedskrivningsregulering</span><span class="sxs-lookup"><span data-stu-id="34907-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="34907-168">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="34907-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="34907-169">Virkning af afskrivning</span><span class="sxs-lookup"><span data-stu-id="34907-169">Depreciation effect</span></span>

| <span data-ttu-id="34907-170">Dato</span><span class="sxs-lookup"><span data-stu-id="34907-170">Date</span></span>        | <span data-ttu-id="34907-171">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="34907-171">Transaction type</span></span>        | <span data-ttu-id="34907-172">Beløb</span><span class="sxs-lookup"><span data-stu-id="34907-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="34907-173">28. februar</span><span class="sxs-lookup"><span data-stu-id="34907-173">February 28</span></span> | <span data-ttu-id="34907-174">Afskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="34907-174">Depreciation (proposal)</span></span> | <span data-ttu-id="34907-175">983,62Beregning: Bogført værdi (59.000 - 966,67 afskrivning) / Antal resterende afskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="34907-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="34907-176">Afskrivningen er undervurderet med 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="34907-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="see-also"></a><span data-ttu-id="34907-177">Se også</span><span class="sxs-lookup"><span data-stu-id="34907-177">See also</span></span>
--------

[<span data-ttu-id="34907-178">Afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="34907-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




