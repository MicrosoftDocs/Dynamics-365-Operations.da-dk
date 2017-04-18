---
title: "Syntaksen for avanceret filtrering og forespørgsler"
description: "I denne artikel beskrives de indstillinger for filtrering og forespørgsler, der er tilgængelige, når du bruger operatoren &quot;matches&quot; i dialogboksen Avanceret filtrering/sortering."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>Syntaksen for avanceret filtrering og forespørgsler

I denne artikel beskrives de indstillinger for filtrering og forespørgsler, der er tilgængelige, når du bruger operatoren "matches" i dialogboksen Avanceret filtrering/sortering.

<a name="advanced-query-syntax"></a>Avanceret forespørgselssyntaks
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Syntaks</th>
<th>Tegnbeskrivelse</th>
<th>Betegnelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>værdi</em></td>
<td>Lig med den værdi, der er angivet</td>
<td>Skriv værdien, der skal findes.</td>
<td><strong>Jensen</strong> finder &quot;Smith&quot;.</td>
</tr>
<tr class="even">
<td>! <em>værdi</em> (udråbstegnet)</td>
<td>Ikke lig med den værdi, der er angivet</td>
<td>Skriv et udråbstegn og den værdi, der skal udelades.</td>
<td><strong>! Jensen</strong> finder alle værdier undtagen &quot;Smith&quot;.</td>
</tr>
<tr class="odd">
<td><em>fra-værdi</em>..<em>til-værdi</em> (dobbelt punktum)</td>
<td>Mellem de to angivne værdier, der er adskilt af dobbelt punktum</td>
<td>Skriv fra-værdien, derefter to punktummer og til sidst til-værdien.</td>
<td><strong>1..10</strong> finder alle værdier fra 1 til 10. Men i et strengfelt, <strong>A.. C</strong> finder alle værdier, der starter med &quot;A&quot; og &quot;B&quot;, og værdier, der er helt identisk med &quot;C&quot;. For eksempel denne forespørgsel kan ikke finde &quot;Ca&quot;. At finde alle værdier fra &quot;A*&quot; gennem &quot;C*&quot;, type <strong>A.. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>værdi</em> (dobbelt punktum)</td>
<td>Mindre end eller lig med den værdi, der er angivet.</td>
<td>Skriv to punktummer og derefter værdien.</td>
<td><strong>.. 1000</strong> finder alle tal, der er mindre end eller lig med 1000, som &quot;100&quot;, &quot;999.95&quot;, og &quot;1.000&quot;.</td>
</tr>
<tr class="odd">
<td><em>værdi</em>.. (dobbelt punktum)</td>
<td>Større end eller lig med den værdi, der er angivet.</td>
<td>Skriv værdien og de to punktummer.</td>
<td><strong>1000..</strong> Finder alle tal, der er større end eller lig med 1000, som &quot;1.000&quot;, &quot;1,000.01&quot;, og &quot;1000000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>værdien</em> (større end-tegn)</td>
<td>Større end den værdi, der er angivet</td>
<td>Skriv et større end-tegn (<strong>&gt;</strong>) og derefter værdien.</td>
<td><strong>&gt;1000</strong> finder alle tal, der er større end 1000, som &quot;1000.01&quot;, &quot;20.000&quot;, og &quot;1000000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>værdien</em> (mindre end)</td>
<td>Mindre end den værdi, der er angivet</td>
<td>Skriv et mindre end-tegnet (<strong>&lt;</strong>) og derefter værdien.</td>
<td><strong>&lt;1000</strong> finder alle tal, der er mindre end 1000, som &quot;999.99&quot;, &quot;1&quot;, og &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>værdien</em>* (stjerne)</td>
<td>Starter med den værdi, der er angivet</td>
<td>Skriv startværdien og derefter en stjerne (<strong>*</strong>).</td>
<td><strong>S *</strong> søger efter en streng, der begynder med &quot;S&quot;, som &quot;Stockholm&quot;, &quot;Sydney&quot;, og &quot;San Francisco&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>Slutter med den værdi, der er angivet.</td>
<td>Skriv en stjerne og derefter slutværdien.</td>
<td><strong>* Øst</strong> søger efter en streng, der slutter med &quot;Øst&quot;, som &quot;nordøstlige&quot; og &quot;sydøstasiatiske&quot;.</td>
</tr>
<tr class="even">
<td>*<em>værdien</em>* (stjerne)</td>
<td>Indeholder den værdi, der er angivet</td>
<td>Skriv en stjerne, derefter en værdi og så en stjerne igen.</td>
<td><strong>*te*</strong> søger efter en streng, der indeholder &quot;te&quot;, som &quot;nordøstlige&quot; og &quot;sydøstasiatiske&quot;.</td>
</tr>
<tr class="odd">
<td>? (spørgsmålstegn)</td>
<td>Et eller flere ukendte tegn</td>
<td>Skriv et spørgsmålstegn det sted i værdien, hvor det ukendte tegn er placeret.</td>
<td><strong>SM? te</strong> finder &quot;Smith&quot; og &quot;Pedersen&quot;.</td>
</tr>
<tr class="even">
<td><em>værdi</em>,<em>værdi</em> (komma)</td>
<td>Svarer til de værdier, der er adskilt af kommaer</td>
<td>Skriv alle kriterierne, og adskil dem med kommaer.</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10, 20, 30, 100</strong> finder nøjagtigt &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL-sætning</span>) (SQL-sætning i parenteser)</td>
<td>Svarende til en defineret forespørgsel</td>
<td>Skriv en forespørgsel som en SQL-sætning mellem parenteser.</td>
<td><strong><span class="code">(datakilde. Feltnavn! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td> </td>
<td>Dags dato</td>
<td>Skriv <strong>T</strong>.</td>
<td><strong>T</strong> svarer til dags dato.</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode i parenteser)</td>
<td>Svarer til værdien eller intervallet af værdier, der er angivet af parametrene i metoden <strong>SysQueryRangeUtil</strong></td>
<td>Skriv en <strong>SysQueryRangeUtil</strong>-metode, der har parametre, som angiver værdien eller et interval af værdier.</td>
<td><ol>
<li>Klik på <strong>tilgodehavender</strong>&gt;<strong>fakturaer</strong>&gt;<strong>åbne debitorfakturaer</strong>.</li>
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
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dag (_relativeDays=0)</td>
<td>Find en dato i forhold til sessionsdatoen. Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</td>
<td><ul>
<li><strong>I morgen </strong> – Skriv <strong>(Day(1))</strong>.</li>
<li><strong>I dag</strong> – Skriv <strong>(Day(0))</strong>.</li>
<li><strong>I går</strong> – Skriv <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Find et datointerval i forhold til sessionsdatoen. Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</td>
<td><ul>
<li><strong>Sidste 30 dage</strong> – Skriv <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Seneste 30 dage og næste 30 dage</strong> – Skriv <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Find alle datoer efter den angivne relative dato.</td>
<td><ul>
<li><strong>Mere end 30 dage fra nu af</strong> – Skriv <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Find alle poster med dato og klokkeslæt efter det aktuelle tidspunkt.</td>
<td><ul>
<li><strong>Alle fremtidige datoer/klokkeslæt</strong> – Skriv <strong>(GreaterThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Find alle datoer før den angivne relative dato.</td>
<td><ul>
<li><strong>Mindre end syv dage fra nu af</strong> – Skriv <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Find alle poster med dato og klokkeslæt før det aktuelle tidspunkt.</td>
<td><ul>
<li><strong>Alle tidligere datoer og klokkeslæt</strong> – Skriv <strong>(LessThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Find et datointerval baseret på måneder i forhold til den aktuelle måned.</td>
<td><ul>
<li><strong>Forrige to måneder</strong> – Skriv <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Næste tre måneder</strong> – Skriv <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Find et datointerval baseret på år i forhold til det aktuelle år.</td>
<td><ul>
<li><strong>Næste år</strong> – Skriv <strong>(YearRange (0, 1))</strong>.</li>
<li><strong>Forrige år</strong> – Skriv <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



