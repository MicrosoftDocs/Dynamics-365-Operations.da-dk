---
title: Forsinkelser
description: Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/20/2019
ms.locfileid: "878304"
---
# <a name="delays"></a><span data-ttu-id="67cfb-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="67cfb-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67cfb-105">Dette emne indeholder oplysninger om forsinkede datoer i forbindelse med varedisponering.</span><span class="sxs-lookup"><span data-stu-id="67cfb-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="67cfb-106">En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.</span><span class="sxs-lookup"><span data-stu-id="67cfb-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="67cfb-107">Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="67cfb-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="67cfb-108">Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden.</span><span class="sxs-lookup"><span data-stu-id="67cfb-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="67cfb-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="67cfb-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="67cfb-110">I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider.</span><span class="sxs-lookup"><span data-stu-id="67cfb-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="67cfb-111">Disse leveringstider starter med alle komponentvarer på lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="67cfb-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="67cfb-112">Ordren tildeles derefter en forsinket dato.</span><span class="sxs-lookup"><span data-stu-id="67cfb-112">The order then receives a delayed date.</span></span> <span data-ttu-id="67cfb-113">En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data.</span><span class="sxs-lookup"><span data-stu-id="67cfb-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="67cfb-114">Varedisponering beregner også forsinkelsen i antal dage.</span><span class="sxs-lookup"><span data-stu-id="67cfb-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="67cfb-115">I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="67cfb-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="67cfb-116">Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="67cfb-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="67cfb-117">Du kan så senere knytte disponeringsgruppen til en vare.</span><span class="sxs-lookup"><span data-stu-id="67cfb-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="67cfb-118">På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="67cfb-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="67cfb-119">Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato.</span><span class="sxs-lookup"><span data-stu-id="67cfb-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="67cfb-120">[!Bemærk} I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en fremtidig angivet transaktion*.</span><span class="sxs-lookup"><span data-stu-id="67cfb-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="67cfb-121">Ønsket dato</span><span class="sxs-lookup"><span data-stu-id="67cfb-121">Desired date</span></span>

<span data-ttu-id="67cfb-122">På siden **Planlagt ordre** under fanen **Forsinkelser** forefindes den **Ønskede dato** for den planlagte ordre.</span><span class="sxs-lookup"><span data-stu-id="67cfb-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="67cfb-123">Den ønskede dato for en planlagt ordre er basisdatoen for forsinkelser, hvilket er en beregnet dato, der svarer til **Anmodet dato**, som beregnes på grundlag af **Nettobehov**.</span><span class="sxs-lookup"><span data-stu-id="67cfb-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="67cfb-124">Såfremt den planlagte ordre er en styklistelinje, en produktionslinje eller en kanbanlinje, baseres den ønskede dato på **Behovsdatoen**, og den ønskede dato vil ikke fremgå af siden med **Planlagt ordre**.</span><span class="sxs-lookup"><span data-stu-id="67cfb-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="67cfb-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="67cfb-125">Additional resources</span></span>
--------

[<span data-ttu-id="67cfb-126">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="67cfb-126">Coverage settings</span></span>](coverage-settings.md)
