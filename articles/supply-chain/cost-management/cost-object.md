---
title: Omkostningsobjekter
description: Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50849a173e74ad88dd10c6a30ea66c91b936e165
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201772"
---
# <a name="cost-objects"></a>Omkostningsobjekter

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.  

## <a name="cost-objects"></a>Omkostningsobjekter

Siden **Omkostningsobjekter** viser alle omkostningsobjekter, der er registreret på et produkt. Omkostningsobjekter er defineret af data fra følgende kilder:

-   Produkt
-   Produktdimensionsgruppe
-   Lagringsdimensionsgruppe
-   Sporingsdimensionsgruppe

**Bemærk!** Et omkostningsobjekt repræsenterer kun et omkostningselement af typen **Direkte material**. Et omkostningsobjekt og et lagerobjekt er forskellige på den måde, at et omkostningsobjekt er defineret af de lagerdimensioner, der er valgt til økonomisk lager. I dette eksempel har en vare følgende konfiguration:

-   **Websted:** Fysisk lager = Ja, økonomisk lager = Ja
-   **Websted:** Fysisk lager = Ja, økonomisk lager = Nej
-   **Batch nr.:** Fysisk lager = Ja, økonomisk lager = Nej

Tabellen nedenfor viser, hvad der er et omkostningsobjekt, og hvad er et lagerobjekt.

| Objekttype      | Varenummer | Lokation | Lagersted | Batch nr. |
|------------------|-------------|------|-----------|-----------|
| Omkostningsobjekt      | x           | x    |           |           |
| Lagerobjekt | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Akkumulering af omkostninger og antal
-   Værdien i felterne **Værdi** er en sum af følgende værdier:
    -   Fysisk kostbeløb
    -   Økonomisk kostbeløb
    -   Reguleringer
-   Værdien i feltet **Antal** er en sum af følgende værdier:
    -   Modtaget
    -   Trukket
    -   Bogført antal
-   Feltet **Gennemsnitlig enhedskostpris** er et beregnet felt. Værdien beregnes ved at dividere værdien **Værdi** med værdien **Antal**.

**Bemærk!** Parameteren **Medtag fysisk værdi** har ingen effekt på de foregående beregninger.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Produktdimensionsgruppe](https://technet.microsoft.com/library/aa499382.aspx)

[Lagringsdimensionsgruppe](https://technet.microsoft.com/library/hh209317.aspx)

[Sporingsdimensionsgruppe](https://technet.microsoft.com/library/hh209465.aspx)

[Nyheder eller ændringer](../../fin-and-ops/get-started/whats-new-changed.md)

[Omkostningsposter](cost-entries.md)



