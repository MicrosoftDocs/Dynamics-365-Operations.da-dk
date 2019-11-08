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
ms.openlocfilehash: 92481749fa15d8a9c273edf6a79ee9fcfdc722e7
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550665"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="138ec-103">ER Bruge økonomiske dimensioner som en datakilde (del 1: Design datamodel)</span><span class="sxs-lookup"><span data-stu-id="138ec-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="138ec-104">Følgende trin beskriver, hvordan en systemadministrator eller udvikler til elektronisk rapportering kan konfigurere en model for elektronisk rapportering (ER) til at bruge økonomiske dimensioner so datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="138ec-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="138ec-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="138ec-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="138ec-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="138ec-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="138ec-107">Opret en ny datamodel</span><span class="sxs-lookup"><span data-stu-id="138ec-107">Create a new data model</span></span>
1. <span data-ttu-id="138ec-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="138ec-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="138ec-109">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="138ec-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="138ec-110">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="138ec-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="138ec-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="138ec-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="138ec-112">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="138ec-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="138ec-113">Skriv 'Eksempelmodel til økonomiske dimensioner' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="138ec-114">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="138ec-114">Click Create configuration.</span></span>
6. <span data-ttu-id="138ec-115">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="138ec-115">Click Designer.</span></span>
7. <span data-ttu-id="138ec-116">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="138ec-117">Skriv 'Post' et navn i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="138ec-118">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-118">Click Add.</span></span>
10. <span data-ttu-id="138ec-119">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="138ec-120">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="138ec-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-121">Click Add.</span></span>
    * <span data-ttu-id="138ec-122">Vi vil føje en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="138ec-122">We will add to our model a new record list.</span></span> <span data-ttu-id="138ec-123">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) indstillingerne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="138ec-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="138ec-124">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens indstilling.</span><span class="sxs-lookup"><span data-stu-id="138ec-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="138ec-125">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="138ec-126">Skriv 'Dimensionsindstilling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="138ec-127">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="138ec-128">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-128">Click Add.</span></span>
17. <span data-ttu-id="138ec-129">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="138ec-130">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="138ec-131">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="138ec-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-132">Click Add.</span></span>
21. <span data-ttu-id="138ec-133">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="138ec-134">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="138ec-135">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-135">Click Add.</span></span>
24. <span data-ttu-id="138ec-136">Vælg 'Post' i træet.</span><span class="sxs-lookup"><span data-stu-id="138ec-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="138ec-137">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="138ec-138">Skriv 'Journal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="138ec-139">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="138ec-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-140">Click Add.</span></span>
29. <span data-ttu-id="138ec-141">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="138ec-142">Skriv 'Batch' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="138ec-143">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="138ec-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-144">Click Add.</span></span>
33. <span data-ttu-id="138ec-145">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="138ec-146">Skriv "Transaktion" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="138ec-147">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="138ec-148">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-148">Click Add.</span></span>
37. <span data-ttu-id="138ec-149">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="138ec-150">Skriv 'Dato' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="138ec-151">Vælg "Dato" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="138ec-152">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-152">Click Add.</span></span>
41. <span data-ttu-id="138ec-153">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="138ec-154">Skriv 'Debet' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="138ec-155">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="138ec-156">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-156">Click Add.</span></span>
45. <span data-ttu-id="138ec-157">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="138ec-158">Skriv "Kredit" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="138ec-159">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-159">Click Add.</span></span>
48. <span data-ttu-id="138ec-160">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="138ec-161">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="138ec-162">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="138ec-163">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-163">Click Add.</span></span>
52. <span data-ttu-id="138ec-164">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="138ec-165">Skriv 'Bilag' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="138ec-166">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-166">Click Add.</span></span>
55. <span data-ttu-id="138ec-167">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="138ec-168">Skriv 'Dimensionsdata' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="138ec-169">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="138ec-170">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-170">Click Add.</span></span>
    * <span data-ttu-id="138ec-171">Vi har føjet en ny liste over poster til vores model.</span><span class="sxs-lookup"><span data-stu-id="138ec-171">We added to our model a new record list.</span></span> <span data-ttu-id="138ec-172">Denne liste viser (for alle ER-rapporter, der bruger denne model som datakilde) værdierne for den valgte økonomiske dimension.</span><span class="sxs-lookup"><span data-stu-id="138ec-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="138ec-173">Hver økonomisk dimension præsenteres på denne liste som en post med relevante felter, der repræsenterer dimensionens værdier.</span><span class="sxs-lookup"><span data-stu-id="138ec-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="138ec-174">Dimensionsnavnet præsenteres også i denne post som et felt, der skal bruges, hvis det er nødvendigt med henblik på valg.</span><span class="sxs-lookup"><span data-stu-id="138ec-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="138ec-175">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="138ec-176">Skriv 'Kode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="138ec-177">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="138ec-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="138ec-178">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-178">Click Add.</span></span>
63. <span data-ttu-id="138ec-179">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="138ec-180">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="138ec-181">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-181">Click Add.</span></span>
66. <span data-ttu-id="138ec-182">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="138ec-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="138ec-183">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="138ec-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="138ec-184">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="138ec-184">Click Add.</span></span>
69. <span data-ttu-id="138ec-185">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="138ec-185">Click Save.</span></span>
70. <span data-ttu-id="138ec-186">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="138ec-186">Close the page.</span></span>

