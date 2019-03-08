---
title: 'ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)'
description: Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84f546b73eefe3ead78c6ab3fdbbc05d0db5fef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "339504"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="bbcd8-103">ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)</span><span class="sxs-lookup"><span data-stu-id="bbcd8-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbcd8-104">Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="bbcd8-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bbcd8-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="bbcd8-107">Opret en ny datamodel</span><span class="sxs-lookup"><span data-stu-id="bbcd8-107">Create a new data model</span></span>
1. <span data-ttu-id="bbcd8-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="bbcd8-109">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="bbcd8-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="bbcd8-110">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="bbcd8-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="bbcd8-112">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="bbcd8-113">Skriv 'Eksempelmodel til økonomiske dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="bbcd8-114">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-114">Click Create configuration.</span></span>
6. <span data-ttu-id="bbcd8-115">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-115">Click Designer.</span></span>
7. <span data-ttu-id="bbcd8-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="bbcd8-117">Skriv 'Post' et navn i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="bbcd8-118">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-118">Click Add.</span></span>
10. <span data-ttu-id="bbcd8-119">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="bbcd8-120">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="bbcd8-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-121">Click Add.</span></span>
    * <span data-ttu-id="bbcd8-122">Vi vil føje en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-122">We will add to our model a new record list.</span></span> <span data-ttu-id="bbcd8-123">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) indstillingerne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="bbcd8-124">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens indstilling.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="bbcd8-125">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="bbcd8-126">Skriv 'Dimensionsindstilling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="bbcd8-127">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="bbcd8-128">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-128">Click Add.</span></span>
17. <span data-ttu-id="bbcd8-129">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="bbcd8-130">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="bbcd8-131">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="bbcd8-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-132">Click Add.</span></span>
21. <span data-ttu-id="bbcd8-133">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="bbcd8-134">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="bbcd8-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-135">Click Add.</span></span>
24. <span data-ttu-id="bbcd8-136">Vælg 'Post' i træet.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="bbcd8-137">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="bbcd8-138">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="bbcd8-139">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="bbcd8-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-140">Click Add.</span></span>
29. <span data-ttu-id="bbcd8-141">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="bbcd8-142">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="bbcd8-143">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="bbcd8-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-144">Click Add.</span></span>
33. <span data-ttu-id="bbcd8-145">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="bbcd8-146">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="bbcd8-147">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="bbcd8-148">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-148">Click Add.</span></span>
37. <span data-ttu-id="bbcd8-149">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="bbcd8-150">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="bbcd8-151">Vælg "Dato" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="bbcd8-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-152">Click Add.</span></span>
41. <span data-ttu-id="bbcd8-153">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="bbcd8-154">Skriv 'Debet' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="bbcd8-155">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="bbcd8-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-156">Click Add.</span></span>
45. <span data-ttu-id="bbcd8-157">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="bbcd8-158">Skriv "Kredit" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="bbcd8-159">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-159">Click Add.</span></span>
48. <span data-ttu-id="bbcd8-160">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="bbcd8-161">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="bbcd8-162">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="bbcd8-163">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-163">Click Add.</span></span>
52. <span data-ttu-id="bbcd8-164">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="bbcd8-165">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="bbcd8-166">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-166">Click Add.</span></span>
55. <span data-ttu-id="bbcd8-167">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="bbcd8-168">Skriv 'Dimensionsdata' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="bbcd8-169">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="bbcd8-170">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-170">Click Add.</span></span>
    * <span data-ttu-id="bbcd8-171">Vi har føjet en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-171">We added to our model a new record list.</span></span> <span data-ttu-id="bbcd8-172">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) værdierne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="bbcd8-173">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens værdier.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="bbcd8-174">Dimensionsnavnet præsenteres også i denne post som et felt, der skal bruges, hvis det er nødvendigt med henblik på valg.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="bbcd8-175">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="bbcd8-176">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="bbcd8-177">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="bbcd8-178">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-178">Click Add.</span></span>
63. <span data-ttu-id="bbcd8-179">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="bbcd8-180">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="bbcd8-181">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-181">Click Add.</span></span>
66. <span data-ttu-id="bbcd8-182">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="bbcd8-183">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="bbcd8-184">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-184">Click Add.</span></span>
69. <span data-ttu-id="bbcd8-185">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-185">Click Save.</span></span>
70. <span data-ttu-id="bbcd8-186">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bbcd8-186">Close the page.</span></span>

