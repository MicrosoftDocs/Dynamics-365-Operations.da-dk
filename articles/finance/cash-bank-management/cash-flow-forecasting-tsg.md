---
title: Foretage fejlfinding af opsætning af likviditetsbudget
description: Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827308"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="6d65a-104">Foretage fejlfinding af opsætning af likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="6d65a-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d65a-105">Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering.</span><span class="sxs-lookup"><span data-stu-id="6d65a-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="6d65a-106">Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.</span><span class="sxs-lookup"><span data-stu-id="6d65a-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="6d65a-107">Hvorfor vises der kun likviditet for én juridisk enhed?</span><span class="sxs-lookup"><span data-stu-id="6d65a-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="6d65a-108">Likviditetsbudgettering konfigureres og beregnes pr. juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6d65a-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="6d65a-109">Power BI-rapporterne og funktionen til likviditetsbudgetter i Finance Insights viser resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6d65a-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="6d65a-110">Der skal oprettes likviditetsbudget for hver juridisk enhed, du vil have vist et budget for.</span><span class="sxs-lookup"><span data-stu-id="6d65a-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="6d65a-111">Gennemse konfigurationen af likviditetsbudgettering i alle de juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="6d65a-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="6d65a-112">Alternativt kan du gennemse konfigurationen af alle juridiske enheder til likviditetsbudgettering og sikre dig, at de er indstillet efter behov.</span><span class="sxs-lookup"><span data-stu-id="6d65a-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="6d65a-113">Hvorfor vises alle Power BI-likviditetsdata ikke?</span><span class="sxs-lookup"><span data-stu-id="6d65a-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="6d65a-114">Der er flere trin, der skal udføres, før likviditetsbudgetter kan vises i Power BI-visninger.</span><span class="sxs-lookup"><span data-stu-id="6d65a-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="6d65a-115">Gennemse følgende checkliste, og kontroller, at alle trin er udført:</span><span class="sxs-lookup"><span data-stu-id="6d65a-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="6d65a-116">Konfigurer likviditet for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6d65a-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="6d65a-117">Angiv systemvalutaen og systemvalutakurstypen i økonomiparametrene.</span><span class="sxs-lookup"><span data-stu-id="6d65a-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="6d65a-118">Angiv finansregnskabsvalutaen og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="6d65a-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="6d65a-119">Angiv valutakurser mellem transaktionsvalutaen og regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="6d65a-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="6d65a-120">Angiv valutakurser mellem regnskabsvalutaen og systemvalutaen.</span><span class="sxs-lookup"><span data-stu-id="6d65a-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="6d65a-121">Angiv valutakurser mellem regnskabsvalutaen og hver bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="6d65a-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="6d65a-122">Hvorfor blev Power BI-likviditetsarbejdet i tidligere versioner, men det er nu tomt?</span><span class="sxs-lookup"><span data-stu-id="6d65a-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="6d65a-123">Kontroller, at målingerne "Likviditetsmåleenhed V2" og "LedgerCovLiquidityMeasurement" fra en enhed er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="6d65a-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="6d65a-124">Du kan finde flere oplysninger om, hvordan du arbejder med data i enhedslager, i [Power BI-integration med enhedslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6d65a-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="6d65a-125">Kontrollér, at alle trin, der kræves for at se Power BI-indhold, er fuldført.</span><span class="sxs-lookup"><span data-stu-id="6d65a-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="6d65a-126">Du kan finde flere oplysninger i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="6d65a-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="6d65a-127">Er enhederne i enhedslageret blevet opdateret?</span><span class="sxs-lookup"><span data-stu-id="6d65a-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="6d65a-128">Du skal opdatere enhederne jævnligt for at sikre, at dataene er aktuelle og nøjagtige.</span><span class="sxs-lookup"><span data-stu-id="6d65a-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="6d65a-129">Hvis du vil opdatere en bestemt enhed manuelt, skal du gå til **Systemadministration \> Opsætning \> Enhedslager** og vælge enheden og derefter vælge **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="6d65a-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="6d65a-130">Dataene kan også opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="6d65a-130">The data can also be updated automatically.</span></span> <span data-ttu-id="6d65a-131">På siden **Enhedslager** skal du indstille til **Automatisk opdatering aktiveret** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6d65a-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="6d65a-132">Hvilken beregningsmetode skal bruges ved beregning af likviditetsbudgetter?</span><span class="sxs-lookup"><span data-stu-id="6d65a-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="6d65a-133">Beregningsmetoden likviditetsbudget har to vigtige valgmuligheder.</span><span class="sxs-lookup"><span data-stu-id="6d65a-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="6d65a-134">Indstillingen **Ny** beregner likviditetsbudgetter for nye dokumenter og dokumenter, der er ændret, siden det seneste batchjob blev kørt.</span><span class="sxs-lookup"><span data-stu-id="6d65a-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="6d65a-135">Denne indstilling betyder, at det køres hurtigere, fordi den behandler et mindre undersæt af dokumenterne.</span><span class="sxs-lookup"><span data-stu-id="6d65a-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="6d65a-136">Indstillingen **Total** genberegner likviditetsbudgetter for hvert dokument i systemet.</span><span class="sxs-lookup"><span data-stu-id="6d65a-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="6d65a-137">Denne indstilling tager længere tid, fordi der er mere arbejde at udføre.</span><span class="sxs-lookup"><span data-stu-id="6d65a-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="6d65a-138">Hvordan forbedrer jeg ydeevnen for det batchjob, der gentages ved likviditetsbudgettering?</span><span class="sxs-lookup"><span data-stu-id="6d65a-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="6d65a-139">Det anbefales, at du kører likviditetsbudgettet én gang om dagen på de mindst belastede tidspunkter ved hjælp af beregningsmetoden **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6d65a-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="6d65a-140">Det anbefales at bruge denne fremgangsmåde seks dage om ugen.</span><span class="sxs-lookup"><span data-stu-id="6d65a-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="6d65a-141">Kør derefter et likviditetsbudget én gang om ugen med brug af metoden **Total** på dagen med mindst aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6d65a-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

