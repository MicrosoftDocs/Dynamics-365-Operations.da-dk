---
title: Design ER-domænespecifik datamodel
description: Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681943"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="3eff5-103">Design ER-domænespecifik datamodel</span><span class="sxs-lookup"><span data-stu-id="3eff5-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3eff5-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="3eff5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="3eff5-105">Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.</span><span class="sxs-lookup"><span data-stu-id="3eff5-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="3eff5-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="3eff5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="3eff5-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="3eff5-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="3eff5-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="3eff5-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="3eff5-109">Vælg konfigurationsudbyderen for eksempelvirksomheden, 'Litware, Inc'.</span><span class="sxs-lookup"><span data-stu-id="3eff5-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="3eff5-110">Hvis du ikke kan se denne konfigurationsudbyder, skal du først fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="3eff5-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="3eff5-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="3eff5-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="3eff5-112">Du skal oprette en konfiguration, der indeholder en datamodel for dokumenter til elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="3eff5-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="3eff5-113">Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.</span><span class="sxs-lookup"><span data-stu-id="3eff5-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="3eff5-114">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3eff5-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="3eff5-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3eff5-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="3eff5-116">Skriv "Betalinger (forenklet model)" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="3eff5-117">Skriv "Betalingsmodelkonfiguration" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="3eff5-118">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="3eff5-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="3eff5-119">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3eff5-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="3eff5-120">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="3eff5-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="3eff5-121">Klik på "Opret konfiguration" for at fuldføre oprettelsen af konfigurationsopgaven</span><span class="sxs-lookup"><span data-stu-id="3eff5-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="3eff5-122">Opret en datamodel</span><span class="sxs-lookup"><span data-stu-id="3eff5-122">Create a data model</span></span>
<span data-ttu-id="3eff5-123">Du er ved at oprette en ny datamodel for den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3eff5-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="3eff5-124">Denne konfigurationsversion får statussen Kladde.</span><span class="sxs-lookup"><span data-stu-id="3eff5-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="3eff5-125">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="3eff5-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="3eff5-126">Definer strukturen af en part, der deltager i en betalingsproces</span><span class="sxs-lookup"><span data-stu-id="3eff5-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="3eff5-127">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="3eff5-128">Skriv "Part" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="3eff5-129">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-129">Click Add.</span></span>
4. <span data-ttu-id="3eff5-130">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="3eff5-131">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="3eff5-132">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="3eff5-133">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-133">Click Add.</span></span>
8. <span data-ttu-id="3eff5-134">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="3eff5-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="3eff5-135">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="3eff5-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="3eff5-136">Definer bankstrukturen for denne model</span><span class="sxs-lookup"><span data-stu-id="3eff5-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="3eff5-137">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="3eff5-138">Skriv "Agent" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="3eff5-139">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="3eff5-140">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-140">Click Add.</span></span>
5. <span data-ttu-id="3eff5-141">Angiv "Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor)" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="3eff5-142">Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor).</span><span class="sxs-lookup"><span data-stu-id="3eff5-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="3eff5-143">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="3eff5-144">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="3eff5-145">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="3eff5-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-146">Click Add.</span></span>
10. <span data-ttu-id="3eff5-147">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="3eff5-148">Skriv "SWIFT" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="3eff5-149">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-149">Click Add.</span></span>
13. <span data-ttu-id="3eff5-150">Skriv "Bankens identifikationskode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="3eff5-151">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="3eff5-152">Skriv "RoutingNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="3eff5-153">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-153">Click Add.</span></span>
17. <span data-ttu-id="3eff5-154">Skriv "Registreringsnummer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="3eff5-155">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="3eff5-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="3eff5-156">Definer bankkontostrukturen for denne model</span><span class="sxs-lookup"><span data-stu-id="3eff5-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="3eff5-157">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="3eff5-158">Skriv "Konto" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="3eff5-159">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="3eff5-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-160">Click Add.</span></span>
5. <span data-ttu-id="3eff5-161">Skriv "Identifikation af en parts konto i et pengeinstitut (f.eks. en bank)." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="3eff5-162">Identifikation af en parts konto i et pengeinstitut (f.eks. en bank).</span><span class="sxs-lookup"><span data-stu-id="3eff5-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="3eff5-163">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="3eff5-164">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="3eff5-165">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="3eff5-166">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-166">Click Add.</span></span>
10. <span data-ttu-id="3eff5-167">Indtast "Valutakode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="3eff5-168">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="3eff5-169">Skriv "Tal" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="3eff5-170">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-170">Click Add.</span></span>
14. <span data-ttu-id="3eff5-171">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="3eff5-172">Skriv "IBAN" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="3eff5-173">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-173">Click Add.</span></span>
17. <span data-ttu-id="3eff5-174">Skriv "Internationalt bankkontonummer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="3eff5-175">Definer betalingsmeddelelsesstruktur for overførsel af kundekredittype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="3eff5-176">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="3eff5-177">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="3eff5-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="3eff5-178">Skriv "CustomerCreditTransferInitiation" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="3eff5-179">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-179">Click Add.</span></span>
5. <span data-ttu-id="3eff5-180">Skriv "CustomerCreditTransferInitiation" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="3eff5-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="3eff5-181">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="3eff5-181">Click Find previous.</span></span>
7. <span data-ttu-id="3eff5-182">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="3eff5-183">Skriv "MessageIdentification" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="3eff5-184">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-184">Click Add.</span></span>
10. <span data-ttu-id="3eff5-185">Angiv "Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="3eff5-186">Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="3eff5-187">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="3eff5-188">Skriv "ProcessingDateTime" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="3eff5-189">Vælg "DateTime" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="3eff5-190">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-190">Click Add.</span></span>
15. <span data-ttu-id="3eff5-191">Angiv "Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="3eff5-192">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="3eff5-193">Definer betalingstransaktionen for denne model.</span><span class="sxs-lookup"><span data-stu-id="3eff5-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="3eff5-194">Skriv "Betalinger" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="3eff5-195">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="3eff5-196">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-196">Click Add.</span></span>
20. <span data-ttu-id="3eff5-197">Angiv "Betalingslinjer for den aktuelle meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="3eff5-198">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="3eff5-199">Skriv "Kreditor" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="3eff5-200">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="3eff5-201">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-201">Click Add.</span></span>
25. <span data-ttu-id="3eff5-202">Angiv "Part, til hvem et beløb er forfaldent." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="3eff5-203">Klik på Skift varereference.</span><span class="sxs-lookup"><span data-stu-id="3eff5-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="3eff5-204">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="3eff5-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="3eff5-205">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="3eff5-205">Click Find next.</span></span>
29. <span data-ttu-id="3eff5-206">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3eff5-206">Click OK.</span></span>
30. <span data-ttu-id="3eff5-207">Skriv "Betalinger" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="3eff5-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="3eff5-208">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="3eff5-208">Click Find next.</span></span>
32. <span data-ttu-id="3eff5-209">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="3eff5-210">Skriv "Debitor"i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="3eff5-211">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-211">Click Add.</span></span>
35. <span data-ttu-id="3eff5-212">Angiv "Part, der skylder et beløb til (den endelige) kreditor." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="3eff5-213">Klik på Skift varereference.</span><span class="sxs-lookup"><span data-stu-id="3eff5-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="3eff5-214">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="3eff5-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="3eff5-215">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="3eff5-215">Click Find next.</span></span>
39. <span data-ttu-id="3eff5-216">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3eff5-216">Click OK.</span></span>
40. <span data-ttu-id="3eff5-217">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="3eff5-217">Click Find next.</span></span>
41. <span data-ttu-id="3eff5-218">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="3eff5-219">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="3eff5-220">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="3eff5-221">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-221">Click Add.</span></span>
45. <span data-ttu-id="3eff5-222">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="3eff5-223">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="3eff5-224">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-224">Click Add.</span></span>
48. <span data-ttu-id="3eff5-225">Indtast "Valutakode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="3eff5-226">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="3eff5-227">Angiv "TransactionDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="3eff5-228">Vælg "Dato" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="3eff5-229">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-229">Click Add.</span></span>
53. <span data-ttu-id="3eff5-230">Angiv "Posteringsdato" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="3eff5-231">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="3eff5-232">Skriv "InstructedAmount" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="3eff5-233">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="3eff5-234">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-234">Click Add.</span></span>
58. <span data-ttu-id="3eff5-235">Angiv "Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="3eff5-236">Beløbet skal angives i den valuta, som bestilt af den startende part.</span><span class="sxs-lookup"><span data-stu-id="3eff5-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="3eff5-237">Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer.</span><span class="sxs-lookup"><span data-stu-id="3eff5-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="3eff5-238">Beløbet skal angives i den valuta, som bestilt af den startende part.</span><span class="sxs-lookup"><span data-stu-id="3eff5-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="3eff5-239">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="3eff5-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="3eff5-240">Skriv "End2EndID" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="3eff5-241">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="3eff5-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="3eff5-242">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="3eff5-242">Click Add.</span></span>
63. <span data-ttu-id="3eff5-243">Angiv "Den entydige identifikation, der er tildelt af den startende part" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3eff5-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="3eff5-244">Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden.</span><span class="sxs-lookup"><span data-stu-id="3eff5-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="3eff5-245">Skriv "PaymentModel" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="3eff5-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="3eff5-246">Navnet på PaymentModel justeres med foruddefinerede grænseflader for betalingsformer.</span><span class="sxs-lookup"><span data-stu-id="3eff5-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="3eff5-247">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3eff5-247">Click Save.</span></span>
66. <span data-ttu-id="3eff5-248">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3eff5-248">Close the page.</span></span>

