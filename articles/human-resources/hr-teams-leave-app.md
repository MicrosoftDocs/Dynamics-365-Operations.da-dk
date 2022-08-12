---
title: Administrere fraværsanmodninger i Teams
description: Denne artikel viser, hvordan du anmoder om fravær i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdfd8db68647623e2b5f1b9eca93b57776e1bfe9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067025"
---
# <a name="manage-leave-requests-in-teams"></a>Administrere fraværsanmodninger i Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams. Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning. Fanen **Fridage** giver mere detaljerede oplysninger. Du kan også sende personer oplysninger om dine kommende fridage i Teams og chatte uden for Human Resource-appen.

## <a name="install-the-app"></a>Installere appen

Du kan finde appen Dynamics 365 Human Resources i lageret til Teams.

1. Gå til listen over apps i Microsoft Teams.
 
2. Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Human Resources**.

> [!NOTE]
> Fra og med 20. december 2021 vil de robottjenester for Human Resources-appen (version 1.1.4), der har Microsoft-lejeren som vært, blive taget ud af drift. Den seneste udvidelse (version af 1.1.5) er tilgængelig for installation. Du kan finde flere oplysninger i [Administrere fraværsanmodninger i Teams](hr-admin-teams-leave-app.md#update-app).

3. Klik på knappen **Tilføj** for at installere appen.

Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.

> [!NOTE]
> Hvis du ikke kan se logondialogboksen, skal du opdatere browserindstillingerne for at tillade pop op-vinduer. 

Hvis du har adgang til mere end én forekomst af Human Resources, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.

> [!NOTE]
> Appen understøtter nu sikkerhedsrollen Systemadministrator.
 
## <a name="use-the-bot"></a>Brug botten

Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.

> [!NOTE]
> Når du interagerer med robotten for første gang, skal du muligvis logge på. Hvis du ikke kan se logondialogboksen, skal du opdatere browserindstillingerne for at tillade pop op-vinduer.

Du kan bede bot om at:

- Få vist dine aktuelle orlovssaldi. Send f.eks. meddelelsen "Vis orlovssaldi".

- Starte en anmodning om en orlov for dig. Send f.eks. en meddelelse med teksten "Tag fri" eller "Jeg ønsker holde ferie næste torsdag og fredag" for at være mere specifik, når du anmoder om orlov for ferietypen. 

  ![Starte en anmodning om orlov i Teams-chat.](./media/hr-teams-leave-app-initiate.png)

- Chatrobotten udfylder en orlovsanmodning for dig. Vælg **Anmod om fri**, og rediger detaljerne om anmodningen.

   Hvis du vil sende orlovsanmodninger for flere orlovstyper for den samme dato, skal du vælge indstillingen **Opdel dag med** fra menuen **Flere indstillinger**. 

   Hvis du vælger en halv dags orlov, og orlovsanmodningsenheden er i dage, kan du angive, om du vil anmode om fri første halvdel af dagen eller anden halvdel af dagen, ved at vælge indstillingen **Halvdagsdefinition** i menuen **Flere indstillinger**.
   
   ![Halvdagsdefintioner.](./media/HalfDayDefinitions.png)

- Når du er færdig med at redigere oplysningerne om din anmodning om orlov, skal du vælge **Send** for at sende den til godkendelse.

  ![Sende orlovsanmodning.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Administrere din orlov i Teams

Fanen **Fri** gør det muligt at vise: 

- Kontooplysninger om hver orlovstype, du er tilmeldt

- Kommende orlovsanmodninger

- Anmodninger om fravær

- kladdeorlovsanmodninger
 
### <a name="create-a-new-request"></a>Oprette en ny anmodning

1. Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.

2. Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.

   ![Tilføj fridag i orlovsappen i Human Resources i Teams.](./media/TimeOffHours.png)

3. Angiv en årsagskode, hvis det er relevant. Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.

4. Vælg indstillingen **Opdel dag med** i menuen **Flere indstillinger**, hvis du vil sende flere orlovsanmodninger for den samme dato for forskellige orlovstyper.

5. Vælg indstillingen **Halvdagsdefinition** for at angive, om du vil anmode om fri den første halvdel af dagen eller den anden halvdel af dagen. Denne indstilling er tilgængelig, når orlovsanmodningsenheden er i dage, og det ønskede antal dage er 0,5 dage.

6. Når du er færdig med at angive oplysninger, skal du vælge **Send** for at sende dem til godkendelse. Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.

### <a name="manage-draft-requests"></a>Administrere kladdeanmodninger

1. Vælg fanen **Kladder**.

2. Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.

3. Foretag eventuelle nødvendige ændringer. Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse. Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.
   
### <a name="respond-to-teams-notifications"></a>Besvare Teams-beskeder

Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Human Resources i Teams. Du kan vælge beskeden for at få vist orlovsanmodningen. Beskeder vises også i **Chat**-området.

Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden. Du kan også angive en valgfri meddelelse.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Sende oplysninger om kommende fridage til dine kolleger

Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.

1. I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.

   ![Knappen Human Resources under chatvinduet.](./media/hr-teams-leave-app-chat-button.png)

2. Vælg den orlovsanmodning, du vil dele. Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.

Din orlovsanmodning vises i chatten.

Hvis du har delt en kladdebaseret anmodning, vises den som en kladde.

## <a name="view-your-teams-leave-calendar"></a>Se dit teams orlovskalender

Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.

1. I appen Human Resources i Teams skal du vælge **Fri**.

2. Vælg **Teamkalender**. I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.

   > [!NOTE]
   > Hvis du ikke kan se teamkalenderen, kan du bede din administrator om at aktivere den. Du kan finde flere oplysninger i [Installere og konfigurere](hr-admin-teams-leave-app.md#install-and-setup).

## <a name="supported-languages"></a>Understøttede sprog

Appen Dynamics 365 Human Resources i Teams understøtter følgende sprog:

| Landestandard-id | Sprog |
| --- | --- |
| de-DE | Tysk (Tyskland) |
| es-ES | Spansk (Spanien) |
| es-MX | Spansk (Mexico) |
| fr-CA | Fransk (Canada) |
| fr-FR | Fransk (Frankrig) |
| it-IT | Italiensk (Italien) |
| nl-NL | Hollandsk (Nederlandene) |
| pt-BR | Portugisisk (Brasilien) |
| tr-TR | Tyrkisk (Tyrkiet) |
| zh-CN | Kinesisk (forenklet) |

## <a name="troubleshooting"></a>Fejlfinding

Hvis du har problemer med at logge på eller bruge Dynamics 365 Human Resources-appen Teams, kan du prøve at følge disse fejlfindingsinstruktioner. Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support. Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Der kan ikke logge på appen Human Resources i Teams

Hvis du ikke kan logge på appen, er det muligt, at den konto, du bruger til at logge på Microsoft Teams, ikke er knyttet til en medarbejderpost i Dynamics 365 Human Resources. Kontakt systemadministratoren for at sikre, at din medarbejderpost er tilknyttet korrekt.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Miljøet for Dynamics 365 Human Resources blev ikke fundet i indstillinger

Hvis du ikke kan vælge det korrekte Dynamics 365-miljø, er brugerposten muligvis ikke synkroniseret korrekt. Kontakt systemadministratoren for at oprette brugerposten igen og knytte den til brugerlegitimationsoplysningerne. Prøv derefter at logge på Human Resources-appen for Microsoft Teams efter nogle få minutter.

### <a name="translations-dont-display-correctly"></a>Oversættelser vises ikke korrekt

Hvis oversættelser ikke vises som forventet, skal du sørge for, at det sprog, du vælger i Teams, svarer til det sprog, der er valgt i **Brugerindstillinger** i Human Resources.

I Teams skal du se på **App-sprog** i **Indstillinger**.

![Teams-indstillinger.](./media/hr-teams-leave-app-settings.png)

Vælg **Indstillinger** i Human Resources, og vælg derefter **Brugerindstillinger**. Kontrollér, at feltet **Sprog** svarer til feltet **App-sprog** i Teams.

![Brugerindstillinger i Human Resources.](./media/hr-teams-leave-app-user-options.png)

Hvis du stadig oplever oversættelsesproblemer, kan du give os besked. Du kan finde flere oplysninger i [Få support til programmer til finans og drift eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams

Hvis du modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du prøve følgende fejlfindingstrin:

1. Kontrollér, at den konto, du bruger til at logge på Microsoft Teams, er den samme, som du bruger til at få adgang til Dynamics 365 Human Resources.

2. Kontrollér, at du er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse. Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Orlovsgodkendere modtager ikke Teams-chatmeddelelser til godkendelse af orlovsanmodninger

1. Sørg for, at beskeder er aktiveret for miljøet og brugeren. Du kan finde flere oplysninger i [Aktivere beskeder for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Slå Teams-beskeder til eller fra for individuelle brugere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Sørg for, at brugere er logget under fanen **Chatbeskeder** med de samme legitimationsoplysninger, som de bruger til at godkende orlovsanmodninger. Brug meddelelserne for "Log af" og derefter "Log på" for at logge på med de rette legitimationsoplysninger.

3. Hvis problemet fortsætter, skal du kontrollere statussen for systembatchjobbet **Forretningshændelser** som systemadministrator. Hvis det er i **Venter**- eller **Udfører**-fasen, skal du tjekke igen om et par minutter. Hvis statussen forbliver uændret, skal du logge en supportanmodning, så vores team kan hjælpe med at løse problemet.

## <a name="known-accessibility-issues"></a>Kendte problemer med tilgængelighed

Human Resources-appen i Teams har følgende tilgængelighedsproblemer, som vi arbejder på at løse i fremtidige versioner.

| Udsted | Løsning eller forklaring |
| --- | --- |
| Hvis du zoomer til 400 % på skrivebordet, skjules nogle af handlingsknapperne i visningen. | Vi anbefaler, at du bruger et forstørrelsesglas i stedet, indtil vi kan understøtte dette zoomniveau. |
| Under fanen **Fridage** annoncerer VoiceOver en knaphandling under læsning af overskriften til gitteret for fridage. | Overskriften og elementerne i gitteret grupperes efter år, og de kan skjules. VoiceOver fortolker denne præsentation som et element, der kan handles på, men det er ikke tilfældet. |
| Under fanen **Fridage** er der en ekstra strygebevægelse, når du navigerer til **Årsagskode** i en ny anmodning. | Der er ikke noget skjult kontrolelement, som strygenavigationen forsøger at få adgang til. |
| Hvis du lave en strygebevægelser under fanen **Fridage**, mens kalenderen er åben, havner du uden for kontrolelementet i stedet for øverst i en ny anmodning, eller når du redigerer en anmodning. | Når du når **Gå til i dag**, skal du betragte det som slutningen af kontrolelementet og stryge i modsatte retning for at gå tilbage til toppen. |
| Under fanen **Chat** springer fokus tilbage til toppen, når du angiver en dato, mens du bruger hjælpeværktøjet eller tastaturnavigation. | Tabulér, indtil du når til inputområdet igen. |

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Med Dynamics 365 Human Resources-robotten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/hensigt. Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service). Læs mere om LUIS [her](https://www.luis.ai/). LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso). Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen. 

Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse. LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources. Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure Bot Framework. 

Indholdet af brugerforespørgsler og -meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten. Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid og Azure Cosmos DB

Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers Human Resources-service er installeret.

Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsprocesopgave til Microsoft Azure Event Grid og Microsoft Teams. Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester. Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams. Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer. Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Se også

[Downloade og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams Hjælp-center](https://support.office.com/teams)</br>
[Human Resources-app i Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

