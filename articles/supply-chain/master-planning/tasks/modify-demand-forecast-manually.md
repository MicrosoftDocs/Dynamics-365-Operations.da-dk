---
title: Ændre en behovsprognose manuelt
description: Denne fremgangsmåde viser, hvordan du redigerer prognosen for en vare.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58846f896d60610d0e90f8d04fda3101def53511
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148095"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="7c8c6-103">Ændre en behovsprognose manuelt</span><span class="sxs-lookup"><span data-stu-id="7c8c6-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c8c6-104">Denne fremgangsmåde viser, hvordan du redigerer prognosen for en vare.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="7c8c6-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7c8c6-106">Denne registrering er beregnet til produktionsplanlæggeren.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="7c8c6-107">Rediger prognosen for en vare</span><span class="sxs-lookup"><span data-stu-id="7c8c6-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="7c8c6-108">I **navigationsruden** skal du gå til **Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="7c8c6-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="7c8c6-110">Vælg den vare, du vil ændre varetypen prognosen for.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="7c8c6-111">Du kan f.eks. vælge elementet D0001.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="7c8c6-112">Klik på **Plan** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="7c8c6-113">Klik på **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="7c8c6-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-114">In the list, mark the selected row.</span></span> <span data-ttu-id="7c8c6-115">Hvis der ingen prognoselinjer er, kan du oprette en ny linje ved at klikke på Ny på programlinjen.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="7c8c6-116">Skriv et tal i feltet **Salgsantal**.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="7c8c6-117">Dette tal repræsenterer prognosemængden for varen.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="7c8c6-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="7c8c6-119">Ændr prognosen i Excel</span><span class="sxs-lookup"><span data-stu-id="7c8c6-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="7c8c6-120">Klik på **Åbn** i Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="7c8c6-121">Klik på **Rediger behovsprognose** i Excel.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="7c8c6-122">I Excel kan du tilføje, slette og redigere behovsprognoselinjer.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="7c8c6-123">Hvis du ikke kan se data i Excel, skal du logge på med indstillingen "Forbliv logget på" aktiveret, og du skal have tillid til dataforbindelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="7c8c6-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

