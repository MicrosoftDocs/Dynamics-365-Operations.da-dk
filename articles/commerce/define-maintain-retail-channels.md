---
title: Definere og vedligeholde detailkanaler
description: Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes butikker i Dynamics 365 Commerce. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en butik.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410997"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="b9bc3-104">Definere og vedligeholde detailkanaler</span><span class="sxs-lookup"><span data-stu-id="b9bc3-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9bc3-105">Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes butikker i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b9bc3-106">Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en butik.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="b9bc3-107">Commerce understøtter flere detailkanaler, f.eks. onlinebutikker, callcentre og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="b9bc3-108">En fysisk butik kaldes en butik.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="b9bc3-109">Hver butik kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="b9bc3-110">Du skal oprette alle disse elementer for en butik, før du opretter den.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="b9bc3-111">Når du har oprettet butikken, kan du tildele de produkter, som skal føres i denne butik.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="b9bc3-112">Du skal også knytte medarbejdere, kasseapparater og kunder til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="b9bc3-113">Endelig kan føje den nye butik til et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="b9bc3-114">Konfigurere butikker</span><span class="sxs-lookup"><span data-stu-id="b9bc3-114">Setting up stores</span></span>

<span data-ttu-id="b9bc3-115">Før du kan konfigurere en butik i Commerce, skal du udføre nogle nødvendige opgaver.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="b9bc3-116">Du kan derefter oprette butikken og tilføje oplysninger.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b9bc3-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="b9bc3-117">Prerequisites</span></span>

<span data-ttu-id="b9bc3-118">Du skal fuldføre følgende opgaver, før du kan konfigurere en butik:</span><span class="sxs-lookup"><span data-stu-id="b9bc3-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="b9bc3-119">Konfigurer organisationsstrukturen, og opret organisationshierarkier for detailudvalg, genopfyldning og rapportering.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="b9bc3-120">Opret et lager, der repræsenterer butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="b9bc3-121">Definer nummerserier til butikker, butiksopgørelser og opgørelsesbilag.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="b9bc3-122">Konfigurer parametre for Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="b9bc3-123">Konfigurer betalingsmetoderne, som butikken accepterer.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="b9bc3-124">Hvis du vil behandle kreditkorttransaktioner på butikkens POS-kasseapparater, kan du også konfigurere betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="b9bc3-125">Konfigurer momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="b9bc3-126">konfigurer produkter.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-126">Set up products.</span></span> <span data-ttu-id="b9bc3-127">Som en del af denne opgave skal du oprette produkthierarkier, produktvarianter og produktudvalg.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="b9bc3-128">Konfigurer produktprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-128">Set up product price groups.</span></span>
10. <span data-ttu-id="b9bc3-129">Konfigurer produktpriser.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-129">Set up product pricing.</span></span> <span data-ttu-id="b9bc3-130">Som en del af denne opgave skal du også konfigurere prisjusteringer, rabatter og rabatperioder.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="b9bc3-131">Opsætning af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b9bc3-132">Du skal også tildele relevante tilladelser til arbejdstagerne, så de kan logge på og udføre opgaver ved hjælp af POS-systemet.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="b9bc3-133">Konfigurer de POS-profiler, som du vil tildele til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="b9bc3-134">Denne opgave omfatter mange andre opgaver, f.eks. opsætning af registre, konfiguration af offlineprofiler samt opsætning af kvitteringsformater og -profiler.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="b9bc3-135">Gennemse alle de opgaver, der er inkluderet i forudsætningerne, og udfør kun de opgaver, der gælder for dig.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="b9bc3-136">Opsætning af en butik</span><span class="sxs-lookup"><span data-stu-id="b9bc3-136">Set up a store</span></span>

<span data-ttu-id="b9bc3-137">Når du har fuldført de nødvendige opgaver, skal du udføre disse opgaver for at konfigurere oplysninger til butikken:</span><span class="sxs-lookup"><span data-stu-id="b9bc3-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="b9bc3-138">Opret en butik.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-138">Create a store.</span></span>
2. <span data-ttu-id="b9bc3-139">Knyt en momsgruppe til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="b9bc3-140">Tildel de accepterede betalingsmetoder til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="b9bc3-141">Føj oplysninger til produktbeskrivelserne for de produkter, du tilbyder i dine butikker.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="b9bc3-142">Du kan for eksempel tilføje RTF-tekst og billeder.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="b9bc3-143">Disse produktoplysninger vises i forskellige sammenhænge som på POS-kasseapparat eller på udskrevne etiketter.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="b9bc3-144">Føj butikken til det standardorganisationshierarki, der er tildelt med formålet **Detailudvalg**, **Detailgenopfyldning** eller **Detailrapportering**.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="b9bc3-145">Når du har oprettet en butik</span><span class="sxs-lookup"><span data-stu-id="b9bc3-145">After you set up a store</span></span>

<span data-ttu-id="b9bc3-146">Når du har angivet oplysningerne om butikken, skal du udføre disse opgaver for at sende de nye butiksdata til POS:</span><span class="sxs-lookup"><span data-stu-id="b9bc3-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="b9bc3-147">Konfigurer POS-kasseapparaterne til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="b9bc3-148">Tildel produktudvalg til butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="b9bc3-149">Du kan behandle udvalg for at oprette listen over produkter, der indgår i udvalget, og for at gøre produkterne tilgængelige i butikken.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="b9bc3-150">Send data som f.eks. nummerserier, hardwareprofiler og layout for POS-skærmen til POS-kasseapparaterne.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="b9bc3-151">Udgiv butikken for at sende lagringsdata til POS.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="b9bc3-152">Kør jobbene for at sende dataene til POS.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="b9bc3-153">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="b9bc3-153">Organization hierarchies</span></span>

<span data-ttu-id="b9bc3-154">Commerce bruger organisationshierarkier til at strukturere kanaler.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="b9bc3-155">Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="b9bc3-156">Når du opretter butikker, kan du føje dem til et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="b9bc3-157">Butikkerne deler derefter data, der bruges til udvalg, genbestilling og rapportering.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="b9bc3-158">Hvis du vil bruge funktionaliteten Commerce Sales, skal konfigurationsnøglen for **Flere leveringssteder** være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="b9bc3-159">Denne konfigurationsnøgle kan findes i **Konfigurationsnøgler til handel** under **Systemadministration**\> **Opsætning** \> **Licenskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="b9bc3-160">Dette er påkrævet på grund af forskellige valideringer, som er baseret på den leveringsadresse, der er konfigureret på salgsordrelinjeniveau.</span><span class="sxs-lookup"><span data-stu-id="b9bc3-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

