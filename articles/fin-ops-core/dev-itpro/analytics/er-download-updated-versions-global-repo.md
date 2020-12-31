---
title: Importere opdaterede versioner af ER-konfigurationer
description: Dette emne forklarer, hvordan du kan importere ER-konfigurationer (elektronisk rapportering) fra det globale lager til Konfigurationstjeneste.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679504"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="51f9a-103">Importere opdaterede versioner af ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="51f9a-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51f9a-104">ER-[lagre](general-electronic-reporting.md#Repository) (Elektroniske rapportering) bruges til at dele [ER-konfigurationer](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="51f9a-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="51f9a-105">Du kan [importere](download-electronic-reporting-configuration-lcs.md) ER-konfigurationer fra forskellige lagre i din forekomst af Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="51f9a-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="51f9a-106">Når du importerer ER-konfigurationer, [kan konfigurationsudbydere](general-electronic-reporting.md#Provider) udgive nye [versioner](general-electronic-reporting.md#component-versioning) af lagrene, så de kan deles.</span><span class="sxs-lookup"><span data-stu-id="51f9a-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="51f9a-107">Dette emne forklarer, hvordan du kan importere ER-fra det globale lager til Konfigurationstjeneste.</span><span class="sxs-lookup"><span data-stu-id="51f9a-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="51f9a-108">Du kan finde flere oplysninger under [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurationstjeneste](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="51f9a-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="51f9a-109">Gennemse de tilgængelige opdaterede versioner</span><span class="sxs-lookup"><span data-stu-id="51f9a-109">Review the available updated versions</span></span>

1. <span data-ttu-id="51f9a-110">Log på Finance ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="51f9a-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="51f9a-111">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="51f9a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="51f9a-112">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="51f9a-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="51f9a-113">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="51f9a-113">System administrator</span></span>

2. <span data-ttu-id="51f9a-114">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="51f9a-115">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Importer opdateringer af konfigurationsversioner** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Siden Lokaliseringskonfigurationer](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="51f9a-117">Gå til dialogboksen **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering** og vælg **Vis kun tilgængelige opdateringer** i feltet **Kørselstilstand**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="51f9a-118">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-118">Then select **OK**.</span></span> 

    ![Feltet Kørselstilstand er angivet til kun at vise tilgængelige opdateringer](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="51f9a-120">Gennemse de meddelelser, du modtager.</span><span class="sxs-lookup"><span data-stu-id="51f9a-120">Review the messages that you receive.</span></span> <span data-ttu-id="51f9a-121">Disse meddelelser indeholder følgende oplysninger om de ER-konfigurationer i den aktuelle forekomst af Finance, og hvordan de sammenligner indholdet af det globale lager:</span><span class="sxs-lookup"><span data-stu-id="51f9a-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="51f9a-122">Det samlede antal ER-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="51f9a-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="51f9a-123">ER-konfigurationer, der ikke findes i det globale lager</span><span class="sxs-lookup"><span data-stu-id="51f9a-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="51f9a-124">ER-konfigurationer, for hvilke den seneste version allerede er tilgængelig i den aktuelle forekomst af Finance (hvis du vil have vist den fulde liste over disse ER-konfigurationer, skal du vælge linket **Meddelelsesdetaljer**).</span><span class="sxs-lookup"><span data-stu-id="51f9a-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meddelelsen "Seneste versioner af følgende konfigurationer er allerede importeret" og meddelelsesdetaljer](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="51f9a-126">ER-konfigurationer, for hvilke den seneste version allerede er tilgængelig i det globale lager og kan importeres ind i den aktuelle forekomst af Finance (hvis du vil have vist den fulde liste over disse ER-konfigurationer, skal du vælge linket **Meddelelsesdetaljer**).</span><span class="sxs-lookup"><span data-stu-id="51f9a-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meddelelsen "Tilgængelige opdateringer" og meddelelsesdetaljer](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="51f9a-128">Importere tilgængelige opdaterede versioner</span><span class="sxs-lookup"><span data-stu-id="51f9a-128">Import available updated versions</span></span>

1. <span data-ttu-id="51f9a-129">Log på Finance ved hjælp af en af følgende roller:</span><span class="sxs-lookup"><span data-stu-id="51f9a-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="51f9a-130">Udvikler til elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="51f9a-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="51f9a-131">Funktionel konsulent i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="51f9a-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="51f9a-132">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="51f9a-132">System administrator</span></span>

2. <span data-ttu-id="51f9a-133">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="51f9a-134">På siden **Lokaliseringskonfigurationer** skal du vælge feltet **Importer opdateringer af konfigurationsversioner** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="51f9a-135">Gå til dialogboksen **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering** i feltet **Kørselstilstand**, vælg **Importer seneste opdateringer** for at importere de seneste versioner af ER-konfigurationer fra det globale lager i den aktuelle forekomst af Finance.</span><span class="sxs-lookup"><span data-stu-id="51f9a-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="51f9a-136">Hvis du vil planlægge et batchjob til importen, skal du i oversigtspanelet **Kør i baggrunden** angive indstillingen **Batchbehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="51f9a-137">Hvis du vil gentage importen med jævne mellemrum, skal du konfigurere den nødvendige gentagelse.</span><span class="sxs-lookup"><span data-stu-id="51f9a-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Feltet Kørselstilstand er angivet til Import seneste opdateringer](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="51f9a-139">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-139">Select **OK**.</span></span>
7. <span data-ttu-id="51f9a-140">Du kan finde ud af, hvilke konfigurationsversioner der er importeret, ved at følge et af disse trin:</span><span class="sxs-lookup"><span data-stu-id="51f9a-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="51f9a-141">Hvis du kører import interaktivt i stedet for at bruge et batchjob, skal du gennemse de meddelelser, du modtager.</span><span class="sxs-lookup"><span data-stu-id="51f9a-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Meddelelser, der modtages under en interaktiv importkørsel](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="51f9a-143">Hvis du kører importen i batchtilstand, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="51f9a-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="51f9a-144">Gå til **Almindeligt** \> **Forespørgsler** \> **Batchjob** \> **Mine batchjob**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="51f9a-145">Find og vælg jobbet **Importer opdateringer af versioner af konfigurationer af elektronisk rapportering**, og klik derefter på **Batchjob** i handlingsruden, og vælg **Batchjobhistorik** for at få vist jobhistorikken.</span><span class="sxs-lookup"><span data-stu-id="51f9a-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="51f9a-146">Gå til siden **Batchjobhistorik**, og vælg **Logfil**.</span><span class="sxs-lookup"><span data-stu-id="51f9a-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="51f9a-147">Vælg derefter linket **Meddelelsesdetaljer** i den meddelelse, du modtager, for at få vist jobbets logfil.</span><span class="sxs-lookup"><span data-stu-id="51f9a-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Joblogfil](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="51f9a-149">Vi anbefaler ikke, at du planlægger et tilbagevendende batchjob for at importere opdaterede versioner af ER-konfigurationer direkte fra det globale lager til et produktionsmiljø, da de importerede versioner med det samme vil være tilgængelige til anvendelse.</span><span class="sxs-lookup"><span data-stu-id="51f9a-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="51f9a-150">Brug i stedet denne fremgangsmåde til at implementere versioner af ER-konfigurationer til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="51f9a-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="51f9a-151">De kan derefter evalueres i sandkassemiljøet, før de installeres i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="51f9a-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51f9a-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="51f9a-152">Additional resources</span></span>

- [<span data-ttu-id="51f9a-153">Oversigt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="51f9a-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="51f9a-154">Hente ER-konfigurationer fra det globale lager til Konfigurationstjenesten</span><span class="sxs-lookup"><span data-stu-id="51f9a-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
