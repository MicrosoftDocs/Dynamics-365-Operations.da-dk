---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (10. september 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 1340f17e57f49d6adb9dc0a7c769bafa655de56e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551237"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="15528-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (10. september 2018)</span><span class="sxs-lookup"><span data-stu-id="15528-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15528-104">**Build 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="15528-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="15528-105">I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="15528-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="15528-106">Tillad bestemt tidspunkter på dagen på anmodninger om fritid (halve dage)</span><span class="sxs-lookup"><span data-stu-id="15528-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="15528-107">Hvis orlov og fravær er konfigureret, så der sendes fritid i dage, kan du nu også aktivere en halv dag-definition.</span><span class="sxs-lookup"><span data-stu-id="15528-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="15528-108">Derefter, når brugere sender anmodninger om fritid, kan de angive, om de anmoder om den første halvdel eller anden halvdel af dagen.</span><span class="sxs-lookup"><span data-stu-id="15528-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="15528-109">Denne indstilling er som standard slået fra.</span><span class="sxs-lookup"><span data-stu-id="15528-109">By default, this option is turned off.</span></span> <span data-ttu-id="15528-110">For medarbejdere, der anmoder om fritid den første halvdel eller anden halvdel af dagen, skal du slå denne indstilling til i **Orlov og fravær**-området af personaleparametre.</span><span class="sxs-lookup"><span data-stu-id="15528-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="15528-111">Sikkerhedsrettigheden for denne funktion er Vedligehold personaleparametre.</span><span class="sxs-lookup"><span data-stu-id="15528-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="15528-112">Validering af orlovs- og fraværsposter</span><span class="sxs-lookup"><span data-stu-id="15528-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="15528-113">Afhængigt af, hvordan orlov er konfigureret, vil medarbejdere, der forsøger at sende en fritidsanmodning, der er længere end deres arbejdsdag, modtage en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="15528-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="15528-114">De bliver med andre ord advaret, hvis de forsøger at tage mere end en hel dag fri på en given dato.</span><span class="sxs-lookup"><span data-stu-id="15528-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="15528-115">Denne kontrol er altid aktiveret.</span><span class="sxs-lookup"><span data-stu-id="15528-115">This validation is always turned on.</span></span> <span data-ttu-id="15528-116">Medarbejdere, der overstiger dagsgrænsen, der er defineret, modtager hver gang en advarsel i deres fritidsanmodning.</span><span class="sxs-lookup"><span data-stu-id="15528-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="15528-117">Flere felter til betingelsessætninger i arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="15528-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="15528-118">Yderligere felter er føjet til betingelsessætninger og pladsholdere for flere arbejdsgange i Core HR.</span><span class="sxs-lookup"><span data-stu-id="15528-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="15528-119">Følgende felter er føjet til arbejdsgange for løn, fratrædelse og overførsel:</span><span class="sxs-lookup"><span data-stu-id="15528-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="15528-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="15528-120">EmploymentType</span></span>
- <span data-ttu-id="15528-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="15528-121">LegalEntity</span></span>
- <span data-ttu-id="15528-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="15528-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="15528-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="15528-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="15528-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="15528-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="15528-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="15528-125">TransitionDate</span></span>
- <span data-ttu-id="15528-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="15528-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="15528-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="15528-127">WorkerStartDate</span></span>
- <span data-ttu-id="15528-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="15528-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="15528-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="15528-129">ProbationEndDate</span></span>
- <span data-ttu-id="15528-130">Stilling</span><span class="sxs-lookup"><span data-stu-id="15528-130">Position</span></span>
- <span data-ttu-id="15528-131">Fagforening</span><span class="sxs-lookup"><span data-stu-id="15528-131">Union</span></span>
- <span data-ttu-id="15528-132">Afdeling</span><span class="sxs-lookup"><span data-stu-id="15528-132">Department</span></span>
- <span data-ttu-id="15528-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="15528-133">PositionType</span></span>
- <span data-ttu-id="15528-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="15528-134">CompLocation</span></span>
- <span data-ttu-id="15528-135">Stilling</span><span class="sxs-lookup"><span data-stu-id="15528-135">Title</span></span>
- <span data-ttu-id="15528-136">Job</span><span class="sxs-lookup"><span data-stu-id="15528-136">Job</span></span>
- <span data-ttu-id="15528-137">JobType</span><span class="sxs-lookup"><span data-stu-id="15528-137">JobType</span></span>
- <span data-ttu-id="15528-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="15528-138">JobFamily</span></span>
- <span data-ttu-id="15528-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="15528-139">JobFunction</span></span>

<span data-ttu-id="15528-140">Følgende felter er føjet til stillingens arbejdsgang:</span><span class="sxs-lookup"><span data-stu-id="15528-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="15528-141">Stilling</span><span class="sxs-lookup"><span data-stu-id="15528-141">Position</span></span>
- <span data-ttu-id="15528-142">Fagforening</span><span class="sxs-lookup"><span data-stu-id="15528-142">Union</span></span>
- <span data-ttu-id="15528-143">Afdeling</span><span class="sxs-lookup"><span data-stu-id="15528-143">Department</span></span>
- <span data-ttu-id="15528-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="15528-144">PositionType</span></span>
- <span data-ttu-id="15528-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="15528-145">CompLocation</span></span>
- <span data-ttu-id="15528-146">Stilling</span><span class="sxs-lookup"><span data-stu-id="15528-146">Title</span></span>
- <span data-ttu-id="15528-147">Job</span><span class="sxs-lookup"><span data-stu-id="15528-147">Job</span></span>
- <span data-ttu-id="15528-148">JobType</span><span class="sxs-lookup"><span data-stu-id="15528-148">JobType</span></span>
- <span data-ttu-id="15528-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="15528-149">JobFamily</span></span>
- <span data-ttu-id="15528-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="15528-150">JobFunction</span></span>

<span data-ttu-id="15528-151">Felterne i betingelsessætninger og pladsholdere er tilgængelige for alle brugere, der har adgang til at konfigurere de tidligere nævnte arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="15528-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="15528-152">Navigation til Attract fra personalestyring</span><span class="sxs-lookup"><span data-stu-id="15528-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="15528-153">I personalestyring, hvis Attract ikke er konfigureret, vil **Kandidater, der skal ansættes**-afsnittet hjælpe brugerne i gang med Attract i stedet for at vise meddelelsen "Vi fandt ingenting at vise her".</span><span class="sxs-lookup"><span data-stu-id="15528-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="15528-154">Andre ændringer</span><span class="sxs-lookup"><span data-stu-id="15528-154">Other changes</span></span>

<span data-ttu-id="15528-155">Denne version indeholder flere supplerende fejlrettelser:</span><span class="sxs-lookup"><span data-stu-id="15528-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="15528-156">Når en kontrahent ansættes, skal fanen **Kompensation** ikke være tilgængelig på anmodnings-/handlingssiden.</span><span class="sxs-lookup"><span data-stu-id="15528-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="15528-157">Du kan ikke fortsætte i processen Anmod om opsigelse, før alle obligatoriske felter indeholder data.</span><span class="sxs-lookup"><span data-stu-id="15528-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="15528-158">Problemer med at få vist sorteringsrækkefølge og dato i analyser af Personalestyring er håndteret.</span><span class="sxs-lookup"><span data-stu-id="15528-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
