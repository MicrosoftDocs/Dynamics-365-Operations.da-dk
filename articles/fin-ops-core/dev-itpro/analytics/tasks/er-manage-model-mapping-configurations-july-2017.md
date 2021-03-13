---
title: Administrere ER-modeltilknytning i separate ER-konfigurationer
description: I dette emne beskrives, hvordan du administrerer ER-modeltilknytninger i separate ER-konfigurationer af elektronisk rapportering.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f1013cfc9f421525fb0661cd5ace5eeaa157f9a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093792"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="dc975-103">Administrere ER-modeltilknytning i separate ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="dc975-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc975-104">Følgende trin forklarer, hvordan en bruger, der er tildelt rollen som Systemadministrator eller Udvikler til elektronisk rapportering, kan administrere ER-modeltilknytninger i separate ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="dc975-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="dc975-105">I denne opgaveguide skal du oprette de nødvendige ER konfigurationer for eksempelfirmaet Litware, Inc. For at fuldføre denne opgaveguide skal du først fuldføre trinnene i opgaveguiden "ER Oprette en konfigurationsudbyder" og markere den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="dc975-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="dc975-106">Da ER-konfigurationer deles af firmaer, kan du fuldføre denne opgaveguide ved hjælp af et virksomhedsdatasæt efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="dc975-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="dc975-107">Funktionerne i denne opgaveguide er tilgængelig, hvis du har installeret et af følgende hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 til versionen Dynamics AX 7.0 eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 til versionen Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="dc975-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="dc975-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="dc975-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="dc975-109">Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="dc975-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="dc975-110">Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i opgaveguiden Opret en konfigurationsudbyder, og markér den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="dc975-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="dc975-111">Tilføj en ny ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc975-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="dc975-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="dc975-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="dc975-113">Tilføj en ny modelkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-113">Add a new model configuration.</span></span> <span data-ttu-id="dc975-114">Navnet skal være entydigt i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="dc975-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="dc975-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc975-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="dc975-116">Skriv 'Eksempeldatamodel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="dc975-117">Eksempeldatamodel</span><span class="sxs-lookup"><span data-stu-id="dc975-117">Sample data model</span></span>  
4. <span data-ttu-id="dc975-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-118">Click Create configuration.</span></span>
5. <span data-ttu-id="dc975-119">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-119">Click Designer.</span></span>
6. <span data-ttu-id="dc975-120">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc975-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="dc975-121">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="dc975-122">Rod</span><span class="sxs-lookup"><span data-stu-id="dc975-122">Root</span></span>  
8. <span data-ttu-id="dc975-123">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="dc975-123">Click Add.</span></span>
9. <span data-ttu-id="dc975-124">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="dc975-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="dc975-125">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="dc975-126">Regnskab</span><span class="sxs-lookup"><span data-stu-id="dc975-126">Company</span></span>  
11. <span data-ttu-id="dc975-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="dc975-127">Click Add.</span></span>
12. <span data-ttu-id="dc975-128">I feltet Beskrivelse skal du angive teksten, beskrivelsen af den juridiske enhed eller det firma, hvor en bruger er logget på på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="dc975-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="dc975-129">Beskrivelse af den juridiske enhed eller det firma, som en bruger loggede på på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="dc975-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="dc975-130">Klik på Rodreference.</span><span class="sxs-lookup"><span data-stu-id="dc975-130">Click Root reference.</span></span>
14. <span data-ttu-id="dc975-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-131">Click OK.</span></span>
15. <span data-ttu-id="dc975-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="dc975-132">Click Save.</span></span>
16. <span data-ttu-id="dc975-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-133">Close the page.</span></span>
17. <span data-ttu-id="dc975-134">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="dc975-134">Click Change status.</span></span>
18. <span data-ttu-id="dc975-135">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="dc975-135">Click Complete.</span></span>
19. <span data-ttu-id="dc975-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="dc975-137">Tilføje en ny ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc975-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="dc975-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc975-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="dc975-139">Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="dc975-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="dc975-140">Skriv 'Eksempeltilknytning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="dc975-141">Eksempeltilknytning</span><span class="sxs-lookup"><span data-stu-id="dc975-141">Sample mapping</span></span>  
4. <span data-ttu-id="dc975-142">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-142">Click Create configuration.</span></span>
5. <span data-ttu-id="dc975-143">Udvid eller skjul sektionen Forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="dc975-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="dc975-144">Forudsætningsgruppen Implementeringer er tilføjet automatisk.</span><span class="sxs-lookup"><span data-stu-id="dc975-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="dc975-145">Gruppen indeholder den påkrævede komponent, der refererer til den overordnede datamodelkonfiguration og er markeret som Implementering.</span><span class="sxs-lookup"><span data-stu-id="dc975-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="dc975-146">Det betyder, at denne tilknytningskonfiguration for eksempeltilknytningsmodellen betragtes som implementeringen af datamodellen Eksempeldatamodel.</span><span class="sxs-lookup"><span data-stu-id="dc975-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="dc975-147">Denne komponent tvinger derfor ER til at hente modeltilknytningskonfigurationen Eksempeltilknytning fra et ER-lager, når modelkonfigurationen Eksempeldatamodel hentes.</span><span class="sxs-lookup"><span data-stu-id="dc975-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="dc975-148">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-148">Click Designer.</span></span>
    * <span data-ttu-id="dc975-149">Den oprettede modeltilknytningskonfiguration indeholder en ny tom tilknytning med samme navn som den oprettede konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="dc975-150">Når en valgt overordnet models konfiguration indeholder modeltilknytninger, kopieres de til en ny modeltilknytningskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="dc975-151">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-151">Click Designer.</span></span>
8. <span data-ttu-id="dc975-152">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="dc975-153">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="dc975-153">Click Add root.</span></span>
10. <span data-ttu-id="dc975-154">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="dc975-155">Regnskab</span><span class="sxs-lookup"><span data-stu-id="dc975-155">Company</span></span>  
11. <span data-ttu-id="dc975-156">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="dc975-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="dc975-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="dc975-157">CompanyInfo</span></span>  
12. <span data-ttu-id="dc975-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-158">Click OK.</span></span>
13. <span data-ttu-id="dc975-159">Udvid 'Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="dc975-160">Udvid 'Firma\find()' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="dc975-161">Vælg 'Firma\find()\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="dc975-162">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="dc975-162">Click Bind.</span></span>
17. <span data-ttu-id="dc975-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="dc975-163">Click Save.</span></span>
18. <span data-ttu-id="dc975-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-164">Close the page.</span></span>
19. <span data-ttu-id="dc975-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-165">Close the page.</span></span>
20. <span data-ttu-id="dc975-166">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="dc975-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="dc975-167">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="dc975-167">Click User parameters.</span></span>
22. <span data-ttu-id="dc975-168">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="dc975-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="dc975-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-169">Click OK.</span></span>
24. <span data-ttu-id="dc975-170">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="dc975-170">Click Edit.</span></span>
25. <span data-ttu-id="dc975-171">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="dc975-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="dc975-172">Tilføje en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc975-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="dc975-173">Vælg 'Eksempeldatamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="dc975-174">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc975-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="dc975-175">Skriv 'Format baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="dc975-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="dc975-176">Skriv 'Eksempelformat' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="dc975-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="dc975-177">Sample format</span></span>  
5. <span data-ttu-id="dc975-178">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-178">Click Create configuration.</span></span>
6. <span data-ttu-id="dc975-179">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-179">Click Designer.</span></span>
7. <span data-ttu-id="dc975-180">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc975-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="dc975-181">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="dc975-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-182">Click OK.</span></span>
10. <span data-ttu-id="dc975-183">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="dc975-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="dc975-184">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="dc975-185">Vælg 'model\Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="dc975-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="dc975-186">Click Bind.</span></span>
14. <span data-ttu-id="dc975-187">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="dc975-187">Click Save.</span></span>
15. <span data-ttu-id="dc975-188">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-188">Close the page.</span></span>
    * <span data-ttu-id="dc975-189">Kør kladdeversionen af det oprettede format med henblik på test.</span><span class="sxs-lookup"><span data-stu-id="dc975-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="dc975-190">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="dc975-190">Click Run.</span></span>
    * <span data-ttu-id="dc975-191">Klik på Kør i oversigtspanelet Versioner.</span><span class="sxs-lookup"><span data-stu-id="dc975-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="dc975-192">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-192">Click OK.</span></span>
    * <span data-ttu-id="dc975-193">Gennemse det output, der indeholder navnet på det firma, som den bruger, der kører denne formatkonfiguration, er logget på.</span><span class="sxs-lookup"><span data-stu-id="dc975-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="dc975-194">Den oprettede modeltilknytningskonfiguration bruges af denne formatkonfiguration, fordi der kun er én tilgængelig konfiguration, der indeholder de nødvendige modeltilknytninger.</span><span class="sxs-lookup"><span data-stu-id="dc975-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="dc975-195">Tilføje en alternativ ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc975-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="dc975-196">Vælg 'Eksempeldatamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="dc975-197">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="dc975-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="dc975-198">Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="dc975-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="dc975-199">Skriv 'Eksempeltilknytning (alternativ)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="dc975-200">Eksempeltilknytning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="dc975-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="dc975-201">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc975-201">Click Create configuration.</span></span>
6. <span data-ttu-id="dc975-202">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-202">Click Designer.</span></span>
7. <span data-ttu-id="dc975-203">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="dc975-203">Click Designer.</span></span>
8. <span data-ttu-id="dc975-204">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="dc975-205">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="dc975-205">Click Add root.</span></span>
10. <span data-ttu-id="dc975-206">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="dc975-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="dc975-207">Regnskab</span><span class="sxs-lookup"><span data-stu-id="dc975-207">Company</span></span>  
11. <span data-ttu-id="dc975-208">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="dc975-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="dc975-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="dc975-209">CompanyInfo</span></span>  
12. <span data-ttu-id="dc975-210">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-210">Click OK.</span></span>
13. <span data-ttu-id="dc975-211">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="dc975-211">Click Edit.</span></span>
14. <span data-ttu-id="dc975-212">Vælg '"Streng\SAMMENKÆD" i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="dc975-213">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="dc975-213">Click Add function.</span></span>
16. <span data-ttu-id="dc975-214">Udvid 'Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="dc975-215">Udvid 'Firma\find()' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="dc975-216">Vælg 'Firma\find()\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="dc975-217">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="dc975-217">Click Add data source.</span></span>
20. <span data-ttu-id="dc975-218">Skriv en værdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="dc975-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="dc975-219">CONCATENATE(Firma.'find()'.Navn, ";",</span><span class="sxs-lookup"><span data-stu-id="dc975-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="dc975-220">Vælg 'Firma\find()\Firma(DataArea)' i træet.</span><span class="sxs-lookup"><span data-stu-id="dc975-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="dc975-221">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="dc975-221">Click Add data source.</span></span>
23. <span data-ttu-id="dc975-222">Skriv en værdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="dc975-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="dc975-223">CONCATENATE(Firma.'find()'. Navn, ";", Firma.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="dc975-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="dc975-224">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="dc975-224">Click Save.</span></span>
25. <span data-ttu-id="dc975-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-225">Close the page.</span></span>
26. <span data-ttu-id="dc975-226">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="dc975-226">Click Save.</span></span>
27. <span data-ttu-id="dc975-227">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-227">Close the page.</span></span>
28. <span data-ttu-id="dc975-228">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="dc975-228">Close the page.</span></span>
29. <span data-ttu-id="dc975-229">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="dc975-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="dc975-230">Bruge en eksisterende ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="dc975-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="dc975-231">Vælg i træet 'Eksempeldatamodel\Eksempelformat'.</span><span class="sxs-lookup"><span data-stu-id="dc975-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="dc975-232">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="dc975-232">Click Run.</span></span>
    * <span data-ttu-id="dc975-233">Den valgte kladdeversion af ER-formatkonfigurationen ikke kan udføres, fordi der findes mere end én konfiguration af modeltilknytningen til den udefinerede datamodel, der er valgt som datakilde for det ER-format, der køres.</span><span class="sxs-lookup"><span data-stu-id="dc975-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="dc975-234">Som det næste skal du definere den alternative modeltilknytningskonfiguration som den, hvorfra modeltilknytninger bliver brugt som datakilder ved kørsel af ER-format.</span><span class="sxs-lookup"><span data-stu-id="dc975-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="dc975-235">Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.</span><span class="sxs-lookup"><span data-stu-id="dc975-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="dc975-236">Vælg Ja i feltet Standard for modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="dc975-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="dc975-237">Vælg i træet 'Eksempeldatamodel\Eksempelformat'.</span><span class="sxs-lookup"><span data-stu-id="dc975-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="dc975-238">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="dc975-238">Click Run.</span></span>
7. <span data-ttu-id="dc975-239">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="dc975-239">Click OK.</span></span>
    * <span data-ttu-id="dc975-240">Standardkonfigurationen for modeltilknytningen bruges af denne formatkonfiguration til oprettelse af det elektroniske dokument (det oprettede output indeholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="dc975-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

