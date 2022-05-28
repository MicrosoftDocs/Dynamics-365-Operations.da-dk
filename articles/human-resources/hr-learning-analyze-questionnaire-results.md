---
title: Analysere spørgeskemaresultater
description: Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692913"
---
# <a name="analyzing-questionnaire-results"></a>Analysere spørgeskemaresultater


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Spørgeskemastatistik kan bruges til at beregne gennemsnit, totaler og procentdele baseret på en række demografiske data. Du begynder denne procedure ved at gå til **Spørgeskema** > **Vis og analysér resultater** > **Spørgeskemastatistik**. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-a-questionnaire-statistics-record"></a>Opret en Spørgeskemastatistikpost
1. Gå til **Spørgeskemastatistik**.
2. Klik på **Ny**.
3. Markér den valgte række på listen.
4. Skriv en værdi i feltet **Statistik**.
5. Indtast en værdi i feltet **Beskrivelse**.
6. Klik på rullelisten i feltet **Spørgeskema** for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Klik på fanen **Generelt**.
    * Vælg, hvis du vil medtage anonyme resultater eller resultater fra arbejdere, kontaktpersoner og ansøgere.  
9. Markér eller fjern markeringen i afkrydsningsfeltet **Arbejder**.
    * Hvis du have vist resultaterne efter anciennitet eller alder, kan du angive de intervaller, som du vil bruge til at gruppere resultaterne.  
    * Angiv 5 for aldersintervallet for at gruppere resultaterne, så de er baseret på aldersintervaller a fem år.  
10. Angiv et tal i feltet **Alder**.
    * Vælg, hvis du vil køre beregningen mod hele spørgeskemaet for hver resultatgruppe, for hvert spørgsmål eller for hver spørgsmålsrække.  
    * Vælg, hvordan du vil gruppere resultaterne.  
    * Hvis du f.eks. beregner det gennemsnitlige antal point pr. spørgsmål, kan du se de spørgsmål grupperet efter Resultatgruppe.  
    * Markér de data, du vil basere beregningen på.  
    * Hvis du f.eks. vil se den gennemsnitlige procentdel modtaget på spørgeskemaet på tværs af dine arbejderne i forhold til det gennemsnitlige antal point, der er opnået på tværs af dine medarbejdere.  
11. Klik på fanen **Område**.
    * Du kan bruge intervaller til at indsnævre resultatsættet til kun dem, der opfylder kriterierne for området.  
12. Klik på fanen **Gruppering pr.**
    * Brug Grupperinger til at finde ud af, hvordan resultatet skal vises.  
    * Gruppér f.eks resultaterne først efter køn, derpå efter alder.  
13. Find og vælg den ønskede post på listen.
    * Flyt grupperinger ind på den **markerede** side, og placer dem i den ønskede rækkefølge.  

## <a name="execute-the-statistics-calculation"></a>Udfør statistikberegningen.
1. Klik på **Udfør**.
    * Vælg, hvilken beregningsfunktion du vil udføre på resultaterne.  
    * Du kan f.eks. beregne de gennemsnitlige procentsatser på tværs af spørgeskemaet for de valgte grupperinger eller det samlede antal point på tværs af resultatgrupper for de valgte grupperinger.  
2. Markér eller fjern markeringen i afkrydsningsfeltet **Slet tidligere søgninger**.
3. Klik på **OK**.

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>Få vist resultaterne af kørslen af spørgeskemastatistikken.
1. Klik på **Resultat**.
2. Klik på **Resultat**.
3. Luk siden.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
