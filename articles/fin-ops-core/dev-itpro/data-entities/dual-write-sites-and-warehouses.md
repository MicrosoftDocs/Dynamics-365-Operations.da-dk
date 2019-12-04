---
title: Integrerede lokationer og lagersteder
description: I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations og Common Data Service.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770976"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="0420e-103">Integrerede lokationer og lagersteder</span><span class="sxs-lookup"><span data-stu-id="0420e-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0420e-104">I dette emne beskrives integrationen af lokations- og lagerstedsdata mellem Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0420e-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="0420e-105">Operationelle steder og lagersteder er almindelige begreber i et Supply Chain Management-program.</span><span class="sxs-lookup"><span data-stu-id="0420e-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="0420e-106">De bruges til at modellere forsyningskæden i dit firma.</span><span class="sxs-lookup"><span data-stu-id="0420e-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="0420e-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="0420e-107">Templates</span></span>

<span data-ttu-id="0420e-108">Med integrationen med Common Data Service kan disse begreber og alle tilhørende oplysninger være tilgængelige i Common Data Service ved hjælp af enhederne for lokationer og lagersteder i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="0420e-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="0420e-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="0420e-109">Finance and Operations apps</span></span> | <span data-ttu-id="0420e-110">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="0420e-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0420e-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0420e-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="0420e-112">Steder</span><span class="sxs-lookup"><span data-stu-id="0420e-112">Sites</span></span> | <span data-ttu-id="0420e-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="0420e-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="0420e-114">Lagersteder</span><span class="sxs-lookup"><span data-stu-id="0420e-114">Warehouses</span></span> | <span data-ttu-id="0420e-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="0420e-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

