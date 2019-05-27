---
title: Virkninger af afskrivninger med tilbageførsler
description: I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d624fa998329680d9fa471fa325f6fcfd3920c6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556289"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="6e132-103">Virkninger af afskrivninger med tilbageførsler</span><span class="sxs-lookup"><span data-stu-id="6e132-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e132-104">I denne artikel beskrives mulige konsekvenser af tilbageførsel af en anlægsaktivtransaktion.</span><span class="sxs-lookup"><span data-stu-id="6e132-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="6e132-105">Du kan tilbageføre anlægsaktivposteringer og de transaktioner, der er knyttet til et anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="6e132-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="6e132-106">Du kan også annullere en tilbageført postering.</span><span class="sxs-lookup"><span data-stu-id="6e132-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="6e132-107">Du kan tilbageføre eller tilbagekalde en transaktion, der ikke er den seneste transaktion, som er bogført i modellen for aktivet.</span><span class="sxs-lookup"><span data-stu-id="6e132-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="6e132-108">Du skal først afgøre, om der er blevet bogført nogen afskrivningsposteringer efter den postering, du vil tilbageføre.</span><span class="sxs-lookup"><span data-stu-id="6e132-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="6e132-109">Det skyldes, at afskrivning ikke genberegnes, når du tilbagefører en postering.</span><span class="sxs-lookup"><span data-stu-id="6e132-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="6e132-110">Afskrivningen vil derfor ofte blive overvurderet eller undervurderet efter tilbageførslen, som det fremgår af eksemplerne.</span><span class="sxs-lookup"><span data-stu-id="6e132-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="6e132-111">Hvis du vil sikre, at afskrivningen er korrekt, når du tilbagefører en postering, skal du ikke fortsætte med tilbageførslen, hvis du modtager en besked om, at afskrivningen ikke genberegnes.</span><span class="sxs-lookup"><span data-stu-id="6e132-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="6e132-112">Du skal i stedet først tilbageføre den afskrivningspostering, der blev bogført efter den postering, du prøvede at tilbageføre, og derefter fortsætte med tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="6e132-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="6e132-113">Du bliver ikke advaret om genberegning af afskrivningen, og du kan fortsætte med tilbageførslen.</span><span class="sxs-lookup"><span data-stu-id="6e132-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="6e132-114">I nedenstående eksempler vises de beregninger, der forekommer, hvis du fortsætter efter advarslen uden først at tilbageføre afskrivningsposteringerne.</span><span class="sxs-lookup"><span data-stu-id="6e132-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="6e132-115">Eksempel 1: Afskrivningen overvurderes</span><span class="sxs-lookup"><span data-stu-id="6e132-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="6e132-116">Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="6e132-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6e132-117">I dette eksempel overvurderes afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="6e132-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6e132-118">Posteringshistorik for aktiv</span><span class="sxs-lookup"><span data-stu-id="6e132-118">Asset transaction history</span></span>

| <span data-ttu-id="6e132-119">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-119">Date</span></span>       | <span data-ttu-id="6e132-120">Posttype</span><span class="sxs-lookup"><span data-stu-id="6e132-120">Transaction type</span></span>                                                          | <span data-ttu-id="6e132-121">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6e132-122">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-122">January 1</span></span>  | <span data-ttu-id="6e132-123">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="6e132-123">Acquisition</span></span>                                                               | <span data-ttu-id="6e132-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-124">59,000.00</span></span>                                 |
| <span data-ttu-id="6e132-125">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-125">January 1</span></span>  | <span data-ttu-id="6e132-126">Anskaffelsesregulering</span><span class="sxs-lookup"><span data-stu-id="6e132-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="6e132-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-127">1,000.00</span></span>                                  |
| <span data-ttu-id="6e132-128">31. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-128">January 31</span></span> | <span data-ttu-id="6e132-129">Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="6e132-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6e132-130">1.000,00Beregning: Bogført værdi (59.000 + 1.000) / Antal resterende afskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="6e132-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6e132-131">Tilbageførselshandling</span><span class="sxs-lookup"><span data-stu-id="6e132-131">Reversal action</span></span>

| <span data-ttu-id="6e132-132">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-132">Date</span></span>      | <span data-ttu-id="6e132-133">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="6e132-133">Transaction type</span></span>                | <span data-ttu-id="6e132-134">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="6e132-135">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-135">January 1</span></span> | <span data-ttu-id="6e132-136">Tilbageførsel af anskaffelsesregulering</span><span class="sxs-lookup"><span data-stu-id="6e132-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="6e132-137">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6e132-138">Virkning af afskrivning</span><span class="sxs-lookup"><span data-stu-id="6e132-138">Depreciation effect</span></span>

| <span data-ttu-id="6e132-139">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-139">Date</span></span>        | <span data-ttu-id="6e132-140">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="6e132-140">Transaction type</span></span>        | <span data-ttu-id="6e132-141">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e132-142">28. februar</span><span class="sxs-lookup"><span data-stu-id="6e132-142">February 28</span></span> | <span data-ttu-id="6e132-143">Afskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="6e132-143">Depreciation (proposal)</span></span> | <span data-ttu-id="6e132-144">983,05Beregning: Bogført værdi (59.000 - 1.000 afskrivning) / Antal resterende afskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="6e132-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6e132-145">Afskrivningen er overvurderet med 16,95 (1.000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="6e132-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="6e132-146">Eksempel 2: Afskrivningen undervurderes</span><span class="sxs-lookup"><span data-stu-id="6e132-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="6e132-147">Der er konfigureret et aktiv med en levetid på 5 år og lineær afskrivning (60 afskrivningsperioder).</span><span class="sxs-lookup"><span data-stu-id="6e132-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6e132-148">I dette eksempel undervurderes afskrivningen.</span><span class="sxs-lookup"><span data-stu-id="6e132-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6e132-149">Posteringshistorik for aktiv</span><span class="sxs-lookup"><span data-stu-id="6e132-149">Asset transaction history</span></span>

| <span data-ttu-id="6e132-150">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-150">Date</span></span>       | <span data-ttu-id="6e132-151">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="6e132-151">Transaction type</span></span>                                                          | <span data-ttu-id="6e132-152">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6e132-153">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-153">January 1</span></span>  | <span data-ttu-id="6e132-154">Anskaffelse</span><span class="sxs-lookup"><span data-stu-id="6e132-154">Acquisition</span></span>                                                               | <span data-ttu-id="6e132-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-155">59,000.00</span></span>                                   |
| <span data-ttu-id="6e132-156">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-156">January 1</span></span>  | <span data-ttu-id="6e132-157">Nedskrivningsregulering</span><span class="sxs-lookup"><span data-stu-id="6e132-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="6e132-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-158">1,000.00</span></span>                                    |
| <span data-ttu-id="6e132-159">31. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-159">January 31</span></span> | <span data-ttu-id="6e132-160">Afskrivning (oprettet ved hjælp af et forslag for én afskrivningsperiode)</span><span class="sxs-lookup"><span data-stu-id="6e132-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6e132-161">966,67Beregning: Bogført værdi (59.000 - 1.000) / Antal resterende afskrivningsperioder (60)</span><span class="sxs-lookup"><span data-stu-id="6e132-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6e132-162">Tilbageførselshandling</span><span class="sxs-lookup"><span data-stu-id="6e132-162">Reversal action</span></span>

| <span data-ttu-id="6e132-163">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-163">Date</span></span>      | <span data-ttu-id="6e132-164">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="6e132-164">Transaction type</span></span>               | <span data-ttu-id="6e132-165">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="6e132-166">1. januar</span><span class="sxs-lookup"><span data-stu-id="6e132-166">January 1</span></span> | <span data-ttu-id="6e132-167">Tilbageførsel af nedskrivningsregulering</span><span class="sxs-lookup"><span data-stu-id="6e132-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="6e132-168">–1.000,00</span><span class="sxs-lookup"><span data-stu-id="6e132-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6e132-169">Virkning af afskrivning</span><span class="sxs-lookup"><span data-stu-id="6e132-169">Depreciation effect</span></span>

| <span data-ttu-id="6e132-170">Dato</span><span class="sxs-lookup"><span data-stu-id="6e132-170">Date</span></span>        | <span data-ttu-id="6e132-171">Transaktionstype</span><span class="sxs-lookup"><span data-stu-id="6e132-171">Transaction type</span></span>        | <span data-ttu-id="6e132-172">Beløb</span><span class="sxs-lookup"><span data-stu-id="6e132-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e132-173">28. februar</span><span class="sxs-lookup"><span data-stu-id="6e132-173">February 28</span></span> | <span data-ttu-id="6e132-174">Afskrivning (forslag)</span><span class="sxs-lookup"><span data-stu-id="6e132-174">Depreciation (proposal)</span></span> | <span data-ttu-id="6e132-175">983,62Beregning: Bogført værdi (59.000 - 966,67 afskrivning) / Antal resterende afskrivningsperioder (59)</span><span class="sxs-lookup"><span data-stu-id="6e132-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6e132-176">Afskrivningen er undervurderet med 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="6e132-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="6e132-177">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6e132-177">Additional resources</span></span>
--------

[<span data-ttu-id="6e132-178">Afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="6e132-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



