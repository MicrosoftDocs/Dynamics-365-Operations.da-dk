--- 
title: Oprette en afskrivningskladde for en debitor
description: "Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a>Oprette en afskrivningskladde for en debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde. Denne opgave bruger demofirmaet USMF.


## <a name="set-up-the-write-off-parameters"></a>Konfigurer afskrivningsparametre
1. Gå til Kredit og inkasso > Opsætning > Debitorparametre.
2. Klik på fanen Rykkere.
3. Udvid eller skjul sektionen Afskrivning.
    * Afskrivningskladden er den finanskladde, der indeholder afskrivningstransaktioner, du opretter.  
    * Du kan knytte en årsagskode til alle afskrivninger. Du kan overskrive denne standard, når afskrivningen lavet.  
    * Angiv dette til Ja, hvis du vil adskille momsen fra den oprindelige transaktion i afskrivningen.  
4. Luk siden.
5. Gå til Kredit og inkasso > Opsætning > Debitorposteringsprofiler.
    * Afskrivningskontoen vil blive brugt som udgiftskontoen eller tilbageføringsregulering i finanskladden   
6. Luk siden.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Afskriv hele debitorsaldoen fra siden Aldersfordelte saldi.
1. Gå til Kredit > Rykkere > Aldersfordelte saldi.
2. Marker rækken for den debitor, du vil afskrive. Du kan for eksempel markere linjen med Birch Company på den.
3. Klik på Indsaml i handlingsruden.
4. Klik på Afskriv.
5. Klik på OK.
6. Luk siden.
7. Gå til Finans > Kladdeposteringer > Finanskladder.
8. Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning.
    * Der oprettes én linje for at tilbageføre debitorens saldo. En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.  
9. Luk siden.
10. Luk siden.

## <a name="write-off-transactions-from-the-collections-form"></a>Afskriv transaktioner fra formen Rykkere.
1. Gå til Kredit > Rykkere > Aldersfordelte saldi.
2. Vælg navnet på den kunde, som har de posteringer, du vil afskrive. Vælg for eksempel Cave Wholesales (US-004).
3. Markér rækken for den første transaktion.
4. Markér rækken for den anden transaktion.
5. Klik på Afskriv.
6. Skriv "Tab" feltet Årsagskommentar.
7. Klik på OK.
8. Luk siden.
9. Luk siden.
10. Gå til Finans > Kladdeposteringer > Finanskladder.
11. Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning.
    * Der oprettes én linje for at tilbageføre debitorens saldo. En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.  
12. Luk siden.
13. Luk siden.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Afskriv en faktura fra siden Åbne debitorfakturaer
1. Gå til Debitor > Fakturaer > Åbne debitorfakturaer.
2. Markér linjen for en faktura. Du kan for eksempel markere linjen for CIV-000667.
3. Klik på Faktura i handlingsruden.
4. Klik på Afskriv.
5. Klik på OK.
6. Luk siden.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Afskriv en debitorsaldo fra siden Kunde.
1. Gå til Debitor > Kunder > Alle kunder.
2. Vælg en debitorkonto. Vælg for eksempel US-001 (Contoso Retail San Diego).
3. Klik på Indsaml i handlingsruden.
4. Klik på Afskriv.
5. Klik på OK.
6. Luk siden.


