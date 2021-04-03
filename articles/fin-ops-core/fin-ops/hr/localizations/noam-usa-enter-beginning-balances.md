---
title: Angive primosaldi for løn
description: Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms. Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209636d6416a784d298bcfb134f5486c1f5cf202
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568539"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="d28ea-104">Angive primosaldi for løn</span><span class="sxs-lookup"><span data-stu-id="d28ea-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d28ea-105">Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms.</span><span class="sxs-lookup"><span data-stu-id="d28ea-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="d28ea-106">Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system.</span><span class="sxs-lookup"><span data-stu-id="d28ea-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="d28ea-107">Som indledning til at angive primolønsaldi skal vi kontrollere følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="d28ea-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="d28ea-108">Medarbejderregistreringer er angivet og er tilgængelige i systemet</span><span class="sxs-lookup"><span data-stu-id="d28ea-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="d28ea-109">Følgende data er konfigureret og tildelt til medarbejdere:</span><span class="sxs-lookup"><span data-stu-id="d28ea-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="d28ea-110">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="d28ea-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="d28ea-111">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="d28ea-111">Earning codes</span></span>
    - <span data-ttu-id="d28ea-112">Moms</span><span class="sxs-lookup"><span data-stu-id="d28ea-112">Taxes</span></span>
    - <span data-ttu-id="d28ea-113">Frynsegoder og fradrag</span><span class="sxs-lookup"><span data-stu-id="d28ea-113">Benefits and deductions</span></span>

- <span data-ttu-id="d28ea-114">Virksomheden skal have valgt en dato, som skal gælde for angivelse af primosaldi for løn.</span><span class="sxs-lookup"><span data-stu-id="d28ea-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="d28ea-115">Der er indsamlet oplysninger om alle indtægter, frynsegoder/fradrag, frynsegodebidrag, medarbejderskat, selskabsskat og deres år til dato-beløb fra det gamle system.</span><span class="sxs-lookup"><span data-stu-id="d28ea-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="d28ea-116">Når du skal angive primosaldi, skal du overveje, hvor detaljerede dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="d28ea-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="d28ea-117">De fleste virksomheder angive et enkelt, konsolideret år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="d28ea-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="d28ea-118">Hvis der kræves mere detaljerede oplysninger, kan saldi dog angives kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="d28ea-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="d28ea-119">Angivelse af det detaljeringsniveau, der er nødvendigt, bestemmer også, hvor mange manuelle betalingsopgørelser der skal oprettes for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="d28ea-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="d28ea-120">Der er kun brug for én manuel opgørelse for hver medarbejder for et enkelt år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="d28ea-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="d28ea-121">Brug år-til-dato-beløb fra den endelige betalingsopgørelse fra det tidligere system som det beløb, der skal angives i det nye lønsystem, for at bruge dette.</span><span class="sxs-lookup"><span data-stu-id="d28ea-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="d28ea-122">Følgende eksempel viser, hvordan du kan angive medarbejderens primolønsaldi, herunder lønkoder, frynsegoder/fradrag og skat.</span><span class="sxs-lookup"><span data-stu-id="d28ea-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="d28ea-123">I et eksempel fra den virkelige verden har du et linjeelement for hver lønkode, hvert frynsegodefradrag, frynsegodebidrag, medarbejderskat og selskabsskat, hvor det angivne beløb er år-til-dato-beløbet.</span><span class="sxs-lookup"><span data-stu-id="d28ea-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="d28ea-124">Brug listen over koder og beløb, og følg trinene for at oprette en manuel løn- og betalingsopgørelse. Deaktiver regnskab for at overføre primosaldi i forbindelse med lønbehandling.</span><span class="sxs-lookup"><span data-stu-id="d28ea-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="d28ea-125">Du skal deaktivere regnskab, fordi du ikke vil bogføre primosaldoen for denne betalingsopgørelse til finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="d28ea-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="d28ea-126">Det blev foretaget i det oprindelige system og overføres til det nye system, når du definerer startsaldi i Finans.</span><span class="sxs-lookup"><span data-stu-id="d28ea-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="d28ea-127">A.</span><span class="sxs-lookup"><span data-stu-id="d28ea-127">A.</span></span> <span data-ttu-id="d28ea-128">Sådan konfigurerer du lønkoder, der skal bruges på primolønsaldi</span><span class="sxs-lookup"><span data-stu-id="d28ea-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="d28ea-129">Når du angiver primosaldi for løn, skal du kontrollere, at de lønkoder, du vil bruge, er konfigureret, så indstillingen "Tillad redigering af satser på lønopgørelsen" er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d28ea-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="d28ea-130">På denne måde kan du manuelt indtaste beløbet fra det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="d28ea-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="d28ea-131">B.</span><span class="sxs-lookup"><span data-stu-id="d28ea-131">B.</span></span> <span data-ttu-id="d28ea-132">Oprette lønopgørelse for en medarbejder med en primosaldo</span><span class="sxs-lookup"><span data-stu-id="d28ea-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="d28ea-133">Dette trin opretter manuelt en lønopgørelse for hver arbejder for den sidste lønperiode af oprindelige system, som opretter lønopgørelseslinjerne i nye lønsystem.</span><span class="sxs-lookup"><span data-stu-id="d28ea-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="d28ea-134">Angiv én linje pr. lønkode og år til dato-beløb og timer.</span><span class="sxs-lookup"><span data-stu-id="d28ea-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="d28ea-135">Der er følgende trin i eksemplet:</span><span class="sxs-lookup"><span data-stu-id="d28ea-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="d28ea-136">Åbn siden **Alle lønopgørelser**, og klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="d28ea-137">Angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="d28ea-137">Enter the following:</span></span> 

    | <span data-ttu-id="d28ea-138">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-138">Field</span></span>      | <span data-ttu-id="d28ea-139">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="d28ea-140">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="d28ea-140">Worker</span></span>     | <span data-ttu-id="d28ea-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d28ea-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="d28ea-142">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="d28ea-142">Pay cycle</span></span>  | <span data-ttu-id="d28ea-143">sm</span><span class="sxs-lookup"><span data-stu-id="d28ea-143">sm</span></span>                    |
    | <span data-ttu-id="d28ea-144">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="d28ea-144">Pay period</span></span> | <span data-ttu-id="d28ea-145">16-06-2017 - 30-06-2017</span><span class="sxs-lookup"><span data-stu-id="d28ea-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="d28ea-146">Under fanen **Post på lønopgørelse** skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="d28ea-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="d28ea-147">Linje 1: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="d28ea-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d28ea-148">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-148">Field</span></span>            | <span data-ttu-id="d28ea-149">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="d28ea-150">Lønkode</span><span class="sxs-lookup"><span data-stu-id="d28ea-150">Earnings code</span></span>    | <span data-ttu-id="d28ea-151">Fast løn</span><span class="sxs-lookup"><span data-stu-id="d28ea-151">Regular pay</span></span> |
    | <span data-ttu-id="d28ea-152">Mængde</span><span class="sxs-lookup"><span data-stu-id="d28ea-152">Quantity</span></span>         | <span data-ttu-id="d28ea-153">1.00</span><span class="sxs-lookup"><span data-stu-id="d28ea-153">1.00</span></span>        |
    | <span data-ttu-id="d28ea-154">Kurs</span><span class="sxs-lookup"><span data-stu-id="d28ea-154">Rate</span></span>             | <span data-ttu-id="d28ea-155">30,000</span><span class="sxs-lookup"><span data-stu-id="d28ea-155">30,000</span></span>      |
    | <span data-ttu-id="d28ea-156">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="d28ea-156">Line details tab</span></span> |             |
    | <span data-ttu-id="d28ea-157">Manuelt</span><span class="sxs-lookup"><span data-stu-id="d28ea-157">Manual</span></span>           | <span data-ttu-id="d28ea-158">(markeret)</span><span class="sxs-lookup"><span data-stu-id="d28ea-158">(marked)</span></span>    |

    <span data-ttu-id="d28ea-159">Linje 2: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="d28ea-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d28ea-160">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-160">Field</span></span>            | <span data-ttu-id="d28ea-161">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="d28ea-162">Lønkode</span><span class="sxs-lookup"><span data-stu-id="d28ea-162">Earnings code</span></span>    | <span data-ttu-id="d28ea-163">Bonus</span><span class="sxs-lookup"><span data-stu-id="d28ea-163">Bonus</span></span>    |
    | <span data-ttu-id="d28ea-164">Mængde</span><span class="sxs-lookup"><span data-stu-id="d28ea-164">Quantity</span></span>         | <span data-ttu-id="d28ea-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="d28ea-165">1.0000</span></span>   |
    | <span data-ttu-id="d28ea-166">Kurs</span><span class="sxs-lookup"><span data-stu-id="d28ea-166">Rate</span></span>             | <span data-ttu-id="d28ea-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="d28ea-167">4250.00</span></span>  |
    | <span data-ttu-id="d28ea-168">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="d28ea-168">Line details tab</span></span> |          |
    | <span data-ttu-id="d28ea-169">Manuelt</span><span class="sxs-lookup"><span data-stu-id="d28ea-169">Manual</span></span>           | <span data-ttu-id="d28ea-170">(markeret)</span><span class="sxs-lookup"><span data-stu-id="d28ea-170">(marked)</span></span> |

    <span data-ttu-id="d28ea-171">Linje 3: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="d28ea-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d28ea-172">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-172">Field</span></span>           | <span data-ttu-id="d28ea-173">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="d28ea-174">Lønkode</span><span class="sxs-lookup"><span data-stu-id="d28ea-174">Earnings code</span></span>   | <span data-ttu-id="d28ea-175">Provision i standardvaluta</span><span class="sxs-lookup"><span data-stu-id="d28ea-175">Commission</span></span> |
    | <span data-ttu-id="d28ea-176">Mængde</span><span class="sxs-lookup"><span data-stu-id="d28ea-176">Quantity</span></span>        | <span data-ttu-id="d28ea-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="d28ea-177">1.0000</span></span>     |
    | <span data-ttu-id="d28ea-178">Kurs</span><span class="sxs-lookup"><span data-stu-id="d28ea-178">Rate</span></span>            | <span data-ttu-id="d28ea-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="d28ea-179">!,299.00</span></span>   |
    | <span data-ttu-id="d28ea-180">Kurs</span><span class="sxs-lookup"><span data-stu-id="d28ea-180">Rate</span></span>            | <span data-ttu-id="d28ea-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="d28ea-181">1,299.00</span></span>   |
    | <span data-ttu-id="d28ea-182">Fanen Linjedetalje</span><span class="sxs-lookup"><span data-stu-id="d28ea-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="d28ea-183">Manuelt</span><span class="sxs-lookup"><span data-stu-id="d28ea-183">Manual</span></span>          | <span data-ttu-id="d28ea-184">(markeret)</span><span class="sxs-lookup"><span data-stu-id="d28ea-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="d28ea-185">Det er vigtigt, at indstille skyderen **Manuel** til **Ja** under fanen **Linjedetaljer** for hver lønopgørelseslinje, når der skal angives primolønsaldi for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="d28ea-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="d28ea-186">I ruden **Handling** skal du klikke på **Frigiv lønopgørelse** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="d28ea-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="d28ea-187">Klik i ruden **Handling** på **Betalingsopgørelse** for at åbne siden **Generér betalingsopgørelser**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="d28ea-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="d28ea-188">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-188">Field</span></span>              | <span data-ttu-id="d28ea-189">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="d28ea-190">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="d28ea-190">Payment date</span></span>       | <span data-ttu-id="d28ea-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d28ea-191">6/30/2017</span></span> |
    | <span data-ttu-id="d28ea-192">Betalingskørselstype</span><span class="sxs-lookup"><span data-stu-id="d28ea-192">Payment run type</span></span>   | <span data-ttu-id="d28ea-193">Manuelt</span><span class="sxs-lookup"><span data-stu-id="d28ea-193">Manual</span></span>    |
    | <span data-ttu-id="d28ea-194">Deaktiver regnskab</span><span class="sxs-lookup"><span data-stu-id="d28ea-194">Disable accounting</span></span> |   <span data-ttu-id="d28ea-195">Ja</span><span class="sxs-lookup"><span data-stu-id="d28ea-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="d28ea-196">Dette er kun tilgængeligt, når betalingskørselstypen er manuel, og når brugeren vil deaktivere regnskab for lønkørslen.</span><span class="sxs-lookup"><span data-stu-id="d28ea-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="d28ea-197">Klik på **OK**, og luk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="d28ea-198">Hvorfor skal skyderen Deaktiver regnskab være indstillet til Ja, når der genereres betalingsopgørelser?</span><span class="sxs-lookup"><span data-stu-id="d28ea-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="d28ea-199">Indstilling af skyderen til **Ja** forhindrer, at linjer i betalingsopgørelsen fordeles til hovedbogen.</span><span class="sxs-lookup"><span data-stu-id="d28ea-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="d28ea-200">Finansbeløb blev opdateret tidligere, da kontosaldi fra det oprindelige system blev angivet.</span><span class="sxs-lookup"><span data-stu-id="d28ea-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="d28ea-201">Når du angiver primosaldi for løn, kan du generere rapporter, der indeholder oplysninger fra tidligere år, samt til at identificere grænser med tanke på frynsegoder og til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="d28ea-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="d28ea-202">C.</span><span class="sxs-lookup"><span data-stu-id="d28ea-202">C.</span></span> <span data-ttu-id="d28ea-203">Oprette betalingsopgørelser for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="d28ea-203">Create pay statements for employees</span></span>

<span data-ttu-id="d28ea-204">Når du har oprettet betalingsopgørelser, der har primosaldi, skal du kontrollere, at opgørelserne præcist afspejler lønoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d28ea-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="d28ea-205">Du skal også manuelt opdatere oplysningerne om frynsegoder og skat, så de svarer til værdierne i det oprindelige lønsystem.</span><span class="sxs-lookup"><span data-stu-id="d28ea-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="d28ea-206">Når du har kontrolleret, at beløbene fra oprindelige lønsystem svarer til beløbene på de aktuelle betalingsopgørelser, skal du færdiggøre betalingsopgørelserne.</span><span class="sxs-lookup"><span data-stu-id="d28ea-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="d28ea-207">Åbn siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="d28ea-208">Fremhæve den sidst genererede betalingsopgørelse for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d28ea-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="d28ea-209">Klik på **Rediger** for at åbne siden **Betalingsopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="d28ea-210">Åbn fanen **Frynsegodefradrag**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="d28ea-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="d28ea-211">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-211">Field</span></span>             | <span data-ttu-id="d28ea-212">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="d28ea-213">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="d28ea-213">Benefit</span></span>           | <span data-ttu-id="d28ea-214">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="d28ea-214">Deduction amount</span></span> |
    | <span data-ttu-id="d28ea-215">401K</span><span class="sxs-lookup"><span data-stu-id="d28ea-215">401K</span></span>              | <span data-ttu-id="d28ea-216">Deltag</span><span class="sxs-lookup"><span data-stu-id="d28ea-216">Participate</span></span>      |
    | <span data-ttu-id="d28ea-217">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="d28ea-217">Dental</span></span>            | <span data-ttu-id="d28ea-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="d28ea-218">SubSp</span></span>            |
    | <span data-ttu-id="d28ea-219">Beløb til sikring af afhængige</span><span class="sxs-lookup"><span data-stu-id="d28ea-219">Dep care spending</span></span> | <span data-ttu-id="d28ea-220">Deltag</span><span class="sxs-lookup"><span data-stu-id="d28ea-220">Participate</span></span>      |
    | <span data-ttu-id="d28ea-221">Vision</span><span class="sxs-lookup"><span data-stu-id="d28ea-221">Vision</span></span>            | <span data-ttu-id="d28ea-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="d28ea-222">SupSp</span></span>            |

5. <span data-ttu-id="d28ea-223">Angiv følgende under fanen **Frynsegodebidrag**:</span><span class="sxs-lookup"><span data-stu-id="d28ea-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="d28ea-224">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-224">Field</span></span>   | <span data-ttu-id="d28ea-225">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="d28ea-226">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="d28ea-226">Benefit</span></span> | <span data-ttu-id="d28ea-227">Bidragsbeløb</span><span class="sxs-lookup"><span data-stu-id="d28ea-227">Contribution amount</span></span> |
    | <span data-ttu-id="d28ea-228">401K</span><span class="sxs-lookup"><span data-stu-id="d28ea-228">401K</span></span>    | <span data-ttu-id="d28ea-229">Deltag</span><span class="sxs-lookup"><span data-stu-id="d28ea-229">Participate</span></span>         |
    | <span data-ttu-id="d28ea-230">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="d28ea-230">Dental</span></span>  | <span data-ttu-id="d28ea-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="d28ea-231">SubSp</span></span>               |
    | <span data-ttu-id="d28ea-232">Vision</span><span class="sxs-lookup"><span data-stu-id="d28ea-232">Vision</span></span>  | <span data-ttu-id="d28ea-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="d28ea-233">SubSp</span></span>               |

6. <span data-ttu-id="d28ea-234">Angiv følgende under fanen **Skattefradrag**:</span><span class="sxs-lookup"><span data-stu-id="d28ea-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="d28ea-235">Felt</span><span class="sxs-lookup"><span data-stu-id="d28ea-235">Field</span></span>           | <span data-ttu-id="d28ea-236">Værdi</span><span class="sxs-lookup"><span data-stu-id="d28ea-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="d28ea-237">Momskode</span><span class="sxs-lookup"><span data-stu-id="d28ea-237">Tax code</span></span>        | <span data-ttu-id="d28ea-238">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="d28ea-238">Deduction amount</span></span> |
    | <span data-ttu-id="d28ea-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="d28ea-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="d28ea-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="d28ea-240">1600.00</span></span>          |
    | <span data-ttu-id="d28ea-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="d28ea-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="d28ea-242">825.75</span><span class="sxs-lookup"><span data-stu-id="d28ea-242">825.75</span></span>           |

7. <span data-ttu-id="d28ea-243">Angiv følgende under fanen **Skattebidrag**:</span><span class="sxs-lookup"><span data-stu-id="d28ea-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="d28ea-244">Klik på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="d28ea-245">Kontroller, at de samlede beløb på betalingsopgørelsen svarer til år til dato i det oprindelige system for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="d28ea-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="d28ea-246">Du kan eventuelt vente med afslutningen i næste trin for at foretage en overordnet validering af alle samlede betalingsopgørelser.</span><span class="sxs-lookup"><span data-stu-id="d28ea-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="d28ea-247">Efter valideringen skal du gennemse alle betalingsopgørelser og færdiggøre dem.</span><span class="sxs-lookup"><span data-stu-id="d28ea-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="d28ea-248">Den samme proces kan evt. udføres kvartalsvis for alle tidligere kvartaler i året.</span><span class="sxs-lookup"><span data-stu-id="d28ea-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="d28ea-249">Dette er kun nødvendigt, hvis kunden har brug at se dataene pr. kvartal uden at skulle gå tilbage til det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="d28ea-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="d28ea-250">Hvis du laver en fejl under angivelse af primosaldi for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="d28ea-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="d28ea-251">Det er muligt at tilbageføre posteringer og angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="d28ea-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="d28ea-252">Hvis du vil tilbageføre posteringen, skal du blot udføre følgende trin på siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="d28ea-253">Klik på **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="d28ea-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="d28ea-254">Klik på **Ja**, når meddelelsen "Når du tilbagefører denne betalingsopgørelse, oprettes en tilbageførselsbetalingsopgørelse til modregning af betalingsopgørelsen.</span><span class="sxs-lookup"><span data-stu-id="d28ea-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="d28ea-255">Ingen af betalingsopgørelserne kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="d28ea-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="d28ea-256">Vil du tilbageføre denne betalingsopgørelse?"</span><span class="sxs-lookup"><span data-stu-id="d28ea-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="d28ea-257">vises.</span><span class="sxs-lookup"><span data-stu-id="d28ea-257">displays.</span></span> 

<span data-ttu-id="d28ea-258">Når du tilbagefører betalingsopgørelsen, kan du generere en ny betalingsopgørelse for arbejderen ud fra den lønopgørelse, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="d28ea-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="d28ea-259">Sørg for at rette forkerte linjer på lønopgørelsen, før du genererer den nye betalingsopgørelse, og derefter genererer nye betalingsopgørelser med de korrekte beløb.</span><span class="sxs-lookup"><span data-stu-id="d28ea-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]