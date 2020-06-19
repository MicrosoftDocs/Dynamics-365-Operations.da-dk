---
title: Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten
description: Dette emne forklarer, hvordan du kan hente ER-konfigurationer (elektronisk rapportering) fra det globale lager til Konfigurationstjenesten.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421696"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="b2cb4-103">Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten</span><span class="sxs-lookup"><span data-stu-id="b2cb4-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2cb4-104">Dette emne forklarer, hvordan du kan hente [ER-konfigurationer (elektronisk rapportering)](general-electronic-reporting.md#Configuration) fra det globale lager til konfigurationstjenesten.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="b2cb4-105">Du kan finde flere oplysninger under [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurationstjeneste](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="b2cb4-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="b2cb4-106">Åbn konfigurationslageret</span><span class="sxs-lookup"><span data-stu-id="b2cb4-106">Open configurations repository</span></span>

1. <span data-ttu-id="b2cb4-107">Log på programmet Dynamics 365 Finance ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="b2cb4-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="b2cb4-108">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="b2cb4-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="b2cb4-109">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="b2cb4-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b2cb4-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="b2cb4-110">System administrator</span></span>

2. <span data-ttu-id="b2cb4-111">Gå til **Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="b2cb4-112">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="b2cb4-113">I feltet **Microsoft** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Arbejdsområde til elektronisk rapportering](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="b2cb4-115">På siden **Konfigurationslagre** i gitteret skal du vælge det eksisterende lager for **Global**-typen.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="b2cb4-116">Hvis lageret ikke vises i gitteret, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="b2cb4-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b2cb4-117">Vælg **Tilføj** for at tilføje et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="b2cb4-118">Vælg **Global** som lagertype, og vælg derefter **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="b2cb4-119">Hvis du bliver spurgt, skal du følge godkendelsesinstruktionerne.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="b2cb4-120">Angiv et navn til og en beskrivelse af lagringsstedet, og vælg derefter **OK** for at bekræfte den nye lagerpost.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="b2cb4-121">I gitteret skal du vælge det nye lager for **Global**-typen.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="b2cb4-122">Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Siden Konfigurationslagre](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="b2cb4-124">Importere en enkelt konfiguration</span><span class="sxs-lookup"><span data-stu-id="b2cb4-124">Import a single configuration</span></span>

1. <span data-ttu-id="b2cb4-125">På siden **Konfigurationslagre** skal du i konfigurationstræet vælge den ER-konfiguration, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="b2cb4-126">I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="b2cb4-127">Vælg **Importér** for at hente den valgte version fra Global-lager til den aktuelle Finans-forekomst.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2cb4-128">Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes i den aktuelle Finans-forekomst.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Siden Konfigurationslager](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="b2cb4-130">Importere filtrerede konfigurationer</span><span class="sxs-lookup"><span data-stu-id="b2cb4-130">Import filtered configurations</span></span>

1. <span data-ttu-id="b2cb4-131">På siden **Konfigurationslagre** skal du i konfigurationstræet udvide oversigtspanelet **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="b2cb4-132">I gitteret **Koder** skal du tilføje eventuelle koder, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="b2cb4-133">I feltet **Land/område** skal du vælge de relevante lande-/områdekoder og derefter vælge **Anvend filter**.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2cb4-134">Oversigtspanelet **Konfigurationer** viser alle de konfigurationer, der opfylder de angivne udvælgelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="b2cb4-135">I oversigtspanelet **Konfigurationer** skal du vælge **Importér** for at hente de filtrerede konfigurationer fra det globale lager til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="b2cb4-136">I oversigtspanelet **Konfigurationer** skal du vælge **Nulstil filter** for at rydde op i de angivne udvælgelsesbetingelser.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Siden Konfigurationslager](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="b2cb4-138">Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b2cb4-139">Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b2cb4-140">Før du kan bruge den importerede konfigurationsversion, skal du løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="b2cb4-141">Se listen over relaterede ressourcer i dette emne for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="b2cb4-142">ER-konfigurationer kan konfigureres som værende afhængige af andre konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="b2cb4-143">Sammen med en valgt konfiguration kan andre konfigurationer derfor blive importeret automatisk.</span><span class="sxs-lookup"><span data-stu-id="b2cb4-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="b2cb4-144">Yderligere oplysninger om konfigurationsafhængigheder finder du i [Definere afhængigheden for ER-konfigurationer af andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="b2cb4-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2cb4-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b2cb4-145">Additional resources</span></span>

[<span data-ttu-id="b2cb4-146">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b2cb4-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
