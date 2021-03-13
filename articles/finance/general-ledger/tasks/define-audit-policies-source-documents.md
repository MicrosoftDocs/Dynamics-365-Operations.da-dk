---
title: Definere revisionspolitikker for kildedokumenter
description: Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.
author: panolte
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e020a9e82ff18055e40e3e0ddc7bbed1068c886c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021423"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="4ccff-103">Definere revisionspolitikker for kildedokumenter</span><span class="sxs-lookup"><span data-stu-id="4ccff-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ccff-104">Dette emne viser, hvordan du kan konfigurere og køre regler for overvågningspolitik.</span><span class="sxs-lookup"><span data-stu-id="4ccff-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="4ccff-105">I eksemplet bruges udgiftsrapporter med udgiftstypen hotel.</span><span class="sxs-lookup"><span data-stu-id="4ccff-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="4ccff-106">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="4ccff-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="4ccff-107">Rollen revisor indeholder de korrekte tilladelser til at kunne udføre disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="4ccff-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="4ccff-108">Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="4ccff-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-109">Select **New**.</span></span>
3. <span data-ttu-id="4ccff-110">Skriv en værdi i feltet **Regelnavn**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="4ccff-111">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="4ccff-112">Vælg **Udgiftsrapportlinje** i feltet **Forespørgselsnavn**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="4ccff-113">Vælg **Aggreger** i Feltet **Forespørgselstype**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="4ccff-114">Vælg **Juridisk enhed** i feltet **Juridisk enhed**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="4ccff-115">Vælg **Dato og klokkeslæt for ændring** i feltet **Dokumentdatohenvisning**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="4ccff-116">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-116">Select **Save**.</span></span>
10. <span data-ttu-id="4ccff-117">Gå i navigationsruden til **Moduler > Revisionspanel > Opsætning > Overvågningspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="4ccff-118">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-118">Select **New**.</span></span>
12. <span data-ttu-id="4ccff-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="4ccff-120">Udvid sektionen **Regelstyrede organisationer**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="4ccff-121">Vælg **Contoso Entertainment System USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="4ccff-122">Vælg **Contoso Consulting USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="4ccff-123">Vælg **Contoso Retail USA** i træet, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="4ccff-124">Skjul sektionen **Regelstyrede organisationer**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="4ccff-125">Udvid sektionen **Regler**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="4ccff-126">Find og vælg den Politikregel, som blev oprettet tidligere, på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="4ccff-127">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="4ccff-128">Angiv en dato og et klokkeslæt i feltet **Ikrafttrædelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="4ccff-129">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-129">Select **Filter**.</span></span>
23. <span data-ttu-id="4ccff-130">Vælg rækken for **Udgiftsart** på listen, og angiv detaljerne til **Hotel**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="4ccff-131">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="4ccff-132">Vælg fanen **Aggregering**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="4ccff-133">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-133">Select **Add**.</span></span>
27. <span data-ttu-id="4ccff-134">Vælg feltværdien **Transaktionsbeløb** på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="4ccff-135">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="4ccff-136">Vælg **Sum** i feltet **Aggregeringsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="4ccff-137">Vælg fanen **Sammenlæg pr.**</span><span class="sxs-lookup"><span data-stu-id="4ccff-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="4ccff-138">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-138">Select **Add**.</span></span>
32. <span data-ttu-id="4ccff-139">Vælg værdien af **Medarbejder** på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="4ccff-140">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-140">Select **Add**.</span></span>
34. <span data-ttu-id="4ccff-141">Vælg værdien af **Udgiftsart** på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="4ccff-142">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="4ccff-143">Vælg fanen **Har**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="4ccff-144">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-144">Select **Add**.</span></span>
38. <span data-ttu-id="4ccff-145">Vælg **Transaktionsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="4ccff-146">Indtast eller vælg en værdi i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="4ccff-147">Vælg **Sum** i feltet **Aggregeringsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="4ccff-148">Skriv `>2000` i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="4ccff-149">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-149">Select **OK**.</span></span>
43. <span data-ttu-id="4ccff-150">Vælg **Test**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-150">Select **Test**.</span></span>
44. <span data-ttu-id="4ccff-151">Angiv en dato og klokkeslæt i feltet **Startdato for dokumentudvælgelse**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="4ccff-152">Angiv en dato og klokkeslæt i feltet **Slutdato for dokumentudvælgelse**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="4ccff-153">Vælg **Kør test**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-153">Select **Run test**.</span></span>
47. <span data-ttu-id="4ccff-154">Vælg **Overvågningspolitik** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4ccff-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="4ccff-155">Vælge **Flere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="4ccff-156">Angiv en dato og et klokkeslæt i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="4ccff-157">Angiv en dato og et klokkeslæt i feltet **Slutdato**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="4ccff-158">Vælg **Batch**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-158">Select **Batch**.</span></span>
52. <span data-ttu-id="4ccff-159">Udvid sektionen **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="4ccff-160">Vælg **Ja** i feltet **Batchbehandling**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="4ccff-161">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-161">Select **OK**.</span></span>
55. <span data-ttu-id="4ccff-162">Gå i navigationsruden til **Moduler > Revisionspanel > Overvåg sager**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="4ccff-163">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="4ccff-164">Udvid sektionen **Tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="4ccff-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="4ccff-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4ccff-165">In the list, find and select the desired record.</span></span>

