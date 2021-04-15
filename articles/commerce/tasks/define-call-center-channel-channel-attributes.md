---
title: Oprette callcenter-kanaler og definere kanalattributter
description: Denne procedure gennemgår oprettelse af en ny kanal og definition af kanalattributter.
author: mugunthanm
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b053ea3a5792d016cfe4850f07c65de97fbfc9e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802689"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="d7a5e-103">Oprette callcenter-kanaler og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="d7a5e-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7a5e-104">Denne procedure gennemgår oprettelse af en ny handelskanal og definition af kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="d7a5e-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="d7a5e-106">Denne procedure er beregnet til Commerce IT-rollen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="d7a5e-107">Opret ny butik</span><span class="sxs-lookup"><span data-stu-id="d7a5e-107">Create new store</span></span>
1. <span data-ttu-id="d7a5e-108">Gå til Alle arbejdsområder > Installation af kanal.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="d7a5e-109">Klik på Ny kanal.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-109">Click New channel.</span></span>
3. <span data-ttu-id="d7a5e-110">Klik på Butik.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-110">Click Store.</span></span>
4. <span data-ttu-id="d7a5e-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d7a5e-112">Skriv en værdi i feltet Butiksnummer.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="d7a5e-113">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d7a5e-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d7a5e-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d7a5e-116">Vælg en indstilling i feltet Lagertidszone.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="d7a5e-117">Klik på rullelisten i feltet Kanalprofil for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d7a5e-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d7a5e-119">Klik på rullelisten i feltet Sprog for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="d7a5e-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d7a5e-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d7a5e-122">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d7a5e-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="d7a5e-124">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d7a5e-125">Klik på rullelisten i feltet Kundeadressekartotek for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d7a5e-126">Vælg det adressekartotek, der bruges til at knytte kunder til denne butik.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="d7a5e-127">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="d7a5e-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="d7a5e-129">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-129">Click Select.</span></span>
22. <span data-ttu-id="d7a5e-130">Klik på rullelisten i feltet Medarbejderadressekartotek for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d7a5e-131">Vælg det adressekartotek, der bruges til at knytte kasserer til denne kanal.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="d7a5e-132">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="d7a5e-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="d7a5e-134">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-134">Click Select.</span></span>
26. <span data-ttu-id="d7a5e-135">Klik på rullelisten i feltet Standardkunde for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="d7a5e-136">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="d7a5e-137">Udvis eller skjul sektionen Skærmlayout.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="d7a5e-138">Klik på rullelisten i feltet Skærmlayout-id for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d7a5e-139">Vælg standard POS-skærmlayoutet for denne butik.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="d7a5e-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="d7a5e-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="d7a5e-142">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="d7a5e-143">Klik på Kanalattributter.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="d7a5e-144">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-144">Click New.</span></span>
35. <span data-ttu-id="d7a5e-145">Klik på rullelisten i feltet Navn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="d7a5e-146">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="d7a5e-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="d7a5e-148">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-148">Click Save.</span></span>
39. <span data-ttu-id="d7a5e-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-149">Close the page.</span></span>
40. <span data-ttu-id="d7a5e-150">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="d7a5e-151">Klik på Betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-151">Click Payment methods.</span></span>
42. <span data-ttu-id="d7a5e-152">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-152">Click New.</span></span>
43. <span data-ttu-id="d7a5e-153">Klik på rullelisten i feltet Betalingsmetode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="d7a5e-154">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="d7a5e-155">Udvid eller skjul sektionen Bogføring.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="d7a5e-156">Angiv de ønskede værdier i feltet Kontonummer.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="d7a5e-157">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-157">Click Save.</span></span>
48. <span data-ttu-id="d7a5e-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-158">Close the page.</span></span>
49. <span data-ttu-id="d7a5e-159">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="d7a5e-160">Klik på Kontantopgørelse.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="d7a5e-161">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-161">Click New.</span></span>
52. <span data-ttu-id="d7a5e-162">Indtast et tal i feltet Beløb i transaktionsvaluta.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="d7a5e-163">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="d7a5e-164">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="d7a5e-165">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="d7a5e-166">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-166">Click Save.</span></span>
57. <span data-ttu-id="d7a5e-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-167">Close the page.</span></span>
58. <span data-ttu-id="d7a5e-168">Klik på Konfigurer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="d7a5e-169">Klik på Tildeling af butikssøgergruppe.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="d7a5e-170">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-170">Click New.</span></span>
61. <span data-ttu-id="d7a5e-171">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="d7a5e-172">Klik på rullelisten i feltet Søgegruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="d7a5e-173">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="d7a5e-174">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="d7a5e-175">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-175">Click Save.</span></span>
66. <span data-ttu-id="d7a5e-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d7a5e-176">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]