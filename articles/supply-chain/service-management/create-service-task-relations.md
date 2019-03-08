---
title: Oprette serviceopgaverelationer
description: Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aa0e5200ff2a6822e631c72124335e2dc556c14
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "317194"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="f9bf3-103">Oprette serviceopgaverelationer</span><span class="sxs-lookup"><span data-stu-id="f9bf3-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9bf3-104">Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="f9bf3-105">Disse oplysninger er tilgængelige for serviceteknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="f9bf3-106">Oprette en relation med en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="f9bf3-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="f9bf3-107">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="f9bf3-108">Vælg en eksisterende serviceaftale, eller opret en ny.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="f9bf3-109">Klik på knappen **Serviceopgaver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="f9bf3-110">Tryk på CTRL+N i formularen **Serviceopgaver** for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaven til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="f9bf3-111">Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="f9bf3-112">Luk formen for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-112">Close the form to save the record.</span></span>

<span data-ttu-id="f9bf3-113">Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="f9bf3-114">Du kan nu angive disse serviceaftaler for alle tilknyttede aftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="f9bf3-115">En serviceopgaverelation, der oprettes til en serviceaftale, kan vælges fra alle de serviceordrer, der er tilknyttet serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="f9bf3-116">Oprette en relation med en serviceordre</span><span class="sxs-lookup"><span data-stu-id="f9bf3-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="f9bf3-117">Klik på **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f9bf3-118">Vælg en eksisterende serviceordre, eller opret en ny.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="f9bf3-119">Klik på knappen **Serviceopgaver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="f9bf3-120">Tryk i formularen **Serviceopgaver** på CTRL+N for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaver til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="f9bf3-121">Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="f9bf3-122">Luk formen for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-122">Close the form to save the record.</span></span>

<span data-ttu-id="f9bf3-123">Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="f9bf3-124">Du kan nu vælge den serviceopgave, du har oprettet relationen for, når du opretter serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="f9bf3-125">Serviceopgaverelationer, der oprettes til en serviceordre, kan vælges i den specifikke serviceordre.</span><span class="sxs-lookup"><span data-stu-id="f9bf3-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9bf3-126">Se også</span><span class="sxs-lookup"><span data-stu-id="f9bf3-126">See also</span></span>

[<span data-ttu-id="f9bf3-127">Serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="f9bf3-127">Service tasks</span></span>](service-tasks.md)


  


