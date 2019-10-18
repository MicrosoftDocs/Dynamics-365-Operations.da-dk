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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800b7009f023bd2a0d8437b81d82c0e9de770841
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174368"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="35724-103">Oprette et foreløbigt budget til den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="35724-103">Create a preliminary budget for Public sector</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35724-104">Du kan oprette foreløbige budgetregisterposteringer for en specifik budgetmodel og dimensionsværdier.</span><span class="sxs-lookup"><span data-stu-id="35724-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="35724-105">Når det faktiske budget er godkendt, kan du oprette oprindelige budgetregisterposter.</span><span class="sxs-lookup"><span data-stu-id="35724-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="35724-106">Denne procedure er oprettet med PSUS-demodatafirmaet i den offentlige sektor partition.</span><span class="sxs-lookup"><span data-stu-id="35724-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="35724-107">Gå til Budgettering > Budgetregisterposter.</span><span class="sxs-lookup"><span data-stu-id="35724-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="35724-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="35724-108">Click New.</span></span>
3. <span data-ttu-id="35724-109">Klik på rullelisten i feltet Budgetmodel for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35724-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="35724-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35724-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="35724-111">Klik på rullelisten i feltet Budgetkode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35724-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="35724-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35724-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="35724-113">Klik på rullelisten i feltet Årsagskode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35724-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="35724-114">Klik på den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35724-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="35724-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="35724-115">Click Save.</span></span>
10. <span data-ttu-id="35724-116">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="35724-116">Click Add line.</span></span>
    * <span data-ttu-id="35724-117">Valgfrit: Angiv en ny dato, hvis du vil ændre datoen i forhold til den i overskriften.</span><span class="sxs-lookup"><span data-stu-id="35724-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="35724-118">Datoen bestemmer den regnskabsperiode, som budgettet registreres for.</span><span class="sxs-lookup"><span data-stu-id="35724-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="35724-119">Hvis du vil udfylde andre felter, skal du klikke på Lås øverst på siden, mens opgaveguiden er åben.</span><span class="sxs-lookup"><span data-stu-id="35724-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="35724-120">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35724-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="35724-121">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35724-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="35724-122">I feltet Dimensionsværdier skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="35724-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="35724-123">Angiv et tal i feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="35724-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="35724-124">Du kan også angive en beløbstype.</span><span class="sxs-lookup"><span data-stu-id="35724-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="35724-125">Klik på rullelisten i feltet Valuta for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="35724-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="35724-126">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="35724-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="35724-127">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="35724-127">Click Save.</span></span>
18. <span data-ttu-id="35724-128">Klik på Opdater budgetsaldi.</span><span class="sxs-lookup"><span data-stu-id="35724-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="35724-129">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="35724-129">Click Update.</span></span>
    * <span data-ttu-id="35724-130">Hvis du vil se resultaterne af opdateringen, skal du klikke på Meddelelsesdetaljer på den blå linje.</span><span class="sxs-lookup"><span data-stu-id="35724-130">To see the results of the update, click Message details on the blue bar.</span></span>  

