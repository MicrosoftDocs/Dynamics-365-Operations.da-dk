---
title: Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration
description: Dette emne beskriver, hvordan du kommer i gang med tilføjelsesprogrammet til elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592520"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="1598b-103">Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration</span><span class="sxs-lookup"><span data-stu-id="1598b-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1598b-104">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="1598b-104">Prerequisites</span></span>

<span data-ttu-id="1598b-105">Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="1598b-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="1598b-106">Du skal have adgang til din Microsoft Dynamics Lifecycle Services-konto (LCS).</span><span class="sxs-lookup"><span data-stu-id="1598b-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="1598b-107">Du skal have et LCS-projekt, der omfatter version 10.0.17 eller en senere version af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1598b-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1598b-108">Derudover skal disse apps implementeres i en af følgende Azure-geografisk områder:</span><span class="sxs-lookup"><span data-stu-id="1598b-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="1598b-109">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-109">East US</span></span>
    - <span data-ttu-id="1598b-110">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-110">West US</span></span>
    - <span data-ttu-id="1598b-111">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-111">North EU</span></span>
    - <span data-ttu-id="1598b-112">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-112">West EU</span></span>

- <span data-ttu-id="1598b-113">Du skal have adgang til din Dynamics 365 Regulatory Configuration Services (RCS-konto).</span><span class="sxs-lookup"><span data-stu-id="1598b-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="1598b-114">Du skal aktivere globaliseringsfunktionen for din RCS-konto i modulet Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="1598b-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="1598b-115">Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="1598b-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="1598b-116">Du skal oprette en Key Vault og en lagerkonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="1598b-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="1598b-117">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="1598b-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="1598b-118">Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="1598b-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="1598b-119">Log på din LCS-konto.</span><span class="sxs-lookup"><span data-stu-id="1598b-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="1598b-120">Vælg feltet **Prøveversion af funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="1598b-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="1598b-121">I afsnittet **Funktioner til offentlig visning** skal du vælge en **e-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="1598b-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="1598b-122">Kontroller, at indstillingen **Prøveversion af funktion aktiveret** er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1598b-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="1598b-123">Vælg dit LCS-implementeringsprojekt på LCS-dashboardet.</span><span class="sxs-lookup"><span data-stu-id="1598b-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="1598b-124">LCS-projektet skal køre.</span><span class="sxs-lookup"><span data-stu-id="1598b-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="1598b-125">Vælg **Installér et nyt tilføjelsesprogram** på fanen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="1598b-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="1598b-126">Vælg **e-faktureringstjenester**, og angiv i feltet **AAD-ansøgnings-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="1598b-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="1598b-127">Denne værdi er en fast værdi.</span><span class="sxs-lookup"><span data-stu-id="1598b-127">This is a fixed value.</span></span>
10. <span data-ttu-id="1598b-128">Angiv lejer-id for din Azure-abonnementskonto i feltet **AAD-lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="1598b-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="1598b-129">Gennemse vilkår og betingelser, og marker afkrydsningsfeltet.</span><span class="sxs-lookup"><span data-stu-id="1598b-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="1598b-130">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="1598b-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="1598b-131">Konfigurer parametre for RCS-integration med tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="1598b-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="1598b-132">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="1598b-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1598b-133">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="1598b-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="1598b-134">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URI i feltet **Serviceslutpunkt URI** under fanen **e-faktureringsservice**.</span><span class="sxs-lookup"><span data-stu-id="1598b-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1598b-135">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="1598b-135">Datacenter Azure geography</span></span> | <span data-ttu-id="1598b-136">URI for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="1598b-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1598b-137">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-138">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-139">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-140">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="1598b-141">Kontrollér, at **Applikations-id** er angivet til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="1598b-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="1598b-142">Denne værdi er en fast værdi.</span><span class="sxs-lookup"><span data-stu-id="1598b-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="1598b-143">Angiv id'et for din LCS-abonnementskonto i feltet **LCS-miljø-id**.</span><span class="sxs-lookup"><span data-stu-id="1598b-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="1598b-144">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="1598b-145">Oprette Key Vault-hemmelighed</span><span class="sxs-lookup"><span data-stu-id="1598b-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="1598b-146">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="1598b-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1598b-147">I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="1598b-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="1598b-148">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.</span><span class="sxs-lookup"><span data-stu-id="1598b-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="1598b-149">Vælg **Ny** for at oprette en key vault-hemmelighed.</span><span class="sxs-lookup"><span data-stu-id="1598b-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="1598b-150">Angiv navnet på key vault-hemmeligheden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1598b-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="1598b-151">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1598b-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1598b-152">Indsæt hemmeligheden fra Azure Key Vault i feltet **Key Vault URI**.</span><span class="sxs-lookup"><span data-stu-id="1598b-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="1598b-153">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1598b-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="1598b-154">Oprette hemmelig lagerkonto</span><span class="sxs-lookup"><span data-stu-id="1598b-154">Create Storage account secret</span></span>

1. <span data-ttu-id="1598b-155">Gå til **Systemadministration** > **Konfiguration** > **Key Vault-parametre**, og vælg en hemmelig Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1598b-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1598b-156">Vælg **Tilføj** under **Certifikater**.</span><span class="sxs-lookup"><span data-stu-id="1598b-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1598b-157">I feltet **Navn** angives navnet på den hemmelige lagerkonto og i feltet **Beskrivelse** indsættes en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1598b-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1598b-158">I **Type**-feltet skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="1598b-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1598b-159">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="1598b-160">Oprette en digital certifikathemmelighed</span><span class="sxs-lookup"><span data-stu-id="1598b-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="1598b-161">Gå til **Systemadministration** > **Konfiguration** > **Key Vault-parametre**, og vælg en hemmelig Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1598b-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="1598b-162">Vælg **Tilføj** under **Certifikater**.</span><span class="sxs-lookup"><span data-stu-id="1598b-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="1598b-163">I feltet **Navn** angives navnet på det hemmelige digitale certifikat, og i feltet **Beskrivelse** indsættes en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="1598b-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1598b-164">I **Type**-feltet skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="1598b-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="1598b-165">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="1598b-166">Opret et miljø for tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="1598b-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="1598b-167">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="1598b-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1598b-168">I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Tilføjelsesprogram til elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="1598b-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="1598b-169">Opret et servicemiljø</span><span class="sxs-lookup"><span data-stu-id="1598b-169">Create a service environment</span></span>

1. <span data-ttu-id="1598b-170">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1598b-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="1598b-171">Vælg **Ny** for at oprette et nyt servicemiljø.</span><span class="sxs-lookup"><span data-stu-id="1598b-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="1598b-172">Angiv navnet på e-faktureringsmiljøet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1598b-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="1598b-173">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1598b-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="1598b-174">Vælg navnet på den hemmelige lagerkonto, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.</span><span class="sxs-lookup"><span data-stu-id="1598b-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="1598b-175">I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet, og også oprette forbindelse til lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="1598b-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="1598b-176">Angiv **Bruger-id** i feltet for brugerens alias.</span><span class="sxs-lookup"><span data-stu-id="1598b-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="1598b-177">I feltet **E-mail** skal du angive brugerens e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="1598b-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="1598b-178">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1598b-178">Select **Save**.</span></span>
8. <span data-ttu-id="1598b-179">Hvis dine lande-/områdespecifikke fakturaer kræver en kæde af certifikater for at anvende en digital signaturer, skal du vælge **Key Vault-parametre** i handlingsruden og derefter vælge **Kæde af certifikater** og følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1598b-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="1598b-180">Vælg **Ny** for at oprette en kæde af certifikater.</span><span class="sxs-lookup"><span data-stu-id="1598b-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="1598b-181">Angiv navnet på kæden af certifikater i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1598b-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="1598b-182">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1598b-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="1598b-183">I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.</span><span class="sxs-lookup"><span data-stu-id="1598b-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="1598b-184">Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden.</span><span class="sxs-lookup"><span data-stu-id="1598b-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="1598b-185">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="1598b-186">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-186">Close the page.</span></span>
9. <span data-ttu-id="1598b-187">Vælg **Udgiv** i handlingsruden for at publicere miljøet til skyen på siden **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="1598b-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="1598b-188">Værdien i feltet **Status** ændres til **Publiceret**.</span><span class="sxs-lookup"><span data-stu-id="1598b-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="1598b-189">Opret en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="1598b-189">Create a connected application</span></span>

1. <span data-ttu-id="1598b-190">På siden **Miljøopsætninger** skal du vælge **Tilsluttede applikationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1598b-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="1598b-191">Vælg **Ny** for at oprette en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="1598b-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="1598b-192">Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1598b-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="1598b-193">I feltet **Applikation** skal du angive URL-adressen til det finans- og Supply Chain Management-miljø, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="1598b-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="1598b-194">I feltet **Lejer** skal du angive den lejer til finans- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1598b-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="1598b-195">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="1598b-195">Select **Save**.</span></span>
6. <span data-ttu-id="1598b-196">Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="1598b-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="1598b-197">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="1598b-198">Sammenkæd tilknyttede applikationer med miljøer</span><span class="sxs-lookup"><span data-stu-id="1598b-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="1598b-199">På siden **Miljøopsætninger** skal du vælge **Ny** for at tildele en tilknyttet applikation til et miljø.</span><span class="sxs-lookup"><span data-stu-id="1598b-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="1598b-200">Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.</span><span class="sxs-lookup"><span data-stu-id="1598b-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="1598b-201">Vælg et servicemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="1598b-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="1598b-202">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="1598b-203">Konfigurer integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1598b-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="1598b-204">Aktivere funktionen til integration af tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="1598b-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="1598b-205">Log på din Finance eller Supply Chain Management-forekomst.</span><span class="sxs-lookup"><span data-stu-id="1598b-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="1598b-206">Gå til arbejdsområdet **Funktionsstyring**, og søg efter funktionen **Integration af tilføjelsesprogrammet til elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="1598b-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="1598b-207">Hvis denne funktion ikke vises på siden, skal du vælge **Kontroller, om der er opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="1598b-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="1598b-208">Vælg funktionen, og vælg derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="1598b-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="1598b-209">Konfigurere URL-adressen til tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="1598b-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="1598b-210">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="1598b-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1598b-211">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel, i feltet URL i feltet **Serviceslutpunkt URL** under fanen **Indsendelsestjeneste**.</span><span class="sxs-lookup"><span data-stu-id="1598b-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="1598b-212">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="1598b-212">Datacenter Azure geography</span></span> | <span data-ttu-id="1598b-213">URL for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="1598b-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="1598b-214">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-215">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="1598b-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-216">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="1598b-217">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="1598b-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="1598b-218">Angiv navnet på tilføjelsesprogrammet elektronisk faktureringsmiljøet i feltet **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="1598b-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="1598b-219">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="1598b-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
