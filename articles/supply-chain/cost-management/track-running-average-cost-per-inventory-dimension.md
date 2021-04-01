---
title: Spore løbende gennemsnitskostpris pr. lagerdimension
description: Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2bf04a42edf09c35e81742b1c60db8944eba2ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252864"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Spore løbende gennemsnitskostpris pr. lagerdimension

[!include [banner](../includes/banner.md)]

Der er tildelt en lagerdimensionsgruppe til de enkelte lagervarer. Den løbende gennemsnitskostpris for en vare beregnes derfor på baggrund af de valgte lagerdimensioner, der spores økonomisk.

Der findes tre typer lagerdimensioner: produkt, lager og sporing. Produktdimensioner omfatter konfiguration, størrelse og farve. Produktdimensioner spores altid økonomisk. Lager- og sporingsdimensioner omfatter lokation, lagersted, lokalitet, lagerstatus, nummerplade, batchnummer og serienummer. Du kan vælge, hvilke lager- og sporingsdimensioner der skal spores økonomisk. 

**Eksempel 1** 

Hvis den lagerdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, beregnes den løbende gennemsnitskostpris pr. lagersted. Følgende indkøbsordrer er faktureret:

-   En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL.
-   En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL.
-   En indkøbsordre på et antal på 5 til en kostpris af kr. 15,00 er faktureret for lagerstedet HL.

Den løbende gennemsnitskostpris for lagerstedet GL er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL er kr. 15,00. En salgsordrefaktura bogføres for lagerstedet GL. Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 11,20. En anden salgsordre bogføres for lagerstedet GL. Værdien af lageret og kostprisen for solgte varer (før der køres lagerlukning og uden afmærkning) er kr. 15,00. 

**Eksempel 2** Hvis den lagringsdimensionsgruppe, der er knyttet til varen, spores økonomisk af lagerstedet, og sporingsdimensionsgruppen spores økonomisk af batchnummeret, beregnes den løbende gennemsnitskostpris for de enkelte batches. 

**Bemærk!** Det anbefales, at du altid ser kostprisen for alle økonomiske dimensioner, der spores. Følgende indkøbsordrer er faktureret:

-   En indkøbsordre på et antal på 2 til en kostpris af kr. 10,00 er faktureret for lagerstedet GL og batch AAA.
-   En indkøbsordre på et antal på 3 til en kostpris af kr. 12,00 er faktureret for lagerstedet GL og batch AAA.
-   En indkøbsordre på et antal på 2 til en kostpris af kr. 15,00 er faktureret for lagerstedet GL og batch BBB.

Den løbende gennemsnitskostpris for lagerstedet GL og batch AAA er kr. 11,20, og den løbende gennemsnitskostpris for lagerstedet HL og batch BBB er kr. 15,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]