---
title: Overvåge politikregler
description: Du kan bruge overvågningspolitikker til at sikre, at udgiftsrapporter, kreditorfakturaer og indkøbsordrer overholder de politikregler, du opretter. Alle de regler, der er knyttet til en overvågningspolitik, køres i batchtilstand i henhold til en tidsplan, du angiver.  Hver politikregel er en forekomst af en politikregeltype. Kun én politikregel ad gangen kan være aktiv for hver politikregeltype.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839587"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="a083d-106">Overvåge politikregler</span><span class="sxs-lookup"><span data-stu-id="a083d-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a083d-107">Du kan bruge overvågningspolitikker til at sikre, at udgiftsrapporter, kreditorfakturaer og indkøbsordrer overholder de politikregler, du opretter.</span><span class="sxs-lookup"><span data-stu-id="a083d-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="a083d-108">Alle de regler, der er knyttet til en overvågningspolitik, køres i batchtilstand i henhold til en tidsplan, du angiver.</span><span class="sxs-lookup"><span data-stu-id="a083d-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="a083d-109">Hver politikregel er en forekomst af en politikregeltype.</span><span class="sxs-lookup"><span data-stu-id="a083d-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="a083d-110">Kun én politikregel ad gangen kan være aktiv for hver politikregeltype.</span><span class="sxs-lookup"><span data-stu-id="a083d-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="a083d-111">Forespørgsler og forespørgselstyper</span><span class="sxs-lookup"><span data-stu-id="a083d-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="a083d-112">Når du opretter en overvågningspolitikregel, skal du først vælge en politikregeltype.</span><span class="sxs-lookup"><span data-stu-id="a083d-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="a083d-113">Politikregeltypen angiver den AOT-forespørgsel (Application Object Tree), der skal bruges som udgangspunkt for oprettelse af politikreglen.</span><span class="sxs-lookup"><span data-stu-id="a083d-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="a083d-114">Den angiver også den forespørgselstype, der skal bruges til politikreglen.</span><span class="sxs-lookup"><span data-stu-id="a083d-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="a083d-115">Forespørgslen definerer det kildedokument, som politikreglen evaluerer.</span><span class="sxs-lookup"><span data-stu-id="a083d-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="a083d-116">Den angiver også de felter i kildedokumentet, der identificerer både den juridiske enhed og det felt, der identificerer den dato, der skal bruges ved valg af dokumenter til overvågning.</span><span class="sxs-lookup"><span data-stu-id="a083d-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="a083d-117">Forespørgselstypen styrer standardfelterne på forespørgselssiden og på siden Regel for overvågning.</span><span class="sxs-lookup"><span data-stu-id="a083d-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="a083d-118">Følgende tabel viser de forespørgselstyper, der er tilgængelige for overvågningspolitikregler.</span><span class="sxs-lookup"><span data-stu-id="a083d-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a083d-119">Forespørgselstype</span><span class="sxs-lookup"><span data-stu-id="a083d-119">Query type</span></span></th>
<th><span data-ttu-id="a083d-120">Formål</span><span class="sxs-lookup"><span data-stu-id="a083d-120">Purpose</span></span></th>
<th><span data-ttu-id="a083d-121">Flere oplysninger</span><span class="sxs-lookup"><span data-stu-id="a083d-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a083d-122">Betinget</span><span class="sxs-lookup"><span data-stu-id="a083d-122">Conditional</span></span></td>
<td><span data-ttu-id="a083d-123">Evaluer kildedokumentattributter i forhold til angivne værdier.</span><span class="sxs-lookup"><span data-stu-id="a083d-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a083d-124">Aggregér</span><span class="sxs-lookup"><span data-stu-id="a083d-124">Aggregate</span></span></td>
<td><span data-ttu-id="a083d-125">Evaluer flere kildedokumenter eller kildedokumentlinjer i forhold til en politikregel ved aggregering af numeriske værdier.</span><span class="sxs-lookup"><span data-stu-id="a083d-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a083d-126">Stikprøvekontrol</span><span class="sxs-lookup"><span data-stu-id="a083d-126">Sampling</span></span></td>
<td><span data-ttu-id="a083d-127">Udvælg vilkårligt en angivet procentdel af kildedokumenterne, der skal evalueres for politikovertrædelser.</span><span class="sxs-lookup"><span data-stu-id="a083d-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="a083d-128">Når du vælger denne indstilling, skal du anvende siden Regel for overvågning til at angive procentdelen af dokumenter, der skal vælges tilfældigt til overvågning.</span><span class="sxs-lookup"><span data-stu-id="a083d-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a083d-129">Dupliker</span><span class="sxs-lookup"><span data-stu-id="a083d-129">Duplicate</span></span></td>
<td><span data-ttu-id="a083d-130">Evaluerer kildedokumenter for at afgøre, om de indeholder identiske poster i angivne felter.</span><span class="sxs-lookup"><span data-stu-id="a083d-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="a083d-131">Når du vælger denne indstilling, skal du anvende siden Regel for overvågning til at angive det antal dage, du vil føje til starten af datointervallet for dokumentvalg, når dokumenter evalueres for identiske poster.</span><span class="sxs-lookup"><span data-stu-id="a083d-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a083d-132">Listesøgning</span><span class="sxs-lookup"><span data-stu-id="a083d-132">List search</span></span></td>
<td><span data-ttu-id="a083d-133">Evaluer kildedokumenter for bestemte enheder.</span><span class="sxs-lookup"><span data-stu-id="a083d-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="a083d-134">Forespørgslens roddokument definerer det dokument, der overvåges.</span><span class="sxs-lookup"><span data-stu-id="a083d-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="a083d-135">Forespørgslen skal være en listeforespørgsel, der indeholder en reference til tabellen dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="a083d-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="a083d-136">Denne indstilling kan kun bruges med følgende AOT-forespørgsler:</span><span class="sxs-lookup"><span data-stu-id="a083d-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="a083d-137"><span class="ui">AuditPolicyExpenseList</span> (Udgiftsrapport - overvågede medarbejdere)</span><span class="sxs-lookup"><span data-stu-id="a083d-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="a083d-138"><span class="ui">AuditPolicyPurchList</span> (Indkøbsordre - overvågede kreditorer)</span><span class="sxs-lookup"><span data-stu-id="a083d-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="a083d-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditorfaktura - overvågede kreditorer)</span><span class="sxs-lookup"><span data-stu-id="a083d-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="a083d-140">Når du vælger denne indstilling, skal du angive de overvågede enheder på siden Regel for overvågning.</span><span class="sxs-lookup"><span data-stu-id="a083d-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a083d-141">Nøgleordssøgning</span><span class="sxs-lookup"><span data-stu-id="a083d-141">Keyword search</span></span></td>
<td><span data-ttu-id="a083d-142">Evaluer kildedokumenter for at afgøre, om de indeholder bestemte ord.</span><span class="sxs-lookup"><span data-stu-id="a083d-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="a083d-143">Når du vælger denne indstilling, skal du angive de ord, der skal ledes efter, på siden Regel for overvågning.</span><span class="sxs-lookup"><span data-stu-id="a083d-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="a083d-144">Siden Regel for overvågning indeholder indstillinger, så du kan angive de tabeller og felter, der skal evalueres for de ord, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="a083d-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="a083d-145">Fælles parametre</span><span class="sxs-lookup"><span data-stu-id="a083d-145">Common parameters</span></span>
<span data-ttu-id="a083d-146">Alle politikreglerne for en bestemt overvågningspolitik deler samme batchparametre og samme datointerval for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="a083d-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="a083d-147">Disse parametre angives for politikken på siden Flere indstillinger.</span><span class="sxs-lookup"><span data-stu-id="a083d-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="a083d-148">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a083d-148">Additional resources</span></span>
--------

<span data-ttu-id="a083d-149">[Overtrædelser af overvågningspolitik og sager](audit-policy-violations-cases.md)
[Definere revisionspolitikker for kildedokumenter](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="a083d-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


