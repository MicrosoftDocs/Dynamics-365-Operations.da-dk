---
title: Udarbejde en kompensationsstruktur
description: Dette emne forklarer, hvordan du kan oprette en fast kompensationsplan og tilmelde medarbejdere i planen via berettigelsesregler.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e35f4978cc4e8162c56ba05de28ab5b2366ccc7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065280"
---
# <a name="develop-a-compensation-structure"></a>Udarbejde en kompensationsstruktur


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne forklarer, hvordan du kan oprette en fast kompensationsplan og tilmelde medarbejdere i planen via berettigelsesregler. Dette emne bruger USMF-demodata og gælder for styring af kompensation og frynsegoder.

## <a name="create-a-fixed-compensation-plan"></a>Oprette en fast løn-struktur

1. Vælg **Kompensationsstyring**.

2. Vælg **Faste lønstrukturer**.

3. Vælg **Ny**.

4. Angiv en værdi i feltet **Plan**.

5. Indtast en værdi i feltet **Beskrivelse**.

6. Angiv en dato i feltet **Ikrafttrædelsesdato**.

7. I feltet **Type** skal du vælge, om den faste lønstruktur er en plan af typen **Omfang**, **Klasse** eller **Trin**.

8. Afkrydsningsfeltet **Anbefaling tilladt** er standardværdien for alle handlinger, der er føjet til denne plan i en proceshændelse. Ved at tillade anbefalinger kan du tilsidesætte det beregnede aftalebeløb ved behandling af kompensation.

9. I feltet **Tolerance uden for afgrænsningerne** kan du angive, hvordan du vil håndtere kompensationsbeløb, der falder uden for den angivne lønstrukturramme på det givne niveau. Hvis du angiver feltet **Tolerance uden for afgrænsningerne** til **Ingen**, kan du bruge et hvilket som helst kompensationsbeløb. **Tolerancen Blød** advarer brugerne, hvis kompensationsbeløbet er mindre end minimum- eller større end maksimumbeløbet for referencepunktet for det pågældende niveau. Brugerne kan ignorere advarslen og fortsætte. **Tolerancen Hård** genererer en fejl, hvis en medarbejders løn er angivet uden for minimale og maksimale referencepunkter for niveauet og justerer automatisk medarbejderens løn, så den ligger inden for rammen.

10. I feltet **Ansættelsesregel** beregnes en medarbejders kompensation under en proceshændelse. En **Ansættelsesregel** af **Procent** beregner en forholdsmæssig stigning for den tid, arbejderen har været ansat i cyklussen.

11. Skriv en værdi i feltet **Valuta**.

12. Indtast eller vælg en værdi i feltet **Konvertering af lønsats**.

13. Udvid sektionen **Rammeudnyttelsesmatrix**. Du kan eventuelt tilføje poster for rammeudnyttelse for at få medarbejdere til deres middelpunkt hurtigere og gøre det langsommere for dem at nå maksimum for deres ramme.

14. Vælg **Gem**. Det aktiverer knappen **Konfigurer kompensation** og fortsætter med at definere kompensationsstrukturen for planen.

15. Vælg **Konfigurer kompensation**. Du kan oprette en kompensationsstruktur ved hjælp af en af disse tre metoder:

    - Opret en helt ny struktur ved at vælge et sæt referencepunkter og tilføje niveauer for at oprette din egen struktur.
    - Kopiér kompensationsstruktur fra en eksisterende plan som udgangspunkt, og tilpas den til den nye plan.
    - Vælg et eksisterende kompensationsgitter. Hvis en anden plan allerede bruger kompensationsgitteret, afspejler den anden plan også eventuelle ændringer, du laver i gitteret.

16. Vælg **Opret nyt matrix fra eksisterende kompensationsmatrix**.

17. Indtast eller vælg en værdi i feltet **Kopier fra gitter**. Du kan eventuelt ændre navnet på det nye kompensationsgitter, du opretter, ved at kopiere det valgte gitter.

18. Vælg **OK**.

19. Vælg **Masseændring**. **Masseændring** gør det muligt at bevare kompensationsbeløb for matrixen ved at anvende en stigning i procent eller fladt beløb på ét eller flere niveauer og/eller referencepunkter.

20. Indtast et tal i feltet **Justeringsbeløb**.

21. Markér eller fjern markeringen af alle rækker på listen.

22. Klik på **Anvend på gitter**.

23. Luk siden. Når du har oprettet kompensationsstrukturen, kan du vælge, hvilke referencepunkter der skal bruges som kontrolpunkt for den faste lønstruktur. Kontrolpunktet bruges til at beregne kompensationsforholdet for en medarbejder.

24. Indtast eller vælg en værdi i feltet **Kontrolpunkt**.

25. Luk siden.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Opret en berettigelsesregel for den faste lønstruktur

Du kan ikke tildele en fast lønstruktur til en medarbejder, før du definerer berettigelsesregler for strukturen.  

1. Vis **Berettigelsesregler**.

2. Vælg **Ny**.

3. Indtast en værdi i feltet **Berettigelse**.

4. Indtast en værdi i feltet **Beskrivelse**.

5. Angiv en dato i feltet **Ikrafttrædelsesdato**. Faste og variable lønstrukturer bruger berettigelsesregler. Vælg plantypen i feltet **Type**.

6. I feltet **Plan** indtastes eller vælges en værdi. Vælg de kriterier, en medarbejder skal opfylde for at være berettiget til lønstrukturen. Kriterier kan omfatte:

    - **Afdeling**
    - **Fagforening**
    - **Sted** (**Kompensationsregion**)
    - **Stilling**
    - **Funktion**
    - **Jobtype**
    - **Kompensationsniveau**
    
    Medarbejderen skal opfylde alle angivne kriterier for at være berettiget til lønstrukturen. Hvis du ikke angiver nogen kriterier, er alle medarbejdere berettiget til lønstrukturen. Hvis en medarbejder ikke opfylder de kriterier, der er angivet i berettigelsesreglen, eller er der ikke angivet en berettigelsesregel for en lønstruktur, vises lønstrukturen ikke i opslaget, når du opretter en post for fast løn for en medarbejder.

7. Luk siden.

8. Luk siden.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
