---
title: Oversigt over indtægtsføring
description: Dette emne indeholder oplysninger om funktionen Indtægtsføring. Denne funktion giver en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen for ordrer med flere elementer.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458720"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="4eb4b-104">Oversigt over indtægtsføring</span><span class="sxs-lookup"><span data-stu-id="4eb4b-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4eb4b-105">Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="4eb4b-106">I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="4eb4b-107">Virksomheder i brancher, der sælger flere elementer, f. eks. produkter, tjenester, abonnementer osv., skal være i stand til at opdele ordrer med flere elementer, så omsætningen kan genkendes på grundlag af en række firmaspecifikke og branchespecifikke retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="4eb4b-108">Generelt kan processen til indtægtsføring bruges til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="4eb4b-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="4eb4b-109">Fordele omsætning som en hjælp til at sikre, at den relevante indtægtspris genkendes på basis af værdien af komponenterne i ordrer med flere elementer.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="4eb4b-110">Udskyde omsætning på basis af en indtægtstidsplan, der repræsenterer den kontraktmæssige tidsramme og procentdele til indtægtsføring over tid.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="4eb4b-111">Videoen [Sådan bruges indtægtsføring i Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="4eb4b-112">Funktionen Indtægtsføring indeholder en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="4eb4b-113">Frigivne produkter bruges til at understøtte indtægtsføring på salgsordredokumenter.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="4eb4b-114">De frigivne produkter indeholder den opsætning, der skal bruges til at bestemme indtægtsprisen og indtægtstidsplanen.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="4eb4b-115">Salgsordren kan stamme fra et Tid og materialer-projekt.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="4eb4b-116">Virksomheder kan bruge funktionen Indtægtstidsplan uden at bruge funktionen Indtægtspris.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="4eb4b-117">Derfor bruges prisen på salgsordrelinjerne som enten omsætning eller udskudt omsætning.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="4eb4b-118">Hvis der findes en indtægtstidsplan på salgsordrelinjen, udskydes prisen på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="4eb4b-119">Hvis der ikke findes en indtægtstidsplan på salgsordrelinjen, bogføres prisen på salgsordrelinjen på en indtægtskonto, når den faktureres.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="4eb4b-120">Indtægtsprisen beregnes enten, når salgsordren bekræftes, eller når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="4eb4b-121">Hvis du vil have vist indtægtsprisen, før fakturaen bogføres, skal du bekræfte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="4eb4b-122">Når salgsordren bekræftes, oprettes der også en forventet indtægtstidsplan, hvis nogen af salgsordrelinjerne indeholder en indtægtstidsplan.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="4eb4b-123">Når salgsordren faktureres, slettes den forventede indtægtstidsplan, og den forventede indtægtstidsplan erstattes af den faktiske indtægtsføringstidsplan.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="4eb4b-124">Oplysningerne om indtægtsføringstidsplanen vedligeholdes for hver salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="4eb4b-125">Den ansvarlige for indtægtsføring kan derfor få vist detaljerne og frigive linjer til omsætning, når kontraktforpligtelsen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="4eb4b-126">Ved afslutningen af hver periode kan den ansvarlige for indtægtsføringen oprette en omsætningskladde for at frigive alle tidsplanlinjer, der forfalder på eller før en dato, som pågældende definerer.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="4eb4b-127">Denne omsætningskladde bogføres ikke med det samme.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="4eb4b-128">Derfor kan den ansvarlige for indtægtsføringen kontrollere, at de korrekte beløb frigives fra udskudt indtægt til faktisk indtægt.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="4eb4b-129">Hvis en kontraktmæssig ændring medfører, at en ny salgsordrelinje føjes til enten den eksisterende salgsordre eller en ny salgsordre, kan der køres en omfordelingsproces for at rette indtægtsprisen på alle linjer på salgsordrerne.</span><span class="sxs-lookup"><span data-stu-id="4eb4b-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>
