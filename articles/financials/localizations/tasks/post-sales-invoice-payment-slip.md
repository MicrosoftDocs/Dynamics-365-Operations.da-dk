--- 
title: "Bogføre en salgsfaktura med et indbetalingskort (Danmark)"
description: "Denne procedure fører dig gennem bogføring af en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 05/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a443a892e2c23c2baf67b8a28922109b7c1f59ec
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="post-a-sales-invoice-with-a-payment-slip-denmark"></a>Bogføre en salgsfaktura med et indbetalingskort (Danmark)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure fører dig gennem bogføring af en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format. Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.

Før du kan udføre denne procedure, skal du først oprette et indbetalingskortformat og oprette indbetalingskort til kundefakturaer. 

Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF. Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark.

1. Gå til Debitor > Ordrer > Alle salgsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
    * Du skal først oprette det tilknyttede betalingsbilag i debitorfakturaen for den valgte kunde.  
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Valuta for at åbne opslaget.
    * Indbetalingskortet kan kun udskrives for salgsordrer med valutaen danske kroner (DKK).  
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Klik på OK.
10. Markér den valgte række på listen.
11. Klik på rullelisten i feltet Varenummer for at åbne opslaget.
12. Klik op linket i den valgte række på listen.
13. Klik på Gem.
14. Klik på Faktura i handlingsruden.
15. Klik på Faktura.
16. Klik på OK.
    * Sørg for, at den tilknyttede betaling, der er knyttet til debitorfakturaen, er indstillet til FIK 751 eller FIK 752.  
17. Klik på Ja.


