--- 
title: "Konfigurere politikker for indkøbskategorihierarkier"
description: "Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Konfigurere politikker for indkøbskategorihierarkier

[!include [task guide banner](../../includes/task-guide-banner.md)]

Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori. Reglerne er defineret for en bestemt indkøbspolitik. Kategoriadgangspolitikreglen styrer, hvilke indkøbskategorier medarbejdere har adgang til, når de opretter en indkøbsrekvisition. Når der oprettes en indkøbsrekvisition, afgøres den indkøbspolitik og den regel for kategoriadgang, der skal anvendes, af den juridiske enhed og den driftsenhed, som medarbejderen tilhører. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne opgave vil typisk blive udført af en indkøbschef.


## <a name="find-the-procurement-policy"></a>Find politikken for indkøb
1. Gå til Indkøb og forsyning > Konfiguration > Politikker > Indkøbspolitikker.
2. Klik på linket i indkøbspolitikkens USMF-politik.
    * Det er den politik, som du vil føje en regel til. Det skal være en aktiv politik.  

## <a name="create-a-category-access-rule"></a>Oprette en regel for adgang til kategori
1. Vælg reglen for adgang til kategori.
    * Hvis knappen Opret politikregel er nedtonet, skyldes det, at der allerede findes en aktiv politikregel for kategoriadgang. Kontrollér felterne Ikrafttrædelsesdato og Udløbsdato for at finde ud af, hvad reglen er, markér den derefter, og klik på Træk regel tilbage. Hvis knappen Opret politikregel er tilgængelig, skal du ikke gøre noget.  
2. Klik på Opret politikregel.
3. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
    * Tiden må ikke overlappe med en anden regel, der allerede er aktiv.  
    * Vælg en kategori, som reglen skal gælde for. Notér, hvilken kategori det er – du skal bruge den senere. Når du vælger en kategori, tilføjes den eller de tilhørende overordnede kategorier også på listen Valgte kategorier.  
    * Hvis reglen skal anvendes på alle underkategorier af den valgte kategori, skal du markere afkrydsningsfeltet Medtag underkategorier.  
4. Klik på Tilføj.
    * Hvis du angiver indstillingen Medtag overordnet regel til Ja, tildeles den politikregel, du definerer for en overordnet kategori, også til dens underordnede kategorier, hvis der ikke er defineret en politikregel for de underordnede kategorier.  
5. Klik på OK.

## <a name="create-a-category-policy-rule"></a>Oprette en politikregel for kategori.
1. Vælg reglen for kategori
    * Hvis knappen Opret politikregel er nedtonet, skal du vælge den aktive politikregel og derefter klikke på Træk regel tilbage.  
2. Klik på Opret politikregel.
3. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
4. Klik på Tilføj.
5. Vælg den samme kategori, du har brugt til reglen for kategoriadgang.
6. Vælg en indstilling i feltet Kreditorvalg.
    * Vælg en regel, der skal styre, hvilken slags kreditorer der kan vælges til kategorien, når der oprettes indkøbsrekvisitioner.  
7. Klik på Luk.
    * De politikregler, du har defineret, har været for indkøbsrekvisitionen af typen Forbrug. Hvis du vil definere politikker for indkøbsrekvisitioner af typen Opfyldning, skal du oprette en regel for politikregeltypen kaldet "Regel for adgang til genopfyldningskategori".  


