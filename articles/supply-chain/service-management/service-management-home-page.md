---
title: Servicestyring
description: "Du kan bruge Servicestyring til at udarbejde serviceaftaler og serviceabonnementer, håndtere serviceordrer og kundeforespørgsler samt administrere og analysere leveringen af tjenester til kunder."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
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
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: da-dk
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="2a245-103">Servicestyring</span><span class="sxs-lookup"><span data-stu-id="2a245-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2a245-104">Du kan bruge **Servicestyring** til at udarbejde serviceaftaler og serviceabonnementer, håndtere serviceordrer og kundeforespørgsler samt administrere og analysere leveringen af tjenester til kunder.</span><span class="sxs-lookup"><span data-stu-id="2a245-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="2a245-105">Du kan bruge serviceaftaler til at definere de ressourcer, der bruges under et typisk servicebesøg.</span><span class="sxs-lookup"><span data-stu-id="2a245-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="2a245-106">Du kan også bruges serviceaftaler til at få vist, hvordan disse ressourcer faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="2a245-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="2a245-107">En serviceaftale kan også inkludere en serviceniveauaftale, der angiver standardsvartider og inkluderer værktøjer til registrering af den faktiske tid.</span><span class="sxs-lookup"><span data-stu-id="2a245-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="2a245-108">Du kan oprette serviceordrer til administrering af oplysninger om planlagte og ikke-planlagte besøg af en servicetekniker hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="2a245-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="2a245-109">Serviceordrer inkluderer oplysninger, som f.eks.:</span><span class="sxs-lookup"><span data-stu-id="2a245-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="2a245-110">De arbejdstimer, som servicetekniker skal bruge</span><span class="sxs-lookup"><span data-stu-id="2a245-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="2a245-111">Service- eller reparationstypen</span><span class="sxs-lookup"><span data-stu-id="2a245-111">The type of service or repair</span></span>

3.  <span data-ttu-id="2a245-112">Det objekt, der skal repareres, inklusive oplysninger om symptomer og diagnose</span><span class="sxs-lookup"><span data-stu-id="2a245-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="2a245-113">Eventuelle udgifter og gebyrer, der er relateret til servicen eller reparationen</span><span class="sxs-lookup"><span data-stu-id="2a245-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="2a245-114">Kunder kan sende serviceanmodninger via internettet ved hjælp af Enterprise Portal.</span><span class="sxs-lookup"><span data-stu-id="2a245-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="2a245-115">Du kan modtage, behandle og ekspedere disse anmodninger.</span><span class="sxs-lookup"><span data-stu-id="2a245-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="2a245-116">Når du har oprettet en serviceordre, kan du bruge servicestadier til at overvåge status og angive regler, der bestemmer, hvilke handlinger der er aktiveret i hvert af stadierne.</span><span class="sxs-lookup"><span data-stu-id="2a245-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="2a245-117">Når en serviceordre er færdig, kan du afslutte ordren for at bekræfte, at den er færdig, og derefter bogføre ordren for at starte fakturaprocessen.</span><span class="sxs-lookup"><span data-stu-id="2a245-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="2a245-118">Brug rapporteringsværktøjerne til at overvåge serviceordremargener og abonnementstransaktioner samt udskrive arbejdsbeskrivelser og arbejdskvitteringer.</span><span class="sxs-lookup"><span data-stu-id="2a245-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="2a245-119">Forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="2a245-119">Business processes</span></span>

<span data-ttu-id="2a245-120">I følgende diagram illustreres forretningsprocesserne på højt niveau for **Servicestyring** og viser, hvor serviceprocesserne integreres med andre moduler i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2a245-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="2a245-121">[![Forretningsprocesdiagram for Servicestyring](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="2a245-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="2a245-122">Hurtigt overblik over servicestyring</span><span class="sxs-lookup"><span data-stu-id="2a245-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a245-123">Vigtige opgaver</span><span class="sxs-lookup"><span data-stu-id="2a245-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="2a245-124">Primære forms</span><span class="sxs-lookup"><span data-stu-id="2a245-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="2a245-125">Populære rapporter</span><span class="sxs-lookup"><span data-stu-id="2a245-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a245-126">Opfyld serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="2a245-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="2a245-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Serviceaftaler (form)</a></span><span class="sxs-lookup"><span data-stu-id="2a245-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="2a245-128"><strong>Serviceordremargen</strong></span><span class="sxs-lookup"><span data-stu-id="2a245-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a245-129">Håndter kundeforespørgsler</span><span class="sxs-lookup"><span data-stu-id="2a245-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="2a245-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Serviceordrer (form)</a></span><span class="sxs-lookup"><span data-stu-id="2a245-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="2a245-131"><strong>Arbejdsbeskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="2a245-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="2a245-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Planlægningstavle (form)</a></span><span class="sxs-lookup"><span data-stu-id="2a245-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="2a245-133"><strong>Postering - Abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="2a245-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2a245-134"><strong>Abonnementsgebyrtransaktioner</strong></span><span class="sxs-lookup"><span data-stu-id="2a245-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="2a245-135">Integration af servicestyring</span><span class="sxs-lookup"><span data-stu-id="2a245-135">Integration of Service management</span></span>

<span data-ttu-id="2a245-136">Servicestyring kan integreres med følgende moduler i Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2a245-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="2a245-137">Salg og marketing</span><span class="sxs-lookup"><span data-stu-id="2a245-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="2a245-138">Personale</span><span class="sxs-lookup"><span data-stu-id="2a245-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


