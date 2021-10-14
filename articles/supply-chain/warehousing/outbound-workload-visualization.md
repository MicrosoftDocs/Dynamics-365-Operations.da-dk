---
title: Visualisering af udgående arbejdsbyrde
description: Dette emne indeholder oplysninger om visualisering af udgående arbejdsbyrde. Denne funktion giver lagerchefer og tilsynsførende mulighed for at oprette brugerdefinerede arbejdsbyrdediagrammer, der kan bruges til at overvåge forløbet af det aktuelle arbejde og den mængde, der mangler. Lagerchefer kan oprette flere visninger og konfigurere automatisk opdatering efter behov.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8416d43fe2b8b08e4d66434a1d95daa4b01a0fa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576154"
---
# <a name="outbound-workload-visualization"></a>Visualisering af udgående arbejdsbyrde

[!include [banner](../includes/banner.md)]

De avancerede opsætningsmuligheder, der er tilgængelige fra siden **Visualisering af udgående arbejdsbyrder**, giver lagerchefer og tilsynsførende mulighed for at oprette brugerdefinerede arbejdsbyrdediagrammer, der kan bruges til at overvåge forløbet af det aktuelle arbejde og den mængde, der mangler. Lagerchefer kan oprette flere visninger og konfigurere automatisk opdatering efter behov. Visualiseringer af udgående arbejdsbyrder er egnede til visning på lagerstedets ydeevnesider.

Denne funktion kan bruges til at spore status for plukarbejde. Funktionen er integreret med arbejdsstyring, og hvis arbejdsstyring er konfigureret, kan visualiseringer af udgående arbejdsbyrder vise en beregning af det antal timer, der er tilbage for det plukarbejde, der vises (filtreret).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Aktivere funktionen Visualisering af udgående arbejdsbyrde

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Visualisering af udgående arbejdsbyrde*

## <a name="set-up-outbound-workload-visualizations"></a>Konfigurere visualiseringer af udgående arbejdsbyrde

Hvis du vil konfigurere dine visualiseringer, skal du oprette en samling filtre (visninger) og designe hvert filter, så det viser en anden type analyse. Du kan bruge siden **Konfigurer filtre** til at designe filtrene.

Benyt følgende fremgangsmåde for at konfigurere en visualisering af udgående arbejdsbyrde.

1. Gå til **Lokationsstyring \> Overvågningsrapporter for lagersted \> Visualisering af udgående arbejdsbyrde**.

    Siden **Visualisering af udgående arbejdsbyrde** vises. Når du har oprettet nogle filtre, vil denne side vise din visualisering. Du kan oprette lige så mange filtre, som du vil. Alle de filtre, du opretter, gemmes under din brugerkonto, så du kan bruge dem senere. Med andre ord har hver bruger deres eget sæt filtre, som de har oprettet. Disse filtre deles ikke med andre brugere.

1. Vælg **Konfigurer filtre** under fanen **Filtre** på siden **Visualisering af udgående arbejdsbyrde** i handlingsruden.
1. Vælg **Ny** i handlingsruden på siden **Konfigurer filtre** for at tilføje et filter, og angiv derefter følgende felter til det:

    - **X-akse-gruppetabel** – Vælg den tabel, der indeholder det felt, der skal bruges til at gruppere X-akseværdierne.
    - **X-akse-gruppefelt** – Vælg det felt, der skal bruges til at gruppere X-akse-værdierne, blandt felterne i den tabel, du har valgt i feltet **X-akse-gruppetabel**.
    - **X-akse-værditabel** – Vælg den tabel, der indeholder det felt, der skal bruges til at analysere grupperne yderligere.
    - **X-akse-værdifelt** – Vælg det felt blandt felterne i den tabel, du har valgt i feltet **X-akse-værditabel**, der skal levere værdier, som skal analyseres for hver gruppe.
    - **Automatisk opdatering** – Vælg, om visualiseringen automatisk skal opdateres.
    - **Opdateringsinterval (minutter)** – Angiv antallet af minutter mellem automatiske opdateringer.
    - **Visningsniveau** – Vælg, om der skal vises åbne linjer eller åbne overskriftsantal i diagrammet.
    - **Pluktype** – Hvis du angiver feltet **Visningsniveau** til _Åbne linjer_, skal du vælge, om antallet af åbne arbejdslinjer i diagrammet skal indeholde de første pluk, stadieinddelte pluk eller både første pluk og stadieinddelte pluk.
    - **Sted** – Vælg det sted, som diagrammet skal indlæses for.
    - **Lagersted** – Vælg det lagersted, som diagrammet skal indlæses for.
    - **Dage, der skal medtages** – Angiv det antal dage i fortiden, som diagrammet skal genereres for.
    - **Arbejdsordretype** – Vælg de udgående arbejdsordretyper, der skal filtreres efter.

    ![Siden Konfigurer filtre.](media/work-viz-filters-1.png "Siden Konfigurer filtre")

1. Luk siden **Konfigurer filtre** for at vende tilbage til siden **Visualiseringer af udgående arbejdsbyrder**.

    Siden **Visualiseringer af udgående arbejdsbyrder** viser nu data ud fra de nye filterindstillinger. Det nye filter er nu tilgængeligt og er valgt i feltet **Filter**. Følgende felter er tilgængelige øverst i diagrammet:

    - **Filter** – Dette felt indeholder alle de filtre, du har oprettet indtil nu. Vælg et filter for at få vist dataene i diagrammet.
    - **Sidst opdateret** – iI dette felt vises den dato og det tidspunkt, hvor oplysningerne i diagrammet sidst blev opdateret.
    - **Estimeret/faktisk tid** – Hvis der er konfigureret arbejdsstandarder i systemet, skal du angive denne indstilling til *Ja* for at få vist de samlede estimerede pluktider øverst i hver kolonne i diagrammet. Hvis du ikke bruger arbejdsstandarder, er denne indstilling ikke tilgængelig.

    ![Eksempel på visualisering.](media/work-viz-chart.png "Eksempel på visualisering")

1. Vælg en vilkårlig søjle i diagrammet for at få vist oplysningerne i den tilknyttede arbejdslinje.

    ![Arbejdslinjedetaljer.](media/work-viz-work-details.png "Arbejdslinjedetaljer")

## <a name="example-outbound-workload-visualization-for-zones"></a>Eksempel: Visualisering af udgående arbejdsbyrde for zoner

I dette eksempel skal du oprette en visualisering, der viser arbejdslinjer for hver enkelt zone, og status for hver enkelt arbejdslinje (_Åben_, _Lukket_ eller _Annulleret_). I dette tilfælde kan du oprette et filter, der har følgende indstillinger:

- **Filternavn** – Angiv et navn til dette filter (f.eks. en _Zone vs. arbejdsstatus_).
- **Beskrivelse** – Angiv en kort beskrivelse af dette filter (f.eks. en _Zone vs. arbejdsstatus_).
- **X-akse-gruppetabel** – Vælg _Lokationer._
- **X-aksegruppe** – Vælg _Zone-id_.
- **X-akseværditabel** – Vælg _Arbejde_, da du vil have vist arbejde pr. zone.
- **X-akseværdifelt** – Vælg _Arbejdsstatus_, da du vil have vist arbejdsstatus.
- **Automatisk opdatering** – Vælg, om visualiseringen automatisk skal opdateres.
- **Pluktype** – Vælg _Første pluk og stadieinddelte pluk_, da du vil medtage både første pluk og pluk fra midlertidige lokationer. Det vil sige, at du vil medtage alle de pluklinjer, du har.
- **Visningsniveau** – Vælg _Åbne linjer_, da du vil have vist oplysningerne pr. linje, ikke pr. arbejdsoverskrift.

I følgende illustration vises et eksempel på resultatdiagrammet.

![Visualisering af zone vs. arbejdsstatus.](media/work-viz-chart.png "Visualisering af zone vs. arbejdsstatus")

Dette diagram indeholder to zoner, der hedder **PRODUKTION** og **BULK**, plus en zone med navnet **Blank**. Zonen **Blank** repræsenterer alle de arbejdslinjer, der ikke er medlemmer af nogen zoner. Diagrammet viser altid alle ikke-relaterede filtrerede data som **Blank**, så det giver så høj synlighed som muligt. I området **PRODUKTION** vises tre lukkede linjer og fire åbne linjer i diagrammet. I området **BULK** vises fire lukkede linjer og én åben linje og 24 annullerede linjer i diagrammet. Endelig viser diagrammet otte lukkede linjer, der ikke indgår i en zone og derfor er angivet som **Blank**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]