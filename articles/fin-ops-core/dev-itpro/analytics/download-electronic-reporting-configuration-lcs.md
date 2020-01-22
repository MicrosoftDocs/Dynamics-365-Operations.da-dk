---
title: Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services
description: I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 4cc14860bd969048c4378b40d97a7940a8710e89
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934648"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="73662-103">Download af elektroniske rapporteringskonfigurationer fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="73662-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73662-104">I dette emne beskrives det, hvordan du henter konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="73662-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="73662-105">Dette selvstudium fører dig gennem processen med at hente den nyeste version af konfigurationer af elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="73662-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="73662-106">Log på programmet ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="73662-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="73662-107">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="73662-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="73662-108">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="73662-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="73662-109">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="73662-109">System administrator</span></span>

2. <span data-ttu-id="73662-110">Gå til **Organisationsadministration** &gt; **Arbejdsområder** &gt; **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="73662-110">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="73662-111">I sektionen **Konfigurationsudbydere** skal du vælge feltet **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="73662-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="73662-112">I feltet **Microsoft** skal du klikke på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="73662-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="73662-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="73662-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="73662-114">På siden **Konfigurationslagre** i gitteret, skal du vælge det eksisterende lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="73662-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="73662-115">Hvis lageret ikke vises i gitteret, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="73662-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="73662-116">Klik på **Tilføj** for at tilføje et nyt lager.</span><span class="sxs-lookup"><span data-stu-id="73662-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="73662-117">Vælg **LCS** som lagertype.</span><span class="sxs-lookup"><span data-stu-id="73662-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="73662-118">Klik på **Opret lager**.</span><span class="sxs-lookup"><span data-stu-id="73662-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="73662-119">Hvis du bliver spurgt, skal du følge godkendelsesinstruktionerne.</span><span class="sxs-lookup"><span data-stu-id="73662-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="73662-120">Angiv et navn og en beskrivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="73662-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="73662-121">Klik på **OK** at bekræfte den nye lagerpost.</span><span class="sxs-lookup"><span data-stu-id="73662-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="73662-122">I gitteret skal du vælge det nye lager for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="73662-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="73662-123">Klik på **Åbn** for at få vist listen over ER-konfigurationer for det valgte lager.</span><span class="sxs-lookup"><span data-stu-id="73662-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="73662-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="73662-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="73662-125">I konfigurationstræet i venstre rude skal du vælge de ER-konfigurationer, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="73662-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="73662-126">I oversigtspanelet **Versioner** skal vælge den krævede version af den valgte ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73662-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="73662-127">Klik på **Importer** til at hente den valgte version fra LCS til den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="73662-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="73662-128">Knappen **Importer** er ikke tilgængelig for ER-konfigurationsversioner, der allerede findes på den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="73662-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="73662-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="73662-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="73662-130">Konfigurationer valideres, efter de er importeret, afhængigt af ER-indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="73662-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="73662-131">Du kan blive underrettet om eventuelle uoverensstemmelsesproblemer, der er opdaget.</span><span class="sxs-lookup"><span data-stu-id="73662-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="73662-132">Du skal løse disse problemer, før du kan bruge den importerede konfigurationsversion.</span><span class="sxs-lookup"><span data-stu-id="73662-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="73662-133">Se listen over relaterede artikler i dette emne for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="73662-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73662-134">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="73662-134">Additional resources</span></span>

[<span data-ttu-id="73662-135">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="73662-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
