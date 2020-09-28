---
title: Råbalance med detaljeret transaktionsrapport
description: I dette emne beskrives standardrapporten til råbalancer. Her beskrives også de komponenter, der er knyttet til denne rapport, og hvordan du kan redigere rapporten, så den passer til virksomhedens behov.
author: v-kiarnd
manager: AnnBe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2019-10-24
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 76b0560499532eb3e97b03a9e797a9168ebcbcdc
ms.sourcegitcommit: d6b17b9bafa84b574a597a560a80e6b7b1852b14
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/12/2020
ms.locfileid: "3799917"
---
# <a name="trial-balance-with-transactional-detail-report"></a>Råbalance med detaljeret transaktionsrapport

[!include [banner](../includes/banner.md)]

I dette emne beskrives standardrapporten til råbalancer. Her beskrives også de komponenter, der er knyttet til denne rapport, og hvordan du kan redigere rapporten, så den passer til virksomhedens behov.

Du kan bruge **Råbalance med detaljeret transaktionsrapport**-rapporten til at få vist detaljer om hver enkelt transaktion for finanskonti. Rapporten indeholder følgende oplysninger: 

- Startsaldi
- Debet- og kreditbeløb 
- De resulterende saldi for et datointerval på 31 dage eller derunder

I forbindelse med transaktioner indeholder rapporten følgende oplysninger: 

- Posteringsdato
- Bilagsnummer
- Kontonummer
- Dokumentnr.
- Finansdimension
- Finansdimensionsnavn
- Posteringsbeskrivelse
- Debet- eller kreditbeløb
- En løbende saldo for året til dato baseret på det indeværende regnskabsår

Du kan bruge råbalance til at identificere fejl i kontosaldi. Alle konti, der har debetsaldi, skal svare til alle konti, der har kreditsaldi. Rapporten indeholder oplysninger fra finanskladdens regnskabsposter.

Du kan filtrere dataene efter et af følgende punkter:

- Bogførte posteringer
- Ventende transaktioner (disse transaktioner omfatter alle transaktioner, der ikke er bogført). 
- Alle transaktioner 

Hvis transaktionerne omfatter økonomiske dimensioner, vises disse oplysninger under en finanskonto i rapporten. Ellers grupperes oplysningerne for økonomiske dimensioner øverst på siden. 

I øjeblikket eksporteres rapporten direkte til Microsoft Excel. 

## <a name="transaction-information-on-the-report"></a>Transaktionsoplysninger i rapporten

Afhængigt af transaktionstypen, f.eks. en avanceret finanspost (ALE) eller en indkøbsordre, vises følgende yderligere oplysninger i rapporten.

<table> 
<thead>
<tr>
<th>Konteringstype</th>
<th>Yderligere dokumentoplysninger</th>
<th>Yderligere beskrivelsesoplysninger</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<ul>
<li>ALE-bilag</li>
<li>Fordelingsregel</li>
<li>Overførsel af finanskladde</li>
<li>Kladden</li>
</ul>
</td>
<td>ALE-nummer eller finanskladdenummer</td>
<td>Beskrivelse af linjeelement</td>
</tr>
<tr>
<td></td>
<td>Ingen data</td>
<td>Beskrivelse af overskrift i ALE eller finanskladde</td>
</tr>
<tr>
<td>
<ul>
<li>Fakturabilag</li>
<li>Kreditnotabilag</li>
</ul>
</td>
<td>Fakturanummer</td>
<td>Kreditornummer og kreditornavn</td>
</tr>
<tr>
<td></td>
<td>Fakturadato</td>
<td>Beskrivelse af linjeelement</td>
</tr>
<tr>
<td></td>
<td>Ingen data</td>
<td>Indkøbsordrenummer og/eller PA-nummer</td>
</tr>
<tr>
<td>Betalingsbilag for kreditor</td>
<td>Checknummer eller nummer på elektronisk pengeoverførsel</td>
<td>Kreditornummer – kreditornavn for "skal betales" eller faktureringskonto</td>
</tr>
<tr>
<td></td>
<td>Checkdato, elektronisk pengeoverførselsdato eller udligningsdato</td>
<td>Kreditornummer og kreditornavn for den oprindelige ordrekonto</td>
</tr>
<tr>
<td>
<ul>
<li>Fritekstkreditnota</li>
<li>Fritekstfakturabilag</li>
</ul>
</td>
<td>Nummer på fritekstfaktura</td>
<td>Kundenummer og kundenavn</td>
</tr>
<tr>
<td></td>
<td>Faktureringskode</td>
<td>Beskrivelse af linjeelement i fritekstfaktura<br>
(Feltet <strong>Beskrivelse</strong> i oversigtspanelet <strong>Fakturalinjer</strong> på siden <strong>Fritekstfakturaer</strong>)</td>
</tr>
<tr>
<td>Betalingsbilag for debitor (AR)</td>
<td>Kladdebatchnummer<br>
(Feltet <strong>Kladdebatchnummer</strong> under fanen <strong>Oversigt</strong> på siden <strong>Betalingskladde</strong>)</td>
<td>Kundenummer – kundenavn<br>
(Felterne <strong>Konto</strong> og <strong>Kontonavn</strong> under fanen <strong>Oversigt</strong> på siden <strong>Kladdebilag</strong>)</td>
</tr>
<tr>
<td></td>
<td>Betalingsreference</td>
<td>Betegnelse for linjen.<br>
(Feltet <strong>Beskrivelse</strong> under fanen <strong>Oversigt</strong> på siden <strong>Kladdebilag</strong>)</td>
</tr>
<tr>
<td>Budgetposteringer</td>
<td>Budgetregisterpostens nummer</td>
<td>Beskrivelse af budgetregisterpost</td>
</tr>
<tr>
<td></td>
<td>Budgetkode</td>
<td>Årsagskode – Beskrivelse af overskrift for budgetregisterpost<br>
(Feltet <strong>Kommentar</strong> i oversigtspanelet <strong>Oplysninger om budgetkontoposter</strong> på siden <strong>Budgetpost</strong> eller <strong>Budgetregisterpost </strong>)</td>
</tr>
<tr>
<td>
<ul>
<li>Indkøbsordrebekræftelse</li>
<li>Bekræftelsesbilag på indkøbsordre</li>
</ul>
</td>
<td>Indkøbsordrenummer</td>
<td>Beskrivelse af linjeelement<br>
(Feltet <strong>Tekst</strong> i oversigtspanelet <strong>Linjedetaljer</strong> på siden <strong>Indkøbsordre</strong>)</td>
</tr>
<tr>
<td></td>
<td>Nummer på indkøbsordrelinje</td>
<td>Indkøbskategori</td>
</tr>
<tr>
<td>Indkøbsrekvisitionsbilag</td>
<td>Indkøbsrekvisitionsnummer</td>
<td>Navn på indkøbsrekvisition</td>
</tr>
<tr>
<td></td>
<td>Indkøbsrekvisitionslinjenummer</td>
<td>Beskrivelse af indkøbsrekvisitionslinje<br>
(Feltet <strong>Produktnavn</strong> i oversigtspanelet <strong>Indkøbsrekvisitionslinjer</strong> på siden <strong>Indkøbsrekvisition</strong>)</td>
</tr>
<tr>
<td>
<ul>
<li>Projektfakturabilag</li>
<li>Projektfaktura</li>
</ul>
</td>
<td>Projektfakturanummer</td>
<td>Fakturakonto og kontonavn</td>
</tr>
<tr>
<td></td>
<td>Finansieringskilde</td>
<td>Projekt-id og projektnavn</td>
</tr>
</tbody>
</table>
