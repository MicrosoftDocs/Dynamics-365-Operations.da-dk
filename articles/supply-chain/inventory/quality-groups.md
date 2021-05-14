---
title: Varekvalitetsgrupper
description: Dette emne beskriver, hvordan du kan bruge og oprette varekvalitetsgrupper til logisk gruppering af produkter, så de kan tildeles til kvalitetstilknytninger med henblik på automatisk generering af kvalitetsordrer.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956590"
---
# <a name="item-quality-groups"></a><span data-ttu-id="b33db-103">Varekvalitetsgrupper</span><span class="sxs-lookup"><span data-stu-id="b33db-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b33db-104">En kvalitetsgruppe repræsenterer almindelige testkrav til varer.</span><span class="sxs-lookup"><span data-stu-id="b33db-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b33db-105">Dette emne beskriver, hvordan du kan bruge og oprette varekvalitetsgrupper til logisk gruppering af produkter, så de kan tildeles til kvalitetstilknytninger med henblik på automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="b33db-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="b33db-106">Hvis du vil konfigurere, redigere og have vist de varer, der er tildelt en kvalitetsgruppe, eller de kvalitetsgrupper, der er tildelt en vare, skal du gå til **Lagerstyring \> Opsætning \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="b33db-107">Når du har defineret testkravene på siden **Testgrupper**, kan du definere reglerne for automatisk generering af kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="b33db-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b33db-108">For at forenkle processen skal du undlade at definere regler for de enkelte varer.</span><span class="sxs-lookup"><span data-stu-id="b33db-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="b33db-109">I stedet kan du definere regler for en kvalitetsgruppe på siden **Kvalitetstilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="b33db-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="b33db-110">Eksempel på en varekvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33db-110">Example of an item quality group</span></span>

<span data-ttu-id="b33db-111">En produktionsvirksomhed indkøber forskellige råvarer, der har samme testkrav til indgående inspektion.</span><span class="sxs-lookup"><span data-stu-id="b33db-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b33db-112">Virksomheden definerer derfor en kvalitetsgruppe og tildeler derefter kvalitetsgruppen de varenumre, der er tilknyttet råmaterialer for den pågældende gruppe.</span><span class="sxs-lookup"><span data-stu-id="b33db-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b33db-113">Senere indkøber virksomheden en ny type råvarer med de samme testkrav.</span><span class="sxs-lookup"><span data-stu-id="b33db-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b33db-114">I stedet for at konfigurere nye testkrav til de nye råvarer føjer virksomheden varenummeret på de nye råvarer til den eksisterende kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b33db-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="b33db-115">Den samme virksomhed producerer desuden varer med de samme produktionstestkrav og leverer varer med de samme testkrav før forsendelse.</span><span class="sxs-lookup"><span data-stu-id="b33db-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b33db-116">Virksomheden definerer derfor yderligere to kvalitetsgrupper og tildeler derefter hver gruppe de relevante varenumre.</span><span class="sxs-lookup"><span data-stu-id="b33db-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="b33db-117">Oprette en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33db-117">Create a quality group</span></span>

<span data-ttu-id="b33db-118">Benyt denne fremgangsmåde for at oprette en kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b33db-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b33db-119">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b33db-120">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b33db-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b33db-121">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="b33db-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b33db-122">**Kvalitetsgruppe** – Angiv et entydigt id eller navn til kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="b33db-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="b33db-123">**Beskrivelse** – Indtast en detaljeret beskrivelse af kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="b33db-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="b33db-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b33db-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="b33db-125">Tilføje varer manuelt til en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33db-125">Manually add items to a quality group</span></span>

<span data-ttu-id="b33db-126">Hvis du vil føje varer manuelt til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b33db-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b33db-127">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b33db-128">Vælg den kvalitetsgruppe, du vil føje varer til.</span><span class="sxs-lookup"><span data-stu-id="b33db-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="b33db-129">Vælg **Varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b33db-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="b33db-130">På siden **Varer i kvalitetsgruppe** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b33db-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b33db-131">Derefter skal du for den nye række indstille feltet **Varenummer** til det varenummer, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="b33db-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="b33db-132">Gentag forrige trin for hver ekstra vare, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="b33db-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="b33db-133">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="b33db-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="b33db-134">Tilføje flere varer til en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33db-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="b33db-135">Hvis du vil føje flere varer til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b33db-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b33db-136">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Kvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="b33db-137">Opret eller vælg den kvalitetsgruppe, du vil føje varer til.</span><span class="sxs-lookup"><span data-stu-id="b33db-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="b33db-138">Vælg **Tilføj varer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b33db-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="b33db-139">Angiv filtreringskriterierne for de varer, du vil tilføje, i dialogboksen **Forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="b33db-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="b33db-140">Du kan f.eks. filtrere efter alle varer i en bestemt varegruppe.</span><span class="sxs-lookup"><span data-stu-id="b33db-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="b33db-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33db-141">Select **OK**.</span></span>
1. <span data-ttu-id="b33db-142">I dialogboksen **Tilføj varer** vises alle de varer, der svarer til din forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="b33db-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="b33db-143">Gennemgå resultaterne.</span><span class="sxs-lookup"><span data-stu-id="b33db-143">Review the results.</span></span>

    <span data-ttu-id="b33db-144">Hvis der kræves ændringer, skal du vælge **Vælg** at vende tilbage til dialogboksen **Forespørgsel** og justere forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b33db-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="b33db-145">Når resultaterne omfatter alle de varer, du vil tilføje, skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33db-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="b33db-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b33db-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="b33db-147">Knytte en vare manuelt til en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="b33db-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="b33db-148">Hvis du vil knytte en vare manuelt til en kvalitetsgruppe, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b33db-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="b33db-149">Gå til **Lagerstyring \> Opsætning \> Kvalitetskontrol \> Varekvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="b33db-150">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b33db-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b33db-151">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="b33db-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b33db-152">**Varenummer** – Vælg det varenummer, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="b33db-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="b33db-153">**Kvalitetsgruppe** – Vælg den kvalitetsgruppe, som varen skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="b33db-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="b33db-154">Gentag det forrige trin for hver ekstra kombination af en vare og en kvalitetsgruppe, som du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="b33db-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="b33db-155">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="b33db-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="b33db-156">Tilføje en kvalitetsgruppe manuelt fra siden Frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="b33db-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="b33db-157">Hvis du vil tilføje en kvalitetsgruppe manuelt fra siden **Frigivne produkter**, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b33db-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="b33db-158">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b33db-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b33db-159">Vælg det produkt, som du vil tildele en kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b33db-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="b33db-160">I handlingsruden under fanen **Styr lager** skal du i gruppen **Kvalitet** vælge **Varekvalitetsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b33db-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="b33db-161">På siden **Varer i kvalitetsgruppe** i handlingsruden skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b33db-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b33db-162">Derefter skal du for den nye række indstille feltet **Kvalitetsgruppe** til den kvalitetsgruppe, du vil tildele produktet.</span><span class="sxs-lookup"><span data-stu-id="b33db-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="b33db-163">Gentag det forrige trin for hver ekstra kvalitetsgruppe, du vil tildele produktet.</span><span class="sxs-lookup"><span data-stu-id="b33db-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="b33db-164">Luk siderne.</span><span class="sxs-lookup"><span data-stu-id="b33db-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b33db-165">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b33db-165">Additional resources</span></span>

- [<span data-ttu-id="b33db-166">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="b33db-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="b33db-167">Test for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="b33db-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="b33db-168">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="b33db-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="b33db-169">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="b33db-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="b33db-170">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="b33db-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
