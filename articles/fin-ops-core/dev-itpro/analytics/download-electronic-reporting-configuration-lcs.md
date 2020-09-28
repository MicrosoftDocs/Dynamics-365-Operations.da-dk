---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810613"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="db2c1-103">Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="db2c1-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db2c1-104">Dette emne forklarer, hvordan du henter den nyeste version af [Konfigurationer af elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra det [delte aktivbibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="db2c1-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="db2c1-105">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="db2c1-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="db2c1-106">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="db2c1-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="db2c1-107">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="db2c1-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="db2c1-108">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="db2c1-108">System administrator</span></span>

2. <span data-ttu-id="db2c1-109">Gå til **Organisationsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="db2c1-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="db2c1-110">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="db2c1-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="db2c1-111">I feltet **Microsoft** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="db2c1-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="db2c1-112">[![Microsoft-felt på siden Lokaliseringskonfigurationer](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="db2c1-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="db2c1-113">På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="db2c1-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="db2c1-114">Hvis lageret ikke vises i gitteret, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="db2c1-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="db2c1-115">Vælg **Tilføj** for at tilføje et lager.</span><span class="sxs-lookup"><span data-stu-id="db2c1-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="db2c1-116">Vælg **LCS** som lagertype.</span><span class="sxs-lookup"><span data-stu-id="db2c1-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="db2c1-117">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="db2c1-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="db2c1-118">Hvis du bliver spurgt om godkendelse, skal du følge vejledningen på skærmen.</span><span class="sxs-lookup"><span data-stu-id="db2c1-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="db2c1-119">Angiv et navn og en beskrivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="db2c1-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="db2c1-120">Vælg **OK** for at bekræfte den nye lagerpost.</span><span class="sxs-lookup"><span data-stu-id="db2c1-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="db2c1-121">I gitteret skal du vælge det nye lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="db2c1-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="db2c1-122">Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.</span><span class="sxs-lookup"><span data-stu-id="db2c1-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="db2c1-123">[![Siden Konfigurationslagre](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="db2c1-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="db2c1-124">Hvis du har problemer med at få adgang til LCS-lageret for at kunne hente konfigurationer fra det delte aktivbibliotek i LCS, kan du i stedet hente konfigurationer fra det [globale lager](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="db2c1-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="db2c1-125">I konfigurationstræet i venstre rude skal du vælge den ER-konfiguration, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="db2c1-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="db2c1-126">I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="db2c1-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="db2c1-127">Vælg **Importér** for at download den valgte version fra LCS til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="db2c1-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db2c1-128">Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="db2c1-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="db2c1-129">[![Siden Konfigurationslager](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="db2c1-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="db2c1-130">Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="db2c1-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="db2c1-131">Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget.</span><span class="sxs-lookup"><span data-stu-id="db2c1-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="db2c1-132">Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion.</span><span class="sxs-lookup"><span data-stu-id="db2c1-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="db2c1-133">Se listen over relaterede emner til dette emne for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="db2c1-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db2c1-134">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="db2c1-134">Additional resources</span></span>

[<span data-ttu-id="db2c1-135">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="db2c1-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="db2c1-136">Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten</span><span class="sxs-lookup"><span data-stu-id="db2c1-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
