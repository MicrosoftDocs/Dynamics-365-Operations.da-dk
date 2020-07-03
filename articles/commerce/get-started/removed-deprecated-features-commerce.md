---
title: Fjernede eller udfasede funktioner i Dynamics 365 Commerce
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443912"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="fdf72-103">Fjernede eller udfasede funktioner i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fdf72-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdf72-104">Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fdf72-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="fdf72-105">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="fdf72-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="fdf72-106">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="fdf72-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="fdf72-107">Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="fdf72-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="fdf72-108">Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="fdf72-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="fdf72-109">Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="fdf72-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="fdf72-110">Fjernede eller udfasede funktioner i Commerce 10.0.11-frigivelsen</span><span class="sxs-lookup"><span data-stu-id="fdf72-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="fdf72-111">Datahandlings-hooks</span><span class="sxs-lookup"><span data-stu-id="fdf72-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="fdf72-112">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="fdf72-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="fdf72-113">Funktionen Datahandlings-hooks frarådes på grund af problemer med ydeevnen.</span><span class="sxs-lookup"><span data-stu-id="fdf72-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="fdf72-114">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="fdf72-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="fdf72-115">Du anbefales i stedet at bruge [datahandlingstilsidesættelser](../e-commerce-extensibility/data-action-overrides.md) til at redigere forretningslogik i datahandlingslaget.</span><span class="sxs-lookup"><span data-stu-id="fdf72-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="fdf72-116">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="fdf72-116">**Product areas affected**</span></span>         | <span data-ttu-id="fdf72-117">Datahandlinger for udvidelse af e-handel</span><span class="sxs-lookup"><span data-stu-id="fdf72-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="fdf72-118">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="fdf72-118">**Deployment option**</span></span>              | <span data-ttu-id="fdf72-119">Alt</span><span class="sxs-lookup"><span data-stu-id="fdf72-119">All</span></span> |
| <span data-ttu-id="fdf72-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="fdf72-120">**Status**</span></span>                         | <span data-ttu-id="fdf72-121">Forældet fra og med version 10.0.11</span><span class="sxs-lookup"><span data-stu-id="fdf72-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="fdf72-122">Fjernede eller udfasede funktioner i Commerce 10.0.10-frigivelsen</span><span class="sxs-lookup"><span data-stu-id="fdf72-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="fdf72-123">POS-operation 803 – pluk og tilgang</span><span class="sxs-lookup"><span data-stu-id="fdf72-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="fdf72-124">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="fdf72-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="fdf72-125">Pluk- og tilgangsoperationer frarådes på grund af nyt omdesign af operationerne.</span><span class="sxs-lookup"><span data-stu-id="fdf72-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="fdf72-126">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="fdf72-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="fdf72-127">Ja.</span><span class="sxs-lookup"><span data-stu-id="fdf72-127">Yes.</span></span> <span data-ttu-id="fdf72-128">Det erstattes af to nye POS-operationer: indgående operation (804) og udgående operation (805).</span><span class="sxs-lookup"><span data-stu-id="fdf72-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="fdf72-129">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="fdf72-129">**Product areas affected**</span></span>         | <span data-ttu-id="fdf72-130">POS-program</span><span class="sxs-lookup"><span data-stu-id="fdf72-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="fdf72-131">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="fdf72-131">**Deployment option**</span></span>              | <span data-ttu-id="fdf72-132">Alt</span><span class="sxs-lookup"><span data-stu-id="fdf72-132">All</span></span> |
| <span data-ttu-id="fdf72-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="fdf72-133">**Status**</span></span>                         | <span data-ttu-id="fdf72-134">Frarådes: Fra og med version 10.0.10 modtager pluk- og tilgangsoperationer ikke længere nye funktionsforbedringer.</span><span class="sxs-lookup"><span data-stu-id="fdf72-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="fdf72-135">Der udføres kun kritiske fejlrettelser for denne operation i fremtidige versioner.</span><span class="sxs-lookup"><span data-stu-id="fdf72-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="fdf72-136">Alle kunder opfordres til at skifte til de nye [Indgående operationer](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) og [Udgående operationer](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), som fortsat vil være en del af vores langsigtede produktoversigt.</span><span class="sxs-lookup"><span data-stu-id="fdf72-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="fdf72-137">Fjernede eller udfasede funktioner i Commerce 10.0.7-frigivelsen</span><span class="sxs-lookup"><span data-stu-id="fdf72-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="fdf72-138">Commerce GetProductAvailabilities- og GetAvailableInventoryNearby-API'er</span><span class="sxs-lookup"><span data-stu-id="fdf72-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="fdf72-139">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="fdf72-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="fdf72-140">Nye optimerede API'er er oprettet for at erstatte GetProductAvailabilities- og GetAvailableInventoryNearby-API'erne.</span><span class="sxs-lookup"><span data-stu-id="fdf72-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="fdf72-141">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="fdf72-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="fdf72-142">Ja: Det erstattes af GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er.</span><span class="sxs-lookup"><span data-stu-id="fdf72-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="fdf72-143">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="fdf72-143">**Product areas affected**</span></span>         | <span data-ttu-id="fdf72-144">SDK til e-handelsprogrammer</span><span class="sxs-lookup"><span data-stu-id="fdf72-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="fdf72-145">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="fdf72-145">**Deployment option**</span></span>              | <span data-ttu-id="fdf72-146">Alt</span><span class="sxs-lookup"><span data-stu-id="fdf72-146">All</span></span> |
| <span data-ttu-id="fdf72-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="fdf72-147">**Status**</span></span>                         | <span data-ttu-id="fdf72-148">Frarådes: Fra og med version 10.0.7 foretages der ikke længere tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="fdf72-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="fdf72-149">Organisationer, der bruger disse API'er i deres e-handelsinstallationer, skal konvertere til de nye GetEstimatedAvailability- og GetEstimatedProductWarehouseAvailability-API'er og aktivere [funktionen Beregning af optimeret produkttilgængelighed](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="fdf72-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="fdf72-150">Tidligere meddelelser om fjernede eller udfasede funktioner</span><span class="sxs-lookup"><span data-stu-id="fdf72-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="fdf72-151">Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fdf72-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
