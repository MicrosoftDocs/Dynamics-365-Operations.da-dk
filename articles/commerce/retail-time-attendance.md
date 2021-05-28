---
title: Tids- og fremmødestyring i Retail
description: Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7ac7eec69bda7ad2fa41a7311a71a969eddeafb6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021482"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="d2ad7-103">Tids- og fremmødestyring i Retail</span><span class="sxs-lookup"><span data-stu-id="d2ad7-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2ad7-104">Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="d2ad7-105">Administrer arbejderopsætning og -planlægning</span><span class="sxs-lookup"><span data-stu-id="d2ad7-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="d2ad7-106">Indledende konfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ad7-106">Initial configuration</span></span>

- <span data-ttu-id="d2ad7-107">Kør konfigurationsguiden.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="d2ad7-108">Registrer arbejdere som arbejdere, der registrerer tid</span><span class="sxs-lookup"><span data-stu-id="d2ad7-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="d2ad7-109">Planlæg tidsplaner for arbejdere</span><span class="sxs-lookup"><span data-stu-id="d2ad7-109">Plan worker schedules</span></span>

- <span data-ttu-id="d2ad7-110">Anvende profiler ved hjælp af arbejdsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="d2ad7-111">Du kan finde flere oplysninger om arbejdstidsprofiler i [Anvende profiler ved hjælp af arbejdsplanlægning](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-111">For more information, see [Apply profiles using work planner](/dynamicsax-2012/appuser-itpro/apply-profiles-using-work-planner).</span></span>

<span data-ttu-id="d2ad7-112">Du kan finde oplysninger om konfigurationstrin under [Opsætning af tid og fremmøde](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-112">For information about the configuration steps, see [Setting up time and attendance](/dynamicsax-2012/appuser-itpro/setting-up-time-and-attendance).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="d2ad7-113">Commerce-specifik konfiguration</span><span class="sxs-lookup"><span data-stu-id="d2ad7-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="d2ad7-114">Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="d2ad7-115">Klik på **POS-funktionalitetsprofiler** &gt; **Funktioner** &gt; **POS-tidsregistreringer** &gt; **Aktivér tidsregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="d2ad7-116">Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="d2ad7-117">Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, (som brugeren er knyttet til, via adressekartoteket).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="d2ad7-118">Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="d2ad7-119">Klik på **POS-rettighedsgrupper** &gt; **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="d2ad7-120">Registrer tid</span><span class="sxs-lookup"><span data-stu-id="d2ad7-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="d2ad7-121">Tidsregistreringer for kassereren og andre</span><span class="sxs-lookup"><span data-stu-id="d2ad7-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="d2ad7-122">Om POS:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-122">On POS:</span></span>

    - <span data-ttu-id="d2ad7-123">Komme-handlinger:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-123">Clock-in operations:</span></span>

        - <span data-ttu-id="d2ad7-124">Log på med en handling uden pengeskuffe eller et nyt skift.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="d2ad7-125">Vælg en tidsurshandling.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="d2ad7-126">Vælg en ønsket handling:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-126">Select a desired operation:</span></span>

            - <span data-ttu-id="d2ad7-127">Komme</span><span class="sxs-lookup"><span data-stu-id="d2ad7-127">Clock-in</span></span>
            - <span data-ttu-id="d2ad7-128">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-128">Break for Work</span></span>
            - <span data-ttu-id="d2ad7-129">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-129">Break for Lunch</span></span>
            - <span data-ttu-id="d2ad7-130">Gå</span><span class="sxs-lookup"><span data-stu-id="d2ad7-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="d2ad7-131">Aktuel status</span><span class="sxs-lookup"><span data-stu-id="d2ad7-131">Current state</span></span></th>
        <th><span data-ttu-id="d2ad7-132">Tilgængelige handlinger</span><span class="sxs-lookup"><span data-stu-id="d2ad7-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="d2ad7-133">Komme</span><span class="sxs-lookup"><span data-stu-id="d2ad7-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="d2ad7-134">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-134">Break for Work</span></span></li>
        <li><span data-ttu-id="d2ad7-135">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="d2ad7-136">Gå</span><span class="sxs-lookup"><span data-stu-id="d2ad7-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="d2ad7-137">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-137">Break for Work</span></span></td>
        <td><span data-ttu-id="d2ad7-138">Komme</span><span class="sxs-lookup"><span data-stu-id="d2ad7-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="d2ad7-139">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="d2ad7-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="d2ad7-140">Komme</span><span class="sxs-lookup"><span data-stu-id="d2ad7-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="d2ad7-141">Gå</span><span class="sxs-lookup"><span data-stu-id="d2ad7-141">Clock-out</span></span></td>
        <td><span data-ttu-id="d2ad7-142">Komme</span><span class="sxs-lookup"><span data-stu-id="d2ad7-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="d2ad7-143">[![Tidsurstilstande](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="d2ad7-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="d2ad7-144">Få vist en bekræftelsesmeddelelse, og kontrollér, at den aktuelle aktivitetstid er korrekt.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="d2ad7-145">Logbog:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-145">Logbook:</span></span>

    - <span data-ttu-id="d2ad7-146">Klik på **Logbog** for at få vist tidsuraktivitet.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="d2ad7-147">Du kan bruge tidsfiltre til at vælge forskellige tidsvinduer.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="d2ad7-148">Hvis du arbejder i flere butikker på forskellige steder, kan du se dine tidsregistreringer fra alle de butikker, hvor du har registreret tid.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="d2ad7-149">Du kan bruge butiksfiltret til at få vist tidsregistreringer fra en valgt butik.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="d2ad7-150">Forskellige tidszoner:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-150">Different time zones:</span></span>

    - <span data-ttu-id="d2ad7-151">Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="d2ad7-152">Du er f.eks. leder for to butikker, en i Arizona og den anden i Nevada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="d2ad7-153">En kasserer registrerer en mødetid klokken 9:00</span><span class="sxs-lookup"><span data-stu-id="d2ad7-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="d2ad7-154">i Arizona.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-154">in Arizona.</span></span> <span data-ttu-id="d2ad7-155">På dette tidspunkt er tiden 8.00 om morgenen i Nevada.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="d2ad7-156">Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="d2ad7-157">Få vist tidsregistrering for arbejder</span><span class="sxs-lookup"><span data-stu-id="d2ad7-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="d2ad7-158">Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype</span><span class="sxs-lookup"><span data-stu-id="d2ad7-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="d2ad7-159">Om POS:</span><span class="sxs-lookup"><span data-stu-id="d2ad7-159">On POS:</span></span>

- <span data-ttu-id="d2ad7-160">Vælg **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="d2ad7-161">Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="d2ad7-162">Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="d2ad7-163">Behandl og administrer tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="d2ad7-163">Process and manage time registrations</span></span>

<span data-ttu-id="d2ad7-164">En Commerce-bruger følger arbejdsgangen for at beregne, godkende og overføre tidsregistreringer til løn.</span><span class="sxs-lookup"><span data-stu-id="d2ad7-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="d2ad7-165">Primære handlinger</span><span class="sxs-lookup"><span data-stu-id="d2ad7-165">Primary operations</span></span>

- <span data-ttu-id="d2ad7-166">Beregn</span><span class="sxs-lookup"><span data-stu-id="d2ad7-166">Calculate</span></span>
- <span data-ttu-id="d2ad7-167">Godkend</span><span class="sxs-lookup"><span data-stu-id="d2ad7-167">Approve</span></span>
- <span data-ttu-id="d2ad7-168">Sende til løn</span><span class="sxs-lookup"><span data-stu-id="d2ad7-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="d2ad7-169">Andre almindelige handlinger</span><span class="sxs-lookup"><span data-stu-id="d2ad7-169">Other common operations</span></span>

- <span data-ttu-id="d2ad7-170">Flere udklokninger</span><span class="sxs-lookup"><span data-stu-id="d2ad7-170">Bulk Clock-out</span></span>
- <span data-ttu-id="d2ad7-171">Registrere fravær</span><span class="sxs-lookup"><span data-stu-id="d2ad7-171">Register Absence</span></span>

<span data-ttu-id="d2ad7-172">Du kan finde flere oplysninger om, hvordan du behandler registreringer af tid og fremmøde, under [Behandle registreringer af tid og fremmøde](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).</span><span class="sxs-lookup"><span data-stu-id="d2ad7-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](/dynamicsax-2012/appuser-itpro/process-time-and-attendance-registrations).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]