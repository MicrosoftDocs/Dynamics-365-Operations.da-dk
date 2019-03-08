---
title: Planlægning af engangsleverandører i den offentlige sektor
description: Denne artikel beskriver, hvordan du forbereder import og oprettelse af flere engangskreditorer og fakturaer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27251
ms.assetid: 936570cb-932f-4027-b3c7-2235ad79bc1c
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29468ab0dc20ff0c9c15ad242cfd5900c321ec0d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "370303"
---
# <a name="plan-for-one-time-vendors-in-the-public-sector"></a><span data-ttu-id="c1fb2-103">Planlægning af engangsleverandører i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="c1fb2-103">Plan for one-time vendors in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1fb2-104">Denne artikel beskriver, hvordan du forbereder import og oprettelse af flere engangskreditorer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-104">This article explains how to prepare to import and create multiple one-time vendors and invoices.</span></span> 

<span data-ttu-id="c1fb2-105">Hvis du planlægger at masseimportere leverandør- og importoplysninger, skal du typisk først oprette en datafil i regnearksformat og gemme den i CSV-format (kommaseparerede værdier).</span><span class="sxs-lookup"><span data-stu-id="c1fb2-105">Typically, if you plan to mass-import vendor and invoice information, you first create a data file in spreadsheet format and save it in CSV (comma-separated values) format.</span></span>

-   <span data-ttu-id="c1fb2-106">Da der bruges komma til at adskille felterne i en CSV-fil, må du ikke bruge kommaer i teksten i en post.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-106">Because commas are used to separate the fields in a CSV file, don't use commas in the text of an entry.</span></span> <span data-ttu-id="c1fb2-107">Hvis du f.eks. vil angive firmanavnet "Smith, Jensen og Jensen", skal du indtaste det som **Smith Jensen og Jensen**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-107">For example, to specify a company name of “Smith, Smith, and Jones,” enter it as **Smith Smith and Jones**.</span></span>
-   <span data-ttu-id="c1fb2-108">Hvis du ikke angiver værdier for felter på denne side, bruger de nyoprettede kreditorkonti værdier fra den engangskreditorprofil, der er henvist til på siden **Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-108">If you don't set values for fields on this page, the newly created vendor accounts use values from the one-time vendor profile that is referenced on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="c1fb2-109">Hvis betalingsmetoden f.eks. er angivet til **Bankcheck** for engangskreditorprofilen på siden **Kreditorparametre**, så angives denne betalingsmetode også for de engangskreditorer, som du tilføjer.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-109">For example, if the method of payment is set to **Check** for the one-time vendor profile on the **Accounts payable parameters** page, that method of payment will also be set for the one-time vendors that you're adding.</span></span>
-   <span data-ttu-id="c1fb2-110">Kreditornummerserien **Engangsleverandør** bruges til at tildele engangskreditorkontiene og må ikke være angivet til **Fortløbende** for denne tjeneste.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-110">The **One-time supplier** Accounts payable number sequence is used to assign the one-time vendor accounts and must not be set to **Continuous** for this service.</span></span> <span data-ttu-id="c1fb2-111">Fakturaer genereres i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-111">Invoices are generated in a draft state.</span></span> <span data-ttu-id="c1fb2-112">Før du opretter betalingsforslag til betaling, skal du bogføre fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-112">Before you create payment proposals for payment, you must post the invoices.</span></span>

<span data-ttu-id="c1fb2-113">Følgende tabel viser de felter, som den importerede fil skal indeholde.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-113">The following table show the fields that the import file must contain.</span></span> <span data-ttu-id="c1fb2-114">Hver enkelt feltetiket svarer til en kolonneoverskrift i et regneark, og hver række i regnearket indeholder dataene for hver relevant kolonne.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-114">Each field label is equivalent to a column heading in a spreadsheet, and each spreadsheet row contains the data for each applicable column.</span></span>

<span data-ttu-id="c1fb2-115">**Kreditorsektion**</span><span class="sxs-lookup"><span data-stu-id="c1fb2-115">**Vendor section**</span></span>

| <span data-ttu-id="c1fb2-116">Felt</span><span class="sxs-lookup"><span data-stu-id="c1fb2-116">Field</span></span>                                          | <span data-ttu-id="c1fb2-117">Oplysninger</span><span class="sxs-lookup"><span data-stu-id="c1fb2-117">Details</span></span>                                                 |
|------------------------------------------------|---------------------------------------------------------|
|<span data-ttu-id="c1fb2-118">Posttype</span><span class="sxs-lookup"><span data-stu-id="c1fb2-118">Record type</span></span>                                     | <span data-ttu-id="c1fb2-119">**Person** eller **Organisation**</span><span class="sxs-lookup"><span data-stu-id="c1fb2-119">**Person** or **Organization**</span></span>                          |
| <span data-ttu-id="c1fb2-120">Fornavn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-120">First name</span></span>                                     | <span data-ttu-id="c1fb2-121">(Hvis posttypeværdien er **Person**)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-121">(If the record type value is **Person**)</span></span>                |
| <span data-ttu-id="c1fb2-122">Mellemnavn (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="c1fb2-122">Middle name (Optional)</span></span>                         | <span data-ttu-id="c1fb2-123">(Hvis posttypen er **Person**)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-123">(If the record type is **Person**)</span></span>                      |
| <span data-ttu-id="c1fb2-124">Efternavn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-124">Last name</span></span>                                      | <span data-ttu-id="c1fb2-125">(Hvis posttypen er **Person**)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-125">(If the record type is **Person**)</span></span>                      |
| <span data-ttu-id="c1fb2-126">Navn på kreditor</span><span class="sxs-lookup"><span data-stu-id="c1fb2-126">Vendor name</span></span>                                    | <span data-ttu-id="c1fb2-127">(Hvis posttypen er **Organisation**)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-127">(If the record type is **Organization**)</span></span>                |
| <span data-ttu-id="c1fb2-128">Gruppe</span><span class="sxs-lookup"><span data-stu-id="c1fb2-128">Group</span></span>                                          | <span data-ttu-id="c1fb2-129">Grænse på 10 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-129">Ten-character limit</span></span>                                     |
| <span data-ttu-id="c1fb2-130">Land/område</span><span class="sxs-lookup"><span data-stu-id="c1fb2-130">Country/region</span></span>                                 | <span data-ttu-id="c1fb2-131">Grænse på 10 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-131">Ten-character limit</span></span>                                     |
| <span data-ttu-id="c1fb2-132">Postnummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-132">ZIP/postal code</span></span>                                |                                                         |
| <span data-ttu-id="c1fb2-133">Gade</span><span class="sxs-lookup"><span data-stu-id="c1fb2-133">Street</span></span>                                         |                                                         |
| <span data-ttu-id="c1fb2-134">By</span><span class="sxs-lookup"><span data-stu-id="c1fb2-134">City</span></span>                                           |                                                         |
| <span data-ttu-id="c1fb2-135">By</span><span class="sxs-lookup"><span data-stu-id="c1fb2-135">City</span></span>                                           |                                                         |
|<span data-ttu-id="c1fb2-136">Federal Tax ID (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-136">Federal tax ID (Optional)</span></span>                       | <span data-ttu-id="c1fb2-137">(Kun USA) 1099-nummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-137">(U.S. only) 1099 number</span></span>                                 |
| <span data-ttu-id="c1fb2-138">1099-nummertype</span><span class="sxs-lookup"><span data-stu-id="c1fb2-138">Tax ID type</span></span>                                    | <span data-ttu-id="c1fb2-139">(Kun USA) Værdierne kan være **Ukendt**, **Employer Identification Number (EIN - US)**, **Social Security Number (SSN - US)**, **Individuelt Taxpayer Identification Number (TIN - US)**, eller **Anvendt Taxpayer Identification Number (TIN - US)**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-139">(U.S. only) Values can be **Unknown**, **Employer Identification Number**, **Social Security Number**, **Individual Taxpayer Identification Number**, or **Adopted Tax Payer Identification Number**.</span></span>  <span data-ttu-id="c1fb2-140">**Bemærk:** Hvis der ikke er angivet noget Federal Tax ID, indstilles feltet til **ukendt**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-140">**Note:** If no federal tax ID is provided, this field should be set to **Unknown**.</span></span>                                               |
| <span data-ttu-id="c1fb2-141">Bankkonto (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-141">Bank account (Optional)</span></span>                        | <span data-ttu-id="c1fb2-142">Bankkontonavn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-142">Bank account name</span></span>                                       |
| <span data-ttu-id="c1fb2-143">Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-143">Bank account number</span></span>                            |                                                         |
| <span data-ttu-id="c1fb2-144">Registreringsnummer (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-144">Routing number (Optional)</span></span>                      |                                                         |
| <span data-ttu-id="c1fb2-145">SWIFT-kode (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-145">SWIFT code (Optional)</span></span>                          | <span data-ttu-id="c1fb2-146">Også kaldet BIC-kode (Bank Identifier Code).</span><span class="sxs-lookup"><span data-stu-id="c1fb2-146">Also known as BIC (Bank identifier code)</span></span>                |
|<span data-ttu-id="c1fb2-147">IBAN (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-147">IBAN (Optional)</span></span>                                 | <span data-ttu-id="c1fb2-148">IBAN (International Bank Account Number). Maks. 34 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-148">International bank account number, 34-character limit</span></span>   |



<span data-ttu-id="c1fb2-149">**Fakturasektion**</span><span class="sxs-lookup"><span data-stu-id="c1fb2-149">**Invoice section**</span></span>

| <span data-ttu-id="c1fb2-150">Felt</span><span class="sxs-lookup"><span data-stu-id="c1fb2-150">Field</span></span>                                                | <span data-ttu-id="c1fb2-151">Oplysninger</span><span class="sxs-lookup"><span data-stu-id="c1fb2-151">Details</span></span>                                           |
|------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c1fb2-152">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-152">Invoice number</span></span>                                       | <span data-ttu-id="c1fb2-153">Fakturanummer. Maks. 20 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-153">Invoice number, 20-character limit</span></span>                |
| <span data-ttu-id="c1fb2-154">Fakturabeskrivelse (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-154">Invoice description (Optional)</span></span>                       |                                                   |
| <span data-ttu-id="c1fb2-155">Bogføringsdato (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-155">Posting date (Optional)</span></span>                              | <span data-ttu-id="c1fb2-156">Datoformat</span><span class="sxs-lookup"><span data-stu-id="c1fb2-156">Date format</span></span>                                       |
| <span data-ttu-id="c1fb2-157">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="c1fb2-157">Invoice date</span></span>                                         | <span data-ttu-id="c1fb2-158">Datoformat</span><span class="sxs-lookup"><span data-stu-id="c1fb2-158">Date format</span></span>                                       |
| <span data-ttu-id="c1fb2-159">Forfaldsdato (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-159">Due date (Optional)</span></span>                                  | <span data-ttu-id="c1fb2-160">Datoformat</span><span class="sxs-lookup"><span data-stu-id="c1fb2-160">Date format</span></span>                                       |
| <span data-ttu-id="c1fb2-161">Linjenummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-161">Line number</span></span>                                          |                                                   |
|<span data-ttu-id="c1fb2-162">Varenummer (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-162">Item number (Optional)</span></span>                                | <span data-ttu-id="c1fb2-163">Grænse på 20 tegn   **Bemærk!** Hvis der ikke er angivet noget varenummer, skal du angive værdier i felterne **Indkøbskategori** og **Indkøbskategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-163">20-character limit   **Note:** If no item number is provided, you must provide values in the **Procurement category** and **Procurement category hierarchy** fields.</span></span> <span data-ttu-id="c1fb2-164">Hvis ingen indkøbskategori og intet indkøbskategorihierarki er angivet, skal du angive en værdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-164">If no procurement category and procurement category hierarchy are provided, you must provide a value in the **Item number** field.</span></span>                    |
| <span data-ttu-id="c1fb2-165">Varenavn (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-165">Item name (Optional)</span></span>                                 |  <span data-ttu-id="c1fb2-166">Maks. 60 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-166">60-character limit</span></span>                               |
| <span data-ttu-id="c1fb2-167">Indkøbskategorihierarki (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-167">Procurement category hierarchy (Optional)</span></span>            |    <span data-ttu-id="c1fb2-168">**Bemærk!** Hvis du angiver en værdi for dette felt, skal feltet **Indkøbskategori** også udfyldes.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-168">**Note:** If you provide a value for this field, the **Procurement category** field is also required.</span></span>                                                                         |
| <span data-ttu-id="c1fb2-169">Indkøbskategori (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-169">Procurement category (Optional)</span></span>                      | <span data-ttu-id="c1fb2-170">**Bemærk!** Hvis du angiver en værdi for dette felt, skal feltet **Indkøbskategorihierarki** også udfyldes.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-170">**Note:** If you provide a value for this field, the **Procurement category hierarchy** field is also required.</span></span>                                                                        |
| <span data-ttu-id="c1fb2-171">Antal (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-171">Quantity (Optional)</span></span>                                  |                                                   |
| <span data-ttu-id="c1fb2-172">Enhed (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-172">Unit (Optional)</span></span>                                      | <span data-ttu-id="c1fb2-173">Grænse på 10 tegn</span><span class="sxs-lookup"><span data-stu-id="c1fb2-173">Ten-character limit</span></span>                               |
|<span data-ttu-id="c1fb2-174">Linjenettobeløb</span><span class="sxs-lookup"><span data-stu-id="c1fb2-174">Line net amount</span></span>                                       | <span data-ttu-id="c1fb2-175">Decimalværdier er tilladt.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-175">Decimal values are allowed.</span></span>                       |
| <span data-ttu-id="c1fb2-176">Enhedspris (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="c1fb2-176">Unit price (Optional)</span></span>                                | <span data-ttu-id="c1fb2-177">Decimalværdier er tilladt.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-177">Decimal values are allowed.</span></span>                       |


<span data-ttu-id="c1fb2-178">**Distributionssektion**</span><span class="sxs-lookup"><span data-stu-id="c1fb2-178">**Distributions section**</span></span>

| <span data-ttu-id="c1fb2-179">Felt</span><span class="sxs-lookup"><span data-stu-id="c1fb2-179">Field</span></span>                                                | <span data-ttu-id="c1fb2-180">Oplysninger</span><span class="sxs-lookup"><span data-stu-id="c1fb2-180">Details</span></span>                                  |
|------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="c1fb2-181">Antal</span><span class="sxs-lookup"><span data-stu-id="c1fb2-181">Number</span></span>                                               | <span data-ttu-id="c1fb2-182">Regnskabsfordelingslinjenummer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-182">Accounting distribution line number</span></span>      |
| <span data-ttu-id="c1fb2-183">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c1fb2-183">Ledger account</span></span>                                       |                                          |
| <span data-ttu-id="c1fb2-184">Procent</span><span class="sxs-lookup"><span data-stu-id="c1fb2-184">Percent</span></span>                                              | <span data-ttu-id="c1fb2-185">Decimalværdier er tilladt.</span><span class="sxs-lookup"><span data-stu-id="c1fb2-185">Decimal values are allowed.</span></span>              |




## <a name="what-do-i-do-next"></a><span data-ttu-id="c1fb2-186">Hvad skal jeg gøre nu?</span><span class="sxs-lookup"><span data-stu-id="c1fb2-186">What do I do next?</span></span>
<span data-ttu-id="c1fb2-187">Når du har konfigureret forudsætninger, du skal bruge, kan du se [Engangsleverandører i den offentlige sektor](one-time-vendors-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="c1fb2-187">After you’ve set up the prerequisites that you require, see [One time vendors in the public sector](one-time-vendors-public-sector.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="c1fb2-188">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c1fb2-188">Additional resources</span></span>
--------

[<span data-ttu-id="c1fb2-189">Engangsleverandører i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="c1fb2-189">One-time vendors in the public sector</span></span>](one-time-vendors-public-sector.md)

[<span data-ttu-id="c1fb2-190">Kreditor i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="c1fb2-190">Accounts payable in the public sector</span></span>](accounts-payable-public-sector.md)



