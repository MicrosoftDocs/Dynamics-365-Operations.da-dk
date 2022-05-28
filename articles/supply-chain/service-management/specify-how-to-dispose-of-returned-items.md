---
title: Angive, hvordan returvarer skal kasseres
description: Angiv, hvordan returvarer skal kasseres.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3123f49ef5fbd07afa61b035a2f6dd4c0af2ce40
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679213"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Angive, hvordan returvarer skal kasseres

[!include [banner](../includes/banner.md)]

Når du håndterer en returordre, skal du angive en årsagskode for returneringer for at fortælle, hvorfor produktet returneres. Du skal også angive en dispositionskode og en dispositionshandling for at afgøre, hvad der skal ske med selve det returnerede produkt.

En dispositionskode kan anvendes, når du opretter en returordre, registrerer en varetilgang eller følgeseddelopdaterer en varetilgang og afslutter en karantæneordre.

Du kan angive de dispositionskoder, du har brug for for at understøtte forretningsprocesserne. Nedenstående tabel indeholder et sæt af typisk anvendte koder til tildeling af disposition for returvarer.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Dispositionstype</p></th>
<th><p>Fælles kode</p></th>
<th><p>Beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Kassation</p></td>
<td><p>SC</p></td>
<td><p>Kasser/Destruer</p></td>
</tr>
<tr class="even">
<td><p>Kassation</p></td>
<td><p>DC</p></td>
<td><p>Giv til velgørenhed</p></td>
</tr>
<tr class="odd">
<td><p>Kassation</p></td>
<td><p>TD</p></td>
<td><p>Tredjepartskassation</p></td>
</tr>
<tr class="even">
<td><p>Kassation</p></td>
<td><p>SL</p></td>
<td><p>Restværdi</p></td>
</tr>
<tr class="odd">
<td><p>Kassation</p></td>
<td><p>TS</p></td>
<td><p>Tredjepartssalg (sekundære markeder)</p></td>
</tr>
<tr class="even">
<td><p>Reparer/Modificer</p></td>
<td><p>RW</p></td>
<td><p>Genbearbejdning</p></td>
</tr>
<tr class="odd">
<td><p>Reparer/Modificer</p></td>
<td><p>RF</p></td>
<td><p>Genproduktion/Geninstallation</p></td>
</tr>
<tr class="even">
<td><p>Reparer/Modificer</p></td>
<td><p>MD</p></td>
<td><p>Modificer</p></td>
</tr>
<tr class="odd">
<td><p>Reparer/Modificer</p></td>
<td><p>RP</p></td>
<td><p>Reparer</p></td>
</tr>
<tr class="even">
<td><p>Reparer/Modificer</p></td>
<td><p>RV</p></td>
<td><p>Returner til leverandør</p></td>
</tr>
<tr class="odd">
<td><p>Andet</p></td>
<td><p>AI</p></td>
<td><p>Brug som den er</p></td>
</tr>
<tr class="even">
<td><p>Andet</p></td>
<td><p>RS</p></td>
<td><p>Videresalg</p></td>
</tr>
<tr class="odd">
<td><p>Andet</p></td>
<td><p>EX</p></td>
<td><p>Veksling</p></td>
</tr>
<tr class="even">
<td><p>Andet</p></td>
<td><p>MS</p></td>
<td><p>Diverse</p></td>
</tr>
</tbody>
</table>


Du skal vælge en dispositionshandling for hver dispositionskode, du definerer. Dispositionshandlingen bestemmer de fysiske og økonomiske følger af dispositionskoderne. Dispositionshandlingen bestemmer f.eks. den fysiske håndtering af den returnerede vare, den økonomiske effekt af den returnerede vare, og om der skal sendes en erstatningsvare til kunden. Du kan definere et ubegrænset antal dispositionskoder, afhængigt af virksomhedens behov, men der er kun seks foruddefinerede dispositionshandlingerne, du kan vælge mellem. Følgende tabel indeholder dispositionshandlingerne og deres definitioner.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Dispositionshandling</p></th>
<th><p>Beskrivelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kredit</strong></p></td>
<td><p>Returner varen til lageret, og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Krediter kun</strong></p></td>
<td><p>Krediter kunden uden at kræve eller forvente, at varen returneres.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Spild</strong></p></td>
<td><p>Kassér varen, og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Erstat og krediter</strong></p></td>
<td><p>Returner varen til lageret, opret en erstatningsordre, og krediter kunden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Erstat og kasser</strong></p></td>
<td><p>Kassér varen, opret en erstatningsordre, og krediter kunden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Returner til kunde</strong></p></td>
<td><p>Afvis den returnerede vare, og returner den til debitoren.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Vælge en dispositionskode for en karantæneordre

1. Gå til **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karantæneordrer**.
1. For en eksisterende karantæneordre skal du vælge en handling i feltet **Dispositionskode** under fanen **Oversigt**.

## <a name="see-also"></a>Se også

[Karantæneordre (form)](/dynamicsax-2012//quarantine-order-form)

[Dispositionskoder (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
