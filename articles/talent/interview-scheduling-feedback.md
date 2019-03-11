---
title: Samtaleplanlægning og tilbagemelding
description: Dette emne indeholder oplysninger om samtaleplanlægning og tilbagemeldingsaktiviteter i Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2019
ms.locfileid: "374870"
---
# <a name="interview-scheduling-and-feedback"></a>Samtaleplanlægning og tilbagemelding

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Aktiviteten Planlægger

Planlæggeraktiviteten er valgfri og består af to komponenter: anmodning om og tidsplan for kandidatens tilgængelighed. I komponenten Kandidatens tilgængelighed kan du bruge e-mail til at anmode om en kandidats tilgængelighed. Komponenten Planlægger giver mulighed for at planlægge samtaler med kandidaten og ansættelsesteamet.

### <a name="candidate-availability-request"></a>Anmode om kandidatens tilgængelighed

Hvis du vil sende en mail til kandidater for at anmode om deres tilgængelighed, skal du markere feltet **Anmod om kandidatens tilgængelighed**. Hvis feltet ikke er markeret, vises dette trin ikke i ansættelsesprocessen for jobbet.

Du kan sende anmodningen om tilgængelighed ved at klikke på **Send anmodning**, vælge de tilgængelige datoer og derefter sende mailen til kandidaten.

[![Rekrutteringsvisning i Attract til afsendelse af anmodning om kandidatens tilgængelighed](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Når kandidaten modtager en mail, som kan bruges til at svare på anmodningen, kan vedkommende logge på sin kandidatportal, vælge de datoer, hvor han eller hun er tilgængelig, og klikke på **Send**.

### <a name="schedule"></a>Plan
Der findes flere konfigurationer, som den, der planlægger samtalen, kan bruge til hurtigt at oprette og sende samtaleløkken til interviewerne og kandidaten.

1. Klik på **Opret tidplan**, og angive i feltet **Tilføj interviewere** alle interviewere, der skal være en del af samtaleløkken.
[![Rekrutteringsvisning i Attract til planlægning af en samtaleløkke](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Hvis kandidaten har besvaret anmodningen om tilgængelighed for samtale, er feltet **Samtaledato** udfyldt på forhånd med deres valg. Du kan vælge en anden dato.
    
    Hvis du vælger feltet **Gør dette til en panelsamtale**, flyttes gruppen af interviewere til venstre til en enkelt panelløkke, så samtalen kan oprettes. Derefter skal du definere en bestemt rækkefølge for samtalerne.
    
    Tidsplanen for samtalen skal udfærdiges, så den bedst opfylder deltagernes tilgængelighed. Hvis det er en intern kandidat, kan du medtage vedkommendes tilgængelighed som en del af den anbefalede tidsplan.
    
    Hvis du vil have et onlinemøde, skal du vælge feltet **Tilføj Skype-møder**, så hver samtalehændelse får et **Skype for Business** link.

2. Vælg samtalevarigheden for hver samtalehændelse, og klik derefter på **OK** for at begynde at oprette tidsplanen.

    Hvis **Anbefalinger** er markeret, vises forslag, og samtalegitteret er udfyldt på forhånd. Du kan se den aktuelle kalendertilgængelighed for alle valgte interviewere. Du kan også se kalenderen for kandidaten, hvis det er en intern ansøger.

3. Hvis der ikke er nogen tilgængelige forslag, skal du i kolonnen **Interviewere** klikke på et tidsinterval, angive overskriften for samtalen og oplysninger det valgte sted efter behov. Du kan vælge at medtage **Skype for Business** linket til samtalen.

4. Hvis du vil medtage yderligere interviewere, skal du klikke på gitterkolonnen **Tilføj samtale** for at vælge en eller flere interviewere. Du kan bruge ellipseindstillingen (...) til at fjerne en samtale fra løkken.
    
5. Hvis samtalerne er planlagt i en anden tidszone, kan du vælge den nødvendige by/tidszone på listen på rullelisten øverst til højre. Gitteret med interviewertilgængelighed opdateres, så det afspejler den nye tidszone. Valg af tidszone fremgår nu også af visningen **Samtaleoversigt**, som deles med interviewerne og kandidaten. 

6. Klik på **Send til interviewere** for at sende mødeinvitationerne til de pågældende interviewere.

    Når samtaleanmodningerne er sendt til interviewerne, kan de svare direkte fra den mailinvitation, de modtager.

    >[!NOTE]
    > For alle 1:1-samtaler sendes påmindelser til interviewerne hvert døgn, hvis intervieweren ikke har svaret på (accepteret eller afvist) samtaleanmodningen.

    > Der ingen automatiske påmindelser om samtaleanmodningen ved panelsamtaler. For at udløse en påmindelse manuelt kan du redigere samtalen og bruge indstillingen **Opdater og send** til at sende anmodningen til interviewerne.

    Interviewernes svar registreres og vises i Attract. Hvis en interviewer afviser invitationen, bliver du mindet om at foretage en ændring. Du kan få vist deres svar i gittervisningen **Planlægger** ved at klikke på boble-ikonet.

[![Rekrutteringsvisning i Attract af en interviewers svar](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Når tidsplanen for samtalen er klar til at blive delt med kandidaten, skal du klikke på **Send til kandidat**. Du kan vælge at skjule eller vise interviewernes navne og intervaller med kandidaten.

8. Vælg en mailskabelon, og send samtaleoversigten til kandidaten. Kandidaten kan få vist disse oplysninger i deres mail og på deres kandidatportal.
    
>[!NOTE] 
> En kandidats kalendertilgængelighed vises kun, hvis kandidaten er intern. På samme måde kan kun en intern kandidat bruges til at forbedre anbefalede samtaletidsplaner. I øjeblikket modtager kandidater (interne eller eksterne) ikke en mail med en mødeinvitation. I stedet modtager kandidaten kun en oversigt over samtalerne.

## <a name="feedback-activity"></a>Aktiviteten Tilbagemelding

Tilbagemeldingsaktiviteten er valgfri i en jobskabelon. Med denne aktivitet kan deltagerne i samtalen angive anbefalinger eller tilbagemelding for en ansøger. Hvis feltet **Overtag tilbagemeldingsdeltagere fra ansættelsesteam** er markeret, angives rekrutteringsmedarbejder, den ansættelsesansvarlige og interviewerne automatisk i tilbagemeldingsaktiviteten. Organisationer kan tillade, at interviewere får vist tilbagemeldinger fra andre, før de sender deres egen feedback. Organisationer kan også tillade, at interviewere redigerer deres tilbagemeldinger, når de sender dem. Interviewerne mindes om at sende tilbagemelding på samtaler, de har deltaget i for nylig, baseret på den foruddefinerede konfiguration som en del af jobskabelonen. Ansættelseschefen eller en rekrutteringsmedarbejder for et job kan også vælge at minde en interviewer om at sende tilbagemelding manuelt.

## <a name="interview-activity"></a>Aktiviteten Samtale

Samtaleaktiviteten er en valgfri aktivitet med tre komponenter: anmodning om kandidatens tilgængelighed, tidsplan og tilbagemelding. Brug samtaleaktiviteten i jobskabelonen, hvis du vil se hele kandidatens tilgængelighedsanmodning, tidsplan og tilbagemelding som en del af processen i stedet at bruge dem enkeltvist som en del af ansættelsesprocessen.
