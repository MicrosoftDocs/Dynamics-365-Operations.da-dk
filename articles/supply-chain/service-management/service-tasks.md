---
title: Oversigt over serviceopgaver
description: Du kan bruge serviceopgaver, når du skal beskrive den opgave, der skal fuldføres i forbindelse med en serviceordre. Både teknikere og kunder ser disse oplysninger.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebad3a5fdd65155eb822dcd69a1d2624a1891337
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835816"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="ed094-104">Oversigt over serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="ed094-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed094-105">Du kan bruge serviceopgaver, når du skal beskrive den opgave, der skal fuldføres i forbindelse med en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="ed094-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="ed094-106">Både teknikere og kunder ser disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="ed094-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="ed094-107">Du opretter serviceopgaver på siden **Serviceopgaver**, og du kan knytte serviceopgaver til en bestemt serviceaftale eller serviceordre ved at oprette serviceopgaverelationer.</span><span class="sxs-lookup"><span data-stu-id="ed094-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="ed094-108">Hver gang du opretter en serviceopgaverelation, kan du oprette følgende:</span><span class="sxs-lookup"><span data-stu-id="ed094-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="ed094-109">Interne noter til opgaven, f.eks. detaljerede oplysninger om tekniske krav til opgaven, som det er vigtigt, at teknikeren kender til.</span><span class="sxs-lookup"><span data-stu-id="ed094-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="ed094-110">Eksterne noter, der kan ses af kunden.</span><span class="sxs-lookup"><span data-stu-id="ed094-110">External notes that the customer can see.</span></span> <span data-ttu-id="ed094-111">Det kan f.eks. være en knap så teknisk beskrivelse af den opgave, der udføres i overensstemmelse med aftalen mellem kunden og servicefirmaet.</span><span class="sxs-lookup"><span data-stu-id="ed094-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="ed094-112">Når du har oprettet en serviceopgaverelation mellem en serviceopgave og en serviceordre eller serviceaftale, kan du angive denne serviceopgave, når du opretter serviceordrelinjer eller serviceaftalelinjer til den aktuelle serviceordre eller serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="ed094-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="ed094-113">Når du genererer serviceordrer fra en serviceaftale, kan du gruppere serviceordrelinjer i serviceordrer på basis af de serviceopgaver, der er tildelt de enkelte aftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="ed094-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="ed094-114">Oprette en serviceopgave</span><span class="sxs-lookup"><span data-stu-id="ed094-114">Create a service task</span></span>

1. <span data-ttu-id="ed094-115">Klik på **Servicestyring** \> **Opsætning** \> **Serviceopgaver**.</span><span class="sxs-lookup"><span data-stu-id="ed094-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="ed094-116">Opet en ny linje.</span><span class="sxs-lookup"><span data-stu-id="ed094-116">Create a new line.</span></span>
3. <span data-ttu-id="ed094-117">Angiv service-id og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ed094-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="ed094-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ed094-118">Example</span></span>

<span data-ttu-id="ed094-119">En tekniker skal udføre to job på en gearkasse (serviceobjekt GB-1234) hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="ed094-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="ed094-120">Der oprettes en serviceaftale til kunden, og flere konteringer knyttes til disse job.</span><span class="sxs-lookup"><span data-stu-id="ed094-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="ed094-121">Der er følgende serviceaftale og serviceaftalelinjer for de to job:</span><span class="sxs-lookup"><span data-stu-id="ed094-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="ed094-122">Serviceaftale</span><span class="sxs-lookup"><span data-stu-id="ed094-122">Service agreement</span></span>

| <span data-ttu-id="ed094-123">Project</span><span class="sxs-lookup"><span data-stu-id="ed094-123">Project</span></span> | <span data-ttu-id="ed094-124">Serviceaftale</span><span class="sxs-lookup"><span data-stu-id="ed094-124">Service agreement</span></span> | <span data-ttu-id="ed094-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed094-125">Description</span></span>                                  | <span data-ttu-id="ed094-126">Multi</span><span class="sxs-lookup"><span data-stu-id="ed094-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="ed094-127">9012</span><span class="sxs-lookup"><span data-stu-id="ed094-127">9012</span></span>    | <span data-ttu-id="ed094-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="ed094-128">000008\_001</span></span>       | <span data-ttu-id="ed094-129">Eftersyn og rutinemæssig udskiftning – GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="ed094-130">Løntillæg</span><span class="sxs-lookup"><span data-stu-id="ed094-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="ed094-131">Serviceaftalelinjer</span><span class="sxs-lookup"><span data-stu-id="ed094-131">Service agreement lines</span></span>

| <span data-ttu-id="ed094-132">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed094-132">Description</span></span>             | <span data-ttu-id="ed094-133">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="ed094-133">Transaction type</span></span> | <span data-ttu-id="ed094-134">Seriviceobjekt</span><span class="sxs-lookup"><span data-stu-id="ed094-134">Service object</span></span> | <span data-ttu-id="ed094-135">Serviceopgave</span><span class="sxs-lookup"><span data-stu-id="ed094-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="ed094-136">Eftersyn og rensning</span><span class="sxs-lookup"><span data-stu-id="ed094-136">Inspection and cleaning</span></span> | <span data-ttu-id="ed094-137">Time</span><span class="sxs-lookup"><span data-stu-id="ed094-137">Hour</span></span>             | <span data-ttu-id="ed094-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-138">GB-1234</span></span>        | <span data-ttu-id="ed094-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-139">I/C - GB1234</span></span> |
| <span data-ttu-id="ed094-140">Transport</span><span class="sxs-lookup"><span data-stu-id="ed094-140">Travel</span></span>                  | <span data-ttu-id="ed094-141">Expense</span><span class="sxs-lookup"><span data-stu-id="ed094-141">Expense</span></span>          | <span data-ttu-id="ed094-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-142">GB-1234</span></span>        | <span data-ttu-id="ed094-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-143">I/C - GB1234</span></span> |
| <span data-ttu-id="ed094-144">Materialer</span><span class="sxs-lookup"><span data-stu-id="ed094-144">Materials</span></span>               | <span data-ttu-id="ed094-145">Post</span><span class="sxs-lookup"><span data-stu-id="ed094-145">Item</span></span>             | <span data-ttu-id="ed094-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-146">GB-1234</span></span>        | <span data-ttu-id="ed094-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-147">I/C - GB1234</span></span> |
| <span data-ttu-id="ed094-148">Rutinemæssig udskiftning</span><span class="sxs-lookup"><span data-stu-id="ed094-148">Routine replacement</span></span>     | <span data-ttu-id="ed094-149">Time</span><span class="sxs-lookup"><span data-stu-id="ed094-149">Hour</span></span>             | <span data-ttu-id="ed094-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-150">GB-1234</span></span>        | <span data-ttu-id="ed094-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-151">RR - GB1234</span></span>  |
| <span data-ttu-id="ed094-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="ed094-152">GR-1</span></span>                    | <span data-ttu-id="ed094-153">Post</span><span class="sxs-lookup"><span data-stu-id="ed094-153">Item</span></span>             | <span data-ttu-id="ed094-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-154">GB-1234</span></span>        | <span data-ttu-id="ed094-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-155">RR - GB1234</span></span>  |
| <span data-ttu-id="ed094-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="ed094-156">GR-5</span></span>                    | <span data-ttu-id="ed094-157">Post</span><span class="sxs-lookup"><span data-stu-id="ed094-157">Item</span></span>             | <span data-ttu-id="ed094-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-158">GB-1234</span></span>        | <span data-ttu-id="ed094-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-159">RR - GB1234</span></span>  |

<span data-ttu-id="ed094-160">Serviceaftalelinjerne for de to job har to tilknyttede serviceopgaver.</span><span class="sxs-lookup"><span data-stu-id="ed094-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="ed094-161">Serviceopgaverne bestemmer, hvilke transaktioner der er forbundet med hvert job.</span><span class="sxs-lookup"><span data-stu-id="ed094-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="ed094-162">I det første tilfælde identificerer serviceopgaven I/C - GB1234 alle de serviceaftalelinjer, der indgår i eftersynet og rensningen af objektet GB-1234.</span><span class="sxs-lookup"><span data-stu-id="ed094-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="ed094-163">I det andet tilfælde identificerer serviceordren R - GB1234 alle de serviceaftalelinjer, der indgår i fuldførelse af en rutinemæssig udskiftning.</span><span class="sxs-lookup"><span data-stu-id="ed094-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="ed094-164">Følgende serviceopgaverelationer udgør forbindelsen mellem serviceopgaverne og den bestemte aftale:</span><span class="sxs-lookup"><span data-stu-id="ed094-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="ed094-165">Serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="ed094-165">Service tasks</span></span>

| <span data-ttu-id="ed094-166">Serviceopgave</span><span class="sxs-lookup"><span data-stu-id="ed094-166">Service task</span></span> | <span data-ttu-id="ed094-167">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed094-167">Description</span></span>                             | <span data-ttu-id="ed094-168">Intern note</span><span class="sxs-lookup"><span data-stu-id="ed094-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="ed094-169">Ekstern note</span><span class="sxs-lookup"><span data-stu-id="ed094-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="ed094-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-170">I/C - GB1234</span></span> | <span data-ttu-id="ed094-171">Eftersyn af gearkasse GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="ed094-172">Visuelt og mekanisk eftersyn og rensning af gearkasse GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="ed094-173">Rutinemæssigt eftersyn af gearkasse</span><span class="sxs-lookup"><span data-stu-id="ed094-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="ed094-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="ed094-174">RR - GB1234</span></span>  | <span data-ttu-id="ed094-175">Rutinemæssig udskiftning af dele i GB-1234</span><span class="sxs-lookup"><span data-stu-id="ed094-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="ed094-176">Rutinemæssig udskiftning af komponenterne GR-1 GR-5 (i gearkasser, der er produceret før 2002, skal komponenten GR-2 også udskiftes)</span><span class="sxs-lookup"><span data-stu-id="ed094-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="ed094-177">Rutinemæssig udskiftning af dele</span><span class="sxs-lookup"><span data-stu-id="ed094-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="ed094-178">Gruppere serviceordrer</span><span class="sxs-lookup"><span data-stu-id="ed094-178">Group service orders</span></span>

<span data-ttu-id="ed094-179">Når der oprettes serviceordrer automatisk, kan du bruge serviceopgaver som grupperingskriterium.</span><span class="sxs-lookup"><span data-stu-id="ed094-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="ed094-180">Hvis du vil gruppere serviceordrer efter serviceopgaver, skal det angives i serviceaftalen, at serviceordrer, der er baseret på serviceaftalen, skal grupperes efter serviceopgavens id som første grupperingskriterium.</span><span class="sxs-lookup"><span data-stu-id="ed094-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="ed094-181">**Gruppere efter serviceopgave**</span><span class="sxs-lookup"><span data-stu-id="ed094-181">**Group by service task**</span></span>

1. <span data-ttu-id="ed094-182">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="ed094-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="ed094-183">Under fanen **Opsætning** skal du vælge **Efter serviceopgave** i feltet **Kombinere serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="ed094-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]