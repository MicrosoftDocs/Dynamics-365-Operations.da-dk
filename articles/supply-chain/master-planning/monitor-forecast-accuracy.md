---
title: Overvåge prognosenøjagtighed
description: I dette emne beskrives de typer af prognosenøjagtighed, som Dynamics 365 Supply Chain Management beregner, og det forklares, hvordan du kan få vist nøjagtighedsværdierne.
author: roxanadiaconu
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db8b9fdaf05f58d1386513348c11fcc54887d9c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826461"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="b2f10-103">Overvåge prognosenøjagtighed</span><span class="sxs-lookup"><span data-stu-id="b2f10-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2f10-104">I dette emne beskrives de typer af prognosenøjagtighed, som Microsoft Dynamics 365 Supply Chain Management beregner, og det forklares, hvordan du kan få vist nøjagtighedsværdierne.</span><span class="sxs-lookup"><span data-stu-id="b2f10-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="b2f10-105">Supply Chain Management beregner følgende typer prognosenøjagtighed:</span><span class="sxs-lookup"><span data-stu-id="b2f10-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="b2f10-106">Historiske prognosenøjagtighed ved at sammenligne den historiske prognose, som Varedisponering bruger, med den historiske efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="b2f10-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="b2f10-107">For at få vist værdierne (både de absolutte værdier og procentvise værdier) for historisk prognosenøjagtighed skal du klikke på **Vis nøjagtighed** på siden **Detaljer om behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="b2f10-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="b2f10-108">Den anslåede nøjagtighed af den prognosemodel, der bruges til at generere forudsigelserne.</span><span class="sxs-lookup"><span data-stu-id="b2f10-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="b2f10-109">Du kan få vist en procentangivelse for nøjagtighed under **Modeldetaljer – MAPE** på siden **Detaljer om behovsanalyse**.</span><span class="sxs-lookup"><span data-stu-id="b2f10-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="b2f10-110">Hvis du bruger Microsoft Azure Machine Learning Behovsprognosen, baseres beregningen af nøjagtigheden af den interne model på testdatasæt.</span><span class="sxs-lookup"><span data-stu-id="b2f10-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="b2f10-111">Hvis du vil angive størrelsen på testdatasættet, skal du indstille parameteren **TEST\_SET\_SIZE\_PERCENT** på siden **Parametre til behovsprognoser**.</span><span class="sxs-lookup"><span data-stu-id="b2f10-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="b2f10-112">Hvis du f.eks. indstiller værdien til **20**, bruges de sidste 20 procent af de historiske data til at beregne nøjagtigheden af den interne model.</span><span class="sxs-lookup"><span data-stu-id="b2f10-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="b2f10-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b2f10-113">Additional resources</span></span>
--------

[<span data-ttu-id="b2f10-114">Autorisere en justeret prognose</span><span class="sxs-lookup"><span data-stu-id="b2f10-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b2f10-115">Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose</span><span class="sxs-lookup"><span data-stu-id="b2f10-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]