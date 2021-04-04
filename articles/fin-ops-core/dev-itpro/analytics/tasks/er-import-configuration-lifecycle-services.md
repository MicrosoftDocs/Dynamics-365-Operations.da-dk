---
title: Importere en konfiguration fra Lifecycle Services
description: Dette emne beskriver, hvordan en ny version af en ER-konfiguration (elektronisk rapportering) importeres fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: 636ed27c157c8322cc1be4ca8eca10ef37eb8bbc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569503"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="4efdb-103">Importere en konfiguration fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="4efdb-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4efdb-104">Dette emne beskriver, hvordan en bruger i rollen som Systemadministrator eller Udvikler af elektronisk rapportering kan importere en ny version af en [Elektronisk rapporteringskonfiguration (ER)](../general-electronic-reporting.md#Configuration) fra [aktivbiblioteket på projektniveau](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4efdb-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="4efdb-105">I dette eksempel skal du vælge den ønskede version af ER-konfigurationen og importere den til eksempelfirmaet med navnet Litware, Inc. Denne fremgangsmåde kan fuldføres i alle virksomheder, fordi ER-konfigurationer deles af firmaer.</span><span class="sxs-lookup"><span data-stu-id="4efdb-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="4efdb-106">For at fuldføre disse trin skal du først fuldføre trinnene i proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="4efdb-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="4efdb-107">Der kræves også adgang til LCS.</span><span class="sxs-lookup"><span data-stu-id="4efdb-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="4efdb-108">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="4efdb-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="4efdb-109">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="4efdb-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="4efdb-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="4efdb-110">System administrator</span></span>

2. <span data-ttu-id="4efdb-111">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="4efdb-112">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="4efdb-113">Sørg for, at den aktuelle Dynamics 365 Finance-bruger er medlem af det LCS projekt, der indeholder det aktivbibliotek, som brugeren vil [have adgang](../../lifecycle-services/asset-library.md#asset-library-support) til for at importere ER-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="4efdb-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="4efdb-114">Du kan ikke få adgang til et LCS-projekt fra et ER-lager, der repræsenterer et andet domæne end det domæne, der bruges i Finans.</span><span class="sxs-lookup"><span data-stu-id="4efdb-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="4efdb-115">Hvis du forsøger, vises der en tom liste over LCS-projekter, og du kan ikke importere ER-konfigurationer fra aktivbiblioteket på projektniveau i LCS.</span><span class="sxs-lookup"><span data-stu-id="4efdb-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="4efdb-116">Hvis du vil have adgang til aktivbiblioteker på projektniveau fra et ER-lager, der bruges til at importere ER-konfigurationer, skal du logge på Finans ved hjælp af legitimationsoplysningerne for en bruger, der tilhører den lejer (domæne), som den aktuelle Finans-forekomst er klargjort til.</span><span class="sxs-lookup"><span data-stu-id="4efdb-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="4efdb-117">Slette en delt version af en datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="4efdb-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="4efdb-118">På siden **Konfigurationer** skal du i konfigurationstræet vælge **Eksempemodellkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="4efdb-119">Den første version af en eksempeldatamodelkonfiguration har du oprettet og udgivet til LCS, da du fuldførte proceduren [Overføre en ER-konfiguration til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="4efdb-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="4efdb-120">I denne procedure skal du slette den version af ER-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4efdb-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="4efdb-121">Derefter skal du importere denne version fra LCS senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="4efdb-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="4efdb-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4efdb-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4efdb-123">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="4efdb-124">Denne status angiver, at konfigurationen er blevet publiceret til LCS.</span><span class="sxs-lookup"><span data-stu-id="4efdb-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="4efdb-125">Vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-125">Select **Change status**.</span></span>
4. <span data-ttu-id="4efdb-126">Vælg **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="4efdb-127">Ved at skifte status for den valgte version fra **Delt** til **Annulleret** gøres versionen tilgængelig for sletning.</span><span class="sxs-lookup"><span data-stu-id="4efdb-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="4efdb-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-128">Select **OK**.</span></span>
6. <span data-ttu-id="4efdb-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4efdb-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4efdb-130">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Annulleret**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="4efdb-131">Vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-131">Select **Delete**.</span></span>
8. <span data-ttu-id="4efdb-132">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-132">Select **Yes**.</span></span>

    <span data-ttu-id="4efdb-133">Bemærk, at kun kladdeversion 2 af den valgte datamodelkonfiguration nu er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="4efdb-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="4efdb-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4efdb-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="4efdb-135">Importere en delt version af en datamodelkonfiguration fra LCS</span><span class="sxs-lookup"><span data-stu-id="4efdb-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="4efdb-136">Gå til **Virksomhedsadministration \> Arbejdsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="4efdb-137">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="4efdb-138">I feltet **Litware, Inc.** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="4efdb-139">Nu kan du åbne listen over lagre for konfigurationsudbyderen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4efdb-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="4efdb-140">Vælg **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-140">Select **Open**.</span></span>

    <span data-ttu-id="4efdb-141">I dette eksempel skal du vælge **LCS**-lageret og åbne det.</span><span class="sxs-lookup"><span data-stu-id="4efdb-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="4efdb-142">Du skal have [adgang](#accessconditions) til det LCS-projekt og til det aktivbibliotek, som det valgte ER-lager har adgang til.</span><span class="sxs-lookup"><span data-stu-id="4efdb-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="4efdb-143">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4efdb-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="4efdb-144">Vælg i dette eksempel den første version af **Eksempelmodelkonfiguration** på versionslisten.</span><span class="sxs-lookup"><span data-stu-id="4efdb-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="4efdb-145">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-145">Select **Import**.</span></span>
7. <span data-ttu-id="4efdb-146">Vælg **Ja** for at bekræfte importen af den valgte version fra LCS.</span><span class="sxs-lookup"><span data-stu-id="4efdb-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="4efdb-147">En informationsmeddelelse bekræfter, at den valgte version er blevet importeret.</span><span class="sxs-lookup"><span data-stu-id="4efdb-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="4efdb-148">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4efdb-148">Close the page.</span></span>
9. <span data-ttu-id="4efdb-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4efdb-149">Close the page.</span></span>
10. <span data-ttu-id="4efdb-150">Vælg **Konfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="4efdb-151">Vælg **Eksempelmodelkonfiguration** i træet.</span><span class="sxs-lookup"><span data-stu-id="4efdb-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="4efdb-152">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4efdb-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="4efdb-153">I dette eksempel skal du vælge den konfigurationsversion, der har statussen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="4efdb-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="4efdb-154">Bemærk, at den delte version 1 af den valgte datamodelkonfiguration nu også er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="4efdb-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]