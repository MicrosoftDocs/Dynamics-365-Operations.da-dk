---
title: Opdele et anlægsaktiv
description: Denne opgaveguide opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566886"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="55ccb-103">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="55ccb-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55ccb-104">Denne opgaveguide opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="55ccb-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="55ccb-105">Den bruger rollen Revisor og USMF demodata.</span><span class="sxs-lookup"><span data-stu-id="55ccb-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="55ccb-106">Opret et nyt anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="55ccb-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="55ccb-107">Gå til Anlægsaktiver > Anlægsaktiver > Anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="55ccb-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="55ccb-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="55ccb-108">Click New.</span></span>
3. <span data-ttu-id="55ccb-109">Skriv eller vælg en værdi i feltet Anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="55ccb-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="55ccb-110">Bemærk nummeret på anlægsaktivet til senere brug i opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="55ccb-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="55ccb-111">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="55ccb-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="55ccb-112">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="55ccb-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="55ccb-113">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="55ccb-113">Split a fixed asset</span></span>
1. <span data-ttu-id="55ccb-114">På listen skal du finde og vælge det anlægsaktiv, der skal opdeles.</span><span class="sxs-lookup"><span data-stu-id="55ccb-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="55ccb-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="55ccb-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="55ccb-116">Klik på Bøger.</span><span class="sxs-lookup"><span data-stu-id="55ccb-116">Click Books.</span></span>
    * <span data-ttu-id="55ccb-117">Vælg det kartotek, der skal opdeles til det nye aktiv.</span><span class="sxs-lookup"><span data-stu-id="55ccb-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="55ccb-118">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="55ccb-118">Click Functions.</span></span>
5. <span data-ttu-id="55ccb-119">Klik på Opdel anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="55ccb-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="55ccb-120">Skriv eller vælg en værdi i feltet Til anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="55ccb-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="55ccb-121">Klik på rullelisten i feltet Til bog for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="55ccb-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="55ccb-122">Angiv en dato i feltet Transaktionsdato.</span><span class="sxs-lookup"><span data-stu-id="55ccb-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="55ccb-123">Angiv et tal i feltet Procent.</span><span class="sxs-lookup"><span data-stu-id="55ccb-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="55ccb-124">Indtast eller vælg en værdi i feltet Kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="55ccb-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="55ccb-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55ccb-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="55ccb-126">Bogfør kladdeposteringen</span><span class="sxs-lookup"><span data-stu-id="55ccb-126">Post the journal transaction</span></span>
1. <span data-ttu-id="55ccb-127">Gå til Anlægsaktiver > Kladdepostering > Anlægsaktivkladde.</span><span class="sxs-lookup"><span data-stu-id="55ccb-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="55ccb-128">Vælg på listen den kladde, der er oprettet med opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="55ccb-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="55ccb-129">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="55ccb-129">Click Lines.</span></span>
    * <span data-ttu-id="55ccb-130">Bekræft de oprettede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="55ccb-130">Verify the journal lines created.</span></span>  <span data-ttu-id="55ccb-131">Der oprettes en postering til anskaffelsesregulering for det oprindelige aktiv for at formindske værdien af den procentdel, der er angivet under opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="55ccb-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="55ccb-132">Der oprettes en anskaffelsespostering for det nye aktiv for det samme beløb.</span><span class="sxs-lookup"><span data-stu-id="55ccb-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="55ccb-133">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="55ccb-133">Click Post.</span></span>

