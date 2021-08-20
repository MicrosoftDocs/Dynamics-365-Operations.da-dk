---
title: Omkostningsobjekter
description: Denne artikel indeholder oplysninger om omkostningsobjekter og forklarer, hvordan omkostninger og antal akkumuleres. Et omkostningsobjekt er en enhed, hvor omkostninger og antal akkumuleres. En omkostningsobjektenhed kan være et produkt eller produktvarianter som f.eks. varianter af typografier og farver.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a835f699a8f412cf15dc528c11d2bfcbf7988985eea21386e92994c66259094
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781603"
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

## <a name="additional-resources"></a>Yderligere ressourcer

[Produktdimensionsgruppe](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Lagringsdimensionsgruppe](/dynamicsax-2012//storage-dimension-groups-form)

[Sporingsdimensionsgruppe](/dynamicsax-2012//tracking-dimension-groups-form)

[Nyheder eller ændringer](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Omkostningsposter](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]