---
title: Integreret finans
description: I dette emne beskrives integrationen af finansdata mellem Finance and Operations og andre Dynamics 365-programmer ved hjælp af Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f794d8306a3a752d811d7d84c0ed5f739f423cad
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681636"
---
# <a name="integrated-ledger"></a><span data-ttu-id="50d7b-103">Integreret finans</span><span class="sxs-lookup"><span data-stu-id="50d7b-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="50d7b-104">I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift.</span><span class="sxs-lookup"><span data-stu-id="50d7b-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="50d7b-105">Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges.</span><span class="sxs-lookup"><span data-stu-id="50d7b-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="50d7b-106">I dette emne beskrives integrationen af disse økonomiske kernedata.</span><span class="sxs-lookup"><span data-stu-id="50d7b-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="50d7b-107">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="50d7b-107">Templates</span></span>

<span data-ttu-id="50d7b-108">Finansdata omfatter en samling af centrale finansielle tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="50d7b-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="50d7b-109">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="50d7b-109">Finance and Operations apps</span></span>      | <span data-ttu-id="50d7b-110">Modelstyret app i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="50d7b-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="50d7b-111">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="50d7b-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="50d7b-112">Valutaer</span><span class="sxs-lookup"><span data-stu-id="50d7b-112">Currencies</span></span>                       | <span data-ttu-id="50d7b-113">handelsvaluta</span><span class="sxs-lookup"><span data-stu-id="50d7b-113">transactioncurrencies</span></span>            |
<span data-ttu-id="50d7b-114">Regnskabskalender</span><span class="sxs-lookup"><span data-stu-id="50d7b-114">FiscalCalendar</span></span>                   | <span data-ttu-id="50d7b-115">msdyn\_regnskabskalendere</span><span class="sxs-lookup"><span data-stu-id="50d7b-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="50d7b-116">Regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="50d7b-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="50d7b-117">msdyn\_regnskabskalenderår</span><span class="sxs-lookup"><span data-stu-id="50d7b-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="50d7b-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="50d7b-118">ExchRateType</span></span>                     | <span data-ttu-id="50d7b-119">msdyn\_vekseltyper</span><span class="sxs-lookup"><span data-stu-id="50d7b-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="50d7b-120">ValutaparForValutakurser</span><span class="sxs-lookup"><span data-stu-id="50d7b-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="50d7b-121">msdyn\_valutaomvekslingspar</span><span class="sxs-lookup"><span data-stu-id="50d7b-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="50d7b-122">RegnskabsperiodeEnhed</span><span class="sxs-lookup"><span data-stu-id="50d7b-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="50d7b-123">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="50d7b-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="50d7b-124">KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="50d7b-124">MainAccountCategory</span></span>              | <span data-ttu-id="50d7b-125">msdyn\_KategoriForHovedkonto</span><span class="sxs-lookup"><span data-stu-id="50d7b-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="50d7b-126">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="50d7b-126">MainAccount</span></span>                      | <span data-ttu-id="50d7b-127">msdyn\_hovedkonti</span><span class="sxs-lookup"><span data-stu-id="50d7b-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="50d7b-128">Finans</span><span class="sxs-lookup"><span data-stu-id="50d7b-128">Ledger</span></span>                           | <span data-ttu-id="50d7b-129">msdyn\_finans</span><span class="sxs-lookup"><span data-stu-id="50d7b-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="50d7b-130">Vekselkurser</span><span class="sxs-lookup"><span data-stu-id="50d7b-130">ExchangeRates</span></span>                    | <span data-ttu-id="50d7b-131">msdyn\_valutaomvekslingskurser</span><span class="sxs-lookup"><span data-stu-id="50d7b-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="50d7b-132">FinansielKalenderperiode</span><span class="sxs-lookup"><span data-stu-id="50d7b-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="50d7b-133">msdyn\_regnskabskalenderperioder</span><span class="sxs-lookup"><span data-stu-id="50d7b-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="50d7b-134">DimensionAttributEnhed</span><span class="sxs-lookup"><span data-stu-id="50d7b-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="50d7b-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="50d7b-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="50d7b-136">DimensionIntegrationFormatEnhed</span><span class="sxs-lookup"><span data-stu-id="50d7b-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="50d7b-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="50d7b-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="50d7b-138">Finanskontoplan</span><span class="sxs-lookup"><span data-stu-id="50d7b-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="50d7b-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="50d7b-139">msdyn\_chartofaccounts</span></span>        |


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




