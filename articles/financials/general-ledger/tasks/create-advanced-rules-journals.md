---
title: Oprette avancerede regler for kladder
description: Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553101"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="fdeb4-103">Oprette avancerede regler for kladder</span><span class="sxs-lookup"><span data-stu-id="fdeb4-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fdeb4-104">Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="fdeb4-105">Dette omfatter opsætning af kladdekontrol og brugerbogføringsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="fdeb4-106">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="fdeb4-107">Opsæt kladdekontrol.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-107">Set up journal control</span></span>
1. <span data-ttu-id="fdeb4-108">Gå til Finans > Kladdeopsætning > Kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="fdeb4-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fdeb4-110">Klik på Kladdekontrol.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-110">Click Journal control.</span></span>
4. <span data-ttu-id="fdeb4-111">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-111">Click Add.</span></span>
5. <span data-ttu-id="fdeb4-112">Klik på rullelisten i feltet Regnskaber for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fdeb4-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fdeb4-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fdeb4-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-115">Click Add.</span></span>
9. <span data-ttu-id="fdeb4-116">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fdeb4-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="fdeb4-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="fdeb4-119">Klik på rullelisten i feltet Segment for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="fdeb4-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="fdeb4-121">Klik på rullelisten i feltet Fra-værdi for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="fdeb4-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="fdeb4-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="fdeb4-124">Klik på rullelisten i feltet Til-værdi for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="fdeb4-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="fdeb4-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="fdeb4-127">Angive bogføringsbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="fdeb4-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="fdeb4-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-128">Close the page.</span></span>
2. <span data-ttu-id="fdeb4-129">Klik på Bogføringsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="fdeb4-130">Vælg Pr. brugergruppe i Hvordan vil du indstille bogføringsbegrænsninger?.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="fdeb4-131">Markér 'den gruppe, du vil tillade bogføring af dette kladdenavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="fdeb4-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fdeb4-132">Click OK.</span></span>

