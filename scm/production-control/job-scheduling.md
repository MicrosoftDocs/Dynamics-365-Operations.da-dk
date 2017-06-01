---
title: "Finplanlægning"
description: "Denne artikel indeholder oplysninger om jobplanlægning, som er en mere detaljeret form for planlægning end grovplanlægning. Du kan bruge finplanlægning til at planlægge individuelle job eller værkstedsordrer og til at styre produktionsmiljøet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3c7224390ce336439c2e43188c19b4b93cf793b8
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="job-scheduling"></a>Finplanlægning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om jobplanlægning, som er en mere detaljeret form for planlægning end grovplanlægning. Du kan bruge finplanlægning til at planlægge individuelle job eller værkstedsordrer og til at styre produktionsmiljøet.

Du kan bruge finplanlægning til at planlægge individuelle job eller værkstedsordrer og til at styre produktionsmiljøet. Finplanlægning opbryder hver enkelt operation i individuelle opgaver eller job. Disse job tildeles derefter til de operationsressourcer, der skal udføre dem. Du kan også bruge finplanlægning til at synkronisere alle job, der refereres til af det valgte job. Du kan angive startdato og -klokkeslæt eller slutdato og -klokkeslæt for jobbet og derefter udføre planlægning. Den tid, du angiver, kan være starttidspunktet eller sluttidspunktet, afhængigt af planlægningsvejen. Denne funktion er f.eks. nyttigt, når et job kun kan køres på én maskine ad gangen, eller hvis du vil optimere det job, der køres for hver ressource.

## <a name="tasks-in-the-job-scheduling-process"></a>Opgaver i finplanlægningen
Finplanlægning omfatter følgende opgaver:

-   Split operationer op i job.
-   Planlæg job, der er baseret på datoerne og klokkeslættene for de ressourcer, der er angivet for den tilknyttede operation.
-   Beregn start- og sluttidspunkter for hvert job. Du kan bruge kapacitetsbegrænsning for at sikre, at der ikke er overlapninger.
-   Bestem, hvilke ressourcer i ressourcegruppen der skal udføre jobbet. Denne opgave kræver, at der angives en ressourcegruppe for en operation. Finplanlægning vælger ressourcerne eller ressourcegrupperne på baggrund af den korteste gennemløbstid og tager også højde for tidligere reservationer på ressourcerne.
-   Udfold operationer i job, når du kører finplanlægning. Jobbene planlægges efter dato og klokkeslæt i den rækkefølge, der er angivet i produktionsruten. Opsætningen af operationen bestemmer, hvilke job der skal udfoldes under planlægningsprocessen. Den rutegruppe, der er knyttet til operationen, kontrollerer, om der er genereret job. Et job genereres kun, hvis det har en bestemt varighed. Der genereres f.eks. et transporttidsjob, hvis der blev angivet en transporttid for den valgte operation.

## <a name="scheduling-direction"></a>Planlægningsvej
Du kan planlægge job forud eller bagud.

-   **Forud** – Brug planlægningsvejen fremad for at starte produktionen så tidligt som muligt. Dette kaldes også skubmetoden, fordi produktionen skubbes fremad gennem produktionsprocessen. Produktionen er planlagt til at starte og slutte på de tidligst mulige datoer.
-   **Bagud** – Brug planlægningsvejen bagud for at starte produktionen så sent som muligt. Dette kaldes også trækmetoden, fordi den er baseret på den dato, hvor produktionen skal være færdig. Planlægning bagud tæller bagud til den senest mulige dato, produktion kan startes, uden at den ønskede deadline overskrides.

## <a name="finite-capacity"></a>Kapacitetsbegrænsning
Du kan planlægge job ved hjælp af begrænset kapacitet. Når du bruger begrænset kapacitet, må den kapacitet, der planlægges, ikke være større end den kapacitet, der er tilgængelig for ressourcen. Disponibel tid defineres som det interval, hvor ressourcen er ledig, og der ikke er andre kapacitetsreservationer. Planlægning, der er baseret på begrænset kapacitet, sikrer, at start- og sluttidspunkter for en operation på en bestemt dato ikke overlapper. Der tages højde for den ressourcekapacitet, der allerede er reserveret, og overlapninger mellem start- og sluttidspunkterne tages også i betragtning. Kapacitetsbegrænsning bestemmer omfanget af den kapacitet, der skal være tilgængelig for en ressource for at opnå optimal udnyttelse af den pågældende ressource. Denne bestemmelse er afstemt mod en beregning af den kortest mulige gennemløbstid mellem operationer.

## <a name="finite-materials"></a>Materialebegrænsning
Finplanlægning, der er baseret på materialebegrænsning, sørger for, at de nødvendige materialer er tilgængelige, når operationen startes. Disponeringsreglerne for varer definerer disse grænser. Planlægning bruger behovsudfoldning til at fastsætte, hvornår komponentvarerne er tilgængelige. Hvis du planlægger uden at angive materialebegrænsning, antages det automatisk, at alle varer er tilgængelige, når der er brug for dem.

## <a name="finite-properties"></a>Egenskabsbegrænsning
Finplanlægning, der er baseret på særlige egenskaber, forudsætter, at der angives egenskaber for produktionsrutens operationer. Disse egenskaber skal være opfyldt, før der kan reserveres kapacitet.

## <a name="references"></a>Referencer
Under finplanlægningen planlægges alle produktioner, der refereres til af den aktuelle produktion. Hvis en produktion har en eller flere underproduktioner, skal underproduktionerne planlægges på samme tid som den overordnede produktion, fordi den overordnede produktion ikke kan sættes i gang, før alle relaterede underproduktioner er afsluttet.

## <a name="schedule-resources"></a>Planlæg ressourcer
I planlægningsprogrammet undersøges kombinationer af ressourcer for at identificere de kombinationer, der opfylde kravene. Du kan angive udvalgskriterier ved at vælge en af følgende værdier i feltet **Valg af primær ressource** på siden **Planlægningsparametre**:

-   **Varighed** – Planlægningsprogrammet vælger de ressourcer, der har den korteste gennemløbstid. **Bemærk:** Planlægning efter varighed kan medføre forringet præstation, når samme ressourcegruppe indeholder mange ressourcer, og der bruges sekundære operationer. Du kan højst planlægge med 32 ressourcer pr. operation. Hvis denne mængde overskrides, vises der en infologmeddelelse, og finplanlægningen kan ikke finde den bedste alternative ressource.
-   **Prioritet** – Planlægningsprogrammet vælger ressourcen med den højeste prioritet, hvis to eller flere ressourcer har identiske færdigheder og niveauer. Den ressource, der har den laveste værdi i dette felt, har højeste prioritet.

Når du kører finplanlægning, planlægger systemet ressourcerne på baggrund af de begrænsninger, der er defineret i ressourceparametrene. Du kan styre ressourcernes kapacitet ved hjælp af kalenderindstillinger. Der beregnes indlæsninger for ressourcer under planlægningsprocessen. **Bemærk:** Til produktioner, der benytter grovplanlægningsfunktionen, kan du køre finplanlægning efter grovplanlægningen. Hvis du ikke benytter grovplanlægning, kan du køre finplanlægning alene.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Maksimal kapacitet for ressourcer pr. jobordre
Ressourcer tildeles til job via finplanlægning. Du kan definere den maksimale kapacitet for ressourcer pr. jobordre. Du kan f.eks. konfigurere systemet til at planlægge 50 procent af den samlede kapacitet for en produktionsordre. Denne konfiguration giver dig mere kontrol med planlægningen af ressourcerne på finplanlægningsniveauet. Det kan derfor hjælpe med at forhindre problemer, hvis der ikke er tilstrækkelig kapacitet til at udføre samtidige produktioner.

## <a name="resource-efficiency"></a>Ressourceeffektivitet
Under finplanlægning tages der højde for de effektivitetsprocenter, der er angivet for ressourcerne. Effektivitetsprocenter afkorter eller forlænger den tid, der er reserveret for ressourcen. Det betyder derfor, at gennemløbstiden også bliver længere eller kortere. Følgende formel bruges til beregningen: Planlægningstid = Tid × 100 ÷ Effektivitetsprocent *Tiden*, der bruges i formlen, omfatter både procestid og opstillingstid.




