--- 
title: "Fastlægge betalingsmåde for debitor"
description: "Opret en betalingsmåde til debitorbetalinger."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 0ba359567126efaa8274644444a8a261e24c6621
ms.contentlocale: da-dk
ms.lasthandoff: 10/26/2017

---
# <a name="establish-customer-method-of-payment"></a>Fastlægge betalingsmåde for debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

Opret en betalingsmåde til debitorbetalinger. Denne opgave bruger demofirmaet USMF.

1. Gå til Debitor > Betalingsopsætning > Betalingsmetoder.
2. Klik på Ny.
3. Angiv et id for betalingsmåden i feltet Betalingsmåde.
    * Metoden for betalings-id vises på fakturaer og betalinger, så udform beskrivelsen på en måde, så læseren ved, hvilken type betaling der registreres og for hvilken bankkonto.  
4. Indtast en beskrivelse i feltet Beskrivelse.
5. Vælg, hvilken betalingsstatus der kræves, for at betalinger kan bogføres.
    * Når du opretter en kundebetaling, kan den kun bogføres, når betalingsstatus svarer den betalingsstatus, som du angiver her.  
6. Vælg, hvordan debitorbetalinger skal oprettes for fakturaer.
    * Denne indstilling bruges kun, når du kører et betalingsforslag. Der kunne bruges et betalingsforslag til debitorbetalinger, når der udføres direkte debiteringer og trækkes midler fra kundernes bankkonti.  
7. Vælg betalingstype.
    * Betalingstypen hjælper med at afgøre, om der udføres en form for validering eller ej af betalingen.  
8. Vælg den kontotype, betalinger bogføres på.
    * Bank vil normalt blive valgt for denne indstilling.  
9. Vælg den bankkonto, som betalingen vil blive registreret på.
10. Angiv den banktransaktionstype, der identificerer den type betaling, der bruges af din bank.
    * Banktransaktionstypen bruges under bankafstemningsprocessen og kan gøre afstemningen nemmere.  
11. Vælg, om denne betaling midlertidigt skal bogføres på en mellemkonto.
    * Hvis du vil prøve variabeltid for en betaling for at cleare banken, kan du bruge funktionen Mellemkontering. Betalingen bogføres midlertidigt på en finanskonto, indtil banken er clearet, hvorefter betalingen flyttes til den bankkonto, du her defineret her.  
12. Angiv den hovedkonto, der er brugt til mellemkonteringen.
    * Dette er den hovedkonto, som betalingen skal bogføres på midlertidigt, hvis der anvendes mellemkonto.  
13. Brug fanen Filformat til at definere indstillingen for elektroniske betalinger.
14. Brug fanen Betalingskontrol til at definere felter, der er obligatoriske.
    * Hvis du f.eks. har brug for, at alle betalinger med denne betalingsmåde skal indbetales, kan du vælge denne indstilling under denne fane.  
15. Brug fanen Betalingsattributter til at definere, hvilke betalingsattributter du vil bruge til denne betalingsmåde.
16. Klik på Gem.


