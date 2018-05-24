---
title: "Overvåge politikregler"
description: "Du kan bruge overvågningspolitikker til at sikre, at udgiftsrapporter, kreditorfakturaer og indkøbsordrer overholder de politikregler, du opretter. Alle de regler, der er knyttet til en overvågningspolitik, køres i batchtilstand i henhold til en tidsplan, du angiver.  Hver politikregel er en forekomst af en politikregeltype. Kun én politikregel ad gangen kan være aktiv for hver politikregeltype."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6bebe9ce83c4b979ffbb7c86ef67ad03a650e0c2
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="audit-policy-rules"></a>Overvåge politikregler

[!include [banner](../includes/banner.md)]

Du kan bruge overvågningspolitikker til at sikre, at udgiftsrapporter, kreditorfakturaer og indkøbsordrer overholder de politikregler, du opretter. Alle de regler, der er knyttet til en overvågningspolitik, køres i batchtilstand i henhold til en tidsplan, du angiver.  Hver politikregel er en forekomst af en politikregeltype. Kun én politikregel ad gangen kan være aktiv for hver politikregeltype. 

<a name="queries-and-query-types"></a>Forespørgsler og forespørgselstyper
-----------------------

Når du opretter en overvågningspolitikregel, skal du først vælge en politikregeltype. Politikregeltypen angiver den AOT-forespørgsel (Application Object Tree), der skal bruges som udgangspunkt for oprettelse af politikreglen. Den angiver også den forespørgselstype, der skal bruges til politikreglen. Forespørgslen definerer det kildedokument, som politikreglen evaluerer. Den angiver også de felter i kildedokumentet, der identificerer både den juridiske enhed og det felt, der identificerer den dato, der skal bruges ved valg af dokumenter til overvågning. Forespørgselstypen styrer standardfelterne på forespørgselssiden og på siden Regel for overvågning. Følgende tabel viser de forespørgselstyper, der er tilgængelige for overvågningspolitikregler.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Forespørgselstype</th>
<th>Formål</th>
<th>Flere oplysninger</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Betinget</td>
<td>Evaluer kildedokumentattributter i forhold til angivne værdier.</td>
<td></td>
</tr>
<tr class="even">
<td>Aggregér</td>
<td>Evaluer flere kildedokumenter eller kildedokumentlinjer i forhold til en politikregel ved aggregering af numeriske værdier.</td>
<td></td>
</tr>
<tr class="odd">
<td>Stikprøvekontrol</td>
<td>Udvælg vilkårligt en angivet procentdel af kildedokumenterne, der skal evalueres for politikovertrædelser.</td>
<td>Når du vælger denne indstilling, skal du anvende siden Regel for overvågning til at angive procentdelen af dokumenter, der skal vælges tilfældigt til overvågning.</td>
</tr>
<tr class="even">
<td>Dupliker</td>
<td>Evaluerer kildedokumenter for at afgøre, om de indeholder identiske poster i angivne felter.</td>
<td>Når du vælger denne indstilling, skal du anvende siden Regel for overvågning til at angive det antal dage, du vil føje til starten af datointervallet for dokumentvalg, når dokumenter evalueres for identiske poster.</td>
</tr>
<tr class="odd">
<td>Listesøgning</td>
<td>Evaluer kildedokumenter for bestemte enheder.</td>
<td>Forespørgslens roddokument definerer det dokument, der overvåges. Forespørgslen skal være en listeforespørgsel, der indeholder en reference til tabellen dirpartytable. Denne indstilling kan kun bruges med følgende AOT-forespørgsler:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Udgiftsrapport - overvågede medarbejdere)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Indkøbsordre - overvågede kreditorer)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditorfaktura - overvågede kreditorer)</li>
</ul>
Når du vælger denne indstilling, skal du angive de overvågede enheder på siden Regel for overvågning.</td>
</tr>
<tr class="even">
<td>Nøgleordssøgning</td>
<td>Evaluer kildedokumenter for at afgøre, om de indeholder bestemte ord.</td>
<td>Når du vælger denne indstilling, skal du angive de ord, der skal ledes efter, på siden Regel for overvågning. Siden Regel for overvågning indeholder indstillinger, så du kan angive de tabeller og felter, der skal evalueres for de ord, du har angivet.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Fælles parametre
Alle politikreglerne for en bestemt overvågningspolitik deler samme batchparametre og samme datointerval for dokumentvalg. Disse parametre angives for politikken på siden Flere indstillinger.



<a name="additional-resources"></a>Yderligere ressourcer
--------

[Overtrædelser af overvågningspolitik og sager](audit-policy-violations-cases.md)
[Definere revisionspolitikker for kildedokumenter](tasks/define-audit-policies-source-documents.md)



