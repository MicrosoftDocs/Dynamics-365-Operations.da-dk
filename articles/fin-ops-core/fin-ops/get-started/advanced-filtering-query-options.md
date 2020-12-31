---
title: Avanceret filtrering og forespørgselssyntaks
description: I dette emne beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering, eller operatoren forekomster i ruden Filter eller i filtre til gitterets kolonneoverskrifter.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b867099b131594a64cad102e50ead7c355594f2b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694537"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="d8c93-103">Avanceret filtrering og forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="d8c93-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8c93-104">I dette emne beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering, eller operatoren **forekomster** i ruden Filter eller i filtre til gitterets kolonneoverskrifter.</span><span class="sxs-lookup"><span data-stu-id="d8c93-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="d8c93-105">Avanceret forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="d8c93-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d8c93-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d8c93-106">Syntax</span></span></th>
<th><span data-ttu-id="d8c93-107">Tegnbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d8c93-107">Character description</span></span></th>
<th><span data-ttu-id="d8c93-108">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d8c93-108">Description</span></span></th>
<th><span data-ttu-id="d8c93-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d8c93-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8c93-110"><em>værdi</em></span><span class="sxs-lookup"><span data-stu-id="d8c93-110"><em>value</em></span></span></td>
<td><span data-ttu-id="d8c93-111">Lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-112">Skriv værdien, der skal findes.</span><span class="sxs-lookup"><span data-stu-id="d8c93-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="d8c93-113"><strong>Sørensen</strong> finder &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-114">!<em>værdi</em> (udråbstegn)</span><span class="sxs-lookup"><span data-stu-id="d8c93-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="d8c93-115">Ikke lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-116">Skriv et udråbstegn og den værdi, der skal udelades.</span><span class="sxs-lookup"><span data-stu-id="d8c93-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="d8c93-117"><strong>!Sørensen</strong> finder alle værdier undtagen &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-118"><em>fra-værdi</em>..<em>til-værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="d8c93-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="d8c93-119">Mellem de to angivne værdier, der er adskilt af dobbelt punktum</span><span class="sxs-lookup"><span data-stu-id="d8c93-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="d8c93-120">Skriv fra-værdien, derefter to punktummer og til sidst til-værdien.</span><span class="sxs-lookup"><span data-stu-id="d8c93-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="d8c93-121"><strong>1..10</strong> finder alle værdier fra 1 til og med 10.</span><span class="sxs-lookup"><span data-stu-id="d8c93-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="d8c93-122">I strengfeltet <strong>A..C</strong> findes imidlertid alle værdier, der starter med &quot;A&quot; og &quot;B&quot;, og værdier, der svarer præcist til &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="d8c93-123">Denne forespørgsel finder f.eks. ikke &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="d8c93-124">Hvis du vil finde alle værdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skal du skrive <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-125">..<em>værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="d8c93-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="d8c93-126">Mindre end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="d8c93-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-127">Skriv to punktummer og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="d8c93-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="d8c93-128"><strong>..1000</strong> finder eventuelle tal, der er mindre end eller lig med 1000, f.eks. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-129"><em>værdi</em>..</span><span class="sxs-lookup"><span data-stu-id="d8c93-129"><em>value</em>..</span></span> <span data-ttu-id="d8c93-130">(dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="d8c93-130">(double period)</span></span></td>
<td><span data-ttu-id="d8c93-131">Større end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="d8c93-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-132">Skriv værdien og de to punktummer.</span><span class="sxs-lookup"><span data-stu-id="d8c93-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="d8c93-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="d8c93-133"><strong>1000..</strong></span></span> <span data-ttu-id="d8c93-134">finder eventuelle tal, der er større end eller lig med 1000, f.eks. &quot;1.000&quot;, &quot;1.000,01&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-135">&gt;<em>værdi</em> (større end-tegn)</span><span class="sxs-lookup"><span data-stu-id="d8c93-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="d8c93-136">Større end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-137">Skriv et større end-tegn (<strong>&gt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="d8c93-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="d8c93-138"><strong>&gt;1000</strong> finder eventuelle tal, der er større end 1000, f.eks. &quot;1000,01&quot;, &quot;20.000&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-139">&lt;<em>værdi</em> (mindre end-tegn)</span><span class="sxs-lookup"><span data-stu-id="d8c93-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="d8c93-140">Mindre end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-141">Skriv et mindre end-tegn (<strong>&lt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="d8c93-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="d8c93-142"><strong>&lt;1000</strong> finder eventuelle tal, der er mindre end 1000, f.eks. &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-143"><em>værdi</em>\* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="d8c93-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="d8c93-144">Starter med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-145">Skriv startværdien og derefter en stjerne (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="d8c93-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="d8c93-146"><strong>S\*</strong> finder enhver strenge, der starter med &quot;S&quot;, f.eks. &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-147">\*<em>værdi</em> (stjerne)</span><span class="sxs-lookup"><span data-stu-id="d8c93-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="d8c93-148">Slutter med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="d8c93-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-149">Skriv en stjerne og derefter slutværdien.</span><span class="sxs-lookup"><span data-stu-id="d8c93-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="d8c93-150"><strong>\*øst</strong> finder alle strenge, der slutter med &quot;øst&quot;, f.eks. &quot;Nordøst&quot; og &quot;Sydøst&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-151">*<em>værdi</em>* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="d8c93-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="d8c93-152">Indeholder den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="d8c93-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="d8c93-153">Skriv en stjerne, derefter en værdi og så en stjerne igen.</span><span class="sxs-lookup"><span data-stu-id="d8c93-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="d8c93-154"><strong>*rd*</strong> finder alle strenge, der indeholder &quot;rd&quot;, f.eks. &quot;Nordøst&quot; og &quot;Nordvest&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-155">?</span><span class="sxs-lookup"><span data-stu-id="d8c93-155">?</span></span> <span data-ttu-id="d8c93-156">(spørgsmålstegn)</span><span class="sxs-lookup"><span data-stu-id="d8c93-156">(question mark)</span></span></td>
<td><span data-ttu-id="d8c93-157">Et eller flere ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="d8c93-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="d8c93-158">Skriv et spørgsmålstegn det sted i værdien, hvor det ukendte tegn er placeret.</span><span class="sxs-lookup"><span data-stu-id="d8c93-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="d8c93-159"><strong>Pe?ersen</strong> finder &quot;Petersen&quot; og &quot;Pedersen&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-160"><em>værdi</em>,<em>værdi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="d8c93-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="d8c93-161">Svarer til de værdier, der er adskilt af kommaer</span><span class="sxs-lookup"><span data-stu-id="d8c93-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="d8c93-162">Skriv alle kriterierne, og adskil dem med kommaer.</span><span class="sxs-lookup"><span data-stu-id="d8c93-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="d8c93-163"><strong>A, D, F, G</strong> finder nøjagtigt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="d8c93-164"><strong>10, 20, 30, 100</strong> finder nøjagtigt &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="d8c93-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-165">"" (to dobbelte anførselstegn)</span><span class="sxs-lookup"><span data-stu-id="d8c93-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="d8c93-166">Matche en tom værdi</span><span class="sxs-lookup"><span data-stu-id="d8c93-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="d8c93-167">Skriv to fortløbende dobbelte anførselstegn for at filtrere efter tomme værdier i det pågældende felt.</span><span class="sxs-lookup"><span data-stu-id="d8c93-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="d8c93-168">To på hinanden følgende dobbelte anførselstegn (<strong>""</strong>) finder rækker uden værdi for den aktuelle kolonne.</span><span class="sxs-lookup"><span data-stu-id="d8c93-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-169">(<span class="code">Finance and Operations-forespørgsel</span>) (Finance and Operations-forespørgsel mellem parenteser)</span><span class="sxs-lookup"><span data-stu-id="d8c93-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="d8c93-170">Svarende til en defineret forespørgsel</span><span class="sxs-lookup"><span data-stu-id="d8c93-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="d8c93-171">Skriv en forespørgsel som en SQL-sætning mellem parenteser ved hjælp af Finance and Operations-forespørgselssproget.</span><span class="sxs-lookup"><span data-stu-id="d8c93-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="d8c93-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="d8c93-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="d8c93-173">som et eksempel på en filterbetingelse i et felt fra rodens datakilden samt et felt fra en anden datakilde (for siden Alle kunder)</span><span class="sxs-lookup"><span data-stu-id="d8c93-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-174">V</span><span class="sxs-lookup"><span data-stu-id="d8c93-174">T</span></span></td>
<td><span data-ttu-id="d8c93-175">Dags dato</span><span class="sxs-lookup"><span data-stu-id="d8c93-175">Today's date</span></span></td>
<td><span data-ttu-id="d8c93-176">Skriv <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="d8c93-177"><strong>T</strong> svarer til dags dato.</span><span class="sxs-lookup"><span data-stu-id="d8c93-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode i parenteser)</span><span class="sxs-lookup"><span data-stu-id="d8c93-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="d8c93-179">Svarer til værdien eller intervallet af værdier, der er angivet af parametrene i metoden <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="d8c93-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="d8c93-180">Skriv en <strong>SysQueryRangeUtil</strong>-metode, der har parametre, som angiver værdien eller et interval af værdier.</span><span class="sxs-lookup"><span data-stu-id="d8c93-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="d8c93-181">Klik på <strong>Debitor</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åbne debitorfakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-182">Tryk på Ctrl + Skift + F3 for at åbne siden <strong>Forespørgsel</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="d8c93-183">Klik på <strong>Tilføj</strong> under fanen <strong>Interval</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-184">Vælg <strong>Åbne debitorposteringer</strong> i feltet <strong>Tabel</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-185">Vælg <strong>Forfaldsdato</strong> i feltet <strong>Felt</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-186">Skriv <strong>(yearRange(-2,0))</strong> i feltet <strong>Kriterier</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-187">Klik på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="d8c93-188">Siden opdateres og viser de fakturaer, der opfylder de kriterier, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="d8c93-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="d8c93-189">I dette eksempel vises fakturaer, der var forfaldne de foregående to år, på siden.</span><span class="sxs-lookup"><span data-stu-id="d8c93-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="d8c93-190">Se tabellen i næste afsnit for at få flere oplysninger om datometoden <strong>SysQueryRangeUtil</strong> og flere eksempler.</span><span class="sxs-lookup"><span data-stu-id="d8c93-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="d8c93-191">Avancerede datoforespørgsler, der bruger SysQueryRangeUtil-metoder</span><span class="sxs-lookup"><span data-stu-id="d8c93-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d8c93-192">Metode</span><span class="sxs-lookup"><span data-stu-id="d8c93-192">Method</span></span></th>
<th><span data-ttu-id="d8c93-193">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d8c93-193">Description</span></span></th>
<th><span data-ttu-id="d8c93-194">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d8c93-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d8c93-195">Dag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="d8c93-196">Find en dato i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d8c93-196">Find a date relative to the session date.</span></span> <span data-ttu-id="d8c93-197">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="d8c93-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-198"><strong>I morgen</strong> – Skriv <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-199"><strong>I dag</strong> – Skriv <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-200"><strong>I går</strong> – Skriv <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="d8c93-202">Find et datointerval i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d8c93-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="d8c93-203">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="d8c93-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-204"><strong>Sidste 30 dage</strong> – Skriv <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-205"><strong>Seneste 30 dage og næste 30 dage</strong> – Skriv <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="d8c93-207">Find alle datoer efter den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="d8c93-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-208"><strong>Mere end 30 dage fra nu af</strong> – Skriv <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="d8c93-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="d8c93-210">Find alle poster med dato og klokkeslæt efter det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="d8c93-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-211"><strong>Alle fremtidige datoer/klokkeslæt</strong> – Skriv <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="d8c93-213">Find alle datoer før den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="d8c93-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-214"><strong>Mindre end syv dage fra nu af</strong> – Skriv <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="d8c93-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="d8c93-216">Find alle poster med dato og klokkeslæt før det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="d8c93-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-217"><strong>Alle tidligere datoer og klokkeslæt</strong> – Skriv <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="d8c93-219">Find et datointerval baseret på måneder i forhold til den aktuelle måned.</span><span class="sxs-lookup"><span data-stu-id="d8c93-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-220"><strong>Forrige to måneder</strong> – Skriv <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-221"><strong>Næste tre måneder</strong> – Skriv <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d8c93-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="d8c93-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="d8c93-223">Find et datointerval baseret på år i forhold til det aktuelle år.</span><span class="sxs-lookup"><span data-stu-id="d8c93-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="d8c93-224"><strong>Næste år</strong> – Skriv <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="d8c93-225"><strong>Forrige år</strong> – Skriv <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8c93-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
