---
title: Beskeder om udførelse af bølge
description: Dette emne beskriver beskeder om bølgeudførelse og forklarer, hvordan du konfigurerer dem.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 47f270b5fff37e8e231d8a9c4a011172df3d9385
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271371"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="6388b-103">Beskeder om udførelse af bølge</span><span class="sxs-lookup"><span data-stu-id="6388b-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6388b-104">Funktionen *Beskeder om bølgeudførelse* bruger forretningshændelser og handlingscenteret til at levere beskeder, der vedrører bølgeudførelse.</span><span class="sxs-lookup"><span data-stu-id="6388b-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="6388b-105">Den giver dig mulighed for at angive de hændelsestyper, der genererer beskeder, de lagersteder, der genererer dem, og de brugere, der modtager dem.</span><span class="sxs-lookup"><span data-stu-id="6388b-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="6388b-106">Knappen **Vis meddelelser** (klokkesymbol) i højre side af navigationslinjen angiver, hvornår en meddelelse fra handlingscenteret er tilgængelig for den aktuelle bruger.</span><span class="sxs-lookup"><span data-stu-id="6388b-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="6388b-107">Brugeren kan vælge knappen **Vis meddelelser** for at åbne handlingscenteret og gennemse meddelelserne.</span><span class="sxs-lookup"><span data-stu-id="6388b-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="6388b-108">Forretningshændelser forekommer, når der køres forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="6388b-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="6388b-109">Forretningsprocesser består af opgaver.</span><span class="sxs-lookup"><span data-stu-id="6388b-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="6388b-110">I løbet af en forretningsproces udfører de brugere, der deltager i den, forretningshandlinger for at udføre disse opgaver.</span><span class="sxs-lookup"><span data-stu-id="6388b-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="6388b-111">Forretningshændelser udgør en mekanisme, der giver de eksterne systemer mulighed for at modtage beskeder fra Finance and Operations-programmer.</span><span class="sxs-lookup"><span data-stu-id="6388b-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="6388b-112">På denne måde kan systemerne udføre forretningshandlinger som svar på forretningshændelser.</span><span class="sxs-lookup"><span data-stu-id="6388b-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="6388b-113">Yderligere oplysninger finder du under [Oversigt over forretningshændelser](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="6388b-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="6388b-114">Slå funktionen Beskeder om bølgeudførelse til</span><span class="sxs-lookup"><span data-stu-id="6388b-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="6388b-115">Før du kan bruge funktionen *Beskeder om bølgeudførelse*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="6388b-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="6388b-116">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="6388b-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6388b-117">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="6388b-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6388b-118">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="6388b-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6388b-119">**Funktionsnavn:** *Beskeder om bølgeudførelse*</span><span class="sxs-lookup"><span data-stu-id="6388b-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="6388b-120">Scenario: Send beskeder om batchkørsel af bølger til handlingscenteret</span><span class="sxs-lookup"><span data-stu-id="6388b-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="6388b-121">Dette scenario viser hele flowet for afsendelse af beskeder om udførelsesfejl i bølgebatch til en bestemt rolle via handlingscenter.</span><span class="sxs-lookup"><span data-stu-id="6388b-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="6388b-122">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="6388b-122">Make demo data available</span></span>

<span data-ttu-id="6388b-123">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="6388b-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="6388b-124">Sørg for, at der køres bølger i batchtilstand</span><span class="sxs-lookup"><span data-stu-id="6388b-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="6388b-125">Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="6388b-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="6388b-126">Angiv **Udfør behandling af bølger i batch** til **Ja** i oversigtspanelet *Bølgebehandling*.</span><span class="sxs-lookup"><span data-stu-id="6388b-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="6388b-127">Hvis du vil deaktivere beskeder om udførelse af bølgebatch, skal du angive indstillingen **Deaktiver beskeder om udførelse af bølgebatch** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="6388b-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="6388b-128">Konfigurere en politik for bølgebeskeder</span><span class="sxs-lookup"><span data-stu-id="6388b-128">Configure a wave notification policy</span></span>

<span data-ttu-id="6388b-129">Politikker for bølgebeskeder definerer de typer beskeder, der sendes, og de brugere, der får besked.</span><span class="sxs-lookup"><span data-stu-id="6388b-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="6388b-130">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Politikker for bølgebeskeder**.</span><span class="sxs-lookup"><span data-stu-id="6388b-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="6388b-131">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="6388b-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="6388b-132">**Politik for bølgebesked:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="6388b-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="6388b-133">**Beskrivelse:** *Bølgebatchfejl på lagersted 24*</span><span class="sxs-lookup"><span data-stu-id="6388b-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="6388b-134">**Send besked om:** *Kun fejl*</span><span class="sxs-lookup"><span data-stu-id="6388b-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="6388b-135">**Til rolle:** *Systemadministrator*</span><span class="sxs-lookup"><span data-stu-id="6388b-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="6388b-136">Da der i dette scenario bruges demodata, er rollen *Systemadministrator* valgt for at gøre det enkelt.</span><span class="sxs-lookup"><span data-stu-id="6388b-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="6388b-137">Derfor vil du modtage beskeder, fordi du er logget på som systemadministratorbruger.</span><span class="sxs-lookup"><span data-stu-id="6388b-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="6388b-138">I praksis skal du dog normalt vælge en mere specifik rolle for at give besked om fejl i udførelse af bølgebatch, f.eks. *Lagerchef*.</span><span class="sxs-lookup"><span data-stu-id="6388b-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="6388b-139">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6388b-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="6388b-140">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="6388b-140">Configure a wave template</span></span>

<span data-ttu-id="6388b-141">Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til tilsvarende bølgeetiketskabeloner.</span><span class="sxs-lookup"><span data-stu-id="6388b-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="6388b-142">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="6388b-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="6388b-143">Angiv feltet **Bølgeskabelontype** til *Forsendelse* i listeruden, og vælg derefter *24 Standard for forsendelse* som bølgeskabelon til lagersted 24.</span><span class="sxs-lookup"><span data-stu-id="6388b-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="6388b-144">Gå til oversigtspanelet **Generelt**, og indstil feltet **Politik for bølgebesked** til *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="6388b-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="6388b-145">Konfigurere en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="6388b-145">Configure a work template</span></span>

<span data-ttu-id="6388b-146">Arbejdsskabeloner bruges under udførelse af bølger til at generere arbejde.</span><span class="sxs-lookup"><span data-stu-id="6388b-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="6388b-147">I dette scenario skal der udløses en fejl ved udførelse af bølger.</span><span class="sxs-lookup"><span data-stu-id="6388b-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="6388b-148">Ved at indstille forespørgslen i arbejdsskabelonen til at bruge et ikke-eksisterende lagersted, sikrer du, at bølgeudførelse mislykkes og derfor sender en besked.</span><span class="sxs-lookup"><span data-stu-id="6388b-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="6388b-149">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="6388b-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6388b-150">Angiv feltet **Arbejdsskabelontype** til *Salgsordrer* i listeruden, og vælg derefter *24 Salgsordrestadie* som arbejdsskabelon til lagersted 24.</span><span class="sxs-lookup"><span data-stu-id="6388b-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="6388b-151">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6388b-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="6388b-152">I dialogboksen til forespørgselseditoren skal du under fanen **Område** redigere følgende række (eller tilføje den, hvis den ikke findes):</span><span class="sxs-lookup"><span data-stu-id="6388b-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="6388b-153">**Tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="6388b-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="6388b-154">**Afledt tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="6388b-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="6388b-155">**Felt:** *Lagersted*</span><span class="sxs-lookup"><span data-stu-id="6388b-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="6388b-156">**Kriterier:** Ret værdien fra *24* til *Fejl*.</span><span class="sxs-lookup"><span data-stu-id="6388b-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="6388b-157">Vælg **OK**, og bekræft ændringen.</span><span class="sxs-lookup"><span data-stu-id="6388b-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="6388b-158">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="6388b-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="6388b-159">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="6388b-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="6388b-160">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="6388b-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="6388b-161">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="6388b-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="6388b-162">**Lagersted:** *24*</span><span class="sxs-lookup"><span data-stu-id="6388b-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="6388b-163">I oversigtspanelet **Salgsordrelinjer** skal du tilføje en salgsordrelinje, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="6388b-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="6388b-164">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="6388b-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="6388b-165">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="6388b-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="6388b-166">Disse varer og antal er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="6388b-166">These items and quantities are only examples.</span></span> <span data-ttu-id="6388b-167">Det angivne lagersted skal have stort nok lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="6388b-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="6388b-168">Mens den nye linje stadig er valgt i oversigtspanelet **Salgsordrelinjer**, skal du vælge **Lager \> Reservation** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="6388b-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="6388b-169">På siden **Reservation** skal du i handlingsruden vælge **Reserve parti**.</span><span class="sxs-lookup"><span data-stu-id="6388b-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="6388b-170">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="6388b-170">Then close the page.</span></span>
1. <span data-ttu-id="6388b-171">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6388b-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="6388b-172">Beskeder fra udførelse af batchjob for bølge</span><span class="sxs-lookup"><span data-stu-id="6388b-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="6388b-173">Afhængigt af opsætningen af dine forretningshændelser modtager du i sidste ende en besked om fejl i bølgeudførelse.</span><span class="sxs-lookup"><span data-stu-id="6388b-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="6388b-174">Meddelelsen i handlingscenteret vil ligne følgende eksempel og indeholde et link til den bølge, der mislykkedes.</span><span class="sxs-lookup"><span data-stu-id="6388b-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="6388b-175">**Fejl under udførelse af bølge**</span><span class="sxs-lookup"><span data-stu-id="6388b-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="6388b-176">Der opstod en fejl under udførelse af bølgen USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="6388b-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="6388b-177">Sidste meddelelser: Der er ikke oprettet noget arbejde for Bølge USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="6388b-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="6388b-178">**STATUS**</span><span class="sxs-lookup"><span data-stu-id="6388b-178">**STATUS**</span></span>  
> <span data-ttu-id="6388b-179">Aktive</span><span class="sxs-lookup"><span data-stu-id="6388b-179">Active</span></span>
>
> <span data-ttu-id="6388b-180">Åbn bølgedetaljer</span><span class="sxs-lookup"><span data-stu-id="6388b-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
