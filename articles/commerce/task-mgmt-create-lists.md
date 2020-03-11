---
title: Oprette opgavelister og tilføje opgaver
description: Dette emne indeholder en beskrivelse af, hvordan du opretter opgavelister og føjer opgaver til dem i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 1cab31784db9f3242dce20e98762088436a5a8f8
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036826"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="515c4-103">Oprette opgavelister og tilføje opgaver</span><span class="sxs-lookup"><span data-stu-id="515c4-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="515c4-104">Dette emne indeholder en beskrivelse af, hvordan du opretter opgavelister og føjer opgaver til dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="515c4-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="515c4-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="515c4-105">Overview</span></span>

<span data-ttu-id="515c4-106">En *opgave* definerer et bestemt arbejde eller en handling, som en anden skal udføre på eller før en angivet forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="515c4-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="515c4-107">I Dynamics 365 Commerce kan en opgave indeholde detaljerede instruktioner og oplysninger om en kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="515c4-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="515c4-108">Den kan også indeholde links til bagbutikshandlinger, POS-handlinger eller webstedssider, som medvirker til at forbedre produktiviteten og levere den kontekst, som opgaveejeren kræver for at kunne fuldføre opgaven effektivt.</span><span class="sxs-lookup"><span data-stu-id="515c4-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="515c4-109">En *opgaveliste* er en samling opgaver, der skal fuldføres som en del af en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="515c4-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="515c4-110">Der kan f.eks. være en opgaveliste, som en ny arbejder skal udfylde under indlæringen, en opgaveliste til kasserere, der arbejder på et skiftehold, eller en opgaveliste, der skal fuldføres for at forberede butikken på den kommende ferie.</span><span class="sxs-lookup"><span data-stu-id="515c4-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="515c4-111">I Commerce kan alle de opgavelister, der har en måldato, tildeles et vilkårligt antal butikker eller medarbejdere, og den kan konfigureres til at gentages.</span><span class="sxs-lookup"><span data-stu-id="515c4-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="515c4-112">Både ledere og arbejdere kan oprette opgavelister på Commerce-bagkontor og derefter knytte dem til et sæt butikker.</span><span class="sxs-lookup"><span data-stu-id="515c4-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="515c4-113">Opret en opgaveliste</span><span class="sxs-lookup"><span data-stu-id="515c4-113">Create a task list</span></span>

<span data-ttu-id="515c4-114">Brug følgende trin for at oprette en opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="515c4-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="515c4-115">Gå til **Retail og Commerce \> Opgavestyring \> Administration af opgavestyring**.</span><span class="sxs-lookup"><span data-stu-id="515c4-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="515c4-116">Vælg **Ny**, og angiv derefter værdier i felterne **Navn**, **Beskrivelse**og **Ejer**.</span><span class="sxs-lookup"><span data-stu-id="515c4-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="515c4-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="515c4-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="515c4-118">Føje opgaver til en opgaveliste</span><span class="sxs-lookup"><span data-stu-id="515c4-118">Add tasks to a task list</span></span>

<span data-ttu-id="515c4-119">Følg disse trin for at føje opgaver til en opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="515c4-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="515c4-120">Vælg **Ny** i oversigtspanelet **Opgaver** af en eksisterende opgaveliste for at tilføje en opgave.</span><span class="sxs-lookup"><span data-stu-id="515c4-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="515c4-121">Skriv et navn på opgaven i feltet **Navn** i dialogboksen **Opret en ny opgave**.</span><span class="sxs-lookup"><span data-stu-id="515c4-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="515c4-122">Angiv en positiv eller negativ heltalsværdi i feltet **Forskydning af forfaldsdato fra måldato**.</span><span class="sxs-lookup"><span data-stu-id="515c4-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="515c4-123">Skriv f.eks. **-2** , hvis opgaven skal fuldføres to dage før opgavelistens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="515c4-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="515c4-124">Angiv detaljerede instruktioner i feltet **Bemærkninger**.</span><span class="sxs-lookup"><span data-stu-id="515c4-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="515c4-125">Skriv navnet på et emne for en ekspert, som opgaveejeren kan kontakte, hvis han eller hun har brug for hjælp, i feltet **Kontaktperson**.</span><span class="sxs-lookup"><span data-stu-id="515c4-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="515c4-126">Skriv et link baseret på opgavens art i feltet **Opgavelink**.</span><span class="sxs-lookup"><span data-stu-id="515c4-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="515c4-127">Selvom du kan bruge feltet **Tildelt til** for at tildele opgaver til en person, mens du opretter en opgaveliste, anbefaler vi, at du undgår at tildele opgaver under oprettelse af opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="515c4-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="515c4-128">I stedet skal du tildele opgaverne, når listen er instantieret for de enkelte butikker.</span><span class="sxs-lookup"><span data-stu-id="515c4-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="515c4-129">Brug opgavelinks som en hjælp til at forbedre medarbejderens produktivitet</span><span class="sxs-lookup"><span data-stu-id="515c4-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="515c4-130">Med Commerce kan du sammenkæde opgaver med bestemte POS-handlinger, f.eks. køre en salgsrapport, få vist en video med onlineundervisning til orientering for nye medarbejder eller udføre en sikkerhedskopiering af et kontor.</span><span class="sxs-lookup"><span data-stu-id="515c4-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="515c4-131">Denne funktion hjælper opgaveejere med at få de oplysninger, de skal bruge til at udføre en opgave mere effektivt.</span><span class="sxs-lookup"><span data-stu-id="515c4-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="515c4-132">Hvis du vil tilføje opgavelinks, mens du opretter en opgave, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="515c4-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="515c4-133">Vælg **Rediger** i oversigtspanelet **Opgaver** af en eksisterende opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="515c4-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="515c4-134">Vælg en eller flere af følgende indstillinger i feltet **Opgavelink** i dialogboksen **Rediger opgave**:</span><span class="sxs-lookup"><span data-stu-id="515c4-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="515c4-135">Vælg **Menupunkt** for at konfigurere en butikshandling, f.eks. "Produktpakker".</span><span class="sxs-lookup"><span data-stu-id="515c4-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="515c4-136">Vælg **POS-handling** for at konfigurere en POS-handling, f.eks. "Salgsrapporter".</span><span class="sxs-lookup"><span data-stu-id="515c4-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="515c4-137">Vælg **URL-adresse** for at konfigurere en absolut URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="515c4-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="515c4-138">I følgende illustration vises valget af opgavelinks i dialogboksen **Rediger opgave**.</span><span class="sxs-lookup"><span data-stu-id="515c4-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Vælge opgavelinks i dialogboksen Rediger opgave](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="515c4-140">Konfigurere en POS-handling, så den kan kædes sammen med en opgave</span><span class="sxs-lookup"><span data-stu-id="515c4-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="515c4-141">Du konfigurerer en POS-handling, så den kan kædes sammen med en opgave, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="515c4-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="515c4-142">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.</span><span class="sxs-lookup"><span data-stu-id="515c4-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="515c4-143">Vælg **Rediger**, find POS-handlingen, og vælg derefter afkrydsningsfeltet **Aktivér opgavestyring** for den.</span><span class="sxs-lookup"><span data-stu-id="515c4-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="515c4-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="515c4-144">Additional resources</span></span>

[<span data-ttu-id="515c4-145">Oversigt over opgavestyring</span><span class="sxs-lookup"><span data-stu-id="515c4-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="515c4-146">Konfigurer opgavestyring</span><span class="sxs-lookup"><span data-stu-id="515c4-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="515c4-147">Tildele opgavelister til butikker eller medarbejdere</span><span class="sxs-lookup"><span data-stu-id="515c4-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="515c4-148">Opgavestyring i POS</span><span class="sxs-lookup"><span data-stu-id="515c4-148">Task management in POS</span></span>](task-mgmt-POS.md)
