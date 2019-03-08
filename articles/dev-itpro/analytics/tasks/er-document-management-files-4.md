---
title: Køre formater til at bruge dokumentstyringsfiler i ER-output
description: Følgende trin beskriver, hvordan en bruger, der er tildelt rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER-output.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "364781"
---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="72493-103">Køre formater til at bruge dokumentstyringsfiler i ER-output</span><span class="sxs-lookup"><span data-stu-id="72493-103">Run formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72493-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="72493-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="72493-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="72493-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="72493-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 3: Opret model)".</span><span class="sxs-lookup"><span data-stu-id="72493-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="72493-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="72493-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="72493-108">Tilføj de nødvendige vedhæftede filer for en salgsordre til en enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="72493-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="72493-109">Gå til Debitor > Fakturaer > Åbne debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="72493-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="72493-110">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="72493-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="72493-111">Du kan for eksempel filtrere på feltet Faktura med værdien 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="72493-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="72493-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="72493-112">CIV-000148</span></span>  
3. <span data-ttu-id="72493-113">Klik for at følge linket til den valgte faktura.</span><span class="sxs-lookup"><span data-stu-id="72493-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="72493-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="72493-114">CIV-000148</span></span>  
4. <span data-ttu-id="72493-115">Klik for at følge linket i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="72493-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="72493-116">000148</span><span class="sxs-lookup"><span data-stu-id="72493-116">000148</span></span>  
5. <span data-ttu-id="72493-117">Vælg indstillingen Hoved i feltet Linjer eller hoved.</span><span class="sxs-lookup"><span data-stu-id="72493-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="72493-118">Marker Hoved for at angive, at dette vil være mål for tilføjelse af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="72493-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="72493-119">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="72493-119">Click Attach.</span></span>
    * <span data-ttu-id="72493-120">Tilføj et par filer som vedhæftede filer til denne salgsordre.</span><span class="sxs-lookup"><span data-stu-id="72493-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="72493-121">Brug filerne af de dokumenttyper, som understøttes i Dokumentstyring (med filtypenavne DOCX, DPF, XML, JPG osv.).</span><span class="sxs-lookup"><span data-stu-id="72493-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="72493-122">Gennemse og vælg filer, der skal vedhæftes og behandles yderligere med den relaterede faktura i den elektroniske ER-meddelelse.</span><span class="sxs-lookup"><span data-stu-id="72493-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="72493-123">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72493-123">Click New.</span></span>
8. <span data-ttu-id="72493-124">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="72493-124">Click File.</span></span>
9. <span data-ttu-id="72493-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="72493-125">Click New.</span></span>
10. <span data-ttu-id="72493-126">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="72493-126">Click File.</span></span>
11. <span data-ttu-id="72493-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72493-127">Close the page.</span></span>
12. <span data-ttu-id="72493-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72493-128">Close the page.</span></span>
13. <span data-ttu-id="72493-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72493-129">Close the page.</span></span>
14. <span data-ttu-id="72493-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="72493-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="72493-131">Kør rapporten, der er designet til den valgte faktura</span><span class="sxs-lookup"><span data-stu-id="72493-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="72493-132">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="72493-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="72493-133">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="72493-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="72493-134">Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="72493-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="72493-135">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.</span><span class="sxs-lookup"><span data-stu-id="72493-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="72493-136">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="72493-136">Click Run.</span></span>
6. <span data-ttu-id="72493-137">Udvid posterne for at inkludere sektion ().</span><span class="sxs-lookup"><span data-stu-id="72493-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="72493-138">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="72493-138">Click Filter.</span></span>
8. <span data-ttu-id="72493-139">Markér rækken Debitorfakturajournal og feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="72493-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="72493-140">Skriv "000148" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="72493-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="72493-141">Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="72493-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="72493-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="72493-142">Click OK.</span></span>
11. <span data-ttu-id="72493-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="72493-143">Click OK.</span></span>
    * <span data-ttu-id="72493-144">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="72493-144">Review the generated output.</span></span> <span data-ttu-id="72493-145">Bemærk, at der er oprettet en enkelt XML-node for hver vedhæftet fil.</span><span class="sxs-lookup"><span data-stu-id="72493-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="72493-146">Indholdet i den vedhæftede fil udfyldes til XML-outputtet i MIME-tekstformat (base64).</span><span class="sxs-lookup"><span data-stu-id="72493-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

