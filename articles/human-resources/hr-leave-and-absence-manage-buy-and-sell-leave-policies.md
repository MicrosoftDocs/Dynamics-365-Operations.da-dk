---
title: Administrere politikker for køb og salg af orlov
description: Du kan give medarbejderne mulighed for at købe og sælge orlov i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429007"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="5ad32-103">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="5ad32-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5ad32-104">Du kan give medarbejderne mulighed for at købe orlov ved at oprette en politik for køb af orlov.</span><span class="sxs-lookup"><span data-stu-id="5ad32-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="5ad32-105">Give medarbejdere mulighed for at købe og sælge orlov</span><span class="sxs-lookup"><span data-stu-id="5ad32-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="5ad32-106">På siden **Parametre for orlov og fravær** skal du vælge **Ja** for **Tillad medarbejderne at købe orlov**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="5ad32-107">Oprette en politik for køb af orlov</span><span class="sxs-lookup"><span data-stu-id="5ad32-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="5ad32-108">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="5ad32-109">Vælg **Politik for køb oig salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="5ad32-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-110">Select **New**.</span></span>

4. <span data-ttu-id="5ad32-111">Angiv et **Navn** og en **Beskrivelse** for politikken under **Politik for køb og salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="5ad32-112">Vælg en **Politiktype**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="5ad32-113">De tilgængelige politiktyper er **Beløb** og **Timer pr. uge**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="5ad32-114">Vælg **Beløb** for at angive et **Fast beløb** for de maksimale beløb, som medarbejderne kan købe og sælge.</span><span class="sxs-lookup"><span data-stu-id="5ad32-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="5ad32-115">Hvis du vælger **Timer pr. uge**, bruges den arbejdstid, der er defineret i medarbejderens tildelte arbejdstidskalender, til at bestemme det maksimale antal for politikken.</span><span class="sxs-lookup"><span data-stu-id="5ad32-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="5ad32-116">Vælg en **Startdato** og en **Slutdato** for politikken.</span><span class="sxs-lookup"><span data-stu-id="5ad32-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="5ad32-117">Anmodninger om at købe eller sælge orlov vil kun kunne sendes i løbet af denne tidsramme.</span><span class="sxs-lookup"><span data-stu-id="5ad32-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="5ad32-118">Under **Politik for køb** skal du vælge **Fuldtidsækvivalens** (FTÆ) for at opnå det maksimale beløb baseret på den FTÆ, der er defineret folr medarbejderens stilling.</span><span class="sxs-lookup"><span data-stu-id="5ad32-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="5ad32-119">Hvis politiktypen er **Beløb**, skal du angive et **Maksimalt fast beløb**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="5ad32-120">Vælg **Tilføj** for at tilføje orlovstyper, som medarbejderne kan købe orlov for.</span><span class="sxs-lookup"><span data-stu-id="5ad32-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="5ad32-121">Du kan føje flere orlovstyper til politikken.</span><span class="sxs-lookup"><span data-stu-id="5ad32-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="5ad32-122">Angiv **Måneders tjeneste** for orlovstypen for at aktivere forskellige tjenestemåneder og bestemme det maksimale beløb, som en medarbejder kan købe.</span><span class="sxs-lookup"><span data-stu-id="5ad32-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="5ad32-123">Angiv **Maksimalt beløb** for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="5ad32-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="5ad32-124">Angiv den **Lønsats**, som medarbejderen skal købe orloven med.</span><span class="sxs-lookup"><span data-stu-id="5ad32-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="5ad32-125">Du kan vælge at angive den **Lønkode**, der skal bruges til købet af orlov.</span><span class="sxs-lookup"><span data-stu-id="5ad32-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="5ad32-126">Du kan evt. angive, om du vil bruge FTÆ til at bestemme det maksimale beløb for orlovstypen.</span><span class="sxs-lookup"><span data-stu-id="5ad32-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="5ad32-127">Føje politikken for køb og salg af orlov til en orlovs- og fraværsplan</span><span class="sxs-lookup"><span data-stu-id="5ad32-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="5ad32-128">På siden **Orlov og fravær** skal du vælge en orlovs- og fraværsplan.</span><span class="sxs-lookup"><span data-stu-id="5ad32-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="5ad32-129">Under **Regler** skal du vælge **Politik for køb og salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="5ad32-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ad32-130">Se også</span><span class="sxs-lookup"><span data-stu-id="5ad32-130">See also</span></span>

[<span data-ttu-id="5ad32-131">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="5ad32-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="5ad32-132">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="5ad32-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="5ad32-133">Periodiser orlovs- og fraværsplaner</span><span class="sxs-lookup"><span data-stu-id="5ad32-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="5ad32-134">Køb og sælg orlov</span><span class="sxs-lookup"><span data-stu-id="5ad32-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

