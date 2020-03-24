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
ms.openlocfilehash: d9bcec1d4bb0207a2c3e0d46f7661b666fea3736
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112208"
---
# <a name="integrated-ledger"></a>Integreret finans

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift. Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges. I dette emne beskrives integrationen af disse økonomiske kernedata.

## <a name="templates"></a>Skabeloner

Finansdata omfatter en samling af centrale finansielle enhedstilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

Finance and Operations-apps      | Modelstyret app i Dynamics 365 | Beskrivende tekst
---------------------------------|----------------------------------|------------
Valutaer                       | handelsvaluta            |
Regnskabskalender                   | msdyn\_regnskabskalendere        |
Regnskabskalenderår               | msdyn\_regnskabskalenderår        |
ExchRateType                     | msdyn\_vekseltyper        |
ValutaparForValutakurser         | msdyn\_valutaomvekslingspar        |
RegnskabsperiodeEnhed               | msdyn\_regnskabskalenderperioder        |
KategoriForHovedkonto              | msdyn\_KategoriForHovedkonto        |
Hovedkonto                      | msdyn\_hovedkonti        |
Finans                           | msdyn\_finans        |
Vekselkurser                    | msdyn\_valutaomvekslingskurser        |
FinansielKalenderperiode          | msdyn\_regnskabskalenderperioder        |
DimensionAttributEnhed         | msdyn\_dimensionattributes        |
DimensionIntegrationFormatEnhed | msdyn\_financialdimensionformats        |
Finanskontoplan            | msdyn\_chartofaccounts        |


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




