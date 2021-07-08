---
title: Importér historiske data til behovsprognoser
description: For at få nøjagtige behovsprognoser skal du have historiske behovsdata pr. vare eller varefordelingsnøgle. Dette emne forklarer, hvordan du bruger dataenheder til at importere historiske behovsdata fra alle systemer, så du har en længere historik over behovsprognosedata.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301644"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="67e7a-104">Importér historiske data til behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="67e7a-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67e7a-105">For at garantere for nøjagtigheden af behovsprognoser skal du have så mange historiske behovsdata pr. vare eller en varefordelingsnøgle, som du kan få.</span><span class="sxs-lookup"><span data-stu-id="67e7a-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="67e7a-106">Hvis du ikke allerede har importeret historiske behovsdata, kan du bruge dataenheden **Historisk eksternt behov** (ReqDemPlanHistoricalExternalDemandEntity) i Dynamics 365 Supply Chain Management til at importere dem.</span><span class="sxs-lookup"><span data-stu-id="67e7a-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="67e7a-107">I arbejdsområdet **Datastyring**, kan du se en oversigt over alle felterne i enheden.</span><span class="sxs-lookup"><span data-stu-id="67e7a-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="67e7a-108">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="67e7a-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="67e7a-109">Vælg feltet **Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="67e7a-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="67e7a-110">Søg i enhedslisten efter **Historisk eksternt behov**.</span><span class="sxs-lookup"><span data-stu-id="67e7a-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="67e7a-111">Vælg **Målfelter**.</span><span class="sxs-lookup"><span data-stu-id="67e7a-111">Select **Target fields**.</span></span> <span data-ttu-id="67e7a-112">Følgende enhedsfelter er obligatoriske: websted (**DeliveringSiteId**), dato (**DemandDate**), antal (**DemandQuantity**), og enten varenummer (**ItemNumber**) eller varefordelingsnøgle (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="67e7a-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="67e7a-113">For at kunne bruge dataenheden skal du have en Microsoft Excel-fil eller kommaseparerede værdier (CSV), der indeholder de historiske behovsdata.</span><span class="sxs-lookup"><span data-stu-id="67e7a-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="67e7a-114">Følgende eksempel viser, hvordan du importerer data fra en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="67e7a-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="67e7a-115">Yderligere oplysninger om, hvordan du importerer data, herunder hvordan du rydder data efter en import, finder du i [Oversigt over dataimport- og -eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og relaterede emner.</span><span class="sxs-lookup"><span data-stu-id="67e7a-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="67e7a-116">Se også [Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="67e7a-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]