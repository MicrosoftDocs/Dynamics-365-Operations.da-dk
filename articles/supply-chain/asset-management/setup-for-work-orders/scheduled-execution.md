---
title: Planlagt udførelse
description: I dette emne beskrives planlagt udførelse i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424658"
---
# <a name="scheduled-execution"></a><span data-ttu-id="9533f-103">Planlagt udførelse</span><span class="sxs-lookup"><span data-stu-id="9533f-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9533f-104">Du kan bruge serviceniveauer for arbejdsordrer til at konfigurere planlagt udførelse.</span><span class="sxs-lookup"><span data-stu-id="9533f-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="9533f-105">(Yderligere oplysninger om serviceniveauer for arbejdsordrer finder du under [Serviceniveau og -beskrivelse](service-level-and-description.md)). Planlagt udførelse giver fleksibilitet i arbejdsplanlægningen for vedligeholdelsesarbejdere, fordi du kan konfigurere mere eller mindre detaljerede krav for det interval, som en arbejdsordre skal fuldføres i.</span><span class="sxs-lookup"><span data-stu-id="9533f-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="9533f-106">En vedligeholdelsesarbejder, der fuldfører et job hurtigere end forventet i en produktionsfacilitet, kan f.eks. gå videre til et andet job i nærheden, der er planlagt for den aktuelle uge, men ikke nødvendigvis for den aktuelle dag.</span><span class="sxs-lookup"><span data-stu-id="9533f-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="9533f-107">Denne fremgangsmåde giver mulighed for optimering af arbejderplanlægningen og jobudførelsen.</span><span class="sxs-lookup"><span data-stu-id="9533f-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="9533f-108">Opsætning af planlagt udførelse, der er relateret til arbejdsordrer, kan være generisk eller specifik.</span><span class="sxs-lookup"><span data-stu-id="9533f-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="9533f-109">Du kan oprette generiske linjer, der ikke er begrænset til bestemte arbejdsordretyper, aktivtyper osv.</span><span class="sxs-lookup"><span data-stu-id="9533f-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="9533f-110">Du kan også oprette planlagte udførelseslinjer, der gælder for en bestemt arbejdsordretype, aktivtype, vedligeholdelsesjobtype osv.</span><span class="sxs-lookup"><span data-stu-id="9533f-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="9533f-111">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdsordrer** \> **Planlagt udførelse**.</span><span class="sxs-lookup"><span data-stu-id="9533f-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="9533f-112">Vælg **Ny** for at oprette en linje for planlagt udførelse.</span><span class="sxs-lookup"><span data-stu-id="9533f-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="9533f-113">Vælg værdier efter behov i felterne **Arbejdssted**, **Arbejdsordretype**, **Aktivtype** **Producent**, **Model**, **Vedligeholdelsesjobtypekategori**, **Vedligeholdelsesjobtype**, **Vedligeholdelsesjobtypevariant** og **Fag**.</span><span class="sxs-lookup"><span data-stu-id="9533f-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="9533f-114">Vælg et serviceniveau for arbejdsordren i feltet **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="9533f-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="9533f-115">Hvis du lader dette felt være tomt, skal du angive den mest generelle linjetype for planlagt udførelse.</span><span class="sxs-lookup"><span data-stu-id="9533f-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="9533f-116">Du kan se et eksempel på en generisk linje i den første post i illustrationen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9533f-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="9533f-117">Denne linje gør det muligt, at planlægge alle arbejdsordrer, der ikke har et serviceniveau for arbejdsordren, til en bestemt dato og tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="9533f-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="9533f-118">Vælg tidsinterval i feltet **Planlagt udførelse**.</span><span class="sxs-lookup"><span data-stu-id="9533f-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="9533f-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9533f-119">Select **Save**.</span></span>

![Planlagt udførelse](media/20-setup-for-work-orders.png)
