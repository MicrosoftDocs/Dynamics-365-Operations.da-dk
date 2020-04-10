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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc4b5c31d9a478a5226ae6b5e8c776de3b661dd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144829"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="71023-103">Oprette momsposteringer på dokumenter</span><span class="sxs-lookup"><span data-stu-id="71023-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71023-104">Moms på dokumenter beregnes ved at angive en momsgruppe og en varemomsgruppe på dokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="71023-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="71023-105">Disse hentes standard fra masterdata, men den kan ændres manuelt, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="71023-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="71023-106">Den beregnede moms kan kontrolleres på linje- og dokumentniveau.</span><span class="sxs-lookup"><span data-stu-id="71023-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="71023-107">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="71023-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="71023-108">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="71023-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="71023-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="71023-109">Click New.</span></span>
3. <span data-ttu-id="71023-110">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="71023-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="71023-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="71023-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="71023-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71023-113">Click OK.</span></span>
7. <span data-ttu-id="71023-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="71023-115">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="71023-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="71023-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="71023-117">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="71023-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="71023-118">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="71023-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="71023-119">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="71023-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="71023-120">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="71023-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="71023-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="71023-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="71023-123">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="71023-123">Click Financials.</span></span>
17. <span data-ttu-id="71023-124">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="71023-124">Click Sales tax.</span></span>
18. <span data-ttu-id="71023-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71023-125">Click OK.</span></span>
19. <span data-ttu-id="71023-126">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="71023-126">Click Add line.</span></span>
20. <span data-ttu-id="71023-127">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="71023-128">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="71023-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="71023-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="71023-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="71023-131">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="71023-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="71023-132">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="71023-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="71023-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="71023-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71023-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="71023-135">Klik på Sælg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="71023-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="71023-136">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="71023-136">Click Sales tax.</span></span>
30. <span data-ttu-id="71023-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71023-137">Click OK.</span></span>

