---
title: Kvalitetskontrol
description: Dette emne indeholder oplysninger om funktionen Kvalitetskontrol. Denne funktion giver lagermedarbejderne mulighed for hurtig spottjek af kvalitet, mens de modtager varer i modtagelsesområdet.
author: mirzaab
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c270426a228ac58652f1f60d6fe99d4886071fa6
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621432"
---
# <a name="quality-check"></a><span data-ttu-id="12728-104">Kvalitetskontrol</span><span class="sxs-lookup"><span data-stu-id="12728-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12728-105">Funktionen *Kvalitetskontrol* giver lagermedarbejderne mulighed for hurtig spottjek af kvalitet, mens de modtager varer i modtagelsesområdet.</span><span class="sxs-lookup"><span data-stu-id="12728-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="12728-106">Disse stikprøvekontroller er nyttige, når arbejderne kontrollerer emballagen eller andre let genkendelige dele af en vare.</span><span class="sxs-lookup"><span data-stu-id="12728-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="12728-107">Funktionen hjælper medarbejderne med hurtigt at se, om noget er defekt eller forkert, før de lagrer varen på dens læg på lager-lokation.</span><span class="sxs-lookup"><span data-stu-id="12728-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="12728-108">Denne funktion er et alternativ til standardprocessen for kvalitetskontrol.</span><span class="sxs-lookup"><span data-stu-id="12728-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="12728-109">Den giver større fleksibilitet og hurtigere behandling.</span><span class="sxs-lookup"><span data-stu-id="12728-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="12728-110">Når du bruger denne funktion, sker modtagelse og kvalitetskontrol på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="12728-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="12728-111">Når en forsendelse ankommer, registrerer en lagermedarbejder ankomsten.</span><span class="sxs-lookup"><span data-stu-id="12728-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="12728-112">Arbejderen scanner også et id for at registrere lokationen.</span><span class="sxs-lookup"><span data-stu-id="12728-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="12728-113">Arbejderen udfører en hurtig kvalitetskontrol og registrerer resultatet (bestået eller mislykket) for det pågældende id.</span><span class="sxs-lookup"><span data-stu-id="12728-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="12728-114">En af følgende handlinger sker:</span><span class="sxs-lookup"><span data-stu-id="12728-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="12728-115">Hvis kvalitetskontrollen er bestået, vil id'et blive accepteret og styret til en modtagelseslokalitet på normal vis.</span><span class="sxs-lookup"><span data-stu-id="12728-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="12728-116">Hvis kvalitetskontrollen er mislykket, afvises id'et, og eksisterende læg på lager-arbejde omdirigeres til en alternativ placering til yderligere inspektion.</span><span class="sxs-lookup"><span data-stu-id="12728-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="12728-117">Der oprettes en ny kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="12728-117">A new quality order is created.</span></span> <span data-ttu-id="12728-118">Hvis du vil have vist den kvalitetsordre, der er oprettet ud fra den mislykkede kvalitetskontrol, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12728-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="12728-119">Denne proces kan også konfigureres, så alle scannede id'er straks omdirigeres til kvalitetskontrollens lokation.</span><span class="sxs-lookup"><span data-stu-id="12728-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="12728-120">Aktivere funktionen Kvalitetskontrol</span><span class="sxs-lookup"><span data-stu-id="12728-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="12728-121">Før du kan bruge funktionen *Kvalitetskontrol*, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="12728-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="12728-122">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="12728-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="12728-123">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="12728-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="12728-124">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="12728-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="12728-125">**Funktionsnavn:** *Kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="12728-126">Konfigurere funktionen til eksempelscenariet</span><span class="sxs-lookup"><span data-stu-id="12728-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="12728-127">Dette afsnit indeholder retningslinjer og et eksempel, der viser, hvordan du kan konfigurere funktionen *Kvalitetskontrol* og forberede eksempeldata til det eksempelscenario, der er angivet senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="12728-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="12728-128">Gøre eksempeldata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="12728-128">Make sample data available</span></span>

<span data-ttu-id="12728-129">Hvis du vil arbejde dig gennem [eksempelscenariet](#example-scenario) ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="12728-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="12728-130">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="12728-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="12728-131">Kvalitetskontrolskabelon</span><span class="sxs-lookup"><span data-stu-id="12728-131">Quality check template</span></span>

<span data-ttu-id="12728-132">Kvalitetskontrolskabelonen definerer reglerne for udførelse af hurtige stikprøvekontroller af kvaliteten på modtagelsestidspunktet.</span><span class="sxs-lookup"><span data-stu-id="12728-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="12728-133">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Kvalitetskontrolskabelon**.</span><span class="sxs-lookup"><span data-stu-id="12728-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="12728-134">Vælg **Ny** for at føje en skabelon til gitteret.</span><span class="sxs-lookup"><span data-stu-id="12728-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="12728-135">Definer skabelonen ved at angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="12728-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="12728-136">**Skabelonnavn for kvalitetskontrol:** *Dock check*</span><span class="sxs-lookup"><span data-stu-id="12728-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="12728-137">Angiv et navn, der identificerer de politikker, der anvendes for denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="12728-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="12728-138">**Acceptpolitik:** *Spørg bruger*</span><span class="sxs-lookup"><span data-stu-id="12728-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="12728-139">Angiv, om brugere skal blive bedt om at acceptere eller afvise lagerkvaliteten, mens de behandler arbejdet, eller om kvaliteten skal afvises automatisk.</span><span class="sxs-lookup"><span data-stu-id="12728-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="12728-140">De tilgængelige indstillinger er *Automatisk afvisning* og *Spørg brugeren*.</span><span class="sxs-lookup"><span data-stu-id="12728-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="12728-141">**Politik for kvalitetsbehandling:** *Opret kvalitetsordre*</span><span class="sxs-lookup"><span data-stu-id="12728-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="12728-142">Vælg den politik, der skal bruges ved afvisning af lagerkvaliteten.</span><span class="sxs-lookup"><span data-stu-id="12728-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="12728-143">Der findes følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="12728-143">The following options are available:</span></span>

        - <span data-ttu-id="12728-144">*Opret kun arbejde* – Opret kun arbejde for at lette lagerbevægelse.</span><span class="sxs-lookup"><span data-stu-id="12728-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="12728-145">*Opret kvalitetsordre* – Opret en kvalitetsordre for at forenkle kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="12728-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="12728-146">**Testgruppe:** *Kabinet*</span><span class="sxs-lookup"><span data-stu-id="12728-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="12728-147">Angiv den testgruppe, der skal bruges i den kvalitetsordre, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="12728-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="12728-148">Testgrupper konfigureres i modulet **Lagerstyring**.</span><span class="sxs-lookup"><span data-stu-id="12728-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="12728-149">Lad indstillingen **Destruktiv tekst** være slået fra for testgruppen.</span><span class="sxs-lookup"><span data-stu-id="12728-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="12728-150">Denne indstilling definerer, om prøven skal destrueres som en del af testene i testgruppen.</span><span class="sxs-lookup"><span data-stu-id="12728-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="12728-151">Når der anvendes en destruktiv test, vil oprettelsen af en kvalitetsordre for en vare få systemet til at generere en lagertransaktion.</span><span class="sxs-lookup"><span data-stu-id="12728-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="12728-152">Den nye lagerpostering foregriber lagerreduktionen for testantallet.</span><span class="sxs-lookup"><span data-stu-id="12728-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="12728-153">Lagerreduktionen sker, når kvalitetsordren er fuldført via valideringstrinnet.</span><span class="sxs-lookup"><span data-stu-id="12728-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="12728-154">Lagertransaktionen identificeres som en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="12728-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="12728-155">Arbejdsklasse – Kvalitetskontrol</span><span class="sxs-lookup"><span data-stu-id="12728-155">Work class – Quality check</span></span>

<span data-ttu-id="12728-156">Arbejdsklasser bruges til at dirigere og/eller begrænse typen af arbejdsordrelinjer, som lagermedarbejdere kan behandle på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="12728-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="12728-157">Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.</span><span class="sxs-lookup"><span data-stu-id="12728-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="12728-158">Vælg **Ny** for at oprette en arbejdsklasse.</span><span class="sxs-lookup"><span data-stu-id="12728-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="12728-159">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="12728-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="12728-160">**Arbejdsklasse-id:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="12728-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="12728-161">Angiv et navn, der identificerer arbejdsklassen.</span><span class="sxs-lookup"><span data-stu-id="12728-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="12728-162">**Beskrivelse:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="12728-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="12728-163">Angiv en kort beskrivelse, der angiver, hvad arbejdsklassen bruges til.</span><span class="sxs-lookup"><span data-stu-id="12728-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="12728-164">**Arbejdsordretype:** *Kvalitet i kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="12728-165">Vælg den type arbejdsordre, der oprettes af arbejdsklassen.</span><span class="sxs-lookup"><span data-stu-id="12728-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="12728-166">Når du konfigurerer kvalitetskontrolarbejde, skal du altid vælge *Kvalitet i kvalitetskontrol*.</span><span class="sxs-lookup"><span data-stu-id="12728-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="12728-167">Lad feltet **Lokationstype** være tomt i oversigtspanelet **Gyldige lokationstyper**.</span><span class="sxs-lookup"><span data-stu-id="12728-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="12728-168">Hvis du vælger en lokationstype, begrænser du de lokationer, hvor varer kan lægges på lager, efter at de er blevet plukket.</span><span class="sxs-lookup"><span data-stu-id="12728-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="12728-169">Dette felt bruges, når en lokationsvejledning forsøger at finde lokationen, eller hvis en lagermedarbejder manuelt angiver lokationen for varen i mobilenhedsmenuen.</span><span class="sxs-lookup"><span data-stu-id="12728-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="12728-170">Du kan finde flere oplysninger om arbejdsklasser, og hvordan du opretter dem, under [Oprette en arbejdsklasse](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="12728-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="12728-171">Arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="12728-171">Work template</span></span>

<span data-ttu-id="12728-172">Arbejdsskabeloner gør det muligt at definere arbejdshandlinger, der skal udføres på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="12728-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="12728-173">Arbejdshandlinger på lagersted består typisk af parvise handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering.</span><span class="sxs-lookup"><span data-stu-id="12728-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="12728-174">En arbejdsskabelon til kvalitetskontrol definerer de arbejdshandlinger, der skal udføres kvalitetskontrol for.</span><span class="sxs-lookup"><span data-stu-id="12728-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="12728-175">Indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="12728-175">Purchase orders</span></span>

1. <span data-ttu-id="12728-176">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="12728-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="12728-177">Indstil feltet **Arbejdsordretype** i overskriften til *Indkøbsordrer*.</span><span class="sxs-lookup"><span data-stu-id="12728-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="12728-178">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="12728-179">Vælg en arbejdsskabelon, der skal omfatte et kvalitetskontroltrin.</span><span class="sxs-lookup"><span data-stu-id="12728-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="12728-180">Vælg **51 indkøbsordremodtagelse** i feltet **Arbejdsskabelon** i sektionen *Oversigt*.</span><span class="sxs-lookup"><span data-stu-id="12728-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="12728-181">Bemærk, at gitteret indeholder to eksisterende linjer i sektionen **Arbejdsskabelondetaljer**: én til *Pluk* og én til *Læg på lager*.</span><span class="sxs-lookup"><span data-stu-id="12728-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="12728-182">Vælg **Ny** i sektionen **Arbejdsskabelondetaljer** for at føje en række for kvalitetskontrol til gitteret.</span><span class="sxs-lookup"><span data-stu-id="12728-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="12728-183">Bemærk, at feltet **Linjenummer** for den nye linje er angivet til *3*.</span><span class="sxs-lookup"><span data-stu-id="12728-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="12728-184">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="12728-184">On the new line, set the following values.</span></span> <span data-ttu-id="12728-185">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="12728-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="12728-186">**Arbejdstyp:** *Kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="12728-187">**Arbejdsklasse-id:** *Indkøb*</span><span class="sxs-lookup"><span data-stu-id="12728-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="12728-188">**Skabelonnavn for kvalitetskontrol:** *Dock check*</span><span class="sxs-lookup"><span data-stu-id="12728-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="12728-189">Vælg det entydige id for arbejdsklassen.</span><span class="sxs-lookup"><span data-stu-id="12728-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="12728-190">Du bruger denne værdi til at konfigurere menupunkterne på mobilenheden og de typer arbejde, som disse menupunkter kan behandle.</span><span class="sxs-lookup"><span data-stu-id="12728-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="12728-191">Vælg **Gem** i handlingsruden for at gemme arbejdet indtil videre.</span><span class="sxs-lookup"><span data-stu-id="12728-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="12728-192">Du modtager en meddelelse med oplysningen "Ugyldig - Kvalitetskontrol skal følge lige efter et pluk".</span><span class="sxs-lookup"><span data-stu-id="12728-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="12728-193">Derfor skal du ændre **Linjenummer**-værdien for den linje, du lige har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="12728-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="12728-194">Udfør følgende trin for at ændre **Linjenummer**-værdien for den nye linje:</span><span class="sxs-lookup"><span data-stu-id="12728-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="12728-195">Vælg den linje, hvor feltet **Arbejdstype** i sektionen **Arbejdsskabelondetaljer** er angivet til *Kvalitetskontrol*.</span><span class="sxs-lookup"><span data-stu-id="12728-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="12728-196">Vælg knappen **Flyt op** eller **Flyt ned** for at flytte *Kvalitetskontrol*-linjen, så den er efter *Pluk*-linjen.</span><span class="sxs-lookup"><span data-stu-id="12728-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="12728-197">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="12728-198">Kvalitet i kvalitetskontrol</span><span class="sxs-lookup"><span data-stu-id="12728-198">Quality in quality check</span></span>

<span data-ttu-id="12728-199">Derefter skal du oprette en arbejdsskabelon til kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="12728-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="12728-200">I overskriften på siden **Arbejdsskabeloner** skal du ændre værdien af feltet **Arbejdsordretype** til *Kvalitet i kvalitetskontrol*.</span><span class="sxs-lookup"><span data-stu-id="12728-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="12728-201">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret i sektionen **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="12728-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="12728-202">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="12728-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="12728-203">**Arbejdsskabelon:** *51 Kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="12728-204">Angiv et navn til skabelonen.</span><span class="sxs-lookup"><span data-stu-id="12728-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="12728-205">**Beskrivelse af arbejdsskabelon:** *51 Kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="12728-206">Vælg **Gem** i handlingsruden for at gøre sektionen **Arbejdsskabelondetaljer** tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="12728-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="12728-207">Mens den nye skabelon stadig er markeret i sektionen **Oversigt**, skal du vælge **Ny** i sektionen **Arbejdsskabelondetaljer** for at føje en række til gitteret der.</span><span class="sxs-lookup"><span data-stu-id="12728-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="12728-208">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="12728-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="12728-209">**Arbejdstype:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="12728-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="12728-210">**Arbejdsklasse-id:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="12728-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="12728-211">Vælg navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="12728-212">Vælg **Ny** igen i sektionen **Arbejdsskabelondetaljer** for at tilføje endnu en række.</span><span class="sxs-lookup"><span data-stu-id="12728-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="12728-213">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="12728-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="12728-214">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="12728-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="12728-215">**Arbejdsklasse-id:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="12728-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="12728-216">Vælg navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="12728-217">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="12728-218">Yderligere oplysninger om arbejdsskabeloner finder du under [Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="12728-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="12728-219">Lokationsvejledning – Kvalitetsfejl</span><span class="sxs-lookup"><span data-stu-id="12728-219">Location directive – Quality failures</span></span>

<span data-ttu-id="12728-220">Lokalitetsvejledninger er regler, der hjælper med at identificere pluk og læg-lokationer for lagerbevægelser.</span><span class="sxs-lookup"><span data-stu-id="12728-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="12728-221">I f.eks. en salgsordretransaktion bestemmer en lokationsvejledning , hvor varerne plukkes, og hvor de plukkede varer skal lægges på lager.</span><span class="sxs-lookup"><span data-stu-id="12728-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="12728-222">Du skal konfigurere en lokationsvejledningsregel for at definere, hvordan mislykkede kvalitetskontroller skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="12728-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="12728-223">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="12728-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="12728-224">I ruden til venstre skal du angive feltet **Arbejdsordretype** til *Indkøbsordrer* for at arbejde med lokationsvejledninger af den pågældende type.</span><span class="sxs-lookup"><span data-stu-id="12728-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="12728-225">Vælg **Ny** i handlingsruden for at oprette en lokationsvejledning til kvalitetskontrol.</span><span class="sxs-lookup"><span data-stu-id="12728-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="12728-226">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="12728-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="12728-227">**Løbenummer:** Accepter standardværdien.</span><span class="sxs-lookup"><span data-stu-id="12728-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="12728-228">**Navn:** *51 til kvalitet*</span><span class="sxs-lookup"><span data-stu-id="12728-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="12728-229">I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="12728-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="12728-230">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="12728-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="12728-231">**Arbejdstype:** *Læg på lager*</span><span class="sxs-lookup"><span data-stu-id="12728-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="12728-232">**Lokation:** *5*</span><span class="sxs-lookup"><span data-stu-id="12728-232">**Site:** *5*</span></span>
    - <span data-ttu-id="12728-233">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="12728-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="12728-234">Vælg **Gem** i handlingsruden for at gemme vejledningen og gøre oversigtspanelet **Linjer** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="12728-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="12728-235">Gå til oversigtspanelet **Linjer** og vælg **Ny** for at føje en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="12728-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="12728-236">Angiv følgende værdier på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="12728-236">On the new line, set the following values.</span></span> <span data-ttu-id="12728-237">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="12728-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="12728-238">**Fra antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="12728-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="12728-239">**Til antal:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="12728-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="12728-240">Vælg **Gem** i handlingsruden for at gemme den nye linje og gøre oversigtspanelet **Handlinger for lokationsvejledninger** tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="12728-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="12728-241">Mens den nye linje stadig er valgt i oversigtspanelet **Linjer**, skal du vælge **Ny** i oversigtspanelet **Handlinger for lokationsvejledninger** for at føje en række til gitteret der, så du kan oprette en handling for linjen.</span><span class="sxs-lookup"><span data-stu-id="12728-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="12728-242">Angiv feltet **Navn** til *Kvalitet* i den nye række.</span><span class="sxs-lookup"><span data-stu-id="12728-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="12728-243">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="12728-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="12728-244">Vælg **Gem** i handlingsruden for at gøre knappen **Rediger forespørgsel** tilgængelig i oversigtspanelet **Handlinger i lokationsvejledning**.</span><span class="sxs-lookup"><span data-stu-id="12728-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="12728-245">Selvom den linje, du lige har tilføjet, stadig er valgt i oversigtspanelet **Handlinger for lokationsvejledninger**, skal du vælge **Rediger forespørgsel** for at åbne en dialogboks, hvor du kan redigere forespørgslen for handlingen.</span><span class="sxs-lookup"><span data-stu-id="12728-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="12728-246">Gå til fanen **Interval**, og vælg **Tilføj** for at føje en række til forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="12728-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="12728-247">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="12728-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="12728-248">**Tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="12728-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="12728-249">**Afledt tabel:** *Lokationer*</span><span class="sxs-lookup"><span data-stu-id="12728-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="12728-250">**Felt:** *Lokation*</span><span class="sxs-lookup"><span data-stu-id="12728-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="12728-251">**Kriterier:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="12728-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="12728-252">Lokationen *QMS* er en lagerlokation til kvalitet.</span><span class="sxs-lookup"><span data-stu-id="12728-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="12728-253">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="12728-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="12728-254">Nu skal du ændre rækkefølgen af de eksisterende lokationsvejledninger for lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="12728-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="12728-255">Gem den nye lokationsvejledning *51 til kvalitet*, opdater siden, og vælg lokationsvejledningen på listen.</span><span class="sxs-lookup"><span data-stu-id="12728-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="12728-256">Brug derefter knapperne **Flyt op** og **Flyt ned** i handlingsruden til at placere lokationsvejledningen for lagersted *51* i følgende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="12728-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="12728-257">(Før du vælger **Flyt op** eller **Flyt ned**, skal du vælge en lokationsvejledning på listen).</span><span class="sxs-lookup"><span data-stu-id="12728-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="12728-258">51 til kvalitet</span><span class="sxs-lookup"><span data-stu-id="12728-258">51 To Quality</span></span>
    2. <span data-ttu-id="12728-259">51 PO Direct</span><span class="sxs-lookup"><span data-stu-id="12728-259">51 PO Direct</span></span>
    3. <span data-ttu-id="12728-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="12728-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="12728-261">Menupunkter i mobilenhed</span><span class="sxs-lookup"><span data-stu-id="12728-261">Mobile device menu items</span></span>

<span data-ttu-id="12728-262">Konfigurere et menupunkt, så mobilenheder kan udføre funktionen **Kvalitetskontrol**.</span><span class="sxs-lookup"><span data-stu-id="12728-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="12728-263">Læg indkøb på lager</span><span class="sxs-lookup"><span data-stu-id="12728-263">Purchase putaway</span></span>

1. <span data-ttu-id="12728-264">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="12728-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="12728-265">Vælg menupunktet **Læg indkøb på lager** på listen.</span><span class="sxs-lookup"><span data-stu-id="12728-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="12728-266">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="12728-267">I sektionen **Arbejdsklasser** skal du vælge **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="12728-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="12728-268">Angiv følgende værdier i den nye række:</span><span class="sxs-lookup"><span data-stu-id="12728-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="12728-269">**Arbejdsklasse-id:** *QC Check*</span><span class="sxs-lookup"><span data-stu-id="12728-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="12728-270">Angiv navnet på den [arbejdsklasse](#work-class), du oprettede tidligere til kvalitetskontrolarbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="12728-271">**Arbejdsordretype:** *Kvalitet i kvalitetskontrol*</span><span class="sxs-lookup"><span data-stu-id="12728-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="12728-272">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="12728-273">Indkøbsordrelinje til modtagelse</span><span class="sxs-lookup"><span data-stu-id="12728-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="12728-274">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="12728-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="12728-275">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="12728-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12728-276">Angiv følgende værdier i overskriften:</span><span class="sxs-lookup"><span data-stu-id="12728-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="12728-277">**Navn på menupunkt:** *Modtagelse af indkøbsordrelinje*</span><span class="sxs-lookup"><span data-stu-id="12728-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="12728-278">**Titel:** *Modtagelse af indkøbsordrelinje*</span><span class="sxs-lookup"><span data-stu-id="12728-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="12728-279">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="12728-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="12728-280">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="12728-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="12728-281">I oversigtspanelet **Generelt** kan du angive følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="12728-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="12728-282">Acceptér standardværdierne for alle de andre felter.</span><span class="sxs-lookup"><span data-stu-id="12728-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="12728-283">**Arbejdsoprettelsesproces:** *Modtagelse og læg på lager for ordrelinje*</span><span class="sxs-lookup"><span data-stu-id="12728-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="12728-284">**Generer nummerplade:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="12728-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="12728-285">**Arbejdsskabelon:** *51 indkøbsordremodtagelse*</span><span class="sxs-lookup"><span data-stu-id="12728-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="12728-286">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="12728-287">Føje menupunktet til en mobilenhedsmenu</span><span class="sxs-lookup"><span data-stu-id="12728-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="12728-288">Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.</span><span class="sxs-lookup"><span data-stu-id="12728-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="12728-289">Vælg menuen **Indgående** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="12728-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="12728-290">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="12728-291">I kolonnen **Tilgængelig menuer og menupunkter** skal vælge menupunktet **Modtagelse af indkøbsordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="12728-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="12728-292">Vælg den højre piletast for at flytte **Modtagelse af indkøbsordrelinje** til kolonnen **Menustruktur**.</span><span class="sxs-lookup"><span data-stu-id="12728-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="12728-293">Vælg **Modtagelse af indkøbsordrelinje** i kolonnen **Menustruktur**, og vælg derefter pil op eller pil ned for at flytte menupunktet til den ønskede placering i mobilenhedsmenuen.</span><span class="sxs-lookup"><span data-stu-id="12728-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="12728-294">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="12728-295">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="12728-295">Example scenario</span></span>

<span data-ttu-id="12728-296">Når du har gjort alle de tidligere nævnte eksempeldata tilgængelige og konfigureret dem, kan du arbejde gennem dette scenario for at afprøve funktionen *Kvalitetskontrol*.</span><span class="sxs-lookup"><span data-stu-id="12728-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="12728-297">De værdier, der vises i dette scenarie, forudsætter, at du arbejder med standarddemodataene, at du har valgt **USMF** som juridisk enhed, og at du har forberedt de eksempelposter, der er beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="12728-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="12728-298">Dette scenario fungerer også som et eksempel, der viser, hvordan funktionen kan bruges i en produktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="12728-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="12728-299">Oprette en indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="12728-299">Create a purchase order</span></span>

1. <span data-ttu-id="12728-300">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12728-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="12728-301">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="12728-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12728-302">Angiv følgende værdier i dialogboksen **Opret indkøbsordre**:</span><span class="sxs-lookup"><span data-stu-id="12728-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="12728-303">**Kreditorkonto:** *104*</span><span class="sxs-lookup"><span data-stu-id="12728-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="12728-304">**Lagersted:** *51*</span><span class="sxs-lookup"><span data-stu-id="12728-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="12728-305">Vælg **OK** for at åbne den nye indkøbsordre og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="12728-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="12728-306">I oversigtspanelet **Indkøbsordrelinjer** indeholder gitteret en ny tom linje.</span><span class="sxs-lookup"><span data-stu-id="12728-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="12728-307">Angiv følgende værdier på denne linje:</span><span class="sxs-lookup"><span data-stu-id="12728-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="12728-308">**Varenummer:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="12728-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="12728-309">**Antal:** *3*</span><span class="sxs-lookup"><span data-stu-id="12728-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="12728-310">**Enhed:** *PL*</span><span class="sxs-lookup"><span data-stu-id="12728-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="12728-311">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="12728-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="12728-312">Behandle kvalitetskontrol ved modtagelse</span><span class="sxs-lookup"><span data-stu-id="12728-312">Process quality check receiving</span></span>

<span data-ttu-id="12728-313">Når indkøbsordren er blevet oprettet, kan den modtages ved hjælp af menupunktet **Modtagelse af indkøbsordrelinje** og funktionaliteten af *Kvalitetskontrol*.</span><span class="sxs-lookup"><span data-stu-id="12728-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="12728-314">Modtage palle 1</span><span class="sxs-lookup"><span data-stu-id="12728-314">Receive pallet 1</span></span>

1. <span data-ttu-id="12728-315">Log på lagerstedsappen som bruger af lagersted *51*.</span><span class="sxs-lookup"><span data-stu-id="12728-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="12728-316">(Angiv *51* som bruger-id og *1* som adgangskode).</span><span class="sxs-lookup"><span data-stu-id="12728-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="12728-317">Gå til **Indgående \> Modtagelse af indkøbsordrelinje**.</span><span class="sxs-lookup"><span data-stu-id="12728-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="12728-318">Angiv dit indkøbsordrenummer i feltet **IO-num**.</span><span class="sxs-lookup"><span data-stu-id="12728-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="12728-319">Bekræft indkøbsordrens nummer.</span><span class="sxs-lookup"><span data-stu-id="12728-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="12728-320">Angiv linjenummeret fra den indkøbsordre, der modtages, i feltet **LINJENUM**.</span><span class="sxs-lookup"><span data-stu-id="12728-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="12728-321">Da ordren kun har én linje i dette scenario, skal du skrive *1* i feltet **LINJENUM** for hvert modtagelsestrin.</span><span class="sxs-lookup"><span data-stu-id="12728-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="12728-322">Bekræft linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="12728-322">Confirm the line number.</span></span>
1. <span data-ttu-id="12728-323">Angiv det antal, der skal modtages, i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="12728-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="12728-324">Da indkøbsordren er for tre paller (*PL*) i dette scenario, og der er tre modtagelsestrin, skal du skrive *1* i feltet **Antal** for hvert modtagelsestrin.</span><span class="sxs-lookup"><span data-stu-id="12728-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="12728-325">Bekræft antallet.</span><span class="sxs-lookup"><span data-stu-id="12728-325">Confirm the quantity.</span></span>

    <span data-ttu-id="12728-326">Siden **Kvalitetskontrol** vises uden postfelter.</span><span class="sxs-lookup"><span data-stu-id="12728-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="12728-327">Den har kun bekræftelsesknappen (markering) nederst og menuknappen (**≡**) øverst.</span><span class="sxs-lookup"><span data-stu-id="12728-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="12728-328">(Menuknappen kaldes undertiden hamburgeren eller hamburgerknappen). Når pallen passerer kvalitetskontrollen, bekræfter brugeren blot kvalitetskontrollen på siden **Kvalitetskontrol**.</span><span class="sxs-lookup"><span data-stu-id="12728-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="12728-329">![Siden Kvalitetskontrol](media/quality-check.png "Siden Kvalitetskontrol")</span><span class="sxs-lookup"><span data-stu-id="12728-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="12728-330">Vælg bekræftelsesknappen for at bestå kvalitetskontrollen af palle 1 fra linje 1.</span><span class="sxs-lookup"><span data-stu-id="12728-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="12728-331">Siden **Indkøbsordrer: læg på lager** viser oplysninger om læg på lager-arbejdet:</span><span class="sxs-lookup"><span data-stu-id="12728-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="12728-332">**LOK:** Systemet har fastlagt lokationen</span><span class="sxs-lookup"><span data-stu-id="12728-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="12728-333">Denne lokation er den angivne læg på lager-lokation for modtagelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="12728-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="12728-334">**LP:** Det systemgenererede id</span><span class="sxs-lookup"><span data-stu-id="12728-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="12728-335">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="12728-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="12728-336">**Antal:** *1 PL: 100 hver*</span><span class="sxs-lookup"><span data-stu-id="12728-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="12728-337">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="12728-337">The item description is also shown.</span></span>

1. <span data-ttu-id="12728-338">Bekræft læg på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="12728-339">På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført".</span><span class="sxs-lookup"><span data-stu-id="12728-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="12728-340">Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.</span><span class="sxs-lookup"><span data-stu-id="12728-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="12728-341">Modtage palle 2</span><span class="sxs-lookup"><span data-stu-id="12728-341">Receive pallet 2</span></span>

<span data-ttu-id="12728-342">I dette scenario vil palle 2 blive afvist.</span><span class="sxs-lookup"><span data-stu-id="12728-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="12728-343">Angiv **1** i feltet *LINJENUM*, og bekræft linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="12728-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="12728-344">Feltet **Antal** er nu tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="12728-344">The **QTY** field is now available.</span></span> <span data-ttu-id="12728-345">Angiv *1*, og bekræft antallet.</span><span class="sxs-lookup"><span data-stu-id="12728-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="12728-346">Siden **Kvalitetskontrol** vises.</span><span class="sxs-lookup"><span data-stu-id="12728-346">The **Quality check** page appears.</span></span> <span data-ttu-id="12728-347">I forbindelse med denne modtagelse vil pallen blive afvist for kvalitet, og den vil blive placeret i *QMS*-kvalitetslokationen.</span><span class="sxs-lookup"><span data-stu-id="12728-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="12728-348">Vælg menuknappen (**≡**) øverst på siden, og vælg derefter **Afvis** i menuen.</span><span class="sxs-lookup"><span data-stu-id="12728-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="12728-349">På den **Opgave**-side, der vises, skal du angive **QMS** som den *Læg på lager*-lokation, hvor pallen skal sendes til yderligere inspektion.</span><span class="sxs-lookup"><span data-stu-id="12728-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="12728-350">Siden **Kvalitet i kvalitetskontrol: læg på lager** viser oplysninger om læg på lager-arbejdet:</span><span class="sxs-lookup"><span data-stu-id="12728-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="12728-351">**LOK:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="12728-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="12728-352">Denne lokation er den angivne læg på lager-lokation for modtagelse af afvist kvalitet.</span><span class="sxs-lookup"><span data-stu-id="12728-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="12728-353">**LP:** Det systemgenererede id</span><span class="sxs-lookup"><span data-stu-id="12728-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="12728-354">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="12728-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="12728-355">**Antal:** *1 PL: 100 hver*</span><span class="sxs-lookup"><span data-stu-id="12728-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="12728-356">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="12728-356">The item description is also shown.</span></span>

1. <span data-ttu-id="12728-357">Bekræft læg på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="12728-358">På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført".</span><span class="sxs-lookup"><span data-stu-id="12728-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="12728-359">Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.</span><span class="sxs-lookup"><span data-stu-id="12728-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="12728-360">Du har nu fuldført kvalitetskontrollen og oprettet en kvalitetsordre for den afviste palle.</span><span class="sxs-lookup"><span data-stu-id="12728-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="12728-361">Hvis du vil se den ordre, der er oprettet, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="12728-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="12728-362">Test af kvalitetsordre kan nu behandles.</span><span class="sxs-lookup"><span data-stu-id="12728-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="12728-363">Kvalitetstesten beskrives ikke i dette emne.</span><span class="sxs-lookup"><span data-stu-id="12728-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="12728-364">Du kan finde flere oplysninger om kvalitetsstyring under [Oversigt over kvalitetsstyring](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="12728-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="12728-365">Modtage palle 3</span><span class="sxs-lookup"><span data-stu-id="12728-365">Receive pallet 3</span></span>

<span data-ttu-id="12728-366">I dette scenario vil palle 3 blive accepteret.</span><span class="sxs-lookup"><span data-stu-id="12728-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="12728-367">Angiv **1** i feltet *LINJENUM*, og bekræft linjenummeret.</span><span class="sxs-lookup"><span data-stu-id="12728-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="12728-368">Feltet **Antal** er nu tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="12728-368">The **QTY** field is now available.</span></span> <span data-ttu-id="12728-369">Angiv *1*, og bekræft antallet.</span><span class="sxs-lookup"><span data-stu-id="12728-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="12728-370">Siden **Kvalitetskontrol** vises.</span><span class="sxs-lookup"><span data-stu-id="12728-370">The **Quality check** page appears.</span></span> <span data-ttu-id="12728-371">I forbindelse med denne modtagelse vil pallen blive accepteret for kvalitet, og den vil blive placeret i lokationen for masselæg på lager.</span><span class="sxs-lookup"><span data-stu-id="12728-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="12728-372">Vælg bekræftelsesknappen for at bestå kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="12728-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="12728-373">Siden **Indkøbsordrer: læg på lager** viser oplysninger om læg på lager-arbejdet:</span><span class="sxs-lookup"><span data-stu-id="12728-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="12728-374">**LOK:** Systemet har fastlagt lokationen</span><span class="sxs-lookup"><span data-stu-id="12728-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="12728-375">Denne lokation er den angivne læg på lager-lokation for modtagelse af indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="12728-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="12728-376">**LP:** Det systemgenererede id</span><span class="sxs-lookup"><span data-stu-id="12728-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="12728-377">**Vare:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="12728-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="12728-378">**Antal:** *1 PL: 100 hver*</span><span class="sxs-lookup"><span data-stu-id="12728-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="12728-379">Varebeskrivelsen vises også.</span><span class="sxs-lookup"><span data-stu-id="12728-379">The item description is also shown.</span></span>

1. <span data-ttu-id="12728-380">Bekræft læg på lager-arbejdet.</span><span class="sxs-lookup"><span data-stu-id="12728-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="12728-381">På siden **Opgave** for modtagelse af indkøbsordrelinje vises meddelelsen "Arbejde fuldført".</span><span class="sxs-lookup"><span data-stu-id="12728-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="12728-382">Feltet **LINJENUM** er tilgængeligt, så du kan begynde at modtage den næste palle.</span><span class="sxs-lookup"><span data-stu-id="12728-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="12728-383">Vælg menuknappen (**≡**) øverst på siden, og vælg derefter **Annuller** i menuen for at gå tilbage til menuen.</span><span class="sxs-lookup"><span data-stu-id="12728-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="12728-384">Du kan nu lukke mobilappen.</span><span class="sxs-lookup"><span data-stu-id="12728-384">You can now close the mobile app.</span></span>
