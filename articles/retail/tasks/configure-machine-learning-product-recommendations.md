--- 
title: "Konfigurere produktanbefalinger, der er baseret på maskinel indlæring"
description: "Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="e39b4-103">Konfigurere produktanbefalinger, der er baseret på maskinel indlæring</span><span class="sxs-lookup"><span data-stu-id="e39b4-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e39b4-104">Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="e39b4-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="e39b4-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="e39b4-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e39b4-106">Gå til Systemadministration > Opsætning > Enhedslager.</span><span class="sxs-lookup"><span data-stu-id="e39b4-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="e39b4-107">Find og vælg den posten 'RetailSales' på listen.</span><span class="sxs-lookup"><span data-stu-id="e39b4-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="e39b4-108">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="e39b4-108">Click Refresh.</span></span>
4. <span data-ttu-id="e39b4-109">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e39b4-109">Click OK.</span></span>
5. <span data-ttu-id="e39b4-110">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e39b4-110">Close the page.</span></span>
6. <span data-ttu-id="e39b4-111">Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.</span><span class="sxs-lookup"><span data-stu-id="e39b4-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="e39b4-112">Klik på fanen Maskinel indlæring.</span><span class="sxs-lookup"><span data-stu-id="e39b4-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="e39b4-113">Vælg 'Ja' i feltet Aktivér produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="e39b4-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="e39b4-114">Hvis du modtager meddelelsen "Anbefalingsmodellerne blev ikke hentet", skyldes det, at du har opdateret enhedslageret for nylig, og systemet er måske ikke færdig med at samle de nye data.</span><span class="sxs-lookup"><span data-stu-id="e39b4-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="e39b4-115">Vent 2-3 timer, og prøv igen.</span><span class="sxs-lookup"><span data-stu-id="e39b4-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="e39b4-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e39b4-116">Click Save.</span></span>
10. <span data-ttu-id="e39b4-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e39b4-117">Close the page.</span></span>


