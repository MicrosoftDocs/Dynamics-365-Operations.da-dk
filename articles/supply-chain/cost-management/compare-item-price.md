---
title: Sammenlign lagerrapport over varepriser
description: Få mere at vide om, hvordan du opretter en rapport vedrørende sammenligning af lagerets varepriser og derefter gennemser og/eller eksporterer resultatet.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424828"
---
# <a name="compare-item-prices-storage-report"></a>Sammenlign lagerrapport over varepriser

[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du kan køre en rapport over **Sammenligning af lagerets varepriser** og gøre outputtet digitalt tilgængeligt enten som en interaktiv side i Dynamics 365 Supply Chain Management eller som et eksporteret dokument i et af de flere tilgængelige formater.

Når du får vist rapporten i din browser, reguleres kolonner og aggregerede saldi dynamisk, afhængigt af det layout, du har konfigureret. Du kan sortere resultaterne, filtrere dem, gå mere i dybden i dataene og meget mere.

Rapportresultater gemmes i dataenheden **Sammenligning af varepriser**, som giver dig mulighed for at filtrere og eksportere resultaterne til et format som f.eks. CSV eller Microsoft Excel.

Rapporten **Sammenligning af varepriser på lageret** er nyttig, hvis afgangen indeholder mange linjer. Outputtet indeholder f.eks. mange linjer, hvis du har mere end 40.000 varer, der har en afventende varepris i efterkalkulationsversionen.

## <a name="enable-compare-item-prices-storage"></a>Aktiver sammenligning af varepriser på lageret

Før du kan bruge denne funktion, skal du aktivere den i dit system. Administratorer kan bruge indstillingerne [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Her er funktionen angivet som:

- **Modul** - Omkostningsstyring
- **Funktionsnavn** - Sammenligning af varepriser på lager

## <a name="generate-a-compare-item-prices-storage-report"></a>Generér en rapport, der sammenligner varepriserne på lageret

Udfør følgende trin for at generere og gemme en rapport for **Sammenligning af varepriser på lageret**:

1. Gå til **Omkostningsstyring > Forespørgsler og rapporter > Forudbestemte omkostningsrapporter > Sammenligning af varepriser på lageret**.

1. Vælg **Ny** for at åbne ruden **Sammenligning af varepriser**. Angiv følgende indstillinger for at definere, hvilke priser der skal sammenlignes i rapporten:

    - I oversigtspanelet **Parametre** kan du give rapporten et unikt **Navn** og bruge felterne i de sektionerne **Afventende priser til sammenligning** og **Priser, som anvendes sammenligning** til at definere, hvilke priser og datoer der skal sammenlignes.
    - I oversigtspanelet **Poster, som skal medtages** skal du konfigurere filtre og begrænsninger for at definere, hvilke data der skal medtages i rapporten.
    - På oversigtspanelet **Kør i baggrunden** skal du angive, hvornår og hvor ofte rapporten skal genereres.
    > [!NOTE]
    > Denne rapport udføres altid som en del af et batchjob.

1. Vælg **OK** for at anvende dine indstillinger og lukke ruden.

1. Når batchjobbet er fuldført, vises det på siden **Sammenligning af varepriser på lageret**. Du er muligvis nødt til at opdatere siden for at se rapporten.

## <a name="explore-the-compare-item-prices-storage-report"></a>Udforsk rapporten med sammenligningen af varepriserne på lageret

Når du har genereret en rapport, kan du til enhver tid få vist og udforske den på følgende måde:

1. Gå til **Omkostningsstyring > Forespørgsler og rapporter > Forudbestemte omkostningsrapporter > Sammenligning af varepriser på lageret**.

1. Vælg en rapport på listen.

1. Benyt en af følgende fremgangsmåder:

    - Vælg **Oversigt** for at få en oversigt over dine rapportresultater.
    - Vælg **Visningsdetaljer** for at få en mere detaljeret visning af rapporten

1. Når den valgte visning åbner, kan du gøre følgende:

    - Vælge næsten enhver kolonneoverskrift for at sortere eller filtrere tabellen efter værdier i kolonnen på samme måde som de fleste standardformularer i Supply Chain Management. Bemærk, at du ikke kan sortere eller filtrere kolonnen **Nettoprisændring %**, da det er et beregnet felt.
    - Vælg **Dimensionsvisning** for at åbne en rude, hvor du kan vælge, hvilken dimensionskolonne der skal medtages i formularen. Angiv **Gem opsætning** til **Ja**, hvis du vil gemme disse indstillinger, så de bevares, næste gang du åbner rapporten. Vælg **OK** for at anvende dine indstillinger og lukke.
    - Vælg en række i formularen, og vælg derefter **Vis detaljer** for at få vist flere oplysninger om den valgte vare. Du vil kunne gå i dybden med dataene herfra.
    - Vælg en række i formularen, og vælg derefter **Vis sammenligningsdiagram** for at få vist en interaktiv grafisk repræsentation af resultaterne, som de relaterer til den valgte vare. Du kan udforske disse resultater ved at vælge forskellige grafiske elementer i diagrammet og i diagramforklaringen.
    - Vælg en række i formularen, og vælg derefter **Vis beregningsdetaljer** for at få vist flere oplysninger om de beregninger, der er relateret til den valgte vare. Du vil kunne gå i dybden med dataene herfra.

## <a name="export-the-compare-item-prices-storage-report"></a>Eksporter rapporten med sammenligningen af varepriserne på lageret

Hver rapport, du opretter, gemmes i dataenheden **Sammenligning af varepriser**. Du kan bruge standardfunktionerne til datastyring i Supply Chain Management til at eksportere data fra denne enhed til alle understøttede dataformater, herunder CSV eller Microsoft Excel.

Følgende er et eksempel på, hvordan du kan eksportere en rapport over **Sammenligning af varepriser på lageret**:

1. Gå til **Systemadministration > Arbejdsområder > Datastyring**.

1. Klik på knappen **Eksporter** i sektionen **Datastyring**.

1. Siden **Eksportér** åbnes, som du kan bruge til at konfigurere eksportjobbet. Start med at give dit job et **Gruppenavn**.

1. I sektionen **Valgte enheder** skal du vælge **Tilføj enhed** for at åbne en dialogboks, hvor du kan angive følgende indstillinger:

    - **Enhedsnavn** - Vælg **Sammenligning af varepriser**.
    - **Målformat for data** - Vælg det format, du vil eksportere til.

1. Vælg **Tilføj** for at tilføje den nye række, og vælg derefter **Luk** for at lukke dialogboksen.

1. Normalt skal du eksportere én rapport ad gangen. Det kan du gøre ved at oprette et **Filter** for den række, du lige har tilføjet til ruden **Forespørgsler**. På den måde kan du definere, hvilke rapporter fra enheden **Sammenligning af varepriser**, du vil medtage i eksporten. Angiv følgende filterindstillinger for at eksportere en enkelt rapport:

    - På fanen **Afgrænsning** skal du vælge **Tilføj** for at tilføje en ny række.
    - Angiv **Tabel** til **Sammenligning af varepriser**.
    - Angiv **Afledt tabel** til **Sammenligning af varepriser**.
    - Angiv **Felt** til det felt, du vil filtrere efter. Normalt bruges **Udførelsesnavn** eller **Kørselstidspunkt**.
    - Angiv **Kriterier** til værdien fra det valgte felt, som du vil søge efter (enten rapportens navn eller det tidspunkt, rapporten blev oprettet på).
    - Hvis det er nødvendigt, kan du tilføje flere rækker til tabellen **Afgrænsning**, indtil du entydigt har identificeret den rapport, du søger efter.

1. Vælg **OK** for at gemme dine indstillinger og lukke.

1. Vælg **Gem** for at gemme eksportindstillingerne.

1. Åbn fanen **Eksportindstillinger**, og vælg **Eksporter nu** for at generere eksportfilen.

1. Siden **Udførelsesoversigt** åbnes, hvor du kan se statussen for eksportjobbet og en liste over de enheder, der er eksporteret. Vælg enheden **Sammenligning af varepriser** i området **Status for behandling af enhed**, og vælg derefter **Hent fil** for at hente de data, der eksporteres fra den pågældende enhed.

Du kan finde flere oplysninger om, hvordan du bruger datastyring til at eksportere data i [Oversigt over dataimport og eksportjob](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
