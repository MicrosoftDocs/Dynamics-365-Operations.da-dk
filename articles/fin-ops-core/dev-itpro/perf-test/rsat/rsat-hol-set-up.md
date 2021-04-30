---
title: Konfigurere og installere selvstudium til Regression Suite Automation Tool
description: Dette emne er et selvstudium, der viser, hvordan du kan konfigurere og installere Regression Suite Automation Tool (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c6e4dcbd854cfadbc34f0040dcffd277d32a8d9
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909028"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="a9a24-103">Konfigurere og installere selvstudium til Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="a9a24-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="a9a24-104">Dette emne er et selvstudium, der hjælper dig med konfigurere og komme i gang med RSAT og de værktøjer, der er knyttet til brugen af RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a9a24-105">Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format.</span><span class="sxs-lookup"><span data-stu-id="a9a24-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="a9a24-106">Nøglebegreber</span><span class="sxs-lookup"><span data-stu-id="a9a24-106">Key concepts</span></span>

- <span data-ttu-id="a9a24-107">Forstå den opsætning af installation og forudsætning , der kræves til de forskellige programmer, som understøtter Regression Suite Automation Tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="a9a24-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="a9a24-108">Forstå, hvordan du kan bruge funktionen Arbejdsrutineoptager sammen med Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps til at oprette, konfigurere, køre, undersøge og rapportere om testsager.</span><span class="sxs-lookup"><span data-stu-id="a9a24-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="a9a24-109">Giv funktionelle brugere mulighed for at registrere forretningsopgaver ved hjælp af Arbejdsrutineoptager og derefter konvertere opgaveregistreringerne til en pakke af automatiske test uden at skulle skrive kildekode.</span><span class="sxs-lookup"><span data-stu-id="a9a24-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a9a24-110">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="a9a24-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a9a24-111">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a9a24-111">Prerequisites</span></span>

- <span data-ttu-id="a9a24-112">Der kræves et miljø, der kører Microsoft Dynamics 365 for Finance and Operations version 10.0 (april 2019) eller nyere, til dette selvstudium.</span><span class="sxs-lookup"><span data-stu-id="a9a24-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="a9a24-113">For kunder, der bruger Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3, er Platform update 20 (PU20) eller nyere også understøttet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="a9a24-114">Brugeren skal have administratorrettigheder til miljøet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="a9a24-115">Du skal have adgang til kundens lejer-LCS og Azure DevOps (tidligere kaldet Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="a9a24-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="a9a24-116">Den bruger, der opretter og administrerer testpakker, skal have licens til Azure DevOps Test Plans eller Test Manager.</span><span class="sxs-lookup"><span data-stu-id="a9a24-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="a9a24-117">Følgende licenser giver dig også adgang til Test Plans:</span><span class="sxs-lookup"><span data-stu-id="a9a24-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="a9a24-118">Visual Studio Enterprise-licens</span><span class="sxs-lookup"><span data-stu-id="a9a24-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="a9a24-119">Visual Studio Test Professional-licens</span><span class="sxs-lookup"><span data-stu-id="a9a24-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="a9a24-120">Abonnementslicens til MSDN-platforme</span><span class="sxs-lookup"><span data-stu-id="a9a24-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="a9a24-121">RSAT skal have adgang til testmiljøet via en webbrowser.</span><span class="sxs-lookup"><span data-stu-id="a9a24-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="a9a24-122">Hvis du vil generere og redigere testparametre, skal du have Microsoft Excel installeret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="a9a24-123">Konfigurer Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="a9a24-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="a9a24-124">Brugerberettigelse</span><span class="sxs-lookup"><span data-stu-id="a9a24-124">User eligibility</span></span>

<span data-ttu-id="a9a24-125">Sørg for, at brugeren er oprettet i Azure DevOps og har et abonnementsniveau, der giver adgang til Azure Test Plans.</span><span class="sxs-lookup"><span data-stu-id="a9a24-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="a9a24-126">Der kræves kun en licens til Azure DevOps Test Plans, hvis brugeren opretter og administrerer testsager (så ikke alle RSAT-brugere kræver denne licens).</span><span class="sxs-lookup"><span data-stu-id="a9a24-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="a9a24-127">Oplysninger om licenskravene finder du under [Licenskrav](/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="a9a24-127">For information about the license requirements, see [License requirements](/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="a9a24-128">Opret et nyt Azure DevOps-projekt</span><span class="sxs-lookup"><span data-stu-id="a9a24-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="a9a24-129">RSAT bruger Azure Devops til styring af testsager og testpakker, rapportering og undersøgelse af testkørselsresultater.</span><span class="sxs-lookup"><span data-stu-id="a9a24-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-130">Du kan bruge et eksisterende Azure DevOps-projekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="a9a24-131">Men hvis det eksisterende Azure DevOps-projekt er konfigureret, så det har en brugerdefineret skabelon, får du vist en "VSTS-synkroniseringsfejl", når du synkroniserer testsager fra Forretningsmodeldesigner (BPM) til Azure DevOps (se afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="a9a24-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="a9a24-132">Hvis følgende bedste fremgangsmåder er blevet fulgt for den brugerdefinerede skabelon, kan du synkronisere testsagerne til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="a9a24-133">(Disse bedste fremgangsmåder vises i fejlmeddelelsen).</span><span class="sxs-lookup"><span data-stu-id="a9a24-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="a9a24-134">Slet ikke nogen arbejdselementtyper eller indbyggede felter.</span><span class="sxs-lookup"><span data-stu-id="a9a24-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="a9a24-135">Slet ikke nogen tilstand af en arbejdselementtype.</span><span class="sxs-lookup"><span data-stu-id="a9a24-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="a9a24-136">Føj ikke nogen påkrævede felter til en arbejdselementtype.</span><span class="sxs-lookup"><span data-stu-id="a9a24-136">Do not add any required fields to a work item type.</span></span>

![Fejlmeddelelse med en liste over bedste fremgangsmåder](./media/setup_rsa_tool_02.png)

<span data-ttu-id="a9a24-138">For dette selvstudium anbefales det ellers, at du opretter et nyt Azure DevOps-projekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="a9a24-139">Yderligere oplysninger finder du under [Problemer under synkronisering af BPM ved at bruge en brugerdefineret Azure DevOps-processkabelon (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="a9a24-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="a9a24-140">Åbn Azure DevOps-URL-adressen (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="a9a24-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="a9a24-141">Vælg **Opret projekt** i øverste højre hjørne af Azure DevOps-siden.</span><span class="sxs-lookup"><span data-stu-id="a9a24-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Knappen Opret projekt](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="a9a24-143">Udfyld følgende felter, og vælg derefter **Opret**:</span><span class="sxs-lookup"><span data-stu-id="a9a24-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="a9a24-144">**Projektnavn**</span><span class="sxs-lookup"><span data-stu-id="a9a24-144">**Project name**</span></span>
    - <span data-ttu-id="a9a24-145">**Versionskontrol** – Vælg **Team Foundation Version Control**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="a9a24-146">Bemærk, at standardindstillingen, **Git**, ikke understøttes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="a9a24-147">**Arbejdselementproces**</span><span class="sxs-lookup"><span data-stu-id="a9a24-147">**Work item process**</span></span>

    ![Dialogboksen Opret nyt projekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="a9a24-149">Oprette et token for personlig adgang</span><span class="sxs-lookup"><span data-stu-id="a9a24-149">Create a personal access token</span></span>

<span data-ttu-id="a9a24-150">I dette selvstudium skal du bruge LCS som Forretningsmodeldesigner (BPM) til at oprette et testsagsbibliotek og synkronisere testsagerne med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="a9a24-151">Du skal bruge et personligt adgangstoken for at synkronisere BPM med Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="a9a24-152">Vælg profilikonet i øverste højre hjørne af siden til Azure DevOps-projektet, og vælg derefter **Sikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Kommandoen Sikkerhed](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="a9a24-154">Vælg **Tokens for personlig adgang** under **Sikkerhed** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="a9a24-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="a9a24-155">Vælg derefter **Nyt token**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-155">Then select **New Token**.</span></span>

    ![Knappen Nyt token under fanen Tokens for personlig adgang i Brugerindstillinger](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="a9a24-157">Udfyld følgende felter, og vælg derefter **Opret**:</span><span class="sxs-lookup"><span data-stu-id="a9a24-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="a9a24-158">**Navn**</span><span class="sxs-lookup"><span data-stu-id="a9a24-158">**Name**</span></span>
    - <span data-ttu-id="a9a24-159">**Udløb (UTC)** – Vælg **Brugerdefineret**, og brug derefter datovælgeren til at vælge den seneste tilgængelige dato.</span><span class="sxs-lookup"><span data-stu-id="a9a24-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="a9a24-160">**Områder** – Vælg indstillingen **Fuld adgang**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Dialogboksen Opret et nyt personligt adgangstoken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-162">Noter det personlige adgangstoken, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="a9a24-163">Du skal bruge det senere, når du opretter RSAT-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Token for personlig adgang](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="a9a24-165">Konfigurere LCS-projektet</span><span class="sxs-lookup"><span data-stu-id="a9a24-165">Configure the LCS project</span></span>

<span data-ttu-id="a9a24-166">Du skal bruge et LCS-projekt (Lifecycle Services) til mastertestbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="a9a24-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="a9a24-167">LCS Forretningsmodeldesigner (BPM) bruges som masterbibliotek for testsagerne.</span><span class="sxs-lookup"><span data-stu-id="a9a24-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="a9a24-168">BPM bruges til at administrere og distribuere testbiblioteker på tværs af LCS-projekter.</span><span class="sxs-lookup"><span data-stu-id="a9a24-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="a9a24-169">En Microsoft-partner eller en uafhængig softwareleverandør (ISV), der f.eks. bygger testsager, skal frigive testsagerne i form af BPM-biblioteker.</span><span class="sxs-lookup"><span data-stu-id="a9a24-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="a9a24-170">I BPM er testsager organiseret efter forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="a9a24-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="a9a24-171">BPM definerer ikke udførelsesrækkefølgen eller hyppigheden af testforløb.</span><span class="sxs-lookup"><span data-stu-id="a9a24-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="a9a24-172">Disse detaljer styres i Azure DevOps, som beskrevet senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="a9a24-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="a9a24-173">Til dit LCS-projekt kan du bruge et eksisterende kundeimplementerings- eller partnerprojekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="a9a24-174">Opdatere LCS-sproget</span><span class="sxs-lookup"><span data-stu-id="a9a24-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-175">For at få brugergrænsefladen (UI) til at vise forretningsprocesser korrekt skal det foretrukne LCS-sprog indstilles til **Engelsk (USA)**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="a9a24-176">Gå til LCS-implementeringsprojektet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="a9a24-177">Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Foretrukket sprog**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Opdatere sprogpræference](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="a9a24-179">Vælg **Engelsk (USA)** i feltet **Foretrukket sprog**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Fanen Foretrukket sprog i Brugerindstillinger](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="a9a24-181">Konfigurere LCS til at oprette forbindelse til Azure DevOps-projektet</span><span class="sxs-lookup"><span data-stu-id="a9a24-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="a9a24-182">Hvis du tidligere har oprettet et nyt Azure DevOps-projekt, skal du konfigurere LCS-projektet til at oprette forbindelse til det.</span><span class="sxs-lookup"><span data-stu-id="a9a24-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="a9a24-183">Ellers kan du fortsætte til næste afsnit, hvis dit LCS-projekt allerede er forbundet med Azure DevOps-projektet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="a9a24-184">Gå til LCS-implementeringsprojektet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="a9a24-185">Vælg knappen **Menu**, og vælg derefter **Projektindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Kommandoen Projektindstillinger](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="a9a24-187">Vælg **Visual Studio Team Services** i ruden til venstre, og vælg derefter **Konfigurer Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Fanen Visual Studio Team Services i Projektindstillinger](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="a9a24-189">Brug feltet **URL-adresse til Azure DevOps-websted** til at angive URL-adressen til Azure DevOps-webstedet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="a9a24-190">Angiv det personlige adgangstoken, der blev oprettet tidligere, i feltet **Token for personlig adgang**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-191">Selvom VSTS nu kaldes Azure DevOps skal du bruge den gamle URL-adresse til at knytte LCS til dit Azure DevOps-projekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="a9a24-192">Den Azure DevOps-URL-adresse, der bruges i dette selvstudium, er f.eks `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="a9a24-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="a9a24-193">Men på følgende illustration angives den som `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="a9a24-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Trin 1 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="a9a24-195">Vælg **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-195">Select **Continue**.</span></span>
6. <span data-ttu-id="a9a24-196">Vælg VSTS-projektet på det valgte websted, som skal knyttes til LCS-projektet, i feltet **Visual Studio Team Services-projekt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="a9a24-197">Feltet **Processkabelon** er som standard indstillet til **Agile**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="a9a24-198">Du kan se en brugerdefineret skabelon i vejledningen til Best Practice i afsnittet [Oprette et nyt Azure DevOps-projekt](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="a9a24-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="a9a24-199">Vælg derefter **Fortsæt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-199">Then select **Continue**.</span></span>

    ![Trin 2 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="a9a24-201">Gennemse indstillingerne, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-201">Review your settings, and then select **Save**.</span></span>

    ![Trin 3 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="a9a24-203">Vælg **Godkend** for at godkende LCS-adgang til det konfigurerede Azure DevOps-websted på dine vegne og for at aktivere funktioner, der kan integreres med VSTS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Knappen Godkend](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="a9a24-205">Der vises en meddelelsesboks med teksten "Du er ved at blive omdirigeret til et eksternt websted for at give LCS tilladelse til at oprette forbindelse til Visual Studio Team Services på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="a9a24-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="a9a24-206">Vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="a9a24-206">Proceed?"</span></span> <span data-ttu-id="a9a24-207">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-207">Select **Yes**.</span></span>

    ![Meddelelsesboks](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="a9a24-209">Vælg **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-209">Select **Accept**.</span></span>

    ![Godkende adgang](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="a9a24-211">Hvis du er godkendt som bruger, skal brugergrænsefladen vende tilbage til siden med projektindstillinger til LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Godkendt bruger](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="a9a24-213">Oprette et nyt BPM-bibliotek</span><span class="sxs-lookup"><span data-stu-id="a9a24-213">Create a new BPM library</span></span>

1. <span data-ttu-id="a9a24-214">Gå til LCS-implementeringsprojektet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="a9a24-215">Vælg knappen **Menu**, og vælg derefter **Forretningsmodeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Kommandoen Forretningsmodeldesigner](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="a9a24-217">Vælg **Nyt bibliotek**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-217">Select **New library**.</span></span>

    ![Knappen Nyt bibliotek](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="a9a24-219">Angiv et navn i feltet **Biblioteksnavn**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="a9a24-220">Til dette selvstudium skal du navngive BPM-biblioteket **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Dialogboksen Opret nyt bibliotek](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="a9a24-222">Åbn det nye **RSAT** BPM-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="a9a24-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="a9a24-223">Vælg eksempelprocessen **Kerneforretningsprocesser**, og vælg derefter **Redigeringstilstand** i højre side.</span><span class="sxs-lookup"><span data-stu-id="a9a24-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Knappen Redigeringstilstand](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="a9a24-225">Rediger værdien i både feltet **Navn** og feltet **Beskrivelse** til **Opret et produkt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="a9a24-226">Vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-226">Then select **Save**.</span></span>

    ![Felterne Navn og Beskrivelse](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="a9a24-228">Miljø</span><span class="sxs-lookup"><span data-stu-id="a9a24-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="a9a24-229">Versionskrav</span><span class="sxs-lookup"><span data-stu-id="a9a24-229">Version requirement</span></span>

<span data-ttu-id="a9a24-230">Der kræves et test- eller sandkassemiljø, som kører version 10.</span><span class="sxs-lookup"><span data-stu-id="a9a24-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="a9a24-231">For kunder, der bruger version 7.3, er Platform update 20 eller nyere også understøttet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-232">RSAT skal have adgang til testmiljøet via en webbrowser.</span><span class="sxs-lookup"><span data-stu-id="a9a24-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="a9a24-233">Brugerkriterier</span><span class="sxs-lookup"><span data-stu-id="a9a24-233">User criteria</span></span>

<span data-ttu-id="a9a24-234">Brugeren skal have administratorrettigheder til dette miljø.</span><span class="sxs-lookup"><span data-stu-id="a9a24-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="a9a24-235">Konfigurere indstillinger for hjælp til at oprette forbindelse til LCS</span><span class="sxs-lookup"><span data-stu-id="a9a24-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="a9a24-236">Dette trin er nødvendigt for at oprette forbindelse til LCS, så opgaveregistreringer kan gemmes i det relevante BPM-bibliotek i LCS via klienten.</span><span class="sxs-lookup"><span data-stu-id="a9a24-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="a9a24-237">Åbn klienten.</span><span class="sxs-lookup"><span data-stu-id="a9a24-237">Open the client.</span></span>
2. <span data-ttu-id="a9a24-238">Gå til **Systemadministration \> Opsætning \> Systemparametre**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="a9a24-239">Vælg det relevante LCS projekt (**RSAT** til dette selvstudium) i feltet **Konfiguration af hjælp til Lifecycle Services** under fanen **Hjælp**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Feltet Konfiguration af hjælp til Lifecycle Services under fanen Hjælp](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="a9a24-241">BPM-biblioteker udfyldes under det relevante LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="a9a24-242">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-242">Select **Save**.</span></span>
5. <span data-ttu-id="a9a24-243">Du skal muligvis opdatere browseren for at få vist det opdaterede Hjælp-indhold.</span><span class="sxs-lookup"><span data-stu-id="a9a24-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Besked om opdatering af browseren](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="a9a24-245">Opgaveregistreringer</span><span class="sxs-lookup"><span data-stu-id="a9a24-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-246">Sørg for, at alle opgaveregistreringer starter på det primære dashboard.</span><span class="sxs-lookup"><span data-stu-id="a9a24-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="a9a24-247">Sørg for, at de enkelte poster er korte, og fokusér på én forretningsopgave, f.eks. oprettelse af en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a9a24-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="a9a24-248">Oprette en opgaveregistrering og gemme den i BPM-biblioteket</span><span class="sxs-lookup"><span data-stu-id="a9a24-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="a9a24-249">Opret en tilsvarende opgaveregistrering, som du kan knytte til den simple forretningsproces, der blev oprettet i det nye BPM-bibliotek.</span><span class="sxs-lookup"><span data-stu-id="a9a24-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="a9a24-250">Åbn klienten.</span><span class="sxs-lookup"><span data-stu-id="a9a24-250">Open the client.</span></span>
2. <span data-ttu-id="a9a24-251">I hoveddashboardet skal du vælge knappen **Indstillinger** (tandhjulsymbolet) og derefter vælge **Arbejdsrutineoptager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Vælge Arbejdsrutineoptager i menuen Indstillinger](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="a9a24-253">Vælg **Opret registrering**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-253">Select **Create recording**.</span></span>

    ![Knappen Opret registrering](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="a9a24-255">Udfyld felterne **Registreringsnavn** og **Beskrivelse af registrering**, og vælg derefter **Start**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Felterne Registreringsnavn og Beskrivelse af registrering](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="a9a24-257">Registrer trinnene til oprettelse af et produkt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-257">Record the steps for creating a product.</span></span> <span data-ttu-id="a9a24-258">Når du er færdig, skal du vælge **Stop** for at stoppe registreringen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Trin til oprettelse af et produkt](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="a9a24-260">Vælg **Gem i Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-260">Select **Save to Lifecycle Services**.</span></span>

    ![Gemme Opgaveregistrering i Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="a9a24-262">Biblioteksoplysninger indlæses fra LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-262">Library information is loaded from LCS.</span></span>

    ![Indlæse oplysninger om bibliotek](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="a9a24-264">Vælg det BPM-bibliotek, der skal knyttes til opgaveregistreringen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="a9a24-265">I dette selvstudium skal du vælge det BPM-bibliotek **RSAT**, der blev oprettet tidligere, og **Opret et produkt** som forretningsproces under det.</span><span class="sxs-lookup"><span data-stu-id="a9a24-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="a9a24-266">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-266">Then select **OK**.</span></span>

    ![Tilknytning af opgaveregistrering med et BPM-bibliotek og en forretningsproces](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="a9a24-268">Meddelelsen "Blev gemt i Lifecycle Services" vises.</span><span class="sxs-lookup"><span data-stu-id="a9a24-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Meddelelse om en vellykket lagring i LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="a9a24-270">Hvis du vil gemme opgaveregistreringen lokalt og derefter overføre den til BPM via LCS, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="a9a24-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="a9a24-271">Vælg **Gem på denne pc**, når registreringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a9a24-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Gem til denne pc](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="a9a24-273">På meddelelseslinjen i browseren skal du vælge **Gem** eller **Gem som** for at gemme filen på din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="a9a24-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Meddelelseslinje](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="a9a24-275">Gå til BPM-biblioteket **RSAT**, og vælg den forretningsproces, hvor opgaveregistreringen skal gemmes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="a9a24-276">Vælg **Overfør** under fanen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Knappen Overfør](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="a9a24-278">Vælg **Gennemse**, og vælg den. axtr-fil, du gemte tidligere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="a9a24-279">Vælg derefter **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-279">Then select **Upload**.</span></span>

        ![Vælg den. axtr-fil, der skal overføres](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="a9a24-281">Teste synkroniseringen fra BPM til Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="a9a24-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="a9a24-282">Nu, hvor en opgaveregistrering er knyttet til forretningsprocessen, skal du validere, at forretningsprocessen og den tilknyttede opgaveregistrering kan synkroniseres til Azure DevOps som en funktion og en testsag (henholdsvist) ved hjælp af synkroniseringsfunktionen VSTS i LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-283">Den tilsvarende arbejdselementtype, der oprettes i Azure DevOps, varierer, afhængigt af den processkabelon du valgte, da du konfigurerede LCS-projektet med Azure DevOps, som beskrevet i afsnittet [Oprette et nyt Azure DevOps-projekt](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="a9a24-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="a9a24-284">Gå til BPM-biblioteket, og åbn det **RSAT**-bibliotek, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="a9a24-285">Vælg ellipseknappen (**...**), og vælg **VSTS-synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![VSTS-synkroniseringskommando i ellipsemenuen](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="a9a24-287">Når VSTS-synkronisering er fuldført, vises fanen **Krav** i venstre side og omfatter det tilsvarende Azure DevOps-arbejdselement.</span><span class="sxs-lookup"><span data-stu-id="a9a24-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-288">Der arbejdselement, der oprettes i Azure DevOps, vil have BPM-biblioteksnavnet som titelpræfiks.</span><span class="sxs-lookup"><span data-stu-id="a9a24-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Fanen Krav](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="a9a24-290">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="a9a24-290">Refresh the page.</span></span>
4. <span data-ttu-id="a9a24-291">Vælg ellipseknappen (**...**). Du vil se en ekstra indstilling, **Synkroniser testsager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="a9a24-292">Vælg denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="a9a24-292">Select this option.</span></span>

    ![Kommandoen Synkroniser testsager i ellipsemenuen](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-294">Hvis indstillingen **Synkroniser testsager** ikke er tilgængelig, efter at du har opdateret siden, skal du gå til hovedsiden for BPM og vælge **Synkroniser testsager** for hele biblioteket.</span><span class="sxs-lookup"><span data-stu-id="a9a24-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="a9a24-295">På denne måde gennemtvinger du effektivt en synkronisering af hele biblioteket.</span><span class="sxs-lookup"><span data-stu-id="a9a24-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Vælge synkronisering af testsager for hele biblioteket](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="a9a24-297">Når synkroniseringen af testsager er fuldført, oprettes der en ny testsag under fanen **Krav**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Ny testsag under fanen Krav](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="a9a24-299">Gå til dit Azure DevOps-projekt, og vælg **Tavler \> Workflowopgaver**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Kommandoen Workflowopgaver under Tavler](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="a9a24-301">Valider, at den workflowopgave og den testsag, du har oprettet via BPM-synkronisering, findes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Workflowopgave og testsag](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="a9a24-303">Installere og konfigurere RSAT</span><span class="sxs-lookup"><span data-stu-id="a9a24-303">Install and Configure RSAT</span></span>

<span data-ttu-id="a9a24-304">RSAT kan installeres på en hvilken som helst computer, der kører Windows 10, og som kan oprette forbindelse til miljøet via en webbrowser (Internet Explorer eller Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="a9a24-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-305">Før du installerer en ny version af værktøjet, anbefales du at fjerne den tidligere version.</span><span class="sxs-lookup"><span data-stu-id="a9a24-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="a9a24-306">Installere et godkendelsescertifikat</span><span class="sxs-lookup"><span data-stu-id="a9a24-306">Install an authentication certificate</span></span>

<span data-ttu-id="a9a24-307">Hvis du vil aktivere godkendelse, skal du generere og installere et certifikat på den computer, som RSAT kører på.</span><span class="sxs-lookup"><span data-stu-id="a9a24-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="a9a24-308">Generere et nyt certifikat</span><span class="sxs-lookup"><span data-stu-id="a9a24-308">Generate a certificate</span></span>

1. <span data-ttu-id="a9a24-309">Hvis du vil oprette en certifikatfil, skal du åbne et Microsoft Windows PowerShell-vindue som administrator og derefter køre følgende kommando.</span><span class="sxs-lookup"><span data-stu-id="a9a24-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="a9a24-310">Åbn certifikatstyring ved at indtaste **certlm.msc** i dialogboksen **Kør**, og bekræft, at **Certifikat til automatisk afprøvning af D365** er oprettet under **Personlige \> certifikater**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-311">Sørg for at angive **certlm.msc**, ikke **certmgr.msc**, da certifikaterne er gemt på den lokale computer.</span><span class="sxs-lookup"><span data-stu-id="a9a24-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Certifikat for D365-automatiseret testcertifikat](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="a9a24-313">Højreklik på certifikatet, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="a9a24-314">Gå til **Rodnøglecentre, der er tillid til \> Certifikater**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Mappen Certifikater under mappen Rodnøglecentre, der er tillid til](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="a9a24-316">Vælg **Sæt ind** i menuen **Handling** for at kopiere certifikatet til placeringen af **Rodnøglecentre, der er tillid til**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Kommandoen Sæt ind i menuen Handling](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="a9a24-318">Hvis du vil hente et aftryk af det installerede certifikat uden mellemrum eller specialtegn, skal du åbne et Windows PowerShell-vindue som administrator og køre følgende kommandoer.</span><span class="sxs-lookup"><span data-stu-id="a9a24-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="a9a24-319">Gem aftrykket, da du senere skal bruge det, når du opdaterer .wif-filerne til Applikationsobjektserver (AOS) og opretter konfigurationen af RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="a9a24-320">Konfigurere AOS-computeren til at vise tillid til forbindelsen</span><span class="sxs-lookup"><span data-stu-id="a9a24-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="a9a24-321">Hvis miljøet er et niveau 2+-miljø, skal certifikataftrykket opdateres i filen wif.config for **alle** AOS-computere for miljøet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="a9a24-322">Opret en RDP-forbindelse (Remote Desktop Protocol) til AOS-computeren.</span><span class="sxs-lookup"><span data-stu-id="a9a24-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="a9a24-323">Logonoplysninger er tilgængelige på siden med miljødetaljer i LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="a9a24-324">Åbn Microsoft IIS (Internet Information Services), og find **AOSService** på listen over websteder.</span><span class="sxs-lookup"><span data-stu-id="a9a24-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService på listen over websteder](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="a9a24-326">Højreklik på **Stifinder** for at åbne mappen **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="a9a24-327">Find filen **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-327">Find the **wif.config** file.</span></span>

    ![Filen wif.config i mappen WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="a9a24-329">Opdater filen **wif.config** ved at tilføje en ny myndighedspost for certifikatet og navnet på myndigheden, som vist i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="a9a24-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="a9a24-330">Hvis flere brugere benytter samme program, skal hver bruger oprette separate aftryk, og hvert af disse aftryk skal tilføjes i sektionen **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="a9a24-331">Hvis der er mere end én AOS-computer, skal du gentage trin 3 til 4 for hver ekstra computer.</span><span class="sxs-lookup"><span data-stu-id="a9a24-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-332">I modsætning til ældre niveau 2-miljøer installeres nye niveau 2-miljøer med to forekomster af AOS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="a9a24-333">Kør **iisreset** på alle AOS-computere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-334">Hvis du ikke har administratorrettigheder til at køre **iisreset** på en computer med niveau 1, skal du vælge Vedligehold > Genstart tjenester på siden med miljødetaljer i LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="a9a24-335">Miljø på niveau 2</span><span class="sxs-lookup"><span data-stu-id="a9a24-335">Tier 2+ environment</span></span>

<span data-ttu-id="a9a24-336">Hvis der bruges et niveau 2+-miljø (Sandkasse: Standardgodkendelsestest eller højere), skal du kontrollere eller angive følgende indstilling i registreringsdatabasen på den computer, hvor RSAT er installeret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="a9a24-337">Dette trin er påkrævet, fordi det hjælper dig med at undgå godkendelses- eller RSAT-forbindelsesfejl.</span><span class="sxs-lookup"><span data-stu-id="a9a24-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="a9a24-338">Installere RSAT</span><span class="sxs-lookup"><span data-stu-id="a9a24-338">Install RSAT</span></span>

1. <span data-ttu-id="a9a24-339">Gå til <https://www.microsoft.com/download/details.aspx?id=57357>, og vælg **Download**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="a9a24-340">Vælg alle filerne, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-340">Select all the files, and then select **Next**.</span></span>

    ![Vælge alle filer](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="a9a24-342">Dobbeltklik på .msi-pakken for at køre installationsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="a9a24-343">Vælg **Udfør**, når installationen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a9a24-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT-installationsprogramfil](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="a9a24-345">Installere Selenium- og browserdrivere</span><span class="sxs-lookup"><span data-stu-id="a9a24-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="a9a24-346">I ældre versioner af RSAT skulle du installere Selenium- og browserdrivere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="a9a24-347">Du behøver ikke længere at installere disse drivere, fordi de installeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="a9a24-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="a9a24-348">Første gang du åbner RSAT, bliver du bedt om automatisk at downloade og installere Selenium.</span><span class="sxs-lookup"><span data-stu-id="a9a24-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="a9a24-349">Du kan finde flere oplysninger i afsnittet [Konfigurere RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="a9a24-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="a9a24-350">Før du kan køre en testsag, bliver du bedt om automatisk at hente og installere den browserdriver, der svarer til den standardbrowser, der er valgt i RSAT-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="a9a24-351">Du kan finde flere oplysninger i afsnittet [Indlæse og køre testsager](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="a9a24-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="a9a24-352">Kom i gang med RSAT</span><span class="sxs-lookup"><span data-stu-id="a9a24-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="a9a24-353">Oprette en testplan og testpakker</span><span class="sxs-lookup"><span data-stu-id="a9a24-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="a9a24-354">Gå til Azure DevOps-projektet, og vælg **Testplaner**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Kommandoen Testplaner](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="a9a24-356">Vælg **Ny testplan**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-356">Select **New Test Plan**.</span></span>

    ![Knappen Ny testplan](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="a9a24-358">Udfyld feltet **Navn**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="a9a24-359">Til dette selvstudium skal du navngive testplanen **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Dialogboksen Ny testplan](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="a9a24-361">Vælg plustegnet (**+**), og vælg derefter **Statisk pakke** for at oprette en statisk pakke under den nye testplan.</span><span class="sxs-lookup"><span data-stu-id="a9a24-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="a9a24-362">Navngiv den nye testpakke **T01 – Fremstilling til lager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-363">Du kan også oprette en forespørgselsbaseret pakke, hvis de nye testsager fra BPM ikke automatisk skal trækkes ind i RSAT-testpakken.</span><span class="sxs-lookup"><span data-stu-id="a9a24-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Oprettelse af en statisk pakke](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="a9a24-365">Knytte testsager til testpakker</span><span class="sxs-lookup"><span data-stu-id="a9a24-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="a9a24-366">Vælg **Tilføj eksisterende** i højre side for at føje eksisterende testsager til testpakken.</span><span class="sxs-lookup"><span data-stu-id="a9a24-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Knappen Tilføj eksisterende](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="a9a24-368">På siden **Føj testsager til pakke** skal du vælge **Kør forespørgsel** og derefter vælge den testsag, der skal føjes til testpakken.</span><span class="sxs-lookup"><span data-stu-id="a9a24-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="a9a24-369">I dette selvstudium skal du vælge **Opret et nyt produkt** som testsag.</span><span class="sxs-lookup"><span data-stu-id="a9a24-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="a9a24-370">Vælg derefter **Tilføj testsager** i nederste højre hjørne af siden (denne knap vises ikke i følgende illustration).</span><span class="sxs-lookup"><span data-stu-id="a9a24-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Knappen Kør forespørgsel](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="a9a24-372">Testsagen føjes til testpakken **T01-Fremstilling til lager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Testsag, der er føjet til testpakken](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="a9a24-374">Konfigurer RSAT</span><span class="sxs-lookup"><span data-stu-id="a9a24-374">Configure RSAT</span></span>

1. <span data-ttu-id="a9a24-375">Åbn RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-375">Open RSAT.</span></span>

    ![RSAT-ikon](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="a9a24-377">Du får vist advarselsmeddelelsen "Regression Suite Automation Tool kræver Selenium. Vil du automatisk hente og installere det nu?"</span><span class="sxs-lookup"><span data-stu-id="a9a24-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="a9a24-378">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-378">Select **Yes**.</span></span>

    ![Advarsel om, at Regression Suite Automation Tool kræver Selenium](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="a9a24-380">Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne, og udfyld derefter følgende felter i den dialogboks, der vises:</span><span class="sxs-lookup"><span data-stu-id="a9a24-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="a9a24-381">**URL-adresse til Azure DevOps** – Angiv URL-adressen til dit Azure DevOps-projekt, f.eks `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="a9a24-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="a9a24-382">**Adgangstoken** – Angiv det adgangstoken, der giver værktøjet mulighed for at oprette forbindelse til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="a9a24-383">Brug det personlige adgangstoken, som du oprettede tidligere i dette selvstudium.</span><span class="sxs-lookup"><span data-stu-id="a9a24-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="a9a24-384">Yderligere oplysninger finder du under [Godkende adgang med personlige adgangstokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="a9a24-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="a9a24-385">**Projektnavn** – Vælg navnet på dit Azure DevOps-projekt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="a9a24-386">**Testplan** – Vælg den Azure DevOps-testplan, der indeholder dine testsager.</span><span class="sxs-lookup"><span data-stu-id="a9a24-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="a9a24-387">Du kan finde flere oplysninger under [Oprette testplaner og testpakker](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="a9a24-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="a9a24-388">Når du har valgt en testplan, skal du vælge **Test forbindelse** for at teste forbindelsen til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="a9a24-389">**Værtsnavn** – Angiv værtsnavnet på testmiljøet, f.eks. **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="a9a24-390">Du skal ikke medtage præfikset **https://** eller **http://**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="a9a24-391">**SOAP-værtsnavn** – Angiv SOAP-værtsnavnet for testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="a9a24-392">SOAP-værtsnavnet er typisk det samme som værtsnavnet, men har et **soap**-suffiks.</span><span class="sxs-lookup"><span data-stu-id="a9a24-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="a9a24-393">Her er et eksempel: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="a9a24-394">Du skal ikke medtage præfikset **https://** eller **http://**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9a24-395">Hvis du vil finde værtsnavnet og SOAP-værtsnavnet, skal du åbne IIS Manager, højreklikke på **Websteder \> AOSService** og derefter vælge **Rediger bindinger**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="a9a24-396">Værdierne i kolonnen **Værtsnavn** giver dig værtsnavnet og SOAP-værtsnavnet (SOAP-værtsnavnet har suffikset **soap** i URL-adressen).</span><span class="sxs-lookup"><span data-stu-id="a9a24-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Værtsnavn og SOAP-værtsnavn i kolonnen Værtsnavn](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="a9a24-398">**Administratorbrugernavn** – Angiv mailadressen på en administratorbruger i testmiljøet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="a9a24-399">**Aftryk** – Angiv aftrykket på godkendelsescertifikatet som beskrevet tidligere i dette selvstudium.</span><span class="sxs-lookup"><span data-stu-id="a9a24-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="a9a24-400">**Arbejdsmappe** – Angiv mappeplaceringen til lagring af automatiserede testfiler, f.eks. Excel-testdatafiler.</span><span class="sxs-lookup"><span data-stu-id="a9a24-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="a9a24-401">Angiv eller vælg f.eks. **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9a24-402">Hvis navnet på mappen har mellemrum, mislykkes udførelsen, fordi mappen ikke blev fundet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="a9a24-403">Dette problem er et kendt problem, som skulle være rettet i den seneste version af værktøjet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="a9a24-404">**Standardbrowser** – Vælg enten **Internet Explorer** eller **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="a9a24-405">Sørg for, at de relevante browserdrivere er installeret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="a9a24-406">**Timeout for testkørsel** – Angiv timeoutperioden i minutter for testkørsler.</span><span class="sxs-lookup"><span data-stu-id="a9a24-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="a9a24-407">Når timeoutperioden udløber, lukkes alle aktive vinduer, og ventende testsager mislykkes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="a9a24-408">**Timeout for testhandling** – Dette felt kontrollerer timeoutperioden i minutter for Finance and Operations-miljøets serveranmodninger.</span><span class="sxs-lookup"><span data-stu-id="a9a24-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="a9a24-409">Normalt skal standardværdien (2 minutter) være tilstrækkelig.</span><span class="sxs-lookup"><span data-stu-id="a9a24-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="a9a24-410">Men i langsomme miljøer kan det være en god idé at øge værdien, hvis der opstår fejl, der er relateret til timeout.</span><span class="sxs-lookup"><span data-stu-id="a9a24-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="a9a24-411">**Firmanavn** – Angiv det firmanavn, der skal bruges som standardfirma, når Excel-parameterfiler oprettes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="a9a24-412">Du kan ændre firmaet senere ved at redigere Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Dialogboksen Indstillinger](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="a9a24-414">Vælg **Anvend** for at anvende og gemme dine indstillinger.</span><span class="sxs-lookup"><span data-stu-id="a9a24-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="a9a24-415">Hvis du vil gemme de aktuelle indstillinger i en konfigurationsfil på din computer, skal du vælge **Gem som**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="a9a24-416">Hvis du vil gendanne dine indstillinger fra en konfigurationsfil på din computer, skal du vælge **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="a9a24-417">Vælg **Luk** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="a9a24-418">Indlæse og køre testsager</span><span class="sxs-lookup"><span data-stu-id="a9a24-418">Load and run test cases</span></span>

1. <span data-ttu-id="a9a24-419">Vælg **Indlæs** for at indlæse testplanen **RSAT-testplan** fra Azure DevOps-projektet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Knappen Indlæs](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="a9a24-421">Vælg testsagen **Opret et nyt produkt** fra testpakken, og vælg derefter **Ny \> Generér testkørsels- og parameterfiler**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Kommandoen Generér testkørsels- og parameterfiler i menuen Ny](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="a9a24-423">Excel-parameterfilen oprettes i den lokale mappe, som du har angivet i RSAT-konfigurationen (f.eks. **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="a9a24-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Excel-parameterfil er oprettet](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="a9a24-425">Hvis du vil gemme parameterfilerne, skal du vælge **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="a9a24-426">Test automatiseringsfiler for alle valgte testsager, der overføres til Azure DevOps til fremtidig brug.</span><span class="sxs-lookup"><span data-stu-id="a9a24-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="a9a24-427">(Disse filer omfatter Excel-testparameterfiler).</span><span class="sxs-lookup"><span data-stu-id="a9a24-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="a9a24-428">På denne måde kan du vælge **Indlæs** for at indlæse parameterfilerne (og automatiseringsfiler) fra testsagen direkte fra Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="a9a24-429">Du behøver ikke at generere parameterfilerne igen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="a9a24-430">Denne fremgangsmåde vil blive vigtig senere, når du vil beholde ændringerne i parameterfilen, så de ikke bliver overskrevet.</span><span class="sxs-lookup"><span data-stu-id="a9a24-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="a9a24-431">Hvis du vil kontrollere, at automatiseringsfilerne og parameterfilerne gemmes i Azure DevOps, skal du gå til Azure DevOps-projektet, vælge **Tavler \> Workflowopgaver** og vælge testsagen **Opret et nyt produkt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="a9a24-432">Under fanen **Vedhæftede filer** skulle du få vist fire filer:</span><span class="sxs-lookup"><span data-stu-id="a9a24-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="a9a24-433">**.cs** – C\# automatiseringsfil</span><span class="sxs-lookup"><span data-stu-id="a9a24-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="a9a24-434">**.dll** – Kompileret automatiseringsfil som en assembly</span><span class="sxs-lookup"><span data-stu-id="a9a24-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="a9a24-435">**.xlsx** – Excel-parameterfil</span><span class="sxs-lookup"><span data-stu-id="a9a24-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="a9a24-436">**.xml** – Registreringsfil</span><span class="sxs-lookup"><span data-stu-id="a9a24-436">**.xml** – Recording file</span></span>

    ![Filer under fanen Vedhæftede filer](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="a9a24-438">Vælg den testsag, der skal køres, og vælg derefter **Kør**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-439">Før du kører testsager, og hvis du bruger Internet Explorer som browser, skal du sørge for, at din skrivebordsopløsning er angivet til **100 %** i **Windows-skærmindstillingerne \> Skalering og layout**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="a9a24-440">Hvis du ikke kan ændre denne indstilling på en virtuel maskine (VM), skal du ændre den på den klient (bærbar), hvor du forsøger at få adgang til den virtuelle maskine.</span><span class="sxs-lookup"><span data-stu-id="a9a24-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="a9a24-441">Opløsningsindstillingerne nedarves derefter med skærmindstillingerne for den virtuelle maskine.</span><span class="sxs-lookup"><span data-stu-id="a9a24-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Skrivebordsopløsning angivet til 100 %](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="a9a24-443">Hvis browserdriverne ikke er installeret i systemet, får du vist en advarselsmeddelelse om, at "Denne handling kræver driveren \<browser name\>.</span><span class="sxs-lookup"><span data-stu-id="a9a24-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="a9a24-444">Vil du downloade og installere den automatisk nu?"</span><span class="sxs-lookup"><span data-stu-id="a9a24-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="a9a24-445">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-445">Select **Yes**.</span></span>

    ![Advarselsmeddelelse for Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Advarselsmeddelelse for Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-448">Hvis du bruger Chrome som browser og modtager en fejlmeddelelse om, at sessionen ikke blev oprettet, fordi Chrome-versionen ikke er korrekt, skal du downloade den seneste Chrome-driver fra <http://chromedriver.chromium.org/downloads> til mappen **C:\\Programmer (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Fejlmeddelelse for Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="a9a24-450">Testsagen er kørt, og feltet **Resultat** er opdateret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Feltet Opdateret resultat](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="a9a24-452">Hvis du har fulgt dette selvstudium slavisk, vil testsagen **Opret et nyt produkt** mislykkes, fordi opgaveregistreringen til oprettelse af et produkt har gemt produktnavnet som en fast kodet værdi.</span><span class="sxs-lookup"><span data-stu-id="a9a24-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="a9a24-453">Hvis du kører den samme testsag igen, skulle du modtage en fejlmeddelelse, da produktet allerede findes.</span><span class="sxs-lookup"><span data-stu-id="a9a24-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Resultatfelt er angivet til Ikke bestået](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="a9a24-455">Vise testresultaterne</span><span class="sxs-lookup"><span data-stu-id="a9a24-455">View the test results</span></span>

1. <span data-ttu-id="a9a24-456">Dobbeltklik på den mislykkede testsag.</span><span class="sxs-lookup"><span data-stu-id="a9a24-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="a9a24-457">Du får en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="a9a24-457">You receive an error message.</span></span>

    ![Fejlmeddelelse](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="a9a24-459">Vælg **Detaljer** for at få vist hele fejlmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-459">Select **Details** to view the whole error message.</span></span>

    ![Hel fejlmeddelelse](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="a9a24-461">Hvis du vil have vist en detaljeret version af fejlmeddelelsen i Azure DevOps, skal du vælge **Åbn i Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="a9a24-462">I Azure DevOps kan du få vist status for testsagen og den detaljerede fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="a9a24-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Detaljeret fejlmeddelelse i Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="a9a24-464">Hvis du vil have vist testresultaterne direkte i Azure DevOps-projektet, skal du gå til **Testplaner \> Testplaner \> Kørsler**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="a9a24-465">Dobbeltklik på den testkørsel, du vil have vist flere oplysninger om.</span><span class="sxs-lookup"><span data-stu-id="a9a24-465">Double-click the test run that you want to see more details for.</span></span>

    ![Liste over testkørsler i Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="a9a24-467">Fanen **Kørselsoversigt** viser, at testsagen ikke lykkedes, men den viser ikke den faktiske fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="a9a24-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="a9a24-468">Hvis du vil have vist den detaljerede fejlmeddelelse, skal du vælge fanen **Testresultater**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Fanen Kørselsoversigt](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="a9a24-470">Fanen **Testresultater** indeholder oplysninger om testsagen sammen med resultatet og fejlmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Fanen Testresultater](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="a9a24-472">Dobbeltklik på den relevante post for at få vist den detaljerede fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="a9a24-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Detaljeret fejlmeddelelse](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-474">Alle fejlmeddelelser er også tilgængelige lokalt i **C:\\Brugere\\\$DitBrugernavn\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="a9a24-475">Du kan også eksportere testkørselsresultaterne fra testplanniveauet ved at vælge **Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Eksportere en testplan](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="a9a24-477">Redigere Excel-parameterfilen</span><span class="sxs-lookup"><span data-stu-id="a9a24-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="a9a24-478">Åbn RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-478">Open RSAT.</span></span>
2. <span data-ttu-id="a9a24-479">Vælg testsagen, og vælg derefter **Rediger** for at åbne Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="a9a24-480">Bemærk, at værdien i feltet **Produktnummer** i **EcoResProductCreate**-arket er hard-coded.</span><span class="sxs-lookup"><span data-stu-id="a9a24-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="a9a24-481">Du skal opdatere dette felt til et nyt produktnummer, før du kører testsagen igen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="a9a24-482">Hvis du vil generere et entydigt produktnummer for hver kørsel uden at skulle genåbne Excel-parameterfilen og manuelt opdatere produktnummeret hver gang, skal du bruge følgende Excel-formel.</span><span class="sxs-lookup"><span data-stu-id="a9a24-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="a9a24-483">Udover fanen **Generelt** indeholder Excel-parameterfilen en datafane for hver formularside, som testsagen besøger.</span><span class="sxs-lookup"><span data-stu-id="a9a24-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Feltet Produktnummer](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="a9a24-485">Vælg **Gem**, og luk derefter Excel-projektmappen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="a9a24-486">Vælg **Overfør** for at gemme Excel-parameterfilen i Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Meddelelse om vellykket overførsel](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-488">Hvis du vil køre testsager i en bestemt brugerkontekst, skal du angive brugerens e mail-id i feltet **Testbruger** under fanen **Generelt** i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="a9a24-489">I den seneste version af RSAT er layoutet i felterne i Excel-parameterfilen blevet opdateret, men konceptet forbliver uændret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Feltet Testbruger](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="a9a24-491">Validere resultaterne</span><span class="sxs-lookup"><span data-stu-id="a9a24-491">Validate the results</span></span>

- <span data-ttu-id="a9a24-492">Vælg **Kør** for at køre testsagen igen, og kontrollér, at testsagen er bestået.</span><span class="sxs-lookup"><span data-stu-id="a9a24-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="a9a24-493">Du kan få vist testresultaterne som beskrevet i afsnittet [Vise testresultaterne](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="a9a24-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Resultatfelt er angivet til Bestået](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="a9a24-495">Sammenkædning af testsager</span><span class="sxs-lookup"><span data-stu-id="a9a24-495">Chaining of test cases</span></span>

<span data-ttu-id="a9a24-496">En nøglefunktion i RSAT er sammenkædning af testsager (dvs. en test kan overføre værdier til andre test).</span><span class="sxs-lookup"><span data-stu-id="a9a24-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="a9a24-497">Testsager køres efter deres definerede rækkefølge i Azure DevOps-testplanen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="a9a24-498">(Denne rækkefølge kan også opdateres i selve testværktøjet). Hvis du derfor vil overføre variabler fra én testsag til en anden, er det vigtigt, at testene befinder sig i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a9a24-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="a9a24-499">I dette afsnit skal du oprette en gemt variabel i den første testsag, oprette endnu en testsag og overføre den gemte variabel fra den første testsag til den anden testsag.</span><span class="sxs-lookup"><span data-stu-id="a9a24-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="a9a24-500">Derefter skal du køre testsagerne som en sammenkædet testsag i RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="a9a24-501">Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel</span><span class="sxs-lookup"><span data-stu-id="a9a24-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="a9a24-502">Åbn klienten.</span><span class="sxs-lookup"><span data-stu-id="a9a24-502">Open the client.</span></span>
2. <span data-ttu-id="a9a24-503">Vælg knappen **Indstillinger** (tandhjulsymbolet), og vælg derefter **Arbejdsrutineoptager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="a9a24-504">Vælg **Rediger registrering**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-504">Select **Edit Recording**.</span></span>

    ![Knappen Rediger registrering](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="a9a24-506">Vælg **Åbn fra Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-506">Select **Open from Lifecycle Services**.</span></span>

    ![Knappen Åbn fra Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="a9a24-508">Vælg **Vælg biblioteket Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Knappen Vælg biblioteket Lifecycle Services](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="a9a24-510">BPM-biblioteker indlæses fra LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-510">BPM libraries are loaded from LCS.</span></span>

    ![Indlæse BPM-biblioteker](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="a9a24-512">Når BPM-bibliotekerne er indlæst fra LCS, skal du vælge BPM-biblioteket **RSAT** og derefter den **Opret et nyt produkt**-forretningsproces, som opgaveregistrering blev knyttet til.</span><span class="sxs-lookup"><span data-stu-id="a9a24-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="a9a24-513">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-513">Then select **OK**.</span></span>

    ![Valg af et BPM-bibliotek og en forretningsproces](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="a9a24-515">Navnet på den rette opgaveregistrering angives i feltet **Registreringsnavn**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="a9a24-516">Vælg **Start**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-516">Select **Start**.</span></span>

    ![Navn på opgaveregistrering i feltet Registreringsnavn](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="a9a24-518">Gå til **Administration af produktoplysninger \> Produkter**, og vælg **Nyt** for at åbne den side, hvor den oprindelige opgaveregistrering, **Opret et produkt**, blev registreret.</span><span class="sxs-lookup"><span data-stu-id="a9a24-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="a9a24-519">Vælg **Indsæt trin**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-520">Det nye trin indsættes **efter** det trin, du har valgt i ruden.</span><span class="sxs-lookup"><span data-stu-id="a9a24-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Knappen Indsæt trin](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="a9a24-522">Højreklik på feltet **Produktnummer**, og vælg derefter **Arbejdsrutineoptager \> Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Kommandoen Kopiér](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="a9a24-524">Der tilføjes et nyt trin i ruden.</span><span class="sxs-lookup"><span data-stu-id="a9a24-524">A new step is added in the pane.</span></span> <span data-ttu-id="a9a24-525">Notér værdien i feltet **Produktnummer**, da du skal bruge nummeret senere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Nyt tilføjet trin](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="a9a24-527">Vælg **Redigeringen blev afsluttet**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="a9a24-528">Vælg **Gem i Lifecycle Services**, og knyt den nye opgaveregistrering til det samme BPM-bibliotek og den samme forretningsproces, som den oprindelige opgaveregistrering blev knyttet til.</span><span class="sxs-lookup"><span data-stu-id="a9a24-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="a9a24-529">Du kan finde flere oplysninger i afsnittet [Oprette en opgaveregistrering og gemme den i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="a9a24-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="a9a24-530">Gå til BPM-biblioteket, og vælg **Synkroniser testsager** for at overskrive den opgaveregistrering, der er knyttet til testsagen i Azure DevOps, som beskrevet i afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="a9a24-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="a9a24-531">Åbn RSAT, og vælg **Indlæs** for at genindlæse alle testsagerne i testpakken.</span><span class="sxs-lookup"><span data-stu-id="a9a24-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="a9a24-532">Du skal generere automatiserings- og parameterfilerne for den relevante testsag ved at vælge testsagen og derefter vælge **Ny \> Generér testkørsels- og parameterfiler** som beskrevet i afsnittet [Indlæse og køre testsager](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="a9a24-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-533">Hvis Excel-parameterfilen er åben, mislykkes regenering.</span><span class="sxs-lookup"><span data-stu-id="a9a24-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="a9a24-534">Derfor skal du kontrollere, at Excel-parameterfilen til testsagen er lukket, før du genererer den nye Excel-parameterfil.</span><span class="sxs-lookup"><span data-stu-id="a9a24-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="a9a24-535">Vælg **Rediger** for at åbne den nye Excel-parameterfil.</span><span class="sxs-lookup"><span data-stu-id="a9a24-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="a9a24-536">Du får vist en ny **Gemt variabel**-post i linje 9.</span><span class="sxs-lookup"><span data-stu-id="a9a24-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="a9a24-537">Denne variabel, **{{EcoResProductCreate\_identifikation\_ProductNumber\_Copy}}**, gemmes i opgaveregistreringens XML-fil og kan bruges i efterfølgende test.</span><span class="sxs-lookup"><span data-stu-id="a9a24-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Gemt variabelpost](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="a9a24-539">Oprette en ny testsag</span><span class="sxs-lookup"><span data-stu-id="a9a24-539">Create a new test case</span></span>

1. <span data-ttu-id="a9a24-540">Gå til BPM-biblioteket **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="a9a24-541">Vælg eksempelprocessen **Supportforretningsprocesser**, og vælg derefter **Redigeringstilstand** i højre side.</span><span class="sxs-lookup"><span data-stu-id="a9a24-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="a9a24-542">Rediger værdien i både feltet **Navn** og feltet **Beskrivelse** til **Frigiv et produkt**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="a9a24-543">Vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-543">Then select **Save**.</span></span>

    ![Navn og beskrivelse er ændret til Frigiv et produkt](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="a9a24-545">Oprette en ny opgaveregistrering, der har en valideringsfunktion</span><span class="sxs-lookup"><span data-stu-id="a9a24-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="a9a24-546">Opret en opgaveregistrering for at frigive det produkt, der er oprettet tidligere, til den juridiske enhed USRT.</span><span class="sxs-lookup"><span data-stu-id="a9a24-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="a9a24-547">Du kan finde flere oplysninger i afsnittet [Oprette en opgaveregistrering og gemme den i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="a9a24-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9a24-548">Ved sammenkædede testsager anbefaler vi altid, at du finder eller filtrerer efter den post, du har brug for, ved at *skrive værdien i feltet manuelt*.</span><span class="sxs-lookup"><span data-stu-id="a9a24-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="a9a24-549">På denne måde kan værktøjet bestemme den post, som handlingen skal udføres på, i den efterfølgende testsag.</span><span class="sxs-lookup"><span data-stu-id="a9a24-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Ny opgaveregistrering, der har en valideringsfunktion](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="a9a24-551">Som den foregående illustration viser, når produktet blev fundet ved hjælp af Quick filter, men før du vælger **Frigiv produkter**, skal du validere værdien i feltet **Produktnummer** for at sikre, at produkt-id'et er det produkt-id, der blev oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="a9a24-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="a9a24-552">Hvis du vil validere værdien, skal du højreklikke på feltet **Produktnummer** og derefter vælge **Arbejdsrutineoptager \> Valider \> Aktuel værdi**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Validering af den aktuelle værdi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="a9a24-554">Gemme opgaveregistreringen i BPM</span><span class="sxs-lookup"><span data-stu-id="a9a24-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="a9a24-555">Vælg **Gem i Lifecycle Services**, når opgaveregistreringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a9a24-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Gemme fuldført Opgaveregistrering i Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="a9a24-557">Biblioteksoplysninger indlæses fra LCS.</span><span class="sxs-lookup"><span data-stu-id="a9a24-557">Library information is loaded from LCS.</span></span>

    ![Indlæse oplysninger om bibliotek fra LCS](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="a9a24-559">Vælg det BPM-bibliotek, der skal knyttes til opgaveregistreringen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="a9a24-560">I dette selvstudium skal du vælge det BPM-bibliotek **RSAT**, der blev oprettet tidligere, og **Frigiv et produkt** som forretningsproces under det.</span><span class="sxs-lookup"><span data-stu-id="a9a24-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="a9a24-561">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="a9a24-562">Synkronisere BPM til Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="a9a24-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="a9a24-563">Gå til BPM-biblioteket, og åbn biblioteket **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="a9a24-564">Vælg **VSTS-synkronisering** og derefter **Synkroniser testsager**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="a9a24-565">Du kan finde flere oplysninger i afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="a9a24-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="a9a24-566">Når synkroniseringen er fuldført, vises den nye workflowopgave og den tilsvarende testsag for forretningsprocessen **Frigiv et produkt** i Azure DevOps ved **Tavler \> Workflowopgaver**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="a9a24-567">Føje den nye testsag til den eksisterende testpakke</span><span class="sxs-lookup"><span data-stu-id="a9a24-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="a9a24-568">Gå til **Testplaner \> Testplaner**, og vælg planen **RSAT-testplan**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="a9a24-569">Vælg **Tilføj eksisterende**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="a9a24-570">Vælg **Kør forespørgsel** på siden **Føj testsager til pakke**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="a9a24-571">Vælg den nye testsag, der blev oprettet til **Frigiv et produkt**, og vælg derefter **Tilføj testsager** i nederste højre hjørne af siden (denne knap vises ikke i følgende illustration).</span><span class="sxs-lookup"><span data-stu-id="a9a24-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Siden Føj testsager til pakke](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="a9a24-573">Testpakken har nu to testsager.</span><span class="sxs-lookup"><span data-stu-id="a9a24-573">The test suite now has two test cases.</span></span>

    ![To testsager i testpakken](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="a9a24-575">Indlæse testsager i RSAT</span><span class="sxs-lookup"><span data-stu-id="a9a24-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="a9a24-576">Åbn RSAT, og vælg **Indlæs**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="a9a24-577">Testsagerne indlæses, og du får vist en advarsel om, at "Handlingen vil overskrive Excel-testdatafiler, og lokale ændringer vil gå tabt.</span><span class="sxs-lookup"><span data-stu-id="a9a24-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="a9a24-578">Vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="a9a24-578">Do you want to proceed?"</span></span> <span data-ttu-id="a9a24-579">Vælg **Ja** for at opdatere Excel-parameterfilerne i det lokale system, men ikke de Excel-parameterfiler, der er overført til Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Denne handling overskriver Excel-testdatafiler](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="a9a24-581">Begge testsager indlæses sammen med Excel-parameterfilen til den første testsag.</span><span class="sxs-lookup"><span data-stu-id="a9a24-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="a9a24-582">Da du valgte **Overførsel** i sidste kørsel, hentes parameterfilerne fra Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9a24-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Testsager er indlæst](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="a9a24-584">Vælg kun den anden testsag, og vælg derefter **Ny \> Generér testkørsels- og parameterfiler**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="a9a24-585">Redigere Excel-parameterfilen</span><span class="sxs-lookup"><span data-stu-id="a9a24-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="a9a24-586">Vælg kun den anden testsag, og vælg derefter **Rediger** for at åbne den tilsvarende Excel-parameterfil.</span><span class="sxs-lookup"><span data-stu-id="a9a24-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="a9a24-587">Kopiér den gemte variabel **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (se afsnittet [Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel](#modify-an-existing-task-recording-to-create-a-saved-variable)) fra den første testsag til alle de felter, hvor produktnummeret bruges.</span><span class="sxs-lookup"><span data-stu-id="a9a24-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="a9a24-588">I dette tilfælde skal du kopiere variablen til felterne **Produktnummer** og **Valider produktnummer** på arket **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Felterne Produktnummer og Valider produktnummer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="a9a24-590">Der kan kun overføres variabler mellem testene under den samme testkørsel.</span><span class="sxs-lookup"><span data-stu-id="a9a24-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="a9a24-591">Navnene på variablerne skal være helt ens.</span><span class="sxs-lookup"><span data-stu-id="a9a24-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="a9a24-592">Vælg **Gem**, og luk derefter Excel-projektmappen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="a9a24-593">Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen.</span><span class="sxs-lookup"><span data-stu-id="a9a24-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="a9a24-594">Køre de sammenkædede testsager</span><span class="sxs-lookup"><span data-stu-id="a9a24-594">Run the chained test cases</span></span>

1. <span data-ttu-id="a9a24-595">Vælg begge testsager, og vælg derefter **Kør**.</span><span class="sxs-lookup"><span data-stu-id="a9a24-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="a9a24-596">Kontrollér, at begge testsager er bestået.</span><span class="sxs-lookup"><span data-stu-id="a9a24-596">Verify that both test cases have passed.</span></span>

    ![Resultatfelt er angivet til bestået for begge testsager](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]