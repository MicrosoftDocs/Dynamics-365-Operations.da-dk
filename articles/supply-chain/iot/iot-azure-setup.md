---
title: Konfigurere Azure-ressourcer til IoT-viden
description: I dette emne forklares det, hvordan du opretter og konfigurerer de Microsoft Azure-ressourcer, du skal bruge til IoT-viden.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 431ad6766f1e7f2035d6d5ed87bed4856e58e098
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597258"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="5edb6-103">Konfigurere Azure-ressourcer til IoT-viden</span><span class="sxs-lookup"><span data-stu-id="5edb6-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5edb6-104">I dette emne forklares det, hvordan du opretter og konfigurerer de Microsoft Azure-ressourcer, du skal bruge til IoT-viden.</span><span class="sxs-lookup"><span data-stu-id="5edb6-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="5edb6-105">Oprette Azure-ressourcer</span><span class="sxs-lookup"><span data-stu-id="5edb6-105">Create Azure resources</span></span>

<span data-ttu-id="5edb6-106">Udfør følgende trin for at oprette en IoT-hub, en Redis-cache og en key vault, som Microsoft Dynamics 365 Supply Chain Management kan få adgang til.</span><span class="sxs-lookup"><span data-stu-id="5edb6-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="5edb6-107">Kontrollér, at det Microsoft Dynamics RP Microservices-førsteparts-id findes i din lejer</span><span class="sxs-lookup"><span data-stu-id="5edb6-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="5edb6-108">Benyt følgende fremgangsmåde for at kontrollere, at app-id'et for Microsoft Dynamics ERP Microservices-førstepartsappen følger disse trin.</span><span class="sxs-lookup"><span data-stu-id="5edb6-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-109">Log på Azure-portalen på <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="5edb6-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="5edb6-110">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="5edb6-111">Gå til **Virksomhedsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="5edb6-112">I feltet **Programtype** skal du vælge **Microsoft-programmer**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="5edb6-113">Angiv **Microsoft Dynamics ERP Microservices** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="5edb6-114">Kontrollér, at **Microsoft Dynamics ERP Microservices** er på listen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="5edb6-115">Andre programmer har lignende navne.</span><span class="sxs-lookup"><span data-stu-id="5edb6-115">Other applications have similar names.</span></span> <span data-ttu-id="5edb6-116">Du skal derfor sikre dig, at du finder det rigtige program.</span><span class="sxs-lookup"><span data-stu-id="5edb6-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="5edb6-117">App-id'et er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="5edb6-118">Hvis programmet ikke findes på listen, skal du føje det til din lejer:</span><span class="sxs-lookup"><span data-stu-id="5edb6-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="5edb6-119">På værktøjslinjen i Azure Portal skal du vælge knappen for at åbne Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="5edb6-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="5edb6-120">Kør kommandoen **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="5edb6-121">Angiv **Y** for at installere modulet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="5edb6-122">Kør kommandoen **Get-InstalledModule -Name "AzureAD"** for at kontrollere, at modulet er installeret.</span><span class="sxs-lookup"><span data-stu-id="5edb6-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="5edb6-123">Kør kommandoen **Connect-AzureAD -Confirm** for at køre godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="5edb6-124">Kør kommandoen **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="5edb6-125">Du kan nu gentage trin 1 til 6 for at kontrollere, at app-id'et findes i din lejer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="5edb6-126">Oprette en ny key vault-ressource</span><span class="sxs-lookup"><span data-stu-id="5edb6-126">Create a key vault resource</span></span>

<span data-ttu-id="5edb6-127">Benyt følgende fremgangsmåde for at oprette en ny key vault-ressource.</span><span class="sxs-lookup"><span data-stu-id="5edb6-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-128">Opret eller gå til en ressourcegruppe i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="5edb6-129">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-129">Select **Add**.</span></span>
3. <span data-ttu-id="5edb6-130">Gå til siden **Ny**, og angiv **Key vault** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="5edb6-131">Vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-131">Then select **Create**.</span></span>
4. <span data-ttu-id="5edb6-132">Gå til siden **Opret key vault**, og angiv et navn i **Key vault-navn**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="5edb6-133">Gennemse standardværdierne, og vælg derefter **Gennemgå + Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="5edb6-134">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-134">Select **Create**.</span></span>

<span data-ttu-id="5edb6-135">Key vaulten oprettes i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="5edb6-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="5edb6-136">Oprette en IoT Hub-ressource</span><span class="sxs-lookup"><span data-stu-id="5edb6-136">Create an IoT hub resource</span></span>

<span data-ttu-id="5edb6-137">Benyt følgende fremgangsmåde for at oprette en IoT Hub-ressource.</span><span class="sxs-lookup"><span data-stu-id="5edb6-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-138">Oprette eller gå til en ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="5edb6-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="5edb6-139">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-139">Select **Add**.</span></span>
3. <span data-ttu-id="5edb6-140">Gå til siden **Ny**, og angiv **Iot Hub** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="5edb6-141">Vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-141">Then select **Create**.</span></span>
4. <span data-ttu-id="5edb6-142">Angiv et navn i feltet **IoT Hub-navn**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="5edb6-143">Gennemse standardværdierne, og vælg derefter **Gennemgå + Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="5edb6-144">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-144">Select **Create**.</span></span>

<span data-ttu-id="5edb6-145">IoT Hub'en oprettes i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="5edb6-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="5edb6-146">Det anbefales, at du kun opretter én IoT Hub-ressource pr. miljø.</span><span class="sxs-lookup"><span data-stu-id="5edb6-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="5edb6-147">Oprette en Redis-cacheressource</span><span class="sxs-lookup"><span data-stu-id="5edb6-147">Create a Redis cache resource</span></span>

<span data-ttu-id="5edb6-148">Benyt følgende fremgangsmåde for at oprette en Redis-cacheressource.</span><span class="sxs-lookup"><span data-stu-id="5edb6-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-149">Oprette eller gå til en ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="5edb6-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="5edb6-150">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-150">Select **Add**.</span></span>
3. <span data-ttu-id="5edb6-151">Gå til siden **Ny**, og angiv **Azure Cache for Redis** i søgefeltet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="5edb6-152">Vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-152">Then select **Create**.</span></span>
4. <span data-ttu-id="5edb6-153">Indtast et navn i feltet **DNS-navn**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="5edb6-154">Gennemse standardværdierne, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="5edb6-155">Redis-cachen oprettes i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="5edb6-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="5edb6-156">Det anbefales, at du kun opretter én Redis-cacheressource pr. miljø.</span><span class="sxs-lookup"><span data-stu-id="5edb6-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="5edb6-157">Alle ressourcerne er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="5edb6-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="5edb6-158">Konfigurere Azure-ressourcerne</span><span class="sxs-lookup"><span data-stu-id="5edb6-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="5edb6-159">Konfigurere IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5edb6-159">Configure the IoT hub</span></span>

<span data-ttu-id="5edb6-160">Hvis du vil konfigurere IoT hub, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="5edb6-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-161">Vælg IoT hub-ressourcen i dine ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="5edb6-162">Vælg **Indbyggede slutpunkter** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="5edb6-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="5edb6-163">Indsæt følgende forbrugergrupper under **Forbrugergrupper**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="5edb6-164">Disse brugergrupper svarer til de færdiglavede scenarier.</span><span class="sxs-lookup"><span data-stu-id="5edb6-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="5edb6-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="5edb6-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="5edb6-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="5edb6-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="5edb6-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="5edb6-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="5edb6-168">Konfigurere key vaulten</span><span class="sxs-lookup"><span data-stu-id="5edb6-168">Configure the key vault</span></span>

<span data-ttu-id="5edb6-169">Benyt følgende fremgangsmåde for at konfigurere key vaulten.</span><span class="sxs-lookup"><span data-stu-id="5edb6-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-170">Vælg key vault-ressourcen i dine ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="5edb6-171">Vælg **Adgangspolitikker** i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="5edb6-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="5edb6-172">Vælg **Tilføj en adgangspolitik**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="5edb6-173">Gå til siden **Tilføj adgangspolitik**, og vælg **Hent** og **Vis** i feltet **Hemmelige tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="5edb6-174">Klik i feltet **Vælg hoved**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="5edb6-175">I dialogboksen **Principal** skal du søge efter og vælge **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="5edb6-176">Vælg derefter **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-176">Then select **Select**.</span></span>
7. <span data-ttu-id="5edb6-177">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-177">Select **Add**.</span></span>
8. <span data-ttu-id="5edb6-178">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-178">Select **Save**.</span></span>

<span data-ttu-id="5edb6-179">Appen har nu adgang til hemmeligheder i key vaulten.</span><span class="sxs-lookup"><span data-stu-id="5edb6-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="5edb6-180">Gemme hemmeligheden for IoT Hub-forbindelsesstrengen</span><span class="sxs-lookup"><span data-stu-id="5edb6-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="5edb6-181">Benyt følgende fremgangsmåde, hvis du vil gemme hemmeligheden for IoT Hub-forbindelsesstrengen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-182">Vælg IoT hub-ressourcen i dine ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="5edb6-183">Vælg **Indbyggede slutpunkter** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="5edb6-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="5edb6-184">Kopiér værdien i feltet **Event Hub-kompatibel slutpunkts-key vault**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="5edb6-185">Gå til key vault-ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="5edb6-186">Vælg **Hemmeligheder** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5edb6-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="5edb6-187">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="5edb6-188">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="5edb6-189">I feltet **Værdi** skal du indsætte den værdi for slutpunktet, du har kopieret tidligere.</span><span class="sxs-lookup"><span data-stu-id="5edb6-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="5edb6-190">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="5edb6-191">Gemme hemmeligheden for Redis-cacheforbindelsesstrengen</span><span class="sxs-lookup"><span data-stu-id="5edb6-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="5edb6-192">Benyt følgende fremgangsmåde, hvis du vil gemme hemmeligheden for Redis-cacheforbindelsesstrengen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="5edb6-193">Vælg Redis-cacheressourcen i dine ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="5edb6-194">Vælg **Adgangsnøgler**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="5edb6-195">Kopiér værdien i feltet **Primær forbindelsesstreng**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="5edb6-196">Gå til key vault-ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5edb6-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="5edb6-197">Vælg **Hemmeligheder** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5edb6-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="5edb6-198">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="5edb6-199">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="5edb6-200">I feltet **Værdi** skal du indsætte den forbindelsesstreng, du har kopieret tidligere.</span><span class="sxs-lookup"><span data-stu-id="5edb6-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="5edb6-201">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="5edb6-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="5edb6-202">Når du opdaterer en af forbindelsesstrengene, skal du også opdatere de hemmelige værdier.</span><span class="sxs-lookup"><span data-stu-id="5edb6-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="5edb6-203">Nu er du færdig med at klargøre de krævede Azure-ressourcer.</span><span class="sxs-lookup"><span data-stu-id="5edb6-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="5edb6-204">Det næste skridt er at [installere tilføjelsesprogrammet IoT-viden i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5edb6-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
