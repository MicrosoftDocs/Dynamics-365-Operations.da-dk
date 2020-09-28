---
title: Installere tilføjelsesprogrammet IoT-viden i LCS
description: I dette emne forklares, hvordan du kan installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae6b36c40d2f2f9e5266dfb3e2d1cbbb57755222
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803085"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="b348c-103">Installere tilføjelsesprogrammet IoT-viden i LCS</span><span class="sxs-lookup"><span data-stu-id="b348c-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b348c-104">I dette emne forklares, hvordan du kan installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b348c-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b348c-105">Bemærk, at tilføjelsesprogrammer ikke kan installeres i et demo- eller testmiljø.</span><span class="sxs-lookup"><span data-stu-id="b348c-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="b348c-106">Før du kan installere tilføjelsesprogrammet, skal du [oprette Azure-ressourcerne](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b348c-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="b348c-107">Konfigurere LCS-miljøet</span><span class="sxs-lookup"><span data-stu-id="b348c-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="b348c-108">Åbn LCS, og gå til dit Microsoft Dynamics 365 Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="b348c-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="b348c-109">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="b348c-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="b348c-110">Vælg **Installér et nyt tilføjelsesprogram** for at få vist listen over de tilføjelsesprogrammer, der er aktiveret for miljøet.</span><span class="sxs-lookup"><span data-stu-id="b348c-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="b348c-111">Vælg **IoT-viden** i dialogboksen **Vælg et tilføjelsesprogram, der skal installeres**.</span><span class="sxs-lookup"><span data-stu-id="b348c-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="b348c-112">Gå til dialogboksen **Konfigurer tilføjelsesprogram**, og angiv detaljerne i din IoT-hub og Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="b348c-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="b348c-113">Du kan finde de nødvendige værdier i den key vault, du har oprettet under [Oprette Azure-ressourcer](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b348c-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="b348c-114">**Lejer-id** – gå til key vault'en på Azure-portalen, og vælg derefter **Oversigt** i den venstre navigationsrude, kopiér værdien for **Mappe-id**.</span><span class="sxs-lookup"><span data-stu-id="b348c-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="b348c-115">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="b348c-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="b348c-116">**URI-adresse til IoT Event Hub-kompatibel slutpunkts-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="b348c-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="b348c-117">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="b348c-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="b348c-118">**Hemmeligt navn for IoT Event Hub-kompatibel slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for IoT-hubben er gemt.</span><span class="sxs-lookup"><span data-stu-id="b348c-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="b348c-119">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="b348c-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="b348c-120">**URI-adresse til Redis-cache-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="b348c-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="b348c-121">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="b348c-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="b348c-122">**Hemmeligt navn for Redis-cache-slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for Redis-cachen er gemt.</span><span class="sxs-lookup"><span data-stu-id="b348c-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="b348c-123">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="b348c-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="b348c-124">Markér afkrydsningsfeltet for at acceptere vilkår og betingelser.</span><span class="sxs-lookup"><span data-stu-id="b348c-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="b348c-125">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="b348c-125">Select **Install**.</span></span>
8. <span data-ttu-id="b348c-126">Der vises en meddelelsesboks, som angiver, at "Tilføjelsesprogram er blevet udløst til installation".</span><span class="sxs-lookup"><span data-stu-id="b348c-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="b348c-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b348c-127">Select **OK**.</span></span>

<span data-ttu-id="b348c-128">LCS-opsætning er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="b348c-128">LCS setup is now completed.</span></span> <span data-ttu-id="b348c-129">I det næste trin skal du konfigurere [scenarierne](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b348c-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="b348c-130">Fjern tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="b348c-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="b348c-131">I Supply Chain Management skal du [deaktivere scenarierne](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="b348c-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="b348c-132">I LCS skal du gå til Supply Chain Management-miljødetaljerne.</span><span class="sxs-lookup"><span data-stu-id="b348c-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="b348c-133">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="b348c-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="b348c-134">Vælg **Fjern** for tilføjelsesprogrammet IoT-viden.</span><span class="sxs-lookup"><span data-stu-id="b348c-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
