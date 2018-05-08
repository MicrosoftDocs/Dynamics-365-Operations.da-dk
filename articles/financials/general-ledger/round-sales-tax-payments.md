---
title: Momsafregninger og afrundingsregler
description: "I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>Momsafregninger og afrundingsregler

[!include [banner](../includes/banner.md)]

I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.

Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne. Dette kan gøres ved at køre processen til udligning og postering af moms på siden Moms. Moms for en periode udlignes til momskontiene og momssaldoen posteres til momsafregningskontoen. Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms. 

Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.

Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.

### <a name="example"></a>Eksempel:

Den samlede moms for en periode viser en kreditsaldo på -98.765,43. Den juridiske enhed opkrævede mere moms, end den betalte. Den juridiske enhed skylder derfor penge til skattemyndighederne. 

Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00. Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.

1.  Klik på Moms &gt; Indirekte skatter &gt; Moms &gt; Skattemyndigheder
2.  I oversigtspanelet Generelt skal du vælge Normal i feltet Afrundingsform.
3.  Angiv 1,00 i feltet Afrunding.
4.  Når det er tid til at betale momsen til skattemyndighederne, skal du åbne siden Afregn og bogfør moms. (Klik på Moms &gt; Opgørelser &gt; Moms &gt; Afregn og bogfør moms).
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

Du kan finde flere oplysninger under følgende emner:
- [Momsoversigt](indirect-taxes-overview.md)
- [Oprette en momsbetaling](tasks/create-sales-tax-payment.md)
- [Oprette momsposteringer i dokumenter](tasks/create-sales-tax-transactions-documents.md)
- [Vise bogførte momsposteringer](tasks/view-posted-sales-tax-transactions.md)



