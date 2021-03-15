---
title: Konfigurere politikker for indkøbskategorihierarkier
description: Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc01793ee83444e5c7097021c19aeda80a132e6
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017083"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Konfigurere politikker for indkøbskategorihierarkier

[!include [banner](../../includes/banner.md)]

Brug denne fremgangsmåde til at oprette regler for bestilling af produkter i en kategori. Reglerne er defineret for en bestemt indkøbspolitik. Kategoriadgangspolitikreglen styrer, hvilke indkøbskategorier medarbejdere har adgang til, når de opretter en indkøbsrekvisition. Når der oprettes en indkøbsrekvisition, afgøres den indkøbspolitik og den regel for kategoriadgang, der skal anvendes, af den juridiske enhed og den driftsenhed, som medarbejderen tilhører. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne opgave vil typisk blive udført af en indkøbschef.


## <a name="find-the-procurement-policy"></a>Find politikken for indkøb
1. I Navigationsruden skal du gå til **Moduler > Indkøb og forsyning > Opsætning > Politikker > Indkøbspolitikker**.
2. Klik på linket i "Indkøbspolitikkens USMF"-politik. Det er den politik, som du vil føje en regel til. Det skal være en aktiv politik.  

## <a name="create-a-category-access-rule"></a>Oprette en regel for adgang til kategori
1. Udvid sektionen **Politikregler**.
2. I listen **Politikregeltype** skal du vælge **Politikregel for adgangskategori**. Hvis knappen **Opret politikregel** er nedtonet, skyldes det, at der allerede findes en aktiv politikregel for kategoriadgang. Kontrollér felterne **Ikrafttrædelse** og **Udløb** for at finde ud af, hvad reglen er, og markér den derefter, samt klik på **Træk regel tilbage**. Hvis knappen **Opret politikregel** er tilgængelig, skal du ikke gøre noget.  
3. Klik på **Opret politikregel**.
4. Angiv en dato og et klokkeslæt i feltet **Ikrafttrædelsesdato**. Tiden må ikke overlappe med en anden regel, der allerede er aktiv.  
5. Vælg en kategori, som reglen skal gælde for. Notér, hvilken kategori det er – du skal bruge den senere. Når du vælger en kategori, tilføjes den eller de tilhørende overordnede kategorier også på listen Valgte kategorier. Hvis reglen skal anvendes på alle underkategorier af den valgte kategori, skal du markere afkrydsningsfeltet **Medtag underkategorier**.
6. Klik på den højre pil for at føje dem til listen **Valgte kategorier**.  
4. Klik på **OK**. Hvis du angiver indstillingen **Medtag overordnet regel** til Ja, tildeles den politikregel, du definerer for en overordnet kategori, også til dens underordnede kategorier, hvis der ikke er defineret en politikregel for de underordnede kategorier.

## <a name="create-a-category-policy-rule"></a>Oprette en politikregel for kategori.
1. I listen **Politikregeltype** skal du vælge **Politikregel for kategori**. Hvis knappen **Opret politikregel** er nedtonet, skal du vælge den aktive politikregel og derefter klikke på **Træk regel tilbage**.  
2. Klik på **Opret politikregel**.
3. Angiv en dato og et klokkeslæt i feltet **Ikrafttrædelsesdato**.
4. Klik på **Tilføj**.
5. I feltet **Kategori** skal du vælge den samme kategori, du har brugt til **Regel for kategoriadgang**.
6. Vælg en indstilling i feltet **Kreditorvalg**. Vælg en regel, der skal styre, hvilken slags kreditorer der kan vælges til kategorien, når der oprettes indkøbsrekvisitioner.  
7. Klik på **Luk**. De politikregler, du har defineret, har været for indkøbsrekvisitionen af typen Forbrug. Hvis du vil definere politikker for indkøbsrekvisitioner af typen Opfyldning, skal du oprette en regel for politikregeltypen kaldet "Regel for adgang til genopfyldningskategori".  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]