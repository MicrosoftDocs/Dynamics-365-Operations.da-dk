---
title: Registrere forbrug
description: Dette emne forklarer, hvordan du registrerer forbrug i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c9bbd51da23ea412bc124f932f73876a9506d47
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889235"
---
# <a name="register-consumption"></a><span data-ttu-id="a5d5b-103">Registrere forbrug</span><span class="sxs-lookup"><span data-stu-id="a5d5b-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a5d5b-104">Når et vedligeholdelsesjob er fuldført i en arbejdsordre, er det næste trin at foretage registrering af forbrug og bogføre kladderne.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="a5d5b-105">Du kan foretage registreringer på følgende forbrugstyper: timer, varer og udgifter.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="a5d5b-106">De forskellige typer af forbrug registreres og bogføres på siden **Arbejdsordrekladder**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="a5d5b-107">Kladdeopsætningen i **Styring af aktiver** bruges til at oprette og bogføre separate kladder for timer, varer og udgifter i modulet **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="a5d5b-108">Du kan muligvis tilføje eller slette prognoselinjer på en arbejdsordre i visse tilfælde.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="a5d5b-109">Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne for projekttypen bestemmer, om du kan tilføje eller redigere kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="a5d5b-110">Du kan læse mere om arbejdsordrers livscyklustilstande og relaterede projektstadier i [Budgetter, arbejdsordrer og projekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="a5d5b-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="a5d5b-111">Det er muligt at konfigurere automatisk bogføring af kladder på en livscyklustilstand for en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="a5d5b-112">Du kan finde flere oplysninger i [Livscyklustilstande for arbejdsordrer](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="a5d5b-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="a5d5b-113">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a5d5b-114">Vælg arbejdsordren, og klik på **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="a5d5b-115">Klik på **Kopiér fra prognose** for at overføre eventuelle prognoselinjer, der er knyttet til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="a5d5b-116">Du kan vælge, hvilke forbrugstyper du vil overføre.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="a5d5b-117">Hvis det er nødvendigt, kan du tilføje flere forbrugslinjer i det relevante oversigtspanel ved at klikke på **Tilføj linje** og angive data på linjen.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="a5d5b-118">Klik på **Valider kladder** for at validere kladdelinjerne inden bogføringen.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="a5d5b-119">Klik på **Bogfør kladder** for at bogføre kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="a5d5b-120">Når du har bogført forbrugskladderne, kan du opdatere livscyklustilstanden for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="a5d5b-121">Hvis du f.eks. vil angive, at arbejdsordren er fuldført, kan du opdatere livscyklustilstanden til "Afsluttet".</span><span class="sxs-lookup"><span data-stu-id="a5d5b-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="a5d5b-122">I feltet **Vis** øverst på siden **Arbejdsordrekladder** skal du vælge, hvilke kladdelinjer du vil have vist: **Alle**, **Ikke bogført** eller **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="a5d5b-123">Bogførte kladder er markeret i afkrydsningsfeltet **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="a5d5b-124">Når der oprettes varelinjer i arbejdsordrekladden, overføres produktdimensioner og sporingsdimensioner, der er knyttet til varen, automatisk til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="a5d5b-125">Skærmbilledet nedenfor viser et eksempel på time- og vareregistreringer på en arbejdsordre i **Arbejdsordrekladder**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="a5d5b-127">Opdele timer i arbejdsordrer med flere arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="a5d5b-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="a5d5b-128">Hvis en arbejdsordre indeholder flere arbejdsordrejob, kan du registrere arbejdstimer ved hjælp af funktionen **Opdel timer**. Det betyder, at én timeregistreringslinje kan fordeles jævnt på hvert arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="a5d5b-129">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a5d5b-130">Vælg arbejdsordren, og klik på **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="a5d5b-131">Vælg den timeregistreringslinje, du vil opdele, og klik på **Opdel timer**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="a5d5b-132">Navnet på den arbejder, der er logget på automatisk, vises i feltet **Arbejder** i dialogboksen med **Opdel timer på vedligeholdelsesjob for arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="a5d5b-133">Hvis du har brug for det, kan du vælge en anden arbejder.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="a5d5b-134">Vælg en kategori til timeregistreringen i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="a5d5b-135">Indsæt det antal arbejdstimer, der skal opdeles, i feltet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Figur 2](media/02-consumption.png)

7. <span data-ttu-id="a5d5b-137">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-137">Click **OK**.</span></span>

<span data-ttu-id="a5d5b-138">*Eksempel:* I skærmbilledet nedenfor vises kladdelinjer for en arbejdsordre, der indeholder tre arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="a5d5b-139">Den første linje, der indeholder tre arbejdstimer, er opdelt, og der er registreret én arbejdstime for hvert job i en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="a5d5b-140">Når registreringslinjerne på tre timer er oprettet, bestemmer du, hvad du vil gøre med den oprindelige timeregistreringslinje (den første linje i eksemplet).</span><span class="sxs-lookup"><span data-stu-id="a5d5b-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="a5d5b-141">Du kan beholde den, som den er, eller slette den.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-141">You can keep it as is or delete it.</span></span> 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="a5d5b-143">Økonomiske dimensioner for registrering af forbrug</span><span class="sxs-lookup"><span data-stu-id="a5d5b-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="a5d5b-144">Når du foretager registreringer af forbrug, føjes økonomiske dimensioner, der er relateret til de forskellige registreringstyper, til registreringerne i en bestemt rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="a5d5b-145">*Time- og udgiftsregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a5d5b-146">Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a5d5b-147">Til sidst tilføjes økonomiske dimensioner fra ressourcen (arbejderen).</span><span class="sxs-lookup"><span data-stu-id="a5d5b-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="a5d5b-148">*Vareregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="a5d5b-149">Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="a5d5b-150">Så tilføjes økonomiske dimensioner fra stedet.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="a5d5b-151">Til sidst tilføjes økonomiske dimensioner fra varen.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="a5d5b-152">For alle tre registreringstyper valideres den økonomiske dimensionskombination, og ugyldige kombinationer står tomme.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="a5d5b-153">Det er standardkonfigurationen med andre Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="a5d5b-153">This is standard setup with other Finance and Operations apps.</span></span>

