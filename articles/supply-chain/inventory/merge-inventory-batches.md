---
title: Flet lagerbatches
description: Denne artikel indeholder oplysninger om, hvordan du konsoliderer to eller flere lagerbatchnumre i et flettet batch.
author: pjacobse
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d43733455765bc8b69ce8595c46b00942ddac6b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228581"
---
# <a name="merge-inventory-batches"></a>Flet lagerbatches

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan du konsoliderer to eller flere lagerbatchnumre i et flettet batch.

Når du fletter batches, kan beregninger hjælpe med at optimere karakteristika og batchattributter for det flettede batch. Når du har valgt kildebatchnumrene, kan du gennemgå og ændre det flettede batch, før du bogfører det. Du kan også overføre batchfletningen til en lagerkladde til godkendelse. Lager kan derefter reserveres eller bogføres direkte fra denne lagerkladde. Når du bogfører et flettet batch, reguleres lagerbeholdningen for kildebatches og det flettede batch.

## <a name="are-there-any-prerequisites"></a>Findes der nogen krav?
Ja, der er nogle ting, du skal konfigurere, før du kan bruge batchfletningsværktøjerne. Kravene er beskrevet i følgende tabel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Side</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kladdenavne, lager</td>
<td>Du skal oprette et kladdenavn af typen Stykliste , der bruges som standard, når du bogfører batchfletninger i lagerkladder. Valgfrit, men anbefalet: Du kan angive, at reservationer skal oprettes automatisk, når batchfletningen overføres til lagerkladden. Ellers er der risiko for, at den disponible lagerbeholdning ændres, når batchfletningsdetaljerne er angivet, og kladden er bogført. Vælg <strong>Automatisk</strong> i feltet <strong><strong>Reservation</strong></strong> for at aktivere automatiske reservationer til kladdenavnet.</td>
</tr>
<tr class="even">
<td>Parametre til lager- og lokationsstyring</td>
<td>Du skal angive standardkladdenavn for lagerkladden.</td>
</tr>
<tr class="odd">
<td>Frigivne produkter</td>
<td>Her er de anbefalede indstillinger for varen:
<ul>
<li>Du kan generere batchnumrene for flettede batches automatisk ved at tildele det frigivne produkt til en batchnummergruppe. Du kan også angive et batchnummer manuelt, når du opretter et flettet batch, eller vælge et eksisterende batchnummer. Hvis du vælger et eksisterende batchnummer, skal du sikre dig, at det markerede batch ikke er inkluderet i nogen lagertransaktioner.</li>
<li>Hvis du bruger hyldelevetid eller sidste holdbarhedsdato for det frigivne produkt, bliver datoerne for et flettet batch beregnet baseret på valget i feltet <strong>Beregning af datoen for batchfletning</strong>. Følgende valgmuligheder er tilgængelige:
<ul>
<li><strong>Tidligste</strong> – Beregningen er baseret på den tidligste dato, der er angivet for et kildebatch, der er valgt til batchfletning.</li>
<li><strong>Seneste</strong> – Beregningen er baseret på den seneste dato, der er angivet for et kildebatch, der er valgt til batchfletning.</li>
<li><strong>Manuel</strong> – Der foretages ikke nogen beregning. Hvis en dato er den samme på alle kildebatches, foreslås en dato. Du kan ændre denne dato. Hvis en dato ikke er den samme på kildebatchene, kan du manuelt angive datoen.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Batchnummergruppe</td>
<td>Valgfrit: Hvis du vil generere et batchnummer, når du opretter et flettet batch, skal du tildele en batchnummergruppe til den frigivne produkt. Ellers kan du angive et batchnummer manuelt.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Hvornår har jeg brug for at flette batches fra lageret?
Her er nogle eksempler på scenarier, hvor det kan være nyttigt at flette batches:

-   Da Sammy går igennem lageret, bemærker han, at flere batches af samme vare kun findes i små mængder. Han forventer at modtage flere nye forsendelser, og han kan se, at han kan frigøre gulvplads på ved at sammenlægge de forskellige mængder til et nyt batch.
-   Sammy modtager lagerbeholdning, og han ønsker at kombinere det nye batch med et, som han allerede har modtaget, for at øge batchattributværdien for det eksisterende batch. Når du gør dette, opretter du et nyt batch.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Er det muligt at flette batches på tværs af steder og juridiske enheder?
Nej, du kan kun flette batches, der har det samme sted og de samme lagringsdimensioner i én juridisk enhed. Du kan dog angive en anden lokalitet og et andet palle-id for det flettede batch.

## <a name="can-i-merge-partial-quantities"></a>Kan jeg flette delmængder?
Nej, du kan kun flette det fulde antal partier. Batchfletfunktionen er beregnet som en lagerfunktion, og ikke en produktionsfunktion.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Hvad hvis batchene har forskellige batchattributværdier?
Når du vælger kildebatches, der skal kombineres i den flettede batch, vil Supply Chain Management kontrollere, om alle batches har karakteristika eller attributværdier. Når en attributværdi er den samme, foreslås der en værdi for det flettede batch. Du kan ændre denne værdi. Attributværdier, der ikke er de samme, udfyldes ikke for det flettede batch, og du kan angive disse værdier manuelt. Hvis batchattributtypen for attributværdien er et heltal eller en brøk, og værdierne er ikke de samme for alle kildebatches, beregnes værdien ved hjælp af en beregning af vægtet gennemsnit. De beregnede værdier rundes op eller ned til det nærmeste interval. Hvis værdien er tom for et kildebatch, medtages batchet og dets mængde ikke i beregningen. **Eksempel** Følgende eksempel viser en vægtet gennemsnitsberegning for et flettet batch. To af kildebatchene har en tom værdi for en batchattributtype, der er et heltal. Følgende attribut tildeles kildebatchene.

| Egenskab | Minimum | Multiplum | Maksimum |
|-----------|---------|-----------|---------|
| Klasse     | 3       | 3         | 30      |

Kildebatchene har følgende attributværdier for attributten **Klassebatch**.

| Batch | Antal | Egenskab | Attributværdi |
|-------|----------|-----------|-----------------|
| B1    | 10       | Klasse     | Tom           |
| B2    | 15       | Klasse     | 15              |
| B3    | 20       | Klasse     | 20              |
| B4    | 25       | Klasse     | Tom           |
| B5    | 30       | Klasse     | 25              |

Når du tilføjer disse batches som kildebatches, tildeles følgende værdier til det flettede batch.

| Batch | Antal | Egenskab | Attributværdi |
|-------|----------|-----------|-----------------|
| B6    | 100      | Klasse     | 21              |

Værdier og mængder for batchnumre B1 og B4 medtages ikke i beregningen af vægtede gennemsnit. Derfor får du vist, hvordan værdien beregnes for det flettede batch her.

| Værdi | Mængde (vægt)                              | Relativ vægt | Relativ vægt × værdi                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **I alt:** 65, som er summen for vægtningen |                 | **I alt:** 21,5384615, som afrundes til 21 (det nærmeste interval). |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Hvad, hvis batchene har forskellige batchdatoer?
Hvis disse batches har forskellige datoer, beregnes nogle af datoerne på grundlag af værdierne i gruppen **Batchdatoer** i oversigtspanelet **Flettet batch** på siden **Batchfletning**. Feltværdierne beregnes på basis af felterne i gruppen **Batchdatoer**. Disse værdier omfatter fremstillingsdato, udløbsdato, hyldeadviseringsdato og sidste holdbarhedsdato. Datoerne beregnes ud fra indstillingerne for varen i feltgruppen **Varedata** på siden **Frigivne produktdetaljer**. Du kan evt. ændre værdierne eller indtaste dem manuelt. For alle andre datoer foretages der ingen beregning. Det samme princip anvendes for batchattributværdier. Hvis en dato er den samme for alle kildebatches, foreslås denne dato for det flettede batch. Hvis datoen ikke er den samme for alle kildebatches, vil datoen være tom for det flettede batch, og du kan indtaste den manuelt.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Hvad nu, hvis dimensionerne er forskellige på de batches, som jeg vil flette?
Sådan håndteres produktdimensioner, sporingsdimensioner og lagringsdimensioner:

-   **Produktdimensioner** – Alle produktdimensioner for den valgte vare skal være de samme. Du kan ikke flette batches på tværs af produktdimensioner.
-   **Sporingsdimensioner** – Et nyt batchnummer genereres automatisk, hvis der er angivet en batchnummergruppe for varen. Hvis en batchnummergruppe ikke er knyttet til en vare, kan du vælge et eksisterende batch eller indtaste nummeret manuelt. Serienumre overføres fra kildebatchet til lagerkladdelinjer for det flettede batch.
-   **Lagringsdimensioner** – Lagringsdimensioner for sted og lagersted skal være de samme for alle kildebatches og det flettede batch. Du kan dog angive en ny lokalitet og et nyt palle-id for det flettede batch.

## <a name="how-does-posting-work"></a>Hvordan fungerer bogføring?
Bogføring fungerer på to måder, afhængigt af om du bruger en godkendelsesproces for kladder. Du kan bruge handlingerne **Overfør til kladde** og **Bogfør batchfletningen** til at overføre batchfletningen til en kladde, hvor den kan kontrolleres og bogføres, eller du kan bogføre batchfletningen direkte. Den væsentligste forskel mellem de to handlinger er, at en overførsel til en kladde ikke bogfører batchfletningen. Begge handlinger opretter et nyt batch, hvis et eksisterende batch ikke er valgt, opdatere alle batchoplysninger og attributværdier og oprette en lagerkladde.

-   **Overfør til kladde** – Overfør batchfletningsoplysninger til en ny lagerkladde. Hvis du har konfigureret automatisk reservation, reserveres mængderne i kildebatchene. Detaljer om batchfletningen kan ikke ændres. Hvis du vil ændre batchfletningen, skal du slette kladden. Kladden kan bruges som en opgave, som en anden medarbejder skal udføre senere. Reservation af batchantallet på kladdelinjen er sikret. Med denne fordeling kan en kvalitetsplanlæggeren eller en lagerchef oprette opgaver for sine medarbejdere.
-   **Bogfør batchfletningen** – Bogfør batchfletningen direkte. Denne handling kan kun udføres, når den fysiske fletning er foretaget.

Du kan godkende lagerkladden for batchfletningen fra listesiden **Alle batchfletninger**. Klik på **Kladde** &gt; **Bogfør**. Når en kladde er bogført, kan du ikke ændre oplysningerne i det flettede batch. Når du overfører en batchfletning til en lagerkladde, kan du kun ændre oplysningerne, hvis kladden slettes.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Hvorfor kan jeg ikke se oplysningerne om fastvægtvarer i lagerkladden, når jeg har flettet en fastvægtvare?
Du kan flette batches af fastvægtvarer ligesom alle andre varer. Fastvægtoplysningerne vises dog ikke i lagerkladden. Vi anbefaler, at du kontrollerer fastvægtoplysningerne, før du overfører batchfletningen til lagerkladden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]