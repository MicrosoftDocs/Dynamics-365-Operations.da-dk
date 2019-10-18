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
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176929"
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

[Økonomirapportering](financial-reporting-getting-started.md)

[Se økonomiske rapporter](view-financial-reports.md)

[Dynamics Financial Reporting-blog](https://blogs.msdn.com/b/dynamics_financial_reporting/)



