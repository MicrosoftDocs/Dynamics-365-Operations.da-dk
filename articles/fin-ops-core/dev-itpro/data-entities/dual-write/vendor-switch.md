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
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744459"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="8d708-103">Skifte mellem kreditordesign</span><span class="sxs-lookup"><span data-stu-id="8d708-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="8d708-104">Kreditordataflow</span><span class="sxs-lookup"><span data-stu-id="8d708-104">Vendor data flow</span></span> 

<span data-ttu-id="8d708-105">Hvis du vælger at bruge tabellen **Konto** til at gemme kreditorer af typen **Organisation** og tabellen **Kontaktperson** til at gemme kreditorer af typen **Person**, skal du konfigurere følgende arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="8d708-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="8d708-106">Ellers kræves denne konfiguration ikke.</span><span class="sxs-lookup"><span data-stu-id="8d708-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="8d708-107">Bruge det udvidede kreditordesign til kreditorer af typen Organisation</span><span class="sxs-lookup"><span data-stu-id="8d708-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="8d708-108">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="8d708-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="8d708-109">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="8d708-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="8d708-110">Opret kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="8d708-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="8d708-111">Opret kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="8d708-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="8d708-112">Opdater kreditorer i tabellen Konti</span><span class="sxs-lookup"><span data-stu-id="8d708-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="8d708-113">Opdater kreditorer i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="8d708-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="8d708-114">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="8d708-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="8d708-115">Opret en arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opret kreditorer i tabellen Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="8d708-116">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d708-116">Then select **OK**.</span></span> <span data-ttu-id="8d708-117">Denne arbejdsgang håndterer leverandøroprettelsesscenariet for tabellen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="8d708-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Opret kreditorer i arbejdsgangprocessen for tabellen Konti](media/create_process.png)

2. <span data-ttu-id="8d708-119">Opret en arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opdater kreditorer i tabellen Konti** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="8d708-120">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d708-120">Then select **OK**.</span></span> <span data-ttu-id="8d708-121">Denne arbejdsgang håndterer opdateringsscenariet for leverandører for tabellen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="8d708-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="8d708-122">Opret en arbejdsgangsproces for tabellen **Konto**, og vælg skabelonen **Opret kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="8d708-123">Opret en arbejdsgangsproces for tabellen **Konto**, og vælg skabelonen **Opdater kreditorer i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="8d708-124">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="8d708-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="8d708-125">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="8d708-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Konvertere til en baggrundsarbejdsgangsknap](media/background_workflow.png)

6. <span data-ttu-id="8d708-127">Aktiver de arbejdsgange, du har oprettet for tabellerne **Konto** og **Kreditor** for at påbegynde anvendelsen af tabellen **Konto** til lagring af oplysninger til kreditorer af typen **Organisation**.</span><span class="sxs-lookup"><span data-stu-id="8d708-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="8d708-128">Bruge det udvidede kreditordesign til kreditorer af typen Person</span><span class="sxs-lookup"><span data-stu-id="8d708-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="8d708-129">Løsnings pakken **Dynamics365FinanceExtended** indeholder følgende arbejdsgangsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="8d708-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="8d708-130">Du skal oprette en arbejdsgang for hver skabelon.</span><span class="sxs-lookup"><span data-stu-id="8d708-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="8d708-131">Opret kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="8d708-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="8d708-132">Opret kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d708-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="8d708-133">Opdater kreditorer af typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="8d708-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="8d708-134">Opdater kreditorer af typen Person i tabellen Kreditorer</span><span class="sxs-lookup"><span data-stu-id="8d708-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="8d708-135">Følg disse trin for at oprette nye arbejdsgangsprocesser ved hjælp af arbejdsgangsprocesskabeloner:</span><span class="sxs-lookup"><span data-stu-id="8d708-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="8d708-136">Opret en ny arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="8d708-137">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d708-137">Then select **OK**.</span></span> <span data-ttu-id="8d708-138">Denne arbejdsgang håndterer kreditoroprettelsesscenariet for tabellen **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="8d708-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="8d708-139">Opret en ny arbejdsgangsproces for tabellen **Kreditor**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kontaktpersoner** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="8d708-140">Vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d708-140">Then select **OK**.</span></span> <span data-ttu-id="8d708-141">Denne arbejdsgang håndterer opdateringsscenariet for kreditorer for tabellen **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="8d708-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="8d708-142">Opret en ny arbejdsgangsproces for tabellen **Kontaktperson**, og vælg skabelonen **Opret kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="8d708-143">Opret en ny arbejdsgangsproces for tabellen **Kontaktperson**, og vælg skabelonen **Opdater kreditorer af typen Person i tabellen Kreditorer** for arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8d708-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="8d708-144">Du kan konfigurere arbejdsprocesser som enten realtids- eller baggrundsarbejdsgange, afhængigt af dine krav.</span><span class="sxs-lookup"><span data-stu-id="8d708-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="8d708-145">Hvis du vil konfigurere en arbejdsgang som en baggrundsarbejdsgang, skal du vælge **Konverter til en baggrundsarbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="8d708-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="8d708-146">Aktiver de arbejdsgange, du har oprettet i tabellerne **Kontaktperson** og **Kreditor** for at påbegynde anvendelsen af tabellen **Kontaktperson** til lagring af oplysninger til kreditorer af typen **Person**.</span><span class="sxs-lookup"><span data-stu-id="8d708-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
