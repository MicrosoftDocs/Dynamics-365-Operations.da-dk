---
title: Serviceordrer
description: En serviceordre repræsenterer en serviceteknikers besøg hos en kunde på en bestemt dato.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e9825dbd4ebe05b2efb590f491b3b54e68ec5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010466"
---
# <a name="service-orders"></a><span data-ttu-id="967d4-103">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="967d4-104">En serviceordre repræsenterer en serviceteknikers besøg hos en kunde på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="967d4-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="967d4-105">Hver serviceordre består af en eller flere serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="967d4-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="967d4-106">Serviceordrelinjer repræsenterer de arbejdstimer, der skal udføres af serviceteknikeren, og de relaterede varer, omkostninger og gebyrer.</span><span class="sxs-lookup"><span data-stu-id="967d4-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="967d4-107">Du kan knytte opgaver og objekter til en serviceordrelinje.</span><span class="sxs-lookup"><span data-stu-id="967d4-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="967d4-108">Du kan derefter gruppere serviceordrelinjer efter opgave eller objekt.</span><span class="sxs-lookup"><span data-stu-id="967d4-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="967d4-109">Du kan også knytte varer, der findes på lagerlisten, til serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="967d4-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="967d4-110">Oprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-110">Create service orders</span></span>

<span data-ttu-id="967d4-111">Du kan oprette serviceordrer på basis af en serviceaftale og linjerne i den pågældende aftale.</span><span class="sxs-lookup"><span data-stu-id="967d4-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="967d4-112">Du kan dog kun oprette serviceordrer, der er tilknyttet en serviceaftale, i den periode, der er angivet i aftalen.</span><span class="sxs-lookup"><span data-stu-id="967d4-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="967d4-113">Hvis en serviceaftale f.eks. er gyldig for kalenderåret 2011, kan du oprette serviceordrer for aftalen fra 1. januar 2011 og 31. december 2011.</span><span class="sxs-lookup"><span data-stu-id="967d4-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="967d4-114">Du kan også oprette serviceordrer individuelt, uden at knytte dem til en aftale.</span><span class="sxs-lookup"><span data-stu-id="967d4-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="967d4-115">Disse serviceordrer kan bruges til at håndtere ikke-planlagt eller enkeltstående servicebesøg.</span><span class="sxs-lookup"><span data-stu-id="967d4-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="967d4-116">I marts måned beslutter din kunde sig f.eks. for at få udført service på to maskiner ud over dem, der er angivet i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="967d4-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="967d4-117">Til denne opgave skal du oprette serviceordrer, men de skal ikke knyttes til en aftale.</span><span class="sxs-lookup"><span data-stu-id="967d4-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="967d4-118">Hvis du vil oprette serviceordrer, der ikke der er tilknyttet en serviceaftale, skal du markere afkrydsningsfeltet <STRONG>Tillad uden serviceaftale</STRONG> i formularen <STRONG>Parametre for servicestyring</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="967d4-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="967d4-119">**Scenario**</span><span class="sxs-lookup"><span data-stu-id="967d4-119">**Scenario**</span></span>

<span data-ttu-id="967d4-120">I følgende scenario beskrives en anden situation, hvor det er praktisk at oprette en serviceordre, der ikke er knyttet til en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="967d4-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="967d4-121">Firmadispatcheren modtager et opkald om hasteservice for en elevator.</span><span class="sxs-lookup"><span data-stu-id="967d4-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="967d4-122">Der er ikke tid til at oprette en serviceaftale og et projekt for servicen.</span><span class="sxs-lookup"><span data-stu-id="967d4-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="967d4-123">Derfor opretter afsenderen en serviceordre direkte i formularen **Serviceordrer**, vedhæfter serviceordren til et eksisterende projekt og opretter serviceordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="967d4-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="967d4-124">Afsenderen opretter også en opgave- eller objektrelation for en eksisterende serviceordre for at registrere arbejde, der ikke er relateret til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="967d4-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="967d4-125">Du kan finde flere oplysninger under [Oprette serviceordrer manuelt](create-service-orders-manually.md) og [Oprette serviceopgaverelationer](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="967d4-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="967d4-126">Overvåge status for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="967d4-127">Hvis du vil overvåge status for en salgsordre via gennem de forskellige teams og arbejdsprocesser, kan du opretteet system over trin og årsagskoder for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="967d4-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="967d4-128">Du kan angive de handlinger, der er tilladt for hvert trin.</span><span class="sxs-lookup"><span data-stu-id="967d4-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="967d4-129">Du kan finde flere oplysninger under [Oprette årsagskoder](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="967d4-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="967d4-130">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="967d4-130">**Example**</span></span>

<span data-ttu-id="967d4-131">En serviceordre godkendes af afsenderen.</span><span class="sxs-lookup"><span data-stu-id="967d4-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="967d4-132">Afsenderen opdaterer serviceordretrinnet og angiver en årsagskode, som angiver, at serviceordren er blevet frigivet til serviceteknikeren.</span><span class="sxs-lookup"><span data-stu-id="967d4-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="967d4-133">Serviceteknikeren besøger kunden og udfører servicen.</span><span class="sxs-lookup"><span data-stu-id="967d4-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="967d4-134">Angive varebehov til serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="967d4-135">Du kan angive de lagervarer, der er nødvendige til serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="967d4-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="967d4-136">Serviceordren skal dog være tilknyttet et projekt.</span><span class="sxs-lookup"><span data-stu-id="967d4-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="967d4-137">Varebehov til serviceordrer behandles løbende igennem et projekt.</span><span class="sxs-lookup"><span data-stu-id="967d4-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="967d4-138">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="967d4-138">**Example**</span></span>

<span data-ttu-id="967d4-139">De serviceordrer, der oprettes ud fra serviceaftalen, behandles derefter af afsenderen.</span><span class="sxs-lookup"><span data-stu-id="967d4-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="967d4-140">På den første serviceordre kan afsenderen se, at serviceteknikeren skal bruge en vigtig reservedel, der ikke findes på lageret.</span><span class="sxs-lookup"><span data-stu-id="967d4-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="967d4-141">Afsenderen opretter derfor et varebehov for reservedelen direkte ud fra serviceordren.</span><span class="sxs-lookup"><span data-stu-id="967d4-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="967d4-142">Flytte og bogføre linjer</span><span class="sxs-lookup"><span data-stu-id="967d4-142">Move and post lines</span></span>

<span data-ttu-id="967d4-143">En servicetekniker returnerer fra et servicebesøg og ændrer og opdaterer derefter serviceordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="967d4-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="967d4-144">Under servicebesøget udførte teknikeren et servicejob, der var planlagt til næste servicebesøg.</span><span class="sxs-lookup"><span data-stu-id="967d4-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="967d4-145">Derfor flytter teknikeren linjerne fra det næste servicebesøg til det aktuelle servicebesøg.</span><span class="sxs-lookup"><span data-stu-id="967d4-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="967d4-146">Teknikeren bogfører derefter serviceordren.</span><span class="sxs-lookup"><span data-stu-id="967d4-146">The technician then posts the service order.</span></span> <span data-ttu-id="967d4-147">Du kan finde flere oplysninger under [Flytte serviceordrelinjer](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="967d4-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="967d4-148">Annuller serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-148">Cancel service orders</span></span>

<span data-ttu-id="967d4-149">En af de andre serviceordrer, der blev oprettet for januar måned, bliver forældet, fordi jobbet er annulleret.</span><span class="sxs-lookup"><span data-stu-id="967d4-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="967d4-150">Serviceafsenderen annullerer derfor serviceordren.</span><span class="sxs-lookup"><span data-stu-id="967d4-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="967d4-151">Du kan finde flere oplysninger under [Annullere serviceordrer](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="967d4-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="967d4-152">Bogføre fra projekter</span><span class="sxs-lookup"><span data-stu-id="967d4-152">Post from projects</span></span>

<span data-ttu-id="967d4-153">I slutningen af ugen ønsker afsenderen at bogføre alle serviceordrer, der er knyttet til et bestemt projekt.</span><span class="sxs-lookup"><span data-stu-id="967d4-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="967d4-154">Afsenderen finder derfor det relevante projekt i formularen **Projekter** og bogfører de fuldførte serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="967d4-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="967d4-155">Du kan finde flere oplysninger under [Bogføre serviceordrer (klasseformular)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="967d4-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="967d4-156">Slet serviceordrer</span><span class="sxs-lookup"><span data-stu-id="967d4-156">Delete service orders</span></span>

<span data-ttu-id="967d4-157">I løbet af anden halvdel af året beslutter kunden sig for, at servicebesøgene ikke sker ofte nok.</span><span class="sxs-lookup"><span data-stu-id="967d4-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="967d4-158">Du skal oprette en ny række af mere hyppige servicebesøg for den resterende tid i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="967d4-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="967d4-159">Du skal derfor slette de eksisterende oprettede serviceordrer og oprette nye serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="967d4-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="967d4-160">Du kan finde flere oplysninger under [Slette serviceordrer](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="967d4-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="967d4-161">Se også</span><span class="sxs-lookup"><span data-stu-id="967d4-161">See also</span></span>

<span data-ttu-id="967d4-162">[Serviceordrer (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="967d4-162">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


