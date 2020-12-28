---
title: Leveranceplaner
description: Leveranceplaner giver dig mulighed for at spore antallet, når du bruger flere leverancer til en enkelt salgsordre, et salgstilbud eller en indkøbsordre.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc25ff113291b2a8a0a7ba15637e4d094feb9aae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424791"
---
# <a name="delivery-schedules"></a>Leveranceplaner

[!include [banner](../includes/banner.md)]

Leveranceplaner giver dig mulighed for at spore antallet, når du bruger flere leverancer til en enkelt salgsordre, et salgstilbud eller en indkøbsordre.

Brug en leveranceplan bruges, når det samlede antal i en ordre eller et tilbud skal leveres i flere leverancer. Individuelle leverancer repræsenteres af leveringslinjer. To eller flere leverancelinjer udgør én leveranceplan. Leverancelinjerne kan have forskellige leveringsdatoer, antal, leveringsmåder og lagringsdimensioner, som f.eks. sted og lagersted.  

**Eksempel på en leveranceplan**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Samlet ordre (oprindelig salgsordrelinje) | 600 stole                               |
| Ønsket leveranceplan       | 100 stole pr. måned                     |
| Ønsket tidsramme for leverance | 6 måneder, på den første dag i hver måned |

I dette scenario anmoder kunden om en leverance på 600 stole i batch på 100 stole over en periode på seks måneder. Du kan holde styr på leveringskravene ved at oprette en leveranceplan. Du kan oprette seks forskellige leverancelinjer på siden med leveranceplanen. Hver leverancelinje indeholder 100 stole og angiver leveringsdatoen for disse 100 stole. I dette tilfælde modregnes hver linje på den første i måneden i seks på hinanden efterfølgende måneder.  

Når du opretter en leveranceplan, ændres typen af den oprindelige ordrelinje automatisk til **Ordrelinje med flere leveringer**. En linje af denne type kaldes en kommerciel linje og er markeret ved et ikon. Leveringslinjen er markeret ved et andet ikon. Hvis du ændrer et antal på en leverancelinje, opdateres den kommercielle linje til det samlede antal i leveranceplanen. Hvis der i en samhandelsaftale er defineret en slutrabat for ordren, sørger leveranceplanen for, at din ordre bliver berettiget til slutrabatten, selv når ordren opdeles i adskilte leverancer.  

Ordrer, der har en leveranceplan, behandles i forhold til leverancelinjerne. Behandling omfatter bogføringen af følgesedler, produktkvitteringer og fakturering.  

Dokumentudskrifter af ordrer og tilbud, der har en leveranceplan, viser kun leverancelinjerne. De viser ikke de oprindelige linjer (kommercielle linjer). **Bemærk:** Desuden er det kun leverancelinjerne, der vises i, når du udfører disse handlinger:

-   Bogfør
-   Kopierer sider
-   Gennemser listesider og rapporter

Når du bekræfter salgstilbud, viser de oprettede salgsordrer hele leveranceplanen, også selvom ordrelinjerne har flere leverancer. Hele leveranceplanen vises derudover på alle større sider, som f.eks. salgsordrer, salgstilbud og indkøbsordrer.



