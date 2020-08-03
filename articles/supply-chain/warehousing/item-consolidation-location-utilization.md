---
title: Udnyttelse af varekonsolideringslokation
description: Dette emne indeholder oplysninger om funktioner, der gør det nemt for lagerchefer at få vist og filtrere volumetrisk anvendelse af lokationer på tværs af lagerstedet. Ledere kan vælge lokationer og oprette lagerbevægelse direkte fra siden siden Varekonsolidering for at konsolidere varer og dermed udnytte lagerstedets areal bedre.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5e4172a8d3f82e6eeb8868aac87abd183a94c088
ms.sourcegitcommit: 14b554b43b9d86152ef27fdde6141589bcaf1161
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3598779"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="10ba9-104">Udnyttelse af varekonsolideringslokation</span><span class="sxs-lookup"><span data-stu-id="10ba9-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10ba9-105">Dette emne indeholder oplysninger om funktioner, der gør det nemt for lagerchefer at få vist og filtrere volumetrisk anvendelse af lokationer på tværs af lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="10ba9-106">Ledere kan vælge lokationer og oprette lagerbevægelse direkte fra siden **Varekonsolidering** for at konsolidere varer og dermed udnytte lagerstedets areal bedre.</span><span class="sxs-lookup"><span data-stu-id="10ba9-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="10ba9-107">Slå funktionerne til</span><span class="sxs-lookup"><span data-stu-id="10ba9-107">Turn on the features</span></span>

<span data-ttu-id="10ba9-108">Før du kan bruge de funktioner, der er beskrevet i dette emne, skal du aktivere dem i systemet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="10ba9-109">Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges.</span><span class="sxs-lookup"><span data-stu-id="10ba9-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="10ba9-110">Slå begge af følgende funktioner til i den rækkefølge, de angives i.</span><span class="sxs-lookup"><span data-stu-id="10ba9-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="10ba9-111">(Begge funktioner er til modulet **Lokationsstyring**).</span><span class="sxs-lookup"><span data-stu-id="10ba9-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="10ba9-112">Placeringsstatus for lagersted</span><span class="sxs-lookup"><span data-stu-id="10ba9-112">Warehouse location status</span></span>
2. <span data-ttu-id="10ba9-113">Udnyttelse af varekonsolideringslokation</span><span class="sxs-lookup"><span data-stu-id="10ba9-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="10ba9-114">Placeringsstatus for lagersted</span><span class="sxs-lookup"><span data-stu-id="10ba9-114">Warehouse location status</span></span>

<span data-ttu-id="10ba9-115">Funktionen *Placeringsstatus for lagersted* føjer fire nye felter til siden **Lokationer** for at spore yderligere oplysninger om den aktuelle status for lokationen:</span><span class="sxs-lookup"><span data-stu-id="10ba9-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="10ba9-116">**Varenummer** – den vare, der i øjeblikket findes på lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="10ba9-117">Hvis lokationen indeholder flere varer, er feltet tomt.</span><span class="sxs-lookup"><span data-stu-id="10ba9-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="10ba9-118">**Dato og klokkeslæt for seneste aktivitet** – tidsstemplet for den sidste lagertransaktion, der blev udført i forhold til lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="10ba9-119">**Forældelsesdato** – den dato, hvor lagerbeholdingen på lokationen blev bragt ind på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="10ba9-120">Denne dato beregnes på basis af den aldersfordelte dato for nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="10ba9-121">Selvom denne dato er nøjagtig for lokationer, hvor nummerpladen bruges til sporing, men er muligvis ikke nøjagtig for lokationer, hvor nummerpladen ikke bruges til sporing.</span><span class="sxs-lookup"><span data-stu-id="10ba9-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="10ba9-122">**Lokationsstatus** – statussen for lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="10ba9-123">Fire værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="10ba9-123">Four values are available:</span></span>

    - <span data-ttu-id="10ba9-124">**Ikke fastlagt** – lokationsprofilen sporer ikke status.</span><span class="sxs-lookup"><span data-stu-id="10ba9-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="10ba9-125">Derfor er den aktuelle status ukendt.</span><span class="sxs-lookup"><span data-stu-id="10ba9-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="10ba9-126">**Tom** – der er i øjeblikket ingen lagerbeholdning på lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="10ba9-127">**Pluk** – der er udført udgående transaktioner i forhold til lokationen, efter den sidst var tom.</span><span class="sxs-lookup"><span data-stu-id="10ba9-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="10ba9-128">**Lager** – der er kun udført indgående transaktioner, siden den sidst var tom.</span><span class="sxs-lookup"><span data-stu-id="10ba9-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="10ba9-129">Disse felter giver lagerchefer mulighed for at få et bedre overblik over statussen på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="10ba9-130">De giver også mulighed for mere avanceret rapportering og filtrering.</span><span class="sxs-lookup"><span data-stu-id="10ba9-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="10ba9-131">Konfigurere varekonsolidering og lokationsudnyttelse</span><span class="sxs-lookup"><span data-stu-id="10ba9-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="10ba9-132">I dette afsnit beskrives, hvordan du forbereder dit system til at bruge varekonsolidering og lokationsudnyttelse.</span><span class="sxs-lookup"><span data-stu-id="10ba9-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="10ba9-133">Procedurerne bruger eksempelværdier fra standarddemodataene.</span><span class="sxs-lookup"><span data-stu-id="10ba9-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="10ba9-134">Hvis du planlægger at arbejde dig gennem det eksempelscenarie, der er angivet senere i dette emne, skal du vælge den juridiske enhed **USMF** (som indeholder standarddemodataene) og oprette de enkelte poster, der er beskrevet i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="10ba9-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="10ba9-135">Hvis du ikke planlægger at arbejde dig gennem eksempelscenariet, kan de værdier, der angives her, betragtes som eksempler på de typer af opsætning, du skal udføre for at kunne bruge funktionerne.</span><span class="sxs-lookup"><span data-stu-id="10ba9-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="10ba9-136">Frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="10ba9-136">Released product</span></span>

1. <span data-ttu-id="10ba9-137">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="10ba9-138">Gå til feltet **Varenummer**, vælg *M9201*, og åbn detaljesiden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="10ba9-139">I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="10ba9-140">Gå til siden **Fysiske dimensioner**, og vælg **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="10ba9-141">Der føjes en ny linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="10ba9-141">A new line is added to the grid.</span></span> <span data-ttu-id="10ba9-142">Feltet **Varenummer** er foruddefineret.</span><span class="sxs-lookup"><span data-stu-id="10ba9-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="10ba9-143">Vælg **hver** i feltet *Enhed*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="10ba9-144">De resterende felter på linjen angives automatisk.</span><span class="sxs-lookup"><span data-stu-id="10ba9-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="10ba9-145">Vælg **Gem**, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="10ba9-146">Lokationsprofil</span><span class="sxs-lookup"><span data-stu-id="10ba9-146">Location profile</span></span>

1. <span data-ttu-id="10ba9-147">Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="10ba9-148">Vælg **PRODUKTION-05** på listen over lokationsprofiler.</span><span class="sxs-lookup"><span data-stu-id="10ba9-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="10ba9-149">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="10ba9-150">Gå til oversigtspaneletI **Generelt**, og sørg for, at følgende indstillinger er angivet til *Ja*:</span><span class="sxs-lookup"><span data-stu-id="10ba9-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="10ba9-151">Aktivér vare på placering</span><span class="sxs-lookup"><span data-stu-id="10ba9-151">Enable item in location</span></span>
    - <span data-ttu-id="10ba9-152">Aktivér placeringsstatus</span><span class="sxs-lookup"><span data-stu-id="10ba9-152">Enable location status</span></span>

1. <span data-ttu-id="10ba9-153">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="10ba9-154">Hvis indstillingen **Aktivér vare på lokation** og **Indstillinger for lokationsstatus** allerede er angivet til *Ja*, skal du gå videre til instruktionerne for opsætning af oversigtspanelet **Dimensioner** i trin 10.</span><span class="sxs-lookup"><span data-stu-id="10ba9-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="10ba9-155">Hvis indstillingerne ikke allerede er angivet til *Ja*, skal du udføre en konsistenskontrol for modulet **Lokationsstyring**, når du har angivet dem manuelt.</span><span class="sxs-lookup"><span data-stu-id="10ba9-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="10ba9-156">I dette tilfælde skal du fortsætte til næste trin.</span><span class="sxs-lookup"><span data-stu-id="10ba9-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="10ba9-157">Hvis du vil køre konsistenskontrollen, skal du gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="10ba9-158">Angiv følgende værdier i dialogboksen **Konsistenskontrol**:</span><span class="sxs-lookup"><span data-stu-id="10ba9-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="10ba9-159">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="10ba9-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="10ba9-160">**Kontrollér/ret:** *Kontrol*</span><span class="sxs-lookup"><span data-stu-id="10ba9-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="10ba9-161">**Fra dato** – Lad dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="10ba9-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="10ba9-162">**Konsistenskontrol af placeringsstatus for lagersted:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="10ba9-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="10ba9-163">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="10ba9-164">Når konsistenskontrollen er udført, modtager du en besked.</span><span class="sxs-lookup"><span data-stu-id="10ba9-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="10ba9-165">Åbn [Handlingscenter](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) for at få vist meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="10ba9-166">Vælg **Meddelelsesdetaljer** for at få vist detaljerne.</span><span class="sxs-lookup"><span data-stu-id="10ba9-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="10ba9-167">Hvis meddelelsen for konsistenskontrollen angive, at der er "fundet forkerte statusoplysninger for lokationen for lokation XXXX i lager XX", skal du køre konsistenskontrollen igen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="10ba9-168">Denne gang skal du angive feltet **Kontrollér/ret** til *Ret fejl*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="10ba9-169">Få vist meddelelserne for at sikre dig, at der ikke blev fundet fejl.</span><span class="sxs-lookup"><span data-stu-id="10ba9-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="10ba9-170">Du skal nu afslutte konfigurationen af lokationsprofilen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="10ba9-171">Gå tilbage til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**, vælg lokationsprofilen **PRODUKTION-05**, og vælg derefter **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="10ba9-172">I oversigtspanelet **Dimensioner** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="10ba9-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="10ba9-173">**Volumenudnyttelse i procent:** *100*</span><span class="sxs-lookup"><span data-stu-id="10ba9-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="10ba9-174">**Volumetrisk metode, der anvendes til lagerlokation:** *Brug lokationsvolumen*</span><span class="sxs-lookup"><span data-stu-id="10ba9-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="10ba9-175">**Lokationens faktiske højde:** *10*</span><span class="sxs-lookup"><span data-stu-id="10ba9-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="10ba9-176">**Lokationens faktiske bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="10ba9-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="10ba9-177">**Lokationens faktiske dybde:** *10*</span><span class="sxs-lookup"><span data-stu-id="10ba9-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="10ba9-178">**Maks. vægt:** *100*</span><span class="sxs-lookup"><span data-stu-id="10ba9-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="10ba9-179">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="10ba9-180">Menupunkter i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="10ba9-180">Mobile device menu items</span></span>

1. <span data-ttu-id="10ba9-181">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="10ba9-182">Vælg **Ny** i handlingsruden for at oprette et menupunkt til sortering.</span><span class="sxs-lookup"><span data-stu-id="10ba9-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="10ba9-183">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="10ba9-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="10ba9-184">**Navn på menupunkt:** *Regulering i*</span><span class="sxs-lookup"><span data-stu-id="10ba9-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="10ba9-185">**Titel:** *Reguler i*</span><span class="sxs-lookup"><span data-stu-id="10ba9-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="10ba9-186">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="10ba9-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="10ba9-187">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="10ba9-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="10ba9-188">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="10ba9-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="10ba9-189">**Arbejdsgang for oprettelse:** *Regulering ind*</span><span class="sxs-lookup"><span data-stu-id="10ba9-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="10ba9-190">**Typer af lagerreguleringer:** *Reguler ind*</span><span class="sxs-lookup"><span data-stu-id="10ba9-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="10ba9-191">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="10ba9-192">Menu i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="10ba9-192">Mobile device menu</span></span>

1. <span data-ttu-id="10ba9-193">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="10ba9-194">Vælg **Lager** på listen over menuer.</span><span class="sxs-lookup"><span data-stu-id="10ba9-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="10ba9-195">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="10ba9-196">På listen **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Reguler ind**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="10ba9-197">Vælg den højre piletast for at flytte **Reguler ind** til listen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="10ba9-198">På denne måde føjer du det nye menupunkt til den valgte menu.</span><span class="sxs-lookup"><span data-stu-id="10ba9-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="10ba9-199">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="10ba9-200">Bevægelsestyper</span><span class="sxs-lookup"><span data-stu-id="10ba9-200">Movement types</span></span>

1. <span data-ttu-id="10ba9-201">Gå til **Lokationsstyring \> Opsætning \> Lager \> Bevægelsestyper**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="10ba9-202">I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="10ba9-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="10ba9-203">**Kode for bevægelsestype:** *KONSOLIDER*</span><span class="sxs-lookup"><span data-stu-id="10ba9-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="10ba9-204">**Beskrivelse:** *Konsolider lokationer*</span><span class="sxs-lookup"><span data-stu-id="10ba9-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="10ba9-205">**Arbejdsklasse-id:** *LagBev*</span><span class="sxs-lookup"><span data-stu-id="10ba9-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="10ba9-206">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="10ba9-207">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="10ba9-207">Example scenario</span></span>

<span data-ttu-id="10ba9-208">I følgende scenarie bruges lagerstedsappen på en mobilenhed, når der foretages en *regulering ind* for lager på to lokationer på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="10ba9-209">Føj lager til lagerlokationer</span><span class="sxs-lookup"><span data-stu-id="10ba9-209">Add inventory to locations</span></span>

1. <span data-ttu-id="10ba9-210">Log på mobilenheden som en bruger, der er konfigureret til lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="10ba9-211">Gå til **Lager \> Reguler ind**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="10ba9-212">Du skal nu angive den første lokationsregulering.</span><span class="sxs-lookup"><span data-stu-id="10ba9-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="10ba9-213">I opgaven **Regulering ind** skal du vælge den lokation, som lagerreguleringen skal foretages for.</span><span class="sxs-lookup"><span data-stu-id="10ba9-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="10ba9-214">I feltet **LOK** skal du vælge *NP-001*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="10ba9-215">Bekræft lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-215">Confirm the location.</span></span>
1. <span data-ttu-id="10ba9-216">Opret et nummerplade-id for den vare, der skal føjes til lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="10ba9-217">I feltet **NP** skal du angive *NP00101*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="10ba9-218">Bekræft nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="10ba9-219">Angiv den vare, der skal føjes til nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="10ba9-220">I feltet **ITEM** skal du angive *M9201*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="10ba9-221">Bekræft varen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-221">Confirm the item.</span></span>
1. <span data-ttu-id="10ba9-222">Angiv det antal af varen, der bliver tilføjet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="10ba9-223">I feltet **Antal** skal du angive *10*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="10ba9-224">Bekræft antallet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-224">Confirm the quantity.</span></span>

    <span data-ttu-id="10ba9-225">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="10ba9-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="10ba9-226">Du skal nu angive den anden lokationsregulering.</span><span class="sxs-lookup"><span data-stu-id="10ba9-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="10ba9-227">I opgaven **Regulering ind** skal du vælge den lokation, som lagerreguleringen skal foretages for.</span><span class="sxs-lookup"><span data-stu-id="10ba9-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="10ba9-228">I feltet **LOK** skal du vælge *NP-002*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="10ba9-229">Bekræft lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-229">Confirm the location.</span></span>
1. <span data-ttu-id="10ba9-230">Opret et nummerplade-id for den vare, der skal føjes til lokationen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="10ba9-231">I feltet **NP** skal du angive *NP00201*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="10ba9-232">Bekræft nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="10ba9-233">Angiv den vare, der skal føjes til nummerpladen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="10ba9-234">I feltet **ITEM** skal du angive *M9201*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="10ba9-235">Bekræft varen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-235">Confirm the item.</span></span>
1. <span data-ttu-id="10ba9-236">Angiv det antal af varen, der bliver tilføjet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="10ba9-237">I feltet **Antal** skal du angive *15*.</span><span class="sxs-lookup"><span data-stu-id="10ba9-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="10ba9-238">Bekræft antallet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-238">Confirm the quantity.</span></span>

    <span data-ttu-id="10ba9-239">Du modtager en meddelelse om arbejde fuldført.</span><span class="sxs-lookup"><span data-stu-id="10ba9-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="10ba9-240">Vælg menuknappen (kaldes også hamburger eller hamburgerknappen), og vælg derefter **Annuller** for at afslutte opgaven **Regulering i**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="10ba9-241">Konsolidere lokationer</span><span class="sxs-lookup"><span data-stu-id="10ba9-241">Consolidate locations</span></span>

1. <span data-ttu-id="10ba9-242">Gå til **Lagerstyring \> Periodiske opgaver for \> Varekonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="10ba9-243">Vælg et lagersted, som konsolideringen skal udføres for, i overskriften.</span><span class="sxs-lookup"><span data-stu-id="10ba9-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="10ba9-244">Angiv *51* i feltet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="10ba9-245">Der vises en post for hver lokation, hvor varen *M9201* blev reguleret.</span><span class="sxs-lookup"><span data-stu-id="10ba9-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="10ba9-246">Kolonnen **Udnyttelsesgrad** viser den enkelte lokations volumetriske udnyttelse.</span><span class="sxs-lookup"><span data-stu-id="10ba9-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="10ba9-247">Hvis du vil konsolidere lagerbeholdning, skal du vælge alle de lokationer, der skal konsolideres, og derefter skal du vælge **Konsolider lager** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="10ba9-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="10ba9-248">I dialogboksen **Konsolider lager** skal du angive lokationen og bevægelsestypen, der skal bruges til at oprette arbejdet for lagerbevægelsen.</span><span class="sxs-lookup"><span data-stu-id="10ba9-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="10ba9-249">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="10ba9-249">Set the following values:</span></span>

    - <span data-ttu-id="10ba9-250">**Lokation:** *NP-001*</span><span class="sxs-lookup"><span data-stu-id="10ba9-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="10ba9-251">**Kode for bevægelsestype:** *KONSOLIDER*</span><span class="sxs-lookup"><span data-stu-id="10ba9-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="10ba9-252">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-252">Select **OK**.</span></span>
1. <span data-ttu-id="10ba9-253">Du modtager en meddelelse med oplysninger, der viser det udførte bevægelsesarbejde.</span><span class="sxs-lookup"><span data-stu-id="10ba9-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="10ba9-254">Notér dig bevægelsesarbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="10ba9-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="10ba9-255">Få vist bevægelsesarbejde</span><span class="sxs-lookup"><span data-stu-id="10ba9-255">View movement work</span></span>

1. <span data-ttu-id="10ba9-256">Gå til **Lokationsstyring \> Arbejde \> Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="10ba9-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="10ba9-257">Få vist det arbejde, der blev oprettet.</span><span class="sxs-lookup"><span data-stu-id="10ba9-257">View the work that was created.</span></span> <span data-ttu-id="10ba9-258">Brug bevægelsesarbejds-id'et fra lagerkonsolideringen til at filtrere eller søge i arbejdsgitteret.</span><span class="sxs-lookup"><span data-stu-id="10ba9-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="10ba9-259">I dette scenarie blev der brugt en eksisterende lokation, som har haft en lagerbeholdning, der blev brugt som lagerkonsolideringslokation.</span><span class="sxs-lookup"><span data-stu-id="10ba9-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="10ba9-260">Derfor er der kun oprettet ét arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="10ba9-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="10ba9-261">Systemet opretter et arbejds-id for hver flytning, der skal fuldføres.</span><span class="sxs-lookup"><span data-stu-id="10ba9-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="10ba9-262">Hvis du angiver en lokation, der allerede indeholder lager, oprettes der kun ét arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="10ba9-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="10ba9-263">Hvis du angiver en ny lokation, oprettes der to arbejds-id'er.</span><span class="sxs-lookup"><span data-stu-id="10ba9-263">If you specify a new location, two work IDs are created.</span></span>
