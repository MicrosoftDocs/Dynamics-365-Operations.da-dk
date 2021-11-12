---
title: Momsafregninger og afrundingsregler
description: I dette emne forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a75d41195875c5ed48cbe8ce5f5e448f173e718
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726794"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Momsafregninger og afrundingsregler

[!include [banner](../includes/banner.md)]

I dette emne forklares opsætning af afrundingsregel for momsmyndigheder og afrunding af momssaldoen under jobbet Afregn og bogfør moms.

Moms skal med jævne mellemrum rapporteres og betales til skattemyndighederne. Denne handling kan udføres ved at køre processen Afregn og bogfør moms på siden **Moms**. Moms for en periode afregnes på momskontiene, og momssaldoen posteres på momsafregningskontoen. Momssaldoen, der bogføres på afregningskontoen Moms, afrundes som krævet af skattemyndighederne ved at angive en afrundingsregel på siden **Moms**. 

Afrundingsdifferencen bogføres på momsen afrundingskontoen Moms, der er valgt i feltet Konti til automatisk posteringer under Finans.

Det nedenstående eksempel illustrerer, hvordan afrundingsreglen på skattemyndigheden fungerer.

## <a name="examples"></a>Eksempler

Den samlede moms for en periode viser en kreditsaldo på -98.765,43. Den juridiske enhed opkrævede mere moms, end den betalte. Den juridiske enhed skylder derfor penge til skattemyndighederne. 

Den juridiske enhed vil bruge en afrundingsmetode, der afrunder saldoen til nærmeste hele 1,00. Den bruger, der er ansvarlig for bogføring af moms, udfører følgende trin.

1. Klik på **Moms** > **Indirekte skatter** > **Moms** > **Momsmyndigheder**.
2. I oversigtspanelet **Generelt** skal du vælge **Normal** i feltet **Afrundingsform**.
3. Angiv 1,00 i feltet **Afrunding**.
4. Når det er tid til at betale momsen til skattemyndighederne, skal du gå til **Moms** > **Erklæringer** > **Moms** > **Afregn og bogfør moms**. I momsafregningskontoen kan du se, at skattetilsvarsbeløbet på **98.765,43** er afrundet til **98.765**.

Følgende tabel viser, hvordan et beløb på 98.765,43 afrundes ved hjælp af hver afrundingsmetode, der er tilgængelig i feltet **Afrundingsform** på siden **Skattemyndigheder**.

> [!NOTE]                                                                                  
> Hvis afrundingsværdien er angivet til 0,00, gælder følgende:
>
> - Ved normal afrunding er afrundingsfunktionen den samme som for **Afrunding = 0,01**.
> - I forbindelse med **Indstilling for afrundingsform**, **Nedad**, **Oprunding** og **Egen fordel** er funktionsmåden den samme som for **Afrunding = 1,00**.

| Indstilling for afrundingsform                | Afrundingsværdi = 0,01 | Afrundingsværdi = 0,10 | Afrundingsværdi = 1,00 | Afrundingsværdi = 100,00 | Afrundingsværdi = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normal                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Nedad                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Oprunding                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Egen fordel, for en kreditsaldo | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Egen fordel, for en debetsaldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normal afrunding og afrundingspræcision er 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Hvis du vælger Egen fordel, er afrundingen altid til fordel for den juridiske enhed. 

Du kan finde flere oplysninger under følgende emner:
- [Momsoversigt](indirect-taxes-overview.md)
- [Oprette en momsbetaling](tasks/create-sales-tax-payment.md)
- [Oprette momstransaktioner på dokumenter](tasks/create-sales-tax-transactions-documents.md)
- [Vise bogførte momstransaktioner](tasks/view-posted-sales-tax-transactions.md)
- [afrundingsfunktion](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
