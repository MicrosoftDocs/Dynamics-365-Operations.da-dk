---
title: Start her med serviceadministration i elektronisk fakturering
description: Dette emne beskriver, hvordan du kommer i gang med elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840142"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="7a370-103">Start her med serviceadministration i elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7a370-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7a370-104">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="7a370-104">Prerequisites</span></span>

<span data-ttu-id="7a370-105">Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="7a370-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="7a370-106">Du skal have adgang til din Microsoft Dynamics Lifecycle Services-konto (LCS).</span><span class="sxs-lookup"><span data-stu-id="7a370-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="7a370-107">Du skal have et LCS-projekt, der omfatter version 10.0.17 eller en senere version af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7a370-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7a370-108">Derudover skal disse apps implementeres i en af følgende Azure-geografisk områder:</span><span class="sxs-lookup"><span data-stu-id="7a370-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="7a370-109">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-109">East US</span></span>
    - <span data-ttu-id="7a370-110">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-110">West US</span></span>
    - <span data-ttu-id="7a370-111">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-111">North EU</span></span>
    - <span data-ttu-id="7a370-112">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-112">West EU</span></span>

- <span data-ttu-id="7a370-113">Du skal have adgang til din Dynamics 365 Regulatory Configuration Services (RCS-konto).</span><span class="sxs-lookup"><span data-stu-id="7a370-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="7a370-114">Du skal aktivere globaliseringsfunktionen for din RCS-konto i modulet Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="7a370-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="7a370-115">Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="7a370-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="7a370-116">Du skal oprette en Key Vault og en lagerkonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="7a370-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="7a370-117">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7a370-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="7a370-118">Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7a370-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="7a370-119">Log på din LCS-konto.</span><span class="sxs-lookup"><span data-stu-id="7a370-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="7a370-120">Vælg feltet **Prøveversion af funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="7a370-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="7a370-121">I afsnittet **Funktioner til offentlig visning** skal du vælge en **e-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="7a370-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="7a370-122">Kontroller, at indstillingen **Prøveversion af funktion aktiveret** er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7a370-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="7a370-123">Vælg dit LCS-implementeringsprojekt på LCS-dashboardet.</span><span class="sxs-lookup"><span data-stu-id="7a370-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="7a370-124">LCS-projektet skal køre.</span><span class="sxs-lookup"><span data-stu-id="7a370-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="7a370-125">Vælg **Installér et nyt tilføjelsesprogram** på fanen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="7a370-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="7a370-126">Vælg **e-faktureringstjenester**.</span><span class="sxs-lookup"><span data-stu-id="7a370-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="7a370-127">Angiv i feltet **AAD-program-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="7a370-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="7a370-128">Denne værdi er en fast værdi.</span><span class="sxs-lookup"><span data-stu-id="7a370-128">This is a fixed value.</span></span>
10. <span data-ttu-id="7a370-129">Angiv lejer-id for din Azure-abonnementskonto i feltet **AAD-lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="7a370-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="7a370-130">Gennemse vilkår og betingelser, og marker afkrydsningsfeltet.</span><span class="sxs-lookup"><span data-stu-id="7a370-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="7a370-131">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="7a370-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="7a370-132">Konfigurere parametre for RCS-integration med elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7a370-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="7a370-133">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="7a370-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7a370-134">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="7a370-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="7a370-135">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URI i feltet **Serviceslutpunkt URI** under fanen **e-faktureringsservice**.</span><span class="sxs-lookup"><span data-stu-id="7a370-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="7a370-136">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="7a370-136">Datacenter Azure geography</span></span> | <span data-ttu-id="7a370-137">URI for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="7a370-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7a370-138">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-139">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-140">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-141">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="7a370-142">Kontrollér, at **Applikations-id** er angivet til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="7a370-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="7a370-143">Denne værdi er en fast værdi.</span><span class="sxs-lookup"><span data-stu-id="7a370-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="7a370-144">Angiv id'et for dit LCS-abonnementsmiljø i feltet **LCS-miljø-id**.</span><span class="sxs-lookup"><span data-stu-id="7a370-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="7a370-145">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="7a370-146">Oprette Key Vault-referencer</span><span class="sxs-lookup"><span data-stu-id="7a370-146">Create Key Vault references</span></span>

1. <span data-ttu-id="7a370-147">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="7a370-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7a370-148">I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="7a370-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="7a370-149">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.</span><span class="sxs-lookup"><span data-stu-id="7a370-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="7a370-150">Vælg **Ny** for at oprette en Key Vault-reference.</span><span class="sxs-lookup"><span data-stu-id="7a370-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="7a370-151">Angiv navnet på key vault-referencen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="7a370-152">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7a370-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7a370-153">Indsæt Key Vault-hemmeligheden fra Azure Key Vault i feltet **Key Vault URI**.</span><span class="sxs-lookup"><span data-stu-id="7a370-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="7a370-154">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7a370-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="7a370-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7a370-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="7a370-156">Oprette hemmelig lagerkonto</span><span class="sxs-lookup"><span data-stu-id="7a370-156">Create Storage account secret</span></span>

1. <span data-ttu-id="7a370-157">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** > **Key Vault-parametre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7a370-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="7a370-158">Vælg en **Key Vault-reference**, og vælg **Tilføj** i sektionen **Certifikater**.</span><span class="sxs-lookup"><span data-stu-id="7a370-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="7a370-159">Angiv navnet på lagerkontohemmeligheden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="7a370-160">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7a370-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="7a370-161">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7a370-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="7a370-162">I feltet **Type** skal du vælge **Hemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="7a370-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="7a370-163">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="7a370-164">Oprette en digital certifikathemmelighed</span><span class="sxs-lookup"><span data-stu-id="7a370-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="7a370-165">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.</span><span class="sxs-lookup"><span data-stu-id="7a370-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="7a370-166">Vælg en **Key Vault-reference**, og vælg derefter **Tilføj** i sektionen **Certifikater**.</span><span class="sxs-lookup"><span data-stu-id="7a370-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="7a370-167">Angiv navnet på den digitale certifikathemmelighed i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="7a370-168">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7a370-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="7a370-169">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7a370-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="7a370-170">I **Type**-feltet skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="7a370-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="7a370-171">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="7a370-172">Opret et servicemiljø</span><span class="sxs-lookup"><span data-stu-id="7a370-172">Create a service environment</span></span>

1. <span data-ttu-id="7a370-173">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="7a370-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7a370-174">I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="7a370-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="7a370-175">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7a370-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="7a370-176">Vælg **Ny** for at oprette et nyt servicemiljø.</span><span class="sxs-lookup"><span data-stu-id="7a370-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="7a370-177">Angiv navnet på e-faktureringsmiljøet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="7a370-178">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7a370-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7a370-179">Vælg navnet på den hemmelige lagerkonto, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.</span><span class="sxs-lookup"><span data-stu-id="7a370-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="7a370-180">I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet, og også oprette forbindelse til lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="7a370-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="7a370-181">Angiv **Bruger-id** i feltet for brugerens alias.</span><span class="sxs-lookup"><span data-stu-id="7a370-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="7a370-182">I feltet **E-mail** skal du angive brugerens e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="7a370-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="7a370-183">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7a370-183">Select **Save**.</span></span>
10. <span data-ttu-id="7a370-184">Hvis dine lande-/områdespecifikke fakturaer kræver en kæde af certifikater for at anvende en digital signaturer, skal du vælge **Key Vault-parametre** i handlingsruden og derefter vælge **Kæde af certifikater** og følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="7a370-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="7a370-185">Vælg **Ny** for at oprette en kæde af certifikater.</span><span class="sxs-lookup"><span data-stu-id="7a370-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="7a370-186">Angiv navnet på kæden af certifikater i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="7a370-187">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="7a370-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="7a370-188">I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.</span><span class="sxs-lookup"><span data-stu-id="7a370-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="7a370-189">Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden.</span><span class="sxs-lookup"><span data-stu-id="7a370-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="7a370-190">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="7a370-191">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-191">Close the page.</span></span>
11. <span data-ttu-id="7a370-192">Vælg **Udgiv** i handlingsruden for at publicere miljøet til skyen på siden **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="7a370-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="7a370-193">Værdien i feltet **Status** ændres til **Publiceret**.</span><span class="sxs-lookup"><span data-stu-id="7a370-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="7a370-194">Opret en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="7a370-194">Create a connected application</span></span>

1. <span data-ttu-id="7a370-195">På siden **Miljøopsætninger** skal du vælge **Tilsluttede applikationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7a370-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="7a370-196">Vælg **Ny** for at oprette en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="7a370-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="7a370-197">Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7a370-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="7a370-198">I feltet **Applikation** skal du angive URL-adressen til det finans- og Supply Chain Management-miljø, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="7a370-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="7a370-199">I feltet **Lejer** skal du angive den lejer til finans- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="7a370-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="7a370-200">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7a370-200">Select **Save**.</span></span>
6. <span data-ttu-id="7a370-201">Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="7a370-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="7a370-202">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="7a370-203">Sammenkæd tilknyttede applikationer med miljøer</span><span class="sxs-lookup"><span data-stu-id="7a370-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="7a370-204">På siden **Miljøopsætninger** skal du vælge **Ny** for at tildele en tilknyttet applikation til et miljø.</span><span class="sxs-lookup"><span data-stu-id="7a370-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="7a370-205">Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.</span><span class="sxs-lookup"><span data-stu-id="7a370-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="7a370-206">Vælg et servicemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="7a370-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="7a370-207">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="7a370-208">Konfigurere integrationen af elektronisk fakturering i Finance eller Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7a370-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="7a370-209">Aktivere funktionen til integration af elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="7a370-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="7a370-210">Log på din Finance eller Supply Chain Management-forekomst.</span><span class="sxs-lookup"><span data-stu-id="7a370-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="7a370-211">Gå til arbejdsområdet **Funktionsstyring**, og søg efter funktionen **Integration af elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="7a370-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="7a370-212">Hvis denne funktion ikke vises på siden, skal du vælge **Kontroller, om der er opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="7a370-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="7a370-213">Vælg funktionen, og vælg derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="7a370-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="7a370-214">Konfigurere URL-adressen til tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="7a370-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="7a370-215">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="7a370-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="7a370-216">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel, i feltet URL i feltet **Serviceslutpunkt URL** under fanen **Indsendelsestjeneste**.</span><span class="sxs-lookup"><span data-stu-id="7a370-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="7a370-217">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="7a370-217">Datacenter Azure geography</span></span> | <span data-ttu-id="7a370-218">URL for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="7a370-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7a370-219">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-220">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="7a370-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-221">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7a370-222">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="7a370-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="7a370-223">Angiv navnet på det servicemiljø, der er publiceret i elektronisk fakturering, i feltet **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="7a370-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="7a370-224">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="7a370-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="7a370-225">Aktivere flighting-nøgler</span><span class="sxs-lookup"><span data-stu-id="7a370-225">Enable Flighting keys</span></span>

<span data-ttu-id="7a370-226">Aktiver flighting-nøgler til Microsoft Dynamics 365 Finance eller Microsoft Dynamics 365 Supply Chain Management version 10.0.17 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="7a370-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="7a370-227">Kør følgende SQL-kommando:</span><span class="sxs-lookup"><span data-stu-id="7a370-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="7a370-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="7a370-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="7a370-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="7a370-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="7a370-230">Udfør en IISreset-kommando for alle AOS'er.</span><span class="sxs-lookup"><span data-stu-id="7a370-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
