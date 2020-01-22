---
title: Konfigurer og køre forespørgslen Likviditet
description: Dette emne indeholder oplysninger om forespørgslen Likviditet. Dette forespørgslen gør det muligt for dig at fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.
author: velofog
manager: AnnBe
ms.date: 10/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2019-10-07
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 28d295db574080735173bed0f40037fb7d66ecad
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935479"
---
# <a name="set-up-and-run-the-cash-position-inquiry"></a><span data-ttu-id="1e0d9-104">Konfigurer og køre forespørgslen Likviditet</span><span class="sxs-lookup"><span data-stu-id="1e0d9-104">Set up and run the Cash position inquiry</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="1e0d9-105">Dette emne indeholder oplysninger om forespørgslen Likviditet.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-105">This topic provides information about the Cash position inquiry.</span></span> <span data-ttu-id="1e0d9-106">Dette forespørgslen gør det muligt for dig at fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-106">This inquiry lets you determine the corresponding cash positions for financial dimension sets that contain self-balancing dimensions.</span></span> <span data-ttu-id="1e0d9-107">Det viser følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-107">It shows the following items:</span></span>

- <span data-ttu-id="1e0d9-108">Startsaldoen for kontantbeholdningen</span><span class="sxs-lookup"><span data-stu-id="1e0d9-108">The beginning cash balance</span></span>
- <span data-ttu-id="1e0d9-109">Virkningen af tilførelsen af kasseboner</span><span class="sxs-lookup"><span data-stu-id="1e0d9-109">The effect of the addition of cash receipts</span></span>
- <span data-ttu-id="1e0d9-110">Subtraktion af kontante udbetalinger</span><span class="sxs-lookup"><span data-stu-id="1e0d9-110">The subtraction of cash disbursements</span></span>
- <span data-ttu-id="1e0d9-111">Subtraktion af overførsler mellem fonde for at komme til en slutsaldo</span><span class="sxs-lookup"><span data-stu-id="1e0d9-111">The subtraction of interfund transfers to arrive at an ending balance</span></span>
- <span data-ttu-id="1e0d9-112">Subtraktion af generelle budgetreservationer, behæftelser eller budgetreservationer fra slutsaldoen for at få en ikke-behæftet saldo</span><span class="sxs-lookup"><span data-stu-id="1e0d9-112">The subtraction of general budget reservations, encumbrances, or pre-encumbrances from the ending balance to arrive at an unencumbered balance</span></span>

<span data-ttu-id="1e0d9-113">Denne forespørgsel adskiller sig fra andre forespørgsler, fordi du kan tilpasse terminologien for kolonnenavne og de hovedkonti, der bruges til at aflede de beløb, der fremgår af kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-113">This inquiry differs from other inquiries because you can customize the terminology for column names and for the main accounts that are used to derive the amounts that appear in the columns.</span></span> <span data-ttu-id="1e0d9-114">På siden **Likviditetsparametre** nummereres de kolonner, der vises i forespørgslen, fortløbende fra venstre mod højre.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-114">On the **Cash position parameters** page, the columns that appear in the inquiry are numbered sequentially from left to right.</span></span> <span data-ttu-id="1e0d9-115">Kolonnen yderst til venstre er **Kolonne et**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-115">The left-most column is **Column one**.</span></span>

## <a name="set-up-the-cash-position-inquiry"></a><span data-ttu-id="1e0d9-116">Konfigurer forespørgslen Likviditet</span><span class="sxs-lookup"><span data-stu-id="1e0d9-116">Set up the Cash position inquiry</span></span>

1. <span data-ttu-id="1e0d9-117">Gå til **Finans \> Opsætning af finans \> Likviditetsparametre**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-117">Go to **General ledger \> Ledger setup \> Cash position parameters**.</span></span>
2. <span data-ttu-id="1e0d9-118">På siden **Likviditetsparametre** i gruppen **Kolonne ét** skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-118">On the **Cash position parameters** page, in the **Column one** group, follow these steps:</span></span>

    - <span data-ttu-id="1e0d9-119">I feltet **Kolonnenavn** skal du angive en etiket for overskriften på den første kolonne i forespørgslen (f.eks. **Startsaldo**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-119">In the **Column name** field, enter a label for the heading of the first column in the inquiry (for example, **Beginning balance**).</span></span>
    - <span data-ttu-id="1e0d9-120">I feltet **Startsaldo på hovedkonti** skal du vælge de konti, du vil referere til i forbindelse med forespørgsler om startsaldoen.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-120">In the **Opening balance main accounts** field, select the accounts that you want to reference for inquiries about the opening balance.</span></span>

3. <span data-ttu-id="1e0d9-121">Benyt følgende fremgangsmåde i gruppen **Kolonne to**:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-121">In the **Column two** group, follow these steps:</span></span>

    - <span data-ttu-id="1e0d9-122">Indtast en etiket for overskriften på den anden kolonne (f.eks. **Indbetalinger**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-122">Enter a label for the heading of the second column (for example, **Cash receipts**).</span></span>
    - <span data-ttu-id="1e0d9-123">På listen **Debet- og kredit hovedkonti** skal du vælge hovedkontiene, for kun at anvende summen af alle debet- og kredittransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-123">To use only the sum of all debit and credit transaction amounts for the data that is included in the inquiry, select the main accounts in the **Debit and credit main accounts** list.</span></span>
    
        <span data-ttu-id="1e0d9-124">Forespørgslen tilføjer nettobeløbet for debet- og kreditkontiene plus debetbeløb og kreditbeløb fra de hovedkonti, der er specificeret i de andre felter i gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-124">The inquiry will add the net amount of the debit and credit accounts, plus the debit and credit amounts from the main accounts that are specified in the other fields in the group.</span></span>

    - <span data-ttu-id="1e0d9-125">For kun at bruge summen af alle debettransaktioner for forespørgselsdataene skal du vælge hovedkontiene på listen **Kun debethovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-125">To use only the sum of all debit transaction amounts for the inquiry's data, select the main accounts in the **Debit-only main accounts** list.</span></span>
    - <span data-ttu-id="1e0d9-126">For kun at bruge summen af alle kredittransaktioner for forespørgselsdataene skal du vælge hovedkontiene på listen **Kun kredithovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-126">To use only the sum of all credit transaction amounts for the inquiry's data, select the main accounts in the **Credit-only main accounts** list.</span></span>

4. <span data-ttu-id="1e0d9-127">Følg disse trin for **Kolonne tre**- og **Kolonne fire**-grupper:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-127">In the **Column three** and **Column four** groups, follow these steps:</span></span>

    - <span data-ttu-id="1e0d9-128">Indtast en etiket for overskriften til den tredje kolonne (f.eks. **Kontante udbetalinger**) og den fjerde kolonne (f.eks. **Overførsler mellem fonde**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-128">Enter a label for the heading of the third column (for example, **Cash disbursements**) and the fourth column (for example, **Interfund transfers**).</span></span>
    - <span data-ttu-id="1e0d9-129">For begge kolonner skal du angive de hovedkonti, du vil distribuere debet- og kreditposter til.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-129">For both columns, specify the main accounts to distribute debit and credit entries.</span></span> <span data-ttu-id="1e0d9-130">Du skal også angive "kun debet"- og "kun kredit"-hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-130">Also specify the debit-only main accounts and credit-only main accounts.</span></span>

5. <span data-ttu-id="1e0d9-131">I gruppen **Kolonne fem** skal du angive en etiket for overskriften for den femte kolonne (f.eks. **Slutsaldo**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-131">In the **Column five** group, enter a label for the heading of the fifth column (for example, **Ending balance**).</span></span>

    <span data-ttu-id="1e0d9-132">Et resultat beregnes automatisk ud fra de konti, du har angivet i de første fire kolonner.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-132">A result is automatically calculated from the accounts that you specified in the first four columns.</span></span> <span data-ttu-id="1e0d9-133">I dette eksempel er beregningen Åbningssaldo + Kontantindbetalinger - Kontante udbetalinger - Overførsler mellem fonde.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-133">For this example, the calculation is Beginning balance + Cash receipts – Cash disbursements – Interfund transfers.</span></span>

6. <span data-ttu-id="1e0d9-134">Følg disse trin for **Kolonne seks**- og **Kolonne syv**-grupper:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-134">In the **Column six** and **Column seven** groups, follow these steps:</span></span>

    - <span data-ttu-id="1e0d9-135">Indtast en etiket for overskriften for den sjette kolonne seks (f.eks. **Generelle budgetreservationer** eller **Behæftelser**) og den syvende kolonne (f.eks. **Budgetreservationer**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-135">Enter a label for the heading of the sixth column (for example, **General budget reservations** or **Encumbrances**) and the seventh column (for example, **Pre-encumbrances**).</span></span>
    - <span data-ttu-id="1e0d9-136">I begge kolonner kan du angive kontonumre for debet- og kredithovedkonti, og for kun debethovedkontiene samt kun kredithovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-136">For both columns, specify account numbers for the debit and credit main accounts, and for the debit-only main accounts and credit-only main accounts.</span></span>

7. <span data-ttu-id="1e0d9-137">I gruppen **Kolonne otte** skal du angive en etiket for overskriften for den ottende kolonne (f.eks. **Ikke-behæftet saldo**).</span><span class="sxs-lookup"><span data-stu-id="1e0d9-137">In the **Column eight** group, enter a label for the heading of the eighth column (for example, **Unencumbered balance**).</span></span>

    <span data-ttu-id="1e0d9-138">Et resultat beregnes automatisk ud fra de konti, du har angivet i femte til syvende kolonne.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-138">A result is automatically calculated from the accounts that you specified in the fifth through seventh columns.</span></span> <span data-ttu-id="1e0d9-139">I dette eksempel er beregningen Slutsaldo - Behæftelser - Budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-139">For this example, the calculation is Ending balance – Encumbrances – Pre-encumbrances.</span></span>

8. <span data-ttu-id="1e0d9-140">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-140">Select **Save**.</span></span>

## <a name="run-the-cash-position-inquiry"></a><span data-ttu-id="1e0d9-141">Kør forespørgslen Likviditet</span><span class="sxs-lookup"><span data-stu-id="1e0d9-141">Run the Cash position inquiry</span></span>

1. <span data-ttu-id="1e0d9-142">Gå til **Finans \> Forespørgsler og rapporter \> Likviditet**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-142">Go to **General ledger \> Inquiries and reports \> Cash position**.</span></span>
2. <span data-ttu-id="1e0d9-143">Benyt følgende fremgangsmåde i afsnittet **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="1e0d9-143">In the **Parameters** section, follow these steps:</span></span>

    - <span data-ttu-id="1e0d9-144">Vælg koden for datointervallet i feltet **Datointerval**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-144">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="1e0d9-145">Alternativt kan du i felterne **Fra dato** og **Til dato** definere datointervallet.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-145">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    - <span data-ttu-id="1e0d9-146">Vælg det økonomiske dimensionssæt i feltet **Økonomisk dimensionssæt**.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-146">In the **Financial dimension set** field, select the financial dimension set.</span></span>
    - <span data-ttu-id="1e0d9-147">Valgmulighed: Indstil **Undertryk konti med ene nuller** til **Ja** for at udelukke konti, der kun har 0 (nul) saldi, fra forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-147">Optional: Set the **Suppress accounts with all zeroes** option to **Yes** to exclude accounts from the inquiry if they have all 0 (zero) balances.</span></span>
    - <span data-ttu-id="1e0d9-148">Valgmulighed: Indstil **Vis segmenter i separate kolonner** til **Ja** for at få vist kontonavnene for hver dimension som separate kolonner i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-148">Optional: Set the **Display segments in separate columns** option to **Yes** to show the account names for each dimension as separate columns in the grid.</span></span>
    - <span data-ttu-id="1e0d9-149">Valgmulighed: For at filtrere værdierne for en bestemt dimension, skal du i felterne under feltet **Økonomiske dimensionssæt** vælge, hvilke dimensioner der skal medtages.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-149">Optional: To filter the values for a specific dimension, in the fields below the **Financial dimension set** field, select the dimensions to include.</span></span> <span data-ttu-id="1e0d9-150">De tilgængelige valgmuligheder varierer afhængigt af det økonomiske dimensionssæt, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-150">The options that are available vary, depending on the financial dimension set that you selected.</span></span>

3. <span data-ttu-id="1e0d9-151">Vælg **Beregn saldi** for at køre forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="1e0d9-151">Select **Calculate balances** to run the inquiry.</span></span>
