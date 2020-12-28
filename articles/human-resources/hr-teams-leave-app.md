---
title: Administrere anmodninger i Teams
description: I dette emne kan du se, hvordan du anmoder om fri i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4417892"
---
# <a name="manage-leave-requests-in-teams"></a>Administrere anmodninger i Teams

[!include [banner](includes/preview-feature.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams. Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning. Fanen **Fridage** giver mere detaljerede oplysninger. Du kan også sende personer oplysninger om dine kommende fridage i teams og chatte uden for Human Resource-appen.

## <a name="install-the-app"></a>Installere appen

Du kan finde Personale-appen i storen til Teams.

1. I Microsoft Teams skal du vælge ellipserne.

   ![Ellipser i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Personale**.

   ![HR-feltet i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Klik på knappen **Tilføj** for at installere appen.

   ![Installer orlovsappen i Personale i Teams](./media/hr-teams-leave-app-in-store.png)

Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.

![Fanen Indstillinger i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer. 

Hvis du har adgang til mere end én forekomst af Personale, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.

> [!NOTE]
> Appen understøtter nu sikkerhedsrollen Systemadministrator.
 
## <a name="use-the-bot"></a>Brug botten

Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.

![Botvelkomstmeddelelse i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Når du interagerer med bot for første gang, skal du muligvis logge på. Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.

Du kan bede bot om at:

- Vise oplysninger om flekskontoen for hver orlovstype, du er tilmeldt.

   ![Vise konti i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- Vise flere detaljer om en bestemt orlovstype.

   ![Vise detaljer i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-details.png)

- Starte en anmodning om en orlov for dig.

   ![Anmodning om orlov i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-request.png)
 
Når du har startet en orlovsanmodning, kan du justere dagene direkte på kortet.

![Redigering af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-edit.png)
 
Når du er færdig med at angive oplysninger, skal du vælge **Send** for at sende dem til godkendelse. Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.

![Afsendelse af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Administrere din orlov i Teams

Fanen **Fri** gør det muligt at vise:

- Kontooplysninger om hver orlovstype, du er tilmeldt

- Kommende orlovsanmodninger

- Anmodninger om fri

- kladdeorlovsanmodninger

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Oprette en ny anmodning

1. Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.

   ![Ny anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.

   ![Tilføj fridag i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Angiv en årsagskode, hvis det er relevant. Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.

4. Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse. Du kan også indtaste **Gem som kladde** for at vende tilbage til den senere.

### <a name="manage-draft-requests"></a>Administrere kladdeanmodninger

1. Vælg fanen **Kladder**.

   ![Fanen Kladder i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.

3. Foretag eventuelle nødvendige ændringer. Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse. Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.

   ![Redigering af kladde i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Besvare Teams-beskeder

Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Personale i Teams. Du kan vælge beskeden for at få den vist. Beskeder vises også i **Chat**-området.

Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden. Du kan også angive en valgfri meddelelse.

![Besked om orlovsanmodning i Teams-appen Personale](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Sende kommende oplysninger om fridage til dine kolleger

Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.

1. I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.

   ![Knappen Human Resources under chatvinduet](./media/hr-teams-leave-app-chat-button.png)

2. Vælg den orlovsanmodning, du vil dele. Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.

   ![Vælge en kommende orlovsanmodning til at dele](./media/hr-teams-leave-app-chat-search.png)

Din orlovsanmodning vises i chatten.

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

Hvis du har delt en kladdebaseret anmodning, vises den som en kladde:

![Kladde af Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Se dit teams orlovskalender

Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.

1. I appen Personale i Teams skal du vælge **Fri**.

2. Vælg **Teamkalender**.

   ![Se kalender i Teams-appen Personale](./media/hr-teams-leave-app-view-calendar.png)

I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.

![Fraværskalender i Teams-appen Personale](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a>Fejlfinding

Hvis du har problemer med at logge på eller bruge appen Human Resources Teams, kan du prøve at følge disse fejlfindingsinstruktioner. Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support. Du kan finde flere oplysninger under [Få support](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Der kan ikke logge på appen Human Resources i Teams

Hvis du ikke kan logge på appen, er det muligt, at den konto, du bruger til at logge på Microsoft Teams, ikke er knyttet til en medarbejderpost i Dynamics 365 Human Resources. Kontakt systemadministratoren for at sikre, at din medarbejderpost er tilknyttet korrekt.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams

Hvis du modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du prøve følgende fejlfindingstrin:

1. Kontrollér, at den konto, du bruger til at logge på Microsoft Teams, er den samme, som du bruger til at få adgang til Dynamics 365 Human Resources.

2. Kontrollér, at du er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse. Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).

## <a name="known-accessibility-issues"></a>Kendte problemer med tilgængelighed

Human Resources-appen i Teams har følgende tilgængelighedsproblemer, som vi arbejder på at løse i fremtidige versioner.

| Udsted | Løsning eller forklaring |
| --- | --- |
| Hvis du zoomer til 400 % på skrivebordet, skjules nogle af handlingsknapperne i visningen. | Vi anbefaler, at du bruger et forstørrelsesglas i stedet, indtil vi kan understøtte dette zoomniveau. |
| Under fanen **Fridage** annoncerer VoiceOver en knaphandling under læsning af overskriften til gitteret for fridage. | Overskriften og elementerne i gitteret grupperes efter år, og de kan skjules. VoiceOver fortolker dette som et element, der kræver en handling, men det er ikke. |
| Hvis du foretager en strygebevægelse, mens en pop op-menu er åben, ignorerer VoiceOver læsningen af pop op-menuen eller menuindholdet. | Udforsk indholdet ved hjælp af fingerscanning. |
| Under fanen **Fridage** er der en ekstra strygebevægelse, når du navigerer til **Årsagskode** i en ny anmodning. | Der er ikke noget skjult kontrolelement, som strygenavigationen forsøger at få adgang til. |
| Hvis du lave en strygebevægelser under fanen **Fridage**, mens kalenderen er åben, havner du uden for kontrolelementet i stedet for øverst i en ny anmodning, eller når du redigerer en anmodning. | Når du når **Gå til i dag**, skal du betragte det som slutningen af kontrolelementet og stryge i modsatte retning for at gå tilbage til toppen. |
| VoiceOver kan ikke læse datoetiketterne. | De datoer, der optræder som par, er altid **Startdato** og **Slutdato**. |
| Under fanen **Chat** springer fokus tilbage til toppen, når du angiver en dato, mens du bruger hjælpeværktøjet eller tastaturnavigation. | Tabulér, indtil du når til inputområdet igen. |

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål. Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service). Læs mere om LUIS [her](https://www.luis.ai/). LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso). Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen. 

Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse. LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources. Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen. 

Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten. Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid og Azure Cosmos DB

Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.

Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams. Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester. Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams. Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer. Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Se også

[Downloade og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams Hjælp-center](https://support.office.com/teams)</br>
[Human Resources-app i Teams](hr-admin-teams-leave-app.md)
