---
title: Angive primosaldi for løn
description: Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms.
author: andreabichsel
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
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752144"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="5f455-103">Angive startsaldi for løn</span><span class="sxs-lookup"><span data-stu-id="5f455-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f455-104">Emnet beskriver trinnene til angivelse af primosaldi for lønkoder, fradrag, frynsegoder og moms.</span><span class="sxs-lookup"><span data-stu-id="5f455-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="5f455-105">Disse oplysninger er vigtig for partnere, som vil overflytte eller overføre data til en ny lønimplementering fra et andet system.</span><span class="sxs-lookup"><span data-stu-id="5f455-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="5f455-106">Som indledning til at angive primolønsaldi skal vi kontrollere følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="5f455-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="5f455-107">Medarbejderregistreringer er angivet og er tilgængelige i systemet</span><span class="sxs-lookup"><span data-stu-id="5f455-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="5f455-108">Følgende data er konfigureret og tildelt til medarbejdere:</span><span class="sxs-lookup"><span data-stu-id="5f455-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="5f455-109">Betalingscyklusser og lønperioder</span><span class="sxs-lookup"><span data-stu-id="5f455-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="5f455-110">Lønkoder</span><span class="sxs-lookup"><span data-stu-id="5f455-110">Earning codes</span></span>
    - <span data-ttu-id="5f455-111">Moms</span><span class="sxs-lookup"><span data-stu-id="5f455-111">Taxes</span></span>
    - <span data-ttu-id="5f455-112">Frynsegoder og fradrag</span><span class="sxs-lookup"><span data-stu-id="5f455-112">Benefits and deductions</span></span>

- <span data-ttu-id="5f455-113">Virksomheden skal have valgt en dato, som skal gælde for angivelse af primosaldi for løn.</span><span class="sxs-lookup"><span data-stu-id="5f455-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="5f455-114">Der er indsamlet oplysninger om alle indtægter, frynsegoder/fradrag, frynsegodebidrag, medarbejderskat, selskabsskat og deres år til dato-beløb fra det gamle system.</span><span class="sxs-lookup"><span data-stu-id="5f455-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="5f455-115">Når du skal angive primosaldi, skal du overveje, hvor detaljerede dataene skal være.</span><span class="sxs-lookup"><span data-stu-id="5f455-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="5f455-116">De fleste virksomheder angive et enkelt, konsolideret år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="5f455-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="5f455-117">Hvis der kræves mere detaljerede oplysninger, kan saldi dog angives kvartalsvis.</span><span class="sxs-lookup"><span data-stu-id="5f455-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="5f455-118">Angivelse af det detaljeringsniveau, der er nødvendigt, bestemmer også, hvor mange manuelle betalingsopgørelser der skal oprettes for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="5f455-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="5f455-119">Der er kun brug for én manuel opgørelse for hver medarbejder for et enkelt år-til-dato-beløb.</span><span class="sxs-lookup"><span data-stu-id="5f455-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="5f455-120">Brug år-til-dato-beløb fra den endelige betalingsopgørelse fra det tidligere system som det beløb, der skal angives i det nye lønsystem, for at bruge dette.</span><span class="sxs-lookup"><span data-stu-id="5f455-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="5f455-121">Følgende eksempel viser, hvordan du kan angive medarbejderens primolønsaldi, herunder lønkoder, frynsegoder/fradrag og skat.</span><span class="sxs-lookup"><span data-stu-id="5f455-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="5f455-122">I et eksempel fra den virkelige verden har du et linjeelement for hver lønkode, hvert frynsegodefradrag, frynsegodebidrag, medarbejderskat og selskabsskat, hvor det angivne beløb er år-til-dato-beløbet.</span><span class="sxs-lookup"><span data-stu-id="5f455-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="5f455-123">Brug listen over koder og beløb, og følg trinene for at oprette en manuel løn- og betalingsopgørelse. Deaktiver regnskab for at overføre primosaldi i forbindelse med lønbehandling.</span><span class="sxs-lookup"><span data-stu-id="5f455-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="5f455-124">Du skal deaktivere regnskab, fordi du ikke vil bogføre primosaldoen for denne betalingsopgørelse til finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="5f455-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="5f455-125">Det blev foretaget i det oprindelige system og overføres til det nye system, når du definerer startsaldi i Finans.</span><span class="sxs-lookup"><span data-stu-id="5f455-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="5f455-126">A.</span><span class="sxs-lookup"><span data-stu-id="5f455-126">A.</span></span> <span data-ttu-id="5f455-127">Sådan konfigurerer du lønkoder, der skal bruges på primolønsaldi</span><span class="sxs-lookup"><span data-stu-id="5f455-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="5f455-128">Når du angiver primosaldi for løn, skal du kontrollere, at de lønkoder, du vil bruge, er konfigureret, så indstillingen "Tillad redigering af satser på lønopgørelsen" er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="5f455-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="5f455-129">På denne måde kan du manuelt indtaste beløbet fra det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="5f455-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="5f455-130">B.</span><span class="sxs-lookup"><span data-stu-id="5f455-130">B.</span></span> <span data-ttu-id="5f455-131">Oprette lønopgørelse for en medarbejder med en primosaldo</span><span class="sxs-lookup"><span data-stu-id="5f455-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="5f455-132">Dette trin opretter manuelt en lønopgørelse for hver arbejder for den sidste lønperiode af oprindelige system, som opretter lønopgørelseslinjerne i nye lønsystem.</span><span class="sxs-lookup"><span data-stu-id="5f455-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="5f455-133">Angiv én linje pr. lønkode og år til dato-beløb og timer.</span><span class="sxs-lookup"><span data-stu-id="5f455-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="5f455-134">Der er følgende trin i eksemplet:</span><span class="sxs-lookup"><span data-stu-id="5f455-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="5f455-135">Åbn siden **Alle lønopgørelser**, og klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5f455-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="5f455-136">Angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="5f455-136">Enter the following:</span></span> 

    | <span data-ttu-id="5f455-137">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-137">Field</span></span>      | <span data-ttu-id="5f455-138">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="5f455-139">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="5f455-139">Worker</span></span>     | <span data-ttu-id="5f455-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="5f455-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="5f455-141">Betalingscyklus</span><span class="sxs-lookup"><span data-stu-id="5f455-141">Pay cycle</span></span>  | <span data-ttu-id="5f455-142">sm</span><span class="sxs-lookup"><span data-stu-id="5f455-142">sm</span></span>                    |
    | <span data-ttu-id="5f455-143">Lønperiode</span><span class="sxs-lookup"><span data-stu-id="5f455-143">Pay period</span></span> | <span data-ttu-id="5f455-144">16-06-2017 - 30-06-2017</span><span class="sxs-lookup"><span data-stu-id="5f455-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="5f455-145">Under fanen **Post på lønopgørelse** skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="5f455-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="5f455-146">Linje 1: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="5f455-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5f455-147">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-147">Field</span></span>            | <span data-ttu-id="5f455-148">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="5f455-149">Lønkode</span><span class="sxs-lookup"><span data-stu-id="5f455-149">Earnings code</span></span>    | <span data-ttu-id="5f455-150">Fast løn</span><span class="sxs-lookup"><span data-stu-id="5f455-150">Regular pay</span></span> |
    | <span data-ttu-id="5f455-151">Mængde</span><span class="sxs-lookup"><span data-stu-id="5f455-151">Quantity</span></span>         | <span data-ttu-id="5f455-152">1.00</span><span class="sxs-lookup"><span data-stu-id="5f455-152">1.00</span></span>        |
    | <span data-ttu-id="5f455-153">Kurs</span><span class="sxs-lookup"><span data-stu-id="5f455-153">Rate</span></span>             | <span data-ttu-id="5f455-154">30,000</span><span class="sxs-lookup"><span data-stu-id="5f455-154">30,000</span></span>      |
    | <span data-ttu-id="5f455-155">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="5f455-155">Line details tab</span></span> |             |
    | <span data-ttu-id="5f455-156">Manuelt</span><span class="sxs-lookup"><span data-stu-id="5f455-156">Manual</span></span>           | <span data-ttu-id="5f455-157">(markeret)</span><span class="sxs-lookup"><span data-stu-id="5f455-157">(marked)</span></span>    |

    <span data-ttu-id="5f455-158">Linje 2: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="5f455-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5f455-159">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-159">Field</span></span>            | <span data-ttu-id="5f455-160">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="5f455-161">Lønkode</span><span class="sxs-lookup"><span data-stu-id="5f455-161">Earnings code</span></span>    | <span data-ttu-id="5f455-162">Bonus</span><span class="sxs-lookup"><span data-stu-id="5f455-162">Bonus</span></span>    |
    | <span data-ttu-id="5f455-163">Mængde</span><span class="sxs-lookup"><span data-stu-id="5f455-163">Quantity</span></span>         | <span data-ttu-id="5f455-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="5f455-164">1.0000</span></span>   |
    | <span data-ttu-id="5f455-165">Kurs</span><span class="sxs-lookup"><span data-stu-id="5f455-165">Rate</span></span>             | <span data-ttu-id="5f455-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="5f455-166">4250.00</span></span>  |
    | <span data-ttu-id="5f455-167">Fanen Linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="5f455-167">Line details tab</span></span> |          |
    | <span data-ttu-id="5f455-168">Manuelt</span><span class="sxs-lookup"><span data-stu-id="5f455-168">Manual</span></span>           | <span data-ttu-id="5f455-169">(markeret)</span><span class="sxs-lookup"><span data-stu-id="5f455-169">(marked)</span></span> |

    <span data-ttu-id="5f455-170">Linje 3: Fanen **Post på lønopgørelse**</span><span class="sxs-lookup"><span data-stu-id="5f455-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5f455-171">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-171">Field</span></span>           | <span data-ttu-id="5f455-172">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="5f455-173">Lønkode</span><span class="sxs-lookup"><span data-stu-id="5f455-173">Earnings code</span></span>   | <span data-ttu-id="5f455-174">Provision i standardvaluta</span><span class="sxs-lookup"><span data-stu-id="5f455-174">Commission</span></span> |
    | <span data-ttu-id="5f455-175">Mængde</span><span class="sxs-lookup"><span data-stu-id="5f455-175">Quantity</span></span>        | <span data-ttu-id="5f455-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="5f455-176">1.0000</span></span>     |
    | <span data-ttu-id="5f455-177">Kurs</span><span class="sxs-lookup"><span data-stu-id="5f455-177">Rate</span></span>            | <span data-ttu-id="5f455-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="5f455-178">!,299.00</span></span>   |
    | <span data-ttu-id="5f455-179">Kurs</span><span class="sxs-lookup"><span data-stu-id="5f455-179">Rate</span></span>            | <span data-ttu-id="5f455-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="5f455-180">1,299.00</span></span>   |
    | <span data-ttu-id="5f455-181">Fanen Linjedetalje</span><span class="sxs-lookup"><span data-stu-id="5f455-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="5f455-182">Manuelt</span><span class="sxs-lookup"><span data-stu-id="5f455-182">Manual</span></span>          | <span data-ttu-id="5f455-183">(markeret)</span><span class="sxs-lookup"><span data-stu-id="5f455-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="5f455-184">Det er vigtigt, at indstille skyderen **Manuel** til **Ja** under fanen **Linjedetaljer** for hver lønopgørelseslinje, når der skal angives primolønsaldi for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="5f455-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="5f455-185">I ruden **Handling** skal du klikke på **Frigiv lønopgørelse** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="5f455-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="5f455-186">Klik i ruden **Handling** på **Betalingsopgørelse** for at åbne siden **Generér betalingsopgørelser**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="5f455-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="5f455-187">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-187">Field</span></span>              | <span data-ttu-id="5f455-188">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="5f455-189">Betalingsdato</span><span class="sxs-lookup"><span data-stu-id="5f455-189">Payment date</span></span>       | <span data-ttu-id="5f455-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="5f455-190">6/30/2017</span></span> |
    | <span data-ttu-id="5f455-191">Betalingskørselstype</span><span class="sxs-lookup"><span data-stu-id="5f455-191">Payment run type</span></span>   | <span data-ttu-id="5f455-192">Manuelt</span><span class="sxs-lookup"><span data-stu-id="5f455-192">Manual</span></span>    |
    | <span data-ttu-id="5f455-193">Deaktiver regnskab</span><span class="sxs-lookup"><span data-stu-id="5f455-193">Disable accounting</span></span> |   <span data-ttu-id="5f455-194">Ja</span><span class="sxs-lookup"><span data-stu-id="5f455-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="5f455-195">Dette er kun tilgængeligt, når betalingskørselstypen er manuel, og når brugeren vil deaktivere regnskab for lønkørslen.</span><span class="sxs-lookup"><span data-stu-id="5f455-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="5f455-196">Klik på **OK**, og luk **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="5f455-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="5f455-197">Hvorfor skal skyderen Deaktiver regnskab være indstillet til Ja, når der genereres betalingsopgørelser?</span><span class="sxs-lookup"><span data-stu-id="5f455-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="5f455-198">Indstilling af skyderen til **Ja** forhindrer, at linjer i betalingsopgørelsen fordeles til hovedbogen.</span><span class="sxs-lookup"><span data-stu-id="5f455-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="5f455-199">Finansbeløb blev opdateret tidligere, da kontosaldi fra det oprindelige system blev angivet.</span><span class="sxs-lookup"><span data-stu-id="5f455-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="5f455-200">Når du angiver primosaldi for løn, kan du generere rapporter, der indeholder oplysninger fra tidligere år, samt til at identificere grænser med tanke på frynsegoder og til skattemæssige formål.</span><span class="sxs-lookup"><span data-stu-id="5f455-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="5f455-201">C.</span><span class="sxs-lookup"><span data-stu-id="5f455-201">C.</span></span> <span data-ttu-id="5f455-202">Oprette betalingsopgørelser for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="5f455-202">Create pay statements for employees</span></span>

<span data-ttu-id="5f455-203">Når du har oprettet betalingsopgørelser, der har primosaldi, skal du kontrollere, at opgørelserne præcist afspejler lønoplysninger.</span><span class="sxs-lookup"><span data-stu-id="5f455-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="5f455-204">Du skal også manuelt opdatere oplysningerne om frynsegoder og skat, så de svarer til værdierne i det oprindelige lønsystem.</span><span class="sxs-lookup"><span data-stu-id="5f455-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="5f455-205">Når du har kontrolleret, at beløbene fra oprindelige lønsystem svarer til beløbene på de aktuelle betalingsopgørelser, skal du færdiggøre betalingsopgørelserne.</span><span class="sxs-lookup"><span data-stu-id="5f455-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="5f455-206">Åbn siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="5f455-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="5f455-207">Fremhæve den sidst genererede betalingsopgørelse for Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="5f455-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="5f455-208">Klik på **Rediger** for at åbne siden **Betalingsopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="5f455-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="5f455-209">Åbn fanen **Frynsegodefradrag**, og angiv følgende:</span><span class="sxs-lookup"><span data-stu-id="5f455-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="5f455-210">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-210">Field</span></span>             | <span data-ttu-id="5f455-211">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="5f455-212">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="5f455-212">Benefit</span></span>           | <span data-ttu-id="5f455-213">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="5f455-213">Deduction amount</span></span> |
    | <span data-ttu-id="5f455-214">401K</span><span class="sxs-lookup"><span data-stu-id="5f455-214">401K</span></span>              | <span data-ttu-id="5f455-215">Deltag</span><span class="sxs-lookup"><span data-stu-id="5f455-215">Participate</span></span>      |
    | <span data-ttu-id="5f455-216">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="5f455-216">Dental</span></span>            | <span data-ttu-id="5f455-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="5f455-217">SubSp</span></span>            |
    | <span data-ttu-id="5f455-218">Beløb til sikring af afhængige</span><span class="sxs-lookup"><span data-stu-id="5f455-218">Dep care spending</span></span> | <span data-ttu-id="5f455-219">Deltag</span><span class="sxs-lookup"><span data-stu-id="5f455-219">Participate</span></span>      |
    | <span data-ttu-id="5f455-220">Vision</span><span class="sxs-lookup"><span data-stu-id="5f455-220">Vision</span></span>            | <span data-ttu-id="5f455-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="5f455-221">SupSp</span></span>            |

5. <span data-ttu-id="5f455-222">Angiv følgende under fanen **Frynsegodebidrag**:</span><span class="sxs-lookup"><span data-stu-id="5f455-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="5f455-223">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-223">Field</span></span>   | <span data-ttu-id="5f455-224">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="5f455-225">Frynsegode</span><span class="sxs-lookup"><span data-stu-id="5f455-225">Benefit</span></span> | <span data-ttu-id="5f455-226">Bidragsbeløb</span><span class="sxs-lookup"><span data-stu-id="5f455-226">Contribution amount</span></span> |
    | <span data-ttu-id="5f455-227">401K</span><span class="sxs-lookup"><span data-stu-id="5f455-227">401K</span></span>    | <span data-ttu-id="5f455-228">Deltag</span><span class="sxs-lookup"><span data-stu-id="5f455-228">Participate</span></span>         |
    | <span data-ttu-id="5f455-229">Tandlægeforsikring</span><span class="sxs-lookup"><span data-stu-id="5f455-229">Dental</span></span>  | <span data-ttu-id="5f455-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="5f455-230">SubSp</span></span>               |
    | <span data-ttu-id="5f455-231">Vision</span><span class="sxs-lookup"><span data-stu-id="5f455-231">Vision</span></span>  | <span data-ttu-id="5f455-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="5f455-232">SubSp</span></span>               |

6. <span data-ttu-id="5f455-233">Angiv følgende under fanen **Skattefradrag**:</span><span class="sxs-lookup"><span data-stu-id="5f455-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="5f455-234">Felt</span><span class="sxs-lookup"><span data-stu-id="5f455-234">Field</span></span>           | <span data-ttu-id="5f455-235">Værdi</span><span class="sxs-lookup"><span data-stu-id="5f455-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="5f455-236">Momskode</span><span class="sxs-lookup"><span data-stu-id="5f455-236">Tax code</span></span>        | <span data-ttu-id="5f455-237">Fradragsbeløb</span><span class="sxs-lookup"><span data-stu-id="5f455-237">Deduction amount</span></span> |
    | <span data-ttu-id="5f455-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="5f455-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="5f455-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="5f455-239">1600.00</span></span>          |
    | <span data-ttu-id="5f455-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="5f455-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="5f455-241">825.75</span><span class="sxs-lookup"><span data-stu-id="5f455-241">825.75</span></span>           |

7. <span data-ttu-id="5f455-242">Angiv følgende under fanen **Skattebidrag**:</span><span class="sxs-lookup"><span data-stu-id="5f455-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="5f455-243">Klik på **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="5f455-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="5f455-244">Kontroller, at de samlede beløb på betalingsopgørelsen svarer til år til dato i det oprindelige system for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="5f455-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="5f455-245">Du kan eventuelt vente med afslutningen i næste trin for at foretage en overordnet validering af alle samlede betalingsopgørelser.</span><span class="sxs-lookup"><span data-stu-id="5f455-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="5f455-246">Efter valideringen skal du gennemse alle betalingsopgørelser og færdiggøre dem.</span><span class="sxs-lookup"><span data-stu-id="5f455-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="5f455-247">Den samme proces kan evt. udføres kvartalsvis for alle tidligere kvartaler i året.</span><span class="sxs-lookup"><span data-stu-id="5f455-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="5f455-248">Dette er kun nødvendigt, hvis kunden har brug at se dataene pr. kvartal uden at skulle gå tilbage til det oprindelige system.</span><span class="sxs-lookup"><span data-stu-id="5f455-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="5f455-249">Hvis du laver en fejl under angivelse af primosaldi for en medarbejder</span><span class="sxs-lookup"><span data-stu-id="5f455-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="5f455-250">Det er muligt at tilbageføre posteringer og angive dem igen.</span><span class="sxs-lookup"><span data-stu-id="5f455-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="5f455-251">Hvis du vil tilbageføre posteringen, skal du blot udføre følgende trin på siden **Alle betalingsopgørelser**.</span><span class="sxs-lookup"><span data-stu-id="5f455-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="5f455-252">Klik på **Tilbagefør**.</span><span class="sxs-lookup"><span data-stu-id="5f455-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="5f455-253">Klik på **Ja**, når meddelelsen "Når du tilbagefører denne betalingsopgørelse, oprettes en tilbageførselsbetalingsopgørelse til modregning af betalingsopgørelsen.</span><span class="sxs-lookup"><span data-stu-id="5f455-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="5f455-254">Ingen af betalingsopgørelserne kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="5f455-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="5f455-255">Vil du tilbageføre denne betalingsopgørelse?"</span><span class="sxs-lookup"><span data-stu-id="5f455-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="5f455-256">vises.</span><span class="sxs-lookup"><span data-stu-id="5f455-256">displays.</span></span> 

<span data-ttu-id="5f455-257">Når du tilbagefører betalingsopgørelsen, kan du generere en ny betalingsopgørelse for arbejderen ud fra den lønopgørelse, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="5f455-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="5f455-258">Sørg for at rette forkerte linjer på lønopgørelsen, før du genererer den nye betalingsopgørelse, og derefter genererer nye betalingsopgørelser med de korrekte beløb.</span><span class="sxs-lookup"><span data-stu-id="5f455-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]