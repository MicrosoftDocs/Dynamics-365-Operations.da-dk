---
title: Subtotal for ordreoversigt indeholder ikke moms på gebyrer, når der bruges tilpassede ordreoversigtsmoduler
description: Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når du bruger tilpassede ordreoversigtsmoduler, og subtotalen for ordreoversigten ikke inkluderer moms på gebyrer i scenariet "pris inkluderer moms".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 260dcb6bc1585615195e32adfcd1da6bfbca294e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848831"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Subtotal for ordreoversigt indeholder ikke moms på gebyrer, når der bruges tilpassede ordreoversigtsmoduler

Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når du bruger tilpassede ordreoversigtsmoduler, og subtotalen for ordreoversigten ikke inkluderer moms på gebyrer i scenariet "pris inkluderer moms".

## <a name="description"></a>Beskrivende tekst

Fra og med Microsoft Dynamics 365 Commerce version 10.0.27 er følgende ændringer foretaget i "pris inkluderer moms"-scenario for at give en gennemført oplevelse i ordreoversigtsmoduler på tværs af e-handelswebsider.

- Der er tilføjet to nye felter: **TaxOnShippingCharge** og **TaxOnNonShippingCharges**.
- **GetSalesOrderBySalesId**- og **GetSalesOrderByTransactionId**-API'erne (Application Programming Interface) har nøjagtige værdier for følgende felter i "pris inkluderer moms"-scenariet:

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

Men hvis du bruger tilpassede ordreoversigtsmoduler, kan disse ændringer påvirke subtotalværdier i ordreoversigter uden moms på gebyrer.

## <a name="resolution"></a>Løsning

Hvis du bruger tilpassede ordreoversigtsmoduler og ikke vil arve de ændringer, der er foretaget i "pris inkluderer moms"-scenariet i Commerce version 10.0.27 og senere, skal du følge instruktionerne i dette afsnit.

Ved at vende tilbage til den forrige ordreoversigtsfunktionsmåde (før version 10.0.27) for felterne **salesTransaction.SubtotalAmount** og **salesTransaction.SubtotalAmountWithoutTax** gendanner du inkluderingen af det samlede gebyrmomsbeløb (**TaxOnShippingCharge** og **TaxOnNonShippingCharges**) i subtotalbeløbene (**SubtotalAmount** og **SubtotalAmountWithoutTax**).

Benyt følgende fremgangsmåde for at vende tilbage til den forrige funktionsmåde for ordreoversigt.

1. I Commerce headquarters skal du åbne siden Handelsparametre (**Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Handelsparametre**).
1. Vælg **Konfigurationsparametre** i venstre navigationsrude.
1. Tilføj følgende konfigurationsparametre, og angiv værdien for hver af dem til **sand**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> Hvis du tidligere har brugt konfigurationsparameteren **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled**, og du vil bevare den samme funktionalitet for egenskaben **order.NetAmountWithoutTax**, skal du også tilføje konfigurationsparameteren **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** og angive værdien til **sand**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Skjule oplysninger om momsopdeling i ordreoversigter](../hide-taxes-breakup.md)
