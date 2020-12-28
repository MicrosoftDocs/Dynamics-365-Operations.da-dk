---
title: Oprette og opdatere tidsintervaller for kundeafhentning
description: I dette emne beskrives, hvordan du opretter, konfigurerer og opdaterer tidsintervaller for kundeafhentning i Commerce Headquarters.
author: anupamar-ms
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: f86eb47ec64dff230223ed0ecbe792373aca649f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681536"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a><span data-ttu-id="b057f-103">Oprette og opdatere tidsintervaller for kundeafhentning</span><span class="sxs-lookup"><span data-stu-id="b057f-103">Create and update time slots for customer pickup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b057f-104">I dette emne beskrives, hvordan du opretter, konfigurerer og opdaterer tidsintervaller for kundeafhentning i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b057f-104">This topic describes how to create, configure, and update customer pickup time slots in Commerce headquarters.</span></span>

<span data-ttu-id="b057f-105">Tidsintervalfunktionen giver detailhandlere mulighed for at definere et tidsinterval for varer, som leveringsmåden ved kundeafhentning er slået til for.</span><span class="sxs-lookup"><span data-stu-id="b057f-105">The time slot feature gives retailers a way to define a time slot for items that the customer pickup delivery mode is turned on for.</span></span> <span data-ttu-id="b057f-106">Med tidsintervaller kan detailhandlere definere dage og tidspunkter, hvor ordrer kan afhentes fra en butik.</span><span class="sxs-lookup"><span data-stu-id="b057f-106">Time slots let retailers define the days and times when orders can be picked up from a store.</span></span> <span data-ttu-id="b057f-107">Detailhandlende kan også definere antallet af ordrer, der kan afhentes i en given periode.</span><span class="sxs-lookup"><span data-stu-id="b057f-107">Retailers can also define the number of orders that can be picked up during a given period.</span></span> <span data-ttu-id="b057f-108">På denne måde kan detailhandlerne begrænse antallet af ordrer, der kan afhentes på en given dag og på et givent tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="b057f-108">In this way, retailers can limit the number of orders that can be picked up on a given day and at a given time.</span></span> <span data-ttu-id="b057f-109">Resultatet er en bedre oplevelse for kunderne.</span><span class="sxs-lookup"><span data-stu-id="b057f-109">The result is a better-quality experience for their customers.</span></span>

> [!NOTE]
> <span data-ttu-id="b057f-110">Tidsintervalfunktionen er tilgængelig i Microsoft Dynamics 365 Commerce version 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="b057f-110">The time slot feature is available in Microsoft Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="b057f-111">I følgende illustration vises et eksempel på valg af tidsinterval under betaling ved e-handel.</span><span class="sxs-lookup"><span data-stu-id="b057f-111">The following illustration shows an example of time slot selection during e-commerce checkout.</span></span>

![Eksempel på valg af tidsinterval under betaling ved e-handel](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a><span data-ttu-id="b057f-113">Egenskaber for tidsinterval</span><span class="sxs-lookup"><span data-stu-id="b057f-113">Time slot properties</span></span>

<span data-ttu-id="b057f-114">Et tidsinterval er et specifikt interval, hvor en kunde kan vælge at hente en ordre fra en bestemt butik eller lokalitet.</span><span class="sxs-lookup"><span data-stu-id="b057f-114">A time slot is a specific interval when a customer can choose to pick up an order from a specific store or location.</span></span> <span data-ttu-id="b057f-115">Funktionen til styring af tidsintervaller er kun tilgængelig, når leveringsmåden ved kundeafhentning er konfigureret i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b057f-115">The time slot management feature is available only when the customer pickup delivery mode is configured in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b057f-116">Et tidsinterval defineres ved hjælp af følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="b057f-116">A time slot is defined by using the following properties:</span></span>

- <span data-ttu-id="b057f-117">**Leveringsmåde** – Angiv den afhentningsmåde for leveringen, som tidsintervallet gælder for.</span><span class="sxs-lookup"><span data-stu-id="b057f-117">**Mode of delivery** – Specify the pickup mode of delivery that the time slot applies to.</span></span>
- <span data-ttu-id="b057f-118">**Minimum dage** og **Maksimum dage** – Angiv de tidligste og seneste datoer, der kan vælges for afhentning i forhold til den dato, hvor ordren er afgivet.</span><span class="sxs-lookup"><span data-stu-id="b057f-118">**Minimum Days** and **Maximum Days** – Specify the earliest and latest dates that can be selected for pickup relative to the date when the order is placed.</span></span> 

    <span data-ttu-id="b057f-119">Egenskaben **Minimum dage** sikrer, at der er tilstrækkelig tid til, at forhandleren kan behandle ordren, før den er klar til afhentning.</span><span class="sxs-lookup"><span data-stu-id="b057f-119">The **Minimum Days** property ensures that there is enough time for the retailer to process the order before it's ready for pickup.</span></span> <span data-ttu-id="b057f-120">Egenskaben **Maksimum dage** sikrer, at brugeren ikke kan vælge en dato, der ligger for langt ude i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="b057f-120">The **Maximum Days** property ensures that the user can't select a date that is too far in the future.</span></span> <span data-ttu-id="b057f-121">Hvis minimumværdien f.eks. er **1**, og der afgives en ordre den 20. september, er den tidligste dag, hvor ordren vil være tilgængelig for afhentning, den næste dag, der kan vælges (21. september).</span><span class="sxs-lookup"><span data-stu-id="b057f-121">For example, if the minimum value is set to **1**, and an order is placed on September 20, the earliest day that the order will be available for pickup is the next eligible day (September 21).</span></span> <span data-ttu-id="b057f-122">På samme måde kan du definere det maksimale antal dage, en ordre kan afhentes, ved at angive en maksimumværdi.</span><span class="sxs-lookup"><span data-stu-id="b057f-122">In a similar way, by setting a maximum value, you can define the maximum number of days that an order can be picked up.</span></span> <span data-ttu-id="b057f-123">Når der er defineret minimum- og maksimumværdier, kan webstedets brugere kun se og vælge et bestemt interval af dage under betalingen.</span><span class="sxs-lookup"><span data-stu-id="b057f-123">When minimum and maximum values are defined, site users can see and select only a specific set of days during their checkout experience.</span></span>

    <span data-ttu-id="b057f-124">Du kan indstille minimumværdien til en decimalværdi, der er mindre end 1.</span><span class="sxs-lookup"><span data-stu-id="b057f-124">You can set the minimum value to a decimal value that is less than 1.</span></span> <span data-ttu-id="b057f-125">Hvis f.eks. afhentning er tilgængelig i fire timer, efter at en ordre er afgivet, skal du indstille minimumværdien til **0,17** (= 4 ÷ 24, rundet op til to decimaler).</span><span class="sxs-lookup"><span data-stu-id="b057f-125">For example, if pickup is available four hours after an order is placed, set the minimum value to **0.17** (= 4 ÷ 24, rounded up to two decimal places).</span></span> <span data-ttu-id="b057f-126">Hvis du indstiller minimumværdien til en decimalværdi, der er større end 1, afrundes den dog altid til det nærmeste hele tal (op eller ned).</span><span class="sxs-lookup"><span data-stu-id="b057f-126">However, if you set the minimum value to a decimal value that is more than 1, it's always rounded to the nearest whole number (up or down).</span></span>

    <span data-ttu-id="b057f-127">Hvis du indstiller maksimumværdien til en decimalværdi, rundes den altid op.</span><span class="sxs-lookup"><span data-stu-id="b057f-127">If you set the maximum value to a decimal value, it's always rounded up.</span></span> <span data-ttu-id="b057f-128">En værdi på **1,2** rundes f.eks. op til **2**.</span><span class="sxs-lookup"><span data-stu-id="b057f-128">For example, a value of **1.2** will be rounded up to **2**.</span></span>

- <span data-ttu-id="b057f-129">**Startdato** og **Slutdato** – Angiv start- og slutdatoer for tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="b057f-129">**Start Date** and **End Date** – Specify the start and end dates of the time slot.</span></span> <span data-ttu-id="b057f-130">Hvert tidsinterval har en startdato og en slutdato.</span><span class="sxs-lookup"><span data-stu-id="b057f-130">Each time slot entry has a start date and an end date.</span></span> <span data-ttu-id="b057f-131">Det gør det muligt for dig at tilføje forskellige tidsintervaller i løbet af hele året (f.eks. afhentning i løbet af ferier).</span><span class="sxs-lookup"><span data-stu-id="b057f-131">Therefore, you have the flexibility to add different time slots throughout the year (for example, pickups during holiday hours).</span></span> <span data-ttu-id="b057f-132">Hvis start- og slutdatoer for et tidsinterval ændres, efter at en ordre er afgivet, gælder ændringerne ikke for den pågældende ordre.</span><span class="sxs-lookup"><span data-stu-id="b057f-132">If a time slot's start and dates are changed after an order is placed, the changes won't apply to that order.</span></span> <span data-ttu-id="b057f-133">Når du definerer start-og slutdatoer, skal du overveje at gemme lukkedatoer (f.eks. juledag) og sikre, at der ikke defineres tidsintervaller for disse dage.</span><span class="sxs-lookup"><span data-stu-id="b057f-133">When you define start and end dates, you must consider store closure dates (for example, Christmas day) and ensure that time slots aren't defined for those days.</span></span>
- <span data-ttu-id="b057f-134">**Aktive leveringstimer** – Angiv den periode, hvor afhentning er tilladt.</span><span class="sxs-lookup"><span data-stu-id="b057f-134">**Active Hours of Delivery** – Specify the period when pickup is allowed.</span></span> <span data-ttu-id="b057f-135">Afhentningstiden kan f.eks. være mellem kl. 14 og 17 hver dag.</span><span class="sxs-lookup"><span data-stu-id="b057f-135">For example, the pickup times might be between 2 PM and 5 PM every day.</span></span> <span data-ttu-id="b057f-136">Med denne egenskab kan afhentningstiden være uafhængig af butikkens åbningstider.</span><span class="sxs-lookup"><span data-stu-id="b057f-136">This property enables the pickup times to be independent of store hours.</span></span> <span data-ttu-id="b057f-137">Derfor kan forhandleren konfigurere afhentningstider, der opfylder butikkens specifikke krav.</span><span class="sxs-lookup"><span data-stu-id="b057f-137">Therefore, the retailer can configure pickup times that meet its specific business requirements.</span></span> <span data-ttu-id="b057f-138">Når du definerer de aktive timer for afhentning, skal du overveje at gemme tiderne og sikre, at der ikke defineres afhentningstider, når butikken er lukket.</span><span class="sxs-lookup"><span data-stu-id="b057f-138">When you define the active hours of pickup, you must consider store hours and ensure that pickup times aren't defined for times when the store is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b057f-139">Tiderne for afhentning i butikken skal defineres i tidszonen for den relevante butik.</span><span class="sxs-lookup"><span data-stu-id="b057f-139">The hours for store pickup must be defined in the time zone of the appropriate store.</span></span>

- <span data-ttu-id="b057f-140">**Tidsinterval** – Angiv den varighed, der kan tildeles til hvert tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="b057f-140">**Time Slot Interval** – Specify the duration that can be allotted to each time slot.</span></span> <span data-ttu-id="b057f-141">Varigheden af hver tidsinterval kan f.eks. angives i trin på 15 minutter, 30 minutter eller en time.</span><span class="sxs-lookup"><span data-stu-id="b057f-141">For example, the duration of each time slot might be in increments of 15 minutes, 30 minutes, or one hour.</span></span>
- <span data-ttu-id="b057f-142">**Slots pr. interval** – Angiv det antal kunder eller ordrer, der kan betjenes ved afhentning i løbet af hvert tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="b057f-142">**Slots Per Interval** – Specify the number of customer or orders that can be served for pickup during each time slot interval.</span></span> <span data-ttu-id="b057f-143">Du kan f.eks. angive **1,** **2**, **3** eller et andet helt tal.</span><span class="sxs-lookup"><span data-stu-id="b057f-143">For example, enter **1**, **2**, **3**, or any other whole number.</span></span>
- <span data-ttu-id="b057f-144">**Aktive dage** – Angiv de ugedage, hvor tidsintervaller for afhentning er aktive.</span><span class="sxs-lookup"><span data-stu-id="b057f-144">**Active Days** – Specify the days of the week when the pickup time slots are active.</span></span> <span data-ttu-id="b057f-145">Denne egenskab gør det muligt for forhandleren at definere de dage, hvor afhentning af ordrer kan understøttes.</span><span class="sxs-lookup"><span data-stu-id="b057f-145">This property lets the retailer define the days when it wants to support pickup orders.</span></span>
- <span data-ttu-id="b057f-146">**Detailkanaler** – Angiv detailkanalerne.</span><span class="sxs-lookup"><span data-stu-id="b057f-146">**Retail Channels** – Specify the retail channels.</span></span> <span data-ttu-id="b057f-147">Hvert tidsinterval kan knyttes til en eller flere detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="b057f-147">Each time slot can be associated with one or more retail stores.</span></span> <span data-ttu-id="b057f-148">Afhængigt af en butiks åbningstider, kan der oprettes en eller flere tidsintervalposter, som kan knyttes til en kanal.</span><span class="sxs-lookup"><span data-stu-id="b057f-148">Depending on each store's hours of operation, one or more time slot entries can be created and associated with a channel.</span></span> 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

<span data-ttu-id="b057f-149">Der kan kun konfigureres én tidsintervalskabelon pr. kanal.</span><span class="sxs-lookup"><span data-stu-id="b057f-149">Only one time slot template can be configured per channel.</span></span> <span data-ttu-id="b057f-150">Disse kanaler omfatter fysiske butikker, callcentre, mobilenheder og e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="b057f-150">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a><span data-ttu-id="b057f-151">Konfigurere tidsintervalfunktionen i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="b057f-151">Configure the time slot feature in Commerce headquarters</span></span>

<span data-ttu-id="b057f-152">Der skal defineres tidsintervaller for hver leveringsmåde for afhentning i Commerce Headquarters, så POS- og e-handelskanaler kan referere til dem.</span><span class="sxs-lookup"><span data-stu-id="b057f-152">Time slots must be defined for each pickup mode of delivery in Commerce headquarters, so that point of sale (POS) and e-commerce channels can reference them.</span></span>

- <span data-ttu-id="b057f-153">Der kan kun knyttes én tidsintervalskabelon til hver butik eller kanal.</span><span class="sxs-lookup"><span data-stu-id="b057f-153">Only one time slot template can be associated with each store or channel.</span></span>
- <span data-ttu-id="b057f-154">Hvert tidsinterval, der oprettes, skal være entydig for hver leveringsmåde i hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="b057f-154">Each time slot that is created should be unique to each delivery mode in each template.</span></span>
- <span data-ttu-id="b057f-155">Når tidsintervalfunktionen er konfigureret, vil tidsintervalkalenderen være tilgængelig for de valgte butikker eller butiksgrupper.</span><span class="sxs-lookup"><span data-stu-id="b057f-155">After the time slot feature is configured, the time slot calendar will be available to the selected stores or store groups.</span></span> <span data-ttu-id="b057f-156">Den vil også være synlig i POS, som reference.</span><span class="sxs-lookup"><span data-stu-id="b057f-156">It will also be visible at the POS, for reference.</span></span>

<span data-ttu-id="b057f-157">Følg disse trin for at konfigurere tidsintervalfunktionen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b057f-157">To configure the time slot feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b057f-158">Gå til **Commerce** \> **Konfiguration af kanal** \> **Tidsinterval for afhentning i butik**.</span><span class="sxs-lookup"><span data-stu-id="b057f-158">Go to **Commerce** \> **Channel setup** \> **Store pickup time slot**.</span></span>
1. <span data-ttu-id="b057f-159">Vælg **Ny** for at oprette en ny tidsintervalskabelon.</span><span class="sxs-lookup"><span data-stu-id="b057f-159">Select **New** to create a new time slot template.</span></span> <span data-ttu-id="b057f-160">Hvis du vil bruge en eksisterende skabelon, skal du vælge skabelonen i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="b057f-160">To use an existing template, select the template in the left pane.</span></span>
1. <span data-ttu-id="b057f-161">Angiv værdier i felterne **Id for tidsinterval** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b057f-161">Enter values in the **Time Slot ID** and **Description** fields.</span></span>
1. <span data-ttu-id="b057f-162">Vælg **Tilføj** i oversigtspanelet **Ordreafhentning - Tidsindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="b057f-162">On the **Order Pickup - Time Settings** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="b057f-163">I dialogboksen **Ordreafhentning - Tidsindstillinger** skal du definere datointervallet, leveringsmåde, aktive leveringstimer, antal aktive dage, tidsinterval, slots pr. interval og andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b057f-163">In the **Order Pickup - Time Settings** dialog box, define the date range, mode of delivery, active hours of delivery, active days, time slot interval, slots per interval, and other settings.</span></span>

    <span data-ttu-id="b057f-164">Hvis tidsintervaller er statiske i en overskuelig fremtid, skal du lade feltet **Slutdato** være tomt.</span><span class="sxs-lookup"><span data-stu-id="b057f-164">If time slots will be static for the foreseeable future, leave the **End Date** field blank.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b057f-165">Du kan oprette flere skabeloner, men kun én skabelon kan knyttes til en enkelt kanal eller butik.</span><span class="sxs-lookup"><span data-stu-id="b057f-165">You can create multiple templates, but only one template can be associated with a single channel or store.</span></span>

    ![Dialogboksen Ordreafhentning - Tidsindstillinger](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. <span data-ttu-id="b057f-167">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="b057f-167">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="b057f-168">Hvis tidsintervallerne for en dag varierer, kan du oprette flere poster i oversigtspanelet **Ordreafhentning - Tidsindstillinger** for at sikre, at datoer og klokkeslæt ikke overlapper hinanden.</span><span class="sxs-lookup"><span data-stu-id="b057f-168">If the time slots in a day will vary, create additional entries on the **Order Pickup - Time Settings** FastTab to ensure that the dates and times don't overlap.</span></span>
1. <span data-ttu-id="b057f-169">I oversigtspanelet **Detailkanaler** skal du vælge **Tilføj** for at knytte skabelonen for tidsrubrikken til de butikker eller kanaler, hvor den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="b057f-169">On the **Retail Channels** FastTab, select **Add** to associate the time slot template with the stores or channels where it will be used.</span></span>
1. <span data-ttu-id="b057f-170">Brug pileknapperne eller vælg (eller fjern markeringen af) de butikker, områder og organisationer, skabelonen skal knyttes til, i dialogboksen **Vælg organisationsnoder**.</span><span class="sxs-lookup"><span data-stu-id="b057f-170">In the **Choose organization nodes** dialog box, use the arrow buttons to select (or clear the selection of) the stores, regions, and organizations that the template should be associated with.</span></span>

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. <span data-ttu-id="b057f-171">Vælg **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="b057f-171">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="b057f-172">På siden **Distributionstidsplan** skal du køre jobbene **1070** og **1135** for at synkronisere data til kanalerne.</span><span class="sxs-lookup"><span data-stu-id="b057f-172">On the **Distribution schedule** page, run the **1070** and **1135** jobs to sync the data to the channels.</span></span>

## <a name="time-slot-selection-for-pos-orders"></a><span data-ttu-id="b057f-173">Valg af tidsinterval for POS-ordrer</span><span class="sxs-lookup"><span data-stu-id="b057f-173">Time slot selection for POS orders</span></span>

<span data-ttu-id="b057f-174">Når en ordre eller en ordrelinje identificeres for afhentning i POS, kan kassereren vælge afhentningsbutik eller -lokalitet samt et dato- og klokkeslætsinterval.</span><span class="sxs-lookup"><span data-stu-id="b057f-174">At the POS, when an order or order line is identified for pickup, the cashier can select the pickup store or location, and a date and time slot.</span></span> <span data-ttu-id="b057f-175">Hvis en kunde har en afhentningsordre i en anden butik, kan kassereren vælge datoer, hvor varen til afhentning er tilgængelig i den pågældende butik.</span><span class="sxs-lookup"><span data-stu-id="b057f-175">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="b057f-176">Butiksopslaget giver en reference til datoerne og åbningstiderne.</span><span class="sxs-lookup"><span data-stu-id="b057f-176">The store lookup will provide a reference to the dates and store times.</span></span>

<span data-ttu-id="b057f-177">I følgende illustration vises et eksempel på valg af tidsinterval for en POS-ordre.</span><span class="sxs-lookup"><span data-stu-id="b057f-177">The following illustration shows an example of time slot selection for a POS order.</span></span>

![Et eksempel på valg af tidsinterval for en POS-ordre](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a><span data-ttu-id="b057f-179">Valg af tidsinterval for e-handelsordrer</span><span class="sxs-lookup"><span data-stu-id="b057f-179">Time slot selection for e-commerce orders</span></span>

<span data-ttu-id="b057f-180">Du kan finde oplysninger om, hvordan du kan gøre tidsinterval tilgængelig for e-handelsordrer, i [modulet med afhentningsoplysninger](../pickup-info-module.md).</span><span class="sxs-lookup"><span data-stu-id="b057f-180">For information about how to make time slot selection available for e-commerce orders, see [Pickup information module](../pickup-info-module.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b057f-181">Brugere kan kun få vist eller redigere tidsintervaller for afhentning på betalingssiden for en Commerce-websted, hvis modulet med oplysninger om afhentning er føjet til den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="b057f-181">Users can view or edit pickup time slots on a Commerce site's checkout page only if the pickup information module has been added to that page.</span></span> <span data-ttu-id="b057f-182">Hvis betalingssiden ikke indeholder modulet med afhentningsoplysninger, placeres ordrer, uden at brugerne får mulighed for at angive eller få vist oplysninger om tidsintervaller.</span><span class="sxs-lookup"><span data-stu-id="b057f-182">If the checkout page doesn't include the pickup information module, orders will be placed without letting users specify or view time slot information.</span></span>

<span data-ttu-id="b057f-183">I følgende illustration vises et eksempel på en e-handelsordre, hvor der er valgt et tidsinterval for afhentning.</span><span class="sxs-lookup"><span data-stu-id="b057f-183">The following illustration shows an example of an e-commerce order where a pickup time slot has been selected.</span></span>

![Eksempel på en e-handelsordre, hvor der er valgt et tidsinterval for afhentning](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="b057f-185">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b057f-185">Additional resources</span></span>

[<span data-ttu-id="b057f-186">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="b057f-186">Pickup information module</span></span>](../pickup-info-module.md)