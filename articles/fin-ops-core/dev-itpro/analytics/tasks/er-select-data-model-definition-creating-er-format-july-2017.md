---
title: Vælge datamodeldefinitioner, når du opretter formater
description: For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68c5114b8c1e2a2ac5d357ee9e75cc54c149f39d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564260"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="97c97-103">Vælge datamodeldefinitioner, når du opretter formater</span><span class="sxs-lookup"><span data-stu-id="97c97-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97c97-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Oprette en konfigurationsudbyder og markere den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="97c97-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="97c97-105">Denne fremgangsmåde viser, hvordan rodelementet i en model kan vælges som en datamodeldefinition til indsættelse af en ER-formatkonfiguration, der er designet til at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="97c97-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="97c97-106">I denne procedure skal du tilføje en ny ER-formatkonfiguration til eksempelfirmaet Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="97c97-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="97c97-107">Denne procedure er beregnet til brugere, der har fået tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="97c97-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="97c97-108">Trinnene kan udføres ved hjælp af et vilkårligt datasæt.</span><span class="sxs-lookup"><span data-stu-id="97c97-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="97c97-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="97c97-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="97c97-110">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="97c97-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="97c97-111">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren Opret en konfigurationsudbyder, og markér den som aktiv.</span><span class="sxs-lookup"><span data-stu-id="97c97-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="97c97-112">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="97c97-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="97c97-113">Tilføj en ny ER-datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97c97-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="97c97-114">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97c97-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="97c97-115">Vi tilføjer en ny ER-modelkonfiguration, der indeholder en datamodel, der skal bruges som datakilde ved oprettelse af ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="97c97-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="97c97-116">Skriv 'Betalingsmodel (fiktiv)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97c97-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="97c97-117">Betalingsmodel (fiktiv)</span><span class="sxs-lookup"><span data-stu-id="97c97-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="97c97-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97c97-118">Click Create configuration.</span></span>
4. <span data-ttu-id="97c97-119">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="97c97-119">Click Designer.</span></span>
    * <span data-ttu-id="97c97-120">Åbn ER-designeren for at angive strukturen af datamodellen i denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97c97-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="97c97-121">Antag, at vi udvikler datamodellen for en betalings forretningsdomæne for at understøtte 2 betalingsmetoder – pengeoverførsel og direkte debitering.</span><span class="sxs-lookup"><span data-stu-id="97c97-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="97c97-122">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="97c97-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="97c97-123">Skriv 'Betalinger – kreditoverførsel' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97c97-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="97c97-124">Betalinger – kreditoverførsel</span><span class="sxs-lookup"><span data-stu-id="97c97-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="97c97-125">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="97c97-125">Click Add.</span></span>
8. <span data-ttu-id="97c97-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="97c97-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="97c97-127">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="97c97-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="97c97-128">Skriv 'Betalinger – direkte debitering' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97c97-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="97c97-129">Betalinger – direkte debitering</span><span class="sxs-lookup"><span data-stu-id="97c97-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="97c97-130">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="97c97-130">Click Add.</span></span>
12. <span data-ttu-id="97c97-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="97c97-131">Click Save.</span></span>
13. <span data-ttu-id="97c97-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97c97-132">Close the page.</span></span>
14. <span data-ttu-id="97c97-133">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="97c97-133">Click Change status.</span></span>
    * <span data-ttu-id="97c97-134">Fuldfør kladdeversionen af modellen for at gøre den tilgængelig i nye modeltilknytninger og formater.</span><span class="sxs-lookup"><span data-stu-id="97c97-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="97c97-135">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="97c97-135">Click Complete.</span></span>
16. <span data-ttu-id="97c97-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97c97-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="97c97-137">Begynde at angive en ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97c97-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="97c97-138">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97c97-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="97c97-139">Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="97c97-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="97c97-140">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="97c97-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="97c97-141">Bemærk, at alle rodelementer i den valgte datamodel aktuelt kan vælges som datamodeldefinition.</span><span class="sxs-lookup"><span data-stu-id="97c97-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="97c97-142">Du kan fortsætte med at designe dit format ved at bruge et af de krævede rodelementer i datamodellen.</span><span class="sxs-lookup"><span data-stu-id="97c97-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="97c97-143">En manglende modeltilknytning for det valgte rodelementet forhindrer ikke, at du kan fortsætte.</span><span class="sxs-lookup"><span data-stu-id="97c97-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="97c97-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97c97-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="97c97-145">Tilføje en ny ER-modeltilknytningskonfiguration</span><span class="sxs-lookup"><span data-stu-id="97c97-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="97c97-146">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97c97-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="97c97-147">Skriv 'Modeltilknytning baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="97c97-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="97c97-148">Skriv 'Betalingsmodeltilknytninger (fiktiv)' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97c97-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="97c97-149">Betalingsmodeltilknytninger (fiktive)</span><span class="sxs-lookup"><span data-stu-id="97c97-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="97c97-150">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="97c97-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="97c97-151">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97c97-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="97c97-152">Designe ER-modeltilknytninger</span><span class="sxs-lookup"><span data-stu-id="97c97-152">Design ER model mappings</span></span>
1. <span data-ttu-id="97c97-153">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="97c97-153">Click Designer.</span></span>
    * <span data-ttu-id="97c97-154">Brug ER-designeren til at angive modeltilknytningerne for de krævede rodelementer.</span><span class="sxs-lookup"><span data-stu-id="97c97-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="97c97-155">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="97c97-155">Click Designer.</span></span>
    * <span data-ttu-id="97c97-156">Simuler indstilling af den valgte modeltilknytning for rodelementet i den valgte model.</span><span class="sxs-lookup"><span data-stu-id="97c97-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="97c97-157">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="97c97-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="97c97-158">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="97c97-158">Click Add root.</span></span>
5. <span data-ttu-id="97c97-159">Skriv Finans i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="97c97-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="97c97-160">Skriv "LedgerJournalTrans" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="97c97-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="97c97-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="97c97-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="97c97-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="97c97-162">Click OK.</span></span>
8. <span data-ttu-id="97c97-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="97c97-163">Click Save.</span></span>
9. <span data-ttu-id="97c97-164">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97c97-164">Close the page.</span></span>
10. <span data-ttu-id="97c97-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97c97-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="97c97-166">Begynde at angive en anden ny ER-formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="97c97-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="97c97-167">Vælg 'Betalingsmodel (fiktiv)' i træet.</span><span class="sxs-lookup"><span data-stu-id="97c97-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="97c97-168">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="97c97-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="97c97-169">Skriv 'Format baseret på datamodel af typen Betalingsmodel (fiktiv)' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="97c97-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="97c97-170">Indtast eller vælg en værdi i feltet Definition af datamodel.</span><span class="sxs-lookup"><span data-stu-id="97c97-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="97c97-171">Bemærk, at der nu kun findes ét rodelementet, som kan tilknyttes programdatakilderne.</span><span class="sxs-lookup"><span data-stu-id="97c97-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="97c97-172">Når der introduceres mindst én modeltilknytning, er det kun modellens rodelementer, som er knyttet til programdatakilder, der kan vælges som modeldefinition, mens ER-formatet er tilføjet.</span><span class="sxs-lookup"><span data-stu-id="97c97-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="97c97-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="97c97-173">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]