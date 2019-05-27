---
title: Detailhierarkier
description: I denne artikel beskrives detailhierarkier i Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
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
ms.openlocfilehash: 198c8da336f3e225c5d6da2eb02c86581dc9b4d6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568016"
---
# <a name="retail-hierarchies"></a><span data-ttu-id="367dc-103">Detailhierarkier</span><span class="sxs-lookup"><span data-stu-id="367dc-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="367dc-104">I denne artikel beskrives detailhierarkier i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="367dc-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="367dc-105">Du kan oprette et detailkategorihierarki for at organisere de produkter, du sælger gennem dine detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="367dc-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="367dc-106">Du kan bruge detailprodukthierarkier til at kategorisere eller gruppere produkter.</span><span class="sxs-lookup"><span data-stu-id="367dc-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="367dc-107">Du kan derefter bruge disse produkter til at oprettet produktudvalg og fordelskundeprogrammer.</span><span class="sxs-lookup"><span data-stu-id="367dc-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="367dc-108">Du kan også tildele produktattributter og egenskaber, tildele en prisstruktur, inkludere produkterne i produktkampagner og bruge produkterne til rapportering.</span><span class="sxs-lookup"><span data-stu-id="367dc-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="367dc-109">Du kan oprette ét detailkategorihierarki til at repræsentere alle produkterne og kategorierne i organisationen og derefter bruge kategorihierarkiet til flere formål.</span><span class="sxs-lookup"><span data-stu-id="367dc-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="367dc-110">Du kan også oprette flere detailkategorihierarkier til særlige formål, f.eks. produktkampagner.</span><span class="sxs-lookup"><span data-stu-id="367dc-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="367dc-111">Når du opretter et detailprodukthierarki, skal du tildele en kategorihierarkitype for at identificere formålet med kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="367dc-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="367dc-112">Det er f.eks. kun produkthierarkier, som er tildelt typen **Detailnavigationshierarki**, der refereres til, når du gennemser produkter efter kategori, online eller ved POS.</span><span class="sxs-lookup"><span data-stu-id="367dc-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="367dc-113">Detailhierarkityper</span><span class="sxs-lookup"><span data-stu-id="367dc-113">Retail hierarchy types</span></span>

<span data-ttu-id="367dc-114">Følgende tabel viser de typer detailkategorihierarkier, der er tilgængelige, og det generelle formål med hver type.</span><span class="sxs-lookup"><span data-stu-id="367dc-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="367dc-115">Kategori for hierarkitype</span><span class="sxs-lookup"><span data-stu-id="367dc-115">Category hierarchy type</span></span>       | <span data-ttu-id="367dc-116">Formål</span><span class="sxs-lookup"><span data-stu-id="367dc-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="367dc-117">Detailprodukthierarki</span><span class="sxs-lookup"><span data-stu-id="367dc-117">Retail product hierarchy</span></span>      | <span data-ttu-id="367dc-118">Brug denne type hierarki for at definere det generelle produkthierarki for organisationen.</span><span class="sxs-lookup"><span data-stu-id="367dc-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="367dc-119">Du kan bruge denne type hierarki til merchandising, priser og kampagner, rapportering og planlægning af udvalg.</span><span class="sxs-lookup"><span data-stu-id="367dc-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="367dc-120">Kun ét detailprodukthierarki kan få tildelt denne hierarkitype.</span><span class="sxs-lookup"><span data-stu-id="367dc-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="367dc-121">Supplerende detailhierarki</span><span class="sxs-lookup"><span data-stu-id="367dc-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="367dc-122">Brug denne hierarkitype til eventuelle yderligere detailkategorihierarkier, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="367dc-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="367dc-123">I foråret er der for eksempel et salgsfremstød for badetøj.</span><span class="sxs-lookup"><span data-stu-id="367dc-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="367dc-124">Derfor skal du medtage dine badetøjsprodukter i et separat kategorihierarki og anvende salgsfremmende priser til de forskellige produktkategorier.</span><span class="sxs-lookup"><span data-stu-id="367dc-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="367dc-125">Detailnavigationshierarki</span><span class="sxs-lookup"><span data-stu-id="367dc-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="367dc-126">Brug denne hierarkitype til at gruppere og organisere produkter i kategorier, så produkterne kan gennemses online eller i POS.</span><span class="sxs-lookup"><span data-stu-id="367dc-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="367dc-127">Når du bruger et detailkategorihierarki til at strukturere dine produkter, kan du definere og vedligeholde produktattributter og egenskaber på kategoriniveau.</span><span class="sxs-lookup"><span data-stu-id="367dc-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="367dc-128">Disse attributter og egenskaber omfatter indstillinger for produktdimensioner og POS.</span><span class="sxs-lookup"><span data-stu-id="367dc-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="367dc-129">Evt. produkter, som du automatisk tildeler kategorierne, arver automatisk de attributter og egenskaber, du definerer.</span><span class="sxs-lookup"><span data-stu-id="367dc-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="367dc-130">Du kan også kopiere flere egenskabsindstillinger for et vilkårligt produkt til flere produkter i en valgt kategori på samme tid.</span><span class="sxs-lookup"><span data-stu-id="367dc-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
