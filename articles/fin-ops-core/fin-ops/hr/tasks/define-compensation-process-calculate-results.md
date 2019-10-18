---
title: Definere kompensationsproces og beregne resultater
description: Kompensationsprocesser bruges til at fastlægge nye kompensationsbeløb og bonusser for medarbejdere, der er tilmeldt faste og variable kompensationsstrukturer.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0825c80e43baf0803552f7051dca5ee79dbe521e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177082"
---
# <a name="define-compensation-process-and-calculate-results"></a>Definere kompensationsproces og beregne resultater

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kompensationsprocesser bruges til at fastlægge nye kompensationsbeløb og bonusser for medarbejdere, der er tilmeldt faste og variable kompensationsstrukturer. Kompensationsprocesser kan køres flere gange for at udføre "what-if"-analyser, som kontrollerer, at alle ændringer og indstillinger er korrekte. Denne procedure opretter en kompensationsproces, kører processen og viser resultaterne. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-compensation-process"></a>Oprette en kompensationsproces
1. Gå til Personale > Kompensation > Proces > Kompensationsprocesser.
2. Klik på Ny.
3. Skriv en værdi i feltet Proces.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Procestype.
    * En cyklus angiver den tidsperiode, der er evalueret for at fastlægge kompensation. I vurderingen indgår, hvilke stillinger der var besat af medarbejdere, hvilke performance-rangeringer, der skal medtages, beregning af procentdelen af tid, som medarbejderen var ansat under cyklussen, og meget mere. Et eksempel på en cyklusstartdato kan være den første dag i det seneste regnskabsår.  
6. Angiv en dato i feltet Start på forløb.
    * Cyklussens slutdato er vigtig, fordi det er den dato, der bruges til at bestemme, hvilke medarbejdere der var aktivt beskæftiget og tilmeldt en eller flere kompensationsplaner.  
7. Angiv en dato i feltet Afslutning på forløb.
    * Den aktive transaktionsdato er den dato, hvor de nye kompensationssatser skal træde i kraft. Mange virksomheder omfatter et par måneder mellem deres cyklusafslutning og det tidspunkt, hvor nye kompensationssatser træder i kraft. Den ekstra tid bruges til behandling og gennemgang af den nye kompensation.  
8. Angiv en dato i feltet Aktiv-dato for transaktion.
    * Den tidsbestemte dato bruges til variable kompensationsstrukturer, der bestemmer en medarbejders bonusbeløb baseret på deres kompensationssats på dette tidspunkt.  
    * Ansættelsesdato med fast lønsats bruges med planer for fast kompensation med ansættelsesreglen Procent.  Medarbejdere, der ansættes mellem cyklusstarten og ansættelsesdatoen med fast lønsats, modtager 100 % af deres beregnede kompensationsstigning i stedet for vurderet procentdel.  
9. Angiv en dato i feltet Fast løn iht. vurderet ansættelsesdato.
    * Korrekturens deadline er den dato, hvor alle procesresultater skal være revideret, så de kan indlæses i en medarbejders kompensationspost før den aktive posteringsdato. Feltet er kun til orientering.  
10. Angiv en dato i feltet Gennemse deadline.
11. Klik på Gem.

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a>Konfigurere kompensationsplaner og handlinger for en kompensationsproces
1. Klik på Opsætning.
    * Opsætningssiden bruges til at vælge, hvilke strukturer der skal behandles som en del af denne kompensationsproces, samt hvilke handlinger bør træffes for hver enkelt struktur.  
2. Indtast eller vælg en værdi i feltet Plan.
3. Klik på Gem.
4. Klik på Tilføj.
5. Vælg en handling af typen Egenkapital i feltet Handling.
6. Klik på Tilføj.
7. Vælg en handling af typen Merit i feltet Handling.
    * Kompensationshandlinger kan være "sammenkædet" vha. feltet Brug tidligere resultat for at angive, om den valgte handling skal bruge medarbejdergrundlønnen eller resultatet af den foregående handling som udgangspunkt for beregning af denne handling.  
8. Vælg Ja i feltet Brug tidligere resultat.
9. Klik på Tilføj.
10. Vælg en handling af typen Generel i feltet Handling.
    * Forskellige kompensationsaktionstyper aktiverer forskellige felter. For en generel kompensationsaktionstype kan der angives en stigningsprocent eller stigningsbeløb.  
11. Vælg indstillingen Vælg stigningsbeløb.
12. Angiv et tal i feltet Stigningsbeløb.
13. Klik på Tilføj.
14. Vælg en handling af typen Forfremmelse i feltet Handling.
    * Aktionstyperne Forfremmelse og Anden niveauændring gør det muligt for brugere at foretage manuelle reguleringer af medarbejderkompensation. Anbefalinger kan aktiveres for disse aktionstyper, samt andre aktionstyper, så du kan angive en ny anbefalet kompensationsværdi for en medarbejder.  
15. Klik på Tilføj.
16. Vælg en indstilling i feltet Type.
    * Faste og variable kompensationsstrukturer kan køres i den samme kompensationsproces.  
17. Indtast eller vælg en værdi i feltet Plan.
    * Brug afkrydsningsfelt Aktiver løn for performance til at bestemme, om faste og variable kompensationsbeløb skal reguleres baseret på medarbejderens performancevurdering.  
    * Regulering kan tilsidesættes for variable kompensationsstrukturer.  
18. Klik på Gem.
19. Klik på Tilføj.
20. Luk siden.

## <a name="run-the-compensation-process"></a>Kør kompensationsprocessen
1. Klik på Kør proces.
    * Med kontrolelementet Vis resultater af behandling kan du se behandlingsmeddelelser for hele kompensationsprocessen, når behandlingen er afsluttet.  
2. Vælg Ja i feltet Vis resultater af behandling.
3. Klik på OK.

## <a name="view-the-results"></a>Få vist resultaterne
1. Klik på Procesresultater.
2. Klik på Medarbejderresultater.
3. Find og vælg den ønskede post på listen.
4. Udvid sektionen Fast løn.
    * Udvid oversigtspanelet for at få vist resultaterne af processen. Hvis Aktiver anbefalinger er markeret for en kompensationsaktion, aktiveres anbefalingsfelterne for aktionen.  
5. Find og vælg den ønskede post på listen.
    * Resultaterne for en enkelt medarbejder kan ses ved at klikke på knappen Vis resultater.  
    * Du kan overskrive det beregnede kompensationsbeløb ved at justere procentdelen eller stigningsbeløbet i Anbefaling-felterne.  
6. Angiv et tal i feltet for anbefalet procent.
7. Find og vælg den ønskede post på listen.
8. Angiv et tal i feltet for anbefalet procent.
    * Genberegning kan bruges til at ignorere alle ændringer til den eksisterende post og generere et nyt kompensationsresultat for den valgte medarbejder.  
    * Når alle ændringer er udført for en medarbejder, kan du ændre status til Godkendt.  
9. Klik på Skift status.
10. Klik på Godkendt.
    * Når posten er blevet godkendt, kan den indlæses i medarbejderens officielle kompensationspost. Den nye kompensation træder i kraft på den posteringsdato, der blev angivet i kompensationsprocessen.  

