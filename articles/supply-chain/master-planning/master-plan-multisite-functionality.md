---
title: Oversigt over varedisponering og funktionen til flere lokationer
description: Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2adbac35d556314b3ec9916e2b7b2706ce3528c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424864"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="8f375-103">Oversigt over varedisponering og funktionen til flere lokationer</span><span class="sxs-lookup"><span data-stu-id="8f375-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f375-104">Den overordnede planlægning tager indretningen af stedet og lagerstedets og lagerets dimensioner i betragtning.</span><span class="sxs-lookup"><span data-stu-id="8f375-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="8f375-105">Dimensionen for lokation er obligatorisk, og du kan angive, at dimensionen for lagersted skal være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="8f375-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="8f375-106">Når en dimension er obligatorisk, skal der angives en dimensionsværdi på alle lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="8f375-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="8f375-107">Under overordnet planlægning er lokationen og lagerstedet for den første efterspørgsel derfor kendt.</span><span class="sxs-lookup"><span data-stu-id="8f375-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="8f375-108">Dimensionen for lokation er også ensartet, så lokationsværdien ikke ændres ved udfoldning af efterspørgsel på lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="8f375-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="8f375-109">Når lagerstedet ikke er indstillet til obligatorisk, kendes det muligvis ikke fra den første efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="8f375-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="8f375-110">Planlægningssystemet skal afgøre, hvilket lagersted der skal bruges ud fra de indstillinger, der er defineret for varen, individuelle lagersteder og detaljerne i ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8f375-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="8f375-111">Følgende emner beskriver, hvordan planlægningssystemet fungerer, når der defineres forskellige indstillinger for at afgøre, hvilket lagersted der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="8f375-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="8f375-112">Varedisponering for lokalitets- og lagerdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="8f375-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8f375-113">Varedisponering for lokalitetsdisponering, obligatorisk lagersted</span><span class="sxs-lookup"><span data-stu-id="8f375-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8f375-114">Varedisponering for lokalitets- og lagerdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8f375-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="8f375-115">Varedisponering for lokalitetsdisponering, lagersted ikke obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8f375-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="8f375-116">Bestemme styklisteversionen</span><span class="sxs-lookup"><span data-stu-id="8f375-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



