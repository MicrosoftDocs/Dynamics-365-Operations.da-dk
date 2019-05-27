---
title: Disponeringsindstillinger
description: Dette emne indeholder oplysninger om de indstillinger for disponering, som behovsplanlægningen bruger til at beregne varebehov.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538888"
---
# <a name="coverage-settings"></a><span data-ttu-id="26889-103">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="26889-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26889-104">Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="26889-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="26889-105">Du kan angive disponeringsindstillinger på flere måder:</span><span class="sxs-lookup"><span data-stu-id="26889-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="26889-106">Angiv disponeringsindstillinger for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="26889-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="26889-107">Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="26889-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="26889-108">Du kan oprette en disponeringsgruppe ved at gå til **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="26889-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="26889-109">Du kan sammenkæde en disponeringsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="26889-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="26889-110">Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="26889-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="26889-111">Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge feltet **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="26889-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="26889-112">Hvis du som standard ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning den standarddisponeringsgruppe, der er angivet på siden **Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="26889-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="26889-113">Angiv disponeringsindstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="26889-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="26889-114">Du kan oprette disponeringsindstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="26889-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="26889-115">Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="26889-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="26889-116">Vælg produktet, og vælg derefter **Varedisponering** i gruppen **Disponering** under fanen **Plan** i handlingsruden for at åbne siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="26889-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="26889-117">Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**.</span><span class="sxs-lookup"><span data-stu-id="26889-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="26889-118">Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="26889-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="26889-119">Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="26889-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="26889-120">Guiden hjælper dig trin for trin gennem opsætningen af de primære varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="26889-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="26889-121">På siden **Varedisponering** skal du i handlingsruden klikke på **Guide** for at åbne **Varedisponeringsguide**.</span><span class="sxs-lookup"><span data-stu-id="26889-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="26889-122">Angiv disponeringsindstillinger for en dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="26889-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="26889-123">Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="26889-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="26889-124">Vælg linket feltet **Lagringsdimensionsgruppe** i sektionen **Administration** i oversigtspanelet **Generelt** på siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="26889-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="26889-125">På siden **Lagringsdimensionsgrupper** skal du markere afkrydsningsfeltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="26889-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="26889-126">Feltet **Disponer pr. dimension** skal være markeret for alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi.</span><span class="sxs-lookup"><span data-stu-id="26889-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26889-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="26889-127">Additional resources</span></span>

[<span data-ttu-id="26889-128">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="26889-128">Master plans</span></span>](master-plans.md)
