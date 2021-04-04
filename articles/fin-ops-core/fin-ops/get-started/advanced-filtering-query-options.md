---
title: Avanceret filtrering og forespørgselssyntaks
description: I dette emne beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering, eller operatoren forekomster i ruden Filter eller i filtre til gitterets kolonneoverskrifter.
author: jasongre
manager: AnnBe
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
ms.openlocfilehash: 15805e24c46603afd34d40c5f94c1422b01cab4c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566060"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="71148-103">Avanceret filtrering og forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="71148-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71148-104">I dette emne beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering, eller operatoren **forekomster** i ruden Filter eller i filtre til gitterets kolonneoverskrifter.</span><span class="sxs-lookup"><span data-stu-id="71148-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="71148-105">Avanceret forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="71148-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71148-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="71148-106">Syntax</span></span></th>
<th><span data-ttu-id="71148-107">Tegnbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="71148-107">Character description</span></span></th>
<th><span data-ttu-id="71148-108">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="71148-108">Description</span></span></th>
<th><span data-ttu-id="71148-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="71148-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="71148-110"><em>værdi</em></span><span class="sxs-lookup"><span data-stu-id="71148-110"><em>value</em></span></span></td>
<td><span data-ttu-id="71148-111">Lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="71148-112">Skriv værdien, der skal findes.</span><span class="sxs-lookup"><span data-stu-id="71148-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="71148-113"><strong>Sørensen</strong> finder &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-114">!<em>værdi</em> (udråbstegn)</span><span class="sxs-lookup"><span data-stu-id="71148-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="71148-115">Ikke lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="71148-116">Skriv et udråbstegn og den værdi, der skal udelades.</span><span class="sxs-lookup"><span data-stu-id="71148-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="71148-117"><strong>!Sørensen</strong> finder alle værdier undtagen &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-118"><em>fra-værdi</em>..<em>til-værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="71148-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="71148-119">Mellem de to angivne værdier, der er adskilt af dobbelt punktum</span><span class="sxs-lookup"><span data-stu-id="71148-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="71148-120">Skriv fra-værdien, derefter to punktummer og til sidst til-værdien.</span><span class="sxs-lookup"><span data-stu-id="71148-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="71148-121"><strong>1..10</strong> finder alle værdier fra 1 til og med 10.</span><span class="sxs-lookup"><span data-stu-id="71148-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="71148-122">I strengfeltet <strong>A..C</strong> findes imidlertid alle værdier, der starter med &quot;A&quot; og &quot;B&quot;, og værdier, der svarer præcist til &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="71148-123">Denne forespørgsel finder f.eks. ikke &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="71148-124">Hvis du vil finde alle værdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skal du skrive <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-125">..<em>værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="71148-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="71148-126">Mindre end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="71148-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="71148-127">Skriv to punktummer og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="71148-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="71148-128"><strong>..1000</strong> finder eventuelle tal, der er mindre end eller lig med 1000, f.eks. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-129"><em>værdi</em>..</span><span class="sxs-lookup"><span data-stu-id="71148-129"><em>value</em>..</span></span> <span data-ttu-id="71148-130">(dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="71148-130">(double period)</span></span></td>
<td><span data-ttu-id="71148-131">Større end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="71148-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="71148-132">Skriv værdien og de to punktummer.</span><span class="sxs-lookup"><span data-stu-id="71148-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="71148-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="71148-133"><strong>1000..</strong></span></span> <span data-ttu-id="71148-134">finder eventuelle tal, der er større end eller lig med 1000, f.eks. &quot;1.000&quot;, &quot;1.000,01&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-135">&gt;<em>værdi</em> (større end-tegn)</span><span class="sxs-lookup"><span data-stu-id="71148-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="71148-136">Større end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="71148-137">Skriv et større end-tegn (<strong>&gt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="71148-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="71148-138"><strong>&gt;1000</strong> finder eventuelle tal, der er større end 1000, f.eks. &quot;1000,01&quot;, &quot;20.000&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-139">&lt;<em>værdi</em> (mindre end-tegn)</span><span class="sxs-lookup"><span data-stu-id="71148-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="71148-140">Mindre end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="71148-141">Skriv et mindre end-tegn (<strong>&lt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="71148-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="71148-142"><strong>&lt;1000</strong> finder eventuelle tal, der er mindre end 1000, f.eks. &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-143"><em>værdi</em>\* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="71148-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="71148-144">Starter med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="71148-145">Skriv startværdien og derefter en stjerne (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="71148-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="71148-146"><strong>S\*</strong> finder enhver strenge, der starter med &quot;S&quot;, f.eks. &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-147">\*<em>værdi</em> (stjerne)</span><span class="sxs-lookup"><span data-stu-id="71148-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="71148-148">Slutter med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="71148-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="71148-149">Skriv en stjerne og derefter slutværdien.</span><span class="sxs-lookup"><span data-stu-id="71148-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="71148-150"><strong>\*øst</strong> finder alle strenge, der slutter med &quot;øst&quot;, f.eks. &quot;Nordøst&quot; og &quot;Sydøst&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-151">*<em>værdi</em>* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="71148-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="71148-152">Indeholder den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="71148-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="71148-153">Skriv en stjerne, derefter en værdi og så en stjerne igen.</span><span class="sxs-lookup"><span data-stu-id="71148-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="71148-154"><strong>*rd*</strong> finder alle strenge, der indeholder &quot;rd&quot;, f.eks. &quot;Nordøst&quot; og &quot;Nordvest&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-155">?</span><span class="sxs-lookup"><span data-stu-id="71148-155">?</span></span> <span data-ttu-id="71148-156">(spørgsmålstegn)</span><span class="sxs-lookup"><span data-stu-id="71148-156">(question mark)</span></span></td>
<td><span data-ttu-id="71148-157">Et eller flere ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="71148-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="71148-158">Skriv et spørgsmålstegn det sted i værdien, hvor det ukendte tegn er placeret.</span><span class="sxs-lookup"><span data-stu-id="71148-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="71148-159"><strong>Pe?ersen</strong> finder &quot;Petersen&quot; og &quot;Pedersen&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-160"><em>værdi</em>,<em>værdi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="71148-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="71148-161">Svarer til de værdier, der er adskilt af kommaer</span><span class="sxs-lookup"><span data-stu-id="71148-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="71148-162">Skriv alle kriterierne, og adskil dem med kommaer.</span><span class="sxs-lookup"><span data-stu-id="71148-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="71148-163"><strong>A, D, F, G</strong> finder nøjagtigt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="71148-164"><strong>10, 20, 30, 100</strong> finder nøjagtigt &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="71148-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-165">"" (to dobbelte anførselstegn)</span><span class="sxs-lookup"><span data-stu-id="71148-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="71148-166">Matche en tom værdi</span><span class="sxs-lookup"><span data-stu-id="71148-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="71148-167">Skriv to fortløbende dobbelte anførselstegn for at filtrere efter tomme værdier i det pågældende felt.</span><span class="sxs-lookup"><span data-stu-id="71148-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="71148-168">To på hinanden følgende dobbelte anførselstegn (<strong>""</strong>) finder rækker uden værdi for den aktuelle kolonne.</span><span class="sxs-lookup"><span data-stu-id="71148-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-169">(<span class="code">Finance and Operations-forespørgsel</span>) (Finance and Operations-forespørgsel mellem parenteser)</span><span class="sxs-lookup"><span data-stu-id="71148-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="71148-170">Svarende til en defineret forespørgsel</span><span class="sxs-lookup"><span data-stu-id="71148-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="71148-171">Skriv en forespørgsel som en SQL-sætning mellem parenteser ved hjælp af Finance and Operations-forespørgselssproget.</span><span class="sxs-lookup"><span data-stu-id="71148-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="71148-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="71148-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="71148-173">som et eksempel på en filterbetingelse i et felt fra rodens datakilden samt et felt fra en anden datakilde (for siden Alle kunder)</span><span class="sxs-lookup"><span data-stu-id="71148-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-174">V</span><span class="sxs-lookup"><span data-stu-id="71148-174">T</span></span></td>
<td><span data-ttu-id="71148-175">Dags dato</span><span class="sxs-lookup"><span data-stu-id="71148-175">Today's date</span></span></td>
<td><span data-ttu-id="71148-176">Skriv <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="71148-177"><strong>T</strong> svarer til dags dato.</span><span class="sxs-lookup"><span data-stu-id="71148-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="71148-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode i parenteser)</span><span class="sxs-lookup"><span data-stu-id="71148-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="71148-179">Svarer til værdien eller intervallet af værdier, der er angivet af parametrene i metoden <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="71148-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="71148-180">Skriv en <strong>SysQueryRangeUtil</strong>-metode, der har parametre, som angiver værdien eller et interval af værdier.</span><span class="sxs-lookup"><span data-stu-id="71148-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="71148-181">Klik på <strong>Debitor</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åbne debitorfakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="71148-182">Tryk på Ctrl + Skift + F3 for at åbne siden <strong>Forespørgsel</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="71148-183">Klik på <strong>Tilføj</strong> under fanen <strong>Interval</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="71148-184">Vælg <strong>Åbne debitorposteringer</strong> i feltet <strong>Tabel</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="71148-185">Vælg <strong>Forfaldsdato</strong> i feltet <strong>Felt</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="71148-186">Skriv <strong>(yearRange(-2,0))</strong> i feltet <strong>Kriterier</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="71148-187">Klik på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="71148-188">Siden opdateres og viser de fakturaer, der opfylder de kriterier, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="71148-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="71148-189">I dette eksempel vises fakturaer, der var forfaldne de foregående to år, på siden.</span><span class="sxs-lookup"><span data-stu-id="71148-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="71148-190">Se tabellen i næste afsnit for at få flere oplysninger om datometoden <strong>SysQueryRangeUtil</strong> og flere eksempler.</span><span class="sxs-lookup"><span data-stu-id="71148-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="71148-191">Avancerede datoforespørgsler, der bruger SysQueryRangeUtil-metoder</span><span class="sxs-lookup"><span data-stu-id="71148-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="71148-192">Metode</span><span class="sxs-lookup"><span data-stu-id="71148-192">Method</span></span></th>
<th><span data-ttu-id="71148-193">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="71148-193">Description</span></span></th>
<th><span data-ttu-id="71148-194">Eksempel</span><span class="sxs-lookup"><span data-stu-id="71148-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="71148-195">Dag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="71148-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="71148-196">Find en dato i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="71148-196">Find a date relative to the session date.</span></span> <span data-ttu-id="71148-197">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="71148-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-198"><strong>I morgen</strong> – Skriv <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="71148-199"><strong>I dag</strong> – Skriv <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="71148-200"><strong>I går</strong> – Skriv <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="71148-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="71148-202">Find et datointerval i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="71148-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="71148-203">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="71148-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-204"><strong>Sidste 30 dage</strong> – Skriv <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="71148-205"><strong>Seneste 30 dage og næste 30 dage</strong> – Skriv <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="71148-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="71148-207">Find alle datoer efter den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="71148-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-208"><strong>Mere end 30 dage fra nu af</strong> – Skriv <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="71148-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="71148-210">Find alle poster med dato og klokkeslæt efter det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="71148-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-211"><strong>Alle fremtidige datoer/klokkeslæt</strong> – Skriv <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="71148-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="71148-213">Find alle datoer før den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="71148-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-214"><strong>Mindre end syv dage fra nu af</strong> – Skriv <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="71148-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="71148-216">Find alle poster med dato og klokkeslæt før det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="71148-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-217"><strong>Alle tidligere datoer og klokkeslæt</strong> – Skriv <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="71148-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="71148-219">Find et datointerval baseret på måneder i forhold til den aktuelle måned.</span><span class="sxs-lookup"><span data-stu-id="71148-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-220"><strong>Forrige to måneder</strong> – Skriv <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="71148-221"><strong>Næste tre måneder</strong> – Skriv <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="71148-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="71148-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="71148-223">Find et datointerval baseret på år i forhold til det aktuelle år.</span><span class="sxs-lookup"><span data-stu-id="71148-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="71148-224"><strong>Næste år</strong> – Skriv <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="71148-225"><strong>Forrige år</strong> – Skriv <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="71148-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]