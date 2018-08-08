---
title: Integration med Microsoft Project-klienten
description: "Planlægning og vedligeholdelse af en projektplan kan være kompleks, så projektledere skal bruge værktøjer, som kan hjælper dem med at administrere denne opgave. Integration med Microsoft Project-klienten giver understøttelse til at åbne og styre et arbejdsopgavehierarki for projektet."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="ee37f-104">Integration med Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="ee37f-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee37f-105">Planlægning og vedligeholdelse af en projektplan kan være kompleks, så projektledere skal bruge værktøjer, som kan hjælper dem med at administrere denne opgave.</span><span class="sxs-lookup"><span data-stu-id="ee37f-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="ee37f-106">Integration med Microsoft Project-klienten giver understøttelse til at åbne og styre et arbejdsopgavehierarki for projektet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="ee37f-107">Projektlederen kan publicere eventuelle ændringer tilbage til arbejdsopgavehierarki i Finance and Operations-projektet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="ee37f-108">Hvis du bruger opdateringen til Microsoft Dynamics 365 for Finans and Operations fra juli, skal du installere KB 4054797 og 4055884.</span><span class="sxs-lookup"><span data-stu-id="ee37f-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="ee37f-109">Konfigurere tilføjelsesprogrammet til Microsoft Project-klient</span><span class="sxs-lookup"><span data-stu-id="ee37f-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="ee37f-110">Hvis du vil aktivere integrationen med Microsoft Project-klienten, skal et tilføjelsesprogram til Microsoft Dynamics 365 skal installeres i brugerens klientprogram Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="ee37f-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="ee37f-111">Dette gøres ved at åbne **Arbejdsområdet til projektstyring**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="ee37f-112">• Klik på **Konfigurer tilføjelsesprogram til Project-klient** fra sektionen **Links** > **Konfiguration** af arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="ee37f-113">• Klik på **Åbn**, og klik derefter på **Kør**, når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="ee37f-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="ee37f-114">Åbne og redigere en eksisterende kladde til arbejdsopgavehierarki i Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="ee37f-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="ee37f-115">Hvis et projekt i Finance and Operations allerede har et arbejdsopgavehierarki, der er oprettet, kan arbejdsopgavehierarkiet åbnes i klientprogrammet Microsoft Project, hvis arbejdsopgavehierarkiet er i kladdestatus.</span><span class="sxs-lookup"><span data-stu-id="ee37f-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="ee37f-116">Du åbner fra siden **Project** ved at klikke på linket **Åbne i Microsoft Project** under fanen **Plan**. Denne side kan også åbnes fra Microsoft Project-klientprogrammet ved at klikke på **Åbn** under fanen **Microsoft Dynamics 365**. Vælg **Juridisk enhed** og **Projekt** på listen.</span><span class="sxs-lookup"><span data-stu-id="ee37f-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="ee37f-117">Hvis du bruger Internet Explorer som browser, skal du klikke på **Gem** for manuelt at åbne fra den placering, filen er overført til.</span><span class="sxs-lookup"><span data-stu-id="ee37f-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="ee37f-118">Eller klik på **Gem og åbn** for at åbne filen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="ee37f-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="ee37f-119">Omdøb ikke filnavnet, når du gemmer.</span><span class="sxs-lookup"><span data-stu-id="ee37f-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="ee37f-120">Før du redigerer filen med Microsoft Project-klienten, skal du tjekke den ud. Klik på **Check ud** under fanen **Microsoft Dynamics 365**. Dette forhindrer andre brugere i samtidig at redigere arbejdsopgavehierarkiet inde fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ee37f-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="ee37f-121">For at udgive arbejdsopgavehierarkiet, når du har fuldført alle redigeringer, skal du klikke på **Check ind** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="ee37f-122">Hvis en projektteam allerede er føjet til projektet i Finance and Operations, udfyldes ressourcelisten med teammedlemmerne.</span><span class="sxs-lookup"><span data-stu-id="ee37f-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="ee37f-123">Hvis et projektteam endnu ikke er føjet til projektet, kan du vælge ressourcer og opbygge teamet i Microsoft Project-klienten ved at klikke på knappen **Ressourcer** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="ee37f-124">Følgende data synkroniseres tilbage til Finance and Operations som en del af check-in-processen:</span><span class="sxs-lookup"><span data-stu-id="ee37f-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="ee37f-125">•   Arbejdsrutinenavn</span><span class="sxs-lookup"><span data-stu-id="ee37f-125">•   Task name</span></span>

<span data-ttu-id="ee37f-126">•   Startdato</span><span class="sxs-lookup"><span data-stu-id="ee37f-126">•   Start date</span></span>

<span data-ttu-id="ee37f-127">•   Slutdato</span><span class="sxs-lookup"><span data-stu-id="ee37f-127">•   Finish date</span></span>

<span data-ttu-id="ee37f-128">•   Forgængere</span><span class="sxs-lookup"><span data-stu-id="ee37f-128">•   Predecessors</span></span>

<span data-ttu-id="ee37f-129">•   Ressourcenavne</span><span class="sxs-lookup"><span data-stu-id="ee37f-129">•   Resource names</span></span>

<span data-ttu-id="ee37f-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="ee37f-130">•   Category</span></span>

<span data-ttu-id="ee37f-131">•   Ressourcekategori</span><span class="sxs-lookup"><span data-stu-id="ee37f-131">•   Resource category</span></span>

<span data-ttu-id="ee37f-132">•   Arbejdstimer</span><span class="sxs-lookup"><span data-stu-id="ee37f-132">•   Work hours</span></span>

<span data-ttu-id="ee37f-133">•   Notater</span><span class="sxs-lookup"><span data-stu-id="ee37f-133">•   Notes</span></span>

<span data-ttu-id="ee37f-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="ee37f-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="ee37f-135">Hvis du føjer andre kolonner til din Microsoft Project-klientfil, bliver de ikke gemt i filen og vises ikke, når filen åbnes igen.</span><span class="sxs-lookup"><span data-stu-id="ee37f-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ee37f-136">Oprette arbejdsopgavehierarki til et eksisterende projekt ved hjælp af Microsoft Project-klient</span><span class="sxs-lookup"><span data-stu-id="ee37f-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ee37f-137">Du opretter et nyt arbejdsopgavehierarki ved hjælp af Microsoft Project-klient ved at følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="ee37f-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="ee37f-138">Åbn Microsoft Project-klient.</span><span class="sxs-lookup"><span data-stu-id="ee37f-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ee37f-139">Klik på **Åbn** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="ee37f-140">Vælg **Juridisk enhed** for projektet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="ee37f-141">Vælg **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="ee37f-142">Klik på **Check ud** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="ee37f-143">Når du er klar til at udgive til Finance and Operations, skal du klikke på **Check ind** under fanen **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ee37f-144">Erstat det eksisterende arbejdsopgavehierarki for et eksisterende projekt ved hjælp af Microsoft Project-klient</span><span class="sxs-lookup"><span data-stu-id="ee37f-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ee37f-145">Hvis du vil oprette en ny arbejdsopgavehierarki ved hjælp af Microsoft Project-klienten og erstatte en eksisterende arbejdsopgavehierarki for et eksisterende projekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="ee37f-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="ee37f-146">Åbn Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="ee37f-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ee37f-147">Opret tidsplanen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="ee37f-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ee37f-148">Under fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Erstat eksisterende projekt**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="ee37f-149">Vælg **Juridisk enhed** for projektet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ee37f-150">Vælg **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="ee37f-151">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="ee37f-152">Opret et nyt projekt fra Microsoft Project-klienten</span><span class="sxs-lookup"><span data-stu-id="ee37f-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="ee37f-153">Åbn Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="ee37f-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ee37f-154">Opret tidsplanen i Microsoft Project-klienten.</span><span class="sxs-lookup"><span data-stu-id="ee37f-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ee37f-155">Under fanen **Microsoft Dynamics 365** skal du klikke på **Gem ændringer** > **Gem i nyt projekt**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="ee37f-156">Vælg **Juridisk enhed** for projektet.</span><span class="sxs-lookup"><span data-stu-id="ee37f-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ee37f-157">Angiv **Projekt-id'et** om nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="ee37f-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="ee37f-158">Angiv **Projektnavn**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="ee37f-159">Vælg **Projekttype**, **Projektgruppe** og **Projektkontrakt-id**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="ee37f-160">Du kan også oprette en ny projektkontrakt ved at klikke på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="ee37f-161">Vælg den **kalender** der skal bruges til fremskaffelse af ressourcer.</span><span class="sxs-lookup"><span data-stu-id="ee37f-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="ee37f-162">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee37f-162">Click **OK**.</span></span>

