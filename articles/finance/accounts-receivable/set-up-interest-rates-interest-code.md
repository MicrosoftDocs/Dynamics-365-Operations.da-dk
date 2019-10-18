---
title: Angive rentesatser for en rentekode
description: Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188987"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="a6cc5-103">Angive rentesatser for en rentekode</span><span class="sxs-lookup"><span data-stu-id="a6cc5-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6cc5-104">Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="a6cc5-105">Du kan oprette en enkelt rentekode og anvende den på flere debitorposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="a6cc5-106">Når oplysningerne om rentekoden ændres, implementeres ændringerne automatisk i forbindelse med nye transaktioner for alle funktioner, der bruger koden.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="a6cc5-107">Du kan oprette to typer af satser for hver rentekode:</span><span class="sxs-lookup"><span data-stu-id="a6cc5-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="a6cc5-108">Satser for renteindtægter − Repræsentere indtægter, der er opnået ved opkrævning af renter på fakturaer eller rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="a6cc5-109">Satser for rentebetalinger − Repræsenterer en omkostning, der betales for renter på kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="a6cc5-110">Begge typer kan findes på samme tid og i samme rentekode.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="a6cc5-111">Rentesatser kan være baseret på tre beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="a6cc5-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="a6cc5-112">Rente efter procent.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-112">Interest by percentage.</span></span>
-   <span data-ttu-id="a6cc5-113">Rente efter beløb.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-113">Interest by amount.</span></span>
-   <span data-ttu-id="a6cc5-114">Rente efter interval, der resulterer i en enkelt procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="a6cc5-115">Når en rentekode bruges til at beregne renter, oprettes en separat rentenota for hver rentesats, der er gældende på det tidspunkt, hvor betalingen har overskredet forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="a6cc5-116">Du bruger fanen **Indtægter** på siden **Rentekode** til at angive rentesatser for renter, du tjener ved opkrævning af renter.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="a6cc5-117">Brug fanen **Betalinger** til at oprette rentesatser for den rente, du betaler.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="a6cc5-118">Rentesatser baseret på en procentdel</span><span class="sxs-lookup"><span data-stu-id="a6cc5-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="a6cc5-119">Du kan oprette rentesatser, der beregner en angivet procentdel.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="a6cc5-120">Rentebeløb, der gælder for alle valutaer.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="a6cc5-121">Valgfri rentebeløbsgrænser kan angives.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="a6cc5-122"><strong>Procent</strong> vælges\*\* <strong>i feltet \*\*Beregn renten på baggrund af</strong> på siden <strong>Konfigurer rentekoder</strong>.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="a6cc5-123">Hvis du f.eks. vil oprette en rentekode, der opkræver 5 procent rente for hver to måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 2 i feltet **Beregn rente hver** og vælge **Måned**.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="a6cc5-124">Rentesatser baseret på beløb</span><span class="sxs-lookup"><span data-stu-id="a6cc5-124">Interest rates based on amounts</span></span>
<span data-ttu-id="a6cc5-125">Du kan oprette rentesatser, der beregner et bestemt beløb pr. valuta.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="a6cc5-126">Der angives et rentebeløb for hver valuta i rentekoden.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="a6cc5-127">Valgfri rentebeløbsgrænser kan angives.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="a6cc5-128">**Beløb** vælges i feltet **Beregn rente på baggrund af** på siden **Konfigurer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="a6cc5-129">Hvis du f.eks. vil oprette en rentekode, der opkræver en rente på 25,00 for hver 20 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 20 i feltet **Beregn rente hver** og vælge **Dag**.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="a6cc5-130">Rentesatser baseret på intervaller</span><span class="sxs-lookup"><span data-stu-id="a6cc5-130">Interest rates based on ranges</span></span>
<span data-ttu-id="a6cc5-131">Du kan oprette rentesatser, der varierer afhængigt af det forfaldne beløb, antallet dage, betalingen er forsinket, eller antallet af måneder, betalingen er forsinket.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="a6cc5-132">Du kan bruge fanen **Overskud efter valuta** til at angive indstillinger for din rente for hver valuta.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="a6cc5-133">Det er også der, hvor du kan definere området.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="a6cc5-134">Brug knappen **Afgrænsninger** for at tilføje linjer, der repræsenterer de afgrænsninger, du vil konfigurere.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="a6cc5-135">Værdien **Fra** repræsenterer starten af afgrænsningen, og tallet **Renteværdi** repræsenterer en procentdel eller et beløb, afhængigt af valget i feltet **Beregn renter på baggrund af** på siden **Konfigurer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="a6cc5-136">Eksempel 1: Renter efter interval = beløb</span><span class="sxs-lookup"><span data-stu-id="a6cc5-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="a6cc5-137">Du har oprettet en rentekode, der opkræver rente én gang for hver tre måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="a6cc5-138">Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise beløbsintervaller.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="a6cc5-139">Renteværdien vil være 1 procent for fakturabeløb op til 1.000,00, 2 procent for beløb fra 1,001.00 til 5,000.00, og 3 procent for beløb, der er større end 5,000.00.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="a6cc5-140">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="a6cc5-141">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-141">**Field name**</span></span>                  | <span data-ttu-id="a6cc5-142">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="a6cc5-143">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-143">**Interest code**</span></span>               | <span data-ttu-id="a6cc5-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="a6cc5-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="a6cc5-145">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-145">**Calculate interest every**</span></span>    | <span data-ttu-id="a6cc5-146">3/Måned</span><span class="sxs-lookup"><span data-stu-id="a6cc5-146">3/Month</span></span>         |
| <span data-ttu-id="a6cc5-147">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-147">**Interest by range**</span></span>           | <span data-ttu-id="a6cc5-148">Beløb</span><span class="sxs-lookup"><span data-stu-id="a6cc5-148">Amount</span></span>          |
| <span data-ttu-id="a6cc5-149">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-149">**Calculate interest based on**</span></span> | <span data-ttu-id="a6cc5-150">Procentdel</span><span class="sxs-lookup"><span data-stu-id="a6cc5-150">Percentage</span></span>      |

<span data-ttu-id="a6cc5-151">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="a6cc5-152">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-152">**From value**</span></span> | <span data-ttu-id="a6cc5-153">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="a6cc5-154">0</span><span class="sxs-lookup"><span data-stu-id="a6cc5-154">0</span></span>              | <span data-ttu-id="a6cc5-155">1</span><span class="sxs-lookup"><span data-stu-id="a6cc5-155">1</span></span>                  |
| <span data-ttu-id="a6cc5-156">1,001</span><span class="sxs-lookup"><span data-stu-id="a6cc5-156">1,001</span></span>          | <span data-ttu-id="a6cc5-157">2</span><span class="sxs-lookup"><span data-stu-id="a6cc5-157">2</span></span>                  |
| <span data-ttu-id="a6cc5-158">5,001</span><span class="sxs-lookup"><span data-stu-id="a6cc5-158">5,001</span></span>          | <span data-ttu-id="a6cc5-159">3</span><span class="sxs-lookup"><span data-stu-id="a6cc5-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="a6cc5-160">Eksempel 2: Renter efter interval = dage</span><span class="sxs-lookup"><span data-stu-id="a6cc5-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="a6cc5-161">Du har oprettet en rentekode, der opkræver rente én gang for hver 15 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="a6cc5-162">Du vil basere beregningen på en beløbsmæssig renteværdi i henhold til de trinvise dagsintervaller.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="a6cc5-163">Renteværdien vil være 10,00 pr. 15 dage i de første 60 dage, 15,00 pr. 15 dag i dagene 61-90 og 20,00 pr. 15 dage fra dag 91 og efter.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="a6cc5-164">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="a6cc5-165">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-165">**Field name**</span></span>                  | <span data-ttu-id="a6cc5-166">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="a6cc5-167">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-167">**Interest code**</span></span>               | <span data-ttu-id="a6cc5-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="a6cc5-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="a6cc5-169">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-169">**Calculate interest every**</span></span>    | <span data-ttu-id="a6cc5-170">15/Dag</span><span class="sxs-lookup"><span data-stu-id="a6cc5-170">15/Day</span></span>          |
| <span data-ttu-id="a6cc5-171">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-171">**Interest by range**</span></span>           | <span data-ttu-id="a6cc5-172">Dage</span><span class="sxs-lookup"><span data-stu-id="a6cc5-172">Days</span></span>            |
| <span data-ttu-id="a6cc5-173">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-173">**Calculate interest based on**</span></span> | <span data-ttu-id="a6cc5-174">Beløb</span><span class="sxs-lookup"><span data-stu-id="a6cc5-174">Amount</span></span>          |

<span data-ttu-id="a6cc5-175">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="a6cc5-176">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-176">**From value**</span></span> | <span data-ttu-id="a6cc5-177">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="a6cc5-178">0</span><span class="sxs-lookup"><span data-stu-id="a6cc5-178">0</span></span>              | <span data-ttu-id="a6cc5-179">10</span><span class="sxs-lookup"><span data-stu-id="a6cc5-179">10</span></span>                 |
| <span data-ttu-id="a6cc5-180">61</span><span class="sxs-lookup"><span data-stu-id="a6cc5-180">61</span></span>             | <span data-ttu-id="a6cc5-181">15</span><span class="sxs-lookup"><span data-stu-id="a6cc5-181">15</span></span>                 |
| <span data-ttu-id="a6cc5-182">91</span><span class="sxs-lookup"><span data-stu-id="a6cc5-182">91</span></span>             | <span data-ttu-id="a6cc5-183">20</span><span class="sxs-lookup"><span data-stu-id="a6cc5-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="a6cc5-184">Eksempel 3: Renter efter interval = måneder</span><span class="sxs-lookup"><span data-stu-id="a6cc5-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="a6cc5-185">Du har oprettet en rentekode, der opkræver rente én gang for hver måned, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="a6cc5-186">Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise månedsintervaller.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="a6cc5-187">Renteværdien vil være 1,5 procent pr. måned for de første tre måneder, 2,0 procent pr. måned for de næste tre måneder og 2,5 procent pr. måned for hver måned ud over de første seks måneder.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="a6cc5-188">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="a6cc5-189">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-189">**Field name**</span></span>                  | <span data-ttu-id="a6cc5-190">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="a6cc5-191">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-191">**Interest code**</span></span>               | <span data-ttu-id="a6cc5-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="a6cc5-192">1M%ByMth</span></span>        |
| <span data-ttu-id="a6cc5-193">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-193">**Calculate interest every**</span></span>    | <span data-ttu-id="a6cc5-194">1/Måned</span><span class="sxs-lookup"><span data-stu-id="a6cc5-194">1/Month</span></span>         |
| <span data-ttu-id="a6cc5-195">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-195">**Interest by range**</span></span>           | <span data-ttu-id="a6cc5-196">Måneder</span><span class="sxs-lookup"><span data-stu-id="a6cc5-196">Months</span></span>          |
| <span data-ttu-id="a6cc5-197">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-197">**Calculate interest based on**</span></span> | <span data-ttu-id="a6cc5-198">Procentdel</span><span class="sxs-lookup"><span data-stu-id="a6cc5-198">Percentage</span></span>      |

<span data-ttu-id="a6cc5-199">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="a6cc5-200">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-200">**From value**</span></span> | <span data-ttu-id="a6cc5-201">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="a6cc5-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="a6cc5-202">0</span><span class="sxs-lookup"><span data-stu-id="a6cc5-202">0</span></span>              | <span data-ttu-id="a6cc5-203">1.5</span><span class="sxs-lookup"><span data-stu-id="a6cc5-203">1.5</span></span>                |
| <span data-ttu-id="a6cc5-204">4</span><span class="sxs-lookup"><span data-stu-id="a6cc5-204">4</span></span>              | <span data-ttu-id="a6cc5-205">2</span><span class="sxs-lookup"><span data-stu-id="a6cc5-205">2</span></span>                  |
| <span data-ttu-id="a6cc5-206">7</span><span class="sxs-lookup"><span data-stu-id="a6cc5-206">7</span></span>              | <span data-ttu-id="a6cc5-207">2,5</span><span class="sxs-lookup"><span data-stu-id="a6cc5-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="a6cc5-208">Nye versioner</span><span class="sxs-lookup"><span data-stu-id="a6cc5-208">New versions</span></span>
<span data-ttu-id="a6cc5-209">Rentekoder er for gældende dato.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-209">Interest codes are date effective.</span></span> <span data-ttu-id="a6cc5-210">Hvis du vil ændre renten, kan du oprette en **ny version**, der er gældende for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="a6cc5-211">For at få vist forskellige versioner kan du bruge menupunktet **Pr. dato** til at vælge skæringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="a6cc5-212">Du kan også vælge **Vis alle poster** for at få vist alle rentekoderne på siden.</span><span class="sxs-lookup"><span data-stu-id="a6cc5-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



