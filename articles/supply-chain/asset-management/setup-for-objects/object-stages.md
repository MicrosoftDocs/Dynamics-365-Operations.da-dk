---
title: Tilstande for aktivlivscyklus
description: I dette emne forklares aktivers livscyklustilstand og livscyklusmodeller i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1752298ce726b904defb1c826a1e2d5014286e1f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216522"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="8ad98-103">Aktivers livscyklustilstande</span><span class="sxs-lookup"><span data-stu-id="8ad98-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8ad98-104">I dette emne forklares aktivers livscyklustilstand og livscyklusmodeller i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="8ad98-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="8ad98-105">Aktivers livscyklustilstande bruges til at definere, om et aktiv er aktivt eller inaktivt.</span><span class="sxs-lookup"><span data-stu-id="8ad98-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="8ad98-106">Du kan for eksempel konfigurere livscyklustilstande for aktiver som **Oprettet**, **Aktiv** og **Afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="8ad98-107">Livscyklustilstande for anmodninger er knyttet til aktivernes livscyklustilstande.</span><span class="sxs-lookup"><span data-stu-id="8ad98-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="8ad98-108">Når en anmodning ændres til en ny livscyklustilstand for en anmodning, ændres det aktiv, der er tilknyttet anmodningen, derfor til en ny livscyklustilstand for aktivet.</span><span class="sxs-lookup"><span data-stu-id="8ad98-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="8ad98-109">Hvis livscyklustilstanden for en anmodning eksempelvis ændres til **Indgående**, ændres livscyklustilstanden for det tilknyttede aktiv til den livscyklustilstand, der er valgt i feltet **Indgående livscyklustilstand** på oversigtspanelet for **Aktivets livscyklustilstand** på siden **Aktivets livscyklustilstandmodeller**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="8ad98-110">Aktivers livscyklustilstande kan konfigureres i aktivernes livscyklusmodeller, hvor du kan definere de påkrævede livscyklustilstande for forskellige typer aktiver.</span><span class="sxs-lookup"><span data-stu-id="8ad98-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="8ad98-111">Du konfigurerer først livscyklustilstandene.</span><span class="sxs-lookup"><span data-stu-id="8ad98-111">You first set up lifecycle states.</span></span> <span data-ttu-id="8ad98-112">Derefter opretter du en livscyklusmodel og vælger livscyklustilstande for den.</span><span class="sxs-lookup"><span data-stu-id="8ad98-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="8ad98-113">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="8ad98-114">Vælg **Ny** for at oprette en ny tilstand for aktivets livscyklus.</span><span class="sxs-lookup"><span data-stu-id="8ad98-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="8ad98-115">Indtast ID'et for livscyklustilstanden i feltet **Livscyklustilstand**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="8ad98-116">Angiv en beskrivelse i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="8ad98-117">Feltet **Livscyklusmodeller** viser antallet af livscyklusmodeller for aktiver, der bruger denne aktivlivscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="8ad98-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="8ad98-118">Angiv indstillingen **Aktiv** til **Ja**, hvis denne livscyklustilstand skal være en aktiv livscyklustilstand (med andre ord hvis der kan oprettes arbejdsordrer for aktiver i denne livscyklustilstand).</span><span class="sxs-lookup"><span data-stu-id="8ad98-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="8ad98-119">Angiv indstillingen **Slet åbne kalenderlinjer** til **Ja**, hvis åbne kalenderlinjer for et aktiv, der har en aktivlivscyklustilstand med status **Oprettet**, skal slettes, når de er i denne livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="8ad98-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="8ad98-120">Denne indstilling er nyttig, hvis du vil rydde op i eventuelle åbne vedligeholdelsesplaner, der ikke længere er relevante for aktivet (f.eks. hvis aktivet ikke længere er aktivt).</span><span class="sxs-lookup"><span data-stu-id="8ad98-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="8ad98-121">Aktivers livscyklustilstande, livscyklusmodeller for aktiver og aktivtyper er relateret.</span><span class="sxs-lookup"><span data-stu-id="8ad98-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="8ad98-122">De bruges på samme måde som arbejdsordrers livscyklustilstande, arbejdsordrers livscyklusmodeller og arbejdsordretyper.</span><span class="sxs-lookup"><span data-stu-id="8ad98-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="8ad98-123">Når du har oprettet de påkrævede livscyklustilstande for aktiver, kan du konfigurere livscyklustilstande i aktivlivscyklusmodeller.</span><span class="sxs-lookup"><span data-stu-id="8ad98-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="8ad98-124">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Livscyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="8ad98-125">Vælg **Ny** for at oprette en ny model for aktivets livscyklus.</span><span class="sxs-lookup"><span data-stu-id="8ad98-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="8ad98-126">Angiv ID'et for livscyklusmodellen i feltet **Livscyklusmodel**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="8ad98-127">Angiv en beskrivelse i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="8ad98-128">Feltet **Livscyklustilstande** viser antallet af aktivlivscyklustilstande, der er valgt i denne aktivlivscyklusmodel.</span><span class="sxs-lookup"><span data-stu-id="8ad98-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="8ad98-129">Feltet **Aktivtyper** viser antallet af aktivtyper, der bruger livscyklusmodellen.</span><span class="sxs-lookup"><span data-stu-id="8ad98-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="8ad98-130">I oversigtspanelet **Livscyklustilstande** skal du vælge de aktivlivscyklustilstande, der bør inkluderes i aktivlivscyklusmodellen:</span><span class="sxs-lookup"><span data-stu-id="8ad98-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="8ad98-131">Hvis du vil bruge en livscyklustilstand for modellen, skal du vælge den i sektionen **Resterende livscyklustilstande** og derefter vælge knappen med højre pil ![Højre pil](media/15-setup-for-objects.png) for at flytte den til sektionen med **Valgte livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="8ad98-132">Hvis du vil bruge alle de tilgængelige livscyklustilstande for livscyklusmodellen, skal du vælge knappen **Alle tilgængelige livscyklustilstande** ![Alle tilgængelige livscyklustilstande](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="8ad98-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="8ad98-133">Alle livscyklustilstande overføres til sektionen **Valgte livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="8ad98-134">Hvis du vil fjerne en livscyklustilstand fra modellen, skal du vælge den i sektionen **Valgte livscyklustilstande** og derefter vælge knappen med venstre pil ![Venstre pil](media/16-setup-for-objects.png) for at flytte den til sektionen med **Resterende livscyklustilstande**.</span><span class="sxs-lookup"><span data-stu-id="8ad98-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="8ad98-135">Vælg **Opdateringer til livscyklustilstande** for at definere de aktivlivscyklustilstande, der kan følge en valgt livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="8ad98-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="8ad98-136">Du kan bruge oversigtspanelet **Aktivtilstand**, hvis du håndterer aktiver, som du modtager til reparation.</span><span class="sxs-lookup"><span data-stu-id="8ad98-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="8ad98-137">I sektionen **Indgående/udgående** kan du vælge livscyklustilstand for aktiver for at angive arbejdsgangen for et aktiv, som du modtager til reparation.</span><span class="sxs-lookup"><span data-stu-id="8ad98-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="8ad98-138">Hvis du tilbyder udlånsaktiver til kunder eller afdelinger, kan du i sektionen **Udlån** vælge livscyklustilstande for udlånsaktiver.</span><span class="sxs-lookup"><span data-stu-id="8ad98-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
