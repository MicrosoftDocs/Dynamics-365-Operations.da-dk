---
title: 'Vejledning: Ændre en behovsprognose manuelt'
description: Dette emne viser, hvordan du redigerer prognosen for en vare
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224004"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="12b6f-103">Vejledning: Ændre en behovsprognose manuelt</span><span class="sxs-lookup"><span data-stu-id="12b6f-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12b6f-104">Denne fremgangsmåde viser, hvordan du redigerer prognosen for en vare.</span><span class="sxs-lookup"><span data-stu-id="12b6f-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="12b6f-105">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="12b6f-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="12b6f-106">Redigere prognosen for en valgt vare</span><span class="sxs-lookup"><span data-stu-id="12b6f-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="12b6f-107">Sådan redigerer du prognosen for en valgt vare:</span><span class="sxs-lookup"><span data-stu-id="12b6f-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="12b6f-108">Gå til **Moduler \> Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="12b6f-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="12b6f-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="12b6f-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="12b6f-110">Vælg den vare, du vil ændre varetypen prognosen for.</span><span class="sxs-lookup"><span data-stu-id="12b6f-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="12b6f-111">Åbn fanen **Plan** i handlingsruden, og vælg **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="12b6f-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="12b6f-112">Vælg en række på listen.</span><span class="sxs-lookup"><span data-stu-id="12b6f-112">In the list, select a row.</span></span> <span data-ttu-id="12b6f-113">Hvis der ingen prognoselinjer er, kan du oprette en ny linje ved at vælge **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12b6f-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="12b6f-114">Skriv et positivt tal i feltet **Salgsantal**.</span><span class="sxs-lookup"><span data-stu-id="12b6f-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="12b6f-115">Dette tal repræsenterer prognosemængden for varen.</span><span class="sxs-lookup"><span data-stu-id="12b6f-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="12b6f-116">Der vises en fejl, hvis du angiver et negativt tal.</span><span class="sxs-lookup"><span data-stu-id="12b6f-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="12b6f-117">Udfyld de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="12b6f-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="12b6f-118">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12b6f-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="12b6f-119">Redigere prognosen for en eller flere varer med Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="12b6f-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="12b6f-120">Sådan redigerer du prognosen for en eller flere varer med Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="12b6f-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="12b6f-121">Benyt en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="12b6f-121">Do one of the following:</span></span>
    - <span data-ttu-id="12b6f-122">Åbn siden **Behovsprognose** for en vilkårlig vare som beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="12b6f-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="12b6f-123">Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Behovsprognoselinjer**.</span><span class="sxs-lookup"><span data-stu-id="12b6f-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="12b6f-124">Vælg **Åbn i Microsoft Office \> Behovsprognoseposter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12b6f-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="12b6f-125">Vælg en downloadplacering, gem og åbn derefter den downloadede fil i Excel.</span><span class="sxs-lookup"><span data-stu-id="12b6f-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="12b6f-126">Hvis du får vist en advarsel, skal du vælge **Aktivér redigering**.</span><span class="sxs-lookup"><span data-stu-id="12b6f-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="12b6f-127">Log på Supply Chain Management i Excel ved hjælp af Microsoft Dynamics-opgaveruden.</span><span class="sxs-lookup"><span data-stu-id="12b6f-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="12b6f-128">Du skal logge på med indstillingen **Forbliv logget på**, og du skal have tillid til dataforbindelsesappen.</span><span class="sxs-lookup"><span data-stu-id="12b6f-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="12b6f-129">Excel-regnearket viser nu alle dit firmas aktuelle linjer i behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="12b6f-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="12b6f-130">Du kan tilføje, slette og redigere behovsprognoselinjer efter behov.</span><span class="sxs-lookup"><span data-stu-id="12b6f-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="12b6f-131">Vælg **Publicer** i Microsoft Dynamics-opgaveruden for at uploade dine ændringer tilbage til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="12b6f-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
