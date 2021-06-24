---
title: Regnskabsfordelinger og kladdeposteringer til fritekstfakturaer
description: Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan indtægt, skat eller afgifter redegøres for på en fritekstfaktura. Alle beløb, der skal tages redegøres for, når fritekstfakturaen journaliseres, har en eller flere regnskabsfordelinger.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3e1e0a757dcd51edcd38bb348e52b756e57334
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188752"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Regnskabsfordelinger og posteringer for reskontro til fritekstfakturaer

[!include [banner](../includes/banner.md)]

Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan indtægt, skat eller afgifter redegøres for på en fritekstfaktura. Alle beløb, der skal tages redegøres for, når fritekstfakturaen journaliseres, har en eller flere regnskabsfordelinger.

## <a name="accounting-distributions"></a>Regnskabsfordelinger

Du kan bruge følgende knapper på siden Fritekstfaktura til at få vist og eventuelt ændre regnskabsfordelingerne for hvert beløb på fritekstfakturaen.

-   **Distribuer beløb** – Vis og ret de regnskabsmæssige fordelinger for en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter. Du kan også få vist og redigere regnskabsfordelinger for den underordnede linje direkte fra siden Momstransaktioner eller siden Gebyrposter.
    -   Ret overskriftsbeløb i fritekstfakturaer, f.eks. afgifter eller valutaafrundingsbeløb.
    -   Ret linjebeløb i fritekstfaktura.
-   **Få vist fordelinger** – Få vist regnskabsfordelingerne for alle linjer i dokumentet. Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.
    -   Få vist overskrifts- og linjebeløb.

## <a name="distributing-amounts"></a>Fordeling af beløb
Når du indtaster en fritekstfaktura, fordeles hvert beløb på følgende måde.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type pengebeløb</th>
<th>Hvor hovedkontoen vises fra</th>
<th>Prioritering, der bestemmer, hvilke standard for økonomisk dimensionsværdi der vises.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Linje i fritekstfaktura</td>
<td>Finanskontoen på fritekstfakturalinjen.</td>
<td><ol>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Linje i fritekstfaktura til en kombination af et anlægsaktivnummer og en værdimodel
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Bemærk! </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hovedkontoen på linjen i fritekstfakturaen vil være anlægsaktivets kassationskonto.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Finanskontoen på fritekstfakturalinjen.</td>
<td><ol>
<li>Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Rabatbeløb i fritekstfakturaen</td>
<td>Feltet Hovedkonto til debitorrabatter på siden Kasserabatter.</td>
<td><ol>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Momsbeløb i fritekstfaktura</td>
<td>Feltet Moms, der skal betales på siden Finanskonteringsgrupper.</td>
<td><ol>
<li>Brug de økonomiske dimensioner, der er defineret i linjebeløbet i fritekstfakturaen eller fordelingerne for gebyrlinjebeløbet.</li>
<li>Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Gebyrlinjebeløb i fritekstfaktura</td>
<td>Feltet Kreditkonto på siden Gebyrkode.</td>
<td><ol>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Hvis hovedkontoen ikke er en fordelingskonto, skal du bruge standardskabelonen for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug standardværdierne for økonomisk dimension på linjen i fritekstfakturaen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra finanskontoen på siden Kontoplan.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Fordeling af skatter
Regnskabsfordelinger for skat kan ikke oprettes, før der er beregnet skat. Hvis du vil beregne moms, skal du fuldføre en af følgende opgaver i formularen Fritekstfaktura:
-   Få vist momsen.
-   Få vist fakturatotalen.
-   Få vist pengestrømmen.
-   Få vist regnskabsmæssige fordelinger for hele fritekstfakturaen.
-   Få vist reskontrokladden.

## <a name="subledger-journals-for-free-text-invoices"></a>Reskontrokladder til fritekstfakturaer
Før du bogfører en fritekstfaktura, kan du få vist den komplette regnskabsenhed for fakturaen, hvilket omfatter debiteringer og krediteringer til kontrol af, at fakturaen bogføres på de rigtige konti. Denne visning af hele regnskabsenheden kaldes en reskontrokladde. Hvis kladdeposteringen for reskontro er forkert, når du gennemser den før journalisering af fritekstfakturaen, kan du ikke ændre kladdeposteringen for reskontroen. I stedet skal du redigere de regnskabsmæssige fordelinger eller posteringsprofilen. De regnskabsmæssige fordelinger bruges til at definere én side af regnskabsenheden, debiteringen eller krediteringen. Den modsvarende kontopost for reskontrokladde oprettes ud fra posteringsprofiler, f.eks fra debitorkontoen eller afgiften.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]