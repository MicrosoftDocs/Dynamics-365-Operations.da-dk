---
title: Overføre en konfiguration til Lifecycle Services
description: I dette emne beskrives det, hvordan du opretter en ny konfiguration af elektronisk rapportering (ER) og uploader den til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092535"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="bee78-103">Overføre en konfiguration til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bee78-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bee78-104">Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan oprette en ny [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) og uploade den til [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bee78-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="bee78-105">I dette eksempel skal du oprette en konfiguration og uploade den til LCS for eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="bee78-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="bee78-106">For at fuldføre disse trin skal du først fuldføre trinnene under [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="bee78-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="bee78-107">Der kræves også adgang til LCS.</span><span class="sxs-lookup"><span data-stu-id="bee78-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="bee78-108">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="bee78-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="bee78-109">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bee78-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="bee78-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="bee78-110">System administrator</span></span>

2. <span data-ttu-id="bee78-111">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="bee78-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="bee78-112">Vælg **Litware, Inc.**, og angiv **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="bee78-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="bee78-113">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="bee78-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="bee78-114">Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det [aktivbibliotek](../../lifecycle-services/asset-library.md#asset-library-support), som bruges til at importere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bee78-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="bee78-115">Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finans.</span><span class="sxs-lookup"><span data-stu-id="bee78-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="bee78-116">Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS.</span><span class="sxs-lookup"><span data-stu-id="bee78-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="bee78-117">Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finans ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finans-forekomst er klargjort til.</span><span class="sxs-lookup"><span data-stu-id="bee78-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="bee78-118">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bee78-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="bee78-119">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="bee78-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bee78-120">Vælg **Opret konfiguration** på siden **Konfigurationer** for at åbne dialogboksen med rullemenu.</span><span class="sxs-lookup"><span data-stu-id="bee78-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="bee78-121">I dette eksempel skal du oprette en konfiguration, der indeholder en eksempeldatamodel for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="bee78-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="bee78-122">Denne datakonfigurationsmodel overføres senere til LCS.</span><span class="sxs-lookup"><span data-stu-id="bee78-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="bee78-123">Skriv **Eksempelmodelkonfiguration** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="bee78-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="bee78-124">Skriv **Eksempelmodelkonfiguration** i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="bee78-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="bee78-125">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="bee78-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="bee78-126">Vælg **Modeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="bee78-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="bee78-127">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bee78-127">Select **New**.</span></span>
8. <span data-ttu-id="bee78-128">I feltet **Navn** skal du angive **Indgangspunkt**.</span><span class="sxs-lookup"><span data-stu-id="bee78-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="bee78-129">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="bee78-129">Select **Add**.</span></span>
10. <span data-ttu-id="bee78-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="bee78-130">Select **Save**.</span></span>
11. <span data-ttu-id="bee78-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bee78-131">Close the page.</span></span>
12. <span data-ttu-id="bee78-132">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="bee78-132">Select **Change status**.</span></span>
13. <span data-ttu-id="bee78-133">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="bee78-133">Select **Complete**.</span></span>
14. <span data-ttu-id="bee78-134">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bee78-134">Select **OK**.</span></span>
15. <span data-ttu-id="bee78-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bee78-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="bee78-136">Registrere et nyt lager</span><span class="sxs-lookup"><span data-stu-id="bee78-136">Register a new repository</span></span>

1. <span data-ttu-id="bee78-137">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="bee78-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="bee78-138">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="bee78-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="bee78-139">I feltet **Litware, Inc.** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bee78-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="bee78-140">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="bee78-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="bee78-141">Vælg **Tilføj** for at åbne dialogboksen med rullemenu.</span><span class="sxs-lookup"><span data-stu-id="bee78-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="bee78-142">Nu kan du tilføje et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="bee78-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="bee78-143">Vælg **LCS** i feltet **Konfigurationslagertype**.</span><span class="sxs-lookup"><span data-stu-id="bee78-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="bee78-144">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="bee78-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="bee78-145">Indtast eller vælg en værdi i feltet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bee78-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="bee78-146">Vælg det ønskede LCS-projekt til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="bee78-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="bee78-147">Du skal have [adgang](#accessconditions) til projektet.</span><span class="sxs-lookup"><span data-stu-id="bee78-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="bee78-148">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bee78-148">Select **OK**.</span></span>

    <span data-ttu-id="bee78-149">Udfyld en ny lagerpost.</span><span class="sxs-lookup"><span data-stu-id="bee78-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="bee78-150">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="bee78-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="bee78-151">I dette eksempel skal du vælge **LCS**-lagerposten.</span><span class="sxs-lookup"><span data-stu-id="bee78-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="bee78-152">Bemærk, at et registreret lager er markeret af den aktuelle udbyder.</span><span class="sxs-lookup"><span data-stu-id="bee78-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="bee78-153">Det vil sige, at det kun er de konfigurationer, der ejes af den pågældende udbyder, der kan placeres i lageret og derfor overføres til det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="bee78-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="bee78-154">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="bee78-154">Select **Open**.</span></span>

    <span data-ttu-id="bee78-155">Åbn lageret for at få vist listen over ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bee78-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="bee78-156">Den vil være tom, hvis projektet endnu ikke er blevet brugt til deling af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="bee78-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="bee78-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bee78-157">Close the page.</span></span>
12. <span data-ttu-id="bee78-158">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bee78-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="bee78-159">Uploade en konfiguration til LCS</span><span class="sxs-lookup"><span data-stu-id="bee78-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="bee78-160">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="bee78-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="bee78-161">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="bee78-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="bee78-162">Du skal vælge en oprettet konfiguration, der allerede er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bee78-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="bee78-163">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="bee78-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="bee78-164">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="bee78-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="bee78-165">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="bee78-165">Select **Change status**.</span></span>
5. <span data-ttu-id="bee78-166">Vælg **Del**.</span><span class="sxs-lookup"><span data-stu-id="bee78-166">Select **Share**.</span></span>

    <span data-ttu-id="bee78-167">Status for konfigurationen ændres fra **Fuldført** til **Delt**, når konfigurationen er udgivet i LCS.</span><span class="sxs-lookup"><span data-stu-id="bee78-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="bee78-168">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="bee78-168">Select **OK**.</span></span>
7. <span data-ttu-id="bee78-169">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="bee78-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="bee78-170">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="bee78-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="bee78-171">Bemærk, at statussen for den valgte version er ændret fra **Fuldført** til **Delt**.</span><span class="sxs-lookup"><span data-stu-id="bee78-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="bee78-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="bee78-172">Close the page.</span></span>
9. <span data-ttu-id="bee78-173">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bee78-173">Select **Repositories**.</span></span>

    <span data-ttu-id="bee78-174">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="bee78-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="bee78-175">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="bee78-175">Select **Open**.</span></span>

    <span data-ttu-id="bee78-176">I dette eksempel skal du vælge **LCS**-lageret og åbne det.</span><span class="sxs-lookup"><span data-stu-id="bee78-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="bee78-177">Bemærk, at den valgte konfiguration vises som et aktiv for det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="bee78-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="bee78-178">Åbn LCS ved at gå til <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="bee78-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="bee78-179">Åbn et projekt, der er brugt tidligere til registrering af lager.</span><span class="sxs-lookup"><span data-stu-id="bee78-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="bee78-180">Åbn aktivbiblioteket for projektet.</span><span class="sxs-lookup"><span data-stu-id="bee78-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="bee78-181">Vælg **GER-konfiguration** som aktivtype.</span><span class="sxs-lookup"><span data-stu-id="bee78-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="bee78-182">Den ER-konfiguration, du har uploadet, skal være vist på listen.</span><span class="sxs-lookup"><span data-stu-id="bee78-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="bee78-183">Bemærk, at den uploadede LCS-konfiguration kan importeres til en anden forekomst, hvis udbyderne har adgang til dette LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="bee78-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
