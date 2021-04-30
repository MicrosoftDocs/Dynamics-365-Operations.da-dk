---
title: Ændre en behovsprognose manuelt
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889018"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="fed03-103">Ændre en behovsprognose manuelt</span><span class="sxs-lookup"><span data-stu-id="fed03-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fed03-104">Denne fremgangsmåde viser, hvordan du redigerer prognosen for en vare.</span><span class="sxs-lookup"><span data-stu-id="fed03-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="fed03-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="fed03-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fed03-106">Denne procedure er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="fed03-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="fed03-107">Redigere prognosen for en valgt vare</span><span class="sxs-lookup"><span data-stu-id="fed03-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="fed03-108">Sådan redigerer du prognosen for en valgt vare:</span><span class="sxs-lookup"><span data-stu-id="fed03-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="fed03-109">Gå til **Moduler \> Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="fed03-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="fed03-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fed03-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="fed03-111">Vælg den vare, du vil ændre varetypen prognosen for.</span><span class="sxs-lookup"><span data-stu-id="fed03-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="fed03-112">Åbn fanen **Plan** i handlingsruden, og vælg **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="fed03-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="fed03-113">Vælg en række på listen.</span><span class="sxs-lookup"><span data-stu-id="fed03-113">In the list, select a row.</span></span> <span data-ttu-id="fed03-114">Hvis der ingen prognoselinjer er, kan du oprette en ny linje ved at vælge **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fed03-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="fed03-115">Skriv et positivt tal i feltet **Salgsantal**.</span><span class="sxs-lookup"><span data-stu-id="fed03-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="fed03-116">Dette tal repræsenterer prognosemængden for varen.</span><span class="sxs-lookup"><span data-stu-id="fed03-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="fed03-117">Der vises en fejl, hvis du angiver et negativt tal.</span><span class="sxs-lookup"><span data-stu-id="fed03-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="fed03-118">Udfyld de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="fed03-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="fed03-119">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fed03-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="fed03-120">Redigere prognosen for en eller flere varer i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="fed03-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="fed03-121">sådan redigerer du prognosen for en eller flere varer i Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="fed03-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="fed03-122">Benyt en af følgende fremgangsmåder:</span><span class="sxs-lookup"><span data-stu-id="fed03-122">Do one of the following:</span></span>
    - <span data-ttu-id="fed03-123">Åbn siden **Behovsprognose** for en vilkårlig vare som beskrevet i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="fed03-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="fed03-124">Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Behovsprognoselinjer**.</span><span class="sxs-lookup"><span data-stu-id="fed03-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="fed03-125">Vælg **Åbn i Microsoft Office \> Behovsprognoseposter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="fed03-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="fed03-126">Vælg en downloadplacering, gem og åbn derefter den downloadede fil i Excel.</span><span class="sxs-lookup"><span data-stu-id="fed03-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="fed03-127">Hvis du får vist en advarsel, skal du vælge **Aktivér redigering**.</span><span class="sxs-lookup"><span data-stu-id="fed03-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="fed03-128">Log på Supply Chain Management i Excel ved hjælp af Microsoft Dynamics-opgaveruden.</span><span class="sxs-lookup"><span data-stu-id="fed03-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="fed03-129">Du skal logge på med indstillingen **Forbliv logget på**, og du skal have tillid til dataforbindelsesappen.</span><span class="sxs-lookup"><span data-stu-id="fed03-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="fed03-130">Excel-regnearket viser nu alle dit firmas aktuelle linjer i behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="fed03-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="fed03-131">Du kan tilføje, slette og redigere behovsprognoselinjer efter behov.</span><span class="sxs-lookup"><span data-stu-id="fed03-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="fed03-132">Vælg **Publicer** i Microsoft Dynamics-opgaveruden for at uploade dine ændringer tilbage til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fed03-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
