---
title: Fysiske og økonomiske opdateringer
description: Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ea79bd9c6561c4e4f6fad2c177f44fe62bdea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424814"
---
# <a name="physical-and-financial-updates"></a>Fysiske og økonomiske opdateringer

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal. 

Lagertransaktioner kan opdateres fysisk og økonomisk i Dynamics 365 Supply Chain Management. Nogle typer fysiske og økonomiske posteringer øger lagermængderne, mens andre reducerer mængden.

## <a name="physical-increases"></a>Fysiske opskrivninger
Når der bogføres en fysisk postering, ændres statussen for transaktionsposten til **Modtaget**. Følgende transaktioner betragtes som fysiske opskrivninger:

-   Indkøbsordretilgang
-   Salgsordrefølgeseddelretur
-   Færdigmelde en produktionsordre
-   Biprodukt på en produktionsordreplukliste

## <a name="financial-increases"></a>Økonomiske opskrivninger
Når en økonomisk tilgangspostering er bogført, er statussen for den transaktionspost, der opskriver mængden, **Købt**. Følgende transaktioner betragtes som økonomiske opskrivninger:

-   Kreditorfaktura
-   Salgsordrefaktura for en returnering
-   Efterkalkulation af produktionsordre
-   Lagerkladder med positiv mængde, f.eks. bevægelse, driftsregnskab, optælling, styklister og overførsel

## <a name="transactions-that-increase-quantity"></a>Transaktioner, der opskriver antallet
Posteringer, der øger mængden, bogføres til den løbende gennemsnitskostpris. Den beregnede løbende gennemsnitskostpris er baseret på kostprisen for hver af disse transaktioner for hver lagerdimension, der spores økonomisk. Få mere at vide om kørsel af gennemsnitlige kostpriser på [Løbende gennemsnitskostpris](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transaktioner, der reducerer antallet
Den beregnede løbende gennemsnitskostpris bruges, når en transaktion, der reducerer mængden, bogføres, uanset hvilken lagermodel der knyttes til dette lager. Posteringen, der reducerer mængden, må ikke tidligere have været afmærket til en anden posteringer, før den blev bogført. Hvis den fysisk disponible lagerbeholdning bliver negativ, bruges de lageromkostninger, der er defineret for varen på siden **Vare**. 

> [!NOTE]
> Hvis funktionen til brug af flere lokationer er aktiveret, vil denne lageromkostning i stedet blive defineret for en lokation på siden **Standardindstillinger for ordre**.

## <a name="physical-issues-vs-financial-issues"></a>Fysiske afgange vs. økonomiske afgange
Når der bogføres en fysisk afgangspostering, ændres statussen for transaktionsposten til **Trukket**. Følgende transaktioner betragtes som fysiske afgange:

-   Produktionsordrepluklistekladde
-   Salgsordrefølgeseddel
-   Indkøbsordrefølgeseddelreturnering

Når der bogføres en økonomisk postering, ændres statussen for transaktionsposten til **Solgt**. Følgende transaktioner betragtes som økonomiske afgange:

-   Afslutte en produktionsordre
-   Salgsordrefaktura
-   Kreditorfakturareturnering
-   Lagerkladder med negativ mængde, f.eks. bevægelse, driftsregnskab, optælling, styklister og overførsel

Transaktioner, der reducerer antallet, bogføres til den løbende gennemsnitskostpris. Proceduren til lagerlukning er derfor påkrævet for at udligne afgangsposteringer i forhold til tilgangsposteringer på baggrund af den lagermodel, der er knyttet til hver vare.
