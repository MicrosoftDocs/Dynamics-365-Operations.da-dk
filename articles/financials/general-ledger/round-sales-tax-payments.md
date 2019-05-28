---
title: Momsafregninger og afrundingsregler
description: I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531851"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Momsafregninger og afrundingsregler

[!include [banner](../includes/banner.md)]

I denne artikel forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.

Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne. Dette kan gøres ved at køre processen til udligning og postering af moms på siden Moms. Moms for en periode udlignes til momskontiene og momssaldoen posteres til momsafregningskontoen. Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden Moms. 

Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.

Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.

## <a name="examples"></a>Eksempler

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
| Egen fordel, for en debetsaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Ingen afrunding overhovedet, da afrundingen er 0,00

afrund(1,0151, 0,00) = 1,0151 afrund(1,0149, 0,00) = 1,0149

### <a name="normal-round-and-round-precision-is-001"></a>Normal afrunding og afrundingspræcision er 0,01

<table>
  <tr>
    <td>Afrunding
    </td>
    <td>Beregningsproces
    </td>
  </tr>
    <tr>
    <td>afrund(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>afrund(1,015 / 0,01, 0) = afrund(101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afrund(1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>afrund(1,014 / 0,01, 0) = afrund(101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afrund(1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>afrund(1,011 / 0,02, 0) = afrund(50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>afrund(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>afrund(1,009 / 0,02, 0) = afrund(50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed. 

Du kan finde flere oplysninger under følgende emner:
- [Momsoversigt](indirect-taxes-overview.md)
- [Oprette en momsbetaling](tasks/create-sales-tax-payment.md)
- [Oprette momsposteringer i dokumenter](tasks/create-sales-tax-transactions-documents.md)
- [Vise bogførte momstransaktioner](tasks/view-posted-sales-tax-transactions.md)
- [afrundingsfunktion](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


