---
title: Oprette en rentekode med et interval
description: Rentekoder kan konfigureres til at beregne forskellige rentebeløb baseret på et interval af værdier.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d684eedd5b40ee9775ab779c243d05cdc6e01f58
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188849"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="b37be-103">Oprette en rentekode med et interval</span><span class="sxs-lookup"><span data-stu-id="b37be-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b37be-104">Rentekoder kan konfigureres til at beregne forskellige rentebeløb baseret på et interval af værdier.</span><span class="sxs-lookup"><span data-stu-id="b37be-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="b37be-105">Denne procedure viser, hvordan du kan tilføje en rentekode og føje et interval til den.</span><span class="sxs-lookup"><span data-stu-id="b37be-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="b37be-106">Gå til Kredit og inkasso > Rente > Konfigurer rentekoder.</span><span class="sxs-lookup"><span data-stu-id="b37be-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="b37be-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b37be-107">Click New.</span></span>
3. <span data-ttu-id="b37be-108">Angiv navnet på rentekoden i feltet Rentekode.</span><span class="sxs-lookup"><span data-stu-id="b37be-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="b37be-109">Angiv en beskrivelse af rentekoden i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b37be-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="b37be-110">Vælg Måned.</span><span class="sxs-lookup"><span data-stu-id="b37be-110">Select Month.</span></span>
6. <span data-ttu-id="b37be-111">Udvid afsnittet Indtjeninger.</span><span class="sxs-lookup"><span data-stu-id="b37be-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="b37be-112">Udvid sektionen Indtjeninger pr. valuta.</span><span class="sxs-lookup"><span data-stu-id="b37be-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="b37be-113">I feltet Finansbogføringskonto skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="b37be-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="b37be-114">Vælg 'Måneder' i feltet Rente efter interval.</span><span class="sxs-lookup"><span data-stu-id="b37be-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="b37be-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="b37be-115">Click Add.</span></span>
11. <span data-ttu-id="b37be-116">Angiv en beskrivende for denne valuta og dette interval i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b37be-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="b37be-117">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b37be-117">Click Save.</span></span>
13. <span data-ttu-id="b37be-118">Klik på Afgrænsninger.</span><span class="sxs-lookup"><span data-stu-id="b37be-118">Click Ranges.</span></span>
14. <span data-ttu-id="b37be-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b37be-119">Click New.</span></span>
15. <span data-ttu-id="b37be-120">Angiv Fra-værdien som 0, og angiv derefter den renteprocent pr. måned, der skal bruges til at beregne renten.</span><span class="sxs-lookup"><span data-stu-id="b37be-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="b37be-121">I vores eksempel er det 1.5.</span><span class="sxs-lookup"><span data-stu-id="b37be-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="b37be-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b37be-122">Click New.</span></span>
17. <span data-ttu-id="b37be-123">Angiv den næste Fra-værdi som 4, hvilket er den første måned, hvor du skal beregne et nyt rentebeløb.</span><span class="sxs-lookup"><span data-stu-id="b37be-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="b37be-124">Angiv den renteprocent pr. måned, der skal bruges til at beregne renten, der starter i måned 4.</span><span class="sxs-lookup"><span data-stu-id="b37be-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="b37be-125">I vores eksempel er det 2,0.</span><span class="sxs-lookup"><span data-stu-id="b37be-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="b37be-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b37be-126">Click New.</span></span>
20. <span data-ttu-id="b37be-127">Angiv den næste Fra-værdi som 7, hvilket er den næste måned, hvor du skal beregne et nyt rentebeløb.</span><span class="sxs-lookup"><span data-stu-id="b37be-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="b37be-128">Angiv den renteprocent pr. måned, der skal bruges til at beregne renten, der starter i måned 7.</span><span class="sxs-lookup"><span data-stu-id="b37be-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="b37be-129">I vores eksempel er det 2,5.</span><span class="sxs-lookup"><span data-stu-id="b37be-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="b37be-130">Klik på Luk for at afslutte konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b37be-130">Click Close to complete the setup.</span></span>

