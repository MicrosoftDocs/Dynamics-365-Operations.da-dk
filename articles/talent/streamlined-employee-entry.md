---
title: Strømlinet medarbejderangivelse og navigation
description: Dataindtastning for arbejdere i Dynamics 365 Talent er blevet forbedret for at tillade hurtig indtastning for alle medarbejdere, tidligere, aktive eller fremtidige. En forenklet/konsolideret navigationsmodel er blevet opdateret, så den hurtigt kan finde relaterede oplysninger og se og foretage de nødvendige opdateringer.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 40bbb8429355fa18fe12c7cf56f8d58f19766cad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009416"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="57a33-104">Strømlinet medarbejderangivelse og navigation</span><span class="sxs-lookup"><span data-stu-id="57a33-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57a33-105">Dynamics 365 Talent giver mulighed for effektiv indtastning af medarbejder- og ansættelsesdata.</span><span class="sxs-lookup"><span data-stu-id="57a33-105">Dynamics 365 Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="57a33-106">Du kan hurtigt opdatere oplysninger om arbejdshistorik for tidligere, aktive og fremtidige medarbejdere og kontrahenter.</span><span class="sxs-lookup"><span data-stu-id="57a33-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="57a33-107">Du kan også få en forenklet navigationsoplevelse for hurtigt at finde relaterede oplysninger og foretage de nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="57a33-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="57a33-108">Denne funktionalitet er nu tilgængelig i sandkassemiljøer.</span><span class="sxs-lookup"><span data-stu-id="57a33-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="57a33-109">Hvis du vil aktivere funktionen, skal du gå til **Systemadministration > Links > Opsætning > Systemparametre > Funktioner i prøveversion**.</span><span class="sxs-lookup"><span data-stu-id="57a33-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="57a33-110">Vælg **Udvidet arbejderform og navigation**.</span><span class="sxs-lookup"><span data-stu-id="57a33-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="57a33-111">Dette aktiverer disse ændringer for alle brugere.</span><span class="sxs-lookup"><span data-stu-id="57a33-111">This will enable these changes for all users.</span></span> <span data-ttu-id="57a33-112">Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="57a33-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="57a33-113">Indstillinger for visning</span><span class="sxs-lookup"><span data-stu-id="57a33-113">View options</span></span>

<span data-ttu-id="57a33-114">Du kan bruge **Visningsindstillinger** i arbejderformen til at vælge en kombination af medarbejdere og kontrahenter på en enkelt liste.</span><span class="sxs-lookup"><span data-stu-id="57a33-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="57a33-115">Disse indstillinger giver dig mulighed for at få vist arbejdere på tværs af juridiske enheder eller for den juridiske enhed, du i øjeblikket er logget på.</span><span class="sxs-lookup"><span data-stu-id="57a33-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="57a33-116">Du kan også se aktive, afventende og fratrådte arbejdere, og du kan begrænse resultaterne baseret på arbejdertypen (medarbejder eller kontrahent).</span><span class="sxs-lookup"><span data-stu-id="57a33-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="57a33-117">Hvis avanceret sikkerhed er aktiveret, kan du kun se disse medarbejdere og kontrahenter i de juridiske enheder, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="57a33-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="57a33-118">Kolonner i listevisningen ændres ud fra dine valg.</span><span class="sxs-lookup"><span data-stu-id="57a33-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="57a33-119">Når der f.eks. vises fratrådte medarbejdere, vises fratrædelsesdato og årsagskoder som ekstra kolonner på listen.</span><span class="sxs-lookup"><span data-stu-id="57a33-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="57a33-120">[![Indstillinger for visning](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="57a33-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="57a33-121">Navigation og banner</span><span class="sxs-lookup"><span data-stu-id="57a33-121">Navigation and banner</span></span>

<span data-ttu-id="57a33-122">Et banner viser vigtige oplysninger for hver arbejder.</span><span class="sxs-lookup"><span data-stu-id="57a33-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="57a33-123">Banneret for de aktive arbejdere viser følgende felter:</span><span class="sxs-lookup"><span data-stu-id="57a33-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="57a33-124">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="57a33-124">**Title**</span></span>
- <span data-ttu-id="57a33-125">**Afdeling**</span><span class="sxs-lookup"><span data-stu-id="57a33-125">**Department**</span></span>
- <span data-ttu-id="57a33-126">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="57a33-126">**Position type**</span></span>
- <span data-ttu-id="57a33-127">**Arbejdertype**</span><span class="sxs-lookup"><span data-stu-id="57a33-127">**Worker type**</span></span>
- <span data-ttu-id="57a33-128">**Leder**</span><span class="sxs-lookup"><span data-stu-id="57a33-128">**Manager**</span></span>
- <span data-ttu-id="57a33-129">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="57a33-129">**Legal entity**</span></span>

<span data-ttu-id="57a33-130">Banneret for de fratrådte arbejdere viser følgende felter:</span><span class="sxs-lookup"><span data-stu-id="57a33-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="57a33-131">**Fratrædelsesdato**</span><span class="sxs-lookup"><span data-stu-id="57a33-131">**Exited date**</span></span>
- <span data-ttu-id="57a33-132">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="57a33-132">**Reason**</span></span>

<span data-ttu-id="57a33-133">Banneret for de ventende medarbejdere viser følgende felter:</span><span class="sxs-lookup"><span data-stu-id="57a33-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="57a33-134">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="57a33-134">**Title**</span></span>
- <span data-ttu-id="57a33-135">**Afdeling**</span><span class="sxs-lookup"><span data-stu-id="57a33-135">**Department**</span></span>
- <span data-ttu-id="57a33-136">**Stillingstype**</span><span class="sxs-lookup"><span data-stu-id="57a33-136">**Position type**</span></span>
- <span data-ttu-id="57a33-137">**Leder**</span><span class="sxs-lookup"><span data-stu-id="57a33-137">**Manager**</span></span>
- <span data-ttu-id="57a33-138">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="57a33-138">**Starting date**</span></span>
- <span data-ttu-id="57a33-139">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="57a33-139">**Legal entity**</span></span>

<span data-ttu-id="57a33-140">Handlingsruden på arbejdersiden er blevet omorganiseret, så den indeholder færre muligheder.</span><span class="sxs-lookup"><span data-stu-id="57a33-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="57a33-141">Oplysningerne er nu organiseret i følgende kategorier:</span><span class="sxs-lookup"><span data-stu-id="57a33-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="57a33-142">Arbejde</span><span class="sxs-lookup"><span data-stu-id="57a33-142">Work</span></span>
- <span data-ttu-id="57a33-143">Person</span><span class="sxs-lookup"><span data-stu-id="57a33-143">Person</span></span>
- <span data-ttu-id="57a33-144">Orlov</span><span class="sxs-lookup"><span data-stu-id="57a33-144">Leave</span></span>
- <span data-ttu-id="57a33-145">Kompensation</span><span class="sxs-lookup"><span data-stu-id="57a33-145">Compensation</span></span>
- <span data-ttu-id="57a33-146">Frynsegoder</span><span class="sxs-lookup"><span data-stu-id="57a33-146">Benefits</span></span>
- <span data-ttu-id="57a33-147">Overholdelse</span><span class="sxs-lookup"><span data-stu-id="57a33-147">Compliance</span></span>

<span data-ttu-id="57a33-148">Desuden giver den nye fane **Links** på hovedsiden for arbejdere et centralt sted, hvor de kan få adgang til alle relaterede oplysninger for en arbejder.</span><span class="sxs-lookup"><span data-stu-id="57a33-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="57a33-149">På grund af disse ændringer kan oplysningerne vises på et andet sted, end du er vant til.</span><span class="sxs-lookup"><span data-stu-id="57a33-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="57a33-150">Lønoplysninger, der tidligere blev vist i arbejderformen, vises f.eks. nu i handlingsruden under **Kompensation > Løn**, og fanen **Personlige oplysninger** indeholder nu knappen **Flere oplysninger** for at skjule felter, der ikke bruges så ofte.</span><span class="sxs-lookup"><span data-stu-id="57a33-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="57a33-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="57a33-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="57a33-152">Arbejdshistorik</span><span class="sxs-lookup"><span data-stu-id="57a33-152">Work history</span></span>

<span data-ttu-id="57a33-153">Fanen **Arbejdshistorik** viser arbejdshistorik på tværs af alle juridiske enheder, og den er tilgængelig for fratrådte, aktive og afventende medarbejdere og kontrahenter.</span><span class="sxs-lookup"><span data-stu-id="57a33-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="57a33-154">Du kan nu få vist al arbejdshistorik på én gang for de juridiske enheder, du har adgang til.</span><span class="sxs-lookup"><span data-stu-id="57a33-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="57a33-155">Du kan desuden redigere oplysninger for hver enkelt post i arbejdshistorikken uden at ændre datakonteksten.</span><span class="sxs-lookup"><span data-stu-id="57a33-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="57a33-156">Du kan opdatere alle oplysninger direkte på siden.</span><span class="sxs-lookup"><span data-stu-id="57a33-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="57a33-157">[![Arbejdshistorik](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="57a33-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="57a33-158">Stillingshistorik</span><span class="sxs-lookup"><span data-stu-id="57a33-158">Position history</span></span>

<span data-ttu-id="57a33-159">Fanen **Stillinger** på hovedsiden for arbejdere indeholder en komplet visning af alle stillinger i organisationen, herunder tidligere, nuværende og eventuelle fremtidige tildelinger.</span><span class="sxs-lookup"><span data-stu-id="57a33-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="57a33-160">Du kan stadig gå direkte til arbejderens stillingshistorik i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="57a33-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="57a33-161">[![Stillinger](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="57a33-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

