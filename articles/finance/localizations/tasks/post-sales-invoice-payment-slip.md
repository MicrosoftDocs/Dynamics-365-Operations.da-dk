---
title: Bogføre en salgsfaktura med et indbetalingskort
description: Denne procedure fører dig gennem bogføring af en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 141f77af82ffe61fd9d48ab0a949b96a9c9933e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820493"
---
# <a name="post-a-sales-invoice-with-a-payment-slip"></a>Bogføre en salgsfaktura med et indbetalingskort

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]