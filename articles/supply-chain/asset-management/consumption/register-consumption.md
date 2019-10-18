---
title: Registrere forbrug
description: Dette emne forklarer, hvordan du registrerer forbrug i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024654"
---
# <a name="register-consumption"></a><span data-ttu-id="12dac-103">Registrere forbrug</span><span class="sxs-lookup"><span data-stu-id="12dac-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="12dac-104">Når et vedligeholdelsesjob er fuldført i en arbejdsordre, er det næste trin at foretage registrering af forbrug og bogføre kladderne.</span><span class="sxs-lookup"><span data-stu-id="12dac-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="12dac-105">Du kan foretage registreringer på følgende forbrugstyper: timer, varer og udgifter.</span><span class="sxs-lookup"><span data-stu-id="12dac-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="12dac-106">De forskellige typer af forbrug registreres og bogføres på siden **Arbejdsordrekladder**.</span><span class="sxs-lookup"><span data-stu-id="12dac-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="12dac-107">Kladdeopsætningen i **Styring af aktiver** bruges til at oprette og bogføre separate kladder for timer, varer og udgifter i modulet **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="12dac-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="12dac-108">Du kan muligvis tilføje eller slette prognoselinjer på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="12dac-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="12dac-109">Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne for projekttypen bestemmer, om du kan tilføje eller redigere kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="12dac-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="12dac-110">Læs mere om livscyklustilstande for produktionsordrer og relaterede projektstadier i [Integration med projektstyring og regnskab](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="12dac-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="12dac-111">Det er muligt at konfigurere automatisk bogføring af kladder på en livscyklustilstand for en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="12dac-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="12dac-112">Du kan finde flere oplysninger i [Livscyklustilstande for arbejdsordrer](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="12dac-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="12dac-113">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12dac-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="12dac-114">Vælg arbejdsordren, og klik på **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="12dac-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="12dac-115">Klik på **Kopiér fra prognose** for at overføre eventuelle prognoselinjer, der er knyttet til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="12dac-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="12dac-116">Du kan vælge, hvilke forbrugstyper du vil overføre.</span><span class="sxs-lookup"><span data-stu-id="12dac-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="12dac-117">Hvis det er nødvendigt, kan du tilføje flere forbrugslinjer i det relevante oversigtspanel ved at klikke på **Tilføj linje** og angive data på linjen.</span><span class="sxs-lookup"><span data-stu-id="12dac-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="12dac-118">Klik på **Valider kladder** for at validere kladdelinjerne inden bogføringen.</span><span class="sxs-lookup"><span data-stu-id="12dac-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="12dac-119">Klik på **Bogfør kladder** for at bogføre kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="12dac-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="12dac-120">Når du har bogført forbrugskladderne, kan du opdatere livscyklustilstanden for arbejdsordren, f.eks. til "Afsluttet", for at angive, at arbejdsordren er fuldført.</span><span class="sxs-lookup"><span data-stu-id="12dac-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="12dac-121">I feltet **Vis** øverst på siden **Arbejdsordrekladder** skal du vælge, hvilke kladdelinjer du vil have vist: alle, ikke bogført eller bogført.</span><span class="sxs-lookup"><span data-stu-id="12dac-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="12dac-122">Bogførte kladder er markeret i afkrydsningsfeltet **Bogført**.</span><span class="sxs-lookup"><span data-stu-id="12dac-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="12dac-123">Når der oprettes varelinjer i arbejdsordrekladden, overføres produktdimensioner og sporingsdimensioner, der er knyttet til varen, automatisk til kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="12dac-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="12dac-124">Skærmbilledet nedenfor viser et eksempel på time- og vareregistreringer på en arbejdsordre i **Arbejdsordrekladder**.</span><span class="sxs-lookup"><span data-stu-id="12dac-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="12dac-126">Opdele timer i arbejdsordrer med flere arbejdsordrejob</span><span class="sxs-lookup"><span data-stu-id="12dac-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="12dac-127">Hvis en arbejdsordre indeholder flere arbejdsordrejob, kan du registrere arbejdstimer ved hjælp af funktionen **Opdel timer**. Det betyder, at én timeregistreringslinje kan fordeles jævnt på hvert arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="12dac-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="12dac-128">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12dac-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="12dac-129">Vælg arbejdsordren, og klik på **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="12dac-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="12dac-130">Vælg den timeregistreringslinje, du vil opdele, og klik på **Opdel timer**.</span><span class="sxs-lookup"><span data-stu-id="12dac-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="12dac-131">Navnet på den arbejder, der er logget på automatisk, vises i feltet **Arbejder** i dialogboksen med **Opdel timer på vedligeholdelsesjob for arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12dac-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="12dac-132">Hvis du har brug for det, kan du vælge en anden arbejder.</span><span class="sxs-lookup"><span data-stu-id="12dac-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="12dac-133">Vælg en kategori til timeregistreringen i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="12dac-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="12dac-134">Indsæt det antal arbejdstimer, der skal opdeles, i feltet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="12dac-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Figur 2](media/02-consumption.png)

7. <span data-ttu-id="12dac-136">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="12dac-136">Click **OK**.</span></span>

<span data-ttu-id="12dac-137">*Eksempel:* I skærmbilledet nedenfor vises kladdelinjer for en arbejdsordre, der indeholder tre arbejdsordrejob.</span><span class="sxs-lookup"><span data-stu-id="12dac-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="12dac-138">Den første linje, der indeholder tre arbejdstimer, er opdelt, og der er registreret én arbejdstime for hvert job i en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="12dac-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="12dac-139">Når registreringslinjerne på tre timer er oprettet, bestemmer du, hvad du vil gøre med den oprindelige timeregistreringslinje (den første linje i eksemplet).</span><span class="sxs-lookup"><span data-stu-id="12dac-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="12dac-140">Du kan beholde den, som den er, eller slette den.</span><span class="sxs-lookup"><span data-stu-id="12dac-140">You can keep it as is or delete it.</span></span> 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="12dac-142">Økonomiske dimensioner for registrering af forbrug</span><span class="sxs-lookup"><span data-stu-id="12dac-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="12dac-143">Når du foretager registreringer af forbrug, føjes økonomiske dimensioner, der er relateret til de forskellige registreringstyper, til registreringerne i en bestemt rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="12dac-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="12dac-144">*Time- og udgiftsregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="12dac-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="12dac-145">Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt.</span><span class="sxs-lookup"><span data-stu-id="12dac-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="12dac-146">Til sidst tilføjes økonomiske dimensioner fra ressourcen (arbejderen).</span><span class="sxs-lookup"><span data-stu-id="12dac-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="12dac-147">*Vareregistreringer:* Først tilføjes økonomiske dimensioner fra kladdehovedet, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="12dac-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="12dac-148">Derefter tilføjes økonomiske dimensioner fra det relaterede arbejdsordreprojekt.</span><span class="sxs-lookup"><span data-stu-id="12dac-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="12dac-149">Så tilføjes økonomiske dimensioner fra stedet.</span><span class="sxs-lookup"><span data-stu-id="12dac-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="12dac-150">Til sidst tilføjes økonomiske dimensioner fra varen.</span><span class="sxs-lookup"><span data-stu-id="12dac-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="12dac-151">For alle tre registreringstyper valideres den økonomiske dimensionskombination, og ugyldige kombinationer står tomme.</span><span class="sxs-lookup"><span data-stu-id="12dac-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="12dac-152">Dette er standardopsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12dac-152">This is standard setup in Finance and Operations.</span></span>

