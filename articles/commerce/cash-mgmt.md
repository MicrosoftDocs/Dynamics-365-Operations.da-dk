---
title: Likviditetsstyringsforbedringer
description: Dette emne beskriver likviditetsstyringsforbedringerne i POS for Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 28b034c9b2a2c7ae63b055338dea3aab4a3b86f2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021964"
---
# <a name="cash-management-improvements"></a>Likviditetsstyringsforbedringer

[!include [banner](includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Likviditetsstyring er en nøglefunktion for detailhandlere i fysiske butikker. Detailhandlere ønsker, at deres butikker har systemer, der kan hjælpe dem med at tilbyde en komplet sporbarhed og overvågning af kontanter og deres bevægelse på tværs af de forskellige kasseapparater og kasserere i en butik. De skal kunne afstemme eventuelle forskelle og placere ansvaret.


Microsoft Dynamics 365 Commerce indeholder funktioner til likviditetsstyring i POS-programmet. I de versioner af Retail, der er ældre end version 10.0.3, er funktionen til likviditetsstyring dog ikke robust nok til at give en komplet sporbarhed af kontanters bevægelser i butikker. Selvom detailhandlere kan afstemme kontanter i en butik, kan de ikke præcist placere et ansvar i tilfælde af kontantuoverensstemmelser.


I Retail version 10.0.3 og nyere versioner vil detailhandlerne få mulighed for at spore håndteringen af kontanter. Som en del af denne sporbarhed vil detailhandlerne kunne definere pengeskabe, oprette tosidede kontanttransaktioner og afstemme likviditetsstyringsposteringer.

## <a name="set-up-traceability-and-define-safes"></a>Konfigurere sporbarhed og definere pengeskabe

Når du vil konfigurere de nye funktioner til likviditetsstyring, skal du udføre disse trin for at konfigurere funktionalitetsprofilen for butikker.

1. Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**, og vælg en funktionalitetsprofil, der er knyttet til de butikker, hvor du vil gøre forbedringer af likviditetsstyring tilgængelige.
2. I oversigtspanelet **Funktioner** i funktionalitetsprofilen under **Avanceret likviditetsstyring** skal du vælge **Ja** i indstillingen **Aktiver kontantsporing**.
3. Når du vil konfigurere pengeskabe, skal du gå til **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker** og vælge en butik.
4. På siden **Butikker** i handlingsruden skal du under fanen **Opsætning** vælge **Pengeskabe** i gruppen **Konfigurer**. Ved hjælp af denne indstilling kan du definere og vedligeholde flere pengeskabe for en butik.
4. Før du kan bruge funktionerne, skal du køre distributionsplanjobbet **1070 kanalkonfiguration** for at synkronisere disse konfigurationer med kanaldatabasen.

## <a name="additional-cash-management-changes"></a>Yderligere ændringer i likviditetsstyring

Retail version 10.0.3 og nyere indeholder også følgende egenskaber, der er relateret til kontanttransaktioner:

- En bruger, der bliver bedt om at "angive startbeløb", skal angive kilden til kontanter. Brugeren kan søge efter de tilgængelige pengeskabe, der er defineret i butikken, og vælge det pengeskab, som kontanterne skal tages fra, så de kan placeres i kasseapparatet.
- En bruger, der udfører handlingen "fjernelse af betalingsmiddel", bliver bedt om at vælge den transaktion, som handlingen udføres mod, på en liste med åbne "kassebeholdninger". Hvis den tilsvarende kassebeholdning ikke findes i systemet, kan brugeren oprette en ikke-tilknyttet transaktion til fjernelse af betalingsmiddel.
- Ved en "kassebeholdningshandling" bliver brugeren bedt om at vælge den transaktion, som kassebeholdningshandlingen udføres mod, på en liste med åbne transaktioner til "fjernelse af betalingsmiddel". Hvis den tilsvarende fjernelse af betalingsmiddel ikke findes i systemet, kan brugeren oprette en ikke-tilknyttet kassebeholdningstransaktion.
- En bruger, der foretager en "deponering til pengeskabet", bliver bedt om at vælge det pengeskab, hvor kontanterne skal deponeres.
- For pengeskabe, der er defineret i en butik, kan brugere administrere handlinger, f.eks. angive startbeløb, angive en kassebeholdning, fjerne et betalingsmiddel og foretage en indsættelse i banken.
- For de brugere, der har de relevante brugerrettigheder, viser operationerne "Administrer skift" kassesaldi for aktive og afbrudte skift og skift, der er lukket uden kontrol.
- Hvis du vil afstemme kontanttransaktionerne inden for et skift eller på tværs af flere skift, skal du vælge det skift, der skal afstemmes, og derefter vælge **Afstem**. Den visning, der åbnes, viser listen over afstemte og ikke-afstemte transaktioner under separate faner. I denne visning kan brugerne enten vælge ikke-afstemte afstemmer og afstemme dem eller vælge tidligere afstemte transaktioner og fjerne afstemningen af dem.
- Under afstemningen skal brugeren angive en beskrivelse af årsagen til den manglende balance, hvis den valgte transaktion ikke stemmer. Brugerne kan vælge en enkelt transaktion og afstemme den med den relevante årsagsbeskrivelse efter behov.
- Brugerne kan fortsætte med at afstemme og fjerne afstemning af transaktioner, indtil skiftet afsluttes. Når et skift er afsluttet, kan transaktionerne ikke være ikke-afstemte.
- Når en bruger vælger at afslutte et skift, validerer Commerce, at der ikke er nogen ikke-afstemte transaktioner til likviditetsstyring i skiftet. Brugerne kan ikke afslutte et skift, hvis der er ikke-afstemte transaktioner.
