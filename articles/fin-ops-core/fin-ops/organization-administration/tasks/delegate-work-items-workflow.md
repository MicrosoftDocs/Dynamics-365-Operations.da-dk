---
title: Delegere workflowopgaver i en arbejdsgang
description: Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515758"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="c595f-103">Delegere arbejdselementer i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c595f-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="c595f-104">Manuel delegering af et arbejdselement</span><span class="sxs-lookup"><span data-stu-id="c595f-104">Manually delegate a work item</span></span>

<span data-ttu-id="c595f-105">For at delegere et individuelt arbejdselement skal du vælge indstillingen **Deleger** i menuen **Arbejdsgang** og derefter indtaste den bruger, som elementet skal delegeres til, samt en bemærkning hertil.</span><span class="sxs-lookup"><span data-stu-id="c595f-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="c595f-106">Dette vil omfordele arbejdselementet til den pågældende bruger, således at denne kan udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="c595f-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="c595f-107">Manuelt delegere flere arbejdselementer</span><span class="sxs-lookup"><span data-stu-id="c595f-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="c595f-108">Flere arbejdselementer kan delegeres sammen på siden **Arbejdselementer, der er tildelt mig**.</span><span class="sxs-lookup"><span data-stu-id="c595f-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="c595f-109">Følgende arbejdsgangstyper er berettiget til massedelegering: arbejdsgang til godkendelse af købsaftaler, arbejdsgang til indkøbsordrer, gennemgang af indkøbsrekvisitioner og arbejdsgang til kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="c595f-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="c595f-110">Funktionen **Deleger flere arbejdselementer** er som standard deaktiveret og kan aktiveres under **Arbejdsområder > Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="c595f-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="c595f-111">Kontakt systemadministratoren for at få hjælp til at aktivere denne funktion.</span><span class="sxs-lookup"><span data-stu-id="c595f-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="c595f-112">Gå til **Almindeligt > Almindeligt > Arbejdselementer > Arbejdselementer, der er tildelt til mig**.</span><span class="sxs-lookup"><span data-stu-id="c595f-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="c595f-113">Vælg de arbejdselementer, der skal delegeres.</span><span class="sxs-lookup"><span data-stu-id="c595f-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="c595f-114">Klik på menuen **Deler arbejdselementer**.</span><span class="sxs-lookup"><span data-stu-id="c595f-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="c595f-115">Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Bruger**.</span><span class="sxs-lookup"><span data-stu-id="c595f-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="c595f-116">Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.</span><span class="sxs-lookup"><span data-stu-id="c595f-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="c595f-117">Klik på knappen **Deleger arbejdselementer** for at fuldføre delegeringen af arbejdselementet.</span><span class="sxs-lookup"><span data-stu-id="c595f-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="c595f-118">Automatisk delegering af arbejdselementer</span><span class="sxs-lookup"><span data-stu-id="c595f-118">Automatically delegate work items</span></span>

<span data-ttu-id="c595f-119">Hvis du har planer om at være væk fra kontoret eller på anden vis ikke er til rådighed i en periode, kan du automatisk delegere nye arbejdselementer til andre brugere ved hjælp af siden **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c595f-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="c595f-120">Konfigurere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="c595f-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="c595f-121">Gå til **Generelt > Opsætning > Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="c595f-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="c595f-122">Klik på fanen **Arbejdsgang**. Kontrollér, at afsnittet Delegering er udvidet.</span><span class="sxs-lookup"><span data-stu-id="c595f-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="c595f-123">Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres.</span><span class="sxs-lookup"><span data-stu-id="c595f-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="c595f-124">Udfør følgende trin for at oprette en delegeringsregel:</span><span class="sxs-lookup"><span data-stu-id="c595f-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="c595f-125">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="c595f-125">Click **Add**.</span></span>
4. <span data-ttu-id="c595f-126">Vælg en indstilling i feltet **Omfang**.</span><span class="sxs-lookup"><span data-stu-id="c595f-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="c595f-127">Alle – Deleger alle workflowopgaver, der er tildelt dig.</span><span class="sxs-lookup"><span data-stu-id="c595f-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="c595f-128">Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c595f-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="c595f-129">Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c595f-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="c595f-130">Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c595f-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="c595f-131">Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c595f-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="c595f-132">Vælg den bruger, der skal delegeres arbejdselementer til, i feltet **Deleger**.</span><span class="sxs-lookup"><span data-stu-id="c595f-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="c595f-133">Brug felterne Startdato/-tidspunkt og Slutdato/-tidspunkt til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="c595f-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="c595f-134">Angiv en dato og et klokkeslæt i feltet **Startdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="c595f-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="c595f-135">Angiv en dato og et klokkeslæt i feltet **Slutdato/-klokkeslæt**.</span><span class="sxs-lookup"><span data-stu-id="c595f-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="c595f-136">Markér afkrydsningsfeltet **Aktiveret** for at aktivere delegeringsreglen.</span><span class="sxs-lookup"><span data-stu-id="c595f-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="c595f-137">Hvis du valgte **Modul** som Omfang, skal du vælge modulet i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c595f-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="c595f-138">Hvis du har valgt **Arbejdsgang** som Omfang, skal du vælge den specifikke arbejdsgang, der skal delegeres, i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c595f-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="c595f-139">Skriv en kommentar i feltet **Kommentar** for at forklare, hvorfor du delegerer arbejdselementer.</span><span class="sxs-lookup"><span data-stu-id="c595f-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

