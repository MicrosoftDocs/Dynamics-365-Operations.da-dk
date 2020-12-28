---
title: Arbejdsordrepuljer
description: I dette emne beskrives, hvordan du kan arbejde med arbejdsordrepuljer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424923"
---
# <a name="work-order-pools"></a><span data-ttu-id="eab18-103">Arbejdsordrepuljer</span><span class="sxs-lookup"><span data-stu-id="eab18-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="eab18-104">Du kan bruge arbejdsordrepuljer til at gruppere arbejdsordrer, der har noget fælles.</span><span class="sxs-lookup"><span data-stu-id="eab18-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="eab18-105">Her er nogle eksempler på ting, du kan oprette arbejdsordrepuljer til:</span><span class="sxs-lookup"><span data-stu-id="eab18-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="eab18-106">Arbejdshold, f.eks. Vedligeholdelseshold A eller Vedligeholdelseshold B</span><span class="sxs-lookup"><span data-stu-id="eab18-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="eab18-107">Faglige kompetencer, f.eks. elektrikere eller VVS-folk</span><span class="sxs-lookup"><span data-stu-id="eab18-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="eab18-108">Fysiske adresser</span><span class="sxs-lookup"><span data-stu-id="eab18-108">Physical locations</span></span>  

- <span data-ttu-id="eab18-109">Tidsplaner, f.eks. uger eller andre perioder</span><span class="sxs-lookup"><span data-stu-id="eab18-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="eab18-110">Når du har brug for det, kan du anbringe én arbejdsordre i flere arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="eab18-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="eab18-111">Oprette en arbejdsordrepulje</span><span class="sxs-lookup"><span data-stu-id="eab18-111">Create a work order pool</span></span>

<span data-ttu-id="eab18-112">På siden **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** kan du få en oversigt over dine arbejdsordrepuljer og oprette nye puljer.</span><span class="sxs-lookup"><span data-stu-id="eab18-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="eab18-113">Vælg **Styring af aktiver** > **Almindelig** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer**.</span><span class="sxs-lookup"><span data-stu-id="eab18-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="eab18-114">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="eab18-114">Select **New**.</span></span>

3. <span data-ttu-id="eab18-115">Angiv et id for arbejdsordrepuljen i feltet **Pulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="eab18-116">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="eab18-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="eab18-117">Indstil **Aktiv** til **Ja** for at angive, at arbejdsordrepuljen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="eab18-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="eab18-118">Indstil **Slet arbejdsordrerelationer** til **Ja**, hvis arbejdsordrer automatisk skal fjernes fra arbejdsordrepuljen.</span><span class="sxs-lookup"><span data-stu-id="eab18-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="eab18-119">I feltet **Slet livscyklustilstand** skal du vælge livscyklustilstanden for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="eab18-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="eab18-120">For eksempel kan livscyklustilstanden for færdiggørelse af en arbejdsordre indstilles til automatisk at slette relationer til arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="eab18-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="eab18-121">Du kan begynde at føje arbejdsordrer til din arbejdsordrepulje med det samme.</span><span class="sxs-lookup"><span data-stu-id="eab18-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="eab18-122">Vælg **Tilføj linje** i oversigtspanelet **Arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="eab18-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="eab18-123">I feltet **Arbejdsordre** skal du vælge en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="eab18-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="eab18-124">De relaterede felter opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="eab18-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="eab18-125">Gentag trin 8 til 9 for at tilføje flere arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="eab18-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="eab18-126">Hvis de arbejdsordrer, du har tilføjet, skal udføres i en bestemt rækkefølge, kan du i feltet **Sorteringsrækkefølge** angive numrene **1**, **2**, **3** osv. for at angive den pågældende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="eab18-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="eab18-127">Hvis du vil have vist en liste over alle de arbejdsordrer, der er medtaget i arbejdsordrepuljen, skal du vælge **Arbejdsordrer** i gruppen **Vis relateret til arbejdsordrepulje** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Alle arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="eab18-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="eab18-128">Hvis du vil beregne og se kapacitetsbelastningen for vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer, skal du i handlingsruden under fanen **Arbejdsordrepulje** i gruppen **Vis relateret til arbejdsordrepulje** vælge **Kapacitetsbelastning** for at åbne dialogboksen **Beregn kapacitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="eab18-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="eab18-129">Hvis du vil beregne og se prognoser for varer (reservedele og andre påkrævede varer), der er relateret til vedligeholdelsesplanen, ikke-planlagte arbejdsordrer og planlagte arbejdsordrer, skal du i handlingsruden under fanen **Arbejdsordrepulje** i gruppen **Vis relateret til arbejdsordrepulje** vælge **Varebudget** for at åbne dialogboksen **Beregn varebudget**.</span><span class="sxs-lookup"><span data-stu-id="eab18-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="eab18-130">Hvis du vil have vist en liste over indkøbsrekvisitioner, der er relatere til arbejdsordrer i arbejdsordrepuljen, skal du vælge **Indkøbsrekvisition for arbejdsordre** i gruppen **Indkøb** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Indkøbsrekvisition for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="eab18-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="eab18-131">Hvis du vil have vist en liste over indkøbsordrer, der er relatere til arbejdsordrer i arbejdsordrepuljen, skal du vælge **Arbejdsordreindkøb** i gruppen **Indkøb** under fanen **Arbejdsordrepulje** i handlingsruden for at åbne siden **Arbejdsordreindkøb**.</span><span class="sxs-lookup"><span data-stu-id="eab18-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="eab18-132">Når en arbejdsordrepulje ikke længere er relevant for din arbejdsplanlægning, skal du indstille **Aktiv** til **Nej** for den pågældende pulje i listevisningen på siden **Arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="eab18-133">Hvis du vil slette alle linjer i en arbejdsordre, skal du angive indstillingen **Slet arbejdsordrerelationer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="eab18-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="eab18-134">Denne indstilling er nyttig, hvis du f.eks. vil oprette en tom pulje, som du senere kan bruge til andre arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="eab18-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="eab18-135">Husk at indstille **Slet arbejdsordrerelationer** til **Nej**, hvis du vil bruge arbejdsordrepuljen til at oprette nye arbejdsordrerelationer på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="eab18-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="eab18-136">I illustrationen herunder vises et eksempel på listesiden **Arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Figur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="eab18-138">Føje en arbejdsordre til en arbejdsordrepulje</span><span class="sxs-lookup"><span data-stu-id="eab18-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="eab18-139">Som beskrevet i ovenstående afsnit kan du føje arbejdsordrer til en arbejdsordrepulje, når du opretter puljen.</span><span class="sxs-lookup"><span data-stu-id="eab18-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="eab18-140">Du kan også føje arbejdsordrer til en arbejdsordre pulje på listesiden **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="eab18-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="eab18-141">Vælg arbejdsordren, og vælg derefter **Arbejdsordrepulje** i gruppen **Vedligehold** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="eab18-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="eab18-142">Vælg arbejdsordren på listen, og klik på **Arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="eab18-143">Vælg **Tilføj** i feltet **Tilføj/fjern** i dialogboksen **Vedligehold arbejdsordrepulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="eab18-144">Vælg arbejdsordrepuljen i feltet **Pulje**.</span><span class="sxs-lookup"><span data-stu-id="eab18-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="eab18-145">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="eab18-145">Select **OK**.</span></span>

6. <span data-ttu-id="eab18-146">Hvis du vil placere den arbejdsordre, du har tilføjet, i en bestemt rækkefølge i arbejdsordrepuljen, skal du vælge puljen på listesiden **Alle arbejdsordrepuljer** eller **Aktive arbejdsordrepuljer** og derefter vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="eab18-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="eab18-147">Brug derefter feltet **Sorteringsrækkefølge** i oversigtspanelet **Arbejdsordrer** på siden **Arbejdsordrepulje** til at justere sorteringsrækkefølgen af de arbejdsordrer, der skal medtages i puljen.</span><span class="sxs-lookup"><span data-stu-id="eab18-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="eab18-148">Hvis du vil fjerne en arbejdsordre fra en arbejdsordrepulje, skal du gentage disse trin, men vælge **Fjern** i trin 3.</span><span class="sxs-lookup"><span data-stu-id="eab18-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

