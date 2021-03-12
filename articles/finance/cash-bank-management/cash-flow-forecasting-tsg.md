---
title: Foretage fejlfinding af opsætning af likviditetsbudget
description: Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985281"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="ca63a-104">Foretage fejlfinding af opsætning af likviditetsbudget</span><span class="sxs-lookup"><span data-stu-id="ca63a-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca63a-105">Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering.</span><span class="sxs-lookup"><span data-stu-id="ca63a-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="ca63a-106">Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.</span><span class="sxs-lookup"><span data-stu-id="ca63a-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="ca63a-107">Hvorfor vises der kun likviditet for én juridisk enhed?</span><span class="sxs-lookup"><span data-stu-id="ca63a-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="ca63a-108">Likviditetsbudgettering konfigureres og beregnes pr. juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="ca63a-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="ca63a-109">Power BI-rapporterne og funktionen til likviditetsbudgetter i Finance Insights viser resultaterne.</span><span class="sxs-lookup"><span data-stu-id="ca63a-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="ca63a-110">Der skal oprettes likviditetsbudget for hver juridisk enhed, du vil have vist et budget for.</span><span class="sxs-lookup"><span data-stu-id="ca63a-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="ca63a-111">Gennemse konfigurationen af likviditetsbudgettering i alle de juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="ca63a-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="ca63a-112">Alternativt kan du gennemse konfigurationen af alle juridiske enheder til likviditetsbudgettering og sikre dig, at de er indstillet efter behov.</span><span class="sxs-lookup"><span data-stu-id="ca63a-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="ca63a-113">Hvorfor vises alle Power BI-likviditetsdata ikke?</span><span class="sxs-lookup"><span data-stu-id="ca63a-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="ca63a-114">Der er flere trin, der skal udføres, før likviditetsbudgetter kan vises i Power BI-visninger.</span><span class="sxs-lookup"><span data-stu-id="ca63a-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="ca63a-115">Gennemse følgende checkliste, og kontroller, at alle trin er udført:</span><span class="sxs-lookup"><span data-stu-id="ca63a-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="ca63a-116">Konfigurer likviditet for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="ca63a-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="ca63a-117">Angiv systemvalutaen og systemvalutakurstypen i økonomiparametrene.</span><span class="sxs-lookup"><span data-stu-id="ca63a-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="ca63a-118">Angiv finansregnskabsvalutaen og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="ca63a-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="ca63a-119">Angiv valutakurser mellem transaktionsvalutaen og regnskabsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="ca63a-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="ca63a-120">Angiv valutakurser mellem regnskabsvalutaen og systemvalutaen.</span><span class="sxs-lookup"><span data-stu-id="ca63a-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="ca63a-121">Angiv valutakurser mellem regnskabsvalutaen og hver bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="ca63a-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="ca63a-122">Hvorfor blev Power BI-likviditetsarbejdet i tidligere versioner, men det er nu tomt?</span><span class="sxs-lookup"><span data-stu-id="ca63a-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="ca63a-123">Kontroller, at målingerne "Likviditetsmåleenhed V2" og "LedgerCovLiquidityMeasurement" fra en enhed er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="ca63a-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="ca63a-124">Du kan få flere oplysninger om, hvordan du arbejder med data i Enhedslager, under [Power BI-integration med enhedslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Bekræft, at alle trin til visning af Power BI-indhold er udført.</span><span class="sxs-lookup"><span data-stu-id="ca63a-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="ca63a-125">Du kan finde flere oplysninger i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="ca63a-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="ca63a-126">Er enhederne i enhedslageret blevet opdateret?</span><span class="sxs-lookup"><span data-stu-id="ca63a-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="ca63a-127">Du skal opdatere enhederne jævnligt for at sikre, at dataene er aktuelle og nøjagtige.</span><span class="sxs-lookup"><span data-stu-id="ca63a-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="ca63a-128">Hvis du vil opdatere en bestemt enhed manuelt, skal du gå til **Systemadministration \> Opsætning \> Enhedslager** og vælge enheden og derefter vælge **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="ca63a-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="ca63a-129">Dataene kan også opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="ca63a-129">The data can also be updated automatically.</span></span> <span data-ttu-id="ca63a-130">På siden **Enhedslager** skal du indstille til **Automatisk opdatering aktiveret** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ca63a-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
