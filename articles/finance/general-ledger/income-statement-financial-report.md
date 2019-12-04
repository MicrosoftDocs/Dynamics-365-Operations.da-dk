---
title: Regnskabsrapport over resultatopgørelse
description: I denne artikel beskrives standardrapporten til resultatopgørelser. Her beskrives også de komponenter, der er knyttet til denne rapport.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6322001ea8ccbd2e06e15dc6bc8c273608de895b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771770"
---
# <a name="income-statement-financial-report"></a>Regnskabsrapport over resultatopgørelse

[!include [banner](../includes/banner.md)]

I denne artikel beskrives standardrapporten til resultatopgørelser. Her beskrives også de komponenter, der er knyttet til denne rapport. 

<a name="default-income-statement-report"></a>Standardrapport over resultatopgørelse
-------------------------------

| Standardrapport             | Hvad den gør                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Resultatopgørelse – standard | Viser organisationens rentabilitet for den aktuelle periode og også for år til dato. |

## <a name="building-blocks"></a>Komponenter
Regnskabsrapporten over resultatopgørelse bruger følgende komponenter.

| Standardrapport             | Definition af række                     | Kolonnedefinition          |
|----------------------------|------------------------------------|----------------------------|
| Resultatopgørelse – standard | Oversigt over resultatopgørelse – standard | Periodisk og ÅTD -standard. |

### <a name="row-definition"></a>Definition af række

Rækkedefinitionen, oversigt over resultatopgørelse – standard indeholder et afsnit for hver del af en traditionel resultatopgørelse. Dimensionen Hovedkontokategori bruges til at oprette denne rækkedefinition. Derfor kan alle oprette rapporten uden at skulle foretage ændringer.

### <a name="column-definition"></a>Kolonnedefinition

Kolonnedefinitionerne indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.

-   **Periodisk og ÅTD – standardkolonnetyper:**
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **FD** – Økonomiske data for den aktuelle periode
    -   **FD** – Økonomiske data for år til dato



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Oversigt over økonomirapportering](financial-reporting-getting-started.md)

[Vise økonomirapporter](view-financial-reports.md)

[Dynamics Financial Reporting-blog](https://blogs.msdn.com/b/dynamics_financial_reporting/)



