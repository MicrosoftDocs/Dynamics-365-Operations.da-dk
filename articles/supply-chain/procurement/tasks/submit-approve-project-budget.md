---
title: Send og godkend projektbudget
description: Denne procedure viser, hvordan du opretter og indsender et budget for et projekt.
author: mkirknel
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14683554c45db72061ecbbf4a528656df3132692
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424441"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="75080-103">Send og godkend projektbudget</span><span class="sxs-lookup"><span data-stu-id="75080-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75080-104">Denne procedure viser, hvordan du opretter og indsender et budget for et projekt.</span><span class="sxs-lookup"><span data-stu-id="75080-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="75080-105">Når du opretter et projektbudget, kan du angive estimerede indtægter og omkostninger for et projekt og derefter bruge det til at styre de faktiske projekttransaktioner.</span><span class="sxs-lookup"><span data-stu-id="75080-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="75080-106">I projektbudgettering skal alle de oprindelige budgetter og revisioner sendes til projektarbejdsgangen til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="75080-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="75080-107">Med arbejdsgangen får du øget kontrol over processen, og der oprettes en post for ændringshistorikken.</span><span class="sxs-lookup"><span data-stu-id="75080-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="75080-108">Denne opgave blev oprettet ved hjælp af USSI-datasættet.</span><span class="sxs-lookup"><span data-stu-id="75080-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="75080-109">Gå i **Navigationsrude** til **Moduler > Projektstyring og regnskab > Projekter > Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="75080-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="75080-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="75080-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="75080-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75080-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="75080-112">Klik på **Plan** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="75080-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="75080-113">Klik på **Projektbudget**.</span><span class="sxs-lookup"><span data-stu-id="75080-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="75080-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="75080-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="75080-115">Udvid oversigtspanelet **Omkostning**.</span><span class="sxs-lookup"><span data-stu-id="75080-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="75080-116">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="75080-116">Click **New**.</span></span>
9. <span data-ttu-id="75080-117">Vælg en indstilling i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="75080-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="75080-118">Indtast eller vælg en værdi i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="75080-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="75080-119">Angiv et tal i feltet **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="75080-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="75080-120">Udvid oversigtspanelet **Indtægter**.</span><span class="sxs-lookup"><span data-stu-id="75080-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="75080-121">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="75080-121">Click **New**.</span></span>
14. <span data-ttu-id="75080-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="75080-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="75080-123">Vælg en indstilling i feltet **Transaktionstype**.</span><span class="sxs-lookup"><span data-stu-id="75080-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="75080-124">Indtast eller vælg en værdi i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="75080-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="75080-125">Angiv et tal i feltet **Oprindeligt budget**.</span><span class="sxs-lookup"><span data-stu-id="75080-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="75080-126">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="75080-126">Click **Save**.</span></span>
19. <span data-ttu-id="75080-127">Klik på **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="75080-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="75080-128">Klik på **Send**.</span><span class="sxs-lookup"><span data-stu-id="75080-128">Click **Submit**.</span></span>
21. <span data-ttu-id="75080-129">Skriv en værdi i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="75080-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="75080-130">Klik på **Send**.</span><span class="sxs-lookup"><span data-stu-id="75080-130">Click **Submit**.</span></span>

