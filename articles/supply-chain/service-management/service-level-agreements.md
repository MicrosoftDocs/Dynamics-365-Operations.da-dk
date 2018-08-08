---
title: Serviceniveauaftaler
description: "I en serviceniveauaftale accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="service-level-agreements"></a><span data-ttu-id="cb2cd-103">Serviceniveauaftaler</span><span class="sxs-lookup"><span data-stu-id="cb2cd-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cb2cd-104">En serviceniveauaftale er en aftale mellem et servicefirma og en servicekunde.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="cb2cd-105">I en SLA accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="cb2cd-106">En SLA fastlægger et standardserviceniveau, der tilbydes kunder, og gør det nemt for et servicefirma at overskue, hvornår en serviceopgave skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="cb2cd-107">Der kan oprettes ethvert antal serviceniveauaftaler for at tilbyde forskellige niveauer af service til servicekunder.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="cb2cd-108">Oprette en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="cb2cd-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="cb2cd-109">Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceniveauaftaler**.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="cb2cd-110">Skriv et navn til serviceniveauaftalen i feltet **Serviceniveauaftale**.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="cb2cd-111">Skriv den tid, du vil tillade til afslutning af servicekald, der er tilknyttet serviceaftaleniveauet.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="cb2cd-112">Vælg derefter en kalender, hvis du vil basere serviceaftalen på en bestemt kalender.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="cb2cd-113">Anvende en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="cb2cd-113">Apply a service level agreement</span></span>

<span data-ttu-id="cb2cd-114">Serviceniveauaftalen anvendes direkte på en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="cb2cd-115">Serviceordrer, som du opretter manuelt og knytter til en serviceaftale, som har en SLA, måles i forhold til denne SLA.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="cb2cd-116">Serviceordrer, som du opretter automatisk, knyttes ikke til en serviceniveauaftale.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="cb2cd-117">Anvende serviceniveauaftalen på serviceaftalen</span><span class="sxs-lookup"><span data-stu-id="cb2cd-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="cb2cd-118">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="cb2cd-119">Vælg den serviceaftale, du vil anvende SLA'en til, og klik derefter på **Rediger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="cb2cd-120">I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="cb2cd-121">Anvende serviceniveauaftalen på serviceaftalegruppen</span><span class="sxs-lookup"><span data-stu-id="cb2cd-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="cb2cd-122">Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceaftalegrupper**.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="cb2cd-123">I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="cb2cd-124">Spore tidsforbrug på en serviceordre i forhold til en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="cb2cd-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="cb2cd-125">Når du opretter en ny serviceordre til en serviceaftale, som en SLA er tildelt til, startes tidsintervallet for levering af servicen, og systemet begynder at spore leveringstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="cb2cd-126">Du kan desuden angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="cb2cd-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="cb2cd-127">Du kan starte og stoppe tidsregistreringen for serviceordren for at registrere det samlede tidsforbrug på serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="cb2cd-128">Du kan overvåge overholdelsen af det tidsinterval, der er afsat i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="cb2cd-129">Du kan definere årsagskoder, der skal angives, hvis tidsintervallet for serviceaftalen overskrides.</span><span class="sxs-lookup"><span data-stu-id="cb2cd-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb2cd-130">Se også</span><span class="sxs-lookup"><span data-stu-id="cb2cd-130">See also</span></span>

[<span data-ttu-id="cb2cd-131">Få vist overholdelse af serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="cb2cd-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  



