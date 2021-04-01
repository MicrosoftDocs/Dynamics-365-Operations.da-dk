---
title: Gennemse og publicere et eksperiment
description: I dette emne beskrives, hvordan du gennemser og publicerer et eksperiment fra Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b35af35f5d0347192ed94bed51dfd2484cfa481
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238576"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="939a6-103">Gennemse og publicere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="939a6-103">Preview and publish an experiment</span></span>

<span data-ttu-id="939a6-104">Dette emne beskriver, hvordan du gennemser og publicerer dit eksperiment i Dynamics 365 Commerce, når du har [tilsluttet dit eksperiment og redigeret dine variationer](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="939a6-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="939a6-105">I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="939a6-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="939a6-106">Yderligere trin behandles i separate emner.</span><span class="sxs-lookup"><span data-stu-id="939a6-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="939a6-107">[ ![Eksperimenteringens brugerrejse - gennemse og publicere](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="939a6-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="939a6-108">Gennemse dine eksperimentvariationer</span><span class="sxs-lookup"><span data-stu-id="939a6-108">Preview your experiment variations</span></span>
<span data-ttu-id="939a6-109">Du kan gennemse dine variationer og fortsætte med at redigere dem, indtil de ser ud, som du vil have dem.</span><span class="sxs-lookup"><span data-stu-id="939a6-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="939a6-110">Benyt følgende fremgangsmåde for at afprøve dine eksperimentvariationer i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="939a6-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="939a6-111">I rullemenuen med variationer under kommandoværktøjslinjen skal du vælge det indhold, du vil gennemse.</span><span class="sxs-lookup"><span data-stu-id="939a6-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="939a6-112">Vælg **Forhåndsvisning** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="939a6-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="939a6-113">Et eksempel på, hvordan indholdet vil se ud, når det publiceres, vises.</span><span class="sxs-lookup"><span data-stu-id="939a6-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="939a6-114">Hvis du vil se en anden variation, skal du vælge den på rullelisten Variation og vælge **Eksempel** igen.</span><span class="sxs-lookup"><span data-stu-id="939a6-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="939a6-115">Publicere dit eksperiment</span><span class="sxs-lookup"><span data-stu-id="939a6-115">Publish your experiment</span></span>
<span data-ttu-id="939a6-116">Hvis du ikke bruger en publiceringsgruppe til at planlægge, hvornår dit eksperiment går live, og du vil publicere det med det samme, skal du vælge **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="939a6-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="939a6-117">Alle de variationer, der hører til eksperimentet, vil blive publiceret.</span><span class="sxs-lookup"><span data-stu-id="939a6-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="939a6-118">Hvis siden har en ikke-publiceret URL-adresse, skal du først publicere URL-adressen, ellers kan den ikke ses af brugerne på webstedet.</span><span class="sxs-lookup"><span data-stu-id="939a6-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="939a6-119">Der er flere oplysninger i [Gemme, se og publicere en side](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="939a6-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="939a6-120">Bruge publiceringsgrupper til at planlægge, hvornår dit eksperiment går live</span><span class="sxs-lookup"><span data-stu-id="939a6-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="939a6-121">Varianter, der er oprettet i webstedsgeneratoren, kan planlægges til publicering ved hjælp af en publiceringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="939a6-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="939a6-122">I en publiceringsgruppe kan du forbinde en side eller et fragment med dit eksperiment ved at vælge **Eksperimenter** i venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="939a6-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="939a6-123">Du kan også gøre dette ved at vælge **Sider** eller **Fragmenter** og følge instruktionerne i [Tilslutte et eksperiment og redigere variationer](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="939a6-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="939a6-124">Du kan finde oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="939a6-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="939a6-125">Når du bruger publiceringsgrupper sammen med eksperimenter, er der nogle vigtige overvejelser, du skal være opmærksom på.</span><span class="sxs-lookup"><span data-stu-id="939a6-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="939a6-126">Når du tilføjer en side eller et fragment, der har et eksperiment kørende, i en publiceringsgruppe, fjernes eksperimentet fra siden eller fragmentet i publiceringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="939a6-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="939a6-127">Eksperimenter, der er forbundet med sider på et live websted, er ikke tilgængelige for siderne i publiceringsgrupper og omvendt.</span><span class="sxs-lookup"><span data-stu-id="939a6-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="939a6-128">På samme måde er sider, hvor eksperimenter kører på et live websted, ikke tilgængelige for andre eksperimenter i publiceringsgrupper og omvendt.</span><span class="sxs-lookup"><span data-stu-id="939a6-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="939a6-129">Når du publicerer eller planlægger en publiceringsgruppe, publiceres alt indhold i publiceringsgruppen, uanset om der er et eksperiment knyttet til publiceringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="939a6-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="939a6-130">Da en publiceringsgruppe fortsat vil være aktiv, efter at den er publiceret til et live websted, vil eksperimenter i publiceringsgruppen også fortsætte.</span><span class="sxs-lookup"><span data-stu-id="939a6-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="939a6-131">Derfor kan du ikke knytte andre eksperimenter til den samme side eller det samme fragment.</span><span class="sxs-lookup"><span data-stu-id="939a6-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="939a6-132">Hvis du vil undgå denne begrænsning, skal du slette alle publiceringsgrupper med vedvarende eksperimenter.</span><span class="sxs-lookup"><span data-stu-id="939a6-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="939a6-133">Hvis du ligeledes vil slette et eksperiment på et live websted, der også findes i en publiceringsgruppe, skal du først slette det fra publiceringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="939a6-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="939a6-134">Forrige trin</span><span class="sxs-lookup"><span data-stu-id="939a6-134">Previous step</span></span>
[<span data-ttu-id="939a6-135">Tilslutte og redigere et eksperiment</span><span class="sxs-lookup"><span data-stu-id="939a6-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="939a6-136">Næste trin</span><span class="sxs-lookup"><span data-stu-id="939a6-136">Next step</span></span>
[<span data-ttu-id="939a6-137">Køre og overvåge et eksperiment</span><span class="sxs-lookup"><span data-stu-id="939a6-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]