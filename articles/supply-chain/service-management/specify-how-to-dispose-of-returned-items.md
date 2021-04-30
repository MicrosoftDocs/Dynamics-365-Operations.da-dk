---
title: Angive, hvordan returvarer skal kasseres
description: Angiv, hvordan returvarer skal kasseres.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c827df81621346733953dc77e16e269f8c3767a8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910107"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="a17d7-103">Angive, hvordan returvarer skal kasseres</span><span class="sxs-lookup"><span data-stu-id="a17d7-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a17d7-104">Når du håndterer en returordre, skal du angive en årsagskode for returneringer for at fortælle, hvorfor produktet returneres.</span><span class="sxs-lookup"><span data-stu-id="a17d7-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="a17d7-105">Du skal også angive en dispositionskode og en dispositionshandling for at afgøre, hvad der skal ske med selve det returnerede produkt.</span><span class="sxs-lookup"><span data-stu-id="a17d7-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="a17d7-106">En dispositionskode kan anvendes, når du opretter en returordre, registrerer en varetilgang eller følgeseddelopdaterer en varetilgang og afslutter en karantæneordre.</span><span class="sxs-lookup"><span data-stu-id="a17d7-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="a17d7-107">Du kan angive de dispositionskoder, du har brug for for at understøtte forretningsprocesserne.</span><span class="sxs-lookup"><span data-stu-id="a17d7-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="a17d7-108">Nedenstående tabel indeholder et sæt af typisk anvendte koder til tildeling af disposition for returvarer.</span><span class="sxs-lookup"><span data-stu-id="a17d7-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a17d7-109">Dispositionstype</span><span class="sxs-lookup"><span data-stu-id="a17d7-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="a17d7-110">Fælles kode</span><span class="sxs-lookup"><span data-stu-id="a17d7-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="a17d7-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a17d7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-112">Kassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a17d7-113">SC</span><span class="sxs-lookup"><span data-stu-id="a17d7-113">SC</span></span></p></td>
<td><p><span data-ttu-id="a17d7-114">Kasser/Destruer</span><span class="sxs-lookup"><span data-stu-id="a17d7-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-115">Kassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a17d7-116">DC</span><span class="sxs-lookup"><span data-stu-id="a17d7-116">DC</span></span></p></td>
<td><p><span data-ttu-id="a17d7-117">Giv til velgørenhed</span><span class="sxs-lookup"><span data-stu-id="a17d7-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-118">Kassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a17d7-119">TD</span><span class="sxs-lookup"><span data-stu-id="a17d7-119">TD</span></span></p></td>
<td><p><span data-ttu-id="a17d7-120">Tredjepartskassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-121">Kassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a17d7-122">SL</span><span class="sxs-lookup"><span data-stu-id="a17d7-122">SL</span></span></p></td>
<td><p><span data-ttu-id="a17d7-123">Restværdi</span><span class="sxs-lookup"><span data-stu-id="a17d7-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-124">Kassation</span><span class="sxs-lookup"><span data-stu-id="a17d7-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a17d7-125">TS</span><span class="sxs-lookup"><span data-stu-id="a17d7-125">TS</span></span></p></td>
<td><p><span data-ttu-id="a17d7-126">Tredjepartssalg (sekundære markeder)</span><span class="sxs-lookup"><span data-stu-id="a17d7-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-127">Reparer/Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a17d7-128">RW</span><span class="sxs-lookup"><span data-stu-id="a17d7-128">RW</span></span></p></td>
<td><p><span data-ttu-id="a17d7-129">Genbearbejdning</span><span class="sxs-lookup"><span data-stu-id="a17d7-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-130">Reparer/Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a17d7-131">RF</span><span class="sxs-lookup"><span data-stu-id="a17d7-131">RF</span></span></p></td>
<td><p><span data-ttu-id="a17d7-132">Genproduktion/Geninstallation</span><span class="sxs-lookup"><span data-stu-id="a17d7-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-133">Reparer/Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a17d7-134">MD</span><span class="sxs-lookup"><span data-stu-id="a17d7-134">MD</span></span></p></td>
<td><p><span data-ttu-id="a17d7-135">Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-136">Reparer/Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a17d7-137">RP</span><span class="sxs-lookup"><span data-stu-id="a17d7-137">RP</span></span></p></td>
<td><p><span data-ttu-id="a17d7-138">Reparer</span><span class="sxs-lookup"><span data-stu-id="a17d7-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-139">Reparer/Modificer</span><span class="sxs-lookup"><span data-stu-id="a17d7-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a17d7-140">RV</span><span class="sxs-lookup"><span data-stu-id="a17d7-140">RV</span></span></p></td>
<td><p><span data-ttu-id="a17d7-141">Returner til leverandør</span><span class="sxs-lookup"><span data-stu-id="a17d7-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-142">Andet</span><span class="sxs-lookup"><span data-stu-id="a17d7-142">Other</span></span></p></td>
<td><p><span data-ttu-id="a17d7-143">AI</span><span class="sxs-lookup"><span data-stu-id="a17d7-143">AI</span></span></p></td>
<td><p><span data-ttu-id="a17d7-144">Brug som den er</span><span class="sxs-lookup"><span data-stu-id="a17d7-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-145">Andet</span><span class="sxs-lookup"><span data-stu-id="a17d7-145">Other</span></span></p></td>
<td><p><span data-ttu-id="a17d7-146">RS</span><span class="sxs-lookup"><span data-stu-id="a17d7-146">RS</span></span></p></td>
<td><p><span data-ttu-id="a17d7-147">Videresalg</span><span class="sxs-lookup"><span data-stu-id="a17d7-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-148">Andet</span><span class="sxs-lookup"><span data-stu-id="a17d7-148">Other</span></span></p></td>
<td><p><span data-ttu-id="a17d7-149">EX</span><span class="sxs-lookup"><span data-stu-id="a17d7-149">EX</span></span></p></td>
<td><p><span data-ttu-id="a17d7-150">Veksling</span><span class="sxs-lookup"><span data-stu-id="a17d7-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-151">Andet</span><span class="sxs-lookup"><span data-stu-id="a17d7-151">Other</span></span></p></td>
<td><p><span data-ttu-id="a17d7-152">MS</span><span class="sxs-lookup"><span data-stu-id="a17d7-152">MS</span></span></p></td>
<td><p><span data-ttu-id="a17d7-153">Diverse</span><span class="sxs-lookup"><span data-stu-id="a17d7-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a17d7-154">Du skal vælge en dispositionshandling for hver dispositionskode, du definerer.</span><span class="sxs-lookup"><span data-stu-id="a17d7-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="a17d7-155">Dispositionshandlingen bestemmer de fysiske og økonomiske følger af dispositionskoderne.</span><span class="sxs-lookup"><span data-stu-id="a17d7-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="a17d7-156">Dispositionshandlingen bestemmer f.eks. den fysiske håndtering af den returnerede vare, den økonomiske effekt af den returnerede vare, og om der skal sendes en erstatningsvare til kunden.</span><span class="sxs-lookup"><span data-stu-id="a17d7-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="a17d7-157">Du kan definere et ubegrænset antal dispositionskoder, afhængigt af virksomhedens behov, men der er kun seks foruddefinerede dispositionshandlingerne, du kan vælge mellem.</span><span class="sxs-lookup"><span data-stu-id="a17d7-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="a17d7-158">Følgende tabel indeholder dispositionshandlingerne og deres definitioner.</span><span class="sxs-lookup"><span data-stu-id="a17d7-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a17d7-159">Dispositionshandling</span><span class="sxs-lookup"><span data-stu-id="a17d7-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="a17d7-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a17d7-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-161"><strong>Kredit</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-162">Returner varen til lageret, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="a17d7-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-163"><strong>Krediter kun</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-164">Krediter kunden uden at kræve eller forvente, at varen returneres.</span><span class="sxs-lookup"><span data-stu-id="a17d7-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-165"><strong>Spild</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-166">Kassér varen, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="a17d7-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-167"><strong>Erstat og krediter</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-168">Returner varen til lageret, opret en erstatningsordre, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="a17d7-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a17d7-169"><strong>Erstat og kasser</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-170">Kassér varen, opret en erstatningsordre, og krediter kunden.</span><span class="sxs-lookup"><span data-stu-id="a17d7-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a17d7-171"><strong>Returner til kunde</strong></span><span class="sxs-lookup"><span data-stu-id="a17d7-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="a17d7-172">Afvis den returnerede vare, og returner den til debitoren.</span><span class="sxs-lookup"><span data-stu-id="a17d7-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="a17d7-173">Vælge en dispositionskode for en karantæneordre</span><span class="sxs-lookup"><span data-stu-id="a17d7-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="a17d7-174">Klik på **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karantæneordrer**.</span><span class="sxs-lookup"><span data-stu-id="a17d7-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="a17d7-175">For en eksisterende karantæneordre skal du vælge en handling i feltet **Dispositionskode** under fanen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="a17d7-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="a17d7-176">Se også</span><span class="sxs-lookup"><span data-stu-id="a17d7-176">See also</span></span>

[<span data-ttu-id="a17d7-177">Karantæneordre (form)</span><span class="sxs-lookup"><span data-stu-id="a17d7-177">Quarantine order (form)</span></span>](/dynamicsax-2012//quarantine-order-form)

<span data-ttu-id="a17d7-178">[Dispositionskoder (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a17d7-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]