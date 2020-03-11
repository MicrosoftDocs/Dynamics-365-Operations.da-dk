---
title: Fjernede eller udfasede platformfunktioner
description: Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087877"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="0042b-103">Fjernede eller udfasede platformfunktioner</span><span class="sxs-lookup"><span data-stu-id="0042b-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0042b-104">Dette emne beskriver funktioner, der er blevet fjernet eller er planlagt til at blive fjernet i platformopdateringer af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="0042b-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="0042b-105">En *fjernet* funktion er ikke længere tilgængelige i produktet.</span><span class="sxs-lookup"><span data-stu-id="0042b-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="0042b-106">En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="0042b-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="0042b-107">Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning.</span><span class="sxs-lookup"><span data-stu-id="0042b-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="0042b-108">Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="0042b-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="0042b-109">Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="0042b-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="0042b-110">Platform update 32</span><span class="sxs-lookup"><span data-stu-id="0042b-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="0042b-111">Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg</span><span class="sxs-lookup"><span data-stu-id="0042b-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="0042b-112">**Årsagen til forældelsen/fjernelsen**</span><span class="sxs-lookup"><span data-stu-id="0042b-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="0042b-113">Dette var et sikkerhedsproblem, fordi anmodningen om ændring kunne sendes til en ikke-tiltænkt bruger.</span><span class="sxs-lookup"><span data-stu-id="0042b-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="0042b-114">Dette var også et anvendelighedsproblem, fordi den tvang brugeren til at afgøre, hvem der var arbejdsgangsigangsætteren og vælge dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="0042b-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="0042b-115">**Erstattet af en anden funktion?**</span><span class="sxs-lookup"><span data-stu-id="0042b-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="0042b-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="0042b-116">No</span></span> |
| <span data-ttu-id="0042b-117">**Produktområder, der er berørt**</span><span class="sxs-lookup"><span data-stu-id="0042b-117">**Product areas affected**</span></span>         | <span data-ttu-id="0042b-118">Arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="0042b-118">Workflow</span></span> |
| <span data-ttu-id="0042b-119">**Installationsindstilling**</span><span class="sxs-lookup"><span data-stu-id="0042b-119">**Deployment option**</span></span>              | <span data-ttu-id="0042b-120">Alt</span><span class="sxs-lookup"><span data-stu-id="0042b-120">All</span></span> |
| <span data-ttu-id="0042b-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="0042b-121">**Status**</span></span>                         | <span data-ttu-id="0042b-122">Rullelisten Brugervalg blev fjernet fra dialogboksen Ændring af anmodning i platformsopdatering 32.</span><span class="sxs-lookup"><span data-stu-id="0042b-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="0042b-123">Anmodninger om ændring af anmodninger sendes efter hensigten automatisk til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="0042b-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="0042b-124">Du kan finde flere oplysninger om denne funktion under [Handlinger i godkendelsesprocesser i arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="0042b-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="0042b-125">Tidligere meddelelser om fjernede eller udfasede funktioner</span><span class="sxs-lookup"><span data-stu-id="0042b-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="0042b-126">Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="0042b-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

