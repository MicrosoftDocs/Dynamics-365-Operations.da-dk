---
title: Konfigurere politikker for kreditorfakturaer
description: I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer.
author: ShivamPandey-msft
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c088f6e3fea7c218cfd2108d0f279bccf1292772
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816190"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="84a02-103">Konfigurere politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="84a02-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84a02-104">I dette emne forklares, hvordan du konfigurerer politikker for kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="84a02-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="84a02-105">Du kan køre kreditorfakturapolitikker, når du bogfører en kreditorfaktura ved hjælp af siden Kreditorfaktura, og når du åbner siden Overtrædelser af politik til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="84a02-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="84a02-106">Du kan også konfigurere arbejdsgangen for kreditorfakturaer til at køre politikker for kreditorfakturaer, hver gang du sender en faktura videre i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="84a02-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="84a02-107">Kreditorfakturapolitikker gælder ikke for fakturaer, der er oprettet i indgangsbogen eller i fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="84a02-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="84a02-108">Kreditorfakturapolitikker benyttes ikke til validering af fakturasammenholdelse, men er i stedet konfigureret på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="84a02-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="84a02-109">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="84a02-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="84a02-110">Rollen kreditorchef eller rollen regnskabschef skal udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="84a02-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="84a02-111">Inden du begynder, skal du kontrollere, at konfigurationsnøglen til fakturasammenholdelse er valgt.</span><span class="sxs-lookup"><span data-stu-id="84a02-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="84a02-112">Forberede oprettelse af politikker for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="84a02-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="84a02-113">Gå til **Navigationsrude > Moduler > Kreditor > Opsætning > Kreditorparametre**.</span><span class="sxs-lookup"><span data-stu-id="84a02-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="84a02-114">Vælg fanen **Fakturavalidering**.</span><span class="sxs-lookup"><span data-stu-id="84a02-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="84a02-115">Markér eller fjern markeringen fra afkrydsningsfeltet **Opdater status for fakturahoved automatisk**.</span><span class="sxs-lookup"><span data-stu-id="84a02-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="84a02-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="84a02-116">Select **OK**.</span></span>
5. <span data-ttu-id="84a02-117">Vælg en indstilling i feltet **Bogfør faktura med uoverensstemmelser**.</span><span class="sxs-lookup"><span data-stu-id="84a02-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="84a02-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84a02-118">Close the page.</span></span>
7. <span data-ttu-id="84a02-119">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="84a02-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="84a02-120">Vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="84a02-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="84a02-121">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84a02-121">Select **Add**.</span></span>
10. <span data-ttu-id="84a02-122">Luk siden for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="84a02-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="84a02-123">Oprette politikregeltyper for kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="84a02-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="84a02-124">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Regeltyper for kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="84a02-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="84a02-125">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="84a02-125">Select **New**.</span></span>
3. <span data-ttu-id="84a02-126">Angiv værdier i felterne **Regelnavn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="84a02-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="84a02-127">I feltet **Forespørgselsnavn** skal du vælge rullelisten for at åbne opslaget, og derefter vælge den ønskede post.</span><span class="sxs-lookup"><span data-stu-id="84a02-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="84a02-128">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="84a02-128">Select **Save**.</span></span>
6. <span data-ttu-id="84a02-129">Luk siden for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="84a02-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="84a02-130">Definere en politik for kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="84a02-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="84a02-131">Gå til **Navigationsrude > Moduler > Kreditorer > Politikopsætning > Kreditorfakturapolitikker**.</span><span class="sxs-lookup"><span data-stu-id="84a02-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="84a02-132">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="84a02-132">Select **New**.</span></span>
3. <span data-ttu-id="84a02-133">Angiv værdier i felterne **Navn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="84a02-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="84a02-134">Udvid eller skjul sektionen **Politikorganisationer**.</span><span class="sxs-lookup"><span data-stu-id="84a02-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="84a02-135">Vælg **Contoso Entertainment System USA** i træet.</span><span class="sxs-lookup"><span data-stu-id="84a02-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="84a02-136">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84a02-136">Select **Add**.</span></span>
7. <span data-ttu-id="84a02-137">Udvid eller skjul sektionen **Politikregler**.</span><span class="sxs-lookup"><span data-stu-id="84a02-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="84a02-138">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="84a02-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="84a02-139">Skriv en værdi i feltet **Beskrivelse af politikregel**.</span><span class="sxs-lookup"><span data-stu-id="84a02-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="84a02-140">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="84a02-140">Select **Filter**.</span></span>
11. <span data-ttu-id="84a02-141">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84a02-141">Select **Add**.</span></span> <span data-ttu-id="84a02-142">Vælg den ønskede post.</span><span class="sxs-lookup"><span data-stu-id="84a02-142">Select the desired record.</span></span>
12. <span data-ttu-id="84a02-143">Vælg eller angiv indstillingerne fra rullemenuerne i felterne **Afledt tabel** og **Felt** i **Afledt tabel**.</span><span class="sxs-lookup"><span data-stu-id="84a02-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="84a02-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84a02-144">Close the page.</span></span>
14. <span data-ttu-id="84a02-145">Skriv en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="84a02-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="84a02-146">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="84a02-146">Select **OK**.</span></span>
16. <span data-ttu-id="84a02-147">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="84a02-147">Select **OK**.</span></span>
17. <span data-ttu-id="84a02-148">Luk siderne for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="84a02-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]