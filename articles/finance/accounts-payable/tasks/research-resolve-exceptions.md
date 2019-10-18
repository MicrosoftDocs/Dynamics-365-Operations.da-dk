---
title: Undersøg/løs undtagelser
description: Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2f2e7d401e97aeab9dbc74f65e1a0c03eb0c880
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189332"
---
# <a name="researchresolve-exceptions"></a><span data-ttu-id="0d630-103">Undersøg/løs undtagelser</span><span class="sxs-lookup"><span data-stu-id="0d630-103">Research/Resolve exceptions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d630-104">Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="0d630-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="0d630-105">Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="0d630-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="0d630-106">Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="0d630-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="0d630-107">Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="0d630-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="0d630-108">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="0d630-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="0d630-109">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="0d630-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="0d630-110">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="0d630-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="0d630-111">Forberede oprettelse af politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="0d630-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="0d630-112">Gå til Kreditor > Opsætning > Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="0d630-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="0d630-113">Klik på fanen Fakturavalidering.</span><span class="sxs-lookup"><span data-stu-id="0d630-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="0d630-114">Markér eller fjern markeringen af afkrydsningsfeltet Opdater status for fakturahoved automatisk.</span><span class="sxs-lookup"><span data-stu-id="0d630-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="0d630-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d630-115">Click OK.</span></span>
5. <span data-ttu-id="0d630-116">Vælg en indstilling i feltet Bogfør faktura med uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="0d630-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="0d630-117">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-117">Close the page.</span></span>
7. <span data-ttu-id="0d630-118">Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0d630-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="0d630-119">Klik på Parametre.</span><span class="sxs-lookup"><span data-stu-id="0d630-119">Click Parameters.</span></span>
9. <span data-ttu-id="0d630-120">Klik på btnAdd.</span><span class="sxs-lookup"><span data-stu-id="0d630-120">Click btnAdd.</span></span>
10. <span data-ttu-id="0d630-121">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="0d630-122">Oprette politikregeltyper for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="0d630-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="0d630-123">Gå til Kreditor > Konfiguration af politik > Regeltyper til politik for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0d630-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="0d630-124">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0d630-124">Click New.</span></span>
3. <span data-ttu-id="0d630-125">Skriv en værdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="0d630-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="0d630-126">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0d630-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0d630-127">Klik på rullelisten i feltet Forespørgselsnavn for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0d630-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0d630-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0d630-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0d630-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d630-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0d630-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d630-130">Click Save.</span></span>
9. <span data-ttu-id="0d630-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="0d630-132">Definere en politik for kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="0d630-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="0d630-133">Gå til Kreditor > Konfiguration af politik > Politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0d630-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="0d630-134">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0d630-134">Click New.</span></span>
3. <span data-ttu-id="0d630-135">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d630-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0d630-136">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0d630-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0d630-137">Udvid eller skjul sektionen Politikorganisationer.</span><span class="sxs-lookup"><span data-stu-id="0d630-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="0d630-138">Vælg "Contoso Entertainment System USA" i træet.</span><span class="sxs-lookup"><span data-stu-id="0d630-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="0d630-139">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d630-139">Click Add.</span></span>
8. <span data-ttu-id="0d630-140">Udvid eller skjul sektionen Politikregler.</span><span class="sxs-lookup"><span data-stu-id="0d630-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="0d630-141">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="0d630-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="0d630-142">Skriv en værdi i feltet Beskrivelse af politikregel.</span><span class="sxs-lookup"><span data-stu-id="0d630-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="0d630-143">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="0d630-143">Click Filter.</span></span>
12. <span data-ttu-id="0d630-144">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="0d630-144">Click Add.</span></span>
13. <span data-ttu-id="0d630-145">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d630-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0d630-146">Klik på rullelisten i feltet Tabel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0d630-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0d630-147">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d630-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0d630-148">Klik på rullelisten i feltet Afledt tabel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0d630-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="0d630-149">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0d630-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="0d630-150">Klik på rullelisten i feltet Felt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="0d630-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0d630-151">Skriv en værdi i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="0d630-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="0d630-152">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-152">Close the page.</span></span>
21. <span data-ttu-id="0d630-153">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="0d630-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="0d630-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d630-154">Click OK.</span></span>
23. <span data-ttu-id="0d630-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d630-155">Click OK.</span></span>
24. <span data-ttu-id="0d630-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-156">Close the page.</span></span>
25. <span data-ttu-id="0d630-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d630-157">Close the page.</span></span>

