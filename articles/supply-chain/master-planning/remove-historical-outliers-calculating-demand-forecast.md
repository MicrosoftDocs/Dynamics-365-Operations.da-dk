---
title: Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose
description: Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose. Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44be713a1049e90618392d028c81e974841b348
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886817"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="00680-104">Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose</span><span class="sxs-lookup"><span data-stu-id="00680-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00680-105">Denne artikel beskriver, hvordan du udelader afvigelser fra de historiske data, der bruges til at beregne en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="00680-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="00680-106">Ved at udelukke afvigelser kan du forbedre prognosens nøjagtighed.</span><span class="sxs-lookup"><span data-stu-id="00680-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="00680-107">Du kan udelukke afvigelser for at forbedre prognosens nøjagtighed.</span><span class="sxs-lookup"><span data-stu-id="00680-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="00680-108">Denne opgave er valgfri.</span><span class="sxs-lookup"><span data-stu-id="00680-108">This is an optional task.</span></span> <span data-ttu-id="00680-109">Her er en oversigt over processen:</span><span class="sxs-lookup"><span data-stu-id="00680-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="00680-110">Klik på **Overordnet planlægning** &gt; **Opsætning** &gt; **Behovsprognose** &gt; **Fjernelse af afvigelse** for at åbne siden **Fjernelse af afvigelse**, hvor du kan bruge en forespørgsel til at vælge posteringerne, der skal udelades.</span><span class="sxs-lookup"><span data-stu-id="00680-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="00680-111">Vælg det regnskab, som forespørgslen gælder for, og angiv derefter et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="00680-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="00680-112">Feltet **Forespørgselsdato** angives automatisk til den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="00680-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="00680-113">Markér afkrydsningsfeltet **Aktiv** for at udelukke de transaktioner, som forespørgslen finder fra de historiske data.</span><span class="sxs-lookup"><span data-stu-id="00680-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="00680-114">Denne indstilling træder i kraft, når du opretter en oprindelig prognose.</span><span class="sxs-lookup"><span data-stu-id="00680-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="00680-115">På siden **Forespørgsel om fjernelse af afvigelse** kan du tilføje, fjerne og vælge de kriterier, der definerer, hvilke transaktioner der udelades, når den oprindelige prognose beregnes.</span><span class="sxs-lookup"><span data-stu-id="00680-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="00680-116">Du kan f.eks. vælge en bestemt vare eller ordretransaktion, der skal udelukkes.</span><span class="sxs-lookup"><span data-stu-id="00680-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="00680-117">Klik på **Vis posteringer**.</span><span class="sxs-lookup"><span data-stu-id="00680-117">Click **Display transactions**.</span></span> <span data-ttu-id="00680-118">Siden **Afvigelsestransaktioner** viser de transaktioner, der opfylder de kriterier, du har defineret i forespørgslen, og som skal udelukkes fra de historiske data, når behovsprognosen beregnes.</span><span class="sxs-lookup"><span data-stu-id="00680-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="00680-119">**Bemærk!** Du kan også oprette en forespørgsel, der er baseret på en eksisterende forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="00680-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="00680-120">Vælg den forespørgsel, der skal kopieres, og klik derefter på **Dupliker**.</span><span class="sxs-lookup"><span data-stu-id="00680-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="00680-121">Feltet **Forespørgselsdato** identificerer versionen.</span><span class="sxs-lookup"><span data-stu-id="00680-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="00680-122">Du kan bruge forespørgslen, som den er, eller du kan klikke på **Rediger forespørgsel** for at ændre kriterierne.</span><span class="sxs-lookup"><span data-stu-id="00680-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="00680-123">Du kan eventuelt ændre navnet og beskrivelsen for den nye forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="00680-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="00680-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="00680-124">Additional resources</span></span>
--------

[<span data-ttu-id="00680-125">Oversigt over behovsprognoser</span><span class="sxs-lookup"><span data-stu-id="00680-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="00680-126">Overvåge prognosenøjagtighed</span><span class="sxs-lookup"><span data-stu-id="00680-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



