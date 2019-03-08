---
title: Oprette posteringsprofiler for anlægsaktiver
description: Denne opgaveguide konfigurerer posteringsprofiler for bogføring af anlægsaktiver.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "351096"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="fed77-103">Oprette posteringsprofiler for anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="fed77-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fed77-104">Denne opgaveguide konfigurerer posteringsprofiler for bogføring af anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="fed77-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="fed77-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="fed77-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="fed77-106">Eksemplerne i opgaveguiden er for en grundlæggende posteringsprofil, men posteringsprofiler skal oprettes for din specifikke kontoplan og krav til finansiel rapportering.</span><span class="sxs-lookup"><span data-stu-id="fed77-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="fed77-107">Gå til Anlægsaktiver > Opsætning > Posteringsprofiler for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="fed77-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="fed77-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fed77-108">Click New.</span></span>
3. <span data-ttu-id="fed77-109">Skriv en værdi i feltet Posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="fed77-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="fed77-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fed77-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fed77-111">Du skal oprette en posteringsprofil til hver transaktionstype for anlægsaktiver, som du vil bruge, når du arbejder med anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="fed77-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="fed77-112">Denne opgaveguide starter med transaktionstypen Anskaffelse.</span><span class="sxs-lookup"><span data-stu-id="fed77-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="fed77-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-113">Click Add.</span></span>
6. <span data-ttu-id="fed77-114">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fed77-115">I feltet Grupperinger kan du definere posteringsprofilen ned til tabellen (én konto konfigureret for hvert anlægsaktiv) eller gruppe (én konto konfigureret for hver anlægsaktivgruppe).</span><span class="sxs-lookup"><span data-stu-id="fed77-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="fed77-116">Til denne opgaveguide er værdien angivet til "Alle" for at gælde for alle anlægsaktiver med den angivne bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="fed77-117">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fed77-118">Du kan for Anskaffelser angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.</span><span class="sxs-lookup"><span data-stu-id="fed77-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="fed77-119">Vælg "Anskaffelsesregulering" i feltet Transaktionstype.</span><span class="sxs-lookup"><span data-stu-id="fed77-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="fed77-120">Til posteringer til anskaffelsesreguleringer bruger vi de samme konti som anvendt til anskaffelsesposteringer.</span><span class="sxs-lookup"><span data-stu-id="fed77-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="fed77-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-121">Click Add.</span></span>
10. <span data-ttu-id="fed77-122">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="fed77-123">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fed77-124">Du kan for anskaffelsesreguleringer angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.</span><span class="sxs-lookup"><span data-stu-id="fed77-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="fed77-125">Vælg "Afskrivning" i feltet Transaktionstype.</span><span class="sxs-lookup"><span data-stu-id="fed77-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="fed77-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-126">Click Add.</span></span>
14. <span data-ttu-id="fed77-127">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="fed77-128">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="fed77-129">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="fed77-130">Vælg "Afskrivningsregulering" i feltet Transaktionstype.</span><span class="sxs-lookup"><span data-stu-id="fed77-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="fed77-131">Til posteringer til afskrivningsreguleringer bruger vi de samme konti som anvendt til afskrivningsposteringer.</span><span class="sxs-lookup"><span data-stu-id="fed77-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="fed77-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-132">Click Add.</span></span>
19. <span data-ttu-id="fed77-133">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="fed77-134">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="fed77-135">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="fed77-136">Vælg "Kassation – salg" i feltet Transaktionstype.</span><span class="sxs-lookup"><span data-stu-id="fed77-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="fed77-137">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-137">Click Add.</span></span>
24. <span data-ttu-id="fed77-138">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="fed77-139">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fed77-140">Du kan for Kassation angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.</span><span class="sxs-lookup"><span data-stu-id="fed77-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="fed77-141">Vælg "Kassation – spild" i feltet Transaktionstype.</span><span class="sxs-lookup"><span data-stu-id="fed77-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="fed77-142">Vi bruger de samme konti til kassation-salg og kassation-spild.</span><span class="sxs-lookup"><span data-stu-id="fed77-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="fed77-143">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-143">Click Add.</span></span>
28. <span data-ttu-id="fed77-144">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="fed77-145">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fed77-146">Du kan for Kassation angive en modkonto eller lade det stå tomt, så det udfyldes for den specifikke transaktion.</span><span class="sxs-lookup"><span data-stu-id="fed77-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="fed77-147">Udvid sektionen Kassation.</span><span class="sxs-lookup"><span data-stu-id="fed77-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="fed77-148">Du skal konfigurere posteringsprofiler for både salg og skrot.</span><span class="sxs-lookup"><span data-stu-id="fed77-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="fed77-149">Vi starter med salgstransaktioner for kassation.</span><span class="sxs-lookup"><span data-stu-id="fed77-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="fed77-150">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-150">Click Add.</span></span>
32. <span data-ttu-id="fed77-151">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="fed77-152">Vælg "Anskaffelsesværdi" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="fed77-153">Anskaffelsesværdi håndterer anskaffelse og anskaffelsesreguleringsværdier for alle år.</span><span class="sxs-lookup"><span data-stu-id="fed77-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="fed77-154">Du kan også definere konti for disse posteringstyper separat.</span><span class="sxs-lookup"><span data-stu-id="fed77-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="fed77-155">Du kan angive, at kassationsprocessen skal bruge forskellige konti, afhængigt af om kassationen resulterer i tab eller vinding.</span><span class="sxs-lookup"><span data-stu-id="fed77-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="fed77-156">Jeg vil angive værditypen til "Alle" for at bruge de samme konti til alle former for kassation.</span><span class="sxs-lookup"><span data-stu-id="fed77-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="fed77-157">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="fed77-158">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="fed77-159">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-159">Click Add.</span></span>
37. <span data-ttu-id="fed77-160">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fed77-161">Vælg "Afskrivning (foregående år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="fed77-162">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="fed77-163">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="fed77-164">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-164">Click Add.</span></span>
41. <span data-ttu-id="fed77-165">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="fed77-166">Vælg "Afskrivning (indeværende år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="fed77-167">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="fed77-168">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="fed77-169">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-169">Click Add.</span></span>
46. <span data-ttu-id="fed77-170">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="fed77-171">Vælg "Reguleringer af afskrivning (foregående år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="fed77-172">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="fed77-173">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="fed77-174">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-174">Click Add.</span></span>
51. <span data-ttu-id="fed77-175">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="fed77-176">Vælg "Reguleringer af afskrivning (indeværende år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="fed77-177">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="fed77-178">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="fed77-179">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-179">Click Add.</span></span>
56. <span data-ttu-id="fed77-180">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="fed77-181">Vælg "Bogført nettoværdi" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="fed77-182">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="fed77-183">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="fed77-184">Vælg "Spild" i feltet Salg eller spild.</span><span class="sxs-lookup"><span data-stu-id="fed77-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="fed77-185">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-185">Click Add.</span></span>
62. <span data-ttu-id="fed77-186">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="fed77-187">Vælg "Anskaffelsesværdi" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="fed77-188">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="fed77-189">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="fed77-190">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-190">Click Add.</span></span>
67. <span data-ttu-id="fed77-191">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fed77-192">Vælg "Afskrivning (foregående år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="fed77-193">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="fed77-194">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="fed77-195">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-195">Click Add.</span></span>
71. <span data-ttu-id="fed77-196">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="fed77-197">Vælg "Afskrivning (indeværende år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="fed77-198">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="fed77-199">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="fed77-200">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-200">Click Add.</span></span>
76. <span data-ttu-id="fed77-201">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="fed77-202">Vælg "Reguleringer af afskrivning (foregående år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="fed77-203">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="fed77-204">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="fed77-205">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-205">Click Add.</span></span>
81. <span data-ttu-id="fed77-206">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="fed77-207">Vælg "Reguleringer af afskrivning (indeværende år)" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="fed77-208">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="fed77-209">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="fed77-210">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fed77-210">Click Add.</span></span>
86. <span data-ttu-id="fed77-211">Indtast eller vælg en værdi i feltet Bog.</span><span class="sxs-lookup"><span data-stu-id="fed77-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="fed77-212">Vælg "Bogført nettoværdi" i feltet Bogfør værdi.</span><span class="sxs-lookup"><span data-stu-id="fed77-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="fed77-213">Angive de ønskede værdier i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="fed77-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="fed77-214">I feltet Modkonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="fed77-214">In the Offset account field, specify the desired values.</span></span>

