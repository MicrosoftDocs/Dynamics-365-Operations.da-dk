---
title: Lagerobjektværdier
description: Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a5dd487b9213f8f1289412a6a7b8112e6b57df6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670378"
---
# <a name="inventory-object-values"></a>Lagerobjektværdier

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt. 

Med en ny funktion, der hedder **Fysisk antal**, kan du se værdierne for et bestemt lagerobjektet. 

Et omkostningsobjekt repræsenterer enhedsniveauet, hvor der udføres lagerregnskab. Du kan finde flere oplysninger om omkostningsobjekter i [Omkostningsobjekter](cost-object.md). 

Hvis du vil se værdierne i et bestemt lagerobjekt, skal du klikke på **Fysisk antal** på siden **Omkostningsobjekt**. Sådan beregnes værdien af et lagerobjekt: 

Lager object.Value = Omkostning object.Average enhedskostpris × Lager object.Quantity 

Følgende eksempel viser, hvordan værdierne af et lagerobjekt og et omkostningsobjekt beregnes. To hændelser til modtagelse af produktet er registreret for vare A:

-   Produktkvittering 1: antal = 100 stk., beløb = $1.000,00, websted = 1, lager = 11, batchnummer = B1
-   Produktkvittering 2: antal = 50 stk., beløb = $800,00, websted = 1, lager = 11, batchnummer = B2

I følgende tabel vises resultatet af beregningen for et omkostningsobjekt. Du kan få vist fakturaen på siden **Omkostningsobjekt**.

<table>
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttype</th>
<th>Varenummer</th>
<th>Lokation</th>
<th>Antal</th>
<th>Lagerenhed</th>
<th>Værdi</th>
<th>Gennemsnitlig enhedskostpris</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Omkostningsobjekt</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Styk</td>
<td><p>$1800,00</p></td>
<td><p>$12,00</p></td>
</tr>
</tbody>
</table>

I følgende tabel vises resultatet af beregningen for et lagerobjekt. Du kan få vist resultatet ved at klikke på **Fysisk antal** på siden **Omkostningsobjekt**.

<table>
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttype</th>
<th>Varenummer</th>
<th>Lokation</th>
<th>Lagersted</th>
<th>Batch nr.</th>
<th>Antal</th>
<th>Lagerenhed</th>
<th>Værdi</th>
<th>Gennemsnitlig enhedskostpris</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lagerobjekt</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Styk</td>
<td><p>$1200,00</p></td>
<td><p>$12,00</p></td>
</tr>
<tr class="even">
<td>Lagerobjekt</td>
<td>T</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Styk</td>
<td><p>$600,00</p></td>
<td><p>$12,00</p></td>
</tr>
</tbody>
</table>



## <a name="additional-resources"></a>Yderligere ressourcer

[Omkostningsobjekter](cost-object.md)

[Omkostningsposter](cost-entries.md)

[Nyheder og ændringer](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]