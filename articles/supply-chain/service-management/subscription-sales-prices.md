---
title: Abonnementssalgspriser
description: Når du opretter et abonnement, afledes salgsprisen fra den salgsprisopsætningen, der er oprettet i formularen Salgspris (abonnement).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2019
ms.locfileid: "352154"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="86b80-103">Abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="86b80-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="86b80-104">Når du opretter et abonnement, afledes salgsprisen fra den salgsprisopsætningen, der er oprettet i formularen **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="86b80-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="86b80-105">I formularen **Salgspris (abonnement)** kan du oprette salgspriser til et bestemt abonnement, eller du kan oprette salgspriser, der gælder mere bredt.</span><span class="sxs-lookup"><span data-stu-id="86b80-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="86b80-106">En salgspris kan kun anvendes til et abonnement, hvis abonnementets periodekode og valuta er den samme som periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="86b80-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="86b80-107">Hvis periodekoden og valutaen er ens for abonnementet og salgsprisen, vælges der salgspriser til abonnementet på basis af de prioriteter, der er angivet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="86b80-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="86b80-108">En tom celle i tabellen angiver et tomt felt, og et X angiver en værdi, der er lig med værdien i det abonnement, som posteringen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="86b80-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="86b80-109">Prioritet</span><span class="sxs-lookup"><span data-stu-id="86b80-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="86b80-110"><strong>Art</strong></span><span class="sxs-lookup"><span data-stu-id="86b80-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="86b80-111"><strong>Projekt-id</strong></span><span class="sxs-lookup"><span data-stu-id="86b80-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="86b80-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="86b80-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="86b80-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="86b80-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="86b80-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="86b80-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-115">1</span><span class="sxs-lookup"><span data-stu-id="86b80-115">1</span></span></p></td>
<td><p><span data-ttu-id="86b80-116">X</span><span class="sxs-lookup"><span data-stu-id="86b80-116">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-117">X</span><span class="sxs-lookup"><span data-stu-id="86b80-117">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-118">X</span><span class="sxs-lookup"><span data-stu-id="86b80-118">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-119">X</span><span class="sxs-lookup"><span data-stu-id="86b80-119">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-120">X</span><span class="sxs-lookup"><span data-stu-id="86b80-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-121">2</span><span class="sxs-lookup"><span data-stu-id="86b80-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-122">X</span><span class="sxs-lookup"><span data-stu-id="86b80-122">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-123">X</span><span class="sxs-lookup"><span data-stu-id="86b80-123">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-124">X</span><span class="sxs-lookup"><span data-stu-id="86b80-124">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-125">X</span><span class="sxs-lookup"><span data-stu-id="86b80-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86b80-126">3</span><span class="sxs-lookup"><span data-stu-id="86b80-126">3</span></span></p></td>
<td><p><span data-ttu-id="86b80-127">X</span><span class="sxs-lookup"><span data-stu-id="86b80-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-128">X</span><span class="sxs-lookup"><span data-stu-id="86b80-128">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-129">X</span><span class="sxs-lookup"><span data-stu-id="86b80-129">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-130">X</span><span class="sxs-lookup"><span data-stu-id="86b80-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-131">4</span><span class="sxs-lookup"><span data-stu-id="86b80-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-132">X</span><span class="sxs-lookup"><span data-stu-id="86b80-132">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-133">X</span><span class="sxs-lookup"><span data-stu-id="86b80-133">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-134">X</span><span class="sxs-lookup"><span data-stu-id="86b80-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86b80-135">5</span><span class="sxs-lookup"><span data-stu-id="86b80-135">5</span></span></p></td>
<td><p><span data-ttu-id="86b80-136">X</span><span class="sxs-lookup"><span data-stu-id="86b80-136">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-137">X</span><span class="sxs-lookup"><span data-stu-id="86b80-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-138">X</span><span class="sxs-lookup"><span data-stu-id="86b80-138">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-139">X</span><span class="sxs-lookup"><span data-stu-id="86b80-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-140">6</span><span class="sxs-lookup"><span data-stu-id="86b80-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-141">X</span><span class="sxs-lookup"><span data-stu-id="86b80-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-142">X</span><span class="sxs-lookup"><span data-stu-id="86b80-142">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-143">X</span><span class="sxs-lookup"><span data-stu-id="86b80-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86b80-144">7</span><span class="sxs-lookup"><span data-stu-id="86b80-144">7</span></span></p></td>
<td><p><span data-ttu-id="86b80-145">X</span><span class="sxs-lookup"><span data-stu-id="86b80-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-146">X</span><span class="sxs-lookup"><span data-stu-id="86b80-146">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-147">X</span><span class="sxs-lookup"><span data-stu-id="86b80-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-148">8</span><span class="sxs-lookup"><span data-stu-id="86b80-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b80-149">X</span><span class="sxs-lookup"><span data-stu-id="86b80-149">X</span></span></p></td>
<td><p><span data-ttu-id="86b80-150">X</span><span class="sxs-lookup"><span data-stu-id="86b80-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-151">Når der oprettes et abonnementsgebyr, vælges salgsprisen med det største detaljeringsniveau, som angivet i tabellen ovenfor, som salgspris til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="86b80-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="86b80-152">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="86b80-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="86b80-153">Du kan opdatere abonnementssalgsprisen ved at opdatere basisprisen eller indekset.</span><span class="sxs-lookup"><span data-stu-id="86b80-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="86b80-154">Du kan opdatere med en procentsats eller til en ny værdi.</span><span class="sxs-lookup"><span data-stu-id="86b80-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="86b80-155">Salgspriser til abonnementsgebyrer</span><span class="sxs-lookup"><span data-stu-id="86b80-155">Subscription fee sales prices</span></span>

<span data-ttu-id="86b80-156">Når du opretter et abonnementsgebyr, baseres salgsprisen på abonnementets salgsprisopsætning.</span><span class="sxs-lookup"><span data-stu-id="86b80-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="86b80-157">Du kan enten bruge basisprisen fra abonnementets prisopsætning, eller du kan oprette indekserede salgspriser.</span><span class="sxs-lookup"><span data-stu-id="86b80-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="86b80-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="86b80-158">Example</span></span>

<span data-ttu-id="86b80-159">Du vil oprette abonnementssalgspriser på EUR 500 for et nyt projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="86b80-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="86b80-160">I formularen **Salgspris (abonnement)** opretter du en salgsprislinje for et abonnement, som angivet i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="86b80-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="86b80-161">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="86b80-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="86b80-162">Art</span><span class="sxs-lookup"><span data-stu-id="86b80-162">Category</span></span></p></th>
<th><p><span data-ttu-id="86b80-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="86b80-163">Project</span></span></p></th>
<th><p><span data-ttu-id="86b80-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="86b80-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="86b80-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="86b80-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="86b80-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="86b80-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="86b80-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="86b80-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="86b80-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="86b80-169">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="86b80-170">Måned</span><span class="sxs-lookup"><span data-stu-id="86b80-170">Month</span></span></p></td>
<td><p><span data-ttu-id="86b80-171">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-172">500</span><span class="sxs-lookup"><span data-stu-id="86b80-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-173">Bemærk, at felterne **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="86b80-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="86b80-174">Derefter opretter du følgende abonnementer.</span><span class="sxs-lookup"><span data-stu-id="86b80-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="86b80-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="86b80-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="86b80-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="86b80-176">Project</span></span></p></th>
<th><p><span data-ttu-id="86b80-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="86b80-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="86b80-178">Art</span><span class="sxs-lookup"><span data-stu-id="86b80-178">Category</span></span></p></th>
<th><p><span data-ttu-id="86b80-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="86b80-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="86b80-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="86b80-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="86b80-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-182">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-182">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-183">Abn1</span><span class="sxs-lookup"><span data-stu-id="86b80-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="86b80-184">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="86b80-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="86b80-185">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="86b80-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="86b80-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-188">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-188">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-189">Abn1</span><span class="sxs-lookup"><span data-stu-id="86b80-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="86b80-190">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="86b80-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="86b80-191">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="86b80-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-193">Nu opretter du abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1:</span><span class="sxs-lookup"><span data-stu-id="86b80-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="86b80-194">Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="86b80-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="86b80-195">I formularen **Abonnementsgrupper** skal du klikke **Funktion** \> **Opret abonnementsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="86b80-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="86b80-196">I formularen **Opret abonnementsgebyr** skal du angive de relevante oplysninger.</span><span class="sxs-lookup"><span data-stu-id="86b80-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="86b80-197">Du kan finde flere oplysninger under [Oprette posteringer for abonnementsgebyr](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="86b80-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="86b80-198">Der oprettes abonnementsgebyrer med en salgspris på EUR 500 for begge abonnementer, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="86b80-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="86b80-199">Projektdato</span><span class="sxs-lookup"><span data-stu-id="86b80-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="86b80-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="86b80-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="86b80-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="86b80-201">Project</span></span></p></th>
<th><p><span data-ttu-id="86b80-202">Art</span><span class="sxs-lookup"><span data-stu-id="86b80-202">Category</span></span></p></th>
<th><p><span data-ttu-id="86b80-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="86b80-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="86b80-204">Slutdato</span><span class="sxs-lookup"><span data-stu-id="86b80-204">End date</span></span></p></th>
<th><p><span data-ttu-id="86b80-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="86b80-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="86b80-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="86b80-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="86b80-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="86b80-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="86b80-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-209">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-209">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-210">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="86b80-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="86b80-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-213">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-214">500</span><span class="sxs-lookup"><span data-stu-id="86b80-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="86b80-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="86b80-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="86b80-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-217">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-217">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-218">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="86b80-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="86b80-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-221">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-222">500</span><span class="sxs-lookup"><span data-stu-id="86b80-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-223">På et senere tidspunkt vil du angive salgspriser for arten Abn.art1 for projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="86b80-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="86b80-224">Derfor opretter du en ny salgsprislinje med en salgspris på EUR 550 til kombinationen af projekt 9030 og gebyrarten Abn.art1.</span><span class="sxs-lookup"><span data-stu-id="86b80-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="86b80-225">Der er nu to linjer med abonnementssalgspriser for projekt 9030, som vist i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="86b80-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="86b80-226">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="86b80-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="86b80-227">Art</span><span class="sxs-lookup"><span data-stu-id="86b80-227">Category</span></span></p></th>
<th><p><span data-ttu-id="86b80-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="86b80-228">Project</span></span></p></th>
<th><p><span data-ttu-id="86b80-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="86b80-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="86b80-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="86b80-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="86b80-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="86b80-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="86b80-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="86b80-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="86b80-234">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="86b80-235">Måned</span><span class="sxs-lookup"><span data-stu-id="86b80-235">Month</span></span></p></td>
<td><p><span data-ttu-id="86b80-236">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-237">500</span><span class="sxs-lookup"><span data-stu-id="86b80-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-239">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="86b80-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="86b80-240">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="86b80-241">Måned</span><span class="sxs-lookup"><span data-stu-id="86b80-241">Month</span></span></p></td>
<td><p><span data-ttu-id="86b80-242">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-243">550</span><span class="sxs-lookup"><span data-stu-id="86b80-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-244">Du gentager den fremgangsmåde, der er beskrevet ovenfor, for at oprette abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1.</span><span class="sxs-lookup"><span data-stu-id="86b80-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="86b80-245">Følgende tabeller viser de posteringer, der er oprettet for hvert abonnement, der knyttes til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="86b80-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="86b80-246">Projektdato</span><span class="sxs-lookup"><span data-stu-id="86b80-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="86b80-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="86b80-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="86b80-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="86b80-248">Project</span></span></p></th>
<th><p><span data-ttu-id="86b80-249">Art</span><span class="sxs-lookup"><span data-stu-id="86b80-249">Category</span></span></p></th>
<th><p><span data-ttu-id="86b80-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="86b80-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="86b80-251">Slutdato</span><span class="sxs-lookup"><span data-stu-id="86b80-251">End date</span></span></p></th>
<th><p><span data-ttu-id="86b80-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="86b80-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="86b80-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="86b80-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b80-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="86b80-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="86b80-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="86b80-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-256">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-256">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-257">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="86b80-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="86b80-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="86b80-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="86b80-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="86b80-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="86b80-260">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-261">550</span><span class="sxs-lookup"><span data-stu-id="86b80-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b80-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="86b80-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="86b80-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="86b80-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="86b80-264">9030</span><span class="sxs-lookup"><span data-stu-id="86b80-264">9030</span></span></p></td>
<td><p><span data-ttu-id="86b80-265">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="86b80-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="86b80-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="86b80-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="86b80-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="86b80-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="86b80-268">EUR</span><span class="sxs-lookup"><span data-stu-id="86b80-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="86b80-269">500</span><span class="sxs-lookup"><span data-stu-id="86b80-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b80-270">I den første postering for abonnement 00020\_135 afledes salgsprisen på EUR 550 fra den abonnementssalgspris, der er oprettet for kombinationen af det specifikke projekt og den specifikke art.</span><span class="sxs-lookup"><span data-stu-id="86b80-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="86b80-271">I den anden postering for abonnement 00021\_135 bruges salgsprisen på EUR 500 som projektets abonnementssalgspris, fordi der ikke er oprettet en pris til kombinationen af projekt 9030 og arten Abn.art2.</span><span class="sxs-lookup"><span data-stu-id="86b80-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="86b80-272">Se også</span><span class="sxs-lookup"><span data-stu-id="86b80-272">See also</span></span>

[<span data-ttu-id="86b80-273">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="86b80-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


