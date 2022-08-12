---
title: Planlægning af efterspørgselsbaseret materialebehov (DDMRP)- oversigt
description: Denne artikel indeholder oplysninger om Efterspørgselsbaseret materialebehovsplanlægning (DDMRP), en planlægningsmetode, der er baseret på deling af udbud og efterspørgsel.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186691"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Planlægning af efterspørgselsbaseret materialebehov (DDMRP)- oversigt

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

I flere år har firmaer anvendt MRP (Material Requirements Planning) som et system til beregning af de materialer og komponenter, der kræves til fremstilling af et produkt. Forsyningskæderne er dog nu ændret. Dele har længere leveringstider, fordi de i stigende grad indkøbes fra webdele. Mange firmaer har derfor indberettet lagerføringer eller lagervarer, fordi de ikke ved, hvor meget der skal lagervarerne. Der sker også større udsving på markedet (undertiden forkert prognose), og kunder kræver produkter med kort leveringstid. Derfor er der mangel i forsyningskæden over hele verden. Desuden giver MRP-værktøjer ofte planlæggere tusindvis af handlinger, der skal udføre. Derfor er det svært at vide, hvad der skal fokuseres på. Løsningen på mange af disse problemer er ofte at skifte til DDMRP (Demand Driven Material Requirements Planning).

DDMRP er en planlægningsmetode, der er baseret på efterspørgsels- og efterspørgselsefterspørgsel. Denne nedpostering opnås ved at oprette nedposteringssted. For disse varer vedligeholdes buffers for at sikre, at den rette lagerbeholdning bevares. Når udbud og efterspørgsel afkobles, medvirker det til at forhindre, at "effekten", fordi variationen ikke er passeret gennem kæden. (Denne *bullwhip-effekt* refererer til, hvor lille efterspørgselsudsving på detailniveau kan medføre progressivt større efterspørgsel hos engros-, distributør-, producent- og råvareleverandørniveauerne). Hver buffer er beregnet til at dække den gennemsnitlige brug af en del og kan også justeres, så den dækker efterspørgselsbehovet.

DDMRP er dokumenteret som en værdifulde planlægningsmetode til variable miljøer, hvor kundetolerancetider er kortere end akkumulerede leveringstider.

## <a name="the-five-components-of-ddmrp"></a>De fem komponenter i DDMRP

DDMRP indeholder fem fortløbende komponenter (trin). De første tre komponenter definerer egentlig den indledende og væsentligste konfiguration af en efterspørgselsbaseret model til planlægning af materialebehov. De sidste to komponenter definerer den daglige drift af metoden.

1. **[Strategisk lagerplacering](ddmrp-inventory-positioning.md)** – Identificer afkoblingspunkter i forsyningskædenetværket. Det er specifikke punkt i forsyningskæden, hvor du placerede en lagerbuffer, som du vil overvåge og genopfylde.
2. **[Bufferprofiler og niveauer](ddmrp-buffer-profile-and-levels.md)** – Identificer bufferstørrelserne (minimumantal, maksimumantal og genbestillingspunkt) og genbestillingsantal for hvert mål.
3. **[Dynamiske bufferreguleringer](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Juster bufferniveauer baseret på forskellige driftsparametre eller planlagte fremtidige hændelser.
4. **[Efterspørgselsbaseret planlægning](ddmrp-planning.md)** – Generér leveringsordrer efter behov. Disse forsyningsordrer inkluderer produktionsordrer, indkøbsordrer og lageroverførselsordrer.
5. **[Meget forskellige og synlige udførelser](ddmrp-visual-and-collaborative-execution.md)** – Kør leveringsordrerne ved hjælp af visualisering.

DDMRP bruges typisk af producenter af styklister med flere niveauer. Det kan dog også anvendes til distributions- og detailnetværk.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP i Dynamics 365 Supply Chain Management

DDMRP følger med Microsoft Dynamics 365 Supply Chain Management kræver ingen yderligere licensgebyrer. I Supply Chain Management er funktionen DDMRP føjet til det eksisterende modulet **Behovsplanlægning**. Det kræver dog, at du bruger tilføjelsesprogrammet Planlægningsoptimering. 

DDMRP er integreret med de eksisterende planlægningsopsætninger i Supply Chain Management og bruges sammen med disse opsætninger til at nå frem til den korrekte planlægningskonfiguration til din virksomhed. Det styres af en ny disponeringskode, der er helt forskellig fra periode, min./maks., behov osv. Det er ikke et nyt modul, og den erstatter ikke eksisterende planlægningsfunktionalitet. Det giver dig dog flere funktioner at bruge.
