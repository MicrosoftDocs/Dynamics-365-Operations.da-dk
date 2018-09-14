--- 
title: Afstemme fragt manuelt
description: Denne procedure viser, hvordan du afstemmer fragt manuelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="reconcile-freight-manually"></a>Afstemme fragt manuelt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du afstemmer fragt manuelt. Denne konfiguration vil normalt blive udført af en transportkoordinator. Du kan bruge denne procedure i USMF-demodatafirmaet.


## <a name="select-a-load-to-reconcile"></a>Vælg en last, der skal afstemmes
1. Gå til Transportstyring > Planlægning > Lastplanlægningspanel.
2. Fjern markeringen i afkrydsningsfeltet Skjul leverede og modtagne. 
3. Vælg på listen den last, som har last-id'et 00006.

## <a name="create-a-carrier-invoice"></a>Oprette en faktura fra fragtmand
    * Hvis du manuelt afstemmer fragt og ikke automatisk modtager fakturaer fra fragtmænd, kan du oprette en faktura ud fra fragtbrevet.  
1. Klik på Relaterede oplysninger.
2. Klik på Fragtbrevsdetaljer.
3. Klik på Generér fragtbrevsfaktura.
4. Skriv en værdi i feltet Faktura.
5. Klik på OK.

## <a name="reconcile-the-invoice"></a>Afstem fakturaen
    * Når du afstemmer en fragtfaktura og et fragtbrev, kan du gøre det linje for linje.  
1. Klik på Afstem fragtbreve og fakturaer.
2. Udvid sektionen Fakturadetaljer.
3. Udvid sektionen Oplysninger om uafstemte fragtbreve.
4. Markér den valgte række på listen.
5. Klik på Afstem.
6. Udvid sektionen Oplysninger om afstemte fragtbreve.

## <a name="submit-the-invoice-for-approval"></a>Send fakturaen til godkendelse
1. Klik på Send til godkendelse.
2. Luk siden.
3. Fjern markeringen i afkrydsningsfeltet Skjul godkendte. 
4. Klik på Kreditorfakturajournaler.
5. Klik for at følge linket i feltet Referencekladdenummer.
6. Klik på Linjer.


