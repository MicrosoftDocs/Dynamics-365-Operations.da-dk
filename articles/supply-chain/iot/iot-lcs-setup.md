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
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87d04c3df22e2d9ef56acb61e26304731a2a17a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206046"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="05fbc-103">Installere tilføjelsesprogrammet IoT-viden i LCS</span><span class="sxs-lookup"><span data-stu-id="05fbc-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05fbc-104">I dette emne forklares, hvordan du kan installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="05fbc-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="05fbc-105">Bemærk, at tilføjelsesprogrammer ikke kan installeres i et demo- eller testmiljø.</span><span class="sxs-lookup"><span data-stu-id="05fbc-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="05fbc-106">Før du kan installere tilføjelsesprogrammet, skal du [oprette Azure-ressourcerne](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="05fbc-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="05fbc-107">Konfigurere LCS-miljøet</span><span class="sxs-lookup"><span data-stu-id="05fbc-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="05fbc-108">Åbn LCS, og gå til dit Microsoft Dynamics 365 Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="05fbc-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="05fbc-109">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="05fbc-110">Vælg **Installér et nyt tilføjelsesprogram** for at få vist listen over de tilføjelsesprogrammer, der er aktiveret for miljøet.</span><span class="sxs-lookup"><span data-stu-id="05fbc-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="05fbc-111">Vælg **IoT-viden** i dialogboksen **Vælg et tilføjelsesprogram, der skal installeres**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="05fbc-112">Gå til dialogboksen **Konfigurer tilføjelsesprogram**, og angiv detaljerne i din IoT-hub og Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="05fbc-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="05fbc-113">Du kan finde de nødvendige værdier i den key vault, du har oprettet under [Oprette Azure-ressourcer](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="05fbc-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="05fbc-114">**Lejer-id** – gå til key vault'en på Azure-portalen, og vælg derefter **Oversigt** i den venstre navigationsrude, kopiér værdien for **Mappe-id**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="05fbc-115">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="05fbc-116">**URI-adresse til IoT Event Hub-kompatibel slutpunkts-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="05fbc-117">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="05fbc-118">**Hemmeligt navn for IoT Event Hub-kompatibel slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for IoT-hubben er gemt.</span><span class="sxs-lookup"><span data-stu-id="05fbc-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="05fbc-119">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="05fbc-120">**URI-adresse til Redis-cache-key vault** – gå til key vault'en, vælg **Oversigt** i den venstre navigationsrude, og kopiér værdien for **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="05fbc-121">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="05fbc-122">**Hemmeligt navn for Redis-cache-slutpunkt** – gå til key vault'en, og vælg derefter **Hemmeligheder** i venstre navigationsrude, og kopiér navnet på den hemmelighed, hvor hændelseshubbens forbindelsesstreng for Redis-cachen er gemt.</span><span class="sxs-lookup"><span data-stu-id="05fbc-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="05fbc-123">Indsæt den værdi i dialogboksen **Konfigurer tilføjelsesprogram**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="05fbc-124">Markér afkrydsningsfeltet for at acceptere vilkår og betingelser.</span><span class="sxs-lookup"><span data-stu-id="05fbc-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="05fbc-125">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-125">Select **Install**.</span></span>
8. <span data-ttu-id="05fbc-126">Der vises en meddelelsesboks, som angiver, at "Tilføjelsesprogram er blevet udløst til installation".</span><span class="sxs-lookup"><span data-stu-id="05fbc-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="05fbc-127">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-127">Select **OK**.</span></span>

<span data-ttu-id="05fbc-128">LCS-opsætning er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="05fbc-128">LCS setup is now completed.</span></span> <span data-ttu-id="05fbc-129">I det næste trin skal du konfigurere [scenarierne](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="05fbc-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="05fbc-130">Fjern tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="05fbc-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="05fbc-131">I Supply Chain Management skal du [deaktivere scenarierne](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="05fbc-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="05fbc-132">I LCS skal du gå til Supply Chain Management-miljødetaljerne.</span><span class="sxs-lookup"><span data-stu-id="05fbc-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="05fbc-133">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="05fbc-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="05fbc-134">Vælg **Fjern** for tilføjelsesprogrammet IoT-viden.</span><span class="sxs-lookup"><span data-stu-id="05fbc-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]