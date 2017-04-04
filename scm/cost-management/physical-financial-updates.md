---
title: "Fysiske og økonomiske opdateringer"
description: Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>Fysiske og økonomiske opdateringer

Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal. 

Lagertransaktioner kan opdateres fysisk og økonomisk opdateret i Microsoft Dynamics 365 for operationer. Nogle typer fysiske og økonomiske posteringer øger lagermængderne, mens andre reducerer mængden.

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
Posteringer, der øger mængden, bogføres til den løbende gennemsnitskostpris. Dynamics 365 for operationer beregner en løbende gennemsnitskostpris, der er baseret på kostprisen for hver af disse transaktioner for hver lagerdimension, der spores økonomisk. Få mere at vide om kørsel af gennemsnitlige kostpriser på [Løbende gennemsnitskostpris](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Transaktioner, der reducerer antallet
Dynamics 365 for operationer bruger den beregnede løbende gennemsnitskostpris, når der bogføres en postering, der reducerer antallet, uanset lagermodellen, der er knyttet til dette lager. Posteringen, der reducerer mængden, må ikke tidligere have været afmærket til en anden posteringer, før den blev bogført. Hvis den fysisk disponible lagerbeholdning bliver negativ, bruger Dynamics 365 for operationer de lageromkostninger, der er defineret for varen på den **vare** side. **Bemærk:** Hvis funktionen til brug af flere lokaliteter er aktiveret, vil denne lageromkostning i stedet blive defineret for en lokalitet på siden **Standardindstillinger for ordre**.

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


