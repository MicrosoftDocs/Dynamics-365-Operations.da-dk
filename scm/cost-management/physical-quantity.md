---
title: "Lagerværdier objekt"
description: "Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Lagerværdier objekt

Denne artikel indeholder oplysninger om beregning af værdierne i et lagerobjekt. 

En ny funktion, der hedder ** fysisk antal ** kan du se værdierne for en bestemt inventory-objektet. Et omkostningsobjekt repræsenterer enhedsniveauet, hvor der udføres lagerregnskab. Du kan finde flere oplysninger om omkostningsobjekter i [Omkostningsobjekter](cost-object.md). Klik for at se værdierne i et bestemt lager objekt, **fysisk antal** på den **omkostningsobjekt** side. Her er, hvordan værdien af et objekt på lageret beregnes: Inventory-objektet. Værdi = omkostningsobjekt. Gennemsnitlig kostpris × Inventory-objektet. Antallet i følgende eksempel viser, hvordan beregnes værdier for et objekt af typen lager og et omkostningsobjekt. To hændelser til modtagelse af produktet er registreret for vare A:

-   Produktkvittering 1: antal = 100 pc'er., beløb = $1,000.00, webstedet = 1, lager = 11, Batch nr. = B1
-   Produktkvittering 2: antal = 50 pc'er., beløb = $800.00, webstedet = 1, lager = 11, Batch nr. = B2

I følgende tabel vises resultatet af beregningen for et omkostningsobjekt. Du kan få vist fakturaen på siden **Omkostningsobjekt**.

<table style="width:100%;">
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

<table style="width:100%;">
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
<td>A</td>
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



<a name="see-also"></a>Se også
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Hvad er nye og ændrede i Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

