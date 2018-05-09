---
title: Intervaller for service
description: "Serviceintervallet angiver den frekvens, hvormed serviceordrelinjer oprettes til serviceaftalelinjer, når du opretter serviceordrer."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 96443a8135a0a12ae23895c4ceac4da626fd96fa
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="service-intervals"></a><span data-ttu-id="0b99a-103">Intervaller for service</span><span class="sxs-lookup"><span data-stu-id="0b99a-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b99a-104">Serviceaftaleintervallet angiver den frekvens, hvormed serviceordrelinjer oprettes til serviceaftalelinjer, når du opretter serviceordrer automatisk.</span><span class="sxs-lookup"><span data-stu-id="0b99a-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="0b99a-105">Når du opretter serviceordrer automatisk, oprettes serviceordrelinjer i henhold til det interval, du har angivet for serviceaftalelinjen, fra startdatoen for aftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="0b99a-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="0b99a-106">Hvis feltet **Interval** i en serviceaftalelinje på siden **Serviceaftaler** er tomt, er linjen en engangshændelse, og den bruges ikke gentagne gange til at oprette serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="0b99a-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="0b99a-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0b99a-107">Example</span></span>

<span data-ttu-id="0b99a-108">Dette eksempel viser, hvordan et serviceinterval påvirker serviceaftalelinjer og serviceordrelinjer på en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="0b99a-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="0b99a-109">Oprette en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="0b99a-109">Create a service agreement</span></span>

<span data-ttu-id="0b99a-110">Først skal du oprette en serviceaftale og vælge **Efter serviceaftale** i indstillingen **Kombinere serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="0b99a-111">Klik på **Serviceaftaler**</span><span class="sxs-lookup"><span data-stu-id="0b99a-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="0b99a-112">Klik på **Serviceaftale** i gruppen **Ny** under fanen **Serviceaftale** i **Handlingsrude** for at oprette en ny serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="0b99a-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="0b99a-113">Indtast en beskrivelse, vælg et projekt i feltet **Projekt-id**, og angiv en dato i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="0b99a-114">I feltet **Kombinere serviceordrer** skal du vælge **Efter serviceaftale**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="0b99a-115">Du har nu oprettet følgende serviceaftale:</span><span class="sxs-lookup"><span data-stu-id="0b99a-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="0b99a-116">Project</span><span class="sxs-lookup"><span data-stu-id="0b99a-116">Project</span></span>      | <span data-ttu-id="0b99a-117">Startdato</span><span class="sxs-lookup"><span data-stu-id="0b99a-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b99a-118">Dit projekt</span><span class="sxs-lookup"><span data-stu-id="0b99a-118">Your project</span></span> | <span data-ttu-id="0b99a-119">Den dato, du har angivet for projektet.</span><span class="sxs-lookup"><span data-stu-id="0b99a-119">The date you specified for the project.</span></span> <span data-ttu-id="0b99a-120">I dette eksempel bruges den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="0b99a-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="0b99a-121">Oprette en serviceaftalelinje</span><span class="sxs-lookup"><span data-stu-id="0b99a-121">Create a service agreement line</span></span>

<span data-ttu-id="0b99a-122">Derefter skal du oprette en serviceaftalelinje med posteringstypen **Time**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="0b99a-123">For at fuldføre denne del af eksemplet skal du oprette et serviceinterval på 10 dage på siden **Intervaller for service**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="0b99a-124">Vælg den serviceaftale, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="0b99a-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="0b99a-125">I oversigtspanelet **Linjer** skal du klikke på knappen **Tilføj** for at oprette en ny linje i nederste rude på siden **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="0b99a-126">Vælg **Time** i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="0b99a-127">Vælg den arbejder, der skal udføre serviceydelsen, i feltet **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="0b99a-128">Vælg intervallet på 10 dage i feltet **Serviceinterval**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="0b99a-129">Nu har du oprettet en serviceaftalelinje med følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0b99a-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="0b99a-130">Posteringstype</span><span class="sxs-lookup"><span data-stu-id="0b99a-130">Transaction type</span></span> | <span data-ttu-id="0b99a-131">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="0b99a-131">Start date</span></span>                               | <span data-ttu-id="0b99a-132">Serviceinterval</span><span class="sxs-lookup"><span data-stu-id="0b99a-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="0b99a-133">Time</span><span class="sxs-lookup"><span data-stu-id="0b99a-133">Hour</span></span>             | <span data-ttu-id="0b99a-134">Dags dato.</span><span class="sxs-lookup"><span data-stu-id="0b99a-134">The current date.</span></span>                        | <span data-ttu-id="0b99a-135">Hver 10. dag</span><span class="sxs-lookup"><span data-stu-id="0b99a-135">Every 10 days</span></span>    |
| <span data-ttu-id="0b99a-136">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="0b99a-136">Worker</span></span>           | <span data-ttu-id="0b99a-137">Arbejder, der vil udføre serviceydelsen.</span><span class="sxs-lookup"><span data-stu-id="0b99a-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="0b99a-138">Der er ikke angivet et tidsvindue for linjen.</span><span class="sxs-lookup"><span data-stu-id="0b99a-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="0b99a-139">Oprette planlagte serviceordrer</span><span class="sxs-lookup"><span data-stu-id="0b99a-139">Create planned service orders</span></span>

<span data-ttu-id="0b99a-140">Du kan nu oprette planlagte serviceordrer og serviceordrelinjer for den kommende måned.</span><span class="sxs-lookup"><span data-stu-id="0b99a-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="0b99a-141">På siden **Serviceaftaler** skal du klikke på **Planlagte serviceordrer** under fanen **Levér** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="0b99a-142">På siden **Oprette serviceordrer** skal du indtaste dags dato i feltet **Fra-dato**, og i feltet **Til-dato** skal du indtaste en dato en måned fra dags dato.</span><span class="sxs-lookup"><span data-stu-id="0b99a-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="0b99a-143">Indstil **Time**-skyderen til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="0b99a-144">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-144">Click **OK**.</span></span>

<span data-ttu-id="0b99a-145">Da der ikke er nogen gruppering i serviceordren (defineret af indstillingen **Efter serviceaftale** i feltet **Kombinere serviceordrer**), oprettes der en serviceordrelinje pr. serviceordre.</span><span class="sxs-lookup"><span data-stu-id="0b99a-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="0b99a-146">Oprettede serviceordrer</span><span class="sxs-lookup"><span data-stu-id="0b99a-146">Service orders created</span></span>

<span data-ttu-id="0b99a-147">Der er oprettet tre serviceordrelinjer inden for den tidsramme, du har angivet i dialogboksen **Opret serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="0b99a-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="0b99a-148">Du kan få vist serviceordrelinjerne på siden **Serviceaftaler** (**Handlingsrude** \> fanen **Levér** \>**Vis**-knappen).</span><span class="sxs-lookup"><span data-stu-id="0b99a-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b99a-149">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="0b99a-149">Related topics</span></span>

[<span data-ttu-id="0b99a-150">Oprette serviceintervaller</span><span class="sxs-lookup"><span data-stu-id="0b99a-150">Set up service intervals</span></span>](set-up-service-intervals.md)  


