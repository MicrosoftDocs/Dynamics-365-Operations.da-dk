---
title: Hæve en variation og fuldføre et eksperiment
description: Dette emne beskriver, hvordan du kan hæve en vellykket variation og fuldføre et eksperiment i Dynamics 365 Commerce.
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097087"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="0706c-103">Hæve en variation og fuldføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="0706c-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="0706c-104">Dette emne beskriver, hvordan du kan hæve den variation, der giver de bedste resultater i dit eksperiment, og hvordan du fuldfører eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="0706c-105">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0706c-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0706c-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="0706c-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0706c-107">[ ![Eksperimenteringens brugerrejse - vurdere og fuldføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0706c-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="0706c-108">Når du har [kørt dit eksperiment](experimentation-run-monitor.md) og har indsamlet tilstrækkelige data til at finde ud af, hvilken variation du vil bruge på dit live websted, skal du hæve variationen og afslutte eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="0706c-109">Hæve en variation</span><span class="sxs-lookup"><span data-stu-id="0706c-109">Promote a variation</span></span>
<span data-ttu-id="0706c-110">Brug de data og den analyse, der er knyttet til eksperimentet, i tredjepartstjenesten for at afgøre, hvilken variation der har givet de bedste resultater.</span><span class="sxs-lookup"><span data-stu-id="0706c-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="0706c-111">Du kan derefter hæve den ved at erstatte det aktuelle indhold på det live websted med den vindende variation, så den er tilgængelig for alle brugere af dit websted.</span><span class="sxs-lookup"><span data-stu-id="0706c-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="0706c-112">Benyt følgende fremgangsmåde for at hæve den bedste variation:</span><span class="sxs-lookup"><span data-stu-id="0706c-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="0706c-113">Vælg **Eksperimenter** i venstre navigationsrude af Commerce-webstedsgeneratoren, og vælg derefter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="0706c-114">Vælg **Fuldfør eksperiment** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="0706c-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="0706c-115">Vælg **Gennemse eksperimentdataene** i dialogmenuen **Fuldfør eksperimentet**.</span><span class="sxs-lookup"><span data-stu-id="0706c-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="0706c-116">Tredjepartstjenesten åbner, hvor du kan validere målepunkterne og bestemme, hvilken variation der er udført bedst.</span><span class="sxs-lookup"><span data-stu-id="0706c-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="0706c-117">Vælg den bedste variation i dialogboksen **Fuldfør eksperimentet** , og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="0706c-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="0706c-118">Åbn tredjepartstjenesten, og stop eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="0706c-119">Vælg **Fuldfør** i webstedsgeneratoren for at overskrive den oprindelige aktive side og publicere den vindende variation, så den er tilgængelig for alle brugere på dit websted.</span><span class="sxs-lookup"><span data-stu-id="0706c-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="0706c-120">Hvis du vælger at beholde den aktuelle live side og ikke vil publicere en variation, skal du vælge **Publicer den oprindelige side igen**.</span><span class="sxs-lookup"><span data-stu-id="0706c-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="0706c-121">Slette dit eksperiment</span><span class="sxs-lookup"><span data-stu-id="0706c-121">Delete your experiment</span></span>
<span data-ttu-id="0706c-122">Selvom det ikke er påkrævet, at du sletter et fuldført arbejdsområde i Commerce, kan du vælge at slette det for at spare plads eller rydde op i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="0706c-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="0706c-123">Udfør følgende trin for at slette et eksperiment i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="0706c-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0706c-124">Vælg **Eksperimenter** i venstre navigationsrude, og vælg derefter eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="0706c-125">Hvis eksperimentet stadig er aktivt, skal du stoppe eksperimentet på tredjepartstjenesten, inden du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="0706c-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="0706c-126">Vælg **Annuller publicering** på kommandolinjen for at fjerne variationsindholdet fra det live websted.</span><span class="sxs-lookup"><span data-stu-id="0706c-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="0706c-127">Vælg **Slet** for at slette eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="0706c-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0706c-128">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="0706c-128">Previous step</span></span>
[<span data-ttu-id="0706c-129">Køre og overvåge et eksperiment</span><span class="sxs-lookup"><span data-stu-id="0706c-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
