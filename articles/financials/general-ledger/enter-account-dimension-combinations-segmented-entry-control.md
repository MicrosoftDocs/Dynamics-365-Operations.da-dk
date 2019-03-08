---
title: Angiv kombinationer af konto og dimension (segmenteret postkontrolelement)
description: I denne artikel beskrives det, hvordan du indtaster kontoen og dimensionskombinationer eller finanskonti. Indtastningshandlingen kaldes ofte segmenteret postkontrolelement.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9addb2897bac68115a38f0239764ab65af2378c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "315653"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="6c5f9-104">Angiv kombinationer af konto og dimension (segmenteret postkontrolelement)</span><span class="sxs-lookup"><span data-stu-id="6c5f9-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c5f9-105">I denne artikel beskrives det, hvordan du indtaster kontoen og dimensionskombinationer eller finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="6c5f9-106">Indtastningshandlingen kaldes ofte segmenteret postkontrolelement.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="6c5f9-107">Brugere angiver kombinationer af konto og dimension på forskellige sider, f.eks. sider til finanskladder, budgettering og bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="6c5f9-108">Gyldige kombinationer af konto og dimension afhænger af de kontostrukturer, der er tildelt finans og de avancerede regler, der er tildelt kontostrukturerne.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="6c5f9-109">Når brugerne indtaster en kombination, kan de enten manuelt indtaste værdierne eller drage fordel af omfattende opslagsmuligheder.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="6c5f9-110">Når du angiver feltet, kan du begynde at skrive, og derefter søger det efter værdien og beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="6c5f9-111">For eksempel hvis du skriver 180 søger det efter enhver værdi, der begynder med denne talkombination.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="6c5f9-112">Eller du kan skrive kontanter, hvorefter det søger efter enhver værdi, som har en beskrivelse, der begynder med kontanter.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="6c5f9-113">Du kan også bruge jokertegn, f.eks. \*kontant eller \*180 til at søge, hvis værdien eller beskrivelsen indeholder søgekriterierne.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="6c5f9-114">I følgende tabel beskriver de tastaturgenveje, der kan bruges, når opslaget er lukket.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c5f9-115">Tastaturgenvej</span><span class="sxs-lookup"><span data-stu-id="6c5f9-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="6c5f9-116">Handling</span><span class="sxs-lookup"><span data-stu-id="6c5f9-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c5f9-117">Alt+pil ned</span><span class="sxs-lookup"><span data-stu-id="6c5f9-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="6c5f9-118">Åbn opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-118">Open the lookup.</span></span> <span data-ttu-id="6c5f9-119">Hvis du trykker på Alt + pil ned igen, flyttes fokus til segmenter i pop op-vinduet.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="6c5f9-120">Enter og Skift + Enter</span><span class="sxs-lookup"><span data-stu-id="6c5f9-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="6c5f9-121">Afgrænser til kontoplan</span><span class="sxs-lookup"><span data-stu-id="6c5f9-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="6c5f9-122">Højre pil og venstre pil</span><span class="sxs-lookup"><span data-stu-id="6c5f9-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="6c5f9-123">Flyt til næste eller forrige segment.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c5f9-124">Fane</span><span class="sxs-lookup"><span data-stu-id="6c5f9-124">Tab</span></span></td>
<td><span data-ttu-id="6c5f9-125">Flyt til næste felt i gitteret.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c5f9-126">I følgende tabel beskriver de tastaturgenveje, der kan bruges, når opslaget er åbent.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c5f9-127">Tastaturgenvej</span><span class="sxs-lookup"><span data-stu-id="6c5f9-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="6c5f9-128">Handling</span><span class="sxs-lookup"><span data-stu-id="6c5f9-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c5f9-129">Esc</span><span class="sxs-lookup"><span data-stu-id="6c5f9-129">Esc</span></span></td>
<td><span data-ttu-id="6c5f9-130">Luk opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="6c5f9-131">Pil op og pil ned</span><span class="sxs-lookup"><span data-stu-id="6c5f9-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="6c5f9-132">Page Up og Page Down</span><span class="sxs-lookup"><span data-stu-id="6c5f9-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="6c5f9-133">Home og End</span><span class="sxs-lookup"><span data-stu-id="6c5f9-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="6c5f9-134">Flyt til forrige eller næste værdi på listerne, til den forrige eller næste gruppe af værdier eller til det første eller sidste element i opslaget.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6c5f9-135">Afgrænser til kontoplan</span><span class="sxs-lookup"><span data-stu-id="6c5f9-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="6c5f9-136">Højre pil og venstre pil</span><span class="sxs-lookup"><span data-stu-id="6c5f9-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="6c5f9-137">Flyt til næste eller forrige segment.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c5f9-138">Fane</span><span class="sxs-lookup"><span data-stu-id="6c5f9-138">Tab</span></span></td>
<td><span data-ttu-id="6c5f9-139">Flyt til næste felt i gitteret.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c5f9-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="6c5f9-140">Alt+W</span></span></td>
<td><span data-ttu-id="6c5f9-141">Skift mellem <strong>Vis alle</strong> og <strong>Vis gyldige</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





