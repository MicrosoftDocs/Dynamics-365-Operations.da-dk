---
title: Fastlægge betalingsmåde for debitor
description: I dette emne forklares, hvordan du kan oprette betalingsmåde til debitorbetalinger.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188803"
---
# <a name="establish-customer-method-of-payment"></a>Fastlægge betalingsmåde for debitor

[!include [task guide banner](../../includes/task-guide-banner.md)]

I dette emne forklares, hvordan du kan oprette betalingsmåde til debitorbetalinger. Denne opgave bruger demofirmaet USMF.

1. I navigationsruden skal du gå til **Moduler > Debitor > Betalingsopsætning > Betalingsmåder**.
2. Vælg **Ny**.
3. Angiv et id for betalingsmåden i feltet **Betalingsmåde**. Metoden for betalings-id vises på fakturaer og betalinger, så udform beskrivelsen på en måde, så læseren ved, hvilken type betaling der registreres og for hvilken bankkonto.  
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. Vælg, hvilken betalingsstatus der kræves, for at betalinger kan bogføres. Når du opretter en kundebetaling, kan den kun bogføres, når betalingsstatus svarer den betalingsstatus, som du angiver her.  
6. Vælg, hvordan debitorbetalinger skal oprettes for fakturaer. Denne indstilling bruges kun, når du kører et betalingsforslag. Der kunne bruges et betalingsforslag til debitorbetalinger, når der udføres direkte debiteringer og trækkes midler fra kundernes bankkonti.  
7. Vælg betalingstype. Betalingstypen hjælper med at afgøre, om der udføres en form for validering eller ej af betalingen.  
8. Vælg den kontotype, betalinger bogføres på. Bank vil normalt blive valgt for denne indstilling.  
9. Vælg den bankkonto, som betalingen vil blive registreret på.
10. Angiv den banktransaktionstype, der identificerer den type betaling, der bruges af din bank. Banktransaktionstypen bruges under bankafstemningsprocessen og kan gøre afstemningen nemmere.  
11. Vælg, om denne betaling midlertidigt skal bogføres på en mellemkonto. Hvis du vil prøve variabeltid for en betaling for at cleare banken, kan du bruge funktionen Mellemkontering. Betalingen bogføres midlertidigt på en finanskonto, indtil banken er clearet, hvorefter betalingen flyttes til den bankkonto, du her defineret her.  
12. Angiv den hovedkonto, der er brugt til mellemkonteringen. Dette er den hovedkonto, som betalingen skal bogføres på midlertidigt, hvis der anvendes mellemkonto.  
13. Brug fanen **Filformat** til at definere indstillingen for elektroniske betalinger.
14. Brug fanen **Betalingskontrol** til at definere felter, der er obligatoriske. Hvis du f.eks. har brug for, at alle betalinger med denne betalingsmåde skal indbetales, kan du vælge denne indstilling under denne fane.  
15. Brug fanen **Betalingsattributter** til at definere, hvilke betalingsattributter du vil bruge til denne betalingsmåde.
16. Vælg **Gem**.
