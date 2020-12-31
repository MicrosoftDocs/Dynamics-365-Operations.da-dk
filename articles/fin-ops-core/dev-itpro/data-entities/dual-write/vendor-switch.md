---
title: Skifte mellem kreditordesign
description: I dette emne beskrives det, hvordan du kan skifte integrationen af kreditordata mellem Finance and Operations-apps og Dataverse.
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
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685503"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="2e686-103">Skifte mellem kreditordesign</span><span class="sxs-lookup"><span data-stu-id="2e686-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="2e686-104">Kreditordataflow</span><span class="sxs-lookup"><span data-stu-id="2e686-104">Vendor data flow</span></span> 

<span data-ttu-id="2e686-105">Hvis du vælger at bruge enheden **Konto** til at gemme kreditorer af typen **Organisation** og enheden **Kontaktperson** til at gemme kreditorer af typen **Person**, skal du konfigurere følgende arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="2e686-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="2e686-106">Ellers kræves denne konfiguration ikke.</span><span class="sxs-lookup"><span data-stu-id="2e686-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="2e686-107">Bruge det udvidede kreditordesign til kreditorer af typen Organisation</span><span class="sxs-lookup"><span data-stu-id="2e686-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="2e686-108">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="2e686-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2e686-109">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="2e686-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2e686-110">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="2e686-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="2e686-111">Opret kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="2e686-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="2e686-112">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="2e686-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="2e686-113">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="2e686-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="2e686-114">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="2e686-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2e686-115">Opret en arbejdsgangsproces for enheden **Kreditor**, og vælg skabelonen **Opret kreditorer i tabellen Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="2e686-116">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e686-116">Then select **OK**.</span></span> <span data-ttu-id="2e686-117">Denne arbejdsgang håndterer leverandøroprettelsesscenariet for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="2e686-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Opret kreditorer i arbejdsgangprocessen for tabellen Konti](media/create_process.png)

2. <span data-ttu-id="2e686-119">Opret en arbejdsgangsproces for enheden **Kreditor**, og vælg skabelonen **Opdater kreditorer i tabellen Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="2e686-120">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e686-120">Then select **OK**.</span></span> <span data-ttu-id="2e686-121">Denne arbejdsgang håndterer opdateringsscenariet for leverandører for enheden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="2e686-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="2e686-122">Opret en arbejdsgangsproces for enheden **Konto**, og vælg skabelonen **Opret kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="2e686-123">Opret en arbejdsgangsproces for enheden **Konto**, og vælg skabelonen **Opdater kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="2e686-124">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="2e686-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2e686-125">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="2e686-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Konvertere til en baggrundsarbejdsgangsknap](media/background_workflow.png)

6. <span data-ttu-id="2e686-127">Aktiver de arbejdsgange, du har oprettet for tabellerne **Konto** og **Kreditor** for at påbegynde anvendelsen af enheden **Konto** til lagring af oplysninger til kreditorer af typen **Organisation**.</span><span class="sxs-lookup"><span data-stu-id="2e686-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="2e686-128">Bruge det udvidede kreditordesign til kreditorer af typen Person</span><span class="sxs-lookup"><span data-stu-id="2e686-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="2e686-129">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="2e686-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2e686-130">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="2e686-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2e686-131">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="2e686-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="2e686-132">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="2e686-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="2e686-133">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="2e686-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="2e686-134">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="2e686-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="2e686-135">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="2e686-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2e686-136">Opret en ny arbejdsgangsproces for enheden **Kreditor**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="2e686-137">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e686-137">Then select **OK**.</span></span> <span data-ttu-id="2e686-138">Denne arbejdsgang håndterer kreditoroprettelsesscenariet for enheden **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="2e686-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="2e686-139">Opret en ny arbejdsgangsproces for enheden **Kreditor**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="2e686-140">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e686-140">Then select **OK**.</span></span> <span data-ttu-id="2e686-141">Denne arbejdsgang håndterer opdateringsscenariet for kreditorer for enheden **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="2e686-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="2e686-142">Opret en ny arbejdsgangsproces for enheden **Kontaktperson**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="2e686-143">Opret en ny arbejdsgangsproces for enheden **Kontaktperson**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="2e686-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="2e686-144">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="2e686-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2e686-145">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="2e686-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="2e686-146">Aktiver de arbejdsgange, du har oprettet i tabellerne **Kontaktperson** og **Kreditor** for at påbegynde anvendelsen af enheden **Kontaktperson** til lagring af oplysninger til kreditorer af typen **Person**.</span><span class="sxs-lookup"><span data-stu-id="2e686-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
