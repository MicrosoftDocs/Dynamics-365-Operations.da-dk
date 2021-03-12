---
title: Midler i den offentlige sektor
description: Et middel er et selvafstemmende sæt regnskabsbøger, der bruges til at styre og overvåge den planlagte udnyttelse af ressourcerne, ofte i overensstemmelse med de retlige og administrative krav. Organisationer i den offentlige sektor bruger midler til at demonstrere deres økonomiske ansvarlighed.
author: ShylaThompson
manager: AnnBe
ms.date: 08/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerFund, LedgerFundType
audience: Application User
ms.reviewer: roschlom
ms.custom: 19571
ms.assetid: c746c09f-dc9e-4381-ae92-e1af484064b6
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59ac067257b273dc8d778142a536c5035946acf1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992710"
---
# <a name="funds-in-the-public-sector"></a><span data-ttu-id="766f5-104">Midler i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="766f5-104">Funds in the public sector</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="766f5-105">Et middel er et selvafstemmende sæt regnskabsbøger, der bruges til at styre og overvåge den planlagte udnyttelse af ressourcerne, ofte i overensstemmelse med de retlige og administrative krav.</span><span class="sxs-lookup"><span data-stu-id="766f5-105">A fund is a self-balancing set of financial books that is used to control and monitor the planned use of resources, often in compliance with legal and administrative requirements.</span></span> <span data-ttu-id="766f5-106">Organisationer i den offentlige sektor bruger midler til at demonstrere deres økonomiske ansvarlighed.</span><span class="sxs-lookup"><span data-stu-id="766f5-106">Public-sector organizations use funds to demonstrate their fiscal accountability.</span></span>

<a name="what-general-ledger-parameters-should-be-set-for-funds"></a><span data-ttu-id="766f5-107">Hvilke Finans-parametre skal angives for midler?</span><span class="sxs-lookup"><span data-stu-id="766f5-107">What General ledger parameters should be set for funds?</span></span>
-------------------------------------------------------

<span data-ttu-id="766f5-108">Hvis du vil vide mere om de Finans-parametre, der er nødvendige for midler, skal du se under [Finans i den offentlige sektor](general-ledger-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="766f5-108">To learn about the General ledger parameters required for funds, see [General ledger in the public sector](general-ledger-public-sector.md).</span></span>

## <a name="what-fund-classes-and-fund-types-do-i-need-to-set-up"></a><span data-ttu-id="766f5-109">Hvilke middelklasser og -typer skal jeg angive?</span><span class="sxs-lookup"><span data-stu-id="766f5-109">What fund classes and fund types do I need to set up?</span></span>
<span data-ttu-id="766f5-110">GASB (Governmental Accounting Standards Board) anbefaler GAAP (Generally Accepted Accounting Principles) til regnskabsføring for delstater og lokale myndigheder.</span><span class="sxs-lookup"><span data-stu-id="766f5-110">The Governmental Accounting Standards Board (GASB) recommends a set of Generally Accepted Accounting Principles (GAAP) for state and local governmental accounting.</span></span>  <span data-ttu-id="766f5-111">GAAP identificerer otte middeltyper, der er kategoriseret i de tre middelklasser:</span><span class="sxs-lookup"><span data-stu-id="766f5-111">The GAAP identifies eight fund types that are categorized under the three fund classes:</span></span>

-   <span data-ttu-id="766f5-112">Offentlige midler</span><span class="sxs-lookup"><span data-stu-id="766f5-112">Governmental funds</span></span>
    -   <span data-ttu-id="766f5-113">Generelle midler</span><span class="sxs-lookup"><span data-stu-id="766f5-113">General fund</span></span>
    -   <span data-ttu-id="766f5-114">Særlige indtægtsmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-114">Special revenue funds</span></span>
    -   <span data-ttu-id="766f5-115">Midler i forbindelse med kapitalprojekter</span><span class="sxs-lookup"><span data-stu-id="766f5-115">Capital project funds</span></span>
    -   <span data-ttu-id="766f5-116">Midler i forbindelse med servicing af gæld</span><span class="sxs-lookup"><span data-stu-id="766f5-116">Debt service funds</span></span>
-   <span data-ttu-id="766f5-117">Beskyttede midler eller forretningsrelaterede midler</span><span class="sxs-lookup"><span data-stu-id="766f5-117">Proprietary, or business-type, funds</span></span>
    -   <span data-ttu-id="766f5-118">Virksomhedsmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-118">Enterprise funds</span></span>
    -   <span data-ttu-id="766f5-119">Interne tjenestemidler</span><span class="sxs-lookup"><span data-stu-id="766f5-119">Internal service funds</span></span>
-   <span data-ttu-id="766f5-120">Fiduciariske midler</span><span class="sxs-lookup"><span data-stu-id="766f5-120">Fiduciary funds</span></span>
    -   <span data-ttu-id="766f5-121">Forvaltningsmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-121">Trust funds</span></span>
    -   <span data-ttu-id="766f5-122">Agenturmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-122">Agency funds</span></span>

<span data-ttu-id="766f5-123">De tre GAAP middelklasser, plus en **Notat** klasse, er foruddefinerede indstillinger i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="766f5-123">The three GAAP fund classes, plus a **Memo** class, are predefined options in Dynamics 365 Finance.</span></span> 

<span data-ttu-id="766f5-124">Middeltyper defineres i henhold til organisationens behov.</span><span class="sxs-lookup"><span data-stu-id="766f5-124">Fund types are defined according to the needs of the organization.</span></span> <span data-ttu-id="766f5-125">I de fleste tilfælde skal du angive de otte typer af GAAP-midler.</span><span class="sxs-lookup"><span data-stu-id="766f5-125">In most cases, you’ll set up the eight GAAP fund types.</span></span> <span data-ttu-id="766f5-126">Middeltyperne grupperer midler til detaljeret finansiel opfølgning og rapportering.</span><span class="sxs-lookup"><span data-stu-id="766f5-126">The fund types group funds for detailed fiscal tracking and reporting.</span></span> <span data-ttu-id="766f5-127">Mange midler kan indgå i en enkelt overordnet rapport, men de enkelte midler forbliver en særskilt finansiel og regnskabsmæssig enhed med sin egen finans, resultatopgørelse og egne balancerapporter.</span><span class="sxs-lookup"><span data-stu-id="766f5-127">Many funds can be included in a single high-level report, but each fund remains a separate fiscal and accounting entity with its own general ledger, income statements, and balance sheet reports.</span></span> 

<span data-ttu-id="766f5-128">Hvert enkelt middel skal have et entydigt middelnummer.</span><span class="sxs-lookup"><span data-stu-id="766f5-128">Each fund must have a unique fund number.</span></span> <span data-ttu-id="766f5-129">Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel.</span><span class="sxs-lookup"><span data-stu-id="766f5-129">Fund numbers are used as dimension values in financial account numbers where a dimension has been mapped to a fund.</span></span> <span data-ttu-id="766f5-130">Når et kontonummer er knyttet til et bestemt middel, tilhører det en række finansielle regnskabsbøger, der er omfattet af dette middel.</span><span class="sxs-lookup"><span data-stu-id="766f5-130">When an account number is linked to a particular fund, it belongs to the set of financial books that are contained by that fund.</span></span>

### <a name="example"></a><span data-ttu-id="766f5-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="766f5-131">Example</span></span>

<span data-ttu-id="766f5-132">Her er en liste over nogle af de midler, der kan bruges af myndighederne i en by:</span><span class="sxs-lookup"><span data-stu-id="766f5-132">Here’s a list of some of the funds that might be used by a town government:</span></span>

-   <span data-ttu-id="766f5-133">Generelt middel</span><span class="sxs-lookup"><span data-stu-id="766f5-133">General Fund</span></span>
-   <span data-ttu-id="766f5-134">School of Technology</span><span class="sxs-lookup"><span data-stu-id="766f5-134">School of Technology</span></span>
-   <span data-ttu-id="766f5-135">Informationsteknologi</span><span class="sxs-lookup"><span data-stu-id="766f5-135">Information Technology</span></span>
-   <span data-ttu-id="766f5-136">Farmers Market</span><span class="sxs-lookup"><span data-stu-id="766f5-136">Farmers Market</span></span>
-   <span data-ttu-id="766f5-137">Utilities Commission</span><span class="sxs-lookup"><span data-stu-id="766f5-137">Utilities Commission</span></span>
-   <span data-ttu-id="766f5-138">Fragttjeneste</span><span class="sxs-lookup"><span data-stu-id="766f5-138">Courier Service</span></span>
-   <span data-ttu-id="766f5-139">Worker’s Compensation Fund</span><span class="sxs-lookup"><span data-stu-id="766f5-139">Worker’s Compensation Fund</span></span>
-   <span data-ttu-id="766f5-140">Omfattende medicinordning</span><span class="sxs-lookup"><span data-stu-id="766f5-140">Comprehensive Major Medical Plan</span></span>
-   <span data-ttu-id="766f5-141">Udskudt aflønning</span><span class="sxs-lookup"><span data-stu-id="766f5-141">Deferred Compensation</span></span>
-   <span data-ttu-id="766f5-142">Opkrævning af lokal moms</span><span class="sxs-lookup"><span data-stu-id="766f5-142">Local Sales Tax Collections</span></span>
-   <span data-ttu-id="766f5-143">Domstolsansatte</span><span class="sxs-lookup"><span data-stu-id="766f5-143">Clerk of Courts</span></span>

<span data-ttu-id="766f5-144">Følgende tabel viser disse midler grupperet efter klasse og middeltype.</span><span class="sxs-lookup"><span data-stu-id="766f5-144">The following table shows these funds grouped by fund class and fund type.</span></span>

|                |                        |                 |                                  |
|----------------|------------------------|-----------------|----------------------------------|
| <span data-ttu-id="766f5-145">**Finansieringskildeklasse**</span><span class="sxs-lookup"><span data-stu-id="766f5-145">**Fund class**</span></span> | <span data-ttu-id="766f5-146">**Finansieringskildetype**</span><span class="sxs-lookup"><span data-stu-id="766f5-146">**Fund type**</span></span>          | <span data-ttu-id="766f5-147">**Finansieringskildenummer**</span><span class="sxs-lookup"><span data-stu-id="766f5-147">**Fund number**</span></span> | <span data-ttu-id="766f5-148">**Navn på finansieringskilde**</span><span class="sxs-lookup"><span data-stu-id="766f5-148">**Fund name**</span></span>                    |
| <span data-ttu-id="766f5-149">Offentlig</span><span class="sxs-lookup"><span data-stu-id="766f5-149">Governmental</span></span>   | <span data-ttu-id="766f5-150">Generelt middel</span><span class="sxs-lookup"><span data-stu-id="766f5-150">General Fund</span></span>           | <span data-ttu-id="766f5-151">1103</span><span class="sxs-lookup"><span data-stu-id="766f5-151">1103</span></span>            | <span data-ttu-id="766f5-152">Generelt middel</span><span class="sxs-lookup"><span data-stu-id="766f5-152">General Fund</span></span>                     |
|                | <span data-ttu-id="766f5-153">Særlige indtægtsmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-153">Special Revenue Funds</span></span>  | <span data-ttu-id="766f5-154">1343</span><span class="sxs-lookup"><span data-stu-id="766f5-154">1343</span></span>            | <span data-ttu-id="766f5-155">School of Technology</span><span class="sxs-lookup"><span data-stu-id="766f5-155">School of Technology</span></span>             |
|                |                        | <span data-ttu-id="766f5-156">1372</span><span class="sxs-lookup"><span data-stu-id="766f5-156">1372</span></span>            | <span data-ttu-id="766f5-157">Informationsteknologi</span><span class="sxs-lookup"><span data-stu-id="766f5-157">Information Technology</span></span>           |
| <span data-ttu-id="766f5-158">Beskyttede</span><span class="sxs-lookup"><span data-stu-id="766f5-158">Proprietary</span></span>    | <span data-ttu-id="766f5-159">Virksomhedsmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-159">Enterprise Funds</span></span>       | <span data-ttu-id="766f5-160">2501</span><span class="sxs-lookup"><span data-stu-id="766f5-160">2501</span></span>            | <span data-ttu-id="766f5-161">Farmers Market</span><span class="sxs-lookup"><span data-stu-id="766f5-161">Farmers Market</span></span>                   |
|                |                        | <span data-ttu-id="766f5-162">2541</span><span class="sxs-lookup"><span data-stu-id="766f5-162">2541</span></span>            | <span data-ttu-id="766f5-163">Utilities Commission</span><span class="sxs-lookup"><span data-stu-id="766f5-163">Utilities Commission</span></span>             |
|                | <span data-ttu-id="766f5-164">Interne tjenestemidler</span><span class="sxs-lookup"><span data-stu-id="766f5-164">Internal Service Funds</span></span> | <span data-ttu-id="766f5-165">2723</span><span class="sxs-lookup"><span data-stu-id="766f5-165">2723</span></span>            | <span data-ttu-id="766f5-166">Fragttjeneste</span><span class="sxs-lookup"><span data-stu-id="766f5-166">Courier Service</span></span>                  |
|                |                        | <span data-ttu-id="766f5-167">2738</span><span class="sxs-lookup"><span data-stu-id="766f5-167">2738</span></span>            | <span data-ttu-id="766f5-168">Worker’s Compensation Fund</span><span class="sxs-lookup"><span data-stu-id="766f5-168">Worker’s Compensation Fund</span></span>       |
| <span data-ttu-id="766f5-169">Fiduciariske</span><span class="sxs-lookup"><span data-stu-id="766f5-169">Fiduciary</span></span>      | <span data-ttu-id="766f5-170">Pension Trust Funds</span><span class="sxs-lookup"><span data-stu-id="766f5-170">Pension Trust Funds</span></span>    | <span data-ttu-id="766f5-171">3320</span><span class="sxs-lookup"><span data-stu-id="766f5-171">3320</span></span>            | <span data-ttu-id="766f5-172">Omfattende medicinordning</span><span class="sxs-lookup"><span data-stu-id="766f5-172">Comprehensive Major Medical Plan</span></span> |
|                |                        | <span data-ttu-id="766f5-173">3324</span><span class="sxs-lookup"><span data-stu-id="766f5-173">3324</span></span>            | <span data-ttu-id="766f5-174">Udskudt aflønning</span><span class="sxs-lookup"><span data-stu-id="766f5-174">Deferred Compensation</span></span>            |
|                | <span data-ttu-id="766f5-175">Agenturmidler</span><span class="sxs-lookup"><span data-stu-id="766f5-175">Agency Funds</span></span>           | <span data-ttu-id="766f5-176">3912</span><span class="sxs-lookup"><span data-stu-id="766f5-176">3912</span></span>            | <span data-ttu-id="766f5-177">Opkrævning af lokal moms</span><span class="sxs-lookup"><span data-stu-id="766f5-177">Local Sales Tax Collections</span></span>      |
|                |                        | <span data-ttu-id="766f5-178">3914</span><span class="sxs-lookup"><span data-stu-id="766f5-178">3914</span></span>            | <span data-ttu-id="766f5-179">Domstolsansatte</span><span class="sxs-lookup"><span data-stu-id="766f5-179">Clerk of Courts</span></span>                  |

## <a name="how-are-financial-dimensions-used-with-funds"></a><span data-ttu-id="766f5-180">Hvordan bruges økonomiske dimensioner med midler?</span><span class="sxs-lookup"><span data-stu-id="766f5-180">How are financial dimensions used with funds?</span></span>
<span data-ttu-id="766f5-181">Hvert enkelt middel skal have et entydigt middelnummer.</span><span class="sxs-lookup"><span data-stu-id="766f5-181">Each fund must have a unique fund number.</span></span> <span data-ttu-id="766f5-182">Middeltal bruges som dimensionsværdier i økonomiske kontonumre, hvor en dimension er knyttet til et middel.</span><span class="sxs-lookup"><span data-stu-id="766f5-182">Fund numbers are used as dimension values in financial account numbers where a dimension has been mapped to a fund.</span></span> <span data-ttu-id="766f5-183">Når et kontonummer er knyttet til et bestemt middel, tilhører det en række finansielle regnskabsbøger, der er omfattet af dette middel.</span><span class="sxs-lookup"><span data-stu-id="766f5-183">When an account number is linked to a particular fund, it belongs to the set of financial books that are contained by that fund.</span></span> 

<span data-ttu-id="766f5-184">Offentlige organisationer kræver normalt afstemte poster for økonomiske dimensioner, der er relateret til midler.</span><span class="sxs-lookup"><span data-stu-id="766f5-184">Public sector organizations usually require balanced entries for financial dimensions related to funds.</span></span> <span data-ttu-id="766f5-185">Når en økonomisk dimension eller en kombination af dimensioner er markeret til at kræve afstemte poster, vil systemet ikke bogføre en transaktion, hvor debet ikke svarer til kredit for den økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="766f5-185">When a financial dimension or a combination of dimensions is marked to require balanced entries, the system will not post a transaction where debits do not equal credits for the financial dimension.</span></span>

## <a name="how-do-i-set-a-fund-balance-to-carry-over-to-the-new-year"></a><span data-ttu-id="766f5-186">Hvordan indstiller jeg en middelsaldo, som skal overføres til det nye år?</span><span class="sxs-lookup"><span data-stu-id="766f5-186">How do I set a fund balance to carry over to the new year?</span></span>
<span data-ttu-id="766f5-187">Hvis du vil vide mere om årsafslutningen for midler, skal du se under [Årsafslutningen i den offentlige sektor](year-end-processing-public-sector.md).</span><span class="sxs-lookup"><span data-stu-id="766f5-187">To learn about year-end processing for funds, see [Year-end processing in the public sector](year-end-processing-public-sector.md).</span></span>


<span data-ttu-id="766f5-188">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="766f5-188">For more information, see the following topics:</span></span>

[<span data-ttu-id="766f5-189">Oprettelse af en middeltype</span><span class="sxs-lookup"><span data-stu-id="766f5-189">Create a fund type</span></span>](tasks/create-fund-type-public-sector.md)

[<span data-ttu-id="766f5-190">Konfigurere et middel</span><span class="sxs-lookup"><span data-stu-id="766f5-190">Set up a fund</span></span>](tasks/set-up-fund-public-sector.md)




