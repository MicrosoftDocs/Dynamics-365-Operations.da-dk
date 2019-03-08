---
title: Konfigurere produktanbefalinger, der er baseret på maskinel indlæring
description: Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "348520"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="7c61c-103">Konfigurere produktanbefalinger, der er baseret på maskinel indlæring</span><span class="sxs-lookup"><span data-stu-id="7c61c-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7c61c-104">Denne procedure opdaterer de data i enheden, der bruges af systemet til maskinel ind læring, som er baseret på produktanbefalingerne, og derefter aktiveres produktanbefalinger på POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="7c61c-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="7c61c-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="7c61c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7c61c-106">Gå til Systemadministration > Opsætning > Enhedslager.</span><span class="sxs-lookup"><span data-stu-id="7c61c-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="7c61c-107">Find og vælg den posten 'RetailSales' på listen.</span><span class="sxs-lookup"><span data-stu-id="7c61c-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="7c61c-108">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="7c61c-108">Click Refresh.</span></span>
4. <span data-ttu-id="7c61c-109">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7c61c-109">Click OK.</span></span>
5. <span data-ttu-id="7c61c-110">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7c61c-110">Close the page.</span></span>
6. <span data-ttu-id="7c61c-111">Gå til Detail og handel > Konfiguration af hovedkontor > Parametre > Detailparametre.</span><span class="sxs-lookup"><span data-stu-id="7c61c-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="7c61c-112">Klik på fanen Maskinel indlæring.</span><span class="sxs-lookup"><span data-stu-id="7c61c-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="7c61c-113">Vælg 'Ja' i feltet Aktivér produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="7c61c-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="7c61c-114">Hvis du modtager meddelelsen "Anbefalingsmodellerne blev ikke hentet", skyldes det, at du har opdateret enhedslageret for nylig, og systemet er måske ikke færdig med at samle de nye data.</span><span class="sxs-lookup"><span data-stu-id="7c61c-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="7c61c-115">Vent 2-3 timer, og prøv igen.</span><span class="sxs-lookup"><span data-stu-id="7c61c-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="7c61c-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7c61c-116">Click Save.</span></span>
10. <span data-ttu-id="7c61c-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7c61c-117">Close the page.</span></span>

