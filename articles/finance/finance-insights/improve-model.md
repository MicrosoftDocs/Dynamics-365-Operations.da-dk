---
title: Gøre forudsigelsesmodellen bedre (prøveversion)
description: I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller.
author: ShivamPandey-msft
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 197aba724ea68ef79c2d16028c23533d952329a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810001"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="6b5b2-103">Gøre forudsigelsesmodellen bedre (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6b5b2-104">I dette emne beskrives funktioner, som du kan bruge til at forbedre ydeevnen i forudsigelsesmodeller.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="6b5b2-105">Du begynder at forbedre din model i arbejdsområdet **Forudsigelser om debitorbetalinger** i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="6b5b2-106">Forbedringstrinene afsluttes derefter i AI Builder.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="6b5b2-107">Vælge historiske resultater</span><span class="sxs-lookup"><span data-stu-id="6b5b2-107">Select historical outcomes</span></span>

<span data-ttu-id="6b5b2-108">Du skal først vælge en eller flere af de tre mulige udfald for fakturaer: **Til tiden**, **Sent** og **Meget sent**.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="6b5b2-109">Du skal vælge alle tre resultater.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-109">All three outcomes should be selected.</span></span> <span data-ttu-id="6b5b2-110">Hvis du fjerner markeringen af udfaldet, filtreres fakturaer ud af uddannelsesprocessen, og nøjagtigheden af prognosen reduceres.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="6b5b2-111">[![Bekræfte udfald](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="6b5b2-112">Hvis din organisation kun kræver to udfald, skal du ændre tærsklen **Sent** og **Meget sent** til 0 (nul) dage.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="6b5b2-113">På denne måde kan du effektivt skjule forudsigelsen til en binær tilstand for **Til tiden** eller **Sent**.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="6b5b2-114">Vælg felter</span><span class="sxs-lookup"><span data-stu-id="6b5b2-114">Select fields</span></span>

<span data-ttu-id="6b5b2-115">Når du vælger felter, der skal medtages i modellen, skal du være opmærksom på, at listen indeholder alle tilgængelige felter i den Microsoft Dataverse-tabel, der er knyttet til data i Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="6b5b2-116">Nogle af disse felter skal **ikke** markeres.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="6b5b2-117">De felter, der ikke skal vælges, falder i en af tre kategorier:</span><span class="sxs-lookup"><span data-stu-id="6b5b2-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="6b5b2-118">Feltet er obligatorisk for Dataverse-tabellen, men der er ingen sikkerhedskopi af data i Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="6b5b2-119">Feltet er et id og giver derfor ikke mening for en maskinel indlæringsfunktion.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="6b5b2-120">Feltet viser oplysninger, der ikke vil være tilgængelige i forbindelse med forudsigelse.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="6b5b2-121">Følgende afsnit viser de felter, der er tilgængelige for faktura- og kundeenhederne, og viser de felter, der **ikke** skal vælges til uddannelse.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="6b5b2-122">Den kategori, der er angivet for hvert af disse felter, refererer til kategorierne på den foregående liste.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="6b5b2-123">Dataverse-fakturatabel</span><span class="sxs-lookup"><span data-stu-id="6b5b2-123">Invoice Dataverse table</span></span>

<span data-ttu-id="6b5b2-124">Følgende illustration viser de felter, der er tilgængelige til fakturatabellen.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="6b5b2-125">[![Tilgængelige felter til fakturatabellen](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="6b5b2-126">Følgende felter skal ikke vælges til oplæring:</span><span class="sxs-lookup"><span data-stu-id="6b5b2-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="6b5b2-127">**Fakturakonto** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="6b5b2-128">**Er lukket** (kategori 3) – Dette felt bruges til at filtrere fakturaer for uddannelse (lukket) og forudsigelse (ikke lukket).</span><span class="sxs-lookup"><span data-stu-id="6b5b2-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="6b5b2-129">**Navn** (kategori 1)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-129">**Name** (category 1)</span></span>
- <span data-ttu-id="6b5b2-130">**Kilde-id** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="6b5b2-131">**Kilde-post** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="6b5b2-132">**Kildetabel** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="6b5b2-133">Dataverse-kundetabel</span><span class="sxs-lookup"><span data-stu-id="6b5b2-133">Customer Dataverse table</span></span>

<span data-ttu-id="6b5b2-134">Følgende illustration viser de felter, der er tilgængelige til kundetabellen.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="6b5b2-135">[![Tilgængelige felter til kundetabellen](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="6b5b2-136">Følgende felt skal ikke vælges til oplæring:</span><span class="sxs-lookup"><span data-stu-id="6b5b2-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="6b5b2-137">**Nøgle for entydig række** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="6b5b2-138">Filtre</span><span class="sxs-lookup"><span data-stu-id="6b5b2-138">Filters</span></span>

<span data-ttu-id="6b5b2-139">Filtrene understøtter i øjeblikket ikke scenariet med debitorbetalingsprognoser.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="6b5b2-140">Du kan derfor vælge **Spring dette trin over**, og fortsæt til oversigtssiden.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="6b5b2-141">[![Fokusmodel med filtre](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="6b5b2-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="6b5b2-142">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="6b5b2-142">Privacy notice</span></span>
<span data-ttu-id="6b5b2-143">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="6b5b2-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]