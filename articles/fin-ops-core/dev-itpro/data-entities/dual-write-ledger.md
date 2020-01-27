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
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853876"
---
# <a name="integrated-ledger"></a>Integreret finans

[!include [banner](../includes/banner.md)]

I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift. Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges. I dette emne beskrives integrationen af disse økonomiske kernedata.

## <a name="templates"></a>Skabeloner

Finansdata omfatter en samling af centrale finansielle enhedstilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

Finance and Operations-apps      | Andre Dynamics 365-apps
---------------------------------|---------------------------------
Valutaer                       | handelsvaluta
Regnskabskalender                   | msdyn\_regnskabskalendere
Regnskabskalenderår               | msdyn\_regnskabskalenderår
ExchRateType                     | msdyn\_vekseltyper
ValutaparForValutakurser         | msdyn\_valutaomvekslingspar
RegnskabsperiodeEnhed               | msdyn\_regnskabskalenderperioder
KategoriForHovedkonto              | msdyn\_KategoriForHovedkonto
Hovedkonto                      | msdyn\_hovedkonti
Finans                           | msdyn\_finans
Vekselkurser                    | msdyn\_valutaomvekslingskurser
FinansielKalenderperiode          | msdyn\_finansielkalenderperioder
DimensionAttributEnhed         | msdyn\_dimensionattributter.md
DimensionIntegrationFormatEnhed | msdyn\_finansieldimensionsformat.md
Finanskontoplan            | msdyn\_kontoplan.md


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




