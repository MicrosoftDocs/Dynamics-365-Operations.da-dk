---
title: Lokalisere fejl i salgstilbud
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgstilbud.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974754"
---
# <a name="troubleshoot-sales-quotations"></a>Lokalisere fejl i salgstilbud

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med salgstilbud.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Salgsantallet i et salgstilbud kan ikke ændres for en servicevare.

### <a name="issue-description"></a>Problembeskrivelse

Hvis du forsøger at angive et salgsantal (**SalesQty**-felt) for en vare af typen *Service* på en salgstilbudslinje, får du vist følgende meddelelse: "Opdatering ikke tilladt for feltantal".

### <a name="issue-resolution"></a>Problemløsning

Du kan ikke angive et salgsantal for produkter, der er servicevarer. Hvis du f.eks. tilbyder en service til installation af en vare, giver det ikke mening at registrere et antal, da der ikke er nogen fysisk vare. Der er kun en tjeneste.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]