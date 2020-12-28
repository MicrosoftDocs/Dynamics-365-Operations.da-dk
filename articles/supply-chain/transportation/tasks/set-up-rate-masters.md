---
title: Konfigurere satsmastere
description: Denne procedure viser, hvordan du opretter en satsmaster.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425090"
---
# <a name="set-up-rate-masters"></a>Konfigurere satsmastere

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en satsmaster. Logistikchefen konfigurerer normalt satsmastere, afhængigt af kontrakterne der er signeret med fragtmændene. I dette scenario skal du konfigurer en satsmaster for en fragtmand. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.

## <a name="set-up-break-master"></a>Konfigurere en pausemaster

1. Gå til **Transportstyring > Opsætning > Klassificering > Pausemaster**. Pausemastere bruges til at definere prisstrukturen og dens pausepunkter. Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.  
1. Vælg **Ny**.
1. Indtast en værdi i feltet **Pausemaster**.
1. Angiv en værdi i feltet **Navn**.
1. Vælg datatypen i feltet **Datatype**.
1. I feltet **Sammenligning** skal du angive den type sammenligning, der ønskes (med operatorer).
1. Angiv pauseenheden i feltet **Afbryd enhed**.
1. I **Detaljer**-sektionen kan du oprette så mange pauser, der er brug for til prissætningsstrukturen.
1. Vælg **Gem**.

## <a name="set-up-rate-master"></a>Konfigurer satsmaster

1. Gå til **Transportstyring > Opsætning > Klassificering > Satsmaster**.
1. Vælg **Ny**.
1. Skriv en værdi i feltet **Satsmaster**.
1. Skriv en værdi i feltet **Navn**.
1. Vælg rullelistens knap i feltet **Vurderingsmetadata-id** for at åbne opslaget. Vurderingsmetadata-id'et bestemmer de data, der er nødvendige for satsmasteren, da det definerer de metadata, der forventes af transportstyringsprogrammet, der bruger denne satsmaster.  
1. Vælg P2P-indstillingen til dette eksempel. Dette er allerede defineret i demodataene.
1. Vælg linket i den valgte række på listen.
1. Vælg **Gem**.

## <a name="set-up-rate-base"></a>Konfigurer satsgrundlag

1. Vælg **Satsgrundlag**.
    * Satsgrundlaget bestemmer satsen for fragtmanden og kan bruges til at konfigurere en tarifstruktur, da den strukturerer satserne i pausepunkterne, der er defineret i pausemasteren.  
2. Vælg **Ny**.
3. Skriv en værdi i feltet **Satsgrundlag**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg rullelistens knap i feltet **Pausemaster** for at åbne opslaget.
    * Pausemastere bruges til at definere prisstrukturen og dens pausepunkter. Prisstrukturen bruger lagdelte priser, der er baseret på fysiske dimensioner.  
6. I dette eksempel skal du bruge vægt. Dette er allerede defineret i demodataene.
7. Vælg linket i den fremhævede række på listen.
8. Udvid afsnittet **Detaljer**.
9. Vælg **Ny**.
10. Skriv "30301" i feltet **Postnummer på levering andet sted**.
11. Skriv "30318" i feltet **Til postnummer på levering andet sted**.
12. Skriv "USA" i feltet **Land/område for levering andet sted**.
13. Skriv "100" i feltet **<1.00 Lbs**.
    * Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 1 pund.  
14. Skriv "300" i feltet **<5.00 Lbs**.
    * Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 5 pund.  
15. Skriv "500" i feltet **<20.00 Lbs**.
    * Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 20 pund.  
16. Skriv "1000" i feltet **<100.00 Lbs**.
    * Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 100 pund.  
17. Skriv "3000" i feltet **<1,000.00 Lbs**.
    * Indsæt satsen pr. pund, hvis den samlede vægt af lasten er mindre end 1000 pund.  
18. Vælg **Gem**.
19. Luk siden.

## <a name="assign-rate-base"></a>Tildel satsgrundlag

1. Udvid sektionen **Tildelinger af satsgrundlag**.
2. Vælg **Ny**.
    * Du kan have flere tildelinger af satsgrundlag for hver satsmaster. Det gør det muligt at oprette flere forskellige prispointer for hver fragtmand afhængigt af destinationer, tjenester eller andre satsgrundlag. I denne procedure skal du kun oprette én satsbasistildeling.  
3. Skriv en værdi i feltet **Navn**.
4. Klik på rullelistens knap i feltet **Satsgrundlag** for at åbne opslaget.
5. Vælg linket i den fremhævede række på listen.
6. Vælg rullelistens knap i feltet **Service** for at åbne opslaget.
7. Find og vælg den ønskede post på listen.
8. Vælg linket i den fremhævede række på listen.
9. Skriv "98052" i feltet **Postnummer på afhentning**.
    * Angiv, hvilket postnummer denne satsbasistildeling skal være gyldig fra.
10. Skriv "USA" i feltet **Afhentningsland/område**.
11. Vælg **Gem**.
