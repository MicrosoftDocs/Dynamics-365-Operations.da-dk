---
title: Oprette avancerede regler for kladder
description: Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145207"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="9d049-103">Oprette avancerede regler for kladder</span><span class="sxs-lookup"><span data-stu-id="9d049-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9d049-104">Denne procedure indeholder en trinvis gennemgang, hvordan du opretter avancerede regler for kladder.</span><span class="sxs-lookup"><span data-stu-id="9d049-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="9d049-105">Dette omfatter opsætning af kladdekontrol og brugerbogføringsbegrænsninger.</span><span class="sxs-lookup"><span data-stu-id="9d049-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="9d049-106">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="9d049-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="9d049-107">Opsæt kladdekontrol.</span><span class="sxs-lookup"><span data-stu-id="9d049-107">Set up journal control</span></span>
1. <span data-ttu-id="9d049-108">Gå i **Navigationsrude** til **Moduler > Finans > Konfiguration af kladde > Kladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="9d049-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="9d049-109">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9d049-110">I **Handlingsruden** skal du klikke på **Kladdekontrol**.</span><span class="sxs-lookup"><span data-stu-id="9d049-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="9d049-111">Klik på **Tilføj** i oversigtspanelet **Hvilke kontotyper kan posteres?**.</span><span class="sxs-lookup"><span data-stu-id="9d049-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="9d049-112">Klik på rullelisten i feltet **Regnskaber** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9d049-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9d049-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9d049-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9d049-115">Klik på **Tilføj** i oversigtspanelet **Hvilke segmentværdier er gyldige denne kladde?**.</span><span class="sxs-lookup"><span data-stu-id="9d049-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="9d049-116">Klik på rullelisten i feltet **Kontostruktur** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9d049-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9d049-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="9d049-118">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="9d049-119">Klik på rullelisten i feltet **Segment** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9d049-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9d049-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9d049-121">Klik på rullelisten i feltet **Fra-værdi** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9d049-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="9d049-122">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9d049-123">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9d049-124">Klik på rullelisten i feltet **Til-værdi** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9d049-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="9d049-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="9d049-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9d049-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="9d049-127">Angive bogføringsbegrænsninger</span><span class="sxs-lookup"><span data-stu-id="9d049-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="9d049-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9d049-128">Close the page.</span></span>
2. <span data-ttu-id="9d049-129">Klik på **Bogføringsbegrænsninger**.</span><span class="sxs-lookup"><span data-stu-id="9d049-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="9d049-130">Vælg 'Pr. brugergruppe' i **Hvordan vil du indstille bogføringsbegrænsninger?**.</span><span class="sxs-lookup"><span data-stu-id="9d049-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="9d049-131">Markér 'den gruppe, du vil tillade bogføring af dette kladdenavn' i træet.</span><span class="sxs-lookup"><span data-stu-id="9d049-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="9d049-132">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d049-132">Click **OK**.</span></span>

