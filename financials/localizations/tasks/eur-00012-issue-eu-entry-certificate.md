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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ff00ff0df3835ee2cbf21219ad6f07bfeba6e7ac
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="issue-an-eu-entry-certificate"></a><span data-ttu-id="78555-103">Udstede et EU-indførselscertifikat</span><span class="sxs-lookup"><span data-stu-id="78555-103">Issue an EU entry certificate</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78555-104">Denne procedure fører dig gennem aktivering af et EU-posteringscertifikat og konfiguration af en debitorkonto for at bruge indførselscertifikater og udstede et certifikat.</span><span class="sxs-lookup"><span data-stu-id="78555-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="78555-105">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="78555-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="78555-106">Aktivér administration af indførselscertifikater</span><span class="sxs-lookup"><span data-stu-id="78555-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="78555-107">Gå til Debitor > Opsætning > Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="78555-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="78555-108">Klik på fanen Forsendelser.</span><span class="sxs-lookup"><span data-stu-id="78555-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="78555-109">Udvid sektionen Postcertifikat.</span><span class="sxs-lookup"><span data-stu-id="78555-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="78555-110">Vælg Ja i feltet Aktivér administration af indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="78555-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="78555-111">Vælg Ja i feltet Aktivér udstedelse af indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="78555-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="78555-112">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="78555-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="78555-113">Find og vælg rækken Postcertifikat på listen.</span><span class="sxs-lookup"><span data-stu-id="78555-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="78555-114">Skriv eller vælg en værdi i feltet Nummerseriekode.</span><span class="sxs-lookup"><span data-stu-id="78555-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="78555-115">Oprette en kunde</span><span class="sxs-lookup"><span data-stu-id="78555-115">Set up a customer</span></span>
1. <span data-ttu-id="78555-116">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="78555-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="78555-117">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="78555-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="78555-118">Filtrer f.eks. efter feltet Konto med værdien "DE-015".</span><span class="sxs-lookup"><span data-stu-id="78555-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="78555-119">Åbn kundens kontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="78555-119">Open customer account details.</span></span>
4. <span data-ttu-id="78555-120">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="78555-120">Click Edit.</span></span>
5. <span data-ttu-id="78555-121">Udvid sektionen Faktura og levering.</span><span class="sxs-lookup"><span data-stu-id="78555-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="78555-122">Vælg Ja i feltet Postcertifikat er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="78555-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="78555-123">Vælg Ja i feltet Udsted indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="78555-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="78555-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="78555-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="78555-125">Oprette et EU-posteringscertifikat automatisk</span><span class="sxs-lookup"><span data-stu-id="78555-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="78555-126">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="78555-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="78555-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="78555-127">Click New.</span></span>
3. <span data-ttu-id="78555-128">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="78555-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="78555-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-129">Click OK.</span></span>
5. <span data-ttu-id="78555-130">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="78555-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="78555-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="78555-131">Click Save.</span></span>
7. <span data-ttu-id="78555-132">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="78555-133">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="78555-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="78555-134">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="78555-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="78555-135">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="78555-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="78555-136">Fjern markeringen i feltet Udsted indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="78555-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="78555-137">Et postcertifikat kan udstedes, når følgesedlen bogføres eller under fakturering.</span><span class="sxs-lookup"><span data-stu-id="78555-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="78555-138">Lad afkrydsningsfeltet Udsted indførselscertifikat være umarkeret for at udstede det senere.</span><span class="sxs-lookup"><span data-stu-id="78555-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="78555-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-139">Click OK.</span></span>
13. <span data-ttu-id="78555-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-140">Click OK.</span></span>
14. <span data-ttu-id="78555-141">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="78555-142">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="78555-142">Click Invoice.</span></span>
    * <span data-ttu-id="78555-143">Kontroller, at afkrydsningsfelterne Postcertifikat er påkrævet og Udsted indførselscertifikat i afsnittet Oversigt.</span><span class="sxs-lookup"><span data-stu-id="78555-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="78555-144">Du kan også markere afkrydsningsfeltet Udskriv indførselscertifikat for at tillade udskrivning af certifikatet.</span><span class="sxs-lookup"><span data-stu-id="78555-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="78555-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-145">Click OK.</span></span>
17. <span data-ttu-id="78555-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-146">Click OK.</span></span>
18. <span data-ttu-id="78555-147">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="78555-148">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="78555-148">Click Invoice.</span></span>
20. <span data-ttu-id="78555-149">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="78555-150">Klik på Vis udstedte indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="78555-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="78555-151">Klik på Udskriv.</span><span class="sxs-lookup"><span data-stu-id="78555-151">Click Print.</span></span>
23. <span data-ttu-id="78555-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="78555-152">Close the page.</span></span>
24. <span data-ttu-id="78555-153">Klik på Skift status.</span><span class="sxs-lookup"><span data-stu-id="78555-153">Click Change status.</span></span>
25. <span data-ttu-id="78555-154">Vælg en indstilling i feltet Ny status.</span><span class="sxs-lookup"><span data-stu-id="78555-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="78555-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-155">Click OK.</span></span>
27. <span data-ttu-id="78555-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="78555-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="78555-157">Oprette et EU-posteringscertifikat manuelt</span><span class="sxs-lookup"><span data-stu-id="78555-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="78555-158">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="78555-159">Klik på Opret indførselscertifikat.</span><span class="sxs-lookup"><span data-stu-id="78555-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="78555-160">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="78555-160">Click OK.</span></span>
4. <span data-ttu-id="78555-161">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="78555-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="78555-162">Klik på Vis udstedte indførselscertifikater.</span><span class="sxs-lookup"><span data-stu-id="78555-162">Click View issued entry certificates.</span></span>


