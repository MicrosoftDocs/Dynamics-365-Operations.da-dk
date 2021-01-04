---
title: Debitor, posteringsprofiler
description: Debitorer, der bogfører profiler, styrer, hvordan debitortransaktioner bogføres til Finans.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff786d6e872e48f9605f9a472b7bffd409c5b3f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441422"
---
# <a name="customer-posting-profiles"></a><span data-ttu-id="0db35-103">Debitor, posteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="0db35-103">Customer posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0db35-104">Debitorer, der bogfører profiler, styrer, hvordan debitortransaktioner bogføres til Finans.</span><span class="sxs-lookup"><span data-stu-id="0db35-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="0db35-105">Debitor, posteringsprofiler</span><span class="sxs-lookup"><span data-stu-id="0db35-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="0db35-106">Debitorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle debitorer, en gruppe debitorer eller en enkelt debitor.</span><span class="sxs-lookup"><span data-stu-id="0db35-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="0db35-107">Disse indstillinger bruges, når du opretter salgsordrer, fritekstfakturaer, kontantbetalinger, rykkere og rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="0db35-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="0db35-108">For nogle transaktioner kan du vælge en posteringsprofil, der er anderledes end, og som prioriteres højere end de posteringsprofiler, der er oprettet for transaktioner på denne side.</span><span class="sxs-lookup"><span data-stu-id="0db35-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="0db35-109">Standardposteringsprofilen defineres i oversigtspanelet Finans og Moms på siden Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="0db35-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="0db35-110">Standardposteringsprofilen medtages derefter automatisk i hovedet i nye dokumenter, hvor du kan ændre den til en anden posteringsprofil, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="0db35-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="0db35-111">Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden Definitioner af posteringsbogføring.</span><span class="sxs-lookup"><span data-stu-id="0db35-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="0db35-112">I stedet for posteringsprofiler er det bogføringsdefinitioner, der styrer, hvordan debitorposter bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="0db35-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="0db35-113">Oprette en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="0db35-113">Creating a posting profile</span></span>
<span data-ttu-id="0db35-114">Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="0db35-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="0db35-115">Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="0db35-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="0db35-116">Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge:</span><span class="sxs-lookup"><span data-stu-id="0db35-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="0db35-117">Feltværdien **Kontokode**</span><span class="sxs-lookup"><span data-stu-id="0db35-117">**Account code** field value</span></span> | <span data-ttu-id="0db35-118">Feltværdien **Konto/gruppenummer**</span><span class="sxs-lookup"><span data-stu-id="0db35-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="0db35-119">Søgeprioritet</span><span class="sxs-lookup"><span data-stu-id="0db35-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="0db35-120">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="0db35-120">**Table**</span></span>                    | <span data-ttu-id="0db35-121">Bestemt debitorkonto</span><span class="sxs-lookup"><span data-stu-id="0db35-121">Specific customer account</span></span>                       | <span data-ttu-id="0db35-122">1</span><span class="sxs-lookup"><span data-stu-id="0db35-122">1</span></span>               |
| <span data-ttu-id="0db35-123">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="0db35-123">**Group**</span></span>                    | <span data-ttu-id="0db35-124">Debitorgruppe, som debitor er tilknyttet</span><span class="sxs-lookup"><span data-stu-id="0db35-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="0db35-125">2</span><span class="sxs-lookup"><span data-stu-id="0db35-125">2</span></span>               |
| <span data-ttu-id="0db35-126">**Alle**</span><span class="sxs-lookup"><span data-stu-id="0db35-126">**All**</span></span>                      | <span data-ttu-id="0db35-127">Tom</span><span class="sxs-lookup"><span data-stu-id="0db35-127">Blank</span></span>                                           | <span data-ttu-id="0db35-128">3</span><span class="sxs-lookup"><span data-stu-id="0db35-128">3</span></span>               |

<span data-ttu-id="0db35-129">Hvis alle debitorposteringer skal have samme posteringsprofil, skal du kun definere én posteringsprofil med Alle i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="0db35-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="0db35-130">Angiv følgende værdier for at definere en posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="0db35-130">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0db35-131">Felt</span><span class="sxs-lookup"><span data-stu-id="0db35-131">Field</span></span></th>
<th><span data-ttu-id="0db35-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0db35-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0db35-133"><strong>Posteringsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="0db35-134">Angiv en kode for posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0db35-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="0db35-135">Eksempel: Hvis du vil have én konto for debitorsaldi i indenlandsk valuta og én konto for debitorsaldi i udenlandsk valuta, skal du oprette to posteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="0db35-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="0db35-136">Du kan kalde den ene konto Indland og den anden Udland.</span><span class="sxs-lookup"><span data-stu-id="0db35-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db35-137"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="0db35-138">Angiv en beskrivelse af posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0db35-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="0db35-139">Dette bruges kun til at identificere posteringsprofilen bedre, når du ser den på denne side.</span><span class="sxs-lookup"><span data-stu-id="0db35-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db35-140"><strong>Kontokode</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="0db35-141">Angiv, om posteringsprofilen skal gælde for en bestemt debitor, en gruppe af debitorer eller alle debitorer:</span><span class="sxs-lookup"><span data-stu-id="0db35-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="0db35-142"><strong>Tabel</strong> – Posteringsprofilen anvendes på en enkelt debitor.</span><span class="sxs-lookup"><span data-stu-id="0db35-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="0db35-143">Vælg debitorkontoen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="0db35-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="0db35-144"><strong>Gruppe</strong> – Posteringsprofilen anvendes på en debitorgruppe.</span><span class="sxs-lookup"><span data-stu-id="0db35-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="0db35-145">Vælg debitorgruppen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="0db35-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="0db35-146"><strong>Alle</strong> – Posteringsprofilen anvendes på alle debitorer.</span><span class="sxs-lookup"><span data-stu-id="0db35-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="0db35-147">Lad feltet Konto/gruppenummer være tomt.</span><span class="sxs-lookup"><span data-stu-id="0db35-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db35-148"><strong>Konto/gruppenummer</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="0db35-149">Hvis du vælger Tabel i feltet Kontokode, skal du vælge kontonummeret på den debitor, der er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0db35-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="0db35-150">Hvis du vælger Gruppe, skal du vælge debitorgruppen.</span><span class="sxs-lookup"><span data-stu-id="0db35-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="0db35-151">Hvis du vælger Alle, skal feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="0db35-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db35-152"><strong>Samlekonto</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="0db35-153">Vælg den finanskonto, der skal bruges som samlekonto for de debitorer, som er tilknyttet posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="0db35-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db35-154"><strong>Afregn konto</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="0db35-155">Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="0db35-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="0db35-156">Dette felt vises kun, hvis likviditetsbudgetter er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="0db35-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db35-157"><strong>Momsforudbetalinger</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="0db35-158">Angiv kontonummeret for momsbetaling, der er modtaget forud.</span><span class="sxs-lookup"><span data-stu-id="0db35-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="0db35-160"><strong>Bemærk!</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0db35-161">Brug siden Debitorparametre til at angive den posteringsprofil, der skal bruges, når en betaling er markeret som forudbetaling.</span><span class="sxs-lookup"><span data-stu-id="0db35-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db35-162"><strong>Passiver for rabatkonto</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="0db35-163">Vælg finanskontoen til rabatpassiver.</span><span class="sxs-lookup"><span data-stu-id="0db35-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0db35-164"><strong>Rykkerforløb</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="0db35-165">Vælg identifikationen for den rykkerserie, der skal bruges i forbindelse med debitorer, som har den aktuelle posteringsprofil tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="0db35-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0db35-166"><strong>Rentekode</strong></span><span class="sxs-lookup"><span data-stu-id="0db35-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="0db35-167">Vælg den rentekode, der skal bruges ved renteberegning for debitorer, som har den aktuelle posteringsprofil tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="0db35-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="0db35-168">**Tabelbegrænsninger**</span><span class="sxs-lookup"><span data-stu-id="0db35-168">**Table restrictions**</span></span>

<span data-ttu-id="0db35-169">For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere.</span><span class="sxs-lookup"><span data-stu-id="0db35-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="0db35-170">Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="0db35-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="0db35-171">Angiv følgende værdier for at definere en posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="0db35-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="0db35-172">Felt</span><span class="sxs-lookup"><span data-stu-id="0db35-172">Field</span></span>                 | <span data-ttu-id="0db35-173">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0db35-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db35-174">**Udligning**</span><span class="sxs-lookup"><span data-stu-id="0db35-174">**Settlement**</span></span>        | <span data-ttu-id="0db35-175">Vælg denne, hvis der skal kunne foretages automatisk udligning af poster med denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="0db35-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="0db35-176">Hvis denne indstilling ikke er markeret, skal du manuelt udligne posteringer ved hjælp af siden Udligning af åbne posteringer eller siden Angiv debitorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="0db35-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="0db35-177">**Renter**</span><span class="sxs-lookup"><span data-stu-id="0db35-177">**Interest**</span></span>          | <span data-ttu-id="0db35-178">Vælg denne, hvis der skal beregnes rente på udestående saldi for debitorkonti med denne profil.</span><span class="sxs-lookup"><span data-stu-id="0db35-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="0db35-179">Hvis denne ikke markeres, bliver der ikke beregnet rente for disse debitorer.</span><span class="sxs-lookup"><span data-stu-id="0db35-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="0db35-180">**Rykker**</span><span class="sxs-lookup"><span data-stu-id="0db35-180">**Collection letter**</span></span> | <span data-ttu-id="0db35-181">Vælg denne, hvis der skal genereres rykkere for debitorkonti med denne profil.</span><span class="sxs-lookup"><span data-stu-id="0db35-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="0db35-182">Hvis denne ikke markeres, bliver der ikke genereret rykkere for disse debitorer.</span><span class="sxs-lookup"><span data-stu-id="0db35-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="0db35-183">**Luk**</span><span class="sxs-lookup"><span data-stu-id="0db35-183">**Close**</span></span>             | <span data-ttu-id="0db35-184">Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="0db35-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="0db35-185">En post anses for lukket, når der er fuldt ud udlignet.</span><span class="sxs-lookup"><span data-stu-id="0db35-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="0db35-186">Du kan finde flere oplysninger i [Oversigt over debitorbetalinger](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0db35-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>

