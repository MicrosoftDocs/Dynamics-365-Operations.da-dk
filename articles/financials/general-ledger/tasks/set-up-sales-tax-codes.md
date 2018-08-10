--- 
title: Konfigurer momskoder
description: "Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 968f4bb9f7d54cdb4de4f7842ed1777c9a9acd64
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-codes"></a>Konfigurer momskoder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Momskoder oprettes til enhver indirekte moms eller afgift, som den juridiske enhed er forpligtet til at beregne, opkræve og betale til momsmyndighederne.

Denne opgave bruger demofirmaet USMF.



1. Gå til Moms > Indirekte skatter > Moms > Momskoder.
2. Klik på Ny.
3. Skrive en værdi i feltet Momskode.
4. Skriv en værdi i feltet Navn.
5. Vælg en afregningsperiode for at angive, hvilken momsmyndighed og i hvilke intervaller denne moms skal rapporteres og betales.
6. Klik op linket i den valgte række på listen.
7. Vælg en finanskonteringsgruppe for at angive de hovedkonti, der skal bogføres moms til Finans på.
8. Find og vælg den ønskede post på listen.
9. Klik op linket i den valgte række på listen.
10. Udvid oversigtspanelet Beregning.
    * Oversigtspanelet Beregning har flere felter, der styrer, hvordan momsbeløb beregnes.  
11. Klik på Momskode i handlingsruden.
12. Klik på Værdier.
13. Markér den valgte række på listen.
14. Angiv værdien for denne momskode.
    * I oversigtspanelet beregning i feltet grundlag, hvis beløb pr. enhed er markeret, skal værdien ganges med antallet på transaktionen, der skal beregnes sales tax-beløbet.  Hvis momskoden ikke er en enhed baseret skat, er værdien en procentdel, der er anvendt på oprindelsen for denne momskode til beregning af sales tax-beløbet.     
15. Klik på Gem.
16. Luk siden.
17. Klik på Gem.


