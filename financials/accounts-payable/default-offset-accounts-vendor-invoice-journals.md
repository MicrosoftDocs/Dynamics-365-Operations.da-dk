---
title: Standardmodkonti for kreditorfakturajournaler og fakturagodkendelseskladder
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="6f2e9-102">Standardmodkonti for kreditorfakturajournaler og fakturagodkendelseskladder</span><span class="sxs-lookup"><span data-stu-id="6f2e9-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="6f2e9-103">Standardmodkonti bruges på følgende sider for kreditorfakturakladder:</span><span class="sxs-lookup"><span data-stu-id="6f2e9-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="6f2e9-104">Fakturajournal</span><span class="sxs-lookup"><span data-stu-id="6f2e9-104">Invoice journal</span></span>
-   <span data-ttu-id="6f2e9-105"> Godkendelseskladde</span><span class="sxs-lookup"><span data-stu-id="6f2e9-105">Invoice approval journal</span></span>

<span data-ttu-id="6f2e9-106">Brug følgende tabel til at afgøre, hvor du bør tildele standardkonti for fakturakladder.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f2e9-107">Konfigurer standardkonti her</span><span class="sxs-lookup"><span data-stu-id="6f2e9-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="6f2e9-108">Hvor er standardkonti er</span><span class="sxs-lookup"><span data-stu-id="6f2e9-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="6f2e9-109">Hvordan denne indstilling påvirker behandling</span><span class="sxs-lookup"><span data-stu-id="6f2e9-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="6f2e9-110">Hvornår du skal bruge denne indstilling</span><span class="sxs-lookup"><span data-stu-id="6f2e9-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f2e9-111"><strong>Kreditorgruppe</strong> – Konfigurer standardmodkonti for kreditorgrupper på siden <strong>Standardkontoopsætning</strong>, som du kan åbne fra siden <strong>Kreditorgrupper</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2e9-112">Kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="6f2e9-112">Vendor account</span></span></li>
<li><span data-ttu-id="6f2e9-113">Kladdeposteringer for kreditorkonti i kreditorgruppen, hvis der ikke er angivet standardkonti for kreditorkonti</span><span class="sxs-lookup"><span data-stu-id="6f2e9-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="6f2e9-114">Standardmodkonti for kreditorgrupper vises som standardmodkonti for kreditorer på siden <strong>Standardkontoopsætning</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="6f2e9-115">Du kan åbne denne side fra listesiden <strong>Alle leverandører</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="6f2e9-116">Brug denne indstilling, hvis du typisk betaler for den samme slags ting fra samme kreditorgrupper over tid.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2e9-117"><strong>Kreditorkonto</strong> – Konfigurer standardmodkonti for kreditorkonti på siden <strong>Standardkontoopsætning</strong>, som du kan åbne fra siden <strong>Kreditorer</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="6f2e9-118">Kladdeposteringer for kreditorkontoen</span><span class="sxs-lookup"><span data-stu-id="6f2e9-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="6f2e9-119">Standardmodkonti for kreditorkonti vises som standardmodkonti til kladdeposteringer for kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="6f2e9-120">Brug denne indstilling, hvis du typisk betaler for den samme slags ting fra samme kreditorer over tid.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2e9-121"><strong>Kladdenavne</strong> – Konfigurer standardmodkonti for kladder på siden <strong>Kladdenavne</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="6f2e9-122">Vælg indstillingen <strong>Fast modkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="6f2e9-123">Bemærk, at du ikke kan angive standardmodkonti på kladdenavne, hvis typen af kladdenavnene, der er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2e9-124">Kladdehoved, der bruger kladdenavnet</span><span class="sxs-lookup"><span data-stu-id="6f2e9-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="6f2e9-125">Kladdeposteringer i kladder, der bruger kladdenavnet</span><span class="sxs-lookup"><span data-stu-id="6f2e9-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="6f2e9-126">Hvis indstillingen <strong>Fast modkonto</strong> på siden <strong>Kladdenavne</strong> er markeret, tilsidesætter modkontoen for kladdenavnet standardmodkontoen for kreditoren eller kreditorgruppen.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="6f2e9-127">Brug denne indstilling til at konfigurere kladder til specifikke omkostninger og udgifter, der opkræves på bestemte konti, uanset kreditoren eller hvilken kreditorgruppe kreditoren tilhører.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f2e9-128"><strong>Kladdenavne</strong> – Konfigurer standardmodkonti for kladder på siden <strong>Kladdenavne</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="6f2e9-129">Fjern indstillingen <strong>Fast modkonto</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="6f2e9-130">Bemærk, at du ikke kan angive standardmodkonti på kladdenavne, hvis typen af kladdenavnene, der er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f2e9-131">Kladdehoved</span><span class="sxs-lookup"><span data-stu-id="6f2e9-131">Journal header</span></span></li>
<li><span data-ttu-id="6f2e9-132">Kladdeposteringer i kladder, der bruger kladdenavnet</span><span class="sxs-lookup"><span data-stu-id="6f2e9-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="6f2e9-133">Disse standardposter bruges på kladdehovedsider, og modkontoen på kladdehovedsiden bruges som en standardpost på kladdebilagssiderne.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="6f2e9-134">Standardkonti fra siden <strong>Kladdenavne </strong>bruges kun, hvis standardkonti ikke er konfigureret til kreditorkontoen.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="6f2e9-135">Brug denne indstilling til at oprette de standardkonti, der bruges, når der ikke er tildelt en standardmodkonto for kreditor.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f2e9-136"><strong>Kladdehoved</strong> – Opret en standardmodkonto for en kladde som en standardpost på kladdebilagssiderne.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="6f2e9-137">Bemærk, at du ikke kan angive standardmodkonti på kladdehovedet, hvis typen af kladdenavnene er <strong>Indgangsbog</strong> eller <strong>Godkendelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="6f2e9-138">Kladdeposteringer i kladden</span><span class="sxs-lookup"><span data-stu-id="6f2e9-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="6f2e9-139">Standardmodkontoen for en kladde bruges som standardpost på kladdebilagssiderne.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="6f2e9-140">Brug denne indstilling til at gøre indtastningen af data hurtigere, hvis de fleste poster i en kladde har samme modkonto.</span><span class="sxs-lookup"><span data-stu-id="6f2e9-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






