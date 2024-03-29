---
title: Oprette performancegennemgange
description: Denne artikel viser, hvordan du opretter en performanceevaluering, og beskriver formålet med hvert afsnit i evalueringen.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872175"
---
# <a name="create-performance-reviews"></a>Oprette performancegennemgange


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Denne artikel viser, hvordan du opretter en performanceevaluering, og beskriver formålet med hvert afsnit i evalueringen. Denne procedure blev oprettet ved hjælp af demodatafirmaet USMF.

1. Vælg arbejdsområdet **Medarbejderselvbetjening** på startsiden.
2. Vælg **Ny evaluering** for at oprette en ny evaluering.
3. Indtast eller vælg en værdi i feltet **Evalueringstype**.
4. Indtast eller vælg en værdi i feltet **Performanceperiode**.
5. Indtast en dato i feltet **Slutdato**.
6. Vælg **OK**. Du kan også oprette en evaluering ud fra en skabelon. Dette er den bedste måde at oprette en evaluering på, fordi hver sektion indeholder de oplysninger, du skal bruge for at starte en evaluering.  
7. Du kan vise eller skjule faner som fanen Vedhæftede filer:

    1. I handlingsruden skal du vælge **Vis sektioner** for at åbne dialogmenuen.
    1. Vælg **Ja** eller **Nej** i feltet **Vis vedhæftede filer** for at vise eller skjule fanen Vedhæftede filer.
    1. Vælg **Gem**.

8. Vælg **Tilføj mål til evaluering** for at tilføje et mål. Vælg **OK**, når du er færdig.
9. Vælg **Tilføj kompetence** for at åbne dialogboksen.
10. Skriv en værdi i feltet **Titel**.
11. Angiv `Increase customer skills by working with the support team` i feltet **Beskrivelse**.
12. Vælg **OK**.
13. Vælg **Skjul alle**.
14. Vælg **Udvid alle**.
15. Vælg **Tilføj kommentar**.
16. Vælg **Bogfør**.
17. Vælg fanen **Målinger**.
18. Vælg **Tilføj mål** for at åbne dialogmenuen.
19. Indtast eller vælg en værdi i feltet **Mål**.
26. Angiv et tal i feltet **Målbeløb**.
20. Vælg **OK**.
21. Vælg fanen **Aktiviteter**.
22. Vælg **Tilføj**.
23. Skriv en værdi i feltet **Titel**.
24. Indtast en værdi i feltet **Beskrivelse**.
25. Angiv en dato i feltet **Startdato**.
26. Indtast en dato i feltet **Kompileret dato**.
27. Vælg **Ja** i feltet **Udviklingsplan**.
28. Skriv en værdi i feltet **Nøgleord**.
29. Vælg **Gem**.
30. Vælg fanen **Vurderinger**.  

    - På oversigtspanelet **Bedømmelsesoplysninger** kan medarbejdere bedømme sig selv, og lederen kan bedømme medarbejderen. Hvis der anvendes vægtninger, beregnes den vægtede værdi af resultaterne automatisk.  
    - Hvis du vil have vist dette afsnit, skal du aktivere parameterindstillingerne for visning af medarbejdervurderinger på siden **Delte parametre for personale**.  

31. Vælg fanen **Afslutninger**. Hvis evalueringen bruger arbejdsproces, vises afslutninger kun, når arbejdsprocessen er fuldført. Hvis der ikke bruges arbejdsprocesser, vises både medarbejderen og lederen her. Det **påkrævede** afkrydsningsfelt for **Godkendelser** er markeret baseret på indstillingerne for evalueringstypen.  
32. Vælg fanen **Generelt**.

    - Performanceperioden opretter standard start- og slutdatoer. Du kan ændre disse datoer.  
    - Statusserne styrer adgangen til evalueringen. Statussen **Ikke startet** giver alle tilladelse til at redigere evalueringen. Statussen **I gang** tillader kun, at medarbejderen ser og redigerer evalueringen. **Klar til evaluering** tillader kun, at lederen får vist og redigerer evalueringen. Med statussen **Endelig gennemsyn** kan både medarbejderen og chefen se og redigere gennemsynet, hvis indstillingen **Tillad redigering i endelig gennemsyn** er valgt i gennemsynstypen. I statusserne **Afsluttet** og **Annulleret** er evalueringen skrivebeskyttet. Hvis en gennemgang er **Afvist** og sendes tilbage til medarbejderen, kan både medarbejderen og lederen foretage de nødvendige ændringer, så medarbejderen kan sende den igen.

33. Skriv en værdi i feltet **Oversigt**.
34. Vælg fanen **Evaluer**. Når evalueringen bevæger sig gennem statusserne, kan medarbejderen og lederen tilføje kommentarer for de enkelte mål eller kompetencer.  
35. Vælg fanen **Afslutninger**. Arbejderen og lederen kan afslutte evalueringen. Når alle nødvendige godkendelser er fuldført, status ændres til **Fuldført**, og der foretages ingen yderligere ændringer.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
