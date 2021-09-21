---
title: Oprette et lukket spørgsmål
description: Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8758b74f9ce7c8687b7c2925ccd04cd512602db0
ms.sourcegitcommit: 8246ba3872a1f3eaa18c8bb1ba86d3c2142a6e10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/31/2021
ms.locfileid: "7465167"
---
# <a name="create-a-closed-ended-question"></a>Oprette et lukket spørgsmål

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Lukkede spørgsmål giver dig mulighed at angive muligheder, som svarpersonen kan vælge fra. Først skal du oprette en Svarsamling med svarene, derefter skal du oprette spørgsmålet, som bruger svarsamlingen. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-an-answer-group"></a>Opret en svarsamling
1. Gå til **Spørgeskema** > **Design** > **Svargrupper**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Svarsamling**.
4. Indtast en værdi i feltet **Beskrivelse**.
    * Du kan bruge funktionen Tilfældig til at placere svarene i en tilfældig rækkefølge, hver gang svarsamlingen bruges til et spørgsmål.  
5. Klik på **Svar**.
6. Klik på **Ny**.
    * Sekvensnummeret styrer den rækkefølge, som svarene vises i, medmindre Tilfældig vælges til svarsamlingen.  
    * Point kan overdrages til svar til brug i vurdering af spørgeskemaet.  
7. Angiv et tal i feltet **Point**.
    * Det rigtige svar kan markeres for at angive, at det valgte svar er korrekt. Dette kan bruges til vurdering af spørgeskemaet.  
8. Skriv en værdi i feltet **Svar**.
    * Fortsæt med at oprette valgmuligheder for svar til svarsamlingen.  
9. Klik på **Ny**.
10. Angiv et tal i feltet **Point**.
11. Skriv en værdi i feltet **Svar**.
12. Klik på **Ny**.
13. Angiv et tal i feltet **Point**.
14. Skriv en værdi i feltet **Svar**.
15. Klik på **Ny**.
16. Angiv et tal i feltet **Point**.
17. Skriv en værdi i feltet **Svar**.
18. Klik på **Ny**.
19. Angiv et tal i feltet **Point**.
20. Skriv en værdi i feltet **Svar**.
21. Luk siden.
22. Luk siden.

## <a name="create-the-question"></a>Opret spørgsmålet
1. Gå til **Spørgeskema** > **Design** > **Spørgsmål**.
2. Klik på **Ny**.
3. Brug feltet Type til at gruppere relaterede spørgsmål.
    * Du kan bruge inputtyper som afkrydsningsfelt, alternativknap eller kombinationsboks til lukkede spørgsmål.  
4. Vælg en indstilling i feltet **Inputtype**.
5. Indtast eller vælg en værdi i feltet **Svarsamling**.
6. I feltet **Tekst** skal du indtaste en værdi.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
