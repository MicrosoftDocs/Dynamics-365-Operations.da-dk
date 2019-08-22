---
title: Regnskabsfordelinger og kladdeposteringer for reskontro til kreditorfakturaer
description: Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura. Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837560"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a>Regnskabsfordelinger og kladdeposteringer for reskontro til kreditorfakturaer

[!include [banner](../includes/banner.md)]

Regnskabsfordelinger bruges til at definere, hvordan et beløb skal redegøres for, f.eks. hvordan udgifter, skat eller afgifter redegøres for på en kreditorfaktura. Alle beløb, der skal tages i betragtning, når kreditorfakturaen journaliseres, har en eller flere regnskabsfordelinger. 

<a name="accounting-distributions"></a>Regnskabsfordelinger 
-------------------------

Du kan bruge følgende knapper på siden Kreditorfaktura til at få vist og eventuelt ændre regnskabsfordelingerne for hvert beløb på kreditorfakturaen.
-   **Distribuer beløb** – vis og ret de regnskabsmæssige fordelinger for en enkelt linje og evt. underordnede linjer, f.eks. skatter eller afgifter. Du kan også få vist og redigere regnskabsfordelinger for den underordnede linje direkte fra siden Momstransaktioner eller siden Gebyrposter.
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
<li>Feltet Hovedkonto, når Udgifter til indkøb for produkt er markeret på siden Bogføring.</li>
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
<li>Feltet Hovedkonto, når Udgifter til indkøb for udgift er markeret på siden Bogføring.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Brug de finansielle standarddimensionsværdier på kreditorfakturaen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Anlægsaktiv</td>
<td><ol>
<li>Regnskabsfordelingen for købsordrelinjen, hvis kreditorfakturalinjen henviser til en købsordrelinje.</li>
<li>Hvis Anskaffelse er valgt i feltet Posteringstype i formen Kreditorfaktura, feltet Hovedkonto, når Anskaffelse er markeret på profilsiden Bogføre anlægsaktiver.</li>
<li>Hvis Anskaffelsesregulering er valgt i feltet Posteringstype, feltet Hovedkonto, når Anskaffelsesregulering er markeret på profilsiden Bogføre anlægsaktiver.</li>
</ol></td>
<td><ol>
<li>Brug regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Projekt, der er defineret på kreditorfakturalinjen</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Hvis Balance er valgt i feltet Bogfør omkostninger - Vare på siden Projektgrupper, feltet Hovedkonto, når Omkostning er valgt på konfigurationssiden Finanskontering.</li>
<li>Hvis Drift er valgt i feltet Bogfør omkostninger - Vare på siden Projektgrupper, feltet Hovedkonto, når Omkostning - vare er valgt på konfigurationssiden Finanskontering.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Linjerabat</td>
<td><ol>
<li>Regnskabsfordelingen til købsordrelinjen, hvis fakturalinjen henviser til en købsordrelinje.</li>
<li>Feltet Hovedkonto når, Rabat er valgt på siden Bogføring.</li>
<li>Hvis der ikke er defineret en primær konto til en rabat på posteringsprofilen, regnskabsfordelingen for den samlede pris på købsordrelinjen.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier for kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Indkøbstillæg, der angives under fanen Pris og rabat på indkøbsordrelinjen</td>
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
<li>Hvis Finanskonto er valgt i feltet Debettype i formen Gebyrkode, feltet Debetkonto på siden Gebyrkode.</li>
<li>Hvis Vare er valgt i feltet Debettype i formularen Gebyrkode, regnskabsfordelingen for den udvidede pris på indkøbsordrelinjen.</li>
<li>Hvis Debitor/Kreditor er valgt i feltet Debettype i formen Gebyrkode, feltet Kreditkonto på siden Gebyrkode.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Moms med følgende betingelse:
<ul>
<li>Indstillingen Anvend amerikanske momsregler er valgt på siden Finansparametre.</li>
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
<li>Indstillingen Anvend amerikanske momsregler er ikke valgt på siden Finansparametre.</li>
<li>Feltet Importmoms for momsgruppen er ikke valgt på siden Momsgrupper.</li>
</ul></td>
<td><ol>
<li>Hvis momsbeløbet kan refunderes, feltet Konto for indgående moms på siden Finanskonteringsgrupper.</li>
<li>Hvis skattebeløbet ikke er refunderbart, den udvidede pris eller regnskabsfordelingen for gebyret.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Moms med følgende betingelser:
<ul>
<li>Indstillingen Anvend amerikanske momsregler er ikke valgt på siden Finansparametre.</li>
<li>Feltet Importmoms for momsgruppen er valgt på siden Momsgrupper.</li>
</ul></td>
<td><ol>
<li>Hvis momsbeløbet kan refunderes, feltet Konto for indgående moms på siden Finanskonteringsgrupper.</li>
<li>Hvis momsbeløbet kan ikke refunderes, feltet Udgift for importmoms på siden Finanskonteringsgrupper.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Brug de økonomiske dimensioner fra den udvidede pris eller regnskabsfordelingerne for gebyret på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Gebyr i overskrift</td>
<td><ol>
<li>Hvis Finanskonto er valgt i feltet Debettype i formen Gebyrkode, feltet Debetkonto på siden Gebyrkode.</li>
<li>Hvis Debitor/Kreditor er valgt i feltet Debettype i formen Gebyrkode, feltet Kreditkonto på siden Gebyrkode.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Hvis hovedkontoen er en fordelingskonto, skal du bruge standardværdien fra definitionen af fordelingskontoen.</li>
<li>Brug standardskabelonværdierne for den økonomiske dimension fra kreditorfakturahovedet.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ordrehovedrabat</td>
<td><ol>
<li>Feltet Hovedkonto for bogføringstype Kreditor, fakturarabat på siden Konti til automatisk posteringer.</li>
</ol></td>
<td><ol>
<li>Hvis fakturalinjen henviser til en købsordrelinje, skal du bruge kontodistributionen til købsordrelinjen.</li>
<li>Bruge økonomiske dimensioner fra regnskabfordelingerne for den udvidede pris på kreditorfakturalinjen.</li>
<li>Brug de finansielle dimensionsværdier fra kreditorfakturalinjen.</li>
<li>Brug de økonomiske standarddimensionsværdier fra hovedkontoen på siden Kontoplan.</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Fordeling af skatter
------------------

Regnskabsfordelinger for skat kan ikke oprettes, før der er beregnet skat. Hvis du vil beregne moms, skal du fuldføre en af følgende opgaver på siden Kreditorfaktura:
-   Få vist fakturatotalen.
-   Få vist momsen.
-   Få vist reskontrokladden.
-   Få vist regnskabsfordelinger for den færdige kreditorfaktura.
-   Sæt kreditorfakturaen på hold.
-   Bogfør kreditorfakturaen.

## <a name="subledger-journals-for-vendor-invoices"></a>Reskontrokladder for kreditorfakturaer
Før du bogfører en kreditorfaktura, kan du få vist den komplette regnskabspost for fakturaen, hvilket omfatter debit og kredit, for at kontrollere, at fakturaen bogføres på de rigtige konti. Denne visning af hele regnskabsenheden kaldes en reskontrokladde. 

Hvis kladdeposteringen for reskontroer er forkert, når du gennemser den før journalisering af kreditorfakturaen, kan du ikke ændre kladdeposteringen for reskontro. I stedet skal du redigere de regnskabsmæssige fordelinger eller posteringsprofilen. De regnskabsmæssige fordelinger bruges til at definere én side af regnskabsenheden, debiteringen eller krediteringen. Den modsvarende kontopost for reskontrokladde oprettes ved hjælp af posteringsprofiler, f.eks fra kreditorkontoen eller skat.





