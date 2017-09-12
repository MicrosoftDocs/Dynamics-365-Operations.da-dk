--- 
title: Udvide datamodel til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1a5325dc3a97b9e205b41fe8dae18f43e430daeb
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="7a55e-103">Udvide datamodel til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="7a55e-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a55e-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="7a55e-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7a55e-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="7a55e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7a55e-106">For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".</span><span class="sxs-lookup"><span data-stu-id="7a55e-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="7a55e-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="7a55e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="7a55e-108">Udvid datamodellen for at vise filerne fra Dokumentstyring i den</span><span class="sxs-lookup"><span data-stu-id="7a55e-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="7a55e-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7a55e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7a55e-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7a55e-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7a55e-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7a55e-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="7a55e-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="7a55e-113">Click Designer.</span></span>
6. <span data-ttu-id="7a55e-114">Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="7a55e-115">Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="7a55e-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="7a55e-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="7a55e-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="7a55e-117">Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7a55e-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="7a55e-118">Vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="7a55e-118">Invoice attachments</span></span>  
9. <span data-ttu-id="7a55e-119">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="7a55e-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="7a55e-120">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7a55e-120">Click Add.</span></span>
11. <span data-ttu-id="7a55e-121">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="7a55e-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="7a55e-122">Skriv 'Filindhold' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7a55e-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="7a55e-123">Filindhold</span><span class="sxs-lookup"><span data-stu-id="7a55e-123">File content</span></span>  
13. <span data-ttu-id="7a55e-124">Vælg "Container" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="7a55e-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="7a55e-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7a55e-125">Click Add.</span></span>
15. <span data-ttu-id="7a55e-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="7a55e-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="7a55e-127">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7a55e-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="7a55e-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="7a55e-128">File name</span></span>  
17. <span data-ttu-id="7a55e-129">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="7a55e-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="7a55e-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7a55e-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="7a55e-131">Knytte nye datamodelelementer til Dynamics 365 for Finance and Operations, Enterprise edition-datakilder</span><span class="sxs-lookup"><span data-stu-id="7a55e-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="7a55e-132">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="7a55e-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="7a55e-133">Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="7a55e-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="7a55e-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7a55e-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="7a55e-135">Vi knytter nye modelelementer til relevante datakilder.</span><span class="sxs-lookup"><span data-stu-id="7a55e-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="7a55e-136">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="7a55e-136">Click Designer.</span></span>
4. <span data-ttu-id="7a55e-137">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="7a55e-138">Udvid 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="7a55e-139">Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="7a55e-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7a55e-140">Click Edit.</span></span>
8. <span data-ttu-id="7a55e-141">Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="7a55e-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="7a55e-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="7a55e-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="7a55e-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7a55e-143">Click Save.</span></span>
10. <span data-ttu-id="7a55e-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-144">Close the page.</span></span>
11. <span data-ttu-id="7a55e-145">Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="7a55e-146">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7a55e-146">Click Edit.</span></span>
13. <span data-ttu-id="7a55e-147">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="7a55e-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="7a55e-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="7a55e-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="7a55e-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7a55e-149">Click Save.</span></span>
15. <span data-ttu-id="7a55e-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-150">Close the page.</span></span>
16. <span data-ttu-id="7a55e-151">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="7a55e-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="7a55e-152">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7a55e-152">Click Edit.</span></span>
18. <span data-ttu-id="7a55e-153">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="7a55e-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="7a55e-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="7a55e-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="7a55e-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7a55e-155">Click Save.</span></span>
20. <span data-ttu-id="7a55e-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-156">Close the page.</span></span>
21. <span data-ttu-id="7a55e-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7a55e-157">Click Save.</span></span>
22. <span data-ttu-id="7a55e-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-158">Close the page.</span></span>
23. <span data-ttu-id="7a55e-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-159">Close the page.</span></span>
24. <span data-ttu-id="7a55e-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a55e-160">Close the page.</span></span>
25. <span data-ttu-id="7a55e-161">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="7a55e-161">Click Change status.</span></span>
26. <span data-ttu-id="7a55e-162">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="7a55e-162">Click Complete.</span></span>
27. <span data-ttu-id="7a55e-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7a55e-163">Click OK.</span></span>


