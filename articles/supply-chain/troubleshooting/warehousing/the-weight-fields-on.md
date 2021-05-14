---
title: Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten
description: Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924345"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="855e5-103">Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten</span><span class="sxs-lookup"><span data-stu-id="855e5-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="855e5-104">Fejlkoder: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="855e5-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="855e5-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="855e5-105">Symptoms</span></span>

<span data-ttu-id="855e5-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="855e5-106">The system shows the following error message:</span></span>

> <span data-ttu-id="855e5-107">Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten %1.</span><span class="sxs-lookup"><span data-stu-id="855e5-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="855e5-108">Kør Konsistenskontrol af lastvægt for lagersted for at genberegne vægtfelterne.</span><span class="sxs-lookup"><span data-stu-id="855e5-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="855e5-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="855e5-109">Cause</span></span>

<span data-ttu-id="855e5-110">Felterne **Nettovægt** og **Taravægt** er angivet til *0* (nul) på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="855e5-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="855e5-111">Vægtfelterne er dog ikke angivet til *0* for vægtmålingerne for produktet.</span><span class="sxs-lookup"><span data-stu-id="855e5-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="855e5-112">Når der ikke er angivet vægtfelter på lastlinjen, kan eventuelle rettelser i antallet på lastlinjen medføre forkert vægtberegning af lasten.</span><span class="sxs-lookup"><span data-stu-id="855e5-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="855e5-113">Dette problem kan forekomme, hvis vægten på produktet er blevet ændret, siden lastlinjen blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="855e5-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="855e5-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="855e5-114">Resolution</span></span>

<span data-ttu-id="855e5-115">Når der oprettes en lastlinje, angives vægtfelterne fra produktet som standard på den.</span><span class="sxs-lookup"><span data-stu-id="855e5-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="855e5-116">Hvis vægten er nul, kan du genberegne den ved hjælp af funktionen *Konsistenskontrol af lastvægt for lagersted*.</span><span class="sxs-lookup"><span data-stu-id="855e5-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="855e5-117">Gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol**.</span><span class="sxs-lookup"><span data-stu-id="855e5-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="855e5-118">Angiv feltet **Modul** til **Lagerstedsstyring** i dialogboksen *Konsistenskontrol*.</span><span class="sxs-lookup"><span data-stu-id="855e5-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="855e5-119">Angiv feltet **Kontrollér/ret** til *Ret fejl*.</span><span class="sxs-lookup"><span data-stu-id="855e5-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="855e5-120">Marker afkrydsningsfeltet **Konsistenskontrol af lastvægt for lagersted**, og kontroller, at rækken for dette afkrydsningsfelt er markeret.</span><span class="sxs-lookup"><span data-stu-id="855e5-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="855e5-121">Øverst på listen med afkrydsningsfelter skal du vælge ellipseknappen (**...**) og derefter vælge **Dialog** i menuen.</span><span class="sxs-lookup"><span data-stu-id="855e5-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="855e5-122">I dialogboksen **Konsistenskontrol af lastvægt for lagersted** skal du angive følgende felter for at angive de kriterier, som konsistenskontrollen skal køres for:</span><span class="sxs-lookup"><span data-stu-id="855e5-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="855e5-123">**Last-id:** Angiv et last-id.</span><span class="sxs-lookup"><span data-stu-id="855e5-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="855e5-124">Lad feltet stå tomt for at markere alle last-id'er.</span><span class="sxs-lookup"><span data-stu-id="855e5-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="855e5-125">**Varenummer:** Angiv et varenummer.</span><span class="sxs-lookup"><span data-stu-id="855e5-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="855e5-126">Lad feltet stå tomt for at markere alle elementer.</span><span class="sxs-lookup"><span data-stu-id="855e5-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="855e5-127">**Genberegn altid vægt på laster:** Angiv denne indstilling til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="855e5-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="855e5-128">**Tillad overskrivning af vægt på lastlinjer:** Angiv denne indstilling til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="855e5-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="855e5-129">Vælg **OK** for at lukke dialogboksen **Konsistenskontrol af lastvægt for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="855e5-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="855e5-130">Vælg ellipseknappen, og vælg derefter **Udfør** i menuen.</span><span class="sxs-lookup"><span data-stu-id="855e5-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="855e5-131">Vægten genberegnes baseret på de kriterier, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="855e5-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="855e5-132">Vælg linket **Meddelelsesdetaljer** for at få vist resultatet af konsistenskontrollen.</span><span class="sxs-lookup"><span data-stu-id="855e5-132">Select the **Message details** link to view the result of the consistency check.</span></span>
