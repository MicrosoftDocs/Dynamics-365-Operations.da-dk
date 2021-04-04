---
title: Rapportdefinitioner i Designer til økonomirapporter
description: Denne artikel indeholder oplysninger om rapportdefinitioner.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 073df430892e01d4842b2af147b0ae2765b1c66a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570336"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="a1672-103">Rapportdefinitioner i Designer til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="a1672-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1672-104">Denne artikel indeholder oplysninger om rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="a1672-104">This article provides information about report definitions.</span></span> <span data-ttu-id="a1672-105">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a1672-106">En rapportdefinition indeholder også indstillinger til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="a1672-107">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a1672-108">En rapportdefinition indeholder også yderligere indstillinger, som du kan anvende til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="a1672-109">Når du har defineret rækkedefinitioner og kolonnedefinitioner, skal du kombinere dem i en rapportdefinition.</span><span class="sxs-lookup"><span data-stu-id="a1672-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="a1672-110">På dette tidspunkt definerer du også andre aspekter af definitionerne, som detaljeniveauet og rapportdatoen.</span><span class="sxs-lookup"><span data-stu-id="a1672-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="a1672-111">Du kan derefter gemme og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-111">You can then save and generate a report.</span></span> <span data-ttu-id="a1672-112">Økonomirapportering har følgende detaljeniveauer:</span><span class="sxs-lookup"><span data-stu-id="a1672-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="a1672-113">Finansiel</span><span class="sxs-lookup"><span data-stu-id="a1672-113">Financial</span></span>
- <span data-ttu-id="a1672-114">Finans og Konto</span><span class="sxs-lookup"><span data-stu-id="a1672-114">Financial and Account</span></span>
- <span data-ttu-id="a1672-115">Finans, Konto og Transaktion</span><span class="sxs-lookup"><span data-stu-id="a1672-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="a1672-116">Afhængigt af hvordan dataene er lagret i Microsoft Dynamics ERP-systemet, er transaktionsdetaljerne dog muligvis ikke tilgængelige i rapporter.</span><span class="sxs-lookup"><span data-stu-id="a1672-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="a1672-117">Oprette en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="a1672-117">Create a report definition</span></span>
1. <span data-ttu-id="a1672-118">I Report Designer skal du klikke på **Ny** i menuen **Filer**, og derefter skal du vælge **Rapportdefinition**.</span><span class="sxs-lookup"><span data-stu-id="a1672-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="a1672-119">Angiv de relevante oplysninger på fanerne **Rapport**, **Output og fordeling**, **Sidehoveder og sidefødder** og **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a1672-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="a1672-120">Indholdet af en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="a1672-120">Contents of a report definition</span></span>
<span data-ttu-id="a1672-121">Nedenstående tabel beskriver fanerne i en rapportdefinition, og hvordan oplysningerne bruges.</span><span class="sxs-lookup"><span data-stu-id="a1672-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a1672-122">Fane</span><span class="sxs-lookup"><span data-stu-id="a1672-122">Tab</span></span></th>
<th><span data-ttu-id="a1672-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a1672-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1672-124">Rapport</span><span class="sxs-lookup"><span data-stu-id="a1672-124">Report</span></span></td>
<td><span data-ttu-id="a1672-125">Opret en rapport, konfigurer en rapport eller rediger en eksisterende rapport.</span><span class="sxs-lookup"><span data-stu-id="a1672-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1672-126">Output og distribution</span><span class="sxs-lookup"><span data-stu-id="a1672-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="a1672-127">Rediger rapportens outputtype og destination.</span><span class="sxs-lookup"><span data-stu-id="a1672-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1672-128">Sidehoveder og sidefødder</span><span class="sxs-lookup"><span data-stu-id="a1672-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="a1672-129">Definer og formater sidehovederne og sidefødderne til rapporten.</span><span class="sxs-lookup"><span data-stu-id="a1672-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="a1672-130">Du kan for eksempel tilføje tekst eller billeder til sidehovedet eller sidefoden.</span><span class="sxs-lookup"><span data-stu-id="a1672-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="a1672-131">Økonomirapportering understøtter .bmp-, .jpg- og .png-billedfiler.</span><span class="sxs-lookup"><span data-stu-id="a1672-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="a1672-132">Du kan også tilføje autotekstkoder for at indsætte andre oplysninger, f.eks et firmanavn, rapportnavn eller sidetal.</span><span class="sxs-lookup"><span data-stu-id="a1672-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1672-133">Indstillinger</span><span class="sxs-lookup"><span data-stu-id="a1672-133">Settings</span></span></td>
<td><span data-ttu-id="a1672-134">Angiv rapportdefinitionsindstillinger, f.eks. følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a1672-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="a1672-135">Formater og afrund beløb</span><span class="sxs-lookup"><span data-stu-id="a1672-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="a1672-136">Formater detaljerapporter</span><span class="sxs-lookup"><span data-stu-id="a1672-136">Format detail reports</span></span></li>
<li><span data-ttu-id="a1672-137">Formater rapporteringstræer</span><span class="sxs-lookup"><span data-stu-id="a1672-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="a1672-138">Generér en undtagelsesrapport</span><span class="sxs-lookup"><span data-stu-id="a1672-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="a1672-139">Angiv valutaomregning</span><span class="sxs-lookup"><span data-stu-id="a1672-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="a1672-140">Oplysninger og filtrer kontodetaljer</span><span class="sxs-lookup"><span data-stu-id="a1672-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="a1672-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a1672-141">Additional resources</span></span>

[<span data-ttu-id="a1672-142">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="a1672-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]