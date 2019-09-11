---
title: Arbejdsordrepuljer
description: I dette emne beskrives, hvordan du kan arbejde med arbejdsordrepuljer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875568"
---
# <a name="work-order-pools"></a><span data-ttu-id="92f45-103">Arbejdsordrepuljer</span><span class="sxs-lookup"><span data-stu-id="92f45-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="92f45-104">Du kan bruge arbejdsordrepuljer til at gruppere arbejdsordrer, der har noget fælles.</span><span class="sxs-lookup"><span data-stu-id="92f45-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="92f45-105">Du kan f.eks. oprette arbejdsordrepuljer for</span><span class="sxs-lookup"><span data-stu-id="92f45-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="92f45-106">arbejdshold, f.eks. Vedligeholdelseshold A, Vedligeholdelseshold B</span><span class="sxs-lookup"><span data-stu-id="92f45-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="92f45-107">fagligt kvalificerede, f.eks. elektrikere eller VVS-folk</span><span class="sxs-lookup"><span data-stu-id="92f45-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="92f45-108">fysiske placeringer</span><span class="sxs-lookup"><span data-stu-id="92f45-108">physical locations</span></span>  

- <span data-ttu-id="92f45-109">tidsplaner, f.eks. uger eller andre perioder</span><span class="sxs-lookup"><span data-stu-id="92f45-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="92f45-110">Hvis det er nødvendigt, kan én arbejdsordre placeres i mange arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="92f45-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="92f45-111">Oprette arbejdsordrepulje</span><span class="sxs-lookup"><span data-stu-id="92f45-111">Create work order pool</span></span>

<span data-ttu-id="92f45-112">I **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** kan du få en oversigt over dine arbejdsordrepuljer og oprette nye puljer.</span><span class="sxs-lookup"><span data-stu-id="92f45-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="92f45-113">Klik på **Styring af aktiver** > **Almindelig** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer**.</span><span class="sxs-lookup"><span data-stu-id="92f45-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="92f45-114">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92f45-114">Click **New**.</span></span>

3. <span data-ttu-id="92f45-115">Indsæt et arbejdsordrepulje-id i feltet **Pulje** og et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="92f45-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="92f45-116">Vælg "Ja" på **Aktiv**-til/fra-knappen for at angive, at arbejdsordrepuljen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="92f45-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="92f45-117">Vælg "Ja" på til/fra-knappen **Slet arbejdsordrerelationer**, hvis du ønsker, at arbejdsordrer automatisk skal fjernes fra arbejdsordrepuljen.</span><span class="sxs-lookup"><span data-stu-id="92f45-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="92f45-118">I feltet **Slet livscyklustilstand** skal du vælge livscyklustilstanden for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="92f45-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="92f45-119">For eksempel kan livscyklustilstanden for færdiggørelse af en arbejdsordre indstilles til automatisk at slette relationer til arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="92f45-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="92f45-120">Du kan begynde at føje arbejdsordrer til din arbejdsordrepulje med det samme.</span><span class="sxs-lookup"><span data-stu-id="92f45-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="92f45-121">Klik på **Tilføj linje** i oversigtspanelet **Arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="92f45-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="92f45-122">I feltet **Arbejdsordre** skal du vælge en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="92f45-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="92f45-123">De relaterede felter opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="92f45-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="92f45-124">Gentag trin 7-8, hvis du vil tilføje flere arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="92f45-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="92f45-125">I feltet **Sorteringsrækkefølge** kan du angive, om arbejdsordrerne skal udføres i en bestemt rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="92f45-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="92f45-126">Indsæt nummer 1, 2, 3 osv. for at angive en bestemt rækkefølge for de valgte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="92f45-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="92f45-127">Klik på knappen **Arbejdsordrer** for at få vist en liste over alle de arbejdsordrer, der er inkluderet i arbejdsordrepuljen.</span><span class="sxs-lookup"><span data-stu-id="92f45-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="92f45-128">Klik på knappen **Kapacitetsbelastning** for at åbne **Kapacitetsbelastning** og beregne og få vist kapacitetsbelastningen for vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="92f45-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="92f45-129">Klik på knappen **Varebudget** for at åbne **Varebudget** og beregne og få vist budgetter for varer (reservedele og andre påkrævede varer), der er relateret til vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="92f45-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="92f45-130">Klik på knappen **Indkøbsrekvisition i arbejdsordre** for at åbne listen **Indkøbsrekvisition i arbejdsordre** for at få vist en liste over indkøbsrekvisitioner, der er relateret til arbejdsordrerne i arbejdsordrepuljen.</span><span class="sxs-lookup"><span data-stu-id="92f45-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="92f45-131">Klik på knappen **Indkøb i arbejdsordre** for at åbne listen **Indkøb i arbejdsordre** og få vist en liste over indkøbsordrer, der er relateret til arbejdsordrerne i arbejdsordrepuljen.</span><span class="sxs-lookup"><span data-stu-id="92f45-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="92f45-132">Når en arbejdsordrepulje ikke længere er relevant for din arbejdsplanlægning, skal du vælge "Nej" i afkrydsningsfeltet **Aktiv** for den pågældende pulje i listevisningen **Arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="92f45-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="92f45-133">Marker afkrydsningsfeltet **Slet arbejdsordrerelationer**, hvis du vil slette alle arbejdsordrelinjer, f.eks. for at oprette en tom pulje, som du senere kan bruge til andre arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="92f45-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="92f45-134">Husk at fjerne markeringen i afkrydsningsfeltet **Slet arbejdsordrerelationer**, hvis du vil bruge arbejdsordrepuljen til at oprette nye arbejdsordrerelationer på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="92f45-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Figur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="92f45-136">Føje en arbejdsordre til en arbejdsordrepulje</span><span class="sxs-lookup"><span data-stu-id="92f45-136">Add work order to a work order pool</span></span>

<span data-ttu-id="92f45-137">Som beskrevet i ovenstående afsnit kan du føje arbejdsordrer til en arbejdsordrepulje, når du opretter puljen.</span><span class="sxs-lookup"><span data-stu-id="92f45-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="92f45-138">Du kan også føje en arbejdsordre til en arbejdsordrepulje fra en af **Alle arbejdsordrer** på listen.</span><span class="sxs-lookup"><span data-stu-id="92f45-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="92f45-139">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="92f45-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="92f45-140">Vælg arbejdsordren på listen, og klik på **Arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="92f45-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="92f45-141">Vælg "Tilføj" i feltet **Tilføj/fjern**.</span><span class="sxs-lookup"><span data-stu-id="92f45-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="92f45-142">Vælg arbejdsordrepuljen i feltet **Pulje**.</span><span class="sxs-lookup"><span data-stu-id="92f45-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="92f45-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="92f45-143">Click **OK**.</span></span>

6. <span data-ttu-id="92f45-144">Når du har føjet en arbejdsordre til en arbejdsordrepulje, og du vil placere arbejdsordren i en bestemt rækkefølge i puljen: Åbn en af listesiderne for arbejdsordrepuljer, vælg puljen, og klik på **Rediger**, og juster sorteringsrækkefølgen for arbejdsordrerne i puljen i formularen **Arbejdsordrepulje** > oversigtspanelet **Arbejdsordrer** > feltet **Sorteringsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="92f45-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="92f45-145">Hvis du vil fjerne den valgte arbejdsordre fra en arbejdsordrepulje, skal du vælge "Fjern" i trin 3.</span><span class="sxs-lookup"><span data-stu-id="92f45-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

