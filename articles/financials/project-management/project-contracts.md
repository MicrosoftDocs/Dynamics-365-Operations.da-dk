---
title: Projektkontrakter
description: "I denne artikel beskrives og gives eksempler på de projektkontrakter, du kan oprette for forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektets debitorer i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2017

---

# <a name="project-contracts"></a><span data-ttu-id="eaaef-103">Projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="eaaef-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eaaef-104">I denne artikel beskrives og gives eksempler på de projektkontrakter, du kan oprette for forskellige typer projekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere projektets debitorer i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="eaaef-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="eaaef-105">Den type projekt, du opretter til en projektkontrakt, afgør, hvilken metode der bruges til fakturering af projektdebitorere.</span><span class="sxs-lookup"><span data-stu-id="eaaef-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="eaaef-106">Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="eaaef-107">Når du bruger en projektkontrakt, kan du fakturere ét eller flere projekter på én gang.</span><span class="sxs-lookup"><span data-stu-id="eaaef-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="eaaef-108">Med projektkontrakten kan du også sikre en konsistent faktureringsprocedure til hvert underprojekt i en projektstruktur.</span><span class="sxs-lookup"><span data-stu-id="eaaef-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="eaaef-109">Hvert projekt, der skal faktureres, skal være tilknyttet en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="eaaef-110">Indstillingerne for en projektkontrakt gælder for alle projekter og underprojekter, der er tilknyttet den pågældende projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="eaaef-111">I en projektkontrakt kan der angives én eller flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="eaaef-112">Du kan derfor opdele fakturering blandt flere finansieringskilder, konfigurere finansieringsgrænser, så finansieringskilder ikke faktureres mere end et bestemt beløb, og konfigurere finansieringsregler for opkrævning af udgifter.</span><span class="sxs-lookup"><span data-stu-id="eaaef-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="eaaef-113">Finansiering af projektkontrakter</span><span class="sxs-lookup"><span data-stu-id="eaaef-113">Funding for project contracts</span></span>
<span data-ttu-id="eaaef-114">Visse projektkontrakter kan angive, at flere parter deler ansvaret for finansiering af projektomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="eaaef-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="eaaef-115">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="eaaef-115">Here are some examples:</span></span>

-   <span data-ttu-id="eaaef-116">En stor kunde, der har flere afdelinger, anmoder om, at finansieringen af et projekt skal opdeles efter afdeling.</span><span class="sxs-lookup"><span data-stu-id="eaaef-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="eaaef-117">Firmaet deler udgifterne til et stort projekt med en ekstern organisation.</span><span class="sxs-lookup"><span data-stu-id="eaaef-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="eaaef-118">Et vejprojekt finansieres i fællesskab af to kommuner.</span><span class="sxs-lookup"><span data-stu-id="eaaef-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="eaaef-119">Et broprojekt finansieres af statslige tilskud og en privat virksomhed.</span><span class="sxs-lookup"><span data-stu-id="eaaef-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="eaaef-120">I Finance and Operations kan du opdele fakturering for en enkelt postering eller et helt projekt mellem flere debitorer, tilskud eller organisationer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="eaaef-121">I projekter med flere bidragydere kaldes alle de parter, der bidrager til finansieringen af et avanceret finansieringsprojekt, for finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="eaaef-122">Når en debitor, en organisation eller et tilskud er defineret som en finansieringskilde, kan den/det tildeles en eller flere finansieringsregler.</span><span class="sxs-lookup"><span data-stu-id="eaaef-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="eaaef-123">Finansieringsregler indeholder de kriterier, der afgør, hvordan gebyrer fordeles på et projekts forskellige finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="eaaef-124">Da lagerførte varer som dem, der vises i indkøbsrekvisitioner og indkøbsordrer, ikke kan opdeles, kan omkostningsbeløbet ikke fordeles mellem flere finansieringskilder på tidspunktet for fordeling.</span><span class="sxs-lookup"><span data-stu-id="eaaef-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="eaaef-125">Finansieringskildens værdi er derfor 0 (nul), indtil lagerafgangen bogføres.</span><span class="sxs-lookup"><span data-stu-id="eaaef-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="eaaef-126">Når lagerafgangen bogføres, fordeles omkostningsbeløbet i overensstemmelse med reglerne for kontofordeling på projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="eaaef-127">Her er nogle trin, du kan udføre for at gøre det lettere at opdele fakturering blandt flere finansieringskilder:</span><span class="sxs-lookup"><span data-stu-id="eaaef-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="eaaef-128">Angiv, at alle de posteringer, der angives for et projekt, skal bruge samme salgsvaluta som i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="eaaef-129">Konfigurer finansieringsgrænser, så en finansieringskilde ikke faktureres med mere end et angivet beløb på et projekt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="eaaef-130">Konfigurer finansieringsregler og finansieringsgrænser for hver arbejder, vare, kategori, kategorigruppe og posteringstype (eller for alle posteringstyper).</span><span class="sxs-lookup"><span data-stu-id="eaaef-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="eaaef-131">Vælg en valgfri start- og slutdato for at definere den periode, hvor hver finansieringsregel gælder for.</span><span class="sxs-lookup"><span data-stu-id="eaaef-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="eaaef-132">Angiv den procentdel, som hver finansieringskilde er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="eaaef-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="eaaef-133">Angiv, hvilken finansieringskilde der er ansvarlig for afrundingsdifferencer, som skyldes beregninger af finansieringsfordelinger.</span><span class="sxs-lookup"><span data-stu-id="eaaef-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="eaaef-134">Konfigurer regler, der afgør, hvordan projektomkostninger skal faktureres til eksterne debitorer og debiteres på interne organisationer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="eaaef-135">Registrer posteringer på en finansieringskonto på hold, indtil der kan opnås yderligere finansiering, eller indtil du beslutter at bære omkostningerne internt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="eaaef-136">Hvis du vil finde ud af, hvilken momsgruppe der skal knyttes til en postering, kan du søge i projektet efter en tildeling af momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eaaef-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="eaaef-137">Hvis der ikke er foretaget en tildeling af momsgruppe på projektniveau, kan du søge efter projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="eaaef-138">Eksempel: flere finansieringskilder (simpel)</span><span class="sxs-lookup"><span data-stu-id="eaaef-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="eaaef-139">Følgende tabel indeholder scenarier til administration af finansieringsfordeling mellem flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="eaaef-140">Disse scenarier er baseret på følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="eaaef-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="eaaef-141">Prioritetsindstillinger indregnes i tildelingen af midler, før andre finansieringsregelkriterier anvendes.</span><span class="sxs-lookup"><span data-stu-id="eaaef-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="eaaef-142">Der er ikke angivet et datointerval til at definere periode d, når finansieringsreglen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="eaaef-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eaaef-143"><strong>Scenarie</strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="eaaef-144"><strong>Finansieringskilde </strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="eaaef-145"><strong>Fordelingsprocent </strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="eaaef-146"><strong>Fordelingsprioritet </strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaaef-147">Du skal allokere omkostninger til én finansieringskilde, indtil dens midler er opbrugt, allokere omkostninger til en anden finansieringskilde, indtil dens midler er opbrugt, og endelig allokere de resterende omkostninger til en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-148">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="eaaef-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="eaaef-149">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="eaaef-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="eaaef-150">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="eaaef-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-151">100 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-151">100%</span></span></li>
<li><span data-ttu-id="eaaef-152">100 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-152">100%</span></span></li>
<li><span data-ttu-id="eaaef-153">100 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-154">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-154">1</span></span></li>
<li><span data-ttu-id="eaaef-155">2</span><span class="sxs-lookup"><span data-stu-id="eaaef-155">2</span></span></li>
<li><span data-ttu-id="eaaef-156">3</span><span class="sxs-lookup"><span data-stu-id="eaaef-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaaef-157">Du skal allokere 75 % af omkostningerne til én finansieringskilde og 25 % til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="eaaef-158">Når begge disse finansieringskilder er opbrugt, vil du betale de resterende omkostninger fra et tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-159">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="eaaef-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="eaaef-160">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="eaaef-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="eaaef-161">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="eaaef-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-162">75 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-162">75%</span></span></li>
<li><span data-ttu-id="eaaef-163">25 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-163">25%</span></span></li>
<li><span data-ttu-id="eaaef-164">100 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-165">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-165">1</span></span></li>
<li><span data-ttu-id="eaaef-166">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-166">1</span></span></li>
<li><span data-ttu-id="eaaef-167">2</span><span class="sxs-lookup"><span data-stu-id="eaaef-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaaef-168">Du skal allokere 75 % af omkostningerne til én finansieringskilde og 25 % til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="eaaef-169">Hvis begge disse finansieringskilder er opbrugt, skal du dele de resterende omkostninger mellem en tredje og en fjerde finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-170">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="eaaef-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="eaaef-171">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="eaaef-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="eaaef-172">Finansieringskilde 3</span><span class="sxs-lookup"><span data-stu-id="eaaef-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="eaaef-173">Finansieringskilde 4</span><span class="sxs-lookup"><span data-stu-id="eaaef-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-174">75 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-174">75%</span></span></li>
<li><span data-ttu-id="eaaef-175">25 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-175">25%</span></span></li>
<li><span data-ttu-id="eaaef-176">50 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-176">50%</span></span></li>
<li><span data-ttu-id="eaaef-177">50 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-178">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-178">1</span></span></li>
<li><span data-ttu-id="eaaef-179">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-179">1</span></span></li>
<li><span data-ttu-id="eaaef-180">2</span><span class="sxs-lookup"><span data-stu-id="eaaef-180">2</span></span></li>
<li><span data-ttu-id="eaaef-181">2</span><span class="sxs-lookup"><span data-stu-id="eaaef-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaaef-182">Du skal fordele de første 25 % af omkostningerne til én finansieringskilde og resten til en anden finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-183">Finansieringskilde 1</span><span class="sxs-lookup"><span data-stu-id="eaaef-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="eaaef-184">Finansieringskilde 2</span><span class="sxs-lookup"><span data-stu-id="eaaef-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-185">25 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-185">25%</span></span></li>
<li><span data-ttu-id="eaaef-186">100 %</span><span class="sxs-lookup"><span data-stu-id="eaaef-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaaef-187">1</span><span class="sxs-lookup"><span data-stu-id="eaaef-187">1</span></span></li>
<li><span data-ttu-id="eaaef-188">2</span><span class="sxs-lookup"><span data-stu-id="eaaef-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="eaaef-189">Eksempel: flere finansieringskilder (kompleks)</span><span class="sxs-lookup"><span data-stu-id="eaaef-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="eaaef-190">Du har tre finansieringskilder, som du vil bruge i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="eaaef-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="eaaef-191">Brug lige meget af finansieringskilde 2 og finansieringskilde 3, indtil finansieringskilde 2 er opbrugt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="eaaef-192">Fortsæt med at bruge finansieringskilde 3, indtil den er opbrugt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="eaaef-193">Brug finansieringskilde 1, efter at finansieringskilde 3 er opbrugt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="eaaef-194">For at nå dette mål skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="eaaef-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="eaaef-195">Opret finansieringsgrænser for finansieringskilde 2 og finansieringskilde 3 for deres respektive beløb.</span><span class="sxs-lookup"><span data-stu-id="eaaef-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="eaaef-196">Opret følgende finansieringsregler:</span><span class="sxs-lookup"><span data-stu-id="eaaef-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="eaaef-197">Regel 1 (prioritet 1): Fordel 50 procent af posteringer til finansieringskilde 2 og 50 procent til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="eaaef-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="eaaef-198">Regel 2 (prioritet 2): Fordel 100 procent af posteringer til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="eaaef-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="eaaef-199">Regel 3 (prioritet 3): Fordel 100 procent af posteringer til finansieringskilde 1.</span><span class="sxs-lookup"><span data-stu-id="eaaef-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="eaaef-200">Denne opsætning fungerer, fordi posteringer kontrolleres mod regler og begrænsninger for at bestemme, om nogen af dem gælder for posteringen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="eaaef-201">Hvis ingen specifikke regler eller grænser gælder for posteringen, gælder reglen Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="eaaef-202">Reglen Alle posteringer afstemmer alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="eaaef-203">Hvis der findes en regel, der passer til en postering, anvendes den procentsats, der er allokeret i denne regel, først, men først efter at forekomsterne er blevet kontrolleret mod eventuelle grænser.</span><span class="sxs-lookup"><span data-stu-id="eaaef-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="eaaef-204">Hvis en grænse er nået, og en finansieringskildes midler er opbrugt, ignoreres finansieringsreglen for finansieringsgrænsen, og programmet søger efter den næste gældende regel.</span><span class="sxs-lookup"><span data-stu-id="eaaef-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="eaaef-205">I nogle tilfælde kan kun en del af en postering tildeles under en regel.</span><span class="sxs-lookup"><span data-stu-id="eaaef-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="eaaef-206">Det kan ske, fordi en grænse nås, når posteringen allokeres.</span><span class="sxs-lookup"><span data-stu-id="eaaef-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="eaaef-207">I dette tilfælde tildeles kun et bestemt beløb i henhold til denne regel, f.eks 50 procent til hver finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="eaaef-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="eaaef-208">Dette er tilfældet i regel 1, der er beskrevet tidligere i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="eaaef-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="eaaef-209">Resten fordeles i henhold til den næste regel i rækkefølgen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="eaaef-210">I følgende tabel undersøges dette scenario yderligere.</span><span class="sxs-lookup"><span data-stu-id="eaaef-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eaaef-211"><strong>Fokusering </strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="eaaef-212"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="eaaef-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaaef-213">Finansieringsregler</span><span class="sxs-lookup"><span data-stu-id="eaaef-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-214">Regel 1 (prioritet 1): Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="eaaef-215">Alloker finansieringskilde 2 på 50 % og finansieringskilde 3 på 50 %.</span><span class="sxs-lookup"><span data-stu-id="eaaef-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="eaaef-216">Regel 2 (prioritet 2): Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="eaaef-217">Alloker finansieringskilde 3 på 100 %.</span><span class="sxs-lookup"><span data-stu-id="eaaef-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="eaaef-218">Regel 3 (prioritet 2): Alle posteringer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="eaaef-219">Alloker finansieringskilde 1 på 100 %.</span><span class="sxs-lookup"><span data-stu-id="eaaef-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaaef-220">Finansieringsloft</span><span class="sxs-lookup"><span data-stu-id="eaaef-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-221">Grænse for finansieringskilde 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="eaaef-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="eaaef-222">Grænse for finansieringskilde 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="eaaef-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="eaaef-223">Grænse for finansieringskilde 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="eaaef-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaaef-224">Postering 1</span><span class="sxs-lookup"><span data-stu-id="eaaef-224">Transaction 1</span></span></td>
<td><span data-ttu-id="eaaef-225"><strong>Posteringens beløb:</strong> 100,00<strong>Finansiering:</strong> Posteringen betales i henhold til regel 1, da posteringen er fuldt betalt efter regel 1 anvendes.</span><span class="sxs-lookup"><span data-stu-id="eaaef-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="eaaef-226">Posteringen finansieres ligeligt mellem finansieringskilde 2 og finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="eaaef-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="eaaef-227">Finansieringskilde 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="eaaef-228">Finansieringskilde 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaaef-229">Postering 2</span><span class="sxs-lookup"><span data-stu-id="eaaef-229">Transaction 2</span></span></td>
<td><span data-ttu-id="eaaef-230"><strong>Transaktionsbeløb:</strong> 5.000,00<strong>Finansiering:</strong> Transaktionen betales i henhold til alle tre regler.<strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="eaaef-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="eaaef-231">Finansieringskilde 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="eaaef-232">Finansieringskilde 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="eaaef-233">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="eaaef-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="eaaef-234">Finansieringskilde 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="eaaef-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="eaaef-235">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="eaaef-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="eaaef-236">Finansieringskilde 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="eaaef-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaaef-237">Samlede midler, der distribueres for hver finansieringskilde</span><span class="sxs-lookup"><span data-stu-id="eaaef-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="eaaef-238">Finansieringskilde 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="eaaef-239">Finansieringskilde 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="eaaef-240">Finansieringskilde 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="eaaef-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="eaaef-241">Regler for fakturering</span><span class="sxs-lookup"><span data-stu-id="eaaef-241">Billing rules</span></span>
<span data-ttu-id="eaaef-242">Når du forhandler en projektkontrakt på plads med en kunde, skal du definere, hvordan og hvornår du kan fakturere kunden for arbejde på et projekt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="eaaef-243">Når du har oprettet projektkontrakten og projektet, kan du angive regler for fakturering af projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="eaaef-244">Faktureringsregler er baseret på de projektvilkår, der er angivet i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="eaaef-245">De faktureringsregler, du kan oprette, afhænger af vilkårene i projektkontrakten og projekttypen, f.eks. tid og materialer eller fast pris, som du tilknytter til faktureringsreglen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="eaaef-246">Du kan oprette mere end én faktureringsregel for en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="eaaef-247">Du kan også tildele en faktureringsregel til flere projekter, der er tilknyttet den samme projektkontrakt og har lignende vilkår.</span><span class="sxs-lookup"><span data-stu-id="eaaef-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="eaaef-248">Du kan angive følgende typer faktureringsregler:</span><span class="sxs-lookup"><span data-stu-id="eaaef-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="eaaef-249">**Enhed for levering** – Fakturer en kunde, når du har fuldført en enhed for levering.</span><span class="sxs-lookup"><span data-stu-id="eaaef-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="eaaef-250">Du definerer de enheder, der skal leveres, i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="eaaef-251">**Status** – Fakturer en kunde, når du har fuldført en nærmere angivet procentdel af projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="eaaef-252">Du kan oprette en faktureringsregel til automatisk beregning af procentdelen af udført arbejde, eller du kan manuelt beregne procentdelen af fuldført arbejde og det beløb, der skal faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="eaaef-253">**Milepæl** – Fakturer en kunde for det fulde beløb for et projekts milepæl, når milepælen er nået.</span><span class="sxs-lookup"><span data-stu-id="eaaef-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="eaaef-254">**Gebyr** – Fakturer en kunde for dine servicer plus et administrationsgebyr, som typisk vil være en procentdel af kostprisen for servicen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="eaaef-255">**Tid og materialer** – Fakturer en kunde for værdien af den tid og de materialer, der er brugt på et projekt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="eaaef-256">For alle typer faktureringsregler gælder det, at du kan angive en tilbageholdelsesprocentdel, der trækkes fra debitorfakturaer, indtil et projekt når en aftalt fase.</span><span class="sxs-lookup"><span data-stu-id="eaaef-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="eaaef-257">Tilbageholdelsesprocenten for betalingen angives i projektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="eaaef-258">Beløbet beregnes baseret på og trækkes fra den samlede værdi af linjerne i en debitorfaktura.</span><span class="sxs-lookup"><span data-stu-id="eaaef-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="eaaef-259">For faktureringsreglerne **Tid og materialer** og **Status** kan du tildele fakturerbare kategorier.</span><span class="sxs-lookup"><span data-stu-id="eaaef-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="eaaef-260">Fakturerbare kategorier angiver de posteringer, der skal medtages i debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="eaaef-261">Når du er klar til at fakturere debitoren, beregnes det beløb, der skal faktureres for projektet, på basis af faktureringsreglerne, og der genereres et projektfakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="eaaef-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="eaaef-262">De følgende afsnit indeholder eksempler, der viser, hvordan du kan konfigurere og administrere faktureringsregler for et projekt.</span><span class="sxs-lookup"><span data-stu-id="eaaef-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="eaaef-263">Eksempel: Opret en faktureringsregel, der er baseret på det leverede antal enheder</span><span class="sxs-lookup"><span data-stu-id="eaaef-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="eaaef-264">Din organisation indgår en aftale om at levere fem træningssessioner i alt til en kundes medarbejdere til en pris af 10.000 pr. træningssession.</span><span class="sxs-lookup"><span data-stu-id="eaaef-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="eaaef-265">Du fakturerer kunden efter hver træningssession.</span><span class="sxs-lookup"><span data-stu-id="eaaef-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="eaaef-266">Når du konfigurerer faktureringsreglerne til kontrakten, skal du bruge følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="eaaef-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="eaaef-267">Leveringsenheden er én træningssession.</span><span class="sxs-lookup"><span data-stu-id="eaaef-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="eaaef-268">Enhedsprisen er 10.000 kr. pr. træningssession.</span><span class="sxs-lookup"><span data-stu-id="eaaef-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="eaaef-269">Det samlede antal enheder er fem træningssessioner.</span><span class="sxs-lookup"><span data-stu-id="eaaef-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="eaaef-270">Når du har fuldført én træningssession, kan du oprette en faktura på 10.000 for den første enhed, der blev leveret, og sende fakturaen til kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="eaaef-271">Eksempel: Opret en faktureringsregel, der er baseret på fuldførelse af en nærmere angivet procentdel af projektet (manuel beregning)</span><span class="sxs-lookup"><span data-stu-id="eaaef-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="eaaef-272">Din organisation, som tilbyder softwarerådgivning, indgår aftale med en kunde om at udvikle én del af et produkt, som kunden er ved at udvikle.</span><span class="sxs-lookup"><span data-stu-id="eaaef-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="eaaef-273">Din organisation indgår aftale med kunden om at levere softwarekoden over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="eaaef-274">Kunden indvilliger i at betale din organisation i alt 100.000 kr. for arbejdet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="eaaef-275">Du opretter en faktureringsregel for at fakturere kunden på baggrund af den procentdel af arbejdet, der er udført for projektet, som angivet i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="eaaef-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="eaaef-276">Ved udgangen af den første måned mødes du med kunden for at fastslå, hvor stor en procentdel af arbejdet der er fuldført.</span><span class="sxs-lookup"><span data-stu-id="eaaef-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="eaaef-277">Når du og kunden har gennemgået projektet, beslutter I, at 15 procent af projektet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="eaaef-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="eaaef-278">Du opretter en faktura på 15.000 (15 procent af 100.000) og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="eaaef-279">Eksempel: Opret en faktureringsregel, der er baseret på fuldførelse af en nærmere angivet procentdel af projektet (automatisk beregning)</span><span class="sxs-lookup"><span data-stu-id="eaaef-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="eaaef-280">Organisationen, en softwareudviklingsvirksomhed, indvilliger i at udvikle en pakkeløsning med et system til lønningsregnskab for en kunde for 30.000.</span><span class="sxs-lookup"><span data-stu-id="eaaef-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="eaaef-281">Kunden indvilliger i at betale din organisation på basis af den procentdel af arbejdet, der er fuldført.</span><span class="sxs-lookup"><span data-stu-id="eaaef-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="eaaef-282">Du anslår, at projektomkostningerne beløber sig til 20.000 kr.</span><span class="sxs-lookup"><span data-stu-id="eaaef-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="eaaef-283">Projektkontrakten specificerer de arbejdskategorier, som du skal bruge i forbindelse med faktureringen.</span><span class="sxs-lookup"><span data-stu-id="eaaef-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="eaaef-284">Du opretter regler for fakturering, så fakturabeløbene beregnes automatisk, og så kunden faktureres for den procentdel af arbejdet, der er fuldført inden for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="eaaef-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="eaaef-285">Du opretter et budget for hver enkelt kategori:</span><span class="sxs-lookup"><span data-stu-id="eaaef-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="eaaef-286">**Udvikling** – omkostninger på 15.000 og indtægter på 20.000</span><span class="sxs-lookup"><span data-stu-id="eaaef-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="eaaef-287">**Installation** – omkostninger på 5.000 og indtægter på 10.000</span><span class="sxs-lookup"><span data-stu-id="eaaef-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="eaaef-288">Første gang du opretter en debitorfaktura, beregnes fakturabeløbet automatisk ud fra følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="eaaef-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="eaaef-289">Efter en måned sender arbejderen på projektet en timeseddel for projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="eaaef-290">Omkostningerne til arbejderens timer er 5.000 kr. for udvikling og 1.000 kr. for installation.</span><span class="sxs-lookup"><span data-stu-id="eaaef-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="eaaef-291">Udviklingsarbejdet er 33 procent fuldført (5.000 faktiske omkostninger/15.000 budgetomkostninger), og installationsarbejdet er 20 procent fuldført (1.000 faktiske omkostninger/5.000 budgetomkostninger).</span><span class="sxs-lookup"><span data-stu-id="eaaef-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="eaaef-292">Fakturabeløbet på 8.667 beregnes automatisk (33 procent af 20.000 plus 20 procent af 10.000).</span><span class="sxs-lookup"><span data-stu-id="eaaef-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="eaaef-293">Du opretter en faktura på 8.667 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="eaaef-294">Eksempel: Opret en faktureringsregel, der er baseret på nærmere aftalte milepæle</span><span class="sxs-lookup"><span data-stu-id="eaaef-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="eaaef-295">Din organisation tilbyder ledelsesrådgivning, accepterer at gennemføre markedsundersøgelser for et forbrugerprodukt, som kunden har til hensigt at sælge.</span><span class="sxs-lookup"><span data-stu-id="eaaef-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="eaaef-296">Kunden indvilliger i at bruge dig i en periode på tre måneder fra og med marts og at betale din organisation 50.000 kr.</span><span class="sxs-lookup"><span data-stu-id="eaaef-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="eaaef-297">Der er tre milepæle i projektet:</span><span class="sxs-lookup"><span data-stu-id="eaaef-297">The project has three milestones:</span></span>

-   <span data-ttu-id="eaaef-298">Milepæl 1: Indsamling af forbrugerdata – 31. marts</span><span class="sxs-lookup"><span data-stu-id="eaaef-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="eaaef-299">Milepæl 2: Analyse af forbrugerdata – 30. april</span><span class="sxs-lookup"><span data-stu-id="eaaef-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="eaaef-300">Milepæl 3: Fremlæggelse af rapport om produktets levedygtighed - 31. maj</span><span class="sxs-lookup"><span data-stu-id="eaaef-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="eaaef-301">Kunden indvilliger i at betale din organisation 10.000 for den første milepæl og 20.000 for såvel den anden som den tredje milepæl.</span><span class="sxs-lookup"><span data-stu-id="eaaef-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="eaaef-302">Under udarbejdelsen af projektkontrakten aftales det, at kunden faktureres på basis af den milepæl, der er nået.</span><span class="sxs-lookup"><span data-stu-id="eaaef-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="eaaef-303">Opsætningen af faktureringsreglen omfatter følgende trin:</span><span class="sxs-lookup"><span data-stu-id="eaaef-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="eaaef-304">Angiv milepælene i projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-304">Define the project milestones.</span></span>
-   <span data-ttu-id="eaaef-305">Definer det beløb, der skal faktureres kunden, når hver milepæl er nået.</span><span class="sxs-lookup"><span data-stu-id="eaaef-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="eaaef-306">Når den første milepæl er nået d. 31. marts, skal du markere milepælen som fuldført og derefter oprette en faktura på 10.000 og sende den til kunden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="eaaef-307">Du kan ikke oprette en faktura for en milepæl, indtil du har markeret milepælen som fuldført.</span><span class="sxs-lookup"><span data-stu-id="eaaef-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="eaaef-308">Eksempel: Opret en faktureringsregel, der er baseret på tjenester plus et administrativt gebyr</span><span class="sxs-lookup"><span data-stu-id="eaaef-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="eaaef-309">Din organisation, et ledelsesrådgivningsfirma, accepterer at gennemføre markedsundersøgelser for at vurdere, om et produkt, som kunden, en detailvirksomhed, udvikler, vil kunne overleve på markedet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="eaaef-310">Aftalens vilkår angiver, at du stiller dit firmas tre bedste ledelseskonsulenter til rådighed. Deres opgave er at udføre undersøgelserne baseret på tids- og materialeforbrug.</span><span class="sxs-lookup"><span data-stu-id="eaaef-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="eaaef-311">Kunden indvilliger i at betale 1000 pr. time for konsulenterne plus et ekstra administrationsgebyr på 10 procent for de konsulenttimer, der debiteres på projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="eaaef-312">Når du opretter projektkontrakten, skal du oprette en faktureringsregel, der fastslår, at der skal lægges et administrationsgebyr på 10 procent til de konsulenttimer, der debiteres på projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="eaaef-313">Når du opretter en faktura til kunden, faktureres kunden et administrativt gebyr på 10 procent plus prisen for konsulenttimerne.</span><span class="sxs-lookup"><span data-stu-id="eaaef-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="eaaef-314">Hvis de tre konsulenter f.eks. i alt arbejder 200 timer på projektet, oprettes der en faktura på 220.000 baseret på følgende beregning:</span><span class="sxs-lookup"><span data-stu-id="eaaef-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="eaaef-315">200 timer til 1000 kr. pr. time = 200.000 kr.</span><span class="sxs-lookup"><span data-stu-id="eaaef-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="eaaef-316">10 procent management gebyr = 20.000</span><span class="sxs-lookup"><span data-stu-id="eaaef-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="eaaef-317">Samlet fakturabeløb = 220.000</span><span class="sxs-lookup"><span data-stu-id="eaaef-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="eaaef-318">Hvis gebyrer er afgiftspligtige for en debitor, og du vælger en salgsmomsgruppe i projektkontrakten, angives salgsmomsgruppen automatisk i en faktureringsregel for gebyrer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="eaaef-319">Eksempel: Opret en faktureringsregel for tids- og materialeomkostninger</span><span class="sxs-lookup"><span data-stu-id="eaaef-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="eaaef-320">Din organisation, et softwarekonsulentfirma, aftaler at stille fem tekniske konsulenter til rådighed, som i løbet af de næste seks måneder skal arbejde med et projekt for en kunde om udvikling af computerprogrammer.</span><span class="sxs-lookup"><span data-stu-id="eaaef-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="eaaef-321">Kunden indvilliger i at betale 1.500 kr. for hver konsulenttime plus udgifterne til kontorartikler.</span><span class="sxs-lookup"><span data-stu-id="eaaef-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="eaaef-322">Din organisation sender en faktura til kunden ved udgangen af hver måned.</span><span class="sxs-lookup"><span data-stu-id="eaaef-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="eaaef-323">Når du konfigurerer projektkontrakten, accepterer du at fakturere kunden hver måned for tid og materialer på projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="eaaef-324">Du kan oprette en faktureringsregel, der indeholder følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="eaaef-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="eaaef-325">Kontraktens periode er seks måneder.</span><span class="sxs-lookup"><span data-stu-id="eaaef-325">The contract period is six months.</span></span>
-   <span data-ttu-id="eaaef-326">Konsulenttiden beregnes efter en sats på 1.500 kr. pr. time.</span><span class="sxs-lookup"><span data-stu-id="eaaef-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="eaaef-327">Kontorartikler faktureres med kostprisen, og de samlede omkostninger må ikke overstige 100.000 kr. for projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="eaaef-328">Du opretter en debitorfaktura ved udgangen af hver kalendermåned under projektperioden.</span><span class="sxs-lookup"><span data-stu-id="eaaef-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="eaaef-329">I løbet af den første måned registrerer konsulenterne 800 timer i alt på projektet.</span><span class="sxs-lookup"><span data-stu-id="eaaef-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="eaaef-330">Udgifterne for kontorartikler i forbindelse med projektet er 20.000 kr.</span><span class="sxs-lookup"><span data-stu-id="eaaef-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="eaaef-331">I slutningen af måneden skal du derfor oprette en faktura på 1.220.000, som beregnes som 800 timer ved 1500 i timen plus 20.000 til kontorartikler.</span><span class="sxs-lookup"><span data-stu-id="eaaef-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




