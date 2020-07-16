---
title: Oprette ER-konfigurationer i RCS og overføre dem til det globale lager
description: Dette emne forklarer, hvordan du opretter en ER-konfiguration (Electronic reporting) i Microsoft Regulatory Configuration Services (RCS) og uploader den til det globale lager.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371237"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="251e8-103">Oprette ER-konfigurationer i RCS (Regulatory Configuration Services) og overføre dem til det globale lager</span><span class="sxs-lookup"><span data-stu-id="251e8-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="251e8-104">Du kan bruge Microsoft RCS (Regulatory Configuration Services) til at designe ER-konfigurationer (Electronic reporting) og udgive dem, så de kan bruges i organisationen.</span><span class="sxs-lookup"><span data-stu-id="251e8-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="251e8-105">Følgende procedurer forklarer, hvordan en bruger med rollen systemadministrator eller udvikler af elektronisk rapportering kan oprette en afledt version af en ER-konfiguration, der er konfigureret i en RCS-forekomst, og derefter overføre den afledte konfiguration til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="251e8-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="251e8-106">Før du kan fuldføre disse procedurer, skal du fuldføre følgende forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="251e8-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="251e8-107">Gå til en forekomst.</span><span class="sxs-lookup"><span data-stu-id="251e8-107">Access an RCS instance.</span></span>
- <span data-ttu-id="251e8-108">Oprette en aktiv konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="251e8-108">Create an active configuration provider.</span></span> <span data-ttu-id="251e8-109">Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="251e8-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="251e8-110">Du skal også sikre dig, at der er klargjort et RCS-miljø til dit firma.</span><span class="sxs-lookup"><span data-stu-id="251e8-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="251e8-111">I en Finance and Operations-app skal du gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="251e8-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="251e8-112">Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – ekstern konfiguration** og derefter følge instruktionerne for at klargøre et.</span><span class="sxs-lookup"><span data-stu-id="251e8-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="251e8-113">Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge side-URL-adressen til at få adgang til det ved at vælge indstillingen til logon.</span><span class="sxs-lookup"><span data-stu-id="251e8-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="251e8-114">Oprette en afledt version af en konfiguration i RCS</span><span class="sxs-lookup"><span data-stu-id="251e8-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="251e8-115">I arbejdsområdet **Elektronisk rapportering** skal du kontrollere, at du har en aktiv konfigurationsprovider til din organisation.</span><span class="sxs-lookup"><span data-stu-id="251e8-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="251e8-116">Vælg **Rapporteringskonfigurationer**.</span><span class="sxs-lookup"><span data-stu-id="251e8-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="251e8-117">Vælg den konfiguration, som du vil aflede en ny version af.</span><span class="sxs-lookup"><span data-stu-id="251e8-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="251e8-118">Du kan bruge filterfeltet oven over træet til at indsnævre søgningen.</span><span class="sxs-lookup"><span data-stu-id="251e8-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="251e8-119">Vælg **Opret konfiguration** \> **Afledt fra navn**.</span><span class="sxs-lookup"><span data-stu-id="251e8-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="251e8-120">Angiv et navn og en beskrivelse, og vælg derefter **Opret konfiguration** for at oprette en ny afledt version.</span><span class="sxs-lookup"><span data-stu-id="251e8-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="251e8-121">Vælg den netop afledte konfiguration, tilføj en beskrivelse af versionen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="251e8-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="251e8-122">Statussen for konfigurationen er ændret til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="251e8-122">The status of the configuration to is changed to **Completed**.</span></span>

![Ny konfigurationsversion i RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="251e8-124">Når konfigurationsstatussen ændres, kan du få vist en meddelelse om valideringsfejl, der er relateret til de tilknyttede programmer.</span><span class="sxs-lookup"><span data-stu-id="251e8-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="251e8-125">Hvis du vil deaktivere valideringen, skal du vælge bruger parametre i handlingsruden under fanen **Konfigurationer**, vælge **Brugerparametre** og derefter angive indstillingen **Spring validering ved skift og rebasering af konfigurationsstatus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="251e8-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="251e8-126">Uploade en konfiguration til det globale lager</span><span class="sxs-lookup"><span data-stu-id="251e8-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="251e8-127">Hvis du vil dele en ny eller afledt konfiguration i din organisation, kan du uploade den til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="251e8-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="251e8-128">Vælg den fuldførte version af konfigurationen, og vælg derefter **Upload til lager**.</span><span class="sxs-lookup"><span data-stu-id="251e8-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="251e8-129">Vælg indstillingen **Global (Microsoft)**, og vælg derefter **Send**.</span><span class="sxs-lookup"><span data-stu-id="251e8-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Uploade til lagerindstillingerne](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="251e8-131">Vælg **Ja** i bekræftelsesmeddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="251e8-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="251e8-132">Opdater beskrivelsen af versionen efter behov, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="251e8-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="251e8-133">Status for konfigurationen opdateres til **Del**, og konfigurationen overføres til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="251e8-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="251e8-134">Derfra kan du arbejd med den på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="251e8-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="251e8-135">Importere den til Dynamics 365-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="251e8-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="251e8-136">Du kan finde flere oplysninger under [(ER) Importér konfigurationer fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="251e8-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="251e8-137">Del det med en tredjepart eller en ekstern organisation. Se [RCS ER-konfigurationer (Electronic reporting) med eksterne organisationer](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="251e8-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Den afledte Intrastat Contoso-konfigurationsversion i det globale lager](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)