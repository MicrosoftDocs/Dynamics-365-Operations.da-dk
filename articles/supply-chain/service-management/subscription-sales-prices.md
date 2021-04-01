---
title: Abonnementssalgspriser
description: Når du opretter et abonnement, afledes salgsprisen fra den salgsprisopsætningen, der er oprettet i formularen Salgspris (abonnement).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242295"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="be966-103">Abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="be966-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="be966-104">Når du opretter et abonnement, afledes salgsprisen fra den salgsprisopsætningen, der er oprettet i formularen **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="be966-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="be966-105">I formularen **Salgspris (abonnement)** kan du oprette salgspriser til et bestemt abonnement, eller du kan oprette salgspriser, der gælder mere bredt.</span><span class="sxs-lookup"><span data-stu-id="be966-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="be966-106">En salgspris kan kun anvendes til et abonnement, hvis abonnementets periodekode og valuta er den samme som periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="be966-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="be966-107">Hvis periodekoden og valutaen er ens for abonnementet og salgsprisen, vælges der salgspriser til abonnementet på basis af de prioriteter, der er angivet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="be966-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="be966-108">En tom celle i tabellen angiver et tomt felt, og et X angiver en værdi, der er lig med værdien i det abonnement, som posteringen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="be966-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-109">Prioritet</span><span class="sxs-lookup"><span data-stu-id="be966-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="be966-110"><strong>Art</strong></span><span class="sxs-lookup"><span data-stu-id="be966-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="be966-111"><strong>Projekt-id</strong></span><span class="sxs-lookup"><span data-stu-id="be966-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="be966-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="be966-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="be966-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="be966-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="be966-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="be966-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-115">1</span><span class="sxs-lookup"><span data-stu-id="be966-115">1</span></span></p></td>
<td><p><span data-ttu-id="be966-116">X</span><span class="sxs-lookup"><span data-stu-id="be966-116">X</span></span></p></td>
<td><p><span data-ttu-id="be966-117">X</span><span class="sxs-lookup"><span data-stu-id="be966-117">X</span></span></p></td>
<td><p><span data-ttu-id="be966-118">X</span><span class="sxs-lookup"><span data-stu-id="be966-118">X</span></span></p></td>
<td><p><span data-ttu-id="be966-119">X</span><span class="sxs-lookup"><span data-stu-id="be966-119">X</span></span></p></td>
<td><p><span data-ttu-id="be966-120">X</span><span class="sxs-lookup"><span data-stu-id="be966-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-121">2</span><span class="sxs-lookup"><span data-stu-id="be966-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-122">X</span><span class="sxs-lookup"><span data-stu-id="be966-122">X</span></span></p></td>
<td><p><span data-ttu-id="be966-123">X</span><span class="sxs-lookup"><span data-stu-id="be966-123">X</span></span></p></td>
<td><p><span data-ttu-id="be966-124">X</span><span class="sxs-lookup"><span data-stu-id="be966-124">X</span></span></p></td>
<td><p><span data-ttu-id="be966-125">X</span><span class="sxs-lookup"><span data-stu-id="be966-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be966-126">3</span><span class="sxs-lookup"><span data-stu-id="be966-126">3</span></span></p></td>
<td><p><span data-ttu-id="be966-127">X</span><span class="sxs-lookup"><span data-stu-id="be966-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-128">X</span><span class="sxs-lookup"><span data-stu-id="be966-128">X</span></span></p></td>
<td><p><span data-ttu-id="be966-129">X</span><span class="sxs-lookup"><span data-stu-id="be966-129">X</span></span></p></td>
<td><p><span data-ttu-id="be966-130">X</span><span class="sxs-lookup"><span data-stu-id="be966-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-131">4</span><span class="sxs-lookup"><span data-stu-id="be966-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-132">X</span><span class="sxs-lookup"><span data-stu-id="be966-132">X</span></span></p></td>
<td><p><span data-ttu-id="be966-133">X</span><span class="sxs-lookup"><span data-stu-id="be966-133">X</span></span></p></td>
<td><p><span data-ttu-id="be966-134">X</span><span class="sxs-lookup"><span data-stu-id="be966-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be966-135">5</span><span class="sxs-lookup"><span data-stu-id="be966-135">5</span></span></p></td>
<td><p><span data-ttu-id="be966-136">X</span><span class="sxs-lookup"><span data-stu-id="be966-136">X</span></span></p></td>
<td><p><span data-ttu-id="be966-137">X</span><span class="sxs-lookup"><span data-stu-id="be966-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-138">X</span><span class="sxs-lookup"><span data-stu-id="be966-138">X</span></span></p></td>
<td><p><span data-ttu-id="be966-139">X</span><span class="sxs-lookup"><span data-stu-id="be966-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-140">6</span><span class="sxs-lookup"><span data-stu-id="be966-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-141">X</span><span class="sxs-lookup"><span data-stu-id="be966-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-142">X</span><span class="sxs-lookup"><span data-stu-id="be966-142">X</span></span></p></td>
<td><p><span data-ttu-id="be966-143">X</span><span class="sxs-lookup"><span data-stu-id="be966-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be966-144">7</span><span class="sxs-lookup"><span data-stu-id="be966-144">7</span></span></p></td>
<td><p><span data-ttu-id="be966-145">X</span><span class="sxs-lookup"><span data-stu-id="be966-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-146">X</span><span class="sxs-lookup"><span data-stu-id="be966-146">X</span></span></p></td>
<td><p><span data-ttu-id="be966-147">X</span><span class="sxs-lookup"><span data-stu-id="be966-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-148">8</span><span class="sxs-lookup"><span data-stu-id="be966-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="be966-149">X</span><span class="sxs-lookup"><span data-stu-id="be966-149">X</span></span></p></td>
<td><p><span data-ttu-id="be966-150">X</span><span class="sxs-lookup"><span data-stu-id="be966-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-151">Når der oprettes et abonnementsgebyr, vælges salgsprisen med det største detaljeringsniveau, som angivet i tabellen ovenfor, som salgspris til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="be966-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="be966-152">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="be966-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="be966-153">Du kan opdatere abonnementssalgsprisen ved at opdatere basisprisen eller indekset.</span><span class="sxs-lookup"><span data-stu-id="be966-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="be966-154">Du kan opdatere med en procentsats eller til en ny værdi.</span><span class="sxs-lookup"><span data-stu-id="be966-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="be966-155">Salgspriser til abonnementsgebyrer</span><span class="sxs-lookup"><span data-stu-id="be966-155">Subscription fee sales prices</span></span>

<span data-ttu-id="be966-156">Når du opretter et abonnementsgebyr, baseres salgsprisen på abonnementets salgsprisopsætning.</span><span class="sxs-lookup"><span data-stu-id="be966-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="be966-157">Du kan enten bruge basisprisen fra abonnementets prisopsætning, eller du kan oprette indekserede salgspriser.</span><span class="sxs-lookup"><span data-stu-id="be966-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="be966-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="be966-158">Example</span></span>

<span data-ttu-id="be966-159">Du vil oprette abonnementssalgspriser på EUR 500 for et nyt projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="be966-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="be966-160">I formularen **Salgspris (abonnement)** opretter du en salgsprislinje for et abonnement, som angivet i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="be966-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-161">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="be966-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="be966-162">Art</span><span class="sxs-lookup"><span data-stu-id="be966-162">Category</span></span></p></th>
<th><p><span data-ttu-id="be966-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="be966-163">Project</span></span></p></th>
<th><p><span data-ttu-id="be966-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="be966-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="be966-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="be966-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="be966-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="be966-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="be966-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="be966-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="be966-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be966-169">9030</span><span class="sxs-lookup"><span data-stu-id="be966-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be966-170">Måned</span><span class="sxs-lookup"><span data-stu-id="be966-170">Month</span></span></p></td>
<td><p><span data-ttu-id="be966-171">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-172">500</span><span class="sxs-lookup"><span data-stu-id="be966-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-173">Bemærk, at felterne **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="be966-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="be966-174">Derefter opretter du følgende abonnementer.</span><span class="sxs-lookup"><span data-stu-id="be966-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="be966-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="be966-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="be966-176">Project</span></span></p></th>
<th><p><span data-ttu-id="be966-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="be966-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="be966-178">Art</span><span class="sxs-lookup"><span data-stu-id="be966-178">Category</span></span></p></th>
<th><p><span data-ttu-id="be966-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="be966-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="be966-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="be966-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="be966-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="be966-182">9030</span><span class="sxs-lookup"><span data-stu-id="be966-182">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-183">Abn1</span><span class="sxs-lookup"><span data-stu-id="be966-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="be966-184">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="be966-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="be966-185">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="be966-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="be966-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="be966-188">9030</span><span class="sxs-lookup"><span data-stu-id="be966-188">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-189">Abn1</span><span class="sxs-lookup"><span data-stu-id="be966-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="be966-190">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="be966-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="be966-191">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="be966-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-193">Nu opretter du abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1:</span><span class="sxs-lookup"><span data-stu-id="be966-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="be966-194">Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="be966-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="be966-195">I formularen **Abonnementsgrupper** skal du klikke **Funktion** \> **Opret abonnementsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="be966-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="be966-196">I formularen **Opret abonnementsgebyr** skal du angive de relevante oplysninger.</span><span class="sxs-lookup"><span data-stu-id="be966-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="be966-197">Du kan finde flere oplysninger under [Oprette posteringer for abonnementsgebyr](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="be966-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="be966-198">Der oprettes abonnementsgebyrer med en salgspris på EUR 500 for begge abonnementer, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="be966-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-199">Projektdato</span><span class="sxs-lookup"><span data-stu-id="be966-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="be966-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="be966-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="be966-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="be966-201">Project</span></span></p></th>
<th><p><span data-ttu-id="be966-202">Art</span><span class="sxs-lookup"><span data-stu-id="be966-202">Category</span></span></p></th>
<th><p><span data-ttu-id="be966-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="be966-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="be966-204">Slutdato</span><span class="sxs-lookup"><span data-stu-id="be966-204">End date</span></span></p></th>
<th><p><span data-ttu-id="be966-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="be966-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="be966-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="be966-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="be966-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="be966-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="be966-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="be966-209">9030</span><span class="sxs-lookup"><span data-stu-id="be966-209">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-210">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="be966-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="be966-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="be966-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="be966-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-213">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-214">500</span><span class="sxs-lookup"><span data-stu-id="be966-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="be966-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="be966-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="be966-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="be966-217">9030</span><span class="sxs-lookup"><span data-stu-id="be966-217">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-218">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="be966-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="be966-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="be966-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="be966-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-221">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-222">500</span><span class="sxs-lookup"><span data-stu-id="be966-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-223">På et senere tidspunkt vil du angive salgspriser for arten Abn.art1 for projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="be966-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="be966-224">Derfor opretter du en ny salgsprislinje med en salgspris på EUR 550 til kombinationen af projekt 9030 og gebyrarten Abn.art1.</span><span class="sxs-lookup"><span data-stu-id="be966-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="be966-225">Der er nu to linjer med abonnementssalgspriser for projekt 9030, som vist i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="be966-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-226">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="be966-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="be966-227">Art</span><span class="sxs-lookup"><span data-stu-id="be966-227">Category</span></span></p></th>
<th><p><span data-ttu-id="be966-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="be966-228">Project</span></span></p></th>
<th><p><span data-ttu-id="be966-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="be966-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="be966-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="be966-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="be966-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="be966-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="be966-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="be966-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="be966-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be966-234">9030</span><span class="sxs-lookup"><span data-stu-id="be966-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be966-235">Måned</span><span class="sxs-lookup"><span data-stu-id="be966-235">Month</span></span></p></td>
<td><p><span data-ttu-id="be966-236">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-237">500</span><span class="sxs-lookup"><span data-stu-id="be966-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="be966-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-239">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="be966-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="be966-240">9030</span><span class="sxs-lookup"><span data-stu-id="be966-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="be966-241">Måned</span><span class="sxs-lookup"><span data-stu-id="be966-241">Month</span></span></p></td>
<td><p><span data-ttu-id="be966-242">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-243">550</span><span class="sxs-lookup"><span data-stu-id="be966-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-244">Du gentager den fremgangsmåde, der er beskrevet ovenfor, for at oprette abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1.</span><span class="sxs-lookup"><span data-stu-id="be966-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="be966-245">Følgende tabeller viser de posteringer, der er oprettet for hvert abonnement, der knyttes til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="be966-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be966-246">Projektdato</span><span class="sxs-lookup"><span data-stu-id="be966-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="be966-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="be966-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="be966-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="be966-248">Project</span></span></p></th>
<th><p><span data-ttu-id="be966-249">Art</span><span class="sxs-lookup"><span data-stu-id="be966-249">Category</span></span></p></th>
<th><p><span data-ttu-id="be966-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="be966-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="be966-251">Slutdato</span><span class="sxs-lookup"><span data-stu-id="be966-251">End date</span></span></p></th>
<th><p><span data-ttu-id="be966-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="be966-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="be966-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="be966-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be966-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="be966-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="be966-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="be966-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="be966-256">9030</span><span class="sxs-lookup"><span data-stu-id="be966-256">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-257">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="be966-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="be966-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="be966-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="be966-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="be966-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="be966-260">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-261">550</span><span class="sxs-lookup"><span data-stu-id="be966-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be966-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="be966-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="be966-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="be966-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="be966-264">9030</span><span class="sxs-lookup"><span data-stu-id="be966-264">9030</span></span></p></td>
<td><p><span data-ttu-id="be966-265">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="be966-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="be966-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="be966-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="be966-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="be966-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="be966-268">EUR</span><span class="sxs-lookup"><span data-stu-id="be966-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="be966-269">500</span><span class="sxs-lookup"><span data-stu-id="be966-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be966-270">I den første postering for abonnement 00020\_135 afledes salgsprisen på EUR 550 fra den abonnementssalgspris, der er oprettet for kombinationen af det specifikke projekt og den specifikke art.</span><span class="sxs-lookup"><span data-stu-id="be966-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="be966-271">I den anden postering for abonnement 00021\_135 bruges salgsprisen på EUR 500 som projektets abonnementssalgspris, fordi der ikke er oprettet en pris til kombinationen af projekt 9030 og arten Abn.art2.</span><span class="sxs-lookup"><span data-stu-id="be966-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="be966-272">Se også</span><span class="sxs-lookup"><span data-stu-id="be966-272">See also</span></span>

[<span data-ttu-id="be966-273">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="be966-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]