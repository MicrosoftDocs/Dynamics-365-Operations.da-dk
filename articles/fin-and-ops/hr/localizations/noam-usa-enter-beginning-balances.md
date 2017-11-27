---
title: "Angive primosaldi for løn"
description: "Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms. Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceaf56573c99bb257aed127af5e15ee2a7a961a5
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="cf4fd-104">Angive primosaldi for løn</span><span class="sxs-lookup"><span data-stu-id="cf4fd-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="cf4fd-105">Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="cf4fd-106">Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="cf4fd-107">Som indledning til at angive primolønsaldi skal vi kontrollere følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="cf4fd-108">Medarbejderregistreringer er angivet og er tilgængelige i systemet</span><span class="sxs-lookup"><span data-stu-id="cf4fd-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="cf4fd-109">Følgende data er konfigureret og tildelt til medarbejdere:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="cf4fd-110">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="cf4fd-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="cf4fd-111">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="cf4fd-111">Earning codes</span></span>
> > * <span data-ttu-id="cf4fd-112">Moms</span><span class="sxs-lookup"><span data-stu-id="cf4fd-112">Taxes</span></span>
> > * <span data-ttu-id="cf4fd-113">Frynsegoder og fradrag</span><span class="sxs-lookup"><span data-stu-id="cf4fd-113">Benefits and deductions</span></span>

> * <span data-ttu-id="cf4fd-114">Virksomheden skal have valgt en dato, som skal gælde for angivelse af primosaldi for løn.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="cf4fd-115">Der er indsamlet oplysninger om alle indtægter, frynsegoder/fradrag, frynsegodebidrag, medarbejderskat, selskabsskat og deres år til dato-beløb fra det gamle system.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="cf4fd-116">Når du skal angive primosaldi, skal du overveje, hvor detaljerede dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="cf4fd-117">De fleste virksomheder angive et enkelt, konsolideret år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="cf4fd-118">Hvis der kræves mere detaljerede oplysninger, kan saldi dog angives kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="cf4fd-119">Angivelse af det detaljeringsniveau, der er nødvendigt, bestemmer også, hvor mange manuelle betalingsopgørelser der skal oprettes for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="cf4fd-120">Der er kun brug for én manuel opgørelse for hver medarbejder for et enkelt år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="cf4fd-121">Brug år-til-dato-beløb fra den endelige betalingsopgørelse fra det tidligere system som det beløb, der skal angives i det nye lønsystem, for at bruge dette.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="cf4fd-122">Følgende eksempel viser, hvordan du kan angive medarbejderens primolønsaldi, herunder lønkoder, frynsegoder/fradrag og skat.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="cf4fd-123">I et eksempel fra den virkelige verden har du et linjeelement for hver lønkode, hvert frynsegodefradrag, frynsegodebidrag, medarbejderskat og selskabsskat, hvor det angivne beløb er år-til-dato-beløbet.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="cf4fd-124">Brug listen over koder og beløb, og følg trinene for at oprette en manuel løn- og betalingsopgørelse. Deaktiver regnskab for at overføre primosaldi i forbindelse med lønbehandling.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="cf4fd-125">Du skal deaktivere regnskab, fordi du ikke vil bogføre primosaldoen for denne betalingsopgørelse til finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="cf4fd-126">Det blev foretaget i det oprindelige system og overføres til det nye system, når du definerer startsaldi i Finans.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="cf4fd-127">A.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-127">A.</span></span> <span data-ttu-id="cf4fd-128">Sådan konfigurerer du lønkoder, der skal bruges på primolønsaldi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="cf4fd-129">Når du angiver primosaldi for løn, skal du kontrollere, at de lønkoder, du vil bruge, er konfigureret, så indstillingen "Tillad redigering af satser på lønopgørelsen" er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="cf4fd-130">På denne måde kan du manuelt indtaste beløbet fra det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="cf4fd-131">B.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-131">B.</span></span> <span data-ttu-id="cf4fd-132">Oprette lønopgørelse for en medarbejder med en primosaldo</span><span class="sxs-lookup"><span data-stu-id="cf4fd-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="cf4fd-133">Dette trin opretter manuelt en lønopgørelse for hver arbejder for den sidste lønperiode af oprindelige system, som opretter lønopgørelseslinjerne i nye lønsystem.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="cf4fd-134">Angiv én linje pr. lønkode og år til dato-beløb og timer.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="cf4fd-135">Der er følgende trin i eksemplet:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="cf4fd-136">Åbn siden **Alle lønopgørelser**, og klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="cf4fd-137">Angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-137">Enter the following:</span></span> 

| <span data-ttu-id="cf4fd-138">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-138">Field</span></span>      | <span data-ttu-id="cf4fd-139">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="cf4fd-140">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="cf4fd-140">Worker</span></span>     | <span data-ttu-id="cf4fd-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="cf4fd-141">Michael Redmond</span></span>       |
| <span data-ttu-id="cf4fd-142">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="cf4fd-142">Pay cycle</span></span>  | <span data-ttu-id="cf4fd-143">sm</span><span class="sxs-lookup"><span data-stu-id="cf4fd-143">sm</span></span>                    |
| <span data-ttu-id="cf4fd-144">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-144">Pay period</span></span> | <span data-ttu-id="cf4fd-145">16-06-2017 - 30-06-2017</span><span class="sxs-lookup"><span data-stu-id="cf4fd-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="cf4fd-146">Under fanen **Post på lønopgørelse** skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="cf4fd-147">Linje 1: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="cf4fd-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="cf4fd-148">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-148">Field</span></span>            | <span data-ttu-id="cf4fd-149">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="cf4fd-150">Lønkode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-150">Earnings code</span></span>    | <span data-ttu-id="cf4fd-151">Fast løn</span><span class="sxs-lookup"><span data-stu-id="cf4fd-151">Regular pay</span></span> |
| <span data-ttu-id="cf4fd-152">Mængde</span><span class="sxs-lookup"><span data-stu-id="cf4fd-152">Quantity</span></span>         | <span data-ttu-id="cf4fd-153">1,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-153">1.00</span></span>        |
| <span data-ttu-id="cf4fd-154">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="cf4fd-154">Rage</span></span>             | <span data-ttu-id="cf4fd-155">30.000</span><span class="sxs-lookup"><span data-stu-id="cf4fd-155">30,000</span></span>      |
| <span data-ttu-id="cf4fd-156">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="cf4fd-156">Line details tab</span></span> |             |
| <span data-ttu-id="cf4fd-157">Manuelt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-157">Manual</span></span>           | <span data-ttu-id="cf4fd-158">(markeret)</span><span class="sxs-lookup"><span data-stu-id="cf4fd-158">(marked)</span></span>    |

<span data-ttu-id="cf4fd-159">Linje 2: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="cf4fd-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="cf4fd-160">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-160">Field</span></span>            | <span data-ttu-id="cf4fd-161">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="cf4fd-162">Lønkode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-162">Earnings code</span></span>    | <span data-ttu-id="cf4fd-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="cf4fd-163">Bonus</span></span>    |
| <span data-ttu-id="cf4fd-164">Mængde</span><span class="sxs-lookup"><span data-stu-id="cf4fd-164">Quantity</span></span>         | <span data-ttu-id="cf4fd-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="cf4fd-165">1.0000</span></span>   |
| <span data-ttu-id="cf4fd-166">Kurs</span><span class="sxs-lookup"><span data-stu-id="cf4fd-166">Rate</span></span>             | <span data-ttu-id="cf4fd-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-167">4250.00</span></span>  |
| <span data-ttu-id="cf4fd-168">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="cf4fd-168">Line details tab</span></span> |          |
| <span data-ttu-id="cf4fd-169">Manuelt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-169">Manual</span></span>           | <span data-ttu-id="cf4fd-170">(markeret)</span><span class="sxs-lookup"><span data-stu-id="cf4fd-170">(marked)</span></span> |

<span data-ttu-id="cf4fd-171">Linje 3: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="cf4fd-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="cf4fd-172">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-172">Field</span></span>           | <span data-ttu-id="cf4fd-173">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="cf4fd-174">Lønkode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-174">Earnings code</span></span>   | <span data-ttu-id="cf4fd-175">Provision i standardvaluta</span><span class="sxs-lookup"><span data-stu-id="cf4fd-175">Commission</span></span> |
| <span data-ttu-id="cf4fd-176">Mængde</span><span class="sxs-lookup"><span data-stu-id="cf4fd-176">Quantity</span></span>        | <span data-ttu-id="cf4fd-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="cf4fd-177">1.0000</span></span>     |
| <span data-ttu-id="cf4fd-178">Kurs</span><span class="sxs-lookup"><span data-stu-id="cf4fd-178">Rate</span></span>            | <span data-ttu-id="cf4fd-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-179">!,299.00</span></span>   |
| <span data-ttu-id="cf4fd-180">Kurs</span><span class="sxs-lookup"><span data-stu-id="cf4fd-180">Rate</span></span>            | <span data-ttu-id="cf4fd-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-181">1,299.00</span></span>   |
| <span data-ttu-id="cf4fd-182">Fanen Linjedetalje</span><span class="sxs-lookup"><span data-stu-id="cf4fd-182">Line detail tab</span></span> |            |
| <span data-ttu-id="cf4fd-183">Manuelt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-183">Manual</span></span>          | <span data-ttu-id="cf4fd-184">(markeret)</span><span class="sxs-lookup"><span data-stu-id="cf4fd-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="cf4fd-185">Det er vigtigt, at indstille skyderen **Manuel** til **Ja** under fanen **Linjedetaljer** for hver lønopgørelseslinje, når der skal angives primolønsaldi for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="cf4fd-186">I ruden **Handling** skal du klikke på **Frigiv lønopgørelse** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="cf4fd-187">Klik i ruden **Handling** på **Betalingsopgørelse** for at åbne siden **Generér betalingsopgørelser**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="cf4fd-188">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-188">Field</span></span>              | <span data-ttu-id="cf4fd-189">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="cf4fd-190">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="cf4fd-190">Payment date</span></span>       | <span data-ttu-id="cf4fd-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="cf4fd-191">6/30/2017</span></span> |
| <span data-ttu-id="cf4fd-192">Betalingskørselstype</span><span class="sxs-lookup"><span data-stu-id="cf4fd-192">Payment run type</span></span>   | <span data-ttu-id="cf4fd-193">Manuelt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-193">Manual</span></span>    |
| <span data-ttu-id="cf4fd-194">Deaktiver regnskab</span><span class="sxs-lookup"><span data-stu-id="cf4fd-194">Disable accounting</span></span> |   <span data-ttu-id="cf4fd-195">Ja</span><span class="sxs-lookup"><span data-stu-id="cf4fd-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="cf4fd-196">Dette er kun tilgængeligt, når betalingskørselstypen er manuel, og når brugeren vil deaktivere regnskab for lønkørslen.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="cf4fd-197">Klik på **OK**, og luk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="cf4fd-198">Hvorfor skal skyderen Deaktiver regnskab være indstillet til Ja, når der genereres betalingsopgørelser?</span><span class="sxs-lookup"><span data-stu-id="cf4fd-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="cf4fd-199">Indstilling af skyderen til **Ja** forhindrer, at linjer i betalingsopgørelsen fordeles til Finans.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="cf4fd-200">Finansbeløb blev opdateret tidligere, da kontosaldi fra det oprindelige system blev angivet.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="cf4fd-201">Når du angiver primosaldi for løn, kan du generere rapporter, der indeholder oplysninger fra tidligere år, samt til at identificere grænser med tanke på frynsegoder og til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="cf4fd-202">C.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-202">C.</span></span> <span data-ttu-id="cf4fd-203">Oprette betalingsopgørelser for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="cf4fd-203">Create pay statements for employees</span></span>
<span data-ttu-id="cf4fd-204">Når du har oprettet betalingsopgørelser, der har primosaldi, skal du kontrollere, at opgørelserne præcist afspejler lønoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="cf4fd-205">Du skal også manuelt opdatere oplysningerne om frynsegoder og skat, så de svarer til værdierne i det oprindelige lønsystem.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="cf4fd-206">Når du har kontrolleret, at beløbene fra oprindelige lønsystem svarer til beløbene på de aktuelle betalingsopgørelser, skal du færdiggøre betalingsopgørelserne.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="cf4fd-207">Åbn siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="cf4fd-208">Fremhæve den sidst genererede betalingsopgørelse for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="cf4fd-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="cf4fd-209">Klik på **Rediger** for at åbne siden **Betalingsopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="cf4fd-210">Åbn fanen **Frynsegodefradrag**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="cf4fd-211">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-211">Field</span></span>                           | <span data-ttu-id="cf4fd-212">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="cf4fd-213">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-213">Benefit</span></span>                         | <span data-ttu-id="cf4fd-214">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="cf4fd-214">Deduction amount</span></span> |
| <span data-ttu-id="cf4fd-215">401K</span><span class="sxs-lookup"><span data-stu-id="cf4fd-215">401K</span></span> | <span data-ttu-id="cf4fd-216">Deltag</span><span class="sxs-lookup"><span data-stu-id="cf4fd-216">Participate</span></span>              | <span data-ttu-id="cf4fd-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-217">3000.00</span></span>          |
| <span data-ttu-id="cf4fd-218">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="cf4fd-218">Dental</span></span> | <span data-ttu-id="cf4fd-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="cf4fd-219">SubSp</span></span>                  | <span data-ttu-id="cf4fd-220">495,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-220">495.00</span></span>           |
| <span data-ttu-id="cf4fd-221">Beløb til sikring af afhængige</span><span class="sxs-lookup"><span data-stu-id="cf4fd-221">Dep care spending</span></span> | <span data-ttu-id="cf4fd-222">Deltag</span><span class="sxs-lookup"><span data-stu-id="cf4fd-222">Participate</span></span> | <span data-ttu-id="cf4fd-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-223">2500.00</span></span>          |
| <span data-ttu-id="cf4fd-224">Vision</span><span class="sxs-lookup"><span data-stu-id="cf4fd-224">Vision</span></span> | <span data-ttu-id="cf4fd-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="cf4fd-225">SupSp</span></span>                  | <span data-ttu-id="cf4fd-226">500,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-226">500.00</span></span>           |

5. <span data-ttu-id="cf4fd-227">Angiv følgende under fanen **Frynsegodebidrag**:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="cf4fd-228">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-228">Field</span></span>              | <span data-ttu-id="cf4fd-229">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="cf4fd-230">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-230">Benefit</span></span>            | <span data-ttu-id="cf4fd-231">Bidragsbeløb</span><span class="sxs-lookup"><span data-stu-id="cf4fd-231">Contribution amount</span></span> |
| <span data-ttu-id="cf4fd-232">401K</span><span class="sxs-lookup"><span data-stu-id="cf4fd-232">401K</span></span> | <span data-ttu-id="cf4fd-233">Deltag</span><span class="sxs-lookup"><span data-stu-id="cf4fd-233">Participate</span></span> | <span data-ttu-id="cf4fd-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-234">3000,00</span></span>             |
| <span data-ttu-id="cf4fd-235">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="cf4fd-235">Dental</span></span> | <span data-ttu-id="cf4fd-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="cf4fd-236">SubSp</span></span>     | <span data-ttu-id="cf4fd-237">495,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-237">495.00</span></span>              |
| <span data-ttu-id="cf4fd-238">Vision</span><span class="sxs-lookup"><span data-stu-id="cf4fd-238">Vision</span></span> | <span data-ttu-id="cf4fd-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="cf4fd-239">SubSp</span></span>     | <span data-ttu-id="cf4fd-240">500,00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-240">500.00</span></span>              |

6. <span data-ttu-id="cf4fd-241">Angiv følgende under fanen **Skattefradrag**:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="cf4fd-242">Felt</span><span class="sxs-lookup"><span data-stu-id="cf4fd-242">Field</span></span>           | <span data-ttu-id="cf4fd-243">Værdi</span><span class="sxs-lookup"><span data-stu-id="cf4fd-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="cf4fd-244">Momskode</span><span class="sxs-lookup"><span data-stu-id="cf4fd-244">Tax code</span></span>        | <span data-ttu-id="cf4fd-245">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="cf4fd-245">Deduction amount</span></span> |
| <span data-ttu-id="cf4fd-246">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="cf4fd-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="cf4fd-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="cf4fd-247">1600.00</span></span>          |
| <span data-ttu-id="cf4fd-248">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="cf4fd-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="cf4fd-249">825.75</span><span class="sxs-lookup"><span data-stu-id="cf4fd-249">825.75</span></span>           |

7. <span data-ttu-id="cf4fd-250">Angiv følgende under fanen **Skattebidrag**:</span><span class="sxs-lookup"><span data-stu-id="cf4fd-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="cf4fd-251">Klik på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="cf4fd-252">Kontroller, at de samlede beløb på betalingsopgørelsen svarer til år til dato i det oprindelige system for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="cf4fd-253">Du kan eventuelt vente med afslutningen i næste trin for at foretage en overordnet validering af alle samlede betalingsopgørelser.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="cf4fd-254">Efter valideringen skal du gennemse alle betalingsopgørelser og færdiggøre dem.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="cf4fd-255">Den samme proces kan evt. udføres kvartalsvis for alle tidligere kvartaler i året.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="cf4fd-256">Dette er kun nødvendigt, hvis kunden har brug at se dataene pr. kvartal uden at skulle gå tilbage til det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="cf4fd-257">Hvis du laver en fejl under angivelse af primosaldi for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="cf4fd-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="cf4fd-258">Det er muligt at tilbageføre posteringer og angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="cf4fd-259">Hvis du vil tilbageføre posteringen, skal du blot udføre følgende trin på siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="cf4fd-260">Klik på **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="cf4fd-261">Klik på **Ja**, når meddelelsen "Når du tilbagefører denne betalingsopgørelse, oprettes en tilbageførselsbetalingsopgørelse til modregning af betalingsopgørelsen.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="cf4fd-262">Ingen af betalingsopgørelserne kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="cf4fd-263">Vil du tilbageføre denne betalingsopgørelse?"</span><span class="sxs-lookup"><span data-stu-id="cf4fd-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="cf4fd-264">vises.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-264">displays.</span></span> 

<span data-ttu-id="cf4fd-265">Når du tilbagefører betalingsopgørelsen, kan du generere en ny betalingsopgørelse for arbejderen ud fra den lønopgørelse, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="cf4fd-266">Sørg for at rette forkerte linjer på lønopgørelsen, før du genererer den nye betalingsopgørelse, og derefter genererer nye betalingsopgørelser med de korrekte beløb.</span><span class="sxs-lookup"><span data-stu-id="cf4fd-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

