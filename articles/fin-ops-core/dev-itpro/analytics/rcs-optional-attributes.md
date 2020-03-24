---
title: Importere filer i XML-format med valgfrie attributter
description: Dette emne giver oplysninger om design af ER-formater, der angiver XML-attributter til fortolkning af indgående elektroniske dokumenter i XML-format.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 10795c90cb90961c17a4326b71ed43dc72039f2b
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117419"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="34b23-103">Importere filer i XML-format med valgfrie attributter</span><span class="sxs-lookup"><span data-stu-id="34b23-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34b23-104">Du kan designe ER-formater for at parse indgående elektroniske dokumenter i XML-format.</span><span class="sxs-lookup"><span data-stu-id="34b23-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="34b23-105">Visse attributter af XML-elementer kan angives i designet ER-format som valgfrie.</span><span class="sxs-lookup"><span data-stu-id="34b23-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="34b23-106">Det giver dig mulighed for at håndtere indgående filer med og uden sådanne XML-attributter korrekt.</span><span class="sxs-lookup"><span data-stu-id="34b23-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="34b23-107">Derefter kan du bruge indholdet fra disse filer til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="34b23-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="34b23-108">Hvis du vil vide mere om denne funktion, skal du udføre trinnene i [(RCS) – Importere filer i XML-format med valgfrie attributter](tasks/import-files-xml-format-optional-attributes.md), der er en del af 7.5.4.3 Anskaffe/udarbejde IT-tjeneste/løsningskomponenter (10677).</span><span class="sxs-lookup"><span data-stu-id="34b23-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="34b23-109">Du kan hente denne opgaveguide og tilknyttede eksempelfiler i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="34b23-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="34b23-110">Indholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="34b23-110">Content description</span></span>       | <span data-ttu-id="34b23-111">Fil</span><span class="sxs-lookup"><span data-stu-id="34b23-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="34b23-112">Eksempelfil i XML-format</span><span class="sxs-lookup"><span data-stu-id="34b23-112">Sample file in XML format</span></span> | <span data-ttu-id="34b23-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="34b23-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="34b23-114">Opgaveguide</span><span class="sxs-lookup"><span data-stu-id="34b23-114">Task guide</span></span>                | <span data-ttu-id="34b23-115">RCS Importere filer i XML-format med valgfrie attributter.axtr</span><span class="sxs-lookup"><span data-stu-id="34b23-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="34b23-116">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan designe konfiguration af ER-format til at importere filer i XML-format, der indeholder valgfrie attributter.</span><span class="sxs-lookup"><span data-stu-id="34b23-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="34b23-117">For at fuldføre disse trin skal du først fuldføre trinnene i proceduren [Oprette konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="34b23-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="34b23-118">Før du går i gang, kan du hente og gemme filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml lokalt i Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span><span class="sxs-lookup"><span data-stu-id="34b23-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="34b23-119">Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="34b23-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="34b23-120">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="34b23-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="34b23-121">Hvis denne konfigurationsudbyder ikke vises, skal du fuldføre trinnene i emnet [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="34b23-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="34b23-122">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="34b23-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="34b23-123">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="34b23-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="34b23-124">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34b23-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="34b23-125">Gå til feltet **Navn**, og skriv "Model til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="34b23-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="34b23-126">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="34b23-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="34b23-127">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34b23-127">Click **Designer**.</span></span>
5. <span data-ttu-id="34b23-128">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="34b23-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="34b23-129">Skriv "Rod" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="34b23-130">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="34b23-130">Click **Add**.</span></span>
8. <span data-ttu-id="34b23-131">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="34b23-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="34b23-132">Skriv "Liste" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="34b23-133">Vælg **Liste over poster** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="34b23-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="34b23-134">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="34b23-134">Click **Add**.</span></span>
12.    <span data-ttu-id="34b23-135">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="34b23-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="34b23-136">Skriv 'Kode' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="34b23-137">Vælg **Streng** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="34b23-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="34b23-138">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="34b23-138">Click **Add**.</span></span>
16.    <span data-ttu-id="34b23-139">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="34b23-139">Click **Save**.</span></span>
17.    <span data-ttu-id="34b23-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="34b23-140">Close the page.</span></span>
18.    <span data-ttu-id="34b23-141">Klik på **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="34b23-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="34b23-142">Klik på **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="34b23-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="34b23-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="34b23-144">Opret et format til dataimport</span><span class="sxs-lookup"><span data-stu-id="34b23-144">Create a format for data import</span></span>
1. <span data-ttu-id="34b23-145">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34b23-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="34b23-146">Gå til feltet **Ny**, og indtast "Format baseret på datamodel Model til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="34b23-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="34b23-147">Gå til feltet **Navn**, og skriv "Format til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="34b23-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="34b23-148">Vælg **Ja** i feltet **Understøtter dataimport**.</span><span class="sxs-lookup"><span data-stu-id="34b23-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="34b23-149">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="34b23-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="34b23-150">Designe et format til parsing af en indgående fil i XML-format</span><span class="sxs-lookup"><span data-stu-id="34b23-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="34b23-151">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34b23-151">Click **Designer**.</span></span>
2. <span data-ttu-id="34b23-152">Klik på **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34b23-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="34b23-153">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="34b23-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="34b23-154">Skriv "Rod" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="34b23-155">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-155">Click **OK**.</span></span>
6. <span data-ttu-id="34b23-156">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34b23-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="34b23-157">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="34b23-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="34b23-158">Skriv 'Dokument' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="34b23-159">Vælg **Én mange** i feltet **Multiplicitet**.</span><span class="sxs-lookup"><span data-stu-id="34b23-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="34b23-160">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-160">Click **OK**.</span></span>
11.    <span data-ttu-id="34b23-161">Vælg **rod\layout** i træet.</span><span class="sxs-lookup"><span data-stu-id="34b23-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="34b23-162">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="34b23-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="34b23-163">Vælg **XML\Attribut** i træet.</span><span class="sxs-lookup"><span data-stu-id="34b23-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="34b23-164">Skriv "Id" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="34b23-165">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-165">Click **OK**.</span></span>
16.    <span data-ttu-id="34b23-166">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="34b23-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="34b23-167">Udform en formattilknytning for at gemme oplysninger, der fortolkes, i datamodellen</span><span class="sxs-lookup"><span data-stu-id="34b23-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="34b23-168">Klik på **Knyt format til model**.</span><span class="sxs-lookup"><span data-stu-id="34b23-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="34b23-169">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="34b23-169">Click **New**.</span></span>
3.    <span data-ttu-id="34b23-170">Indtast eller vælg en værdi i feltet **Definition**.</span><span class="sxs-lookup"><span data-stu-id="34b23-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="34b23-171">Skriv "Tilknytning" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="34b23-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="34b23-172">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="34b23-172">Click **Save**.</span></span>
6.    <span data-ttu-id="34b23-173">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34b23-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="34b23-174">Udvid **Format** i træet.</span><span class="sxs-lookup"><span data-stu-id="34b23-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="34b23-175">I træet skal du udvide **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="34b23-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="34b23-176">I træet skal du vælge \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="34b23-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="34b23-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="34b23-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="34b23-178">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="34b23-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="34b23-179">I træet skal du udvide \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="34b23-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="34b23-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="34b23-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="34b23-181">I træet skal du vælge \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="34b23-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="34b23-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="34b23-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="34b23-183">I træet skal du udvide **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="34b23-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="34b23-184">I træet skal du vælge **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="34b23-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="34b23-185">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="34b23-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="34b23-186">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="34b23-186">Click **Save**.</span></span>
17.    <span data-ttu-id="34b23-187">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="34b23-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="34b23-188">Kør formattilknytning</span><span class="sxs-lookup"><span data-stu-id="34b23-188">Run format mapping</span></span>
1. <span data-ttu-id="34b23-189">Klik på **Kør**.</span><span class="sxs-lookup"><span data-stu-id="34b23-189">Click **Run**.</span></span>
2. <span data-ttu-id="34b23-190">Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.</span><span class="sxs-lookup"><span data-stu-id="34b23-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="34b23-191">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="34b23-192">Den valgte fil er ikke importeret, da formatdesignet forudsætter, at attributten "id"' findes for elementet "dokument", men den importerede fil indeholder ikke denne attribut.</span><span class="sxs-lookup"><span data-stu-id="34b23-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="34b23-193">Rediger formatstrukturen for at håndtere XML-attribut som valgfri</span><span class="sxs-lookup"><span data-stu-id="34b23-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="34b23-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="34b23-194">Close the page.</span></span>
2. <span data-ttu-id="34b23-195">I træet skal du udvide **root\document**.</span><span class="sxs-lookup"><span data-stu-id="34b23-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="34b23-196">I træet skal du vælge **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="34b23-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="34b23-197">Vælg **Ja** i feltet **Tom streng for manglende attribut**.</span><span class="sxs-lookup"><span data-stu-id="34b23-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="34b23-198">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="34b23-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="34b23-199">Kør formattilknytning for at teste ændringer</span><span class="sxs-lookup"><span data-stu-id="34b23-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="34b23-200">Klik på **Knyt format til model**.</span><span class="sxs-lookup"><span data-stu-id="34b23-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="34b23-201">Klik på **Kør**.</span><span class="sxs-lookup"><span data-stu-id="34b23-201">Click **Run**.</span></span>
3. <span data-ttu-id="34b23-202">Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.</span><span class="sxs-lookup"><span data-stu-id="34b23-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="34b23-203">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b23-203">Click **OK**.</span></span>
5. <span data-ttu-id="34b23-204">Gennemse den genererede fil.</span><span class="sxs-lookup"><span data-stu-id="34b23-204">Review the generated file.</span></span> <span data-ttu-id="34b23-205">Bemærk, at den samme fil er blevet importeret, da formatdesignet nu anser attributten "id" for elementet "dokument" som valgfrit.</span><span class="sxs-lookup"><span data-stu-id="34b23-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
