---
title: Rabatstyringsgrupper
description: Dette emne beskriver, hvordan du konfigurerer rabatstyringsgrupper. Rabatstyringsgrupper kan bruges under rabatberegninger og kan knyttes til en masterpost.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271071"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="1402d-104">Rabatstyringsgrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1402d-105">Beregninger af rabatstyring kan være baseret på grupper.</span><span class="sxs-lookup"><span data-stu-id="1402d-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="1402d-106">Der kan oprettes rabatstyringsgrupper for debitorer, kreditorer og varer.</span><span class="sxs-lookup"><span data-stu-id="1402d-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="1402d-107">De kan knyttes til en masterpost.</span><span class="sxs-lookup"><span data-stu-id="1402d-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="1402d-108">Debitorgrupper for rabatstyring</span><span class="sxs-lookup"><span data-stu-id="1402d-108">Rebate management customer groups</span></span>

<span data-ttu-id="1402d-109">Beregningen for en debitorgruppe oprettes ofte for en kæde af firmaer som f.eks. en supermarkedskæde eller et franchisefirma.</span><span class="sxs-lookup"><span data-stu-id="1402d-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="1402d-110">Denne type beregning vedrører normalt en rabat.</span><span class="sxs-lookup"><span data-stu-id="1402d-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="1402d-111">Der beregnes ofte et fradrag uden at tage højde for, hvem den relevante ordre er solgt til.</span><span class="sxs-lookup"><span data-stu-id="1402d-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="1402d-112">Der er dog undtagelser.</span><span class="sxs-lookup"><span data-stu-id="1402d-112">However, there are exceptions.</span></span> <span data-ttu-id="1402d-113">En licenstager kan f.eks. oprette et fradragsskema, hvor debitorgruppe A modtager 4 procent, mens debitorgruppe B kun får 3 procent.</span><span class="sxs-lookup"><span data-stu-id="1402d-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="1402d-114">Konfigurer kundegrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-114">Set up customer groups</span></span>

<span data-ttu-id="1402d-115">Du kan arbejde med debitorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="1402d-116">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="1402d-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="1402d-117">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1402d-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="1402d-118">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="1402d-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="1402d-119">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="1402d-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="1402d-120">Administrere tildelinger af debitorgrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-120">Manage customer group assignments</span></span>

<span data-ttu-id="1402d-121">Hver debitor kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="1402d-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="1402d-122">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra debitorlisten.</span><span class="sxs-lookup"><span data-stu-id="1402d-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="1402d-123">Hvis du vil se, tilføje eller fjerne debitorer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="1402d-124">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="1402d-125">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="1402d-125">Select the group to manage.</span></span>
1. <span data-ttu-id="1402d-126">Vælg **Debitorer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="1402d-127">Siden **Rabatstyringsgrupper** vises med en liste over debitorer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="1402d-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="1402d-128">Gå til handlingsruden, og vælg **Ny** for at føje en ny debitor til gruppen for at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-129">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-130">**Debitorkonto** – Vælg debitorkonto-id.</span><span class="sxs-lookup"><span data-stu-id="1402d-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="1402d-131">Hvis du vil fjerne en debitor fra gruppen, skal du markere debitoren og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="1402d-132">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt debitor, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="1402d-133">Gå til **Debitorer \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="1402d-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="1402d-134">Vælg den debitor, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="1402d-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="1402d-135">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="1402d-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="1402d-136">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte debitor allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="1402d-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="1402d-137">Gå til handlingsruden, og vælg **Ny** for at føje debitoren til en ny gruppe for at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-138">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-139">**Rabatstyringsgruppe** – Vælg den gruppe, hvor debitoren skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="1402d-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="1402d-140">Hvis du vil fjerne en debitor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="1402d-141">Rabatstyringsgrupper for kreditor</span><span class="sxs-lookup"><span data-stu-id="1402d-141">Rebate management vendor groups</span></span>

<span data-ttu-id="1402d-142">Beregningen for en gruppe af kreditorer oprettes ofte for en gruppe leveringssteder.</span><span class="sxs-lookup"><span data-stu-id="1402d-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="1402d-143">Denne type beregning vedrører normalt en rabat.</span><span class="sxs-lookup"><span data-stu-id="1402d-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="1402d-144">Konfigurere kreditorgrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-144">Set up vendor groups</span></span>

<span data-ttu-id="1402d-145">Du kan arbejde med kreditorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="1402d-146">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="1402d-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="1402d-147">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1402d-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="1402d-148">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="1402d-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="1402d-149">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="1402d-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="1402d-150">Administrere tildelinger af kreditorgrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-150">Manage vendor group assignments</span></span>

<span data-ttu-id="1402d-151">Hver kreditor kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="1402d-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="1402d-152">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra kreditorlisten.</span><span class="sxs-lookup"><span data-stu-id="1402d-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="1402d-153">Hvis du vil se, tilføje eller fjerne kreditorer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="1402d-154">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="1402d-155">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="1402d-155">Select the group to manage.</span></span>
1. <span data-ttu-id="1402d-156">Vælg **Kreditorer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="1402d-157">Siden **Rabatstyringsgrupper** vises med en liste over kreditorer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="1402d-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="1402d-158">Gå til handlingsruden, og vælg **Ny** for at føje en ny kreditor til gruppen ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-159">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-160">**Kreditorkonto** – Vælg kreditorkonto-id.</span><span class="sxs-lookup"><span data-stu-id="1402d-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="1402d-161">Hvis du vil fjerne en kreditor fra gruppen, skal du markere kreditoren og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="1402d-162">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt kreditor, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="1402d-163">Gå til **Kreditor \> Kreditorer \> Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="1402d-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="1402d-164">Vælg den kreditor, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="1402d-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="1402d-165">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Kreditor**.</span><span class="sxs-lookup"><span data-stu-id="1402d-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="1402d-166">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte kreditor allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="1402d-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="1402d-167">Gå til handlingsruden, og vælg **Ny** for at føje kreditoren til en ny gruppe ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-168">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-169">**Rabatstyringsgruppe** – Vælg den gruppe, hvor kreditoren skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="1402d-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="1402d-170">Hvis du vil fjerne en kreditor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="1402d-171">Varerabatgrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-171">Item rebate groups</span></span>

<span data-ttu-id="1402d-172">Ved at gruppere varer har du større fleksibilitet, når der beregnes rabatter og fradrag.</span><span class="sxs-lookup"><span data-stu-id="1402d-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="1402d-173">Denne metode er ofte en mere effektiv måde at konfigurere rabatter og fradrag for debitorer og kreditorer på.</span><span class="sxs-lookup"><span data-stu-id="1402d-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="1402d-174">Konfigurer varegrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-174">Set up item groups</span></span>

<span data-ttu-id="1402d-175">Du kan arbejde med varegrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="1402d-176">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="1402d-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="1402d-177">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="1402d-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="1402d-178">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="1402d-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="1402d-179">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="1402d-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="1402d-180">Administrere tildelinger af varegrupper</span><span class="sxs-lookup"><span data-stu-id="1402d-180">Manage item group assignments</span></span>

<span data-ttu-id="1402d-181">Hver vare kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="1402d-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="1402d-182">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra varelisten.</span><span class="sxs-lookup"><span data-stu-id="1402d-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="1402d-183">Du kan også tilføje varer på baggrund af kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="1402d-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="1402d-184">Hvis du vil se, tilføje eller fjerne varer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="1402d-185">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="1402d-186">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="1402d-186">Select the group to manage.</span></span>
1. <span data-ttu-id="1402d-187">Vælg **Varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="1402d-188">Siden **Rabatstyringsgrupper** vises med en liste over varer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="1402d-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="1402d-189">Gå til handlingsruden, og vælg **Ny** for at føje en ny vare til gruppen ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-190">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-191">**Varekonto** – Vælg varekonto-id.</span><span class="sxs-lookup"><span data-stu-id="1402d-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="1402d-192">Hvis du vil fjerne en vare fra gruppen, skal du markere varen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="1402d-193">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt vare, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="1402d-194">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="1402d-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1402d-195">Vælg den vare, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="1402d-195">Select the item to work with.</span></span>
1. <span data-ttu-id="1402d-196">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="1402d-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="1402d-197">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte vare allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="1402d-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="1402d-198">Gå til handlingsruden, og vælg **Ny** for at føje varen til en ny gruppe ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="1402d-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="1402d-199">Angiv derefter følgende felt til den nye række:</span><span class="sxs-lookup"><span data-stu-id="1402d-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="1402d-200">**Rabatstyringsgruppe** – Vælg den gruppe, hvor varen skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="1402d-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="1402d-201">Hvis du vil fjerne en vare fra en gruppe, skal du markere gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="1402d-202">Hvis du vil føje varer til en gruppe på basis af kategorihierarkiet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1402d-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1402d-203">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="1402d-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="1402d-204">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="1402d-204">Select the group to manage.</span></span>
1. <span data-ttu-id="1402d-205">Vælg **Tilføj varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1402d-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="1402d-206">Vælg en kategori på øverste niveau i feltet **Kategorihierarki** i dialogboksen **Tilføj varer**.</span><span class="sxs-lookup"><span data-stu-id="1402d-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="1402d-207">Varehierarkiet åbnes i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1402d-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="1402d-208">Vælg det hierarkiniveau, du leder efter.</span><span class="sxs-lookup"><span data-stu-id="1402d-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="1402d-209">Varer fra det valgte hierarki og hierarkiniveau vises nu i højre rude.</span><span class="sxs-lookup"><span data-stu-id="1402d-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="1402d-210">Benyt følgende fremgangsmåde, når du vil arbejde med ruden:</span><span class="sxs-lookup"><span data-stu-id="1402d-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="1402d-211">Markér afkrydsningsfeltet for hver vare, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="1402d-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="1402d-212">Markér afkrydsningsfeltet i gitteroverskriften for at vælge alle de viste varer.</span><span class="sxs-lookup"><span data-stu-id="1402d-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="1402d-213">Vælg knappen **Vis valgte** for at filtrere gitteret, så det kun viser de varer, du har valgt indtil videre.</span><span class="sxs-lookup"><span data-stu-id="1402d-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="1402d-214">Vælg knappen igen for at vende tilbage til hele listen.</span><span class="sxs-lookup"><span data-stu-id="1402d-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="1402d-215">Vælg **OK** for at anvende dit varevalg på den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="1402d-215">Select **OK** to apply your item selection to the selected group.</span></span>
