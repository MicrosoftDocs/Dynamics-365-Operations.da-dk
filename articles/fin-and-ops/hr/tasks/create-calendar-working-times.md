--- 
title: Oprette en kalender og generere arbejdstider
description: Kalendere beskriver kapacitet og arbejdstider for operationsressourcer.
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a8dcef8d8ba6f6d41a997b5b0623cb9577ce00d3
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="c0d99-103">Oprette en kalender og generere arbejdstider</span><span class="sxs-lookup"><span data-stu-id="c0d99-103">Create a calendar and generate working times</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0d99-104">Kalendere beskriver kapacitet og arbejdstider for operationsressourcer.</span><span class="sxs-lookup"><span data-stu-id="c0d99-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="c0d99-105">Denne procedure hjælper dig med at definere en arbejdskalender, der er baseret på en arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c0d99-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="c0d99-106">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c0d99-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="c0d99-107">Gå til alle arbejdsområder > Styring af ressourcelivscyklus.</span><span class="sxs-lookup"><span data-stu-id="c0d99-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="c0d99-108">Klik på Kalendere.</span><span class="sxs-lookup"><span data-stu-id="c0d99-108">Click Calendars.</span></span>
3. <span data-ttu-id="c0d99-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c0d99-109">Click New.</span></span>
4. <span data-ttu-id="c0d99-110">Skriv en værdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="c0d99-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="c0d99-111">Dette er id'et for den kalender, der bruges som reference ved tildeling af kalendere, som f.eks. til en operationsressource eller ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="c0d99-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="c0d99-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c0d99-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="c0d99-113">Skriv et tal i feltet Standardarbejdsdag i timer.</span><span class="sxs-lookup"><span data-stu-id="c0d99-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="c0d99-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c0d99-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c0d99-115">Klik på Arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="c0d99-115">Click Working times.</span></span>
9. <span data-ttu-id="c0d99-116">Klik på Opbyg arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="c0d99-116">Click Compose working times.</span></span>
    * <span data-ttu-id="c0d99-117">Generer arbejdstimer for hver dag i den periode, hvor du vil kunne at planlægge arbejde.</span><span class="sxs-lookup"><span data-stu-id="c0d99-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="c0d99-118">Med tiden kan du oprette arbejdstider for yderligere perioder.</span><span class="sxs-lookup"><span data-stu-id="c0d99-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="c0d99-119">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="c0d99-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c0d99-120">Dette er den første dag, denne kalender skal være åben.</span><span class="sxs-lookup"><span data-stu-id="c0d99-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="c0d99-121">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="c0d99-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="c0d99-122">Dette er den sidste dag, denne kalender er åben.</span><span class="sxs-lookup"><span data-stu-id="c0d99-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="c0d99-123">Indtast eller vælg en værdi i feltet Arbejdstidsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c0d99-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="c0d99-124">Arbejdstidsskabelonen definerer arbejdstider for hver ugedag.</span><span class="sxs-lookup"><span data-stu-id="c0d99-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="c0d99-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c0d99-125">Click OK.</span></span>
14. <span data-ttu-id="c0d99-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c0d99-126">Close the page.</span></span>


