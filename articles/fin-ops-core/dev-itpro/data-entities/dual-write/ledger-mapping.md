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
# <a name="integrated-ledger"></a>Integreret finans

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift. Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges. I dette emne beskrives integrationen af disse økonomiske kernedata.

## <a name="templates"></a>Skabeloner

Finansdata omfatter en samling af centrale finansielle tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

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

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]