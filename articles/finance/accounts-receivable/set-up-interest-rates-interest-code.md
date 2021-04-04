---
title: Angive rentesatser for en rentekode
description: Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d9ff856e34eb894c5d0ab5fe17c8e95f62fff57
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555359"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="fb036-103">Angive rentesatser for en rentekode</span><span class="sxs-lookup"><span data-stu-id="fb036-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb036-104">Rentekoder omfatter indstillinger, der bestemmer, hvornår der opkræves rente, og hvordan det beregnes på forfaldne konti.</span><span class="sxs-lookup"><span data-stu-id="fb036-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="fb036-105">Du kan oprette en enkelt rentekode og anvende den på flere debitorposteringsprofiler, faktureringskoder eller på bestemte fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="fb036-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="fb036-106">Når oplysningerne om rentekoden ændres, implementeres ændringerne automatisk i forbindelse med nye transaktioner for alle funktioner, der bruger koden.</span><span class="sxs-lookup"><span data-stu-id="fb036-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="fb036-107">Du kan oprette to typer af satser for hver rentekode:</span><span class="sxs-lookup"><span data-stu-id="fb036-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="fb036-108">Satser for renteindtægter − Repræsentere indtægter, der er opnået ved opkrævning af renter på fakturaer eller rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="fb036-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="fb036-109">Satser for rentebetalinger − Repræsenterer en omkostning, der betales for renter på kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="fb036-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="fb036-110">Begge typer kan findes på samme tid og i samme rentekode.</span><span class="sxs-lookup"><span data-stu-id="fb036-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="fb036-111">Rentesatser kan være baseret på tre beregningstyper:</span><span class="sxs-lookup"><span data-stu-id="fb036-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="fb036-112">Rente efter procent.</span><span class="sxs-lookup"><span data-stu-id="fb036-112">Interest by percentage.</span></span>
-   <span data-ttu-id="fb036-113">Rente efter beløb.</span><span class="sxs-lookup"><span data-stu-id="fb036-113">Interest by amount.</span></span>
-   <span data-ttu-id="fb036-114">Rente efter interval, der resulterer i en enkelt procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="fb036-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="fb036-115">Når en rentekode bruges til at beregne renter, oprettes en separat rentenota for hver rentesats, der er gældende på det tidspunkt, hvor betalingen har overskredet forfaldsdatoen.</span><span class="sxs-lookup"><span data-stu-id="fb036-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="fb036-116">Du bruger fanen **Indtægter** på siden **Rentekode** til at angive rentesatser for renter, du tjener ved opkrævning af renter.</span><span class="sxs-lookup"><span data-stu-id="fb036-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="fb036-117">Brug fanen **Betalinger** til at oprette rentesatser for den rente, du betaler.</span><span class="sxs-lookup"><span data-stu-id="fb036-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="fb036-118">Rentesatser baseret på en procentdel</span><span class="sxs-lookup"><span data-stu-id="fb036-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="fb036-119">Du kan oprette rentesatser, der beregner en angivet procentdel.</span><span class="sxs-lookup"><span data-stu-id="fb036-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="fb036-120">Rentebeløb, der gælder for alle valutaer.</span><span class="sxs-lookup"><span data-stu-id="fb036-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="fb036-121">Valgfri rentebeløbsgrænser kan angives.</span><span class="sxs-lookup"><span data-stu-id="fb036-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="fb036-122">**Procent** vælges i feltet **Beregn renten på baggrund af** på siden **Konfigurer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="fb036-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="fb036-123">Hvis du f.eks. vil oprette en rentekode, der opkræver 5 procent rente for hver to måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 2 i feltet **Beregn rente hver** og vælge **Måned**.</span><span class="sxs-lookup"><span data-stu-id="fb036-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="fb036-124">Den nye algoritme til beregning af rentenotaer tilføjes ved hjælp af funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="fb036-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="fb036-125">Hvis du vil bruge denne algoritme, skal du aktivere funktionen **(GBL) Tillad beregning af rente pr. dag som en årsprocent divideret med funktionen 365**.</span><span class="sxs-lookup"><span data-stu-id="fb036-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="fb036-126">Du kan finde flere oplysninger om aktivering af funktionen under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb036-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="fb036-127">Formlen til beregning af rentenotabeløbet er:</span><span class="sxs-lookup"><span data-stu-id="fb036-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="fb036-128">Rentenotabeløb = Skyldige beløb \* Årligt rentebeløb % / 365 \* Antal dage for sent</span><span class="sxs-lookup"><span data-stu-id="fb036-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="fb036-129">Denne funktion er tilgængelig i version 10.0.18 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="fb036-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="fb036-130">Rentesatser baseret på beløb</span><span class="sxs-lookup"><span data-stu-id="fb036-130">Interest rates based on amounts</span></span>
<span data-ttu-id="fb036-131">Du kan oprette rentesatser, der beregner et bestemt beløb pr. valuta.</span><span class="sxs-lookup"><span data-stu-id="fb036-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="fb036-132">Der angives et rentebeløb for hver valuta i rentekoden.</span><span class="sxs-lookup"><span data-stu-id="fb036-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="fb036-133">Valgfri rentebeløbsgrænser kan angives.</span><span class="sxs-lookup"><span data-stu-id="fb036-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="fb036-134">**Beløb** vælges i feltet **Beregn rente på baggrund af** på siden **Konfigurer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="fb036-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="fb036-135">Hvis du f.eks. vil oprette en rentekode, der opkræver en rente på 25,00 for hver 20 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato, skal du skrive 20 i feltet **Beregn rente hver** og vælge **Dag**.</span><span class="sxs-lookup"><span data-stu-id="fb036-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="fb036-136">Rentesatser baseret på intervaller</span><span class="sxs-lookup"><span data-stu-id="fb036-136">Interest rates based on ranges</span></span>
<span data-ttu-id="fb036-137">Du kan oprette rentesatser, der varierer afhængigt af det forfaldne beløb, antallet dage, betalingen er forsinket, eller antallet af måneder, betalingen er forsinket.</span><span class="sxs-lookup"><span data-stu-id="fb036-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="fb036-138">Du kan bruge fanen **Overskud efter valuta** til at angive indstillinger for din rente for hver valuta.</span><span class="sxs-lookup"><span data-stu-id="fb036-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="fb036-139">Det er også der, hvor du kan definere området.</span><span class="sxs-lookup"><span data-stu-id="fb036-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="fb036-140">Brug knappen **Afgrænsninger** for at tilføje linjer, der repræsenterer de afgrænsninger, du vil konfigurere.</span><span class="sxs-lookup"><span data-stu-id="fb036-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="fb036-141">Værdien **Fra** repræsenterer starten af afgrænsningen, og tallet **Renteværdi** repræsenterer en procentdel eller et beløb, afhængigt af valget i feltet **Beregn renter på baggrund af** på siden **Konfigurer rentekoder**.</span><span class="sxs-lookup"><span data-stu-id="fb036-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="fb036-142">Eksempel 1: Renter efter interval = beløb</span><span class="sxs-lookup"><span data-stu-id="fb036-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="fb036-143">Du har oprettet en rentekode, der opkræver rente én gang for hver tre måneder, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="fb036-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fb036-144">Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise beløbsintervaller.</span><span class="sxs-lookup"><span data-stu-id="fb036-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="fb036-145">Renteværdien vil være 1 procent for fakturabeløb op til 1.000,00, 2 procent for beløb fra 1,001.00 til 5,000.00, og 3 procent for beløb, der er større end 5,000.00.</span><span class="sxs-lookup"><span data-stu-id="fb036-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="fb036-146">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fb036-147">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="fb036-147">**Field name**</span></span>                  | <span data-ttu-id="fb036-148">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fb036-149">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="fb036-149">**Interest code**</span></span>               | <span data-ttu-id="fb036-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="fb036-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="fb036-151">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="fb036-151">**Calculate interest every**</span></span>    | <span data-ttu-id="fb036-152">3/Måned</span><span class="sxs-lookup"><span data-stu-id="fb036-152">3/Month</span></span>         |
| <span data-ttu-id="fb036-153">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="fb036-153">**Interest by range**</span></span>           | <span data-ttu-id="fb036-154">Beløb</span><span class="sxs-lookup"><span data-stu-id="fb036-154">Amount</span></span>          |
| <span data-ttu-id="fb036-155">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="fb036-155">**Calculate interest based on**</span></span> | <span data-ttu-id="fb036-156">Procentdel</span><span class="sxs-lookup"><span data-stu-id="fb036-156">Percentage</span></span>      |

<span data-ttu-id="fb036-157">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="fb036-158">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-158">**From value**</span></span> | <span data-ttu-id="fb036-159">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fb036-160">0</span><span class="sxs-lookup"><span data-stu-id="fb036-160">0</span></span>              | <span data-ttu-id="fb036-161">1</span><span class="sxs-lookup"><span data-stu-id="fb036-161">1</span></span>                  |
| <span data-ttu-id="fb036-162">1,001</span><span class="sxs-lookup"><span data-stu-id="fb036-162">1,001</span></span>          | <span data-ttu-id="fb036-163">2</span><span class="sxs-lookup"><span data-stu-id="fb036-163">2</span></span>                  |
| <span data-ttu-id="fb036-164">5,001</span><span class="sxs-lookup"><span data-stu-id="fb036-164">5,001</span></span>          | <span data-ttu-id="fb036-165">3</span><span class="sxs-lookup"><span data-stu-id="fb036-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="fb036-166">Eksempel 2: Renter efter interval = dage</span><span class="sxs-lookup"><span data-stu-id="fb036-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="fb036-167">Du har oprettet en rentekode, der opkræver rente én gang for hver 15 dage, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="fb036-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fb036-168">Du vil basere beregningen på en beløbsmæssig renteværdi i henhold til de trinvise dagsintervaller.</span><span class="sxs-lookup"><span data-stu-id="fb036-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="fb036-169">Renteværdien vil være 10,00 pr. 15 dage i de første 60 dage, 15,00 pr. 15 dag i dagene 61-90 og 20,00 pr. 15 dage fra dag 91 og efter.</span><span class="sxs-lookup"><span data-stu-id="fb036-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="fb036-170">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fb036-171">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="fb036-171">**Field name**</span></span>                  | <span data-ttu-id="fb036-172">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fb036-173">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="fb036-173">**Interest code**</span></span>               | <span data-ttu-id="fb036-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="fb036-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="fb036-175">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="fb036-175">**Calculate interest every**</span></span>    | <span data-ttu-id="fb036-176">15/Dag</span><span class="sxs-lookup"><span data-stu-id="fb036-176">15/Day</span></span>          |
| <span data-ttu-id="fb036-177">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="fb036-177">**Interest by range**</span></span>           | <span data-ttu-id="fb036-178">Dage</span><span class="sxs-lookup"><span data-stu-id="fb036-178">Days</span></span>            |
| <span data-ttu-id="fb036-179">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="fb036-179">**Calculate interest based on**</span></span> | <span data-ttu-id="fb036-180">Beløb</span><span class="sxs-lookup"><span data-stu-id="fb036-180">Amount</span></span>          |

<span data-ttu-id="fb036-181">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="fb036-182">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-182">**From value**</span></span> | <span data-ttu-id="fb036-183">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fb036-184">0</span><span class="sxs-lookup"><span data-stu-id="fb036-184">0</span></span>              | <span data-ttu-id="fb036-185">10</span><span class="sxs-lookup"><span data-stu-id="fb036-185">10</span></span>                 |
| <span data-ttu-id="fb036-186">61</span><span class="sxs-lookup"><span data-stu-id="fb036-186">61</span></span>             | <span data-ttu-id="fb036-187">15</span><span class="sxs-lookup"><span data-stu-id="fb036-187">15</span></span>                 |
| <span data-ttu-id="fb036-188">91</span><span class="sxs-lookup"><span data-stu-id="fb036-188">91</span></span>             | <span data-ttu-id="fb036-189">20</span><span class="sxs-lookup"><span data-stu-id="fb036-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="fb036-190">Eksempel 3: Renter efter interval = måneder</span><span class="sxs-lookup"><span data-stu-id="fb036-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="fb036-191">Du har oprettet en rentekode, der opkræver rente én gang for hver måned, hvor fakturabetalingen overskrider posteringens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="fb036-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fb036-192">Du vil basere beregningen på en procentvis renteværdi i henhold til de trinvise månedsintervaller.</span><span class="sxs-lookup"><span data-stu-id="fb036-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="fb036-193">Renteværdien vil være 1,5 procent pr. måned for de første tre måneder, 2,0 procent pr. måned for de næste tre måneder og 2,5 procent pr. måned for hver måned ud over de første seks måneder.</span><span class="sxs-lookup"><span data-stu-id="fb036-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="fb036-194">Indstil rentekodeværdierne på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fb036-195">**Feltnavn**</span><span class="sxs-lookup"><span data-stu-id="fb036-195">**Field name**</span></span>                  | <span data-ttu-id="fb036-196">**Feltværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fb036-197">**Rentekode**</span><span class="sxs-lookup"><span data-stu-id="fb036-197">**Interest code**</span></span>               | <span data-ttu-id="fb036-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="fb036-198">1M%ByMth</span></span>        |
| <span data-ttu-id="fb036-199">**Beregn rente hver**</span><span class="sxs-lookup"><span data-stu-id="fb036-199">**Calculate interest every**</span></span>    | <span data-ttu-id="fb036-200">1/Måned</span><span class="sxs-lookup"><span data-stu-id="fb036-200">1/Month</span></span>         |
| <span data-ttu-id="fb036-201">**Rente efter interval**</span><span class="sxs-lookup"><span data-stu-id="fb036-201">**Interest by range**</span></span>           | <span data-ttu-id="fb036-202">Måneder</span><span class="sxs-lookup"><span data-stu-id="fb036-202">Months</span></span>          |
| <span data-ttu-id="fb036-203">**Beregn renten på baggrund af**</span><span class="sxs-lookup"><span data-stu-id="fb036-203">**Calculate interest based on**</span></span> | <span data-ttu-id="fb036-204">Procentdel</span><span class="sxs-lookup"><span data-stu-id="fb036-204">Percentage</span></span>      |

<span data-ttu-id="fb036-205">Du angiver intervaloplysninger på følgende måde.</span><span class="sxs-lookup"><span data-stu-id="fb036-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="fb036-206">**Fra værdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-206">**From value**</span></span> | <span data-ttu-id="fb036-207">**Renteværdi**</span><span class="sxs-lookup"><span data-stu-id="fb036-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fb036-208">0</span><span class="sxs-lookup"><span data-stu-id="fb036-208">0</span></span>              | <span data-ttu-id="fb036-209">1.5</span><span class="sxs-lookup"><span data-stu-id="fb036-209">1.5</span></span>                |
| <span data-ttu-id="fb036-210">4</span><span class="sxs-lookup"><span data-stu-id="fb036-210">4</span></span>              | <span data-ttu-id="fb036-211">2</span><span class="sxs-lookup"><span data-stu-id="fb036-211">2</span></span>                  |
| <span data-ttu-id="fb036-212">7</span><span class="sxs-lookup"><span data-stu-id="fb036-212">7</span></span>              | <span data-ttu-id="fb036-213">2,5</span><span class="sxs-lookup"><span data-stu-id="fb036-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="fb036-214">Nye versioner</span><span class="sxs-lookup"><span data-stu-id="fb036-214">New versions</span></span>
<span data-ttu-id="fb036-215">Rentekoder er for gældende dato.</span><span class="sxs-lookup"><span data-stu-id="fb036-215">Interest codes are date effective.</span></span> <span data-ttu-id="fb036-216">Hvis du vil ændre renten, kan du oprette en **ny version**, der er gældende for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="fb036-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="fb036-217">For at få vist forskellige versioner kan du bruge menupunktet **Pr. dato** til at vælge skæringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="fb036-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="fb036-218">Du kan også vælge **Vis alle poster** for at få vist alle rentekoderne på siden.</span><span class="sxs-lookup"><span data-stu-id="fb036-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
