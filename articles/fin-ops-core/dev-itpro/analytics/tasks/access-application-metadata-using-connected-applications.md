---
title: Få adgang til programmetadata ved hjælp af tilsluttede programmer
description: Fremgangsmåden i dette emne forklarer, hvordan en Regulatory Configuration Service-bruger kan designe en ny elektronisk rapporteringsmodel ved hjælp af metadata.
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b113f0db1d44dc5fbda30e10d62ff939550f299
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748687"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="a898f-103">Få adgang til programmetadata ved hjælp af tilsluttede programmer</span><span class="sxs-lookup"><span data-stu-id="a898f-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a898f-104">Følgende trin beskriver, hvordan en Regulatory Configuration Service-bruger i rollen Systemadministrator eller Udvikler til elektronisk rapportering kan designe en ny ER-modeltilknytning ved hjælp af metadataene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a898f-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="a898f-105">Du kan få adgang til programmetadata online ved hjælp af det RCS-tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="a898f-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="a898f-106">Eksempel på ER-modeltilknytning konfigureres til at give adgang til udenrigshandelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="a898f-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="a898f-107">For at fuldføre disse trin skal du i RCS først fuldføre trinnene i emnet [Opret konfigurationsudbydere og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a898f-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="a898f-108">Hvis du ikke har fuldført trinnene i emnet [Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), skal du gå til [eksempelsiden for elektroniske rapporter](https://go.microsoft.com/fwlink/?linkid=862266) for at hente og gemme følgende ER-konfigurationer: Udenrigshandelmetadata.xml, Udenrigshandelmodel.xml, Tilknytning af udenrigshandel.xml og derefter udføre trinnene i proceduren.</span><span class="sxs-lookup"><span data-stu-id="a898f-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a898f-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a898f-109">Prerequisites</span></span>
1. <span data-ttu-id="a898f-110">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a898f-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="a898f-111">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a898f-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a898f-112">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a898f-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="a898f-113">Få de nødvendige ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="a898f-113">Get required ER configurations</span></span>
1. <span data-ttu-id="a898f-114">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="a898f-115">Hvis du allerede har udført trinnene i proceduren [Få adgang til programmetadata ved hjælp af ER-konfiguration](access-application-metadata-er-configuration.md), har du allerede alle de nødvendige ER-konfigurationer (konfigurationer af metadata til udenrigshandel, model og tilknytning) i den aktuelle RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a898f-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="a898f-116">Du kan springe over resten af trinnene i denne underordnede opgave.</span><span class="sxs-lookup"><span data-stu-id="a898f-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="a898f-117">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="a898f-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="a898f-118">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a898f-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="a898f-119">Klik på **Gennemse**, og vælg filen **Udenrigshandelmetadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="a898f-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="a898f-120">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a898f-120">Click **OK**.</span></span> 
7. <span data-ttu-id="a898f-121">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="a898f-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="a898f-122">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a898f-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="a898f-123">Klik på **Gennemse**, og vælg filen **Udenrigshandelmodel.xml**.</span><span class="sxs-lookup"><span data-stu-id="a898f-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="a898f-124">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a898f-124">Click **OK**.</span></span> 
11. <span data-ttu-id="a898f-125">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="a898f-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="a898f-126">Klik på **Indlæs fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a898f-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="a898f-127">Klik på **Gennemse**, og vælg filen **Tilknytning af udenrigshandel.xml**.</span><span class="sxs-lookup"><span data-stu-id="a898f-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="a898f-128">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a898f-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="a898f-129">Registrere et tilsluttet program</span><span class="sxs-lookup"><span data-stu-id="a898f-129">Register a connected application</span></span>
1. <span data-ttu-id="a898f-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-130">Close the page.</span></span> 
2. <span data-ttu-id="a898f-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-131">Close the page.</span></span> 
3. <span data-ttu-id="a898f-132">Gå til **Alle arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a898f-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="a898f-133">Klik på **Tilsluttede programmer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="a898f-134">Sørg for, at det konfigurerede program er Azure-baseret og tilgængeligt for den aktuelle RCS-bruger.</span><span class="sxs-lookup"><span data-stu-id="a898f-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="a898f-135">Det kræves også, at den aktuelle RCS-bruger har adgang til det valgte program og er registreret som bruger af dette program og dermed får en rolle, som giver adgangsrettigheder til programmets metadata.</span><span class="sxs-lookup"><span data-stu-id="a898f-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="a898f-136">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a898f-136">Click **New**.</span></span> 
7. <span data-ttu-id="a898f-137">Skriv 'MyConnectedApp' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a898f-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="a898f-138">I feltet **Program** skal du skrive 'https://mycompany.operations.dynamics.com'.</span><span class="sxs-lookup"><span data-stu-id="a898f-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="a898f-139">Skriv 'mycompany.onmicrosoft.com' i feltet **Lejer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="a898f-140">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a898f-140">Click **Save**.</span></span> 
11. <span data-ttu-id="a898f-141">Når du kontrollerer forbindelsen til det konfigurerede program, skal du på siden **Opret forbindelse til eksternt program** klikke på linket **Klik her for at oprette forbindelse til det valgte eksterne program**.</span><span class="sxs-lookup"><span data-stu-id="a898f-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="a898f-142">Klik på **Kontrollér forbindelsen**.</span><span class="sxs-lookup"><span data-stu-id="a898f-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="a898f-143">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="a898f-143">Click **Close**.</span></span> 
14. <span data-ttu-id="a898f-144">Når forbindelsen er valideret korrekt, opdateres versions- og lejeroplysningerne for det konfigurerede program i det aktuelle gitter.</span><span class="sxs-lookup"><span data-stu-id="a898f-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="a898f-145">Gennemgå eksisterende modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="a898f-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="a898f-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-146">Close the page.</span></span> 
2. <span data-ttu-id="a898f-147">Klik på **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="a898f-148">Udvid **Udenrigshandelmodel** i træet.</span><span class="sxs-lookup"><span data-stu-id="a898f-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="a898f-149">I træet skal du vælge **Udenrigshandelmodel\Tilknytning af udenrigshandel**.</span><span class="sxs-lookup"><span data-stu-id="a898f-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="a898f-150">Udvid sektionen **Forudsætninger**.</span><span class="sxs-lookup"><span data-stu-id="a898f-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a898f-151">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a898f-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a898f-152">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="a898f-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="a898f-153">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="a898f-154">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="a898f-155">Vælg **Dynamics 365 for Operations\Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="a898f-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="a898f-156">Klik på **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="a898f-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="a898f-157">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="a898f-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a898f-158">I øjeblikket refererer denne tilknytning til metadatakonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a898f-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a898f-159">Der tilbydes programmetadata fra denne konfiguration, mens denne modeltilknytning bliver udformet.</span><span class="sxs-lookup"><span data-stu-id="a898f-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="a898f-160">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="a898f-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="a898f-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-161">Close the page.</span></span> 
13. <span data-ttu-id="a898f-162">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="a898f-163">Tildele modeltilknytning tilknyttet program</span><span class="sxs-lookup"><span data-stu-id="a898f-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="a898f-164">Klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a898f-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="a898f-165">Vælg **MyConnectedApp**-program.</span><span class="sxs-lookup"><span data-stu-id="a898f-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a898f-166">I øjeblikket refererer denne tilknytning til metadataene for det valgte tilsluttede program.</span><span class="sxs-lookup"><span data-stu-id="a898f-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="a898f-167">Når den samme tilknytning refererer til metadatakonfigurationen og det tilknyttede program samtidig, bruges metadata for det tilknyttede program.</span><span class="sxs-lookup"><span data-stu-id="a898f-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="a898f-168">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="a898f-169">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="a898f-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="a898f-170">Vælg **Dynamics 365 for Operations\Tabelposter** i træet.</span><span class="sxs-lookup"><span data-stu-id="a898f-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="a898f-171">Klik på **Tilføj rod**.</span><span class="sxs-lookup"><span data-stu-id="a898f-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="a898f-172">Indtast eller vælg en værdi i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="a898f-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a898f-173">Der tilbydes mere end to programtabeller nu, da denne tilknytning bruger alle de metadata, der er tildelt det tilknyttede program.</span><span class="sxs-lookup"><span data-stu-id="a898f-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="a898f-174">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="a898f-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="a898f-175">Klik på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a898f-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="a898f-176">Vi har bundet elementer i datamodellen til elementer i de datakilder, der er beskrevet, ved hjælp af oplysninger om metadata for det tilsluttede program, der er tildelt denne tilknytning.</span><span class="sxs-lookup"><span data-stu-id="a898f-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="a898f-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-177">Close the page.</span></span> 
11. <span data-ttu-id="a898f-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a898f-178">Close the page.</span></span> 

<span data-ttu-id="a898f-179">Når du har brug for at evaluere denne modeltilknytning ved hjælp af metadata for et andet versionsprogram, skal du registrere et andet tilknyttet program, tildele det denne modeltilknytning og validere det mod nye metadata.</span><span class="sxs-lookup"><span data-stu-id="a898f-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]