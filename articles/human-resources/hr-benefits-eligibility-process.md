---
title: Proces for frynsegodeberettigelse
description: Denne procedure viser, hvordan frynsegodeberettigelsesprocessen fungerer.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: d23dcf4a16979b14ddf58b54e812f21e6698dfc7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417725"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="efb48-103">Proces for frynsegodeberettigelse</span><span class="sxs-lookup"><span data-stu-id="efb48-103">Benefit eligibility process</span></span>

<span data-ttu-id="efb48-104">Denne procedure viser, hvordan frynsegodeberettigelsesprocessen fungerer.</span><span class="sxs-lookup"><span data-stu-id="efb48-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="efb48-105">Når processen er fuldført, kan du se resultaterne.</span><span class="sxs-lookup"><span data-stu-id="efb48-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="efb48-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="efb48-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="efb48-107">Gå til Personale > Frynsegoder > Frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="efb48-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="efb48-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="efb48-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="efb48-109">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="efb48-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="efb48-110">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="efb48-110">Click Edit.</span></span>
5. <span data-ttu-id="efb48-111">Vælg Regelbaseret i feltet Berettigelse.</span><span class="sxs-lookup"><span data-stu-id="efb48-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="efb48-112">Vælg den politikreglen for frynsegodet, du gerne vil anvende på frynsegodet, i feltet Regeltype.</span><span class="sxs-lookup"><span data-stu-id="efb48-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="efb48-113">Klik på fanen Frynsegode i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="efb48-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="efb48-114">Klik på Opret berettigelseshændelse for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="efb48-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="efb48-115">Skriv en værdi i feltet Hændelse.</span><span class="sxs-lookup"><span data-stu-id="efb48-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="efb48-116">Indtast en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="efb48-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="efb48-117">Vælg en indstilling i feltet "Åbn tilmelding".</span><span class="sxs-lookup"><span data-stu-id="efb48-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="efb48-118">Angiv en dato og et klokkeslæt i feltet Gyldigheds startdato.</span><span class="sxs-lookup"><span data-stu-id="efb48-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="efb48-119">Angiv en dato og et klokkeslæt i feltet Startdato for tilmeldingsperiode.</span><span class="sxs-lookup"><span data-stu-id="efb48-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="efb48-120">Angiv et tal i feltet Tilmeldingsdage.</span><span class="sxs-lookup"><span data-stu-id="efb48-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="efb48-121">Klik på Opret hændelse.</span><span class="sxs-lookup"><span data-stu-id="efb48-121">Click Create event.</span></span>
16. <span data-ttu-id="efb48-122">Klik på Tilføj i oversigtspanelet Arbejdere.</span><span class="sxs-lookup"><span data-stu-id="efb48-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="efb48-123">Vælg Medarbejdere i feltet Vis efter type.</span><span class="sxs-lookup"><span data-stu-id="efb48-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="efb48-124">Vælg "Aktuel juridisk enhed" i feltet Vis efter juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="efb48-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="efb48-125">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="efb48-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="efb48-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="efb48-126">Click OK.</span></span>
21. <span data-ttu-id="efb48-127">Klik på Proces.</span><span class="sxs-lookup"><span data-stu-id="efb48-127">Click Process.</span></span>
22. <span data-ttu-id="efb48-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="efb48-128">Click OK.</span></span>
23. <span data-ttu-id="efb48-129">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="efb48-129">Refresh the page.</span></span>
24. <span data-ttu-id="efb48-130">Klik på Vis resultater.</span><span class="sxs-lookup"><span data-stu-id="efb48-130">Click Show results.</span></span>
25. <span data-ttu-id="efb48-131">Åbn kolonnefilteret Status.</span><span class="sxs-lookup"><span data-stu-id="efb48-131">Open Status column filter.</span></span>
26. <span data-ttu-id="efb48-132">Sortér A til Z</span><span class="sxs-lookup"><span data-stu-id="efb48-132">Sort A to Z</span></span>

