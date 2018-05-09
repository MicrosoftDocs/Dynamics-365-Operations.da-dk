---
title: Definere og vedligeholde detailkanaler
description: "Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes detailbutikker i Microsoft Dynamics 365 for Retail. Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en detailbutik."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 321673a4294e705587bbd5c1afcaab67de50bad5
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="1f9f4-104">Definere og vedligeholde detailkanaler</span><span class="sxs-lookup"><span data-stu-id="1f9f4-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f9f4-105">Dette emne indeholder en oversigt over processen for opsætning af fysiske butikker, som kaldes detailbutikker i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1f9f4-106">Den indeholder oplysninger om de opgaver, du skal udføre, både før og efter du har oprettet en detailbutik.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="1f9f4-107">Dynamics 365 for Retail understøtter flere detailkanaler, f.eks. onlinebutikker, callcentre og fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="1f9f4-108">En fysisk butik kaldes en detailbutik.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="1f9f4-109">Hver detailbutik kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="1f9f4-110">Du skal oprette alle disse elementer for en detailbutik, før du opretter den.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="1f9f4-111">Når du har oprettet detailbutikken, kan du tildele de produkter, som skal føres i denne butik.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="1f9f4-112">Du skal også knytte medarbejdere, kasseapparater og kunder til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="1f9f4-113">Endelig kan føje den nye butik til et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="1f9f4-114">Konfigurere detailbutikker</span><span class="sxs-lookup"><span data-stu-id="1f9f4-114">Setting up retail stores</span></span>
<span data-ttu-id="1f9f4-115">Før du kan konfigurere en detailbutik i Dynamics 365 for Retail, skal du udføre nogle nødvendige opgaver.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="1f9f4-116">Du kan derefter oprette detailbutikken og tilføje oplysninger.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1f9f4-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="1f9f4-117">Prerequisites</span></span>

<span data-ttu-id="1f9f4-118">Du skal fuldføre følgende opgaver, før du kan konfigurere en detailbutik:</span><span class="sxs-lookup"><span data-stu-id="1f9f4-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="1f9f4-119">Konfigurer organisationsstrukturen, og opret organisationshierarkier for detailudvalg, genopfyldning og rapportering.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="1f9f4-120">Opret et lager, der repræsenterer detailbutikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="1f9f4-121">Definer nummerserier til detailbutikker, butiksopgørelser og opgørelsesbilag.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="1f9f4-122">Konfigurer parametre til detail.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="1f9f4-123">Konfigurer betalingsmetoderne, som butikken accepterer.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="1f9f4-124">Hvis du vil behandle kreditkorttransaktioner på butikkens POS-kasseapparater, kan du også konfigurere betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="1f9f4-125">Konfigurer momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="1f9f4-126">Konfigurer detailprodukter.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-126">Set up retail products.</span></span> <span data-ttu-id="1f9f4-127">Som en del af denne opgave skal du oprette detailprodukthierarkier, produktvarianter og produktudvalg.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="1f9f4-128">Konfigurer produktprisgrupper.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-128">Set up product price groups.</span></span>
10. <span data-ttu-id="1f9f4-129">Konfigurer detailproduktpriser.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-129">Set up retail product pricing.</span></span> <span data-ttu-id="1f9f4-130">Som en del af denne opgave skal du også konfigurere prisjusteringer, rabatter og rabatperioder.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="1f9f4-131">Opsætning af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-131">Set up staff members.</span></span> <span data-ttu-id="1f9f4-132">**Bemærk!** Du skal også tildele relevante tilladelser til arbejdstagerne, så de kan logge på og udføre opgaver ved hjælp af Dynamics 365 for Retail POS-systemet.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="1f9f4-133">Konfigurer de Retail POS-profiler, som du vil tildele til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="1f9f4-134">Denne opgave omfatter mange andre opgaver, f.eks. opsætning af registre, konfiguration af offlineprofiler samt opsætning af kvitteringsformater og -profiler.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="1f9f4-135">Gennemse alle de opgaver, der er inkluderet i forudsætningen, og udfør kun de opgaver, der gælder for dig.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="1f9f4-136">Konfigurere en detailbutik</span><span class="sxs-lookup"><span data-stu-id="1f9f4-136">Set up a retail store</span></span>

<span data-ttu-id="1f9f4-137">Når du har fuldført de nødvendige opgaver, skal du udføre disse opgaver for at konfigurere oplysninger til detailbutikken:</span><span class="sxs-lookup"><span data-stu-id="1f9f4-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="1f9f4-138">Opret en detailbutik.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-138">Create a retail store.</span></span>
2.  <span data-ttu-id="1f9f4-139">Knyt en momsgruppe til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="1f9f4-140">Tildel de accepterede betalingsmetoder til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="1f9f4-141">Føj oplysninger til produktbeskrivelserne for de produkter, du tilbyder i dine detailbutikker.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="1f9f4-142">Du kan for eksempel tilføje RTF-tekst og billeder.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="1f9f4-143">Disse produktoplysninger vises i forskellige sammenhænge som på POS-kasseapparat eller på udskrevne etiketter.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="1f9f4-144">Føj butikken til det standardorganisationshierarki, der er tildelt med formålet **Detailudvalg**, **Detailgenopfyldning** eller **Detailrapportering**.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="1f9f4-145">Når du har oprettet en detailbutik</span><span class="sxs-lookup"><span data-stu-id="1f9f4-145">After you set up a retail store</span></span>

<span data-ttu-id="1f9f4-146">Når du har angivet oplysningerne om detailbutikken, skal du udføre disse opgaver for at sende de nye detailbutiksdata til Retail POS:</span><span class="sxs-lookup"><span data-stu-id="1f9f4-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="1f9f4-147">Konfigurer POS-kasseapparaterne til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="1f9f4-148">Tildel produktudvalg til butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="1f9f4-149">Du kan behandle udvalg for at oprette listen over produkter, der indgår i udvalget, og for at gøre produkterne tilgængelige i butikken.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="1f9f4-150">Send data som f.eks. nummerserier, hardwareprofiler og layout for POS-skærmen til Retail POS-kasseapparaterne.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="1f9f4-151">Udgiv detailbutikken for at sende lagringsdata til Retail POS.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="1f9f4-152">Kør jobbene for at sende lagringsdataene til Retail POS.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="1f9f4-153">Organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="1f9f4-153">Organization hierarchies</span></span>
<span data-ttu-id="1f9f4-154">Retail bruger organisationshierarkier til at strukturere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="1f9f4-155">Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="1f9f4-156">Når du opretter butikker, kan du føje dem til et organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="1f9f4-157">Butikkerne deler derefter data, der bruges til udvalg, genbestilling og rapportering.</span><span class="sxs-lookup"><span data-stu-id="1f9f4-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




