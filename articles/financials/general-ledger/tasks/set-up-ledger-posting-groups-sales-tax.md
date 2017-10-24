--- 
title: Oprette finanskonteringsgrupper til moms
description: "Momsen beregnes og bogføres på hovedkonti, der er angivet i finanskonteringsgrupperne."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10386719e925e53e26c7e547b29a72873a4d000d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Oprette finanskonteringsgrupper til moms

[!include[task guide banner](../../includes/task-guide-banner.md)]

Momsen beregnes og bogføres på hovedkonti, der er angivet i finanskonteringsgrupperne. Finanskonteringsgrupperne er tilknyttet de enkelte momskoder. Du kan oprette individuelle finanskonteringsgrupper til hver enkelt momskode, bruge én finanskonteringsgruppe til alle momskoder eller knytte flere finanskonteringsgrupper til momskoderne. Denne registrering anvender demofirmaet DEMF. 

1. Gå til Moms > Opsætning > Moms > Finanskonteringsgrupper.
2. Klik på Ny.
3. Indtast en værdi i feltet Finanskonteringsgruppe.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg hovedkontoen til udgående moms, som skal betales til skattemyndighederne, i feltet Udgående moms.
    * Moms opkræves på vegne af skattemyndighederne, når du sælger afgiftspligtige varer og tjenesteydelser.  
6. Vælg hovedkontoen til indgående moms, som skal modtages fra skattemyndighederne, i feltet Indgående moms.
    * Kreditorer opkræver moms på vegne af skattemyndighederne, når du køber afgiftspligtige varer og tjenesteydelser. Dette felt er ikke tilgængeligt, hvis indstillingen Anvend momsregler er valgt på siden Finansparametre. Den moms, der betales til kreditorer, debiteres i stedet samme konto som købet.   
7. Vælg i feltet Udgift for importmoms den hovedkonto til bogføring af fradragsberettiget importmoms, der ikke er opkrævet eller rapporteret til skattemyndighederne af kreditorer som en del af EU-modtagermoms GST/HST.
    * Indstillingen Importmoms skal være markeret for momskoden i momsgruppen, der bruges i transaktionen.  Dette felt er ikke tilgængeligt, hvis indstillingen Anvend momsregler er valgt på siden Finansparametre.   
8. Vælg hovedkontoen til bogføring af indgående moms, som skal betales til skattemyndighederne, i feltet Importmoms.
    * Indstillingen Importmoms skal være markeret for momskoden i momsgruppen, før importmoms kan bogføres. Hvis indstillingen Anvend momsregler er valgt i Finansparametre, bogføres modregningen til transaktionens udgiftskonto.   
9. Vælg i feltet Afregningskonto den hovedkonto, som nettosaldoen for finanskontiene, der er angivet i felterne Skyldig importmoms og Indgående moms, skal bogføres på.
    * Saldoen oprettes, når du afregner momsen, og kører bogføringsjobbet.  Hvis momsmyndigheden for afregningsperioden er knyttet til en kreditorkonto, bogføres saldoen i stedet på kreditorens konto.   
10. Vælg i feltet Kreditor kasserabat den hovedkonto, der skal bogføres kasserabat på for de momskoder, der er tilknyttet denne finanskonteringsgruppe.
    * Det er valgfrit, og hvis der ikke angives en konto, bruges hovedkontoen på kasserabatkoder. Det kan være nyttigt at bruge forskellige konti pr. finanskonteringsgruppe, hvis bruger reverse momsen på indstilling af kasserabat på momsgrupper.  
11. Vælg i feltet Debitor, kasserabat den hovedkonto, der skal bogføres kasserabat på for de momskoder, der er tilknyttet denne finanskonteringsgruppe.
    * Det er valgfrit, og hvis der ikke angives, bruges den hovedkonto på kasserabatkoderne. Det kan være nyttigt at bruge forskellige konti pr. finanskonteringsgruppe, hvis bruger reverse momsen på indstilling af kasserabat på momsgrupper.  
12. Klik på Gem.


