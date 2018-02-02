--- 
title: "Oprette et lukket spørgsmål"
description: "Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59f1af68e4b1198894a7cdab291021de9f3cf8a9
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-closed-ended-question"></a>Oprette et lukket spørgsmål

[!include[task guide banner](../../includes/task-guide-banner.md)]

Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra. Først skal du oprette en Svarsamling med svarene, derefter skal du oprette spørgsmålet, som bruger svarsamlingen. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-an-answer-group"></a>Opret en svarsamling
1. Gå til Spørgeskema > Design > Svarsamlinger.
2. Klik på Ny.
3. Indtast en værdi i feltet Svarsamling.
4. Skriv en værdi i feltet Beskrivelse.
    * Du kan bruge funktionen Tilfældig til at placere svarene i en tilfældig rækkefølge, hver gang svarsamlingen bruges til et spørgsmål.  
5. Klik på Svar.
6. Klik på Ny.
    * Sekvensnummeret styrer den rækkefølge, som svarene vises i, medmindre Tilfældig vælges til svarsamlingen.  
    * Point kan overdrages til svar til brug i vurdering af spørgeskemaet.  
7. Angiv et tal i feltet Point.
    * Det rigtige svar kan markeres for at angive, at det valgte svar er korrekt. Dette kan bruges til vurdering af spørgeskemaet.  
8. Skriv en værdi i feltet Svar.
    * Fortsæt med at oprette valgmuligheder for svar til svarsamlingen.  
9. Klik på Ny.
10. Angiv et tal i feltet Point.
11. Skriv en værdi i feltet Svar.
12. Klik på Ny.
13. Angiv et tal i feltet Point.
14. Skriv en værdi i feltet Svar.
15. Klik på Ny.
16. Angiv et tal i feltet Point.
17. Skriv en værdi i feltet Svar.
18. Klik på Ny.
19. Angiv et tal i feltet Point.
20. Skriv en værdi i feltet Svar.
21. Luk siden.
22. Luk siden.

## <a name="create-the-question"></a>Opret spørgsmålet
1. Gå til Spørgeskema > Design > Spørgsmål.
2. Klik på Ny.
3. Brug feltet Type til at gruppere relaterede spørgsmål.
    * Du kan bruge inputtyper som afkrydsningsfelt, alternativknap eller kombinationsboks til lukkede spørgsmål.  
4. Vælg en indstilling i feltet Inputtype.
5. Indtast eller vælg en værdi i feltet Svarsamling.
6. Skriv en værdi i feltet Tekst.


