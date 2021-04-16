---
title: Serviceniveau og -beskrivelse
description: I dette emne beskrives serviceniveau og -beskrivelse i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb342e700c9390e1eb9f2a9e9d67b874b3e19b8e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808250"
---
# <a name="service-level-and-description"></a><span data-ttu-id="b0b5a-103">Serviceniveau og -beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b0b5a-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b0b5a-104">Når du opretter en arbejdsordre, kan det være en god ide at definere serviceniveauerne for den og føje en generel beskrivelse til den.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="b0b5a-105">Du kan oprette serviceniveauer for arbejdsordrer på siden **Serviceniveauer for arbejdsordrer** og beskrivelser på siden **Beskrivelse af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="b0b5a-106">Oprette et serviceniveau</span><span class="sxs-lookup"><span data-stu-id="b0b5a-106">Create a service level</span></span>

1. <span data-ttu-id="b0b5a-107">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="b0b5a-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-108">Select **New**.</span></span>
3. <span data-ttu-id="b0b5a-109">Angiv serviceniveauet i feltet **Serviceniveau** (f.eks. et nummer).</span><span class="sxs-lookup"><span data-stu-id="b0b5a-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="b0b5a-110">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="b0b5a-111">I oversigtspanelet **Arbejdsordrer** kan du definere forventede start- og slutdatoer og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="b0b5a-112">Felterne i dette oversigtspanel definerer den periode, hvor arbejdsordrer skal starte og slutte.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="b0b5a-113">De bruges til arbejdsordrer, der er oprettet manuelt, og arbejdsordrer, der oprettes på basis af vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="b0b5a-114">Angiv et antal dage i feltet **Startdag** for at definere den periode, hvor arbejdsordren skal starte.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="b0b5a-115">Antal dage beregnes på grundlag af oprettelsesdatoen i arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="b0b5a-116">Hvis arbejdsordren f.eks. skal begynde, når den oprettes, skal du angive **0**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="b0b5a-117">Hvis arbejdsordren skal starte inden for en uge efter, at den er oprettet, skal du angive **7**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="b0b5a-118">Hvis du vil angive et starttidspunkt for arbejdsordren, skal du ud over at angive en startdato vælge **Ja** i indstillingen **Angiv starttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="b0b5a-119">Angiv derefter starttidspunktet i feltet **Starttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="b0b5a-120">Hvis du vælger **Nej** i denne indstillingen, bruges det aktuelle tidspunkt på dagen.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="b0b5a-121">Angiv et antal dage i feltet **Slutdag** for at definere den periode, hvor arbejdsordren skal slutte.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="b0b5a-122">Antal dage beregnes på grundlag af startdatoen i arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="b0b5a-123">Hvis arbejdsordren f.eks. skal slutte inden for en uge fra startdatoen, skal du angive **7**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="b0b5a-124">Hvis du vil angive et sluttidspunkt for arbejdsordren, skal du ud over at angive en slutdato vælge **Ja** i indstillingen **Angiv sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="b0b5a-125">Angiv derefter sluttidspunktet i feltet **Sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="b0b5a-126">Hvis du vælger **Nej** i denne indstillingen, bruges det aktuelle tidspunkt på dagen.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="b0b5a-127">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-127">Select **Save**.</span></span>

![Siden Serviceniveau for arbejdsordrer](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="b0b5a-129">Oprette en beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b0b5a-129">Create a description</span></span>

1. <span data-ttu-id="b0b5a-130">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Beskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="b0b5a-131">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-131">Select **New**.</span></span>
3. <span data-ttu-id="b0b5a-132">Indtast beskrivelsen i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="b0b5a-133">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b0b5a-133">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]