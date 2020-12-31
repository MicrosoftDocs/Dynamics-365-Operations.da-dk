---
title: Administrere ER-modeltilknytning i separate ER-konfigurationer
description: Følgende trin forklarer, hvordan en bruger, der er tildelt rollen som Systemadministrator eller Udvikler til elektronisk rapportering, kan administrere ER-modeltilknytninger i separate ER-konfigurationer.
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
ms.openlocfilehash: 4e59e9f2dd5a0fa6d5955e3d93d25759a478ede7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684421"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="d9d14-103">Administrere ER-modeltilknytning i separate ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="d9d14-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9d14-104">Følgende trin forklarer, hvordan en bruger, der er tildelt rollen som Systemadministrator eller Udvikler til elektronisk rapportering, kan administrere ER-modeltilknytninger i separate ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="d9d14-105">I denne opgaveguide skal du oprette de nødvendige ER konfigurationer for eksempelfirmaet Litware, Inc. For at fuldføre denne opgaveguide skal du først fuldføre trinnene i opgaveguiden "ER Oprette en konfigurationsudbyder" og markere den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d9d14-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="d9d14-106">Da ER-konfigurationer deles af firmaer, kan du fuldføre denne opgaveguide ved hjælp af et virksomhedsdatasæt efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="d9d14-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="d9d14-107">Funktionerne i denne opgaveguide er tilgængelig, hvis du har installeret et af følgende hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 til versionen Dynamics AX 7.0 eller https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 til versionen Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d9d14-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="d9d14-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d9d14-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d9d14-109">Kontrollér, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d9d14-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d9d14-110">Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i opgaveguiden Opret en konfigurationsudbyder, og markér den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d9d14-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="d9d14-111">Tilføj en ny ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d9d14-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="d9d14-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d9d14-113">Tilføj en ny modelkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-113">Add a new model configuration.</span></span> <span data-ttu-id="d9d14-114">Navnet skal være entydigt i konfigurationstræet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="d9d14-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d9d14-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d9d14-116">Skriv 'Eksempeldatamodel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="d9d14-117">Eksempeldatamodel</span><span class="sxs-lookup"><span data-stu-id="d9d14-117">Sample data model</span></span>  
4. <span data-ttu-id="d9d14-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-118">Click Create configuration.</span></span>
5. <span data-ttu-id="d9d14-119">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-119">Click Designer.</span></span>
6. <span data-ttu-id="d9d14-120">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d9d14-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d9d14-121">Skriv 'Root' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d9d14-122">Rod</span><span class="sxs-lookup"><span data-stu-id="d9d14-122">Root</span></span>  
8. <span data-ttu-id="d9d14-123">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d9d14-123">Click Add.</span></span>
9. <span data-ttu-id="d9d14-124">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d9d14-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d9d14-125">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d9d14-126">Regnskab</span><span class="sxs-lookup"><span data-stu-id="d9d14-126">Company</span></span>  
11. <span data-ttu-id="d9d14-127">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d9d14-127">Click Add.</span></span>
12. <span data-ttu-id="d9d14-128">I feltet Beskrivelse skal du angive teksten, beskrivelsen af den juridiske enhed eller det firma, hvor en bruger er logget på på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="d9d14-129">Beskrivelse af den juridiske enhed eller det firma, som en bruger loggede på på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="d9d14-130">Klik på Rodreference.</span><span class="sxs-lookup"><span data-stu-id="d9d14-130">Click Root reference.</span></span>
14. <span data-ttu-id="d9d14-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-131">Click OK.</span></span>
15. <span data-ttu-id="d9d14-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9d14-132">Click Save.</span></span>
16. <span data-ttu-id="d9d14-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-133">Close the page.</span></span>
17. <span data-ttu-id="d9d14-134">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="d9d14-134">Click Change status.</span></span>
18. <span data-ttu-id="d9d14-135">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="d9d14-135">Click Complete.</span></span>
19. <span data-ttu-id="d9d14-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="d9d14-137">Tilføje en ny ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="d9d14-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="d9d14-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d9d14-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d9d14-139">Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="d9d14-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="d9d14-140">Skriv 'Eksempeltilknytning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="d9d14-141">Eksempeltilknytning</span><span class="sxs-lookup"><span data-stu-id="d9d14-141">Sample mapping</span></span>  
4. <span data-ttu-id="d9d14-142">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-142">Click Create configuration.</span></span>
5. <span data-ttu-id="d9d14-143">Udvid eller skjul sektionen Forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="d9d14-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="d9d14-144">Forudsætningsgruppen Implementeringer er tilføjet automatisk.</span><span class="sxs-lookup"><span data-stu-id="d9d14-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="d9d14-145">Gruppen indeholder den påkrævede komponent, der refererer til den overordnede datamodelkonfiguration og er markeret som Implementering.</span><span class="sxs-lookup"><span data-stu-id="d9d14-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="d9d14-146">Det betyder, at denne tilknytningskonfiguration for eksempeltilknytningsmodellen betragtes som implementeringen af datamodellen Eksempeldatamodel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="d9d14-147">Denne komponent tvinger derfor ER til at hente modeltilknytningskonfigurationen Eksempeltilknytning fra et ER-lager, når modelkonfigurationen Eksempeldatamodel hentes.</span><span class="sxs-lookup"><span data-stu-id="d9d14-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="d9d14-148">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-148">Click Designer.</span></span>
    * <span data-ttu-id="d9d14-149">Den oprettede modeltilknytningskonfiguration indeholder en ny tom tilknytning med samme navn som den oprettede konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="d9d14-150">Når en valgt overordnet models konfiguration indeholder modeltilknytninger, kopieres de til en ny modeltilknytningskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="d9d14-151">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-151">Click Designer.</span></span>
8. <span data-ttu-id="d9d14-152">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d9d14-153">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="d9d14-153">Click Add root.</span></span>
10. <span data-ttu-id="d9d14-154">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d9d14-155">Regnskab</span><span class="sxs-lookup"><span data-stu-id="d9d14-155">Company</span></span>  
11. <span data-ttu-id="d9d14-156">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d9d14-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d9d14-157">CompanyInfo</span></span>  
12. <span data-ttu-id="d9d14-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-158">Click OK.</span></span>
13. <span data-ttu-id="d9d14-159">Udvid 'Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="d9d14-160">Udvid 'Firma\find()' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="d9d14-161">Vælg 'Firma\find()\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="d9d14-162">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d9d14-162">Click Bind.</span></span>
17. <span data-ttu-id="d9d14-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9d14-163">Click Save.</span></span>
18. <span data-ttu-id="d9d14-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-164">Close the page.</span></span>
19. <span data-ttu-id="d9d14-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-165">Close the page.</span></span>
20. <span data-ttu-id="d9d14-166">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="d9d14-167">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="d9d14-167">Click User parameters.</span></span>
22. <span data-ttu-id="d9d14-168">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="d9d14-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-169">Click OK.</span></span>
24. <span data-ttu-id="d9d14-170">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d9d14-170">Click Edit.</span></span>
25. <span data-ttu-id="d9d14-171">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d9d14-172">Tilføje en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d9d14-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d9d14-173">Vælg 'Eksempeldatamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d9d14-174">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d9d14-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d9d14-175">Skriv 'Format baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="d9d14-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d9d14-176">Skriv 'Eksempelformat' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="d9d14-177">Eksempelformat</span><span class="sxs-lookup"><span data-stu-id="d9d14-177">Sample format</span></span>  
5. <span data-ttu-id="d9d14-178">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-178">Click Create configuration.</span></span>
6. <span data-ttu-id="d9d14-179">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-179">Click Designer.</span></span>
7. <span data-ttu-id="d9d14-180">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d9d14-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="d9d14-181">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="d9d14-182">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-182">Click OK.</span></span>
10. <span data-ttu-id="d9d14-183">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="d9d14-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="d9d14-184">Udvid 'model' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="d9d14-185">Vælg 'model\Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="d9d14-186">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="d9d14-186">Click Bind.</span></span>
14. <span data-ttu-id="d9d14-187">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9d14-187">Click Save.</span></span>
15. <span data-ttu-id="d9d14-188">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-188">Close the page.</span></span>
    * <span data-ttu-id="d9d14-189">Kør kladdeversionen af det oprettede format med henblik på test.</span><span class="sxs-lookup"><span data-stu-id="d9d14-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="d9d14-190">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="d9d14-190">Click Run.</span></span>
    * <span data-ttu-id="d9d14-191">Klik på Kør i oversigtspanelet Versioner.</span><span class="sxs-lookup"><span data-stu-id="d9d14-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="d9d14-192">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-192">Click OK.</span></span>
    * <span data-ttu-id="d9d14-193">Gennemse det output, der indeholder navnet på det firma, som den bruger, der kører denne formatkonfiguration, er logget på.</span><span class="sxs-lookup"><span data-stu-id="d9d14-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="d9d14-194">Den oprettede modeltilknytningskonfiguration bruges af denne formatkonfiguration, fordi der kun er én tilgængelig konfiguration, der indeholder de nødvendige modeltilknytninger.</span><span class="sxs-lookup"><span data-stu-id="d9d14-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="d9d14-195">Tilføje en alternativ ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="d9d14-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="d9d14-196">Vælg 'Eksempeldatamodel' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d9d14-197">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d9d14-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d9d14-198">Skriv 'Modeltilknytning baseret på datamodel af typen Eksempeldatamodel' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="d9d14-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d9d14-199">Skriv 'Eksempeltilknytning (alternativ)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="d9d14-200">Eksempeltilknytning (alternativ)</span><span class="sxs-lookup"><span data-stu-id="d9d14-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="d9d14-201">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9d14-201">Click Create configuration.</span></span>
6. <span data-ttu-id="d9d14-202">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-202">Click Designer.</span></span>
7. <span data-ttu-id="d9d14-203">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="d9d14-203">Click Designer.</span></span>
8. <span data-ttu-id="d9d14-204">Vælg 'Dynamics 365 for Operations\Tabel' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d9d14-205">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="d9d14-205">Click Add root.</span></span>
10. <span data-ttu-id="d9d14-206">Skriv "Firma" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d9d14-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d9d14-207">Regnskab</span><span class="sxs-lookup"><span data-stu-id="d9d14-207">Company</span></span>  
11. <span data-ttu-id="d9d14-208">Skriv "CompanyInfo" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d9d14-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d9d14-209">CompanyInfo</span></span>  
12. <span data-ttu-id="d9d14-210">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-210">Click OK.</span></span>
13. <span data-ttu-id="d9d14-211">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d9d14-211">Click Edit.</span></span>
14. <span data-ttu-id="d9d14-212">Vælg '"Streng\SAMMENKÆD" i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="d9d14-213">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="d9d14-213">Click Add function.</span></span>
16. <span data-ttu-id="d9d14-214">Udvid 'Firma' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="d9d14-215">Udvid 'Firma\find()' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="d9d14-216">Vælg 'Firma\find()\Navn' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="d9d14-217">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="d9d14-217">Click Add data source.</span></span>
20. <span data-ttu-id="d9d14-218">Skriv en værdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d9d14-219">CONCATENATE(Firma.'find()'.Navn, ";",</span><span class="sxs-lookup"><span data-stu-id="d9d14-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="d9d14-220">Vælg 'Firma\find()\Firma(DataArea)' i træet.</span><span class="sxs-lookup"><span data-stu-id="d9d14-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="d9d14-221">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="d9d14-221">Click Add data source.</span></span>
23. <span data-ttu-id="d9d14-222">Skriv en værdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d9d14-223">CONCATENATE(Firma.'find()'. Navn, ";", Firma.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="d9d14-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="d9d14-224">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9d14-224">Click Save.</span></span>
25. <span data-ttu-id="d9d14-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-225">Close the page.</span></span>
26. <span data-ttu-id="d9d14-226">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d9d14-226">Click Save.</span></span>
27. <span data-ttu-id="d9d14-227">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-227">Close the page.</span></span>
28. <span data-ttu-id="d9d14-228">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d9d14-228">Close the page.</span></span>
29. <span data-ttu-id="d9d14-229">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="d9d14-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="d9d14-230">Bruge en eksisterende ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="d9d14-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="d9d14-231">Vælg i træet 'Eksempeldatamodel\Eksempelformat'.</span><span class="sxs-lookup"><span data-stu-id="d9d14-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="d9d14-232">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="d9d14-232">Click Run.</span></span>
    * <span data-ttu-id="d9d14-233">Den valgte kladdeversion af ER-formatkonfigurationen ikke kan udføres, fordi der findes mere end én konfiguration af modeltilknytningen til den udefinerede datamodel, der er valgt som datakilde for det ER-format, der køres.</span><span class="sxs-lookup"><span data-stu-id="d9d14-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="d9d14-234">Som det næste skal du definere den alternative modeltilknytningskonfiguration som den, hvorfra modeltilknytninger bliver brugt som datakilder ved kørsel af ER-format.</span><span class="sxs-lookup"><span data-stu-id="d9d14-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="d9d14-235">Vælg i træet 'Eksempeldatamodel\Eksempeltilknytning (alternativ)'.</span><span class="sxs-lookup"><span data-stu-id="d9d14-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="d9d14-236">Vælg Ja i feltet Standard for modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="d9d14-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="d9d14-237">Vælg i træet 'Eksempeldatamodel\Eksempelformat'.</span><span class="sxs-lookup"><span data-stu-id="d9d14-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="d9d14-238">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="d9d14-238">Click Run.</span></span>
7. <span data-ttu-id="d9d14-239">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d9d14-239">Click OK.</span></span>
    * <span data-ttu-id="d9d14-240">Standardkonfigurationen for modeltilknytningen bruges af denne formatkonfiguration til oprettelse af det elektroniske dokument (det oprettede output indeholder firmakoden).</span><span class="sxs-lookup"><span data-stu-id="d9d14-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

