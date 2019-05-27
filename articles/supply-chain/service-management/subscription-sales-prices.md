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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560683"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="f3c08-103">Abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="f3c08-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f3c08-104">Når du opretter et abonnement, afledes salgsprisen fra den salgsprisopsætningen, der er oprettet i formularen **Salgspris (abonnement)**.</span><span class="sxs-lookup"><span data-stu-id="f3c08-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="f3c08-105">I formularen **Salgspris (abonnement)** kan du oprette salgspriser til et bestemt abonnement, eller du kan oprette salgspriser, der gælder mere bredt.</span><span class="sxs-lookup"><span data-stu-id="f3c08-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="f3c08-106">En salgspris kan kun anvendes til et abonnement, hvis abonnementets periodekode og valuta er den samme som periodekoden og valutaen for salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="f3c08-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="f3c08-107">Hvis periodekoden og valutaen er ens for abonnementet og salgsprisen, vælges der salgspriser til abonnementet på basis af de prioriteter, der er angivet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f3c08-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="f3c08-108">En tom celle i tabellen angiver et tomt felt, og et X angiver en værdi, der er lig med værdien i det abonnement, som posteringen genereres fra.</span><span class="sxs-lookup"><span data-stu-id="f3c08-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="f3c08-109">Prioritet</span><span class="sxs-lookup"><span data-stu-id="f3c08-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="f3c08-110"><strong>Art</strong></span><span class="sxs-lookup"><span data-stu-id="f3c08-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="f3c08-111"><strong>Projekt-id</strong></span><span class="sxs-lookup"><span data-stu-id="f3c08-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="f3c08-112"><strong>Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="f3c08-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="f3c08-113"><strong>Salgsvaluta</strong></span><span class="sxs-lookup"><span data-stu-id="f3c08-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="f3c08-114"><strong>Periodekode</strong></span><span class="sxs-lookup"><span data-stu-id="f3c08-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-115">1</span><span class="sxs-lookup"><span data-stu-id="f3c08-115">1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-116">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-116">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-117">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-117">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-118">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-118">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-119">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-119">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-120">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-121">2</span><span class="sxs-lookup"><span data-stu-id="f3c08-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-122">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-122">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-123">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-123">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-124">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-124">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-125">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-126">3</span><span class="sxs-lookup"><span data-stu-id="f3c08-126">3</span></span></p></td>
<td><p><span data-ttu-id="f3c08-127">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-128">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-128">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-129">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-129">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-130">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-131">4</span><span class="sxs-lookup"><span data-stu-id="f3c08-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-132">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-132">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-133">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-133">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-134">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-135">5</span><span class="sxs-lookup"><span data-stu-id="f3c08-135">5</span></span></p></td>
<td><p><span data-ttu-id="f3c08-136">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-136">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-137">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-138">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-138">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-139">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-140">6</span><span class="sxs-lookup"><span data-stu-id="f3c08-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-141">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-142">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-142">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-143">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-144">7</span><span class="sxs-lookup"><span data-stu-id="f3c08-144">7</span></span></p></td>
<td><p><span data-ttu-id="f3c08-145">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-146">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-146">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-147">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-148">8</span><span class="sxs-lookup"><span data-stu-id="f3c08-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="f3c08-149">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-149">X</span></span></p></td>
<td><p><span data-ttu-id="f3c08-150">X</span><span class="sxs-lookup"><span data-stu-id="f3c08-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-151">Når der oprettes et abonnementsgebyr, vælges salgsprisen med det største detaljeringsniveau, som angivet i tabellen ovenfor, som salgspris til abonnementet.</span><span class="sxs-lookup"><span data-stu-id="f3c08-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="f3c08-152">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="f3c08-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="f3c08-153">Du kan opdatere abonnementssalgsprisen ved at opdatere basisprisen eller indekset.</span><span class="sxs-lookup"><span data-stu-id="f3c08-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="f3c08-154">Du kan opdatere med en procentsats eller til en ny værdi.</span><span class="sxs-lookup"><span data-stu-id="f3c08-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="f3c08-155">Salgspriser til abonnementsgebyrer</span><span class="sxs-lookup"><span data-stu-id="f3c08-155">Subscription fee sales prices</span></span>

<span data-ttu-id="f3c08-156">Når du opretter et abonnementsgebyr, baseres salgsprisen på abonnementets salgsprisopsætning.</span><span class="sxs-lookup"><span data-stu-id="f3c08-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="f3c08-157">Du kan enten bruge basisprisen fra abonnementets prisopsætning, eller du kan oprette indekserede salgspriser.</span><span class="sxs-lookup"><span data-stu-id="f3c08-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="f3c08-158">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f3c08-158">Example</span></span>

<span data-ttu-id="f3c08-159">Du vil oprette abonnementssalgspriser på EUR 500 for et nyt projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="f3c08-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="f3c08-160">I formularen **Salgspris (abonnement)** opretter du en salgsprislinje for et abonnement, som angivet i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="f3c08-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="f3c08-161">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="f3c08-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="f3c08-162">Art</span><span class="sxs-lookup"><span data-stu-id="f3c08-162">Category</span></span></p></th>
<th><p><span data-ttu-id="f3c08-163">Projekt</span><span class="sxs-lookup"><span data-stu-id="f3c08-163">Project</span></span></p></th>
<th><p><span data-ttu-id="f3c08-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3c08-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="f3c08-165">Periodekode</span><span class="sxs-lookup"><span data-stu-id="f3c08-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="f3c08-166">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="f3c08-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="f3c08-167">Salgspris</span><span class="sxs-lookup"><span data-stu-id="f3c08-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="f3c08-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3c08-169">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3c08-170">Måned</span><span class="sxs-lookup"><span data-stu-id="f3c08-170">Month</span></span></p></td>
<td><p><span data-ttu-id="f3c08-171">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-172">500</span><span class="sxs-lookup"><span data-stu-id="f3c08-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-173">Bemærk, at felterne **Kategori** og **Abonnement** er tomme.</span><span class="sxs-lookup"><span data-stu-id="f3c08-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="f3c08-174">Derefter opretter du følgende abonnementer.</span><span class="sxs-lookup"><span data-stu-id="f3c08-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="f3c08-175">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="f3c08-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="f3c08-176">Projekt</span><span class="sxs-lookup"><span data-stu-id="f3c08-176">Project</span></span></p></th>
<th><p><span data-ttu-id="f3c08-177">Abonnementsgruppe</span><span class="sxs-lookup"><span data-stu-id="f3c08-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="f3c08-178">Art</span><span class="sxs-lookup"><span data-stu-id="f3c08-178">Category</span></span></p></th>
<th><p><span data-ttu-id="f3c08-179">Valuta</span><span class="sxs-lookup"><span data-stu-id="f3c08-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="f3c08-180">Periodekode</span><span class="sxs-lookup"><span data-stu-id="f3c08-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-182">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-182">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-183">Abn1</span><span class="sxs-lookup"><span data-stu-id="f3c08-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-184">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="f3c08-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-185">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-186">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f3c08-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-188">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-188">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-189">Abn1</span><span class="sxs-lookup"><span data-stu-id="f3c08-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-190">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="f3c08-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="f3c08-191">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-192">Månedlig</span><span class="sxs-lookup"><span data-stu-id="f3c08-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-193">Nu opretter du abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1:</span><span class="sxs-lookup"><span data-stu-id="f3c08-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="f3c08-194">Klik på **Servicestyring** \> **Opsætning** \> **Serviceabonnementer** \> **Abonnementsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f3c08-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="f3c08-195">I formularen **Abonnementsgrupper** skal du klikke **Funktion** \> **Opret abonnementsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="f3c08-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="f3c08-196">I formularen **Opret abonnementsgebyr** skal du angive de relevante oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f3c08-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="f3c08-197">Du kan finde flere oplysninger under [Oprette posteringer for abonnementsgebyr](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="f3c08-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="f3c08-198">Der oprettes abonnementsgebyrer med en salgspris på EUR 500 for begge abonnementer, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f3c08-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="f3c08-199">Projektdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-200">Serviceabonnement</span><span class="sxs-lookup"><span data-stu-id="f3c08-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="f3c08-201">Projekt</span><span class="sxs-lookup"><span data-stu-id="f3c08-201">Project</span></span></p></th>
<th><p><span data-ttu-id="f3c08-202">Art</span><span class="sxs-lookup"><span data-stu-id="f3c08-202">Category</span></span></p></th>
<th><p><span data-ttu-id="f3c08-203">Startdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-204">Slutdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-204">End date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-205">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="f3c08-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="f3c08-206">Salgspris</span><span class="sxs-lookup"><span data-stu-id="f3c08-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="f3c08-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="f3c08-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-209">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-209">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-210">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="f3c08-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-213">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-214">500</span><span class="sxs-lookup"><span data-stu-id="f3c08-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="f3c08-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="f3c08-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-217">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-217">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-218">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="f3c08-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="f3c08-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-221">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-222">500</span><span class="sxs-lookup"><span data-stu-id="f3c08-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-223">På et senere tidspunkt vil du angive salgspriser for arten Abn.art1 for projekt 9030.</span><span class="sxs-lookup"><span data-stu-id="f3c08-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="f3c08-224">Derfor opretter du en ny salgsprislinje med en salgspris på EUR 550 til kombinationen af projekt 9030 og gebyrarten Abn.art1.</span><span class="sxs-lookup"><span data-stu-id="f3c08-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="f3c08-225">Der er nu to linjer med abonnementssalgspriser for projekt 9030, som vist i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="f3c08-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="f3c08-226">Gældende fra</span><span class="sxs-lookup"><span data-stu-id="f3c08-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="f3c08-227">Art</span><span class="sxs-lookup"><span data-stu-id="f3c08-227">Category</span></span></p></th>
<th><p><span data-ttu-id="f3c08-228">Projekt</span><span class="sxs-lookup"><span data-stu-id="f3c08-228">Project</span></span></p></th>
<th><p><span data-ttu-id="f3c08-229">Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3c08-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="f3c08-230">Periodekode</span><span class="sxs-lookup"><span data-stu-id="f3c08-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="f3c08-231">Valuta</span><span class="sxs-lookup"><span data-stu-id="f3c08-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="f3c08-232">Salgspris</span><span class="sxs-lookup"><span data-stu-id="f3c08-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3c08-234">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3c08-235">Måned</span><span class="sxs-lookup"><span data-stu-id="f3c08-235">Month</span></span></p></td>
<td><p><span data-ttu-id="f3c08-236">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-237">500</span><span class="sxs-lookup"><span data-stu-id="f3c08-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-239">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="f3c08-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-240">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f3c08-241">Måned</span><span class="sxs-lookup"><span data-stu-id="f3c08-241">Month</span></span></p></td>
<td><p><span data-ttu-id="f3c08-242">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-243">550</span><span class="sxs-lookup"><span data-stu-id="f3c08-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-244">Du gentager den fremgangsmåde, der er beskrevet ovenfor, for at oprette abonnementsgebyrer for begge abonnementer i abonnementsgruppen Abn1.</span><span class="sxs-lookup"><span data-stu-id="f3c08-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="f3c08-245">Følgende tabeller viser de posteringer, der er oprettet for hvert abonnement, der knyttes til abonnementsgruppen.</span><span class="sxs-lookup"><span data-stu-id="f3c08-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="f3c08-246">Projektdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-247">Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3c08-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="f3c08-248">Projekt</span><span class="sxs-lookup"><span data-stu-id="f3c08-248">Project</span></span></p></th>
<th><p><span data-ttu-id="f3c08-249">Art</span><span class="sxs-lookup"><span data-stu-id="f3c08-249">Category</span></span></p></th>
<th><p><span data-ttu-id="f3c08-250">Startdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-251">Slutdato</span><span class="sxs-lookup"><span data-stu-id="f3c08-251">End date</span></span></p></th>
<th><p><span data-ttu-id="f3c08-252">Salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="f3c08-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="f3c08-253">Salgspris</span><span class="sxs-lookup"><span data-stu-id="f3c08-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3c08-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="f3c08-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="f3c08-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-256">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-256">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-257">Abn.art1</span><span class="sxs-lookup"><span data-stu-id="f3c08-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="f3c08-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="f3c08-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="f3c08-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="f3c08-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="f3c08-260">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-261">550</span><span class="sxs-lookup"><span data-stu-id="f3c08-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3c08-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="f3c08-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="f3c08-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="f3c08-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="f3c08-264">9030</span><span class="sxs-lookup"><span data-stu-id="f3c08-264">9030</span></span></p></td>
<td><p><span data-ttu-id="f3c08-265">Abn.art2</span><span class="sxs-lookup"><span data-stu-id="f3c08-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="f3c08-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="f3c08-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="f3c08-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="f3c08-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="f3c08-268">EUR</span><span class="sxs-lookup"><span data-stu-id="f3c08-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="f3c08-269">500</span><span class="sxs-lookup"><span data-stu-id="f3c08-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f3c08-270">I den første postering for abonnement 00020\_135 afledes salgsprisen på EUR 550 fra den abonnementssalgspris, der er oprettet for kombinationen af det specifikke projekt og den specifikke art.</span><span class="sxs-lookup"><span data-stu-id="f3c08-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="f3c08-271">I den anden postering for abonnement 00021\_135 bruges salgsprisen på EUR 500 som projektets abonnementssalgspris, fordi der ikke er oprettet en pris til kombinationen af projekt 9030 og arten Abn.art2.</span><span class="sxs-lookup"><span data-stu-id="f3c08-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3c08-272">Se også</span><span class="sxs-lookup"><span data-stu-id="f3c08-272">See also</span></span>

[<span data-ttu-id="f3c08-273">Opdatere og indeksere abonnementssalgspriser</span><span class="sxs-lookup"><span data-stu-id="f3c08-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


