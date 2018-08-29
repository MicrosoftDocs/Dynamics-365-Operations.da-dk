--- 
title: "Designe domænespecifikke datamodeller"
description: "Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c59bdea789c4eafd2443a5d1cf802768259858c6
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="design-domain-specific-data-models"></a><span data-ttu-id="542cd-103">Designe domænespecifikke datamodeller</span><span class="sxs-lookup"><span data-stu-id="542cd-103">Design domain-specific data models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="542cd-104">Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler til elektronisk rapportering kan oprette en ny konfiguration til elektronisk rapportering (ER), der indeholder en datamodel til dokumenter til elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="542cd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="542cd-105">Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.</span><span class="sxs-lookup"><span data-stu-id="542cd-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="542cd-106">I dette eksempel skal du oprette en konfiguration af en udbyder for eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i alle virksomheder, da ER-konfigurationer deles af alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="542cd-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="542cd-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="542cd-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="542cd-108">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="542cd-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="542cd-109">Vælg konfigurationsudbyderen for eksempelvirksomheden, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="542cd-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="542cd-110">Hvis konfigurationsudbyderen ikke vises, skal du først fuldføre trinnene i proceduren "Oprette en konfigurationsudbyder og markere den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="542cd-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="542cd-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="542cd-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="542cd-112">Du skal oprette en konfiguration, der indeholder en datamodel for dokumenter til elektronisk betaling.</span><span class="sxs-lookup"><span data-stu-id="542cd-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="542cd-113">Denne datamodel bruges senere som en datakilde, når du har oprettet formatet for betalingsdokumenterne.</span><span class="sxs-lookup"><span data-stu-id="542cd-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="542cd-114">Opret en ny datamodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="542cd-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="542cd-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="542cd-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="542cd-116">Skriv "Betalinger (forenklet model)" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="542cd-117">Betalinger (forenklet model)</span><span class="sxs-lookup"><span data-stu-id="542cd-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="542cd-118">Skriv "Betalingsmodelkonfiguration" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="542cd-119">Betalingsmodelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="542cd-119">Payment model configuration</span></span>  
    * <span data-ttu-id="542cd-120">Den aktive konfigurationsudbyder indsættes automatisk her.</span><span class="sxs-lookup"><span data-stu-id="542cd-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="542cd-121">Denne udbyder vil kunne vedligeholde denne konfiguration.</span><span class="sxs-lookup"><span data-stu-id="542cd-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="542cd-122">Andre udbydere kan bruge denne konfiguration, men vil ikke kunne vedligeholde den.</span><span class="sxs-lookup"><span data-stu-id="542cd-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="542cd-123">Klik på "Opret konfiguration" for at fuldføre oprettelsen af konfigurationsopgaven</span><span class="sxs-lookup"><span data-stu-id="542cd-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="542cd-124">Opret en datamodel</span><span class="sxs-lookup"><span data-stu-id="542cd-124">Create a data model</span></span>
    * <span data-ttu-id="542cd-125">Du er ved at oprette en ny datamodel for den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="542cd-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="542cd-126">Denne konfigurationsversion får statussen Kladde.</span><span class="sxs-lookup"><span data-stu-id="542cd-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="542cd-127">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="542cd-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="542cd-128">Definer strukturen af en part, der deltager i en betalingsproces</span><span class="sxs-lookup"><span data-stu-id="542cd-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="542cd-129">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="542cd-130">Skriv "Part" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="542cd-131">Part</span><span class="sxs-lookup"><span data-stu-id="542cd-131">Party</span></span>  
3. <span data-ttu-id="542cd-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-132">Click Add.</span></span>
4. <span data-ttu-id="542cd-133">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="542cd-134">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="542cd-135">Navn</span><span class="sxs-lookup"><span data-stu-id="542cd-135">Name</span></span>  
6. <span data-ttu-id="542cd-136">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="542cd-137">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-137">Click Add.</span></span>
8. <span data-ttu-id="542cd-138">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="542cd-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="542cd-139">Part</span><span class="sxs-lookup"><span data-stu-id="542cd-139">Party</span></span>  
9. <span data-ttu-id="542cd-140">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="542cd-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="542cd-141">Definer bankstrukturen for denne model</span><span class="sxs-lookup"><span data-stu-id="542cd-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="542cd-142">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="542cd-143">Skriv "Agent" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="542cd-144">Speditør</span><span class="sxs-lookup"><span data-stu-id="542cd-144">Agent</span></span>  
3. <span data-ttu-id="542cd-145">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="542cd-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-146">Click Add.</span></span>
5. <span data-ttu-id="542cd-147">Angiv "Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor)" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="542cd-148">Pengeinstitut (f.eks. bank), der servicerer en konto for parten (debitor/kreditor).</span><span class="sxs-lookup"><span data-stu-id="542cd-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="542cd-149">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="542cd-150">Skriv "Navn" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="542cd-151">Navn</span><span class="sxs-lookup"><span data-stu-id="542cd-151">Name</span></span>  
8. <span data-ttu-id="542cd-152">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="542cd-153">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-153">Click Add.</span></span>
10. <span data-ttu-id="542cd-154">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="542cd-155">Skriv "SWIFT" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="542cd-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="542cd-156">SWIFT</span></span>  
12. <span data-ttu-id="542cd-157">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-157">Click Add.</span></span>
13. <span data-ttu-id="542cd-158">Skriv "Bankens identifikationskode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="542cd-159">Bankens identifikationskode</span><span class="sxs-lookup"><span data-stu-id="542cd-159">Bank identification code</span></span>  
14. <span data-ttu-id="542cd-160">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="542cd-161">Skriv "RoutingNumber" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="542cd-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="542cd-162">RoutingNumber</span></span>  
16. <span data-ttu-id="542cd-163">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-163">Click Add.</span></span>
17. <span data-ttu-id="542cd-164">Skriv "Registreringsnummer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="542cd-165">Registreringsnummer</span><span class="sxs-lookup"><span data-stu-id="542cd-165">Routing number</span></span>  
18. <span data-ttu-id="542cd-166">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="542cd-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="542cd-167">Definer bankkontostrukturen for denne model</span><span class="sxs-lookup"><span data-stu-id="542cd-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="542cd-168">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="542cd-169">Skriv "Konto" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="542cd-170">Konto</span><span class="sxs-lookup"><span data-stu-id="542cd-170">Account</span></span>  
3. <span data-ttu-id="542cd-171">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="542cd-172">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-172">Click Add.</span></span>
5. <span data-ttu-id="542cd-173">Skriv "Identifikation af en parts konto i et pengeinstitut (f.eks. en bank)." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="542cd-174">Identifikation af en parts konto i et pengeinstitut (f.eks. en bank).</span><span class="sxs-lookup"><span data-stu-id="542cd-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="542cd-175">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="542cd-176">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="542cd-177">Valuta</span><span class="sxs-lookup"><span data-stu-id="542cd-177">Currency</span></span>  
8. <span data-ttu-id="542cd-178">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="542cd-179">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-179">Click Add.</span></span>
10. <span data-ttu-id="542cd-180">Indtast "Valutakode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="542cd-181">Valutakode</span><span class="sxs-lookup"><span data-stu-id="542cd-181">Currency code</span></span>  
11. <span data-ttu-id="542cd-182">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="542cd-183">Skriv "Tal" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="542cd-184">Tal</span><span class="sxs-lookup"><span data-stu-id="542cd-184">Number</span></span>  
13. <span data-ttu-id="542cd-185">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-185">Click Add.</span></span>
14. <span data-ttu-id="542cd-186">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="542cd-187">Skriv "IBAN" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="542cd-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="542cd-188">IBAN</span></span>  
16. <span data-ttu-id="542cd-189">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-189">Click Add.</span></span>
17. <span data-ttu-id="542cd-190">Skriv "Internationalt bankkontonummer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="542cd-191">Internationalt bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="542cd-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="542cd-192">Definer betalingsmeddelelsesstruktur for overførsel af kundekredittype.</span><span class="sxs-lookup"><span data-stu-id="542cd-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="542cd-193">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="542cd-194">Skriv "Modelrod" i feltet Ny node som felt.</span><span class="sxs-lookup"><span data-stu-id="542cd-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="542cd-195">Skriv "CustomerCreditTransferInitiation" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="542cd-196">Vælg CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="542cd-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="542cd-197">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-197">Click Add.</span></span>
5. <span data-ttu-id="542cd-198">Skriv "CustomerCreditTransferInitiation" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="542cd-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="542cd-199">Vælg CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="542cd-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="542cd-200">Klik på Find forrige.</span><span class="sxs-lookup"><span data-stu-id="542cd-200">Click Find previous.</span></span>
7. <span data-ttu-id="542cd-201">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="542cd-202">Skriv "MessageIdentification" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="542cd-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="542cd-203">MessageIdentification</span></span>  
9. <span data-ttu-id="542cd-204">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-204">Click Add.</span></span>
10. <span data-ttu-id="542cd-205">Angiv "Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="542cd-206">Punkt til punkt-referencen, som tildelt af den instruerende part (og sendt til den næste part) for at identificere en meddelelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="542cd-207">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="542cd-208">Skriv "ProcessingDateTime" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="542cd-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="542cd-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="542cd-210">Vælg "DateTime" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="542cd-211">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-211">Click Add.</span></span>
15. <span data-ttu-id="542cd-212">Angiv "Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="542cd-213">Dato og klokkeslæt, hvor betalingsmeddelelsen blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="542cd-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="542cd-214">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="542cd-215">Definer betalingstransaktionen for denne model.</span><span class="sxs-lookup"><span data-stu-id="542cd-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="542cd-216">Skriv "Betalinger" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="542cd-217">Betalinger</span><span class="sxs-lookup"><span data-stu-id="542cd-217">Payments</span></span>  
18. <span data-ttu-id="542cd-218">Vælg "Liste over poster" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="542cd-219">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-219">Click Add.</span></span>
20. <span data-ttu-id="542cd-220">Angiv "Betalingslinjer for den aktuelle meddelelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="542cd-221">Betalingslinjer for den aktuelle meddelelse</span><span class="sxs-lookup"><span data-stu-id="542cd-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="542cd-222">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="542cd-223">Skriv "Kreditor" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="542cd-224">Kreditor</span><span class="sxs-lookup"><span data-stu-id="542cd-224">Creditor</span></span>  
23. <span data-ttu-id="542cd-225">Vælg "Post" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="542cd-226">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-226">Click Add.</span></span>
25. <span data-ttu-id="542cd-227">Angiv "Part, til hvem et beløb er forfaldent." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="542cd-228">Part, til hvem et beløb er forfaldent.</span><span class="sxs-lookup"><span data-stu-id="542cd-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="542cd-229">Klik på Skift varereference.</span><span class="sxs-lookup"><span data-stu-id="542cd-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="542cd-230">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="542cd-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="542cd-231">Part</span><span class="sxs-lookup"><span data-stu-id="542cd-231">Party</span></span>  
28. <span data-ttu-id="542cd-232">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="542cd-232">Click Find next.</span></span>
29. <span data-ttu-id="542cd-233">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="542cd-233">Click OK.</span></span>
30. <span data-ttu-id="542cd-234">Skriv "Betalinger" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="542cd-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="542cd-235">Betalinger</span><span class="sxs-lookup"><span data-stu-id="542cd-235">Payments</span></span>  
31. <span data-ttu-id="542cd-236">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="542cd-236">Click Find next.</span></span>
32. <span data-ttu-id="542cd-237">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="542cd-238">Skriv "Debitor"i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="542cd-239">Debitor</span><span class="sxs-lookup"><span data-stu-id="542cd-239">Debtor</span></span>  
34. <span data-ttu-id="542cd-240">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-240">Click Add.</span></span>
35. <span data-ttu-id="542cd-241">Angiv "Part, der skylder et beløb til (den endelige) kreditor." i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="542cd-242">Part, der skylder et beløb til (den endelige) kreditor.</span><span class="sxs-lookup"><span data-stu-id="542cd-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="542cd-243">Klik på Skift varereference.</span><span class="sxs-lookup"><span data-stu-id="542cd-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="542cd-244">Skriv "Part" i feltet Søg.</span><span class="sxs-lookup"><span data-stu-id="542cd-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="542cd-245">Part</span><span class="sxs-lookup"><span data-stu-id="542cd-245">Party</span></span>  
38. <span data-ttu-id="542cd-246">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="542cd-246">Click Find next.</span></span>
39. <span data-ttu-id="542cd-247">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="542cd-247">Click OK.</span></span>
40. <span data-ttu-id="542cd-248">Klik på Find næste.</span><span class="sxs-lookup"><span data-stu-id="542cd-248">Click Find next.</span></span>
41. <span data-ttu-id="542cd-249">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="542cd-250">Skriv "Beskrivelse" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="542cd-251">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="542cd-251">Description</span></span>  
43. <span data-ttu-id="542cd-252">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="542cd-253">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-253">Click Add.</span></span>
45. <span data-ttu-id="542cd-254">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="542cd-255">Skriv "Valuta" feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="542cd-256">Valuta</span><span class="sxs-lookup"><span data-stu-id="542cd-256">Currency</span></span>  
47. <span data-ttu-id="542cd-257">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-257">Click Add.</span></span>
48. <span data-ttu-id="542cd-258">Indtast "Valutakode" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="542cd-259">Valutakode</span><span class="sxs-lookup"><span data-stu-id="542cd-259">Currency code</span></span>  
49. <span data-ttu-id="542cd-260">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="542cd-261">Angiv "TransactionDate" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="542cd-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="542cd-262">TransactionDate</span></span>  
51. <span data-ttu-id="542cd-263">Vælg "Dato" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="542cd-264">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-264">Click Add.</span></span>
53. <span data-ttu-id="542cd-265">Angiv "Posteringsdato" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="542cd-266">Posteringsdato</span><span class="sxs-lookup"><span data-stu-id="542cd-266">Transaction date</span></span>  
54. <span data-ttu-id="542cd-267">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="542cd-268">Skriv "InstructedAmount" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="542cd-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="542cd-269">InstructedAmount</span></span>  
56. <span data-ttu-id="542cd-270">Vælg "Kommatal" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="542cd-271">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-271">Click Add.</span></span>
58. <span data-ttu-id="542cd-272">Angiv "Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="542cd-273">Beløbet skal angives i den valuta, som bestilt af den startende part.</span><span class="sxs-lookup"><span data-stu-id="542cd-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="542cd-274">Det beløb, der skal flyttes mellem debitor og kreditor, før fratrækning af gebyrer.</span><span class="sxs-lookup"><span data-stu-id="542cd-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="542cd-275">Beløbet skal angives i den valuta, som bestilt af den startende part.</span><span class="sxs-lookup"><span data-stu-id="542cd-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="542cd-276">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="542cd-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="542cd-277">Skriv "End2EndID" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="542cd-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="542cd-278">End2EndID</span></span>  
61. <span data-ttu-id="542cd-279">Vælg "Streng" i feltet Varetype.</span><span class="sxs-lookup"><span data-stu-id="542cd-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="542cd-280">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="542cd-280">Click Add.</span></span>
63. <span data-ttu-id="542cd-281">Angiv "Den entydige identifikation, der er tildelt af den startende part" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="542cd-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="542cd-282">Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden.</span><span class="sxs-lookup"><span data-stu-id="542cd-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="542cd-283">Den entydige identifikation, der er tildelt af den startende part.</span><span class="sxs-lookup"><span data-stu-id="542cd-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="542cd-284">Denne identifikation overføres, uændret, i hele slutpunkt til slutpunkt-kæden.</span><span class="sxs-lookup"><span data-stu-id="542cd-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="542cd-285">Skriv "PaymentModel" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="542cd-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="542cd-286">Navnet på PaymentModel justeres med foruddefinerede grænseflader for betalingsformer.</span><span class="sxs-lookup"><span data-stu-id="542cd-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="542cd-287">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="542cd-287">Click Save.</span></span>
66. <span data-ttu-id="542cd-288">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="542cd-288">Close the page.</span></span>


