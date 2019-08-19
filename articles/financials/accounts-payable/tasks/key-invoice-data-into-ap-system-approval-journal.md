---
title: Vigtigste fakturadata til kreditorsystem ved hjælp af godkendelseskladde
description: Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837030"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Vigtigste fakturadata til kreditorsystem ved hjælp af godkendelseskladde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.


## <a name="create-and-post-and-invoice"></a>Oprette og bogføre fakturaen
1. Gå til Kreditor > Fakturaer > Indgangsbog.
2. Klik på Ny.
3. Vælg navnet på den indgangsbog, du vil bruge.
4. Klik op linket i den valgte række på listen.
5. Klik på Linjer for at åbne bogen og angive udgiftslinjer.
6. Vælg en kreditor. Angiv eller vælg for eksempel US-104
7. Skriv en værdi i feltet Faktura.
8. Indtast en værdi i feltet Beskrivelse.
9. Angiv et tal i feltet Kredit.
10. Klik på rullelisten i feltet Godkendt af for at åbne opslaget.
11. Fremhæv en godkender, og klik på Vælg for at vælge den pågældende godkender.
12. Klik på Bogfør.
13. Luk siden.
14. Luk siden.

## <a name="approve-an-invoice"></a>Godkende en faktura
1. Gå til Kreditor > Fakturaer > Fakturagodkendelse.
2. Klik på Ny.
3. Vælg navnet på den kladde til fakturagodkendelse, du vil bruge.
4. Klik op linket i den valgte række på listen.
5. Klik på linjer for at få vist en side, hvor du vil kunne vælge de fakturaer, du vil godkende.
6. Vælg Find bilag for at få vist alle fakturaer, der er klar til godkendelse.
7. Markér den faktura, du oprettede.
8. Klik på Vælg.
    * De bilag, som du har markeret ovenfor, flyttes til denne liste, når du har valgt dem.  
9. Klik på OK.
10. Klik på i feltet Kontonummer for at føje en udgiftskonto til fakturaen.
11. Angiv et kontonummer, og flyt markøren fra feltet. Indtast for eksempel 600120.
12. Klik på Bogfør.
13. Klik på Bilag for at få vist de poster, der blev bogført.
    * Kontoen til fakturaer, der afventer godkendelse, tilbageføres og erstattes med kontoen til faktiske udgifter.  

