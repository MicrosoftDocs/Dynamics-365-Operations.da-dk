---
title: Konfigurere politikker for kreditorfakturaer
description: I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441578"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="b8390-103">Konfigurere politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="b8390-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8390-104">I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="b8390-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="b8390-105">Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="b8390-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="b8390-106">Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="b8390-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="b8390-107">Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="b8390-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="b8390-108">Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="b8390-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="b8390-109">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b8390-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="b8390-110">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="b8390-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="b8390-111">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="b8390-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="b8390-112">Forberede oprettelse af politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="b8390-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="b8390-113">Gå til **Navigationsrude > Moduler > Kreditor > Opsætning > Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="b8390-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="b8390-114">Vælg fanen **Fakturavalidering**.</span><span class="sxs-lookup"><span data-stu-id="b8390-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="b8390-115">Markér eller fjern markeringen fra afkrydsningsfeltet **Opdater status for fakturahoved automatisk**.</span><span class="sxs-lookup"><span data-stu-id="b8390-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="b8390-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8390-116">Select **OK**.</span></span>
5. <span data-ttu-id="b8390-117">Vælg en indstilling i feltet **Bogfør faktura med uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="b8390-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="b8390-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b8390-118">Close the page.</span></span>
7. <span data-ttu-id="b8390-119">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="b8390-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="b8390-120">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="b8390-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="b8390-121">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="b8390-121">Select **Add**.</span></span>
10. <span data-ttu-id="b8390-122">Luk siden for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="b8390-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="b8390-123">Oprette politikregeltyper for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="b8390-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="b8390-124">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Regeltyper for kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="b8390-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="b8390-125">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b8390-125">Select **New**.</span></span>
3. <span data-ttu-id="b8390-126">Angiv værdier i felterne **Regelnavn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b8390-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="b8390-127">I feltet **Forespørgselsnavn** skal du vælge rullelisten for at åbne opslaget, og derefter vælge den ønskede post.</span><span class="sxs-lookup"><span data-stu-id="b8390-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="b8390-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b8390-128">Select **Save**.</span></span>
6. <span data-ttu-id="b8390-129">Luk siden for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="b8390-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="b8390-130">Definere en politik for kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="b8390-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="b8390-131">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="b8390-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="b8390-132">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b8390-132">Select **New**.</span></span>
3. <span data-ttu-id="b8390-133">Angiv værdier i felterne **Navn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b8390-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="b8390-134">Udvid eller skjul sektionen **Politikorganisationer**.</span><span class="sxs-lookup"><span data-stu-id="b8390-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="b8390-135">Vælg **Contoso Entertainment System USA** i træet.</span><span class="sxs-lookup"><span data-stu-id="b8390-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="b8390-136">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="b8390-136">Select **Add**.</span></span>
7. <span data-ttu-id="b8390-137">Udvid eller skjul sektionen **Politikregler**.</span><span class="sxs-lookup"><span data-stu-id="b8390-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="b8390-138">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="b8390-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="b8390-139">Skriv en værdi i feltet **Beskrivelse af politikregel**.</span><span class="sxs-lookup"><span data-stu-id="b8390-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="b8390-140">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b8390-140">Select **Filter**.</span></span>
11. <span data-ttu-id="b8390-141">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="b8390-141">Select **Add**.</span></span> <span data-ttu-id="b8390-142">Vælg den ønskede post.</span><span class="sxs-lookup"><span data-stu-id="b8390-142">Select the desired record.</span></span>
12. <span data-ttu-id="b8390-143">Vælg eller angiv indstillingerne fra rullemenuerne i felterne **Afledt tabel** og **Felt** i **Afledt tabel**.</span><span class="sxs-lookup"><span data-stu-id="b8390-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="b8390-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b8390-144">Close the page.</span></span>
14. <span data-ttu-id="b8390-145">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="b8390-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="b8390-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8390-146">Select **OK**.</span></span>
16. <span data-ttu-id="b8390-147">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8390-147">Select **OK**.</span></span>
17. <span data-ttu-id="b8390-148">Luk siderne for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="b8390-148">Close the pages to return to the home page.</span></span>

