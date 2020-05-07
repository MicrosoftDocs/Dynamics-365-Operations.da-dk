---
title: Lagerrapport over lagerværdi
description: I dette emne forklares det, hvordan du kan køre en lagerrapport over lagerværdi og gøre outputtet digitalt tilgængeligt enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksporteret dokument i et af de tilgængelige formater.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 03426e86186c6aa283531eb37ae26527e6891042
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276898"
---
# <a name="inventory-value-storage-report"></a>Lagerrapport over lagerværdi

I dette emne forklares det, hvordan du kan køre en **lagerrapport over lagerværdi** og gøre outputtet digitalt tilgængeligt enten som en interaktiv side i Microsoft Dynamics 365 Supply Chain Management eller som et eksporteret dokument i et af de tilgængelige formater.

Når du får vist rapporten i din browser, reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det layout, som du har konfigureret. Du kan sortere resultaterne, filtrere dem, gå mere i dybden i dataene og meget mere.

Rapportresultater gemmes i dataenheden **Lagerværdi**. Du kan derfor filtrere og eksportere resultaterne til et format, f.eks. kommaseparerede værdier (CSV) eller Microsoft Excel-format.

**Lagerrapporten over lagerværdi** er nyttig, når outputtet indeholder mange linjer. Du har f.eks. 50.000 varer, og 300 butikker er oprettet som lagersteder. Hvis du i dette tilfælde anmoder om lagerafslutningssaldi pr. vare, sted og lagersted, indeholder outputtet mange linjer.

> [!NOTE]
> Rapporten omfatter ikke subtotaler, der er defineret i rapportlayoutet. Den omfatter heller ikke finanssaldi, selvom de er defineret i rapportlayoutet. Afstemning til finans skal ske ved hjælp af råbalance.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Aktivere lagerfunktionen for lagerværdi

Før du kan generere en **lagerrapport over lagerværdi**, skal du aktivere funktionen i systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul** – Omkostningsstyring
- **Funktionsnavn** – Lagerværdi af lager

## <a name="generate-an-inventory-value-storage-report"></a>Generere en lagerrapport over lagerværdi

Udfør følgende trin for at generere og gemme en **lagerrapport over lagerværdi**.

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerrapport over lagerværdi**.
1. Vælg **Ny**.
1. I dialogboksen **Lagerværdi** skal du angive følgende værdier for at definere, hvilke poster der skal medtages i rapporten:

    - Angiv et entydigt navn til rapporten i oversigtspanelet **Parametre**, og brug felterne i sektionen **Datointerval** til at definere, hvilke poster der skal medtages i rapporten. Hvis du vil definere datointervallet, kan du enten vælge et foruddefineret interval (i forhold til rapportgenereringsdatoen ) i feltet **Datointervalkode** eller vælge bestemte datoer i felterne **Fra dato** og **Til dato**. <!-- KFM: What is the ID setting for here? What do its values mean? -->
    - I oversigtspanelet **Poster, som skal medtages** skal du konfigurere filtre og begrænsninger for at definere, hvilke data der skal medtages i rapporten.
    - Angiv, hvordan, hvornår og hvor ofte rapporten skal genereres, i oversigtspanelet **Kør i baggrunden**.

    > [!NOTE]
    > Denne rapport køres altid som en del af et batchjob.

1. Vælg **OK** for at anvende dine indstillinger og dialogboksen.

Når batchjobbet er fuldført, vises rapporten på siden **Lagerrapport over lagerværdi**. Du skal måske opdatere siden for at se rapporten.

## <a name="explore-an-inventory-value-storage-report"></a>Undersøge en lagerrapport over lagerværdi

Når du har genereret en rapport, kan du til enhver tid se og udforske den på følgende måde.

1. Gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerrapport over lagerværdi**.
1. Vælg en rapport på listen.
1. Vælg **Vis detaljer** for at få vist rapportindholdet.
1. Undersøg rapporten ved at følge disse trin:

    - Du kan vælge næsten enhver kolonneoverskrift for at sortere eller filtrere gitteret efter værdier i kolonnen på samme måde som de fleste standardsider i Supply Chain Management.
    - Brug feltet **Filter** til at filtrere rapporten efter en hvilken som helst værdi i en af de tilgængelige kolonner.
    - Brug menuen Vis (oven over **Filter**-feltet) til at gemme og indlæse dine favoritkombinationer af sorterings- og filtreringsindstillinger.

## <a name="export-an-inventory-value-storage-report"></a>Eksportere en lagerrapport over lagerværdi

Hver rapport, du opretter, gemmes i dataenheden **Lagerværdi**. Du kan bruge standardfunktionerne til datastyring i Supply Chain Management til at eksportere data fra denne enhed til alle understøttede dataformater, herunder CSV eller Excel-format.

I følgende eksempel vises, hvordan du kan eksportere en **lagerrapport over lagerværdi**.

1. Gå til **Systemadministration \> Arbejdsområder \> Datastyring**.
1. Vælg feltet **Eksport** i sektionen **Import/eksport**. 
1. På siden **Eksport**, der vises, skal du konfigurere eksportjobbet. Angiv først et gruppenavn til jobbet.
1. Vælg **Tilføj enhed** i sektionen **Valgte enheder**.
1. Angiv følgende felter i den viste dialogboks:

    - **Enhedsnavn** – Vælg **Lagerværdi**.
    - **Målformat for data** – Vælg det format, der skal eksporteres data til.

1. Vælg **Tilføj** for at tilføje den nye række, og vælg derefter **Luk** for at lukke dialogboksen.
1. Normalt skal du eksportere én rapport ad gangen. Hvis du vil eksportere en enkelt rapport, skal du oprette et filter for den række, du lige har føjet til dialogboksen **Forespørgsel**. På denne måde kan du definere, hvilken rapport fra enheden **Lagerværdi** der skal medtages i eksporten. Følg disse trin for at angive følgende filterindstillinger for at eksportere en enkelt rapport:

    1. Under fanen **Område** skal du vælge **Tilføj** for at tilføje en ny række.
    2. Angiv feltet **Tabel** til **Lagerværdi**.
    3. Angiv feltet **Afledt tabel** til **Lagerværdi**.
    4. Angiv feltet **Felt** til det felt, du vil filtrere efter. Du skal normalt bruge feltet **Udførelsesnavn** og/eller feltet **Udførelsestid**.
    5. Angiv feltet **Kriterier** til den værdi, du vil søge efter i det valgte felt. (Hvis du har valgt feltet **Udførelsesnavn** i det foregående trin, vil denne værdi være navnet på rapporten. Hvis du har valgt feltet **Udførelsestid**, vil det være det tidspunkt, hvor rapporten blev oprettet).
    6. Hvis det er nødvendigt, kan du tilføje flere rækker under fanen **Område**, indtil du entydigt har identificeret den rapport, du søger efter.

1. Vælg **OK** for at gemme dine indstillinger og lukke dialogboksen.
1. Vælg **Gem** for at gemme eksportindstillingerne.
1. Åbn fanen **Eksportindstillinger**, og vælg **Eksporter nu** for at generere eksportfilen.
1. Siden **Udførelsesoversigt** åbnes, hvor du kan se status for eksportjobbet og en liste over de enheder, der er eksporteret. Vælg enheden **Lagerværdi** på listen i sektionen **Status for behandling af enhed**, og vælg derefter **Hent fil** for at hente de data, der er eksporteret fra den pågældende enhed.

Du kan finde flere oplysninger om, hvordan du bruger datastyring til at eksportere data i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
