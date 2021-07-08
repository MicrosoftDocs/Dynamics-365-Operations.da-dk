---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271177"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="c0683-103">Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c0683-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0683-104">Dette emne forklarer, hvordan du henter den nyeste version af [Konfigurationer af elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra det [delte aktivbibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c0683-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0683-105">Brugen af LCS som opbevaringslager for ER-konfigurationer [udfases](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="c0683-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="c0683-106">Du kan finde flere oplysninger under [RCS (Regulatory Configuration Service) – Lifecycle Services (LCS)-lagerudfasning](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="c0683-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="c0683-107">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="c0683-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c0683-108">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c0683-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="c0683-109">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c0683-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="c0683-110">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="c0683-110">System administrator</span></span>

2. <span data-ttu-id="c0683-111">Gå til **Organisationsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c0683-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="c0683-112">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c0683-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="c0683-113">I feltet **Microsoft** skal du vælge **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c0683-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c0683-114">[![Microsoft-felt på siden Lokaliseringskonfigurationer](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="c0683-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="c0683-115">På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="c0683-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="c0683-116">Hvis lageret ikke vises i gitteret, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="c0683-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="c0683-117">Vælg **Tilføj** for at tilføje et lager.</span><span class="sxs-lookup"><span data-stu-id="c0683-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="c0683-118">Vælg **LCS** som lagertype.</span><span class="sxs-lookup"><span data-stu-id="c0683-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="c0683-119">Vælg **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="c0683-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="c0683-120">Hvis du bliver spurgt om godkendelse, skal du følge vejledningen på skærmen.</span><span class="sxs-lookup"><span data-stu-id="c0683-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="c0683-121">Angiv et navn og en beskrivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="c0683-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="c0683-122">Vælg **OK** for at bekræfte den nye lagerpost.</span><span class="sxs-lookup"><span data-stu-id="c0683-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="c0683-123">I gitteret skal du vælge det nye lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="c0683-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="c0683-124">Vælg **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.</span><span class="sxs-lookup"><span data-stu-id="c0683-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="c0683-125">[![Siden Konfigurationslagre](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="c0683-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="c0683-126">Hvis du har problemer med at få adgang til LCS-lageret for at kunne hente konfigurationer fra det delte aktivbibliotek i LCS, kan du i stedet hente konfigurationer fra det [globale lager](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="c0683-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="c0683-127">I konfigurationstræet i venstre rude skal du vælge den ER-konfiguration, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="c0683-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="c0683-128">I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c0683-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="c0683-129">Vælg **Importér** for at download den valgte version fra LCS til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="c0683-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0683-130">Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="c0683-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="c0683-131">[![Siden Konfigurationslager](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="c0683-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c0683-132">Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="c0683-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="c0683-133">Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget.</span><span class="sxs-lookup"><span data-stu-id="c0683-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="c0683-134">Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion.</span><span class="sxs-lookup"><span data-stu-id="c0683-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="c0683-135">Se listen over relaterede emner til dette emne for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c0683-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0683-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c0683-136">Additional resources</span></span>

[<span data-ttu-id="c0683-137">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="c0683-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c0683-138">Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten</span><span class="sxs-lookup"><span data-stu-id="c0683-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
