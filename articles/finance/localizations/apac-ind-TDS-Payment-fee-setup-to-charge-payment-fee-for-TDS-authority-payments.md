---
title: Angive betalingsgebyrer til skattemyndighedsbetalinger
description: Dette emne forklarer, hvordan du kan angive de betalingsgebyrer, der opkræves af myndighederne i forbindelse med kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023133"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="95518-103">Angive betalingsgebyrer til skattemyndighedsbetalinger</span><span class="sxs-lookup"><span data-stu-id="95518-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95518-104">Dette emne forklarer, hvordan du kan angive de betalingsgebyrer, der opkræves af myndighederne i forbindelse med kildeskat (TDS – Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="95518-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="95518-105">Gå til **Kreditor \> Betalingsopsætning \> Betalingsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="95518-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="95518-106">[![Siden Betalingsgebyr](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="95518-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="95518-107">Vælg **Ny** for at oprette et betalingsgebyr, og angive de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="95518-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="95518-108">Vælg typen af betalignsgebyr i feltet **Gebyrtype**:</span><span class="sxs-lookup"><span data-stu-id="95518-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="95518-109">**None**</span><span class="sxs-lookup"><span data-stu-id="95518-109">**None**</span></span>
    - <span data-ttu-id="95518-110">**Renter** – Der opkræves renter af forsinkede betalinger til skattemyndighedskreditoren.</span><span class="sxs-lookup"><span data-stu-id="95518-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="95518-111">**Andre** – Der opkræves andre gebyrer for forsinkede betalinger til skattemyndighedskreditoren.</span><span class="sxs-lookup"><span data-stu-id="95518-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="95518-112">Hvis du vælger **Renter** eller **Andre**, angives feltet **Gebyr** automatisk til **Finans**.</span><span class="sxs-lookup"><span data-stu-id="95518-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="95518-113">Hvis du har valgt **Renter** eller **Andre** i feltet **Felttype**, skal du vælge den finanskonto i feltet **Hovedkonto**, som renter eller andre gebyrer skal bogføres til.</span><span class="sxs-lookup"><span data-stu-id="95518-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="95518-114">Angiv de øvrige krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="95518-114">Enter the other required details.</span></span>
6. <span data-ttu-id="95518-115">Vælg **Opsætning af betalingsgebyr** i handlingsruden for at åbne siden **Opsætning af betalingsgebyr**, hvor du kan definere betalingsgebyrer for forskellige kombinationer af banker, betalingsmåder, betalingsspecifikationer, valutaer og datointervaller.</span><span class="sxs-lookup"><span data-stu-id="95518-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="95518-116">[![Siden Opsætning af betalingsgebyr](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="95518-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="95518-117">Under fanen **Oversigt** i feltet **Grupperinger** kan du angive, hvilke banker du angiver betalingsgebyret for:</span><span class="sxs-lookup"><span data-stu-id="95518-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="95518-118">**Tabel** – Gebyret gælder for en bestemt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="95518-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="95518-119">**Gruppe** – Gebyret gælder for en bestemt bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="95518-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="95518-120">**Alle** – Gebyret er gyldigt for alle bankkonti.</span><span class="sxs-lookup"><span data-stu-id="95518-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="95518-121">Hvis du har valgt **Tabel** eller **Gruppe** i feltet **Grupperinger**, skal du vælge den specifikke bankkonto eller bankgruppe, du konfigurerer betalingsgebyret for, i feltet **Bankrelation**.</span><span class="sxs-lookup"><span data-stu-id="95518-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="95518-122">Vælg den betalingsmåde, der skal bruges til betaling af betalingsgebyret, i feltet **Betalingsmetode**.</span><span class="sxs-lookup"><span data-stu-id="95518-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="95518-123">I feltet **Betalingsspecifikation** skal du vælge eller indtaste den betalingsspecifikationskode, der blev genereret på siden **Betalingsspecifikation**.</span><span class="sxs-lookup"><span data-stu-id="95518-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="95518-124">Betalingsspecifikationen bruges med elektronisk pengeoverførsel som betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="95518-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="95518-125">Vælg den valuta, der aktiverer gebyret, i feltet **Betalingsvaluta**.</span><span class="sxs-lookup"><span data-stu-id="95518-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="95518-126">Det er kun transaktioner, der bruger den valgte valuta, som kan aktivere gebyret.</span><span class="sxs-lookup"><span data-stu-id="95518-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="95518-127">Hvis dette felt ikke udfyldes, aktiverer alle valutaer gebyret.</span><span class="sxs-lookup"><span data-stu-id="95518-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="95518-128">Vælg beregningsmetoden i feltet **Procent/beløb**.</span><span class="sxs-lookup"><span data-stu-id="95518-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="95518-129">Valgmulighederne er **Beløb**, **Procent** og **Interval**.</span><span class="sxs-lookup"><span data-stu-id="95518-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="95518-130">I feltet **Gebyrbeløb** skal du angive gebyrbeløbet som enten en procentdel af betalingen eller som beløbet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="95518-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="95518-131">Angiv valutakoden for gebyret i feltet **Valuta for gebyr**.</span><span class="sxs-lookup"><span data-stu-id="95518-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="95518-132">Vælg fanen **Generelt** for at få vist eller redigere oplysningerne om den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="95518-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="95518-133">[![Fanen Generelt](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="95518-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="95518-134">Angiv det minimale transaktionsbeløb, der aktiverer gebyret, i feltet **Minimum**.</span><span class="sxs-lookup"><span data-stu-id="95518-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="95518-135">Angiv det maksimale transaktionsbeløb, der aktiverer gebyret, i feltet **Maksimum**.</span><span class="sxs-lookup"><span data-stu-id="95518-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="95518-136">Definer et datointerval til beregning af gebyrer i felterne **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="95518-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="95518-137">I feltet **Minimumgebyr** skal du angive gebyrbeløbet som enten en procentdel af betalingen eller som beløbet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="95518-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="95518-138">Vælg den momsgruppe, der skal bruges til at beregne moms for gebyrbeløbet, i feltet **Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="95518-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="95518-139">Vælg den varemomsgruppe, der skal bruges til at beregne varemoms for gebyrbeløbet, i feltet **Varemomsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="95518-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="95518-140">Vælg fanen **Interval**.</span><span class="sxs-lookup"><span data-stu-id="95518-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="95518-141">[![Fanen Interval](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="95518-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="95518-142">Angiv antallet af dage mellem bogføringsdatoen (diskonteringsdatoen) for betalingen og forfaldsdatoen for egenvekslen i feltet **Dage**.</span><span class="sxs-lookup"><span data-stu-id="95518-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="95518-143">I feltet **Procent/beløb** skal du vælge, om specifikationen er en procent eller et angivet beløb.</span><span class="sxs-lookup"><span data-stu-id="95518-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="95518-144">I feltet **Gebyrbeløb** skal du angive beløbet for gebyret som en procentdel af betalingen eller som beløbet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="95518-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="95518-145">Luk siden **Opsætning af betalingsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="95518-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="95518-146">Luk siden **Betalingsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="95518-146">Close the **Payment fee** page.</span></span>
