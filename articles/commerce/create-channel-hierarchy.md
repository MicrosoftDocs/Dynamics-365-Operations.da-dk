---
title: Opret et navigationshierarki for kanal
description: Dette emne beskriver, hvordan du opretter et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e1462c10dfe1c858429e9f4cc5d720ca43df609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221323"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="a4192-103">Oprette et navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="a4192-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a4192-104">Dette emne beskriver, hvordan du opretter et navigationshierarki for en kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a4192-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a4192-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a4192-105">Overview</span></span>

<span data-ttu-id="a4192-106">Et navigationshierarki for en kanal bruges til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller ved POS.</span><span class="sxs-lookup"><span data-stu-id="a4192-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="a4192-107">Opret et navigationshierarki for kanal</span><span class="sxs-lookup"><span data-stu-id="a4192-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="a4192-108">Benyt følgende fremgangsmåde for at oprette et navigationshierarki for en kanal.</span><span class="sxs-lookup"><span data-stu-id="a4192-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="a4192-109">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Navigationskategorier for kanal** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="a4192-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="a4192-110">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a4192-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a4192-111">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4192-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="a4192-112">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4192-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="a4192-113">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a4192-113">Select **Create**.</span></span>
1. <span data-ttu-id="a4192-114">Vælg **Ny kategorinode** i handlingsruden for at oprette en rodnode.</span><span class="sxs-lookup"><span data-stu-id="a4192-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="a4192-115">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4192-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="a4192-116">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4192-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="a4192-117">Indtast et brugervenligt navn i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a4192-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="a4192-118">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a4192-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a4192-119">Følgende billede viser et eksempel på en rodnode.</span><span class="sxs-lookup"><span data-stu-id="a4192-119">The following image shows a example root node.</span></span>

![Eksempel på rodnode](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="a4192-121">Oprette navigationskategorinoder</span><span class="sxs-lookup"><span data-stu-id="a4192-121">Create navigation category nodes</span></span>

<span data-ttu-id="a4192-122">Følge disse trin for at oprette yderligere navigationskategorinoder, der repræsenterer produktkategorierne i kanalen.</span><span class="sxs-lookup"><span data-stu-id="a4192-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="a4192-123">Vælg den overordnede node, du vil føje en kategori til, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="a4192-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="a4192-124">Vælg **Ny kategorinode** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4192-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="a4192-125">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a4192-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="a4192-126">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a4192-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="a4192-127">Indtast et brugervenligt navn i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="a4192-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="a4192-128">Angiv en visningsrækkefølge i feltet **Visningsrækkefølge** (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="a4192-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="a4192-129">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a4192-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a4192-130">Følgende billede viser et eksempel på et fuldført navigationshierarki for kanal.</span><span class="sxs-lookup"><span data-stu-id="a4192-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Eksempel på kanalhierarki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="a4192-132">Føje produkter til kategorinoder</span><span class="sxs-lookup"><span data-stu-id="a4192-132">Add products to category nodes</span></span>

<span data-ttu-id="a4192-133">Følg disse trin for at føje produkter til kategorinoder.</span><span class="sxs-lookup"><span data-stu-id="a4192-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="a4192-134">Vælg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="a4192-134">Select a category node.</span></span>
1. <span data-ttu-id="a4192-135">Vælg **Tilføj** under **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="a4192-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="a4192-136">Find de nye produkter, du vil tilføje, ved hjælp af produktnummer eller produktnavn, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4192-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="a4192-137">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a4192-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="a4192-138">Hvis du føjer produkter til en node i navigationshierarkiet for en kanal, er det ikke tilstrækkeligt, at produkterne vises i en valgt kanal – produkterne skal også være udvalgt til et produkt.</span><span class="sxs-lookup"><span data-stu-id="a4192-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="a4192-139">Følgende billede viser en eksempelnode med tilføjede produkter.</span><span class="sxs-lookup"><span data-stu-id="a4192-139">The following image shows an example node with products added.</span></span>

![Produkter føjet til en kategorinode](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="a4192-141">Føje produktattributgrupper til kategorinoder</span><span class="sxs-lookup"><span data-stu-id="a4192-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="a4192-142">Der skal oprettes attributgrupper, før du kan føje dem til en node i navigationshierarkiet for en kanal.</span><span class="sxs-lookup"><span data-stu-id="a4192-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="a4192-143">Følg disse trin for at føje en produktattributgruppe til en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="a4192-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="a4192-144">Vælg en kategorinode.</span><span class="sxs-lookup"><span data-stu-id="a4192-144">Select a category node.</span></span>
1. <span data-ttu-id="a4192-145">Vælg **Tilføj** under **Produktattributgruppe**.</span><span class="sxs-lookup"><span data-stu-id="a4192-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="a4192-146">Find de attributgrupper, du vil tilføje, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4192-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="a4192-147">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a4192-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a4192-148">Følgende billede viser en eksempelnode med tilføjede produktattributgrupper.</span><span class="sxs-lookup"><span data-stu-id="a4192-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktattributgrupper på en node](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="a4192-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a4192-150">Additional resources</span></span>

[<span data-ttu-id="a4192-151">Konfigurere udvalg</span><span class="sxs-lookup"><span data-stu-id="a4192-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="a4192-152">Administrere attributter for attributgrupper</span><span class="sxs-lookup"><span data-stu-id="a4192-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]