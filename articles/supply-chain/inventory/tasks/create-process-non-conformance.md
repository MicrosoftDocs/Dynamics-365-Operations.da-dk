---
title: Oprette og behandle uoverensstemmelser
description: Dette emne beskriver, hvordan du håndterer uoverensstemmelser baseret på en eksisterende kvalitetsordre.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956200"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="9a19a-103">Oprette og behandle uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a19a-104">Dette emne beskriver, hvordan du håndterer uoverensstemmelser baseret på en eksisterende kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="9a19a-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="9a19a-105">Normalt håndteres uoverensstemmelser af en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="9a19a-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="9a19a-106">Du skal som en forudsætning have en kvalitetsordre til rådighed.</span><span class="sxs-lookup"><span data-stu-id="9a19a-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="9a19a-107">(Du kan finde oplysninger om oprettelse af en kvalitetsordre i [Inspicere varers kvalitet](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="9a19a-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="9a19a-108">Før en bruger kan behandle godkendelsen af en uoverensstemmelse, skal en arbejder tildeles i feltet **Person** på siden **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="9a19a-109">Derudover skal indstillingen **Aktivér dokumenthåndtering** angives til *Ja* i brugerindstillinger, før brugeren kan bruge dokumentbemærkningerne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="9a19a-110">Oprette en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-110">Create a nonconformance</span></span>

<span data-ttu-id="9a19a-111">Benyt denne fremgangsmåde for at oprette en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="9a19a-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-112">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-113">Vælg **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="9a19a-114">Vælg den problemtype, der blev fundet i inspektionsprocessen,I feltet **Problemtype** i dialogboksen **Opret uoverensstemmelse**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="9a19a-115">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="9a19a-116">Godkende eller afvise en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="9a19a-117">Hvis du vil godkende eller afvise en uoverensstemmelse, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="9a19a-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-118">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-119">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-120">Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-121">Vælg **Funktioner \> Godkend uoverensstemmelse** i handlingsruden for at godkende uoverensstemmelsen, eller **Funktioner \> Afvis uoverensstemmelse** for at afvise den.</span><span class="sxs-lookup"><span data-stu-id="9a19a-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="9a19a-122">Du kan knytte godkendte uoverensstemmelser til [relaterede operationer](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="9a19a-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="9a19a-123">På denne måde kan du registrere arbejde, der er udført som en del af håndteringen af uoverensstemmelser og rettelser.</span><span class="sxs-lookup"><span data-stu-id="9a19a-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="9a19a-124">Du bliver bedt om at bekræfte dit valg.</span><span class="sxs-lookup"><span data-stu-id="9a19a-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="9a19a-125">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="9a19a-126">Føje operationer og andre detaljer til uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="9a19a-127">Når du har oprettet en uoverensstemmelse, kan du begynde at tilføje relaterede operationer og angive yderligere oplysninger om disse operationer.</span><span class="sxs-lookup"><span data-stu-id="9a19a-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="9a19a-128">Du kan kun føje relaterede operationer til uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="9a19a-129">Udover de grundlæggende oplysninger kan du føje følgende detaljer til en operation:</span><span class="sxs-lookup"><span data-stu-id="9a19a-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="9a19a-130">**Varer** – Du kan oprette en liste over forbrugte varer for at udføre rettelsen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="9a19a-131">Varerne kan f.eks. være produkter, der skal bruges til reparation af udstyr eller ingredienser, der er nødvendige for at reparere et færdigt produkt.</span><span class="sxs-lookup"><span data-stu-id="9a19a-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="9a19a-132">**Kvalitetsgebyrer** – Du kan oprette en liste over gebyrer, der påløber eller faktureres til eksterne kilder.</span><span class="sxs-lookup"><span data-stu-id="9a19a-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="9a19a-133">**Timeseddel** – Du kan oprette en logfil over den tid, hver arbejder bruger på operationen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="9a19a-134">De resterende indstillinger er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="9a19a-134">The remaining settings are optional.</span></span> <span data-ttu-id="9a19a-135">Omkostningerne for hver vare, kvalitetsgebyrer og timesedlen lægges sammen og vises i operationen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="9a19a-136">Du kan ikke redigere feltet **Omkostning** direkte i operationen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="9a19a-137">Oprette en operation for en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="9a19a-138">Benyt denne fremgangsmåde for at oprette en operation for en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="9a19a-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-139">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-140">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-141">Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-142">Vælg **Relaterede operationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="9a19a-143">På siden **Relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9a19a-144">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="9a19a-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9a19a-145">**Operation** – Vælg koden for den operation, der skal udføres for uoverensstemmelsen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="9a19a-146">**Årsag** – Angiv en detaljeret beskrivelse, der forklarer, hvorfor operationen er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="9a19a-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="9a19a-147">**Salgsordre** – Hvis den valgte operationskode er knyttet til salgsordretypen, skal du vælge den salgsordre, som operationen skal tilknyttes.</span><span class="sxs-lookup"><span data-stu-id="9a19a-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="9a19a-148">**Indkøbsordre** – Hvis den valgte operationskode er knyttet til indkøbsordretypen, skal du vælge den indkøbsordre, som operationen skal tilknyttes.</span><span class="sxs-lookup"><span data-stu-id="9a19a-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="9a19a-149">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="9a19a-150">Føje varer til en operation</span><span class="sxs-lookup"><span data-stu-id="9a19a-150">Add items to an operation</span></span>

<span data-ttu-id="9a19a-151">Benyt følgende fremgangsmåde for at føje varer til en operation.</span><span class="sxs-lookup"><span data-stu-id="9a19a-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-152">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-153">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-154">Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-155">Vælg **Relaterede operationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="9a19a-156">Vælg den operation på siden **Relaterede operationer**, som du vil føje varer til.</span><span class="sxs-lookup"><span data-stu-id="9a19a-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="9a19a-157">Vælg **Varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="9a19a-158">På siden **Relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9a19a-159">Angiv følgende felter for den nye række:</span><span class="sxs-lookup"><span data-stu-id="9a19a-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="9a19a-160">**Varenummer** – Vælg det produkt, der skal bruges som del af den valgte operation.</span><span class="sxs-lookup"><span data-stu-id="9a19a-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="9a19a-161">**Antal** – Angiv antallet af varer, der vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="9a19a-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-162">Du kan få vist omkostningen for varen i feltet **Omkostning** under fanen **Generelt**. Den viste omkostning hentes fra den omkostning, der er angivet på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="9a19a-163">Omkostningen kan ikke opdateres direkte på siden **Relateret operationsvare**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="9a19a-164">Omkostningerne for alle varer, der er tilføjet på siden **Relaterede operationsvarer**, føjes automatisk til feltet **Omkostning** på siden **Relaterede operationer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="9a19a-165">Gentag forrige trin for hver ekstra vare, du skal tilføje.</span><span class="sxs-lookup"><span data-stu-id="9a19a-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="9a19a-166">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="9a19a-167">Føje kvalitetsgebyrer til en operation</span><span class="sxs-lookup"><span data-stu-id="9a19a-167">Add quality charges to an operation</span></span>

<span data-ttu-id="9a19a-168">Benyt følgende fremgangsmåde for at føje kvalitetsgebyrer til en operation.</span><span class="sxs-lookup"><span data-stu-id="9a19a-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-169">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-170">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-171">Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-172">Vælg **Relaterede operationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="9a19a-173">Vælg den operation, du vil føje kvalitetsgebyrer til, på siden **Relaterede operationer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="9a19a-174">Vælg **Kvalitetsgebyrer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="9a19a-175">På siden **Relaterede operationsgebyrer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9a19a-176">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="9a19a-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9a19a-177">**Gebyrkode** – Vælg det kvalitetsgebyr, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="9a19a-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="9a19a-178">**Beskrivelse** – Indtast en detaljeret beskrivelse af gebyret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="9a19a-179">**Gebyrværdi** – Angiv beløbet for gebyret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="9a19a-180">Gentag forrige trin for hvert ekstra gebyr, du skal tilføje.</span><span class="sxs-lookup"><span data-stu-id="9a19a-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="9a19a-181">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="9a19a-182">Beløbet i feltet **Gebyrværdi** lægges automatisk sammen for alle kvalitetsgebyrer og føjes til eventuelle andre beløb i feltet **Omkostning** på siden **Relaterede operationer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="9a19a-183">Oprette en timeseddel for en operation</span><span class="sxs-lookup"><span data-stu-id="9a19a-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="9a19a-184">Benyt følgende fremgangsmåde for at føje en timeseddel til en operation.</span><span class="sxs-lookup"><span data-stu-id="9a19a-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-185">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-186">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-187">Du kan kun tilføje eller opdatere operationer for uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-188">Vælg **Relaterede operationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="9a19a-189">Vælg den operation, du vil føje en timeseddel til, på siden **Relaterede operationer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="9a19a-190">Vælg **Timeseddel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="9a19a-191">På siden **Timesedler for relaterede operationer** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9a19a-192">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="9a19a-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9a19a-193">**Dato** – Angiv den dato, hvor arbejdet blev udført.</span><span class="sxs-lookup"><span data-stu-id="9a19a-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="9a19a-194">Dette felt er som standard indstillet til dags dato.</span><span class="sxs-lookup"><span data-stu-id="9a19a-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="9a19a-195">**Arbejder** – Vælg den arbejder, som udførte arbejdet.</span><span class="sxs-lookup"><span data-stu-id="9a19a-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="9a19a-196">Dette felt er som standard angivet til den arbejder, der er tildelt den aktuelle bruger.</span><span class="sxs-lookup"><span data-stu-id="9a19a-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="9a19a-197">**Operationstimer** – Angiv antallet af timer, hvor der blev arbejdet på den valgte operation.</span><span class="sxs-lookup"><span data-stu-id="9a19a-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="9a19a-198">**Faktureret** – Markér dette afkrydsningsfelt, hvis tiden er blevet debiteret en debitor eller kreditor på en faktura.</span><span class="sxs-lookup"><span data-stu-id="9a19a-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-199">Du kan få vist omkostningerne i feltet **Omkostning** under fanen **Generelt**. Omkostningen beregnes ved hjælp af den sats, du definerer på siden **Lagerstyringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="9a19a-200">Gentag forrige trin for hvert ekstra timeseddellinje, du skal tilføje.</span><span class="sxs-lookup"><span data-stu-id="9a19a-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="9a19a-201">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="9a19a-202">Beløbet i feltet **Omkostning** lægges automatisk sammen for alle timeseddellinjer og føjes til eventuelle andre beløb i feltet **Omkostning** på siden **Relaterede operationer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="9a19a-203">Føje en rettelse til en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="9a19a-204">Hvis du vil tilføje en rettelse til en uoverensstemmelse, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="9a19a-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-205">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-206">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-207">Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-208">Vælg **Rettelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="9a19a-209">Vælg **Ny** på siden **Rettelser** i handlingsruden for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9a19a-210">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="9a19a-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9a19a-211">**Diagnosticering** – Vælg den diagnosticeringstype, der identificerer den type rettelse, du er ved at oprette.</span><span class="sxs-lookup"><span data-stu-id="9a19a-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="9a19a-212">**Arbejder** – Vælg den person, der er ansvarlig for rettelsen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="9a19a-213">**Rettelsesprioritet** – Vælg en indstilling for at angive, hvordan rettelsen skal prioriteres (*Lav*, *Normal* eller *Høj*).</span><span class="sxs-lookup"><span data-stu-id="9a19a-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="9a19a-214">**Ønsket dato** – Angiv den dato, hvor der blev anmodet om den korrigerende handling.</span><span class="sxs-lookup"><span data-stu-id="9a19a-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="9a19a-215">**Planlagt dato** – Angiv den dato, hvor rettelsen forventes at være fuldført.</span><span class="sxs-lookup"><span data-stu-id="9a19a-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="9a19a-216">**Kortsigtet løsning** – Markér dette afkrydsningsfelt, hvis den korrigerende handling kun retter uoverensstemmelsen i en kort periode.</span><span class="sxs-lookup"><span data-stu-id="9a19a-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="9a19a-217">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="9a19a-218">Markere en rettelse som fuldført</span><span class="sxs-lookup"><span data-stu-id="9a19a-218">Mark a correction as completed</span></span>

<span data-ttu-id="9a19a-219">Hvis du vil markere en rettelse af en uoverensstemmelse som fuldført, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="9a19a-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-220">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-221">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a19a-222">Du kan kun føje en rettelse til uoverensstemmelser, der er godkendte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="9a19a-223">Vælg **Rettelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="9a19a-224">Vælg den rettelse, der skal markeres som fuldført, på siden **Rettelser** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="9a19a-225">Vælg **Markér som fuldført** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="9a19a-226">Du bliver bedt om at bekræfte dit valg.</span><span class="sxs-lookup"><span data-stu-id="9a19a-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="9a19a-227">Vælg **OK** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-227">Select **OK** to continue.</span></span> <span data-ttu-id="9a19a-228">Feltet **Færdiggørelsesdato og -klokkeslæt** er indstillet til dags dato og og det aktuelle klokkeslæt, og afkrydsningsfeltet **Fuldført** er markeret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="9a19a-229">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="9a19a-230">Genåbne en fuldført rettelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-230">Reopen a completed correction</span></span>

<span data-ttu-id="9a19a-231">Hvis du vil genåbne en fuldført rettelse, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="9a19a-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-232">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-233">På listen skal du vælge den uoverensstemmelse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="9a19a-234">Vælg **Rettelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="9a19a-235">Vælg den rettelse, du vil genåbne, på siden **Rettelser** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="9a19a-236">Vælg **Genåbn** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="9a19a-237">Du bliver bedt om at bekræfte dit valg.</span><span class="sxs-lookup"><span data-stu-id="9a19a-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="9a19a-238">Vælg **OK** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-238">Select **OK** to continue.</span></span> <span data-ttu-id="9a19a-239">Værdien fjernes fra feltet **Færdiggørelsesdato og -klokkeslæt**, og markeringen i afkrydsningsfeltet **Fuldført** fjernes.</span><span class="sxs-lookup"><span data-stu-id="9a19a-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="9a19a-240">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-240">Close the page.</span></span>

<span data-ttu-id="9a19a-241">Du kan nu redigere eller opdatere rettelsen yderligere.</span><span class="sxs-lookup"><span data-stu-id="9a19a-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="9a19a-242">Når du er færdig, kan du markere rettelsen som fuldført igen.</span><span class="sxs-lookup"><span data-stu-id="9a19a-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="9a19a-243">Luk en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-243">Close a nonconformance</span></span>

<span data-ttu-id="9a19a-244">Benyt denne fremgangsmåde for at lukke en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="9a19a-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="9a19a-245">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="9a19a-246">Vælg en kvalitetsordre i gitteret.</span><span class="sxs-lookup"><span data-stu-id="9a19a-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="9a19a-247">Vælg **Forespørgsler \> Uoverensstemmelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="9a19a-248">Vælg måluoverensstemmelsen i gitteret på siden **Uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="9a19a-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="9a19a-249">Vælg **Funktioner \> Luk uoverensstemmelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9a19a-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="9a19a-250">Du bliver bedt om at bekræfte dit valg.</span><span class="sxs-lookup"><span data-stu-id="9a19a-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="9a19a-251">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9a19a-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9a19a-252">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="9a19a-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a19a-253">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9a19a-253">Additional resources</span></span>

- [<span data-ttu-id="9a19a-254">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="9a19a-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="9a19a-255">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="9a19a-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="9a19a-256">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="9a19a-257">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="9a19a-258">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="9a19a-259">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="9a19a-260">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="9a19a-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="9a19a-261">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="9a19a-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
