---
title: Importere en konfiguration fra Lifecycle Services
description: Dette emne beskriver, hvordan en ny version af en ER-konfiguration (elektronisk rapportering) importeres fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270831"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="a56e8-103">Importere en konfiguration fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a56e8-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a56e8-104">Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan importere en ny version af en [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) fra [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a56e8-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a56e8-105">Brugen af LCS som opbevaringslager for ER-konfigurationer [udfases](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="a56e8-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="a56e8-106">Du kan finde flere oplysninger under [RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a56e8-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="a56e8-107">I dette eksempel skal du vælge den ønskede version af ER-konfigurationen og importere den til eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan fuldføres i alle virksomheder, fordi ER-konfigurationer deles af firmaer.</span><span class="sxs-lookup"><span data-stu-id="a56e8-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="a56e8-108">For at fuldføre disse trin skal du først fuldføre trinnene i proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="a56e8-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a56e8-109">Der kræves også adgang til LCS.</span><span class="sxs-lookup"><span data-stu-id="a56e8-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="a56e8-110">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="a56e8-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="a56e8-111">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a56e8-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="a56e8-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="a56e8-112">System administrator</span></span>

2. <span data-ttu-id="a56e8-113">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="a56e8-114">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="a56e8-115">Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det aktivbibliotek, som brugeren vil [have adgang](../../lifecycle-services/asset-library.md#asset-library-support) til for at importere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="a56e8-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="a56e8-116">Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finans.</span><span class="sxs-lookup"><span data-stu-id="a56e8-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="a56e8-117">Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS.</span><span class="sxs-lookup"><span data-stu-id="a56e8-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="a56e8-118">Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finans ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finans-forekomst er klargjort til.</span><span class="sxs-lookup"><span data-stu-id="a56e8-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="a56e8-119">Slette en delt version af en datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="a56e8-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="a56e8-120">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="a56e8-121">Den første version af en eksempeldatamodelkonfiguration har du oprettet og udgivet til LCS, da du fuldførte proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="a56e8-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a56e8-122">I denne procedure skal du slette den version af ER-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a56e8-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="a56e8-123">Derefter skal du importere denne version fra LCS senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="a56e8-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="a56e8-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a56e8-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a56e8-125">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="a56e8-126">Denne status angiver, at konfigurationen er blevet publiceret til LCS.</span><span class="sxs-lookup"><span data-stu-id="a56e8-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="a56e8-127">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-127">Select **Change status**.</span></span>
4. <span data-ttu-id="a56e8-128">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="a56e8-129">Ved at skifte status for den valgte version fra **Delt** til **Annulleret** gøres versionen tilgængelig for sletning.</span><span class="sxs-lookup"><span data-stu-id="a56e8-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="a56e8-130">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-130">Select **OK**.</span></span>
6. <span data-ttu-id="a56e8-131">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a56e8-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a56e8-132">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="a56e8-133">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-133">Select **Delete**.</span></span>
8. <span data-ttu-id="a56e8-134">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-134">Select **Yes**.</span></span>

    <span data-ttu-id="a56e8-135">Bemærk, at kun kladdeversion 2 af den valgte datamodelkonfiguration nu er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a56e8-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="a56e8-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a56e8-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="a56e8-137">Importere en delt version af en datamodelkonfiguration fra LCS</span><span class="sxs-lookup"><span data-stu-id="a56e8-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="a56e8-138">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="a56e8-139">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="a56e8-140">I feltet **Litware, Inc.** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="a56e8-141">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a56e8-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="a56e8-142">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-142">Select **Open**.</span></span>

    <span data-ttu-id="a56e8-143">I dette eksempel skal du vælge **LCS**-lageret og åbne det.</span><span class="sxs-lookup"><span data-stu-id="a56e8-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="a56e8-144">Du skal have [adgang](#accessconditions) til det LCS-projekt og til det aktivbibliotek, som det valgte ER-lager har adgang til.</span><span class="sxs-lookup"><span data-stu-id="a56e8-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="a56e8-145">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a56e8-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="a56e8-146">Vælg i dette eksempel den første version af **Eksempelmodelkonfiguration** på versionslisten.</span><span class="sxs-lookup"><span data-stu-id="a56e8-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="a56e8-147">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-147">Select **Import**.</span></span>
7. <span data-ttu-id="a56e8-148">Vælg **Ja** for at bekræfte importen af den valgte version fra LCS.</span><span class="sxs-lookup"><span data-stu-id="a56e8-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="a56e8-149">En informationsmeddelelse bekræfter, at den valgte version er blevet importeret.</span><span class="sxs-lookup"><span data-stu-id="a56e8-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="a56e8-150">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a56e8-150">Close the page.</span></span>
9. <span data-ttu-id="a56e8-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a56e8-151">Close the page.</span></span>
10. <span data-ttu-id="a56e8-152">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="a56e8-153">Vælg **Eksempelmodelkonfiguration** i træet.</span><span class="sxs-lookup"><span data-stu-id="a56e8-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="a56e8-154">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a56e8-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a56e8-155">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="a56e8-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="a56e8-156">Bemærk, at den delte version 1 af den valgte datamodelkonfiguration nu også er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a56e8-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
