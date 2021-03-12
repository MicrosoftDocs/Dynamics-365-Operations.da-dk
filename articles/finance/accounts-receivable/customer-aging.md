---
title: Aldersfordelt saldoliste for kunder
description: I rapporten Aldersfordelt saldoliste for kunder vises de saldi, som forfalder fra kunder, der er sorteret efter datointerval eller forældelsesperiode.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9291299e0b2ee040bc25ef21237a73c3bc0ea412
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995657"
---
# <a name="customer-aging-report"></a>Aldersfordelt saldoliste for kunder 

I rapporten **Aldersfordelt saldoliste for kunder** vises de saldi, som forfalder fra kunder, der er sorteret efter datointerval eller forældelsesperiode.

Når du opretter denne rapport, vises følgende standardparametre. Du kan bruge disse parametre til at filtrere de data, der vises i rapporten. Du kan finde flere oplysninger under [Konfigurere rykkere](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Felt</p></th>
<th><p>Betegnelse</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Faktureringsklassifikation</strong></p></td>
<td><p>Vælg en eller flere faktureringsklassifikationer, der skal medtages i rapporten.</p>
<div class="alert">

**Bemærk:** Dette kontrolelement er kun tilgængeligt, hvis konfigurationsnøglen <STRONG>Offentlig sektor</STRONG> er valgt.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Medtag transaktioner uden en faktureringsklassifikation</strong></p></td>
<td><p>Hvis dette afkrydsningsfelt er markeret, bliver alle de posteringer, der ikke har nogen tilknyttet faktureringsklassifikation, vist i rapporten.</p>
<div class="alert">

**Bemærk:** Dette kontrolelement er kun tilgængeligt, hvis konfigurationsnøglen <STRONG>Offentlig sektor</STRONG> er valgt.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Aldersfordeling pr.</strong></p></td>
<td><p>Angiv den dato, der skal bruges på det aktuelle aldersfordelte filsæt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Saldo pr.</strong></p></td>
<td><p>Angiv den dato, der skal vises debitorsaldi for. Dette kaldes skæringsdatoen for transaktioner.</p></td>
</tr>
<tr class="even">
<td><p><strong>Igangsæt dato</strong></p></td>
<td><p>Angiv en dato, der ligger i det første periodeinterval eller den første forældelsesperiode, der skal medtages i rapporten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Afgrænsning</strong></p></td>
<td><p>Vælg den type dato, rapporten skal baseres på.</p>
<ul>
<li><p><strong>Posteringsdato</strong> – Posteringsdatoen for transaktionerne. Det kan f.eks. være en fakturadato, der danner basis for beregningen af forfaldsdatoen.</p></li>
<li><p><strong>Forfaldsdato</strong> – Forfaldsdatoen for transaktionerne baseret på betalingsbetingelserne.</p></li>
<li><p><strong>Dokumentdato</strong> – En brugerdefineret dokumentdato, der ligger til grund for beregningen af forfaldsdatoen.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Definition på forældelsesperiode</strong></p></td>
<td><p>Vælg en definition af forældelsesperiode. Feltet <strong>Interval</strong> bruges ikke, hvis du vælger en definition af forældelsesperiode.</p>
<p>Der kan ikke bruges definitioner af forældelsesperioder, der har mere end seks forældelsesperioder, i den udskrevne rapport.</p>
<div class="alert">

**Bemærk:** Du kan konfigurere forældelsesperioder på siden <STRONG>Definitioner af forældelsesperioder</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Udskriv beskrivelse af forældelsesperiode</strong></p></td>
<td><p>Vælg <strong>Ja</strong> for at medtage beskrivelser af forældelsesperioder øverst i hver enkelt kolonne for en forældelsesperiode i rapporten. Vælg <strong>Nej</strong> for at udskrive rapporten uden kolonneoverskrifter.</p></td>
</tr>
<tr class="even">
<td><p><strong>Interval</strong></p></td>
<td><p>Definer den periode, der skal bruges, ved at angive antallet af dagsenheder eller månedsenheder i hver periode. Hvis du f.eks. vil have vist oplysninger om forældelse efter uge, skal du angive 7 i dette felt og vælge <strong>Dag</strong> i feltet <strong>Dag/måned</strong>.</p>
<div class="alert">

**Bemærk:** De oplysninger, du angiver i dette felt, bruges kun, hvis du ikke har valgt en definition for forældelsesperiode. Ellers defineres udskriftsretningen i definitionen af forældelsesperioden.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Dag/md</strong></p></td>
<td><p>Vælg enhed, enten <strong>Dag</strong> eller <strong>Måned</strong>, som skal bruges til at definere perioden, i feltet <strong>Interval</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Udskriftsretning</strong></p></td>
<td><p>Vælg, om saldi skal beregnes, og forældelsesrapporten skal udskrives for tidligere eller fremtidige perioder. Datoerne evalueres i forhold til den dato, der er valgt i feltet <strong>Saldo som på</strong>. Vælg <strong>Bagud</strong> for at få vist oplysninger om tidligere perioder. Vælg <strong>Fremad</strong> for at få vist oplysninger om fremtidige perioder.</p>
<div class="alert">
  
<STRONG>Bemærk:</STRONG> De oplysninger, du angiver i dette felt, bruges kun, hvis du ikke har valgt en definition for forældelsesperiode.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Detaljer</strong></p></td>
<td><p>Vælg dette for at få vist posteringer, der er medregnet i de saldi, som vises i rapporten.</p></td>
</tr>
<tr class="even">
<td><p><strong>Medtag beløb i transaktionsvaluta</strong></p></td>
<td><p>Vælg dette for at inkludere beløb i transaktionsvalutaen ud over beløb i regnskabsvalutaen. Hvis dette afkrydsningsfelt ikke er markeret, vises beløbene i rapporten kun i regnskabsvalutaen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negativ saldo</strong></p></td>
<td><p>Vælg dette for at medtage debitorkonti, der har negative saldi.</p></td>
</tr>
<tr class="even">
<td><p><strong>Udeluk nul-saldo-konti</strong></p></td>
<td><p>Vælg dette for at udelukke debitorkonti, der har en nul-saldo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Betalingspositionering</strong></p></td>
<td><p>Vælg dette for at få vist betalinger, der ikke er udlignet. Disse vises i den første kolonne i rapporten.</p></td>
</tr>
</tbody>
</table>

