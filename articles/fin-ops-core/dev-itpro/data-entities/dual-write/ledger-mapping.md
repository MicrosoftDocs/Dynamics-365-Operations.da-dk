---
title: Integreret finans
description: I dette emne beskrives integrationen af finansdata mellem Finance and Operations og andre Dynamics 365-programmer ved hjælp af Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6bf1c554f56c1424da9fde98f67f80a6b7c95461
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019699"
---
# <a name="integrated-ledger"></a><span data-ttu-id="65706-103">Integreret finans</span><span class="sxs-lookup"><span data-stu-id="65706-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="65706-104">I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift.</span><span class="sxs-lookup"><span data-stu-id="65706-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="65706-105">Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges.</span><span class="sxs-lookup"><span data-stu-id="65706-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="65706-106">I dette emne beskrives integrationen af disse økonomiske kernedata.</span><span class="sxs-lookup"><span data-stu-id="65706-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="65706-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="65706-107">Templates</span></span>

<span data-ttu-id="65706-108">Finansdata omfatter en samling af centrale finansielle enhedstilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="65706-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="65706-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="65706-109">Finance and Operations apps</span></span>      | <span data-ttu-id="65706-110">Andre Dynamics 365-apps</span><span class="sxs-lookup"><span data-stu-id="65706-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="65706-111">Valutaer</span><span class="sxs-lookup"><span data-stu-id="65706-111">Currencies</span></span>                       | <span data-ttu-id="65706-112">handelsvaluta</span><span class="sxs-lookup"><span data-stu-id="65706-112">transactioncurrencies</span></span>
<span data-ttu-id="65706-113">Regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="65706-113">FiscalCalendar</span></span>                   | <span data-ttu-id="65706-114">msdyn\_regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="65706-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="65706-115">Regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="65706-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="65706-116">msdyn\_regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="65706-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="65706-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="65706-117">ExchRateType</span></span>                     | <span data-ttu-id="65706-118">msdyn\_vekseltyper</span><span class="sxs-lookup"><span data-stu-id="65706-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="65706-119">ValutaparForValutakurser</span><span class="sxs-lookup"><span data-stu-id="65706-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="65706-120">msdyn\_valutaomvekslingspar</span><span class="sxs-lookup"><span data-stu-id="65706-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="65706-121">RegnskabsperiodeEnhed</span><span class="sxs-lookup"><span data-stu-id="65706-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="65706-122">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="65706-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="65706-123">KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="65706-123">MainAccountCategory</span></span>              | <span data-ttu-id="65706-124">msdyn\_KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="65706-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="65706-125">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="65706-125">MainAccount</span></span>                      | <span data-ttu-id="65706-126">msdyn\_hovedkonti</span><span class="sxs-lookup"><span data-stu-id="65706-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="65706-127">Finans</span><span class="sxs-lookup"><span data-stu-id="65706-127">Ledger</span></span>                           | <span data-ttu-id="65706-128">msdyn\_finans</span><span class="sxs-lookup"><span data-stu-id="65706-128">msdyn\_ledgers</span></span>
<span data-ttu-id="65706-129">Vekselkurser</span><span class="sxs-lookup"><span data-stu-id="65706-129">ExchangeRates</span></span>                    | <span data-ttu-id="65706-130">msdyn\_valutaomvekslingskurser</span><span class="sxs-lookup"><span data-stu-id="65706-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="65706-131">FinansielKalenderperiode</span><span class="sxs-lookup"><span data-stu-id="65706-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="65706-132">msdyn\_finansielkalenderperioder</span><span class="sxs-lookup"><span data-stu-id="65706-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="65706-133">DimensionAttributEnhed</span><span class="sxs-lookup"><span data-stu-id="65706-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="65706-134">msdyn\_dimensionattributter.md</span><span class="sxs-lookup"><span data-stu-id="65706-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="65706-135">DimensionIntegrationFormatEnhed</span><span class="sxs-lookup"><span data-stu-id="65706-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="65706-136">msdyn\_finansieldimensionsformat.md</span><span class="sxs-lookup"><span data-stu-id="65706-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="65706-137">Finanskontoplan</span><span class="sxs-lookup"><span data-stu-id="65706-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="65706-138">msdyn\_kontoplan.md</span><span class="sxs-lookup"><span data-stu-id="65706-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




