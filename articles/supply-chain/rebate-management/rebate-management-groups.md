---
title: Rabatstyringsgrupper
description: Dette emne beskriver, hvordan du konfigurerer rabatstyringsgrupper. Rabatstyringsgrupper kan bruges under rabatberegninger og kan knyttes til en masterpost.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920055"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="96c33-104">Rabatstyringsgrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96c33-105">Rabat- og fradragsberegninger kan være baseret på grupper.</span><span class="sxs-lookup"><span data-stu-id="96c33-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="96c33-106">Der kan oprettes rabatstyringsgrupper for debitorer, kreditorer og varer.</span><span class="sxs-lookup"><span data-stu-id="96c33-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="96c33-107">De kan knyttes til en masterpost.</span><span class="sxs-lookup"><span data-stu-id="96c33-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="96c33-108">Debitorgrupper for rabatstyring</span><span class="sxs-lookup"><span data-stu-id="96c33-108">Rebate management customer groups</span></span>

<span data-ttu-id="96c33-109">Beregningen for en debitorgruppe oprettes ofte for en kæde af firmaer som f.eks. en supermarkedskæde eller et franchisefirma.</span><span class="sxs-lookup"><span data-stu-id="96c33-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="96c33-110">Denne type beregning vedrører normalt en rabat.</span><span class="sxs-lookup"><span data-stu-id="96c33-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="96c33-111">Der beregnes ofte et fradrag uden at tage højde for, hvem den relevante ordre er solgt til.</span><span class="sxs-lookup"><span data-stu-id="96c33-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="96c33-112">Der er dog undtagelser.</span><span class="sxs-lookup"><span data-stu-id="96c33-112">However, there are exceptions.</span></span> <span data-ttu-id="96c33-113">En licenstager kan f.eks. oprette et fradragsskema, hvor debitorgruppe A modtager 4 procent, mens debitorgruppe B kun får 3 procent.</span><span class="sxs-lookup"><span data-stu-id="96c33-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="96c33-114">Konfigurer kundegrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-114">Set up customer groups</span></span>

<span data-ttu-id="96c33-115">Du kan arbejde med debitorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="96c33-116">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="96c33-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="96c33-117">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="96c33-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="96c33-118">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="96c33-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="96c33-119">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="96c33-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="96c33-120">Administrere tildelinger af debitorgrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-120">Manage customer group assignments</span></span>

<span data-ttu-id="96c33-121">Hver debitor kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="96c33-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="96c33-122">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra debitorlisten.</span><span class="sxs-lookup"><span data-stu-id="96c33-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="96c33-123">Hvis du vil se, tilføje eller fjerne debitorer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="96c33-124">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Debitorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="96c33-125">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="96c33-125">Select the group to manage.</span></span>
1. <span data-ttu-id="96c33-126">Vælg **Debitorer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="96c33-127">Siden **Rabatstyringsgrupper** vises med en liste over debitorer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="96c33-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="96c33-128">Gå til handlingsruden, og vælg **Ny** for at føje en ny debitor til gruppen for at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-129">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-130">**Debitorkonto** – Vælg debitorkonto-id.</span><span class="sxs-lookup"><span data-stu-id="96c33-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="96c33-131">**Navn** – Angiv et navn og/eller en beskrivelse af debitoren.</span><span class="sxs-lookup"><span data-stu-id="96c33-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="96c33-132">Hvis du vil fjerne en debitor fra gruppen, skal du markere debitoren og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="96c33-133">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt debitor, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="96c33-134">Gå til **Debitorer \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="96c33-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="96c33-135">Vælg den debitor, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="96c33-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="96c33-136">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="96c33-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="96c33-137">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte debitor allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="96c33-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="96c33-138">Gå til handlingsruden, og vælg **Ny** for at føje debitoren til en ny gruppe for at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-139">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-140">**Rabatstyringsgruppe** – Vælg den gruppe, hvor debitoren skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="96c33-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="96c33-141">**Beskrivelse** – Angiv en beskrivelse af gruppen (f.eks. for at forklare, hvorfor debitoren er medlem af den).</span><span class="sxs-lookup"><span data-stu-id="96c33-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="96c33-142">Hvis du vil fjerne en debitor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="96c33-143">Rabatstyringsgrupper for kreditor</span><span class="sxs-lookup"><span data-stu-id="96c33-143">Rebate management vendor groups</span></span>

<span data-ttu-id="96c33-144">Beregningen for en gruppe af kreditorer oprettes ofte for en gruppe leveringssteder.</span><span class="sxs-lookup"><span data-stu-id="96c33-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="96c33-145">Denne type beregning vedrører normalt en rabat.</span><span class="sxs-lookup"><span data-stu-id="96c33-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="96c33-146">Konfigurere kreditorgrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-146">Set up vendor groups</span></span>

<span data-ttu-id="96c33-147">Du kan arbejde med kreditorgrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="96c33-148">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="96c33-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="96c33-149">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="96c33-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="96c33-150">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="96c33-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="96c33-151">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="96c33-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="96c33-152">Administrere tildelinger af kreditorgrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-152">Manage vendor group assignments</span></span>

<span data-ttu-id="96c33-153">Hver kreditor kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="96c33-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="96c33-154">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra kreditorlisten.</span><span class="sxs-lookup"><span data-stu-id="96c33-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="96c33-155">Hvis du vil se, tilføje eller fjerne kreditorer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="96c33-156">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Kreditorgrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="96c33-157">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="96c33-157">Select the group to manage.</span></span>
1. <span data-ttu-id="96c33-158">Vælg **Kreditorer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="96c33-159">Siden **Rabatstyringsgrupper** vises med en liste over kreditorer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="96c33-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="96c33-160">Gå til handlingsruden, og vælg **Ny** for at føje en ny kreditor til gruppen ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-161">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-162">**Kreditorkonto** – Vælg kreditorkonto-id.</span><span class="sxs-lookup"><span data-stu-id="96c33-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="96c33-163">**Navn** – Angiv et navn og/eller en beskrivelse af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="96c33-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="96c33-164">Hvis du vil fjerne en kreditor fra gruppen, skal du markere kreditoren og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="96c33-165">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt kreditor, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="96c33-166">Gå til **Kreditor \> Kreditorer \> Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="96c33-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="96c33-167">Vælg den kreditor, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="96c33-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="96c33-168">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Kreditor**.</span><span class="sxs-lookup"><span data-stu-id="96c33-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="96c33-169">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte kreditor allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="96c33-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="96c33-170">Gå til handlingsruden, og vælg **Ny** for at føje kreditoren til en ny gruppe ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-171">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-172">**Rabatstyringsgruppe** – Vælg den gruppe, hvor kreditoren skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="96c33-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="96c33-173">**Beskrivelse** – Angiv en beskrivelse af gruppen (f.eks. for at forklare, hvorfor kreditoren er medlem af den).</span><span class="sxs-lookup"><span data-stu-id="96c33-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="96c33-174">Hvis du vil fjerne en kreditor fra en gruppe, skal du vælge gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="96c33-175">Varerabatgrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-175">Item rebate groups</span></span>

<span data-ttu-id="96c33-176">Ved at gruppere varer har du større fleksibilitet, når der beregnes rabatter og fradrag.</span><span class="sxs-lookup"><span data-stu-id="96c33-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="96c33-177">Denne metode er ofte en mere effektiv måde at konfigurere rabatter og fradrag for debitorer og kreditorer på.</span><span class="sxs-lookup"><span data-stu-id="96c33-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="96c33-178">Konfigurer varegrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-178">Set up item groups</span></span>

<span data-ttu-id="96c33-179">Du kan arbejde med varegrupper for rabatstyring ved at gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="96c33-180">Brug knapperne i handlingsruden til at tilføje og fjerne grupper efter behov.</span><span class="sxs-lookup"><span data-stu-id="96c33-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="96c33-181">For hver gruppe skal du angive følgende felter:</span><span class="sxs-lookup"><span data-stu-id="96c33-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="96c33-182">**Rabatstyringsgruppe** – Angiv et entydigt navn til gruppen.</span><span class="sxs-lookup"><span data-stu-id="96c33-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="96c33-183">**Beskrivelse** – Angiv en beskrivelse af gruppen for at give flere oplysninger om, hvordan den skal bruges.</span><span class="sxs-lookup"><span data-stu-id="96c33-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="96c33-184">Administrere tildelinger af varegrupper</span><span class="sxs-lookup"><span data-stu-id="96c33-184">Manage item group assignments</span></span>

<span data-ttu-id="96c33-185">Hver vare kan tilhøre et vilkårligt antal rabatstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="96c33-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="96c33-186">Hvis du vil se og tildele gruppemedlemmer, kan du starte enten fra gruppelisten eller fra varelisten.</span><span class="sxs-lookup"><span data-stu-id="96c33-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="96c33-187">Du kan også tilføje varer på baggrund af kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="96c33-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="96c33-188">Hvis du vil se, tilføje eller fjerne varer for en valgt gruppe, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="96c33-189">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="96c33-190">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="96c33-190">Select the group to manage.</span></span>
1. <span data-ttu-id="96c33-191">Vælg **Varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="96c33-192">Siden **Rabatstyringsgrupper** vises med en liste over varer, der allerede er medlem af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="96c33-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="96c33-193">Gå til handlingsruden, og vælg **Ny** for at føje en ny vare til gruppen ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-194">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-195">**Varekonto** – Vælg varekonto-id.</span><span class="sxs-lookup"><span data-stu-id="96c33-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="96c33-196">**Produktnavn** – Angiv et navn og/eller en beskrivelse af varen.</span><span class="sxs-lookup"><span data-stu-id="96c33-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="96c33-197">Hvis du vil fjerne en vare fra gruppen, skal du markere varen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="96c33-198">Hvis du vil se, tilføje eller fjerne gruppetildelinger for en valgt vare, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="96c33-199">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="96c33-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="96c33-200">Vælg den vare, du vil arbejde med.</span><span class="sxs-lookup"><span data-stu-id="96c33-200">Select the item to work with.</span></span>
1. <span data-ttu-id="96c33-201">Vælg **Rabatstyringsgrupper** i gruppen **Rabatstyring** i handlingsruden under fanen **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="96c33-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="96c33-202">Siden **Rabatstyringsgrupper** vises med en liste over grupper, som den valgte vare allerede er medlem af.</span><span class="sxs-lookup"><span data-stu-id="96c33-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="96c33-203">Gå til handlingsruden, og vælg **Ny** for at føje varen til en ny gruppe ved at tilføje en række i gitteret.</span><span class="sxs-lookup"><span data-stu-id="96c33-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="96c33-204">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="96c33-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="96c33-205">**Rabatstyringsgruppe** – Vælg den gruppe, hvor varen skal tilføjes.</span><span class="sxs-lookup"><span data-stu-id="96c33-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="96c33-206">**Beskrivelse** – Angiv en beskrivelse af gruppen (f.eks. for at forklare, hvorfor varen er medlem af den).</span><span class="sxs-lookup"><span data-stu-id="96c33-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="96c33-207">Hvis du vil fjerne en vare fra en gruppe, skal du markere gruppen og derefter vælge **Slet** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="96c33-208">Hvis du vil føje varer til en gruppe på basis af kategorihierarkiet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="96c33-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="96c33-209">Gå til **Rabatstyring \> Konfiguration af rabatstyringsgrupper \> Varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="96c33-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="96c33-210">Vælg den gruppe, der skal administreres.</span><span class="sxs-lookup"><span data-stu-id="96c33-210">Select the group to manage.</span></span>
1. <span data-ttu-id="96c33-211">Vælg **Tilføj varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="96c33-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="96c33-212">Vælg en kategori på øverste niveau i feltet **Kategorihierarki** i dialogboksen **Tilføj varer**.</span><span class="sxs-lookup"><span data-stu-id="96c33-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="96c33-213">Varehierarkiet åbnes i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="96c33-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="96c33-214">Vælg det hierarkiniveau, du leder efter.</span><span class="sxs-lookup"><span data-stu-id="96c33-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="96c33-215">Varer fra det valgte hierarki og hierarkiniveau vises nu i højre rude.</span><span class="sxs-lookup"><span data-stu-id="96c33-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="96c33-216">Benyt følgende fremgangsmåde, når du vil arbejde med ruden:</span><span class="sxs-lookup"><span data-stu-id="96c33-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="96c33-217">Markér afkrydsningsfeltet for hver vare, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="96c33-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="96c33-218">Markér afkrydsningsfeltet i gitteroverskriften for at vælge alle de viste varer.</span><span class="sxs-lookup"><span data-stu-id="96c33-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="96c33-219">Vælg knappen **Vis valgte** for at filtrere gitteret, så det kun viser de varer, du har valgt indtil videre.</span><span class="sxs-lookup"><span data-stu-id="96c33-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="96c33-220">Vælg knappen igen for at vende tilbage til hele listen.</span><span class="sxs-lookup"><span data-stu-id="96c33-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="96c33-221">Vælg **OK** for at anvende dit varevalg på den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="96c33-221">Select **OK** to apply your item selection to the selected group.</span></span>
