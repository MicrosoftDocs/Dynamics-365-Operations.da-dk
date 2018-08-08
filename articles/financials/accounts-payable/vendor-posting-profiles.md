---
title: Kreditorposteringsprofil
description: "Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ae019ebec2788fc499b0f2ef27a7eb2832ceaa9d
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="cef4c-103">Kreditorposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="cef4c-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cef4c-104">Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans.</span><span class="sxs-lookup"><span data-stu-id="cef4c-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="cef4c-105">Kreditorposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="cef4c-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="cef4c-106">Kreditorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle kreditorer, en gruppe kreditorer eller en enkelt kreditor.</span><span class="sxs-lookup"><span data-stu-id="cef4c-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="cef4c-107">Disse indstillinger bruges, når du opretter indkøbsordrer, kreditorfakturaer og kontantbetalinger.</span><span class="sxs-lookup"><span data-stu-id="cef4c-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="cef4c-108">For nogle transaktioner kan du vælge en posteringsprofil, der er anderledes end, og som prioriteres højere end de posteringsprofiler, der er oprettet for transaktioner på denne side.</span><span class="sxs-lookup"><span data-stu-id="cef4c-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="cef4c-109">Standardposteringsprofilen defineres i oversigtspanelet Finans og Moms på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="cef4c-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="cef4c-110">Standardposteringsprofilen medtages derefter automatisk i hovedet i nye dokumenter, hvor du kan ændre den til en anden posteringsprofil, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="cef4c-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="cef4c-111">Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden Definitioner af posteringsbogføring.</span><span class="sxs-lookup"><span data-stu-id="cef4c-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="cef4c-112">I stedet for posteringsprofiler er det bogføringsdefinitioner, der styrer, hvordan kreditorposter bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="cef4c-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="cef4c-113">Oprette en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="cef4c-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="cef4c-114">**Opsætning**</span><span class="sxs-lookup"><span data-stu-id="cef4c-114">**Setup**</span></span>

<span data-ttu-id="cef4c-115">Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="cef4c-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="cef4c-116">Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="cef4c-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="cef4c-117">Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge:</span><span class="sxs-lookup"><span data-stu-id="cef4c-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="cef4c-118">Feltværdien **Kontokode**</span><span class="sxs-lookup"><span data-stu-id="cef4c-118">**Account code** field value</span></span> | <span data-ttu-id="cef4c-119">Feltværdien **Konto/gruppenummer**</span><span class="sxs-lookup"><span data-stu-id="cef4c-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="cef4c-120">Søgeprioritet</span><span class="sxs-lookup"><span data-stu-id="cef4c-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="cef4c-121">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="cef4c-121">**Table**</span></span>                    | <span data-ttu-id="cef4c-122">Specifik kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="cef4c-122">Specific vendor account</span></span>                     | <span data-ttu-id="cef4c-123">1</span><span class="sxs-lookup"><span data-stu-id="cef4c-123">1</span></span>               |
| <span data-ttu-id="cef4c-124">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="cef4c-124">**Group**</span></span>                    | <span data-ttu-id="cef4c-125">kreditorgruppe, som kreditoren er tildelt</span><span class="sxs-lookup"><span data-stu-id="cef4c-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="cef4c-126">2</span><span class="sxs-lookup"><span data-stu-id="cef4c-126">2</span></span>               |
| <span data-ttu-id="cef4c-127">**Alle**</span><span class="sxs-lookup"><span data-stu-id="cef4c-127">**All**</span></span>                      | <span data-ttu-id="cef4c-128">Tom</span><span class="sxs-lookup"><span data-stu-id="cef4c-128">Blank</span></span>                                       | <span data-ttu-id="cef4c-129">3</span><span class="sxs-lookup"><span data-stu-id="cef4c-129">3</span></span>               |

<span data-ttu-id="cef4c-130">Hvis alle kreditorposteringer skal have samme posteringsprofil, skal du kun definere én posteringsprofil med Alle i feltet Kontokode.</span><span class="sxs-lookup"><span data-stu-id="cef4c-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="cef4c-131">Angiv følgende værdier for at definere en posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="cef4c-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cef4c-132">Felt</span><span class="sxs-lookup"><span data-stu-id="cef4c-132">Field</span></span></th>
<th><span data-ttu-id="cef4c-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cef4c-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cef4c-134"><strong>Posteringsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="cef4c-135">Angiv en kode for posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="cef4c-136">Du kan f.eks. oprette to posteringsprofiler for at have én konto til kreditorsaldi i indenlandsk valuta og én konto til kreditorsaldi i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="cef4c-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="cef4c-137">Du kan kalde den ene konto Indland og den anden Udland.</span><span class="sxs-lookup"><span data-stu-id="cef4c-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cef4c-138"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="cef4c-139">Angiv en beskrivelse af posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cef4c-140"><strong>Kontokode</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="cef4c-141">Angiv, om posteringsprofilen skal gælde for en bestemt kreditor, en gruppe kreditorer eller alle kreditorer:</span><span class="sxs-lookup"><span data-stu-id="cef4c-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="cef4c-142"><strong>Tabel</strong> – Posteringsprofilen anvendes til en enkelt kreditor.</span><span class="sxs-lookup"><span data-stu-id="cef4c-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="cef4c-143">Vælg kreditorkontoen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="cef4c-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="cef4c-144"><strong>Gruppe</strong> – Posteringsprofilen anvendes til en kreditorgruppe.</span><span class="sxs-lookup"><span data-stu-id="cef4c-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="cef4c-145">Vælg kreditorgruppen i feltet Konto/gruppenummer.</span><span class="sxs-lookup"><span data-stu-id="cef4c-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="cef4c-146"><strong>Alle</strong> – Posteringsprofilen anvendes til alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="cef4c-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="cef4c-147">Lad feltet Konto/gruppenummer være tomt.</span><span class="sxs-lookup"><span data-stu-id="cef4c-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cef4c-148"><strong>Konto/gruppenummer</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="cef4c-149">Hvis du vælger Tabel i feltet Kontokode, skal du vælge kontonummeret på den kreditor, der er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="cef4c-150">Hvis Gruppe vælges, skal du vælge en kreditorgruppe.</span><span class="sxs-lookup"><span data-stu-id="cef4c-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="cef4c-151">Hvis du vælger Alle, skal feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cef4c-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cef4c-152"><strong>Samlekonto</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="cef4c-153">Vælg den finanskonto, der skal bruges som samlekonto for de kreditorer, som posteringsprofilerne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="cef4c-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="cef4c-155"><strong>Bemærk!</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cef4c-156">Hvis Brug bogføringsdefinitioner er valgt på siden Finans, bruges postbogføringsdefinitionen for kreditorfakturaer i stedet for samlekontoen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cef4c-157"><strong>Afregn konto</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="cef4c-158">Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="cef4c-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="cef4c-159">Dette felt er kun tilgængeligt, når likviditetsbudgettering er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="cef4c-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cef4c-160"><strong>Momsforudbetalinger</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="cef4c-161">Vælg kontoen for momsbetaling, der er modtaget forud.</span><span class="sxs-lookup"><span data-stu-id="cef4c-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="cef4c-163"><strong>Bemærk!</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cef4c-164">Den posteringsprofil, der bruges, når betalingen er markeret som forudbetaling er markeret i posteringsprofilen med feltet kladdebilag for forudbetaling i området Finans og Moms på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="cef4c-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cef4c-165"><strong>Indlevering</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="cef4c-166">Vælg den finanskonto, som oplysninger om ikke-godkendte kreditorfakturaer skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="cef4c-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="cef4c-167">Oplysningerne angives i indgangsbogskladden.</span><span class="sxs-lookup"><span data-stu-id="cef4c-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="cef4c-168">En bruger angiver f.eks. meget grundlæggende oplysninger om kreditorfakturaer, når de modtages i indgangsbogen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="cef4c-169">Når indgangsbogen bogføres, bogføres posterne på den konto, der er angivet her og i feltet Modkonto.</span><span class="sxs-lookup"><span data-stu-id="cef4c-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="cef4c-170">Når fakturaerne er godkendt, overføres gælden fra ankomstkontoen til den samlekonto, der bruges til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="cef4c-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cef4c-171"><strong>Modkonto</strong></span><span class="sxs-lookup"><span data-stu-id="cef4c-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="cef4c-172">Vælg den finanskonto, der bruges som modkonto for ikke-godkendte kreditorfakturaer, der opdateres vha. indgangsbogen.</span><span class="sxs-lookup"><span data-stu-id="cef4c-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="cef4c-173">Modkontoen fungerer som modkonto for poster, der bogføres på ankomstkonti.</span><span class="sxs-lookup"><span data-stu-id="cef4c-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="cef4c-174">Derfor indeholder kontoen kreditorkøb, der endnu ikke er godkendt.</span><span class="sxs-lookup"><span data-stu-id="cef4c-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="cef4c-175">**Tabelbegrænsninger**</span><span class="sxs-lookup"><span data-stu-id="cef4c-175">**Table restrictions**</span></span>

<span data-ttu-id="cef4c-176">For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere.</span><span class="sxs-lookup"><span data-stu-id="cef4c-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="cef4c-177">Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="cef4c-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="cef4c-178">Angiv følgende værdier for at definere en posteringsprofil:</span><span class="sxs-lookup"><span data-stu-id="cef4c-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="cef4c-179">Felt</span><span class="sxs-lookup"><span data-stu-id="cef4c-179">Field</span></span>          | <span data-ttu-id="cef4c-180">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cef4c-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef4c-181">**Udligning**</span><span class="sxs-lookup"><span data-stu-id="cef4c-181">**Settlement**</span></span> | <span data-ttu-id="cef4c-182">Vælg denne indstilling for at kunne foretage automatisk udligning af poster med denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="cef4c-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="cef4c-183">Hvis ikke denne indstilling vælges, skal posteringerne udlignes manuelt på siden Udlign åbne posteringer.</span><span class="sxs-lookup"><span data-stu-id="cef4c-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="cef4c-184">**Annuller**</span><span class="sxs-lookup"><span data-stu-id="cef4c-184">**Cancel**</span></span>     | <span data-ttu-id="cef4c-185">Vælg denne indstilling, hvis du vil kunne annullere poster med denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="cef4c-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="cef4c-186">**Luk**</span><span class="sxs-lookup"><span data-stu-id="cef4c-186">**Close**</span></span>      | <span data-ttu-id="cef4c-187">Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="cef4c-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="cef4c-188">En post anses for lukket, når der er fuldt ud udlignet.</span><span class="sxs-lookup"><span data-stu-id="cef4c-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






