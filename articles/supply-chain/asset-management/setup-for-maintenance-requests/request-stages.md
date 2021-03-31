---
title: Livscyklustilstande for vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer livscyklustilstande for vedligeholdelsesanmodninger i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9022d866bf0da08a72ba9169587f87c1b77527a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217215"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="0a608-103">Levetidstilstande for vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="0a608-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="0a608-104">Livscyklustilstande for vedligeholdelsesanmodninger definerer de stadier, som en anmodning kan gennemgå.</span><span class="sxs-lookup"><span data-stu-id="0a608-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="0a608-105">Som eksempler kan nævnes **Oprettede**, **Aktive** og **Afsluttede**.</span><span class="sxs-lookup"><span data-stu-id="0a608-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="0a608-106">Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, skal vedligeholdelsesanmodningens livscyklustilstand opdateres til **Afsluttet** eller **Lukket** for at angive, at vedligeholdelsesanmodningen ikke længere er aktiv.</span><span class="sxs-lookup"><span data-stu-id="0a608-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="0a608-107">På listesiden **Alle vedligeholdelsesanmodninger** kan du se alle vedligeholdelsesanmodninger, uanset deres livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="0a608-108">Konfigurer livscyklustilstande for vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="0a608-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="0a608-109">Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="0a608-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="0a608-110">Vælg **Ny** for at oprette en tilstand for vedligeholdelsesanmodningens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="0a608-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="0a608-111">Angiv et ID for livscyklustilstand i feltet **Livscyklustilstand**.</span><span class="sxs-lookup"><span data-stu-id="0a608-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="0a608-112">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0a608-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0a608-113">I oversigtspanelet **Detaljer** viser feltet **Livscyklusmodeller** antallet af livscyklusmodeller for vedligeholdelsesanmodninger, der bruger denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="0a608-114">I oversigtspanelet **Generelt** skal du angive indstillingen **Aktiv** til **Ja**, hvis en vedligeholdelsesanmodning bør være aktiv, mens den er i denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="0a608-115">Angiv indstillingen **Angiv faktisk slutning** til **Ja**, hvis der automatisk skal angives en faktisk slutdato og tidspunkt på en vedligeholdelsesanmodning i denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="0a608-116">Angiv indstillingen **Opret arbejdsordre** til **Ja**, hvis der kan oprettes en arbejdsordre ud fra en vedligeholdelsesanmodning i denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="0a608-117">Angiv indstillingen **Slet** til **Ja**, hvis en vedligeholdelsesanmodning kan slettes, mens den er i denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="0a608-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="0a608-118">I oversigtspanelet **Opdater** er indstillingerne **Indgående** og **Udgående** i afsnittet **Aktiv** relevante, hvis du bruger reparation af depot.</span><span class="sxs-lookup"><span data-stu-id="0a608-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="0a608-119">Angiv den relevante indstilling til **ja**, hvis livscyklustilstanden for aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til **Indgående** eller **Udgående**, når vedligeholdelsesanmodningens livscyklustilstand for den pågældende vedligeholdelsesanmodning er angivet til **Indgående** eller **Udgående**.</span><span class="sxs-lookup"><span data-stu-id="0a608-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="0a608-120">Følgende illustration viser et eksempel på listesiden **Vedligeholdelsesanmodningers livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="0a608-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Siden Livscyklustilstande for vedligeholdelsesanmodning](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="0a608-122">Livscyklustilstande for vedligeholdelsesanmodninger, livscyklustilstandsgrupper og -typer er relateret til og bruges på samme måde som arbejdsordres livscyklustilstande, livscyklustilstandsgrupper og -typer.</span><span class="sxs-lookup"><span data-stu-id="0a608-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="0a608-123">Konfigurer livscyklusmodeller for vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="0a608-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="0a608-124">Når du har oprettet de livscyklustilstande, der kræves til dine vedligeholdelsesanmodninger, kan de opdeles i livscyklustilstandsgrupper eller livscyklusmodeller.</span><span class="sxs-lookup"><span data-stu-id="0a608-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="0a608-125">Livscyklusmodeller for vedligeholdelsesanmodning bruges til at oprette det flow, der kan anvendes til forskellige typer af vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="0a608-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="0a608-126">Der skal som minimum oprettes én standardlivscyklusmodel for vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="0a608-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="0a608-127">Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Livscyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="0a608-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="0a608-128">Vælg **Ny** for at oprette en model for vedligeholdelsesanmodningens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="0a608-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="0a608-129">Angiv et ID for livscyklusmodellen i feltet **Livscyklusmodel**.</span><span class="sxs-lookup"><span data-stu-id="0a608-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="0a608-130">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0a608-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0a608-131">I oversigtspanelet **Detaljer** viser feltet **Livscyklustilstande** antallet af livscyklustilstande, der er valgt i denne livscyklusmodel.</span><span class="sxs-lookup"><span data-stu-id="0a608-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="0a608-132">Feltet **Vedligeholdelsesanmodningstyper** viser antallet af vedligeholdelsesanmodningstyper, der bruger denne livscyklusmodel.</span><span class="sxs-lookup"><span data-stu-id="0a608-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="0a608-133">I oversigts panelet **Livscyklustilstande** skal du vælge de livscyklustilstande, der bør inkluderes i livscyklusmodellen:</span><span class="sxs-lookup"><span data-stu-id="0a608-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="0a608-134">Hvis du vil inkludere en livscyklustilstand i livscyklusmodellen, skal du vælge den i sektionen **Resterende livscyklustilstande** og derefter vælge knappen med højre pil ![Højre pil](media/03-setup-for-requests.png) for at flytte den til sektionen med **Valgte livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="0a608-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0a608-135">Hvis du vil inkludere alle de tilgængelige livscyklustilstande i livscyklusmodellen, skal du vælge knappen **Vælg alle tilgængelige tilstande** ![Vælg alle tilgængelige tilstande](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="0a608-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="0a608-136">Alle livscyklustilstande flyttes til sektionen **Valgte livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="0a608-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0a608-137">Hvis du vil fjerne en livscyklustilstand fra livscyklusmodellen, skal du vælge den i sektionen **Valgte livscyklustilstande** og derefter vælge knappen med venstre pil ![Venstre pil](media/05-setup-for-requests.png) for at flytte den til sektionen med **Resterende livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="0a608-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="0a608-138">I oversigtspanelet **Generelt** er felterne i sektionen **Opdateringer** relevante, hvis du bruger reparation af depot.</span><span class="sxs-lookup"><span data-stu-id="0a608-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="0a608-139">I feltet **Livscyklustilstand for modtaget aktiv** skal du vælge den for aktivlivscyklustilstand, som aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til, når de modtages til reparation af depot.</span><span class="sxs-lookup"><span data-stu-id="0a608-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="0a608-140">I feltet **Livscyklustilstand for leveret aktiv** skal du vælge den for livscyklustilstand, som aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til, når de returneres efter reparation.</span><span class="sxs-lookup"><span data-stu-id="0a608-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="0a608-141">Følgende illustration viser et eksempel på listesiden **Vedligeholdelsesanmodningers livscyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="0a608-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Siden Livscyklusmodeller for vedligeholdelsesanmodning](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]