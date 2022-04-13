---
title: Dato- og klokkeslætsparametre, der bruges af planlægningsoptimering
description: Dette emne indeholder oplysninger om parametrene for dato og klokkeslæt, som planlægningsoptimering bruger under driften.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468826"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Dato- og klokkeslætsparametre, der bruges af planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Dette emne indeholder oplysninger om parametrene for dato og klokkeslæt, som planlægningsoptimering bruger under driften.

Mens det indbyggede program til varedisponering bruger transaktionsdatoer i alle beregninger, arbejder planlægningsoptimering med dato- og tidsværdier, der konverteres til datoer. Denne forskel i adfærd kan føre til situationer, hvor prognosetransaktioner, der f.eks. er oprettet ved midnat den dag, hvor der køres varedisponering, ikke er medtaget, da planlægningsoptimering mener, at de var oprettet før dags dato.

## <a name="parameters-for-issue-and-demand-transactions"></a>Parametre for afgangs- og efterspørgselsposteringer

Følgende tabel indeholder de parametre, som planlægningsoptimering bruger, når programmet behandler afgangs- og efterspørgselstransaktioner.

| Parameter | Parameternavn i planlægningsoptimering | Beskrivelse | Tilsvarende felt i Microsoft Dynamics 365 Supply Chain Management (i tabellen ReqTrans) |
|---|---|---|---|
| Planlagt afgangstidspunkt | `PlannedIssueTime` | Den dato, som afgangen aktuelt er planlagt til. | **Til dato** (`FuturesDate`) og **Forsinket til tid** (`FuturesTime`) |
| Ønsket afgangstid | `RequestedIssueTime` | Den afgangsdato, som brugeren har anmodet om og er angivet i Supply Chain Management. Denne parameter gælder kun for frigivne eller godkendte ordreforslag. For ordreforslag er den som standard tom. | **Ønsket dato** (`ReqDateDlvOrig`) |
| Påkrævet afgangstid | `RequiredIssueTime` | Den påkrævede afgangsdato, der justeres af planlægningsoptimering. Hvis den ønskede afgangstid er i fortiden, når planlægningsoptimering køres, justeres den påkrævede afgangstid til den første åbne dag, der ikke ligger før dags dato. Hvis den ønskede afgangstid er markeret som blokeret i kalenderen, justeres den påkrævede afgangstid til den første åbne dag før denne dato. | **Behovsdato** (`ReqDate`) og **Behovstidspunkt** (`ReqTime`) |
| Tidsforsinkelse for afgang | `IssueTimeDelay` | Tidsforskellen mellem den planlagte afgangstid og enten den ønskede afgangstid for godkendte og frigivne ordrer eller den påkrævede afgangstid. | **Forsinkelse (i dage)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Parametre for tilgangs- og forsyningstransaktioner

Følgende tabel indeholder de parametre, som planlægningsoptimering bruger, når programmet behandler tilgangs- og forsyningstransaktioner.

| Parameter | Parameternavn i planlægningsoptimering | Beskrivelse | Tilsvarende felt i Supply Chain Management (i tabellen ReqTrans eller ReqPO) |
|---|---|---|---|
| Planlagt tilgængelighedstid | `PlannedAvailabilityTime` | Den dato, hvor tilgangen er planlagt til at være tilgængelig. | **Behovsdato** (`ReqDate`) og **Behovstidspunkt** (`ReqTime`) |
| Planlagt tilgangstid | `PlannedReceiptTime` | Den dato, hvor tilgangen ankommer til lokationen. | **Til dato** (`FuturesDate`), **Forsinket til tid** (`FuturesTime`) og **Leveringsdato** (`ReqDateDlv`) eller **Ønsket dato** (`ReqDateDlvOrig`), hvis ordren endnu ikke er frigivet. |
| Påkrævet tilgængelighedstid | `RequiredAvailabilityTime` | Den påkrævede tilgængelighedsdato, der justeres af planlægningsoptimering. | **Behovsdato** (`ReqDate`) og **Behovstidspunkt** (`ReqTime`) |
| Forventet tilgangstid | `ExpectedReceiptTime` | Den forventede tilgangsdato for en frigivet tilgang. Værdien angives af brugeren i Supply Chain Management og justeres ikke af planlægningsoptimering. Denne parameter gælder kun for frigivne tilgange. | **Ønsket dato** (`ReqDateDlvOrig`) |
| Påkrævet tilgangstid | `RequiredReceiptTime` | Den påkrævede tilgangsdato, der justeres af planlægningsoptimering. | **Behovsdato** (`ReqDate`) og **Behovstidspunkt** (`ReqTime`) |
| Planlagt bestillingstid | `PlannedOrderingTime` | Den bestillingsdato, der beregnes af planlægningsoptimering. | **Ordredato** (`ReqDateOrder`) og **Ordretidspunkt** (`ReqTimeOrder`) |
| Starttid for planlagt aktivitet | `PlannedActivityStartTime` | Den dato, hvor aktiviteten for denne tilgang skal starte. | **Startdato** (`SchedFromDate`) |
| Tidsforsinkelse for tilgang | `ReceiptTimeDelay` | Tidsforskellen mellem den planlagte tilgangstid og den påkrævede tilgangstid. | **Forsinkelse (dage)** (`FuturesDays`) og **Forsinket til tid** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Eksempler på datoparametre, der bruges af planlægningsoptimering

Planerne i følgende illustrationer er på dagsniveau, men planlægningsoptimering køres på et mere detaljeret niveau. Da margener f.eks. kan være i timer, kan planlægningsordretiden være 22. januar 2021 kl. 11:35 osv.

### <a name="example-1-simple-scenario"></a>Eksempel 1: Simpelt scenario

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. Følgende indstillinger bruges:

- Ingen gennemløbstid
- Ingen kalendere (alle dage er åbne).
- Ingen margener

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Simpelt scenario.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Eksempel 2: Scenario for gennemløbstid

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. Følgende indstillinger bruges:

- Tre dages gennemløbstid
- Ingen kalendere (alle dage er åbne).
- Ingen margener

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Scenario for gennemløbstid.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Eksempel 3: Margenscenario

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. Følgende indstillinger bruges:

- Tre dages gennemløbstid
- Bestillingsmargen på fire dage
- Tilgængelighedsmargen på fem dage
- Ingen kalendere (alle dage er åbne).

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Margenscenario.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Eksempel 4: Forsinkelsesscenario

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. I dette eksempel bruges de samme indstillinger som i eksempel 3, men planlægningsdatoen er flyttet til 15. januar. Planlægning bagud (røde markeringer) mislykkes, fordi den planlagte bestillingstid skulle være før dags dato. Derfor skal varedisponering planlægges fremad og give forsinkelser.

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Forsinkelsesscenario.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Eksempel 5: Flyttescenario

En salgsordre fra lagersted 1, der har ønsket afgangstid den 22. januar, dækkes af én flytteordre fra lagersted 2, der dækkes af et indkøbsordreforslag. Følgende indstillinger bruges:

- Tre dages gennemløbstid for flytning (lagersted 1)
- To dages gennemløbstid for indkøb (lagersted 2)
- Ingen kalendere (alle dage er åbne).

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Flyttescenario.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Eksempel 6: Gennemløbstid med kalenderscenario

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. Følgende indstillinger bruges:

- Tre dages gennemløbstid
- Afgangskalender (lukket fredag)
- Tilgængelighedskalender (lukket torsdag og fredag)
- Tilgangskalender (lukket tirsdag, onsdag og søndag)
- Kalender for gennemløbstid (lukket torsdag og fredag)
- Bestillingskalender (åben mandag og lørdag)

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Gennemløbstid med kalenderscenario.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Eksempel 7: Forsinkelse med kalenderscenario

En salgsordre, der har en ønsket afgangstid den 22. januar, dækkes af én indkøbsordre. I dette eksempel bruges de samme indstillinger som i eksempel 6, men planlægningsdatoen er flyttet til 13. januar. Planlægning bagud (røde markeringer) mislykkes, fordi den planlagte bestillingstid skulle være før dags dato. Derfor skal varedisponering planlægges fremad og give forsinkelser.

Følgende illustration viser dette scenario. (Vælg illustrationen for at åbne en større version.)

[![Forsinkelse med kalenderscenario.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
