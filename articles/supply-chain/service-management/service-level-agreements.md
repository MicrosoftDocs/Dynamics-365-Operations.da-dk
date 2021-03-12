---
title: Oversigt over serviceniveauaftaler
description: I en serviceniveauaftale accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974354"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="0c33c-103">Oversigt over serviceniveauaftaler</span><span class="sxs-lookup"><span data-stu-id="0c33c-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0c33c-104">En serviceniveauaftale er en aftale mellem et servicefirma og en servicekunde.</span><span class="sxs-lookup"><span data-stu-id="0c33c-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="0c33c-105">I en SLA accepterer kunden en minimumsvartid baseret på det tidspunkt, hvor servicefirmaet registrerer problemet, og hvornår problemet er løst.</span><span class="sxs-lookup"><span data-stu-id="0c33c-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="0c33c-106">En SLA fastlægger et standardserviceniveau, der tilbydes kunder, og gør det nemt for et servicefirma at overskue, hvornår en serviceopgave skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="0c33c-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="0c33c-107">Der kan oprettes ethvert antal serviceniveauaftaler for at tilbyde forskellige niveauer af service til servicekunder.</span><span class="sxs-lookup"><span data-stu-id="0c33c-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="0c33c-108">Oprette en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="0c33c-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="0c33c-109">Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceniveauaftaler**.</span><span class="sxs-lookup"><span data-stu-id="0c33c-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="0c33c-110">Skriv et navn til serviceniveauaftalen i feltet **Serviceniveauaftale**.</span><span class="sxs-lookup"><span data-stu-id="0c33c-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="0c33c-111">Skriv den tid, du vil tillade til afslutning af servicekald, der er tilknyttet serviceaftaleniveauet.</span><span class="sxs-lookup"><span data-stu-id="0c33c-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="0c33c-112">Vælg derefter en kalender, hvis du vil basere serviceaftalen på en bestemt kalender.</span><span class="sxs-lookup"><span data-stu-id="0c33c-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="0c33c-113">Anvende en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="0c33c-113">Apply a service level agreement</span></span>

<span data-ttu-id="0c33c-114">Serviceniveauaftalen anvendes direkte på en serviceaftale.</span><span class="sxs-lookup"><span data-stu-id="0c33c-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="0c33c-115">Serviceordrer, som du opretter manuelt og knytter til en serviceaftale, som har en SLA, måles i forhold til denne SLA.</span><span class="sxs-lookup"><span data-stu-id="0c33c-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="0c33c-116">Serviceordrer, som du opretter automatisk, knyttes ikke til en serviceniveauaftale.</span><span class="sxs-lookup"><span data-stu-id="0c33c-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="0c33c-117">Anvende serviceniveauaftalen på serviceaftalen</span><span class="sxs-lookup"><span data-stu-id="0c33c-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="0c33c-118">Klik på **Servicestyring** \> **Almindelige** \> **Serviceaftaler** \> **Serviceaftaler**.</span><span class="sxs-lookup"><span data-stu-id="0c33c-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="0c33c-119">Vælg den serviceaftale, du vil anvende SLA'en til, og klik derefter på **Rediger** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="0c33c-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="0c33c-120">I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="0c33c-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="0c33c-121">Anvende serviceniveauaftalen på serviceaftalegruppen</span><span class="sxs-lookup"><span data-stu-id="0c33c-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="0c33c-122">Klik på **Servicestyring** \> **Opsætning** \> **Serviceaftaler** \> **Serviceaftalegrupper**.</span><span class="sxs-lookup"><span data-stu-id="0c33c-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="0c33c-123">I feltet **Serviceniveauaftale** skal du vælge den SLA, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="0c33c-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="0c33c-124">Spore tidsforbrug på en serviceordre i forhold til en serviceniveauaftale</span><span class="sxs-lookup"><span data-stu-id="0c33c-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="0c33c-125">Når du opretter en ny serviceordre til en serviceaftale, som en SLA er tildelt til, startes tidsintervallet for levering af servicen, og systemet begynder at spore leveringstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="0c33c-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="0c33c-126">Du kan desuden angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0c33c-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="0c33c-127">Du kan starte og stoppe tidsregistreringen for serviceordren for at registrere det samlede tidsforbrug på serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="0c33c-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="0c33c-128">Du kan overvåge overholdelsen af det tidsinterval, der er afsat i serviceaftalen.</span><span class="sxs-lookup"><span data-stu-id="0c33c-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="0c33c-129">Du kan definere årsagskoder, der skal angives, hvis tidsintervallet for serviceaftalen overskrides.</span><span class="sxs-lookup"><span data-stu-id="0c33c-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c33c-130">Se også</span><span class="sxs-lookup"><span data-stu-id="0c33c-130">See also</span></span>

[<span data-ttu-id="0c33c-131">Få vist overholdelse af serviceaftaler</span><span class="sxs-lookup"><span data-stu-id="0c33c-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


