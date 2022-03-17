---
title: Regnskabsfordelinger og kladdepostering for kreditorfakturaer
description: Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura. Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358175"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Regnskabsfordelinger og kladdepostering for kreditorfakturaer

[!include [banner](../includes/banner.md)]

Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura. Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger. 

## <a name="accounting-distributions"></a>Regnskabsfordelinger 

Du kan bruge følgende knapper på siden Kreditorfaktura til at få vist og eventuelt ændre regnskabsfordelingerne for hvert beløb på kreditorfakturaen.
-   **Distribuer beløb** – vis og ret de regnskabsmæssige fordelinger for en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter. Du kan også se og redigere regnskabsfordelinger for den underordnede linje direkte fra siden **Momstransaktioner** eller siden **Gebyrtransaktioner**.
    -   Ændre beløb i fakturahoveder, f.eks. afgifter eller valutaafrundingsbeløb.
    -   Reducer linjebeløb i kreditorfakturaen.
-   **Få vist fordelinger** – Få vist regnskabsfordelingerne for alle linjer i dokumentet. Du kan ikke redigere de regnskabsmæssige fordelinger fra denne visning.
    -   Få vist overskrifts- og linjebeløb.

Hvis kreditorfakturaen henviser til en indkøbsordre, kan du opdele og redigere regnskabfordelingerne for linjer, der indeholder en vare, der ikke er på lager. Hvis kreditorfakturalinjen ikke henviser til en indkøbsordrelinje, kan du også slette en regnskabsfordeling. Du kan ikke opdele eller slette linjer for afgifter, skatter og linjerabatter. Du kan ændre finanskontoen, men du kan ikke ændre beløb eller procenter.
> [!NOTE]                                                                                                                                 
> Hvis den overordnede linje indeholder en vare, der ikke føres på lager, og regnskabsfordelingerne er opdelt, opdeles den underordnede linje automatisk, så den svarer til de økonomiske dimensioner for den overordnede linje. De regnskabsmæssige fordelinger for den underordnede linje kan ikke opdeles yderligere eller blive slettet, men afhængigt af opsætningen af den underordnede linje kan du muligvis ændre finanskontoen for regnskabsfordelingerne af den underordnede linje.

## <a name="distributing-amounts"></a>Fordeling af beløb
Når du indtaster en kreditorfaktura, fordeles hvert beløb på følgende måde.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type kreditorfakturalinje</th>
<th>Prioritering, der bestemmer, hvor den primære konto vises fra</th>
<th>Prioritering, der bestemmer, hvilke standard for økonomisk dimensionsværdi der vises.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lagerført produkt</td>
<td><ol>
<li>Regnskabsfordeling for indkøbsordrelinjen.</li>
<li>Feltet <strong>Hovedkonto</strong>, når Udgifter til indkøb for produkt er markeret på siden <strong>Bogføring</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Brug de finansielle standarddimensionsværdier på kreditorfakturaen.</li>
</ol></td>
</tr>
<tr class="even">
<td>En indkøbskategori eller et produkt, der ikke er på lager.</td>
<td><ol>
<li>Regnskabsfordelingen for købsordrelinjen, hvis kreditorfakturalinjen henviser til en købsordrelinje.</li>
<li>Feltet <strong>Hovedkonto</strong>, når Udgifter til indkøb for udgift er markeret på siden <strong>Bogføring</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Brug de finansielle standarddimensionsværdier på kreditorfakturaen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anlægsaktiv</td>
<td><ol>
<li>Regnskabsfordelingen for købsordrelinjen, hvis kreditorfakturalinjen henviser til en købsordrelinje.</li>
<li>Hvis <strong>Anskaffelse</strong> er valgt i feltet <strong>Posteringstype</strong> på siden <strong>Kreditorfaktura</strong>, feltet <strong>Hovedkonto</strong>, når <strong>Anskaffelse</strong> er markeret på siden <strong>Posteringsprofiler for anlægsaktiver</strong>.</li>
<li>Hvis <strong>Anskaffelsesregulering</strong> er valgt i feltet <strong>Posteringstype</strong>, feltet <strong>Hovedkonto</strong>, når <strong>Anskaffelsesregulering</strong> er markeret på siden <strong>Posteringsprofiler for anlægsaktiver</strong>.</li>
</ol></td>
<td><ol>
<li>Brug regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Projekt, der er defineret på kreditorfakturalinjen</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Hvis <strong>Saldo</strong> er valgt i feltet <strong>Bogfør omkostninger - Vare</strong> på siden <strong>Projektgrupper</strong>, feltet <strong>Hovedkonto</strong>, når <strong>Omkostning</strong> er valgt på siden <strong>Opsætning af finanskontering</strong>.</li>
<li>Hvis <strong>Drift</strong> er valgt i feltet <strong>Bogfør omkostninger - Vare</strong> på siden <strong>Projektgrupper</strong>, feltet <strong>Hovedkonto</strong>, når <strong>Omkostning - vare</strong> er valgt på siden <strong>Opsætning af finanskontering</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjerabat</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Feltet <strong>Hovedkonto</strong> når, <strong>Rabat</strong> er valgt på siden <strong>Bogføring</strong>.</li>
<li>Hvis der ikke er defineret en primær konto til en rabat på posteringsprofilen, regnskabsfordelingen for den samlede pris på købsordrelinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier for kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Indkøbstillæg, der angives under fanen <strong>Pris og rabat</strong> på indkøbsordrelinjen</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Regnskabsfordelinger af den udvidede pris på indkøbsordrelinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjetillæg</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Hvis <strong>Finanskonto</strong> er valgt i feltet <strong>Debettype</strong> på siden <strong>Gebyrkode</strong>, feltet <strong>Debetkonto</strong> på siden <strong>Gebyrkode</strong>.</li>
<li>Hvis <strong>Vare</strong> er valgt i feltet <strong>Debettype</strong> på siden <strong>Gebyrkode</strong>, regnskabsfordelingen for den udvidede pris på indkøbsordrelinjen.</li>
<li>Hvis <strong>Debitor/Kreditor</strong> er valgt i feltet <strong>Debettype</strong> på siden <strong>Gebyrkode</strong>, feltet <strong>Kreditkonto</strong> på siden <strong>Gebyrkode</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Moms med følgende betingelse:
<ul>
<li>Indstillingen <strong>Anvend amerikanske momsregler</strong> er valgt på siden <strong>Finansparametre</strong>.</li>
</ul></td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Regnskabsfordelingen af den udvidede pris eller gebyret.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Moms med følgende betingelser:
<ul>
<li>Indstillingen <strong>Anvend amerikanske momsregler</strong> er ikke valgt på siden <strong>Finansparametre</strong>.</li>
<li>Feltet <strong>Importmoms</strong> for momsgruppen er ikke valgt på siden <strong>Momsgrupper</strong>.</li>
</ul></td>
<td><ol>
<li>Hvis momsbeløbet kan refunderes, feltet <strong>Indgående moms</strong> på siden <strong>Finanskonteringsgrupper</strong>.</li>
<li>Hvis skattebeløbet ikke er refunderbart, den udvidede pris eller regnskabsfordelingen for gebyret.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Moms med følgende betingelser:
<ul>
<li>Indstillingen Anvend amerikanske momsregler er ikke valgt på siden <strong>Finansparametre</strong>.</li>
<li>Feltet <strong>Importmoms</strong> for momsgruppen er valgt på siden <strong>Momsgrupper</strong>.</li>
</ul></td>
<td><ol>
<li>Hvis momsbeløbet kan refunderes, feltet <strong>Indgående moms</strong> på siden <strong>Finanskonteringsgrupper</strong>.</li>
<li>Hvis momsbeløbet ikke kan refunderes, feltet <strong>Udgift for importmoms</strong> på siden <strong>Finanskonteringsgrupper</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Gebyr i overskrift</td>
<td><ol>
<li>Hvis <strong>Finanskonto</strong> er valgt i feltet <strong>Debettype</strong> på siden <strong>Gebyrkode</strong>, feltet <strong>Debetkonto</strong> på siden <strong>Gebyrkode</strong>.</li>
<li>Hvis <strong>Debitor/Kreditor</strong> er valgt i feltet <strong>Debettype</strong> på siden <strong>Gebyrkode</strong>, feltet <strong>Kreditkonto</strong> på siden <strong>Gebyrkode</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Brug standardskabelonværdierne for den økonomiske dimension fra kreditorfakturahovedet.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ordrehovedrabat</td>
<td><ol>
<li>Feltet <strong>Hovedkonto</strong> for bogføringstype <strong>Kreditor, fakturarabat</strong> på siden <strong>Konti til automatisk posteringer</strong>.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden <strong>Kontoplan</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Fordeling af skatter

Regnskabsfordelinger for skat kan ikke oprettes, før der er beregnet skat. Hvis du vil beregne moms, skal du fuldføre en af følgende opgaver på siden **Kreditorfaktura**:
-   Få vist fakturatotalen.
-   Få vist momsen.
-   Få vist reskontrokladden.
-   Få vist regnskabsfordelinger for den færdige kreditorfaktura.
-   Sæt kreditorfakturaen på hold.
-   Bogfør kreditorfakturaen.

## <a name="subledger-journals-for-vendor-invoices"></a>Reskontrokladder for kreditorfakturaer
Før du bogfører en kreditorfaktura, kan du få vist den komplette regnskabspost for fakturaen, hvilket omfatter debit og kredit, for at kontrollere, at fakturaen bogføres på de rigtige konti. Denne visning af hele regnskabsenheden kaldes en reskontrokladde. 

Hvis kladdeposteringen for reskontroer er forkert, når du gennemser den før journalisering af kreditorfakturaen, kan du ikke ændre kladdeposteringen for reskontro. I stedet skal du redigere de regnskabsmæssige fordelinger eller posteringsprofilen. De regnskabsmæssige fordelinger bruges til at definere én side af regnskabsenheden, debiteringen eller krediteringen. Den modsvarende kontopost for reskontrokladde oprettes ved hjælp af posteringsprofiler, f.eks fra kreditorkontoen eller skat.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
