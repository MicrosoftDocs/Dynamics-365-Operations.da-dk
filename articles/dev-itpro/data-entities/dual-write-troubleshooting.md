---
title: Fejlfindingsvejledning til dataintegration
description: Dette emne indeholder fejlfindingsoplysninger for dataintegration mellem Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873099"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="64228-103">Fejlfindingsvejledning til dataintegration</span><span class="sxs-lookup"><span data-stu-id="64228-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="64228-104">Aktivere plug-in-sporingslogge i Common Data Service og se fejldetaljerne for dobbeltskrivnings-plug-in</span><span class="sxs-lookup"><span data-stu-id="64228-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="64228-105">Hvis du oplever problemer eller fejl under dobbeltskrivningssynkronisering, skal du følge disse trin for at undersøge fejlene i sporingslogfilen.</span><span class="sxs-lookup"><span data-stu-id="64228-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="64228-106">Før du kan kontrollere fejlene, skal du aktivere sporingslogge til plug-ins.</span><span class="sxs-lookup"><span data-stu-id="64228-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="64228-107">Du kan finde instruktioner i afsnittet "Vise sporingslogfiler" [Selvstudium: skrive og registrere en plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="64228-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="64228-108">Nu kan du inspicere fejlene.</span><span class="sxs-lookup"><span data-stu-id="64228-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="64228-109">Log på Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="64228-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="64228-110">Vælg knappen **Indstillinger** (tandhjulsymbolet), og vælg derefter **Avancerede indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="64228-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="64228-111">I menuen **Indstillinger** skal du vælge **Tilpasning \> Plug-in-sporingslogfil**.</span><span class="sxs-lookup"><span data-stu-id="64228-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="64228-112">Vælg typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for at få vist fejloplysningerne.</span><span class="sxs-lookup"><span data-stu-id="64228-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="64228-113">Inspicere fejl ved dobbeltskrivningssynkronisering i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="64228-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="64228-114">Udfør følgende trin for at kontrollere fejl under testen.</span><span class="sxs-lookup"><span data-stu-id="64228-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="64228-115">Log på Microsoft Dynamics LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="64228-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="64228-116">Åbn det LCS-projekt, du vil udføre dobbeltskrivningstest for.</span><span class="sxs-lookup"><span data-stu-id="64228-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="64228-117">Vælg **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="64228-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="64228-118">Opret en forbindelse til Fjernskrivebord på den virtuelle Dynamics 365 for Finance and Operations-maskine (VM) ved hjælp af en lokal konto, der vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="64228-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="64228-119">Åbn Logbog.</span><span class="sxs-lookup"><span data-stu-id="64228-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="64228-120">Gå til **Logfiler for programmer og tjenester \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationel**.</span><span class="sxs-lookup"><span data-stu-id="64228-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="64228-121">Fejlene og detaljerne vises.</span><span class="sxs-lookup"><span data-stu-id="64228-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="64228-122">Frakoble ét Common Data Service-miljø fra Finance and Operations og tilknytte et andet miljø</span><span class="sxs-lookup"><span data-stu-id="64228-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="64228-123">Hvis du vil opdatere links, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="64228-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="64228-124">Gå til Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="64228-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="64228-125">Åbn Datastyring.</span><span class="sxs-lookup"><span data-stu-id="64228-125">Open Data Management.</span></span>
3. <span data-ttu-id="64228-126">Vælg **Link til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="64228-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="64228-127">Markér alle de tilknytninger, der kører, og vælg derefter **Stop**.</span><span class="sxs-lookup"><span data-stu-id="64228-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="64228-128">Vælg alle tilknytninger, og vælge derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="64228-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64228-129">Indstillingen **Slet** er ikke tilgængelig, hvis skabelonen **CustomerV3-Account** er valgt.</span><span class="sxs-lookup"><span data-stu-id="64228-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="64228-130">Fjern markeringen af denne skabelon efter behov.</span><span class="sxs-lookup"><span data-stu-id="64228-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="64228-131">**CustomerV3-Account** er en ældre klargjort skabelon, der virker sammen med løsningen Kundeemne til kontant.</span><span class="sxs-lookup"><span data-stu-id="64228-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="64228-132">Fordi den er globalt frigivet, dukker den op under alle skabeloner.</span><span class="sxs-lookup"><span data-stu-id="64228-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="64228-133">Vælg **Ophæv sammenkædning af miljø**.</span><span class="sxs-lookup"><span data-stu-id="64228-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="64228-134">Vælg **Ja** for at bekræfte operationen.</span><span class="sxs-lookup"><span data-stu-id="64228-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="64228-135">Følg trinnene i [installationsvejledningen](https://aka.ms/dualwrite-docs) for at tilknytte det nye miljø.</span><span class="sxs-lookup"><span data-stu-id="64228-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
