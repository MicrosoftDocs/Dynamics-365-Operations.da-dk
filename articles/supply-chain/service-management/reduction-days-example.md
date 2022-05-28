---
title: Eksempel på reduktionsdage
description: Eksempel på reduktionsdage.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674807"
---
# <a name="reduction-days-example"></a>Eksempel på reduktionsdage

[!include [banner](../includes/banner.md)]

Du har oprettet en abonnementspostering for en kundes vedligeholdelsesabonnement som vist i tabellen nedenfor.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
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