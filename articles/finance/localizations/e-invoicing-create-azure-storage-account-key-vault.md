---
title: Oprette en Azure Storage-konto og Key Vault
description: Dette emne forklarer, hvordan du kan oprette en Azure Storage-konto og Key Vault.
author: gionoder
ms.date: 02/12/2021
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
ms.openlocfilehash: b7df4933c1373893e00f48ea3a21bd5af40719a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840214"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="22d6c-103">Oprette en Azure Storage-konto og Key Vault</span><span class="sxs-lookup"><span data-stu-id="22d6c-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="22d6c-104">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="22d6c-104">Prerequisites</span></span>

<span data-ttu-id="22d6c-105">Før du kan fuldføre trinene i dette emne, skal du sørge for, at følgende opgaver er fuldført:</span><span class="sxs-lookup"><span data-stu-id="22d6c-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="22d6c-106">Opret en ny Key Vault-ressource i Azure.</span><span class="sxs-lookup"><span data-stu-id="22d6c-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="22d6c-107">Du kan finde flere oplysninger i [Om Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="22d6c-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="22d6c-108">Opret en Azure Storage-konto (Blob-lager).</span><span class="sxs-lookup"><span data-stu-id="22d6c-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="22d6c-109">Du kan finde flere oplysninger i [Vedligeholde en Azure Storage-konbo](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="22d6c-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="22d6c-110">Overblik</span><span class="sxs-lookup"><span data-stu-id="22d6c-110">Overview</span></span>

<span data-ttu-id="22d6c-111">I dette emne skal du fuldføre to hovedtrin:</span><span class="sxs-lookup"><span data-stu-id="22d6c-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="22d6c-112">Konfigurer Azure Storage-kontoen for at hente URI'en til lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="22d6c-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="22d6c-113">Konfigurer Key Vault'en til opbevaring af URI'en for lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="22d6c-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="22d6c-114">Konfigurere Azure Storage-kontoen for at hente URI'en til lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="22d6c-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="22d6c-115">Åbn den lagerkonto, du planlægger at bruge sammen med elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="22d6c-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="22d6c-116">Gå til **Blob service** \> **Containere**, og opret en ny container.</span><span class="sxs-lookup"><span data-stu-id="22d6c-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="22d6c-117">Angiv et navn til containeren, og angiv feltet **Offentlig adgangsniveau** til **Privat (ingen anonym adgang)**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="22d6c-118">Åbn containeren, og gå til **Indstillinger \> Adgangspolitik**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="22d6c-119">Vælg **Tilføj politik** for at tilføje en lagret adgangspolitik.</span><span class="sxs-lookup"><span data-stu-id="22d6c-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="22d6c-120">Angiv felterne **Identifikator** og **Rettigheder** efter behov.</span><span class="sxs-lookup"><span data-stu-id="22d6c-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="22d6c-121">Vælg alle rettigheder i feltet **Rettigheder**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Tildele tilladelse til Blob-lager](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="22d6c-123">Angiv start- og udløbsdatoerne.</span><span class="sxs-lookup"><span data-stu-id="22d6c-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="22d6c-124">Udløbsdatoen skal være i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="22d6c-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="22d6c-125">Vælg **OK** for at gemme politikken, og gem derefter ændringerne i containeren.</span><span class="sxs-lookup"><span data-stu-id="22d6c-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="22d6c-126">Vend tilbage til lagerkontoen, og åbn **Lagercenter (prøveversion)**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="22d6c-127">Højreklik på containeren, og vælg derefter **Hent delt adgangssignatur**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="22d6c-128">I dialogboksen **Delt adgangssignatur** skal du kopiere og gemme værdien i feltet **URI**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="22d6c-129">Denne værdi vil blive brugt i den næste procedure og vil blive henvist til som *URI for delt adgangssignatur*.</span><span class="sxs-lookup"><span data-stu-id="22d6c-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![Vælge og kopiere URI-værdien](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="22d6c-131">Konfigurere Key Vault'en til opbevaring af URI'en for lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="22d6c-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="22d6c-132">Åbn den Key Vault, du vil bruge sammen med elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="22d6c-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="22d6c-133">Gå til **Indstillinger** \> **Hemmeligheder**, og vælg derefter **Generer/importer** for at oprette en ny hemmelighed.</span><span class="sxs-lookup"><span data-stu-id="22d6c-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="22d6c-134">På siden **Opret en hemmelighed** skal du vælge **Manuel** i feltet **Uploadindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="22d6c-135">Angiv navnet på hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="22d6c-135">Enter the name of the secret.</span></span> <span data-ttu-id="22d6c-136">Dette navn bruges under konfigurationen af tjenesten i RCS (Regulatory Configuration Service) og vil blive henvist til som *det hemmelige Key Vault-navn*.</span><span class="sxs-lookup"><span data-stu-id="22d6c-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="22d6c-137">Vælg **URI for delt adgangssignatur** i feltet **Værdi**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="22d6c-138">Konfigurer adgangspolitikken for at tildele elektronisk fakturering det korrekte niveau for sikker adgang til den hemmelighed, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="22d6c-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="22d6c-139">Gå til **Indstillinger \> Adgangspolitik**, og vælg **Tilføj adgangspolitik**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="22d6c-140">Angiv de hemmelige tilladelser til handlingerne **Get** og **List**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Tildele tjenesteadgang](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="22d6c-142">Angiv certifikattilladelserne til handlingerne **Get** og **List**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Tildele certifikattilladelse](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="22d6c-144">Vælg **Ingen valgt** i feltet **Vælg sikkerhedskonto**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="22d6c-145">I dialogboksen **Sikkerhedskonto** skal du vælge sikkerhedskontoen ved at tilføje **e-faktureringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="22d6c-146">Vælg **Tilføj**, og vælg derefter **Gem Key Vault-ændringer**.</span><span class="sxs-lookup"><span data-stu-id="22d6c-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="22d6c-147">På siden **Oversigt** skal du kopiere værdien **DNS-navn** for Key Vault.</span><span class="sxs-lookup"><span data-stu-id="22d6c-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="22d6c-148">Denne værdi vil blive brugt under konfigurationen af tjenesten i RCS og vil blive henvist til som *URI for Key Vault*.</span><span class="sxs-lookup"><span data-stu-id="22d6c-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

