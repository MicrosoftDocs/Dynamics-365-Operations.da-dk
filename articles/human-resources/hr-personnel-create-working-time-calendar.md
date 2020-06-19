---
title: Oprette kalendere og generere arbejdstider
description: Kalendere beskriver kapacitet og arbejdstider for operationsressourcer. Denne artikel hjælper dig med at definere en arbejdskalender, der er baseret på en arbejdstidsskabelon.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f4960f895ac6a9e6284119a998af540523785ed
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430365"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="acd60-104">Oprette kalendere og generere arbejdstider</span><span class="sxs-lookup"><span data-stu-id="acd60-104">Create calendars and generate working times</span></span>



<span data-ttu-id="acd60-105">Kalendere beskriver kapacitet og arbejdstider for operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="acd60-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="acd60-106">Denne artikel hjælper dig med at definere en arbejdskalender, der er baseret på en arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="acd60-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="acd60-107">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="acd60-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="acd60-108">Vælg **Styring af ressourcelivscyklus** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="acd60-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="acd60-109">Vælg **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="acd60-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="acd60-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="acd60-110">Select **New**.</span></span>
4. <span data-ttu-id="acd60-111">Klassificer kalenderen i feltet **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="acd60-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="acd60-112">Dette er id'et for den kalender, der bruges som reference ved tildeling af kalendere, som f.eks. til en operationsressource eller ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="acd60-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="acd60-113">Navngiv kalenderen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="acd60-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="acd60-114">Skriv et tal i feltet **Standardarbejdsdag i timer**.</span><span class="sxs-lookup"><span data-stu-id="acd60-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="acd60-115">Sørg for, at rækken er markeret, og vælg derefter **Arbejdstider** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="acd60-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="acd60-116">Vælg **Opbyg arbejdstider**.</span><span class="sxs-lookup"><span data-stu-id="acd60-116">Select **Compose working times**.</span></span> <span data-ttu-id="acd60-117">Generer arbejdstimer for hver dag i den periode, hvor du vil kunne at planlægge arbejde.</span><span class="sxs-lookup"><span data-stu-id="acd60-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="acd60-118">Med tiden kan du oprette arbejdstider for yderligere perioder.</span><span class="sxs-lookup"><span data-stu-id="acd60-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="acd60-119">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="acd60-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="acd60-120">Dette er den første dag, denne kalender skal være åben.</span><span class="sxs-lookup"><span data-stu-id="acd60-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="acd60-121">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="acd60-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="acd60-122">Dette er den sidste dag, denne kalender er åben.</span><span class="sxs-lookup"><span data-stu-id="acd60-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="acd60-123">Indtast eller vælg en værdi i feltet **Arbejdstidsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="acd60-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="acd60-124">Arbejdstidsskabelonen definerer arbejdstider for hver ugedag.</span><span class="sxs-lookup"><span data-stu-id="acd60-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="acd60-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="acd60-125">Select **OK**.</span></span>
13. <span data-ttu-id="acd60-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="acd60-126">Close the page.</span></span>

