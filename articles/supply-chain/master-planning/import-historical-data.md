---
title: Importér historiske data til behovsprognoser
description: For at få nøjagtige behovsprognoser skal du have historiske behovsdata pr. vare eller varefordelingsnøgle. Dette emne forklarer, hvordan du bruger dataenheder til at importere historiske behovsdata fra alle systemer, så du har en længere historik over behovsprognosedata.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d415895bd05b9ab1a2311ab69cc3757047df91db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204610"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="0417b-104">Importér historiske data til behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="0417b-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0417b-105">For at garantere for nøjagtigheden af behovsprognoser skal du have så mange historiske behovsdata pr. vare eller en varefordelingsnøgle, som du kan få.</span><span class="sxs-lookup"><span data-stu-id="0417b-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="0417b-106">Hvis du ikke allerede har importeret historiske behovsdata, kan du bruge dataenheden **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til at importere dem.</span><span class="sxs-lookup"><span data-stu-id="0417b-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="0417b-107">I arbejdsområdet **Datastyring**, kan du se en oversigt over alle felterne i enheden.</span><span class="sxs-lookup"><span data-stu-id="0417b-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="0417b-108">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="0417b-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="0417b-109">Vælg feltet **Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="0417b-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="0417b-110">Søg i enhedslisten efter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="0417b-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="0417b-111">Vælg **Målfelter**.</span><span class="sxs-lookup"><span data-stu-id="0417b-111">Select **Target fields**.</span></span> <span data-ttu-id="0417b-112">Følgende enhedsfelter er obligatoriske: websted (**DeliveringSiteId**), dato (**DemandDate**), antal (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøgle (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="0417b-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="0417b-113">For at kunne bruge dataenheden skal du have en Microsoft Excel-fil eller kommaseparerede værdier (CSV), der indeholder de historiske behovsdata.</span><span class="sxs-lookup"><span data-stu-id="0417b-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="0417b-114">Følgende eksempel viser, hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="0417b-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="0417b-115">Yderligere oplysninger om, hvordan du importerer data, herunder hvordan du rydder data efter en import, finder du i [Oversigt over dataimport- og -eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og relaterede emner.</span><span class="sxs-lookup"><span data-stu-id="0417b-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="0417b-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0417b-116">Example</span></span>

<span data-ttu-id="0417b-117">Du kan bruge følgende fil som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="0417b-117">You can use the following file as an example.</span></span> <span data-ttu-id="0417b-118">Hent [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="0417b-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="0417b-119">Denne fil indeholder de historiske behovsdata for vare D0001.</span><span class="sxs-lookup"><span data-stu-id="0417b-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="0417b-120">Den indeholder kun følgende obligatoriske felter: websted, antal og behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="0417b-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="0417b-121">Vælg det firma, du vil importere de historiske behovsdata til.</span><span class="sxs-lookup"><span data-stu-id="0417b-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="0417b-122">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="0417b-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="0417b-123">Vælg feltet **Import**.</span><span class="sxs-lookup"><span data-stu-id="0417b-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="0417b-124">Angiv et navn til importprojektet, f.eks. **Importér historiske behov for vare D0001**.</span><span class="sxs-lookup"><span data-stu-id="0417b-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="0417b-125">I feltet **Kildedataformat** skal du vælge formatet på den fil, du importerer.</span><span class="sxs-lookup"><span data-stu-id="0417b-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="0417b-126">Hvis du vil importere filen HistoricalDemandData i dette eksempel, skal du vælge **CSV**.</span><span class="sxs-lookup"><span data-stu-id="0417b-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="0417b-127">I feltet **Enhedsnavn** skal du vælge **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="0417b-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="0417b-128">Gem filen på computeren, og overfør den derefter.</span><span class="sxs-lookup"><span data-stu-id="0417b-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="0417b-129">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="0417b-129">Select **Import**.</span></span>
9. <span data-ttu-id="0417b-130">Siden **Udførelsesoversigt** åbnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="0417b-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="0417b-131">Kontrollér de importerede data på siden.</span><span class="sxs-lookup"><span data-stu-id="0417b-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="0417b-132">Når du har importeret de historiske behovsdata, kan du generere en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="0417b-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0417b-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0417b-133">Additional resources</span></span>

[<span data-ttu-id="0417b-134">Generere et statistisk budgetgrundlag</span><span class="sxs-lookup"><span data-stu-id="0417b-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="0417b-135">Oversigt over dataimport- og -eksportjob</span><span class="sxs-lookup"><span data-stu-id="0417b-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]