---
title: Opret faste lønstrukturer
description: Fast løn henviser til en medarbejders normale bruttoløn eller løn. I denne artikel beskrives de komponenter, der skal konfigureres, før du kan oprette en fast lønstruktur og tilmelde medarbejdere.
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: cea4aec80bc0b519a6b393724835555b4d0937a8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303813"
---
# <a name="create-fixed-compensation-plans"></a>Opret faste lønstrukturer

[!include [banner](includes/banner.md)]

Fast løn henviser til en medarbejders normale bruttoløn eller løn. I dette emne beskrives de komponenter, der skal konfigureres, før du kan oprette en fast lønstruktur og tilmelde medarbejdere.

Fast løn-beløb kan beregnes for dine medarbejdere baseret på faktorer som ydeevne, område og øgede budgetter. Microsoft Talent understøtter kompensationstyperne trin, lønklasse og omfang.

## <a name="fixed-compensation-components"></a>Komponenter i fast løn
### <a name="compensation-levels"></a>Kompensationsniveauer

Du kan bruge **kompensationsniveauer** til at angive kompensation for forskellige job for at sikre, at de medarbejdere, der har disse job, betales rimeligt. På siden **Kompensationsniveauer** kan du konfigurere de kompensationsniveauer, der er nødvendige for hvert trin, løntrin og omfang. Brug knapperne **Op** og **Ned** til at sætte niveauerne i rigtige rækkefølge efter type. Ved at angive kompensationsniveauer for et job kan du garantere, at alle medarbejdere, der har en position for det pågældende, job betales på samme niveau.

### <a name="reference-points"></a>Referencepunkter

**Referencepunkter** er kolonnerne i gitteret, der definerer kompensationsafgrænsninger for hvert niveau. Kompensationsniveauet er rækken i gitteret. Typiske referencepunkter for en plan af typen klasse er et minimum, et midtpunkt og et maksimum. Du opretter referencepunkter på siden **Opsætninger af referencepunkter**.

### <a name="compensation-grids"></a>Kompensationsgitre

Når du har konfigureret niveauer og referencepunkter, kan de kombineres for at oprette et **kompensationsgitter**. På siden **Kompensationsgitre** skal du angive oplysninger om gitteret. Angiv for eksempel, hvad gitteret er designet til at blive brugt til, hvilken type plan det skal bruges sammen med, og hvilke referencepunkter eller kolonner der kræves i gitteret. Når du er færdig med at angive oplysningerne, skal du klikke på **Kompensationsstruktur** for at føje niveauer og beløb til gitteret. 

**Tip!** Brug funktionen **Masseændringer** i kompensationsstrukturen til at angive startbeløb, og forøg derefter med procentsatser eller beløb på tværs af niveauer eller referencepunkter.

### <a name="pay-frequencies"></a>Lønfrekvenser

**Lønfrekvenser** bruges til at definere, hvordan en medarbejders løn angives (for eksempel $10 pr. time kontra $50.000 om året), og konverteringen mellem satser pr. time, uge, måned (12 måneder) og årlige satser. Eksempelvis definerer en virksomhed, der bruger en 38-timers arbejdsuge for sine timeaflønnede medarbejdere, en lønfrekvens, der har en timesats på 1, en ugentlig sats på 38, en månedlig sats på 164,6666666667 og en årlig sats på 1,976. Disse konverteringer bruges til at beregne de forskellige lønsatser, der vises i posten for en medarbejders faste løn.

## <a name="fixed-compensation-plans"></a>Fast løn-strukturer
Du kan designe fast løn-strukturen til at kombinere alle de komponenter, du har konfigureret. Hvis du vil oprette en fast løn-struktur, skal du åbne siden **Fast løn-strukturer**. Her kan du give din struktur et navn og en beskrivelse, vælge hvilken type struktur der er tale om (trin, trin eller omfang), vælge den lønfrekvens, som du vil bruge til medarbejderens lønsats (beløb pr. time, beløb pr. år, og så videre) og angive nogle indstillinger, der styrer, hvordan kompensation behandles. 

Med indstillingen **Tolerance uden for afgrænsningerne** kan du angive, hvor stringent du vil være med hensyn til at sikre, at kompensationsbeløb ligger mellem minimale og maksimale beløb. Tolerancen **Hård** kræver, at kompensation ligger inden for det område, der er defineret for et givet niveau. Tolerancen **Blød** advarer dig, når kompensationsbeløb ligger uden for området, men tillader dig at fortsætte. Hvis du angiver tolerancen til **Ingen**, kan du indtaste et kompensationsbeløb for en medarbejder uden at få vist en advarsler eller fejlmeddelelser. 

Med indstillingen **Ansættelsesregel** kan du angive, om alle medarbejdere skal have den samme stigning uanset datoen for deres ansættelse (**Ansættelsesregel** = **Ingen**), eller om medarbejderne skal modtage en procentdel af den pågældende bonus, baseret på hvor længe de var ansat under cyklussen (**Ansættelsesregel** = **Procent**). 

En **rammeudnyttelsesmatrix** er nyttig, hvis du enten vil reducere den tid, der kræves, for at medarbejdere kan nå midtpunktet i deres område eller for at øge den tid, der kræves, for at medarbejdere kan nå det maksimale referencepunkt i området. Du vil for eksempel give medarbejdere, der er i de nederste 25 procent af deres område, 110 procent af bonusmålet, mens du kun vil give medarbejdere, der er i de øverste 25 procent af deres område, 80 procent af deres bonusmål for at forhindre dem i at nå maksimum lige så hurtigt. 

Når du definerer de grundlæggende principper for den faste løn-struktur, kan du angive kompensationsstrukturen for planen. Klik på **Konfigurer kompensation**. Der åbnes en dialogboks med en skyder, hvor du har muligheder:

-   Oprette et nyt kompensationsgitter ved at vælge en referencepunktsopsætning og give et navn til gitteret.
-   Oprette et nyt kompensationsgitter ved at oprette en kopi af et eksisterende gitter, som du kan bruge som udgangspunkt.
-   Bruge et eksisterende kompensationsgitter, der allerede er defineret. Alle kompensationsstrukturer, der bruger det samme gitter, modtage opdateringer, hvis dette gitter ændres.

Når du vælger en indstilling, åbnes siden **Kompensationsstruktur**, og du kan foretage ændringer af det nye kompensationsgitter eller det eksisterende kompensationsgitter.

## <a name="fixed-compensation-enrollment"></a>Tilmelding til fast løn
### <a name="determine-who-is-eligible-for-the-plan"></a>Bestem, hvem der er berettiget til planen

Det første trin i tilmelding af medarbejdere i en fast løn-struktur er at bestemme, hvem der er berettiget til den kompensation, der er defineret i strukturen. Indtil du fastlægger berettigelse, kan du ikke tildele strukturen til nogen medarbejdere. Hvis du vil konfigurere berettigelse, skal du åbne siden **Berettigelsesregler**. Her kan du oprette en ny berettigelsesregel til din lønstruktur og definere de kriterier, som en medarbejder skal opfylde, for at være berettiget til en struktur. Du kan begrænse berettigelse baseret på afdeling, fagforening, kompensationsområde (lokation), job, jobfunktion, jobtype eller kompensationsniveau. Medarbejdere kan kun være tilmeldt en kompensationsstruktur, hvis de opfylder alle betingelser, der er angivet i berettigelsesreglen. 

**Bemærk!** Berettigelsesregler bruges til at fastlægge berettigelse for både faste og variable strukturer. 

Berettigelsesreglen tager højde for værdien af bestemte felter i posterne Job, Stilling og Medarbejder, når det skal afgøres, om en medarbejder er berettiget til en kompensationsstruktur.

-   På siden **Job** vurderer berettigelsesreglen følgende felter:
    -   Feltet **Job**
    -   Under fanen **Jobklassificering** felterne **Funktion** og **Jobtype**
    -   Under fanen **Kompensation** feltet **Niveau**
-   På siden **Stillinger** vurderer berettigelsesreglen felterne **Afdeling** og **Kompensationsområde**.

Berettigelsesreglen vurderer også fagforeninger, som er knyttet til medarbejderen (på siden **Medarbejdere** under fanen **Arbejder**, skal du klikke på **Personlige oplysninger** &gt; **Fagforeninger**).

### <a name="define-fixed-compensation-actions"></a>Definere fast løn-handlinger

**Fast løn-handlinger** bruges, når du angiver eller anvender ændringer af en medarbejders fast løn. Fast løn-handlinger giver dig mulighed for at anvende beskrivende navne til de typer handlinger, som chef for kompensation og frynsegoder kan udføre. Forskellige aktionstyper har særlig logik bag sig, så de kan bruges på bestemte tidspunkter. 

Når fast løn f.eks. er konfigureret for en medarbejder, kan der kun bruges handlinger af typen **Ansæt/genansæt**. I dette tilfælde kan du oprette tre forskellige handlinger af typen **Ansæt/genansæt** og kalde dem **Ansæt**, **Genansæt** og **Overfør**. Du har så en mere beskrivende forklaring på, hvorfor den faste løn blev givet til en medarbejder eller ændret.

### <a name="enroll-the-employee"></a>Tilmelde medarbejderen.

Du kan nu knytte en medarbejder til en fast løn-struktur. Åbn siden **Medarbejdere** side, og vælg den medarbejder, der skal tilmeldes kompensationsplanen. Klik i handlingsruden på **Kompensation** &gt; **Fast plan**. Du kan nu oprette en ny fast løn-handling for den pågældende medarbejder. 

**Bemærk!** Feltet Kompensationsstruktur viser kun de strukturer, som en medarbejder er berettiget til i henhold til de berettigelsesregler, der er konfigureret for hver enkelt struktur. Hvis der ikke er konfigureret berettigelsesregler for en struktur, vil ingen medarbejdere være berettiget til denne den. 

Systemet kontrollerer, at det kompensationsbeløb, der er angivet for en kompensationsstruktur af typen klasse eller omfang ligger inden for de minimale og maksimale referencepunkter for det givne kompensationsniveau i medarbejderens job. Hvis kompensationsbeløbet ligger uden for det tilladte interval, vises en advarsel eller fejlmeddelelse, afhængigt af det toleranceniveau, der er angivet for fast løn-strukturen.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Kompensationsordninger](compensation-plans.md)



