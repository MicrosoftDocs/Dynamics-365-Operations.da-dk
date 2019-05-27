---
title: Oprette et foreløbigt budget til den offentlige sektor
description: Du kan oprette foreløbige budgetregisterposteringer for en specifik budgetmodel og dimensionsværdier.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98968b0025ff5c3b9723dc6cc8a8eae799a4eb43
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557182"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="70bf1-103">Oprette et foreløbigt budget til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="70bf1-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70bf1-104">Du kan oprette foreløbige budgetregisterposteringer for en specifik budgetmodel og dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="70bf1-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="70bf1-105">Når det faktiske budget er godkendt, kan du oprette oprindelige budgetregisterposter.</span><span class="sxs-lookup"><span data-stu-id="70bf1-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="70bf1-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="70bf1-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="70bf1-107">Gå til Budgettering > Budgetregisterposter.</span><span class="sxs-lookup"><span data-stu-id="70bf1-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="70bf1-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="70bf1-108">Click New.</span></span>
3. <span data-ttu-id="70bf1-109">Klik på rullelisten i feltet Budgetmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="70bf1-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="70bf1-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70bf1-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="70bf1-111">Klik på rullelisten i feltet Budgetkode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="70bf1-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="70bf1-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70bf1-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="70bf1-113">Klik på rullelisten i feltet Årsagskode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="70bf1-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="70bf1-114">Klik på den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70bf1-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="70bf1-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="70bf1-115">Click Save.</span></span>
10. <span data-ttu-id="70bf1-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="70bf1-116">Click Add line.</span></span>
    * <span data-ttu-id="70bf1-117">Valgfrit: Angiv en ny dato, hvis du vil ændre datoen i forhold til den i overskriften.</span><span class="sxs-lookup"><span data-stu-id="70bf1-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="70bf1-118">Datoen bestemmer den regnskabsperiode, som budgettet registreres for.</span><span class="sxs-lookup"><span data-stu-id="70bf1-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="70bf1-119">Hvis du vil udfylde andre felter, skal du klikke på Lås øverst på siden, mens opgaveguiden er åben.</span><span class="sxs-lookup"><span data-stu-id="70bf1-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="70bf1-120">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="70bf1-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="70bf1-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70bf1-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="70bf1-122">I feltet Dimensionsværdier skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="70bf1-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="70bf1-123">Angiv et tal i feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="70bf1-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="70bf1-124">Du kan også angive en beløbstype.</span><span class="sxs-lookup"><span data-stu-id="70bf1-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="70bf1-125">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="70bf1-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="70bf1-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="70bf1-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="70bf1-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="70bf1-127">Click Save.</span></span>
18. <span data-ttu-id="70bf1-128">Klik på Opdater budgetsaldi.</span><span class="sxs-lookup"><span data-stu-id="70bf1-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="70bf1-129">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="70bf1-129">Click Update.</span></span>
    * <span data-ttu-id="70bf1-130">Hvis du vil se resultaterne af opdateringen, skal du klikke på Meddelelsesdetaljer på den blå linje.</span><span class="sxs-lookup"><span data-stu-id="70bf1-130">To see the results of the update, click Message details on the blue bar.</span></span>  

