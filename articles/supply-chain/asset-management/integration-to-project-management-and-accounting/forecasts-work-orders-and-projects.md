---
title: Budgetter, arbejdsordrer og projekter
description: Dette emne forklarer integrering af budgetter og arbejdsordrer i modulet Projektstyring og regnskab i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886810"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="28428-103">Budgetter, arbejdsordrer og projekter</span><span class="sxs-lookup"><span data-stu-id="28428-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="28428-104">I Styring af aktiver udføres integrationen med modulet **Projektstyring og regnskab** for at optimere omkostningsstyringen, hvilket giver brugerne mulighed for at spore omkostninger i budgetter for vedligeholdelsesjobtyper og arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="28428-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="28428-105">Der skal foretages to indstillinger, før der kan spores budgetter for vedligeholdelsesjobtyper:</span><span class="sxs-lookup"><span data-stu-id="28428-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="28428-106">Vælg et projekt i **Styring af aktiver** > **Opsætning** > **Parametre til aktivstyring** > **Aktiver**-link > oversigtspanelet **Projekt** > feltet **Vedligeholdelsesprognoseprojekt**.</span><span class="sxs-lookup"><span data-stu-id="28428-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="28428-107">Når du opretter en standardlinje for en vedligeholdelsesjobtype i **Standarder for vedligeholdelsesjobtype**, oprettes der automatisk et aktivitetsnummer for linjen (**Styring af aktiver** > **Opsætning** > **Job** > **Standarder for vedligeholdelsesjobtype**).</span><span class="sxs-lookup"><span data-stu-id="28428-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="28428-108">Budgetter for vedligeholdelsesjobtyper tjener to formål: Du kan spore omkostninger til budgetter for vedligeholdelsesjobtyper i modulet **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="28428-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="28428-109">Desuden overføres budgetter automatisk til et jobprojekt for en arbejdsordre, når du vælger en vedligeholdelsesjobtype i et arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="28428-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="28428-110">Hvis du vil spore omkostninger for job i arbejdsordrer, skal du først konfigurere arbejdsordreprojekter.</span><span class="sxs-lookup"><span data-stu-id="28428-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="28428-111">Se afsnittet [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md) for at få en beskrivelse af proceduren.</span><span class="sxs-lookup"><span data-stu-id="28428-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="28428-112">Projekter for arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="28428-112">Work order job projects</span></span>

<span data-ttu-id="28428-113">Når du opretter et arbejdsordrejob på en arbejdsordre, bestemmes arbejdsordreprojektet af opsætningen af det overordnede projekt for arbejdsordrer i **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**.</span><span class="sxs-lookup"><span data-stu-id="28428-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="28428-114">Projekter for arbejdsordrejob oprettes ved hjælp af en kombination af følgende oplysninger om arbejdsordrer:</span><span class="sxs-lookup"><span data-stu-id="28428-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="28428-115">Den arbejdsordretype, der er valgt på arbejdsordren</span><span class="sxs-lookup"><span data-stu-id="28428-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="28428-116">Det arbejdssted, der er relateret til aktivet på arbejdsordrejobbet</span><span class="sxs-lookup"><span data-stu-id="28428-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="28428-117">Den aktivtype, der er relateret til aktivet på arbejdsordrejobbet</span><span class="sxs-lookup"><span data-stu-id="28428-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="28428-118">Det forventede start- og sluttidspunkt, der er angivet på arbejdsordren</span><span class="sxs-lookup"><span data-stu-id="28428-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="28428-119">Det er muligt, at ikke alle ovennævnte oplysninger findes på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="28428-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="28428-120">Derfor sker søgningen efter et overordnet projekt til en arbejdsordre ved hjælp af den tilgængelige kombination af data og valg af det projekt-id, der svarer til arbejdsordredata.</span><span class="sxs-lookup"><span data-stu-id="28428-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="28428-121">Eksempel: Opsætningen af aktivtypen "Truck Engine" i figuren nedenfor betyder, at alle de arbejdsordrejob, der oprettes med den pågældende aktivtype, vil være et underprojekt af projekt-id'et "000186".</span><span class="sxs-lookup"><span data-stu-id="28428-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Figur 1](media/01-integration-to-pma.png)

<span data-ttu-id="28428-123">Formålet med projekt-id'et på arbejdsordrejobbet og det relaterede aktivitetsnummer (**Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** > vælg arbejdsordre på liste > oversigtspanelet **Linjedetaljer** > feltet **Projekt-id** og feltet **Aktivitetsnummer**) er at spore omkostninger, der vedrører arbejdsordrejobbet, og det aktiv, der er valgt på arbejdsordrejobbet, i modulet **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="28428-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="28428-124">I figuren nedenfor ser du en grafisk oversigt over projekter for arbejdsordrer og relaterede projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="28428-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Figur 2](media/02-integration-to-pma.png)

<span data-ttu-id="28428-126">Når et nyt arbejdsordrejob oprettes på en arbejdsordre, oprettes der automatisk et arbejdsordreprojekt for jobbet.</span><span class="sxs-lookup"><span data-stu-id="28428-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="28428-127">De økonomiske dimensioner for aktivet, der er tilknyttet arbejdsordrejobbet, overføres automatisk til arbejdsordreprojektet.</span><span class="sxs-lookup"><span data-stu-id="28428-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="28428-128">Den projektaktivitet, der er oprettet for et arbejdsordrejob, har relaterede oplysninger tilknyttet vedrørende vedligeholdelsesjobtype, variant af vedligeholdelsesjobtype og fag.</span><span class="sxs-lookup"><span data-stu-id="28428-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="28428-129">Disse data er nyttige, hvis du f.eks. opretter en indkøbsordre ud fra en arbejdsordre se( [Indkøb](../work-orders/procurement.md)), eller hvis du bruger modulet **Projektstyring og regnskab** til tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="28428-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="28428-130">Hvis aktivet er installeret på et arbejdssted, og dette aktiv senere installeres på et andet arbejdssted, opdateres de økonomiske dimensioner, der er relateret til det nye arbejdssted, automatisk på aktivet.</span><span class="sxs-lookup"><span data-stu-id="28428-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="28428-131">Når du efterfølgende opretter et arbejdsordrejob for aktivet, henter arbejdsordreprojektet for arbejdsordrejobbet automatisk de økonomiske dimensioner, der nu er relateret til aktivet.</span><span class="sxs-lookup"><span data-stu-id="28428-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="28428-132">Det betyder, at omkostninger altid kan spores på de arbejdssteder, hvor et aktiv var installeret på et givet tidspunkt, når du bruger arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="28428-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="28428-133">Den automatiske opdatering af økonomiske dimensioner sikrer en fuldstændig sporbarhed af omkostninger til projektstyring og rapportering.</span><span class="sxs-lookup"><span data-stu-id="28428-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="28428-134">Arbejdsordreprojekter, livscyklustilstande for arbejdsordrer, projektstadier og projekttyper</span><span class="sxs-lookup"><span data-stu-id="28428-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="28428-135">For at sikre korrekt brug af livscyklusser for arbejdsordrer og relaterede projektstadier i arbejdsordrer skal du overveje afhængighederne i forhold til modulet **Projektstyring og regnskab**:</span><span class="sxs-lookup"><span data-stu-id="28428-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="28428-136">I modulet **Projektstyring og regnskab** defineres projektstadier for projekttyper i **Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="28428-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="28428-137">I **Parametre for projektstyring og regnskab** skal du huske at markere de relevante afkrydsningsfelter for projektstadier for alle de projekttyper, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="28428-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="28428-138">I figuren herunder er de fem stadier **Oprettet** - **Forkalkuleret** - **Planlagt** - **Under behandling** - **Afsluttet** blevet valgt for projekttyperne "Tid og materiale" og "Intern".</span><span class="sxs-lookup"><span data-stu-id="28428-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="28428-139">Disse fem stadier er relevante for både interne vedligeholdelses- og servicevedligeholdelsesjob.</span><span class="sxs-lookup"><span data-stu-id="28428-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="28428-140">I **Styring af aktiver** defineres projekttyper af de projektgrupper, du opretter i formen **Opsætning af arbejdsordreprojekt** > link til **Projektgruppe**.</span><span class="sxs-lookup"><span data-stu-id="28428-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="28428-141">Opsætningen af projektgrupper i **Opsætning af arbejdsordreprojekt** bruges, når du opretter arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="28428-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="28428-142">Når en arbejdsordre er oprettet, oprettes der automatisk et arbejdsordreprojekt for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="28428-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="28428-143">Livscyklustilstande for arbejdsordrer skal hver have et relateret projektstadie.</span><span class="sxs-lookup"><span data-stu-id="28428-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="28428-144">Projektstadiet, der er knyttet til en livscyklustilstand for en arbejdsordre, skal defineres som et aktivt stadie for den projektgruppe, der er defineret i arbejdsordreprojektet.</span><span class="sxs-lookup"><span data-stu-id="28428-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="28428-145">Arbejdsordreprojektet oprettes automatisk på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="28428-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="28428-146">Når du opretter en ny arbejdsordre, er den automatiske tildeling af et arbejdsordreprojekt baseret på opsætningen i **Opsætning af arbejdsordreprojekt** (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Opsætning af Projekt**).</span><span class="sxs-lookup"><span data-stu-id="28428-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="28428-147">Tilknytninger mellem projektgrupper for arbejdsordrer, relaterede projekttyper, projektstadier og livscyklustilstande for arbejdsordrer vises i nedenstående figurer.</span><span class="sxs-lookup"><span data-stu-id="28428-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

<span data-ttu-id="28428-151">Se [Opsætning af arbejdsordreprojekt](../setup-for-work-orders/work-order-project-setup.md) for at få oplysninger om, hvordan du kan konfigurere arbejdsordreprojekter, og [Livscyklustilstande for arbejdsordre](../setup-for-work-orders/work-order-lifecycle-states.md) vedrørende, hvordan du kan oprette livscyklustilstande for arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="28428-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="28428-152">I figuren herunder vises en grafisk oversigt over de forskellige projekter, der oprettes i modulet **Styring af aktiver** for at tillade integration med modulet **Projektstyring og regnskab** samt de arbejdsprocesser, som projekterne er relateret til.</span><span class="sxs-lookup"><span data-stu-id="28428-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Figur 6](media/06-integration-to-pma.png)

