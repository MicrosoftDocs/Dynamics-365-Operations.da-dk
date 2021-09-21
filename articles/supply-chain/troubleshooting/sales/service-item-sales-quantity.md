---
title: Det er ikke muligt at angive servicevareantal på en salgstilbudslinje
description: Når du arbejder med salgstilbud, kan du ikke angive et salgsantal for produkter, der er servicevarer, fordi der ikke er nogen fysiske varer, der skal optælles.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475945"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Kan ikke ændre salgsantallet i et salgstilbud for en salgstilbudslinje

## <a name="symptoms"></a>Symptomer

Hvis du forsøger at angive et salgsantal (**SalesQty**-felt) for en vare af typen *Service* på en salgstilbudslinje, får du vist følgende meddelelse:

> Opdatering ikke tilladt for feltantal.

## <a name="cause"></a>Årsag

Det er efter design. Du kan ikke angive et salgsantal for produkter, der er servicevarer. Hvis du f.eks. tilbyder en service til installation af en vare, giver det ikke mening at registrere et antal, da der ikke er nogen fysisk vare at tælle. Der er kun en tjeneste.
