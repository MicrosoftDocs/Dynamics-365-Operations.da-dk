---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte integrationen af kreditordata mellem Finance and Operations-apps og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997546"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="04d01-103">Skifte mellem kreditordesign</span><span class="sxs-lookup"><span data-stu-id="04d01-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="04d01-104">Kreditordataflow</span><span class="sxs-lookup"><span data-stu-id="04d01-104">Vendor data flow</span></span> 

<span data-ttu-id="04d01-105">Hvis du vælger at bruge enheden **Konto** til at gemme kreditorer af typen **Organisation** og enheden **Kontaktperson** til at gemme kreditorer af typen **Person** , skal du konfigurere følgende arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="04d01-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="04d01-106">Ellers kræves denne konfiguration ikke.</span><span class="sxs-lookup"><span data-stu-id="04d01-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="04d01-107">Bruge det udvidede kreditordesign til kreditorer af typen Organisation</span><span class="sxs-lookup"><span data-stu-id="04d01-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="04d01-108">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="04d01-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="04d01-109">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="04d01-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="04d01-110">Opret kreditorer i enheden Konti</span><span class="sxs-lookup"><span data-stu-id="04d01-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="04d01-111">Opret kreditorer i enheden Kreditorer</span><span class="sxs-lookup"><span data-stu-id="04d01-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="04d01-112">Opdater kreditorer i enheden Konti</span><span class="sxs-lookup"><span data-stu-id="04d01-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="04d01-113">Opdater kreditorer i enheden Kreditorer</span><span class="sxs-lookup"><span data-stu-id="04d01-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="04d01-114">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="04d01-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="04d01-115">Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opret kreditorer i enheden Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="04d01-116">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="04d01-116">Then select **OK**.</span></span> <span data-ttu-id="04d01-117">Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="04d01-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Oprette kreditorer i arbejdsgangprocessen for enheden Konti](media/create_process.png)

2. <span data-ttu-id="04d01-119">Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opdater kreditorer i enheden Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="04d01-120">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="04d01-120">Then select **OK**.</span></span> <span data-ttu-id="04d01-121">Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="04d01-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="04d01-122">Opret en ny arbejdsgangsproces for enheden **Konto** , og vælg skabelonen **Opret kreditorer i enheden Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="04d01-123">Opret en ny arbejdsgangsproces for enheden **Konto** , og vælg skabelonen **Opdater kreditorer i enheden Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="04d01-124">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="04d01-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="04d01-125">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="04d01-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Konvertere til en baggrundsarbejdsgangsknap](media/background_workflow.png)

6. <span data-ttu-id="04d01-127">Aktiver de arbejdsgange, du har oprettet for enhederne **Konto** og **Kreditor** for at påbegynde anvendelsen af enheden **Konto** til lagring af oplysninger til kreditorer af typen **Organisation**.</span><span class="sxs-lookup"><span data-stu-id="04d01-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="04d01-128">Bruge det udvidede kreditordesign til kreditorer af typen Person</span><span class="sxs-lookup"><span data-stu-id="04d01-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="04d01-129">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="04d01-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="04d01-130">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="04d01-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="04d01-131">Oprette kreditorer af typen Person i enheden Kreditorer</span><span class="sxs-lookup"><span data-stu-id="04d01-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="04d01-132">Oprette kreditorer af typen Person i enheden Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="04d01-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="04d01-133">Opdatere kreditorer af typen Person i enheden Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="04d01-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="04d01-134">Opdatere kreditorer af typen Person i enheden Kreditorer</span><span class="sxs-lookup"><span data-stu-id="04d01-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="04d01-135">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="04d01-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="04d01-136">Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opret kreditorer af typen Person i enheden Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="04d01-137">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="04d01-137">Then select **OK**.</span></span> <span data-ttu-id="04d01-138">Denne arbejdsgang håndterer kreditoroprettelsesscenariet for enheden **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="04d01-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="04d01-139">Opret en ny arbejdsgangsproces for enheden **Kreditor** , og vælg skabelonen **Opdater kreditorer af typen Person i enheden Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="04d01-140">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="04d01-140">Then select **OK**.</span></span> <span data-ttu-id="04d01-141">Denne arbejdsgang håndterer opdateringsscenariet for kreditorer for enheden **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="04d01-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="04d01-142">Opret en ny arbejdsgangsproces for enheden **Kontaktperson** , og vælg skabelonen **Opret kreditorer af typen Person i enheden Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="04d01-143">Opret en ny arbejdsgangsproces for enheden **Kontaktperson** , og vælg skabelonen **Opdater kreditorer af typen Person i enheden Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="04d01-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="04d01-144">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="04d01-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="04d01-145">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="04d01-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="04d01-146">Aktiver de arbejdsgange, du har oprettet i enhederne **Kontaktperson** og **Kreditor** for at påbegynde anvendelsen af enheden **Kontaktperson** til lagring af oplysninger til kreditorer af typen **Person**.</span><span class="sxs-lookup"><span data-stu-id="04d01-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
