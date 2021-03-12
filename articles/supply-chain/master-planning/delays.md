---
title: Forsinkelser
description: Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977982"
---
# <a name="delays"></a><span data-ttu-id="a63c0-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="a63c0-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a63c0-105">Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering.</span><span class="sxs-lookup"><span data-stu-id="a63c0-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="a63c0-106">En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.</span><span class="sxs-lookup"><span data-stu-id="a63c0-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="a63c0-107">Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="a63c0-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="a63c0-108">Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden.</span><span class="sxs-lookup"><span data-stu-id="a63c0-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="a63c0-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="a63c0-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="a63c0-110">I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider.</span><span class="sxs-lookup"><span data-stu-id="a63c0-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="a63c0-111">Disse leveringstider starter med alle komponentvarer på lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="a63c0-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="a63c0-112">Ordren tildeles derefter en forsinket dato.</span><span class="sxs-lookup"><span data-stu-id="a63c0-112">The order then receives a delayed date.</span></span> <span data-ttu-id="a63c0-113">En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data.</span><span class="sxs-lookup"><span data-stu-id="a63c0-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="a63c0-114">Varedisponering beregner også forsinkelsen i antal dage.</span><span class="sxs-lookup"><span data-stu-id="a63c0-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="a63c0-115">I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="a63c0-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="a63c0-116">Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a63c0-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="a63c0-117">Du kan så senere knytte disponeringsgruppen til en vare.</span><span class="sxs-lookup"><span data-stu-id="a63c0-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="a63c0-118">På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="a63c0-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="a63c0-119">Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato.</span><span class="sxs-lookup"><span data-stu-id="a63c0-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="a63c0-120">I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en fremtidig angivet transaktion*.</span><span class="sxs-lookup"><span data-stu-id="a63c0-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="a63c0-121">Begrænsede forsinkelser i produktionsopsætningen med flere styklisteniveauer</span><span class="sxs-lookup"><span data-stu-id="a63c0-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="a63c0-122">Når du arbejder med forsinkelser i en produktionsopsætning, der har flere styklisteniveauer, er det vigtigt at bemærke, at det kun er varer direkte over varen (i styklistestrukturen), som forårsager forsinkelsen, der opdateres med en forsinkelse som del af varedisponeringskørslen.</span><span class="sxs-lookup"><span data-stu-id="a63c0-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="a63c0-123">Andre varer i styklistestrukturen vil ikke få den anvendte forsinkelse, før den første varedisponering køres, når den planlagte ordre på øverste niveau er godkendt eller autoriseret.</span><span class="sxs-lookup"><span data-stu-id="a63c0-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="a63c0-124">Produktionsordrerne øverst i styklistestrukturen med forsinkelser kan godkendes (eller autoriseres), før næste varedisponering køres, for at løse denne kendte begrænsning.</span><span class="sxs-lookup"><span data-stu-id="a63c0-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="a63c0-125">På denne måde bevares forsinkelsen fra den godkendte planlagte produktionsordre, og alle underliggende komponenter opdateres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="a63c0-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="a63c0-126">Handlingsmeddelelser kan også bruges til at identificere planlagte ordrer, der kan flyttes til en senere dato på grund af andre forsinkelser i styklistestrukturen.</span><span class="sxs-lookup"><span data-stu-id="a63c0-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="a63c0-127">Ønsket dato</span><span class="sxs-lookup"><span data-stu-id="a63c0-127">Desired date</span></span>

<span data-ttu-id="a63c0-128">På siden **Planlagt ordre** under fanen **Forsinkelser** forefindes den **Ønskede dato** for den planlagte ordre.</span><span class="sxs-lookup"><span data-stu-id="a63c0-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="a63c0-129">Den ønskede dato for en planlagt ordre er basisdatoen for forsinkelser, hvilket er en beregnet dato, der svarer til **Anmodet dato**, som beregnes på grundlag af **Nettobehov**.</span><span class="sxs-lookup"><span data-stu-id="a63c0-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="a63c0-130">Såfremt den planlagte ordre er en styklistelinje, en produktionslinje eller en kanbanlinje, baseres den ønskede dato på **Behovsdatoen**, og den ønskede dato vil ikke fremgå af siden med **Planlagt ordre**.</span><span class="sxs-lookup"><span data-stu-id="a63c0-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a63c0-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a63c0-131">Additional resources</span></span>
--------

[<span data-ttu-id="a63c0-132">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="a63c0-132">Coverage settings</span></span>](coverage-settings.md)
