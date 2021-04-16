---
title: Oprette kalendere og generere arbejdstider
description: Kalendere beskriver kapacitet og arbejdstider for operationsressourcer. Denne artikel hjælper dig med at definere en arbejdskalender, der er baseret på en arbejdstidsskabelon.
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28e11613cb9e10b258e1c373890505fb6e71d29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804907"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="e2a86-104">Oprette kalendere og generere arbejdstider</span><span class="sxs-lookup"><span data-stu-id="e2a86-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="e2a86-105">Kalendere beskriver kapacitet og arbejdstider for operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="e2a86-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="e2a86-106">Denne artikel hjælper dig med at definere en arbejdskalender, der er baseret på en arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e2a86-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="e2a86-107">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="e2a86-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="e2a86-108">Vælg **Styring af ressourcelivscyklus** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="e2a86-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="e2a86-109">Vælg **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="e2a86-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-110">Select **New**.</span></span>
4. <span data-ttu-id="e2a86-111">Klassificer kalenderen i feltet **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="e2a86-112">Dette er id'et for den kalender, der bruges som reference ved tildeling af kalendere, som f.eks. til en operationsressource eller ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="e2a86-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="e2a86-113">Navngiv kalenderen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="e2a86-114">Skriv et tal i feltet **Standardarbejdsdag i timer**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="e2a86-115">Sørg for, at rækken er markeret, og vælg derefter **Arbejdstider** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e2a86-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="e2a86-116">Vælg **Opbyg arbejdstider**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-116">Select **Compose working times**.</span></span> <span data-ttu-id="e2a86-117">Generer arbejdstimer for hver dag i den periode, hvor du vil kunne at planlægge arbejde.</span><span class="sxs-lookup"><span data-stu-id="e2a86-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="e2a86-118">Med tiden kan du oprette arbejdstider for yderligere perioder.</span><span class="sxs-lookup"><span data-stu-id="e2a86-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="e2a86-119">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="e2a86-120">Dette er den første dag, denne kalender skal være åben.</span><span class="sxs-lookup"><span data-stu-id="e2a86-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="e2a86-121">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="e2a86-122">Dette er den sidste dag, denne kalender er åben.</span><span class="sxs-lookup"><span data-stu-id="e2a86-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="e2a86-123">Indtast eller vælg en værdi i feltet **Arbejdstidsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="e2a86-124">Arbejdstidsskabelonen definerer arbejdstider for hver ugedag.</span><span class="sxs-lookup"><span data-stu-id="e2a86-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="e2a86-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-125">Select **OK**.</span></span>
13. <span data-ttu-id="e2a86-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e2a86-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]