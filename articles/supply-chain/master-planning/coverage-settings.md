---
title: Disponeringsindstillinger
description: Dette emne indeholder oplysninger om de indstillinger for disponering, som behovsplanlægningen bruger til at beregne varebehov.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999975"
---
# <a name="coverage-settings"></a><span data-ttu-id="cee88-103">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="cee88-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cee88-104">Ved behovsplanlægning anvendes disponeringsindstillinger til at beregne varebehov.</span><span class="sxs-lookup"><span data-stu-id="cee88-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="cee88-105">Du kan angive disponeringsindstillinger på flere måder:</span><span class="sxs-lookup"><span data-stu-id="cee88-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="cee88-106">Angiv disponeringsindstillinger for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cee88-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="cee88-107">Du kan oprette en disponeringsgruppe, der indeholder alle produkter, der er knyttet til disponeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="cee88-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="cee88-108">Du kan oprette en disponeringsgruppe ved at gå til **Varedisponering &gt; Konfiguration &gt; Disponering &gt; Disponeringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="cee88-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="cee88-109">Du kan sammenkæde en disponeringsgruppe til et produkt.</span><span class="sxs-lookup"><span data-stu-id="cee88-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="cee88-110">Hvis sammenkædningen er specifik for et websted, et lagersted eller en produktdimension, skal du bruge feltet **Disponeringsgruppe** på siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="cee88-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="cee88-111">Hvis sammenkædningen er generisk, uanset produktdimensionerne, skal du bruge feltet **Disponeringsgruppe** på oversigtspanelet **Plan** på siden **Produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="cee88-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="cee88-112">Hvis du som standard ikke knytter en disponeringsgruppe til et produkt, bruger den overordnede planlægning den standarddisponeringsgruppe, der er angivet på siden **Varedisponeringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="cee88-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="cee88-113">Angiv disponeringsindstillinger for et produkt.</span><span class="sxs-lookup"><span data-stu-id="cee88-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="cee88-114">Du kan oprette disponeringsindstillinger for et bestemt produkt.</span><span class="sxs-lookup"><span data-stu-id="cee88-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="cee88-115">Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="cee88-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="cee88-116">Vælg produktet, og vælg derefter **Varedisponering** i gruppen **Disponering** under fanen **Plan** i handlingsruden for at åbne siden **Varedisponering**.</span><span class="sxs-lookup"><span data-stu-id="cee88-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="cee88-117">Hvis produktet allerede er knyttet til en dispositionsgruppe, kan du tilsidesætte indstillingerne for dispositionsgruppen ved hjælp af feltet **Tilsidesæt**.</span><span class="sxs-lookup"><span data-stu-id="cee88-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="cee88-118">Disponeringsindstillinger på siden **Varedisponering** har fortrinsret over indstillingerne på siden **Dækningsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="cee88-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="cee88-119">Angiv disponeringsindstillinger for et produkt ved hjælp af en guide.</span><span class="sxs-lookup"><span data-stu-id="cee88-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="cee88-120">Guiden hjælper dig trin for trin gennem opsætningen af de primære varedisponeringsparametre.</span><span class="sxs-lookup"><span data-stu-id="cee88-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="cee88-121">På siden **Varedisponering** skal du i handlingsruden klikke på **Guide** for at åbne **Varedisponeringsguide**.</span><span class="sxs-lookup"><span data-stu-id="cee88-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="cee88-122">Angiv disponeringsindstillinger for en dimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cee88-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="cee88-123">Gå til **Administration af produktoplysninger &gt; Produkter &gt; Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="cee88-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="cee88-124">Vælg linket feltet **Lagringsdimensionsgruppe** i sektionen **Administration** i oversigtspanelet **Generelt** på siden **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="cee88-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="cee88-125">På siden **Lagringsdimensionsgrupper** skal du markere afkrydsningsfeltet **Disponer pr. dimension** for at oprette dispositionsindstillinger for en dimension i lagringsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="cee88-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="cee88-126">Feltet **Disponer pr. dimension** skal være markeret for alle produktdimensioner, f.eks. konfiguration, farve, størrelse, typografi.</span><span class="sxs-lookup"><span data-stu-id="cee88-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="cee88-127">Disponeringskoder</span><span class="sxs-lookup"><span data-stu-id="cee88-127">Coverage codes</span></span>

<span data-ttu-id="cee88-128">Varedisponering kan konfigureres til at bruge forskellige genopfyldningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="cee88-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="cee88-129">Genopfyldningsmetoderne eller metoderne til angivelse partistørrelse er de teknikker, der bruges af systemet til at bestemme batchstørrelsen for købte eller fremstillede varer.</span><span class="sxs-lookup"><span data-stu-id="cee88-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="cee88-130">Hver genbestillingsmetode tildeles en af følgende disponeringskoder:</span><span class="sxs-lookup"><span data-stu-id="cee88-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="cee88-131">**Manuel** – Metoden til angivelse af partistørrelse, hvor systemet ikke foreslår købte, overflytninger eller produktionsordrer for varen.</span><span class="sxs-lookup"><span data-stu-id="cee88-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="cee88-132">Planlæggeren for varen vil være ansvarlig for oprettelsen af de nødvendige ordrer til genopfyldning af varen.</span><span class="sxs-lookup"><span data-stu-id="cee88-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="cee88-133">**Pr. behov** – Metoden til angivelse af partistørrelse, hvor systemet opretter en planlagt indkøbs-, overførsels- eller produktionsordre pr. behov for varen.</span><span class="sxs-lookup"><span data-stu-id="cee88-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="cee88-134">Dette bruges generelt til dyre varer med forbigående behov.</span><span class="sxs-lookup"><span data-stu-id="cee88-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="cee88-135">**Pr. periode** - Metoden til angivelse af partistørrelse, som kombinerer alle behov for en periode til én ordre for varen.</span><span class="sxs-lookup"><span data-stu-id="cee88-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="cee88-136">Ordren planlægges for den første dag i perioden, og dens antal vil opfylde nettobehovet i den oprettede periode.</span><span class="sxs-lookup"><span data-stu-id="cee88-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="cee88-137">Perioden starter med det første behov for varen og dækker den definerede varighed i tiden.</span><span class="sxs-lookup"><span data-stu-id="cee88-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="cee88-138">Den næste periode vil starte med de næste behov for varen.</span><span class="sxs-lookup"><span data-stu-id="cee88-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="cee88-139">**Min./Maks.** - Metoden til angivelse af partistørrelse, som indeholder genopfyldningen af lageret op til et bestemt niveau, når den forventede beholdning er lavere end en tærskel.</span><span class="sxs-lookup"><span data-stu-id="cee88-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="cee88-140">Genopfyldningsantallet vil være forskellen mellem maksimumniveauet og det forventede disponible lagerniveau.</span><span class="sxs-lookup"><span data-stu-id="cee88-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="cee88-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cee88-141">Additional resources</span></span>

[<span data-ttu-id="cee88-142">Oversigt over behovsplaner</span><span class="sxs-lookup"><span data-stu-id="cee88-142">Master plans overview</span></span>](master-plans.md)
