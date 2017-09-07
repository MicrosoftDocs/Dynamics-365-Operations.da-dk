--- 
title: Oversigt over debitorbetalinger
description: "Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at angive debitorbetalinger."
author: kweekley
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 748ea62e981a2bcea0cd85ef512030a8cebf6649
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="customer-payment-overview"></a>Oversigt over debitorbetalinger

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at angive debitorbetalinger. Denne opgave bruger demofirmaet USMF.

1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Vælg den betalingskladde, som debitorbetalingerne gemmes i.
4. Vælg eller angiv kladden manuelt.
5. Klik på Angiv debitorbetalinger.
    * Angivelse af debitorbetalinger bruges til at registrere én debitorbetaling ad gangen. Du angiver betalingsoplysningerne øverst, og derefter kan du markere de fakturaer, der blev betalt med betalingen fra den samme side.  
6. Angiv den debitor, du modtog betalingen fra.
    * Hvis du ikke kender debitoren, men ved, at en transaktion er blevet betalt, kan du bruge feltet Transaktion til at angive betalingen. Angiv eller vælg fakturaen i feltet Transaktion. Debitoren bliver automatisk valgt som standard, når du har valgt transaktionen.  
7. I feltet Betalingsreference skal du angive en betalingsreference.
    * Betalingsreferencen kan være debitorens checknummer eller en reference fra kundens elektronisk betaling. Betalingsreferencen er kun påkrævet, hvis du markerer, at betalingen skal medtages på et indbetalingsbilag.  
8. Vælg, om betalingen skal medtages i et indbetalingsbilag. 
9. Angiv beløbet på debitorbetalingen.
    * Det indbetalte beløb angives ikke som et standardbeløb. Det skal angives manuelt.  
10. Markér de fakturaer, der er betalt af debitoren.
    * Hvis betalingen er en forudbetaling, behøver du ikke at markere en faktura til udligning. Betalingen kan stadig gemmes og bogføres. Udligning til en faktura kan foregå på et senere tidspunkt.  
11. Angiv det samlede beløb på den betaling, der skal udlignes til den markerede faktura 
    * Dette felt kan bruges, når betalingen er en delvis betaling. Hvis du ikke indtaster et beløb, fastlægges beløbet, der skal udlignes, automatisk for dig.  
12. Klik på Gem i kladde.
    * Før du kan gemme betalingen til kladden, skal du sørge for, at modkontoen er defineret. Med Gem i kladde gemmes betalingen, og den flyttes til kladden. Du kan derefter fortsætte med at angive den næste betaling.  
13. Luk siden.
14. Klik på Linjer.
    * Når du åbner Linjer, kan du se de betalinger, du har registreret på siden på Angiv debitorbetalinger, og som er gemt i kladden. Du kan også bruge denne side til at angive nye debitorbetalinger eller redigere eksisterende debitorbetalinger, før de bogføres.  
15. Klik på Ny for at oprette en anden betaling. 
16. Vælg den debitor, du modtog betalingen fra.
    * Hvis du ikke kender debitoren, men ved, at en faktura er betalt via betalingen, kan du bruge feltet Faktura til manuelt at indtaste eller vælge fakturaen. Debitoren bliver angivet som standard, når fakturaen er valgt.  
17. Klik på Udlign transaktioner for at markere fakturaer, der er betalt.
    * Du behøver ikke at udligne betalinger til fakturaer. Hvis dette er en forudbetaling, eller hvis du ikke ved, hvilken fakturaen der er betalt, kan du indtaste og bogføre betalingen. Betalingen kan udlignes med en faktura på et senere tidspunkt.  
18. Markér fakturaer, der er betalt via betalingen. 
19. Angiv beløbet på den betaling, der skal udlignes til fakturaen.
20. Klik på OK.
21. I feltet Betalingsreference skal du angive en betalingsreference. .
    * Betalingsreferencen er kun påkrævet, hvis du markerer, at betalingen skal medtages på et indbetalingsbilag.  
22. Bogfør debitorbetalingerne. 

