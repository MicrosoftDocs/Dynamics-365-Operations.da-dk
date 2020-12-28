---
title: Commerce-hierarkier
description: I denne artikel beskrives hierarkier i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411173"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="1037b-103">Commerce-hierarkier</span><span class="sxs-lookup"><span data-stu-id="1037b-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1037b-104">I denne artikel beskrives hierarkier i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1037b-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1037b-105">Du kan oprette et kategorihierarki for at organisere de produkter, du sælger gennem dine kanaler.</span><span class="sxs-lookup"><span data-stu-id="1037b-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="1037b-106">Du kan bruge produkthierarkier til at kategorisere eller gruppere produkter.</span><span class="sxs-lookup"><span data-stu-id="1037b-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="1037b-107">Du kan derefter bruge disse produkter til at oprettet produktudvalg og fordelskundeprogrammer.</span><span class="sxs-lookup"><span data-stu-id="1037b-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="1037b-108">Du kan også tildele produktattributter og egenskaber, tildele en prisstruktur, inkludere produkterne i produktkampagner og bruge produkterne til rapportering.</span><span class="sxs-lookup"><span data-stu-id="1037b-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="1037b-109">Du kan oprette ét kategorihierarki til at repræsentere alle produkter og kategorier i organisationen og derefter bruge kategorihierarkiet til flere formål.</span><span class="sxs-lookup"><span data-stu-id="1037b-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="1037b-110">Du kan også oprette flere kategorihierarkier til særlige formål, som produktkampagner.</span><span class="sxs-lookup"><span data-stu-id="1037b-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="1037b-111">Når du opretter et produkthierarki, skal du tildele en kategorihierarkitype for at identificere formålet med kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="1037b-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="1037b-112">Det er f.eks. kun produkthierarkier, som er tildelt typen **Commerce-navigationshierarki**, der refereres til, når du gennemser produkter efter kategori, online eller ved POS.</span><span class="sxs-lookup"><span data-stu-id="1037b-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="1037b-113">Hierarkityper</span><span class="sxs-lookup"><span data-stu-id="1037b-113">Hierarchy types</span></span>

<span data-ttu-id="1037b-114">Følgende tabel viser de typer kategorihierarkier, der er tilgængelige, og det generelle formål med hver type.</span><span class="sxs-lookup"><span data-stu-id="1037b-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="1037b-115">Kategori for hierarkitype</span><span class="sxs-lookup"><span data-stu-id="1037b-115">Category hierarchy type</span></span>       | <span data-ttu-id="1037b-116">Formål</span><span class="sxs-lookup"><span data-stu-id="1037b-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="1037b-117">Produkthierarki</span><span class="sxs-lookup"><span data-stu-id="1037b-117">Product hierarchy</span></span>      | <span data-ttu-id="1037b-118">Brug denne type hierarki for at definere det generelle produkthierarki for organisationen.</span><span class="sxs-lookup"><span data-stu-id="1037b-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="1037b-119">Du kan bruge denne type hierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg.</span><span class="sxs-lookup"><span data-stu-id="1037b-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="1037b-120">Kun ét produkthierarki kan få tildelt denne hierarkitype.</span><span class="sxs-lookup"><span data-stu-id="1037b-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="1037b-121">Supplerende hierarki</span><span class="sxs-lookup"><span data-stu-id="1037b-121">Supplemental hierarchy</span></span> | <span data-ttu-id="1037b-122">Brug denne hierarkitype til eventuelle yderligere kategorihierarkier, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="1037b-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="1037b-123">I foråret er der for eksempel et salgsfremstød for badetøj.</span><span class="sxs-lookup"><span data-stu-id="1037b-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="1037b-124">Derfor skal du medtage dine badetøjsprodukter i et separat kategorihierarki og anvende salgsfremmende priser til de forskellige produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="1037b-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="1037b-125">Navigationshierarki</span><span class="sxs-lookup"><span data-stu-id="1037b-125">Navigation hierarchy</span></span>   | <span data-ttu-id="1037b-126">Brug denne hierarkitype til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller i POS.</span><span class="sxs-lookup"><span data-stu-id="1037b-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="1037b-127">Når du bruger et kategorihierarki til at strukturere dine produkter, kan du definere og vedligeholde produktattributter og egenskaber på kategoriniveau.</span><span class="sxs-lookup"><span data-stu-id="1037b-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="1037b-128">Disse attributter og egenskaber omfatter indstillinger for produktdimensioner og POS.</span><span class="sxs-lookup"><span data-stu-id="1037b-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="1037b-129">Evt. produkter, som du automatisk tildeler kategorierne, arver automatisk de attributter og egenskaber, du definerer.</span><span class="sxs-lookup"><span data-stu-id="1037b-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="1037b-130">Du kan også kopiere flere egenskabsindstillinger for et vilkårligt produkt til flere produkter i en valgt kategori på samme tid.</span><span class="sxs-lookup"><span data-stu-id="1037b-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
