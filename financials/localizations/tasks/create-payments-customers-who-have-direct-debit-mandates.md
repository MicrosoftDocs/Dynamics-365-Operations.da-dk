--- 
title: Oprette betalinger til en debitor, som har bemyndigelser til direkte debitering
description: Denne procedure viser, hvordan du opretter en ISO20022-fil med direkte debiteringsbetalinger for en kunde, der har direkte debitering konfigureret og en faktura, der skal betales.
author: mrolecki
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a0e48d4681014899a4cc1a31ba902f244c6644b
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Oprette betalinger til en debitor, som har bemyndigelser til direkte debitering

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en ISO20022-fil med direkte debiteringsbetalinger for en kunde, der har direkte debitering konfigureret og en faktura, der skal betales. Oprettelse og bogføring af en faktura er valgfrit. I stedet for at en faktura, der skal betales, kan du vælge en bemyndigelse i en kladde, før du genererer en betalingsfil, for at understøtte et scenario for en kundes forudbetaling.



Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.



Det er den femte af fem procedurer, der viser processen til debitorbetaling ved hjælp af elektroniske rapporteringskonfigurationer. Før du kan fuldføre denne opgave, skal du udføre alle tidligere opgaver. Du skal først importere elektroniske rapporteringskonfigurationer for debitorbetaling, konfigurere betalingsmetode, og du skal konfigurere dine virksomheds- og kundeoplysninger. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Bogføre en fritekstfaktura med et direkte debiteringsoplysninger
1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Kundekonto.
    * Vælg f.eks. DE-010.  
4. Indtast eller vælg en værdi i feltet Betalingsmåde.
    * F.eks.: Vælg Elektronisk.  
5. Indtast eller vælg en værdi i feltet Id for bemyndigelse til Direct Debit.
6. Klik på Tilføj linje.
7. Indtast en værdi i feltet Beskrivelse.
8. Angive de ønskede værdier i feltet Hovedkonto.
9. Angiv et tal i feltet Enhedspris.
10. Klik på Bogfør.
11. Klik på OK.

## <a name="create-a-payment"></a>Oprette en betaling
1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Navn.
4. Klik på Linjer.
5. Klik på Betalingsforslag.
6. Klik på Opret betalingsforslag.
7. Udvid posterne for at inkludere sektion.
8. Klik på Filtrér.
9. Markér rækken for tabellen Debitorposter og feltet metoden Betalingsmåde.
    * Du kan anvende et hvilket som helst kriterie for valg af debitorposteringer, der skal betales. I dette eksempel kan du bruge Elektronisk som en betalingsmåde for at filtrere posteringer.  
10. Indtast eller vælg en værdi i feltet Kriterier.
11. Klik på OK.
12. Klik på OK.
13. Klik på Opret betalinger.

## <a name="generate-a-payment-file"></a>Oprette en betalingsfil


