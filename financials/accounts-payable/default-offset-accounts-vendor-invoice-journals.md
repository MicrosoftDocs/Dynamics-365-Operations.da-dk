---
title: Standardmodkonti for kreditorfakturajournaler og fakturagodkendelseskladder
description: 
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4691ac4456b08084bcd93f7a8447719a15299c93
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Standardmodkonti for kreditorfakturajournaler og fakturagodkendelseskladder

[!include[banner](../includes/banner.md)]




Standardmodkonti bruges på følgende sider for kreditorfakturakladder:

-   Fakturajournal
-    Godkendelseskladde

Brug følgende tabel til at afgøre, hvor du bør tildele standardkonti for fakturakladder.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Konfigurer standardkonti her</th>
<th>Hvor er standardkonti er</th>
<th>Hvordan denne indstilling påvirker behandling</th>
<th>Hvornår du skal bruge denne indstilling</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Kreditorgruppe</strong> – Konfigurer standardmodkonti for kreditorgrupper på siden <strong>Standardkontoopsætning</strong>, som du kan åbne fra siden <strong>Kreditorgrupper</strong>.</td>
<td><ul>
<li>Kreditorkonto</li>
<li>Kladdeposteringer for kreditorkonti i kreditorgruppen, hvis der ikke er angivet standardkonti for kreditorkonti</li>
</ul></td>
<td>Standardmodkonti for kreditorgrupper vises som standardmodkonti for kreditorer på siden <strong>Standardkontoopsætning</strong>. Du kan åbne denne side fra listesiden <strong>Alle leverandører</strong>.</td>
<td>Brug denne indstilling, hvis du typisk betaler for den samme slags ting fra samme kreditorgrupper over tid.</td>
</tr>
<tr class="even">
<td><strong>Kreditorkonto</strong> – Konfigurer standardmodkonti for kreditorkonti på siden <strong>Standardkontoopsætning</strong>, som du kan åbne fra siden <strong>Kreditorer</strong>.</td>
<td>Kladdeposteringer for kreditorkontoen</td>
<td>Standardmodkonti for kreditorkonti vises som standardmodkonti til kladdeposteringer for kreditorkontoen.</td>
<td>Brug denne indstilling, hvis du typisk betaler for den samme slags ting fra samme kreditorer over tid.</td>
</tr>
<tr class="odd">
<td><strong>Kladdenavne</strong> – Konfigurer standardmodkonti for kladder på siden <strong>Kladdenavne</strong>. Vælg indstillingen <strong>Fast modkonto</strong>. Bemærk, at du ikke kan angive standardmodkonti på kladdenavne, hvis typen af kladdenavnene, der er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</td>
<td><ul>
<li>Kladdehoved, der bruger kladdenavnet</li>
<li>Kladdeposteringer i kladder, der bruger kladdenavnet</li>
</ul></td>
<td>Hvis indstillingen <strong>Fast modkonto</strong> på siden <strong>Kladdenavne</strong> er markeret, tilsidesætter modkontoen for kladdenavnet standardmodkontoen for kreditoren eller kreditorgruppen.</td>
<td>Brug denne indstilling til at konfigurere kladder til specifikke omkostninger og udgifter, der opkræves på bestemte konti, uanset kreditoren eller hvilken kreditorgruppe kreditoren tilhører.</td>
</tr>
<tr class="even">
<td><strong>Kladdenavne</strong> – Konfigurer standardmodkonti for kladder på siden <strong>Kladdenavne</strong>. Fjern indstillingen <strong>Fast modkonto</strong>. Bemærk, at du ikke kan angive standardmodkonti på kladdenavne, hvis typen af kladdenavnene, der er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</td>
<td><ul>
<li>Kladdehoved</li>
<li>Kladdeposteringer i kladder, der bruger kladdenavnet</li>
</ul></td>
<td>Disse standardposter bruges på kladdehovedsider, og modkontoen på kladdehovedsiden bruges som en standardpost på kladdebilagssiderne. Standardkonti fra siden <strong>Kladdenavne </strong>bruges kun, hvis standardkonti ikke er konfigureret til kreditorkontoen.</td>
<td>Brug denne indstilling til at oprette de standardkonti, der bruges, når der ikke er tildelt en standardmodkonto for kreditor.</td>
</tr>
<tr class="odd">
<td><strong>Kladdehoved</strong> – Opret en standardmodkonto for en kladde som en standardpost på kladdebilagssiderne. Bemærk, at du ikke kan angive standardmodkonti på kladdehovedet, hvis typen af kladdenavnene er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</td>
<td>Kladdeposteringer i kladden</td>
<td>Standardmodkontoen for en kladde bruges som standardpost på kladdebilagssiderne.</td>
<td>Brug denne indstilling til at gøre indtastningen af data hurtigere, hvis de fleste poster i en kladde har samme modkonto.</td>
</tr>
</tbody>
</table>






