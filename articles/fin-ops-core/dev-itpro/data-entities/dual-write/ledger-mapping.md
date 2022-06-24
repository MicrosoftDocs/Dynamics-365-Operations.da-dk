---
title: Integreret finans
description: Denne artikel beskriver integrationen af finansdata mellem Finans og drift og andre Dynamics 365-programmer ved hjælp af Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e83d66f3f8c8927b9baaf99838a4e242e7e011dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847183"
---
# <a name="integrated-ledger"></a>Integreret finans

[!include [banner](../../includes/banner.md)]



I et forretningsprogram definerer finansdata den kerneopsætning, der er angivet for en virksomheds drift. Finansdataene beskriver f.eks. hvilket regnskabsår, firmaet følger, de valutaer, det anvender, og de konti, der bruges. Denne artikel beskriver integrationen af disse økonomiske kernedata.

## <a name="templates"></a>Skabeloner

Finansdata omfatter en samling af centrale finansielle tabeltilknytninger, der arbejder sammen under datainteraktion, som vist i følgende tabel.

Finans og drift-apps | Kundeengagementapps     | Betegnelse
---------------------------------|----------------------------------|------------
[CDS-valutakurser](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Kontoplan](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valutaer](mapping-reference.md#218) | handelsvaluta |
[Valutapar for valutakurser](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Valutakurstype](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Format af økonomisk dimension](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Økonomiske dimensioner](mapping-reference.md#128) | msdyn_dimensionattributes |
[Enhed for regnskabskalenderintegration](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Regnskabskalenderperiode](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Enhed for regnskabskalenderårsintegration](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Hovedkonto](mapping-reference.md#152) | msdyn_mainaccounts |
[Hovedkontokategorier](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
