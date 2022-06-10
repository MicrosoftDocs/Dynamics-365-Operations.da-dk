---
title: Subtotal i ordreoversigt indeholder ikke moms på gebyrer ved brug af tilpassede ordreoversigtsmoduler
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når du bruger tilpassede ordreoversigtsmoduler, og subtotalen for ordreoversigten ikke inkluderer moms på gebyrer i scenariet "pris inkluderer moms".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767949"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Subtotal i ordreoversigt indeholder ikke moms på gebyrer ved brug af tilpassede ordreoversigtsmoduler

Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når du bruger tilpassede ordreoversigtsmoduler, og subtotalen for ordreoversigten ikke inkluderer moms på gebyrer i scenariet "pris inkluderer moms".

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
