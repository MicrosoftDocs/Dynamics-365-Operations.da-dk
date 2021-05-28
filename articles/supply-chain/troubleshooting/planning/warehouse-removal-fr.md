---
title: Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer
description: Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026374"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="f3d85-103">Du kan ikke fjerne behovsprognosedimensionen for et lagersted fra budgetlinjer</span><span class="sxs-lookup"><span data-stu-id="f3d85-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="f3d85-104">KB-nummer: 4614408</span><span class="sxs-lookup"><span data-stu-id="f3d85-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="f3d85-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f3d85-105">Symptoms</span></span>

<span data-ttu-id="f3d85-106">Dette problem opstår, når dimensionen **Lagersted** ikke er tildelt under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser**.</span><span class="sxs-lookup"><span data-stu-id="f3d85-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="f3d85-107">Kolonnen **Lagersted** vises dog på siden **Behovsprognose** (**Varedisponering \> Budgettering \> Manuel budgetenhed \> Behovsprognoselinjer**).</span><span class="sxs-lookup"><span data-stu-id="f3d85-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="f3d85-108">Løsning</span><span class="sxs-lookup"><span data-stu-id="f3d85-108">Resolution</span></span>

<span data-ttu-id="f3d85-109">Indstillingerne under fanen **Budgetdimensioner** på siden **Parametre til behovsprognoser** har ingen indflydelse på siden **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="f3d85-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="f3d85-110">De styrer det oprindelige budget, der oprettes og vises i den regulerede behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="f3d85-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="f3d85-111">De styrer dog ikke de dimensioner, der kræves til den "reelle" behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="f3d85-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="f3d85-112">Når du autoriserer de poster, der vises på siden **Justeret behovsprognose**, kan du konvertere dem til "reelle" budgetposteringer for en prognosemodel.</span><span class="sxs-lookup"><span data-stu-id="f3d85-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="f3d85-113">Denne model kan derefter bruges til behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="f3d85-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="f3d85-114">På siden **Behovsprognose** indgår dimensionerne for det "reelle" budget, der vises på linjerne i efterspørgselsprognosen, i lagerdimensionerne.</span><span class="sxs-lookup"><span data-stu-id="f3d85-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="f3d85-115">(Denne funktionsmåde minder om funktionsmåden for salgsordrelinjer). Hvis systemet ikke er konfigureret til at bruge **Lagersted** som en obligatorisk lagerdimension, kan du tilpasse siden, så kolonnen skjules.</span><span class="sxs-lookup"><span data-stu-id="f3d85-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
