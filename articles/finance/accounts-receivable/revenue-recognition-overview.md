---
title: Oversigt over indtægtsføring
description: Dette emne indeholder oplysninger om funktionen Indtægtsføring. Denne funktion giver en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen for ordrer med flere elementer.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: edc0bab7287e271f1d1197d87a95709599e12b5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820539"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="bdd0e-104">Oversigt over indtægtsføring</span><span class="sxs-lookup"><span data-stu-id="bdd0e-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdd0e-105">Virksomheder i brancher, der sælger flere elementer, f. eks. produkter, tjenester, abonnementer osv., skal være i stand til at opdele ordrer med flere elementer, så omsætningen kan genkendes på grundlag af en række firmaspecifikke og branchespecifikke retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="bdd0e-106">Funktionen Indtægtsføring kan ikke aktiveres via Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="bdd0e-107">I øjeblikket skal du bruge konfigurationsnøgler til at aktivere funktionen.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="bdd0e-108">Indtægtsføring, herunder bundtfunktionalitet, understøttes ikke til brug i handelskanaler (e-handel, POS, callcenter).</span><span class="sxs-lookup"><span data-stu-id="bdd0e-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="bdd0e-109">Varer, der er konfigureret med indtægtsføring, bør ikke føjes til ordrer eller transaktioner, der er oprettet i Commerce-kanaler.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="bdd0e-110">Generelt kan processen til indtægtsføring bruges til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="bdd0e-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="bdd0e-111">Fordele omsætning som en hjælp til at sikre, at den relevante indtægtspris genkendes på basis af værdien af komponenterne i ordrer med flere elementer.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="bdd0e-112">Udskyde omsætning på basis af en indtægtstidsplan, der repræsenterer den kontraktmæssige tidsramme og procentdele til indtægtsføring over tid.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="bdd0e-113">Videoen [Sådan bruges indtægtsføring i Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vist ovenfor) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="bdd0e-114">Funktionen Indtægtsføring indeholder en fleksibel ramme, hvor du kan definere firmaspecifikke regler for genkendelse af både indtægtsprisen og indtægtstidsplanen.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="bdd0e-115">Frigivne produkter bruges til at understøtte indtægtsføring på salgsordredokumenter.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="bdd0e-116">De frigivne produkter indeholder den opsætning, der skal bruges til at bestemme indtægtsprisen og indtægtstidsplanen.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="bdd0e-117">Salgsordren kan stamme fra et Tid og materialer-projekt.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="bdd0e-118">Virksomheder kan bruge funktionen Indtægtstidsplan uden at bruge funktionen Indtægtspris.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="bdd0e-119">Derfor bruges prisen på salgsordrelinjerne som enten omsætning eller udskudt omsætning.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="bdd0e-120">Hvis der findes en indtægtstidsplan på salgsordrelinjen, udskydes prisen på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="bdd0e-121">Hvis der ikke findes en indtægtstidsplan på salgsordrelinjen, bogføres prisen på salgsordrelinjen på en indtægtskonto, når den faktureres.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="bdd0e-122">Indtægtsprisen beregnes enten, når salgsordren bekræftes, eller når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="bdd0e-123">Hvis du vil se en prøveversion af indtægtsprisen, før fakturaen bogføres, skal du bekræfte salgsordren.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="bdd0e-124">Når salgsordren bekræftes, oprettes der også en forventet indtægtstidsplan, hvis nogen af salgsordrelinjerne indeholder en indtægtstidsplan.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="bdd0e-125">Når salgsordren faktureres, slettes den forventede indtægtstidsplan, og den forventede indtægtstidsplan erstattes af den faktiske indtægtsføringstidsplan.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="bdd0e-126">Oplysningerne om indtægtsføringstidsplanen vedligeholdes for hver salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="bdd0e-127">Den ansvarlige for indtægtsføring kan derfor få vist detaljerne og frigive linjer til omsætning, når kontraktforpligtelsen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="bdd0e-128">Ved afslutningen af hver periode kan den ansvarlige for indtægtsføringen oprette en omsætningskladde for at frigive alle tidsplanlinjer, der forfalder på eller før en dato, som pågældende definerer.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="bdd0e-129">Denne omsætningskladde bogføres ikke med det samme.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="bdd0e-130">Derfor kan den ansvarlige for indtægtsføringen kontrollere, at de korrekte beløb frigives fra udskudt indtægt til faktisk indtægt.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="bdd0e-131">Hvis en kontraktmæssig ændring medfører, at en ny salgsordrelinje føjes til enten den eksisterende salgsordre eller en ny salgsordre, kan der køres en omfordelingsproces for at rette indtægtsprisen på alle linjer på salgsordrerne.</span><span class="sxs-lookup"><span data-stu-id="bdd0e-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]