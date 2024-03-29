---
title: Afstemme fragt manuelt
description: Denne procedure viser, hvordan du afstemmer fragt manuelt.
author: Weijiesa
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8afec41cdb10185077d39a665d0153df1c9bdb9f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672732"
---
# <a name="reconcile-freight-manually"></a>Afstemme fragt manuelt

[!include [banner](../../includes/banner.md)]]

Denne procedure viser, hvordan du afstemmer fragt manuelt. Denne konfiguration vil normalt blive udført af en transportkoordinator. Du kan bruge denne procedure i USMF-demodatafirmaet.


## <a name="select-a-load-to-reconcile"></a>Vælg en last, der skal afstemmes
1. Gå til Transportstyring > Planlægning > Lastplanlægningspanel.
2. Fjern markeringen i afkrydsningsfeltet Skjul leverede og modtagne. 
3. Vælg på listen den last, som har last-id'et 00006.

## <a name="create-a-carrier-invoice"></a>Oprette en faktura fra fragtmand
Hvis du manuelt afstemmer fragt og ikke automatisk modtager fakturaer fra fragtmænd, kan du oprette en faktura ud fra fragtbrevet.  
1. Klik på Relaterede oplysninger.
2. Klik på Fragtbrevsdetaljer.
3. Klik på Generér fragtbrevsfaktura.
4. Skriv en værdi i feltet Faktura.
5. Klik på OK.

## <a name="reconcile-the-invoice"></a>Afstem fakturaen
Når du afstemmer en fragtfaktura og et fragtbrev, kan du gøre det linje for linje.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]