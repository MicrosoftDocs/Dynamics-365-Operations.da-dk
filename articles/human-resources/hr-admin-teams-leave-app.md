---
title: Appen Personale i Teams
description: I dette emne introduceres Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776302"
---
# <a name="human-resources-app-in-teams"></a>Appen Personale i Teams

[!include [banner](includes/preview-feature.md)]

Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres flekskontooplysninger i Microsoft Teams. Medarbejderne kan interagere med en bot for at anmode om oplysninger. Fanen **Fridage** giver mere detaljerede oplysninger.

![Orlov via appbot i Personale i Teams](./media/hr-admin-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Installere og konfigurere

Du kan finde Personale-appen i storen til Teams. Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).

Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Aktivere beskeder for appen Personale i Teams

Hvis du ønsker, at brugere skal kunne modtage beskeder om orlov i appen Teams, skal du aktivere beskeder i Personale.

>[!NOTE]
>Kun brugere, der er logget på Teams og bruger Teams-appen Personale, modtager beskederne.

1. I Personale skal du vælge **Systemadministration**.

2. Vælg **Links**.

3. Vælg **Systemparametre** under **Opsætning**.

4. Under fanen **Generelt** skal du angive **Aktivér beskeder for Teams-app** til **Ja**.

   ![Aktivere beskeder for appen Teams i systemparametre](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Hvis du vil aktivere Teams-beskeder for alle brugere, skal du vælge **Ja** ved prompten.

   ![Aktivere Teams-beskeder for alle brugere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Slå Teams-beskeder til eller fra for de enkelte brugere

Når du har aktiveret beskeder for Teams-appen Personale, kan du slå beskeder til eller fra for de enkelte brugere.

1. I Personale skal du vælge **Systemadministration**.

2. Vælg **Links**.

3. Vælg **Brugerindstillinger** under **Brugere**.

4. Vælg fanen **Arbejdsgang**.

5. Indstil **Aktivér beskeder for Teams-app** til **Ja** for at aktivere beskeder for brugeren eller **Nej** for at deaktivere beskeder for brugeren.

   ![Aktivér beskeder for Teams-app i Brugerindstillinger under fanen Arbejdsgang](./media/hr-admin-teams-leave-app-notifications.png)

6. Vælg **Gem**.

## <a name="known-issues"></a>Kendte problemer

| Udsted | Status |
| --- | --- |
| Vandret rulning fungerer ikke på Android-telefoner | Vandret rulning er ikke et problem på iOS-enheder eller stationære computere. Vi arbejder på at løse problemet for Android. |
| Fejl: Der er problemer med at finde et miljø, der skal oprettes forbindelse til. | Du kan få vist denne fejl, selvom du har bekræftet, at brugeren kan få adgang til et eller flere personalemiljøer (HR). Du kan heller ikke se alle de miljøer, du forventer. sIndtil dette problem er løst, skal du slette brugeren og derefter importere vedkommende igen for at løse problemet. |
| Saldoen er forkert, når der angives fri for en fremtidig dato. | Prognosefunktion er ikke tilgængelig endnu. Saldoen viser den aktuelle dato. |
| Kan ikke annullere en anmodning **Til gennemsyn**. | Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version. |
| Saldooplysninger beregnes pr. dags dato. | Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret i orlovs- og fraværsparametre. |

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål. Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service). Læs mere om LUIS [her](https://www.luis.ai/). LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso). Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen. 

Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse. LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources. Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen. 

Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten. Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure Event Grid og Microsoft Teams

Når du bruger beskedfunktionen til Dynamics 365 Human Resources-appen i Teams, vil visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret. Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams. Disse data kan gemmes i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.

## <a name="see-also"></a>Se også 

[Downloade og installere Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams Hjælp-center](https://support.office.com/teams)</br>
[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md)

