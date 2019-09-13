---
title: Konfigurere vareomfordeling for kort plukning
description: Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916747"
---
# <a name="set-up-short-picking-item-reallocation"></a>Konfigurere vareomfordeling for kort plukning

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du giver lagermedarbejderne mulighed for hurtigt at finde alternative lokaliteter, hvis der ikke er tilstrækkeligt lager på den lokalitet, der er blevet henvist til. Det er muligt at bruge en automatisk omfordelingsproces, som bruger lokalitetsbestemmelser til at hente varerne, hvis de er tilgængelige på en anden lokalitet. Når manuel omfordeling bruges, vises der også en liste over lokaliteter med det disponible på mobilenheden, så lagermedarbejderen kan vælge, hvilken lokalitet lageret skal bruges fra. Du kan bruge denne procedure i USMF-demodatafirmaet. Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.


## <a name="set-up-work-exceptions"></a>Konfigurer arbejdsundtagelser
1. I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejde > Arbejdsundtagelser**.
2. Klik på **Ny**. Det er muligt at definere flere undtagelser for arbejde med forskellige politikker for omfordeling af varer for at give lagermedarbejderen mulighed for at vælge én baseret på behov i den leverance, som de behandler.  
3. Indtast en værdi i feltet **Kode for arbejdsundtagelse**. Giv undtagelsen for arbejde en titel for at angive, hvad den skal bruges til. Det kan f.eks. være Vejledning til korte pluk.  
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg 'Kort pluk' i typefeltet **Undtagelse**.
6. Marker afkrydsningsfeltet **Reguler lager**. Denne indstilling betyder, at lageret automatisk reguleres til 0 på den placering, hvor der er udført korte pluk.  
7. Indtast eller vælg en værdi i feltet **Standardkode for reguleringstype**. I USMF kan du for eksempel vælge 'Fjern Res Adj Out'.  
8. Vælg 'Manuelt' i feltet **Vareomfordeling**. Hvis du vælger Manuel eller Automatisk og manuel, skal lagermedarbejderen have mulighed for at bruge manuel omfordeling.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurer en arbejder til at bruge manuel vareomfordeling
1. Luk siden.
2. I **Navigationsrude** skal du gå til **Lokationsstyring > Opsætning > Arbejder**.
3. Klik på **Rediger**.
4. Vælg arbejder 24 på listen.
5. Udvid oversigtspanelet **Arbejde**.
6. Vælg 'Ja' i feltet **Tillad manuel vareomfordeling**.

