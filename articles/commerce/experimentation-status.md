---
title: Gennemgå status for et eksperiment
description: I dette emne forklares, hvad status et eksperiment har i livscyklussen for eksperimenteren i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: eea67ddc1718902198b74614ee1a910fc6e29c1d
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4411221"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="21f61-103">Gennemgå status for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="21f61-103">Review the status of an experiment</span></span>
<span data-ttu-id="21f61-104">Der er mange trin involveret i opsætning og kørsel af et eksperiment i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21f61-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="21f61-105">Du kan finde flere oplysninger om livscyklussen for eksperimenteren under [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="21f61-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="21f61-106">Hvis du vil vide, hvor et eksperiment er i livscyklussen, skal du vælge **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="21f61-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="21f61-107">Der vises en liste over eksperimenter med status for hvert eksperiment i både Commerce og den tredjepartstjeneste, der bruges til at aktivere oprettelse af eksperimenter, tildele variationer og analysere data.</span><span class="sxs-lookup"><span data-stu-id="21f61-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="21f61-108">I kolonnen **Commerce-status** kan følgende værdier vises.</span><span class="sxs-lookup"><span data-stu-id="21f61-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="21f61-109">**Kladde** - Eksperimentet er knyttet til en side eller et fragment i Commerce og er ved at blive redigeret.</span><span class="sxs-lookup"><span data-stu-id="21f61-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="21f61-110">**Publiceret** - Eksperimentvariationerne er klar til at blive vist på dit websted.</span><span class="sxs-lookup"><span data-stu-id="21f61-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="21f61-111">Hvis eksperimentet kører i tredjepartstjenesten, vil brugere af webstedet se en variant af siden eller fragmentet, der er valgt af tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="21f61-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="21f61-112">**Ikke-publiceret** - Eksperimentet er ikke længere tilgængeligt på dit websted.</span><span class="sxs-lookup"><span data-stu-id="21f61-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="21f61-113">Hvis eksperimentet kører i tredjepartstjenesten, vil brugere af webstedet kun se standardversionen af siden eller fragmentet.</span><span class="sxs-lookup"><span data-stu-id="21f61-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="21f61-114">**Fuldført** - Eksperimentet er færdigafviklet, og en variation blev hævet til live for alle brugere af webstedet.</span><span class="sxs-lookup"><span data-stu-id="21f61-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="21f61-115">På samme måde kan følgende værdier vises i kolonnen **tredjepartsstatus** for at angive, hvilken status eksperimenter har i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="21f61-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="21f61-116">**Kladde** - Eksperimentet er konfigureret i tredjepartstjenesten, men er ikke blevet startet.</span><span class="sxs-lookup"><span data-stu-id="21f61-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="21f61-117">**Kører** - Eksperimentet blev startet i tredjepartstjenesten og indsamler data.</span><span class="sxs-lookup"><span data-stu-id="21f61-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="21f61-118">**Afbrudt midlertidigt** - Eksperimentet er midlertidigt afbrudt og indsamler ikke data.</span><span class="sxs-lookup"><span data-stu-id="21f61-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="21f61-119">Du skal fortsætte eksperimentet for at indsamle data igen.</span><span class="sxs-lookup"><span data-stu-id="21f61-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="21f61-120">**Arkiveret** - Eksperimentet er færdigafviklet og er blevet katalogiseret i tredjepartstjenesten til fremtidig brug.</span><span class="sxs-lookup"><span data-stu-id="21f61-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="21f61-121">I nedenstående diagram vises begge sæt statusser, og hvordan de er relateret til hinanden.</span><span class="sxs-lookup"><span data-stu-id="21f61-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="21f61-122">[ ![Eksperimenterens statusser](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="21f61-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
