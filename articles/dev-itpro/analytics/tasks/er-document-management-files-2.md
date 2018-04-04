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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="26bac-103">Udvide datamodel til at bruge dokumentstyringsfiler i formatoutput til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="26bac-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26bac-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere et format til elektronisk rapportering (ER) til at bruge filer fra Dokumentstyring (vedhæftede filer) i ER.</span><span class="sxs-lookup"><span data-stu-id="26bac-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="26bac-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="26bac-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="26bac-106">For at fuldføre disse trin skal du først udføre trinnene i opgaveguiden "ER Brug filer fra Dokumentstyring i formatoutput (del 1: Forbered datamodel)".</span><span class="sxs-lookup"><span data-stu-id="26bac-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="26bac-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="26bac-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="26bac-108">Udvid datamodellen for at vise filerne fra Dokumentstyring i den</span><span class="sxs-lookup"><span data-stu-id="26bac-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="26bac-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="26bac-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="26bac-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="26bac-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="26bac-111">Udvid 'Debitorfakturamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="26bac-112">Vælg 'Debitorfakturamodel\Debitorfakturamodel (brugerdefineret)' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="26bac-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="26bac-113">Click Designer.</span></span>
6. <span data-ttu-id="26bac-114">Vælg 'Debitorfakturamodel(InvoiceCustomer)' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="26bac-115">Vi vil udvide denne datamodel for at se eventuelle filer, der er tilknyttet en salgsordre, som er relateret til en elektronisk behandlet faktura.</span><span class="sxs-lookup"><span data-stu-id="26bac-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="26bac-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="26bac-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="26bac-117">Skriv 'Vedhæftede filer i fakturaer' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="26bac-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="26bac-118">Vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="26bac-118">Invoice attachments</span></span>  
9. <span data-ttu-id="26bac-119">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="26bac-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="26bac-120">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="26bac-120">Click Add.</span></span>
11. <span data-ttu-id="26bac-121">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="26bac-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="26bac-122">Skriv 'Filindhold' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="26bac-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="26bac-123">Filindhold</span><span class="sxs-lookup"><span data-stu-id="26bac-123">File content</span></span>  
13. <span data-ttu-id="26bac-124">Vælg "Container" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="26bac-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="26bac-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="26bac-125">Click Add.</span></span>
15. <span data-ttu-id="26bac-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="26bac-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="26bac-127">Skriv "Filnavn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="26bac-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="26bac-128">Filnavn</span><span class="sxs-lookup"><span data-stu-id="26bac-128">File name</span></span>  
17. <span data-ttu-id="26bac-129">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="26bac-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="26bac-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="26bac-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="26bac-131">Knytte nye datamodelelementer til Dynamics 365 for Finance and Operations-datakilder</span><span class="sxs-lookup"><span data-stu-id="26bac-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="26bac-132">Klik på Tilknyt model til datakilde.</span><span class="sxs-lookup"><span data-stu-id="26bac-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="26bac-133">Brug Quick Filter til at filtrere på feltet Definition med værdien 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="26bac-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="26bac-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="26bac-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="26bac-135">Vi knytter nye modelelementer til relevante datakilder.</span><span class="sxs-lookup"><span data-stu-id="26bac-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="26bac-136">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="26bac-136">Click Designer.</span></span>
4. <span data-ttu-id="26bac-137">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="26bac-138">Udvid 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="26bac-139">Vælg 'Vedhæftede filer i fakturaer\Filnavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="26bac-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="26bac-140">Click Edit.</span></span>
8. <span data-ttu-id="26bac-141">Angiv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="26bac-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="26bac-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="26bac-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="26bac-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26bac-143">Click Save.</span></span>
10. <span data-ttu-id="26bac-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-144">Close the page.</span></span>
11. <span data-ttu-id="26bac-145">Vælg 'Vedhæftede filer i fakturaer\Filindhold' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="26bac-146">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="26bac-146">Click Edit.</span></span>
13. <span data-ttu-id="26bac-147">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="26bac-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="26bac-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.<'Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="26bac-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="26bac-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26bac-149">Click Save.</span></span>
15. <span data-ttu-id="26bac-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-150">Close the page.</span></span>
16. <span data-ttu-id="26bac-151">Vælg 'Vedhæftede filer i fakturaer' i træet.</span><span class="sxs-lookup"><span data-stu-id="26bac-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="26bac-152">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="26bac-152">Click Edit.</span></span>
18. <span data-ttu-id="26bac-153">Skriv 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="26bac-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="26bac-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="26bac-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="26bac-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26bac-155">Click Save.</span></span>
20. <span data-ttu-id="26bac-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-156">Close the page.</span></span>
21. <span data-ttu-id="26bac-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="26bac-157">Click Save.</span></span>
22. <span data-ttu-id="26bac-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-158">Close the page.</span></span>
23. <span data-ttu-id="26bac-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-159">Close the page.</span></span>
24. <span data-ttu-id="26bac-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26bac-160">Close the page.</span></span>
25. <span data-ttu-id="26bac-161">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="26bac-161">Click Change status.</span></span>
26. <span data-ttu-id="26bac-162">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="26bac-162">Click Complete.</span></span>
27. <span data-ttu-id="26bac-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="26bac-163">Click OK.</span></span>


