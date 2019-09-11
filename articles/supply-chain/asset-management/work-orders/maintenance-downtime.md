---
title: Vedligeholdelsesnedetid
description: Dette emne beskriver vedligeholdelsesnedetid i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918238"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="8b6e2-103">Vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="8b6e2-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8b6e2-104">Du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="8b6e2-105">Dette er nyttigt, hvis du vil registrere vedligeholdelsesnedetid på en eller flere maskiner i produktionsområdet.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="8b6e2-106">Først skal du oprette de årsagskoder til vedligeholdelsesnedetid, du vil bruge, f.eks. nedbrud og planlagt stop.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="8b6e2-107">Dette gøres i **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="8b6e2-108">Derefter kan du oprette registreringer af vedligeholdelsesnedetid i **Vedligeholdelsesnedetid** og tilføje de relevante årsagskoder.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="8b6e2-109">Oprette årsagskoder for vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="8b6e2-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="8b6e2-110">Klik på **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="8b6e2-111">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-111">Click **New**.</span></span>

3. <span data-ttu-id="8b6e2-112">Indsæt et id i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="8b6e2-113">Angiv et navn til årsagskoden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="8b6e2-114">Markér afkrydsningsfeltet **Medtag KPI**, hvis årsagskoden skal medtages i KPI-beregninger for aktiv.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="8b6e2-115">Generelt bør planlagte produktionsstop ikke medtages i KPI-beregninger, da de ikke påvirker den forventede ydeevne.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="8b6e2-116">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-116">Click **Save**.</span></span>

![Figur 1](media/15-work-orders.png)


<span data-ttu-id="8b6e2-118">Når du har oprettet de årsagskoder til vedligeholdelsesnedetid, du vil bruge, kan du oprette registreringer af vedligeholdelsesnedetid for arbejdsordrer og aktiver.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="8b6e2-119">Oprette registreringer af vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="8b6e2-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="8b6e2-120">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8b6e2-121">Vælg arbejdsordren, og klik på **Vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="8b6e2-122">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-122">Click **New**.</span></span>

4. <span data-ttu-id="8b6e2-123">Indsæt dato- og tidsinterval for registrering af vedligeholdelsesnedetid i felterne **Fra** og **Til**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="8b6e2-124">Når du forlader feltet **Til**, indsættes varigheden i timer automatisk i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="8b6e2-125">Vælg en årsagskode i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="8b6e2-126">Gentag trin 3-6, hvis du vil tilføje flere registreringer.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="8b6e2-127">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-127">Click **Save**.</span></span>


![Figur 2](media/16-work-orders.png)


<span data-ttu-id="8b6e2-129">Den kalender, der bruges til beregning af registreret vedligeholdelsesnedetid, afhænger af dit valg i opsætningen af aktiver og parametre.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="8b6e2-130">Hvis en ressource er valgt på et aktiv i **Alle aktiver** > **Anlægsaktiv**-oversigtspanelet > feltet **Ressource**, bruges den kalender, der er konfigureret for den tilknyttede ressourcegruppe, som vist i følgende figur.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Figur 3](media/17-work-orders.png)


<span data-ttu-id="8b6e2-132">Hvis der ikke er valgt en ressource på aktivet, bruges den standardkalender, der er valgt i **Parametre til aktivstyring**, som vist i følgende figur.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Figur 4](media/18-work-orders.png)


<span data-ttu-id="8b6e2-134">Klik på **Styring af virksomhedsaktiv** > **Forespørgsler** > **Vedligeholdelsesnedetid** for at få vist en oversigt over alle registreringer af vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="8b6e2-135">Alle de kalendere, der bruges i modulet **Styring af aktiver**, konfigureres i **Virksomhedsadministration** > **Opsætning** > **Kalendere** > **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="8b6e2-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

