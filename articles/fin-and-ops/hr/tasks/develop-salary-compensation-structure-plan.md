--- 
title: "Udarbejde løn-/kompensationsstrukturer og -planer"
description: "Denne opgaveguide fører dig gennem processen med at oprette en fast lønstruktur og sætte medarbejdere i stand til at blive tilmeldt strukturen via berettigelsesregler."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0514cd485c8fa0026390a22be350ff23933afd7b
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="develop-salarycompensation-structures-and-plans"></a>Udarbejde løn-/kompensationsstrukturer og -planer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide fører dig gennem processen med at oprette en fast lønstruktur og sætte medarbejdere i stand til at blive tilmeldt strukturen via berettigelsesregler. Demodatafirmaet, der bruges til at oprette denne opgave, er USMF, og opgaven er beregnet til ledere for kompensation og frynsegoder.


## <a name="create-fixed-compensation-plan"></a>Oprette fast lønstruktur
1. Klik på Kompensationsstyring.
2. Klik på Faste lønstukturer.
3. Klik på Ny.
4. Skriv en værdi i feltet Plan.
5. Skriv en værdi i feltet Beskrivelse.
6. Angiv en dato i feltet Ikrafttrædelsesdato.
7. Vælg, om strukturen med fast løn er en plan af typen Omfang, Klasse eller Trin.
8. Afkrydsningsfeltet Anbefaling tilladt fungerer som standardværdi for alle handlinger, der er føjet til denne plan i en proceshændelse.  Ved at tillade anbefalinger kan du tilsidesætte det beregnede aftalebeløb ved behandling af kompensation.
9. Tolerancen for uden for ramme giver dig mulighed for at angive, hvordan du vil håndtere kompensationsbeløb, der falder uden for den angivne lønstrukturramme på det givne niveau.  En tolerance på Ingen for uden for ramme tillader brug af et hvilket som helst kompensationsbeløb.  Tolerancen Blød advarer brugeren, hvis kompensationsbeløbet er mindre end minimumbeløbet i referencepunktet for det pågældende niveau eller større end maksimumbeløbet for det pågældende niveau. Brugeren kan ignorere advarslen og fortsætte.  Tolerancen Hård genererer en fejl, hvis en medarbejders løn er angivet uden for minimale og maksimale referencepunkter for niveauet og justerer automatisk medarbejderens løn, så den ligger inden for rammen.
10. Feltet Ansættelsesregel bruges, når en kompensationsproceshændelse køres for at beregne en medarbejders løn.  Ansættelsesreglen Procent beregner en forholdsmæssig stigning for den tid, arbejderen har været ansat i cyklussen.
11. Skriv en værdi i feltet Valuta.
12. Indtast eller vælg en værdi i feltet Konvertering af lønsats.
13. Udvid sektionen Rammeudnyttelsesmatrix.
    * Du kan eventuelt tilføje poster for rammeudnyttelse for at få medarbejdere til deres middelpunkt hurtigere og gøre det langsommere for dem at nå maksimum for deres ramme.  
14. På dette tidspunkt skal du gemme den faste lønstruktur for at aktivere knappen Opsæt kompensation og fortsætte med at definere lønstrukturen for planen.  Klik på Gem.
15. Klik på Konfigurer kompensation.
    * Der er tre måder til at oprette en kompensationsstruktur på. 1: Opret en helt ny struktur ved at vælge et sæt referencepunkter og tilføje niveauer for at oprette din egen struktur. 2: Kopiér kompensationsstruktur fra en eksisterende plan som udgangspunkt, og tilpas den til den nye plan. 3: Vælg et eksisterende kompensationsgitter. Hvis kompensationsgitteret bruges allerede af en anden plan, afspejles eventuelle ændringer af gitteret også i anden plan.  
16. Markér indstillingen Opret ny fra eksisterende kompensationsmatrix.
17. Indtast eller vælg en værdi i feltet Kopier fra gitter.
    * Du kan eventuelt ændre navnet på det nye kompensationsgitter, der oprettes som en kopi af det valgte gitter.  
18. Klik på OK.
19. Klik på Masseændring.
    * Masseændring gør det muligt at opretholde kompensationsbeløb for matrixen ved at anvende en stigning i procent eller fladt beløb på ét eller flere niveauer og/eller referencepunkter.  
20. Indtast et tal i feltet Justeringsbeløb.
21. Markér eller fjern markeringen af alle rækker på listen.
22. Klik på Anvend på gitter.
23. Luk siden.
    * Når en kompensationsstruktur er blevet oprettet eller valgt, kan du vælge, hvilke referencepunkter der skal bruges som referencepunkt for den faste lønstruktur.  Referencepunktet bruges til at beregne kompensationsforholdet for en medarbejder.  
24. Indtast eller vælg en værdi i feltet Referencepunkt.
25. Luk siden.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Opret en berettigelsesregel for den nye faste lønstruktur.
    * Den nye faste lønstruktur kan ikke tildeles en medarbejder, før der er defineret berettigelsesregler for strukturen.  
1. Klik på Berettigelsesregler.
2. Klik på Ny.
3. Skriv en værdi i feltet Berettigelse.
4. Skriv en værdi i feltet Beskrivelse.
5. Angiv en dato i feltet Ikrafttrædelsesdato.
    * Berettigelsesregler bruges for både gælder for både faste og variable lønstrukturer.  Vælg i feltet Type, hvilken type struktur dette sæt berettigelsesregler er beregnet til.  
6. Indtast eller vælg en værdi i feltet Plan.
    * Vælg de kriterier, en medarbejder skal opfylde for at være berettiget til lønstrukturen. Kriterier kan omfatte en afdeling, fagforening, lokalitet (kompensationsområde), job, funktion, jobtype eller kompensationsniveau. Medarbejderen skal opfylde alle angivne kriterier for at være berettiget til lønstrukturen. Er der ikke angivet nogen kriterier, er alle medarbejdere berettiget til lønstrukturen. Hvis en medarbejder ikke opfylder de kriterier, der er angivet i berettigelsesreglen, eller er der ikke angivet en berettigelsesregel for en lønstruktur, vises lønstrukturen ikke i opslaget, når der oprettes en post for fast løn for en medarbejder.  
7. Luk siden.
8. Luk siden.


