--- 
title: "Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration til elektronisk rapportering (ER)"
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan bruge en ny formatkonfiguration for elektronisk rapportering (ER) til at generere elektroniske dokumenter til behandling af betalinger."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration til elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan bruge en ny formatkonfiguration for elektronisk rapportering (ER) til at generere elektroniske dokumenter til behandling af betalinger. Disse trin kan udføres i GBSI-eksempelfirmaet.

Du skal først fuldføre proceduren "Opret en konfiguration med format som et betalingsdokument" for at fuldføre disse trin.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Ændre konfigurationen af den elektroniske betalingsmåde
1. Gå til Kreditor > Opsætning af betaling > Betalingsmåder.
2. Skifte sektionen Filformat for at udvide den, hvis det er nødvendigt.
3. Brug Quick Filter til at finde poster. Filtrer for eksempel efter feltet Betalingsmåde med værdien 'Electronic'.
4. Klik på Rediger.
5. Angiv feltet Generisk elektronisk rapportering til Ja.
    * Vælg Ja for at bruge det generelle elektroniske rapporteringsmønster til generering af betalingsfiler.  
6. Klik på rullelisten i feltet Navn for at åbne opslaget.
7. Vælg formatkonfigurationen BACS (UK fiktivt).
8. Klik på Gem.
9. Luk siden.

## <a name="test-the-format-of-generated-payment-files"></a>Teste formatet for genererede betalingsfiler
1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Klik på rullelisten i feltet Navn for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
    * Vælg VendPay.  
6. Klik på Gem.
7. Klik på Linjer.
8. Skriv 'DEMF' i feltet Firma.
    * DEMF  
9. I feltet Konto skal du angive værdien "DE-01001".
    * DE - 01001  
10. Skriv 'Betaling' i feltet 'Beskrivelse'.
    * Betaling  
11. Angiv et tal i feltet Debet.
    * 1000  
12. Klik på fanen Betaling.
13. Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.
14. Find og vælg den ønskede post på listen.
    * Vælg den elektroniske værdi.  
15. Klik op linket i den valgte række på listen.
16. Klik på Gem.
17. Klik på Generer betalinger.
18. Klik på rullelisten i feltet Betalingsmåde for at åbne opslaget.
19. Find og vælg den ønskede post på listen.
    * Vælg den elektroniske værdi.  
20. Klik op linket i den valgte række på listen.
    * Vælg den elektroniske værdi.  
21. Skriv en værdi i feltet Filnavn.
    * Skriv for eksempel 'betalinger'.  
22. Klik på rullelisten i feltet Bankkonto for at åbne opslaget.
23. Klik op linket i den valgte række på listen.
    * Vælg værdien GBSI OPER.  
24. Klik på OK.
25. Klik på OK.
    * Analysér den oprettede betalingsfil i XML-format. Sammenlign det med det designede dokumentlayout og de definerede attributter for betalingstransaktioner.  


