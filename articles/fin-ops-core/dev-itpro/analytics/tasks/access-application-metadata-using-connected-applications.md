---
title: Få adgang til programmetadata ved hjælp af tilsluttede programmer
description: Fremgangsmåden i dette emne forklarer, hvordan en Regulatory Configuration Service-bruger (RCS) kan designe en ny elektronisk rapporteringsmodel (ER) ved hjælp af metadata i Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
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
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182709"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="94985-103">Få adgang til programmetadata ved hjælp af tilsluttede programmer</span><span class="sxs-lookup"><span data-stu-id="94985-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94985-104">Følgende trin beskriver, hvordan en RCS-bruger (Regulatory Configuration Service) i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe en ny ER-modeltilknytning ved hjælp af metadataene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="94985-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="94985-105">Du kan få adgang til programmetadata online ved hjælp af det RCS-tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="94985-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="94985-106">Eksempel på ER-modeltilknytning konfigureres til at give adgang til udenrigshandelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="94985-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="94985-107">Du skal først fuldføre RCS-trinnene i emnet [Opret en konfigurationsudbyder, og markér den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="94985-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="94985-108">Hvis du ikke har fuldført trinnene i emnet [Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), skal du gå til [eksempelsiden for elektroniske rapporter](https://go.microsoft.com/fwlink/?linkid=862266) for at hente og gemme følgende ER-konfigurationer: Udenrigshandelmetadata.xml, Udenrigshandelmodel.xml, Tilknytning af udenrigshandel.xml og derefter udføre trinnene i proceduren.</span><span class="sxs-lookup"><span data-stu-id="94985-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="94985-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="94985-109">Prerequisites</span></span>
1. <span data-ttu-id="94985-110">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="94985-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="94985-111">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="94985-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="94985-112">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret en konfigurationsudbyder, og markér den som aktiv](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="94985-112">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="94985-113">Få de nødvendige ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="94985-113">Get required ER configurations</span></span>
1. <span data-ttu-id="94985-114">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="94985-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="94985-115">Hvis du allerede har udført trinnene i proceduren [(RCS) Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), har du allerede alle de nødvendige ER-konfigurationer (konfigurationer af metadata til udenrigshandel, model og tilknytning) i den aktuelle RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="94985-115">If you already completed the steps in the [(RCS) Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="94985-116">Du kan springe over resten af trinnene i denne underordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="94985-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="94985-117">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="94985-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="94985-118">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="94985-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="94985-119">Klik på **Gennemse**, og vælg filen **Udenrigshandelmetadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="94985-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="94985-120">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94985-120">Click **OK**.</span></span> 
7. <span data-ttu-id="94985-121">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="94985-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="94985-122">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="94985-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="94985-123">Klik på **Gennemse**, og vælg filen **Udenrigshandelmodel.xml**.</span><span class="sxs-lookup"><span data-stu-id="94985-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="94985-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94985-124">Click **OK**.</span></span> 
11. <span data-ttu-id="94985-125">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="94985-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="94985-126">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="94985-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="94985-127">Klik på **Gennemse**, og vælg filen **Tilknytning af udenrigshandel.xml**.</span><span class="sxs-lookup"><span data-stu-id="94985-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="94985-128">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="94985-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="94985-129">Registrere et tilsluttet program</span><span class="sxs-lookup"><span data-stu-id="94985-129">Register a connected application</span></span>
1. <span data-ttu-id="94985-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-130">Close the page.</span></span> 
2. <span data-ttu-id="94985-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-131">Close the page.</span></span> 
3. <span data-ttu-id="94985-132">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="94985-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="94985-133">Klik på **Tilsluttede programmer**.</span><span class="sxs-lookup"><span data-stu-id="94985-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="94985-134">Sørg for, at det konfigurerede program er Azura-baseret og tilgængeligt for den aktuelle RCS-bruger.</span><span class="sxs-lookup"><span data-stu-id="94985-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="94985-135">Det kræves også, at den aktuelle RCS-bruger har adgang til det valgte program og er registreret som bruger af dette program, der spiller en rolle, som giver adgangsrettigheder til programmets metadata.</span><span class="sxs-lookup"><span data-stu-id="94985-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="94985-136">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="94985-136">Click **New**.</span></span> 
7. <span data-ttu-id="94985-137">Skriv 'MyConnectedApp' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="94985-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="94985-138">I feltet **Program** skal du skrive 'https://mycompany.operations.dynamics.com'.</span><span class="sxs-lookup"><span data-stu-id="94985-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="94985-139">Skriv 'mycompany.onmicrosoft.com' i feltet **Lejer**.</span><span class="sxs-lookup"><span data-stu-id="94985-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="94985-140">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="94985-140">Click **Save**.</span></span> 
11. <span data-ttu-id="94985-141">Når du kontrollerer forbindelsen til det konfigurerede program, skal du på siden **Opret forbindelse til eksternt program** klikke på linket **Klik her for at oprette forbindelse til det valgte eksterne program**.</span><span class="sxs-lookup"><span data-stu-id="94985-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="94985-142">Klik på **Kontrollér forbindelsen**.</span><span class="sxs-lookup"><span data-stu-id="94985-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="94985-143">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="94985-143">Click **Close**.</span></span> 
14. <span data-ttu-id="94985-144">Når forbindelsen er valideret korrekt, opdateres versions- og lejeroplysningerne for det konfigurerede program i det aktuelle gitter.</span><span class="sxs-lookup"><span data-stu-id="94985-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="94985-145">Gennemgå eksisterende modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="94985-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="94985-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-146">Close the page.</span></span> 
2. <span data-ttu-id="94985-147">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="94985-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="94985-148">Udvid **Udenrigshandelmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="94985-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="94985-149">I træet skal du vælge **Udenrigshandelmodel\Tilknytning af udenrigshandel**.</span><span class="sxs-lookup"><span data-stu-id="94985-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="94985-150">Udvid sektionen **Forudsætninger**.</span><span class="sxs-lookup"><span data-stu-id="94985-150">Expand the **Prerequisites** section.</span></span> 

> [!NOTE]
> <span data-ttu-id="94985-151">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="94985-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="94985-152">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="94985-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="94985-153">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="94985-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="94985-154">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="94985-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="94985-155">Vælg **Dynamics 365 for Operations\Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="94985-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="94985-156">Klik på **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="94985-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="94985-157">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="94985-157">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="94985-158">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="94985-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="94985-159">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="94985-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="94985-160">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="94985-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="94985-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-161">Close the page.</span></span> 
13. <span data-ttu-id="94985-162">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="94985-163">Tildele modeltilknytning tilknyttet program</span><span class="sxs-lookup"><span data-stu-id="94985-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="94985-164">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="94985-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="94985-165">Vælg **MyConnectedApp**-program.</span><span class="sxs-lookup"><span data-stu-id="94985-165">Select **MyConnectedApp** application.</span></span> 

> [!NOTE]
> <span data-ttu-id="94985-166">I øjeblikket refererer denne tilknytning til metadataene for det valgte tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="94985-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="94985-167">Når den samme tilknytning refererer til metadatakonfigurationen og det tilknyttede program samtidig, bruges metadata for det tilknyttede program.</span><span class="sxs-lookup"><span data-stu-id="94985-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="94985-168">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="94985-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="94985-169">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="94985-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="94985-170">Vælg **Dynamics 365 for Operations\Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="94985-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="94985-171">Klik på **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="94985-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="94985-172">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="94985-172">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="94985-173">Der tilbydes mere end to programtabeller nu, da denne tilknytning bruger alle de metadata, der er tildelt det tilknyttede program.</span><span class="sxs-lookup"><span data-stu-id="94985-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="94985-174">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="94985-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="94985-175">Klik på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="94985-175">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="94985-176">Vi har bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om metadata for det tilsluttede program, der er tildelt denne tilknytning.</span><span class="sxs-lookup"><span data-stu-id="94985-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="94985-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-177">Close the page.</span></span> 
11. <span data-ttu-id="94985-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="94985-178">Close the page.</span></span> 

<span data-ttu-id="94985-179">Når du har brug for at evaluere denne modeltilknytning ved hjælp af metadata for et andet versionsprogram, skal du registrere et andet tilknyttet program, tildele det denne modeltilknytning og validere det mod nye metadata.</span><span class="sxs-lookup"><span data-stu-id="94985-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
