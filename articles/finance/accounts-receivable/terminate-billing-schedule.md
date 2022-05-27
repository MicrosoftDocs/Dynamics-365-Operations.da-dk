---
title: Afslutte faktureringsplaner
description: Dette emne indeholder en forklaring på, hvordan faktureringsplaner og faktureringsplanlinjer afsluttes i abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e823ce950d6a4687dc7cda14e06bffdbb4f37f7e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690970"
---
# <a name="terminate-billing-schedules"></a>Afslutte faktureringsplaner

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan faktureringsplaner og faktureringsplanlinjer afsluttes i abonnementsfakturering. Når du afslutter en faktureringsplan, skal den have statussen **Aktiv**. Den kan ikke have statussen **Venter**. Når du afslutter en faktureringsplanlinje, skal den også have statussen **Aktiv**. Hovedsektionen i faktureringsplanen påvirkes ikke, når du afslutter en faktureringsplanlinje.

Hvis du vil afslutte en faktureringsplan eller faktureringsplanlinje, skal du gå til et af følgende steder:

- Listesiden **Alle/Aktive faktureringsplaner**
- En specifik faktureringsplan på siden **Alle faktureringsplaner**
- En specifik faktureringsplanlinje på siden **Alle faktureringsplaner**

> [!NOTE]
> Hvis du vil afslutte flere faktureringsplaner på én gang, skal du bruge siden **Behandling af masseafslutning**.

## <a name="terminate-a-billing-schedule-or-line"></a>Afslutte en faktureringsplan eller linje

Hvis du vil afslutte en faktureringsplan eller faktureringsplanlinje, skal du følge disse trin.

1. Vælg en faktureringsplan eller en faktureringsplanlinje, og vælg derefter **Afslut**. 
2. Angiv felterne **Ophørsdato**, **Ophørstype** og **Årsagskode**.
3. Angiv feltet **Kreditindstilling** til **Udsted kredit**.
4. Vælg **Afslut**.

Status for faktureringsplanen ændres baseret på den valgte ophørstype. Hvis du har valgt **Resterende fakturering** som ophørstype, er statussen for alle linjer i faktureringsplanen **Sidste fakturering**. Statussen for faktureringsplanen forbliver **Aktiv**, indtil den sidste faktura er behandlet. Når den sidste faktura er behandlet, opdateres status til **Afsluttet**. Hvis du har valgt **Juster tidsplan** som ophørstype, bliver statussen for faktureringsplanen straks opdateret til **Afsluttet**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Afslutte en faktureringsplan eller linje og anvende en refusion

Hvis du vil afslutte en faktureringsplan eller faktureringsplanlinje og anvende en refusion, skal du følge disse trin.

1. Vælg en faktureringsplan eller en faktureringsplanlinje, og vælg derefter **Afslut**.
2. Angiv felterne **Ophørsdato**, **Ophørstype**, **Årsagskode** og **Kreditindstilling**.
3. Vælg **Afslut med refusion**. Siden **Behandling af masseafslutning** vises og filtreres, så den viser faktureringsplanen.
4. Vælg **Vis eksempel** for at se faktureringsplanlinjerne, og vælg derefter **Behandling**.

Når kreditten er behandlet, skal du åbne siden **Vis faktureringsdetaljer** for at gennemse den kredit, der er anvendt på faktureringsplanen. Hvis kreditbeløbet er større end 0 (nul), slettes alle fremtidige ikke-fakturerede linjer, og de erstattes med faktureringsdetaljelinjer, som viser de negative beløb for den kredit, der blev anvendt på faktureringsplanen.

### <a name="view-example"></a>Vis eksempel

En faktureringsplan har følgende oplysninger:

- Startdatoen er 1. januar 2020.
- Slutdatoen er 31. december 2020.
- Beløbet for faktureringsperioden er 100,00 pr. måned.
- Der er oprettet fakturaer for faktureringsperioder fra januar til og med juli.
- Kontraktens ophørsdato er 15. juni 2020.

Når kreditreguleringen er behandlet, fjernes alle fremtidige faktureringsperioder (august til december) fra siden **Vis faktureringsdetaljer**. Der tilføjes en kreditreguleringslinje efter faktureringsperioden for juli:

- 16. juni – 31. juli, med et kreditbeløb på 150,00

Hvis funktionen for ikke-faktureret omsætning bruges, opdateres siden **Revision af ikke-faktureret indtægtskladdepost** med ophørsposten.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Afslutte en faktureringsplan eller linje uden at anvende en kredit

Hvis du vil afslutte en faktureringsplan eller faktureringsplanlinje uden at anvende en kredit, skal du følge disse trin.

1. Vælg en faktureringsplan eller en faktureringsplanlinje, og vælg derefter **Afslut**.
2. Angiv feltet **Ophørsdato**.
3. Angiv feltet **Ophørstype** til **Ingen regulering**. Feltet **Kreditindstilling** angives automatisk til **Ingen kredit**.
3. Angiv feltet **Årsagskode**.
4. Udfyld eventuelt feltet **Ophørsnoter** med nødvendige bemærkninger.
5. Vælg **Afslut**. 

Når afslutningen er behandlet, fjernes alle faktureringsdetaljelinjer efter ophørsdatoen. (Disse linjer omfatter den linje, der indeholder ophørsdatoen). Der kan ikke oprettes fakturaer for linjerne, der er afsluttet. Hvis afslutningen fjernes, føjes alle afsluttede linjer tilbage til siden **Vis faktureringsdetaljer** og bliver tilgængelige for fakturering.

## <a name="fields"></a>Felter

Siden **Vis faktureringsdetaljer** indeholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------| 
| Ophørsdato | Vælg den dato, hvor du vil afslutte en faktureringsplan eller faktureringsplanlinje. |
| Ophørstype | <p>Vælg ophørstypen:</p><ul><li>**Juster tidsplan** – Afskær faktureringsperioderne for linjen på ophørsdatoen, og rediger status for linjen til **Sidste fakturering**. Hvis der findes en udskydelsesplan for linjeelementet, reguleres den ved at tilbageføre det beløb, der ikke længere må anerkendes. Hvis faktureringsstartdatoen ligger efter ophørsdatoen, fjernes de resterende faktureringsperioder.</li><li>**Resterende fakturering** – Føj et eventuelt restbeløb for faktureringsperioden til ophørsperioden, og ret status for linjen til **Sidste fakturering**. Hvis der findes en udskydelsesplan for linjeelementet, opdateres slutdatoen for udskydelsen. Hvis faktureringens startdato ligger efter ophørsdatoen, føjes det samlede beløb for alle resterende faktureringsperioder til faktureringsperioden, og de resterende faktureringsperioder fjernes.</li><li>**Ingen regulering** – Afslut faktureringsperioderne for linjen på den angivne ophørsdato. Der foretages ingen reguleringer. Når denne ophørstype er valgt, angives feltet **Kreditindstilling** til **Ingen kredit**, og feltet **Daglig forholdsmæssig beregning** angives til **Nej**. Begge disse felter bliver skrivebeskyttede og kan ikke ændres.</li></ul> |
| Kreditindstilling | <p>Vælg, hvordan kreditten skal anvendes, når du afslutter en faktureringsplanlinje:</p><ul><li>**Kreditregulering** – Opret en kreditregulering for en faktureringsplan, når en linje afsluttes. Kreditreguleringen vises i en fremtidig faktureringsperiode for faktureringsplanen. Reguleringen justerer også automatisk fakturabeløbet for den næste faktureringsperiode, indtil kreditten er anvendt færdig på faktureringsplanen.</li><li>**Udsted kredit** – Opret en kreditnota, når en faktureringsplan eller faktureringsplanlinje afsluttes.</li><li>**Ingen kredit** – Opret ikke en kreditregulering eller kreditnota, når en faktureringsplan eller faktureringsplanlinje afsluttes. Denne indstilling er kun tilgængelig, når du bruger et ophør af typen **Ingen regulering** til at afslutte en faktureringsplan.</li></ul><p>Standardindstillingen er fra siden **Faktureringsparametre for tilbagevendende kontrakter**.</p> |
| Årsagskode | Vælg årsagskoden til afslutningen. |
| Beskrivelse af årsag | Beskrivelsen af årsagskoden. |
| Opsigelsesvarsler | Angiv evt. noter om afslutningen. |

<!--## Additional information-->
