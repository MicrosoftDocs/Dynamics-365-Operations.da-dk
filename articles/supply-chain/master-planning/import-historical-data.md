---
title: "Importér historiske data til behovsprognoser"
description: "For at få nøjagtige behovsprognoser skal du have historiske behovsdata pr. vare eller varefordelingsnøgle. Dette emne forklarer, hvordan du bruger dataenheder til at importere historiske behovsdata fra alle systemer, så du har en længere historik over behovsprognosedata."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 022a110444bcb420fbbc03b1aa24724c287103a3
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="dfd7c-104">Importér historiske data til behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="dfd7c-104">Import historical data for demand forecasts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dfd7c-105">For at garantere for nøjagtigheden af behovsprognoser skal du have så mange historiske behovsdata pr. vare eller en varefordelingsnøgle, som du kan få.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="dfd7c-106">Hvis du ikke allerede har importeret historiske behovsdata, kan du bruge dataenheden **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Microsoft Dynamics 365 for Finance and Operations til at importere dem.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="dfd7c-107">I arbejdsområdet **Datastyring**, kan du se en oversigt over alle felterne i enheden.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="dfd7c-108">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="dfd7c-109">Klik på feltet **Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="dfd7c-110">Søg i enhedslisten efter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="dfd7c-111">Klik på **Målfelter**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-111">Click **Target fields**.</span></span> <span data-ttu-id="dfd7c-112">Følgende enhedsfelter er obligatoriske: websted (**DeliveringSiteId**), dato (**DemandDate**), antal (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøgle (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="dfd7c-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="dfd7c-113">For at kunne bruge dataenheden skal du have en Microsoft Excel-fil eller kommaseparerede værdier (CSV), der indeholder de historiske behovsdata.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="dfd7c-114">Følgende eksempel viser, hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="dfd7c-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="dfd7c-115">Example</span></span>

<span data-ttu-id="dfd7c-116">Du kan bruge følgende fil som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-116">You can use the following file as an example.</span></span> <span data-ttu-id="dfd7c-117">Hent [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="dfd7c-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="dfd7c-118">Denne fil indeholder de historiske behovsdata for vare D0001.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="dfd7c-119">Den indeholder kun følgende obligatoriske felter: websted, antal og behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="dfd7c-120">Vælg det firma, du vil importere de historiske behovsdata til.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="dfd7c-121">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="dfd7c-122">Klik på feltet **Importér**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="dfd7c-123">Angiv et navn til importprojektet, f.eks. **Importér historiske behov for vare D0001**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="dfd7c-124">I feltet **Kildedataformat** skal du vælge formatet på den fil, du importerer.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="dfd7c-125">Hvis du vil importere filen HistoricalDemandData i dette eksempel, skal du vælge **CSV**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="dfd7c-126">I feltet **Enhedsnavn** skal du vælge **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="dfd7c-127">Gem filen på computeren, og overfør den derefter.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="dfd7c-128">Klik på **Importér**.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-128">Click **Import**.</span></span>
9. <span data-ttu-id="dfd7c-129">Siden **Udførelsesoversigt** åbnes automatisk.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="dfd7c-130">Kontrollér de importerede data på siden.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="dfd7c-131">Når du har importeret de historiske behovsdata, kan du generere en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="dfd7c-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfd7c-132">Se også</span><span class="sxs-lookup"><span data-stu-id="dfd7c-132">See also</span></span>

[<span data-ttu-id="dfd7c-133">Generere et statistisk budgetgrundlag</span><span class="sxs-lookup"><span data-stu-id="dfd7c-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

