---
title: Modtagermomsmekanisme for momsskema (VAT/GST)
description: I dette emne beskrives, hvordan du konfigurerer modtagermoms for europæiske lande, Saudi-Arabien og Singapore.
author: epodkolz
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 46b26fc1c0c45be894e226080a5aa9d5ae48b595
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005989"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>Modtagermomsmekanisme for momsskema (VAT/GST)

[!include [banner](../includes/banner.md)]

I dette emne beskrives en generisk tilgang til opsætning af modtagermoms for lande/områder, der bruger momsskemaer (VAT eller GST).
                                                                                 
Funktionalitetens tilgængelige lande/områder administreres af følgende funktioner i arbejdsområdet **Funktionsstyring**.

| Funktion                                              | Land/område                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ingen specifik funktion                                | Østrig </br>Belgien </br>Bulgarien </br>Kroatien </br>Cypern </br>Tjekkiet </br>Danmark  </br>Estland  </br>Finland  </br>Frankrig  </br>Tyskland  </br>Ungarn  </br>Island  </br>Irland  </br>Italien  </br>Letland  </br>Liechtenstein  </br>Litauen  </br>Luxembourg  </br>Nederlandene  </br>Norge Polen </br>Portugal </br>Rumænien  </br>Saudi-Arabien </br>Singapore  </br>Slovakiet  </br>Slovenien  </br>Spanien  </br>Sverige  </br>Schweiz  </br>Storbritannien  </br>De Forenede Arabiske Emirater |
| Modtagermoms for flere lande/områder            | Bahrain  </br>Kuwait  </br>Oman  </br>Qatar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Aktivér modtagermomsmekanisme for momsskema (VAT/GST) | Alle andre lande/områder undtagen:  </br>Brasilien  </br>Indien  </br>Rusland                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Du kan finde flere oplysninger i afsnittet [Aktivere modtagermomsmekanisme for momsskema (VAT/GST)](#enable-reverse-charge) senere i dette emne.

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

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Konfigurere momsgrupper og varemomsgrupper
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

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Konfigurere varegrupper med modtagermoms
På siden **Varegrupper med modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Varegrupper med modtagermoms**) kan du definere grupper af produkter eller tjenester eller individuelle produkter eller tjenester, som modtagermomsen kan pålægges. For hver varegruppe med modtagermoms skal du definere listen over varer, varegrupper og kategorier for salg og/eller køb.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Konfigurere regler for modtagermoms
På siden **Regler for modtagermoms** (**Moms** &gt; **Opsætning** &gt; **Moms** &gt; **Regler for modtagermoms**) kan du definere anvendelighedsregler til købs- og salgsformål. Du kan konfigurere et sæt regler for anvendelse af modtagermoms. For hvert regelsæt skal du angive følgende felter:

- **Dokumenttype** – Vælg **Indkøbsordre**, **Kreditorfakturajournal**, **Salgsordre**, **Fritekstfaktura**, **Debitorfakturajournal** og/eller **Kreditorfaktura**.
- **Lande-/områdetype for partneren** – Vælg **Indenlandsk**, **EU** **GCC** eller **Udenlandsk**. Alternativt, hvis reglen kan anvendes på alle samarbejdspartnere, uanset landet eller området i deres adresse, skal du vælge **Alle**.
- **Indenlandsk leveringsadresse** – Marker dette afkrydsningsfelt for at anvende reglen på leveringer i det samme land eller område. Dette afkrydsningsfelt kan ikke markeres for dokumenttyperne **Kreditorfakturajournal** og **Debitorfakturajournal**.
- **Varegruppe med modtagermoms** – Vælg den gruppe, som reglen kan anvendes på.
- **Tærskelbeløb** – Skemaet for modtagermoms anvendes kun på en faktura, hvis værdien af varer og/eller tjenesteydelser, der er medtaget i varegruppen med modtagermoms, overskrider den grænse, du angiver her.

Du kan også bruge felterne **Ikrafttrædelsesdato** og **Udløbsdato** til at definere den periode, hvor reglen er i kraft.

Derudover kan du angive, om der skal vises en besked, og om dokumentlinjen skal opdateres med standardmomsgruppen for modtagermoms, hvis betingelsen for den pågældende dokumentlinje er opfyldt. Følgende valgmuligheder er tilgængelige:

- **Ingen** – Bilagslinjen opdateres ikke.
- **Spørg** – Der vises en besked for at bekræfte, at der kan anvendes modtagermoms.
- **Indstil** – Dokumentlinjen opdateres uden yderligere besked.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Konfigurere egenskaber for land/område
På siden **Udenrigshandelsparametre** (**Moms** &gt; **Konfiguration** &gt; **Moms** &gt; **Udenrigshandel** &gt; **Udenrigshandelsparametre**), fanen **Egenskaber for land/område** skal du angive landet/området for den aktuelle juridiske enhed til *Indland*. Angiv **Lande-/områdetype** i EU-lande/områder, der deltager i EU-handel med den aktuelle juridiske enhed, til *EU*. Angiv **Lande-/områdetype** i GCC-lande/områder, der deltager i GCC-handel med den aktuelle juridiske enhed, til *GCC*.

## <a name="set-up-default-parameters"></a>Konfigurere standardparametre
Du aktiverer funktionen for modtagermoms på siden **Finansparametre** under fanen **Modtagermoms** at vælge **Ja** for indstillingen **Aktiver tilbageført gebyr**. I felterne **Indkøbsordremomsgruppe** og **Salgsordremomsgruppe** skal du vælge standardmomsgrupperne. Når en betingelse for anvendelse af modtagermoms er opfyldt, opdateres salgs- eller købsordrelinjen med disse momsgrupper.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Modtagermoms på en salgsfaktura
Sælgeren opkræver ikke moms for salg, der er angivet i modtagermomsskemaet. I stedet angives både de varer, som er genstand for modtagermomsen, og det samlede beløb for modtagermomsen på fakturaen.

Når en salgsfaktura med modtagermoms bogføres, har momstransaktionerne momsretningen **Udgående moms** og ingen moms, og afkrydsningsfelter **Modtagermoms** og **Momsfri** er markeret.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Modtagermoms på en købsfaktura
For køb under modtagermomsskemaet skal den køber, der modtager fakturaen med modtagermoms, fungere som køber og sælger i momsregnskabsmæssig sammenhæng.

Når en købsfaktura med modtagermoms bogføres, oprettes der to momsposteringer. Den ene postering har momsretningen **Indgående moms**. Den anden postering har momsretningen **Udgående moms**, og afkrydsningsfeltet **Modtagermoms** er markeret.

På følgende skærmbillede har den ene transaktion retningen **Indgående moms** og den anden transaktion har retningen **Udgående moms**. 

![Bogført moms](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>Aktivér modtagermomsmekanisme for momsskema (VAT/GST)
Find funktionen i arbejdsområdet **Funktionsstyring**, og vælg **Aktivér**.

Når du har aktiveret funktionen, er fanen **Modtagermoms** tilgængelig i alle juridiske enheder. Aktiver funktionen til modtagermoms for en juridisk enhed ved at indstille **Aktivér modtagermoms** til **Ja**.

Følgende sider og menupunkter, der vedrører opsætningen af funktionen, er tilgængelige:
 - **Varegrupper med modtagermoms** (**Moms** > **Opsætning** > **Moms** > **Varegrupper med modtagermoms**). Yderligere oplysninger finder du i afsnittet [Konfigurere varegrupper med modtagermoms](#reverse-charge-item-group).
 - **Regler for modtagermoms** (**Moms** > **Opsætning** > **Moms** > **Regler for modtagermoms**). Se [Konfigurere regler for modtagermoms](#reverse-charge-rules).
 - **Udenrigshandelsparametre** (**Moms** > **Opsætning** > **Moms** > **Udenrigshandel** > **Parametre for udenrigshandel**). Se [Konfigurere egenskaber for land/område](#Set-up-Country/region-properties).

Afkrydsningsfeltet **Modtagermoms** er tilgængeligt på siderne **Momsgruppe** og **Bogført moms**. Du kan finde flere oplysninger i afsnittene, [Konfigurere momsgrupper og varemomsgrupper](#sales-tax-item-sales-tax-groups), [Modtagermoms på en salgsfaktura](#reverse-charge-sale) og [Modtagermoms på en købsfaktura](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]