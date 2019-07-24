---
title: (RCS) Importere filer i XML-format med valgfrie attributter
description: Dette emne indeholder oplysninger om, hvordan en bruger kan designe ER-formatkonfiguration til at importere filer i XML-format, der indeholder valgfrie attributter.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727069"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="5d991-103">(RCS) Importere filer i XML-format med valgfrie attributter</span><span class="sxs-lookup"><span data-stu-id="5d991-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d991-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan designe konfiguration af ER-format til at importere filer i XML-format, der indeholder valgfrie attributter.</span><span class="sxs-lookup"><span data-stu-id="5d991-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="5d991-105">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="5d991-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="5d991-106">Før du går i gang, kan du hente og gemme filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml lokalt i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5d991-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="5d991-107">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="5d991-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="5d991-108">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5d991-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="5d991-109">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5d991-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="5d991-110">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="5d991-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="5d991-111">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5d991-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="5d991-112">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5d991-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="5d991-113">Gå til feltet **Navn**, og skriv "Model til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="5d991-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="5d991-114">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5d991-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="5d991-115">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="5d991-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="5d991-116">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="5d991-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="5d991-117">Skriv "Rod" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="5d991-118">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5d991-118">Click **Add**.</span></span>
8.  <span data-ttu-id="5d991-119">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="5d991-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="5d991-120">Skriv "Liste" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="5d991-121">Vælg **Liste over poster** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="5d991-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="5d991-122">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5d991-122">Click **Add**.</span></span>
12. <span data-ttu-id="5d991-123">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="5d991-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="5d991-124">Skriv 'Kode' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="5d991-125">Vælg **Streng** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="5d991-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="5d991-126">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5d991-126">Click **Add**.</span></span>
16. <span data-ttu-id="5d991-127">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d991-127">Click **Save**.</span></span>
17. <span data-ttu-id="5d991-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5d991-128">Close the page.</span></span>
18. <span data-ttu-id="5d991-129">Klik på **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="5d991-129">Click **Change status**.</span></span>
19. <span data-ttu-id="5d991-130">Klik på **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="5d991-130">Click **Complete**.</span></span>
20. <span data-ttu-id="5d991-131">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="5d991-132">Opret et format til dataimport</span><span class="sxs-lookup"><span data-stu-id="5d991-132">Create a format for data import</span></span>
1.  <span data-ttu-id="5d991-133">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5d991-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="5d991-134">Gå til feltet **Ny**, og indtast "Format baseret på datamodel Model til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="5d991-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="5d991-135">Gå til feltet **Navn**, og skriv "Format til at importere xml-fil".</span><span class="sxs-lookup"><span data-stu-id="5d991-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="5d991-136">Vælg **Ja** i feltet **Understøtter dataimport**.</span><span class="sxs-lookup"><span data-stu-id="5d991-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="5d991-137">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="5d991-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="5d991-138">Designe et format til parsing af en indgående fil i XML-format</span><span class="sxs-lookup"><span data-stu-id="5d991-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="5d991-139">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="5d991-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="5d991-140">Klik på **Tilføj rod** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5d991-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="5d991-141">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="5d991-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="5d991-142">Skriv "Rod" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="5d991-143">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-143">Click **OK**.</span></span>
6.  <span data-ttu-id="5d991-144">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5d991-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="5d991-145">Vælg **XML\Element** i træet.</span><span class="sxs-lookup"><span data-stu-id="5d991-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="5d991-146">Skriv 'Dokument' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="5d991-147">Vælg **Én mange** i feltet **Multiplicitet**.</span><span class="sxs-lookup"><span data-stu-id="5d991-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="5d991-148">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-148">Click **OK**.</span></span>
11. <span data-ttu-id="5d991-149">Vælg **rod\layout** i træet.</span><span class="sxs-lookup"><span data-stu-id="5d991-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="5d991-150">Klik på **Tilføj** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5d991-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="5d991-151">Vælg **XML\Attribut** i træet.</span><span class="sxs-lookup"><span data-stu-id="5d991-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="5d991-152">Skriv "Id" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="5d991-153">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-153">Click **OK**.</span></span>
16. <span data-ttu-id="5d991-154">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d991-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="5d991-155">Udform en formattilknytning for at gemme oplysninger, der fortolkes, i datamodellen</span><span class="sxs-lookup"><span data-stu-id="5d991-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="5d991-156">Klik på **Knyt format til model**.</span><span class="sxs-lookup"><span data-stu-id="5d991-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="5d991-157">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5d991-157">Click **New**.</span></span>
3. <span data-ttu-id="5d991-158">Indtast eller vælg en værdi i feltet **Definition**.</span><span class="sxs-lookup"><span data-stu-id="5d991-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="5d991-159">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="5d991-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5d991-160">Skriv "Tilknytning" i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5d991-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="5d991-161">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d991-161">Click **Save**.</span></span>
7. <span data-ttu-id="5d991-162">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="5d991-162">Click **Designer**.</span></span>
8. <span data-ttu-id="5d991-163">Udvid **Format** i træet.</span><span class="sxs-lookup"><span data-stu-id="5d991-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="5d991-164">I træet skal du udvide **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="5d991-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="5d991-165">I træet skal du vælge \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5d991-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5d991-166">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5d991-166">(document)\*\*.</span></span>
11. <span data-ttu-id="5d991-167">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5d991-167">Click **Bind**.</span></span>
12. <span data-ttu-id="5d991-168">I træet skal du udvide \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5d991-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5d991-169">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5d991-169">(document)\*\*.</span></span>
13. <span data-ttu-id="5d991-170">I træet skal du vælge \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="5d991-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="5d991-171">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="5d991-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="5d991-172">I træet skal du udvide **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="5d991-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="5d991-173">I træet skal du vælge **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="5d991-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="5d991-174">Klik på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="5d991-174">Click **Bind**.</span></span>
17. <span data-ttu-id="5d991-175">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d991-175">Click **Save**.</span></span>
18. <span data-ttu-id="5d991-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5d991-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="5d991-177">Kør formattilknytning</span><span class="sxs-lookup"><span data-stu-id="5d991-177">Run format mapping</span></span>
1. <span data-ttu-id="5d991-178">Klik på **Kør**.</span><span class="sxs-lookup"><span data-stu-id="5d991-178">Click **Run**.</span></span>
2. <span data-ttu-id="5d991-179">Klik på **Gennemse**, og vælg **IncomingDocumentToLearnHowToHandleOptionalAttributes xml**.</span><span class="sxs-lookup"><span data-stu-id="5d991-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="5d991-180">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="5d991-181">Den valgte fil er ikke importeret, da formatdesignet forudsætter, at attributten "id"' findes for elementet "Dokument", men den importerede fil indeholder ikke denne attribut.</span><span class="sxs-lookup"><span data-stu-id="5d991-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="5d991-182">Rediger formatstrukturen for at håndtere XML-attribut som valgfri</span><span class="sxs-lookup"><span data-stu-id="5d991-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="5d991-183">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5d991-183">Close the page.</span></span>
2. <span data-ttu-id="5d991-184">I træet skal du udvide **root\document**.</span><span class="sxs-lookup"><span data-stu-id="5d991-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="5d991-185">I træet skal du vælge **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="5d991-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="5d991-186">Vælg **Ja** i feltet **Tom streng for manglende attribut**.</span><span class="sxs-lookup"><span data-stu-id="5d991-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="5d991-187">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5d991-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="5d991-188">Kør formattilknytning for at teste ændringer</span><span class="sxs-lookup"><span data-stu-id="5d991-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="5d991-189">Klik på **Knyt format til model**.</span><span class="sxs-lookup"><span data-stu-id="5d991-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="5d991-190">Klik på **Kør**.</span><span class="sxs-lookup"><span data-stu-id="5d991-190">Click **Run**.</span></span>
3. <span data-ttu-id="5d991-191">Klik på **Gennemse**, og vælg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="5d991-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="5d991-192">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d991-192">Click **OK**.</span></span>
5. <span data-ttu-id="5d991-193">Gennemse den genererede fil.</span><span class="sxs-lookup"><span data-stu-id="5d991-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="5d991-194">Den samme fil er blevet importeret, da formatdesignet nu anser attributten "id" for elementet "Document" som valgfrit.</span><span class="sxs-lookup"><span data-stu-id="5d991-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
