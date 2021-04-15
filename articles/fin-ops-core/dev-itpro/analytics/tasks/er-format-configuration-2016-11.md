---
title: Oprette en ER-formatkonfiguration (november 2016)
description: Dette emne forklarer, hvordan du opretter en formatkonfiguration til elektronisk rapportering (ER).
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46686b9e4f6197f565a324a9d03cbb695b6a933b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749063"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="91bc2-103">Oprette en ER-formatkonfiguration (november 2016)</span><span class="sxs-lookup"><span data-stu-id="91bc2-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91bc2-104">Dette emne beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en formatkonfiguration til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="91bc2-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="91bc2-105">Denne formatkonfiguration definerer formatet af elektroniske dokumenter, der bruges til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="91bc2-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="91bc2-106">I dette eksempel skal du oprette en formatkonfiguration for eksempelfirmaet Litware, Inc. For at fuldføre denne fremgangsmåde, skal du først fuldføre trinnene i proceduren "Tilknyt model til markerede datakilder".</span><span class="sxs-lookup"><span data-stu-id="91bc2-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="91bc2-107">Opret en ny formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="91bc2-107">Create a new format configuration</span></span>
1. <span data-ttu-id="91bc2-108">Gå til **Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="91bc2-109">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="91bc2-110">Vælg **Betalinger (forenklet mode)** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="91bc2-111">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="91bc2-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="91bc2-112">Hvis du ikke kan se **Opret konfiguration**, skal du aktivere designtilstand på siden **Parametre til elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="91bc2-113">Skriv **Format baseret på datamodel PaymentModel** i feltet **Ny**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="91bc2-114">Skriv **BACS (UK-fiktiv)** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="91bc2-115">Skriv **BACS kreditorbetalingsformat (UK-fiktiv)** i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="91bc2-116">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="91bc2-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="91bc2-117">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="91bc2-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="91bc2-118">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="91bc2-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="91bc2-119">Du kan definere et bestemt format for det elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="91bc2-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="91bc2-120">Lad feltet være tomt, hvis du vil vælge et format på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="91bc2-121">Indtast eller vælg en værdi i feltet **Definition af datamodel**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="91bc2-122">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-122">Click **Create configuration**.</span></span> <span data-ttu-id="91bc2-123">En ny konfiguration er oprettet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-123">A new configuration has been created.</span></span> <span data-ttu-id="91bc2-124">Kladdeversionen kan bruges til at gemme designformatet til håndtering af elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="91bc2-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="91bc2-125">Designformatet for et elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="91bc2-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="91bc2-126">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-126">Click **Designer**.</span></span>
2. <span data-ttu-id="91bc2-127">Klik på **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="91bc2-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="91bc2-128">Vælg **Common\File** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="91bc2-129">Skriv **Xml** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="91bc2-130">Skriv **UTF-8** i feltet **Kodning**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="91bc2-131">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-131">Click **OK**.</span></span>
7. <span data-ttu-id="91bc2-132">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-132">Click **Add**.</span></span>
8. <span data-ttu-id="91bc2-133">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="91bc2-134">Skriv **Meddelelse** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="91bc2-135">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-135">Click **OK**.</span></span>
11. <span data-ttu-id="91bc2-136">Vælg **Xml\Meddelelse** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="91bc2-137">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="91bc2-138">Skriv **ProcessingDate** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="91bc2-139">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-139">Click **OK**.</span></span>
15. <span data-ttu-id="91bc2-140">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="91bc2-141">Skriv **MessageId** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="91bc2-142">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-142">Click **OK**.</span></span>
18. <span data-ttu-id="91bc2-143">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="91bc2-144">Skriv **Betalinger** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="91bc2-145">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-145">Click **OK**.</span></span>
21. <span data-ttu-id="91bc2-146">Vælg **Xml\Meddelelse\Betalinger** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="91bc2-147">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="91bc2-148">Skriv **Vare** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="91bc2-149">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-149">Click **OK**.</span></span>
25. <span data-ttu-id="91bc2-150">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="91bc2-151">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-151">Click **Add**.</span></span>
27. <span data-ttu-id="91bc2-152">Vælg **XML\Attribut** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="91bc2-153">Skriv **Id** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="91bc2-154">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-154">Click **OK**.</span></span>
30. <span data-ttu-id="91bc2-155">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-155">Click **Add**.</span></span>
31. <span data-ttu-id="91bc2-156">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="91bc2-157">Skriv **Kreditor** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="91bc2-158">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-158">Click **OK**.</span></span>
34. <span data-ttu-id="91bc2-159">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="91bc2-160">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="91bc2-161">Skriv **Navn** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="91bc2-162">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-162">Click **OK**.</span></span>
38. <span data-ttu-id="91bc2-163">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="91bc2-164">Skriv **Bank** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="91bc2-165">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-165">Click **OK**.</span></span>
41. <span data-ttu-id="91bc2-166">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="91bc2-167">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="91bc2-168">Skriv **RoutingNumber** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="91bc2-169">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-169">Click **OK**.</span></span>
45. <span data-ttu-id="91bc2-170">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="91bc2-171">Skriv **AccountNumber** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="91bc2-172">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-172">Click **OK**.</span></span>
48. <span data-ttu-id="91bc2-173">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="91bc2-174">Klik på **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-174">Click **Copy**.</span></span>
50. <span data-ttu-id="91bc2-175">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="91bc2-176">Klik på **Sæt ind**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-176">Click **Paste**.</span></span>
52. <span data-ttu-id="91bc2-177">Skriv **Betaler** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="91bc2-178">Vælg **Xml\Meddelelse\Betalinger\Vare** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="91bc2-179">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="91bc2-180">Skriv **Valuta** feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="91bc2-181">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-181">Click **OK**.</span></span>
57. <span data-ttu-id="91bc2-182">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="91bc2-183">Skriv **Beskrivelse** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="91bc2-184">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-184">Click **OK**.</span></span>
60. <span data-ttu-id="91bc2-185">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="91bc2-186">Skriv **TransDate** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="91bc2-187">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-187">Click **OK**.</span></span>
63. <span data-ttu-id="91bc2-188">Klik på **Tilføj element**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="91bc2-189">Skriv **Beløb** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="91bc2-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="91bc2-190">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="91bc2-191">Klargør formatkomponenter til tilknytning til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="91bc2-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="91bc2-192">Vælg **Xml\Meddelelse\ProcessingDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="91bc2-193">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="91bc2-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="91bc2-194">Vælg **Tekst\DateTime** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="91bc2-195">Skriv **åååå-MM-dd** i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="91bc2-196">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-196">Click **OK**.</span></span>
6. <span data-ttu-id="91bc2-197">Vælg **Xml\Meddelelse\Betalinger\TransDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="91bc2-198">Klik på **Tilføj DateTime**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="91bc2-199">Skriv **åååå-MM-dd** i feltet **Format**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="91bc2-200">Vælg **Date** i feltet **DateTime**-type.</span><span class="sxs-lookup"><span data-stu-id="91bc2-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="91bc2-201">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-201">Click **OK**.</span></span>
11. <span data-ttu-id="91bc2-202">Vælg **Xml\Meddelelse\MessageId** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="91bc2-203">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="91bc2-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="91bc2-204">Vælg **Tekst\Streng** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="91bc2-205">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-205">Click **OK**.</span></span>
15. <span data-ttu-id="91bc2-206">Vælg **Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="91bc2-207">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-207">Click **Add String**.</span></span>
17. <span data-ttu-id="91bc2-208">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-208">Click **OK**.</span></span>
18. <span data-ttu-id="91bc2-209">Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="91bc2-210">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-210">Click **Add String**.</span></span>
20. <span data-ttu-id="91bc2-211">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-211">Click **OK**.</span></span>
21. <span data-ttu-id="91bc2-212">Vælg **Xml\Meddelelse\Betalinger\Vare\Leverandør\Bank\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="91bc2-213">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-213">Click **Add String**.</span></span>
23. <span data-ttu-id="91bc2-214">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-214">Click **OK**.</span></span>
24. <span data-ttu-id="91bc2-215">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Navn** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="91bc2-216">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-216">Click **Add String**.</span></span>
26. <span data-ttu-id="91bc2-217">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-217">Click **OK**.</span></span>
27. <span data-ttu-id="91bc2-218">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="91bc2-219">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-219">Click **Add String**.</span></span>
29. <span data-ttu-id="91bc2-220">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-220">Click **OK**.</span></span>
30. <span data-ttu-id="91bc2-221">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="91bc2-222">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-222">Click **Add String**.</span></span>
32. <span data-ttu-id="91bc2-223">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-223">Click **OK**.</span></span>
33. <span data-ttu-id="91bc2-224">Vælg **Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\Valuta** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="91bc2-225">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-225">Click **Add String**.</span></span>
35. <span data-ttu-id="91bc2-226">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-226">Click **OK**.</span></span>
36. <span data-ttu-id="91bc2-227">Vælg **Xml\Meddelelse\Betalinger\Vare\Beskrivelse** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="91bc2-228">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-228">Click **Add String**.</span></span>
38. <span data-ttu-id="91bc2-229">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-229">Click **OK**.</span></span>
39. <span data-ttu-id="91bc2-230">Vælg **Xml\Meddelelse\Betalinger\Vare\Beløb** i træet.</span><span class="sxs-lookup"><span data-stu-id="91bc2-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="91bc2-231">Klik på **Tilføj streng**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-231">Click **Add String**.</span></span>
41. <span data-ttu-id="91bc2-232">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-232">Click **OK**.</span></span>
42. <span data-ttu-id="91bc2-233">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="91bc2-233">Click **Save**.</span></span>
43. <span data-ttu-id="91bc2-234">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="91bc2-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]