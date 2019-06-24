---
title: Modtagermoms
description: I dette emne beskrives, hvordan du konfigurerer modtagermoms for europæiske lande og Saudi-Arabien.
author: epodkolz
manager: AnnBe
ms.date: 04/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 26f7f3f11408cac387c58a5345b566ac50ed426f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571165"
---
# <a name="reverse-charge-vat"></a>Modtagermoms


[!include [banner](../includes/banner.md)]


I dette emne beskrives den generelle tilgang til konfiguration af modtagermoms moms for Saudi-Arabien og europæiske lande.

Modtagermoms er et momsskema, der flytter ansvaret for momsregnskab og rapportering af moms fra sælgeren til køberen af varer og/eller tjenesteydelser. Derfor registrerer modtagere af varer og/eller ydelser både udgående moms (i rollen som sælger) og indgående moms (i rollen som køber) i deres momsangivelse.

I nogle lande eller områder implementeres modtagermomsskemaet kun for nogle varer og/eller ydelser, og der er yderligere betingelser eller grænser for salgsbeløb. I andre lande eller områder afhænger ansvaret for momsbetalingen af leverandørens og køberens status. Hvis køberen skal betale moms, skal denne oplysning tydeligt fremgå af fakturaen, som leverandøren udsteder. Fakturaen skal f.eks. indeholde ordet "modtagermoms" ("Reverse charge") og skal angive, hvilke stillinger der er underlagt modtagermomsskemaet. 

Når du vil anvende modtagermoms, skal du udføre følgende konfiguration.

## <a name="set-up-sales-tax-codes"></a>Konfigurer momskoder
Det anbefales at bruge separate momskoder til henholdsvis salgs- og indkøbsoperationer.

<table>
<body>
<tr>
<td><strong>Momskode for salg</strong></td>
<td>Opret en momskode for salgsoperationer med modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momskoder</strong>).
</td>
</tr>
<tr>
<td><strong>Momskode for køb</strong></td>
<td><p>Opret positive og negative momskoder for modtagermoms for køb (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momskoder</strong>).</p>
<ol>
<li>Opret en momskode, der har en positiv værdi.</li>
<li>Opret en momskode, der har en negativ værdi. Angiv <strong>Ja</strong> for indstillingen <strong>Tillad en negativ momsprocent</strong>.
Du skal tildele denne negative momskode til en varemomsgruppe og derefter knytte varemomsgruppen til varer, der er omfattet af modtagermomsen.</li>
</ol>
<p>Du kan finde flere oplysninger i det næste afsnit &quot;Konfigurer momsgrupper og varemomsgrupper&quot;.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Konfigurere momsgrupper og varemomsgrupper
Det anbefales at bruge separate momsgrupper til henholdsvis salgs- og indkøbsoperationer.

<table>
<tr>
<td><strong>Momsgrupper for salg</strong></td>
<td>Opret en momsgruppe for salgsoperationer, der har modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momsgrupper</strong>). Under fanen <strong>Opsætning</strong> kan du medtage momskoden for modtagermoms i denne gruppe. Markér afkrydsningsfelterne <strong>Frit</strong> og <strong>Modtagermoms</strong> for momskoden.</td>
</tr>
<tr>
<td><strong>Varemomsgrupper for køb</strong></td>
<td>Opret en momsgruppe for købsoperationer, der har modtagermoms (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Momsgrupper</strong>). Under fanen <strong>Opsætning</strong> kan du medtage både positive og negative momskoder i denne gruppe. Markér afkrydsningsfelt <strong>Modtagermoms</strong> for den momskode, der har en negativ værdi.</td>
</tr>
<tr>
<td><strong>Varemomsgrupper</strong></td>
<td>Opret eller opdater varemomsgruppen med den momskode, der har en negativ værdi (<strong>Moms</strong> &gt; <strong>Indirekte skatter</strong> &gt; <strong>Moms</strong> &gt; <strong>Varemomsgrupper</strong>). Du skal tildele standardvaremomsgruppen til de produkter og kategorier, der er omfattet af modtagermomsen.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Konfigurere modtagermomsgrupper
På siden **Varegrupper med modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Varegrupper med modtagermoms**) kan du definere grupper af produkter eller tjenester eller individuelle produkter eller tjenester, som modtagermomsen kan pålægges. For hver varegruppe med modtagermoms skal du definere listen over varer, varegrupper og kategorier for salg og/eller køb.

## <a name="set-up-reverse-charge-rules"></a>Konfigurere regler for modtagermoms
På siden **Regler for modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Regler for modtagermoms**) kan du definere anvendelighedsregler til købs- og salgsformål. Du kan konfigurere et sæt regler for anvendelse af modtagermoms. For hvert regelsæt skal du angive følgende felter:

- **Dokumenttype** – Vælg **Indkøbsordre**, **Kreditorfakturajournal**, **Salgsordre**, **Fritekstfaktura**, **Debitorfakturajournal** og/eller **Kreditorfaktura**.
- **Lande-/områdetype for partneren** – Vælg **Indenlandsk**, **EU** eller **Udenlandsk**. Alternativt, hvis reglen kan anvendes på alle samarbejdspartnere, uanset landet eller området i deres adresse, skal du vælge **Alle**.
- **Indenlandsk leveringsadresse** – Marker dette afkrydsningsfelt for at anvende reglen på leveringer i det samme land eller område. Dette afkrydsningsfelt kan ikke markeres for dokumenttyperne **Kreditorfakturajournal** og **Debitorfakturajournal**.
- **Varegruppe med modtagermoms** – Vælg den gruppe, som reglen kan anvendes på.
- **Tærskelbeløb** – Skemaet for modtagermoms anvendes kun på en faktura, hvis værdien af varer og/eller tjenesteydelser, der er medtaget i varegruppen med modtagermoms, overskrider den grænse, du angiver her.

Du kan også bruge felterne **Ikrafttrædelsesdato** og **Udløbsdato** til at definere den periode, hvor reglen er i kraft.

Derudover kan du angive, om der skal vises en besked, og om dokumentlinjen skal opdateres med standardmomsgruppen for modtagermoms, hvis betingelsen for den pågældende dokumentlinje er opfyldt. Følgende valgmuligheder er tilgængelige:

- **Ingen** – Bilagslinjen opdateres ikke.
- **Spørg** – Der vises en besked for at bekræfte, at der kan anvendes modtagermoms.
- **Indstil** – Dokumentlinjen opdateres uden yderligere besked.

## <a name="set-up-default-parameters"></a>Konfigurere standardparametre
Du aktiverer funktionen for modtagermoms på siden **Finansparametre** under fanen **Modtagermoms** at vælge **Ja** for indstillingen **Aktiver tilbageført gebyr**. I felterne **Indkøbsordremomsgruppe** og **Salgsordremomsgruppe** skal du vælge standardmomsgrupperne. Når en betingelse for anvendelse af modtagermoms er opfyldt, opdateres salgs- eller købsordrelinjen med disse momsgrupper.

## <a name="reverse-charge-on-a-sales-invoice"></a>Modtagermoms på en salgsfaktura
Sælgeren opkræver ikke moms for salg, der er angivet i modtagermomsskemaet. I stedet angives både de varer, som er genstand for modtagermomsen, og det samlede beløb for modtagermomsen på fakturaen.

Når en salgsfaktura med modtagermoms bogføres, har momstransaktionerne momsretningen **Udgående moms** og ingen moms, og afkrydsningsfeltet **Modtagermoms** er markeret.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Modtagermoms på en købsfaktura
For køb under modtagermomsskemaet skal den køber, der modtager fakturaen med modtagermoms, fungere som køber og sælger i momsregnskabsmæssig sammenhæng.

Når en købsfaktura med modtagermoms bogføres, oprettes der to momsposteringer. Den ene postering har momsretningen **Indgående moms**. Den anden postering har momsretningen **Udgående moms**, og afkrydsningsfeltet **Modtagermoms** er markeret.

På følgende skærmbillede har den ene transaktion retningen **Indgående moms** og den anden transaktion har retningen **Udgående moms**. 

![Bogført moms](media/apac-sau-posted-sales-tax.png)
