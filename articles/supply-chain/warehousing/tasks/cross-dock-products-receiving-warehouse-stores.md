---
title: Levere produkter direkte fra modtagende lagersteder til butikker
description: Denne procedure gennemgår trin til oprettelse og behandling af en cross-dock med henblik på distribution af produkter fra modtagelokationen af en købsordre til en eller flere butikker.
author: ShylaThompson
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7caec5329774baaa03c72f9236f8e3192399089
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810384"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Levere produkter direkte fra modtagende lagersteder til butikker

[!include [banner](../../includes/banner.md)]

Denne procedure gennemgår trin til oprettelse og behandling af en cross-dock med henblik på distribution af produkter fra modtagelokationen af en købsordre til en eller flere butikker. Brugeren kan definere flere konfigurationer og få systemet til at foreslå, hvordan produkter skal distribueres, eller manuelt angive, hvor produkterne skal distribueres til, og hvor meget der bliver distribueret til de enkelte butikker. Proceduren omfatter ikke opsætning af data, der kan bruges i cross-dock'en som f.eks. genopfyldningsregler, organisationshierarkier og vægten af butikken. Proceduren bruger demofirmaet USRT.

1. Gå til Alle indkøbsordrer.
2. Vælg en indkøbsordre på listen, og klik på linket for at åbne ordren.
3. Klik på Retail og Commerce i handlingsruden.
4. Klik på Cross docking.
5. Klik på Rediger.
    * Kategorien, der kan bruges til at filtrere varerne i sektionen Linjer.  
6. Find og vælg den ønskede post på listen.
7. Skriv en værdi i feltet Antal til direkte levering for at angive, hvor meget af den mængde, der købes af det valgte produkt, der skal fordeles.
8. I feltet Yderligere antal til direkte levering skal du angive en værdi for at angive mængderne, der skal fordeles for de tilgængelige produkter, der købes
9. Angiv "Lokationsvægt" i feltet Distribution.
    * Du kan vælge andre typer for at bruge forskellige regler for fordelingen.  
10. Vælg en værdi i feltet Opfyldningshierarki.
11. Vælg Ja i feltet Respektér udvalg.
12. Klik på Beregn antal.
13. Klik på Opret ordre.
14. Klik på Ja.
15. På listen skal du finde og vælge et lagersted, der har modtaget produkter.
16. Klik på Bestil for at få vist de ordrer, der blev oprettet for det valgte lagersted



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]