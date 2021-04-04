---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til at bruge dokumentstyringsfiler (vedhæftede filer) i ER-output. (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559767"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="33f54-104">ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)</span><span class="sxs-lookup"><span data-stu-id="33f54-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33f54-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="33f54-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="33f54-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="33f54-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="33f54-107">For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".</span><span class="sxs-lookup"><span data-stu-id="33f54-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="33f54-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="33f54-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="33f54-109">Udvid datamodellen for at vise filerne fra Dokumentstyring i den</span><span class="sxs-lookup"><span data-stu-id="33f54-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="33f54-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="33f54-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="33f54-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="33f54-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="33f54-112">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="33f54-113">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="33f54-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="33f54-114">Click Designer.</span></span>
6. <span data-ttu-id="33f54-115">Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="33f54-116">Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="33f54-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="33f54-117">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="33f54-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="33f54-118">Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33f54-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="33f54-119">Vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="33f54-119">Invoice attachments</span></span>  
9. <span data-ttu-id="33f54-120">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="33f54-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="33f54-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="33f54-121">Click Add.</span></span>
11. <span data-ttu-id="33f54-122">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="33f54-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="33f54-123">Skriv 'Filindhold' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33f54-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="33f54-124">Filindhold</span><span class="sxs-lookup"><span data-stu-id="33f54-124">File content</span></span>  
13. <span data-ttu-id="33f54-125">Vælg "Container" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="33f54-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="33f54-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="33f54-126">Click Add.</span></span>
15. <span data-ttu-id="33f54-127">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="33f54-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="33f54-128">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="33f54-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="33f54-129">Filnavn</span><span class="sxs-lookup"><span data-stu-id="33f54-129">File name</span></span>  
17. <span data-ttu-id="33f54-130">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="33f54-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="33f54-131">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="33f54-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="33f54-132">Tilknyt nye datamodelelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="33f54-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="33f54-133">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="33f54-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="33f54-134">Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="33f54-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="33f54-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="33f54-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="33f54-136">Vi knytter nye modelelementer til relevante datakilder.</span><span class="sxs-lookup"><span data-stu-id="33f54-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="33f54-137">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="33f54-137">Click Designer.</span></span>
4. <span data-ttu-id="33f54-138">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="33f54-139">Udvid 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="33f54-140">Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="33f54-141">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="33f54-141">Click Edit.</span></span>
8. <span data-ttu-id="33f54-142">Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="33f54-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="33f54-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="33f54-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="33f54-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33f54-144">Click Save.</span></span>
10. <span data-ttu-id="33f54-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-145">Close the page.</span></span>
11. <span data-ttu-id="33f54-146">Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="33f54-147">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="33f54-147">Click Edit.</span></span>
13. <span data-ttu-id="33f54-148">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="33f54-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="33f54-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="33f54-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="33f54-150">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33f54-150">Click Save.</span></span>
15. <span data-ttu-id="33f54-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-151">Close the page.</span></span>
16. <span data-ttu-id="33f54-152">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="33f54-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="33f54-153">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="33f54-153">Click Edit.</span></span>
18. <span data-ttu-id="33f54-154">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="33f54-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="33f54-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="33f54-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="33f54-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33f54-156">Click Save.</span></span>
20. <span data-ttu-id="33f54-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-157">Close the page.</span></span>
21. <span data-ttu-id="33f54-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="33f54-158">Click Save.</span></span>
22. <span data-ttu-id="33f54-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-159">Close the page.</span></span>
23. <span data-ttu-id="33f54-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-160">Close the page.</span></span>
24. <span data-ttu-id="33f54-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="33f54-161">Close the page.</span></span>
25. <span data-ttu-id="33f54-162">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="33f54-162">Click Change status.</span></span>
26. <span data-ttu-id="33f54-163">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="33f54-163">Click Complete.</span></span>
27. <span data-ttu-id="33f54-164">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="33f54-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]