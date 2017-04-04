---
title: "Distribuere og udfylde et spørgeskema"
description: "Dette emne forklarer, hvordan fordeler de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller sammenslutning af personer, der skal udfylde dem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Distribuere og udfylde et spørgeskema

Dette emne forklarer, hvordan fordeler de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller sammenslutning af personer, der skal udfylde dem. 

Der er flere måder at distribuere et spørgeskema på:

-   Markér spørgeskemaet som aktivt. Spørgeskemaet er derefter tilgængeligt for alle medarbejdere, medmindre der er oprettet en spørgeskemagruppe for at begrænse adgangen til det.
-   Tildel rettigheder til en spørgeskemagruppe. Spørgeskemaet er derefter tilgængeligt for alle medlemmer af den valgte gruppe.
-   Opret planlagte besvarelser. Spørgeskemaet er derefter kun tilgængeligt for én bestemt person.
-   Opret tidsplan. Spørgeskemaet kan derefter være tilgængeligt for flere personer.

## <a name="marking-a-questionnaire-as-active"></a>Markering af et spørgeskema som aktivt
Ved at angive den **aktive** til **Ja** på den **spørgeskemaer** side, du gøre spørgeskemaet tilgængeligt for alle medarbejdere til at fuldføre. Svarpersoner kan udfylde spørgeskemaet flere gange. Denne funktion er nyttig, hvis du vil indsamle løbende feedback hele året. Du kan for eksempel oprette et spørgeskema, som medarbejdere bruger til at give feedback om tjenesten frokost i cafeteriaet.

## <a name="questionnaire-groups"></a>Spørgeskemagrupper
Du kan oprette spørgeskemagrupper og derefter medtage de svarpersoner, som et spørgeskema skal distribueres til. 

Du kan oprette spørgeskemagrupper fra følgende sider:

-   **Spørgeskemagrupper **– Kun personer i en spørgeskemagruppe kan udfylde et valgt spørgeskema. Hvis din målgruppe f.eks. er underleverandører, kan du oprette en spørgeskemagruppe, der er specifik for disse svarpersoner.
-   **Medlemmer af spørgeskemagruppe** – Du kan føje personer til spørgeskemagruppen.

At tildele en spørgeskemagruppe et spørgeskema i de **spørgeskemaer** skal du klikke på **brugerrettigheder**. Når spørgeskemaet er gemt som aktiv, kan medlemmerne af spørgeskemagruppen udfylde spørgeskemaet. Denne funktion er nyttig, hvis du vil teste et spørgeskema på en udvalgt gruppe af personer, før du vender til en større gruppe, eller hvis du vil fokusere på et spørgeskema til en meget specifik målgruppe.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Planlagte besvarelser i et spørgeskema
Planlagte besvarelser er spørgeskemaer, som du har designet og valgt svarpersoner for. 

**Bemærk!** Før du kan oprette planlagte besvarelser, skal du designe et spørgeskema. 

På siden **Planlagte besvarelser** kan du oprette en planlagt besvarelse for en bestemt medarbejder. Listen på siden viser alle planlagte spørgeskemaer. 

Planlagte besvarelser bruges også i formen **Spørgeskemaplaner**, hvor du kan planlægge spørgeskemaer for flere personer:

-   Medarbejdere
-   Kursusdeltagere
-   Organisationsenheder

Hver person kan kun besvare spørgeskemaet én gang.

## <a name="scheduling-a-questionnaire"></a>Planlægning af et spørgeskema
Du kan vælge, om du vil planlægge et spørgeskema til flere svarpersoner.

### <a name="planning-types"></a>Planlægningstyper

Planlægningstyper er nødvendige, hvis du vil arrangere planlagte besvarelser for flere svarpersoner. Planlægningstyper bruges klassificering af tidsplaner for spørgeskemaer. Du kan f.eks. planlægge spørgeskemaer til følgende formål:

-   Evaluering
-   Undersøgelse
-   Test

Du kan angive planlægningstyper for en spørgeskemaplan på siden **Spørgeskemaplaner**.

### <a name="reference-types-for-questionnaire"></a>Referencetyper for spørgeskema

Du kan bruge referencetyper til at angive kriterier de svarpersoner, du eventuelt vælger, når du planlægger et spørgeskema. 

Brug siden **Referencetyper** til at angive referencetyper for et spørgeskema. Hver referencetype svarer til en tabel i Microsoft Dynamics 365 for operationer. Når du opretter spørgeskemaplaner, kan du angive individuelle poster i tabellen eller et interval af poster, der skal være tilknyttet spørgeskemaet. 

Hvis du f.eks. vælger tabellen Kurser, kan du bestemme, hvilket kursus spørgeskemaet er beregnet til. Når du opretter en referencetype til tabellen Kurser, bliver nogle felter og knapper på siden **Kurser** tilgængelige.

### <a name="questionnaire-schedules"></a>Spørgeskemaplaner

Du kan bruge spørgeskemaplaner til at generere flere planlagte besvarelser for en gruppe af brugere, på baggrund af en referencetype. Oprette en tidsplan på den **spørgeskemaplaner** side. Vælg den planlægning til at kategorisere tidsplanen, og vælg den referencetype, der skal bruges til at forespørge system for bestemte brugere også. For eksempel, hvis du angiver referencetypen til tabellen kurser, kan du vælge et bestemt kursus i den **Reference** felt. 

Klik på **Oplysninger om opsætning** for at vælge spørgeskemaet og andre kriterier. For eksempel angive instruktørens navn som et kriterium, hvis spørgeskemaet er en vurdering af instruktøren. Når du er færdig med at indtaste oplysninger om de opsætning, genererer systemet planlagte besvarelser for de brugere, der er medtaget i forespørgslen. 

Klik på **Planlagte besvarelser** for at få vist besvarelser for planen. Du kan derefter manuelt oprette yderligere planlagte besvarelser eller slette planlagte besvarelser, der ikke er besvaret. 

Klik på **funktion**&gt;**Start** gøre spørgeskemaet tilgængeligt for brugerne i relaterede planlagte besvarelser. Klik på **Svar** for at få vist de fuldførte besvarelser af spørgeskemaerne. Du kan også kopiere indstillingerne for spørgeskemaplanen, planlagte besvarelser og svar på en ny spørgeskemaplan.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Besked til svarpersoner om spørgeskemaer, der er tilgængelige for dem
Når du distribuerer et spørgeskema, skal du give svarpersonerne besked om, at spørgeskemaerne er tilgængelige for dem. 

**Bemærk:** svarpersoner skal være brugere i Microsoft Dynamics 365 for operationer til at udfylde et spørgeskema.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Besked til svarpersoner om en planlagt besvarelse

Hvis du bruger en planlagt besvarelse, skal du give personen besked direkte, f.eks. via telefon eller e-mail.

### <a name="notifying-respondents-about-a-scheduling"></a>Besked til svarpersoner om en planlægning

Brug siden **Spørgeskemaplaner** til at forberede og sende en e-mail til alle svarpersoner, der er tilknyttet spørgeskemaet. Indtast e-mailteksten under fanen **E-mail for medarbejderselvbetjening**. Når planen er startet, skal du klikke på **funktion**&gt;**sende e-mail** til at generere og sende e-mailen til svarpersoner. Svarpersonerne kan derefter logge på webstedet og udfylde spørgeskemaet. 

**Bemærk!** Før du kan bruge e-mailfunktionen, skal din it-administrator angive e-mailindstillingerne på siden **E-mailparametre**.

## <a name="ending-a-scheduled-questionnaire"></a>Afslutning af et planlagt spørgeskema
Du kan afslutte et planlagt spørgeskema, når alle svarpersoner har udfyldt deres tildelte besvarelser. Når et planlagt spørgeskema er afsluttet, kan du ikke kopiere indstillingerne til en ny tidsplan. 

**Bemærk!** Hvis en eller flere svarpersoner ikke har fuldført spørgeskemaet, men du stadig vil afslutte planlægningen, skal du først slette disse svarpersoner fra listen på siden **Planlagte besvarelser**. Derefter kan du slette tidsplanen.

## <a name="completing-questionnaires"></a>Besvare spørgeskemaer
Når du har designet og distribueret et spørgeskema, kan spørgeskemaet udfyldes af udvalgte svarpersoner. Du kan udfylde de spørgeskemaer, der er tilgængelige for dig, fra to steder:

-   Klik på i navigationsruden, **spørgeskemaer**&gt;**fordel**&gt;**udfylde et spørgeskema,**.
-   Klik på **Spørgeskemaer, der skal udfyldes** i Medarbejderselvbetjening.

Spørgeskemaer kan gøres tilgængelige for bestemte brugere eller brugergrupper eller for alle brugere på et netværk.

<a name="see-also"></a>Se også
--------

[Udforme spørgeskemaer](design-questionnaires.md)

[Brug af spørgeskemaer](questionnaires.md)

[Få vist og evaluere resultaterne af spørgeskemaer](evaluate-questionnaire-results.md)


