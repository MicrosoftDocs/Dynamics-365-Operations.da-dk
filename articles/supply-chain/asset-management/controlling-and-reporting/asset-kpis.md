---
title: KPI'er for aktiver
description: I dette emne beskrives KPI'er for aktiver i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1aee14c869d84bef38a738bfe78fd09ee7f82d94
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652373"
---
# <a name="asset-kpis"></a>KPI'er for aktiver

[!include [banner](../../includes/banner.md)]

 

I Styring af aktiver kan du beregne forskellige KPI'er (nøgletal) for aktiver og aktivtyper. Du kan bruge KPI'er til at få vist en oversigt over aktivernes præstation i forhold til f.eks. oppetid, nedetid, reparationstid og MTBF (Mean Time Between Failure - gennemsnitstid mellem fejl).

1. Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **KPI'er for aktiver**.

2. I dialogboksen **Beregn aktiv-KPI'er** vælger du den **Tidsskala**, der skal bruges i beregning, og en periode i felterne **Fra-dato** og **Til-dato**. 

3. I oversigtspanelet **Poster, der skal indgå**, kan du vælge bestemte aktiver og aktivtyper, der skal medtages i beregningen, hvis det er nødvendigt.

4. Klik på **OK** for at starte beregningen.

5. Resultaterne af beregningen vises i gittervisning i oversigtspanelet **Oversigt**. Hvert aktiv vises på en separat linje.

6. I oversigtspanelet **KPI'er for den valgte linje** kan du se beregninger for det aktiv, der er valgt i oversigtspanelet **Oversigt**. KPI-værdierne er kategoriseret efter **Tid**, **Tilgængelighed**, **Arbejdsordrer**, **Vedligeholdelse**, **Fejl**, **Vedligeholdelsesnedetid** og **Omkostninger**.

I tabellen nedenfor kan du finde en beskrivelse af felterne på siden **KPI'er for aktiver**.

| Felt                   | Beskrivelse                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aktiv                   | Aktiv-id.                                                                                                                                                                                                                                                                                             |
| Samlet tid              | Den samlede tid, der er konfigureret i kalenderen, som bruges i beregningen. Hvis aktivet er relateret til en ressource, bruges den relaterede ressourcekalender. Hvis aktivet ikke er relateret til en ressource, bruges den kalender, der er valgt i feltet **Standardkalender**, i **Parametre til aktivstyring**. |
| Oppetid                  | Samlet tid minus nedetid.                                                                                                                                                                                                                                                                            |
| Nedetid                | Registreringer af vedligeholdelsesnedetid, der er foretaget på aktivet i den valgte periode.                                                                                                                                                                                                                              |
| Reparationstidspunkt             | Det samlede antal arbejdstimer, der er brugt på arbejdsordrer for reparation.                                                                                                                                                                                                                                            |
| Tilgængelighed i %          | Oppetid divideret med samlet tid og multipliceret med 100.                                                                                                                                                                                                                                                   |
| Antal fejl        | Antallet af fejlårsager, der er registreret på fejlsymptomer for aktivet i den valgte periode.                                                                                                                                                                                                             |
| MTBF                    | MTBF (Mean Time Between Failure - gennemsnitstid mellem fejl), hvilket er den samlede tid divideret med antallet af fejl, der er registreret på aktivet i den valgte periode. Hvis antallet af fejl er nul, angives MTBF til samlet tid.                                                                                                                   |
| Fejlrate               | 1 divideret med MTBF.                                                                                                                                                                                                                                                                                    |
| MRT                     | Mean Repair Time, hvilket er reparationstid divideret med antallet af fejl, der er registreret på aktivet i den valgte periode. Hvis antallet af fejl er nul, angives MRT til reparationstid.                                                                                                                           |
| Antal stop         | Antal registreringer af vedligeholdelsesnedetid, der er oprettet på aktivet.                                                                                                                                                                                                                                     |
| MTBS                    | Mean Time Between Stops, hvilket er den samlede tid divideret med antal registreringer af vedligeholdelsesnedetid. Hvis antal registreringer af vedligeholdelsesnedetid er nul i den valgte periode, angives værdien af MTBS til samlet tid.                                                                                      |
| Forebyggende omkostning         | Omkostninger, der er bogført på aktivet for omkostningstypen "Forebyggende" i den valgte periode. Omkostningstyper konfigureres i arbejdsordretyper.                                                                                                                                                                       |
| Korrigerende omkostning         | Omkostninger, der er bogført på aktivet for omkostningstypen "Korrigerende" i den valgte periode. Omkostningstyper konfigureres i arbejdsordretyper.                                                                                                                                                                       |
| Erstatningsværdi       | Den værdi, der er defineret for aktivet som genanskaffelsespris.                                                                                                                                                                                                                                                  |
| Aktivtype             | Identifikation af den aktivtype, der er valgt på aktivet.                                                                                                                                                                                                                                             |
| Producent           | Identifikation af den producent, der er valgt på aktivet.                                                                                                                                                                                                                                                 |
| Model                   | Identifikation af den producentmodel, der er valgt på aktivet.                                                                                                                                                                                                                                           |
| Fra-dato               | Startdato for KPI-beregningen. Hvis aktivet er oprettet efter den startdato, der er valgt for beregningen, vises aktivets startdato i dette felt.                                                                                                                                  |
| Til-dato                 | Slutdato for KPI-beregningen. Hvis aktivet er registreret som inaktivt før den slutdato, der er valgt til beregningen, vises den dato, hvorfra aktivet ikke længere var aktivt, i dette felt.                                                                                               |
| Tidsskala              | Under beregning af KPI'erne skal du vælge en tidsskala, der skal bruges: timer, dage eller uger.                                                                                                                                                                                                            |
| Tilgængelighed            | Oppetid divideret med samlet tid.                                                                                                                                                                                                                                                                         |
| Arbejdsordrer             | Det samlede antal arbejdsordrer, der er medtaget i KPI-beregningen.                                                                                                                                                                                                                                          |
| Arbejdsordretid         | Det samlede antal arbejdstimer, der er brugt på arbejdsordrerne.                                                                                                                                                                                                                                               |
| Primære arbejdsordrer     | Antal primære arbejdsordrer, der er medtaget i KPI-beregningen.                                                                                                                                                                                                                                        |
| Sekundære arbejdsordrer   | Antal sekundære arbejdsordrer, der er medtaget i KPI-beregningen.                                                                                                                                                                                                                                      |
| Vedligeholdelsesarbejdsordrer | Antal arbejdsordrer for vedligeholdelse, der er medtaget i KPI-beregningen. En arbejdsordre for vedligeholdelse er en arbejdsordre uden relaterede fejlårsager.                                                                                                                                                             |
| Vedligeholdelsestid        | Det samlede antal arbejdstimer, der er brugt på arbejdsordrer for vedligeholdelse.                                                                                                                                                                                                                                       |
| Reparationsarbejdsordrer      | Antal arbejdsordrer for reparation, der er medtaget i KPI-beregningen. En arbejdsordre for reparation er en arbejdsordre med en relateret fejlårsag.                                                                                                                                                                        |
| Pålidelighed i %           | Beregning baseret på den forventede eksponentielle udvikling i fejlregistreringer på et aktiv, hvilket betyder, at aktivet bliver mindre pålideligt over tid på grund af slitage. Beregningen af denne KPI er baseret på MTBF og den samlede tid.                                                            |
| MTPS                    | Mean Time Production Stops, hvilket er vedligeholdelsesnedetid divideret med antal registreringer af vedligeholdelsesnedetid. Hvis antal registreringer af vedligeholdelsesnedetid er nul i den valgte periode, angives værdien af MTPS til nul.                                                                               |
| Totalomkostning              | De samlede omkostninger, der er bogført for aktivet i den valgte periode.                                                                                                                                                                                                                                              |
| Investeringsomkostning         | Omkostninger, der er bogført på aktivet for omkostningstypen "Investering" i den valgte periode. Omkostningstyper konfigureres i arbejdsordretyper.                                                                                                                                                                       |

I figuren herunder vises et skærmbillede af en KPI-beregning for fire aktiver.

![Skærmbillede af KPI-beregning for fire aktiver](media/11-controlling-and-reporting.png)

- Du kan vælge flere aktiver i **Alle aktiver** og klikke på knappen **KPI'er for aktiver** under fanen **Generelt**. Klik derefter på **OK** i dialogboksen **Beregn aktiv-KPI'er** for at beregne KPI'er for de valgte aktiver.  
- Resultater fra en KPI-beregning kan også omfatte [registreringer af vedligeholdelsesnedetid](../work-orders/maintenance-downtime.md) afhængigt af opsætning og brug af årsagskoder for vedligeholdelsesnedetid. 

