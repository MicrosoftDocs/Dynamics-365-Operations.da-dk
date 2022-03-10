---
title: Konfigurere generelle budgetreservationer og sende dem til en arbejdsgang
description: I dette emne beskrives, hvordan du kan konfigurere generelle budgetreservationer og sende dem til en arbejdsgang for den offentlige sektor.
author: AlexRenney
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetReservation_PSN, BudgetReservationType_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: ea066a437868c4e5c0bdb28323bb7d5300b8c8cde8c3de0fcb0c7866d103c5ed
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766256"
---
# <a name="set-up-general-budget-reservations-and-submit-them-to-a-workflow"></a>Konfigurere generelle budgetreservationer og sende dem til en arbejdsgang

[!include [banner](../includes/banner.md)]

Når en generel budgetreservation er konfigureret til at bruge en arbejdsgang, skal dokumentet først sendes og godkendes via arbejdsgangssystemet. Når arbejdsgangen er fuldført, og reservationen er godkendt, kan du stadig redigere dokumentet. Selvom det er muligt at bogføre dokumentet, er ingen andre kontrolelementer og felter på siden tilgængelige, medmindre du vælger indstillingen til redigering af dokumentet. Bemærk, at hvis du redigerer en godkendt reservation, nulstilles arbejdsgangsstatussen til **Kladde**, og det er ikke længere muligt at bogføre dokumentet. De andre kontrolelementer og felter på siden er dog tilgængelige. Når du har ændret en reservation, skal du sende den til godkendelse i arbejdsgangssystemet igen.

Følgende illustration viser, hvordan du konfigurerer en arbejdsgang til generelle budgetreservationer. Hvert nummereret trin svarer til et afsnit i dette emne.

![Konfiguration af en arbejdsgang for generel budgetreservation.](media/gbr-workflow-process.jpg "Konfiguration af en arbejdsgang for generel budgetreservation")

## <a name="optional-set-up-reviewers-for-general-budget-reservations"></a>Valgfrit: Konfigurere validatorer til generelle budgetreservationer

Du kan konfigurere validatorer til arbejdsgangselementer for at sende generelle budgetreservationer til gennemsyn. Arbejdsgangen bruger den angivne ejer af projektrollen eller den angivne økonomiske dimension til at afgøre, hvem udgiften skal sendes videre til.

Du kan også tildele en bestemt bruger eller brugergruppe, der skal fungere som validator, når du definerer arbejdsgangen. Men hvis du har en kompleks organisation, kan du effektivisere godkendelsesprocessen ved at angive validatorelementer. På denne måde behøver du ikke ændre tildelingerne af arbejdsgangsvalidator, hver gang en validator skifter jobrolle.

## <a name="create-a-general-budget-reservation-workflow"></a>Oprette en arbejdsgang for generel budgetreservation

Arbejdsgange for generelle budgetreservationer er baseret på reservationstypen. Du kan derfor oprette flere arbejdsgange for generelle budgetreservationer.

Hvis en generel budgetreservation kræver en indkøbsrekvisition, skal du være opmærksom på, at indkøbsrekvisitioner kræver deres egen arbejdsgang. Arbejdsgangen for indkøbsrekvisitionen skal være fuldført, før den generelle budgetreservation kan henvise til den.

Benyt følgende fremgangsmåde, hvis du vil oprette en arbejdsgang for en generel budgetreservation.

1. Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Arbejdsgang for budgettering**.
2. Vælg **Ny**.
3. Vælg skabelonen **Arbejdsgang for generel budgetreservation** i skyderen **Opret arbejdsgang**.
4. Vælg **Godkend generel budgetreservation** under **Godkendelser** i arbejdsgangseditoren i ruden **Arbejdsgangselementer**, og træk den derefter, så den er under **Start**-elementet på lærredet.
5. Træk i kanten af **Start**-elementet for at oprette en forbindelseslinje til godkendelseselementet.
6. Vælg godkendelseselementet, og vælg derefter **Grundlæggende indstillinger** for at konfigurere elementet.

## <a name="optional-configure-manual-and-automated-tasks-for-a-general-budget-reservation-workflow"></a>Valgfrit: Konfigurere manuelle opgaver og automatiserede opgaver i en arbejdsgang for en generel budgetreservation

Konfigurer manuelle og automatiserede opgaver for arbejdsgangen for den generelle budgetreservation, så arbejdsgangen afspejler de godkendelses- eller gennemsynsopgaver, der er en del af din forretningspraksis:

- En manuel evaluering af en generel budgetreservation
- En automatiseret proces til evaluering af feltværdier for en generel budgetreservation

Du kan bruge en kombination af disse opgaver i samme arbejdsgang. Manuelle gennemsynsopgaver og elementer i godkendelsesarbejdsgange er forskellige på følgende måde:

- Hvis du tildeler den manuelle gennemsynsopgave til flere brugere, kan arbejdsgangen fortsætte, efter en af disse brugere fuldfører opgaven.
- Hvis du tildeler et arbejdsgangselement til godkendelse til flere brugere, kan du angive, om alle disse brugere godkende dokumentet, før arbejdsgangen kan fortsætte.

Du kan definere **Emne for arbejdselement** og **Instruktioner til arbejdselement** for opgaven og tildele dem til en bruger, der er godkendt til at gennemse de linjer, der findes i den generelle budgetreservation.

## <a name="optional-create-conditional-decisions"></a>Valgfrit: Opret betingede beslutninger

Opret betingede beslutninger, hvis dine forretningsprocesser kræver forskellige arbejdsgange, afhængigt af beløbet for den generelle budgetreservation. Du kan også oprette betingede beslutninger, der er baseret på regnskabsdatoen, reservationstypen, reservationstitlen, start- eller slutdatoen og andre kriterier.

## <a name="assign-participants-to-workflow-elements"></a>Tilknytning af deltagere til arbejdsgangselementer

Du kan knytte arbejdsgangselementer til følgende deltagergrupper.

| Brugergruppe                 | Beskrivelse |
|----------------------------|-------------|
| Sikkerhedsrolledeltagere | Knyt arbejdsgangselementet til en Microsoft Dynamics 365-sikkerhedsrolle. Du kan bruge denne indstilling, hvis en gruppe arbejdere kan godkende generelle budgetreservationer, og det er ligegyldigt, hvilken person der godkender et bestemt dokument. |
| Brugergruppedeltagere    | Tildel arbejdsgangselementet til en Dynamics 365-brugergruppe. Du kan bruge denne indstilling, hvis en gruppe arbejdere kan godkende generelle budgetreservationer, og alle i den gruppe kan godkende et bestemt dokument. |

Arbejdsgangselementer kan også tildeles ud fra et hierarki eller en bruger.

## <a name="save-the-workflow"></a>Gemme arbejdsgangen

Når du er færdig med at tilføje arbejdsgangselementer, kan du bruge følgende procedure til at kontrollere arbejdsgangen for fejl og derefter gemme den.

I ruden **Fejl og advarsler** nederst i arbejdsgangseditoren vises meddelelser, der er genereret i forbindelse med arbejdsgangen. Du kan finde det element, hvor der opstår en fejl eller advarsel, ved at dobbeltklikke på fejl- eller advarselsmeddelelsen. Alle fejl skal rettes og advarsler afhjælpes, før du kan aktivere arbejdsgangen.

1. Når arbejdsprocessen er fuldført og fejlfri, skal du vælge **Gem og luk**.
2. Vælg **OK** i dialogboksen **Gem arbejdsgang**.
3. Hvis du vil aktivere arbejdsgangen nu, skal du vælge **OK** i dialogboksen **Aktiver arbejdsgang**.

    eller

    Hvis du vil aktivere arbejdsgangen senere, skal du benytte følgende fremgangsmåde:

    1. Gå til **Budgettering \> Opsætning \> Grundlæggende budgettering \> Arbejdsgang for budgettering**.
    2. Vælg den arbejdsgang, du har oprettet.
    3. I handlingsruden under fanen **Arbejdsgang** i gruppen **Administrer** skal du vælge **Versioner**.
    4. I skyderen **Arbejdsgangsversioner** skal du vælge den ønskede version af arbejdsgangen.
    5. Vælg **Gør den aktiv**, og vælg derefter **Luk**.

## <a name="submit-a-general-budget-reservation-to-the-workflow-system"></a>Sende en generel budgetreservation til arbejdsgangssystemet

Hvis du vil sende en generel budgetreservation til arbejdsgangssystemet, skal du være klargører. Før du kan sende en reservation, skal alle obligatoriske felter udfyldes, og reservationen skal indeholde mindst ét linjeelement. Reservationen skal have arbejdsgangsstatussen **Kladde**.

Benyt følgende fremgangsmåde, hvis du vil sende en generel budgetreservation til arbejdsgangssystemet.

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Vælg den generelle budgetreservation, der skal sendes til arbejdsgangssystemet.
3. Vælg **Send** i handlingsruden.
4. Valgfrit: Tilføj en note i feltet **Kommentar**.
5. Vælg **Send**. Reservationsstatussen flyttes til det næste trin i arbejdsgangen.
6. Knappen **Send** i handlingsruden bliver til en **Arbejdsgang**-knap. Når du vælger denne knap, åbnes der en menu. Du kan til enhver tid bruge denne menu til at udføre følgende opgaver:

    - Få vist historikken og se, hvor dokumentet er i arbejdsgangen.
    - Hvis reservationen stadig er i arbejdsgangen, skal du tilbagekalde status for arbejdsgangen til **Kladde**-status. Derefter kan du foretage de nødvendige ændringer af reservationen og sende den til arbejdsgangssystemet igen.

    Efterhånden som reservationen bevæger sig gennem arbejdsgangen, afspejles reservationsstatussen og ændringen i statussen for arbejdsgangen i headeren til den generelle budgetreservation.

7. Når arbejdsgangen er fuldført, og reservationens har status **Godkendt**, kan du bogføre dokumentet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]