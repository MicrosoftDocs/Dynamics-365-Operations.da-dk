---
title: Vedligeholdelsesnedetid
description: Dette emne beskriver vedligeholdelsesnedetid i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b4960aea95d63486207699f3bbd7f4b4f3cf0488
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206858"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="347cd-103">Vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="347cd-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="347cd-104">Du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="347cd-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="347cd-105">Dette er nyttigt, hvis du vil registrere vedligeholdelsesnedetid på en eller flere maskiner i produktionsområdet.</span><span class="sxs-lookup"><span data-stu-id="347cd-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="347cd-106">Først skal du oprette de årsagskoder til vedligeholdelsesnedetid, du vil bruge, f.eks. **Nedbrud** og **Planlagt stop**.</span><span class="sxs-lookup"><span data-stu-id="347cd-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="347cd-107">Dette gøres på siden **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="347cd-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="347cd-108">Derefter kan du oprette registreringer af vedligeholdelsesnedetid på siden **Vedligeholdelsesnedetid** og tilføje de relevante årsagskoder for vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="347cd-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="347cd-109">Oprette årsagskoder for vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="347cd-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="347cd-110">Vælg **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="347cd-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="347cd-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="347cd-111">Select **New**.</span></span>

3. <span data-ttu-id="347cd-112">Angiv et id for årsags koden til vedligeholdelsesnedetid i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="347cd-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="347cd-113">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="347cd-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="347cd-114">Markér afkrydsningsfeltet **Medtag KPI**, hvis årsagskoden skal medtages i beregningerne af KPI'er for aktivet.</span><span class="sxs-lookup"><span data-stu-id="347cd-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="347cd-115">Generelt bør planlagte produktionsstop ikke medtages i KPI-beregninger, da de ikke påvirker den forventede ydeevne.</span><span class="sxs-lookup"><span data-stu-id="347cd-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="347cd-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="347cd-116">Select **Save**.</span></span>

<span data-ttu-id="347cd-117">I følgende illustration vises et eksempel på siden **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="347cd-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Figur 1](media/15-work-orders.png)

<span data-ttu-id="347cd-119">Når du har oprettet de årsagskoder til vedligeholdelsesnedetid, du vil bruge, kan du oprette registreringer af vedligeholdelsesnedetid for arbejdsordrer og aktiver.</span><span class="sxs-lookup"><span data-stu-id="347cd-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="347cd-120">Oprette registreringer af vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="347cd-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="347cd-121">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="347cd-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="347cd-122">Vælg arbejdsordren, og vælg derefter **Vedligeholdelsesnedetid** i gruppen **Aktiv** under fanen **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="347cd-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="347cd-123">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="347cd-123">Select **New**.</span></span>

4. <span data-ttu-id="347cd-124">Indsæt dato- og tidsinterval for registrering af vedligeholdelsesnedetid i felterne **Fra** og **Til**.</span><span class="sxs-lookup"><span data-stu-id="347cd-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="347cd-125">Når du forlader feltet **Til**, indsættes varigheden i timer automatisk i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="347cd-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="347cd-126">Vælg en årsagskode i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="347cd-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="347cd-127">Gentag trin 3 til 5 for at tilføje flere registreringer.</span><span class="sxs-lookup"><span data-stu-id="347cd-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="347cd-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="347cd-128">Select **Save**.</span></span>

<span data-ttu-id="347cd-129">Følgende illustration viser et eksempel på en registrering af vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="347cd-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Figur 2](media/16-work-orders.png)

<span data-ttu-id="347cd-131">Den kalender, der bruges til beregning af registreret vedligeholdelsesnedetid, afhænger af dit valg i opsætningen af aktiver og parametre.</span><span class="sxs-lookup"><span data-stu-id="347cd-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="347cd-132">Hvis en ressource er valgt på et aktiv i feltet **Ressource** i oversigtspanelet **Anlægsaktiv** på siden **Alle aktiver**, bruges den kalender, der er konfigureret for den tilknyttede ressourcegruppe, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="347cd-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Figur 3](media/17-work-orders.png)

<span data-ttu-id="347cd-134">Hvis der ikke er valgt en ressource på aktivet, bruges den standardkalender, der er valgt på siden **Parametre til aktivstyring**, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="347cd-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Figur 4](media/18-work-orders.png)

<span data-ttu-id="347cd-136">Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesnedetid** for at se en oversigt over alle registreringer af vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="347cd-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="347cd-137">Alle de kalendere, der bruges i modulet **Styring af aktiver**, konfigureres i **Virksomhedsadministration** > **Opsætning** > **Kalendere** > **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="347cd-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

