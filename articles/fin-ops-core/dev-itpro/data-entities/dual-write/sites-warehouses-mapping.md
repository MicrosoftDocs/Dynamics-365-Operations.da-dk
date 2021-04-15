---
title: Integrerede lokationer og lagersteder
description: I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750660"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="6d7bc-103">Integrerede lokationer og lagersteder</span><span class="sxs-lookup"><span data-stu-id="6d7bc-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="6d7bc-104">I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6d7bc-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="6d7bc-105">Operationelle steder og lagersteder er almindelige begreber i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="6d7bc-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="6d7bc-106">De bruges til at modellere forsyningskæden i dit firma.</span><span class="sxs-lookup"><span data-stu-id="6d7bc-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="6d7bc-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="6d7bc-107">Templates</span></span>

<span data-ttu-id="6d7bc-108">Med integrationen med Dataverse kan disse begreber og alle tilhørende oplysninger være tilgængelige i Dataverse ved hjælp af tabellerne for lokationer og lagersteder i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6d7bc-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="6d7bc-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="6d7bc-109">Finance and Operations apps</span></span> | <span data-ttu-id="6d7bc-110">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="6d7bc-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="6d7bc-111">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="6d7bc-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="6d7bc-112">Steder</span><span class="sxs-lookup"><span data-stu-id="6d7bc-112">Sites</span></span> | <span data-ttu-id="6d7bc-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="6d7bc-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="6d7bc-114">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="6d7bc-114">Warehouses</span></span> | <span data-ttu-id="6d7bc-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="6d7bc-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]