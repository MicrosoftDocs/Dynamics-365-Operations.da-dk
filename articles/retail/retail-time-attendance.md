---
title: "Detailtid og fremmøde"
description: "Dette emne beskriver de scenarier, der understøttes for styring af tids- og fremmødestyring i Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="aa68a-103">Detailtid og fremmøde</span><span class="sxs-lookup"><span data-stu-id="aa68a-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="aa68a-104">Dette emne beskriver de scenarier, der understøttes for styring af tids- og fremmødestyring i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="aa68a-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="aa68a-105">Administrer arbejderopsætning og -planlægning</span><span class="sxs-lookup"><span data-stu-id="aa68a-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="aa68a-106">Indledende konfiguration</span><span class="sxs-lookup"><span data-stu-id="aa68a-106">Initial configuration</span></span>

-   <span data-ttu-id="aa68a-107">Kør konfigurationsguiden.</span><span class="sxs-lookup"><span data-stu-id="aa68a-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="aa68a-108">Registrer arbejdere som arbejdere, der registrerer tid</span><span class="sxs-lookup"><span data-stu-id="aa68a-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="aa68a-109">Planlæg tidsplaner for arbejdere</span><span class="sxs-lookup"><span data-stu-id="aa68a-109">Plan worker schedules</span></span>

-   <span data-ttu-id="aa68a-110">Anvende profiler ved hjælp af arbejdsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="aa68a-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="aa68a-111">Få flere oplysninger under <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="aa68a-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="aa68a-112">Få oplysninger om konfigurationstrinnene under <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="aa68a-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="aa68a-113">Detailspecifik konfiguration</span><span class="sxs-lookup"><span data-stu-id="aa68a-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="aa68a-114">Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="aa68a-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="aa68a-115">Klik på **POS-funktionalitetsprofiler** &gt; **Funktioner** &gt; **POS-tidsregistreringer** &gt; **Aktivér tidsregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="aa68a-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="aa68a-116">Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser.</span><span class="sxs-lookup"><span data-stu-id="aa68a-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="aa68a-117">Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, som brugeren er knyttet til, via adressekartoteket).</span><span class="sxs-lookup"><span data-stu-id="aa68a-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="aa68a-118">Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle.</span><span class="sxs-lookup"><span data-stu-id="aa68a-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="aa68a-119">Klik på **POS-rettighedsgrupper** &gt; **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="aa68a-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="aa68a-120">Registrer tid</span><span class="sxs-lookup"><span data-stu-id="aa68a-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="aa68a-121">Tidsregistreringer for kassereren og andre</span><span class="sxs-lookup"><span data-stu-id="aa68a-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="aa68a-122">Om POS:</span><span class="sxs-lookup"><span data-stu-id="aa68a-122">On POS:</span></span>
    -   <span data-ttu-id="aa68a-123">Komme-handlinger:</span><span class="sxs-lookup"><span data-stu-id="aa68a-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="aa68a-124">Log på med en handling uden pengeskuffe eller et nyt skift.</span><span class="sxs-lookup"><span data-stu-id="aa68a-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="aa68a-125">Vælg en tidsurshandling.</span><span class="sxs-lookup"><span data-stu-id="aa68a-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="aa68a-126">Vælg en ønsket handling:</span><span class="sxs-lookup"><span data-stu-id="aa68a-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="aa68a-127">Komme</span><span class="sxs-lookup"><span data-stu-id="aa68a-127">Clock-in</span></span>
            -   <span data-ttu-id="aa68a-128">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="aa68a-128">Break for Work</span></span>
            -   <span data-ttu-id="aa68a-129">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="aa68a-129">Break for Lunch</span></span>
            -   <span data-ttu-id="aa68a-130">Gå</span><span class="sxs-lookup"><span data-stu-id="aa68a-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="aa68a-131">Aktuel status</span><span class="sxs-lookup"><span data-stu-id="aa68a-131">Current state</span></span></th>
    <th><span data-ttu-id="aa68a-132">Tilgængelige handlinger</span><span class="sxs-lookup"><span data-stu-id="aa68a-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="aa68a-133">Komme</span><span class="sxs-lookup"><span data-stu-id="aa68a-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="aa68a-134">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="aa68a-134">Break for Work</span></span></li>
    <li><span data-ttu-id="aa68a-135">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="aa68a-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="aa68a-136">Gå</span><span class="sxs-lookup"><span data-stu-id="aa68a-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="aa68a-137">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="aa68a-137">Break for Work</span></span></td>
    <td><span data-ttu-id="aa68a-138">Komme</span><span class="sxs-lookup"><span data-stu-id="aa68a-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="aa68a-139">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="aa68a-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="aa68a-140">Komme</span><span class="sxs-lookup"><span data-stu-id="aa68a-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="aa68a-141">Gå</span><span class="sxs-lookup"><span data-stu-id="aa68a-141">Clock-out</span></span></td>
    <td><span data-ttu-id="aa68a-142">Komme</span><span class="sxs-lookup"><span data-stu-id="aa68a-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="aa68a-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="aa68a-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="aa68a-144">Få vist en bekræftelsesmeddelelse, og kontrollér, at den aktuelle aktivitetstid er korrekt.</span><span class="sxs-lookup"><span data-stu-id="aa68a-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="aa68a-145">Logbog:</span><span class="sxs-lookup"><span data-stu-id="aa68a-145">Logbook:</span></span>
    -   <span data-ttu-id="aa68a-146">Klik på **Logbog** for at få vist tidsuraktivitet.</span><span class="sxs-lookup"><span data-stu-id="aa68a-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="aa68a-147">Du kan bruge tidsfiltre til at vælge forskellige tidsvinduer.</span><span class="sxs-lookup"><span data-stu-id="aa68a-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="aa68a-148">Hvis du arbejder i flere butikker på forskellige steder, kan du se dine tidsregistreringer fra alle de butikker, hvor du har registreret tid.</span><span class="sxs-lookup"><span data-stu-id="aa68a-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="aa68a-149">Du kan bruge butiksfiltret til at få vist tidsregistreringer fra en valgt butik.</span><span class="sxs-lookup"><span data-stu-id="aa68a-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="aa68a-150">Forskellige tidszoner:</span><span class="sxs-lookup"><span data-stu-id="aa68a-150">Different time zones:</span></span>
    -   <span data-ttu-id="aa68a-151">Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone.</span><span class="sxs-lookup"><span data-stu-id="aa68a-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="aa68a-152">Du er f.eks. leder for to butikker, en i Arizona og den anden i Nevada.</span><span class="sxs-lookup"><span data-stu-id="aa68a-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="aa68a-153">En kasserer registrerer en mødetid klokken 9:00</span><span class="sxs-lookup"><span data-stu-id="aa68a-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="aa68a-154">i Arizona.</span><span class="sxs-lookup"><span data-stu-id="aa68a-154">in Arizona.</span></span> <span data-ttu-id="aa68a-155">På dette tidspunkt er tiden 8.00 om morgenen i Nevada.</span><span class="sxs-lookup"><span data-stu-id="aa68a-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="aa68a-156">Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.</span><span class="sxs-lookup"><span data-stu-id="aa68a-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="aa68a-157">Få vist tidsregistrering for arbejder</span><span class="sxs-lookup"><span data-stu-id="aa68a-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="aa68a-158">Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype</span><span class="sxs-lookup"><span data-stu-id="aa68a-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="aa68a-159">Om POS:</span><span class="sxs-lookup"><span data-stu-id="aa68a-159">On POS:</span></span>

-   <span data-ttu-id="aa68a-160">Vælg **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="aa68a-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="aa68a-161">Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="aa68a-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="aa68a-162">Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="aa68a-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="aa68a-163">Behandl og administrer tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="aa68a-163">Process and manage time registrations</span></span>
<span data-ttu-id="aa68a-164">En Dynamics 365 for Retail-bruger følger arbejdsgangen for at beregne, godkende og overføre tidsregistreringer til løn.</span><span class="sxs-lookup"><span data-stu-id="aa68a-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="aa68a-165">Primære handlinger</span><span class="sxs-lookup"><span data-stu-id="aa68a-165">Primary operations</span></span>

-   <span data-ttu-id="aa68a-166">Beregn</span><span class="sxs-lookup"><span data-stu-id="aa68a-166">Calculate</span></span>
-   <span data-ttu-id="aa68a-167">Godkend</span><span class="sxs-lookup"><span data-stu-id="aa68a-167">Approve</span></span>
-   <span data-ttu-id="aa68a-168">Sende til løn</span><span class="sxs-lookup"><span data-stu-id="aa68a-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="aa68a-169">Andre almindelige handlinger</span><span class="sxs-lookup"><span data-stu-id="aa68a-169">Other common operations</span></span>

-   <span data-ttu-id="aa68a-170">Flere udklokninger</span><span class="sxs-lookup"><span data-stu-id="aa68a-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="aa68a-171">Registrere fravær</span><span class="sxs-lookup"><span data-stu-id="aa68a-171">Register Absence</span></span>

<span data-ttu-id="aa68a-172">Få flere oplysninger om, hvordan du behandler tids- og fremmøderegistreringer, under <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="aa68a-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




