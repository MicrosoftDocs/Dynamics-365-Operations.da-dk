---
title: Kreditorposteringsprofil
description: "Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 76defe4dcb187ca948344ab9131eae981cbace3f
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-posting-profiles"></a>Kreditorposteringsprofil

Kreditorbogføringsprofiler styrer bogføringen af kreditortransaktioner til Finans.

<a name="vendor-posting-profiles"></a>Kreditorposteringsprofil
-----------------------

Kreditorposteringsprofiler giver dig mulighed for at tildele finanskonti og dokumentindstillinger til alle kreditorer, en gruppe kreditorer eller en enkelt kreditor. Disse indstillinger bruges, når du opretter indkøbsordrer, kreditorfakturaer og kontantbetalinger. For nogle transaktioner kan du vælge en posteringsprofil, der er anderledes end, og som prioriteres højere end de posteringsprofiler, der er oprettet for transaktioner på denne side. Standardposteringsprofilen defineres i oversigtspanelet Finans og Moms på siden Kreditorparametre. Standardposteringsprofilen medtages derefter automatisk i hovedet i nye dokumenter, hvor du kan ændre den til en anden posteringsprofil, hvis det er nødvendigt.

Du kan også knytte bogføringsdefinitioner til posteringsbogføringstyper på siden Definitioner af posteringsbogføring. I stedet for posteringsprofiler er det bogføringsdefinitioner, der styrer, hvordan kreditorposter bogføres i finansmodulet.

## <a name="creating-a-posting-profile"></a>Oprette en posteringsprofil
### <a name="setup"></a>**Opsætning**

Angiv de finanskonti, der skal bruges til bogføring af poster med den valgte posteringsprofil. Vælg en kontokode og – når det er muligt – en konto eller et gruppenummer til den valgte posteringsprofil. Under bogføringsprocessen finder programmet den posteringsprofil, der passer bedst til hver enkelt post, ved at søge efter den mest specifikke kombination af kontokode, kontonummer eller gruppe og nummer i følgende prioritetsrækkefølge:

| Feltværdien **Kontokode** | Feltværdien **Konto/gruppenummer**        | Søgeprioritet |
|------------------------------|---------------------------------------------|-----------------|
| **Tabel**                    | Specifik kreditorkonto                     | 1               |
| **Gruppe**                    | kreditorgruppe, som kreditoren er tildelt | 2               |
| **Alle**                      | Tom                                       | 3               |

Hvis alle kreditorposteringer skal have samme posteringsprofil, skal du kun definere én posteringsprofil med Alle i feltet Kontokode. Angiv følgende værdier for at definere en posteringsprofil:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Posteringsprofil</strong></td>
<td>Angiv en kode for posteringsprofilen. Du kan f.eks. oprette to posteringsprofiler for at have én konto til kreditorsaldi i indenlandsk valuta og én konto til kreditorsaldi i udenlandsk valuta. Du kan kalde den ene konto Indland og den anden Udland.</td>
</tr>
<tr class="even">
<td><strong>Beskrivelse</strong></td>
<td>Angiv en beskrivelse af posteringsprofilen.</td>
</tr>
<tr class="odd">
<td><strong>Kontokode</strong></td>
<td>Angiv, om posteringsprofilen skal gælde for en bestemt kreditor, en gruppe kreditorer eller alle kreditorer:
<ul>
<li><strong>Tabel</strong> – Posteringsprofilen anvendes til en enkelt kreditor. Vælg kreditorkontoen i feltet Konto/gruppenummer.</li>
<li><strong>Gruppe</strong> – Posteringsprofilen anvendes til en kreditorgruppe. Vælg kreditorgruppen i feltet Konto/gruppenummer.</li>
<li><strong>Alle</strong> – Posteringsprofilen anvendes til alle kreditorer. Lad feltet Konto/gruppenummer være tomt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/gruppenummer</strong></td>
<td>Hvis du vælger Tabel i feltet Kontokode, skal du vælge kontonummeret på den kreditor, der er knyttet til posteringsprofilen. Hvis Gruppe vælges, skal du vælge en kreditorgruppe. Hvis du vælger Alle, skal feltet stå tomt.</td>
</tr>
<tr class="odd">
<td><strong>Samlekonto</strong></td>
<td>Vælg den finanskonto, der skal bruges som samlekonto for de kreditorer, som posteringsprofilerne er tilknyttet.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Bemærk!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvis Brug bogføringsdefinitioner er valgt på siden Finans, bruges postbogføringsdefinitionen for kreditorfakturaer i stedet for samlekontoen.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Afregn konto</strong></td>
<td>Vælg den likviditetskonto i Finans, der bruges til likviditetsbudgetter. Dette felt er kun tilgængeligt, når likviditetsbudgettering er aktiveret.</td>
</tr>
<tr class="odd">
<td><strong>Momsforudbetalinger</strong></td>
<td>Vælg kontoen for momsbetaling, der er modtaget forud.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Bemærk!</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Den posteringsprofil, der bruges, når betalingen er markeret som forudbetaling er markeret i posteringsprofilen med feltet kladdebilag for forudbetaling i området Finans og Moms på siden Kreditorparametre.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Indlevering</strong></td>
<td>Vælg den finanskonto, som oplysninger om ikke-godkendte kreditorfakturaer skal bogføres på. Oplysningerne angives i indgangsbogskladden. En bruger angiver f.eks. meget grundlæggende oplysninger om kreditorfakturaer, når de modtages i indgangsbogen. Når indgangsbogen bogføres, bogføres posterne på den konto, der er angivet her og i feltet Modkonto. Når fakturaerne er godkendt, overføres gælden fra ankomstkontoen til den samlekonto, der bruges til kreditoren.</td>
</tr>
<tr class="odd">
<td><strong>Modkonto</strong></td>
<td>Vælg den finanskonto, der bruges som modkonto for ikke-godkendte kreditorfakturaer, der opdateres vha. indgangsbogen. Modkontoen fungerer som modkonto for poster, der bogføres på ankomstkonti. Derfor indeholder kontoen kreditorkøb, der endnu ikke er godkendt.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Tabelbegrænsninger**

For de posteringer, der har den valgte posteringsprofil, skal du angive, om posterne skal udlignes automatisk, om der skal beregnes rente og udsendes rykkere. Du kan også vælge den konto, der skal bruges, når poster med den valgte posteringsprofil lukkes.

Angiv følgende værdier for at definere en posteringsprofil:

| Felt          | Beskrivelse                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Udligning** | Vælg denne indstilling for at kunne foretage automatisk udligning af poster med denne posteringsprofil. Hvis ikke denne indstilling vælges, skal posteringerne udlignes manuelt på siden Udlign åbne posteringer. |
| **Annuller**     | Vælg denne indstilling, hvis du vil kunne annullere poster med denne posteringsprofil.                                                                                                               |
| **Luk**      | Vælg den posteringsprofil, der skal skiftes til, når poster med denne posteringsprofil lukkes. En post anses for lukket, når der er fuldt ud udlignet.                                       |




