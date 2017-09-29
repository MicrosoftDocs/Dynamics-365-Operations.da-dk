--- 
title: "Analysere spørgeskemaresultater"
description: "Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 353faa30ba37c077479afd985b8808fcdbdcaae6
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="analyze-questionnaire-results"></a>Analysere spørgeskemaresultater

[!include[task guide banner](../../includes/task-guide-banner.md)]

Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data. Du begynder denne procedure ved at gå til Spørgeskema > Vis og analysér resultater > Spørgeskemastatistik. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Opret en Spørgeskemastatistikpost
1. Gå til Spørgeskemastatistik.
2. Klik på Ny.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet Statistik.
5. Indtast en værdi i feltet Beskrivelse.
6. Klik på rullelisten i feltet Spørgeskema for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Klik på fanen Generelt.
    * Vælg, hvis du vil medtage anonyme resultater eller resultater fra arbejdere, kontaktpersoner og ansøgere.  
9. Markér eller fjern markeringen i afkrydsningsfeltet Arbejder.
    * Hvis du have vist resultaterne efter anciennitet eller alder, kan du angive de intervaller, som du vil bruge til at gruppere resultaterne.  
    * Angiv 5 for aldersintervallet for at gruppere resultaterne, så de er baseret på aldersintervaller a fem år.  
10. Angiv et tal i feltet Alder.
    * Vælg, hvis du vil køre beregningen mod hele spørgeskemaet for hver resultatgruppe, for hvert spørgsmål eller for hver spørgsmålsrække.  
    * Vælg, hvordan du vil gruppere resultaterne.  
    * Hvis du f.eks. beregner det gennemsnitlige antal point pr. spørgsmål, kan du se de spørgsmål grupperet efter Resultatgruppe.  
    * Markér de data, du vil basere beregningen på.  
    * Hvis du f.eks. vil se den gennemsnitlige procentdel modtaget på spørgeskemaet på tværs af dine arbejderne i forhold til det gennemsnitlige antal point, der er opnået på tværs af dine medarbejdere.  
11. Klik på fanen Område.
    * Du kan bruge intervaller til at indsnævre resultatsættet til kun dem, der opfylder kriterierne for området.  
12. Klik på fanen Gruppering pr.
    * Brug Grupperinger til at finde ud af, hvordan resultatet skal vises.  
    * Gruppér f.eks resultaterne først efter køn, derpå efter alder.  
13. Find og vælg den ønskede post på listen.
    * Flyt grupperinger ind på den markerede side, og placer dem i den ønskede rækkefølge.  

## <a name="execute-the-statistics-calculation"></a>Udfør statistikberegningen.
1. Klik på Udfør.
    * Vælg, hvilken beregningsfunktion du vil udføre på resultaterne.  
    * Du kan f.eks. beregne de gennemsnitlige procentsatser på tværs af spørgeskemaet for de valgte grupperinger eller det samlede antal point på tværs af resultatgrupper for de valgte grupperinger.  
2. Markér eller fjern markeringen i afkrydsningsfeltet Slet tidligere søgninger.
3. Klik på OK.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Få vist resultaterne af kørslen af spørgeskemastatistikken.
1. Klik på Resultat.
2. Klik på Resultat.
3. Luk siden.

