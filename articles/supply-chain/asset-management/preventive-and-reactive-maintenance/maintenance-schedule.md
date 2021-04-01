---
title: Vedligeholdelsestidsplan
description: I dette emne beskrives vedligeholdelsestidsplaner i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89938a4c5fd9a520c6582215a438670f73085228
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252936"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="72227-103">Vedligeholdelsestidsplan</span><span class="sxs-lookup"><span data-stu-id="72227-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="72227-104">Vedligeholdelsestidsplanen indeholder en liste over alle de forventede forebyggende vedligeholdelsesplaner, vedligeholdelsesanmodninger og vedligeholdelsesrunder, der skal udføres. Nogle tidsplanslinjer kan være blevet konverteret til arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="72227-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="72227-105">De fire visninger for vedligeholdelsestidsplanen er lidt forskellige, afhængigt af hvilke vedligeholdelsestidsplanlinjer du vil have vist.</span><span class="sxs-lookup"><span data-stu-id="72227-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="72227-106">Menupunkt</span><span class="sxs-lookup"><span data-stu-id="72227-106">Menu item</span></span>                  | <span data-ttu-id="72227-107">Indholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="72227-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72227-108">Hele vedligeholdelsestidsplanen</span><span class="sxs-lookup"><span data-stu-id="72227-108">All maintenance schedule</span></span>       | <span data-ttu-id="72227-109">Alle vedligeholdelsestidsplanslinjer vises.</span><span class="sxs-lookup"><span data-stu-id="72227-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="72227-110">Min aktivtidsplan</span><span class="sxs-lookup"><span data-stu-id="72227-110">My asset schedule</span></span>        | <span data-ttu-id="72227-111">Alle vedligeholdelsestidsplanslinjer, der indeholder aktiver, som er installeret på arbejdssteder, som du er relateret til som arbejder (konfigureret i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md)), vises på denne liste.</span><span class="sxs-lookup"><span data-stu-id="72227-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="72227-112">Åbn vedligeholdelsestidsplanslinjer</span><span class="sxs-lookup"><span data-stu-id="72227-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="72227-113">Vedligeholdelsestidsplanslinjer med status "Oprettet" - det vil sige, at de endnu ikke er blevet konverteret til en arbejdsordre eller slettet - vises på denne liste.</span><span class="sxs-lookup"><span data-stu-id="72227-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="72227-114">Åbn vedligeholdelsestidsplanspuljer</span><span class="sxs-lookup"><span data-stu-id="72227-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="72227-115">Vedligeholdelsestidsplanslinjer, der er relateret til en arbejdsordrepulje, vises på denne liste.</span><span class="sxs-lookup"><span data-stu-id="72227-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="72227-116">Hvis en vedligeholdelsestidsplanlinje er medtaget i flere arbejdsordrepuljer (referer til [Arbejdsordrepuljer](../work-orders/work-order-pools.md)), vises der én post for hver pulje i **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="72227-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="72227-117">Dette gøres for at optimere filtreringsindstillinger i arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="72227-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="72227-118">Sådan åbnes en vedligeholdelsestidsplan:</span><span class="sxs-lookup"><span data-stu-id="72227-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="72227-119">Klik på **Styring af aktiver** > **Generelt** > **Vedligeholdelsestidsplan** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="72227-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="72227-120">Hvis du vil opdatere vedligeholdelsesplanen, skal du klikke på **Vedligeholdelsesplan** eller **Vedligeholdelsesrunder**.</span><span class="sxs-lookup"><span data-stu-id="72227-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="72227-121">Du kan redigere en vedligeholdelsesplanlinje ved at markere den og klikke på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="72227-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="72227-122">Du kan f.eks. nemt opdatere serviceniveauet eller den arbejder, der er ansvarlig for jobbet.</span><span class="sxs-lookup"><span data-stu-id="72227-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="72227-123">Du kan kun redigere de vedligeholdelsestidsplanslinjer, der endnu ikke er knyttet til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="72227-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="72227-124">Du kan slette en vedligeholdelsestidsplanslinje ved at vælge den på listesiden og klikke på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="72227-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="72227-125">Du kan kassere en vedligeholdelsestidsplanslinje ved at vælge den på listesiden og klikke på **Kassér**.</span><span class="sxs-lookup"><span data-stu-id="72227-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="72227-126">Denne funktion er nyttig, hvis et aktiv f.eks. har en vedligeholdelsesplan på 2.000 km og en vedligeholdelsesplan på 10.000 km.</span><span class="sxs-lookup"><span data-stu-id="72227-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="72227-127">Du kan derefter vælge at kassere den linje, der er oprettet fra vedligeholdelsesplanen for 2.000 km, når den falder sammen med 10.000 km, 20.000 km, 30.000 km osv.</span><span class="sxs-lookup"><span data-stu-id="72227-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="72227-128">Hvis du sletter en vedligeholdelsestidsplanslinje, der er relateret til en vedligeholdelsesplan, vises den pågældende linje aldrig igen, når vedligeholdelsesplanen er planlagt.</span><span class="sxs-lookup"><span data-stu-id="72227-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="72227-129">Du kan vælge et antal vedligeholdelsestidsplanslinjer i **Alle vedligeholdelsestidsplaner** og klikke på **Arbejdsordrepulje**, hvis alle valgte linjer skal medtages i den samme arbejdsordrepulje.</span><span class="sxs-lookup"><span data-stu-id="72227-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="72227-130">Du kan vælge et antal vedligeholdelsestidsplanlinjer i **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer** og klikke på **Juster tidsplan**, hvis du vil foretage de samme reguleringer på flere linjer.</span><span class="sxs-lookup"><span data-stu-id="72227-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="72227-131">Du kan ændre de forventede start- og slutdatoer, serviceniveauet og den ansvarlige vedligeholdelsesarbejdergruppe eller den ansvarlige vedligeholdelsesarbejder, der er relateret til de valgte vedligeholdelsestidsplanslinjer.</span><span class="sxs-lookup"><span data-stu-id="72227-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="72227-132">Når en vedligeholdelsestidsplanslinje er relateret til en arbejdsordre, vises arbejdsordre-id'et i feltet **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="72227-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="72227-133">I detaljevisningen **Alle aktiver** > oversigtspanelet **Vedligeholdelsesplaner for aktiver** kan du vælge vedligeholdelsesplaner for aktivet.</span><span class="sxs-lookup"><span data-stu-id="72227-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="72227-134">Hvis du senere hen sletter en vedligeholdelsesplanlinje, der er relateret til et aktiv i **Alle aktiver**, sletter du også automatisk alle vedligeholdelsestidsplanlinjer med statussen "Oprettet", der er oprettet på baggrund af den pågældende vedligeholdelsesplan.</span><span class="sxs-lookup"><span data-stu-id="72227-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="72227-135">Se også [Oprette et aktiv](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="72227-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="72227-136">I illustrationen nedenfor vises listesiden **Hele vedligeholdelsestidsplanen**.</span><span class="sxs-lookup"><span data-stu-id="72227-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Figur 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]