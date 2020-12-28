---
title: Oprette en arbejdstidskalender
description: Definer en arbejdstidskalender, feriedage og ikke-arbejdstider i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bedbe65f146c4159c2a809de8f683815fd4a01f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417786"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="559e8-103">Oprette en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="559e8-103">Create a working time calendar</span></span>

<span data-ttu-id="559e8-104">I en arbejdstidskalender i Dynamics 365 Human Resources vises de dage og timer, hvor medarbejdere arbejder i organisationen.</span><span class="sxs-lookup"><span data-stu-id="559e8-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="559e8-105">Når en medarbejder sender en anmodning om fritid, behøver de ikke at bekymre sig om helligdage og lukketider.</span><span class="sxs-lookup"><span data-stu-id="559e8-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="559e8-106">Hvis du vil strømline anmodninger om fritid, skal du konfigurere disse elementer for organisationen:</span><span class="sxs-lookup"><span data-stu-id="559e8-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="559e8-107">Arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="559e8-107">Working time calendar</span></span>
- <span data-ttu-id="559e8-108">Helligdage og lukninger</span><span class="sxs-lookup"><span data-stu-id="559e8-108">Holidays and closures</span></span>
- <span data-ttu-id="559e8-109">Fritid</span><span class="sxs-lookup"><span data-stu-id="559e8-109">Non-work time</span></span>

<span data-ttu-id="559e8-110">Du kan tilføje de sidste to elementer, mens du konfigurerer en arbejdstidskalender.</span><span class="sxs-lookup"><span data-stu-id="559e8-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="559e8-111">Du kan også konfigurere eller opdatere dem separat.</span><span class="sxs-lookup"><span data-stu-id="559e8-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="559e8-112">Konfigurere en arbejdstidskalender</span><span class="sxs-lookup"><span data-stu-id="559e8-112">Set up a working time calendar</span></span>

<span data-ttu-id="559e8-113">Konfigurer mindst én arbejdstidskalender, der viser arbejdsdagene og -timerne.</span><span class="sxs-lookup"><span data-stu-id="559e8-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="559e8-114">Hvis du har adresser i flere lande og områder, kan det være en god ide at oprette en arbejdstidskalender for hvert område.</span><span class="sxs-lookup"><span data-stu-id="559e8-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="559e8-115">Vælg **Kalendere** på siden **Organisationsadministration**.</span><span class="sxs-lookup"><span data-stu-id="559e8-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="559e8-116">Vælg **Ny**, og angiv et navn og en beskrivelse for din nye kalender.</span><span class="sxs-lookup"><span data-stu-id="559e8-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="559e8-117">Under **Oprettelsesindstillinger** kan du vælge arbejdsdage for din organisation og angive arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="559e8-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="559e8-118">Hvis du vil tilføje en helligdag eller en lukning, skal du vælge knappen **Tilføj** ud for **Helligdage og lukninger**.</span><span class="sxs-lookup"><span data-stu-id="559e8-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="559e8-119">Hvis du vil tilføje ikke-arbejdstider, f.eks. frokostpauser, skal du vælge **Tilføj** under **Fritid** og angive navnet og tids intervallet.</span><span class="sxs-lookup"><span data-stu-id="559e8-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="559e8-120">Under **Dage** skal du vælge **Generér** for at generere dagene i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="559e8-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="559e8-121">Angiv datointervallet for kalenderen, og vælg derefter **Generér dage**.</span><span class="sxs-lookup"><span data-stu-id="559e8-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="559e8-122">Hvis du vil tilføje arbejdsplaner, skal du vælge **Tilføj** under **Arbejdsplan** og derefter angive tidspunkterne for hver enkelt arbejdsplan.</span><span class="sxs-lookup"><span data-stu-id="559e8-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="559e8-123">Konfigurere helligdage og lukninger</span><span class="sxs-lookup"><span data-stu-id="559e8-123">Configure holidays and closures</span></span>

<span data-ttu-id="559e8-124">Du kan tilføje eller ændre helligdage og lukninger separat fra en arbejdstidskalender.</span><span class="sxs-lookup"><span data-stu-id="559e8-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="559e8-125">Vælg **Helligdage og lukninger** på siden **Organisationsadministration**.</span><span class="sxs-lookup"><span data-stu-id="559e8-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="559e8-126">Vælg **Ny**, og angiv et navn og en dato for helligdagen eller lukningen.</span><span class="sxs-lookup"><span data-stu-id="559e8-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="559e8-127">Konfigurere fritid</span><span class="sxs-lookup"><span data-stu-id="559e8-127">Configure non-work time</span></span>

<span data-ttu-id="559e8-128">Du kan tilføje eller ændre fritid separat fra en arbejdstidskalender.</span><span class="sxs-lookup"><span data-stu-id="559e8-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="559e8-129">Vælg **Fritid** på siden **Organisationsadministration**.</span><span class="sxs-lookup"><span data-stu-id="559e8-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="559e8-130">Vælg **Ny**, og angiv navnet og tidsintervallet for fritiden.</span><span class="sxs-lookup"><span data-stu-id="559e8-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="559e8-131">Hvis du har aktiveret prøvefunktionen til korrektion af helligdage i orlov og fravær, bruger Personale helligdage og lukningsdatoer til at bestemme det antal dage, der skal reguleres for medarbejdere, der er tilmeldt i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="559e8-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="559e8-132">Se også</span><span class="sxs-lookup"><span data-stu-id="559e8-132">See also</span></span>

- [<span data-ttu-id="559e8-133">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="559e8-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="559e8-134">Konfigurere orlovs- og fraværstyper</span><span class="sxs-lookup"><span data-stu-id="559e8-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
