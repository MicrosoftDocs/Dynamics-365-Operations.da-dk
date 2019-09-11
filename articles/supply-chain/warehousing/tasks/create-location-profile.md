---
title: Oprette en lokalitetsprofil.
description: Dette emne forklarer, hvordan du opretter en lokalitetsprofil i Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866973"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="11741-103">Oprette en lokalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="11741-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11741-104">Dette emne forklarer, hvordan du opretter en lokalitetsprofil i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="11741-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="11741-105">Hver lokalitet på lagerstedet skal have tilknyttet en lokalitetsprofil, der beskriver egenskaberne for lokaliteten, for eksempel om lokaliteten tillader blandede varer.</span><span class="sxs-lookup"><span data-stu-id="11741-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="11741-106">I denne procedure skal vi oprette en profil for en lokalitet, der ikke kræver id-kontrol.</span><span class="sxs-lookup"><span data-stu-id="11741-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="11741-107">Vi aktiverer blandede varer og blandede lagerstatusser og tillader cyklusoptælling.</span><span class="sxs-lookup"><span data-stu-id="11741-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="11741-108">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="11741-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="11741-109">I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Lagersted > Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="11741-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="11741-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="11741-110">Select **New**.</span></span>
3. <span data-ttu-id="11741-111">Skriv en værdi i feltet **Id for lokationsprofil**.</span><span class="sxs-lookup"><span data-stu-id="11741-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="11741-112">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="11741-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="11741-113">Indtast eller vælg en værdi i feltet **Lokationsformat**.</span><span class="sxs-lookup"><span data-stu-id="11741-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="11741-114">Indtast eller vælg en værdi i feltet **Lokationstype**.</span><span class="sxs-lookup"><span data-stu-id="11741-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="11741-115">Indtast eller vælg en værdi i feltet **Id for dokstyringsprofil**.</span><span class="sxs-lookup"><span data-stu-id="11741-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="11741-116">Vælg **Ja** i feltet **Tillad blandede varer**.</span><span class="sxs-lookup"><span data-stu-id="11741-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="11741-117">Vælg **Ja** i feltet **Tillad blandede lagerstatusser**.</span><span class="sxs-lookup"><span data-stu-id="11741-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="11741-118">Vælg **Ja** i feltet **Tillad cyklusoptælling**.</span><span class="sxs-lookup"><span data-stu-id="11741-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="11741-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="11741-119">Select **Save**.</span></span>

