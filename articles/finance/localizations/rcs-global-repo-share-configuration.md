---
title: Dele ER-konfigurationer i RCS/det globale lager med eksterne organisationer
description: Dette emne forklarer, hvordan du deler ER-konfigurationer (Electronic reporting) i Microsoft Regulatory Configuration Services (RCS)/det globale lager direkte med eksterne organisationer.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838739"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="ae6c6-103">Dele ER-konfiguration (Electronic reporting) i Regulatory Configuration Services (RCS)/det globale lager med eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae6c6-104">Du kan bruge Microsoft RCS (Regulatory Configuration Services) til at dele ER-konfigurationer (Electronic reporting) og derefter udgive dem til eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="ae6c6-105">I følgende procedurer forklares det, hvordan en RCS-bruger kan dele en version af en ER-konfiguration, der er konfigureret i en RCS-forekomst, med en ekstern organisation.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="ae6c6-106">Før du kan fuldføre disse procedurer, skal du fuldføre følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="ae6c6-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="ae6c6-107">Gå til en forekomst.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-107">Access an RCS instance.</span></span>
- <span data-ttu-id="ae6c6-108">Oprette en aktiv konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-108">Create an active configuration provider.</span></span> <span data-ttu-id="ae6c6-109">Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ae6c6-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="ae6c6-110">Oprette og uploade en ny version af en ER-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="ae6c6-111">Få flere oplysninger i [Oprette og uploade en ny version af en ER-konfiguration (Electronic reporting)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="ae6c6-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="ae6c6-112">Du skal også sikre dig, at der er klargjort et RCS-miljø til dit firma.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="ae6c6-113">I en Finance and Operations-app skal du gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ae6c6-114">Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – ekstern konfiguration** og derefter følge instruktionerne for at klargøre et.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="ae6c6-115">Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge side-URL-adressen til at få adgang til det ved at vælge indstillingen til logon.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="ae6c6-116">Kontrollér den konfiguration, du vil dele</span><span class="sxs-lookup"><span data-stu-id="ae6c6-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="ae6c6-117">Udfør følgende trin for at kontrollere, at den konfiguration, du vil dele, allerede er uploadet til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="ae6c6-118">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** for din konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigurationsudbydere](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="ae6c6-120">Vælg **Globalt lager** \> **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="ae6c6-121">Vælg den konfiguration, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="ae6c6-122">Du kan bruge filterfeltet til at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="ae6c6-123">Hvis du ikke kan finde konfigurationen i det globale lager, skal du følge trinnene i [Oprette og uploade en ny version af en ER-konfiguration (Electronic reporting)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="ae6c6-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="ae6c6-124">Dele ER-konfigurationer med eksterne organisationer</span><span class="sxs-lookup"><span data-stu-id="ae6c6-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="ae6c6-125">Når der er oprettet en konfiguration under din konfigurationsudbyder, kan du dele den direkte med eksterne organisationer ved hjælp af oversigtspanelet **Delt med** på siden **Globalt konfigurationslager**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="ae6c6-126">I arbejdsområdet **Elektronisk rapportering** skal du vælge **Lagre** for din konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="ae6c6-127">Vælg **Globalt lager** \> **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="ae6c6-128">Vælg den konfiguration, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="ae6c6-129">Gå til oversigtspanelet **Delt med**, og vælg **Organisation**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Delt med oversigtspanel](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="ae6c6-131">Angiv domænenavnet for den eksterne organisation i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Dialogboksen Del konfigurationsversion med ekstern organisation](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="ae6c6-133">Konfigurationen deles med den eksterne organisation og er tilgængelig for den pågældende organisation i det globale lager.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="ae6c6-134">Derfra kan den importeres til organisationens forekomst af RCS eller til dens forekomster af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="ae6c6-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="ae6c6-135">Hvis du vil annullere delingen af en konfiguration, der tidligere er delt med en ekstern organisation, skal du vælge konfigurationen og klikke på **Fjern deling** og derefter vælge **OK**</span><span class="sxs-lookup"><span data-stu-id="ae6c6-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]