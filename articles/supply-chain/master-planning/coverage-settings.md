---
title: Disponeringsindstillinger
description: Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.
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
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "322553"
---
# <a name="coverage-settings"></a><span data-ttu-id="9c528-103">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="9c528-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c528-104">Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="9c528-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="9c528-105">Du kan angive disponeringsindstillinger på flere måder:</span><span class="sxs-lookup"><span data-stu-id="9c528-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="9c528-106">Angiv disponeringsindstillinger for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c528-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="9c528-107">Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="9c528-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="9c528-108">Klik på **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper** for at oprette en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c528-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="9c528-109">Du kan sammenkæde en disponeringsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="9c528-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="9c528-110">Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="9c528-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="9c528-111">Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9c528-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="9c528-112">Hvis du ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning som standard den **standarddisponeringsgruppe**, der er angivet på siden **Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="9c528-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="9c528-113">Angiv disponeringsindstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="9c528-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="9c528-114">Du kan oprette disponeringsindstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="9c528-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="9c528-115">Klik på **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="9c528-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="9c528-116">Vælg produktet, og klik på **Varedisponering** i gruppen **Disponering** under fanen **Plan** i **handlingsruden** for at åbne siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="9c528-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="9c528-117">Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**.</span><span class="sxs-lookup"><span data-stu-id="9c528-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="9c528-118">Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9c528-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="9c528-119">Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="9c528-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="9c528-120">Guiden giver dig en trinvis vejledning i at konfigurere de primære dispositionsparametre for varer.</span><span class="sxs-lookup"><span data-stu-id="9c528-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="9c528-121">På siden **Varedisponering** skal du klikke på **Guide** at åbne **Varedisponeringsguide**.</span><span class="sxs-lookup"><span data-stu-id="9c528-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="9c528-122">Angiv disponeringsindstillinger for en dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9c528-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="9c528-123">Klik på **Administration af produktoplysninger &gt; Almindelige &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="9c528-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="9c528-124">Klik på linket **Lagringsdimensionsgruppe** i gruppen **Administration** under fanen **Generelt** på siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="9c528-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="9c528-125">Vælg **Lagringsdimensionsgruppe** i feltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="9c528-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="9c528-126">Alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi, skal have feltet **Disponer pr. dimension** markeret.</span><span class="sxs-lookup"><span data-stu-id="9c528-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="9c528-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9c528-127">Additional resources</span></span>
--------

[<span data-ttu-id="9c528-128">Behovsplaner</span><span class="sxs-lookup"><span data-stu-id="9c528-128">Master plans</span></span>](master-plans.md)



