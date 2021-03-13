---
title: ER Brug dokumentstyringsfiler i formatoutput (del 4 - Kørselsformat)
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til at bruge dokumentstyringsfiler i ER-output. (Del 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d437b31b8a55f345ebc3567bc8c6a2c5ecfd2eec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092510"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="213f1-104">ER Brug dokumentstyringsfiler i formatoutput (del 4 - Kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="213f1-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="213f1-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="213f1-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="213f1-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="213f1-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="213f1-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "ER Brug filer fra Dokumentstyring i formatoutput (del 3: Opret model)".</span><span class="sxs-lookup"><span data-stu-id="213f1-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="213f1-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="213f1-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="213f1-109">Tilføj de nødvendige vedhæftede filer for en salgsordre til en enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="213f1-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="213f1-110">Gå til Debitor > Fakturaer > Åbne debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="213f1-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="213f1-111">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="213f1-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="213f1-112">Du kan for eksempel filtrere på feltet Faktura med værdien 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="213f1-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="213f1-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="213f1-113">CIV-000148</span></span>  
3. <span data-ttu-id="213f1-114">Klik for at følge linket til den valgte faktura.</span><span class="sxs-lookup"><span data-stu-id="213f1-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="213f1-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="213f1-115">CIV-000148</span></span>  
4. <span data-ttu-id="213f1-116">Klik for at følge linket i feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="213f1-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="213f1-117">000148</span><span class="sxs-lookup"><span data-stu-id="213f1-117">000148</span></span>  
5. <span data-ttu-id="213f1-118">Vælg indstillingen Hoved i feltet Linjer eller hoved.</span><span class="sxs-lookup"><span data-stu-id="213f1-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="213f1-119">Marker Hoved for at angive, at dette vil være mål for tilføjelse af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="213f1-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="213f1-120">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="213f1-120">Click Attach.</span></span>
    * <span data-ttu-id="213f1-121">Tilføj et par filer som vedhæftede filer til denne salgsordre.</span><span class="sxs-lookup"><span data-stu-id="213f1-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="213f1-122">Brug filerne af de dokumenttyper, som understøttes i Dokumentstyring (med filtypenavne DOCX, DPF, XML, JPG osv.).</span><span class="sxs-lookup"><span data-stu-id="213f1-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="213f1-123">Gennemse og vælg filer, der skal vedhæftes og behandles yderligere med den relaterede faktura i den elektroniske ER-meddelelse.</span><span class="sxs-lookup"><span data-stu-id="213f1-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="213f1-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="213f1-124">Click New.</span></span>
8. <span data-ttu-id="213f1-125">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="213f1-125">Click File.</span></span>
9. <span data-ttu-id="213f1-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="213f1-126">Click New.</span></span>
10. <span data-ttu-id="213f1-127">Klik på Filer.</span><span class="sxs-lookup"><span data-stu-id="213f1-127">Click File.</span></span>
11. <span data-ttu-id="213f1-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="213f1-128">Close the page.</span></span>
12. <span data-ttu-id="213f1-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="213f1-129">Close the page.</span></span>
13. <span data-ttu-id="213f1-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="213f1-130">Close the page.</span></span>
14. <span data-ttu-id="213f1-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="213f1-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="213f1-132">Kør rapporten, der er designet til den valgte faktura</span><span class="sxs-lookup"><span data-stu-id="213f1-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="213f1-133">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="213f1-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="213f1-134">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="213f1-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="213f1-135">Udvid 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="213f1-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="213f1-136">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)\Eksempelmeddelelse i elektronisk faktura' i træet.</span><span class="sxs-lookup"><span data-stu-id="213f1-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="213f1-137">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="213f1-137">Click Run.</span></span>
6. <span data-ttu-id="213f1-138">Udvid posterne for at inkludere sektion ().</span><span class="sxs-lookup"><span data-stu-id="213f1-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="213f1-139">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="213f1-139">Click Filter.</span></span>
8. <span data-ttu-id="213f1-140">Markér rækken Debitorfakturajournal og feltet Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="213f1-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="213f1-141">Skriv "000148" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="213f1-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="213f1-142">Skriv ordrenummer 000148 i kriteriefeltet "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="213f1-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="213f1-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="213f1-143">Click OK.</span></span>
11. <span data-ttu-id="213f1-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="213f1-144">Click OK.</span></span>
    * <span data-ttu-id="213f1-145">Gennemse det genererede output.</span><span class="sxs-lookup"><span data-stu-id="213f1-145">Review the generated output.</span></span> <span data-ttu-id="213f1-146">Bemærk, at der er oprettet en enkelt XML-node for hver vedhæftet fil.</span><span class="sxs-lookup"><span data-stu-id="213f1-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="213f1-147">Indholdet i den vedhæftede fil udfyldes til XML-outputtet i MIME-tekstformat (base64).</span><span class="sxs-lookup"><span data-stu-id="213f1-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

