--- 
title: Oprette callcenter-kanaler og definere kanalattributter
description: "Denne procedure gennemgår oprettelse af en ny detailkanal og definition af kanalattributter."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="04d4b-103">Oprette callcenter-kanaler og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="04d4b-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="04d4b-104">Denne procedure gennemgår oprettelse af en ny detailkanal og definition af kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="04d4b-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="04d4b-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="04d4b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="04d4b-106">Denne procedure er beregnet til Retail IT-rollen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="04d4b-107">Opret ny butik</span><span class="sxs-lookup"><span data-stu-id="04d4b-107">Create new store</span></span>
1. <span data-ttu-id="04d4b-108">Gå til Alle arbejdsområder > Installation af kanal.</span><span class="sxs-lookup"><span data-stu-id="04d4b-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="04d4b-109">Klik på Ny kanal.</span><span class="sxs-lookup"><span data-stu-id="04d4b-109">Click New channel.</span></span>
3. <span data-ttu-id="04d4b-110">Klik på Butik.</span><span class="sxs-lookup"><span data-stu-id="04d4b-110">Click Store.</span></span>
4. <span data-ttu-id="04d4b-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="04d4b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="04d4b-112">Skriv en værdi i feltet Butiksnummer.</span><span class="sxs-lookup"><span data-stu-id="04d4b-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="04d4b-113">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="04d4b-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="04d4b-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="04d4b-116">Vælg en indstilling i feltet Lagertidszone.</span><span class="sxs-lookup"><span data-stu-id="04d4b-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="04d4b-117">Klik på rullelisten i feltet Kanalprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="04d4b-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="04d4b-119">Klik på rullelisten i feltet Sprog for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="04d4b-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="04d4b-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="04d4b-122">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="04d4b-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="04d4b-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="04d4b-125">Klik på rullelisten i feltet Kundeadressekartotek for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04d4b-126">Vælg det adressekartotek, der bruges til at knytte kunder til denne butik.</span><span class="sxs-lookup"><span data-stu-id="04d4b-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="04d4b-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="04d4b-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="04d4b-129">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="04d4b-129">Click Select.</span></span>
22. <span data-ttu-id="04d4b-130">Klik på rullelisten i feltet Medarbejderadressekartotek for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04d4b-131">Vælg det adressekartotek, der bruges til at knytte kasserer til denne kanal.</span><span class="sxs-lookup"><span data-stu-id="04d4b-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="04d4b-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="04d4b-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="04d4b-134">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="04d4b-134">Click Select.</span></span>
26. <span data-ttu-id="04d4b-135">Klik på rullelisten i feltet Standardkunde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="04d4b-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="04d4b-137">Udvis eller skjul sektionen Skærmlayout.</span><span class="sxs-lookup"><span data-stu-id="04d4b-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="04d4b-138">Klik på rullelisten i feltet Skærmlayout-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04d4b-139">Vælg standard POS-skærmlayoutet for denne butik.</span><span class="sxs-lookup"><span data-stu-id="04d4b-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="04d4b-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="04d4b-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="04d4b-142">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="04d4b-143">Klik på Kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="04d4b-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="04d4b-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="04d4b-144">Click New.</span></span>
35. <span data-ttu-id="04d4b-145">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="04d4b-146">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="04d4b-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="04d4b-148">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="04d4b-148">Click Save.</span></span>
39. <span data-ttu-id="04d4b-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-149">Close the page.</span></span>
40. <span data-ttu-id="04d4b-150">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="04d4b-151">Klik på Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="04d4b-151">Click Payment methods.</span></span>
42. <span data-ttu-id="04d4b-152">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="04d4b-152">Click New.</span></span>
43. <span data-ttu-id="04d4b-153">Klik på rullelisten i feltet Betalingsmetode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="04d4b-154">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="04d4b-155">Udvid eller skjul sektionen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="04d4b-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="04d4b-156">Angiv de ønskede værdier i feltet Kontonummer.</span><span class="sxs-lookup"><span data-stu-id="04d4b-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="04d4b-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="04d4b-157">Click Save.</span></span>
48. <span data-ttu-id="04d4b-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-158">Close the page.</span></span>
49. <span data-ttu-id="04d4b-159">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="04d4b-160">Klik på Kontantopgørelse.</span><span class="sxs-lookup"><span data-stu-id="04d4b-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="04d4b-161">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="04d4b-161">Click New.</span></span>
52. <span data-ttu-id="04d4b-162">Indtast et tal i feltet Beløb i transaktionsvaluta.</span><span class="sxs-lookup"><span data-stu-id="04d4b-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="04d4b-163">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="04d4b-164">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="04d4b-165">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="04d4b-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="04d4b-166">Click Save.</span></span>
57. <span data-ttu-id="04d4b-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-167">Close the page.</span></span>
58. <span data-ttu-id="04d4b-168">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="04d4b-169">Klik på Tildeling af butikssøgergruppe.</span><span class="sxs-lookup"><span data-stu-id="04d4b-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="04d4b-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="04d4b-170">Click New.</span></span>
61. <span data-ttu-id="04d4b-171">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="04d4b-172">Klik på rullelisten i feltet Søgegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="04d4b-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="04d4b-173">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="04d4b-174">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="04d4b-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="04d4b-175">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="04d4b-175">Click Save.</span></span>
66. <span data-ttu-id="04d4b-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="04d4b-176">Close the page.</span></span>


