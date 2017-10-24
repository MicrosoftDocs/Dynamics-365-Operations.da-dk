---
title: Oversigt over styring af arbejdskraft
description: "Dette emne beskriver, hvordan du kan bruge tjenesten styring af arbejdskraft til at drage fordel af de velkendte POS-klienter, Modern POS og Cloud POS, så butikschefer nemt kan administrere deres personale."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Oversigt over styring af arbejdskraft

[!include[banner](includes/banner.md)]
    
Tjenesten Styring af arbejdskraft drager fordel af de velkendte POS-klienter, Modern POS og Cloud POS, så butikschefer nemt kan administrere deres personale. Tjenesten Styring af arbejdskraft bruger udvidelsesstrukturen til at hente de relevante pakker i POS. Disse pakker hentes, når POS lukkes og genåbnes. Når Microsoft udgiver nye funktioner til Styring af arbejdskraft, skal POS-programmet derfor lukkes og genåbnes.

Ved hjælp af denne tjeneste kan butikschefer nemt at oprette og udgive ugentlige arbejdsplaner for deres butikker. Medarbejderne i butikken kan derefter hurtigt få vist deres egne tidsplaner og tidsplanen for deres kolleger. På denne måde kan de få at vide, hvem de skal arbejde sammen med i de tildelte skiftehold. Medarbejderne i butikken kan også oprette anmodninger om fravær, bytte af skift og tilbud om skift. Alle disse anmodninger udløser en defineret arbejdsgang.

Under et skift kan medarbejderne i butikken drage fordel af den komme- og gå-funktion, der er indbygget i POS-klienterne. Dataene sendes derefter til hovedkontoret til lønudbetaling. Funktionen komme- og gå-registrering er en eksisterende egenskab på POS. Du kan finde yderligere oplysninger om opsætning og understøttede scenarier i [Komme- og gå-tidspunkt](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Understøttede scenarier
Dette afsnit indeholder flere oplysninger om de understøttede scenarier.

- **Oprette og udgive tidsplaner** – Tjenesten Styring af arbejdskraft bruger POS-rettigheder, der er konfigureret i hovedkontoret til at bestemme, om en medarbejder har rettigheder som butikschef. Det er kun butikschefer, der kan oprette og udgive tidsplaner ved hjælp af handlingen Administration af tidsplaner. De kan hurtigt oprette en tidsplan ved at kopiere og indsætte et eksisterende arbejdsskift fra én medarbejder til en anden medarbejder. De kan også oprette en tidsplan ved at importere tidsplanen fra en foregående uge til den aktuelle uge.

    Hvis en tidsplan ikke er udgivet, er den i kladdetilstand, og den ser anderledes ud end en tidsplan, der er udgivet. Butikschefer kan udgive en tidsplan ved at klikke på knappen **Udgiv** for en given uge. Når planen er udgivet for en uge, udgives eventuelle ændringer automatisk. Eksempler på ændringer omfatter tilføjelse og sletning af arbejdsskift eller fravær eller redigeringer af arbejdsskift eller fravær. Medarbejderne i butikken kan kun få vist tidsplaner, der er udgivet til forskellige uger.
    
- **Oprette og godkende anmodninger** – Medarbejdere i butikken kan oprette tre typer af anmodning:

    - Anmodning om fravær
    - Anmode om bytte af skift
    - Anmode om tilbud om skift

    Disse anmodninger kan oprettes ved hjælp af handlingen Planlægning af anmodninger. Hver anmodning følger en defineret arbejdsgang, og medarbejderne kan nemt se den aktuelle status for deres anmodninger.
    
    Anmodninger om fravær sendes automatisk til butikschefen til godkendelse. Hvis der er flere butikschefer, kan alle chefer få vist en given anmodning, men kun én chef kan godkende eller afvise den. Fraværstyper konfigureres i hovedkontoret ved hjælp af siden **Orlovs- og fraværstyper** i modulet **Retail**. Når butikschefen godkender eller afviser en anmodning, flyttes det til fanen **Historik** for handlingen Planlægning af anmodninger.
    
    En anmodning om skiftbytte eller skifttilbud sendes først til den medarbejder, som anmodningen er sendt til. Butikschefen kan kun få vist anmodningen, når denne medarbejder har godkendt den. Hvis medarbejderen afviser anmodningen om skiftbytte eller skifttilbud kan chefen ikke se det. Den medarbejder, der oprettede anmodningen, kan også annullere den, før chefen godkender eller afviser den.

- **Vis de aktive butiksmedarbejdere i tidsplanvisningen** – Når en medarbejder føjes til en butik, f.eks. ved at vedkommende knyttes til butikkens adressekartotek over medarbejdere, bliver medarbejderen tilgængelig for planlægning i tjenesten Styring af arbejdskraft. Et tilbagevendende batchjob, der hedder **Behandl arbejderdata til workforce management**, køres i hovedkontoret. Dette job forbereder de tilknytninger af butiksmedarbejder, der skal sendes til Common Data Service.

    Den samme proces bruges, når en medarbejder fjernes fra en butik. Dog vises den medarbejder, der fjernes, stadig i tidligere, indeværende og fremtidige uger, hvis den pågældende medarbejder er tildelt et aktivt skiftehold eller fravær. Medmindre disse arbejdsskift og fravær slettes, vises den fjernede medarbejder derfor stadig for disse uger.

