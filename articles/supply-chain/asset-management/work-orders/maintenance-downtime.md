---
title: Vedligeholdelsesnedetid for arbejdsordrer
description: Dette emne beskriver, hvordan du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5c0c584ed53dc4ec8a761065838127dc67cbc41e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813719"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="b9dcc-103">Vedligeholdelsesnedetid for arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="b9dcc-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="b9dcc-104">Du kan oprette registreringer af vedligeholdelsesnedetid for det aktiv, der er valgt på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="b9dcc-105">Dette er nyttigt, hvis du vil registrere vedligeholdelsesnedetid på en eller flere maskiner i produktionsområdet.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="b9dcc-106">Først skal du oprette de årsagskoder til vedligeholdelsesnedetid, du vil bruge, f.eks. **Nedbrud** og **Planlagt stop**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="b9dcc-107">Dette gøres på siden **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="b9dcc-108">Derefter kan du oprette registreringer af vedligeholdelsesnedetid på siden **Vedligeholdelsesnedetid** og tilføje de relevante årsagskoder for vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="b9dcc-109">Oprette årsagskoder for vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="b9dcc-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="b9dcc-110">Vælg **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="b9dcc-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-111">Select **New**.</span></span>

3. <span data-ttu-id="b9dcc-112">Angiv et id for årsags koden til vedligeholdelsesnedetid i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="b9dcc-113">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="b9dcc-114">Markér afkrydsningsfeltet **Medtag KPI**, hvis årsagskoden skal medtages i beregningerne af KPI'er for aktivet.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="b9dcc-115">Generelt bør planlagte produktionsstop ikke medtages i KPI-beregninger, da de ikke påvirker den forventede ydeevne.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="b9dcc-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-116">Select **Save**.</span></span>

<span data-ttu-id="b9dcc-117">I følgende illustration vises et eksempel på siden **Årsagskoder til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Figur 1](media/15-work-orders.png)

<span data-ttu-id="b9dcc-119">Når du har oprettet de årsagskoder til vedligeholdelsesnedetid, du vil bruge, kan du oprette registreringer af vedligeholdelsesnedetid for arbejdsordrer og aktiver.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="b9dcc-120">Oprette registreringer af vedligeholdelsesnedetid</span><span class="sxs-lookup"><span data-stu-id="b9dcc-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="b9dcc-121">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="b9dcc-122">Vælg arbejdsordren, og vælg derefter **Vedligeholdelsesnedetid** i gruppen **Aktiv** under fanen **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="b9dcc-123">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-123">Select **New**.</span></span>

4. <span data-ttu-id="b9dcc-124">Indsæt dato- og tidsinterval for registrering af vedligeholdelsesnedetid i felterne **Fra** og **Til**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="b9dcc-125">Når du forlader feltet **Til**, indsættes varigheden i timer automatisk i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="b9dcc-126">Vælg en årsagskode i feltet **Årsagskode til vedligeholdelsesnedetid**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="b9dcc-127">Gentag trin 3 til 5 for at tilføje flere registreringer.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="b9dcc-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-128">Select **Save**.</span></span>

<span data-ttu-id="b9dcc-129">Følgende illustration viser et eksempel på en registrering af vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Figur 2](media/16-work-orders.png)

<span data-ttu-id="b9dcc-131">Den kalender, der bruges til beregning af registreret vedligeholdelsesnedetid, afhænger af dit valg i opsætningen af aktiver og parametre.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="b9dcc-132">Hvis en ressource er valgt på et aktiv i feltet **Ressource** i oversigtspanelet **Anlægsaktiv** på siden **Alle aktiver**, bruges den kalender, der er konfigureret for den tilknyttede ressourcegruppe, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Figur 3](media/17-work-orders.png)

<span data-ttu-id="b9dcc-134">Hvis der ikke er valgt en ressource på aktivet, bruges den standardkalender, der er valgt på siden **Parametre til aktivstyring**, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Figur 4](media/18-work-orders.png)

<span data-ttu-id="b9dcc-136">Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesnedetid** for at se en oversigt over alle registreringer af vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="b9dcc-137">Alle de kalendere, der bruges i modulet **Styring af aktiver**, konfigureres i **Virksomhedsadministration** > **Opsætning** > **Kalendere** > **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="b9dcc-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]