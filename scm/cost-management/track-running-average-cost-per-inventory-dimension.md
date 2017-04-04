---
title: "Spore løbende gennemsnitskostpris pr. lagerdimension"
description: "Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-31 12 - 51 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f464f94632f7114da5a9cbf34036e4fcb87bcd02
ms.lasthandoff: 03/29/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Spore løbende gennemsnitskostpris pr. lagerdimension

Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk.

Der findes tre typer lagerdimensioner: produkt, lager og sporing. Produktdimensioner omfatter konfiguration, størrelse og farve. Produktdimensioner spores altid økonomisk. Lager- og sporingsdimensioner omfatter lokation, lagersted, lokalitet, lagerstatus, nummerplade, batchnummer og serienummer. Du kan vælge, hvilke lager- og sporingsdimensioner der skal spores økonomisk. **Eksempel 1** Hvis den lagerdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, beregnes den løbende gennemsnitskostpris pr. lagersted. Følgende indkøbsordrer er faktureret:

-   En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL.
-   En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL.
-   En indkøbsordre på et antal på 5 til en kostpris af kr. 15,00 er faktureret for lagerstedet HL.

Den løbende gennemsnitskostpris for lagerstedet GL er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL er kr. 15,00. En salgsordrefaktura bogføres for lagerstedet GL. Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 11,20. En anden salgsordre bogføres for lagerstedet GL. Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 15,00. **Eksempel 2** Hvis den lagringsdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, og sporingsdimensionsgruppen spores økonomisk af batchnummeret, beregnes den løbende gennemsnitskostpris for de enkelte batches. **Bemærk!** Det anbefales, at du altid ser kostprisen for alle økonomiske dimensioner, der spores. Følgende indkøbsordrer er faktureret:

-   En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL og batch AAA.
-   En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL og batch AAA.
-   En indkøbsordre på et antal på 2 til en kostpris af kr. 15,00 er faktureret for lagerstedet GL og batch BBB.

Den løbende gennemsnitskostpris for lagerstedet GL og batch AAA er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL og batch BBB er kr. 15,00.


