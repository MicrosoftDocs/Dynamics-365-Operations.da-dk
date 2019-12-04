---
title: Balance - økonomiske rapporter
description: I denne artikel beskrives standardrapporterne til balancer. Her beskrives også de komponenter, der er knyttet til disse rapporter.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96552447182f3692a19d4cfd962afbcb28e5508
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771863"
---
# <a name="balance-sheet-financial-reports"></a>Balance - økonomiske rapporter

[!include [banner](../includes/banner.md)]

I denne artikel beskrives standardrapporterne til balancer. Her beskrives også de komponenter, der er knyttet til disse rapporter. 

<a name="default-balance-sheet-reports"></a>Standardbalancerapporter
-----------------------------

Der er to standardbalancerapporter. I den ene rapport er afsnittene stablet. I den anden er de placeret side om side.

| Standardrapport                       | Hvad den gør                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Balance – standard              | Giver en oversigt over organisationens økonomiske situation for året.                                                                 |
| Parallel balance – standard | Giver en oversigt over organisationens økonomiske situation for året. Aktiver og passiver og egenkapital ved siden af hinanden. |

## <a name="building-blocks"></a>Komponenter
Balanceregnskabsrapporter bruger følgende komponenter.

| Standardrapport                       | Definition af række                       | Kolonnedefinition             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balance – standard              | Balance – standard              | ÅTD og afvigelse - standard    |
| Parallel balance – standard | Parallel balance – standard | År til dato-kolonne - standard |

### <a name="row-definition"></a>Definition af række

Rækkedefinitioner for begge balancerapporter indeholder sektioner for hver del af en traditionel balance. Side om side-rapporten indeholder et kolonneskift, så passiver og egenkapital vises ved siden af aktiver. Dimensionen Hovedkontokategori bruges til at oprette begge rækkedefinitioner. Derfor kan alle oprette rapporterne uden at skulle foretage ændringer.

### <a name="column-definition"></a>Kolonnedefinition

Kolonnedefinitionerne indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.

-   **ÅTD og afvigelse – standardkolonnetyper:**
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **FD** – År til dato-økonomiske data for indeværende år
    -   **FD** – År til dato-økonomiske data for sidste år
    -   **BEREGN** – Afvigelsen ved at fratrække sidste år fra indeværende år

<!-- -->

-   **År til dato-kolonne - standard:**
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **FD** – År til dato-økonomiske data for indeværende år



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over økonomirapportering](financial-reporting-getting-started.md)

[Vise økonomirapporter](view-financial-reports.md)

[Dynamics Financial Reporting-blog](https://blogs.msdn.com/b/dynamics_financial_reporting/)



