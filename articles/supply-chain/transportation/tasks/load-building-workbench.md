---
title: Lastopbygningspanel
description: Dette emne beskriver, hvordan du kan arbejde med lastopbygningspanelet.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974216"
---
# <a name="load-building-workbench"></a><span data-ttu-id="07c8e-103">Lastopbygningspanel</span><span class="sxs-lookup"><span data-stu-id="07c8e-103">Load building workbench</span></span>

<span data-ttu-id="07c8e-104">Med lastopbygningspanelet kan du anvende lastopbygningsstrategier, når du opretter laster.</span><span class="sxs-lookup"><span data-stu-id="07c8e-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="07c8e-105">Oprette en lastopbygningsstrategi</span><span class="sxs-lookup"><span data-stu-id="07c8e-105">Create a load building strategy</span></span>

<span data-ttu-id="07c8e-106">Du kan bruge lastopbygningsstrategier til automatisk at opbygge laster.</span><span class="sxs-lookup"><span data-stu-id="07c8e-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="07c8e-107">Denne funktion kan være nyttige i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="07c8e-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="07c8e-108">Hvis du jævnligt leverer et bestemt sæt produkter, kan du spare tid ved at bruge laststrategier, da du ikke behøver at bygge samme last hver gang.</span><span class="sxs-lookup"><span data-stu-id="07c8e-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="07c8e-109">Hvis du vil undgå halvfulde laster for at maksimere effektiviteten, kan laststrategier være med til at fylde hver last så meget som muligt.</span><span class="sxs-lookup"><span data-stu-id="07c8e-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="07c8e-110">En klasse med lastopbygningsstrategi med navnet `TMSLoadBuildingVolumeStrategy` leverer en laststrategi, der kaldes *Volumenbaseret lastopbygningsstrategi*.</span><span class="sxs-lookup"><span data-stu-id="07c8e-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="07c8e-111">Denne strategi gør det muligt for dig at bruge de maksimumværdier, der er angivet for højde og vægt i lastskabelonen, eller du kan tilsidesætte indstillingerne ved at angive nye værdier.</span><span class="sxs-lookup"><span data-stu-id="07c8e-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="07c8e-112">Denne strategi er den eneste strategi, der er inkluderet i produktet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="07c8e-113">(Du kan dog have nogle brugerdefinerede strategier).</span><span class="sxs-lookup"><span data-stu-id="07c8e-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="07c8e-114">Hvis du vil bruge standardstrategien *Volumenbaseret lastopbygningsstrategi*, skal du markere den i feltet **Lastopbygningsstrategi** på siden **Lastopbygningspanel** (**Transportstyring &gt; Planlægning &gt; Lastopbygningspanel**).</span><span class="sxs-lookup"><span data-stu-id="07c8e-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="07c8e-115">Følg disse trin for at oprette en lastopbygningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="07c8e-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="07c8e-116">Gå til **Transportstyring &gt; Konfiguration &gt; Lastopbygning &gt; Lastopbygningsstrategier**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="07c8e-117">Vælg **Generér klasseliste** i handlingsruden for at sikre dig, at du har de seneste versioner af alle tilgængelige klasser.</span><span class="sxs-lookup"><span data-stu-id="07c8e-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="07c8e-118">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="07c8e-119">Angiv et entydigt navn til strategien, vælg dens klasse for lastopbygningsstrategi, og indtast en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="07c8e-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="07c8e-120">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="07c8e-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="07c8e-121">Gå til handlingsruden, og vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="07c8e-122">Vælg **Volumenkapacitet** på listen på siden **Parametre for lastopbygningsstrategi**, og brug derefter feltet **Værdi** til at angive den procentdel af lastens samlede volumenkapacitet, der skal anvendes for den nye lastopbygningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="07c8e-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="07c8e-123">Vælg **Vægtkapacitet** på listen, og brug derefter feltet **Værdi** til at angive den procentdel af lastens samlede vægtkapacitet, der skal anvendes for den nye lastopbygningsstrategi.</span><span class="sxs-lookup"><span data-stu-id="07c8e-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="07c8e-124">Luk siden **Parametre for lastopbygningsstrategi**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="07c8e-125">Luk siden **Lastopbygningsstrategier**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="07c8e-126">Du kan nu tildele lastopbygningsstrategien til en lastopbygningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="07c8e-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="07c8e-127">Du kan også bruge den direkte i lastplanlægningspanelet.</span><span class="sxs-lookup"><span data-stu-id="07c8e-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="07c8e-128">Bruge en lastopbygningsstrategi i lastopbygningspanelet</span><span class="sxs-lookup"><span data-stu-id="07c8e-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="07c8e-129">Gå til **Transportstyring &gt; Planlægning &gt; Lastopbygningspanel**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="07c8e-130">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="07c8e-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="07c8e-131">Vælg en strategi i feltet **Lastopbygningsstrategi**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="07c8e-132">Hvis du har defineret en lastopbygningsskabelon og tildelt den lastopbygningsstrategien, skal du vælge **Anvend skabelon** under fanen **Administrer skabeloner** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="07c8e-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="07c8e-133">Vælg derefter en skabelon i feltet **Navn på lastopbygningsskabelon** i rullemenuen i dialogboksen **Anvend lastopbygningsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="07c8e-134">Vælg en eller flere [lastskabeloner](load-template.md) i oversigtspanelet **Indlæs skabelonrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="07c8e-135">Panelet vil forsøge at indpasse lasten i disse typer objektbeholdere i den rækkefølge, der er angivet her.</span><span class="sxs-lookup"><span data-stu-id="07c8e-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="07c8e-136">Du skal typisk anbringe de mindste objektbeholdere øverst på listen for at sikre, at den mindst mulige objektbeholder vælges først.</span><span class="sxs-lookup"><span data-stu-id="07c8e-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="07c8e-137">Vælg **Foreslå laster** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="07c8e-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="07c8e-138">Gennemse de foreslåede laster og de foreslåede lastlinjer.</span><span class="sxs-lookup"><span data-stu-id="07c8e-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="07c8e-139">I handlingsruden skal du vælge **Opret laster** for at oprette laster, der er baseret på kildedokumentlinjerne i oversigtspanelet **Foreslåede lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="07c8e-140">Luk siden **Lastopbygningspanel**.</span><span class="sxs-lookup"><span data-stu-id="07c8e-140">Close the **Load building workbench** page.</span></span>
