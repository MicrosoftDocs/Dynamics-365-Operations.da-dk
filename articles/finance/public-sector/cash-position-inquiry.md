---
title: Forespørgsel på likviditet
description: Dette emne indeholder oplysninger om, hvordan du fastlægger den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.
author: velofog
manager: AnnBe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: public sector
ms.author: roschlom
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 3be4613912bece767e52668079841419757e7724
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971176"
---
# <a name="cash-position-inquiry"></a><span data-ttu-id="44563-103">Forespørgsel på likviditet</span><span class="sxs-lookup"><span data-stu-id="44563-103">Cash position inquiry</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="44563-104">Med forespørgslen **Likviditet** kan du fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.</span><span class="sxs-lookup"><span data-stu-id="44563-104">The **Cash position** inquiry allows you to determine the corresponding cash positions for financial dimension sets that contain self-balancing dimensions.</span></span> <span data-ttu-id="44563-105">I forespørgslen vises startkassesaldoen og resultatet af tilførte kasseboner, subtraktion af kontante udbetalinger og subtraktion af overførsler mellem fonde for at komme til en slutsaldo.</span><span class="sxs-lookup"><span data-stu-id="44563-105">The inquiry shows the beginning cash balance, and the effect of the addition of cash receipts, the subtraction of cash disbursements, and the subtraction of interfund transfers to arrive at an ending balance.</span></span> <span data-ttu-id="44563-106">Derefter trækkes de generelle budgetreservationer, behæftelser eller budgetreservationer fra slutsaldoen for at få en ikke-behæftet saldo.</span><span class="sxs-lookup"><span data-stu-id="44563-106">Then, from the ending balance, general budget reservations, encumbrances, or pre-encumbrances are subtracted to arrive at an unencumbered balance.</span></span>

<span data-ttu-id="44563-107">Denne forespørgsel er entydig, da den giver brugerne mulighed for at tilpasse terminologien for kolonnenavne og de hovedkonti, der bruges til at aflede beløbene for kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="44563-107">This inquiry is unique in that it allows users to customize the terminology for column names and for the main accounts that are used to derive amounts for the columns.</span></span> <span data-ttu-id="44563-108">På siden **Likviditetsparametre** er de kolonner, der vises i forespørgslen, nummereret startende med kolonnen længst til venstre som kolonne ét.</span><span class="sxs-lookup"><span data-stu-id="44563-108">On the **Cash position parameters** page, the columns that appear in the inquiry are numbered starting with the left-most data column as column one.</span></span>

## <a name="cash-position-inquiry-setup"></a><span data-ttu-id="44563-109">Opsætning af forespørgsel på likviditet</span><span class="sxs-lookup"><span data-stu-id="44563-109">Cash position inquiry setup</span></span>

1. <span data-ttu-id="44563-110">Gå til **Finans** > **Opsætning Finans** > **Likviditetsparametre**.</span><span class="sxs-lookup"><span data-stu-id="44563-110">Go to **General ledger** > **Ledger setup** > **Cash position parameters**.</span></span>
2. <span data-ttu-id="44563-111">På siden **Likviditetsparametre** i sektionen **Kolonne ét**:</span><span class="sxs-lookup"><span data-stu-id="44563-111">In the **Cash position parameters** page, in the **Column one** section:</span></span>

- <span data-ttu-id="44563-112">I feltet **Kolonnenavn** skal du skrive en etiket, der skal bruges som overskrift til den første kolonne i forespørgslen (f.eks. "Startsaldo").</span><span class="sxs-lookup"><span data-stu-id="44563-112">In the **Column name** field, type a label to use as the header for the inquiry’s first column (for example, "Beginning balance").</span></span>
- <span data-ttu-id="44563-113">I feltet **Startsaldo på hovedkonti** skal du vælge den eller de konti, du vil referere til i forbindelse med forespørgsler på startsaldoen.</span><span class="sxs-lookup"><span data-stu-id="44563-113">In the **Opening balance main accounts** field, select the account(s) that you want to reference for inquiring on the opening balance.</span></span>

3. <span data-ttu-id="44563-114">I sektionen **Kolonne to**:</span><span class="sxs-lookup"><span data-stu-id="44563-114">In the **Column two** section:</span></span> 

- <span data-ttu-id="44563-115">Angiv en etiket til den anden kolonne i forespørgslen (f.eks. "Indbetalinger").</span><span class="sxs-lookup"><span data-stu-id="44563-115">Specify a label for the second column in the inquiry (for example, "Cash receipts").</span></span>
- <span data-ttu-id="44563-116">På listen **Debet- og kredit hovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debet- og kredittransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="44563-116">In the **Debit and credit main accounts** list, select the main accounts from which to use only the sum of all debit and credit transaction amounts for the inquiry's data.</span></span> 

> [!NOTE]
> <span data-ttu-id="44563-117">Forespørgslen tilføjer debet- og kreditkontiene nettobeløb plus debetbeløb og kreditbeløb fra hovedkontiene i de andre felter i gruppen.</span><span class="sxs-lookup"><span data-stu-id="44563-117">The inquiry will add the net of the debit and credit accounts plus the debit amount and credit amounts from the main accounts in the other fields in the group.</span></span>

- <span data-ttu-id="44563-118">På listen **Kun debethovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debettransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="44563-118">In the **Debit-only main accounts** list, select the main accounts from which to use only the sum of all debit transaction amounts for the inquiry's data.</span></span>
- <span data-ttu-id="44563-119">På listen **Kun kredithovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle kredittransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="44563-119">In the **Credit-only main accounts** list, select the main accounts from which to use only the sum of all credit transaction amounts for the inquiry's data.</span></span>

4. <span data-ttu-id="44563-120">I sektionerne **Kolonne tre** og **Kolonne fire**:</span><span class="sxs-lookup"><span data-stu-id="44563-120">In the **Column three** and **Column four** sections:</span></span> 

- <span data-ttu-id="44563-121">Angiv en etiket til den tredje kolonne (f.eks. "Kontante udbetalinger") og fjerde kolonne (f.eks. "Overførsler mellem fonde").</span><span class="sxs-lookup"><span data-stu-id="44563-121">Specify a label for the third column (for example, "Cash disbursements") and fourth column (for example, "Interfund transfers").</span></span>
- <span data-ttu-id="44563-122">I begge kolonner kan du angive kontonumre for debet- og kredithovedkonti, kun debethovedkonti og kun kredithovedkonti.</span><span class="sxs-lookup"><span data-stu-id="44563-122">For both columns, specify account numbers for the debit and credit main accounts, debit-only main accounts, and credit-only main accounts.</span></span>

5. <span data-ttu-id="44563-123">I gruppesektionen **Kolonne fem** skal du angive en etiket for den femte kolonne (f.eks. ""Slutsaldo"").</span><span class="sxs-lookup"><span data-stu-id="44563-123">In the **Column five** group section, specify a label for the fifth column (for example, ""Ending balance"").</span></span> 

> [!NOTE]
> <span data-ttu-id="44563-124">Dynamics 365 Finance beregner automatisk en sum fra de konti, du har angivet, for de første fire kolonner: startsaldoen plus indbetalinger, minus kontante udbetalinger, minus overførsler mellem fonde.</span><span class="sxs-lookup"><span data-stu-id="44563-124">Dynamics 365 Finance automatically calculates a sum from the accounts you specified for the first four columns: Beginning balance plus cash receipts, minus cash disbursements, minus interfund transfers.</span></span>

6. <span data-ttu-id="44563-125">I sektionerne **Kolonne seks** og **Kolonne syv**:</span><span class="sxs-lookup"><span data-stu-id="44563-125">In the **Column six** and **Column seven** sections:</span></span> 

- <span data-ttu-id="44563-126">Angiv en etiket for kolonne seks (f.eks. Generelle budgetreservationer eller Behæftelser") og kolonne syv (f.eks. "Budgetreservationer").</span><span class="sxs-lookup"><span data-stu-id="44563-126">Specify a label for column six (for example, General budget reservations or Encumbrances") and column seven (for example, "Pre-encumbrances").</span></span>
- <span data-ttu-id="44563-127">I begge kolonner kan du angive kontonumre for **Debet- og kredithovedkonti**, **Kun debethovedkonti** og **Kun kredithovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="44563-127">For both columns, specify account numbers for the **Debit and credit main accounts**, **Debit-only main accounts**, and **Credit-only main accounts**.</span></span>

7. <span data-ttu-id="44563-128">Angiv en kolonneetiket i sektionen **Kolonne otte** (f.eks. "Ikke-behæftet saldo").</span><span class="sxs-lookup"><span data-stu-id="44563-128">In the **Column eight** section, specify a column label (for example, "Unencumbered balance").</span></span> 

> [!NOTE]
> <span data-ttu-id="44563-129">Dynamics 365 Finance beregner automatisk et resultat fra de konti, du har angivet for kolonne fem til syv: slutsaldo minus behæftelser, minus budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="44563-129">Dynamics 365 Finance automatically calculates a result from the accounts you specified for columns five through seven: Ending balance minus Encumbrances, minus Pre-encumbrances.</span></span>

8. <span data-ttu-id="44563-130">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="44563-130">Click **Save**.</span></span>

## <a name="running-the-inquiry"></a><span data-ttu-id="44563-131">Kørsel af forespørgslen</span><span class="sxs-lookup"><span data-stu-id="44563-131">Running the inquiry</span></span>

1. <span data-ttu-id="44563-132">Gå til **Finans** > **Forespørgsler og rapporter** > **Likviditet**.</span><span class="sxs-lookup"><span data-stu-id="44563-132">Go to **General ledger** > **Inquiries and reports** > **Cash position**.</span></span>
2. <span data-ttu-id="44563-133">I sektionen **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="44563-133">In the **Parameters** section:</span></span> 

- <span data-ttu-id="44563-134">Vælg **Datointerval** som kode eller **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="44563-134">Select the **Date interval** code, or the **From date** and **To date**.</span></span>
- <span data-ttu-id="44563-135">Vælg **Økonomisk dimensionsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="44563-135">Select the **Financial dimension set**.</span></span>
- <span data-ttu-id="44563-136">Vælg **Beregn saldi** for at køre forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="44563-136">Select **Calculate balances** to run the inquiry.</span></span>

<span data-ttu-id="44563-137">Valgfri:</span><span class="sxs-lookup"><span data-stu-id="44563-137">Optional:</span></span> 

- <span data-ttu-id="44563-138">Indstil **Undertryk konti med ene nuller** til **Ja** for at udelukke konti, der kun har nul saldi, fra forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="44563-138">Set the **Suppress accounts with all zeroes** option to **Yes** to exclude accounts that have zero balances from the inquiry.</span></span>
- <span data-ttu-id="44563-139">Indstil **Vis segmenter i separate kolonner** til **Ja** for at få vist kontonavnene for hver dimension som separate kolonner i gitteret.</span><span class="sxs-lookup"><span data-stu-id="44563-139">Set the **Display segments in separate columns** option to **Yes** to show the account names for each dimension as separate columns in the grid.</span></span>
- <span data-ttu-id="44563-140">Hvis du vil filtrere værdierne for en bestemt dimension, skal du vælge de ønskede dimensioner i felterne under feltet **Økonomiske dimensionsopsætninger**.</span><span class="sxs-lookup"><span data-stu-id="44563-140">If you want to filter the values for a specific dimension selected, select the dimensions you want in the fields below the **Financial dimension set** field.</span></span> <span data-ttu-id="44563-141">De valg, du skal foretage, afhænger af, hvilken økonomisk dimensionsopsætning du har valgt.</span><span class="sxs-lookup"><span data-stu-id="44563-141">The choices you have to select from depend on which financial dimension set you selected.</span></span>

