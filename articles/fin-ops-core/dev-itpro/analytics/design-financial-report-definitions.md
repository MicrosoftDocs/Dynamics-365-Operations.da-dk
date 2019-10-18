---
title: Rapportdefinitioner i Designer til økonomirapporter
description: Denne artikel indeholder oplysninger om rapportdefinitioner. En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også indstillinger til tilpasning af en rapport.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174138"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="4b5c4-105">Rapportdefinitioner i Designer til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="4b5c4-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b5c4-106">Denne artikel indeholder oplysninger om rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-106">This article provides information about report definitions.</span></span> <span data-ttu-id="4b5c4-107">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="4b5c4-108">En rapportdefinition indeholder også indstillinger til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="4b5c4-109">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="4b5c4-110">En rapportdefinition indeholder også yderligere indstillinger, som du kan anvende til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="4b5c4-111">Når du har defineret rækkedefinitioner og kolonnedefinitioner, skal du kombinere dem i en rapportdefinition.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="4b5c4-112">På dette tidspunkt definerer du også andre aspekter af definitionerne, som detaljeniveauet og rapportdatoen.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="4b5c4-113">Du kan derefter gemme og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-113">You can then save and generate a report.</span></span> <span data-ttu-id="4b5c4-114">Økonomirapportering har følgende detaljeniveauer:</span><span class="sxs-lookup"><span data-stu-id="4b5c4-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="4b5c4-115">Finansiel</span><span class="sxs-lookup"><span data-stu-id="4b5c4-115">Financial</span></span>
- <span data-ttu-id="4b5c4-116">Finans og Konto</span><span class="sxs-lookup"><span data-stu-id="4b5c4-116">Financial and Account</span></span>
- <span data-ttu-id="4b5c4-117">Finans, Konto og Transaktion</span><span class="sxs-lookup"><span data-stu-id="4b5c4-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="4b5c4-118">Afhængigt af hvordan dataene er lagret i Microsoft Dynamics ERP-systemet, er transaktionsdetaljerne dog muligvis ikke tilgængelige i rapporter.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="4b5c4-119">Oprette en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="4b5c4-119">Create a report definition</span></span>
1. <span data-ttu-id="4b5c4-120">I Report Designer skal du klikke på **Ny** i menuen **Filer**, og derefter skal du vælge **Rapportdefinition**.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="4b5c4-121">Angiv de relevante oplysninger på fanerne **Rapport**, **Output og fordeling**, **Sidehoveder og sidefødder** og **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="4b5c4-122">Indholdet af en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="4b5c4-122">Contents of a report definition</span></span>
<span data-ttu-id="4b5c4-123">Nedenstående tabel beskriver fanerne i en rapportdefinition, og hvordan oplysningerne bruges.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b5c4-124">Fane</span><span class="sxs-lookup"><span data-stu-id="4b5c4-124">Tab</span></span></th>
<th><span data-ttu-id="4b5c4-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4b5c4-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b5c4-126">Rapport</span><span class="sxs-lookup"><span data-stu-id="4b5c4-126">Report</span></span></td>
<td><span data-ttu-id="4b5c4-127">Opret en rapport, konfigurer en rapport eller rediger en eksisterende rapport.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b5c4-128">Output og distribution</span><span class="sxs-lookup"><span data-stu-id="4b5c4-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="4b5c4-129">Rediger rapportens outputtype og destination.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b5c4-130">Sidehoveder og sidefødder</span><span class="sxs-lookup"><span data-stu-id="4b5c4-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="4b5c4-131">Definer og formater sidehovederne og sidefødderne til rapporten.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="4b5c4-132">Du kan for eksempel tilføje tekst eller billeder til sidehovedet eller sidefoden.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="4b5c4-133">Økonomirapportering understøtter .bmp-, .jpg- og .png-billedfiler.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="4b5c4-134">Du kan også tilføje autotekstkoder for at indsætte andre oplysninger, f.eks et firmanavn, rapportnavn eller sidetal.</span><span class="sxs-lookup"><span data-stu-id="4b5c4-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b5c4-135">Indstillinger</span><span class="sxs-lookup"><span data-stu-id="4b5c4-135">Settings</span></span></td>
<td><span data-ttu-id="4b5c4-136">Angiv rapportdefinitionsindstillinger, f.eks. følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="4b5c4-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="4b5c4-137">Formater og afrund beløb</span><span class="sxs-lookup"><span data-stu-id="4b5c4-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="4b5c4-138">Formater detaljerapporter</span><span class="sxs-lookup"><span data-stu-id="4b5c4-138">Format detail reports</span></span></li>
<li><span data-ttu-id="4b5c4-139">Formater rapporteringstræer</span><span class="sxs-lookup"><span data-stu-id="4b5c4-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="4b5c4-140">Generér en undtagelsesrapport</span><span class="sxs-lookup"><span data-stu-id="4b5c4-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="4b5c4-141">Angiv valutaomregning</span><span class="sxs-lookup"><span data-stu-id="4b5c4-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="4b5c4-142">Oplysninger og filtrer kontodetaljer</span><span class="sxs-lookup"><span data-stu-id="4b5c4-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="4b5c4-143">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4b5c4-143">Additional resources</span></span>

[<span data-ttu-id="4b5c4-144">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="4b5c4-144">Financial reporting</span></span>](financial-reporting-intro.md)
