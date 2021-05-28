---
title: Ydeevne for momsberegning påvirker transaktioner
description: Dette emne indeholder fejlfindingsoplysninger, der vedrører momsberegningens ydeevne og indvirkning på transaktioner.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020133"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="64637-103">Ydeevne for momsberegning påvirker transaktioner</span><span class="sxs-lookup"><span data-stu-id="64637-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64637-104">Nogle gange påvirkes en transaktion af de problemer med ydeevnen, der er i momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="64637-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="64637-105">Du kan udføre fejlfinding af dette problem ved at følge trinnene i følgende afsnit efter behov.</span><span class="sxs-lookup"><span data-stu-id="64637-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="64637-106">Gennemse transaktionslinjeantallet</span><span class="sxs-lookup"><span data-stu-id="64637-106">Review the transaction line count</span></span>

<span data-ttu-id="64637-107">Afgør, om transaktionen indeholder et stort antal linjer (f.eks. mere end flere hundreder).</span><span class="sxs-lookup"><span data-stu-id="64637-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="64637-108">Hvis det ikke er tilfældet, skal du gå videre til næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="64637-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="64637-109">Hvis transaktionen ikke indeholder flere hundrede linjer, skal du udskyde momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="64637-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="64637-110">Du kan finde flere oplysninger i [Aktivere forsinket momsberegning for kladder](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="64637-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="64637-111">Derefter kan du afgøre, om nogen af følgende forhold er aktuelle:</span><span class="sxs-lookup"><span data-stu-id="64637-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="64637-112">Der er importtransaktioner fra store filer.</span><span class="sxs-lookup"><span data-stu-id="64637-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="64637-113">Flere sessioner behandler samme momsberegning for transaktionen samtidigt.</span><span class="sxs-lookup"><span data-stu-id="64637-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="64637-114">Transaktionen har flere linjer, og visningerne opdateres i realtid.</span><span class="sxs-lookup"><span data-stu-id="64637-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="64637-115">Feltet **Beregnet momsbeløb** på siden **Finanskladde** opdateres f.eks. i realtid, når en linjes felter bliver ændret.</span><span class="sxs-lookup"><span data-stu-id="64637-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="64637-116">[![Feltet Beregnet momsbeløb på kladdens bilagsside](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="64637-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="64637-117">Hvis nogen af disse forhold er til stede, skal du udskyde momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="64637-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="64637-118">Gennemse kaldstakken</span><span class="sxs-lookup"><span data-stu-id="64637-118">Review the call stack</span></span>

<span data-ttu-id="64637-119">Gennemse kaldstakken for at finde ud af, om momsberegningen er kaldt flere gange.</span><span class="sxs-lookup"><span data-stu-id="64637-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="64637-120">Hvis det ikke er tilfældet, skal du gå videre til næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="64637-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="64637-121">Hvis kaldstakken er kaldt flere gange, skal du benytte følgende fremgangsmåde for at reducere momsberegningstiderne.</span><span class="sxs-lookup"><span data-stu-id="64637-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="64637-122">Hvis kladden har taget højde for transaktionen, skal du udskyde momsberegningen.</span><span class="sxs-lookup"><span data-stu-id="64637-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="64637-123">Du kan finde flere oplysninger i [Aktivere forsinket momsberegning for kladder](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="64637-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="64637-124">Hvis transaktionen er en indkøbsordre, og programversionen er senere end 10.0.15, kan du udskyde momsberegningen indtil den endelige beregning ved at aktivere flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="64637-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="64637-125">Gennemse kaldstakkens tidslinje</span><span class="sxs-lookup"><span data-stu-id="64637-125">Review the call stack timeline</span></span>

<span data-ttu-id="64637-126">Gennemse kaldstakkens tidslinje for at finde ud af, om der findes følgende problemer.</span><span class="sxs-lookup"><span data-stu-id="64637-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="64637-127">Hvis det er tilfældet, skal du aktivere flighting for **TaxUncommittedDoIsolateScopeFlighting** for at rette problemet.</span><span class="sxs-lookup"><span data-stu-id="64637-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="64637-128">Transaktionen bevirker, at systemet holder op med at svare, indtil sessionen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="64637-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="64637-129">Derfor kan transaktionen ikke beregne momsresultatet.</span><span class="sxs-lookup"><span data-stu-id="64637-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="64637-130">I følgende illustration vises meddelelsen "Session afsluttet", som du modtager.</span><span class="sxs-lookup"><span data-stu-id="64637-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="64637-131">[![Meddelelsen Session afsluttet](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="64637-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="64637-132">Metoderne for **TaxUncommitted** tager længere tid end andre metoder.</span><span class="sxs-lookup"><span data-stu-id="64637-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="64637-133">I følgende illustration tager metoden **TaxUncommitted::updateTaxUncommitted()** f.eks. 43.347,42 sekunder, mens andre metoder tager 0,09 sekunder.</span><span class="sxs-lookup"><span data-stu-id="64637-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="64637-134">[![Metodevarigheder](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="64637-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="64637-135">Tilpasning og kald af momsberegning</span><span class="sxs-lookup"><span data-stu-id="64637-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="64637-136">Når du tilpasser, må du ikke kalde momsberegningen ved metoden **insert()** eller **update()** for hver linje.</span><span class="sxs-lookup"><span data-stu-id="64637-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="64637-137">Momsberegning skal kaldes på transaktionsniveau.</span><span class="sxs-lookup"><span data-stu-id="64637-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="64637-138">Afgøre, om der findes tilpasninger</span><span class="sxs-lookup"><span data-stu-id="64637-138">Determine whether customization exists</span></span>

<span data-ttu-id="64637-139">Hvis du har udført trinnene i de forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="64637-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="64637-140">Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="64637-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
