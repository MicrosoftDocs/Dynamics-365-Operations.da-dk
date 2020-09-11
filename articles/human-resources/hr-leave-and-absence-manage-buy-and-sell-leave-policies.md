---
title: Administrere politikker for køb og salg af orlov
description: Du kan give medarbejderne mulighed for at købe og sælge orlov i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712104"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="96513-103">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="96513-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="96513-104">Du kan give medarbejderne mulighed for at købe og sælge orlov ved at oprette en politik for køb og salg af orlov.</span><span class="sxs-lookup"><span data-stu-id="96513-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="96513-105">Du kan konfigurere disse politikker til at bruge en arbejdsproces til godkendelser, angive maksimumbeløb og satser samt angive satser for køb og salg.</span><span class="sxs-lookup"><span data-stu-id="96513-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="96513-106">Give medarbejdere mulighed for at købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="96513-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="96513-107">På siden **Parametre for orlov og fravær** skal du vælge **Ja** for **Tillad medarbejderne at købe orlov** og **Tillad medarbejderne at sælge orlov**.</span><span class="sxs-lookup"><span data-stu-id="96513-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="96513-108">Oprette en politik for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="96513-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="96513-109">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="96513-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="96513-110">Vælg **Politik for køb oig salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="96513-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="96513-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="96513-111">Select **New**.</span></span>

4. <span data-ttu-id="96513-112">Angiv et **Navn** og en **Beskrivelse** for politikken under **Politik for køb og salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="96513-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="96513-113">Vælg en **Politiktype**.</span><span class="sxs-lookup"><span data-stu-id="96513-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="96513-114">De tilgængelige politiktyper er **Beløb** og **Timer pr. uge**.</span><span class="sxs-lookup"><span data-stu-id="96513-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="96513-115">Vælg **Beløb** for at angive et **Fast beløb** for de maksimale beløb, som medarbejderne kan købe og sælge.</span><span class="sxs-lookup"><span data-stu-id="96513-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="96513-116">Hvis du vælger **Timer pr. uge**, bruges den arbejdstid, der er defineret i medarbejderens tildelte arbejdstidskalender, til at bestemme det maksimale antal for politikken.</span><span class="sxs-lookup"><span data-stu-id="96513-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="96513-117">Vælg en **Startdato** og en **Slutdato** for politikken.</span><span class="sxs-lookup"><span data-stu-id="96513-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="96513-118">Anmodninger om at købe eller sælge orlov vil kun kunne sendes i løbet af denne tidsramme.</span><span class="sxs-lookup"><span data-stu-id="96513-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="96513-119">Vælg et **Arbejdsgangs-id** for politikken.</span><span class="sxs-lookup"><span data-stu-id="96513-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="96513-120">Alle købs- og salgsanmodninger bruger denne arbejdsgang til gennemsyn og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="96513-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="96513-121">Under **Politik for køb** skal du vælge **Fuldtidsækvivalens** (FTÆ) for at opnå det maksimale beløb baseret på den FTÆ, der er defineret folr medarbejderens stilling.</span><span class="sxs-lookup"><span data-stu-id="96513-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="96513-122">Hvis politiktypen er **Beløb**, skal du angive et **Maksimalt fast beløb**.</span><span class="sxs-lookup"><span data-stu-id="96513-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="96513-123">Vælg **Tilføj** for at tilføje orlovstyper, som medarbejderne kan købe orlov for.</span><span class="sxs-lookup"><span data-stu-id="96513-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="96513-124">Du kan føje flere orlovstyper til politikken.</span><span class="sxs-lookup"><span data-stu-id="96513-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="96513-125">Angiv **Måneders tjeneste** for orlovstypen for at aktivere forskellige tjenestemåneder og bestemme det maksimale beløb, som en medarbejder kan købe.</span><span class="sxs-lookup"><span data-stu-id="96513-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="96513-126">Angiv **Maksimalt beløb** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="96513-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="96513-127">Angiv den **Lønsats**, som medarbejderen skal købe orloven med.</span><span class="sxs-lookup"><span data-stu-id="96513-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="96513-128">Du kan vælge at angive den **Lønkode**, der skal bruges til købet af orlov.</span><span class="sxs-lookup"><span data-stu-id="96513-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="96513-129">Du kan evt. angive, om du vil bruge FTÆ til at bestemme det maksimale beløb for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="96513-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="96513-130">Hvis du vil oprette en salgspolitik, skal du følge trin 8 til 14 under **Salgspolitik**.</span><span class="sxs-lookup"><span data-stu-id="96513-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="96513-131">Føje politikken for køb og salg af orlov til en orlovs- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="96513-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="96513-132">På siden **Orlov og fravær** skal du vælge en orlovs- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="96513-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="96513-133">Under **Regler** skal du vælge **Politik for køb og salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="96513-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="96513-134">Se også</span><span class="sxs-lookup"><span data-stu-id="96513-134">See also</span></span>

[<span data-ttu-id="96513-135">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="96513-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="96513-136">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="96513-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="96513-137">Periodiser orlovs- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="96513-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="96513-138">Køb og sælg orlov</span><span class="sxs-lookup"><span data-stu-id="96513-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

