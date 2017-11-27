---
title: "Færdigmeld styklister"
description: "Denne artikel indeholder oplysninger om færdigmelding af styklister."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 92c594213eea8617d11b56be43e581a461830ba4
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="report-boms-as-finished"></a>Færdigmeld styklister

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om færdigmelding af styklister.

Siderne **Færdigmeld** og **Maks. færdigmelding** bruges til at færdigmelde styklister. Processen for færdigmelding af en stykliste er begrebsmæssigt det samme som processen for færdigmelding af en produktionsordre. Denne proces kan f.eks. bruges i enkle samlings- og pakningsprocesser, hvor de mere avancerede funktioner i produktionsordrer ikke er nødvendige. På siden **Færdigmelding** kan du færdigmelde flere styklister i en batch. På siden **Maks. færdigmelding** kan du kun rapportere én stykliste ad gangen. Siden **Færdigmelding** er tilgængelig fra et menupunkt i Lagerstyring, og begge sider er tilgængelige som menuelementer på siden **Frigivne produkter**.

## <a name="report-as-finished-page"></a>Siden Færdigmelding
Hvis du åbner siden **Færdigmeld** fra en frigivet produktside, foreslår siden, at du færdigmelder standardlagerets standardantal. Den aktive styklisteversion vises som standard, men du kan ændre styklisteversionen, hvis der er andre godkendte versioner. På siden kan du også slette poster og oprette nye poster for frigivne produkter, der skal færdigmeldes. Hvis du vil bruge en forespørgsel til at vælge produkter, skal du klikke på menupunktet **Marker**. Du kan manuelt bekræfte færdigmelding for de valgte produkter ved at klikke på **OK**. Du kan også konfigurere processen som en batchjobkørsel. Når færdigmeldingsprocessen er bekræftet, genererer systemet en styklistekladde, hvor bogføring på lager behandles. Denne kladde består af et linjeelement for det færdige produkt og et linjeelement for hver styklistelinje. Du kan styre, om kladden skal bogføres automatisk, eller om den skal være åben for yderligere justeringer.

## <a name="max-report-as-finished-page"></a>Maks. Siden Færdigmelding
På siden **Maks. færdigmelding** angiver hver styklistelinje antal produktelementer, der kan færdigmeldes. Denne beregning er baseret på den fysisk tilgængelige disponible lagerbeholdning for hvert materialelinje. I følgende eksempel bruger ét element af varenummer FG to elementer af råvaren RM10 og ét element af råvare RM20. Da der kun er 10 elementer af RM10 på lager, er det maksimale antal FG, der kan færdigmeldes, fem elementer. Denne værdi vises i feltet **Maks. færdigmelding**.

| Niveau | Varenummer | Antal | Beholdninger | Maks. Færdigmelding |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Styklister, der har flere niveauer
Når en stykliste har flere niveauer, kan du styre, hvordan materialer figurerer på alle niveauer, ved hjælp af feltet **Udfoldning**. Dette felt er tilgængeligt på både siden **Færdigmeld** og siden **Maks. færdigmelding**. Følgende valgmuligheder er tilgængelige:

-   **Aldrig** – Underliggende styklister udfoldes ikke, hvis der er mangel på materialer.
-   **Altid** – Alle underliggende styklister udfoldes helt. Derfor bruges en eventuel fri disponibel lagerbeholdning ikke til halvfærdige komponentvarer.
-   **Mangel** – Underliggende styklister udfoldes kun, hvis der ikke er adgang til hele den ønskede mængde af materialet.

### <a name="example"></a>Eksempel

I dette eksempel er tre elementer af det færdige produkt (varenummer FG) klar til at blive færdigmeldt. Der er en stykliste med to niveauer, som vist her.

| Niveau | Varenummer | Antal på styklistelinje | Beholdninger |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Følgende tabeller viser, hvordan indstillingen i feltet **Udfoldning** påvirker den måde, styklistekladdelinjerne genereres på. **Udfoldning: aldrig**

| Niveau | Varenummer | Antal |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Som ovenstående tabel viser, betragtes kun varenummeret COMP som trukket i kladden. Varenummeret RM, som er en del af COMP, nedbrydes ikke til kladdelinjen, og de to stykker på lager af COMP tages ikke i betragtning. **Udfoldning: altid**

| Niveau | Varenummer | Antal |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

I dette tilfælde udfoldes varenummer COMP som råvarer, varenummer RM. De to elementer på lager af COMP indgår ikke i antallet af RM til forbrug. **Udfoldning: mangel**

| Niveau | Varenummer | Antal |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

I dette tilfælde indgår de to elementer på lager i varenummer COMP. Men fordi der kræves tre elementer af varenummer FG, kræves ét element af varenummer RM også for at udgøre det ekstra element i COMP.




