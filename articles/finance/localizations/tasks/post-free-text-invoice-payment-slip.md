---
title: Bogføre en fritekstfaktura med et indbetalingskort
description: Dette emne forklarer, hvordan du kan bogføre en fritekstfaktura med et vedhæftet indbetalingskort i det angivne format.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, SRSPrintDestinationSettingsForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Denmark
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5dd288583eab2bfe2d95c957685baabea5b68d92
ms.sourcegitcommit: 2fba4f2ef7e513357366fc640befe0d2f7bc31f5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/05/2021
ms.locfileid: "7601484"
---
# <a name="post-a-free-text-invoice-with-a-payment-slip"></a>Bogføre en fritekstfaktura med et indbetalingskort

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
