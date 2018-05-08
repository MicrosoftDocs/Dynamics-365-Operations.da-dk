--- 
title: Konfigurere satsmastere
description: Denne procedure viser, hvordan du opretter en satsmaster.
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a>Konfigurere satsmastere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en satsmaster. Logistikchefen konfigurerer normalt satsmastere, afhængigt af kontrakterne der er signeret med fragtmændene. I dette scenario skal du konfigurer en satsmaster for en fragtmand. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="set-up-rate-master"></a>Konfigurer satsmaster
1. Gå til Transportstyring > Opsætning > Klassificering > Satsmaster.
2. Klik på Ny.
3. Skriv en værdi i feltet Satsmaster.
4. Skriv en værdi i feltet Navn.
5. Klik på rullelisten i feltet Vurderingsmetadata-id for at åbne opslaget.
    * Vurderingsmetadata-id'et bestemmer de data, der er nødvendige for satsmasteren, da det definerer de metadata, der forventes af TMS-programmet, der bruger denne satsmaster.  
6. Vælg P2P-indstillingen til dette eksempel
7. Klik op linket i den valgte række på listen.
8. Klik på Gem.

## <a name="set-up-rate-base"></a>Konfigurer satsgrundlag
1. Klik på Satsgrundlag.
    * Satsgrundlaget bestemmer satsen for fragtmanden og kan bruges til at konfigurere en tarifstruktur, da den strukturerer satserne i pausepunkterne, der er defineret i pausemasteren.  
2. Klik på Ny.
3. Skriv en værdi i feltet Satsgrundlag.
4. Skriv en værdi i feltet Navn.
5. Klik på rullelisten i feltet Pausemaster for at åbne opslaget.
    * Pausemastere bruges til at definere prisstrukturen og dens pausepunkter. Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.  
6. I dette eksempel skal du bruge vægt
7. Klik op linket i den valgte række på listen.
8. Slå udvidelsen af sektionen afsnittet Detaljer til/fra.
9. Klik på Ny.
10. Skriv "30301" i feltet Postnummer på levering andet sted.
11. Skriv "30318" i feltet Til postnummer på levering andet sted.
12. Skriv "USA" i feltet Land/område for levering andet sted.
13. Skriv "100" i feltet <1.00 Lbs.
    * Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 1 pund.  
14. Skriv "300" i feltet <5.00 Lbs.
    * Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 5 pund.  
15. Skriv "500" i feltet <20.00 Lbs.
    * Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 20 pund.  
16. Skriv "1000" i feltet <100.00 Lbs.
    * Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 100 pund.  
17. Skriv "3000" i feltet <1,000.00 Lbs.
    * Indsæt satsen pr. lbs, hvis den samlede vægt af belastningen er mindre end 1000 pund.  
18. Klik på Gem.
19. Luk siden.

## <a name="assign-rate-base"></a>Tildel satsgrundlag
1. Slå udvidelsen af sektionen Tildelinger af satsgrundlag til/fra.
2. Klik på Ny.
    * Du kan have flere tildelinger af satsgrundlag for hver satsmaster. Det gør det muligt at oprette flere forskellige prispointer for hver fragtmand afhængigt af destinationer, tjenester eller andre satsgrundlag. I denne procedure skal du kun oprette én satsbasistildeling.  
3. Skriv en værdi i feltet Navn.
4. Klik på rullelisten i feltet Satsgrundlag for at åbne opslaget.
5. Klik op linket i den valgte række på listen.
6. Klik på rullelisten i feltet Ydelse for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Klik op linket i den valgte række på listen.
9. Skriv "98052" i feltet Postnummer på afhentning.
    * Angiv, hvilket postnummer denne satsbasistildeling skal være gyldig fra.    
10. Skriv "USA" i feltet Afhentningsland/område.
11. Klik på Gem.


