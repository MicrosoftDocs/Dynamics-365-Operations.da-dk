---
title: Delegere workflowopgaver i en arbejdsgang
description: Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140576"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="1446c-103">Delegere arbejdselementer i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1446c-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="1446c-104">Manuel delegering af et arbejdselement</span><span class="sxs-lookup"><span data-stu-id="1446c-104">Manually delegate a work item</span></span>

<span data-ttu-id="1446c-105">For at delegere et individuelt arbejdselement skal du vælge indstillingen **Deleger** i menuen **Arbejdsgang** og derefter indtaste den bruger, som elementet skal delegeres til, samt en bemærkning hertil.</span><span class="sxs-lookup"><span data-stu-id="1446c-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="1446c-106">Dette vil omfordele arbejdselementet til den pågældende bruger, således at denne kan udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="1446c-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="1446c-107">Automatisk delegering af arbejdselementer</span><span class="sxs-lookup"><span data-stu-id="1446c-107">Automatically delegate work items</span></span>

<span data-ttu-id="1446c-108">Hvis du har planer om at være væk fra kontoret eller på anden vis ikke er til rådighed i en periode, kan du automatisk delegere nye arbejdselementer til andre brugere ved hjælp af siden **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1446c-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="1446c-109">Konfigurere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="1446c-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="1446c-110">Gå til **Generelt > Opsætning > Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="1446c-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="1446c-111">Klik på fanen **Arbejdsgang**. Kontrollér, at afsnittet Delegering er udvidet.</span><span class="sxs-lookup"><span data-stu-id="1446c-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="1446c-112">Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres.</span><span class="sxs-lookup"><span data-stu-id="1446c-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="1446c-113">Udfør følgende trin for at oprette en delegeringsregel:</span><span class="sxs-lookup"><span data-stu-id="1446c-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="1446c-114">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="1446c-114">Click **Add**.</span></span>
4. <span data-ttu-id="1446c-115">Vælg en indstilling i feltet **Omfang**.</span><span class="sxs-lookup"><span data-stu-id="1446c-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="1446c-116">Alle – Deleger alle workflowopgaver, der er tildelt dig.</span><span class="sxs-lookup"><span data-stu-id="1446c-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="1446c-117">Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="1446c-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="1446c-118">Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="1446c-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="1446c-119">Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="1446c-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="1446c-120">Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="1446c-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="1446c-121">Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Deleger**.</span><span class="sxs-lookup"><span data-stu-id="1446c-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="1446c-122">Brug felterne Startdato/-tidspunkt og Slutdato/-tidspunkt til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="1446c-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="1446c-123">Angiv en dato og et klokkeslæt i feltet **Startdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="1446c-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="1446c-124">Angiv en dato og et klokkeslæt i feltet **Slutdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="1446c-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="1446c-125">Markér afkrydsningsfeltet **Aktiveret** for at aktivere delegeringsreglen.</span><span class="sxs-lookup"><span data-stu-id="1446c-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="1446c-126">Hvis du valgte **Modul** som Omfang, skal du vælge modulet i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="1446c-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="1446c-127">Hvis du har valgt **Arbejdsgang** som Omfang, skal du vælge den specifikke arbejdsgang, der skal delegeres, i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="1446c-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="1446c-128">Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.</span><span class="sxs-lookup"><span data-stu-id="1446c-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

