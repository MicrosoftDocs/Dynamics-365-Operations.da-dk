---
title: Læg på lager-klynger
description: Læg på lager-klynger giver mulighed for at plukke flere id'er samtidigt og derefter tage dem til læg på lager forskellige steder. De kan være meget nyttige for detailforretninger, hvor id'erne typisk ikke er fulde lagerpaller.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996192"
---
# <a name="putaway-clusters"></a><span data-ttu-id="425d4-104">Læg på lager-klynger</span><span class="sxs-lookup"><span data-stu-id="425d4-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="425d4-105">Læg på lager-klynger giver mulighed for at plukke flere id'er samtidigt og derefter tage dem til læg på lager forskellige steder.</span><span class="sxs-lookup"><span data-stu-id="425d4-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="425d4-106">Denne proces omtales ofte som en *leveringsrute*.</span><span class="sxs-lookup"><span data-stu-id="425d4-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="425d4-107">Læg på lager-klynger kan være meget nyttige for detailforretninger, hvor id'erne typisk ikke er fulde lagerpaller.</span><span class="sxs-lookup"><span data-stu-id="425d4-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="425d4-108">Aktivere funktionen læg på lager-klynge</span><span class="sxs-lookup"><span data-stu-id="425d4-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="425d4-109">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="425d4-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="425d4-110">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="425d4-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="425d4-111">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="425d4-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="425d4-112">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="425d4-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="425d4-113">**Funktionsnavn:** *Funktionen læg på lager-klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="425d4-114">Konfiguration af eksempelscenariet</span><span class="sxs-lookup"><span data-stu-id="425d4-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="425d4-115">Klyngeprofiler</span><span class="sxs-lookup"><span data-stu-id="425d4-115">Cluster profiles</span></span>

<span data-ttu-id="425d4-116">Læg på lager-klyngeprofilen bestemmer, hvor en vare placeres, på baggrund af den lokation, der er tildelt varen på modtagelsestidspunktet.</span><span class="sxs-lookup"><span data-stu-id="425d4-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="425d4-117">Hvis der kræves forskellige klynger, skal der oprettes andre læg på lager-klynger, én for hvert menupunkt på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="425d4-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="425d4-118">Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Klyngeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="425d4-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="425d4-119">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="425d4-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="425d4-120">Angiv følgende værdier i visningen **Overskrift**:</span><span class="sxs-lookup"><span data-stu-id="425d4-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="425d4-121">**Læg på lager-klyngeprofil-id:** *Læg på lager-klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="425d4-122">**Læg på lager-klyngeprofil-id-navn:** *Læg på lager-klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="425d4-123">**Klyngetype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="425d4-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="425d4-124">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="425d4-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="425d4-125">Vælg **Gem** for at gøre de påkrævede felter i oversigtspanelet **Generelt** tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="425d4-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="425d4-126">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="425d4-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="425d4-127">**Tidsindstilling for klyngetildeling:** *Ved modtagelse*</span><span class="sxs-lookup"><span data-stu-id="425d4-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="425d4-128">Dette felt definerer, om læg på lager-klyngen skal tildeles med det samme, når lageret modtages, eller om det skal gøres senere.</span><span class="sxs-lookup"><span data-stu-id="425d4-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="425d4-129">**Regel for klyngetildeling:** *Manuel*</span><span class="sxs-lookup"><span data-stu-id="425d4-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="425d4-130">Dette felt definerer, om klyngetildelingen skal registreres automatisk af systemet eller manuelt af brugeren.</span><span class="sxs-lookup"><span data-stu-id="425d4-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="425d4-131">**Vejledningskode:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="425d4-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="425d4-132">**Find Læg på lager-klynge:** *Modtagelse*</span><span class="sxs-lookup"><span data-stu-id="425d4-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="425d4-133">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="425d4-133">The following values are available:</span></span>

        - <span data-ttu-id="425d4-134">**Modtagelse** – En lokation blev fundet umiddelbart under modtagelsen.</span><span class="sxs-lookup"><span data-stu-id="425d4-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="425d4-135">**Klyngelukning** – En lokation findes, når klyngen lukkes.</span><span class="sxs-lookup"><span data-stu-id="425d4-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="425d4-136">**Brugerstyret** – Der findes en lokation, når id'et plukkes fra klyngen for læg på lager.</span><span class="sxs-lookup"><span data-stu-id="425d4-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="425d4-137">I dette tilfælde er der ikke angivet en lokation, når det læg på lager-arbejde oprettes.</span><span class="sxs-lookup"><span data-stu-id="425d4-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="425d4-138">Under selve læg på lager skal brugeren scanne nummerpladen-id eller arbejds-id for at starte læg på lager-trinnet.</span><span class="sxs-lookup"><span data-stu-id="425d4-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="425d4-139">Systemet finder derefter læg på lager-lokationen igen og fortæller brugeren, hvor det plukkede antal skal placeres.</span><span class="sxs-lookup"><span data-stu-id="425d4-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="425d4-140">**Læg på lager-klynge pr. bruger:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="425d4-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="425d4-141">Dette felt definerer, om de enkelte klynger skal være entydige pr. bruger, når klynger tildeles automatisk.</span><span class="sxs-lookup"><span data-stu-id="425d4-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="425d4-142">Den er kun tilgængelig, når feltet **Klyngetildelingsregel** er angivet til *Automatisk*.</span><span class="sxs-lookup"><span data-stu-id="425d4-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="425d4-143">**Enhedsbegrænsning:** Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="425d4-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="425d4-144">I dette felt defineres den enhed, der skal være modtaget, for at profilen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="425d4-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="425d4-145">Hvis det er tomt, vil alle enheder være gyldige.</span><span class="sxs-lookup"><span data-stu-id="425d4-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="425d4-146">**Opdeling af arbejdsenhed:** *Individuel*</span><span class="sxs-lookup"><span data-stu-id="425d4-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="425d4-147">Dette felt definerer, om al lagerbeholdning skal konsolideres (ved hjælp af klynge-id og nummerplade-) på én nummerplade, når en klynge lukkes, og om den skal lægges på lager som en enkelt nummerplade eller separat på de nummerplader, der er modtaget.</span><span class="sxs-lookup"><span data-stu-id="425d4-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="425d4-148">Dette felt er ikke tilgængeligt, når feltet **Find Læg på lager-klynge** er angivet til *Modtagelse*.</span><span class="sxs-lookup"><span data-stu-id="425d4-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="425d4-149">**Klyngen fortsætter som overordnet id:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="425d4-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="425d4-150">Hvis denne indstilling er angivet til *Ja*, når læg på lager-trinnet udføres, bliver klynge-id'et til et overordnet nummerplade-id, og alle varer i klynge-id'et vil blive knyttet til dette id.</span><span class="sxs-lookup"><span data-stu-id="425d4-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="425d4-151">I oversigtspanelet **Klyngesortering** kan du definere sorteringskriterier for læg på lager.</span><span class="sxs-lookup"><span data-stu-id="425d4-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="425d4-152">Vælg **Ny** på værktøjslinjen for at tilføje en linje, og angiv derefter følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="425d4-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="425d4-153">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="425d4-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="425d4-154">**Feltnavn:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="425d4-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="425d4-155">Dette felt definerer det felt, som denne linje skal bruge som sorteringskriterium.</span><span class="sxs-lookup"><span data-stu-id="425d4-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="425d4-156">**Sortering:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="425d4-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="425d4-157">Dette felt definerer, om sorteringen skal udføres i stigende eller faldende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="425d4-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="425d4-158">I oversigtspanelet **Arbejdsskabelon for klynge** skal du vælge **Ny** på værktøjslinjen for at tilføje en linje og derefter angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="425d4-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="425d4-159">**Arbejdsordretype:** *Indkøbsordrer*</span><span class="sxs-lookup"><span data-stu-id="425d4-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="425d4-160">**Arbejdsskabelon:** *61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="425d4-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="425d4-161">Vælg **Gem** i handlingsruden, og vælg derefter **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="425d4-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="425d4-162">I dialogboksen **Læg på lager-klynge** skal du under fanen **Interval** vælge **Tilføj** for at tilføje endnu en linje i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="425d4-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="425d4-163">Opdater derefter forespørgselslinjerne som vist i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="425d4-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="425d4-164">Tabellen</span><span class="sxs-lookup"><span data-stu-id="425d4-164">Table</span></span> | <span data-ttu-id="425d4-165">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="425d4-165">Derived table</span></span> | <span data-ttu-id="425d4-166">Felt</span><span class="sxs-lookup"><span data-stu-id="425d4-166">Field</span></span> | <span data-ttu-id="425d4-167">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="425d4-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="425d4-168">Arbejde</span><span class="sxs-lookup"><span data-stu-id="425d4-168">Work</span></span> | <span data-ttu-id="425d4-169">Arbejde</span><span class="sxs-lookup"><span data-stu-id="425d4-169">Work</span></span> | <span data-ttu-id="425d4-170">Lagersted</span><span class="sxs-lookup"><span data-stu-id="425d4-170">Warehouse</span></span> | <span data-ttu-id="425d4-171">*61*</span><span class="sxs-lookup"><span data-stu-id="425d4-171">*61*</span></span> |
    | <span data-ttu-id="425d4-172">Arbejde</span><span class="sxs-lookup"><span data-stu-id="425d4-172">Work</span></span> | <span data-ttu-id="425d4-173">Arbejde</span><span class="sxs-lookup"><span data-stu-id="425d4-173">Work</span></span> | <span data-ttu-id="425d4-174">Arbejds-id</span><span class="sxs-lookup"><span data-stu-id="425d4-174">Work ID</span></span> | <span data-ttu-id="425d4-175">Lad feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="425d4-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="425d4-176">Vælg **OK** for at gemme forespørgslen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="425d4-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="425d4-177">Vælg **Gem** i handlingsruden, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="425d4-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="425d4-178">De felter i klyngeprofilen, der vises nedtonet, når **Generér klynge-id** er angivet til *Ja*, er ikke tilgængelige og tages ikke med i betragtning, når denne funktion bruges.</span><span class="sxs-lookup"><span data-stu-id="425d4-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="425d4-179">Menupunkter i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="425d4-179">Mobile device menu items</span></span>

<span data-ttu-id="425d4-180">Der findes to nye menupunkter for mobilenheder til denne funktion.</span><span class="sxs-lookup"><span data-stu-id="425d4-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="425d4-181">Menupunktet **Modtag og sortér klynge** bruges til at sortere den modtagne lagerbeholdning til en læg på lager-klynge ved modtagelse.</span><span class="sxs-lookup"><span data-stu-id="425d4-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="425d4-182">Menupunktet **Læg på lager-klynge** bruges til at lægge klyngen på lager, efter at den er tildelt.</span><span class="sxs-lookup"><span data-stu-id="425d4-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="425d4-183">Modtage og sortere klynge</span><span class="sxs-lookup"><span data-stu-id="425d4-183">Receive and sort cluster</span></span>

<span data-ttu-id="425d4-184">Opret et nyt menupunkt til mobilenheder til modtagelse af lager og sortering i en klynge.</span><span class="sxs-lookup"><span data-stu-id="425d4-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="425d4-185">Dette menupunkt opretter indgående arbejde, efter at der er modtaget en lagerbeholdning, hvilket angiver, at det modtagende menupunkt bruges til læg på lager-klynger.</span><span class="sxs-lookup"><span data-stu-id="425d4-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="425d4-186">Menupunktet **Modtag og sortér klynge** kan bruges sammen med følgende elementer til modtagelse af menupunkter:</span><span class="sxs-lookup"><span data-stu-id="425d4-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="425d4-187">Indkøbsordrelinje til modtagelse</span><span class="sxs-lookup"><span data-stu-id="425d4-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="425d4-188">Indkøbsordrevare til modtagelse</span><span class="sxs-lookup"><span data-stu-id="425d4-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="425d4-189">Modtagelse af varelast</span><span class="sxs-lookup"><span data-stu-id="425d4-189">Load item receiving</span></span>

1. <span data-ttu-id="425d4-190">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="425d4-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="425d4-191">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="425d4-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="425d4-192">Angiv følgende værdier i visningen **Overskrift**:</span><span class="sxs-lookup"><span data-stu-id="425d4-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="425d4-193">**Navn på menupunkt:** *Modtag og sortér klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="425d4-194">**Titel:** *Modtag og sortér klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="425d4-195">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="425d4-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="425d4-196">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="425d4-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="425d4-197">I oversigtspanelet **Generelt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="425d4-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="425d4-198">**Arbejdsoprettelsesproces:** *Indkøbsordrevare til modtagelse*</span><span class="sxs-lookup"><span data-stu-id="425d4-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="425d4-199">**Generer nummerplade:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="425d4-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="425d4-200">**Tildel læg på lager-klynge:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="425d4-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="425d4-201">Indstillingen **Tildel læg på lager-klynge** er kun tilgængelig i forbindelse med aktiviteten *Arbejdsoprettelsesproces* for modtagelse.</span><span class="sxs-lookup"><span data-stu-id="425d4-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="425d4-202">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="425d4-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="425d4-203">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="425d4-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="425d4-204">Klynge for Læg på lager</span><span class="sxs-lookup"><span data-stu-id="425d4-204">Cluster putaway</span></span>

<span data-ttu-id="425d4-205">Opret et nyt menupunkt til mobilenheder til at lægge klyngen på lager, efter at den er tildelt.</span><span class="sxs-lookup"><span data-stu-id="425d4-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="425d4-206">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="425d4-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="425d4-207">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="425d4-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="425d4-208">Angiv følgende værdier i visningen **Overskrift**:</span><span class="sxs-lookup"><span data-stu-id="425d4-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="425d4-209">**Menupunktnavn:** *Læg på lager-klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="425d4-210">**Titel:** *Læg på lager-klynge*</span><span class="sxs-lookup"><span data-stu-id="425d4-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="425d4-211">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="425d4-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="425d4-212">**Brug eksisterende arbejde:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="425d4-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="425d4-213">I oversigtspanelet **Generelt** skal du indstille feltet **Styret af** til *Læg på lager-klynge*.</span><span class="sxs-lookup"><span data-stu-id="425d4-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="425d4-214">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="425d4-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="425d4-215">Konfigurer den gyldige arbejdsklasse for dette menupunkt i mobilenheden i oversigtspanelet **Arbejdsklasser**:</span><span class="sxs-lookup"><span data-stu-id="425d4-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="425d4-216">**Arbejdsklasse-id:** *Indkøb*</span><span class="sxs-lookup"><span data-stu-id="425d4-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="425d4-217">**Arbejdsordretype:** *Indkøbsordrer*</span><span class="sxs-lookup"><span data-stu-id="425d4-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="425d4-218">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="425d4-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="425d4-219">Menu i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="425d4-219">Mobile device menu</span></span>

<span data-ttu-id="425d4-220">Tilføj de menupunkter, du netop har oprettet, i menuen Indgående i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="425d4-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="425d4-221">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="425d4-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="425d4-222">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="425d4-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="425d4-223">Vælg **Indgående** på menulisten.</span><span class="sxs-lookup"><span data-stu-id="425d4-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="425d4-224">På listen **Tilgængelige menuer og menupunkter** skal du finde og vælge **Modtag og sortér klynge**.</span><span class="sxs-lookup"><span data-stu-id="425d4-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="425d4-225">Vælg den højre pileknap for at flytte menupunktet til listen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="425d4-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="425d4-226">Brug knappen Pil op eller Pil ned til at flytte menupunktet til den ønskede placering i menuen.</span><span class="sxs-lookup"><span data-stu-id="425d4-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="425d4-227">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="425d4-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="425d4-228">Gentag trin 4-7 for at tilføje de resterende menupunkter.</span><span class="sxs-lookup"><span data-stu-id="425d4-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="425d4-229">Tildel klynge</span><span class="sxs-lookup"><span data-stu-id="425d4-229">Assign cluster</span></span>
    - <span data-ttu-id="425d4-230">Klynge for Læg på lager</span><span class="sxs-lookup"><span data-stu-id="425d4-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="425d4-231">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="425d4-231">Example scenario</span></span>

<span data-ttu-id="425d4-232">Dette scenario simulerer behandling af læg på lager-klyngen.</span><span class="sxs-lookup"><span data-stu-id="425d4-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="425d4-233">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="425d4-233">Create a purchase order</span></span>

1. <span data-ttu-id="425d4-234">Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="425d4-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="425d4-235">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="425d4-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="425d4-236">Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:</span><span class="sxs-lookup"><span data-stu-id="425d4-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="425d4-237">**Kreditorkonto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="425d4-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="425d4-238">**Lagersted:** *61*</span><span class="sxs-lookup"><span data-stu-id="425d4-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="425d4-239">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="425d4-239">Select **OK**.</span></span>

    <span data-ttu-id="425d4-240">Siden **Alle indkøbsordrer** vises.</span><span class="sxs-lookup"><span data-stu-id="425d4-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="425d4-241">På siden **Alle indkøbsordrer** i oversigtspanelet **Indkøbsordrelinjer** skal du bruge knappen **Tilføj linje** for at tilføje følgende linjer:</span><span class="sxs-lookup"><span data-stu-id="425d4-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="425d4-242">Indkøbsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="425d4-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="425d4-243">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="425d4-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="425d4-244">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="425d4-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="425d4-245">Indkøbsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="425d4-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="425d4-246">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="425d4-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="425d4-247">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="425d4-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="425d4-248">Indkøbsordrelinje 3:</span><span class="sxs-lookup"><span data-stu-id="425d4-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="425d4-249">**Varenummer:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="425d4-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="425d4-250">**Antal:** *30*</span><span class="sxs-lookup"><span data-stu-id="425d4-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="425d4-251">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="425d4-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="425d4-252">Notér dig købsordrenummeret.</span><span class="sxs-lookup"><span data-stu-id="425d4-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="425d4-253">Modtage lagerbeholdning og lægge det på lager fra mobilenheden</span><span class="sxs-lookup"><span data-stu-id="425d4-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="425d4-254">Modtage og sortere lageret i en klynge</span><span class="sxs-lookup"><span data-stu-id="425d4-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="425d4-255">Log på lagerstedsappen som en bruger, der er konfigureret til lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="425d4-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="425d4-256">I hovedmenuen skal du vælge **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="425d4-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="425d4-257">Vælg **Modtag og sortér klynge** i menuen **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="425d4-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="425d4-258">Angiv indkøbsordrenummeret i feltet **IO-num**.</span><span class="sxs-lookup"><span data-stu-id="425d4-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="425d4-259">Vælg knappen **OK** (markeringssymbol).</span><span class="sxs-lookup"><span data-stu-id="425d4-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="425d4-260">Vælg feltet **Vare**, angiv *A0001* som varenummeret, og vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="425d4-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="425d4-261">Vælg feltet **Antal**, indtast *10* på det numeriske tastatur, og vælg derefter knappen med markeringen.</span><span class="sxs-lookup"><span data-stu-id="425d4-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="425d4-262">Vælg **OK** (knappen med markeringen) på siden **Antal** for at bekræfte det antal, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="425d4-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="425d4-263">Vælg **OK** på opgavesiden **Vare** for at bekræfte, at varen *A0001* blev angivet.</span><span class="sxs-lookup"><span data-stu-id="425d4-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="425d4-264">Vælg feltet **Klynge-id**, og angiv en værdi, der tildeles et id for den klynge, du opretter.</span><span class="sxs-lookup"><span data-stu-id="425d4-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="425d4-265">Det id, du angiver her, bruges, når de to resterende varer på indkøbsordren modtages.</span><span class="sxs-lookup"><span data-stu-id="425d4-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="425d4-266">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="425d4-266">Select **OK**.</span></span>

    <span data-ttu-id="425d4-267">Opgavesiden **IO-num** vises med meddelelsen "Arbejde fuldført".</span><span class="sxs-lookup"><span data-stu-id="425d4-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="425d4-268">Vare *A0001* er nu modtaget på lokationen *RECV* og tildelt det klynge-id, du angav i trin 10.</span><span class="sxs-lookup"><span data-stu-id="425d4-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="425d4-269">Gentag trin 4 til 11 for at få de resterende to varer fra indkøbsordren tildele dem klynge-id'et:</span><span class="sxs-lookup"><span data-stu-id="425d4-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="425d4-270">Antallet *20* for vare *A0002*</span><span class="sxs-lookup"><span data-stu-id="425d4-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="425d4-271">Antallet *30* for vare *M9215*</span><span class="sxs-lookup"><span data-stu-id="425d4-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="425d4-272">Luk klyngen</span><span class="sxs-lookup"><span data-stu-id="425d4-272">Close the cluster</span></span>

<span data-ttu-id="425d4-273">Før varerne i klyngen kan lægges på lager, skal klyngen lukkes.</span><span class="sxs-lookup"><span data-stu-id="425d4-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="425d4-274">I Supply Chain Management skal du gå til **Lokationsstyring \> Arbejde \> Udgående \> Arbejdsklynger**.</span><span class="sxs-lookup"><span data-stu-id="425d4-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="425d4-275">Søg efter feltet **Klynge-id** for det klynge-id, du har angivet tidligere, i sektionen **Arbejdsklynge** på siden **Arbejdsklynger**.</span><span class="sxs-lookup"><span data-stu-id="425d4-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="425d4-276">Hvis klyngen ikke vises, er den muligvis allerede lukket.</span><span class="sxs-lookup"><span data-stu-id="425d4-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="425d4-277">Hvis du vil finde ud af, om klyngen blev lukket, skal du markere afkrydsningsfeltet **Vis lukket arbejde** og søge efter det klynge-id, du har angivet tidligere.</span><span class="sxs-lookup"><span data-stu-id="425d4-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="425d4-278">Udfør derefter ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="425d4-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="425d4-279">Hvis klyngen er lukket, kan du springe de resterende trin i denne procedure over og gå videre til den næste procedure, [Lægge klyngen på lager](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="425d4-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="425d4-280">Hvis klyngen ikke er lukket, skal du følge de resterende trin i denne procedure for at lukke klyngen manuelt.</span><span class="sxs-lookup"><span data-stu-id="425d4-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="425d4-281">Gå derefter videre til næste procedure.</span><span class="sxs-lookup"><span data-stu-id="425d4-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="425d4-282">Vælg det klynge-id, du har angivet tidligere, i sektionen **Arbejdsklynge**.</span><span class="sxs-lookup"><span data-stu-id="425d4-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="425d4-283">I handlingsruden skal du vælge **Luk klynge**.</span><span class="sxs-lookup"><span data-stu-id="425d4-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="425d4-284">Når klyngen er lukket, vises den ikke længere i sektionen **Arbejdsklynger** (medmindre afkrydsningsfeltet **Vis lukket arbejde** er markeret).</span><span class="sxs-lookup"><span data-stu-id="425d4-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="425d4-285">Lægge klyngen på lager</span><span class="sxs-lookup"><span data-stu-id="425d4-285">Put the cluster away</span></span>

1. <span data-ttu-id="425d4-286">Log på lagerstedsappen som en bruger, der er konfigureret til lagersted *61*.</span><span class="sxs-lookup"><span data-stu-id="425d4-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="425d4-287">I hovedmenuen skal du vælge **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="425d4-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="425d4-288">Vælg **Læg på lager-klynge** i menuen **Indgående**.</span><span class="sxs-lookup"><span data-stu-id="425d4-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="425d4-289">Vælg **Klynge-id**, og angiv det klynge-id, du tidligere har angivet til den lukkede klynge.</span><span class="sxs-lookup"><span data-stu-id="425d4-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="425d4-290">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="425d4-290">Select **OK**.</span></span>

    <span data-ttu-id="425d4-291">Siden **Læg på lager-klynge: Pluk** vises.</span><span class="sxs-lookup"><span data-stu-id="425d4-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="425d4-292">Den viser klynge-id'et, plukpladsen, varerne (værdien *Flere* vil blive vist) og det samlede antal i klyngen, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="425d4-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="425d4-293">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="425d4-293">Select **OK**.</span></span>

    <span data-ttu-id="425d4-294">Siden **Læg på lager-klynge: Læg** vises.</span><span class="sxs-lookup"><span data-stu-id="425d4-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="425d4-295">**Læg**-instruktionerne identificerer klynge-id'et, læg på lager-lokationen, varerne, det samlede antal og nummerplade-id'erne for de varer, der er modtaget i klyngen.</span><span class="sxs-lookup"><span data-stu-id="425d4-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="425d4-296">Du har standardindstillingerne til at tilsidesætte eller ignorere dette trin.</span><span class="sxs-lookup"><span data-stu-id="425d4-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="425d4-297">![Siden Læg på lager-klynge: Læg](media/Cluster_putaway-Put.png "Siden Læg på lager-klynge: Læg")</span><span class="sxs-lookup"><span data-stu-id="425d4-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="425d4-298">Vælg **OK** for at bekræfte læg på lager af klyngen.</span><span class="sxs-lookup"><span data-stu-id="425d4-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="425d4-299">Meddelelsen "Klynge er fuldført" vises.</span><span class="sxs-lookup"><span data-stu-id="425d4-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="425d4-300">Noter og tip</span><span class="sxs-lookup"><span data-stu-id="425d4-300">Notes and tips</span></span>

<span data-ttu-id="425d4-301">For de tilfælde, hvor klynge-id'et bliver til det overordnede id for en indlejret Palle, angives positionen automatisk, når klynge-id'et scannes.</span><span class="sxs-lookup"><span data-stu-id="425d4-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="425d4-302">Der skal ikke scannes flere id'er, selvom id-genereringen er angivet til manuel.</span><span class="sxs-lookup"><span data-stu-id="425d4-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>
