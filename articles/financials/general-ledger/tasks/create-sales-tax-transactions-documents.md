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
ms.openlocfilehash: 653b93744f5b891655cade0cb669d34179fca9cd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846529"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="95432-103">Oprette momsposteringer på dokumenter</span><span class="sxs-lookup"><span data-stu-id="95432-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95432-104">Moms på dokumenter beregnes ved at angive en momsgruppe og en varemomsgruppe på dokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="95432-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="95432-105">Disse hentes standard fra masterdata, men den kan ændres manuelt, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="95432-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="95432-106">Den beregnede moms kan kontrolleres på linje- og dokumentniveau.</span><span class="sxs-lookup"><span data-stu-id="95432-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="95432-107">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="95432-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="95432-108">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="95432-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="95432-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="95432-109">Click New.</span></span>
3. <span data-ttu-id="95432-110">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95432-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="95432-111">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="95432-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="95432-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="95432-113">Click OK.</span></span>
7. <span data-ttu-id="95432-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="95432-115">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95432-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="95432-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="95432-117">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="95432-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="95432-118">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="95432-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="95432-119">Klik på fanen Opsætning.</span><span class="sxs-lookup"><span data-stu-id="95432-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="95432-120">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95432-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="95432-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="95432-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="95432-123">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="95432-123">Click Financials.</span></span>
17. <span data-ttu-id="95432-124">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="95432-124">Click Sales tax.</span></span>
18. <span data-ttu-id="95432-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="95432-125">Click OK.</span></span>
19. <span data-ttu-id="95432-126">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="95432-126">Click Add line.</span></span>
20. <span data-ttu-id="95432-127">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="95432-128">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95432-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="95432-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="95432-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="95432-131">Angiv et nummer i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="95432-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="95432-132">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="95432-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="95432-133">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="95432-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="95432-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="95432-135">Klik på Sælg i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="95432-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="95432-136">Klik på Moms.</span><span class="sxs-lookup"><span data-stu-id="95432-136">Click Sales tax.</span></span>
30. <span data-ttu-id="95432-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="95432-137">Click OK.</span></span>

