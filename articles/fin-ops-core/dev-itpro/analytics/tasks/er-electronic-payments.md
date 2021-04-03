---
title: Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration
description: Dette emne beskriver, hvordan du bruger en ny ER-formatkonfiguration (elektronisk rapportering) til at oprette elektroniske dokumenter til behandling af betalinger.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dd39b3faba90b38b837cd5167b216f9faa31d82
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570210"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Generere elektroniske dokumenter for betalinger ved hjælp af en formatkonfiguration

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]