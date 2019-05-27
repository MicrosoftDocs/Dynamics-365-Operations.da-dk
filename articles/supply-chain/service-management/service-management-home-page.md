---
title: Servicestyring
description: Du kan bruge Servicestyring til at udarbejde serviceaftaler og serviceabonnementer, håndtere serviceordrer og kundeforespørgsler samt administrere og analysere leveringen af tjenester til kunder.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562597"
---
# <a name="service-management"></a><span data-ttu-id="4b5d0-103">Servicestyring</span><span class="sxs-lookup"><span data-stu-id="4b5d0-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4b5d0-104">Du kan bruge **Servicestyring** til at udarbejde serviceaftaler og serviceabonnementer, håndtere serviceordrer og kundeforespørgsler samt administrere og analysere leveringen af tjenester til kunder.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="4b5d0-105">Du kan bruge serviceaftaler til at definere de ressourcer, der bruges under et typisk servicebesøg.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="4b5d0-106">Du kan også bruges serviceaftaler til at få vist, hvordan disse ressourcer faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="4b5d0-107">En serviceaftale kan også inkludere en serviceniveauaftale, der angiver standardsvartider og inkluderer værktøjer til registrering af den faktiske tid.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="4b5d0-108">Du kan oprette serviceordrer til administrering af oplysninger om planlagte og ikke-planlagte besøg af en servicetekniker hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="4b5d0-109">Serviceordrer inkluderer oplysninger, som f.eks.:</span><span class="sxs-lookup"><span data-stu-id="4b5d0-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="4b5d0-110">De arbejdstimer, som servicetekniker skal bruge</span><span class="sxs-lookup"><span data-stu-id="4b5d0-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="4b5d0-111">Service- eller reparationstypen</span><span class="sxs-lookup"><span data-stu-id="4b5d0-111">The type of service or repair</span></span>

3.  <span data-ttu-id="4b5d0-112">Det objekt, der skal repareres, inklusive oplysninger om symptomer og diagnose</span><span class="sxs-lookup"><span data-stu-id="4b5d0-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="4b5d0-113">Eventuelle udgifter og gebyrer, der er relateret til servicen eller reparationen</span><span class="sxs-lookup"><span data-stu-id="4b5d0-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="4b5d0-114">Du kan modtage, behandle og ekspedere serviceanmodninger.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="4b5d0-115">Når du har oprettet en serviceordre, kan du bruge servicestadier til at overvåge status og angive regler, der bestemmer, hvilke handlinger der er aktiveret i hvert af stadierne.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="4b5d0-116">Når en serviceordre er færdig, kan du afslutte ordren for at bekræfte, at den er færdig, og derefter bogføre ordren for at starte fakturaprocessen.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="4b5d0-117">Brug rapporteringsværktøjerne til at overvåge serviceordremargener og abonnementstransaktioner samt udskrive arbejdsbeskrivelser og arbejdskvitteringer.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="4b5d0-118">Forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="4b5d0-118">Business processes</span></span>

<span data-ttu-id="4b5d0-119">I følgende diagram illustreres forretningsprocesserne på højt niveau for **Servicestyring** og viser, hvor serviceprocesserne integreres med andre moduler i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b5d0-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="4b5d0-120">[![Forretningsprocesdiagram for Servicestyring](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="4b5d0-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="4b5d0-121">Hurtigt overblik over servicestyring</span><span class="sxs-lookup"><span data-stu-id="4b5d0-121">Service management at a glance</span></span>

|<span data-ttu-id="4b5d0-122">Vigtige opgaver</span><span class="sxs-lookup"><span data-stu-id="4b5d0-122">Important tasks</span></span>           | <span data-ttu-id="4b5d0-123">Primære sider</span><span class="sxs-lookup"><span data-stu-id="4b5d0-123">Primary pages</span></span>                         |<span data-ttu-id="4b5d0-124">Populære rapporter</span><span class="sxs-lookup"><span data-stu-id="4b5d0-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="4b5d0-125">Opfyld serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="4b5d0-125">Fulfill service agreements</span></span>|<span data-ttu-id="4b5d0-126">Serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="4b5d0-126">Service agreements</span></span>                     |<span data-ttu-id="4b5d0-127">Serviceordremargen</span><span class="sxs-lookup"><span data-stu-id="4b5d0-127">Service order margin</span></span>         |
|<span data-ttu-id="4b5d0-128">Håndter kundeforespørgsler</span><span class="sxs-lookup"><span data-stu-id="4b5d0-128">Handle customer inquiries</span></span> |<span data-ttu-id="4b5d0-129">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="4b5d0-129">Service orders</span></span>                         |<span data-ttu-id="4b5d0-130">Arbejdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4b5d0-130">Work description</span></span>             |
|                          |<span data-ttu-id="4b5d0-131">Planlægningstavle</span><span class="sxs-lookup"><span data-stu-id="4b5d0-131">Dispatch board</span></span>                         |<span data-ttu-id="4b5d0-132">Postering - Abonnement</span><span class="sxs-lookup"><span data-stu-id="4b5d0-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="4b5d0-133">Abonnementsgebyrtransaktioner</span><span class="sxs-lookup"><span data-stu-id="4b5d0-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="4b5d0-134">Integration af servicestyring</span><span class="sxs-lookup"><span data-stu-id="4b5d0-134">Integration of Service management</span></span>

<span data-ttu-id="4b5d0-135">Servicestyring kan integreres med følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="4b5d0-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="4b5d0-136">Salg og marketing</span><span class="sxs-lookup"><span data-stu-id="4b5d0-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="4b5d0-137">Personale</span><span class="sxs-lookup"><span data-stu-id="4b5d0-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  

