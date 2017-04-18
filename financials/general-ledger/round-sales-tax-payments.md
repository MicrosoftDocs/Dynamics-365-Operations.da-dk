---
title: Momsafregninger og afrundingsregler
description: "I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 8f28ab4ea0fed975edbed60ddf5630d2d26ba0bc
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Momsafregninger og afrundingsregler

I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.

Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne. Dette kan gøres ved at køre på udligning og efterbehandler moms moms på siden. Moms for en periode udlignes mod moms-konti og bogføres saldoen moms til afregningskontoen moms. Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms. 

Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.

Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.

### <a name="example"></a>Eksempel:

Den samlede moms for en periode viser en kreditsaldo på -98.765,43. Den juridiske enhed opkrævede mere moms, end den betalte. Den juridiske enhed skylder derfor penge til skattemyndighederne. 

Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00. Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.

1.  Klik på skat &gt;indirekte skatter &gt;moms &gt;momsmyndigheder
2.  I oversigtspanelet Generelt skal du vælge Normal i feltet Afrundingsform.
3.  Angiv 1,00 i feltet Afrunding.
4.  Når det er tid til at betale momsen til skattemyndighederne, skal du åbne siden Afregn og bogfør moms. (Klik på skat &gt;erklæringer &gt;moms &gt;udligner og bogføre moms.)
5.  I momsafregningskontoen afrundes skattetilsvarsbeløbet på 98.765,43 til 98.765.

Følgende tabel viser, hvordan et beløb på 98.765,43 afrundes ved hjælp af hver afrundingsmetode, der er tilgængelig i feltet Afrundingsform på siden Skattemyndigheder.

| Indstilling for afrundingsform                | Afrundingsværdi = 0,01 | Afrundingsværdi = 0,10 | Afrundingsværdi = 1,00 | Afrundingsværdi = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Almindelig                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Nedad                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Oprunding                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Egen fordel, for en kreditsaldo | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Egen fordel, for en debetsaldo  | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |

> [!NOTE]                                                                                  
> Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed. 

Yderligere oplysninger finder du [oversigt over moms](indirect-taxes-overview.md). 

