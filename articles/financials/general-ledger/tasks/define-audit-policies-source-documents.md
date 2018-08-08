--- 
title: Definere revisionspolitikker for kildedokumenter
description: "Denne procedure viser, hvordan du kan konfigurere og køre regler for overvågningspolitik."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1bcea6257447cc1d1532f30acc2fb6bb4d524810
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="59462-103">Definere revisionspolitikker for kildedokumenter</span><span class="sxs-lookup"><span data-stu-id="59462-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59462-104">Denne procedure viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.</span><span class="sxs-lookup"><span data-stu-id="59462-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="59462-105">I eksemplet bruges udgiftsrapporter med udgiftstypen hotel.</span><span class="sxs-lookup"><span data-stu-id="59462-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="59462-106">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="59462-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="59462-107">Rollen revisor indeholder de korrekte tilladelser til at kunne udføre disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="59462-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="59462-108">Gå til Revisionspanel > Opsætning > Politikregeltype.</span><span class="sxs-lookup"><span data-stu-id="59462-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="59462-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="59462-109">Click New.</span></span>
3. <span data-ttu-id="59462-110">Skriv en værdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="59462-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="59462-111">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="59462-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="59462-112">Vælg Udgiftsrapportlinje i feltet Forespørgselsnavn.</span><span class="sxs-lookup"><span data-stu-id="59462-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="59462-113">Vælg Aggregér i forespørgselstypefeltet</span><span class="sxs-lookup"><span data-stu-id="59462-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="59462-114">Vælg Juridisk enhed i feltet Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="59462-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="59462-115">Vælg Dato og klokkeslæt for ændring i feltet Dokumentdatohenvisning</span><span class="sxs-lookup"><span data-stu-id="59462-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="59462-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="59462-116">Click Save.</span></span>
10. <span data-ttu-id="59462-117">Gå til Revisionspanel > Opsætning > Overvågningspolitikker.</span><span class="sxs-lookup"><span data-stu-id="59462-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="59462-118">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="59462-118">Click New.</span></span>
12. <span data-ttu-id="59462-119">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="59462-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="59462-120">Udvid sektionen Politikorganisationer.</span><span class="sxs-lookup"><span data-stu-id="59462-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="59462-121">Vælg "Contoso Entertainment System USA" i træet.</span><span class="sxs-lookup"><span data-stu-id="59462-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="59462-122">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-122">Click Add.</span></span>
16. <span data-ttu-id="59462-123">Vælg "Contoso Consulting USA" i træet'.</span><span class="sxs-lookup"><span data-stu-id="59462-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="59462-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-124">Click Add.</span></span>
18. <span data-ttu-id="59462-125">Vælg "Contoso Retail USA" i træet'.</span><span class="sxs-lookup"><span data-stu-id="59462-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="59462-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-126">Click Add.</span></span>
20. <span data-ttu-id="59462-127">Skjul sektionen Politikorganisationer.</span><span class="sxs-lookup"><span data-stu-id="59462-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="59462-128">Udvid sektionen Politikregler.</span><span class="sxs-lookup"><span data-stu-id="59462-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="59462-129">Find og vælg den Politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="59462-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="59462-130">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="59462-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="59462-131">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="59462-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="59462-132">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="59462-132">Click Filter.</span></span>
26. <span data-ttu-id="59462-133">Vælg rækken for Udgiftsart på listen, og angiv detaljerne til Hotel</span><span class="sxs-lookup"><span data-stu-id="59462-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="59462-134">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="59462-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="59462-135">Klik på fanen Aggregér.</span><span class="sxs-lookup"><span data-stu-id="59462-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="59462-136">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-136">Click Add.</span></span>
30. <span data-ttu-id="59462-137">Vælg feltværdien Transaktionsbeløb på listen</span><span class="sxs-lookup"><span data-stu-id="59462-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="59462-138">Indtast eller vælg en værdi i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="59462-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="59462-139">Vælg "Sum"i feltet Aggregeringsfunktion.</span><span class="sxs-lookup"><span data-stu-id="59462-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="59462-140">Klik på fanen Gruppér efter.</span><span class="sxs-lookup"><span data-stu-id="59462-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="59462-141">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-141">Click Add.</span></span>
35. <span data-ttu-id="59462-142">Vælg værdien Medarbejder på listen </span><span class="sxs-lookup"><span data-stu-id="59462-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="59462-143">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-143">Click Add.</span></span>
37. <span data-ttu-id="59462-144">Vælg værdien Udgiftsart på listen</span><span class="sxs-lookup"><span data-stu-id="59462-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="59462-145">Indtast eller vælg en værdi i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="59462-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="59462-146">Klik på fanen Har.</span><span class="sxs-lookup"><span data-stu-id="59462-146">Click the Having tab.</span></span>
40. <span data-ttu-id="59462-147">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="59462-147">Click Add.</span></span>
41. <span data-ttu-id="59462-148">Vælg Transaktionsbeløb</span><span class="sxs-lookup"><span data-stu-id="59462-148">Select Transaction amount</span></span>
42. <span data-ttu-id="59462-149">Indtast eller vælg en værdi i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="59462-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="59462-150">Vælg "Sum"i feltet Aggregeringsfunktion.</span><span class="sxs-lookup"><span data-stu-id="59462-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="59462-151">Skriv ">2000" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="59462-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="59462-152">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="59462-152">Click OK.</span></span>
46. <span data-ttu-id="59462-153">Klik på Test.</span><span class="sxs-lookup"><span data-stu-id="59462-153">Click Test.</span></span>
47. <span data-ttu-id="59462-154">Angiv en dato og klokkeslæt i feltet Startdato for dokumentudvælgelse.</span><span class="sxs-lookup"><span data-stu-id="59462-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="59462-155">Angiv en dato og klokkeslæt i feltet Slutdato for dokumentudvælgelse.</span><span class="sxs-lookup"><span data-stu-id="59462-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="59462-156">Klik på Kør test.</span><span class="sxs-lookup"><span data-stu-id="59462-156">Click Run test.</span></span>
50. <span data-ttu-id="59462-157">Klik på Overvågningspolitik i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="59462-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="59462-158">Klik på Flere indstillinger.</span><span class="sxs-lookup"><span data-stu-id="59462-158">Click Additional options.</span></span>
52. <span data-ttu-id="59462-159">Angiv en dato og et klokkeslæt i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="59462-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="59462-160">Angiv en dato og et klokkeslæt i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="59462-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="59462-161">Klik på Batch.</span><span class="sxs-lookup"><span data-stu-id="59462-161">Click Batch.</span></span>
55. <span data-ttu-id="59462-162">Udvid sektionen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="59462-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="59462-163">Vælg Ja i feltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="59462-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="59462-164">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="59462-164">Click OK.</span></span>
58. <span data-ttu-id="59462-165">Gå til Revisionspanel > Overvåg sager.</span><span class="sxs-lookup"><span data-stu-id="59462-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="59462-166">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="59462-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="59462-167">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="59462-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="59462-168">Udvid sektionen Tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="59462-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="59462-169">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="59462-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="59462-170">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="59462-170">In the list, click the link in the selected row.</span></span>


