---
title: Likviditetsbudget (prøveversion)
description: Dette emne beskriver likviditetsbudgetteringsfunktionen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645242"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="8c272-103">Likviditetsbudget (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="8c272-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8c272-104">Pengestrømmen er kritisk for alle virksomheder.</span><span class="sxs-lookup"><span data-stu-id="8c272-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="8c272-105">Selv rentable virksomheder kan udgøre en pålydende insolvens, hvis de ikke bevarer pengestrømmen, så de opfylder de umiddelbare behov.</span><span class="sxs-lookup"><span data-stu-id="8c272-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="8c272-106">Muligheden for likviditetsbudgettering i økonomiske indsigter kan hjælpe virksomheder med at overvåge og styre deres kassesaldi effektivt.</span><span class="sxs-lookup"><span data-stu-id="8c272-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="8c272-107">Denne funktion bruger Machine Learning til at hjælpe virksomheder med at forudsige pengestrømme mere præcist, end de tidligere har haft.</span><span class="sxs-lookup"><span data-stu-id="8c272-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="8c272-108">Den kan også hjælpe ledere med at træffe beslutninger om at optimere mulighederne i forbindelse med deres aktuelle kasseposition.</span><span class="sxs-lookup"><span data-stu-id="8c272-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="8c272-109">For de fleste firmaer er administration af pengestrømme og kørsel af likviditetsbudget en kedelig, gentaget og manuel proces.</span><span class="sxs-lookup"><span data-stu-id="8c272-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="8c272-110">De fleste firmaer anvender Microsoft Excel-løsninger med varierende grad af kompleksitet.</span><span class="sxs-lookup"><span data-stu-id="8c272-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="8c272-111">Udfordringerne ved præcis prognosticering af likviditet omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="8c272-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="8c272-112">Der er ingen tilgængelige data for beslutningstagere, da disse er spredt flere steder, herunder:</span><span class="sxs-lookup"><span data-stu-id="8c272-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="8c272-113">Regnskabs- eller virksomhedsressourceplanlægningssystemet</span><span class="sxs-lookup"><span data-stu-id="8c272-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="8c272-114">Software til økonomisk planlægning</span><span class="sxs-lookup"><span data-stu-id="8c272-114">Financial planning software</span></span>
  - <span data-ttu-id="8c272-115">Excel</span><span class="sxs-lookup"><span data-stu-id="8c272-115">Excel</span></span>
  - <span data-ttu-id="8c272-116">Yderligere programmer</span><span class="sxs-lookup"><span data-stu-id="8c272-116">Additional software applications</span></span> 
- <span data-ttu-id="8c272-117">Prognoser er baseret på en intern viden, der ligger i "siloer" inden for hvert domæne eller hver afdeling.</span><span class="sxs-lookup"><span data-stu-id="8c272-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="8c272-118">Måling af nøjagtigheden af likviditetsbudgettering, efter at regnskaberne er realiseret, er usikker og svær.</span><span class="sxs-lookup"><span data-stu-id="8c272-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="8c272-119">Oplysninger om muligheden for likviditetsbudgetter</span><span class="sxs-lookup"><span data-stu-id="8c272-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="8c272-120">Funktionen til likviditetsbudgetter indeholder følgende funktioner.</span><span class="sxs-lookup"><span data-stu-id="8c272-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="8c272-121">Gør det nemt at integrere pengestrømsdata fra eksterne systemer med Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8c272-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="8c272-122">Likviditetsbudgetter kan også bruge dataimport-eksportstrukturen.</span><span class="sxs-lookup"><span data-stu-id="8c272-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="8c272-123">Denne struktur gør det nemt at integrere med Excel OData.</span><span class="sxs-lookup"><span data-stu-id="8c272-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="8c272-124">Du kan også kombinere data fra flere kilder for at oprette en omfattende likviditetsløsning.</span><span class="sxs-lookup"><span data-stu-id="8c272-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="8c272-125">Introducerer intelligent kasseposition.</span><span class="sxs-lookup"><span data-stu-id="8c272-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="8c272-126">Der oprettes en kasseposition på baggrund af kundens betalingsmåde for at forudsige, hvornår et firma kan forvente at betale kontanter i deres konti.</span><span class="sxs-lookup"><span data-stu-id="8c272-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="8c272-127">Den analyserer også de historiske mønstre for udbetalende kreditorer for at forudsige, hvornår de fremtidige fakturaer og ordrer vil blive betalt.</span><span class="sxs-lookup"><span data-stu-id="8c272-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="8c272-128">Introducerer intelligent likviditetsbudgettering ved langsigtet budgettering ved hjælp af tidsserieprognoser via automatiseret integration med AI Builder.</span><span class="sxs-lookup"><span data-stu-id="8c272-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="8c272-129">Gør det muligt at gemme bestemte likviditetsposter eller -budgetter, redigere dem og derefter nemt sammenligne og måle prognosen for ydeevnen for de faktiske regnskaber.</span><span class="sxs-lookup"><span data-stu-id="8c272-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="8c272-130">Aktiverer hvad hvis-analyse via snapshot-sammenligning.</span><span class="sxs-lookup"><span data-stu-id="8c272-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="8c272-131">Du kan f. eks. oprette flere snapshots, der repræsenterer optimistiske, pessimistiske og de mest realistiske visninger af din likviditet og derefter sammenligne og få vist forskellene.</span><span class="sxs-lookup"><span data-stu-id="8c272-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="8c272-132">Giver mulighed for at se likviditetsbudgettet i flere valutaer, på tværs af juridiske enheder og filtrere og få vist pengestrømme, der vedrører en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="8c272-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="8c272-133">Giver dig mulighed for at filtrere og få vist bankkonti, der er knyttet til økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8c272-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="8c272-134">Funktionen til likviditetsbudget i Dynamics 365 Finance vil sætte organisationen i stand til at transformere den kedelige, komplekse, men gentagende likviditetsprojicering til en simpel, automatiseret proces.</span><span class="sxs-lookup"><span data-stu-id="8c272-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="8c272-135">Automatisering af de mest kedelige aspekter ved likviditetsbudgettering giver dig mulighed for at fokusere på vigtig beslutning om at drive de ønskede firmaresultater.</span><span class="sxs-lookup"><span data-stu-id="8c272-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="8c272-136">Konfigurere dimensioner for likviditetsbudgettering</span><span class="sxs-lookup"><span data-stu-id="8c272-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="8c272-137">En ny fane på siden **Konfiguration af likviditetsbudgettering** giver dig mulighed for at styre, hvilke økonomiske dimensioner der skal bruges til filtrering i arbejdsområdet **Likviditetsbudgettering**.</span><span class="sxs-lookup"><span data-stu-id="8c272-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="8c272-138">Denne fane vises kun, når funktionen Likviditetsbudgetter er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="8c272-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="8c272-139">Under fanen **Dimensioner** skal du vælge på den liste over dimensioner, der skal bruges til filtrering, og bruge piletasterne til at flytte dem til højre kolonne.</span><span class="sxs-lookup"><span data-stu-id="8c272-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="8c272-140">Der kan kun vælges to dimensioner til filtrering af data i likviditetsbudgettet.</span><span class="sxs-lookup"><span data-stu-id="8c272-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="8c272-141">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="8c272-141">Privacy notice</span></span>
<span data-ttu-id="8c272-142">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="8c272-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
