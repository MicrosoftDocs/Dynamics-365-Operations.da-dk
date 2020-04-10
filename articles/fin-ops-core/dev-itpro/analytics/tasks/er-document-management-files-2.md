---
title: 'ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd56ad01b00dfd0fe67f2d8eb36fb2bd39e04f1c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142587"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="0932e-103">ER Brug dokumentstyringsfiler i formatoutput (del 2: Udvidet datamodel)</span><span class="sxs-lookup"><span data-stu-id="0932e-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0932e-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="0932e-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0932e-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0932e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0932e-106">For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".</span><span class="sxs-lookup"><span data-stu-id="0932e-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="0932e-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0932e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="0932e-108">Udvid datamodellen for at vise filerne fra Dokumentstyring i den</span><span class="sxs-lookup"><span data-stu-id="0932e-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="0932e-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0932e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0932e-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0932e-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0932e-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="0932e-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="0932e-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0932e-113">Click Designer.</span></span>
6. <span data-ttu-id="0932e-114">Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="0932e-115">Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="0932e-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="0932e-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="0932e-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0932e-117">Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0932e-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="0932e-118">Vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="0932e-118">Invoice attachments</span></span>  
9. <span data-ttu-id="0932e-119">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="0932e-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="0932e-120">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0932e-120">Click Add.</span></span>
11. <span data-ttu-id="0932e-121">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="0932e-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0932e-122">Skriv 'Filindhold' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0932e-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="0932e-123">Filindhold</span><span class="sxs-lookup"><span data-stu-id="0932e-123">File content</span></span>  
13. <span data-ttu-id="0932e-124">Vælg "Container" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="0932e-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="0932e-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0932e-125">Click Add.</span></span>
15. <span data-ttu-id="0932e-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="0932e-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="0932e-127">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0932e-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="0932e-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="0932e-128">File name</span></span>  
17. <span data-ttu-id="0932e-129">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="0932e-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="0932e-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0932e-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="0932e-131">Tilknyt nye datamodelelementer til datakilder</span><span class="sxs-lookup"><span data-stu-id="0932e-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="0932e-132">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="0932e-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="0932e-133">Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="0932e-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="0932e-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="0932e-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="0932e-135">Vi knytter nye modelelementer til relevante datakilder.</span><span class="sxs-lookup"><span data-stu-id="0932e-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="0932e-136">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0932e-136">Click Designer.</span></span>
4. <span data-ttu-id="0932e-137">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="0932e-138">Udvid 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="0932e-139">Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="0932e-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0932e-140">Click Edit.</span></span>
8. <span data-ttu-id="0932e-141">Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0932e-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="0932e-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="0932e-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="0932e-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0932e-143">Click Save.</span></span>
10. <span data-ttu-id="0932e-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-144">Close the page.</span></span>
11. <span data-ttu-id="0932e-145">Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="0932e-146">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0932e-146">Click Edit.</span></span>
13. <span data-ttu-id="0932e-147">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0932e-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="0932e-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="0932e-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="0932e-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0932e-149">Click Save.</span></span>
15. <span data-ttu-id="0932e-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-150">Close the page.</span></span>
16. <span data-ttu-id="0932e-151">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="0932e-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="0932e-152">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0932e-152">Click Edit.</span></span>
18. <span data-ttu-id="0932e-153">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0932e-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="0932e-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="0932e-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="0932e-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0932e-155">Click Save.</span></span>
20. <span data-ttu-id="0932e-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-156">Close the page.</span></span>
21. <span data-ttu-id="0932e-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0932e-157">Click Save.</span></span>
22. <span data-ttu-id="0932e-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-158">Close the page.</span></span>
23. <span data-ttu-id="0932e-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-159">Close the page.</span></span>
24. <span data-ttu-id="0932e-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0932e-160">Close the page.</span></span>
25. <span data-ttu-id="0932e-161">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="0932e-161">Click Change status.</span></span>
26. <span data-ttu-id="0932e-162">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="0932e-162">Click Complete.</span></span>
27. <span data-ttu-id="0932e-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0932e-163">Click OK.</span></span>

