---
title: Udsende og planlægge spørgeskemaer
description: Denne artikel beskriver, hvordan du distribuerer de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller gruppe af personer, der skal udfylde dem.
author: andreabichsel
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8c79e7b39e092bb85677fed19a53d5b9bf24962
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464976"
---
# <a name="distribute-and-schedule-questionnaires"></a>Udsende og planlægge spørgeskemaer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel beskriver, hvordan du distribuerer de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller gruppe af personer, der skal udfylde dem. 

Der er flere måder at distribuere et spørgeskema på:

-   Markér spørgeskemaet som aktivt. Spørgeskemaet er derefter tilgængeligt for alle medarbejdere, medmindre der er oprettet en spørgeskemagruppe for at begrænse adgangen til det.
-   Tildel rettigheder til en spørgeskemagruppe. Spørgeskemaet er derefter tilgængeligt for alle medlemmer af den valgte gruppe.
-   Opret planlagte besvarelser. Spørgeskemaet er derefter kun tilgængeligt for én bestemt person.
-   Opret tidsplan. Spørgeskemaet kan derefter være tilgængeligt for flere personer.

## <a name="marking-a-questionnaire-as-active"></a>Markering af et spørgeskema som aktivt

Ved at indstille feltet **Aktiv** til **Ja** på siden **Spørgeskemaer** kan du gøre spørgeskemaet tilgængeligt, så alle medarbejdere kan udfylde det. Svarpersoner kan udfylde spørgeskemaet flere gange. Denne funktion er nyttig, hvis du vil indsamle løbende feedback hele året. Du kan for eksempel oprette et spørgeskema, som medarbejdere bruger til at give feedback om tjenesten frokost i cafeteriaet.

## <a name="questionnaire-groups"></a>Spørgeskemagrupper

Du kan oprette spørgeskemagrupper og derefter medtage de svarpersoner, som et spørgeskema skal distribueres til. 

Du kan oprette spørgeskemagrupper fra følgende sider:

-   **Spørgeskemagrupper**– Kun personer i en spørgeskemagruppe kan udfylde et valgt spørgeskema. Hvis din målgruppe f.eks. er underleverandører, kan du oprette en spørgeskemagruppe, der er specifik for disse svarpersoner.
-   **Medlemmer af spørgeskemagruppe** – Du kan føje personer til spørgeskemagruppen.

Hvis du vil tildele en spørgeskemagruppe til et spørgeskema skal du klikke på **Brugerrettigheder** på siden **Spørgeskemaer**. Når spørgeskemaet er gemt som aktivt, kan medlemmerne af spørgeskemagruppen udfylde spørgeskemaet. Denne funktion er nyttig, hvis du vil teste et spørgeskema på en udvalgt gruppe personer, før du ruller det ud til en større gruppe, eller hvis du vil målrette et spørgeskema mod en meget specifik målgruppe.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Planlagte besvarelser i et spørgeskema

Planlagte besvarelser er spørgeskemaer, som du har designet og valgt svarpersoner for. 

> [!NOTE]
> Før du kan oprette planlagte besvarelser, skal du designe et spørgeskema. 

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

Brug siden **Referencetyper** til at angive referencetyper for et spørgeskema. Hver referencetype svarer til en tabel i Microsoft Dynamics 365 Finance. Når du opretter spørgeskemaplaner, kan du angive individuelle poster i tabellen eller et interval af poster, der skal være tilknyttet spørgeskemaet. 

Hvis du f.eks. vælger tabellen Kurser, kan du bestemme, hvilket kursus spørgeskemaet er beregnet til. Når du opretter en referencetype til tabellen Kurser, bliver nogle felter og knapper på siden **Kurser** tilgængelige.

### <a name="questionnaire-schedules"></a>Spørgeskemaplaner

Du kan bruge spørgeskemaplaner til at generere flere planlagte besvarelsessessioner for en gruppe af brugere, på baggrund af en referencetype. Opret en tidsplan på siden **Spørgeskemaplaner**. Vælg planlægningsgruppen for at kategorisere tidsplanen, og vælg også den referencetype, der skal bruges til at forespørge i systemet efter bestemte brugere. For eksempel hvis du indstiller referencetypen til tabellen Kurser, kan du vælge et bestemt kursus i feltet **Reference**. 

Klik på **Oplysninger om opsætning** for at vælge spørgeskemaet og andre kriterier. For eksempel angiv instruktørens navn som et kriterium, hvis spørgeskemaet er en vurdering af instruktøren. Når du er færdig med at indtaste oplysninger om opsætningen, genererer systemet planlagte besvarelsessessioner for de brugere, der er medtaget i forespørgslen. 

Klik på **Planlagte besvarelser** for at få vist besvarelser for planen. Du kan derefter manuelt oprette yderligere planlagte besvarelser eller slette planlagte besvarelser, der ikke er besvaret. 

Klik på **Funktioner** &gt; **Start** for at gøre spørgeskemaet tilgængeligt for brugerne i relaterede planlagte besvarelsessessioner. Klik på **Svar** for at få vist de fuldførte besvarelser af spørgeskemaerne. Du kan også kopiere indstillingerne for spørgeskemaplanen, planlagte besvarelser og svar på en ny spørgeskemaplan.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Besked til svarpersoner om spørgeskemaer, der er tilgængelige for dem
Når du distribuerer et spørgeskema, skal du give svarpersonerne besked om, at spørgeskemaerne er tilgængelige for dem. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Besked til svarpersoner om en planlagt besvarelse

Hvis du bruger en planlagt besvarelse, skal du give personen besked direkte, f.eks. via telefon eller e-mail.

### <a name="notifying-respondents-about-a-scheduling"></a>Besked til svarpersoner om en planlægning

Brug siden **Spørgeskemaplaner** til at forberede og sende en e-mail til alle svarpersoner, der er tilknyttet spørgeskemaet. Angiv mailteksten under fanen **Mail til medarbejderselvbetjening**. Når planen er startet, skal du klikke på **Funktioner** &gt; **Send mail** for at generere og sende mailen til svarpersonerne. Svarpersonerne kan derefter logge på webstedet og udfylde spørgeskemaet. 

> [!NOTE]
> Før du kan bruge e-mailfunktionen, skal din it-administrator angive e-mailindstillingerne på siden **E-mailparametre**.

## <a name="ending-a-scheduled-questionnaire"></a>Afslutning af et planlagt spørgeskema

Du kan afslutte et planlagt spørgeskema, når alle svarpersoner har udfyldt deres tildelte besvarelser. Når et planlagt spørgeskema er afsluttet, kan du ikke kopiere indstillingerne til en ny tidsplan. 

> [!NOTE]
>   Hvis en eller flere svarpersoner ikke har fuldført spørgeskemaet, men du stadig vil afslutte planlægningen, skal du først slette disse svarpersoner fra listen på siden **Planlagte besvarelser**. Derefter kan du slette tidsplanen.

## <a name="completing-questionnaires"></a>Besvare spørgeskemaer

Når du har designet og distribueret et spørgeskema, kan spørgeskemaet udfyldes af udvalgte svarpersoner. Du kan udfylde de spørgeskemaer, der er tilgængelige for dig, fra to steder:

-   Klik i navigationsruden på **Spørgeskemaer** &gt; **Distribuer** &gt; **Besvar et spørgeskema**.
-   Klik på **Spørgeskemaer, der skal udfyldes** i Medarbejderselvbetjening.

Spørgeskemaer kan gøres tilgængelige for bestemte brugere eller brugergrupper eller for alle brugere på et netværk.




[!INCLUDE[footer-include](../includes/footer-banner.md)]