---
title: Vælge datamodeldefinitioner, når du opretter formater
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551083"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="9749f-103">Vælge datamodeldefinitioner, når du opretter formater</span><span class="sxs-lookup"><span data-stu-id="9749f-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9749f-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="9749f-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="9749f-105">Denne fremgangsmåde viser, hvordan rodelementet i en model kan vælges som en datamodeldefinition til indsættelse af en ER-formatkonfiguration, der er designet til at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="9749f-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="9749f-106">I denne procedure skal du tilføje en ny ER-formatkonfiguration til eksempelfirmaet Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="9749f-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="9749f-107">Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="9749f-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="9749f-108">Trinnene kan udføres ved hjælp af et vilkårligt datasæt.</span><span class="sxs-lookup"><span data-stu-id="9749f-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="9749f-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="9749f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9749f-110">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="9749f-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="9749f-111">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="9749f-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="9749f-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="9749f-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="9749f-113">Tilføj en ny ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9749f-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="9749f-114">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9749f-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="9749f-115">Vi tilføjer en ny ER-modelkonfiguration, der indeholder en datamodel, der skal bruges som datakilde ved oprettelse af ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="9749f-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="9749f-116">Skriv 'Betalingsmodel (fiktiv)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9749f-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="9749f-117">Betalingsmodel (fiktiv)</span><span class="sxs-lookup"><span data-stu-id="9749f-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="9749f-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9749f-118">Click Create configuration.</span></span>
4. <span data-ttu-id="9749f-119">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="9749f-119">Click Designer.</span></span>
    * <span data-ttu-id="9749f-120">Åbn ER-designeren for at angive strukturen af datamodellen i denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9749f-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="9749f-121">Antag, at vi udvikler datamodellen for en betalings forretningsdomæne for at understøtte 2 betalingsmetoder – pengeoverførsel og direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="9749f-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="9749f-122">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="9749f-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="9749f-123">Skriv 'Betalinger – kreditoverførsel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9749f-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="9749f-124">Betalinger – kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="9749f-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="9749f-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9749f-125">Click Add.</span></span>
8. <span data-ttu-id="9749f-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="9749f-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="9749f-127">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="9749f-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="9749f-128">Skriv 'Betalinger – direkte debitering' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9749f-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="9749f-129">Betalinger – direkte debitering</span><span class="sxs-lookup"><span data-stu-id="9749f-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="9749f-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9749f-130">Click Add.</span></span>
12. <span data-ttu-id="9749f-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9749f-131">Click Save.</span></span>
13. <span data-ttu-id="9749f-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9749f-132">Close the page.</span></span>
14. <span data-ttu-id="9749f-133">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="9749f-133">Click Change status.</span></span>
    * <span data-ttu-id="9749f-134">Fuldfør kladdeversionen af modellen for at gøre den tilgængelig i nye modeltilknytninger og formater.</span><span class="sxs-lookup"><span data-stu-id="9749f-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="9749f-135">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="9749f-135">Click Complete.</span></span>
16. <span data-ttu-id="9749f-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9749f-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="9749f-137">Begynde at angive en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9749f-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="9749f-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9749f-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="9749f-139">Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="9749f-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="9749f-140">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="9749f-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="9749f-141">Bemærk, at alle rodelementer i den valgte datamodel aktuelt kan vælges som datamodeldefinition.</span><span class="sxs-lookup"><span data-stu-id="9749f-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="9749f-142">Du kan fortsætte med at designe dit format ved at bruge et af de krævede rodelementer i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="9749f-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="9749f-143">En manglende modeltilknytning for det valgte rodelementet forhindrer ikke, at du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9749f-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="9749f-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9749f-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="9749f-145">Tilføje en ny ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="9749f-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="9749f-146">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9749f-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="9749f-147">Skriv 'Modeltilknytning baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="9749f-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="9749f-148">Skriv 'Betalingsmodeltilknytninger (fiktiv)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9749f-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="9749f-149">Betalingsmodeltilknytninger (fiktive)</span><span class="sxs-lookup"><span data-stu-id="9749f-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="9749f-150">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="9749f-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="9749f-151">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9749f-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="9749f-152">Designe ER-modeltilknytninger</span><span class="sxs-lookup"><span data-stu-id="9749f-152">Design ER model mappings</span></span>
1. <span data-ttu-id="9749f-153">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="9749f-153">Click Designer.</span></span>
    * <span data-ttu-id="9749f-154">Brug ER-designeren til at angive modeltilknytningerne for de krævede rodelementer.</span><span class="sxs-lookup"><span data-stu-id="9749f-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="9749f-155">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="9749f-155">Click Designer.</span></span>
    * <span data-ttu-id="9749f-156">Simuler indstilling af den valgte modeltilknytning for rodelementet i den valgte model.</span><span class="sxs-lookup"><span data-stu-id="9749f-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="9749f-157">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="9749f-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="9749f-158">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="9749f-158">Click Add root.</span></span>
5. <span data-ttu-id="9749f-159">Skriv Finans i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9749f-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="9749f-160">Skriv "LedgerJournalTrans" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="9749f-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="9749f-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="9749f-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="9749f-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9749f-162">Click OK.</span></span>
8. <span data-ttu-id="9749f-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9749f-163">Click Save.</span></span>
9. <span data-ttu-id="9749f-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9749f-164">Close the page.</span></span>
10. <span data-ttu-id="9749f-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9749f-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="9749f-166">Begynde at angive en anden ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9749f-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="9749f-167">Vælg 'Betalingsmodel (fiktiv)' i træet.</span><span class="sxs-lookup"><span data-stu-id="9749f-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="9749f-168">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9749f-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="9749f-169">Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="9749f-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="9749f-170">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="9749f-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="9749f-171">Bemærk, at der nu kun findes ét rodelementet, som kan tilknyttes programdatakilderne.</span><span class="sxs-lookup"><span data-stu-id="9749f-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="9749f-172">Når der introduceres mindst én modeltilknytning, er det kun modellens rodelementer, som er knyttet til programdatakilder, der kan vælges som modeldefinition, mens ER-formatet er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="9749f-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="9749f-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9749f-173">Close the page.</span></span>

