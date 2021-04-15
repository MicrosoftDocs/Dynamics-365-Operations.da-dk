---
title: Angive produktantalsgrænser for B2B-e-handelswebsteder
description: Dette emne beskriver, hvordan du angiver produktantalsgrænser for business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799775"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="685ee-103">Angive produktantalsgrænser for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="685ee-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="685ee-104">Dette emne beskriver, hvordan du angiver produktantalsgrænser for business-to-business (B2B)-e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="685ee-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="685ee-105">De fleste produkter har en måleenhed, der definerer gruppering af dem.</span><span class="sxs-lookup"><span data-stu-id="685ee-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="685ee-106">Grupperingerne har indflydelse på, hvordan produkterne kan sælges.</span><span class="sxs-lookup"><span data-stu-id="685ee-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="685ee-107">Nogle produkter kan have en yderligere gruppering for antal.</span><span class="sxs-lookup"><span data-stu-id="685ee-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="685ee-108">Denne gruppe bestemmer, om produkterne kan sælges som individuelle enheder eller multiplum, og om der er en minimums- eller maksimumordreantalsgrænse, der skal overholdes.</span><span class="sxs-lookup"><span data-stu-id="685ee-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="685ee-109">Denne funktion til begrænsning af antal sikrer, at de minimum-, maksimum-, multiplum- og standardmængder, der er konfigureret i Microsoft Dynamics 365 Commerce (i standardordreindstillingerne eller indstillingerne for commerce site builder), anvendes på kundeordrer, der placeres på et e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="685ee-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="685ee-110">Produktantalsgrænser understøttes ikke i øjeblikket for POS og call centers.</span><span class="sxs-lookup"><span data-stu-id="685ee-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="685ee-111">Mange detailhandlere giver mulighed for kundeordrer (også kendt som specialordrer) for at opfylde forskellige produkt- og opfyldelseskrav.</span><span class="sxs-lookup"><span data-stu-id="685ee-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="685ee-112">Her er nogle typiske scenarier:</span><span class="sxs-lookup"><span data-stu-id="685ee-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="685ee-113">En kunde ønsker, at produkter af bestemte varianter skal sælges i multiplum af nogle få.</span><span class="sxs-lookup"><span data-stu-id="685ee-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="685ee-114">En kunde ønsker at afhente varer fra en butik eller et sted, der er forskelligt fra butikken eller det sted, hvor kunden købte varerne.</span><span class="sxs-lookup"><span data-stu-id="685ee-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="685ee-115">Pakkestandarderne for butikkerne er dog ikke de samme som standarderne for onlinesalgsdistribution.</span><span class="sxs-lookup"><span data-stu-id="685ee-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="685ee-116">En kunde ønsker at købe et limited-edition-produkt med en maksimumantalsgrænse for varer, der kan købes.</span><span class="sxs-lookup"><span data-stu-id="685ee-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="685ee-117">Aktivere standardfunktionen for ordreindstillinger i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="685ee-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="685ee-118">Inden du kan angive grænser for produktantal, skal funktionen standardordreindstillinger være aktiveret i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="685ee-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="685ee-119">Følg disse trin for at aktivere standardfunktionen for indstilling af ordrer.</span><span class="sxs-lookup"><span data-stu-id="685ee-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="685ee-120">Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="685ee-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="685ee-121">Find og vælg funktionen **Supportindstillinger for websted- og standardordrer i kundeordre**.</span><span class="sxs-lookup"><span data-stu-id="685ee-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="685ee-122">Vælg **Aktivér nu** nederst til højre i ruden.</span><span class="sxs-lookup"><span data-stu-id="685ee-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="685ee-123">Definere mængdeindstillinger</span><span class="sxs-lookup"><span data-stu-id="685ee-123">Define quantity settings</span></span> 

<span data-ttu-id="685ee-124">Du kan definere mængdeindstillinger på siden **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="685ee-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="685ee-125">Følg disse trin for at definere mængdeindstillinger.</span><span class="sxs-lookup"><span data-stu-id="685ee-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="685ee-126">Gå til Produkt **Retail og Commerce \> Produkter og kategorier \> Frigivne produkter efter kategori**.</span><span class="sxs-lookup"><span data-stu-id="685ee-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="685ee-127">Vælge et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="685ee-127">Select a released product.</span></span>
1. <span data-ttu-id="685ee-128">På fanen **Administrer lager** i handlingsruden i gruppen **Ordreindstillinger** skal du vælge **Standardordreindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="685ee-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="685ee-129">Angiv produktsalgsantallet i sektionen **Salgsmængde** på siden **Standardordreindstillinger** i oversigtspanelet **Salgsordre**:</span><span class="sxs-lookup"><span data-stu-id="685ee-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="685ee-130">**Flere** – Det antal, som produktet kan købes i multiplum af.</span><span class="sxs-lookup"><span data-stu-id="685ee-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="685ee-131">**Minimumordreantal** – Det mindste antal produkter, der skal købes.</span><span class="sxs-lookup"><span data-stu-id="685ee-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="685ee-132">**Maksimumordreantal** – Det maksimale antal produkter, der kan købes.</span><span class="sxs-lookup"><span data-stu-id="685ee-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="685ee-133">**Standardordreantal** – Det standardantal, der automatisk angives, når produktet vælges.</span><span class="sxs-lookup"><span data-stu-id="685ee-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="685ee-134">Aktivator funktionen for B2B-ordreantalsgrænser i Commerce site builder</span><span class="sxs-lookup"><span data-stu-id="685ee-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="685ee-135">Følg disse trin for at aktivere funktionen for B2B-ordreantalsgrænser i Commerce site builder.</span><span class="sxs-lookup"><span data-stu-id="685ee-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="685ee-136">Gå til **Webstedsindstillinger \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="685ee-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="685ee-137">Vælg **Aktiveret for B2B-kunder** i rullemenuen under **Aktivér antalsgrænser for ordre**.</span><span class="sxs-lookup"><span data-stu-id="685ee-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="685ee-138">Opdaterede indstillinger for webstedet træder først i kraft, når app.settings.json-filen er opdateret.</span><span class="sxs-lookup"><span data-stu-id="685ee-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="685ee-139">Yderligere oplysninger finder du i [SDK- og modulbiblioteksopdateringer](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="685ee-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="685ee-140">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="685ee-140">Additional resources</span></span>

[<span data-ttu-id="685ee-141">Konfigurere et B2B-e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="685ee-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="685ee-142">Oprette organisationsmodelhierarkier for B2B-organisationer</span><span class="sxs-lookup"><span data-stu-id="685ee-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="685ee-143">Administrere forretningspartnerbrugere på B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="685ee-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="685ee-144">Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="685ee-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]