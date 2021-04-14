---
title: Integreret finans
description: I dette emne beskrives integrationen af finansdata mellem Finance and Operations og andre Dynamics 365-programmer ved hjælp af Dataverse.
author: robinarh
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
ms.openlocfilehash: 5fedcbcd8db2692214ea66b2fbab9f7381e0a622
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748511"
---
# <a name="integrated-ledger"></a><span data-ttu-id="1b2f2-103">Integreret finans</span><span class="sxs-lookup"><span data-stu-id="1b2f2-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1b2f2-104">I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift.</span><span class="sxs-lookup"><span data-stu-id="1b2f2-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="1b2f2-105">Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges.</span><span class="sxs-lookup"><span data-stu-id="1b2f2-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="1b2f2-106">I dette emne beskrives integrationen af disse økonomiske kernedata.</span><span class="sxs-lookup"><span data-stu-id="1b2f2-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="1b2f2-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="1b2f2-107">Templates</span></span>

<span data-ttu-id="1b2f2-108">Finansdata omfatter en samling af centrale finansielle tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="1b2f2-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="1b2f2-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="1b2f2-109">Finance and Operations apps</span></span>      | <span data-ttu-id="1b2f2-110">Modelstyret app i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1b2f2-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="1b2f2-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="1b2f2-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="1b2f2-112">Valutaer</span><span class="sxs-lookup"><span data-stu-id="1b2f2-112">Currencies</span></span>                       | <span data-ttu-id="1b2f2-113">handelsvaluta</span><span class="sxs-lookup"><span data-stu-id="1b2f2-113">transactioncurrencies</span></span>            |
<span data-ttu-id="1b2f2-114">Regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="1b2f2-114">FiscalCalendar</span></span>                   | <span data-ttu-id="1b2f2-115">msdyn\_regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="1b2f2-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="1b2f2-116">Regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="1b2f2-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="1b2f2-117">msdyn\_regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="1b2f2-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="1b2f2-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="1b2f2-118">ExchRateType</span></span>                     | <span data-ttu-id="1b2f2-119">msdyn\_vekseltyper</span><span class="sxs-lookup"><span data-stu-id="1b2f2-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="1b2f2-120">ValutaparForValutakurser</span><span class="sxs-lookup"><span data-stu-id="1b2f2-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="1b2f2-121">msdyn\_valutaomvekslingspar</span><span class="sxs-lookup"><span data-stu-id="1b2f2-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="1b2f2-122">RegnskabsperiodeEnhed</span><span class="sxs-lookup"><span data-stu-id="1b2f2-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="1b2f2-123">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="1b2f2-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="1b2f2-124">KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="1b2f2-124">MainAccountCategory</span></span>              | <span data-ttu-id="1b2f2-125">msdyn\_KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="1b2f2-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="1b2f2-126">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="1b2f2-126">MainAccount</span></span>                      | <span data-ttu-id="1b2f2-127">msdyn\_hovedkonti</span><span class="sxs-lookup"><span data-stu-id="1b2f2-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="1b2f2-128">Finans</span><span class="sxs-lookup"><span data-stu-id="1b2f2-128">Ledger</span></span>                           | <span data-ttu-id="1b2f2-129">msdyn\_finans</span><span class="sxs-lookup"><span data-stu-id="1b2f2-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="1b2f2-130">Vekselkurser</span><span class="sxs-lookup"><span data-stu-id="1b2f2-130">ExchangeRates</span></span>                    | <span data-ttu-id="1b2f2-131">msdyn\_valutaomvekslingskurser</span><span class="sxs-lookup"><span data-stu-id="1b2f2-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="1b2f2-132">FinansielKalenderperiode</span><span class="sxs-lookup"><span data-stu-id="1b2f2-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="1b2f2-133">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="1b2f2-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="1b2f2-134">DimensionAttributEnhed</span><span class="sxs-lookup"><span data-stu-id="1b2f2-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="1b2f2-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="1b2f2-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="1b2f2-136">DimensionIntegrationFormatEnhed</span><span class="sxs-lookup"><span data-stu-id="1b2f2-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="1b2f2-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="1b2f2-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="1b2f2-138">Finanskontoplan</span><span class="sxs-lookup"><span data-stu-id="1b2f2-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="1b2f2-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="1b2f2-139">msdyn\_chartofaccounts</span></span>        |


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