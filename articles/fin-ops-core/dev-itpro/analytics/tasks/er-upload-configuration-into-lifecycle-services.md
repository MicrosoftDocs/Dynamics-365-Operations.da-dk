---
title: Overføre en konfiguration til Lifecycle Services
description: I dette emne beskrives det, hvordan du opretter en ny konfiguration af elektronisk rapportering (ER) og uploader den til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270553"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="163db-103">Overføre en konfiguration til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="163db-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="163db-104">Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan oprette en ny [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) og uploade den til [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="163db-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="163db-105">Brugen af LCS som opbevaringslager for ER-konfigurationer [udfases](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="163db-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="163db-106">Du kan finde flere oplysninger under [RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="163db-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="163db-107">I dette eksempel skal du oprette en konfiguration og uploade den til LCS for eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="163db-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="163db-108">For at fuldføre disse trin skal du først fuldføre trinnene under [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="163db-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="163db-109">Der kræves også adgang til LCS.</span><span class="sxs-lookup"><span data-stu-id="163db-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="163db-110">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="163db-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="163db-111">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="163db-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="163db-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="163db-112">System administrator</span></span>

2. <span data-ttu-id="163db-113">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="163db-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="163db-114">Vælg **Litware, Inc.**, og angiv **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="163db-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="163db-115">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="163db-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="163db-116">Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det [aktivbibliotek](../../lifecycle-services/asset-library.md#asset-library-support), som bruges til at importere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="163db-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="163db-117">Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finans.</span><span class="sxs-lookup"><span data-stu-id="163db-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="163db-118">Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS.</span><span class="sxs-lookup"><span data-stu-id="163db-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="163db-119">Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finans ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finans-forekomst er klargjort til.</span><span class="sxs-lookup"><span data-stu-id="163db-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="163db-120">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="163db-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="163db-121">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="163db-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="163db-122">Vælg **Opret konfiguration** på siden **Konfigurationer** for at åbne dialogboksen med rullemenu.</span><span class="sxs-lookup"><span data-stu-id="163db-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="163db-123">I dette eksempel skal du oprette en konfiguration, der indeholder en eksempeldatamodel for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="163db-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="163db-124">Denne datakonfigurationsmodel overføres senere til LCS.</span><span class="sxs-lookup"><span data-stu-id="163db-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="163db-125">Skriv **Eksempelmodelkonfiguration** i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="163db-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="163db-126">Skriv **Eksempelmodelkonfiguration** i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="163db-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="163db-127">Vælg **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="163db-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="163db-128">Vælg **Modeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="163db-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="163db-129">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="163db-129">Select **New**.</span></span>
8. <span data-ttu-id="163db-130">I feltet **Navn** skal du angive **Indgangspunkt**.</span><span class="sxs-lookup"><span data-stu-id="163db-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="163db-131">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="163db-131">Select **Add**.</span></span>
10. <span data-ttu-id="163db-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="163db-132">Select **Save**.</span></span>
11. <span data-ttu-id="163db-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="163db-133">Close the page.</span></span>
12. <span data-ttu-id="163db-134">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="163db-134">Select **Change status**.</span></span>
13. <span data-ttu-id="163db-135">Vælg **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="163db-135">Select **Complete**.</span></span>
14. <span data-ttu-id="163db-136">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="163db-136">Select **OK**.</span></span>
15. <span data-ttu-id="163db-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="163db-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="163db-138">Registrere et nyt lager</span><span class="sxs-lookup"><span data-stu-id="163db-138">Register a new repository</span></span>

1. <span data-ttu-id="163db-139">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="163db-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="163db-140">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="163db-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="163db-141">I feltet **Litware, Inc.** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="163db-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="163db-142">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="163db-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="163db-143">Vælg **Tilføj** for at åbne dialogboksen med rullemenu.</span><span class="sxs-lookup"><span data-stu-id="163db-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="163db-144">Nu kan du tilføje et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="163db-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="163db-145">Vælg **LCS** i feltet **Konfigurationslagertype**.</span><span class="sxs-lookup"><span data-stu-id="163db-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="163db-146">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="163db-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="163db-147">Indtast eller vælg en værdi i feltet **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="163db-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="163db-148">Vælg det ønskede LCS-projekt til dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="163db-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="163db-149">Du skal have [adgang](#accessconditions) til projektet.</span><span class="sxs-lookup"><span data-stu-id="163db-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="163db-150">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="163db-150">Select **OK**.</span></span>

    <span data-ttu-id="163db-151">Udfyld en ny lagerpost.</span><span class="sxs-lookup"><span data-stu-id="163db-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="163db-152">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="163db-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="163db-153">I dette eksempel skal du vælge **LCS**-lagerposten.</span><span class="sxs-lookup"><span data-stu-id="163db-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="163db-154">Bemærk, at et registreret lager er markeret af den aktuelle udbyder.</span><span class="sxs-lookup"><span data-stu-id="163db-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="163db-155">Det vil sige, at det kun er de konfigurationer, der ejes af den pågældende udbyder, der kan placeres i lageret og derfor overføres til det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="163db-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="163db-156">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="163db-156">Select **Open**.</span></span>

    <span data-ttu-id="163db-157">Åbn lageret for at få vist listen over ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="163db-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="163db-158">Den vil være tom, hvis projektet endnu ikke er blevet brugt til deling af ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="163db-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="163db-159">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="163db-159">Close the page.</span></span>
12. <span data-ttu-id="163db-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="163db-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="163db-161">Uploade en konfiguration til LCS</span><span class="sxs-lookup"><span data-stu-id="163db-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="163db-162">Gå til **Virksomhedsadministration \> Elektronisk rapportering \> Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="163db-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="163db-163">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="163db-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="163db-164">Du skal vælge en oprettet konfiguration, der allerede er fuldført.</span><span class="sxs-lookup"><span data-stu-id="163db-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="163db-165">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="163db-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="163db-166">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="163db-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="163db-167">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="163db-167">Select **Change status**.</span></span>
5. <span data-ttu-id="163db-168">Vælg **Del**.</span><span class="sxs-lookup"><span data-stu-id="163db-168">Select **Share**.</span></span>

    <span data-ttu-id="163db-169">Status for konfigurationen ændres fra **Fuldført** til **Delt**, når konfigurationen er udgivet i LCS.</span><span class="sxs-lookup"><span data-stu-id="163db-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="163db-170">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="163db-170">Select **OK**.</span></span>
7. <span data-ttu-id="163db-171">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="163db-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="163db-172">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="163db-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="163db-173">Bemærk, at statussen for den valgte version er ændret fra **Fuldført** til **Delt**.</span><span class="sxs-lookup"><span data-stu-id="163db-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="163db-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="163db-174">Close the page.</span></span>
9. <span data-ttu-id="163db-175">Vælg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="163db-175">Select **Repositories**.</span></span>

    <span data-ttu-id="163db-176">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="163db-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="163db-177">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="163db-177">Select **Open**.</span></span>

    <span data-ttu-id="163db-178">I dette eksempel skal du vælge **LCS**-lageret og åbne det.</span><span class="sxs-lookup"><span data-stu-id="163db-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="163db-179">Bemærk, at den valgte konfiguration vises som et aktiv for det valgte LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="163db-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="163db-180">Åbn LCS ved at gå til <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="163db-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="163db-181">Åbn et projekt, der er brugt tidligere til registrering af lager.</span><span class="sxs-lookup"><span data-stu-id="163db-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="163db-182">Åbn aktivbiblioteket for projektet.</span><span class="sxs-lookup"><span data-stu-id="163db-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="163db-183">Vælg **GER-konfiguration** som aktivtype.</span><span class="sxs-lookup"><span data-stu-id="163db-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="163db-184">Den ER-konfiguration, du har uploadet, skal være vist på listen.</span><span class="sxs-lookup"><span data-stu-id="163db-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="163db-185">Bemærk, at den uploadede LCS-konfiguration kan importeres til en anden forekomst, hvis udbyderne har adgang til dette LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="163db-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
