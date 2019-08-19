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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ec0db1bc5018649acaca05c71a510880b415777
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846673"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="198f9-103">Oprette avancerede regler for kladder</span><span class="sxs-lookup"><span data-stu-id="198f9-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="198f9-104">Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.</span><span class="sxs-lookup"><span data-stu-id="198f9-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="198f9-105">Dette omfatter opsætning af kladdekontrol og brugerbogføringsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="198f9-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="198f9-106">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="198f9-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="198f9-107">Opsæt kladdekontrol.</span><span class="sxs-lookup"><span data-stu-id="198f9-107">Set up journal control</span></span>
1. <span data-ttu-id="198f9-108">Gå til Finans > Kladdeopsætning > Kladdenavne.</span><span class="sxs-lookup"><span data-stu-id="198f9-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="198f9-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="198f9-110">Klik på Kladdekontrol.</span><span class="sxs-lookup"><span data-stu-id="198f9-110">Click Journal control.</span></span>
4. <span data-ttu-id="198f9-111">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="198f9-111">Click Add.</span></span>
5. <span data-ttu-id="198f9-112">Klik på rullelisten i feltet Regnskaber for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="198f9-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="198f9-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="198f9-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="198f9-115">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="198f9-115">Click Add.</span></span>
9. <span data-ttu-id="198f9-116">Klik på rullelisten i feltet Kontostruktur for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="198f9-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="198f9-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="198f9-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="198f9-119">Klik på rullelisten i feltet Segment for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="198f9-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="198f9-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="198f9-121">Klik på rullelisten i feltet Fra-værdi for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="198f9-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="198f9-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="198f9-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="198f9-124">Klik på rullelisten i feltet Til-værdi for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="198f9-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="198f9-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="198f9-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="198f9-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="198f9-127">Angive bogføringsbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="198f9-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="198f9-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="198f9-128">Close the page.</span></span>
2. <span data-ttu-id="198f9-129">Klik på Bogføringsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="198f9-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="198f9-130">Vælg Pr. brugergruppe i Hvordan vil du indstille bogføringsbegrænsninger?.</span><span class="sxs-lookup"><span data-stu-id="198f9-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="198f9-131">Markér 'den gruppe, du vil tillade bogføring af dette kladdenavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="198f9-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="198f9-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="198f9-132">Click OK.</span></span>

