--- 
title: "Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde"
description: Denne opgaveguide viser, hvordan du kan bruge indgangsbogen til at oprette fakturaer og derefter bruge godkendelseskladden til at opdatere udgiftskonti.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 604345d357e5019e334017b2b6d0413f40818acc
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Indtaste fakturadata under kreditorer ved hjælp af en godkendelseskladde

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


