---
title: Ændre formater ved at genanvende Excel-skabeloner
description: For at fuldføre trinene i denne procedure skal du først fuldføre proceduren Designe en ER-konfiguration til generering af rapporter i OPENXML-format.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5752caba9327475bb28c7bc6b0ee7e072f44f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327107"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="788cc-103">Ændre formater ved at genanvende Excel-skabeloner</span><span class="sxs-lookup"><span data-stu-id="788cc-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="788cc-104">For at fuldføre trinene i denne procedure skal du først fuldføre proceduren Designe en ER-konfiguration til generering af rapporter i OPENXML-format.</span><span class="sxs-lookup"><span data-stu-id="788cc-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="788cc-105">Denne procedure beskriver, hvordan du ændrer en konfiguration af et elektronisk rapporteringsformat (ER) ved at anvende en Microsoft Excel-skabelon, der er blevet ændret, igen.</span><span class="sxs-lookup"><span data-stu-id="788cc-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="788cc-106">I denne procedure skal du importere en ændret Excel-skabelon til ER-formatkonfigurationer, der er oprettet til eksempelfirmaet Litware, Inc., og derefter generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="788cc-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="788cc-107">Denne procedure er beregnet til brugere, der har rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="788cc-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="788cc-108">Disse trin kan udføres ved hjælp af GBSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="788cc-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="788cc-109">Før du begynder, skal du hente og gemme filen SampleVendPaymWsReport2.xlsx, som er anført i Hjælp-emnet Rediger et elektronisk rapporteringsformat ved at genanvende en Microsoft Excel-skabelon (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="788cc-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="788cc-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="788cc-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="788cc-111">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="788cc-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="788cc-112">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="788cc-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="788cc-113">Vælg ER-formatet</span><span class="sxs-lookup"><span data-stu-id="788cc-113">Select the ER format</span></span>
1. <span data-ttu-id="788cc-114">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="788cc-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="788cc-115">Udvid "Betalingsmodel" i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="788cc-116">Vælg 'Betalingsmodel\Eksempel på regnearksrapport' i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="788cc-117">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="788cc-117">Click Attachments.</span></span>
    * <span data-ttu-id="788cc-118">Bemærk, at Excel-filen SampleVendPaymWsReport.xlsx i øjeblikket bruges som skabelon ved behandling af betalingskladden.</span><span class="sxs-lookup"><span data-stu-id="788cc-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="788cc-119">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="788cc-119">Click Open.</span></span>
    * <span data-ttu-id="788cc-120">Klik på Åbn for at udforske layoutet for Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="788cc-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="788cc-121">Gennemse af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="788cc-121">Review the template.</span></span> <span data-ttu-id="788cc-122">Bemærk, at den aktuelt indeholder følgende oplysninger for hver betalingslinje: kreditorkontonummer, kreditornavnet, bank, registreringsnummer, kontonummer, debet, kredit og valuta.</span><span class="sxs-lookup"><span data-stu-id="788cc-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="788cc-123">I dette eksempel skal vil vi udvide denne liste ved at tilføje detaljer om betalingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="788cc-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="788cc-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="788cc-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="788cc-125">Genanvend en ny Excel-skabelon på ER-format</span><span class="sxs-lookup"><span data-stu-id="788cc-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="788cc-126">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="788cc-126">Click Designer.</span></span>
    * <span data-ttu-id="788cc-127">Åbn kladdeversionen af det valgte ER-format til redigering.</span><span class="sxs-lookup"><span data-stu-id="788cc-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="788cc-128">Klik på Importér i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="788cc-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="788cc-129">Klik på Opdater fra Excel.</span><span class="sxs-lookup"><span data-stu-id="788cc-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="788cc-130">Klik på 'Opdater skabelon', og vælg derefter filen SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="788cc-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="788cc-131">Klik på Opdater skabelon, og gennemse for at finde den SampleVendPaymWsReport2.xlsx-fil, du hentede tidligere.</span><span class="sxs-lookup"><span data-stu-id="788cc-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="788cc-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="788cc-132">Click OK.</span></span>
    * <span data-ttu-id="788cc-133">Skabelonen SampleVendPaymWsReport2.xlsx anvendes.</span><span class="sxs-lookup"><span data-stu-id="788cc-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="788cc-134">Strukturen af ER-formatet synkroniseres med indholdet af skabelonen, hvis elementer føjes til ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="788cc-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="788cc-135">Eventuelle eksisterende elementer i ER-formatet, der ikke findes i skabelonen, fjernes fra formatdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="788cc-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="788cc-136">Vælg Excel i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="788cc-137">Bemærk, at feltet Skabelon nu indeholder en reference til den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="788cc-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="788cc-138">Klik på Vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="788cc-138">Click Attachments.</span></span>
7. <span data-ttu-id="788cc-139">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="788cc-139">Click Open.</span></span>
    * <span data-ttu-id="788cc-140">Klik på Åbn for at udforske layoutet for den ændrede Excel-skabelon.</span><span class="sxs-lookup"><span data-stu-id="788cc-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="788cc-141">Gennemse af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="788cc-141">Review the template.</span></span> <span data-ttu-id="788cc-142">Bemærk, at det nu indeholder en linje til betalingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="788cc-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="788cc-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="788cc-143">Close the page.</span></span>
9. <span data-ttu-id="788cc-144">Udvid Excel i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="788cc-145">Udvid "Excel\PaymLines" i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="788cc-146">Vælg 'Excel\PaymLines\PaymDate' i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="788cc-147">Bemærk, at ER-formatet nu indeholder et element yderligere.</span><span class="sxs-lookup"><span data-stu-id="788cc-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="788cc-148">En celle, PaymDate, er blevet føjet til Excel-skabelonen.</span><span class="sxs-lookup"><span data-stu-id="788cc-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="788cc-149">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="788cc-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="788cc-150">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="788cc-151">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="788cc-152">Vælg "model\Betalinger\Transaktionsdato(TransactionDate)" i træet.</span><span class="sxs-lookup"><span data-stu-id="788cc-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="788cc-153">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="788cc-153">Click Bind.</span></span>
    * <span data-ttu-id="788cc-154">Angiv, hvilke data der skal føjes til den nye celle under kørslen.</span><span class="sxs-lookup"><span data-stu-id="788cc-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="788cc-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="788cc-155">Click Save.</span></span>
18. <span data-ttu-id="788cc-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="788cc-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="788cc-157">Aktivere den ændrede kladdeversion af ER-formatet til brug i behandling af betalingskladde</span><span class="sxs-lookup"><span data-stu-id="788cc-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="788cc-158">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="788cc-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="788cc-159">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="788cc-159">Click User parameters.</span></span>
3. <span data-ttu-id="788cc-160">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="788cc-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="788cc-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="788cc-161">Click OK.</span></span>
5. <span data-ttu-id="788cc-162">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="788cc-162">Click Edit.</span></span>
6. <span data-ttu-id="788cc-163">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="788cc-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="788cc-164">Bruge den ændrede kladdeversion af ER-formatet i behandling af betalingskladde</span><span class="sxs-lookup"><span data-stu-id="788cc-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="788cc-165">Gennemse det oprettede regneark, inklusive nye betalingslinjeoplysninger – betalingsdato.</span><span class="sxs-lookup"><span data-stu-id="788cc-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

