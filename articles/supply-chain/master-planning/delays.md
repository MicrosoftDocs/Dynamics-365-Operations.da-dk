---
title: Forsinkelser
description: "Denne artikel indeholder oplysninger om forsinkede datoer i varedisponering. En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="c51fb-104">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="c51fb-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c51fb-105">Denne artikel indeholder oplysninger om forsinkede datoer i varedisponering.</span><span class="sxs-lookup"><span data-stu-id="c51fb-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="c51fb-106">En forsinket dato er en realistisk forfaldsdato, som en transaktion får, hvis den tidligste dato for udførelse, som Varedisponering beregner, er senere end den ønskede dato.</span><span class="sxs-lookup"><span data-stu-id="c51fb-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="c51fb-107">Varedisponering kan beregne den tidligste dato for udførelse af en transaktion, der er baseret på leveringstider, tilgængelighed af materiale, disponibel kapacitet og forskellige planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="c51fb-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="c51fb-108">Hvis Varedisponering beregner en ordredato, der ligger før dags dato, kan ordren ikke opfyldes til tiden.</span><span class="sxs-lookup"><span data-stu-id="c51fb-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="c51fb-109">Derfor er ordren forsinket.</span><span class="sxs-lookup"><span data-stu-id="c51fb-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="c51fb-110">I så fald planlægger Varedisponering ordren fremad fra dags dato og medtager leveringstider.</span><span class="sxs-lookup"><span data-stu-id="c51fb-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="c51fb-111">Disse leveringstider starter med alle komponentvarer på lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="c51fb-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="c51fb-112">Ordren tildeles derefter en forsinket dato.</span><span class="sxs-lookup"><span data-stu-id="c51fb-112">The order then receives a delayed date.</span></span> <span data-ttu-id="c51fb-113">En forsinket dato er en realistisk forfaldsdato, der er baseret på de aktuelle data.</span><span class="sxs-lookup"><span data-stu-id="c51fb-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="c51fb-114">Varedisponering beregner også forsinkelsen i antal dage.</span><span class="sxs-lookup"><span data-stu-id="c51fb-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="c51fb-115">I nogle situationer kan du vælge ikke at beregne forsinkelser, som når brugerne ved, at de kan fremskynde leveringstider ved at vælge alternative leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="c51fb-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="c51fb-116">Du kan konfigurere, hvordan forsinkelser beregnes for en disponeringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c51fb-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="c51fb-117">Du kan så senere knytte disponeringsgruppen til en vare.</span><span class="sxs-lookup"><span data-stu-id="c51fb-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="c51fb-118">På siden **Varedisponeringsparametre** kan du angive starttidspunktet for beregningen af forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="c51fb-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="c51fb-119">Hvis en ordre opfyldes efter dette tidspunkt, lægges der en forsinkelse på én dag til ordrens forsinkede dato.</span><span class="sxs-lookup"><span data-stu-id="c51fb-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="c51fb-120">**Bemærk!** I tidligere versioner blev beregnede forsinkelser kaldt *terminssætninger*, den forsinkede dato blev kaldt *terminsdato*, og en forsinket transaktion blev kaldt *en transaktion angivet i fremtiden*.</span><span class="sxs-lookup"><span data-stu-id="c51fb-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="c51fb-121">Se også</span><span class="sxs-lookup"><span data-stu-id="c51fb-121">See also</span></span>
--------

[<span data-ttu-id="c51fb-122">Disponeringsindstillinger</span><span class="sxs-lookup"><span data-stu-id="c51fb-122">Coverage settings</span></span>](coverage-settings.md)




