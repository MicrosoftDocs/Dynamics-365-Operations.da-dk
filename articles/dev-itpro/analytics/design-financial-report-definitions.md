---
title: "Rapportdefinitioner i Designer til økonomirapporter"
description: "Denne artikel indeholder oplysninger om rapportdefinitioner. En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport. En rapportdefinition indeholder også indstillinger til tilpasning af en rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58030df8db467f754ec93ecc3f41585b20f03893
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="44540-105">Rapportdefinitioner i Designer til økonomirapporter</span><span class="sxs-lookup"><span data-stu-id="44540-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44540-106">Denne artikel indeholder oplysninger om rapportdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="44540-106">This article provides information about report definitions.</span></span> <span data-ttu-id="44540-107">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="44540-108">En rapportdefinition indeholder også indstillinger til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="44540-109">En rapportdefinition er en rapportkomponent (eller dokumentkomponent), der anvender en rækkedefinition, kolonnedefinition og valgfri rapporteringstrædefinition til at oprette en rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="44540-110">En rapportdefinition indeholder også yderligere indstillinger, som du kan anvende til tilpasning af en rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="44540-111">Når du har defineret rækkedefinitioner og kolonnedefinitioner, skal du kombinere dem i en rapportdefinition.</span><span class="sxs-lookup"><span data-stu-id="44540-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="44540-112">På dette tidspunkt definerer du også andre aspekter af definitionerne, som detaljeniveauet og rapportdatoen.</span><span class="sxs-lookup"><span data-stu-id="44540-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="44540-113">Du kan derefter gemme og generere en rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-113">You can then save and generate a report.</span></span> <span data-ttu-id="44540-114">Økonomirapportering har følgende detaljeniveauer:</span><span class="sxs-lookup"><span data-stu-id="44540-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="44540-115">Finansiel</span><span class="sxs-lookup"><span data-stu-id="44540-115">Financial</span></span>
-   <span data-ttu-id="44540-116">Finans og Konto</span><span class="sxs-lookup"><span data-stu-id="44540-116">Financial and Account</span></span>
-   <span data-ttu-id="44540-117">Finans, Konto og Transaktion</span><span class="sxs-lookup"><span data-stu-id="44540-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="44540-118">Afhængigt af hvordan data gemmes i Microsoft Dynamics ERP-systemet, er transaktionsdetaljer muligvis ikke tilgængelige i rapporter.</span><span class="sxs-lookup"><span data-stu-id="44540-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="44540-119">Oprette en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="44540-119">Create a report definition</span></span>
1.  <span data-ttu-id="44540-120">I Report Designer skal du klikke på **Ny** i menuen **Filer**, og derefter skal du vælge **Rapportdefinition**.</span><span class="sxs-lookup"><span data-stu-id="44540-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="44540-121">Angiv de relevante oplysninger på fanerne **Rapport**, **Output og fordeling**, **Sidehoveder og sidefødder** og **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="44540-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="44540-122">Indholdet af en rapportdefinition</span><span class="sxs-lookup"><span data-stu-id="44540-122">Contents of a report definition</span></span>
<span data-ttu-id="44540-123">Nedenstående tabel beskriver fanerne i en rapportdefinition, og hvordan oplysningerne bruges.</span><span class="sxs-lookup"><span data-stu-id="44540-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44540-124">Fane</span><span class="sxs-lookup"><span data-stu-id="44540-124">Tab</span></span></th>
<th><span data-ttu-id="44540-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="44540-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="44540-126">Rapport</span><span class="sxs-lookup"><span data-stu-id="44540-126">Report</span></span></td>
<td><span data-ttu-id="44540-127">Opret en rapport, konfigurer en rapport eller rediger en eksisterende rapport.</span><span class="sxs-lookup"><span data-stu-id="44540-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44540-128">Output og distribution</span><span class="sxs-lookup"><span data-stu-id="44540-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="44540-129">Rediger rapportens outputtype og destination.</span><span class="sxs-lookup"><span data-stu-id="44540-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="44540-130">Sidehoveder og sidefødder</span><span class="sxs-lookup"><span data-stu-id="44540-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="44540-131">Definer og formater sidehovederne og sidefødderne til rapporten.</span><span class="sxs-lookup"><span data-stu-id="44540-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="44540-132">Du kan for eksempel tilføje tekst eller billeder til sidehovedet eller sidefoden.</span><span class="sxs-lookup"><span data-stu-id="44540-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="44540-133">Økonomirapportering understøtter .bmp-, .jpg- og .png-billedfiler.</span><span class="sxs-lookup"><span data-stu-id="44540-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="44540-134">Du kan også tilføje autotekstkoder for at indsætte andre oplysninger, f.eks et firmanavn, rapportnavn eller sidetal.</span><span class="sxs-lookup"><span data-stu-id="44540-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="44540-135">Indstillinger</span><span class="sxs-lookup"><span data-stu-id="44540-135">Settings</span></span></td>
<td><span data-ttu-id="44540-136">Angiv rapportdefinitionsindstillinger, f.eks. følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="44540-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="44540-137">Formater og afrund beløb</span><span class="sxs-lookup"><span data-stu-id="44540-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="44540-138">Formater detaljerapporter</span><span class="sxs-lookup"><span data-stu-id="44540-138">Format detail reports</span></span></li>
<li><span data-ttu-id="44540-139">Formater rapporteringstræer</span><span class="sxs-lookup"><span data-stu-id="44540-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="44540-140">Generér en undtagelsesrapport</span><span class="sxs-lookup"><span data-stu-id="44540-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="44540-141">Angiv valutaomregning</span><span class="sxs-lookup"><span data-stu-id="44540-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="44540-142">Oplysninger og filtrer kontodetaljer</span><span class="sxs-lookup"><span data-stu-id="44540-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="44540-143">Se også</span><span class="sxs-lookup"><span data-stu-id="44540-143">See also</span></span>
--------

[<span data-ttu-id="44540-144">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="44540-144">Financial reporting</span></span>](financial-reporting-intro.md)




