---
title: Brug af arbejdsgange til at administrere medarbejderoplysninger
description: "I dette emne forklares, hvordan du kan bruge arbejdsgangsfunktionen i Personale til at administrere medarbejderoplysninger. Du kan f.eks. knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejderne ændrer deres post."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0ffae206ae1956e5dc41487f04561ed2c48bd20b
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="43325-104">Brug af arbejdsgange til at administrere medarbejderoplysninger</span><span class="sxs-lookup"><span data-stu-id="43325-104">Use workflows to manage employee information</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43325-105">I dette emne forklares, hvordan du kan bruge arbejdsgangsfunktionen i Personale til at administrere medarbejderoplysninger.</span><span class="sxs-lookup"><span data-stu-id="43325-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="43325-106">Du kan f.eks. knytte en arbejdsgang til en stilling og konfigurere et godkendelsesforløb, der startes, når medarbejderne ændrer deres post.</span><span class="sxs-lookup"><span data-stu-id="43325-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="43325-107">Arbejdsgangsfunktionen til Personale indeholder adskillige arbejdsganger til administration af personaleaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="43325-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="43325-108">Desuden er der adgang til talrige indstillinger, så du kan ændre bestemte arbejdsgange og knytte dem til et rapporteringshierarki.</span><span class="sxs-lookup"><span data-stu-id="43325-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="43325-109">Arbejdsgange er tilgængelige som en hjælp til at styre ændringer af adskillige standardtyper af medarbejderoplysninger.</span><span class="sxs-lookup"><span data-stu-id="43325-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="43325-110">Du kan knytte en arbejdsgang til en stilling.</span><span class="sxs-lookup"><span data-stu-id="43325-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="43325-111">Hvis medarbejderne derefter ændrer deres medarbejderpost, starter en arbejdsproces, der kræver godkendelse, før de nye oplysninger gemmes.</span><span class="sxs-lookup"><span data-stu-id="43325-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="43325-112">Arbejdsgange er foruddefineret for følgende typer oplysninger for at hjælpe dig med effektivt at administrere ændringer og holde dine medarbejderdata nøjagtige:</span><span class="sxs-lookup"><span data-stu-id="43325-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="43325-113">Identifikationsnumre</span><span class="sxs-lookup"><span data-stu-id="43325-113">Identification numbers</span></span>
-   <span data-ttu-id="43325-114">Kurser</span><span class="sxs-lookup"><span data-stu-id="43325-114">Courses</span></span>
-   <span data-ttu-id="43325-115">Uddannelser</span><span class="sxs-lookup"><span data-stu-id="43325-115">Education</span></span>
-   <span data-ttu-id="43325-116">Billede</span><span class="sxs-lookup"><span data-stu-id="43325-116">Image</span></span>
-   <span data-ttu-id="43325-117">Udlånte emner</span><span class="sxs-lookup"><span data-stu-id="43325-117">Loaned items</span></span>
-   <span data-ttu-id="43325-118">Erhvervserfaring</span><span class="sxs-lookup"><span data-stu-id="43325-118">Professional experience</span></span>
-   <span data-ttu-id="43325-119">Projekterfaring</span><span class="sxs-lookup"><span data-stu-id="43325-119">Project experience</span></span>
-   <span data-ttu-id="43325-120">Færdigheder</span><span class="sxs-lookup"><span data-stu-id="43325-120">Skills</span></span>
-   <span data-ttu-id="43325-121">Tillidsposter</span><span class="sxs-lookup"><span data-stu-id="43325-121">Positions of trust</span></span>
-   <span data-ttu-id="43325-122">Handlinger for Personale</span><span class="sxs-lookup"><span data-stu-id="43325-122">Human resources actions</span></span>
-   <span data-ttu-id="43325-123">Kursustilmelding</span><span class="sxs-lookup"><span data-stu-id="43325-123">Course registration</span></span>

<span data-ttu-id="43325-124">Når medarbejdere ansættes, overføres eller fratræder, kan arbejdsgangen omfatter en revisionsproces.</span><span class="sxs-lookup"><span data-stu-id="43325-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="43325-125">På denne måde kan et dokument blive evalueret, eller vilkårene for en handling kan defineres som en del af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="43325-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="43325-126">Når evalueringsprocessen er fuldført, fuldføres dokumentet eller handlingen, og arbejdsgangen flyttes til et trin til endelig godkendelse.</span><span class="sxs-lookup"><span data-stu-id="43325-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="43325-127">Knyt en arbejdsgang til et stillingshierarki</span><span class="sxs-lookup"><span data-stu-id="43325-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="43325-128">Du kan knytte en arbejdsgang til ethvert hierarki, du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="43325-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="43325-129">Hvis en stilling er tilknyttet et matrixrapporteringshierarki, kan du konfigurere en arbejdsgang, der dirigerer udgifter for et bestemt projekt til projektleder i stedet for til lederen af den medarbejder, der er tilknyttet den pågældende stilling.</span><span class="sxs-lookup"><span data-stu-id="43325-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="43325-130">Klik på **Ny** på siden **Arbejdsgange for Personale** for at oprette en ny arbejdsgang eller ændre en eksisterende arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="43325-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="43325-131">Vælg en arbejdsgang på listen for at starte arbejdsgangsdesigneren.</span><span class="sxs-lookup"><span data-stu-id="43325-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="43325-132">Du kan bruge designeren til at oprette en ny arbejdsgang eller til at ændre trinnene i en eksisterende arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="43325-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="43325-133">Når du ændrer en eksisterende arbejdsgang, gemmes ændringerne som en ny version.</span><span class="sxs-lookup"><span data-stu-id="43325-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="43325-134">Derfor, du kan altid gå tilbage til en tidligere version, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="43325-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="43325-135">Konfigurer en arbejdsgang for Personale</span><span class="sxs-lookup"><span data-stu-id="43325-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="43325-136">Følg disse trin for at konfigurere en grundlæggende arbejdsgang, der startes, når medarbejdere anmoder om ændringer i deres personlige id.</span><span class="sxs-lookup"><span data-stu-id="43325-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="43325-137">På siden **Arbejdsgange for Personale** skal du klikke på **ny**.</span><span class="sxs-lookup"><span data-stu-id="43325-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="43325-138">På listen over tilgængelige arbejdsgange skal du vælge **Identifikationsnumre**.</span><span class="sxs-lookup"><span data-stu-id="43325-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="43325-139">Klik på **Kør** for at starte arbejdsgangsdesigneren, og indtast derefter dit brugernavn og din adgangskode, når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="43325-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="43325-140">Træk elementet **Godkend identifikationsnummer** fra listen over arbejdsgangselementer til designerlærredet.</span><span class="sxs-lookup"><span data-stu-id="43325-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="43325-141">Tilslut godkendelseselementet til **Start** og **Afslut**.</span><span class="sxs-lookup"><span data-stu-id="43325-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="43325-142">Dobbeltklik på **Godkend element**, og højreklik derefter, og vælg **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="43325-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="43325-143">Følg disse trin for at tilføje arbejdsgangsinstruktioner:</span><span class="sxs-lookup"><span data-stu-id="43325-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="43325-144">Vælg **Tildeling**, og vælg derefter **Hierarki** under tildelingstypen.</span><span class="sxs-lookup"><span data-stu-id="43325-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="43325-145">Under valget **Hierarki** skal du vælge **Konfigurerbart hierarki**.</span><span class="sxs-lookup"><span data-stu-id="43325-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="43325-146">Tilføj en stopbetingelse, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="43325-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="43325-147">Fuldfør eventuelle yderligere instruktioner (der må ikke findes yderligere advarsler).</span><span class="sxs-lookup"><span data-stu-id="43325-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="43325-148">Klik på **Gem og luk**.</span><span class="sxs-lookup"><span data-stu-id="43325-148">Click **Save and close**.</span></span> <span data-ttu-id="43325-149">Aktivér den nye arbejdsproces, når dialogboksen åbnes, og vælg **Gør den aktiv**.</span><span class="sxs-lookup"><span data-stu-id="43325-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="43325-150">Gå til **Personale** &gt; **Stillinger** &gt; **Stillingshierarkityper**.</span><span class="sxs-lookup"><span data-stu-id="43325-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="43325-151">Vælg **Matrix**.</span><span class="sxs-lookup"><span data-stu-id="43325-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="43325-152">Tilføj arbejdsgangen **Identifikationsnummer på arbejder** til listen.</span><span class="sxs-lookup"><span data-stu-id="43325-152">Add the **Worker identification number** workflow to the list.</span></span>





