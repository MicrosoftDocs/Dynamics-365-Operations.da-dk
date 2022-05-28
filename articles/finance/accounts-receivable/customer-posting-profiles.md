---
title: Debitor, posteringsprofiler
description: I dette emne beskrives debitorposteringsprofiler, der styrer, hvordan kundetransaktioner bogføres i finansmodulet.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5ab24e37c75222080bd242aa72a39ecb476bf
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734626"
---
# <a name="customer-posting-profiles"></a>Debitor, posteringsprofiler

[!include [banner](../includes/banner.md)]

I dette emne beskrives debitorposteringsprofiler, der styrer, hvordan kundetransaktioner bogføres i finansmodulet.

## <a name="customer-posting-profiles"></a>Debitor, posteringsprofiler

Debitorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle debitorer, en gruppe debitorer eller en enkelt debitor. Disse indstillinger bruges, når du opretter salgsordrefakturaer, fritekstfakturaer, projektfakturaer, betalingskladder, rykkere og rentenotaer. 

Standardposteringsprofilen defineres under fanen **Finans og Moms** på siden **Debitorparametre**. Den medtages derefter automatisk i overskriften på nye dokumenter. Du kan ændre den der, hvis der kræves en anden posteringsprofil. 

Organisationer, der accepterer forudbetalinger fra kunder, konfigurerer ofte en anden posteringsprofil til forudbetalinger og tilknytter den i parametrene som standardposteringsprofilen for forudbetalinger. Du kan finde flere oplysninger i [Forudbetalinger fra debitorer](customer-prepayments.md).

Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden **Definitioner af posteringsbogføring**. Bogføringsdefinitioner bruges i stedet for posteringsprofiler til at styre bogføring af kundetransaktioner i finansmodulet. Yderligere oplysninger finder du i afsnittet [Posteringsdefinitioner](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Oprette en posteringsprofil
Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil. Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil. Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge:

| Feltværdien Kontokode | Feltværdien Konto/gruppenummer                | Søgeprioritet |
|--------------------------|-------------------------------------------------|-----------------|
| Tabellen                    | Bestemt debitorkonto                       | 1               |
| Gruppe                    | Debitorgruppe, som debitor er tilknyttet | 2               |
| Alt                      | Tom                                           | 3               |

Hvis alle kundetransaktioner skal have samme posteringsprofil, skal du kun definere én posteringsprofil med **Alle** angivet i feltet **Kontokode**. Angiv følgende værdier for at definere en posteringsprofil.

<table>
<thead>
<tr>
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bogføringsprofil</td>
<td>Angiv en kode for posteringsprofilen. Eksempel: Hvis du vil have én konto for debitorsaldi i indenlandsk valuta og én konto for debitorsaldi i udenlandsk valuta, skal du oprette to posteringsprofiler. Du kan kalde den ene konto Indland og den anden Udland.</td>
</tr>
<tr>
<td>Beskrivelse</td>
<td>Angiv en beskrivelse af posteringsprofilen. Dette bruges kun til at identificere posteringsprofilen bedre, når du ser den på denne side.</td>
</tr>
<tr>
<td>Kontokode</td>
<td>Angiv, om posteringsprofilen skal gælde for en bestemt debitor, en gruppe af debitorer eller alle debitorer:
<ul>
<li><b>Tabel</b> – Posteringsprofilen anvendes på en enkelt debitor. Vælg debitorkontoen i feltet <b>Konto/gruppenummer</b>.</li>
<li><b>Gruppe</b> – Posteringsprofilen anvendes på en debitorgruppe. Vælg debitorgruppen i feltet <b>Konto/gruppenummer</b>.</li>
<li><b>Alle</b> – Posteringsprofilen anvendes på alle debitorer. Lad feltet <b>Konto/gruppenummer</b> være tomt.</li>
</ul>
</td>
</tr>
<tr>
<td>Konto/gruppenummer</td>
<td>Hvis du vælger <b>Tabel</b> i feltet <b>Kontokode</b>, skal du vælge kontonummeret på den debitor, der er knyttet til posteringsprofilen. Hvis du vælger <b>Gruppe</b>, skal du vælge debitorgruppen. Hvis du vælger <b>Alle</b>, skal feltet stå tomt.</td>
</tr>
<tr>
<td>Samlekonto</td>
<td>Vælg den hovedkonto, der skal bruges som debitorhandelskonto for de debitorer, som er tilknyttet posteringsprofilen. Denne konto er kontoen til bogføringstypen <b>Debitorsaldo</b>.</td>
</tr>
<tr>
<td>Likviditetskonto for betalinger</td>
<td>Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter. Dette felt vises kun, hvis likviditetsbudgetter er aktiveret.</td>
</tr>
<tr>
<td>Momsforudbetalinger</td>
<td><p>Angiv kontonummeret for momsbetaling, der er modtaget forud.</p>
<p><strong>Bemærk:</strong> Brug siden <b>Debitorparametre</b> til at angive den posteringsprofil, der bruges, når en betaling er markeret som forudbetaling.</p>
</td>
</tr>
<tr>
<td>Passiver for rabatkonto</td>
<td>Vælg finanskontoen til rabatpassiver.</td>
</tr>
<tr>
<td>Rykkerforløb</td>
<td>Vælg identifikationen for den rykkerserie, der skal bruges i forbindelse med debitorer, som har den aktuelle posteringsprofil tilknyttet.</td>
</tr>
<tr>
<td>Rentekode</td>
<td>Vælg den rentekode, der skal bruges ved renteberegning for debitorer, som har den aktuelle posteringsprofil tilknyttet.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Eksempler på bogføring

I følgende tabel vises eksempler på standardbogføringstyper med eksempler på hovedkonti og beskrivelser. I kolonnen **Debet/Kredit** angives, om transaktionen typisk er debet eller kredit eller i visse tilfælde kan bogføres som det ene eller det andet. I kolonnen **Clearingkonto** angives, om bogføringstypen er en clearingkonto. Det betyder, at det beløb, der bogføres på denne konto, automatisk tilbageføres, når en senere transaktion bogføres. 

| Bogføringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/Kredit | Clearingkonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Debitorsaldo | 130100 | Debitorhandel | Aktiv | Begge | Nej | Angiv kontoen i feltet **Samlekonto**.|
| Ingen | 110110 | Pengeinstitutkonto | Aktiv | Begge | Nej | Angiv hovedkontoen i feltet **Likviditetskonto til betalinger**. Denne konto bruges ikke til bogføring. Den bruges kun til likviditetsbudgettering. |
| Momsforudbetalinger | 202900 | Momsclearing | Passiv | Begge | Ja | Angiv kontonummeret for momsbetaling, der er modtaget forud. |
| Passiver for rabatkonto | 250600 | Udskudt indtægt og rabatter | Passiv | Begge | Ja | Vælg finanskontoen til rabatpassiver.|     

### <a name="table-restrictions"></a>Tabelbegrænsninger

For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere. Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.

Angiv følgende værdier for at definere en posteringsprofil:

| Felt                 | Beskrivelse                                           |
|-----------------------|-------------------------------------------------------|
| Bosted        | Vælg denne, hvis der skal kunne foretages automatisk udligning af poster med denne posteringsprofil. Hvis denne indstilling ikke er markeret, skal du manuelt udligne transaktioner ved hjælp af siden **Udlign åbne posteringer** eller siden **Angiv debitorbetalinger**. |
| Renter          | Vælg denne, hvis der skal beregnes rente på udestående saldi for debitorkonti med denne profil. Hvis denne ikke markeres, bliver der ikke beregnet rente for disse debitorer.                                           |
| Rykkerbrev | Vælg denne, hvis der skal genereres rykkere for debitorkonti med denne profil. Hvis denne ikke markeres, bliver der ikke genereret rykkere for disse debitorer.                                                 |
| Luk             | Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes. En post anses for lukket, når der er fuldt ud udlignet.             |



Du kan finde flere oplysninger i [Oversigt over debitorbetalinger](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
