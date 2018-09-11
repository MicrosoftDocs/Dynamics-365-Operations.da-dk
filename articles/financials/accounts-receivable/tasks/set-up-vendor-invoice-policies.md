--- 
title: Konfigurer politikker for kreditorfakturaer
description: "Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a15d3a15a96c498cb2214db2ad2c5d2b61446480
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="9b5be-103">Konfigurer politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="9b5be-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b5be-104">Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="9b5be-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="9b5be-105">Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="9b5be-106">Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="9b5be-107">Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="9b5be-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="9b5be-108">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9b5be-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="9b5be-109">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b5be-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="9b5be-110">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="9b5be-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="9b5be-111">Forberede oprettelse af politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="9b5be-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="9b5be-112">Gå til Kreditor > Opsætning > Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="9b5be-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="9b5be-113">Klik på fanen Fakturavalidering.</span><span class="sxs-lookup"><span data-stu-id="9b5be-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="9b5be-114">Markér eller fjern markeringen af afkrydsningsfeltet Opdater status for fakturahoved automatisk.</span><span class="sxs-lookup"><span data-stu-id="9b5be-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="9b5be-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9b5be-115">Click OK.</span></span>
5. <span data-ttu-id="9b5be-116">Vælg en indstilling i feltet Bogfør faktura med uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="9b5be-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="9b5be-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-117">Close the page.</span></span>
7. <span data-ttu-id="9b5be-118">Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="9b5be-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="9b5be-119">Klik på Parametre.</span><span class="sxs-lookup"><span data-stu-id="9b5be-119">Click Parameters.</span></span>
9. <span data-ttu-id="9b5be-120">Klik på btnAdd.</span><span class="sxs-lookup"><span data-stu-id="9b5be-120">Click btnAdd.</span></span>
10. <span data-ttu-id="9b5be-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="9b5be-122">Oprette politikregeltyper for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="9b5be-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="9b5be-123">Gå til Kreditor > Konfiguration af politik > Regeltyper til politik for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="9b5be-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="9b5be-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9b5be-124">Click New.</span></span>
3. <span data-ttu-id="9b5be-125">Skriv en værdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="9b5be-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="9b5be-126">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9b5be-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b5be-127">Klik på rullelisten i feltet Forespørgselsnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9b5be-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b5be-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b5be-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b5be-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9b5be-130">Click Save.</span></span>
9. <span data-ttu-id="9b5be-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="9b5be-132">Definere en politik for kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="9b5be-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="9b5be-133">Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="9b5be-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="9b5be-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9b5be-134">Click New.</span></span>
3. <span data-ttu-id="9b5be-135">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9b5be-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9b5be-136">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="9b5be-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b5be-137">Udvid eller skjul sektionen Politikorganisationer.</span><span class="sxs-lookup"><span data-stu-id="9b5be-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="9b5be-138">Vælg "Contoso Entertainment System USA" i træet.</span><span class="sxs-lookup"><span data-stu-id="9b5be-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="9b5be-139">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9b5be-139">Click Add.</span></span>
8. <span data-ttu-id="9b5be-140">Udvid eller skjul sektionen Politikregler.</span><span class="sxs-lookup"><span data-stu-id="9b5be-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="9b5be-141">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="9b5be-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="9b5be-142">Skriv en værdi i feltet Beskrivelse af politikregel.</span><span class="sxs-lookup"><span data-stu-id="9b5be-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="9b5be-143">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="9b5be-143">Click Filter.</span></span>
12. <span data-ttu-id="9b5be-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="9b5be-144">Click Add.</span></span>
13. <span data-ttu-id="9b5be-145">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9b5be-146">Klik på rullelisten i feltet Tabel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9b5be-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="9b5be-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="9b5be-148">Klik på rullelisten i feltet Afledt tabel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9b5be-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9b5be-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9b5be-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9b5be-150">Klik på rullelisten i feltet Felt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9b5be-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="9b5be-151">Skriv en værdi i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="9b5be-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="9b5be-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-152">Close the page.</span></span>
21. <span data-ttu-id="9b5be-153">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="9b5be-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="9b5be-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9b5be-154">Click OK.</span></span>
23. <span data-ttu-id="9b5be-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9b5be-155">Click OK.</span></span>
24. <span data-ttu-id="9b5be-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-156">Close the page.</span></span>
25. <span data-ttu-id="9b5be-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9b5be-157">Close the page.</span></span>


