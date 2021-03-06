---
title: Eksempel på reduktionsdage
description: Eksempel på reduktionsdage.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836056"
---
# <a name="reduction-days-example"></a>Eksempel på reduktionsdage 

[!include [banner](../includes/banner.md)]


Du har oprettet en abonnementspostering for en kundes vedligeholdelsesabonnement som vist i tabellen nedenfor.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fra dato</p></th>
<th><p>Til dato</p></th>
<th><p>Abonnement</p></th>
<th><p>Abonnementstype</p></th>
<th><p>Projekt</p></th>
<th><p>Kategori</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1. marts 2011</p></td>
<td><p>31. marts 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Regulær</strong></p></td>
<td><p>9013</p></td>
<td><p>Abn.art2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>


Kunden rapporterer, at der ikke er behov for servicedækning i to dage (d. 10. og 11. marts). Du indvilliger i at reducere abonnementet med disse to dage.

Du opretter en ny postering af typen **Reduktionsdage** som vist i tabellen nedenfor.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fra-dato</p></th>
<th><p>Til-dato</p></th>
<th><p>Abonnement</p></th>
<th><p>Abonnementstype</p></th>
<th><p>Projekt</p></th>
<th><p>Kategori</p></th>
<th><p>Salgsvaluta</p></th>
<th><p>Salgspris</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10. marts 2011</p></td>
<td><p>11. marts 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Reduktionsdage</strong></p></td>
<td><p>9013</p></td>
<td><p>Abn.art2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>


Når posteringerne for marts 2011 faktureres, reduceres salgsprisen på EUR 200 med EUR 12,90. Det beløb, der kan faktureres for abonnementsposteringen, er derfor EUR 187,10, og der faktureres to posteringer til et samlet beløb på EUR 187,10.

## <a name="see-also"></a>Se også

[Reducere dagene på abonnementsgebyrer](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]