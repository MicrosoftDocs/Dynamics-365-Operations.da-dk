---
title: Integreret finans
description: I dette emne beskrives integrationen af finansdata mellem Finance and Operations og andre Dynamics 365-programmer ved hjælp af Dataverse.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f8095b0a755e40e5665d951d33ea4ce60e749165
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567690"
---
# <a name="integrated-ledger"></a><span data-ttu-id="7b854-103">Integreret finans</span><span class="sxs-lookup"><span data-stu-id="7b854-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="7b854-104">I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift.</span><span class="sxs-lookup"><span data-stu-id="7b854-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="7b854-105">Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges.</span><span class="sxs-lookup"><span data-stu-id="7b854-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="7b854-106">I dette emne beskrives integrationen af disse økonomiske kernedata.</span><span class="sxs-lookup"><span data-stu-id="7b854-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="7b854-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="7b854-107">Templates</span></span>

<span data-ttu-id="7b854-108">Finansdata omfatter en samling af centrale finansielle tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="7b854-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="7b854-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="7b854-109">Finance and Operations apps</span></span>      | <span data-ttu-id="7b854-110">Modelstyret app i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7b854-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="7b854-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="7b854-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="7b854-112">Valutaer</span><span class="sxs-lookup"><span data-stu-id="7b854-112">Currencies</span></span>                       | <span data-ttu-id="7b854-113">handelsvaluta</span><span class="sxs-lookup"><span data-stu-id="7b854-113">transactioncurrencies</span></span>            |
<span data-ttu-id="7b854-114">Regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="7b854-114">FiscalCalendar</span></span>                   | <span data-ttu-id="7b854-115">msdyn\_regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="7b854-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="7b854-116">Regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="7b854-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="7b854-117">msdyn\_regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="7b854-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="7b854-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="7b854-118">ExchRateType</span></span>                     | <span data-ttu-id="7b854-119">msdyn\_vekseltyper</span><span class="sxs-lookup"><span data-stu-id="7b854-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="7b854-120">ValutaparForValutakurser</span><span class="sxs-lookup"><span data-stu-id="7b854-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="7b854-121">msdyn\_valutaomvekslingspar</span><span class="sxs-lookup"><span data-stu-id="7b854-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="7b854-122">RegnskabsperiodeEnhed</span><span class="sxs-lookup"><span data-stu-id="7b854-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="7b854-123">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="7b854-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7b854-124">KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="7b854-124">MainAccountCategory</span></span>              | <span data-ttu-id="7b854-125">msdyn\_KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="7b854-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="7b854-126">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="7b854-126">MainAccount</span></span>                      | <span data-ttu-id="7b854-127">msdyn\_hovedkonti</span><span class="sxs-lookup"><span data-stu-id="7b854-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="7b854-128">Finans</span><span class="sxs-lookup"><span data-stu-id="7b854-128">Ledger</span></span>                           | <span data-ttu-id="7b854-129">msdyn\_finans</span><span class="sxs-lookup"><span data-stu-id="7b854-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="7b854-130">Vekselkurser</span><span class="sxs-lookup"><span data-stu-id="7b854-130">ExchangeRates</span></span>                    | <span data-ttu-id="7b854-131">msdyn\_valutaomvekslingskurser</span><span class="sxs-lookup"><span data-stu-id="7b854-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="7b854-132">FinansielKalenderperiode</span><span class="sxs-lookup"><span data-stu-id="7b854-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="7b854-133">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="7b854-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="7b854-134">DimensionAttributEnhed</span><span class="sxs-lookup"><span data-stu-id="7b854-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="7b854-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="7b854-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="7b854-136">DimensionIntegrationFormatEnhed</span><span class="sxs-lookup"><span data-stu-id="7b854-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="7b854-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="7b854-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="7b854-138">Finanskontoplan</span><span class="sxs-lookup"><span data-stu-id="7b854-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="7b854-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="7b854-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]