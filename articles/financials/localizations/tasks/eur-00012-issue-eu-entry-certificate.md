--- 
title: "Udstede et EU-indførselscertifikat"
description: "Denne procedure fører dig gennem aktivering af et EU-posteringscertifikat og konfiguration af en debitorkonto for at bruge indførselscertifikater og udstede et certifikat."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5f795c5b5591c161388beeb6d01527dc7c4af8cc
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="issue-an-eu-entry-certificate"></a><span data-ttu-id="b29bb-103">Udstede et EU-indførselscertifikat</span><span class="sxs-lookup"><span data-stu-id="b29bb-103">Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b29bb-104">Denne procedure fører dig gennem aktivering af et EU-posteringscertifikat og konfiguration af en debitorkonto for at bruge indførselscertifikater og udstede et certifikat.</span><span class="sxs-lookup"><span data-stu-id="b29bb-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="b29bb-105">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="b29bb-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="b29bb-106">Aktivér administration af indførselscertifikater</span><span class="sxs-lookup"><span data-stu-id="b29bb-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="b29bb-107">Gå til Debitor > Opsætning > Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="b29bb-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="b29bb-108">Klik på fanen Forsendelser.</span><span class="sxs-lookup"><span data-stu-id="b29bb-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="b29bb-109">Udvid sektionen Postcertifikat.</span><span class="sxs-lookup"><span data-stu-id="b29bb-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="b29bb-110">Vælg Ja i feltet Aktivér administration af indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="b29bb-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="b29bb-111">Vælg Ja i feltet Aktivér udstedelse af indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="b29bb-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="b29bb-112">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="b29bb-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="b29bb-113">Find og vælg rækken Postcertifikat på listen.</span><span class="sxs-lookup"><span data-stu-id="b29bb-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="b29bb-114">Skriv eller vælg en værdi i feltet Nummerseriekode.</span><span class="sxs-lookup"><span data-stu-id="b29bb-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="b29bb-115">Oprette en kunde</span><span class="sxs-lookup"><span data-stu-id="b29bb-115">Set up a customer</span></span>
1. <span data-ttu-id="b29bb-116">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="b29bb-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b29bb-117">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="b29bb-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b29bb-118">Filtrer f.eks. efter feltet Konto med værdien "DE-015".</span><span class="sxs-lookup"><span data-stu-id="b29bb-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="b29bb-119">Åbn kundens kontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="b29bb-119">Open customer account details.</span></span>
4. <span data-ttu-id="b29bb-120">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b29bb-120">Click Edit.</span></span>
5. <span data-ttu-id="b29bb-121">Udvid sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="b29bb-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="b29bb-122">Vælg Ja i feltet Postcertifikat er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="b29bb-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="b29bb-123">Vælg Ja i feltet Udsted indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="b29bb-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="b29bb-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b29bb-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="b29bb-125">Oprette et EU-posteringscertifikat automatisk</span><span class="sxs-lookup"><span data-stu-id="b29bb-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="b29bb-126">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="b29bb-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="b29bb-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b29bb-127">Click New.</span></span>
3. <span data-ttu-id="b29bb-128">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="b29bb-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="b29bb-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-129">Click OK.</span></span>
5. <span data-ttu-id="b29bb-130">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="b29bb-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="b29bb-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b29bb-131">Click Save.</span></span>
7. <span data-ttu-id="b29bb-132">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="b29bb-133">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="b29bb-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="b29bb-134">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="b29bb-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="b29bb-135">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="b29bb-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="b29bb-136">Fjern markeringen i feltet Udsted indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="b29bb-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="b29bb-137">Et postcertifikat kan udstedes, når følgesedlen bogføres eller under fakturering.</span><span class="sxs-lookup"><span data-stu-id="b29bb-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="b29bb-138">Lad afkrydsningsfeltet Udsted indførselscertifikat være umarkeret for at udstede det senere.</span><span class="sxs-lookup"><span data-stu-id="b29bb-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="b29bb-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-139">Click OK.</span></span>
13. <span data-ttu-id="b29bb-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-140">Click OK.</span></span>
14. <span data-ttu-id="b29bb-141">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="b29bb-142">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="b29bb-142">Click Invoice.</span></span>
    * <span data-ttu-id="b29bb-143">Kontroller, at afkrydsningsfelterne Postcertifikat er påkrævet og Udsted indførselscertifikat i afsnittet Oversigt.</span><span class="sxs-lookup"><span data-stu-id="b29bb-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="b29bb-144">Du kan også markere afkrydsningsfeltet Udskriv indførselscertifikat for at tillade udskrivning af certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b29bb-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="b29bb-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-145">Click OK.</span></span>
17. <span data-ttu-id="b29bb-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-146">Click OK.</span></span>
18. <span data-ttu-id="b29bb-147">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="b29bb-148">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="b29bb-148">Click Invoice.</span></span>
20. <span data-ttu-id="b29bb-149">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="b29bb-150">Klik på Vis udstedte indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="b29bb-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="b29bb-151">Klik på Udskriv.</span><span class="sxs-lookup"><span data-stu-id="b29bb-151">Click Print.</span></span>
23. <span data-ttu-id="b29bb-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-152">Close the page.</span></span>
24. <span data-ttu-id="b29bb-153">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="b29bb-153">Click Change status.</span></span>
25. <span data-ttu-id="b29bb-154">Vælg en indstilling i feltet Ny status.</span><span class="sxs-lookup"><span data-stu-id="b29bb-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="b29bb-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-155">Click OK.</span></span>
27. <span data-ttu-id="b29bb-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="b29bb-157">Oprette et EU-posteringscertifikat manuelt</span><span class="sxs-lookup"><span data-stu-id="b29bb-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="b29bb-158">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="b29bb-159">Klik på Opret indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="b29bb-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="b29bb-160">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b29bb-160">Click OK.</span></span>
4. <span data-ttu-id="b29bb-161">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b29bb-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="b29bb-162">Klik på Vis udstedte indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="b29bb-162">Click View issued entry certificates.</span></span>


