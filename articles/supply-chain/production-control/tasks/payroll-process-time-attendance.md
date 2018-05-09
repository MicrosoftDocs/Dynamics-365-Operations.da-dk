---
title: "Aktivere lønproces for tid og fremmøde"
description: "Denne procedure viser, hvordan lønprocessen for tid og fremmøde aktiveres."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0858b7628536a37020841489378e2f1762fb046e
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="a54fc-103">Aktivere lønproces for tid og fremmøde</span><span class="sxs-lookup"><span data-stu-id="a54fc-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a54fc-104">Denne procedure viser, hvordan lønprocessen for tid og fremmøde aktiveres.</span><span class="sxs-lookup"><span data-stu-id="a54fc-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="a54fc-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a54fc-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="a54fc-106">Opret en lønart med en relateret lønsats</span><span class="sxs-lookup"><span data-stu-id="a54fc-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="a54fc-107">Tid og fremmøde > Opsætning > Løn > Lønarter</span><span class="sxs-lookup"><span data-stu-id="a54fc-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="a54fc-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a54fc-108">Click New.</span></span>
3. <span data-ttu-id="a54fc-109">Indtast en værdi i feltet Lønart.</span><span class="sxs-lookup"><span data-stu-id="a54fc-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="a54fc-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a54fc-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a54fc-111">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a54fc-111">Click Save.</span></span>
6. <span data-ttu-id="a54fc-112">Klik på Satser.</span><span class="sxs-lookup"><span data-stu-id="a54fc-112">Click Rates.</span></span>
    * <span data-ttu-id="a54fc-113">Satser for lønarter defineres for bestemte tidsintervaller og kan være angivet for individuelle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="a54fc-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="a54fc-114">Det er ikke altid nødvendigt at oprette satser til lønarterne i tid og fremmøde.</span><span class="sxs-lookup"><span data-stu-id="a54fc-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="a54fc-115">Disse oplysninger findes muligvis i det lønsystem, der bruges til at oprette løn.</span><span class="sxs-lookup"><span data-stu-id="a54fc-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="a54fc-116">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a54fc-116">Click New.</span></span>
8. <span data-ttu-id="a54fc-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a54fc-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a54fc-118">Indtast et tal i satsfeltet.</span><span class="sxs-lookup"><span data-stu-id="a54fc-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="a54fc-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a54fc-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="a54fc-120">Opret en lønaftale</span><span class="sxs-lookup"><span data-stu-id="a54fc-120">Create a pay agreement</span></span>
1. <span data-ttu-id="a54fc-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a54fc-121">Close the page.</span></span>
2. <span data-ttu-id="a54fc-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a54fc-122">Close the page.</span></span>
3. <span data-ttu-id="a54fc-123">Gå til Lønaftaler.</span><span class="sxs-lookup"><span data-stu-id="a54fc-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="a54fc-124">Tid og fremmøde > Opsætning > Lønaftaler</span><span class="sxs-lookup"><span data-stu-id="a54fc-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="a54fc-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a54fc-125">Click New.</span></span>
5. <span data-ttu-id="a54fc-126">Indtast en værdi i feltet Lønaftale.</span><span class="sxs-lookup"><span data-stu-id="a54fc-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="a54fc-127">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a54fc-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="a54fc-128">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a54fc-128">Click Save.</span></span>
8. <span data-ttu-id="a54fc-129">Klik på Aftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="a54fc-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="a54fc-130">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a54fc-130">Click New.</span></span>
10. <span data-ttu-id="a54fc-131">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a54fc-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="a54fc-132">Indtast eller vælg en værdi i feltet Profiltype.</span><span class="sxs-lookup"><span data-stu-id="a54fc-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="a54fc-133">Indtast eller vælg en værdi i feltet Lønart.</span><span class="sxs-lookup"><span data-stu-id="a54fc-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="a54fc-134">Opret lønaftale for tidsregistreringsarbejder</span><span class="sxs-lookup"><span data-stu-id="a54fc-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="a54fc-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a54fc-135">Close the page.</span></span>
2. <span data-ttu-id="a54fc-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a54fc-136">Close the page.</span></span>
3. <span data-ttu-id="a54fc-137">Gå til Arbejdere, der registrerer tid.</span><span class="sxs-lookup"><span data-stu-id="a54fc-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="a54fc-138">Tid og fremmøde > Opsætning > Arbejdere, der registrerer tid</span><span class="sxs-lookup"><span data-stu-id="a54fc-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="a54fc-139">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a54fc-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a54fc-140">Klik på fanen Ansættelse.</span><span class="sxs-lookup"><span data-stu-id="a54fc-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="a54fc-141">Udvid sektionen Tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="a54fc-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="a54fc-142">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a54fc-142">Click Edit.</span></span>
8. <span data-ttu-id="a54fc-143">Indtast eller vælg en værdi i feltet Lønaftale.</span><span class="sxs-lookup"><span data-stu-id="a54fc-143">In the Pay agreement field, enter or select a value.</span></span>

