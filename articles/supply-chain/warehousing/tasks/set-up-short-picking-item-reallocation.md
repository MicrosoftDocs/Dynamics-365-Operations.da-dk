---
title: Konfigurere vareomfordeling for kort plukning
description: Dette emner viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokation, der er blevet henvist til.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8baf846d65e6fefe9ca575b5af5a2dbceac666
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976882"
---
# <a name="set-up-short-picking-item-reallocation"></a>Konfigurere vareomfordeling for kort plukning

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokationer, hvis der ikke er tilstrækkeligt lager på den lokation, der er blevet henvist til. 

Omfordelingsprocessen styres af en **Arbejdsundtagelse** og bruges af **lagermedarbejderen.**

Det er muligt at bruge automatiske, manuelle eller begge omfordelingsprocesser:

- Automatisk omfordeling – lokationsvejledninger bruges til at bestemme, om varerne er tilgængelige på en anden lokation. Hvis det er muligt, opdateres arbejdet, og lagerbrugeren dirigeres videre til den alternative lokation.
- Manuel omfordeling – gør det muligt for lagerbrugeren at vælge mellem en eller flere lokationer med ikke-reserverede antal varer. 
- Automatisk og manuel – hvis systemet ikke kan udføre en automatisk omfordeling, og der er tilgængelige lokationer med ikke-reserverede antal, vil brugeren blive bedt om at vælge en lokalitet.

## <a name="set-up-work-exceptions"></a>Konfigurer arbejdsundtagelser
Det er muligt at definere flere undtagelser for arbejde med forskellige politikker for omfordeling af varer for at give lagermedarbejderen mulighed for at vælge én baseret på behov i den leverance, som de behandler.

Demodatafirmaet USMF bruges til at oprette denne procedure.

1. I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejde > Arbejdsundtagelser**.
2. Klik på **Ny** 
3. Indtast en værdi i feltet **Kode for arbejdsundtagelse**. Dette vil være titlen på denne undtagelse. Det kan f.eks. være Vejledning til korte pluk.
4. Indtast en værdi i feltet **Beskrivelse**. Dette er en kort beskrivelse af brugen af denne undtagelse. Elementet Kort pluk er f. eks. ikke tilgængelig.
5. Vælg **Kort pluk** i feltet **Undtagelsestype**.
6. Marker afkrydsningsfeltet **Reguler lager**. Hvis indstillingen er valg, reguleres lageret automatisk til 0 på den lokation, hvor der er udført korte pluk.
7. Indtast eller vælg en værdi i feltet **Standardkode for reguleringstype**. I USMF kan du f.eks. vælge **Fjern Res Adj Out**. Hver reguleringstypekode indeholder fire karakteristika: navn, beskrivelse, lagerkladdenavn og **Fjern reservationer**. Hvis **Fjern reservationer** er aktiveret, vil reservationerne for ordrelinjer med kort pluk blive fjernet.  
8. Vælg en værdi i feltet **Vareomfordeling** som f.eks. Manuel. Hvis du vælger Manuel eller Automatisk og manuel, skal lagermedarbejderen have mulighed for at bruge manuel omfordeling.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurer en arbejder til at bruge manuel vareomfordeling

Demodatafirmaet USMF bruges til at oprette denne procedure.

1. Luk siden.
2. I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejder**.
3. Klik på **Rediger**.
4. Vælg arbejder på listen. F.eks. Julia Funderburk.
5. Udvid oversigtspanelet **Brugere**.
6. Vælg et **bruger-id** på listen. For eksempel 24.
7. Udvid oversigtspanelet **Arbejde**.
8. Vælg **Ja** i feltet **Tillad manuel vareomfordeling**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]