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
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-alpavk
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 450b59290eea6bf7460d4b239341203c13f2d1ba
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659038"
---
# <a name="cash-position-inquiry"></a><span data-ttu-id="151a8-103">Forespørgsel på likviditet</span><span class="sxs-lookup"><span data-stu-id="151a8-103">Cash position inquiry</span></span>
[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="151a8-104">Med forespørgslen **Likviditet** kan du fastlægge den tilsvarende likviditet for økonomiske dimensionssæt, der indeholder selvafstemmende dimensioner.</span><span class="sxs-lookup"><span data-stu-id="151a8-104">The **Cash position** inquiry allows you to determine the corresponding cash positions for financial dimension sets that contain self-balancing dimensions.</span></span> <span data-ttu-id="151a8-105">I forespørgslen vises startkassesaldoen og resultatet af tilførte kasseboner, subtraktion af kontante udbetalinger og subtraktion af overførsler mellem fonde for at komme til en slutsaldo.</span><span class="sxs-lookup"><span data-stu-id="151a8-105">The inquiry shows the beginning cash balance, and the effect of the addition of cash receipts, the subtraction of cash disbursements, and the subtraction of interfund transfers to arrive at an ending balance.</span></span> <span data-ttu-id="151a8-106">Derefter trækkes de generelle budgetreservationer, behæftelser eller budgetreservationer fra slutsaldoen for at få en ikke-behæftet saldo.</span><span class="sxs-lookup"><span data-stu-id="151a8-106">Then, from the ending balance, general budget reservations, encumbrances, or pre-encumbrances are subtracted to arrive at an unencumbered balance.</span></span>

<span data-ttu-id="151a8-107">Denne forespørgsel er entydig, da den giver brugerne mulighed for at tilpasse terminologien for kolonnenavne og de hovedkonti, der bruges til at aflede beløbene for kolonnerne.</span><span class="sxs-lookup"><span data-stu-id="151a8-107">This inquiry is unique in that it allows users to customize the terminology for column names and for the main accounts that are used to derive amounts for the columns.</span></span> <span data-ttu-id="151a8-108">På siden **Likviditetsparametre** er de kolonner, der vises i forespørgslen, nummereret startende med kolonnen længst til venstre som kolonne ét.</span><span class="sxs-lookup"><span data-stu-id="151a8-108">On the **Cash position parameters** page, the columns that appear in the inquiry are numbered starting with the left-most data column as column one.</span></span>

## <a name="cash-position-inquiry-setup"></a><span data-ttu-id="151a8-109">Opsætning af forespørgsel på likviditet</span><span class="sxs-lookup"><span data-stu-id="151a8-109">Cash position inquiry setup</span></span>

1. <span data-ttu-id="151a8-110">Gå til **Finans** > **Opsætning Finans** > **Likviditetsparametre**.</span><span class="sxs-lookup"><span data-stu-id="151a8-110">Go to **General ledger** > **Ledger setup** > **Cash position parameters**.</span></span>
2. <span data-ttu-id="151a8-111">På siden **Likviditetsparametre** i sektionen **Kolonne ét**:</span><span class="sxs-lookup"><span data-stu-id="151a8-111">In the **Cash position parameters** page, in the **Column one** section:</span></span>

- <span data-ttu-id="151a8-112">I feltet **Kolonnenavn** skal du skrive en etiket, der skal bruges som overskrift til den første kolonne i forespørgslen (f.eks. "Startsaldo").</span><span class="sxs-lookup"><span data-stu-id="151a8-112">In the **Column name** field, type a label to use as the header for the inquiry’s first column (for example, "Beginning balance").</span></span>
- <span data-ttu-id="151a8-113">I feltet **Startsaldo på hovedkonti** skal du vælge den eller de konti, du vil referere til i forbindelse med forespørgsler på startsaldoen.</span><span class="sxs-lookup"><span data-stu-id="151a8-113">In the **Opening balance main accounts** field, select the account(s) that you want to reference for inquiring on the opening balance.</span></span>

3. <span data-ttu-id="151a8-114">I sektionen **Kolonne to**:</span><span class="sxs-lookup"><span data-stu-id="151a8-114">In the **Column two** section:</span></span> 

- <span data-ttu-id="151a8-115">Angiv en etiket til den anden kolonne i forespørgslen (f.eks. "Indbetalinger").</span><span class="sxs-lookup"><span data-stu-id="151a8-115">Specify a label for the second column in the inquiry (for example, "Cash receipts").</span></span>
- <span data-ttu-id="151a8-116">På listen **Debet- og kredit hovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debet- og kredittransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="151a8-116">In the **Debit and credit main accounts** list, select the main accounts from which to use only the sum of all debit and credit transaction amounts for the inquiry's data.</span></span> 

> [!NOTE]
> <span data-ttu-id="151a8-117">Forespørgslen tilføjer debet- og kreditkontiene nettobeløb plus debetbeløb og kreditbeløb fra hovedkontiene i de andre felter i gruppen.</span><span class="sxs-lookup"><span data-stu-id="151a8-117">The inquiry will add the net of the debit and credit accounts plus the debit amount and credit amounts from the main accounts in the other fields in the group.</span></span>

- <span data-ttu-id="151a8-118">På listen **Kun debethovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle debettransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="151a8-118">In the **Debit-only main accounts** list, select the main accounts from which to use only the sum of all debit transaction amounts for the inquiry's data.</span></span>
- <span data-ttu-id="151a8-119">På listen **Kun kredithovedkonti** skal du vælge de hovedkonti, hvorfra der kun skal bruges summen af alle kredittransaktioner for forespørgselsdataene.</span><span class="sxs-lookup"><span data-stu-id="151a8-119">In the **Credit-only main accounts** list, select the main accounts from which to use only the sum of all credit transaction amounts for the inquiry's data.</span></span>

4. <span data-ttu-id="151a8-120">I sektionerne **Kolonne tre** og **Kolonne fire**:</span><span class="sxs-lookup"><span data-stu-id="151a8-120">In the **Column three** and **Column four** sections:</span></span> 

- <span data-ttu-id="151a8-121">Angiv en etiket til den tredje kolonne (f.eks. "Kontante udbetalinger") og fjerde kolonne (f.eks. "Overførsler mellem fonde").</span><span class="sxs-lookup"><span data-stu-id="151a8-121">Specify a label for the third column (for example, "Cash disbursements") and fourth column (for example, "Interfund transfers").</span></span>
- <span data-ttu-id="151a8-122">I begge kolonner kan du angive kontonumre for debet- og kredithovedkonti, kun debethovedkonti og kun kredithovedkonti.</span><span class="sxs-lookup"><span data-stu-id="151a8-122">For both columns, specify account numbers for the debit and credit main accounts, debit-only main accounts, and credit-only main accounts.</span></span>

5. <span data-ttu-id="151a8-123">I gruppesektionen **Kolonne fem** skal du angive en etiket for den femte kolonne (f.eks. ""Slutsaldo"").</span><span class="sxs-lookup"><span data-stu-id="151a8-123">In the **Column five** groupsection, specify a label for the fifth column (for example, ""Ending balance"").</span></span> 

> [!NOTE]
> <span data-ttu-id="151a8-124">Dynamics 365 Finance beregner automatisk en sum fra de konti, du har angivet, for de første fire kolonner: startsaldoen plus indbetalinger, minus kontante udbetalinger, minus overførsler mellem fonde.</span><span class="sxs-lookup"><span data-stu-id="151a8-124">Dynamics 365 Finance automatically calculates a sum from the accounts you specified for the first four columns: Beginning balance plus cash receipts, minus cash disbursements, minus interfund transfers.</span></span>

6. <span data-ttu-id="151a8-125">I sektionerne **Kolonne seks** og **Kolonne syv**:</span><span class="sxs-lookup"><span data-stu-id="151a8-125">In the **Column six** and **Column seven** sections:</span></span> 

- <span data-ttu-id="151a8-126">Angiv en etiket for kolonne seks (f.eks. Generelle budgetreservationer eller Behæftelser") og kolonne syv (f.eks."Budgetreservationer").</span><span class="sxs-lookup"><span data-stu-id="151a8-126">Specify a label for column six (for example, General budget reservations or Encunbrances") and column seven (for example, "Pre-encumbrances").</span></span>
- <span data-ttu-id="151a8-127">I begge kolonner kan du angive kontonumre for **Debet- og kredithovedkonti**, **Kun debethovedkonti** og **Kun kredithovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="151a8-127">For both columns, specify account numbers for the **Debit and credit main accounts**, **Debit-only main accounts**, and **Credit-only main accounts**.</span></span>

7. <span data-ttu-id="151a8-128">Angiv en kolonneetiket i sektionen **Kolonne otte** (f.eks. "Ikke-behæftet saldo").</span><span class="sxs-lookup"><span data-stu-id="151a8-128">In the **Column eight** section, specify a column label (for example, "Unencumbered balance").</span></span> 

> [!NOTE]
> <span data-ttu-id="151a8-129">Dynamics 365 Finance beregner automatisk et resultat fra de konti, du har angivet for kolonne fem til syv: slutsaldo minus behæftelser, minus budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="151a8-129">Dynamics 365 Finance automatically calculates a result from the accounts you specified for columns five through seven: Ending balance minus Encumbrances, minus Pre-encumbrances.</span></span>

8. <span data-ttu-id="151a8-130">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="151a8-130">Click **Save**.</span></span>

## <a name="running-the-inquiry"></a><span data-ttu-id="151a8-131">Kørsel af forespørgslen</span><span class="sxs-lookup"><span data-stu-id="151a8-131">Running the inquiry</span></span>

1. <span data-ttu-id="151a8-132">Gå til **Finans** > **Forespørgsler og rapporter** > **Likviditet**.</span><span class="sxs-lookup"><span data-stu-id="151a8-132">Go to **General ledger** > **Inqiuries and reports** > **Cash position**.</span></span>
2. <span data-ttu-id="151a8-133">I sektionen **Parametre**:</span><span class="sxs-lookup"><span data-stu-id="151a8-133">In the **Parameters** section:</span></span> 

- <span data-ttu-id="151a8-134">Vælg **Datointerval** som kode eller **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="151a8-134">Select the **Date interval** code, or the **From date** and **To date**.</span></span>
- <span data-ttu-id="151a8-135">Vælg **Økonomisk dimensionsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="151a8-135">Select the **Financial dimension set**.</span></span>
- <span data-ttu-id="151a8-136">Vælg **Beregn saldi** for at køre forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="151a8-136">Select **Calculate balances** to run the inquiry.</span></span>

<span data-ttu-id="151a8-137">Valgfri:</span><span class="sxs-lookup"><span data-stu-id="151a8-137">Optional:</span></span> 

- <span data-ttu-id="151a8-138">Indstil **Undertryk konti med ene nuller** til **Ja** for at udelukke konti, der kun har nul saldi, fra forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="151a8-138">Set the **Suppress accounts with all zeroes** option to **Yes** to exclude accounts that ahve all zero balances from the inquiry.</span></span>
- <span data-ttu-id="151a8-139">Indstil **Vis segmenter i separate kolonner** til **Ja** for at få vist kontonavnene for hver dimension som separate kolonner i gitteret.</span><span class="sxs-lookup"><span data-stu-id="151a8-139">Set the **Display segments in seperate columns** option to **Yes** to show the account names for each dimension as seperate columns in the grid.</span></span>
- <span data-ttu-id="151a8-140">Hvis du vil filtrere værdierne for en bestemt dimension, skal du vælge de ønskede dimensioner i felterne under feltet **Økonomiske dimensionsopsætninger**.</span><span class="sxs-lookup"><span data-stu-id="151a8-140">If you want to filter the values for a specific dimension selected, select the dimensions you want in the fields below the **Financial dimension set** field.</span></span> <span data-ttu-id="151a8-141">De valg, du skal foretage, afhænger af, hvilken økonomisk dimensionsopsætning du har valgt.</span><span class="sxs-lookup"><span data-stu-id="151a8-141">The choices you have to select from depend on which financial dimension set you selected.</span></span>

