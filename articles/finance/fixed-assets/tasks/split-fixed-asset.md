---
title: Opdele et anlægsaktiv
description: I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176944"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="99335-103">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="99335-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99335-104">I dette emne beskrives, hvordan du opdeler en procentdel af et anlægskartotek til et nyt anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="99335-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="99335-105">Den bruger rollen Revisor og USMF demodata.</span><span class="sxs-lookup"><span data-stu-id="99335-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="99335-106">Opret et nyt anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="99335-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="99335-107">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="99335-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="99335-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="99335-108">Select **New**.</span></span>
3. <span data-ttu-id="99335-109">Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="99335-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="99335-110">Bemærk nummeret på anlægsaktivet til senere brug i opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="99335-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="99335-111">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="99335-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="99335-112">Luk formularen.</span><span class="sxs-lookup"><span data-stu-id="99335-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="99335-113">Opdele et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="99335-113">Split a fixed asset</span></span>
1. <span data-ttu-id="99335-114">På listen skal du finde og vælge linket for det anlægsaktiv, der skal opdeles.</span><span class="sxs-lookup"><span data-stu-id="99335-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="99335-115">Vælg **Bøger**.</span><span class="sxs-lookup"><span data-stu-id="99335-115">Select **Books**.</span></span> <span data-ttu-id="99335-116">Vælg det kartotek, der skal opdeles til det nye aktiv.</span><span class="sxs-lookup"><span data-stu-id="99335-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="99335-117">Vælg **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="99335-117">Select **Functions**.</span></span>
4. <span data-ttu-id="99335-118">Vælg **Opdel anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="99335-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="99335-119">Skriv eller vælg en værdi i feltet **Til anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="99335-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="99335-120">Vælg rullelisteknappen i feltet **Til bog** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="99335-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="99335-121">Angiv en dato i feltet **Transaktionsdato**.</span><span class="sxs-lookup"><span data-stu-id="99335-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="99335-122">Angiv et tal i feltet **Procent**.</span><span class="sxs-lookup"><span data-stu-id="99335-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="99335-123">Indtast eller vælg en værdi i feltet **Kladdenavn**.</span><span class="sxs-lookup"><span data-stu-id="99335-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="99335-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="99335-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="99335-125">Bogfør kladdeposteringen</span><span class="sxs-lookup"><span data-stu-id="99335-125">Post the journal transaction</span></span>
1. <span data-ttu-id="99335-126">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="99335-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="99335-127">Vælg på listen den kladde, der er oprettet med opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="99335-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="99335-128">Vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="99335-128">Select **Lines**.</span></span>

    - <span data-ttu-id="99335-129">Bekræft de oprettede kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="99335-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="99335-130">Der oprettes en postering til anskaffelsesregulering for det oprindelige aktiv for at formindske værdien af den procentdel, der er angivet under opdelingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="99335-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="99335-131">Der oprettes en anskaffelsespostering for det nye aktiv for det samme beløb.</span><span class="sxs-lookup"><span data-stu-id="99335-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="99335-132">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="99335-132">Select **Post**.</span></span>

