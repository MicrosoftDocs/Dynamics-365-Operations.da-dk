---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)'
description: Dette emne beskriver, hvordan du konfigurerer en ER-model (elektronisk rapportering) til at bruge økonomiske dimensioner som datakilde til ER-rapporter. (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570186"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="38059-104">ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)</span><span class="sxs-lookup"><span data-stu-id="38059-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38059-105">Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="38059-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="38059-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="38059-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="38059-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="38059-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="38059-108">Opret en ny datamodel</span><span class="sxs-lookup"><span data-stu-id="38059-108">Create a new data model</span></span>
1. <span data-ttu-id="38059-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="38059-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="38059-110">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="38059-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="38059-111">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="38059-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="38059-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="38059-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="38059-113">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="38059-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="38059-114">Skriv 'Eksempelmodel til økonomiske dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="38059-115">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="38059-115">Click Create configuration.</span></span>
6. <span data-ttu-id="38059-116">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="38059-116">Click Designer.</span></span>
7. <span data-ttu-id="38059-117">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="38059-118">Skriv 'Post' et navn i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="38059-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-119">Click Add.</span></span>
10. <span data-ttu-id="38059-120">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="38059-121">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="38059-122">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-122">Click Add.</span></span>
    * <span data-ttu-id="38059-123">Vi vil føje en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="38059-123">We will add to our model a new record list.</span></span> <span data-ttu-id="38059-124">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) indstillingerne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="38059-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="38059-125">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens indstilling.</span><span class="sxs-lookup"><span data-stu-id="38059-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="38059-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="38059-127">Skriv 'Dimensionsindstilling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="38059-128">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="38059-129">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-129">Click Add.</span></span>
17. <span data-ttu-id="38059-130">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="38059-131">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="38059-132">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="38059-133">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-133">Click Add.</span></span>
21. <span data-ttu-id="38059-134">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="38059-135">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="38059-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-136">Click Add.</span></span>
24. <span data-ttu-id="38059-137">Vælg 'Post' i træet.</span><span class="sxs-lookup"><span data-stu-id="38059-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="38059-138">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="38059-139">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="38059-140">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="38059-141">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-141">Click Add.</span></span>
29. <span data-ttu-id="38059-142">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="38059-143">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="38059-144">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="38059-145">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-145">Click Add.</span></span>
33. <span data-ttu-id="38059-146">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="38059-147">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="38059-148">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="38059-149">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-149">Click Add.</span></span>
37. <span data-ttu-id="38059-150">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="38059-151">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="38059-152">Vælg "Dato" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="38059-153">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-153">Click Add.</span></span>
41. <span data-ttu-id="38059-154">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="38059-155">Skriv 'Debet' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="38059-156">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="38059-157">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-157">Click Add.</span></span>
45. <span data-ttu-id="38059-158">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="38059-159">Skriv "Kredit" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="38059-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-160">Click Add.</span></span>
48. <span data-ttu-id="38059-161">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="38059-162">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="38059-163">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="38059-164">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-164">Click Add.</span></span>
52. <span data-ttu-id="38059-165">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="38059-166">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="38059-167">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-167">Click Add.</span></span>
55. <span data-ttu-id="38059-168">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="38059-169">Skriv 'Dimensionsdata' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="38059-170">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="38059-171">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-171">Click Add.</span></span>
    * <span data-ttu-id="38059-172">Vi har føjet en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="38059-172">We added to our model a new record list.</span></span> <span data-ttu-id="38059-173">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) værdierne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="38059-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="38059-174">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens værdier.</span><span class="sxs-lookup"><span data-stu-id="38059-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="38059-175">Dimensionsnavnet præsenteres også i denne post som et felt, der skal bruges, hvis det er nødvendigt med henblik på valg.</span><span class="sxs-lookup"><span data-stu-id="38059-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="38059-176">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="38059-177">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="38059-178">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="38059-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="38059-179">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-179">Click Add.</span></span>
63. <span data-ttu-id="38059-180">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="38059-181">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="38059-182">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-182">Click Add.</span></span>
66. <span data-ttu-id="38059-183">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="38059-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="38059-184">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="38059-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="38059-185">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="38059-185">Click Add.</span></span>
69. <span data-ttu-id="38059-186">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="38059-186">Click Save.</span></span>
70. <span data-ttu-id="38059-187">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="38059-187">Close the page.</span></span>

![Side for ER-datamodeldesigner](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]