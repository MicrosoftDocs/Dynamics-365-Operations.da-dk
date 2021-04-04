---
title: Kreditorposteringsprofil
description: Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022e7d979ca7572bb824bc5248fec8c0b3c283d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248153"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="a8ee4-103">Kreditorposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="a8ee4-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8ee4-104">Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="a8ee4-105">Kreditorposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="a8ee4-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="a8ee4-106">Kreditorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle kreditorer, en gruppe kreditorer eller en enkelt kreditor.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="a8ee4-107">Disse indstillinger bruges, når du opretter indkøbsordrer, kreditorfakturaer og kontantbetalinger.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="a8ee4-108">For nogle transaktioner kan du vælge en posteringsprofil, der er anderledes end, og som prioriteres højere end de posteringsprofiler, der er oprettet for transaktioner på denne side.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="a8ee4-109">Standardposteringsprofilen defineres i oversigtspanelet **Finans og Moms** på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="a8ee4-110">Standardposteringsprofilen medtages derefter automatisk i hovedet i nye dokumenter, hvor du kan ændre den til en anden posteringsprofil, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="a8ee4-111">Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden **Definitioner af posteringsbogføring**.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="a8ee4-112">I stedet for posteringsprofiler er det bogføringsdefinitioner, der styrer, hvordan kreditorposter bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="a8ee4-113">Oprette en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="a8ee4-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="a8ee4-114">**Opsætning**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-114">**Setup**</span></span>

<span data-ttu-id="a8ee4-115">Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="a8ee4-116">Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="a8ee4-117">Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="a8ee4-118">Feltværdien **Kontokode**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-118">**Account code** field value</span></span> | <span data-ttu-id="a8ee4-119">Feltværdien **Konto/gruppenummer**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="a8ee4-120">Søgeprioritet</span><span class="sxs-lookup"><span data-stu-id="a8ee4-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="a8ee4-121">**Tabellen**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-121">**Table**</span></span>                    | <span data-ttu-id="a8ee4-122">Specifik kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="a8ee4-122">Specific vendor account</span></span>                     | <span data-ttu-id="a8ee4-123">1</span><span class="sxs-lookup"><span data-stu-id="a8ee4-123">1</span></span>               |
| <span data-ttu-id="a8ee4-124">**Multi**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-124">**Group**</span></span>                    | <span data-ttu-id="a8ee4-125">Kreditorgruppe, som kreditoren er tildelt</span><span class="sxs-lookup"><span data-stu-id="a8ee4-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="a8ee4-126">2</span><span class="sxs-lookup"><span data-stu-id="a8ee4-126">2</span></span>               |
| <span data-ttu-id="a8ee4-127">**Alt**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-127">**All**</span></span>                      | <span data-ttu-id="a8ee4-128">Tom</span><span class="sxs-lookup"><span data-stu-id="a8ee4-128">Blank</span></span>                                       | <span data-ttu-id="a8ee4-129">3</span><span class="sxs-lookup"><span data-stu-id="a8ee4-129">3</span></span>               |

<span data-ttu-id="a8ee4-130">Hvis alle kreditorposteringer skal have samme posteringsprofil, skal du kun definere én posteringsprofil med **Alle** i feltet **Kontokode**.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="a8ee4-131">Angiv følgende værdier for at definere en posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a8ee4-132">Felt</span><span class="sxs-lookup"><span data-stu-id="a8ee4-132">Field</span></span></th>
<th><span data-ttu-id="a8ee4-133">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a8ee4-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8ee4-134"><strong>Posteringsprofil</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="a8ee4-135">Angiv en kode for posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="a8ee4-136">Du kan f.eks. oprette to posteringsprofiler for at have én konto til kreditorsaldi i indenlandsk valuta og én konto til kreditorsaldi i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="a8ee4-137">Du kan kalde den ene konto Indland og den anden Udland.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8ee4-138"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="a8ee4-139">Angiv en beskrivelse af posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8ee4-140"><strong>Kontokode</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="a8ee4-141">Angiv, om posteringsprofilen skal gælde for en bestemt kreditor, en gruppe kreditorer eller alle kreditorer:</span><span class="sxs-lookup"><span data-stu-id="a8ee4-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="a8ee4-142"><strong>Tabel</strong> – Posteringsprofilen anvendes til en enkelt kreditor.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="a8ee4-143">Vælg kreditorkontoen i feltet <strong>Konto/gruppenummer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="a8ee4-144"><strong>Gruppe</strong> – Posteringsprofilen anvendes til en kreditorgruppe.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="a8ee4-145">Vælg kreditorgruppen i feltet <strong>Konto/gruppenummer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="a8ee4-146"><strong>Alle</strong> – Posteringsprofilen anvendes til alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="a8ee4-147">Lad feltet <strong>Konto/gruppenummer</strong> være tomt.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8ee4-148"><strong>Konto/gruppenummer</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="a8ee4-149">Hvis du vælger <strong>Tabel</strong> i feltet <strong>Kontokode</strong>, skal du vælge kontonummeret på den kreditor, der er knyttet til posteringsprofilen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="a8ee4-150">Hvis <strong>Gruppe</strong> vælges, skal du vælge en kreditorgruppe.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="a8ee4-151">Hvis du vælger <strong>Alle</strong>, skal feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8ee4-152"><strong>Samlekonto</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="a8ee4-153">Vælg den finanskonto, der skal bruges som samlekonto for de kreditorer, som posteringsprofilerne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="a8ee4-154">Parameteren <strong>Tillad ikke manuel angivelse</strong> for denne hovedkonto markeres.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="a8ee4-155">Hvis du efterfølgende fjerner kontoen fra posteringsprofilen, skal du validere indstillingen <strong>Tillad ikke manuel angivelse</strong> på <strong>Hovedkonti</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="a8ee4-156"><strong>Bemærk:</strong> Hvis indstillingen <strong>Brug bogføringsdefinitioner</strong> er valgt på siden <strong>Finansparametre</strong>, bruges postbogføringsdefinitionen for kreditorfakturaer i stedet for samlekontoen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8ee4-157"><strong>Afregn konto</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="a8ee4-158">Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="a8ee4-159">Dette felt er kun tilgængeligt, når likviditetsbudgettering er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8ee4-160"><strong>Momsforudbetalinger</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="a8ee4-161">Vælg kontoen for momsbetaling, der er modtaget forud.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="a8ee4-162"><strong>Bemærk!</strong> Den posteringsprofil, der bruges, når betalingen er markeret som forudbetaling er markeret i <strong>posteringsprofilen</strong> med feltet <strong>Kladdebilag for forudbetaling</strong> i området <strong>Finans og Moms</strong> på siden <strong>Kreditorparametre</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8ee4-163"><strong>Indlevering</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="a8ee4-164">Vælg den finanskonto, som oplysninger om ikke-godkendte kreditorfakturaer skal bogføres på.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="a8ee4-165">Oplysningerne angives i indgangsbogskladden.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="a8ee4-166">En bruger angiver f.eks. meget grundlæggende oplysninger om kreditorfakturaer, når de modtages i indgangsbogen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="a8ee4-167">Når indgangsbogen bogføres, bogføres posterne på den konto, der er angivet her og i feltet <strong>Modkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="a8ee4-168">Når fakturaerne er godkendt, overføres gælden fra ankomstkontoen til den samlekonto, der bruges til kreditoren.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8ee4-169"><strong>Modkonto</strong></span><span class="sxs-lookup"><span data-stu-id="a8ee4-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="a8ee4-170">Vælg den finanskonto, der bruges som modkonto for ikke-godkendte kreditorfakturaer, der opdateres vha. indgangsbogen.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="a8ee4-171">Modkontoen fungerer som modkonto for poster, der bogføres på ankomstkonti.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="a8ee4-172">Derfor indeholder kontoen kreditorkøb, der endnu ikke er godkendt.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="a8ee4-173">**Tabelbegrænsninger**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-173">**Table restrictions**</span></span>

<span data-ttu-id="a8ee4-174">For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="a8ee4-175">Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="a8ee4-176">Angiv følgende værdier for at definere en posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="a8ee4-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="a8ee4-177">Felt</span><span class="sxs-lookup"><span data-stu-id="a8ee4-177">Field</span></span>          | <span data-ttu-id="a8ee4-178">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a8ee4-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ee4-179">**Udligning**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-179">**Settlement**</span></span> | <span data-ttu-id="a8ee4-180">Vælg denne indstilling for at kunne foretage automatisk udligning af poster med denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="a8ee4-181">Hvis ikke denne indstilling vælges, skal posteringerne udlignes manuelt på siden **Udlign åbne posteringer**.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="a8ee4-182">**Annuller**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-182">**Cancel**</span></span>     | <span data-ttu-id="a8ee4-183">Vælg denne indstilling, hvis du vil kunne annullere poster med denne posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="a8ee4-184">**Luk**</span><span class="sxs-lookup"><span data-stu-id="a8ee4-184">**Close**</span></span>      | <span data-ttu-id="a8ee4-185">Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="a8ee4-186">En post anses for lukket, når der er fuldt ud udlignet.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]