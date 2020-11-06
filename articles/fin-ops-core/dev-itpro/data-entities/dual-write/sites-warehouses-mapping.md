---
title: Integrerede lokationer og lagersteder
description: I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997618"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="e6d5b-103">Integrerede lokationer og lagersteder</span><span class="sxs-lookup"><span data-stu-id="e6d5b-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e6d5b-104">I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e6d5b-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="e6d5b-105">Operationelle steder og lagersteder er almindelige begreber i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="e6d5b-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="e6d5b-106">De bruges til at modellere forsyningskæden i dit firma.</span><span class="sxs-lookup"><span data-stu-id="e6d5b-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="e6d5b-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="e6d5b-107">Templates</span></span>

<span data-ttu-id="e6d5b-108">Med integrationen med Common Data Service kan disse begreber og alle tilhørende oplysninger være tilgængelige i Common Data Service ved hjælp af enhederne for lokationer og lagersteder i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="e6d5b-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="e6d5b-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="e6d5b-109">Finance and Operations apps</span></span> | <span data-ttu-id="e6d5b-110">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="e6d5b-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="e6d5b-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e6d5b-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="e6d5b-112">Steder</span><span class="sxs-lookup"><span data-stu-id="e6d5b-112">Sites</span></span> | <span data-ttu-id="e6d5b-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="e6d5b-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="e6d5b-114">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="e6d5b-114">Warehouses</span></span> | <span data-ttu-id="e6d5b-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e6d5b-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

