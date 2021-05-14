---
title: Konfigurere momsafregningsperioder
description: I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder i Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944771"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="9d2a9-103">Konfigurere momsafregningsperioder</span><span class="sxs-lookup"><span data-stu-id="9d2a9-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d2a9-104">I dette emne beskrives, hvordan du konfigurerer momsafregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="9d2a9-105">Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="9d2a9-106">Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="9d2a9-107">Alle momskoder, der er knyttet til afregningsperioden, udlignes.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="9d2a9-108">Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="9d2a9-109">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9d2a9-110">I navigationsruden skal du gå til **Moduler > Moms > Indirekte skatter > Moms > Momsafregningsperioder**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="9d2a9-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-111">Select **New**.</span></span>
3. <span data-ttu-id="9d2a9-112">Skriv en værdi i feltet **Afregningsperiode**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="9d2a9-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9d2a9-114">I feltet **Momsmyndighed** skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="9d2a9-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9d2a9-116">I feltet **Betalingsbetingelser** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="9d2a9-117">De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="9d2a9-118">Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="9d2a9-119">Vælg en type for intervaller for afregningsperioder.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="9d2a9-120">Angiv antallet af enheder i periodeintervallet pr. periode.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="9d2a9-121">For eksempel har en kvart 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="9d2a9-122">Markér eller fjern markeringen af afkrydsningsfeltet **Brug batchbehandling til afregning af moms**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="9d2a9-123">Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="9d2a9-124">Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="9d2a9-125">Marker eller fjern markeringen i afkrydsningsfeltet **Undgå at generere modregning af momsposteringer**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="9d2a9-126">Som standard genererer systemet modregning af momsposteringer under udligningsprocessen, hvilket kan give problemer med ydeevnen, hvis der er et stort antal momsposteringer inden for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="9d2a9-127">Marker dette afkrydsningsfeltet for at undgå, at der genereres modregning af momsposteringer.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="9d2a9-128">Udvid fanen **Periodeintervaller**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="9d2a9-129">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-129">Select **Add**.</span></span>
14. <span data-ttu-id="9d2a9-130">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="9d2a9-131">Indtast en dato i feltet **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="9d2a9-132">Vælg **Nyt periodeinterval**.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-132">Select **New period interval**.</span></span> <span data-ttu-id="9d2a9-133">Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="9d2a9-134">Du kan vende tilbage og tilføje nye periodeintervaller efter behov.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="9d2a9-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9d2a9-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
