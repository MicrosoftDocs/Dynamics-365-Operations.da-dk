---
title: Disponeringsindstillinger
description: "Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a><span data-ttu-id="bb8fc-103">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="bb8fc-103">Coverage settings</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bb8fc-104">Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="bb8fc-105">Du kan angive disponeringsindstillinger på flere måder:</span><span class="sxs-lookup"><span data-stu-id="bb8fc-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="bb8fc-106">Angiv disponeringsindstillinger for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="bb8fc-107">Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="bb8fc-108">Klik på **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper** for at oprette en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="bb8fc-109">Du kan sammenkæde en disponeringsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="bb8fc-110">Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="bb8fc-111">Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="bb8fc-112">Hvis du ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning som standard den **standarddisponeringsgruppe**, der er angivet på siden **Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="bb8fc-113">Angiv disponeringsindstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="bb8fc-114">Du kan oprette disponeringsindstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="bb8fc-115">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="bb8fc-116">Vælg produktet, og klik på **Varedisponering** i gruppen **Disponering** under fanen **Plan** i **handlingsruden** for at åbne siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="bb8fc-117">Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="bb8fc-118">Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="bb8fc-119">Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="bb8fc-120">Guiden giver dig en trinvis vejledning i at konfigurere de primære dispositionsparametre for varer.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="bb8fc-121">På siden **Varedisponering** skal du klikke på **Guide** at åbne **Varedisponeringsguide**.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="bb8fc-122">Angiv disponeringsindstillinger for en dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="bb8fc-123">Klik på <strong>Administration af produktoplysninger &gt; Almindelige &gt; Frigivne produkter</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-123">Click <strong>Product information management &gt; Common &gt; Released products</strong>.</span></span> <span data-ttu-id="bb8fc-124">På siden <strong>Frigivet produkt** på fanen **Generelt</strong> i gruppen <strong>Administration</strong> skal du klikke på linket <strong>Lagerdimensionsgruppe</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-124">On the <strong>Released product detail **page, on the **General</strong> tab, in the <strong>Administration</strong> group, click the <strong>Storage dimension group</strong> link.</span></span> <span data-ttu-id="bb8fc-125">Vælg <strong>Lagringsdimensionsgruppe</strong> i feltet <strong>Disponer pr. dimension</strong> for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-125">On the <strong>Storage dimension group</strong> page, select the <strong>Coverage plan by dimension</strong> field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="bb8fc-126">Alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi, skal have feltet <strong>Disponer pr. dimension</strong> markeret.</span><span class="sxs-lookup"><span data-stu-id="bb8fc-126">All product dimensions, such as configuration, color, size, style, must have the <strong>Coverage plan by dimension</strong> field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="bb8fc-127">Se også</span><span class="sxs-lookup"><span data-stu-id="bb8fc-127">See also</span></span>
--------

[<span data-ttu-id="bb8fc-128">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="bb8fc-128">Master plans</span></span>](master-plans.md)




