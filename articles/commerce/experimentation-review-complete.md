---
title: Hæve en variation og fuldføre et eksperiment
description: Dette emne beskriver, hvordan du kan hæve en vellykket variation og fuldføre et eksperiment i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930160"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="b8854-103">Hæve en variation og fuldføre et eksperiment</span><span class="sxs-lookup"><span data-stu-id="b8854-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="b8854-104">Dette emne beskriver, hvordan du kan hæve den variation, der giver de bedste resultater i dit eksperiment, og hvordan du fuldfører eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="b8854-105">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8854-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b8854-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="b8854-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="b8854-107">[ ![Eksperimenteringens brugerrejse - vurdere og fuldføre](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b8854-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="b8854-108">Når du har [kørt dit eksperiment](experimentation-run-monitor.md) og har indsamlet tilstrækkelige data til at finde ud af, hvilken variation du vil bruge på dit live websted, skal du hæve variationen og afslutte eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="b8854-109">Hæve en variation</span><span class="sxs-lookup"><span data-stu-id="b8854-109">Promote a variation</span></span>
<span data-ttu-id="b8854-110">Brug de data og den analyse, der er knyttet til eksperimentet, i tredjepartstjenesten for at afgøre, hvilken variation der har givet de bedste resultater.</span><span class="sxs-lookup"><span data-stu-id="b8854-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="b8854-111">Hvis du vil erstatte det aktuelle indhold på det live websted med den vindende variation, så den er tilgængelig for alle brugere af dit websted, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="b8854-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="b8854-112">Gå til fanen **Eksperimenter** i webstedsgeneratoren, og vælg eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="b8854-113">Vælg **Fuldfør eksperiment** på øverste linje.</span><span class="sxs-lookup"><span data-stu-id="b8854-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="b8854-114">Vælg **Gennemse eksperimentdataene** i dialogmenuen **Fuldfør eksperimentet**.</span><span class="sxs-lookup"><span data-stu-id="b8854-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="b8854-115">Tredjepartstjenesten åbner, hvor du kan validere målepunkterne og bestemme, hvilken variation der er udført bedst.</span><span class="sxs-lookup"><span data-stu-id="b8854-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="b8854-116">Vælg den bedste variation i dialogboksen **Fuldfør eksperimentet** i webstedsgeneratoren, og vælg derefter **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b8854-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="b8854-117">Åbn tredjepartstjenesten, og stop eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="b8854-118">Vælg **Fuldfør** i webstedsgeneratoren for at overskrive den oprindelige aktive side og publicere den vindende variation, så den er tilgængelig for alle brugere på dit websted.</span><span class="sxs-lookup"><span data-stu-id="b8854-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="b8854-119">Hvis du vælger at beholde den aktuelle live side og ikke vil publicere en variation, skal du vælge **Publicer den oprindelige side igen**.</span><span class="sxs-lookup"><span data-stu-id="b8854-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="b8854-120">Slette dit eksperiment</span><span class="sxs-lookup"><span data-stu-id="b8854-120">Delete your experiment</span></span>
<span data-ttu-id="b8854-121">Selvom det ikke er påkrævet, at du sletter et fuldført arbejdsområde i Commerce, kan du vælge at slette det for at spare plads eller rydde op i arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="b8854-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="b8854-122">Benyt følgende fremgangsmåde for at slette et eksperiment.</span><span class="sxs-lookup"><span data-stu-id="b8854-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="b8854-123">Gå til fanen **Eksperimenter** i webstedsgeneratoren, og vælg eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="b8854-124">Hvis eksperimentet stadig er aktivt, skal du stoppe eksperimentet på tredjepartstjenesten, inden du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="b8854-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="b8854-125">Vælg **Annuller publicering** på kommandolinjen for at fjerne variationsindholdet fra det live websted.</span><span class="sxs-lookup"><span data-stu-id="b8854-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="b8854-126">Vælg **Slet** på kommandolinjen for at slette eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="b8854-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="b8854-127">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="b8854-127">Previous step</span></span>
[<span data-ttu-id="b8854-128">Køre og overvåge et eksperiment</span><span class="sxs-lookup"><span data-stu-id="b8854-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
