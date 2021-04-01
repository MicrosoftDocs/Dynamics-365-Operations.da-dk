---
title: Oprette momsposteringer på dokumenter
description: Moms på dokumenter beregnes ved at angive en momsgruppe og en varemomsgruppe på dokumentlinjer.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc70915902863d85aa75af7f4c03e5b83c7cb22
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240804"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="53c44-103">Oprette momsposteringer på dokumenter</span><span class="sxs-lookup"><span data-stu-id="53c44-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53c44-104">Moms på dokumenter beregnes ved at angive en momsgruppe og en varemomsgruppe på dokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="53c44-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="53c44-105">Disse hentes standard fra masterdata, men den kan ændres manuelt, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="53c44-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="53c44-106">Den beregnede moms kan kontrolleres på linje- og dokumentniveau.</span><span class="sxs-lookup"><span data-stu-id="53c44-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="53c44-107">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="53c44-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="53c44-108">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="53c44-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="53c44-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="53c44-109">Click New.</span></span>
3. <span data-ttu-id="53c44-110">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53c44-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="53c44-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="53c44-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="53c44-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="53c44-113">Click OK.</span></span>
7. <span data-ttu-id="53c44-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="53c44-115">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53c44-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="53c44-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="53c44-117">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="53c44-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="53c44-118">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="53c44-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="53c44-119">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="53c44-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="53c44-120">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53c44-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="53c44-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="53c44-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="53c44-123">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="53c44-123">Click Financials.</span></span>
17. <span data-ttu-id="53c44-124">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="53c44-124">Click Sales tax.</span></span>
18. <span data-ttu-id="53c44-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="53c44-125">Click OK.</span></span>
19. <span data-ttu-id="53c44-126">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="53c44-126">Click Add line.</span></span>
20. <span data-ttu-id="53c44-127">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="53c44-128">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53c44-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="53c44-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="53c44-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="53c44-131">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="53c44-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="53c44-132">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="53c44-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="53c44-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="53c44-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="53c44-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="53c44-135">Klik på Sælg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="53c44-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="53c44-136">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="53c44-136">Click Sales tax.</span></span>
30. <span data-ttu-id="53c44-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="53c44-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]