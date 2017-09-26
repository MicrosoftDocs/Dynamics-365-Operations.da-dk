--- 
title: Opret en fritekstfaktura
description: Denne opgaveguide viser, hvordan du opretter en fritekstfaktura.
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a9f9a780868926009f30cee6aa634c53ca870b3f
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-free-text-invoice"></a>Opret en fritekstfaktura

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide viser, hvordan du opretter en fritekstfaktura. Denne opgave bruger demofirmaet USMF.

1. Gå til Debitor > Fakturaer > Alle fritekstfakturaer.
2. Klik på Ny.
3. Vælg en værdi i feltet Debitorkonto.
    * Fakturakontoen er som standard den samme konto, der er brugt til debitorkontoen.   
    * Regnskabsstatus begynder med Igangværende, hvis fakturaen ikke er bogført.   
    * Fakturanummeret tildeles, når fakturaen bogføres.  
    * Hvis du bruger SEPA-bemyndigelser, udfyldes bemyndigelsen til Direct Debit automatisk med en bemyndigelse, når du vælger debitorkontoen.  
4. Skriv en værdi i feltet Beskrivelse.
5. Angive et kontonummer uden dimensioner i feltet Hovedkonto.
    * Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde din konto. Du skal angive dimensioner senere i denne vejledning.  
6. Udvid oversigtspanelet Linjedetaljer, så du kan føje dimensioner til din hovedkonto.
7. Klik på fanen Økonomisk dimensionslinje.
    * Dimensionerne er kun for den valgte linje.    
    * Momsgruppen udfyldes fra kunden. Hvis kunden ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.  
    * Varemomsgruppen hentes fra hovedkontoen. Hvis hovedkontoen ikke har en varemomsgruppe, bruges varemomsgruppen fra momsparametrene i Finans.    
8. Angiv et tal i feltet Antal.
    * Antallet er valgfrit.  
9. Angiv et tal i feltet Enhedspris.
    * Enhedsprisen er valgfri.  
    * Beløbet beregnes som antallet ganget med enhedsprisen. Du kan dog tilsidesætte denne beregning og angive et beløb.  
10. Klik på Moms for at få vist den moms, der er beregnet for din faktura.
    * Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene på fanen Regulering.  
11. Klik på OK.
12. Klik på Gebyrer for at føje et gebyr til din faktura. 
13. Skriv en værdi i feltet Gebyrkode.
14. Indtast et tal i feltet Gebyrværdi.
15. Luk siden.
16. Klik på Totaler for at få vist opsummerede fakturadetaljer og totaler.
17. Klik på Luk.
18. Klik på Bogfør for at bogføre fakturaen. Du kan annullere, før du bogfører.
    * Sådan ændrer du tidspunktet for fakturaudskrivning: Vælg Aktuel for at udskrive hver faktura, når den opdateres, eller vælg Efter for at udskrive alle fakturaer, der er blevet opdateret.  
    * Hvis du vil ændre, hvordan kundens kreditmaksimum kontrolleres før bogføring, skal du ændre kreditmaksimumtypen.  
    * Hvis du vil udskrive fakturaen, skal du vælge Ja.  
    * Hvis du vil bogføre fakturaen, skal du vælge Ja. Du kan udskrive fakturaen uden bogføring.  
19. Klik på OK.


