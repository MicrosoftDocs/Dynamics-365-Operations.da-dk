---
title: Forberede programspecifikke metadata til RCS og ER
description: Dette emne forklarer, hvordan du forbereder programspecifikke metadata til Regulatory Configuration Service (RCS) og elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 37da06f4ba86594c6368dcd1049456c58bf87e3a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565459"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="97d08-103">Forberede programspecifikke metadata til RCS og ER</span><span class="sxs-lookup"><span data-stu-id="97d08-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97d08-104">I dette emne gennemgås eksempler på følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="97d08-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="97d08-105">Klargøre programmetadata, der kan bruges i RCS</span><span class="sxs-lookup"><span data-stu-id="97d08-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="97d08-106">Få adgang til programmetadata ved hjælp af ER-konfiguration</span><span class="sxs-lookup"><span data-stu-id="97d08-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="97d08-107">Få adgang til programmetadata ved hjælp af tilsluttede programmer</span><span class="sxs-lookup"><span data-stu-id="97d08-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="97d08-108">Klargøre programmetadata, der kan bruges i RCS</span><span class="sxs-lookup"><span data-stu-id="97d08-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="97d08-109">Følgende procedure viser, hvordan en bruger, der har rollen **Systemadministrator** eller rollen **Udvikler af elektronisk rapportering**, kan oprette en elektronisk rapporteringskonfiguration (ER), der indeholder metadata til programmet, og som bruges til at designe konfigurationer af ER-modeltilknytning i Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="97d08-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="97d08-110">Eksempelkonfigurationen af ER-modeltilknytning, der oprettes i dette eksempel, bruges til at få adgang til udenlandske handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="97d08-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="97d08-111">I dette eksempel skal du bruge RCS til at designe en ER-løsning for programmet, der skal bruges til at generere elektroniske dokumenter, der indeholder oplysninger fra forretningsdomænet til udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="97d08-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="97d08-112">Hvis du vil angive tilknytningen mellem ER-datamodellen og kilderne til de påkrævede data, skal du have adgang til programmetadata i RCS.</span><span class="sxs-lookup"><span data-stu-id="97d08-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="97d08-113">Som en del af processen med at designe ER-løsningen skal du oprette en ny ER-metadatakonfiguration, der indeholder alle de metadata, der i øjeblikket er påkrævet for at generere ER-rapporter for det valgte forretningsdomæne.</span><span class="sxs-lookup"><span data-stu-id="97d08-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="97d08-114">I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i enhver virksomhed.</span><span class="sxs-lookup"><span data-stu-id="97d08-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="97d08-115">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97d08-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="97d08-116">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="97d08-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="97d08-117">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="97d08-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="97d08-118">Vælg **Konfiguration af metadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="97d08-119">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="97d08-120">Angiv et navn i feltet **Navn** i rulledialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97d08-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="97d08-121">I dette eksempel skal du angive **Udenrigshandelmetadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="97d08-122">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="97d08-123">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-123">Select **Designer**.</span></span>
8. <span data-ttu-id="97d08-124">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-125">Du kan enten vælge alle metadata for hele programmet eller for udvalgte modeller eller moduler.</span><span class="sxs-lookup"><span data-stu-id="97d08-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="97d08-126">Bemærk i begge tilfælde, at følgende metadata vil blive tilføjet automatisk: tabeller over poster, fasttekster og udvidede datatyper (EDT'er).</span><span class="sxs-lookup"><span data-stu-id="97d08-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="97d08-127">Når der kræves flere typer metadata, skal de tilføjes manuelt.</span><span class="sxs-lookup"><span data-stu-id="97d08-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="97d08-128">Du skal tilføje nogle metadata, der er relateret til udenlandske handelstransaktioner, og vælge metadataelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="97d08-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="97d08-129">Vælg **Tilføj datakilde \> Tabelposter**.</span><span class="sxs-lookup"><span data-stu-id="97d08-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="97d08-130">Filtrer efter værdien **Intrastat** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="97d08-131">Vælg **Intrastat** -tabelposten.</span><span class="sxs-lookup"><span data-stu-id="97d08-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="97d08-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-132">Select **OK**.</span></span>

    <span data-ttu-id="97d08-133">Du skal tilføje metadataoplysninger om Intrastat-tabellen med poster.</span><span class="sxs-lookup"><span data-stu-id="97d08-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="97d08-134">I træet skal du vælge **Tabelposter Intrastat \> \>Relationer \> IntrastatCommodity (tabelposter EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="97d08-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="97d08-135">Vælg **Tilføj metadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-136">Metadata om nødvendige relationer for den valgte tabel med poster skal tilføjes manuelt.</span><span class="sxs-lookup"><span data-stu-id="97d08-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="97d08-137">Vælg **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="97d08-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="97d08-138">Vælg **Fasttekst**.</span><span class="sxs-lookup"><span data-stu-id="97d08-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="97d08-139">Filtrer efter værdien **IntrastatDirection** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="97d08-140">Vælg **IntrastatDirection**-fasttekstposten.</span><span class="sxs-lookup"><span data-stu-id="97d08-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="97d08-141">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-141">Select **OK**.</span></span>
20. <span data-ttu-id="97d08-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="97d08-142">Select **Save**.</span></span>
21. <span data-ttu-id="97d08-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97d08-143">Close the page.</span></span>
22. <span data-ttu-id="97d08-144">Fuldfør kladdeversionen af metadatakonfigurationen:</span><span class="sxs-lookup"><span data-stu-id="97d08-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="97d08-145">Vælg **Skift status \> Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="97d08-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="97d08-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-146">Select **OK**.</span></span>
    3. <span data-ttu-id="97d08-147">Vælg den fuldførte version 1.</span><span class="sxs-lookup"><span data-stu-id="97d08-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="97d08-148">Eksportér den fuldførte version af metadatakonfigurationen fra programmet som en XML-fil:</span><span class="sxs-lookup"><span data-stu-id="97d08-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="97d08-149">Vælg **Udveksling \> Eksportér som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="97d08-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="97d08-150">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-150">Select **OK**.</span></span>

<span data-ttu-id="97d08-151">Den ER-metadatakonfiguration, som du har oprettet, gemmes som filen **Udenrigshandelmetadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="97d08-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="97d08-152">Du kan nu importere den i RCS, så den kan bruges som kilden til metadata i forretningsdomænet for udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="97d08-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="97d08-153">Baseret på disse oplysninger kan du angive tilknytningen mellem programmetadata og ER-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="97d08-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="97d08-154">Få adgang til programmetadata ved hjælp af ER-konfiguration</span><span class="sxs-lookup"><span data-stu-id="97d08-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="97d08-155">Følgende procedure viser, hvordan en RCS-bruger, der har rollen **Systemadministrator** eller **Udvikler til elektronisk rapportering** kan designe en ny ER-modeltilknytning ved hjælp af metadata fra programmet.</span><span class="sxs-lookup"><span data-stu-id="97d08-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="97d08-156">Der opnås adgang til programmetadata ved hjælp af en ER-metadatakonfiguration, der indeholder et eksempel sæt af metadata for adgang til udenrigshandelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="97d08-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="97d08-157">Før du kan fuldføre denne procedure, skal du fuldføre følgende procedurer:</span><span class="sxs-lookup"><span data-stu-id="97d08-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="97d08-158">Oprette konfigurationsudbydere og markere dem som aktive</span><span class="sxs-lookup"><span data-stu-id="97d08-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="97d08-159">Klargøre programmetadata, der kan bruges i RCS</span><span class="sxs-lookup"><span data-stu-id="97d08-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="97d08-160">Gå til **Alle arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97d08-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="97d08-161">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="97d08-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="97d08-162">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="97d08-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="97d08-163">Importer den ER-metadatakonfiguration, der indeholder metadata for programmet, og som er konfigureret til at generere elektroniske dokumenter for udenrigshandelens forretningsdomæne.</span><span class="sxs-lookup"><span data-stu-id="97d08-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="97d08-164">Du har oprettet denne ER-metadatakonfiguration og eksporteret den som en XML-fil i proceduren [Klargøre programmetadata, der kan bruges i RCS](#prepare-application-metadata-that-can-be-used-in-rcs) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="97d08-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="97d08-165">Vælg **Konfiguration af metadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="97d08-166">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="97d08-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="97d08-167">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="97d08-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="97d08-168">Naviger for at vælge filen **Udenrigshandelmetadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="97d08-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="97d08-169">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-169">Select **OK**.</span></span>
    6. <span data-ttu-id="97d08-170">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97d08-170">Close the page.</span></span>

4. <span data-ttu-id="97d08-171">Opret en datamodelkonfiguration:</span><span class="sxs-lookup"><span data-stu-id="97d08-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="97d08-172">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="97d08-173">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="97d08-174">Angiv **Udenrigshandelmodel** i feltet **Navn** i rulledialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97d08-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="97d08-175">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="97d08-176">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="97d08-177">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="97d08-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="97d08-178">Skriv **Rod** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="97d08-179">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="97d08-180">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="97d08-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="97d08-181">Skriv **Transaktion** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="97d08-182">Vælg **Liste over poster** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="97d08-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="97d08-183">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="97d08-184">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="97d08-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="97d08-185">Skriv **Varekode** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="97d08-186">Vælg **Streng** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="97d08-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="97d08-187">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-187">Select **Add**.</span></span>

    9. <span data-ttu-id="97d08-188">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="97d08-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="97d08-189">Skriv **Faktureret beløb** i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97d08-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="97d08-190">Vælg **Kommatal** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="97d08-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="97d08-191">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-191">Select **Add**.</span></span>

    10. <span data-ttu-id="97d08-192">Vælg **Ny** for at åbne dialogboksen Slip.</span><span class="sxs-lookup"><span data-stu-id="97d08-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="97d08-193">Skriv **Dato** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="97d08-194">Vælg **Dato** i feltet **Varetype**.</span><span class="sxs-lookup"><span data-stu-id="97d08-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="97d08-195">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="97d08-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="97d08-196">Vælg **Tilføj \> Rodreference**.</span><span class="sxs-lookup"><span data-stu-id="97d08-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="97d08-197">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-197">Select **OK**.</span></span>
    13. <span data-ttu-id="97d08-198">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="97d08-198">Select **Save**.</span></span>
    14. <span data-ttu-id="97d08-199">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97d08-199">Close the page.</span></span>
    15. <span data-ttu-id="97d08-200">Vælg **Skift status \> Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="97d08-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="97d08-201">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-201">Select **OK**.</span></span>

5. <span data-ttu-id="97d08-202">Opret en konfiguration af modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="97d08-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="97d08-203">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="97d08-204">Angiv **Modeltilknytning baseret på datamodellen Udenrigshandelmodel** i feltet **Ny** i rulledialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97d08-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="97d08-205">Skriv **Tilknytning af udenrigshandel** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="97d08-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="97d08-206">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="97d08-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="97d08-207">Vælg **Rediger** i oversigtspanelet **Forudsætninger**.</span><span class="sxs-lookup"><span data-stu-id="97d08-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="97d08-208">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97d08-208">Select **New**.</span></span>
    7. <span data-ttu-id="97d08-209">Vælg **Konfiguration** i feltet **Type af forudsætningskomponent**.</span><span class="sxs-lookup"><span data-stu-id="97d08-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="97d08-210">Vælg konfigurationen **Udenrigshandelmetadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="97d08-211">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="97d08-211">Select **Save**.</span></span> <span data-ttu-id="97d08-212">Bemærk, at referencen er føjet til version 1 af konfigurationen **Udenrigshandelmetadata**.</span><span class="sxs-lookup"><span data-stu-id="97d08-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="97d08-213">Der tilbydes programmetadata fra denne konfiguration, mens modeltilknytningen bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="97d08-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="97d08-214">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97d08-214">Close the page.</span></span>
    11. <span data-ttu-id="97d08-215">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="97d08-216">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="97d08-217">Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="97d08-218">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="97d08-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="97d08-219">I feltet **Navn** skal du skrive **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="97d08-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="97d08-220">Vælg **Intrastat** -tabelposter.</span><span class="sxs-lookup"><span data-stu-id="97d08-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="97d08-221">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="97d08-222">Der tilbydes kun to tabeller, da der kun blev føjet to tabeller til det sæt metadata, der bruges i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="97d08-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="97d08-223">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="97d08-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="97d08-224">Vælg **Intrastat \> AmountMST** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="97d08-225">Vælg **Transaktion = Intrastat \> Faktureret beløb** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="97d08-226">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="97d08-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="97d08-227">Vælg **Intrastat \> TransDate** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="97d08-228">Vælg **Transaktion = Intrastat \> Dato** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="97d08-229">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="97d08-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="97d08-230">Vælg **Intrastat \> \>Relationer \> IntrastatCommodity \> Kode** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="97d08-231">Vælg **Transaktion = Intrastat \> Varekode** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="97d08-232">Vælg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="97d08-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="97d08-233">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="97d08-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="97d08-234">Når validering er fuldført, har du bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om programmetadata fra den ER-metadatakonfiguration, der refereres til.</span><span class="sxs-lookup"><span data-stu-id="97d08-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="97d08-235">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="97d08-235">Select **Save**.</span></span>

<span data-ttu-id="97d08-236">Du kan efter behov udvide det eksisterende sæt metadata i programmet.</span><span class="sxs-lookup"><span data-stu-id="97d08-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="97d08-237">Du kan derefter eksportere den nye fuldførte version af ER-metadatakonfigurationen, importere den til RCS og opdatere forudsætningerne for den konfigurerede konfiguration af modeltilknytning, der refererer til en ny version af den importerede metadatakonfiguration.</span><span class="sxs-lookup"><span data-stu-id="97d08-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="97d08-238">Denne indlæsningsmetode af oplysninger om programmetadata er den eneste, der er tilgængelig for lokalt installerede programmer (når der bruges lokale virksomhedsdata \[LBD\] eller en lokal installationsmodel for programmet).</span><span class="sxs-lookup"><span data-stu-id="97d08-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="97d08-239">Få adgang til programmetadata ved hjælp af tilsluttede programmer</span><span class="sxs-lookup"><span data-stu-id="97d08-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="97d08-240">Følgende procedure viser, hvordan en RCS-bruger, der har rollen **Systemadministrator** eller **Udvikler til elektronisk rapportering** kan designe en ny ER-modeltilknytning ved hjælp af metadata fra programmet.</span><span class="sxs-lookup"><span data-stu-id="97d08-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="97d08-241">Du kan få adgang til programmetadata online ved hjælp af det RCS-tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="97d08-242">Et eksempel på ER-modeltilknytning konfigureres til at give adgang til udenrigshandelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="97d08-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="97d08-243">For at fuldføre denne procedure skal du først fuldføre proceduren [Opret konfigurationsudbydere og markere dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.</span><span class="sxs-lookup"><span data-stu-id="97d08-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="97d08-244">Hvis du ikke har fuldført [Få adgang til programmetadata ved hjælp af ER-konfiguration](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emne, skal du gå til siden [Opgaveguider til elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) for at downloade følgende ER-konfigurationsfiler på forhånd og gemme dem lokalt: **Udenrigshandelmetadata.xml**, **Udenrigshandelmodel.xml** og **Tilknytning af udenrigshandel.xml**.</span><span class="sxs-lookup"><span data-stu-id="97d08-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="97d08-245">Få de nødvendige ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="97d08-245">Get required ER configurations</span></span>

<span data-ttu-id="97d08-246">Hvis du allerede har udført trinnene i proceduren [Få adgang til programmetadata ved hjælp af ER-konfiguration](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emne, har du allerede alle de nødvendige ER-konfigurationer (konfigurationer af metadata til udenrigshandel, model og tilknytning) i den aktuelle RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="97d08-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="97d08-247">I dette tilfælde kan du springe denne procedure over.</span><span class="sxs-lookup"><span data-stu-id="97d08-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="97d08-248">Gå til **Alle arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97d08-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="97d08-249">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="97d08-250">Indlæs konfigurationsfilerne **Udenrigshandelmetadata.xml**, **Udenrigshandelmodel.xml** og **Tilknytning af udenrigshandel.xml** ved at gentage følgende trinserie for hver af dem:</span><span class="sxs-lookup"><span data-stu-id="97d08-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="97d08-251">Vælg **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="97d08-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="97d08-252">Vælg **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="97d08-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="97d08-253">Vælg **Gennemse**, og vælg en fil.</span><span class="sxs-lookup"><span data-stu-id="97d08-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="97d08-254">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d08-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="97d08-255">Registrer forbindelsen til programmet</span><span class="sxs-lookup"><span data-stu-id="97d08-255">Register the connection with the application</span></span>

1. <span data-ttu-id="97d08-256">Gå til **Alle arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97d08-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="97d08-257">Vælg **Tilsluttede programmer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="97d08-258">Sørg for, at det konfigurerede program er baseret på Microsoft Azure, og at det er generelt tilgængeligt for RCS-brugere.</span><span class="sxs-lookup"><span data-stu-id="97d08-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="97d08-259">Det kræves også, at den aktuelle RCS-bruger har adgang til det konfigurerede program, der registreres, som bruger af dette program med en rolle, som giver adgangsrettigheder til programmets metadata.</span><span class="sxs-lookup"><span data-stu-id="97d08-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="97d08-260">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97d08-260">Select **New**.</span></span>
5. <span data-ttu-id="97d08-261">I feltet **Navn** skal du angive **MyConnectedApp** som navnet på det tilknyttede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="97d08-262">Angiv programmets URL-adresse i feltet **Applikation**.</span><span class="sxs-lookup"><span data-stu-id="97d08-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="97d08-263">Angiv programmets udbyder i feltet **Lejer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="97d08-264">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="97d08-264">Select **Save**.</span></span> 
9. <span data-ttu-id="97d08-265">Når du kontrollerer forbindelsen til det konfigurerede program, skal du på siden **Opret forbindelse til eksternt program** vælge linket **Klik her for at oprette forbindelse til det valgte eksterne program**.</span><span class="sxs-lookup"><span data-stu-id="97d08-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="97d08-266">Vælg **Kontrollér forbindelsen** for at validere adgangen til det konfigurerede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="97d08-267">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="97d08-267">Select **Close**.</span></span>

<span data-ttu-id="97d08-268">Når du har udført denne procedure, og forbindelsen er valideret korrekt, opdateres versions- og lejeroplysningerne for det konfigurerede program i det aktuelle gitter.</span><span class="sxs-lookup"><span data-stu-id="97d08-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="97d08-269">Gennemgå den eksisterende modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="97d08-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="97d08-270">Gå til **Alle arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97d08-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="97d08-271">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="97d08-272">Vælg **Udenrigshandelmodel \> Tilknytning af udenrigshandel** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="97d08-273">Vælg oversigtspanelet **Forudsætninger**.</span><span class="sxs-lookup"><span data-stu-id="97d08-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-274">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="97d08-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="97d08-275">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="97d08-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="97d08-276">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-276">Select **Designer**.</span></span>
5. <span data-ttu-id="97d08-277">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-277">Select **Designer**.</span></span>
6. <span data-ttu-id="97d08-278">Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="97d08-279">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="97d08-279">Select **Add root**.</span></span>
8. <span data-ttu-id="97d08-280">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="97d08-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-281">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="97d08-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="97d08-282">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="97d08-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="97d08-283">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="97d08-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="97d08-284">Tildele det tilsluttede program en modeltilknytning</span><span class="sxs-lookup"><span data-stu-id="97d08-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="97d08-285">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="97d08-285">Select **Edit**.</span></span>
2. <span data-ttu-id="97d08-286">Vælg programmet **MyConnectedApp** i feltet **Tilsluttet program**.</span><span class="sxs-lookup"><span data-stu-id="97d08-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-287">Denne tilknytning refererer til metadataene for det valgte tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="97d08-288">Hvis en tilknytning refererer til metadatakonfigurationen og det tilsluttede program samtidig, bruges metadataene for det tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="97d08-289">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-289">Select **Designer**.</span></span>
4. <span data-ttu-id="97d08-290">Vælg **Designer**.</span><span class="sxs-lookup"><span data-stu-id="97d08-290">Select **Designer**.</span></span>
5. <span data-ttu-id="97d08-291">Vælg **Dynamics 365 for Operations \> Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="97d08-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="97d08-292">Vælg **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="97d08-292">Select **Add root**.</span></span>
7. <span data-ttu-id="97d08-293">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="97d08-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97d08-294">Nu tilbydes der mere end to programtabeller, da denne tilknytning bruger alle de metadata, der er tildelt det tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="97d08-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="97d08-295">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="97d08-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="97d08-296">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="97d08-296">Select **Validate**.</span></span>

<span data-ttu-id="97d08-297">Du har nu bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om metadata for det tilsluttede program, der er tildelt denne tilknytning.</span><span class="sxs-lookup"><span data-stu-id="97d08-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="97d08-298">Når du skal evaluere denne modeltilknytning ved hjælp af metadata for en anden version af programmet, skal du registrere et andet tilsluttet program, tildele det denne modeltilknytning og validere det mod de nye metadata.</span><span class="sxs-lookup"><span data-stu-id="97d08-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97d08-299">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="97d08-299">Additional resources</span></span>

<span data-ttu-id="97d08-300">Du kan også afspille opgaveguiden **Klargøre programmetadata, der kan bruges i RCS** i programmet samt opgaveguiderne **Få adgang til programmetadata ved hjælp af ER-konfiguration** og **Få adgang til programmetadata ved hjælp af tilsluttede programmer** i RCS.</span><span class="sxs-lookup"><span data-stu-id="97d08-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="97d08-301">Disse opgaveguider kan downloades fra siden [Opgaveguider til elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="97d08-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]