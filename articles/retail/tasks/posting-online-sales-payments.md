---
title: Bogføring af onlinesalg og betalinger
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864147"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="3b8ff-103">Bogføring af onlinesalg og betalinger</span><span class="sxs-lookup"><span data-stu-id="3b8ff-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3b8ff-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="3b8ff-105">Bogføring af onlinesalg og -betalinger er en proces i to faser.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="3b8ff-106">Hentning af online detailtransaktionsdata i hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="3b8ff-107">Synkronisering af ordrer for at oprette salgsordrer i hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="3b8ff-108">Når du henter online detailtransaktionsdata, kan du enten gøre det ved at udføre P-job manuelt eller ved at oprette et tilbagevendende batchjob.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="3b8ff-109">Manuel kørsel af P-job</span><span class="sxs-lookup"><span data-stu-id="3b8ff-109">Manually running the P-job</span></span>

1. <span data-ttu-id="3b8ff-110">Gå til Alle arbejdsområder > Retail IT.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="3b8ff-111">Klik på Distributionsplan.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3b8ff-112">Vælg P-0001.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-112">Select P-0001.</span></span>
4. <span data-ttu-id="3b8ff-113">Juster kanaldatabasegrupper, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="3b8ff-114">Klik på Kør nu.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-114">Click Run now.</span></span>
6. <span data-ttu-id="3b8ff-115">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="3b8ff-116">Planlægning af et tilbagevendende P-job</span><span class="sxs-lookup"><span data-stu-id="3b8ff-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="3b8ff-117">Gå til Alle arbejdsområder > Retail IT.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="3b8ff-118">Klik på Distributionsplan.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="3b8ff-119">Vælg P-0001.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-119">Select P-0001.</span></span>
4. <span data-ttu-id="3b8ff-120">Klik på Opret batchjob.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-120">Click Create batch job.</span></span>
5. <span data-ttu-id="3b8ff-121">Klik på Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-121">Click Run in the background.</span></span>
5. <span data-ttu-id="3b8ff-122">Aktivér batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="3b8ff-123">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-123">Click Recurrence..</span></span>
7. <span data-ttu-id="3b8ff-124">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-124">Select the No end date option.</span></span>
8. <span data-ttu-id="3b8ff-125">Angiv intervallet mellem kørslerne i minutter i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3b8ff-126">Dette vil typisk være 5-10.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="3b8ff-127">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-127">Click OK.</span></span>
10. <span data-ttu-id="3b8ff-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-128">Click OK.</span></span>

<span data-ttu-id="3b8ff-129">Ordrer kan synkroniseres enten via manuel kørsel af "Synkroniser ordrer"-job eller ved at oprette et tilbagevendende batchjob.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="3b8ff-130">Manuel kørsel af ordresynkronisering</span><span class="sxs-lookup"><span data-stu-id="3b8ff-130">Manually running order synchronization</span></span> 

<span data-ttu-id="3b8ff-131">Udfør følgende trin for manuelt at køre jobbet "Synkroniser ordrer" én gang.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="3b8ff-132">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3b8ff-133">Kik på Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3b8ff-134">Vælg "Detailbutikker efter område" i feltet Organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="3b8ff-135">Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3b8ff-136">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3b8ff-137">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3b8ff-138">Deaktiver batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-138">Disable Batch processing</span></span>
6. <span data-ttu-id="3b8ff-139">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-139">Click Recurrence.</span></span>
7. <span data-ttu-id="3b8ff-140">Vælg indstillingen Afslut efter.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-140">Select End After option</span></span>
8. <span data-ttu-id="3b8ff-141">Angiv 1 i feltet Afslut efter.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="3b8ff-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-142">Click OK.</span></span>
10. <span data-ttu-id="3b8ff-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="3b8ff-144">Planlægge synkronisering af tilbagevendende ordrer</span><span class="sxs-lookup"><span data-stu-id="3b8ff-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="3b8ff-145">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="3b8ff-146">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3b8ff-147">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3b8ff-148">Kik på Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="3b8ff-149">Vælg "Detailbutikker efter område" i feltet Organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="3b8ff-150">Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3b8ff-151">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="3b8ff-152">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="3b8ff-153">Aktivér batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-153">Enable Batch processing</span></span>
6. <span data-ttu-id="3b8ff-154">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-154">Click Recurrence.</span></span>
7. <span data-ttu-id="3b8ff-155">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-155">Select the No end date option.</span></span>
8. <span data-ttu-id="3b8ff-156">Angiv intervallet mellem kørslerne i minutter i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="3b8ff-157">Dette er typisk 2-20.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="3b8ff-158">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-158">Click OK.</span></span>
10. <span data-ttu-id="3b8ff-159">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3b8ff-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="3b8ff-160">Dataenheder, der er involveret i processen</span><span class="sxs-lookup"><span data-stu-id="3b8ff-160">Data entities involved in the process</span></span>

- <span data-ttu-id="3b8ff-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="3b8ff-161">RetailTransactionTable</span></span>
- <span data-ttu-id="3b8ff-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="3b8ff-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="3b8ff-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="3b8ff-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="3b8ff-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="3b8ff-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="3b8ff-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="3b8ff-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="3b8ff-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="3b8ff-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="3b8ff-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="3b8ff-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="3b8ff-171">RetailTransactionAttributeTrans</span></span>
