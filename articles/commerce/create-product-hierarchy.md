---
title: Oprette et nyt produkthierarki
description: Dette emne beskriver, hvordan du opretter et nyt produkthierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001892"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="22fc1-103">Oprette et nyt produkthierarki</span><span class="sxs-lookup"><span data-stu-id="22fc1-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="22fc1-104">Dette emne beskriver, hvordan du opretter et nyt produkthierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22fc1-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="22fc1-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="22fc1-105">Overview</span></span>

<span data-ttu-id="22fc1-106">Dynamics 365 Commerce understøtter flere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="22fc1-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="22fc1-107">Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="22fc1-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="22fc1-108">Hver detailbutikskanal kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="22fc1-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="22fc1-109">Du skal oprette alle disse elementer, for at du kan oprette en detailbutikskanal.</span><span class="sxs-lookup"><span data-stu-id="22fc1-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="22fc1-110">Et Commerce-produkthierarki bruges for at definere det generelle produkthierarki for organisationen.</span><span class="sxs-lookup"><span data-stu-id="22fc1-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="22fc1-111">Du kan bruge et Commerce-produkthierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg.</span><span class="sxs-lookup"><span data-stu-id="22fc1-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="22fc1-112">Der kan kun tildeles ét Commerce-produkthierarki pr. organisation.</span><span class="sxs-lookup"><span data-stu-id="22fc1-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="22fc1-113">Oprette og konfigurere et produkthierarki</span><span class="sxs-lookup"><span data-stu-id="22fc1-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="22fc1-114">Følg disse trin for at oprette og konfigurere et Commerce-produkthierarki.</span><span class="sxs-lookup"><span data-stu-id="22fc1-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="22fc1-115">Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Commerce-produkthierarki** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="22fc1-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="22fc1-116">Hvis der endnu ikke findes et hierarki, skal du vælge **Ny** i **handlingsruden** for at oprette roden for hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="22fc1-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="22fc1-117">Under **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="22fc1-117">Under **General**:</span></span>
    1. <span data-ttu-id="22fc1-118">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="22fc1-119">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="22fc1-120">Indtast et brugervenligt navn i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="22fc1-121">Angiv **Aktiv** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="22fc1-122">Tilføje hierarkinoder</span><span class="sxs-lookup"><span data-stu-id="22fc1-122">Add hierarchy nodes</span></span>

<span data-ttu-id="22fc1-123">Følg disse trin for at tilføje hierarkinoder.</span><span class="sxs-lookup"><span data-stu-id="22fc1-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="22fc1-124">Vælg **Rediger kategorihierarki** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="22fc1-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="22fc1-125">Vælg den overordnede node, du vil føje en ny node til, og vælg derefter **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="22fc1-126">I afsnittet **Generelt** skal du angive **Navn**, **Beskrivelse**, **Brugervenligt navn** og **Nøgleord**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="22fc1-127">Under **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="22fc1-127">Under **General**:</span></span>
    1. <span data-ttu-id="22fc1-128">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="22fc1-129">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="22fc1-130">Indtast et brugervenligt navn i feltet **Brugervenligt navn**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="22fc1-131">Angiv relevante nøgleord i feltet **Nøgleord**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="22fc1-132">Angiv et nummer til visningsrækkefølgen, i feltet **Visningsrækkefølge** (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="22fc1-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="22fc1-133">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="22fc1-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="22fc1-134">Gentag trinnene ovenfor for at tilføje yderligere noder.</span><span class="sxs-lookup"><span data-stu-id="22fc1-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="22fc1-135">Følgende billede viser oprettelsen af en ny produkthierarkinode.</span><span class="sxs-lookup"><span data-stu-id="22fc1-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Oprette produkthierarki](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="22fc1-137">Andre indstillinger</span><span class="sxs-lookup"><span data-stu-id="22fc1-137">Other settings</span></span>

<span data-ttu-id="22fc1-138">Kategoriattributgrupper kan også tildeles til hver gruppe efter behov.</span><span class="sxs-lookup"><span data-stu-id="22fc1-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="22fc1-139">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="22fc1-139">Additional resources</span></span>

[<span data-ttu-id="22fc1-140">Detailhierarkier</span><span class="sxs-lookup"><span data-stu-id="22fc1-140">Retail hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="22fc1-141">Administrere produktkategorier og -produkter </span><span class="sxs-lookup"><span data-stu-id="22fc1-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="22fc1-142">Ændre sorteringsrækkefølgen for merchandisingenheder</span><span class="sxs-lookup"><span data-stu-id="22fc1-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
