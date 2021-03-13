---
title: Send og godkend projektbudget
description: Denne procedure viser, hvordan du opretter og indsender et budget for et projekt.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b871a3fef3515d3a79fb4b55406a93fc16d02faa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018722"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="33aa9-103">Send og godkend projektbudget</span><span class="sxs-lookup"><span data-stu-id="33aa9-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33aa9-104">Denne procedure viser, hvordan du opretter og indsender et budget for et projekt.</span><span class="sxs-lookup"><span data-stu-id="33aa9-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="33aa9-105">Når du opretter et projektbudget, kan du angive estimerede indtægter og omkostninger for et projekt og derefter bruge det til at styre de faktiske projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="33aa9-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="33aa9-106">I projektbudgettering skal alle de oprindelige budgetter og revisioner sendes til projektarbejdsgangen til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="33aa9-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="33aa9-107">Med arbejdsgangen får du øget kontrol over processen, og der oprettes en post for ændringshistorikken.</span><span class="sxs-lookup"><span data-stu-id="33aa9-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="33aa9-108">Denne opgave blev oprettet ved hjælp af USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="33aa9-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="33aa9-109">Gå i **Navigationsrude** til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="33aa9-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="33aa9-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="33aa9-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="33aa9-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="33aa9-112">Klik på **Plan** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="33aa9-113">Klik på **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="33aa9-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="33aa9-115">Udvid oversigtspanelet **Omkostning**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="33aa9-116">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-116">Click **New**.</span></span>
9. <span data-ttu-id="33aa9-117">Vælg en indstilling i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="33aa9-118">Indtast eller vælg en værdi i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="33aa9-119">Angiv et tal i feltet **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="33aa9-120">Udvid oversigtspanelet **Indtægter**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="33aa9-121">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-121">Click **New**.</span></span>
14. <span data-ttu-id="33aa9-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="33aa9-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="33aa9-123">Vælg en indstilling i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="33aa9-124">Indtast eller vælg en værdi i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="33aa9-125">Angiv et tal i feltet **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="33aa9-126">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-126">Click **Save**.</span></span>
19. <span data-ttu-id="33aa9-127">Klik på **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="33aa9-128">Klik på **Send**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-128">Click **Submit**.</span></span>
21. <span data-ttu-id="33aa9-129">Skriv en værdi i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="33aa9-130">Klik på **Send**.</span><span class="sxs-lookup"><span data-stu-id="33aa9-130">Click **Submit**.</span></span>

