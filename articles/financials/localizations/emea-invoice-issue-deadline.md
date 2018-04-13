---
title: Deadline for fakturaudstedelse
description: "Denne artikel forklarer, hvordan du konfigurerer parametre for at beregne forfaldsdatoerne for udstedelse af debitorfakturaer og kreditorfakturaer i Den Europæiske Union (EU)."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 34dac634e09a8daa8a22b9f1efbc18ca44444e21
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="invoice-issue-deadline"></a>Deadline for fakturaudstedelse

[!INCLUDE [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du konfigurerer parametre for at beregne forfaldsdatoerne for udstedelse af debitorfakturaer og kreditorfakturaer i Den Europæiske Union (EU).

Den Europæiske Union (EU) direktiv 45/2010 og andre direktiver kræver, at forsendelser inden for EU (intra-EU-leverancer) skal faktureres på eller før den femtende dag i måneden, efter at leveringen har fundet sted. Hvert EU-land kan samtidig have forskellige faktureringsfrister for nationale leveringer. Funktionaliteten til forfaldsdato for fakturaudstedelse giver dig mulighed på at justere datointervallet efter type land/område. For alle forsendelse til og fra et land/område af en bestemt type til beregnes derefter forfaldsdato for fakturaudstedelse med brug af regler, der er angivet i det specificerede datointerval. Desuden kan du få alle følgesedler, der har en bestemt forfaldsdato for fakturaudstedelse, filtrere efter forfaldsdato for fakturaudstedelse under periodisk salgsfakturering og kontrollere udstedelsesdato for salgsfakturering under fakturabogføring. Du kan oprette en datointervalkode og derefter oprette en beregningsregel for fakturaudstedelsesdatoer ved at tildele datointervalkoden til en lande-/områdetype. Beregningsreglen bruges til at beregne forfaldsdatoen for udstedelse af fakturaer for følgende transaktioner:

-   Intra-EU-leverancer
-   Indenlandske forsendelser inden for en EU-medlemsstat

Du kan også konfigurere datokontroller for at sikre, at debitorfakturaer og kreditnotaer for debitorposteringer genereres inden for det angivne tidsrum, når leveringen har fundet sted.

## <a name="prerequisites"></a>Forudsætninger
Følgende tabel viser de forudsætninger, der skal være på plads, før du kan bruge funktionaliteten til forfaldsdato for fakturaudstedelse.

| Kategori            | Forudsætning                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/område      | Den primære adresse for den juridiske skal enhed være i et EU-medlemsland.                                                                                                                                                                                                                                                                                                                    |
| Relaterede opsætningsopgaver | På siden **Datointervaller** skal du definere et datointerval, der bruges til at beregne forfaldsdatoen for fakturaudstedelse. (Klik på **Finans** &gt; **Opsætning Finans** &gt; **Datointervaller**). På siden **Udenrigshandelsparametre** skal du konfigurere egenskaber for udenrigshandel for forskellige lande. (Klik på **Moms** &gt; **Opsætning** &gt; **Udenrigshandel** &gt; **Udenrigshandelsparametre**). |

## <a name="invoice-issue-due-date-calculation-rule"></a>Regel for beregning af forfaldsdato for fakturaudstedelse
Brug siden **Konfigurer beregning af forfaldsdato for fakturaudstedelse** til at konfigurere en beregningsregel for forfaldsdato for fakturaudstedelse ved at tildele en datointervalkode til en lande-/områdetype.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Datokontrolparametre for debitorfakturaer og kreditnotaer
Du kan også konfigurere datokontrolparametre for at sikre, at debitorfakturaer og kreditnotaer for debitorposteringer genereres inden for det angivne tidsrum, når leveringen har fundet sted. Du kan finde disse parametre i området **Datokontrol for faktura** på siden **Debitorparametre**.

## <a name="example"></a>Eksempel
Når du vil konfigurere Microsoft Dynamics 365 for Finance and Operations til at beregne forfaldsdatoer for fakturaudstedelse for Intrastat-EU-forsendelser den 15. i måneden efter leveringen, skal du oprette en datointervalkode og en beregningsregel, der har følgende indstillinger:

### <a name="date-interval-code"></a>Datointervalkode

| Felt                                                           | Værdi                           |
|-----------------------------------------------------------------|---------------------------------|
| Datointervalkode                                              | 15-NM                           |
| Beskrivelse                                                     | 15. dag i den næste måned |
| Før (i feltgruppen **Til dato**)                         | Måned                           |
| Start/slut (i feltgruppen **Til dato**)                      | Afslut                             |
| +/- (i feltgruppen **Til dato**)                            | 15                              |
| Dage, måneder, år eller perioder (i feltgruppen **Til dato**) | Dage                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Regel for beregning af forfaldsdato for fakturaudstedelse

| Felt               | Værdi                                                     |
|---------------------|-----------------------------------------------------------|
| Lande-/områdetype | **EU**                                                    |
| Startdato          | Angiv den dato, hvor den aktuelle linje for opsætning bliver gyldig. |
| Datointervalkode  | **15-NM**                                                 |

## <a name="next-steps"></a>Næste trin
Når du er færdig med at konfigurere parametrene for at beregne forfaldsdatoer for fakturaudstedelse, kan du oprette og bogføre følgende transaktioner for automatisk at beregne og opdatere forfaldsdatoerne for fakturaudstedelse:

-   **Salgsordrer** – Når du opretter en salgsordre og bogfører en følgeseddel, beregnes og opdateres forfaldsdatoen for udstedelse af fakturaen på følgesedlen. Forfaldsdatoen beregnes baseret på det datointerval, der er knyttet til det land/område, der er angivet i leveringsadressen på salgsordren. Når du bogfører følgesedlen, kan du kontrollere forfaldsdatoen for fakturaudstedelse i feltet **Forfaldsdato for fakturaudstedelse** på siden **Følgeseddelkladde**. (Klik på **Salg og marketing** &gt; **Salgsordre** &gt; **Ordreforsendelse** &gt; **Følgeseddel**). Du kan få vist alle de følgesedler, der ikke er faktureret, og forfaldsdatoer for fakturaudstedelsen på siden **Følgesedler, der ikke er faktureret**. (Klik på **Salg og marketing** &gt; **Salgsordre** &gt; **Ordreforsendelse** &gt; **Følgesedler, der ikke er faktureret**).
-   **Indkøbsordrer** – Når du opretter en indkøbsordre og bogfører en produktkvittering, beregnes og opdateres forfaldsdatoen for udstedelse af fakturaen på produktkvitteringen. Forfaldsdatoen beregnes baseret på det datointerval, der er knyttet til det land/område, der er angivet som kreditors primære adresse. Når du bogfører produktkvitteringen, kan du kontrollere forfaldsdatoen for fakturaudstedelse i feltet **Forfaldsdato for fakturaudstedelse** på siden **Produktkvitteringskladde**. (Klik på **Indkøb og forsyning** &gt; **Indkøbsordrer** &gt; **Modtage produkter** &gt; **Produktkvittering**). Du kan se alle de produktkvitteringer, der ikke er faktureret, og forfaldsdatoer for fakturaudstedelse, på siden **Produktkvitteringer, der ikke er faktureret**. (Klik på **Indkøb og forsyning** &gt; **Indkøbsordrer** &gt; **Modtage produkter** &gt; **Produktkvitteringer, der ikke er faktureret**).

## <a name="technical-information-for-system-administrators"></a>Tekniske oplysninger til systemadministratorer
Hvis du ikke har adgang til de sider, der bruges til at fuldføre opgaverne, som er nævnt i denne artikel, kan du kontakte din systemadministrator og angive de oplysninger, der vises i følgende tabel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategori</th>
<th>Forudsætning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurationsnøgler</td>
<td>Klik på <strong>Systemadministration</strong> &gt; <strong>Opsætning</strong> &gt; <strong>Licensering</strong> &gt; <strong>Licenskonfiguration</strong>. Klik på konfigurationsnøglen <strong>Finans</strong>.</td>
</tr>
<tr class="even">
<td>Sikkerhedsroller og programadgangsrettigheder</td>
<td>Hvis du vil udføre denne opgave, skal du være medlem af en sikkerhedsrolle, som omfatter følgende opgaver:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Aktivere faktura- og kontantbeholdningsproces)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Aktivere faktura- og betalingsproces)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sikkerhedsroller og rettigheder</td>
<td>Hvis du vil udføre denne opgave, skal du være medlem af en sikkerhedsrolle, som omfatter følgende rettigheder:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Vise liste over følgesedler)</li>
<li><strong>VendPackingSlipJournalView</strong> (Vise produktkvitteringskladde fra indkøbsordre)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (Beregne forfaldsdatoer for udstedelse af fakturaer)</li>
</ul></td>
</tr>
</tbody>
</table>






