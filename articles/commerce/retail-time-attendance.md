---
title: Tids- og fremmødestyring i Retail
description: Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411198"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="cc172-103">Tids- og fremmødestyring i Retail</span><span class="sxs-lookup"><span data-stu-id="cc172-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc172-104">Dette emne beskriver de scenarier, der understøttes for styring af tid og fremmøde i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc172-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="cc172-105">Administrer arbejderopsætning og -planlægning</span><span class="sxs-lookup"><span data-stu-id="cc172-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="cc172-106">Indledende konfiguration</span><span class="sxs-lookup"><span data-stu-id="cc172-106">Initial configuration</span></span>

- <span data-ttu-id="cc172-107">Kør konfigurationsguiden.</span><span class="sxs-lookup"><span data-stu-id="cc172-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="cc172-108">Registrer arbejdere som arbejdere, der registrerer tid</span><span class="sxs-lookup"><span data-stu-id="cc172-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="cc172-109">Planlæg tidsplaner for arbejdere</span><span class="sxs-lookup"><span data-stu-id="cc172-109">Plan worker schedules</span></span>

- <span data-ttu-id="cc172-110">Anvende profiler ved hjælp af arbejdsplanlægningen.</span><span class="sxs-lookup"><span data-stu-id="cc172-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="cc172-111">Du kan finde flere oplysninger om arbejdstidsprofiler i [Anvende profiler ved hjælp af arbejdsplanlægning](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc172-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="cc172-112">Du kan finde oplysninger om konfigurationstrin under [Opsætning af tid og fremmøde](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc172-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="cc172-113">Commerce-specifik konfiguration</span><span class="sxs-lookup"><span data-stu-id="cc172-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="cc172-114">Aktivér en funktionalitetsprofil til ur, for arbejdere, som du vil aktivere tidsregistreringer for.</span><span class="sxs-lookup"><span data-stu-id="cc172-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="cc172-115">Klik på **POS-funktionalitetsprofiler** &gt; **Funktioner** &gt; **POS-tidsregistreringer** &gt; **Aktivér tidsregistreringer**.</span><span class="sxs-lookup"><span data-stu-id="cc172-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="cc172-116">Konfigurer POS-tilladelser for at aktivere tilladelsen Vis tidsursangivelser.</span><span class="sxs-lookup"><span data-stu-id="cc172-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="cc172-117">Denne tilladelse lader en bruger at se tidsur-registreringer for andre arbejdere i butikken og fra alle de butikker, (som brugeren er knyttet til, via adressekartoteket).</span><span class="sxs-lookup"><span data-stu-id="cc172-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="cc172-118">Det kan være, at du vil aktivere denne tilladelse for en chefrolle, men ikke for en kasseassistentrolle.</span><span class="sxs-lookup"><span data-stu-id="cc172-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="cc172-119">Klik på **POS-rettighedsgrupper** &gt; **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="cc172-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="cc172-120">Registrer tid</span><span class="sxs-lookup"><span data-stu-id="cc172-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="cc172-121">Tidsregistreringer for kassereren og andre</span><span class="sxs-lookup"><span data-stu-id="cc172-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="cc172-122">Om POS:</span><span class="sxs-lookup"><span data-stu-id="cc172-122">On POS:</span></span>

    - <span data-ttu-id="cc172-123">Komme-handlinger:</span><span class="sxs-lookup"><span data-stu-id="cc172-123">Clock-in operations:</span></span>

        - <span data-ttu-id="cc172-124">Log på med en handling uden pengeskuffe eller et nyt skift.</span><span class="sxs-lookup"><span data-stu-id="cc172-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="cc172-125">Vælg en tidsurshandling.</span><span class="sxs-lookup"><span data-stu-id="cc172-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="cc172-126">Vælg en ønsket handling:</span><span class="sxs-lookup"><span data-stu-id="cc172-126">Select a desired operation:</span></span>

            - <span data-ttu-id="cc172-127">Komme</span><span class="sxs-lookup"><span data-stu-id="cc172-127">Clock-in</span></span>
            - <span data-ttu-id="cc172-128">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="cc172-128">Break for Work</span></span>
            - <span data-ttu-id="cc172-129">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="cc172-129">Break for Lunch</span></span>
            - <span data-ttu-id="cc172-130">Gå</span><span class="sxs-lookup"><span data-stu-id="cc172-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="cc172-131">Aktuel status</span><span class="sxs-lookup"><span data-stu-id="cc172-131">Current state</span></span></th>
        <th><span data-ttu-id="cc172-132">Tilgængelige handlinger</span><span class="sxs-lookup"><span data-stu-id="cc172-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="cc172-133">Komme</span><span class="sxs-lookup"><span data-stu-id="cc172-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="cc172-134">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="cc172-134">Break for Work</span></span></li>
        <li><span data-ttu-id="cc172-135">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="cc172-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="cc172-136">Gå</span><span class="sxs-lookup"><span data-stu-id="cc172-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="cc172-137">Arbejdspause</span><span class="sxs-lookup"><span data-stu-id="cc172-137">Break for Work</span></span></td>
        <td><span data-ttu-id="cc172-138">Komme</span><span class="sxs-lookup"><span data-stu-id="cc172-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="cc172-139">Frokostpause</span><span class="sxs-lookup"><span data-stu-id="cc172-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="cc172-140">Komme</span><span class="sxs-lookup"><span data-stu-id="cc172-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="cc172-141">Gå</span><span class="sxs-lookup"><span data-stu-id="cc172-141">Clock-out</span></span></td>
        <td><span data-ttu-id="cc172-142">Komme</span><span class="sxs-lookup"><span data-stu-id="cc172-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="cc172-143">[![Tidsurstilstande](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="cc172-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="cc172-144">Få vist en bekræftelsesmeddelelse, og kontrollér, at den aktuelle aktivitetstid er korrekt.</span><span class="sxs-lookup"><span data-stu-id="cc172-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="cc172-145">Logbog:</span><span class="sxs-lookup"><span data-stu-id="cc172-145">Logbook:</span></span>

    - <span data-ttu-id="cc172-146">Klik på **Logbog** for at få vist tidsuraktivitet.</span><span class="sxs-lookup"><span data-stu-id="cc172-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="cc172-147">Du kan bruge tidsfiltre til at vælge forskellige tidsvinduer.</span><span class="sxs-lookup"><span data-stu-id="cc172-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="cc172-148">Hvis du arbejder i flere butikker på forskellige steder, kan du se dine tidsregistreringer fra alle de butikker, hvor du har registreret tid.</span><span class="sxs-lookup"><span data-stu-id="cc172-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="cc172-149">Du kan bruge butiksfiltret til at få vist tidsregistreringer fra en valgt butik.</span><span class="sxs-lookup"><span data-stu-id="cc172-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="cc172-150">Forskellige tidszoner:</span><span class="sxs-lookup"><span data-stu-id="cc172-150">Different time zones:</span></span>

    - <span data-ttu-id="cc172-151">Hvis du får vist tid fra et andet sted (for kasseassistentens logbog eller ved hjælp af **Vis tidsursangivelser** i et chefscenarie), og den placering er i en anden tidszone, konverteres de tidsregistreringer, som du kan se, til din lokale tidszone.</span><span class="sxs-lookup"><span data-stu-id="cc172-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="cc172-152">Du er f.eks. leder for to butikker, en i Arizona og den anden i Nevada.</span><span class="sxs-lookup"><span data-stu-id="cc172-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="cc172-153">En kasserer registrerer en mødetid klokken 9:00</span><span class="sxs-lookup"><span data-stu-id="cc172-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="cc172-154">i Arizona.</span><span class="sxs-lookup"><span data-stu-id="cc172-154">in Arizona.</span></span> <span data-ttu-id="cc172-155">På dette tidspunkt er tiden 8.00 om morgenen i Nevada.</span><span class="sxs-lookup"><span data-stu-id="cc172-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="cc172-156">Hvis du derfor er i Nevada-butikken og ser på tidsregistreringsposter, er tidsregistreringen markeret som 08:00 om morgenen.</span><span class="sxs-lookup"><span data-stu-id="cc172-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="cc172-157">Få vist tidsregistrering for arbejder</span><span class="sxs-lookup"><span data-stu-id="cc172-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="cc172-158">Få vist tidsregistrering for arbejdere, og filtrer efter butik eller aktivitetstype</span><span class="sxs-lookup"><span data-stu-id="cc172-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="cc172-159">Om POS:</span><span class="sxs-lookup"><span data-stu-id="cc172-159">On POS:</span></span>

- <span data-ttu-id="cc172-160">Vælg **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="cc172-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="cc172-161">Du kan se tidsursregistreringsaktiviteter fra alle arbejdere, der er tildelt til de samme butikker, du er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="cc172-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="cc172-162">Du kan bruge aktivitetstypen og butiksfiltre til at filtrere tidsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="cc172-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="cc172-163">Behandl og administrer tidsregistreringer</span><span class="sxs-lookup"><span data-stu-id="cc172-163">Process and manage time registrations</span></span>

<span data-ttu-id="cc172-164">En Commerce-bruger følger arbejdsgangen for at beregne, godkende og overføre tidsregistreringer til løn.</span><span class="sxs-lookup"><span data-stu-id="cc172-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="cc172-165">Primære handlinger</span><span class="sxs-lookup"><span data-stu-id="cc172-165">Primary operations</span></span>

- <span data-ttu-id="cc172-166">Beregn</span><span class="sxs-lookup"><span data-stu-id="cc172-166">Calculate</span></span>
- <span data-ttu-id="cc172-167">Godkend</span><span class="sxs-lookup"><span data-stu-id="cc172-167">Approve</span></span>
- <span data-ttu-id="cc172-168">Sende til løn</span><span class="sxs-lookup"><span data-stu-id="cc172-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="cc172-169">Andre almindelige handlinger</span><span class="sxs-lookup"><span data-stu-id="cc172-169">Other common operations</span></span>

- <span data-ttu-id="cc172-170">Flere udklokninger</span><span class="sxs-lookup"><span data-stu-id="cc172-170">Bulk Clock-out</span></span>
- <span data-ttu-id="cc172-171">Registrere fravær</span><span class="sxs-lookup"><span data-stu-id="cc172-171">Register Absence</span></span>

<span data-ttu-id="cc172-172">Du kan finde flere oplysninger om, hvordan du behandler registreringer af tid og fremmøde, under [Behandle registreringer af tid og fremmøde](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc172-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
