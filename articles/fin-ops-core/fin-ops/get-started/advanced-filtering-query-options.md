---
title: Syntaks for avanceret filtrering og forespørgsler
description: Denne artikel beskriver indstillingerne for filtrering og forespørgsler i dialogboksen Avanceret filtrering/sortering og operatoren matches i ruden Filter eller i filtre til gitterets kolonneoverskrifter.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89175763357f4309c4eb7874d0068586c5d9e726
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123942"
---
# <a name="advanced-filtering-and-query-syntax"></a>Avanceret filtrering og forespørgselssyntaks

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

I denne artikel beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering eller operatoren **matches** i ruden Filter eller i filtre til gitterets kolonneoverskrifter.

## <a name="advanced-query-syntax"></a>Avanceret forespørgselssyntaks

<table>
<thead>
<tr>
<th>Syntaks</th>
<th>Tegnbeskrivelse</th>
<th>Betegnelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>værdi</em></td>
<td>Lig med den værdi, der er angivet</td>
<td>Skriv værdien, der skal findes.</td>
<td><strong>Sørensen</strong> finder &quot;Sørensen&quot;.</td>
</tr>
<tr>
<td>!<em>værdi</em> (udråbstegn)</td>
<td>Ikke lig med den værdi, der er angivet</td>
<td>Skriv et udråbstegn og den værdi, der skal udelades.</td>
<td><strong>!Sørensen</strong> finder alle værdier undtagen &quot;Sørensen&quot;.</td>
</tr>
<tr>
<td><em>fra-værdi</em>..<em>til-værdi</em> (dobbelt punktum)</td>
<td>Mellem de to angivne værdier, der er adskilt af dobbelt punktum</td>
<td>Skriv fra-værdien, derefter to punktummer og til sidst til-værdien.</td>
<td><strong>1..10</strong> finder alle værdier fra 1 til og med 10. I strengfeltet <strong>A..C</strong> findes imidlertid alle værdier, der starter med &quot;A&quot; og &quot;B&quot;, og værdier, der svarer præcist til &quot;C&quot;. Denne forespørgsel finder f.eks. ikke &quot;Ca&quot;. Hvis du vil finde alle værdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skal du skrive <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>værdi</em> (dobbelt punktum)</td>
<td>Mindre end eller lig med den værdi, der er angivet.</td>
<td>Skriv to punktummer og derefter værdien.</td>
<td><strong>..1000</strong> finder eventuelle tal, der er mindre end eller lig med 1000, f.eks. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</td>
</tr>
<tr>
<td><em>værdi</em>.. (dobbelt punktum)</td>
<td>Større end eller lig med den værdi, der er angivet.</td>
<td>Skriv værdien og de to punktummer.</td>
<td><strong>1000..</strong> finder eventuelle tal, der er større end eller lig med 1000, f.eks. &quot;1.000&quot;, &quot;1.000,01&quot; og &quot;1.000.000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>værdi</em> (større end-tegn)</td>
<td>Større end den værdi, der er angivet</td>
<td>Skriv et større end-tegn (<strong>&gt;</strong>) og derefter værdien.</td>
<td><strong>&gt;1000</strong> finder eventuelle tal, der er større end 1000, f.eks. &quot;1000,01&quot;, &quot;20.000&quot; og &quot;1.000.000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>værdi</em> (mindre end-tegn)</td>
<td>Mindre end den værdi, der er angivet</td>
<td>Skriv et mindre end-tegn (<strong>&lt;</strong>) og derefter værdien.</td>
<td><strong>&lt;1000</strong> finder eventuelle tal, der er mindre end 1000, f.eks. &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>værdi</em>* (stjerne)</td>
<td>Starter med den værdi, der er angivet</td>
<td>Skriv startværdien og derefter en stjerne (<strong>*</strong>).</td>
<td><strong>S*</strong> finder enhver strenge, der starter med &quot;S&quot;, f.eks. &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>værdi</em> (stjerne)</td>
<td>Slutter med den værdi, der er angivet.</td>
<td>Skriv en stjerne og derefter slutværdien.</td>
<td><strong>*øst</strong> finder alle strenge, der slutter med &quot;øst&quot;, f.eks. &quot;Nordøst&quot; og &quot;Sydøst&quot;.</td>
</tr>
<tr>
<td>*<em>værdi</em>* (stjerne)</td>
<td>Indeholder den værdi, der er angivet</td>
<td>Skriv en stjerne, derefter en værdi og så en stjerne igen.</td>
<td><strong>*rd*</strong> finder alle strenge, der indeholder &quot;rd&quot;, f.eks. &quot;Nordøst&quot; og &quot;Nordvest&quot;.</td>
</tr>
<tr>
<td>? (spørgsmålstegn)</td>
<td>Et eller flere ukendte tegn</td>
<td>Skriv et spørgsmålstegn det sted i værdien, hvor det ukendte tegn er placeret.</td>
<td><strong>Pe?ersen</strong> finder &quot;Petersen&quot; og &quot;Pedersen&quot;.</td>
</tr>
<tr>
<td><em>værdi</em>,<em>værdi</em> (komma)</td>
<td>Svarer til de værdier, der er adskilt af kommaer</td>
<td>Skriv alle kriterierne, og adskil dem med kommaer.</td>
<td><strong>A, D, F, G</strong> finder nøjagtigt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;. <strong>10, 20, 30, 100</strong> finder nøjagtigt &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>"" (to dobbelte anførselstegn)</td>
<td>Matche en tom værdi</td>
<td>Skriv to fortløbende dobbelte anførselstegn for at filtrere efter tomme værdier i det pågældende felt.</td>
<td>To på hinanden følgende dobbelte anførselstegn (<strong>""</strong>) finder rækker uden værdi for den aktuelle kolonne.</td>
</tr>
<tr>
<td>(<span class="code">Finans- og driftsforespørgsel</span>) (finans- og driftsforespørgsel mellem parenteser)</td>
<td>Svarende til en defineret forespørgsel</td>
<td>Skriv en forespørgsel som en SQL-sætning mellem parenteser ved hjælp af finans- og driftsforespørgselssproget.</td>
  <td><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong><br><br> 
       som et eksempel på en filterbetingelse i et felt fra rodens datakilden samt et felt fra en anden datakilde (for siden Alle kunder)</td>
</tr>
<tr>
<td>V</td>
<td>Dags dato</td>
<td>Skriv <strong>T</strong>.</td>
<td><strong>T</strong> svarer til dags dato.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode i parenteser)</td>
<td>Svarer til værdien eller intervallet af værdier, der er angivet af parametrene i metoden <strong>SysQueryRangeUtil</strong></td>
<td>Skriv en <strong>SysQueryRangeUtil</strong>-metode, der har parametre, som angiver værdien eller et interval af værdier.</td>
<td>
<ol>
<li>Klik på <strong>Debitor</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åbne debitorfakturaer</strong>.</li>
<li>Tryk på Ctrl + Skift + F3 for at åbne siden <strong>Forespørgsel</strong>.</li>
<li>Klik på <strong>Tilføj</strong> under fanen <strong>Interval</strong>.</li>
<li>Vælg <strong>Åbne debitorposteringer</strong> i feltet <strong>Tabel</strong>.</li>
<li>Vælg <strong>Forfaldsdato</strong> i feltet <strong>Felt</strong>.</li>
<li>Skriv <strong>(yearRange(-2,0))</strong> i feltet <strong>Kriterier</strong>.</li>
<li>Klik på <strong>OK</strong>. Siden opdateres og viser de fakturaer, der opfylder de kriterier, du har angivet. I dette eksempel vises fakturaer, der var forfaldne de foregående to år, på siden.</li>
</ol>
Se tabellen i næste afsnit for at få flere oplysninger om datometoden <strong>SysQueryRangeUtil</strong> og flere eksempler.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Avancerede datoforespørgsler, der bruger SysQueryRangeUtil-metoder

<table>
<thead>
<tr>
<th>Metode</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>Dag (_relativeDays=0)</td>
<td>Find en dato i forhold til sessionsdatoen. Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</td>
<td>
<ul>
<li><strong>I morgen</strong> – Skriv <strong>(Day(1))</strong>.</li>
<li><strong>I dag</strong> – Skriv <strong>(Day(0))</strong>.</li>
<li><strong>I går</strong> – Skriv <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Find et datointerval i forhold til sessionsdatoen. Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</td>
<td>
<ul>
<li><strong>Sidste 30 dage</strong> – Skriv <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Seneste 30 dage og næste 30 dage</strong> – Skriv <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Find alle datoer efter den angivne relative dato.</td>
<td>
<ul>
<li><strong>Mere end 30 dage fra nu af</strong> – Skriv <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Find alle poster med dato og klokkeslæt efter det aktuelle tidspunkt.</td>
<td>
<ul>
<li><strong>Alle fremtidige datoer/klokkeslæt</strong> – Skriv <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Find alle datoer før den angivne relative dato.</td>
<td>
<ul>
<li><strong>Mindre end syv dage fra nu af</strong> – Skriv <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Find alle poster med dato og klokkeslæt før det aktuelle tidspunkt.</td>
<td>
<ul>
<li><strong>Alle tidligere datoer og klokkeslæt</strong> – Skriv <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Find et datointerval baseret på måneder i forhold til den aktuelle måned.</td>
<td>
<ul>
<li><strong>Forrige to måneder</strong> – Skriv <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Næste tre måneder</strong> – Skriv <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Find et datointerval baseret på år i forhold til det aktuelle år.</td>
<td>
<ul>
<li><strong>Næste år</strong> – Skriv <strong>(YearRange (0, 1))</strong>.</li>
<li><strong>Forrige år</strong> – Skriv <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
