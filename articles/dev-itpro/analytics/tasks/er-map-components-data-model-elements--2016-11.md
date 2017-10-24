--- 
title: Tilknytte komponenter af det oprettede format til modelelementer til elektronisk rapportering (ER)
description: "Følgende procedure viser, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan knytte datamodelelementer til komponenter i den oprettede ER-konfiguration (elektroniske rapportering), der definerer et elektronisk dokumentformat for betalingsvirksomhedens domæne."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1c81a1268a56164e0d4465359a0f9ec425ee7c31
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a><span data-ttu-id="8d27c-103">Tilknytte komponenter af det oprettede format til modelelementer til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="8d27c-103">Map components of the created format to data model elements for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d27c-104">Følgende procedure viser, hvordan en bruger med rollen Systemadministrator eller Udvikler til elektronisk rapportering kan knytte datamodelelementer til komponenter i den oprettede ER-konfiguration (elektroniske rapportering), der definerer et elektronisk dokumentformat for betalingsvirksomhedens domæne.</span><span class="sxs-lookup"><span data-stu-id="8d27c-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="8d27c-105">Dette format bruges senere til at generere elektroniske dokumenter til behandling af betalinger.</span><span class="sxs-lookup"><span data-stu-id="8d27c-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="8d27c-106">I dette eksempel skal du oprette en formatkonfiguration til eksempelfirmaet "Litware Inc."</span><span class="sxs-lookup"><span data-stu-id="8d27c-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="8d27c-107">Disse trin kan udføres i alle firmaer, da ER-konfigurationer deles mellem alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="8d27c-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="8d27c-108">For at fuldføre disse trin skal du først fuldføre trinnene i opgaveguiden "Opret en formatkonfiguration".</span><span class="sxs-lookup"><span data-stu-id="8d27c-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="8d27c-109">Vælg en formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d27c-109">Select a format configuration</span></span>
1. <span data-ttu-id="8d27c-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="8d27c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8d27c-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="8d27c-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8d27c-112">Udvid 'Betalinger (forenklet model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="8d27c-113">Vælg 'Betalinger (forenklet model)\BACS (UK fiktivt)' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="8d27c-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="8d27c-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="8d27c-115">Tilknyt formatkomponenter til datamodelelementer</span><span class="sxs-lookup"><span data-stu-id="8d27c-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="8d27c-116">Klik på Udvid/skjul.</span><span class="sxs-lookup"><span data-stu-id="8d27c-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="8d27c-117">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="8d27c-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="8d27c-118">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="8d27c-119">Vælg "Xml\Meddelelse\ProcessingDate\DateTime" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="8d27c-120">Vælg "model\ProcessingDateTime" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="8d27c-121">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-121">Click Bind.</span></span>
7. <span data-ttu-id="8d27c-122">Vælg "Xml\Meddelelse\MessageId\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="8d27c-123">Vælg "model\MessageIdentification" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="8d27c-124">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-124">Click Bind.</span></span>
10. <span data-ttu-id="8d27c-125">Udvid 'model\Betalinger' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="8d27c-126">Vælg "Xml\Meddelelse\Betalinger\Vare\Beløb\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="8d27c-127">Vælg "model\Betalinger\InstructedAmount" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="8d27c-128">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-128">Click Bind.</span></span>
14. <span data-ttu-id="8d27c-129">Vælg "Xml\Meddelelse\Betalinger\TransDate\DateTime" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="8d27c-130">Vælg "model\Betalinger\TransactionDate" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="8d27c-131">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-131">Click Bind.</span></span>
17. <span data-ttu-id="8d27c-132">Vælg "Xml\Meddelelse\Betalinger\Vare\Beskrivelse\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="8d27c-133">Vælg "model\Betalinger\Beskrivelse" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="8d27c-134">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-134">Click Bind.</span></span>
20. <span data-ttu-id="8d27c-135">Vælg "Xml\Meddelelse\Betalinger\Vare\Valuta\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="8d27c-136">Vælg 'model\Betalinger\Valuta' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="8d27c-137">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-137">Click Bind.</span></span>
23. <span data-ttu-id="8d27c-138">Vælg "Xml\Meddelelse\Betalinger\Vare\Id" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="8d27c-139">Vælg "model\Betalinger\End2EndID" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="8d27c-140">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-140">Click Bind.</span></span>
26. <span data-ttu-id="8d27c-141">Udvid "model\Betalinger\Kreditor" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="8d27c-142">Udvid 'model\Betalinger\Kreditor\Konto' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="8d27c-143">Udvid "model\Betalinger\Kreditor\Speditør" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="8d27c-144">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Navn\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="8d27c-145">Vælg "model\Betalinger\Kreditor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="8d27c-146">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-146">Click Bind.</span></span>
32. <span data-ttu-id="8d27c-147">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\RoutingNumber\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="8d27c-148">Vælg "model\Betalinger\Kreditor\Agent\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="8d27c-149">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-149">Click Bind.</span></span>
35. <span data-ttu-id="8d27c-150">Vælg "Xml\Meddelelse\Betalinger\Vare\Kreditor\Bank\AccountNumber\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="8d27c-151">Vælg "model\Betalinger\Kreditor\Konto\Nummer" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="8d27c-152">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-152">Click Bind.</span></span>
38. <span data-ttu-id="8d27c-153">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Navn\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="8d27c-154">Udvid "model\Betalinger\Debitor" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="8d27c-155">Udvid 'model\Betalinger\Debitor\Konto' i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="8d27c-156">Udvid "model\Betalinger\Debitor\Speditør" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="8d27c-157">Vælg "model\Betalinger\Debitor\Navn" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="8d27c-158">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-158">Click Bind.</span></span>
44. <span data-ttu-id="8d27c-159">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\RoutingNumber\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="8d27c-160">Vælg "model\Betalinger\Kreditor\Agent\RoutingNumber" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="8d27c-161">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-161">Click Bind.</span></span>
47. <span data-ttu-id="8d27c-162">Vælg "Xml\Meddelelse\Betalinger\Vare\Betaler\Bank\AccountNumber\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="8d27c-163">Vælg "model\Betalinger\Debitor\Konto\Nummer" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="8d27c-164">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-164">Click Bind.</span></span>
50. <span data-ttu-id="8d27c-165">Vælg "Xml\Meddelelse\Betalinger\Vare" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="8d27c-166">Vælg "model\Betalinger" i træet.</span><span class="sxs-lookup"><span data-stu-id="8d27c-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="8d27c-167">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="8d27c-167">Click Bind.</span></span>
53. <span data-ttu-id="8d27c-168">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8d27c-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="8d27c-169">Valider formattilknytning</span><span class="sxs-lookup"><span data-stu-id="8d27c-169">Validate format mapping</span></span>
1. <span data-ttu-id="8d27c-170">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="8d27c-170">Click Validate.</span></span>
    * <span data-ttu-id="8d27c-171">Valider den nye tilknytning for at sikre, at alle bindinger er i orden.</span><span class="sxs-lookup"><span data-stu-id="8d27c-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="8d27c-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8d27c-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="8d27c-173">Ændr status for den aktuelle version af formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="8d27c-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="8d27c-174">I de næste trin skal du ændre status for formatkonfigurationen fra Udkast til Fuldført for at gøre den tilgængelig for generering af betalingsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="8d27c-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="8d27c-175">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="8d27c-175">Click Change status.</span></span>
2. <span data-ttu-id="8d27c-176">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="8d27c-176">Click Complete.</span></span>
3. <span data-ttu-id="8d27c-177">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8d27c-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="8d27c-178">For eksempel "version 1".</span><span class="sxs-lookup"><span data-stu-id="8d27c-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="8d27c-179">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="8d27c-179">Click OK.</span></span>
5. <span data-ttu-id="8d27c-180">Vælg den færdige version af den aktuelle konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d27c-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="8d27c-181">Bemærk, at konfigurationen gemmes som fuldført version 1.1: Dette er version 1 af det format, der er baseret på version 1 af datamodellen.</span><span class="sxs-lookup"><span data-stu-id="8d27c-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="8d27c-182">Definer ikrafttrædelsesdatoen for færdig version af format</span><span class="sxs-lookup"><span data-stu-id="8d27c-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="8d27c-183">Hver formatversion kan konfigureres som tilgængelig for brug fra en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="8d27c-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="8d27c-184">Når der er mere end én formatversion aktiv på en bestemt dato, vælges det nyeste format (baseret på versionsnummer) til anvendelse.</span><span class="sxs-lookup"><span data-stu-id="8d27c-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="8d27c-185">Sessionens datoværdi bruges til valg af korrekt version.</span><span class="sxs-lookup"><span data-stu-id="8d27c-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="8d27c-186">Begræns adgang til oprettet format fra firmaer</span><span class="sxs-lookup"><span data-stu-id="8d27c-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="8d27c-187">Udvid sektionen ISO-land/områdekoder.</span><span class="sxs-lookup"><span data-stu-id="8d27c-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="8d27c-188">Hver formatadgang kan begrænses ved at identificere bestemte lande/områder, hvori et format er gældende.</span><span class="sxs-lookup"><span data-stu-id="8d27c-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="8d27c-189">Hvis listen over lande/områder for det pågældende format er tom, kan dette format bruges i ethvert firma.</span><span class="sxs-lookup"><span data-stu-id="8d27c-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="8d27c-190">Når der indsættes nogle ISO-lande/-områdekoder på denne liste over lande/områder, kan dette format kun bruges i firmaer, hvis den primære adresse er i landet/området.</span><span class="sxs-lookup"><span data-stu-id="8d27c-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  


