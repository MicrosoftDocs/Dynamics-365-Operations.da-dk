---
title: Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde
description: Dette emne viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ce66a4b92f26bcec0849accad3878aef2b2f658
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109650"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde

[!include [banner](../../includes/banner.md)]

Dette emne viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.

## <a name="create-and-post-and-invoice"></a>Oprette og bogføre fakturaen
1. Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Indgangsbog**.
2. Vælg **Ny**.
3. Vælg navnet på den indgangsbog, du vil bruge.
4. Vælg **Linjer** for at åbne bogen og angive udgiftslinjer.
5. Vælg en kreditor. Angiv eller vælg for eksempel `US-104`.
6. Skriv en værdi i feltet **Faktura**.
7. Indtast en værdi i feltet **Beskrivelse**.
8. Angiv et tal i feltet **Kredit**.
9. Vælg en godkender på rullelisten i feltet **Godkendt af**.
10. Vælg **Bogfør**.

## <a name="approve-an-invoice"></a>Godkende en faktura
1. Gå i navigationsruden til **Moduler > Kreditorer > Fakturaer > Godkendelse af faktura**.
2. Vælg **Ny**.
3. Vælg navnet på den kladde til fakturagodkendelse, du vil bruge.
4. Vælg **Linjer** for at få vist en side, hvor du vil kunne vælge de fakturaer, du vil godkende.
5. Vælg **Find bilag** for at få vist alle fakturaer, der er klar til godkendelse.
6. Markér den faktura, du har oprettet, og klik derefter på **Vælg**. De bilag, som du har markeret ovenfor, flyttes til denne liste, når du har valgt dem.  
7. Vælg **OK**.
8. Vælg feltet **Kontonummer** for at føje en udgiftskonto til fakturaen.
9. Angiv et kontonummer, og flyt markøren fra feltet. Angiv for eksempel `600120`.
10. Vælg **Bogfør**.
11. Vælg **Bilag** for at få vist de poster, der blev bogført. Kontoen til fakturaer, der afventer godkendelse, tilbageføres og erstattes med kontoen til faktiske udgifter.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
