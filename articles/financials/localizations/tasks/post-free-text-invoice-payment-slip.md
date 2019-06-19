---
title: Bogføre en fritekstfaktura med et indbetalingskort
description: Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, SRSPrintDestinationSettingsForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b693dd297ff644d39991c809ebaa0ac2903c5180
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552470"
---
# <a name="post-a-free-text-invoice-with-a-payment-slip"></a>Bogføre en fritekstfaktura med et indbetalingskort

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format. Indbetalingskortet udskrives med kreditorens id-nummer og fakturanummeret, så indbetalingen kan identificeres.



Denne procedure fører dig gennem bogføring af en fritekstfaktura med et indbetalingskort.



Før du kan udføre denne procedure, skal du oprette et indbetalingskortformater og oprette indbetalingskort til kundefakturaer. 

Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF. 

Denne funktionalitet er kun tilgængelig for juridiske enheder, hvis primære adresse er i Danmark. 



1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kundekonto for at åbne opslaget.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Valuta for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
    * Indbetalingskortet kan kun udskrives for en fritekstfaktura med valutaen danske kroner (DKK).  
8. Klik op linket i den valgte række på listen.
9. Markér den valgte række på listen.
10. Indtast en værdi i feltet Beskrivelse.
11. Angive de ønskede værdier i feltet Hovedkonto.
12. Angiv et tal i feltet Enhedspris.
13. Klik på Gem.
14. Klik på Bogfør.
15. Klik på OK.
16. Klik på OK.

