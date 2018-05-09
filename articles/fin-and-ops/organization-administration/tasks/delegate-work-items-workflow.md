--- 
title: Delegere workflowopgaver i en arbejdsgang
description: "Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 752c52431049093d0d9a1961d8f8bab604621f12
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="82428-103">Delegere workflowopgaver i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="82428-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82428-104">Hvis du planlægger at være væk fra kontoret eller af anden årsag ikke kan udføre workflowopgaver, kan du delegere eller tildele dine workflowopgaver til andre brugere.</span><span class="sxs-lookup"><span data-stu-id="82428-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="82428-105">Denne procedure hjælper dig med at konfigurere systemet til automatisk at delegere dine arbejdselementer til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="82428-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="82428-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="82428-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="82428-107">Konfigurere automatisk delegering</span><span class="sxs-lookup"><span data-stu-id="82428-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="82428-108">Gå til Generelt > Opsætning > Brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="82428-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="82428-109">Klik på fanen Arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="82428-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="82428-110">Sørg for, at sektionen Delegering er udvidet.</span><span class="sxs-lookup"><span data-stu-id="82428-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="82428-111">Hvis du vil konfigurere systemet til automatisk at delegere dine workflowopgaver til andre brugere, skal du oprette delegeringsregler, som angiver, hvornår bestemte workflowopgaver skal uddelegeres.</span><span class="sxs-lookup"><span data-stu-id="82428-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="82428-112">Udfør følgende trin for at oprette en delegeringsregel:</span><span class="sxs-lookup"><span data-stu-id="82428-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="82428-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="82428-113">Click Add.</span></span>
4. <span data-ttu-id="82428-114">Vælg en indstilling i feltet Område.</span><span class="sxs-lookup"><span data-stu-id="82428-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="82428-115">Alle – Deleger alle workflowopgaver, der er tildelt dig.</span><span class="sxs-lookup"><span data-stu-id="82428-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="82428-116">Modul – Deleger kun de arbejdselementer, der er relateret til en bestemt type arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="82428-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="82428-117">Hvis du vælger denne indstilling, skal du også vælge arbejdsgangens type i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82428-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="82428-118">Arbejdsgang – Deleger kun de arbejdselementer, der er relateret til en bestemt arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="82428-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="82428-119">Hvis du vælger denne indstilling, skal du vælge arbejdsgangen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82428-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="82428-120">Vælg den bruger, der skal delegeres arbejdselementer til, i feltet Deleger.</span><span class="sxs-lookup"><span data-stu-id="82428-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="82428-121">Brug felterne Startdato/-tidspunkt og Slutdato/-tidspunkt til at angive, hvornår du ønsker, at arbejdselementerne skal delegeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="82428-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="82428-122">Angiv en dato og et klokkeslæt i feltet Startdato/-tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="82428-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="82428-123">Angiv en dato og et klokkeslæt i feltet Slutdato/-tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="82428-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="82428-124">Marker afkrydsningsfeltet Aktiveret for at aktivere delegeringsreglen.</span><span class="sxs-lookup"><span data-stu-id="82428-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="82428-125">Hvis du valgte Modul som Område, skal du vælge modulet i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82428-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="82428-126">Hvis du har valgt Arbejdsgang som Område, skal du vælge den specifikke arbejdsgang, der skal delegeres, i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="82428-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="82428-127">Skriv en kommentar i feltet Kommentar for at forklare, hvorfor du delegerer arbejdselementer.</span><span class="sxs-lookup"><span data-stu-id="82428-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


