--- 
title: "Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat"
description: "Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.openlocfilehash: 16c2af862a73047a2e6ebdc056275392fa8a0d93
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Oprette og eksportere kreditorbetalinger ved hjælp af ISO20022-betalingsformat

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter betalingslinjer i kreditorbetalingskladde og genererer en kreditorbetalingsfil ved hjælp af eksempel med ISO2022-overførsel. 

Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.

Det er den femte procedure af fem, der illustrerer kreditors betalingsproces ved hjælp af konfigurationer af elektronisk rapportering. Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="create-payment-lines"></a>Opret betalingslinjer
1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Indtast eller vælg en værdi i feltet Navn.
5. Klik på Linjer.
6. Klik på Betalingsforslag.
7. Klik på Opret betalingsforslag.
8. Udvid posterne for at inkludere sektion.
9. Klik på Filtrér.
10. Markér rækken til tabellen Leverandører og feltet Kreditorkonto på listen.
11. Indtast eller vælg en værdi i feltet Kriterier.
    * Du kan anvende kriterier efter eget valg for udvælgelse af kreditorposteringer, der skal betales. I dette eksempel bruges DE 001 som en kreditorkonto.  
12. Klik på OK.
13. Klik på OK.
14. Klik på Opret betalinger.

## <a name="generate-an-iso20022-payment-file"></a>Generer en ISO20022-betalingsfil

