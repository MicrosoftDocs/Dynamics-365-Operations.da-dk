---
title: Fejlfindingsvejledning til dataintegration
description: Dette emne indeholder fejlfindingsoplysninger om dataintegration mellem Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797269"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="702ba-103">Fejlfindingsvejledning til dataintegration</span><span class="sxs-lookup"><span data-stu-id="702ba-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="702ba-104">Aktivere plug-in-sporing i Common Data Service, og se fejldetaljerne for dobbeltskrivnings-plug-in</span><span class="sxs-lookup"><span data-stu-id="702ba-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="702ba-105">Hvis du står over for et problem eller en fejl i synkronisering med dobbeltskrivning, kan du undersøge fejlene i sporingsloggen:</span><span class="sxs-lookup"><span data-stu-id="702ba-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="702ba-106">Før du kan inspicere fejlene, skal du aktivere plug-in-sporing ved hjælp af instruktionerne i [Registrere plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="702ba-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="702ba-107">Nu kan du inspicere fejlene.</span><span class="sxs-lookup"><span data-stu-id="702ba-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="702ba-108">Log på Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="702ba-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="702ba-109">Klik på indstillingsikonet (et tandhjul), og vælg **Avancerede indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="702ba-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="702ba-110">I menuen **Indstillinger** skal du vælge **Tilpasning > Plug-in-sporingslogfil**.</span><span class="sxs-lookup"><span data-stu-id="702ba-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="702ba-111">Klik på typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for at få vist fejloplysningerne.</span><span class="sxs-lookup"><span data-stu-id="702ba-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="702ba-112">Kontrollere fejl ved dobbeltskrivningssynkronisering i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="702ba-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="702ba-113">Du kan kontrollere fejlene under testen ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="702ba-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="702ba-114">Log på LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="702ba-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="702ba-115">Åbn det LCS-projekt, du har valgt til at udføre dobbeltskrivningstest.</span><span class="sxs-lookup"><span data-stu-id="702ba-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="702ba-116">Gå til Skybaserede miljøer.</span><span class="sxs-lookup"><span data-stu-id="702ba-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="702ba-117">Fjernskrivebord til Finance and Operations-VM ved hjælp af lokal konto, der vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="702ba-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="702ba-118">Åbn logbogen.</span><span class="sxs-lookup"><span data-stu-id="702ba-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="702ba-119">Naviger til **Logfiler for programmer og tjenester > Microsoft > Dynamics AX-DualWriteSync > Operationel**.</span><span class="sxs-lookup"><span data-stu-id="702ba-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="702ba-120">Fejlene og detaljerne vises.</span><span class="sxs-lookup"><span data-stu-id="702ba-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="702ba-121">Sådan frakobler og tilknytter du et andet Common Data Service-miljø fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="702ba-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="702ba-122">Du kan opdatere links ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="702ba-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="702ba-123">Naviger til Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="702ba-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="702ba-124">Åbn Datastyring.</span><span class="sxs-lookup"><span data-stu-id="702ba-124">Open Data Management.</span></span>
+ <span data-ttu-id="702ba-125">Klik på **Link til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="702ba-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="702ba-126">Vælg alle de kørende tilknytninger, og klik på **Stop**.</span><span class="sxs-lookup"><span data-stu-id="702ba-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="702ba-127">Vælg alle tilknytninger, og klik på **Slet**.</span><span class="sxs-lookup"><span data-stu-id="702ba-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="702ba-128">Indstillingen **Slet** vises ikke, hvis skabelonen **CustomerV3-Account** er valgt.</span><span class="sxs-lookup"><span data-stu-id="702ba-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="702ba-129">Fjern markeringen af den, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="702ba-129">Unselect it if needed.</span></span> <span data-ttu-id="702ba-130">**CustomerV3-Account** er en ældre klargjort skabelon, der virker sammen med løsningen Kundeemne til kontant.</span><span class="sxs-lookup"><span data-stu-id="702ba-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="702ba-131">Fordi den er globalt frigivet, dukker den op under alle skabeloner.</span><span class="sxs-lookup"><span data-stu-id="702ba-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="702ba-132">Klik på **Ophæv sammenkædning af miljø**.</span><span class="sxs-lookup"><span data-stu-id="702ba-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="702ba-133">Klik på **Ja** for at bekræfte.</span><span class="sxs-lookup"><span data-stu-id="702ba-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="702ba-134">Følg trinnene i [installationsvejledningen](https://aka.ms/dualwrite-docs) for at tilknytte det nye miljø.</span><span class="sxs-lookup"><span data-stu-id="702ba-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

