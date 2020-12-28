---
title: Tildeling af opgavelister til butikker eller medarbejdere
description: Dette emne beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 82cec9861b759037f40315fb2e6f36002a0ac059
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411146"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="fcdc5-103">Tildeling af opgavelister til butikker eller medarbejdere</span><span class="sxs-lookup"><span data-stu-id="fcdc5-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcdc5-104">Dette emne beskriver, hvordan du tildeler opgavelister til butikker eller medarbejdere i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcdc5-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="fcdc5-105">Overview</span></span>

<span data-ttu-id="fcdc5-106">Opgavestyring i Dynamics 365 Commerce giver dig mulighed for at tildele en opgaveliste til flere butikker eller medarbejdere eller til en kombination af butikker og medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-106">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="fcdc5-107">En regional chef for 20 butikker kan f.eks. vælge at tildele opgavelisten **Forberedelser til juleferien** til alle 20 butikker.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-107">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="fcdc5-108">Start tildelingsprocessen for opgavelisten</span><span class="sxs-lookup"><span data-stu-id="fcdc5-108">Start the task list assignment process</span></span>

<span data-ttu-id="fcdc5-109">Benyt følgende fremgangsmåde for at starte tildelingen af en opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-109">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="fcdc5-110">Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-110">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="fcdc5-111">Vælg den opgaveliste, der skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-111">Select the task list to assign.</span></span>
1. <span data-ttu-id="fcdc5-112">Vælg **Start proces**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-112">Select **Start process**.</span></span>
1. <span data-ttu-id="fcdc5-113">Angiv et navn (f.eks. **Butikker i den østlige region**) i feltnavnet **Procesnavn** i dialogboksen **Start proces** på fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-113">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="fcdc5-114">Angiv en dato i feltet **Måldato**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-114">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="fcdc5-115">Hvis du vil tildele opgavelisten til butikker, skal du finde og vælge butikker på fanen **Butikker** vha. filteret **Organisationshierarki**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-115">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="fcdc5-116">Hvis du vil tildele opgavelisten til medarbejdere, skal du finde og vælge medarbejderne under fanen **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-116">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="fcdc5-117">Vælg **OK** for at starte processen.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-117">Select **OK** to start the process.</span></span> <span data-ttu-id="fcdc5-118">Opgavelisten tildeles til de valgte butikker eller medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-118">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="fcdc5-119">I følgende illustration vises et eksempel på, hvordan du finder og vælger butikker i dialogboksen **Start proces**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-119">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![Finde og vælge butikker i dialogboksen Start proces](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="fcdc5-121">Tildele tilbagevendende opgavelister</span><span class="sxs-lookup"><span data-stu-id="fcdc5-121">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="fcdc5-122">Detailhandleren har nogle gange tilbagevendende opgaver, f.eks. "Tjekliste til torsdagslukning" eller "Tjekliste til første dag i måneden".</span><span class="sxs-lookup"><span data-stu-id="fcdc5-122">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="fcdc5-123">Det kan derfor være en god ide at tildele en tilbagevendende opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-123">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="fcdc5-124">Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-124">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="fcdc5-125">Vælg den opgaveliste, der skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-125">Select the task list to assign.</span></span>
1. <span data-ttu-id="fcdc5-126">Vælg **Start proces**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-126">Select **Start process**.</span></span>
1. <span data-ttu-id="fcdc5-127">Angiv et navn i feltet **Procesnavn** i dialogboksen **Start proces** på fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-127">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="fcdc5-128">Indstil indstillingen **Gentagelse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-128">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="fcdc5-129">Angiv antallet af dage i feltet **Forskydning af gentagelse af måldage i dage**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-129">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="fcdc5-130">Hvis du f.eks. angiver **4**, vil måldatoen være gentagelsesdatoen plus fire dage.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-130">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="fcdc5-131">Vælg **Gentagelse** på fanen **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-131">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="fcdc5-132">Angiv frekvenskriterierne i dialogboksen **Definer gentagelse**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-132">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="fcdc5-133">I følgende illustration vises et eksempel på, hvordan du kan angive hyppighedskriterier i dialogboksen **Definer gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-133">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![Angive frekvenskriterierne i dialogboksen Definer gentagelse](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="fcdc5-135">Spor status for opgaveliste</span><span class="sxs-lookup"><span data-stu-id="fcdc5-135">Track task list status</span></span>

<span data-ttu-id="fcdc5-136">Hvis du er regional chef eller butikschef, kan det være en god ide at spore status for opgavelister, der er tildelt til flere butikker eller medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-136">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="fcdc5-137">Du kan derefter følge op med butikker eller arbejdere, der ikke har fuldført deres tildelte opgaver til tiden.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-137">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="fcdc5-138">Med funktionen Commerce-bagkontor kan du få vist status for opgavelister, tildele opgaver igen eller ændre status for en opgave.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-138">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="fcdc5-139">Hvis du vil følge op på opgavelistestatus for alle opgaver, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-139">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="fcdc5-140">Gå til **Retail og Commerce \> Opgavestyring \> Opgavestyringsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-140">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="fcdc5-141">Vælg fanen **Alle opgavelister** for at få vist status for alle opgavelister, der er knyttet til forskellige butikker.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-141">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="fcdc5-142">Hvis du vil følge spore status for opgavelister for alle opgaver, som er tildelt dig, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-142">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="fcdc5-143">Gå til **Retail og Commerce \> Opgavestyring \> Opgavestyringsprocesser**.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-143">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="fcdc5-144">Vælg fanen **Mine opgaver** eller **Alle opgaver** for at få vist eller opdatere status for de opgaver, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-144">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcdc5-145">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fcdc5-145">Additional resources</span></span>

[<span data-ttu-id="fcdc5-146">Oversigt over opgavestyring</span><span class="sxs-lookup"><span data-stu-id="fcdc5-146">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="fcdc5-147">Konfigurer opgavestyring</span><span class="sxs-lookup"><span data-stu-id="fcdc5-147">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="fcdc5-148">Oprette opgavelister og tilføje opgaver</span><span class="sxs-lookup"><span data-stu-id="fcdc5-148">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="fcdc5-149">Opgavestyring i POS</span><span class="sxs-lookup"><span data-stu-id="fcdc5-149">Task management in POS</span></span>](task-mgmt-POS.md)
