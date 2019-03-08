---
title: Konfigurere visning af ældre batches på lagerstedet på en mobilenhed
description: I dette emne beskrives, hvordan du konfigurerer en mobilenhed til at vise en liste over lokaliteter med navne, der er ældre end den aktuelle lokalitet af en arbejdslinje.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "352637"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="ea6d7-103">Konfigurere visning af ældre batches på lagerstedet på en mobilenhed</span><span class="sxs-lookup"><span data-stu-id="ea6d7-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea6d7-104">Med konfigurationen **Visning af ældre batches på lagersted** kan du få vist en liste over lokaliteter med batches, der er ældre end den aktuelle lokalitet af arbejdslinjen.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="ea6d7-105">Listen over de lokaliteter, der vises, indeholder oplysninger om de ældre batches på lokaliteten med udløbsdatoen og det fysiske lager for hvert batch.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="ea6d7-106">Du kan vælge at plukke fra en ny lokalitet eller fortsætte med at plukke fra den aktuelle lokalitet.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="ea6d7-107">Pluk fra en ny lokalitet - Hvis du vælger en ny lokalitet, der skal plukkes fra, opdateres den aktuelle arbejdslinje og bruger den nye lokalitet, og arbejde fortsætter som normalt med den nye lokalitet.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="ea6d7-108">Den nye lokalitet skal have tilstrækkeligt stort disponibelt antal for hele arbejdslinjen for at være gyldig.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="ea6d7-109">Hvis behovsantallet ikke er tilgængeligt, bliver arbejdslinjen ikke opdateret, og listen vises.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="ea6d7-110">Fortsætte med pluk fra den aktuelle lokalitet – Hvis du fortsætter med den aktuelle arbejdslinjelokalitet, bliver antal for arbejdslinjen fortsat plukket fra den oprindelige lokalitet.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="ea6d7-111">Hvor det er relevant</span><span class="sxs-lookup"><span data-stu-id="ea6d7-111">Where it applies</span></span>
<span data-ttu-id="ea6d7-112">Visning af ældre batches på lagerstedet konfigureres i menupunkter på en mobilenhed og påvirker pluk for-batchet under varer.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="ea6d7-113">Konfigurere Visning af ældre batches på lagerstedet</span><span class="sxs-lookup"><span data-stu-id="ea6d7-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="ea6d7-114">Konfigurationen **Visning af ældre batches på lagerstedet** er tilgængelig i menupunkter på en mobilenhed, når indstillingen **Pluk den ældste batch** er sat til **Advar**.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="ea6d7-115">Under **Lokationsstyring** > **Konfiguration** > **Mobilenhed** > **Menupunkter i mobilenhed** skal du indstille **Brug eksisterende arbejde** til **Ja** for menupunktet og vælge **Advar** i feltet **Pluk den ældste batch**.</span><span class="sxs-lookup"><span data-stu-id="ea6d7-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

