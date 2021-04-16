---
title: Definere revisionspolitikker for kildedokumenter
description: Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836955"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="2feb1-103">Definere revisionspolitikker for kildedokumenter</span><span class="sxs-lookup"><span data-stu-id="2feb1-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2feb1-104">Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.</span><span class="sxs-lookup"><span data-stu-id="2feb1-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="2feb1-105">I eksemplet bruges udgiftsrapporter med udgiftstypen hotel.</span><span class="sxs-lookup"><span data-stu-id="2feb1-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="2feb1-106">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="2feb1-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="2feb1-107">Rollen revisor indeholder de korrekte tilladelser til at kunne udføre disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="2feb1-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="2feb1-108">Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="2feb1-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-109">Select **New**.</span></span>
3. <span data-ttu-id="2feb1-110">Skriv en værdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="2feb1-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="2feb1-112">Vælg **Udgiftsrapportlinje** i feltet **Forespørgselsnavn**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="2feb1-113">Vælg **Aggreger** i Feltet **Forespørgselstype**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="2feb1-114">Vælg **Juridisk enhed** i feltet **Juridisk enhed**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="2feb1-115">Vælg **Dato og klokkeslæt for ændring** i feltet **Dokumentdatohenvisning**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="2feb1-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-116">Select **Save**.</span></span>
10. <span data-ttu-id="2feb1-117">Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Overvågningspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="2feb1-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-118">Select **New**.</span></span>
12. <span data-ttu-id="2feb1-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="2feb1-120">Udvid sektionen **Regelstyrede organisationer**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="2feb1-121">Vælg **Contoso Entertainment System USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="2feb1-122">Vælg **Contoso Consulting USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="2feb1-123">Vælg **Contoso Retail USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="2feb1-124">Skjul sektionen **Regelstyrede organisationer**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="2feb1-125">Udvid sektionen **Regler**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="2feb1-126">Find og vælg den Politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="2feb1-127">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="2feb1-128">Angiv en dato og et klokkeslæt i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="2feb1-129">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-129">Select **Filter**.</span></span>
23. <span data-ttu-id="2feb1-130">Vælg rækken for **Udgiftsart** på listen, og angiv detaljerne til **Hotel**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="2feb1-131">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="2feb1-132">Vælg fanen **Aggregering**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="2feb1-133">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-133">Select **Add**.</span></span>
27. <span data-ttu-id="2feb1-134">Vælg feltværdien **Transaktionsbeløb** på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="2feb1-135">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="2feb1-136">Vælg **Sum** i feltet **Aggregeringsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="2feb1-137">Vælg fanen **Sammenlæg pr.**</span><span class="sxs-lookup"><span data-stu-id="2feb1-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="2feb1-138">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-138">Select **Add**.</span></span>
32. <span data-ttu-id="2feb1-139">Vælg værdien af **Medarbejder** på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="2feb1-140">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-140">Select **Add**.</span></span>
34. <span data-ttu-id="2feb1-141">Vælg værdien af **Udgiftsart** på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="2feb1-142">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="2feb1-143">Vælg fanen **Har**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="2feb1-144">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-144">Select **Add**.</span></span>
38. <span data-ttu-id="2feb1-145">Vælg **Transaktionsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="2feb1-146">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="2feb1-147">Vælg **Sum** i feltet **Aggregeringsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="2feb1-148">Skriv `>2000` i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="2feb1-149">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-149">Select **OK**.</span></span>
43. <span data-ttu-id="2feb1-150">Vælg **Test**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-150">Select **Test**.</span></span>
44. <span data-ttu-id="2feb1-151">Angiv en dato og klokkeslæt i feltet **Startdato for dokumentudvælgelse**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="2feb1-152">Angiv en dato og klokkeslæt i feltet **Slutdato for dokumentudvælgelse**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="2feb1-153">Vælg **Kør test**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-153">Select **Run test**.</span></span>
47. <span data-ttu-id="2feb1-154">Vælg **Overvågningspolitik** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2feb1-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="2feb1-155">Vælge **Flere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="2feb1-156">Angiv en dato og et klokkeslæt i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="2feb1-157">Angiv en dato og et klokkeslæt i feltet **Slutdato**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="2feb1-158">Vælg **Batch**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-158">Select **Batch**.</span></span>
52. <span data-ttu-id="2feb1-159">Udvid sektionen **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="2feb1-160">Vælg **Ja** i feltet **Batchbehandling**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="2feb1-161">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-161">Select **OK**.</span></span>
55. <span data-ttu-id="2feb1-162">Gå i navigationsruden til **Moduler > Revisionspanel > Overvåg sager**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="2feb1-163">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="2feb1-164">Udvid sektionen **Tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="2feb1-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="2feb1-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="2feb1-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]