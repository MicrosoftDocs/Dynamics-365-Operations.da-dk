---
title: Debitor, posteringsprofiler
description: Debitorer, der bogfører profiler, styrer, hvordan debitortransaktioner bogføres til Finans.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff786d6e872e48f9605f9a472b7bffd409c5b3f
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830521"
---
# <a name="customer-posting-profiles"></a>Debitor, posteringsprofiler

[!include [banner](../includes/banner.md)]

Debitorer, der bogfører profiler, styrer, hvordan debitortransaktioner bogføres til Finans.

<a name="customer-posting-profiles"></a>Debitor, posteringsprofiler
-------------------------

Debitorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle debitorer, en gruppe debitorer eller en enkelt debitor. Disse indstillinger bruges, når du opretter salgsordrer, fritekstfakturaer, kontantbetalinger, rykkere og rentenotaer. For nogle transaktioner kan du vælge en posteringsprofil, der er anderledes end, og som prioriteres højere end de posteringsprofiler, der er oprettet for transaktioner på denne side. 

Standardposteringsprofilen defineres i oversigtspanelet Finans og Moms på siden Debitorparametre. Standardposteringsprofilen medtages derefter automatisk i hovedet i nye dokumenter, hvor du kan ændre den til en anden posteringsprofil, hvis det er nødvendigt.

Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden Definitioner af posteringsbogføring. I stedet for posteringsprofiler er det bogføringsdefinitioner, der styrer, hvordan debitorposter bogføres i finansmodulet.

## <a name="creating-a-posting-profile"></a>Oprette en posteringsprofil
Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil. Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil. Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge:

| Feltværdien **Kontokode** | Feltværdien **Konto/gruppenummer**            | Søgeprioritet |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabel**                    | Bestemt debitorkonto                       | 1               |
| **Gruppe**                    | Debitorgruppe, som debitor er tilknyttet | 2               |
| **Alle**                      | Tom                                           | 3               |

Hvis alle debitorposteringer skal have samme posteringsprofil, skal du kun definere én posteringsprofil med Alle i feltet Kontokode. Angiv følgende værdier for at definere en posteringsprofil:

<table>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Posteringsprofil</strong></td>
<td>Angiv en kode for posteringsprofilen. Eksempel: Hvis du vil have én konto for debitorsaldi i indenlandsk valuta og én konto for debitorsaldi i udenlandsk valuta, skal du oprette to posteringsprofiler. Du kan kalde den ene konto Indland og den anden Udland.</td>
</tr>
<tr class="even">
<td><strong>Beskrivelse</strong></td>
<td>Angiv en beskrivelse af posteringsprofilen. Dette bruges kun til at identificere posteringsprofilen bedre, når du ser den på denne side.</td>
</tr>
<tr class="odd">
<td><strong>Kontokode</strong></td>
<td>Angiv, om posteringsprofilen skal gælde for en bestemt debitor, en gruppe af debitorer eller alle debitorer:
<ul>
<li><strong>Tabel</strong> – Posteringsprofilen anvendes på en enkelt debitor. Vælg debitorkontoen i feltet Konto/gruppenummer.</li>
<li><strong>Gruppe</strong> – Posteringsprofilen anvendes på en debitorgruppe. Vælg debitorgruppen i feltet Konto/gruppenummer.</li>
<li><strong>Alle</strong> – Posteringsprofilen anvendes på alle debitorer. Lad feltet Konto/gruppenummer være tomt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/gruppenummer</strong></td>
<td>Hvis du vælger Tabel i feltet Kontokode, skal du vælge kontonummeret på den debitor, der er knyttet til posteringsprofilen. Hvis du vælger Gruppe, skal du vælge debitorgruppen. Hvis du vælger Alle, skal feltet stå tomt.</td>
</tr>
<tr class="odd">
<td><strong>Samlekonto</strong></td>
<td>Vælg den finanskonto, der skal bruges som samlekonto for de debitorer, som er tilknyttet posteringsprofilen.</td>
</tr>
<tr class="even">
<td><strong>Afregn konto</strong></td>
<td>Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter. Dette felt vises kun, hvis likviditetsbudgetter er aktiveret.</td>
</tr>
<tr class="odd">
<td><strong>Momsforudbetalinger</strong></td>
<td>Angiv kontonummeret for momsbetaling, der er modtaget forud.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Bemærk!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Brug siden Debitorparametre til at angive den posteringsprofil, der skal bruges, når en betaling er markeret som forudbetaling.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Passiver for rabatkonto</strong></td>
<td>Vælg finanskontoen til rabatpassiver.</td>
</tr>
<tr class="odd">
<td><strong>Rykkerforløb</strong></td>
<td>Vælg identifikationen for den rykkerserie, der skal bruges i forbindelse med debitorer, som har den aktuelle posteringsprofil tilknyttet.</td>
</tr>
<tr class="even">
<td><strong>Rentekode</strong></td>
<td>Vælg den rentekode, der skal bruges ved renteberegning for debitorer, som har den aktuelle posteringsprofil tilknyttet.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabelbegrænsninger**

For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere. Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.

Angiv følgende værdier for at definere en posteringsprofil:

| Felt                 | Beskrivelse                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Udligning**        | Vælg denne, hvis der skal kunne foretages automatisk udligning af poster med denne posteringsprofil. Hvis denne indstilling ikke er markeret, skal du manuelt udligne posteringer ved hjælp af siden Udligning af åbne posteringer eller siden Angiv debitorbetalinger. |
| **Renter**          | Vælg denne, hvis der skal beregnes rente på udestående saldi for debitorkonti med denne profil. Hvis denne ikke markeres, bliver der ikke beregnet rente for disse debitorer.                                           |
| **Rykker** | Vælg denne, hvis der skal genereres rykkere for debitorkonti med denne profil. Hvis denne ikke markeres, bliver der ikke genereret rykkere for disse debitorer.                                                 |
| **Luk**             | Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes. En post anses for lukket, når der er fuldt ud udlignet.                                                                           |



Du kan finde flere oplysninger i [Oversigt over debitorbetalinger](../cash-bank-management/tasks/customer-payment-overview.md).

