---
title: Konfigurere momsafregningsperioder
description: I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5068c121e921c1586dc6ae003c0021bf41d2254
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441565"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ee217-103">Konfigurere momsafregningsperioder</span><span class="sxs-lookup"><span data-stu-id="ee217-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee217-104">I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ee217-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="ee217-105">Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.</span><span class="sxs-lookup"><span data-stu-id="ee217-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ee217-106">Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="ee217-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ee217-107">Alle momskoder, der er knyttet til afregningsperioden, udlignes.</span><span class="sxs-lookup"><span data-stu-id="ee217-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ee217-108">Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ee217-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="ee217-109">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ee217-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ee217-110">I navigationsruden skal du gå til **Moduler > Moms > Indirekte skatter > Moms > Momsafregningsperioder**.</span><span class="sxs-lookup"><span data-stu-id="ee217-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="ee217-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ee217-111">Select **New**.</span></span>
3. <span data-ttu-id="ee217-112">Skriv en værdi i feltet **Afregningsperiode**.</span><span class="sxs-lookup"><span data-stu-id="ee217-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="ee217-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ee217-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ee217-114">I feltet **Momsmyndighed** skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="ee217-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ee217-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ee217-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ee217-116">I feltet **Betalingsbetingelser** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="ee217-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="ee217-117">De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="ee217-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ee217-118">Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="ee217-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="ee217-119">Vælg en type for intervaller for afregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ee217-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="ee217-120">Angiv antallet af enheder i periodeintervallet pr. periode.</span><span class="sxs-lookup"><span data-stu-id="ee217-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ee217-121">For eksempel har en kvart 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="ee217-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="ee217-122">Markér eller fjern markeringen af afkrydsningsfeltet **Brug batchbehandling til afregning af moms**.</span><span class="sxs-lookup"><span data-stu-id="ee217-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="ee217-123">Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="ee217-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ee217-124">Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="ee217-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="ee217-125">I øjeblikket understøttes dette ikke i Spanien, Japan og Nederlandene.</span><span class="sxs-lookup"><span data-stu-id="ee217-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="ee217-126">Marker eller fjern markeringen i afkrydsningsfeltet **Undgå at generere modregning af momsposteringer**.</span><span class="sxs-lookup"><span data-stu-id="ee217-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="ee217-127">Som standard genererer systemet modregning af momsposteringer under udligningsprocessen, hvilket kan give problemer med ydeevnen, hvis der er et stort antal momsposteringer inden for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="ee217-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="ee217-128">Marker dette afkrydsningsfeltet for at undgå, at der genereres modregning af momsposteringer.</span><span class="sxs-lookup"><span data-stu-id="ee217-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="ee217-129">Udvid fanen **Periodeintervaller**.</span><span class="sxs-lookup"><span data-stu-id="ee217-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="ee217-130">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="ee217-130">Select **Add**.</span></span>
14. <span data-ttu-id="ee217-131">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="ee217-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="ee217-132">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="ee217-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="ee217-133">Vælg **Nyt periodeinterval**.</span><span class="sxs-lookup"><span data-stu-id="ee217-133">Select **New period interval**.</span></span> <span data-ttu-id="ee217-134">Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder.</span><span class="sxs-lookup"><span data-stu-id="ee217-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ee217-135">Du kan vende tilbage og tilføje nye periodeintervaller efter behov.</span><span class="sxs-lookup"><span data-stu-id="ee217-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="ee217-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ee217-136">Close the page.</span></span>

