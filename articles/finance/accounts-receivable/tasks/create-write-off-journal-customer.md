---
title: Oprette en afskrivningskladde for en debitor
description: Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188826"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Oprette en afskrivningskladde for en debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan konfigurere parametre for afskrivninger og derefter afskrive transaktioner fra siden Rykkere, siden Åbne debitorfakturaer og siden Kunde. Denne opgave bruger demofirmaet USMF.


## <a name="set-up-the-write-off-parameters"></a>Konfigurer afskrivningsparametre
1. Gå til **navigationsruden > Moduler > Kredit og inkasso > Opsætning > Debitorparametre**.
2. Klik på fanen **Rykkere**.
3. Udvid eller skjul sektionen **Afskrivning**.
    - **Afskrivningskladden** er den finanskladde, der indeholder afskrivningstransaktioner, du opretter.  
    - Du kan knytte en årsagskode til alle afskrivninger. Du kan overskrive denne standard, når afskrivningen lavet.  
    - Angiv **Separat moms** til Ja, hvis du vil adskille momsen fra den oprindelige transaktion i afskrivningen.  
4. Luk siden.
5. Gå til **Kredit og inkasso > Opsætning > Debitorposteringsprofiler**. Afskrivningskontoen vil blive brugt som udgiftskontoen eller reserveregulering i finanskladden.
6. Luk siden.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Afskriv hele debitorsaldoen fra siden Aldersfordelte saldi.
1. Gå til **Kredit > Rykkere > Aldersfordelte saldi**.
2. Marker rækken for den debitor, du vil afskrive. Du kan for eksempel markere linjen med Birch Company på den.
3. Klik på **Indsaml** i **handlingsruden**.
4. Klik på **Afskriv**.
5. Klik på **OK**.
6. Luk siden.
7. Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.
8. Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning. Der oprettes én linje for at tilbageføre debitorens saldo. En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.  
9. Luk siden.
10. Luk siden.

## <a name="write-off-transactions-from-the-collections-form"></a>Afskriv transaktioner fra formen Rykkere.
1. Gå til **Kredit > Rykkere > Aldersfordelte saldi**.
2. Vælg navnet på den kunde, som har de posteringer, du vil afskrive. Vælg for eksempel Cave Wholesales (US-004).
3. Markér rækken for den første transaktion.
4. Markér rækken for den anden transaktion.
5. Klik på **Afskriv**.
6. Skriv 'Tab' i feltet **Årsagskommentar**.
7. Klik på **OK**.
8. Luk siden.
9. Luk siden.
10. Gå til **Finans > Kladdeposteringer > Finanskladder**.
11. Vælg kladdebatchnummeret for den kladde, der indeholder din afskrivning. Der oprettes én linje for at tilbageføre debitorens saldo. En eller flere linjer oprettes for at bogføre afskrivningen på afskrivningskontoen.  
12. Luk siden.
13. Luk siden.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Afskriv en faktura fra siden Åbne debitorfakturaer
1. Gå til **navigationsruden > Moduler > Debitor > Fakturaer > Åbne debitorfakturaer**.
2. Markér linjen for en faktura. Du kan for eksempel markere linjen for CIV-000667.
3. Klik på **Faktura** i **handlingsruden**.
4. Klik på **Afskriv**.
5. Klik på **OK**.
6. Luk siden.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Afskriv en debitorsaldo fra siden Kunde.
1. Gå til **Debitor > Kunder > Alle kunder**.
2. Vælg en debitorkonto. Vælg for eksempel US-001 (Contoso Retail San Diego).
3. Klik på **Indsaml** i **handlingsruden**.
4. Klik på **Afskriv**.
5. Klik på **OK**.
6. Luk siden.
