---
title: Oprette serviceopgaverelationer
description: Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470724"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="1b0ad-103">Oprette serviceopgaverelationer</span><span class="sxs-lookup"><span data-stu-id="1b0ad-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b0ad-104">Du kan knytte serviceopgaver til serviceaftaler eller serviceordrer for at beskrive den serviceopgave, der skal udføres for aftalen eller ordren.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="1b0ad-105">Disse oplysninger er tilgængelige for serviceteknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="1b0ad-106">Oprette en relation med en serviceaftale</span><span class="sxs-lookup"><span data-stu-id="1b0ad-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="1b0ad-107">Gå til **Servicestyring** \> **Fælles** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="1b0ad-108">Vælg en eksisterende serviceaftale, eller opret en ny.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="1b0ad-109">Vælg knappen **Serviceopgaver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="1b0ad-110">Vælg **Ny** i formularen **Serviceopgaver** for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaven til serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="1b0ad-111">Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="1b0ad-112">Luk formen for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-112">Close the form to save the record.</span></span>

<span data-ttu-id="1b0ad-113">Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="1b0ad-114">Du kan nu angive disse serviceaftaler for alle tilknyttede aftalelinjer.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="1b0ad-115">En serviceopgaverelation, der oprettes til en serviceaftale, kan vælges fra alle de serviceordrer, der er tilknyttet serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="1b0ad-116">Oprette en relation med en serviceordre</span><span class="sxs-lookup"><span data-stu-id="1b0ad-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="1b0ad-117">Gå til **Servicestyring** \> **Almindelige** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="1b0ad-118">Vælg en eksisterende serviceordre, eller opret en ny.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="1b0ad-119">Vælg knappen **Serviceopgaver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="1b0ad-120">Vælg **Ny** i formularen **Serviceopgaver** for at oprette en ny linje, og vælg derefter en serviceopgave på listen **Serviceopgave** for at knytte serviceopgaverne til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="1b0ad-121">Angiv beskrivelser af evt. interne eller eksterne noter i fritekstfelterne under fanen **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="1b0ad-122">Luk formen for at gemme posten.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-122">Close the form to save the record.</span></span>

<span data-ttu-id="1b0ad-123">Gentag denne procedure, indtil du har oprettet alle nødvendige serviceopgaverelationer for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="1b0ad-124">Du kan nu vælge den serviceopgave, du har oprettet relationen for, når du opretter serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="1b0ad-125">Serviceopgaverelationer, der oprettes til en serviceordre, kan vælges i den specifikke serviceordre.</span><span class="sxs-lookup"><span data-stu-id="1b0ad-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b0ad-126">Se også</span><span class="sxs-lookup"><span data-stu-id="1b0ad-126">See also</span></span>

[<span data-ttu-id="1b0ad-127">Oversigt over serviceopgaver</span><span class="sxs-lookup"><span data-stu-id="1b0ad-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]