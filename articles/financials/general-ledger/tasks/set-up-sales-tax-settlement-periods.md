--- 
title: Konfigurer momsafregningsperioder
description: Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for.
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
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a>Konfigurer momsafregningsperioder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Momsafregningsperioder indeholder oplysninger om de periodeintervaller, der skal indrapporteres og betales moms for. Du kan køre en udligningsproces for en afregningsperiode for et bestemt datointerval. Alle momskoder, der er knyttet til afregningsperioden, udlignes. Afhængigt af konfigurationen af den relaterede momsmyndighed bogføres skattetilsvar enten til en kreditor eller en finanskonto.



Denne opgave bruger demofirmaet USMF.



1. Gå til Moms > Indirekte skatter > Moms > Momsafregningsperioder.
2. Klik på Ny.
3. Skriv en værdi i feltet Afregningsperiode.
4. Skriv en værdi i feltet Beskrivelse.
5. I feltet Momsmyndighed skal du vælge den momsmyndighed, der modtager rapporter og betalinger, der er oprettet for afregningsperioden.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Betalingsbetingelse for at åbne opslaget.
    * De relaterede momsmyndigheder kan konfigureres som en kreditor, og momsafregningen opretter en åben kreditorfaktura. Betalingsbetingelserne definerer forfaldsdatoen for den åbne kreditorfaktura.  
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Vælg en type for intervaller for afregningsperioder.
12. Angiv antallet af enheder i periodeintervallet pr. periode. For eksempel har en kvart 3 måneder.
13. Markér eller fjern markeringen af afkrydsningsfeltet Brug batchbehandling til afregning af moms.
    * Udligningsprocessen for afregningsperioden kan behandles som batchjob i baggrunden. Dette anbefales ved et stort antal momstransaktioner inden for et periodeinterval.  
14. Udvid fanen Periodeintervaller.
15. Klik på Tilføj.
16. Markér den valgte række på listen.
17. Indtast en dato i feltet Fra dato.
18. Indtast en dato i feltet Til dato.
19. Klik på Nyt periodeinterval.
    * Når du har angivet det første periodeinterval, kan der automatisk oprettes nye perioder. Du kan vende tilbage og tilføje nye periodeintervaller efter behov.  
20. Luk siden.


