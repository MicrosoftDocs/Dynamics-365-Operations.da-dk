--- 
title: Oprette en ER-formatkonfiguration (november 2016)
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="9dd2e-103">Oprette en ER-formatkonfiguration (november 2016)</span><span class="sxs-lookup"><span data-stu-id="9dd2e-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9dd2e-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="9dd2e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="9dd2e-105">Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="9dd2e-106">I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".</span><span class="sxs-lookup"><span data-stu-id="9dd2e-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="9dd2e-107">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9dd2e-107">Create a new format configuration</span></span>
1. <span data-ttu-id="9dd2e-108">Gå til **Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="9dd2e-109">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="9dd2e-110">Vælg **Betalinger (forenklet mode)** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="9dd2e-111">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="9dd2e-112">Hvis du ikke kan se **Opret konfiguration**, skal du aktivere designtilstand på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="9dd2e-113">Skriv **Format baseret på datamodel PaymentModel** i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="9dd2e-114">Skriv **BACS (UK-fiktiv)** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="9dd2e-115">Skriv **BACS kreditorbetalingsformat (UK-fiktiv)** i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="9dd2e-116">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="9dd2e-117">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9dd2e-118">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="9dd2e-119">Du kan definere et bestemt format for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="9dd2e-120">Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="9dd2e-121">Indtast eller vælg en værdi i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="9dd2e-122">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-122">Click **Create configuration**.</span></span> <span data-ttu-id="9dd2e-123">En ny konfiguration er oprettet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-123">A new configuration has been created.</span></span> <span data-ttu-id="9dd2e-124">Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="9dd2e-125">Hvis du ikke kan se **Opret konfiguration**, skal du aktivere designtilstand på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="9dd2e-126">Designformatet for et elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="9dd2e-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="9dd2e-127">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-127">Click **Designer**.</span></span>
2. <span data-ttu-id="9dd2e-128">Klik på **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="9dd2e-129">Vælg **Common\File** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="9dd2e-130">Skriv **Xml** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="9dd2e-131">Skriv **UTF-8** i feltet **Kodning**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="9dd2e-132">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-132">Click **OK**.</span></span>
7. <span data-ttu-id="9dd2e-133">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-133">Click **Add**.</span></span>
8. <span data-ttu-id="9dd2e-134">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="9dd2e-135">Skriv **Meddelelse** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="9dd2e-136">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-136">Click **OK**.</span></span>
11. <span data-ttu-id="9dd2e-137">Vælg **Xml\Meddelelse** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="9dd2e-138">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="9dd2e-139">Skriv **ProcessingDate** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="9dd2e-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-140">Click **OK**.</span></span>
15. <span data-ttu-id="9dd2e-141">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="9dd2e-142">Skriv **MessageId** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="9dd2e-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-143">Click **OK**.</span></span>
18. <span data-ttu-id="9dd2e-144">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="9dd2e-145">Skriv **Betalinger** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="9dd2e-146">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-146">Click **OK**.</span></span>
21. <span data-ttu-id="9dd2e-147">Vælg **Xml\Meddelelse\Betalinger** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="9dd2e-148">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="9dd2e-149">Skriv **Vare** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="9dd2e-150">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-150">Click **OK**.</span></span>
25. <span data-ttu-id="9dd2e-151">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="9dd2e-152">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-152">Click **Add**.</span></span>
27. <span data-ttu-id="9dd2e-153">Vælg **XML\Attribut** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="9dd2e-154">Skriv **Id** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="9dd2e-155">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-155">Click **OK**.</span></span>
30. <span data-ttu-id="9dd2e-156">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-156">Click **Add**.</span></span>
31. <span data-ttu-id="9dd2e-157">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="9dd2e-158">Skriv **Kreditor** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="9dd2e-159">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-159">Click **OK**.</span></span>
34. <span data-ttu-id="9dd2e-160">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="9dd2e-161">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="9dd2e-162">Skriv **Navn** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="9dd2e-163">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-163">Click **OK**.</span></span>
38. <span data-ttu-id="9dd2e-164">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="9dd2e-165">Skriv **Bank** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="9dd2e-166">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-166">Click **OK**.</span></span>
41. <span data-ttu-id="9dd2e-167">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="9dd2e-168">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="9dd2e-169">Skriv **RoutingNumber** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="9dd2e-170">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-170">Click **OK**.</span></span>
45. <span data-ttu-id="9dd2e-171">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="9dd2e-172">Skriv **AccountNumber** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="9dd2e-173">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-173">Click **OK**.</span></span>
48. <span data-ttu-id="9dd2e-174">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="9dd2e-175">Klik på **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-175">Click **Copy**.</span></span>
50. <span data-ttu-id="9dd2e-176">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="9dd2e-177">Klik på **Sæt ind**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-177">Click **Paste**.</span></span>
52. <span data-ttu-id="9dd2e-178">Skriv **Betaler** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="9dd2e-179">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="9dd2e-180">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="9dd2e-181">Skriv **Valuta** feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="9dd2e-182">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-182">Click **OK**.</span></span>
57. <span data-ttu-id="9dd2e-183">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="9dd2e-184">Skriv **Beskrivelse** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="9dd2e-185">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-185">Click **OK**.</span></span>
60. <span data-ttu-id="9dd2e-186">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="9dd2e-187">Skriv **TransDate** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="9dd2e-188">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-188">Click **OK**.</span></span>
63. <span data-ttu-id="9dd2e-189">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="9dd2e-190">Skriv **Beløb** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="9dd2e-191">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="9dd2e-192">Klargør formatkomponenter til tilknytning til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="9dd2e-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="9dd2e-193">Vælg **Xml\Meddelelse\ProcessingDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="9dd2e-194">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="9dd2e-195">Vælg **Tekst\DateTime** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="9dd2e-196">Skriv **åååå-MM-dd** i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="9dd2e-197">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-197">Click **OK**.</span></span>
6. <span data-ttu-id="9dd2e-198">Vælg **Xml\Meddelelse\Betalinger\TransDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="9dd2e-199">Klik på **Tilføj DateTime**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="9dd2e-200">Skriv **åååå-MM-dd** i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="9dd2e-201">Vælg **Date** i feltet **DateTime**-type.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="9dd2e-202">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-202">Click **OK**.</span></span>
11. <span data-ttu-id="9dd2e-203">Vælg **Xml\Meddelelse\MessageId** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="9dd2e-204">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="9dd2e-205">Vælg **Tekst\Streng** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="9dd2e-206">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-206">Click **OK**.</span></span>
15. <span data-ttu-id="9dd2e-207">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="9dd2e-208">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-208">Click **Add String**.</span></span>
17. <span data-ttu-id="9dd2e-209">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-209">Click **OK**.</span></span>
18. <span data-ttu-id="9dd2e-210">Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="9dd2e-211">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-211">Click **Add String**.</span></span>
20. <span data-ttu-id="9dd2e-212">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-212">Click **OK**.</span></span>
21. <span data-ttu-id="9dd2e-213">Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="9dd2e-214">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-214">Click **Add String**.</span></span>
23. <span data-ttu-id="9dd2e-215">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-215">Click **OK**.</span></span>
24. <span data-ttu-id="9dd2e-216">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Navn** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="9dd2e-217">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-217">Click **Add String**.</span></span>
26. <span data-ttu-id="9dd2e-218">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-218">Click **OK**.</span></span>
27. <span data-ttu-id="9dd2e-219">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="9dd2e-220">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-220">Click **Add String**.</span></span>
29. <span data-ttu-id="9dd2e-221">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-221">Click **OK**.</span></span>
30. <span data-ttu-id="9dd2e-222">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="9dd2e-223">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-223">Click **Add String**.</span></span>
32. <span data-ttu-id="9dd2e-224">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-224">Click **OK**.</span></span>
33. <span data-ttu-id="9dd2e-225">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="9dd2e-226">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-226">Click **Add String**.</span></span>
35. <span data-ttu-id="9dd2e-227">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-227">Click **OK**.</span></span>
36. <span data-ttu-id="9dd2e-228">Vælg **Xml\Meddelelse\Betalinger\Vare\Beskrivelse** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="9dd2e-229">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-229">Click **Add String**.</span></span>
38. <span data-ttu-id="9dd2e-230">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-230">Click **OK**.</span></span>
39. <span data-ttu-id="9dd2e-231">Vælg **Xml\Meddelelse\Betalinger\Vare\Beløb** i træet.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="9dd2e-232">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-232">Click **Add String**.</span></span>
41. <span data-ttu-id="9dd2e-233">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-233">Click **OK**.</span></span>
42. <span data-ttu-id="9dd2e-234">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-234">Click **Save**.</span></span>
43. <span data-ttu-id="9dd2e-235">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9dd2e-235">Close the page.</span></span>


