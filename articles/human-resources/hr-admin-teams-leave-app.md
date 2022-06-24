---
title: Appen Human Resources i Teams
description: Denne artikel introducerer Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7ff576efbfeb0c5383a48756fdd7e79f1abdba2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902250"
---
# <a name="human-resources-app-in-teams"></a>Appen Human Resources i Teams


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres fritidskontooplysninger i Microsoft Teams. Medarbejderne kan interagere med en bot for at anmode om oplysninger. Fanen **Fridage** giver mere detaljerede oplysninger. De kan også sende oplysninger om kommende fridage i teams og chatte uden for Human Resource-appen.

![Orlov via appbot i Human Resources i Teams.](./media/hr-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Human Resources i Teams.](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-orlovsanmodningskort.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Installere og konfigurere

Du kan finde appen Dynamics 365 Human Resources i lageret til Teams. Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).

Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

Hvis brugerne skal have vist orlovs- og fraværskalenderen i appen, skal du aktivere **Orlovs- og fraværskalenderen i Teams** i funktionsstyring. Du kan finde flere oplysninger om aktivering af funktioner i [Administrere funktioner](hr-admin-manage-features.md).

## <a name="update-app"></a>Opdatere app
>[!NOTE]
> Fra og med 20. december 2021 vil de robottjenester for Human Resources-appen, der har Microsoft-lejeren som vært, blive taget ud af drift. Det påvirker ikke en opdateret udvidelse (version 1.1.5), der kan installeres. Den væsentligste effekt vil være på den forældede udvidelse (version 1.1.4). Chatrobotten i denne version holder op med at fungere. Fanen **Fridage** fortsætter med at fungere i begge udvidelser.

I version 1.1.4 holder chatrobotten op med at svare på enhver meddelelse. For eksempel **Log på**, **Vis saldi** og **Se fridage**. Appen skal opdateres manuelt til den seneste version. Du kan finde flere oplysninger i [Opdatere apps i Microsoft Teams](/MicrosoftTeams/apps-update-experience).

Udfør følgende trin for at opdatere til version 1.1.5:
1. Gå i Microsoft Teams til **Apps**.
2. Find appen **Human Resources**.
3. Vælg **Opgrader**.

Du kan kontrollere versionen af appen Human Resources ved enten at gå til fanen **Om** eller ved at gå til afsnittet **Personlig app**. 

![Human Resources-fanen **Om**.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Aktivere beskeder for appen Human Resources i Teams

Hvis du ønsker, at brugere skal kunne modtage beskeder om orlov i appen Teams, skal du aktivere beskeder i Dynamics 365 Human Resources.

>[!NOTE]
>Kun brugere, der er logget på Teams og bruger Dynamics 365 Human Resources Teams-appen, modtager beskederne.

1. I Human Resources skal du vælge **Systemadministration**.

2. Vælg **Links**.

3. Vælg **Systemparametre** under **Opsætning**.

4. Under fanen **Generelt** skal du angive **Aktivér beskeder for Teams-app** til **Ja**.

   ![Aktivere beskeder for appen Teams i systemparametre.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Hvis du vil aktivere Teams-beskeder for alle brugere, skal du vælge **Ja** ved prompten.

   ![Aktivere Teams-beskeder for alle brugere.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Slå Teams-beskeder til eller fra for de enkelte brugere

Når du har aktiveret beskeder for Teams-appen Dynamics 365 Human Resources, kan du slå beskeder til eller fra for de enkelte brugere.

1. I Human Resources skal du vælge **Systemadministration**.

2. Vælg **Links**.

3. Vælg **Brugerindstillinger** under **Brugere**.

4. Vælg fanen **Arbejdsgang**.

5. Indstil **Aktivér beskeder for Teams-app** til **Ja** for at aktivere beskeder for brugeren eller **Nej** for at deaktivere beskeder for brugeren.

   ![Aktivér beskeder for Teams-app i Brugerindstillinger under fanen Arbejdsgang.](./media/hr-admin-teams-leave-app-notifications.png)

6. Vælg **Gem**.

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

## <a name="notes"></a>Notater

Følgende arbejdselementer oversættes i fremtidige versioner:

| Workflowopgave | Status |
| --- | --- |
| Saldoen er forkert, når der angives fri for en fremtidig dato. | Prognosefunktion er ikke tilgængelig endnu. Saldoen viser den aktuelle dato. |
| Kan ikke annullere en anmodning **Til gennemsyn**. | Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version. |
| Saldooplysninger beregnes pr. dags dato. | Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret på siden **Orlovs- og fraværsparametre**. |

## <a name="troubleshooting"></a>Fejlfinding

Hvis en bruger har problemer med at logge på eller bruge appen Human Resources Teams, kan brugeren prøve at følge disse fejlfindingsinstruktioner. Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support. Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Sørg for, at Human Resources-programmet i Teams er opdateret
Hvis der opstår problemer med Teams-appen Human Resources, skal du kontrollere, at du kører den seneste version. Den version, der som minimum understøttes, er 1.1.5. Du kan finde oplysninger om, hvordan du opdaterer et Teams-program, i [dokumentationen til Teams](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Der kan ikke logge på appen Human Resources i Teams

Hvis en bruger kontakter dig, fordi vedkommende ikke kan logge på appen, skal du kontrollere, at brugeren har en tilknyttet medarbejderpost i Human Resources.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams

Hvis en bruger modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du afprøve følgende fejlfindingstrin:

1. Kontrollér, at deres Teams-konto er den samme, som de bruger til at få adgang til Human Resources.

2. Kontrollér, at de er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse. Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Orlovsgodkendere modtager ikke Teams-chatmeddelelser til godkendelse af orlovsanmodninger

1. Sørg for, at beskeder er aktiveret for miljøet og brugeren. Du kan finde flere oplysninger i [Aktivere beskeder for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Slå Teams-beskeder til eller fra for individuelle brugere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Sørg for, at brugere er logget under fanen **Chatbeskeder** med de samme legitimationsoplysninger, som de bruger til at godkende orlovsanmodninger. Brug meddelelserne for "Log af" og derefter "Log på" for at logge på med de rette legitimationsoplysninger.

3. Hvis problemet fortsætter, skal du kontrollere statussen for systembatchjobbet **Forretningshændelser** som systemadministrator. Hvis det er i **Venter**- eller **Udfører**-fasen, skal du tjekke igen om et par minutter. Hvis statussen forbliver uændret, skal du logge en supportanmodning, så vores team kan hjælpe med at løse problemet.

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
[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
