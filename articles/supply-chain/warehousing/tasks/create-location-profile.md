---
title: Oprette en lokalitetsprofil.
description: Dette emne forklarer, hvordan du opretter en lokalitetsprofil i Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 764d1dc1d7fb54e0fa14a681d6d3cdb1d829aa57
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146117"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="e9519-103">Oprette en lokalitetsprofil.</span><span class="sxs-lookup"><span data-stu-id="e9519-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9519-104">Dette emne forklarer, hvordan du opretter en lokalitetsprofil i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e9519-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e9519-105">Hver lokalitet på lagerstedet skal have tilknyttet en lokalitetsprofil, der beskriver egenskaberne for lokaliteten, for eksempel om lokaliteten tillader blandede varer.</span><span class="sxs-lookup"><span data-stu-id="e9519-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="e9519-106">I denne procedure skal vi oprette en profil for en lokalitet, der ikke kræver id-kontrol.</span><span class="sxs-lookup"><span data-stu-id="e9519-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="e9519-107">Vi aktiverer blandede varer og blandede lagerstatusser og tillader cyklusoptælling.</span><span class="sxs-lookup"><span data-stu-id="e9519-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="e9519-108">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="e9519-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="e9519-109">I navigationsruden skal du gå til **Moduler > Lokationsstyring > Opsætning > Lagersted > Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="e9519-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="e9519-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e9519-110">Select **New**.</span></span>
3. <span data-ttu-id="e9519-111">Skriv en værdi i feltet **Id for lokationsprofil**.</span><span class="sxs-lookup"><span data-stu-id="e9519-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="e9519-112">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="e9519-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="e9519-113">Indtast eller vælg en værdi i feltet **Lokationsformat**.</span><span class="sxs-lookup"><span data-stu-id="e9519-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="e9519-114">Indtast eller vælg en værdi i feltet **Lokationstype**.</span><span class="sxs-lookup"><span data-stu-id="e9519-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="e9519-115">Indtast eller vælg en værdi i feltet **Id for dokstyringsprofil**.</span><span class="sxs-lookup"><span data-stu-id="e9519-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="e9519-116">Vælg **Ja** i feltet **Tillad blandede varer**.</span><span class="sxs-lookup"><span data-stu-id="e9519-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="e9519-117">Vælg **Ja** i feltet **Tillad blandede lagerstatusser**.</span><span class="sxs-lookup"><span data-stu-id="e9519-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="e9519-118">Vælg **Ja** i feltet **Tillad cyklusoptælling**.</span><span class="sxs-lookup"><span data-stu-id="e9519-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="e9519-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e9519-119">Select **Save**.</span></span>

