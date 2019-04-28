---
title: Proces for frynsegodeberettigelse
description: Denne procedure viser, hvordan frynsegodeberettigelsesprocessen fungerer.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b842d76d2c02b7f5daa45c5a34c8f61029f6c035
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "855626"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="83c66-103">Proces for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="83c66-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83c66-104">Denne procedure viser, hvordan frynsegodeberettigelsesprocessen fungerer.</span><span class="sxs-lookup"><span data-stu-id="83c66-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="83c66-105">Når processen er fuldført, kan du se resultaterne.</span><span class="sxs-lookup"><span data-stu-id="83c66-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="83c66-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="83c66-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="83c66-107">Gå til Personale > Frynsegoder > Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="83c66-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="83c66-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="83c66-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="83c66-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="83c66-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="83c66-110">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="83c66-110">Click Edit.</span></span>
5. <span data-ttu-id="83c66-111">Vælg Regelbaseret i feltet Berettigelse.</span><span class="sxs-lookup"><span data-stu-id="83c66-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="83c66-112">Vælg den politikreglen for frynsegodet, du gerne vil anvende på frynsegodet, i feltet Regeltype.</span><span class="sxs-lookup"><span data-stu-id="83c66-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="83c66-113">Klik på fanen Frynsegode i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="83c66-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="83c66-114">Klik på Opret berettigelseshændelse for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="83c66-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="83c66-115">Skriv en værdi i feltet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="83c66-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="83c66-116">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="83c66-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="83c66-117">Vælg en indstilling i feltet "Åbn tilmelding".</span><span class="sxs-lookup"><span data-stu-id="83c66-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="83c66-118">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="83c66-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="83c66-119">Angiv en dato og et klokkeslæt i feltet Startdato for tilmeldingsperiode.</span><span class="sxs-lookup"><span data-stu-id="83c66-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="83c66-120">Angiv et tal i feltet Tilmeldingsdage.</span><span class="sxs-lookup"><span data-stu-id="83c66-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="83c66-121">Klik på Opret hændelse.</span><span class="sxs-lookup"><span data-stu-id="83c66-121">Click Create event.</span></span>
16. <span data-ttu-id="83c66-122">Klik på Tilføj i oversigtspanelet Arbejdere.</span><span class="sxs-lookup"><span data-stu-id="83c66-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="83c66-123">Vælg Medarbejdere i feltet Vis efter type.</span><span class="sxs-lookup"><span data-stu-id="83c66-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="83c66-124">Vælg "Aktuel juridisk enhed" i feltet Vis efter juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="83c66-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="83c66-125">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="83c66-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="83c66-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="83c66-126">Click OK.</span></span>
21. <span data-ttu-id="83c66-127">Klik på Proces.</span><span class="sxs-lookup"><span data-stu-id="83c66-127">Click Process.</span></span>
22. <span data-ttu-id="83c66-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="83c66-128">Click OK.</span></span>
23. <span data-ttu-id="83c66-129">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="83c66-129">Refresh the page.</span></span>
24. <span data-ttu-id="83c66-130">Klik på Vis resultater.</span><span class="sxs-lookup"><span data-stu-id="83c66-130">Click Show results.</span></span>
25. <span data-ttu-id="83c66-131">Åbn kolonnefilteret Status.</span><span class="sxs-lookup"><span data-stu-id="83c66-131">Open Status column filter.</span></span>
26. <span data-ttu-id="83c66-132">Sortér A til Z</span><span class="sxs-lookup"><span data-stu-id="83c66-132">Sort A to Z</span></span>

