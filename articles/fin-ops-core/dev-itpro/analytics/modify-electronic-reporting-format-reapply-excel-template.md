---
title: Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner
description: Dette emne beskriver, hvordan du kan redigere formatet for elektroniske rapportering (ER), der bruges til at generere forretningsdokumenter ved at anvende en Excel-skabelon, der er ændret.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f28760f42d16b6ffcd301f121e583542bce0fac0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559284"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="40ac3-103">Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner</span><span class="sxs-lookup"><span data-stu-id="40ac3-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40ac3-104">Værktøjet til elektronisk rapportering (ER) bruges til at oprette forretningsdokumenter i et elektronisk format.</span><span class="sxs-lookup"><span data-stu-id="40ac3-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="40ac3-105">For at generere et forretningsdokument, skal du oprette et ER-format, og derefter bruge ER-designeren til at definere layoutet for forretningsdokumentet og angive de data, der skal medtages i det.</span><span class="sxs-lookup"><span data-stu-id="40ac3-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="40ac3-106">Du kan derefter køre ER-formatet for at generere forretningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="40ac3-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="40ac3-107">ER-værktøjet kan bruges til at generere forretningsdokumenter som Microsoft Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="40ac3-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="40ac3-108">Du kan bruge et Excel-dokument som en skabelon for disse dokumenter.</span><span class="sxs-lookup"><span data-stu-id="40ac3-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="40ac3-109">For at definere dokumentets layout i ER-designeren kan du importere indholdet af det Excel-dokument, du vil bruge som skabelon til det definerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="40ac3-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="40ac3-110">For at få flere oplysninger og øve dig i dette scenarie kan du afspille opgaveguiden **Designe en ER-konfiguration til generering af rapporter i OPENXML-format** (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)).</span><span class="sxs-lookup"><span data-stu-id="40ac3-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="40ac3-111">Hvis du redigerer det Excel-dokument, der bruges som en skabelon til et forretningsdokument, giver ny ER-funktionalitet dig mulighed for at genanvende den opdaterede skabelon på ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="40ac3-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="40ac3-112">ER-formatet opdateres derefter, så det overholder den opdaterede skabelon.</span><span class="sxs-lookup"><span data-stu-id="40ac3-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="40ac3-113">Du kan få flere oplysninger om denne funktion ved at afspille opgaveguiden **Rediger et elektronisk rapporteringsformat ved at genanvende en Excel-skabelon** (som er en del af forretningsprocessen 7.5.5.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10683)).</span><span class="sxs-lookup"><span data-stu-id="40ac3-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="40ac3-114">I det trin i opgaveguiden, hvor du importerer en opdateret skabelon, skal du bruge den ændrede skabelon for Excel-filen Betalingsrapport, SampleVendPaymWsReport2, som skabelon.</span><span class="sxs-lookup"><span data-stu-id="40ac3-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]