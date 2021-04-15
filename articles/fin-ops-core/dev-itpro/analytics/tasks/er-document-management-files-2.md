---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)'
description: Dette emne beskriver, hvordan du konfigurerer et ER-format (elektronisk rapportering) til at bruge dokumentstyringsfiler (vedhæftede filer) i ER-output. (Del 2)
author: NickSelin
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
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754908"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="bcc14-104">ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)</span><span class="sxs-lookup"><span data-stu-id="bcc14-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcc14-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="bcc14-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="bcc14-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="bcc14-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="bcc14-107">For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".</span><span class="sxs-lookup"><span data-stu-id="bcc14-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="bcc14-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="bcc14-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="bcc14-109">Udvid datamodellen for at vise filerne fra Dokumentstyring i den</span><span class="sxs-lookup"><span data-stu-id="bcc14-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="bcc14-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="bcc14-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bcc14-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bcc14-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="bcc14-112">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="bcc14-113">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="bcc14-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="bcc14-114">Click Designer.</span></span>
6. <span data-ttu-id="bcc14-115">Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="bcc14-116">Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="bcc14-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="bcc14-117">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bcc14-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="bcc14-118">Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bcc14-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="bcc14-119">Vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="bcc14-119">Invoice attachments</span></span>  
9. <span data-ttu-id="bcc14-120">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bcc14-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="bcc14-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bcc14-121">Click Add.</span></span>
11. <span data-ttu-id="bcc14-122">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bcc14-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="bcc14-123">Skriv 'Filindhold' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bcc14-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="bcc14-124">Filindhold</span><span class="sxs-lookup"><span data-stu-id="bcc14-124">File content</span></span>  
13. <span data-ttu-id="bcc14-125">Vælg "Container" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bcc14-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="bcc14-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bcc14-126">Click Add.</span></span>
15. <span data-ttu-id="bcc14-127">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bcc14-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="bcc14-128">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bcc14-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="bcc14-129">Filnavn</span><span class="sxs-lookup"><span data-stu-id="bcc14-129">File name</span></span>  
17. <span data-ttu-id="bcc14-130">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bcc14-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="bcc14-131">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bcc14-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="bcc14-132">Tilknyt nye datamodelelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="bcc14-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="bcc14-133">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="bcc14-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="bcc14-134">Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="bcc14-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="bcc14-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="bcc14-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="bcc14-136">Vi knytter nye modelelementer til relevante datakilder.</span><span class="sxs-lookup"><span data-stu-id="bcc14-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="bcc14-137">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="bcc14-137">Click Designer.</span></span>
4. <span data-ttu-id="bcc14-138">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="bcc14-139">Udvid 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="bcc14-140">Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="bcc14-141">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="bcc14-141">Click Edit.</span></span>
8. <span data-ttu-id="bcc14-142">Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="bcc14-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="bcc14-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="bcc14-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="bcc14-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcc14-144">Click Save.</span></span>
10. <span data-ttu-id="bcc14-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-145">Close the page.</span></span>
11. <span data-ttu-id="bcc14-146">Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="bcc14-147">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="bcc14-147">Click Edit.</span></span>
13. <span data-ttu-id="bcc14-148">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="bcc14-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="bcc14-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="bcc14-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="bcc14-150">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcc14-150">Click Save.</span></span>
15. <span data-ttu-id="bcc14-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-151">Close the page.</span></span>
16. <span data-ttu-id="bcc14-152">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="bcc14-153">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="bcc14-153">Click Edit.</span></span>
18. <span data-ttu-id="bcc14-154">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="bcc14-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="bcc14-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="bcc14-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="bcc14-156">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcc14-156">Click Save.</span></span>
20. <span data-ttu-id="bcc14-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-157">Close the page.</span></span>
21. <span data-ttu-id="bcc14-158">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bcc14-158">Click Save.</span></span>
22. <span data-ttu-id="bcc14-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-159">Close the page.</span></span>
23. <span data-ttu-id="bcc14-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-160">Close the page.</span></span>
24. <span data-ttu-id="bcc14-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bcc14-161">Close the page.</span></span>
25. <span data-ttu-id="bcc14-162">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="bcc14-162">Click Change status.</span></span>
26. <span data-ttu-id="bcc14-163">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="bcc14-163">Click Complete.</span></span>
27. <span data-ttu-id="bcc14-164">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="bcc14-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]