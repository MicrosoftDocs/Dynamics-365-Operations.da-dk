---
title: Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration
description: Dette emne beskriver, hvordan du kommer i gang med tilføjelsesprogrammet til elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104358"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="f3399-103">Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration</span><span class="sxs-lookup"><span data-stu-id="f3399-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f3399-104">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="f3399-104">Prerequisites</span></span>

<span data-ttu-id="f3399-105">Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="f3399-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="f3399-106">Du skal have adgang til din Microsoft Dynamics Lifecycle Services-konto (LCS).</span><span class="sxs-lookup"><span data-stu-id="f3399-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="f3399-107">Du skal have et LCS-projekt, der omfatter version 10.0.13 eller en senere version af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f3399-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f3399-108">Derudover skal disse apps implementeres i en af følgende Azure-geografisk områder:</span><span class="sxs-lookup"><span data-stu-id="f3399-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="f3399-109">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-109">East US</span></span>
    - <span data-ttu-id="f3399-110">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-110">West US</span></span>
    - <span data-ttu-id="f3399-111">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-111">North EU</span></span>
    - <span data-ttu-id="f3399-112">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-112">West EU</span></span>

- <span data-ttu-id="f3399-113">Du skal have adgang til din Dynamics 365 Regulatory Configuration Services (RCS-konto).</span><span class="sxs-lookup"><span data-stu-id="f3399-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="f3399-114">Du skal aktivere globaliseringsfunktionen for din RCS-konto i modulet Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="f3399-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="f3399-115">Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="f3399-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="f3399-116">Du skal oprette en Key Vault og en lagerkonto i Azure.</span><span class="sxs-lookup"><span data-stu-id="f3399-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="f3399-117">Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="f3399-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="f3399-118">Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f3399-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="f3399-119">Log på din LCS-konto.</span><span class="sxs-lookup"><span data-stu-id="f3399-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="f3399-120">Vælg feltet **Prøveversion af funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="f3399-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="f3399-121">I afsnittet **Funktioner til offentlig visning** skal du vælge en **e-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="f3399-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="f3399-122">Kontroller, at indstillingen **Prøveversion af funktion aktiveret** er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f3399-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="f3399-123">Konfigurer parametre for RCS-integration med tilføjelsesprogrammet til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="f3399-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="f3399-124">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="f3399-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f3399-125">Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.</span><span class="sxs-lookup"><span data-stu-id="f3399-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f3399-126">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URI i feltet **Serviceslutpunkt URI** under fanen **e-faktureringsservice**.</span><span class="sxs-lookup"><span data-stu-id="f3399-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="f3399-127">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="f3399-127">Datacenter Azure geography</span></span> | <span data-ttu-id="f3399-128">URI for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="f3399-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="f3399-129">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-130">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-131">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-132">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="f3399-133">Kontrollér, at **Applikations-id** er angivet til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="f3399-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="f3399-134">Denne værdi er en fast værdi.</span><span class="sxs-lookup"><span data-stu-id="f3399-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="f3399-135">Angiv id'et for din LCS-abonnementskonto i feltet **LCS-miljø-id**.</span><span class="sxs-lookup"><span data-stu-id="f3399-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="f3399-136">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="f3399-137">Oprette Key Vault-hemmelighed</span><span class="sxs-lookup"><span data-stu-id="f3399-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="f3399-138">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="f3399-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f3399-139">I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="f3399-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="f3399-140">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.</span><span class="sxs-lookup"><span data-stu-id="f3399-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="f3399-141">Vælg **Ny** for at oprette en key vault-hemmelighed.</span><span class="sxs-lookup"><span data-stu-id="f3399-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="f3399-142">Angiv navnet på key vault-hemmeligheden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3399-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="f3399-143">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3399-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="f3399-144">Indsæt hemmeligheden fra Azure Key Vault i feltet **Key Vault URI**.</span><span class="sxs-lookup"><span data-stu-id="f3399-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="f3399-145">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f3399-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="f3399-146">Oprette hemmelig lagerkonto</span><span class="sxs-lookup"><span data-stu-id="f3399-146">Create Storage account secret</span></span>

1. <span data-ttu-id="f3399-147">Vælg **Tilføj** i afsnittet **Certifikater** på siden **Nøgleparametre**.</span><span class="sxs-lookup"><span data-stu-id="f3399-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="f3399-148">Angiv det samme for lagerkontohemmeligheden i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3399-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="f3399-149">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3399-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="f3399-150">I **Type**-feltet skal du vælge **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="f3399-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="f3399-151">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="f3399-152">Opret et miljø for tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="f3399-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="f3399-153">Log på din RCS-konto.</span><span class="sxs-lookup"><span data-stu-id="f3399-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="f3399-154">I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="f3399-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="f3399-155">Opret et servicemiljø</span><span class="sxs-lookup"><span data-stu-id="f3399-155">Create a service environment</span></span>

1. <span data-ttu-id="f3399-156">På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3399-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="f3399-157">Vælg **Ny** for at oprette et nyt servicemiljø.</span><span class="sxs-lookup"><span data-stu-id="f3399-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="f3399-158">Angiv navnet på e-faktureringsmiljøet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3399-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="f3399-159">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3399-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="f3399-160">Vælg navnet på det certifikat, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.</span><span class="sxs-lookup"><span data-stu-id="f3399-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="f3399-161">I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet, og også oprette forbindelse til lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="f3399-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="f3399-162">Angiv **Bruger-id** i feltet for brugerens alias.</span><span class="sxs-lookup"><span data-stu-id="f3399-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="f3399-163">I feltet **E-mail** skal du angive brugerens e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="f3399-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="f3399-164">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f3399-164">Select **Save**.</span></span>
8. <span data-ttu-id="f3399-165">Hvis dine lande-/områdespecifikke fakturaer kræver en kæde af certifikater for at anvende en digital signaturer, skal du vælge **Key Vault-parametre** i handlingsruden og derefter vælge **Kæde af certifikater** og følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f3399-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="f3399-166">Vælg **Ny** for at oprette en kæde af certifikater.</span><span class="sxs-lookup"><span data-stu-id="f3399-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="f3399-167">Angiv navnet på kæden af certifikater i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3399-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="f3399-168">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3399-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="f3399-169">I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.</span><span class="sxs-lookup"><span data-stu-id="f3399-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="f3399-170">Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden.</span><span class="sxs-lookup"><span data-stu-id="f3399-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="f3399-171">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="f3399-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-172">Close the page.</span></span>
9. <span data-ttu-id="f3399-173">Vælg **Udgiv** i handlingsruden for at publicere miljøet til skyen på siden **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="f3399-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="f3399-174">Værdien i feltet **Status** ændres til **Publiceret**.</span><span class="sxs-lookup"><span data-stu-id="f3399-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="f3399-175">Opret en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="f3399-175">Create a connected application</span></span>

1. <span data-ttu-id="f3399-176">På siden **Miljøopsætninger** skal du vælge **Tilsluttede applikationer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f3399-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="f3399-177">Vælg **Ny** for at oprette en tilsluttet applikation.</span><span class="sxs-lookup"><span data-stu-id="f3399-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="f3399-178">Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="f3399-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="f3399-179">I feltet **Applikation** skal du angive URL-adressen til det finans- og Supply Chain Management-miljø, der skal oprettes forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="f3399-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="f3399-180">I feltet **Lejer** skal du angive den lejer til finans- og Supply Chain Management-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f3399-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="f3399-181">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f3399-181">Select **Save**.</span></span>
6. <span data-ttu-id="f3399-182">Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet.</span><span class="sxs-lookup"><span data-stu-id="f3399-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="f3399-183">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="f3399-184">Sammenkæd tilknyttede applikationer med miljøer</span><span class="sxs-lookup"><span data-stu-id="f3399-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="f3399-185">På siden **Miljøopsætninger** skal du vælge **Ny** for at tildele en tilknyttet applikation til et miljø.</span><span class="sxs-lookup"><span data-stu-id="f3399-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="f3399-186">Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.</span><span class="sxs-lookup"><span data-stu-id="f3399-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="f3399-187">Vælg et servicemiljø i feltet **Servicemiljø**.</span><span class="sxs-lookup"><span data-stu-id="f3399-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="f3399-188">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="f3399-189">Konfigurer integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f3399-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="f3399-190">Aktivere funktionen til integration af tilføjelsesprogrammet til elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="f3399-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="f3399-191">Log på din Finance eller Supply Chain Management-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f3399-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="f3399-192">Gå til arbejdsområdet **Funktionsstyring**, og søg efter funktionen **Integration af tilføjelsesprogrammet til elektronisk fakturering**.</span><span class="sxs-lookup"><span data-stu-id="f3399-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="f3399-193">Hvis denne funktion ikke vises på siden, skal du vælge **Kontroller, om der er opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="f3399-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="f3399-194">Vælg funktionen, og vælg derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="f3399-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="f3399-195">Konfigurere URL-adressen til tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="f3399-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="f3399-196">Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="f3399-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="f3399-197">Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel, i feltet URL i feltet **Serviceslutpunkt URL** under fanen **Indsendelsestjeneste**.</span><span class="sxs-lookup"><span data-stu-id="f3399-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="f3399-198">Datacenter Azure-geografisk område</span><span class="sxs-lookup"><span data-stu-id="f3399-198">Datacenter Azure geography</span></span> | <span data-ttu-id="f3399-199">URL for tjenesteslutpunkt</span><span class="sxs-lookup"><span data-stu-id="f3399-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="f3399-200">Det østlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-201">Det vestlige USA</span><span class="sxs-lookup"><span data-stu-id="f3399-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-202">Det nordlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="f3399-203">Det vestlige Europa</span><span class="sxs-lookup"><span data-stu-id="f3399-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="f3399-204">Angiv navnet på tilføjelsesprogrammet elektronisk faktureringsmiljøet i feltet **Miljø**.</span><span class="sxs-lookup"><span data-stu-id="f3399-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="f3399-205">Vælg **Gem**, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="f3399-205">Select **Save**, and then close the page.</span></span>
