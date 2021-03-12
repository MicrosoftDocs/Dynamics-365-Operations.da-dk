---
title: Tærskel for genopfyldning af zone
description: Ved zonebaseret genopfyldning bruges en opfyldningsstrategi for minimum/maksimum (min./maks.), men den evaluerer hele lagerzoner i stedet for kun individuelle lokationer. Lagercheferne kan derfor hurtigere finde ud af, når der kræves yderligere lagerplads i en plukzone.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 2e83d6885bf7400916d633a49d3b19b8843b0269
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965496"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="c0e76-104">Tærskel for genopfyldning af zone</span><span class="sxs-lookup"><span data-stu-id="c0e76-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0e76-105">Ved zonebaseret genopfyldning bruges en opfyldningsstrategi for minimum/maksimum (min./maks.) [genopfyldning](replenishment.md), men den evaluerer hele lagerzoner i stedet for kun individuelle lokationer.</span><span class="sxs-lookup"><span data-stu-id="c0e76-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="c0e76-106">Lagercheferne kan derfor hurtigere finde ud af, når der kræves yderligere lagerplads i en plukzone.</span><span class="sxs-lookup"><span data-stu-id="c0e76-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="c0e76-107">Konfigurationen for denne funktion ligner konfigurationen af lokationsbaseret genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="c0e76-108">Men når du konfigurerer en skabelon for min.-/maks.-genopfyldning, kan du også angive, om tærsklen skal evalueres pr. lokation eller pr. zone.</span><span class="sxs-lookup"><span data-stu-id="c0e76-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="c0e76-109">Hvis du konfigurerer evaluering, der er baseret på zoner, skal du føje bestemte zoner til zoneudvælgelsesforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="c0e76-110">Som lokationsbaseret min./maks.-genopfyldning er den zonebaserede min./maks.-genopfyldning baseret på konfigurationen af en minimumtærskel for lager, der udløser oprettelsen af genopfyldningsarbejde for udvalgte varer.</span><span class="sxs-lookup"><span data-stu-id="c0e76-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="c0e76-111">Dette genopfyldningsarbejde vil øge lageret op til den angivne tærskel for zonens maksimumtærskel.</span><span class="sxs-lookup"><span data-stu-id="c0e76-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="c0e76-112">Processer til zonegenopfyldning for produktvarianter understøttes ikke i den aktuelle version.</span><span class="sxs-lookup"><span data-stu-id="c0e76-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="c0e76-113">I modsætning til lokationsbaseret min./maks.-genopfyldning kræver zonebaseret min/maks.-genopfyldning ikke faste lokationer for at vurdere, om lokationer skal opbevare en bestemt vare.</span><span class="sxs-lookup"><span data-stu-id="c0e76-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="c0e76-114">Derfor giver zonebaseret opfyldning mulighed for at bruge min./maks.-genopfyldning, selvom du ikke har faste lokationer for hver vare eller varevariant på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="c0e76-115">Når et antal i zonen falder til under den angivne minimumstærskel, oprettes genopfyldningsarbejde.</span><span class="sxs-lookup"><span data-stu-id="c0e76-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="c0e76-116">Lokationsvejledninger bestemmer, hvilken specifik lokation lageret skal lægges på.</span><span class="sxs-lookup"><span data-stu-id="c0e76-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="c0e76-117">Aktivér funktionen til tærskel for genopfyldning af zone</span><span class="sxs-lookup"><span data-stu-id="c0e76-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="c0e76-118">Før du kan bruge funktionen *Tærskel for genopfyldning af zone*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="c0e76-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="c0e76-119">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="c0e76-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c0e76-120">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c0e76-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c0e76-121">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="c0e76-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c0e76-122">**Funktionsnavn:** *Tærskel for genopfyldning af zone*</span><span class="sxs-lookup"><span data-stu-id="c0e76-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="c0e76-123">Konfigurer zonebaseret genopfyldning</span><span class="sxs-lookup"><span data-stu-id="c0e76-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="c0e76-124">Hvis du vil konfigurere zonebaseret genopfyldning, skal du konfigurere flere dele af systemet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="c0e76-125">I dette afsnit introduceres de forskellige indstillinger og de demodataværdier, du kan angive, hvis du vil arbejde dig gennem scenariet sidst i dette emne.</span><span class="sxs-lookup"><span data-stu-id="c0e76-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="c0e76-126">Konfigurere vejledningskoder</span><span class="sxs-lookup"><span data-stu-id="c0e76-126">Set up directive codes</span></span>

<span data-ttu-id="c0e76-127">[Vejledningskoder](control-warehouse-location-directives.md) gør, at du kan være mere specifik, når du definerer den lokationsskabelon, der bruges i en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c0e76-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="c0e76-128">Hver kode opretter en fælles værdi, som du kan referere til, når du konfigurerer hver type skabelon.</span><span class="sxs-lookup"><span data-stu-id="c0e76-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="c0e76-129">Få vist og redigere vejledningskoder</span><span class="sxs-lookup"><span data-stu-id="c0e76-129">View and edit directive codes</span></span>

<span data-ttu-id="c0e76-130">Hvis du vil have vist eller redigere dine vejledningskoder, skal du gå til **Lokationsstyring \> Konfiguration \> Vejledningskoder**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="c0e76-131">Forberede vejledningskoder til demodata</span><span class="sxs-lookup"><span data-stu-id="c0e76-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="c0e76-132">I dette eksempel vises, hvordan du forbereder en vejledningskode.</span><span class="sxs-lookup"><span data-stu-id="c0e76-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="c0e76-133">Hvis du planlægger at arbejde dig gennem scenariet i slutningen af dette emne, skal du bruge de demoværdier, der angives her.</span><span class="sxs-lookup"><span data-stu-id="c0e76-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="c0e76-134">Ellers skal du bruge dine egne værdier.</span><span class="sxs-lookup"><span data-stu-id="c0e76-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="c0e76-135">Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.</span><span class="sxs-lookup"><span data-stu-id="c0e76-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="c0e76-136">Gå til **Lokationsstyring \> Opsætning \> Vejledningskoder**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="c0e76-137">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-138">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-139">**Vejledningskode:** _Zonegenopfyldning_</span><span class="sxs-lookup"><span data-stu-id="c0e76-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="c0e76-140">**Vejledningsbeskrivelse:** _Zonegenopfyldning_</span><span class="sxs-lookup"><span data-stu-id="c0e76-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="c0e76-141">Vælg **Gem** for at gemme den nye kode.</span><span class="sxs-lookup"><span data-stu-id="c0e76-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="c0e76-142">Konfigurer genopfyldningsskabeloner</span><span class="sxs-lookup"><span data-stu-id="c0e76-142">Set up replenishment templates</span></span>

<span data-ttu-id="c0e76-143">[Min/Max er genopfyldningsskabeloner](tasks/set-up-min-max-replenishment-process.md) er den primære mekanisme til opretholdelse af optimale niveauer på pluklokationer.</span><span class="sxs-lookup"><span data-stu-id="c0e76-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="c0e76-144">I disse skabeloner skal du konfigurere de regler, der skal bruges til genopfyldning af lageret på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="c0e76-145">Den genopfyldning, som skabelonerne kan bruges til, omfatter zonebaseret genopfyldning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="c0e76-146">Få vist og rediger genopfyldningsskabeloner</span><span class="sxs-lookup"><span data-stu-id="c0e76-146">View and edit replenishment templates</span></span>

<span data-ttu-id="c0e76-147">En genopfyldningsskabelon er et sæt regler, der styrer, hvornår og hvordan en lokation skal genopfyldes.</span><span class="sxs-lookup"><span data-stu-id="c0e76-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="c0e76-148">Du kan vælge en skabelon til at styre, hvornår og hvordan genopfyldningen skal udføres.</span><span class="sxs-lookup"><span data-stu-id="c0e76-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="c0e76-149">Du kan få vist eller redigere dine genopfyldningsskabeloner ved at gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="c0e76-150">Forberede en genopfyldningsskabelon til demodata</span><span class="sxs-lookup"><span data-stu-id="c0e76-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="c0e76-151">I dette eksempel vises, hvordan du forbereder en genopfyldningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="c0e76-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="c0e76-152">Hvis du planlægger at arbejde dig gennem scenariet i slutningen af dette emne, skal du bruge de demoværdier, der angives her.</span><span class="sxs-lookup"><span data-stu-id="c0e76-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="c0e76-153">Ellers skal du bruge dine egne værdier.</span><span class="sxs-lookup"><span data-stu-id="c0e76-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="c0e76-154">Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.</span><span class="sxs-lookup"><span data-stu-id="c0e76-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="c0e76-155">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="c0e76-156">Vælg **Rediger** for at sætte siden i redigeringstilstand.</span><span class="sxs-lookup"><span data-stu-id="c0e76-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="c0e76-157">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="c0e76-158">Angiv følgende værdier i den nye række.</span><span class="sxs-lookup"><span data-stu-id="c0e76-158">In the new row, set the following values.</span></span> <span data-ttu-id="c0e76-159">Accepter standardværdierne for alle andre felter.</span><span class="sxs-lookup"><span data-stu-id="c0e76-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="c0e76-160">**Genopfyldningsskabelon:** _Zone – min./maks. genopfyld._</span><span class="sxs-lookup"><span data-stu-id="c0e76-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="c0e76-161">**Beskrivelse:** _Min./maks. genopfyldning for zone_</span><span class="sxs-lookup"><span data-stu-id="c0e76-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="c0e76-162">**Genopfyldningstype:** _minimum eller maksimum_</span><span class="sxs-lookup"><span data-stu-id="c0e76-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="c0e76-163">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-163">Select **Save**.</span></span>
1. <span data-ttu-id="c0e76-164">Mens den nye række stadig er markeret i gitteret **Oversigt**, skal du vælge **Ny** over **Detaljer for genopfyldningsskabelon** for at tilføje en række, der er knyttet til genopfyldningsskabelonen *Zone – min./maks. genopfyld.*, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="c0e76-165">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-166">**Løbenummer:** Angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="c0e76-167">**Beskrivelse:** Angiv _Genopfyldning af plukzone_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="c0e76-168">**Opfyldningsenhed:** Vælg _hver_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="c0e76-169">**Anmodningstype** Lad dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="c0e76-170">**Vejledningskode:** Dette felt knytter genopfyldningsskabelonen sammen med en lokationsvejledning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="c0e76-171">Vælg den vejledningskode til demodata, du oprettede tidligere (_Zonegenopfyldning_).</span><span class="sxs-lookup"><span data-stu-id="c0e76-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="c0e76-172">**Arbejdsskabelon:** Lad feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="c0e76-173">**Minimumantal:** Dette felt angiver det antal, som opfyldning skal udløses på.</span><span class="sxs-lookup"><span data-stu-id="c0e76-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="c0e76-174">Angiv _50_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-174">Enter _50_.</span></span>
    - <span data-ttu-id="c0e76-175">**Maksimumantal:** Dette felt angiver det maksimale antal af en vare, der kan være til stede i en zone.</span><span class="sxs-lookup"><span data-stu-id="c0e76-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="c0e76-176">Oprettet genopfyldningsarbejde vil øge lagerbeholdningen til dette antal.</span><span class="sxs-lookup"><span data-stu-id="c0e76-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="c0e76-177">Angiv _150_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-177">Enter _150_.</span></span>
    - <span data-ttu-id="c0e76-178">**Enhed:** Dette felt angiver enheden for minimum- og maksimumværdier.</span><span class="sxs-lookup"><span data-stu-id="c0e76-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="c0e76-179">Vælg _hver_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-179">Select _ea_.</span></span>
    - <span data-ttu-id="c0e76-180">**Efterspørgselsstigning:** Vælg _Rund op_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="c0e76-181">**Genopfyld tomme faste lokationer:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="c0e76-182">**Genopfyld kun faste lokationer:** Ryd dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-183">**Produktforespørgselstilstand:** Vælg _Produktforespørgsel_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="c0e76-184">**Tærskelområde for genopfyldning:** Dette felt definerer, om skabelonen skal evalueres pr. zone eller efter en bestemt lokation.</span><span class="sxs-lookup"><span data-stu-id="c0e76-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="c0e76-185">Vælg _Zone_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-185">Select _Zone_.</span></span>
    - <span data-ttu-id="c0e76-186">**Lagersted:** Vælg _61_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="c0e76-187">Vælg **Vælg produkter** over gitteret **Detaljer for genopfyldningsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="c0e76-188">I dialogboksen **Produktforespørgsel** skal du på fanen **Område** vælge **Tilføj** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-189">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-190">**Tabel:** _Varer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="c0e76-191">**Afledt tabel:** _Varer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="c0e76-192">**Felt:** _Varenummer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="c0e76-193">**Kriterier:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="c0e76-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="c0e76-194">Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="c0e76-195">Vælg **Vælg zoner til genopfyldning** over gitteret **Detaljer for genopfyldningsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="c0e76-196">I dialogboksen **Zoneforespørgsel** skal du på fanen **Område** føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-197">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-198">**Tabel:** _Lagerstedszone_</span><span class="sxs-lookup"><span data-stu-id="c0e76-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="c0e76-199">**Afledt tabel:** _Lagerstedszone_</span><span class="sxs-lookup"><span data-stu-id="c0e76-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="c0e76-200">**Felt:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="c0e76-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="c0e76-201">**Kriterier:** _PRODUKTION_</span><span class="sxs-lookup"><span data-stu-id="c0e76-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="c0e76-202">Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="c0e76-203">Konfigurer lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="c0e76-203">Set up location directives</span></span>

<span data-ttu-id="c0e76-204">I modsætning til lokationsbaseret min./maks.-genopfyldning kræver zonebaseret min./maKS.-genopfyldning, at du konfigurerer både lokationsvejledninger for pluk og lokationsvejledninger for læg på lager, fordi systemet evaluerer hele zonen i stedet for blot pluklokationen til udgående arbejde.</span><span class="sxs-lookup"><span data-stu-id="c0e76-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="c0e76-205">Få vist og redigere lokationsvejledninger</span><span class="sxs-lookup"><span data-stu-id="c0e76-205">View and edit location directives</span></span>

<span data-ttu-id="c0e76-206">Hvis du vil have vist eller redigere dine lokationsvejledninger, skal du gå til **Lokationsstyring \> Konfiguration \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="c0e76-207">Du kan se eksempler, der viser, hvordan du kan bruge indstillingerne til at oprette de lokationsvejledninger til pluk og lokationsvejledninger til læg på lager, i næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="c0e76-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="c0e76-208">Forberede lokationsvejledninger til demodata</span><span class="sxs-lookup"><span data-stu-id="c0e76-208">Prepare demo data location directives</span></span>

<span data-ttu-id="c0e76-209">Hvis du vil forberede demodata, så de kan bruges i scenariet sidst i dette emne, skal du oprette to lokationsvejledninger: et til pluk og et til læg på lager.</span><span class="sxs-lookup"><span data-stu-id="c0e76-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="c0e76-210">Oprette en plukkevejledning for genopfyldning</span><span class="sxs-lookup"><span data-stu-id="c0e76-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="c0e76-211">Vælg den juridiske enhed **USMF**, der skal bruges til at arbejde med demodataene.</span><span class="sxs-lookup"><span data-stu-id="c0e76-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="c0e76-212">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c0e76-213">I venstre rude skal du angive feltet **Arbejdsordretype** til _Genopfyldning_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="c0e76-214">Vælg **Ny** i handlingsruden for at oprette en ny vejledning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="c0e76-215">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="c0e76-215">Set the following values:</span></span>

    - <span data-ttu-id="c0e76-216">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="c0e76-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="c0e76-217">**Navn:** Angiv _Zonepluk_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="c0e76-218">**Arbejdstype:** Vælg _Pluk_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="c0e76-219">**Lokation:** Vælg _6_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="c0e76-220">**Lagersted:** Vælg _61_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="c0e76-221">**Vejledningskode:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="c0e76-222">**Multi-SKU:** Angiv denne indstilling til _Nej_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="c0e76-223">Vælg **Gem** for at oprette en vejledning, der har de indstillinger, som du har konfigureret indtil nu.</span><span class="sxs-lookup"><span data-stu-id="c0e76-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="c0e76-224">Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="c0e76-225">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="c0e76-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c0e76-226">**Løbenummer:** Angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="c0e76-227">**Fra antal:** Angiv _0_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="c0e76-228">**Til antal:** Angiv _10000000_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="c0e76-229">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="c0e76-230">**Find antal:** Vælg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="c0e76-231">**Begræns efter enhed:** Ryd dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-232">**Rund op til enhed:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-233">**Find emballagemængde:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-234">**Tillad opdeling:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="c0e76-235">Vælg **Gem** for at gemme den nye linje.</span><span class="sxs-lookup"><span data-stu-id="c0e76-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="c0e76-236">Mens den nye linje stadig er markeret i gitteret **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger i lokationsvejledning** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-237">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-238">**Løbenummer:** Angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="c0e76-239">**Navn:** Angiv _Pluk fra masse_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="c0e76-240">**Anvendelse af fast lokation:** Vælg _Faste og ikke-faste lokationer_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="c0e76-241">**Tillad negativ lagerbeholdning:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-242">**Batch aktiveret:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-243">**Strategi:** Vælg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="c0e76-244">Vælg **Gem** for at gemme den nye handling.</span><span class="sxs-lookup"><span data-stu-id="c0e76-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="c0e76-245">Mens den nye handling stadig er valgt, skal du vælge **Rediger forespørgsel** over gitteret **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="c0e76-246">Der vises en forespørgselsdialogboks, hvor du kan vælge de lokationer, der skal genopfyldes fra.</span><span class="sxs-lookup"><span data-stu-id="c0e76-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="c0e76-247">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-248">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-249">**Tabel:** _Lokationer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="c0e76-250">**Afledt tabel:** _Lokationer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="c0e76-251">**Felt:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="c0e76-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="c0e76-252">**Kriterier:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="c0e76-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="c0e76-253">Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="c0e76-254">Vælg **Gem** for at gemme din lokationsvejledning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="c0e76-255">Oprette en læg på lager-vejledning for genopfyldning</span><span class="sxs-lookup"><span data-stu-id="c0e76-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="c0e76-256">På siden **Lokationsvejledninger** skal du i venstre rude kontrollere, at feltet **Arbejdsordretype** stadig er angivet til _Genopfyldning_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="c0e76-257">Vælg **Ny** i handlingsruden for at oprette en anden vejledning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="c0e76-258">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="c0e76-258">Set the following values:</span></span>

    - <span data-ttu-id="c0e76-259">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="c0e76-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="c0e76-260">**Navn:** Angiv _Zone-læg på lager_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="c0e76-261">**Ordretype:** Vælg _Læg på lager_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="c0e76-262">**Lokation:** Vælg _6_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="c0e76-263">**Lagersted:** Vælg _61_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="c0e76-264">**Vejledningskode:** Vælg _Zonegenopfyldning_ for at knytte denne lokationsvejledning direktiv til den opfyldningsskabelon, du har oprettet tidligere ved hjælp af den kode, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="c0e76-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="c0e76-265">**Multi-SKU:** Angiv denne indstilling til _Nej_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="c0e76-266">Vælg **Gem** for at oprette en vejledning, der har de indstillinger, som du har konfigureret indtil nu.</span><span class="sxs-lookup"><span data-stu-id="c0e76-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="c0e76-267">Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="c0e76-268">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="c0e76-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="c0e76-269">**Løbenummer:** Angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="c0e76-270">**Fra antal:** Angiv _0_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="c0e76-271">**Til antal:** Angiv _10000000_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="c0e76-272">**Enhed:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="c0e76-273">**Find antal:** Vælg _Ingen_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="c0e76-274">**Begræns efter enhed:** Ryd dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-275">**Rund op til enhed:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-276">**Find emballagemængde:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-277">**Tillad opdeling:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="c0e76-278">Vælg **Gem** for at gemme den nye linje.</span><span class="sxs-lookup"><span data-stu-id="c0e76-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="c0e76-279">Mens den nye linje stadig er markeret i gitteret **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger i lokationsvejledning** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-280">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-281">**Løbenummer:** Angiv _1_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="c0e76-282">**Navn:** Angiv _Zone-læg på lager_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="c0e76-283">**Anvendelse af fast lokation:** Vælg _Faste og ikke-faste lokationer_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="c0e76-284">**Tillad negativ lagerbeholdning:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-285">**Batch aktiveret:** Fjern markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="c0e76-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="c0e76-286">**Strategi:** Vælg _Konsolider_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="c0e76-287">Vælg **Gem** for at gemme den nye handling.</span><span class="sxs-lookup"><span data-stu-id="c0e76-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="c0e76-288">Mens den nye handling stadig er valgt, skal du vælge **Rediger forespørgsel** over gitteret **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="c0e76-289">Der vises en forespørgselsdialogboks, hvor du kan vælge den zone, der skal genopfyldes til.</span><span class="sxs-lookup"><span data-stu-id="c0e76-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="c0e76-290">Denne zone skal være den samme som den zone, der er angivet i genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="c0e76-291">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="c0e76-292">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="c0e76-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="c0e76-293">**Tabel:** _Lokationer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="c0e76-294">**Afledt tabel:** _Lokationer_</span><span class="sxs-lookup"><span data-stu-id="c0e76-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="c0e76-295">**Felt:** _Zone-id_</span><span class="sxs-lookup"><span data-stu-id="c0e76-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="c0e76-296">**Kriterier:** _PRODUKTION_</span><span class="sxs-lookup"><span data-stu-id="c0e76-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="c0e76-297">Vælg **OK** for at gemme din forespørgsel og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="c0e76-298">Vælg **Gem** for at gemme din lokationsvejledning.</span><span class="sxs-lookup"><span data-stu-id="c0e76-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="c0e76-299">Scenario</span><span class="sxs-lookup"><span data-stu-id="c0e76-299">Scenario</span></span>

<span data-ttu-id="c0e76-300">Dette afsnit indeholder et eksempel på et scenarie, der viser, hvordan du kan arbejde med funktionen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="c0e76-301">Forbered de eksempeldata, der kræves i eksempelscenariet</span><span class="sxs-lookup"><span data-stu-id="c0e76-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="c0e76-302">Før du går i gang med at arbejde med scenariet, skal du aktivere eksempeldata og konfigurere funktionen som beskrevet i dette afsnit og i forudgående afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="c0e76-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="c0e76-303">Brug den juridiske enhed USMF</span><span class="sxs-lookup"><span data-stu-id="c0e76-303">Use the USMF legal entity</span></span>

<span data-ttu-id="c0e76-304">Hvis du vil arbejde gennem scenariet ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="c0e76-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="c0e76-305">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="c0e76-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="c0e76-306">Forberede yderligere eksempeldata</span><span class="sxs-lookup"><span data-stu-id="c0e76-306">Prepare additional sample data</span></span>

<span data-ttu-id="c0e76-307">Når du har valgt den juridiske enhed **USMF**, skal du tilføje de ekstra eksempeldata, der kræves, som beskrevet i afsnittet [Konfigurer zonebaseret genopfyldning](#setup) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="c0e76-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="c0e76-308">Kontrollér dit disponible lager</span><span class="sxs-lookup"><span data-stu-id="c0e76-308">Check your on-hand inventory</span></span>

<span data-ttu-id="c0e76-309">Udfør følgende trin for at sikre, at systemet har et tilstrækkeligt lager til at understøtte eksempelscenariet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="c0e76-310">Kontroller, at der er et disponibelt lager for vare *A0001* på to forskellige lokationer i plukzonen (*PRODUKTION*), der er angivet i genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="c0e76-311">Det samlede lager skal dog være mindre end det krævede minimumantal (*50*), der er angivet på genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="c0e76-312">På denne måde kan du simulere, hvordan beregningen finder sted for hele zonen i stedet for en enkelt lokation.</span><span class="sxs-lookup"><span data-stu-id="c0e76-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="c0e76-313">**Brug en af lagerstedsprocesserne til at regulere lageret efter behov.**</span><span class="sxs-lookup"><span data-stu-id="c0e76-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="c0e76-314">Sørg for, at der er tilstrækkeligt lager til vare *A0001* på en massevarelokation, der er angivet i lokationsvejledningen til zone-pluk, hvor genopfyldningsarbejdet skal plukke varerne fra zone-id'et *MASSE*.</span><span class="sxs-lookup"><span data-stu-id="c0e76-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="c0e76-315">Det samlede lager skal være mere end det krævede maksimantal (*150*), der er angivet i genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="c0e76-316">Valgfrit, men anbefalet: Udfør følgende trin for at oprette en lagerreguleringskladde:</span><span class="sxs-lookup"><span data-stu-id="c0e76-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="c0e76-317">Gå til **Lokationsstyring \> Kladdeposteringer \> Varer \> Lagerregulering**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="c0e76-318">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-318">Select **New**.</span></span>
    1. <span data-ttu-id="c0e76-319">Vælg **61** i dialogboksen **Opret lagerkladde** i feltet *Lagersted*.</span><span class="sxs-lookup"><span data-stu-id="c0e76-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="c0e76-320">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-320">Select **OK**.</span></span>
    1. <span data-ttu-id="c0e76-321">I oversigtspanelet **Kladdelinjer** skal du bruge knappen **Ny** til at føje tre linjer til gitteret og angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="c0e76-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="c0e76-322">Vælg **Gem**, når du er færdig med at definere hver linje.</span><span class="sxs-lookup"><span data-stu-id="c0e76-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="c0e76-323">**Linje 1:**</span><span class="sxs-lookup"><span data-stu-id="c0e76-323">**Line 1:**</span></span>

            - <span data-ttu-id="c0e76-324">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0e76-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="c0e76-325">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0e76-325">**Site:** *6*</span></span>
            - <span data-ttu-id="c0e76-326">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="c0e76-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="c0e76-327">**Lokation:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="c0e76-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="c0e76-328">**Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.</span><span class="sxs-lookup"><span data-stu-id="c0e76-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="c0e76-329">**Antal:** *1000*</span><span class="sxs-lookup"><span data-stu-id="c0e76-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="c0e76-330">**Linje 2:**</span><span class="sxs-lookup"><span data-stu-id="c0e76-330">**Line 2:**</span></span>

            - <span data-ttu-id="c0e76-331">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0e76-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="c0e76-332">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0e76-332">**Site:** *6*</span></span>
            - <span data-ttu-id="c0e76-333">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="c0e76-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="c0e76-334">**Lokation:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="c0e76-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="c0e76-335">**Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.</span><span class="sxs-lookup"><span data-stu-id="c0e76-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="c0e76-336">**Antal:** *15*</span><span class="sxs-lookup"><span data-stu-id="c0e76-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="c0e76-337">**Linje 3:**</span><span class="sxs-lookup"><span data-stu-id="c0e76-337">**Line 3:**</span></span>

            - <span data-ttu-id="c0e76-338">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c0e76-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="c0e76-339">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="c0e76-339">**Site:** *6*</span></span>
            - <span data-ttu-id="c0e76-340">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="c0e76-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="c0e76-341">**Lokation:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="c0e76-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="c0e76-342">**Nummerplade:** Vælg en eksisterende nummerplade på listen, eller opret en ny nummerplade.</span><span class="sxs-lookup"><span data-stu-id="c0e76-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="c0e76-343">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="c0e76-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="c0e76-344">Vælg **Valider** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c0e76-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="c0e76-345">Løs eventuelle fejl, der findes, før du går videre til næste trin.</span><span class="sxs-lookup"><span data-stu-id="c0e76-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="c0e76-346">I handlingsruden skal du vælge **Bogfør** for at postere lageret til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="c0e76-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="c0e76-347">Eksempelscenarie: Kør zonebaseret min-/maks.-genopfyldning</span><span class="sxs-lookup"><span data-stu-id="c0e76-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="c0e76-348">Når alle de nødvendige eksempeldata er på plads, kan du udløse genopfyldning ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c0e76-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="c0e76-349">Gå til **Lokationsstyring \> Genopfyldning \> Genopfyldninger**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="c0e76-350">I dialogboksen **Genopfyldning** skal du i oversigtspanelet **Poster, der skal indgå** vælge **Filter**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="c0e76-351">I dialogboksen **Forespørgsel** skal du under fanen **Område** redigere standardtabelrækken på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c0e76-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="c0e76-352">**Tabel:** Vælg _Genopfyldningsskabeloner_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="c0e76-353">**Afledt tabel:** Vælg _Genofyldningsskabeloner_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="c0e76-354">**Felt:** Vælg _Genopfyldningsskabelon_.</span><span class="sxs-lookup"><span data-stu-id="c0e76-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="c0e76-355">**Kriterier:** Vælg _Zone – min./maks. genopfyld._.</span><span class="sxs-lookup"><span data-stu-id="c0e76-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="c0e76-356">Denne genopfyldningsskabelon er den genopfyldningsskabelon, du oprettede, mens du forberedte demodataene til dette scenarie.</span><span class="sxs-lookup"><span data-stu-id="c0e76-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="c0e76-357">Vælg **OK** for at gemme forespørgslen, og gå tilbage til dialogboksen **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="c0e76-358">Vælg **OK** for at køre opfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="c0e76-359">Genopfyldningsarbejdet er nu oprettet til at plukke lager fra *MASSE*-zonen og genopfylde det zonen *PRODUKTION*.</span><span class="sxs-lookup"><span data-stu-id="c0e76-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="c0e76-360">Noter og tip</span><span class="sxs-lookup"><span data-stu-id="c0e76-360">Notes and tips</span></span>

<span data-ttu-id="c0e76-361">Her er nogle få noter og tip til arbejdet med funktionen:</span><span class="sxs-lookup"><span data-stu-id="c0e76-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="c0e76-362">Hvis du vil konfigurere genopfyldningsarbejde, der går til den ønskede zone, kan du sammenkæde linjer i genopfyldningsskabelonen og lokationsvejledningerne på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="c0e76-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="c0e76-363">Rediger forespørgslen efter lokationsvejledningens overskrift, og filtrer de valgte linjer på genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="c0e76-364">Brug en vejledningskode på linjen i genopfyldningsskabelonen, og kæd den sammen med læg på lager-lokationsvejledningen.</span><span class="sxs-lookup"><span data-stu-id="c0e76-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="c0e76-365">Hvis du bruger dynamiske lokationer, oprettes genopfyldningsarbejdet enten for den første tilgængelige lokation eller for en lokation, der allerede indeholder lager, hvis handlingen i lokationsvejledningen er konfigureret til at bruge strategien **Konsolider**.</span><span class="sxs-lookup"><span data-stu-id="c0e76-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="c0e76-366">Hvis du bruger faste lokationer i stedet for zoner, skal du bruge [standard-min./maks. for genopfyldning](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="c0e76-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
