---
title: Medtag fysisk værdi
description: Du skal bruge afkrydsningsfeltet Medtag fysisk værdi i oversigtspanelet Lagermodel på siden Varemodelgrupper til at angive, om fysisk opdaterede transaktioner medtages, når varens løbende gennemsnitlige kostpris beregnes.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e70a40b15bf08d88958cbf3ee3e82ed63e7a48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424607"
---
# <a name="include-physical-value"></a>Medtag fysisk værdi

[!include [banner](../includes/banner.md)]

Du skal bruge afkrydsningsfeltet Medtag fysisk værdi i oversigtspanelet Lagermodel på siden Varemodelgrupper til at angive, om fysisk opdaterede transaktioner medtages, når varens løbende gennemsnitlige kostpris beregnes.

Afkrydsningsfeltet **Medtag fysisk værdi** har følgende værdier.

| Værdi    | Resultat                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Markeret | Både de fysisk opdaterede transaktioner og økonomisk opdaterede transaktioner bruges til at beregne den løbende gennemsnitskostpris. |
| Afstemt  | Kun de økonomisk opdaterede transaktioner bruges til at beregne den løbende gennemsnitskostpris.                                     |

Afkrydsningsfeltet har lidt forskellige effekter, afhængigt af hvilken lagermodel du bruger.

-   Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi**, når du bruger lagermodellen FIFO (First in, first out), LIFO (Last in, first out) eller LIFO-dato, foretages der også reguleringer af fysisk opdaterede transaktioner ved lukning af lageret.
-   Hvis du ikke markerer afkrydsningsfeltet **Medtag fysisk værdi**, når du bruger disse lagermodeller, foretages der kun udligninger af økonomisk opdaterede transaktioner ved lukning af lager.
-   Når du bruger det vægtede gennemsnit eller lagermodellen for vægtet gennemsnitsdato, udlignes der kun økonomisk opdaterede transaktioner under lukning af lager, uanset om du markerer afkrydsningsfeltet **Medtag fysisk værdi** eller ej.

**Eksempel 1** Du har markeret afkrydsningsfeltet **Medtag fysisk værdi** og modtager følgende indkøbsordrer:

-   En indkøbsordre for et antal af 2 og en kostpris på kr. 10,00, der er følgeseddelopdateret.
-   En indkøbsordre for et antal af 3 og en kostpris på kr. 12,00, der er fakturaopdateret.

I dette tilfælde er den løbende gennemsnitlige kostpris kr. 11,20 = (2x10+3x12)/(2+3), da både de fysisk og økonomisk opdaterede transaktioner bruges til at beregne kostprisen. 

**Eksempel 2** Du har ikke markeret afkrydsningsfeltet **Medtag fysisk værdi**, og kostprisen i vareopsætningen er kr. 10,00. 

-   Du modtager en indkøbsordre på et antal på 20 og en kostpris på kr. 12,00, der er følgeseddelopdateret.

Når en salgsordre bogføres, bogføres kostbeløbet på kr. 10,00, da den løbende gennemsnitlige kostpris ikke inkluderer fysisk bogførte transaktioner. 

> [!NOTE]
> Til sammenligning: Hvis du markerer afkrydsningsfeltet **Medtag fysisk værdi** for denne vare, når en salgsordre bogføres, er det bogførte kostbeløb kr. 12,00.
