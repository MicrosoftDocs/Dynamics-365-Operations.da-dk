---
title: Oversigt over udvikling og udfyldelse af serviceaftaler
description: Med serviceaftaler kan du definere de ressourcer, der bruges under et typisk servicebesøg, og hvordan disse ressourcer faktureres til kunden.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd17cc0304d58d27afe2cededa5bc0b96557b5e9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424717"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="c781f-103">Oversigt over udvikling og udfyldelse af serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="c781f-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c781f-104">Med serviceaftaler kan du definere de ressourcer, der bruges under et typisk servicebesøg, og hvordan disse ressourcer faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="c781f-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="c781f-105">Alle serviceaftaler er knyttet til projekter, som posteringer bogføres og faktureres gennem.</span><span class="sxs-lookup"><span data-stu-id="c781f-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="c781f-106">Men du kan også fakturere serviceordreposteringer direkte gennem projektet uden først at skulle knytte serviceordren til en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="c781f-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="c781f-107">Det kan du beslutte dig for at gøre, hvis serviceordren gælder et enkeltstående servicebesøg, og behovet for at behandle serviceposteringer hurtigt opvejer behovet for at vedligeholde detaljerede oplysninger i en serviceaftale om kunden over en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="c781f-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="c781f-108">Serviceaftale</span><span class="sxs-lookup"><span data-stu-id="c781f-108">Service agreement</span></span>

<span data-ttu-id="c781f-109">I de enkelte serviceaftaler skal du angive et projekt, et serviceaftale-id og en serviceaftalegruppe.</span><span class="sxs-lookup"><span data-stu-id="c781f-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="c781f-110">Serviceaftalegruppen kan bruges til at sortere og organisere serviceaftaler.</span><span class="sxs-lookup"><span data-stu-id="c781f-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="c781f-111">Et serviceaftalehoved indeholder indstillinger, der gælder for alle tilknyttede aftalelinjer:</span><span class="sxs-lookup"><span data-stu-id="c781f-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="c781f-112">Hvorvidt serviceaftalen er suspenderet.</span><span class="sxs-lookup"><span data-stu-id="c781f-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="c781f-113">Hvis serviceaftalen er suspenderet, kan du ikke oprette serviceordrer ud fra serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="c781f-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="c781f-114">Serviceaftalens varighed.</span><span class="sxs-lookup"><span data-stu-id="c781f-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="c781f-115">Hvordan serviceordrelinjer skal samles i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="c781f-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="c781f-116">Hvorvidt serviceaftalen er en skabelon.</span><span class="sxs-lookup"><span data-stu-id="c781f-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="c781f-117">I sidehovedet til serviceaftalen skal du også angive alle de serviceobjekter og serviceopgaver, der kan bruges sammen med serviceaftalen ved at angive den specifikke serviceopgave eller det specifikke serviceobjekt, der skal knyttes til linjerne i aftalen.</span><span class="sxs-lookup"><span data-stu-id="c781f-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="c781f-118">Fra sidehovedet til serviceaftalen kan du også kopiere serviceaftalelinjer eller serviceskabelonlinjer til den aktuelle serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="c781f-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="c781f-119">Du kan suspendere serviceaftaler og stoppe individuelle serviceaftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="c781f-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="c781f-120">Hvis du markerer afkrydsningsfeltet **Suspenderet** i en serviceaftale, kan du ikke:</span><span class="sxs-lookup"><span data-stu-id="c781f-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="c781f-121">Oprette serviceordrer automatisk eller manuelt fra serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="c781f-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="c781f-122">Hvis du markerer afkrydsningsfeltet **Stoppet** på en linje i serviceaftalen, kan du ikke:</span><span class="sxs-lookup"><span data-stu-id="c781f-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="c781f-123">Oprette serviceordrer automatisk eller manuelt fra serviceaftalelinjen.</span><span class="sxs-lookup"><span data-stu-id="c781f-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="c781f-124">Kopiere serviceaftalelinjen til en anden serviceaftale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="c781f-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="c781f-125">Hvis en serviceaftale suspenderes, stoppes alle tilknyttede linjer uanset deres individuelle status.</span><span class="sxs-lookup"><span data-stu-id="c781f-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="c781f-126">Serviceaftalelinjer</span><span class="sxs-lookup"><span data-stu-id="c781f-126">Service-agreement lines</span></span>

<span data-ttu-id="c781f-127">Serviceaftalelinjerne indeholder en detaljeret beskrivelse af indholdet af det foreslåede servicearbejde.</span><span class="sxs-lookup"><span data-stu-id="c781f-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="c781f-128">Linjerne indeholder følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="c781f-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="c781f-129">Posteringstypen og en beskrivelse af posteringstypen.</span><span class="sxs-lookup"><span data-stu-id="c781f-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="c781f-130">Den medarbejder, der udfører servicearbejdet.</span><span class="sxs-lookup"><span data-stu-id="c781f-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="c781f-131">De objekter, servicen skal udføres på for serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="c781f-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="c781f-132">Den hyppighed, arbejdet udføres med, og tilknyttede vare-, udgifts- og gebyrposteringer registreres.</span><span class="sxs-lookup"><span data-stu-id="c781f-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="c781f-133">Det tidsvindue, hvor serviceordrelinjer kan grupperes i en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="c781f-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="c781f-134">Serviceopgaver bruges til at gruppere flere sæt aftalelinjer sammen i arbejdsopgaver og til at give servicemedarbejdere og kunder en overordnet beskrivelse af, hvilken serviceopgave der skal udføres.</span><span class="sxs-lookup"><span data-stu-id="c781f-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="c781f-135">Hvorvidt en linje er standset.</span><span class="sxs-lookup"><span data-stu-id="c781f-135">Whether a line is stopped.</span></span> <span data-ttu-id="c781f-136">Hvis en linje er standset, kan du ikke oprette serviceordrer for den pågældende linje.</span><span class="sxs-lookup"><span data-stu-id="c781f-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="c781f-137">Projektindstillinger som kategori og linjeegenskab.</span><span class="sxs-lookup"><span data-stu-id="c781f-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c781f-138">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="c781f-138">Related topics</span></span>

[<span data-ttu-id="c781f-139">Oprette serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="c781f-139">Create service agreements</span></span>](create-service-agreements.md)
