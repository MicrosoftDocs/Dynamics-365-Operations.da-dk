---
title: Syntaks for avanceret filtrering og forespørgsler
description: I denne artikel beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering eller operatoren matches i ruden Filter eller i filtre til gitterets kolonneoverskrifter.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9e57cac740a26c6c5b451c92d856e533c6db33e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180823"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="07de1-103">Avanceret filtrering og forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="07de1-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07de1-104">I denne artikel beskrives indstillingerne for filtrering og forespørgsler, der er tilgængelige, når du bruger dialogboksen Avanceret filtrering/sortering eller operatoren **matches** i ruden Filter eller i filtre til gitterets kolonneoverskrifter.</span><span class="sxs-lookup"><span data-stu-id="07de1-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="07de1-105">Avanceret forespørgselssyntaks</span><span class="sxs-lookup"><span data-stu-id="07de1-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07de1-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="07de1-106">Syntax</span></span></th>
<th><span data-ttu-id="07de1-107">Tegnbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="07de1-107">Character description</span></span></th>
<th><span data-ttu-id="07de1-108">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="07de1-108">Description</span></span></th>
<th><span data-ttu-id="07de1-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="07de1-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07de1-110"><em>værdi</em></span><span class="sxs-lookup"><span data-stu-id="07de1-110"><em>value</em></span></span></td>
<td><span data-ttu-id="07de1-111">Lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-112">Skriv værdien, der skal findes.</span><span class="sxs-lookup"><span data-stu-id="07de1-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="07de1-113"><strong>Sørensen</strong> finder &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-114">!<em>værdi</em> (udråbstegn)</span><span class="sxs-lookup"><span data-stu-id="07de1-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="07de1-115">Ikke lig med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-116">Skriv et udråbstegn og den værdi, der skal udelades.</span><span class="sxs-lookup"><span data-stu-id="07de1-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="07de1-117"><strong>!Sørensen</strong> finder alle værdier undtagen &quot;Sørensen&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-118"><em>fra-værdi</em>..<em>til-værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="07de1-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="07de1-119">Mellem de to angivne værdier, der er adskilt af dobbelt punktum</span><span class="sxs-lookup"><span data-stu-id="07de1-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="07de1-120">Skriv fra-værdien, derefter to punktummer og til sidst til-værdien.</span><span class="sxs-lookup"><span data-stu-id="07de1-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="07de1-121"><strong>1..10</strong> finder alle værdier fra 1 til og med 10.</span><span class="sxs-lookup"><span data-stu-id="07de1-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="07de1-122">I strengfeltet <strong>A..C</strong> findes imidlertid alle værdier, der starter med &quot;A&quot; og &quot;B&quot;, og værdier, der svarer præcist til &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="07de1-123">Denne forespørgsel finder f.eks. ikke &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="07de1-124">Hvis du vil finde alle værdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skal du skrive <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-125">..<em>værdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="07de1-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="07de1-126">Mindre end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="07de1-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-127">Skriv to punktummer og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="07de1-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="07de1-128"><strong>..1000</strong> finder eventuelle tal, der er mindre end eller lig med 1000, f.eks. &quot;100&quot;, &quot;999,95&quot; og &quot;1.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-129"><em>værdi</em>..</span><span class="sxs-lookup"><span data-stu-id="07de1-129"><em>value</em>..</span></span> <span data-ttu-id="07de1-130">(dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="07de1-130">(double period)</span></span></td>
<td><span data-ttu-id="07de1-131">Større end eller lig med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="07de1-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-132">Skriv værdien og de to punktummer.</span><span class="sxs-lookup"><span data-stu-id="07de1-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="07de1-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="07de1-133"><strong>1000..</strong></span></span> <span data-ttu-id="07de1-134">finder eventuelle tal, der er større end eller lig med 1000, f.eks. &quot;1.000&quot;, &quot;1.000,01&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-135">&gt;<em>værdi</em> (større end-tegn)</span><span class="sxs-lookup"><span data-stu-id="07de1-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="07de1-136">Større end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-137">Skriv et større end-tegn (<strong>&gt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="07de1-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="07de1-138"><strong>&gt;1000</strong> finder eventuelle tal, der er større end 1000, f.eks. &quot;1000,01&quot;, &quot;20.000&quot; og &quot;1.000.000&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-139">&lt;<em>værdi</em> (mindre end-tegn)</span><span class="sxs-lookup"><span data-stu-id="07de1-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="07de1-140">Mindre end den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-141">Skriv et mindre end-tegn (<strong>&lt;</strong>) og derefter værdien.</span><span class="sxs-lookup"><span data-stu-id="07de1-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="07de1-142"><strong>&lt;1000</strong> finder eventuelle tal, der er mindre end 1000, f.eks. &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-143"><em>værdi</em>\* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="07de1-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="07de1-144">Starter med den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-145">Skriv startværdien og derefter en stjerne (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="07de1-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="07de1-146"><strong>S\*</strong> finder enhver strenge, der starter med &quot;S&quot;, f.eks. &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-147">\*<em>værdi</em> (stjerne)</span><span class="sxs-lookup"><span data-stu-id="07de1-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="07de1-148">Slutter med den værdi, der er angivet.</span><span class="sxs-lookup"><span data-stu-id="07de1-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-149">Skriv en stjerne og derefter slutværdien.</span><span class="sxs-lookup"><span data-stu-id="07de1-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="07de1-150"><strong>\*øst</strong> finder alle strenge, der slutter med &quot;øst&quot;, f.eks. &quot;Nordøst&quot; og &quot;Sydøst&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-151">*<em>værdi</em>* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="07de1-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="07de1-152">Indeholder den værdi, der er angivet</span><span class="sxs-lookup"><span data-stu-id="07de1-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="07de1-153">Skriv en stjerne, derefter en værdi og så en stjerne igen.</span><span class="sxs-lookup"><span data-stu-id="07de1-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="07de1-154"><strong>*rd*</strong> finder alle strenge, der indeholder &quot;rd&quot;, f.eks. &quot;Nordøst&quot; og &quot;Nordvest&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-155">?</span><span class="sxs-lookup"><span data-stu-id="07de1-155">?</span></span> <span data-ttu-id="07de1-156">(spørgsmålstegn)</span><span class="sxs-lookup"><span data-stu-id="07de1-156">(question mark)</span></span></td>
<td><span data-ttu-id="07de1-157">Et eller flere ukendte tegn</span><span class="sxs-lookup"><span data-stu-id="07de1-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="07de1-158">Skriv et spørgsmålstegn det sted i værdien, hvor det ukendte tegn er placeret.</span><span class="sxs-lookup"><span data-stu-id="07de1-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="07de1-159"><strong>Pe?ersen</strong> finder &quot;Petersen&quot; og &quot;Pedersen&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-160"><em>værdi</em>,<em>værdi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="07de1-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="07de1-161">Svarer til de værdier, der er adskilt af kommaer</span><span class="sxs-lookup"><span data-stu-id="07de1-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="07de1-162">Skriv alle kriterierne, og adskil dem med kommaer.</span><span class="sxs-lookup"><span data-stu-id="07de1-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="07de1-163"><strong>A, D, F, G</strong> finder nøjagtigt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="07de1-164"><strong>10, 20, 30, 100</strong> finder nøjagtigt &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="07de1-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-165">(<span class="code">SQL-sætning</span>) (SQL-sætning i parenteser)</span><span class="sxs-lookup"><span data-stu-id="07de1-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="07de1-166">Svarende til en defineret forespørgsel</span><span class="sxs-lookup"><span data-stu-id="07de1-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="07de1-167">Skriv en forespørgsel som en SQL-sætning mellem parenteser.</span><span class="sxs-lookup"><span data-stu-id="07de1-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="07de1-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="07de1-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-169">T</span><span class="sxs-lookup"><span data-stu-id="07de1-169">T</span></span></td>
<td><span data-ttu-id="07de1-170">Dags dato</span><span class="sxs-lookup"><span data-stu-id="07de1-170">Today's date</span></span></td>
<td><span data-ttu-id="07de1-171">Skriv <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="07de1-172"><strong>T</strong> svarer til dags dato.</span><span class="sxs-lookup"><span data-stu-id="07de1-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07de1-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metode i parenteser)</span><span class="sxs-lookup"><span data-stu-id="07de1-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="07de1-174">Svarer til værdien eller intervallet af værdier, der er angivet af parametrene i metoden <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="07de1-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="07de1-175">Skriv en <strong>SysQueryRangeUtil</strong>-metode, der har parametre, som angiver værdien eller et interval af værdier.</span><span class="sxs-lookup"><span data-stu-id="07de1-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="07de1-176">Klik på <strong>Debitor</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åbne debitorfakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="07de1-177">Tryk på Ctrl + Skift + F3 for at åbne siden <strong>Forespørgsel</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="07de1-178">Klik på <strong>Tilføj</strong> under fanen <strong>Interval</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="07de1-179">Vælg <strong>Åbne debitorposteringer</strong> i feltet <strong>Tabel</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="07de1-180">Vælg <strong>Forfaldsdato</strong> i feltet <strong>Felt</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="07de1-181">Skriv <strong>(yearRange(-2,0))</strong> i feltet <strong>Kriterier</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-182">Klik på <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="07de1-183">Siden opdateres og viser de fakturaer, der opfylder de kriterier, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="07de1-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="07de1-184">I dette eksempel vises fakturaer, der var forfaldne de foregående to år, på siden.</span><span class="sxs-lookup"><span data-stu-id="07de1-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="07de1-185">Se tabellen i næste afsnit for at få flere oplysninger om datometoden <strong>SysQueryRangeUtil</strong> og flere eksempler.</span><span class="sxs-lookup"><span data-stu-id="07de1-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="07de1-186">Avancerede datoforespørgsler, der bruger SysQueryRangeUtil-metoder</span><span class="sxs-lookup"><span data-stu-id="07de1-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07de1-187">Metode</span><span class="sxs-lookup"><span data-stu-id="07de1-187">Method</span></span></th>
<th><span data-ttu-id="07de1-188">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="07de1-188">Description</span></span></th>
<th><span data-ttu-id="07de1-189">Eksempel</span><span class="sxs-lookup"><span data-stu-id="07de1-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07de1-190">Dag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="07de1-191">Find en dato i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="07de1-191">Find a date relative to the session date.</span></span> <span data-ttu-id="07de1-192">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="07de1-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-193"><strong>I morgen</strong> – Skriv <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-194"><strong>I dag</strong> – Skriv <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-195"><strong>I går</strong> – Skriv <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="07de1-197">Find et datointerval i forhold til sessionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="07de1-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="07de1-198">Positive værdier angiver fremtidige datoer, og negative værdier angiver tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="07de1-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-199"><strong>Sidste 30 dage</strong> – Skriv <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-200"><strong>Seneste 30 dage og næste 30 dage</strong> – Skriv <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="07de1-202">Find alle datoer efter den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="07de1-202">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-203"><strong>Mere end 30 dage fra nu af</strong> – Skriv <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="07de1-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="07de1-205">Find alle poster med dato og klokkeslæt efter det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="07de1-205">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-206"><strong>Alle fremtidige datoer/klokkeslæt</strong> – Skriv <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="07de1-208">Find alle datoer før den angivne relative dato.</span><span class="sxs-lookup"><span data-stu-id="07de1-208">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-209"><strong>Mindre end syv dage fra nu af</strong> – Skriv <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="07de1-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="07de1-211">Find alle poster med dato og klokkeslæt før det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="07de1-211">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-212"><strong>Alle tidligere datoer og klokkeslæt</strong> – Skriv <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="07de1-214">Find et datointerval baseret på måneder i forhold til den aktuelle måned.</span><span class="sxs-lookup"><span data-stu-id="07de1-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-215"><strong>Forrige to måneder</strong> – Skriv <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-216"><strong>Næste tre måneder</strong> – Skriv <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="07de1-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="07de1-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="07de1-218">Find et datointerval baseret på år i forhold til det aktuelle år.</span><span class="sxs-lookup"><span data-stu-id="07de1-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="07de1-219"><strong>Næste år</strong> – Skriv <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="07de1-220"><strong>Forrige år</strong> – Skriv <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="07de1-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
