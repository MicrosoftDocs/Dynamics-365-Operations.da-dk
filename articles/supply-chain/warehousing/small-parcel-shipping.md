---
title: Forsendelse af småpakker
description: Dette emne indeholder oplysninger om funktionen til forsendelse af småpakker (SPS). Denne funktion sætter Microsoft Dynamics 365 Supply Chain Management i stand til at sende oplysninger om en pakket container til fragtmanden og derefter modtage en forsendelseslabel, forsendelsessats og sporingsnummeret fra fragtmanden.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3969ee6b46f38fe2650881fb0183c60aadce6c8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831164"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="3767a-104">Forsendelse af småpakker</span><span class="sxs-lookup"><span data-stu-id="3767a-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3767a-105">Funktionen til forsendelse af småpakker (SPS) giver Microsoft Dynamics 365 Supply Chain Management mulighed for at kommunikere direkte med fragtmænd ved at give en struktur til kommunikation via fragtmands-API'er.</span><span class="sxs-lookup"><span data-stu-id="3767a-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="3767a-106">Denne funktionalitet er nyttig, når du sender individuelle salgsordrer via kommercielle fragtmænd i stedet for at bruge containerforsendelse eller LTL (Less than Load)-forsendelse.</span><span class="sxs-lookup"><span data-stu-id="3767a-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="3767a-107">SPS-funktionen interagerer med fragtmanden via et dedikeret *satsprogram*.</span><span class="sxs-lookup"><span data-stu-id="3767a-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="3767a-108">Din organisation skal udvikle dette satsprogram i samarbejde med din fragtmand eller fragtmandens hubtjeneste.</span><span class="sxs-lookup"><span data-stu-id="3767a-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="3767a-109">Satsprogrammet sætter Supply Chain Management i stand til at sende oplysninger om en pakket container til fragtmanden og derefter modtage en forsendelseslabel, forsendelsessats og sporingsnummeret fra fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="3767a-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="3767a-110">Den forsendelsessats, der returneres, føjes til den tilknyttede salgsordre som et tillægsgebyr.</span><span class="sxs-lookup"><span data-stu-id="3767a-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="3767a-111">Den forsendelsesetiket, der returneres, kan derefter automatisk udskrives ved hjælp af en ZPL-printer (Zebra Programming Language) og anvendes på forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="3767a-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="3767a-112">Fragtmanden vil scanne denne forsendelsesetiket ved afhentning af pakkerne på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="3767a-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="3767a-113">Forberede systemet til at understøtte SPS</span><span class="sxs-lookup"><span data-stu-id="3767a-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="3767a-114">Før du kan begynde at bruge SPS-funktionalitet, skal du aktivere SPS-funktionen i Funktionsstyring, tilføje satsprogrammet og konfigurere modulerne **Transportstyring** og **Lokationsstyring** for at understøtte funktionen.</span><span class="sxs-lookup"><span data-stu-id="3767a-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="3767a-115">Slå SPS-funktionen til</span><span class="sxs-lookup"><span data-stu-id="3767a-115">Turn on the SPS feature</span></span>

<span data-ttu-id="3767a-116">Før du kan bruge SPS-funktionen, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="3767a-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="3767a-117">Administratorer kan bruge arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="3767a-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3767a-118">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="3767a-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3767a-119">**Module** *Transportstyring*</span><span class="sxs-lookup"><span data-stu-id="3767a-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="3767a-120">**Funktionsnavn:** *Forsendelse af småpakker*</span><span class="sxs-lookup"><span data-stu-id="3767a-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="3767a-121">Implementere og konfigurere satsprogrammer</span><span class="sxs-lookup"><span data-stu-id="3767a-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="3767a-122">Supply Chain Management inkluderer ikke nogen satsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="3767a-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="3767a-123">Du skal anskaffe eller oprette de satsprogrammer, du har brug for, og derefter føje dem til systemet.</span><span class="sxs-lookup"><span data-stu-id="3767a-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="3767a-124">Microsoft stiller dog et demosatsprogram til rådighed, som du kan bruge til test.</span><span class="sxs-lookup"><span data-stu-id="3767a-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="3767a-125">Downloade og installere demosatsprogrammet</span><span class="sxs-lookup"><span data-stu-id="3767a-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="3767a-126">Følg disse trin for at hente demosatsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3767a-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="3767a-127">På GitHub kan du downloade [DLL-værten (dynamic-link library) til demosatsprogrammet](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="3767a-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="3767a-128">På din Supply Chain Management-server skal du gemme DLL'en i mappen **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="3767a-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="3767a-129">Oprette og implementere funktionelle satsprogrammer</span><span class="sxs-lookup"><span data-stu-id="3767a-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="3767a-130">Du kan finde flere oplysninger om oprettelse og implementering af funktionelle satsprogrammer, så de kan bruges i en produktion eller et testmiljø, under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="3767a-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="3767a-131">Oprette et nyt transportstyringsprogram</span><span class="sxs-lookup"><span data-stu-id="3767a-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="3767a-132">Konfigurere transportstyringsprogrammer</span><span class="sxs-lookup"><span data-stu-id="3767a-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="3767a-133">Yderligere oplysninger om, hvordan du opretter et SPS-satsprogram, finder du i følgende blogindlæg: [Forsendelse af småpakker: Sådan udnytter du funktionen til forsendelse af småpakker i Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="3767a-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="3767a-134">Konfigurere et satsprogram i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3767a-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="3767a-135">Når du har oprettet og implementeret et satsprogram til SPS, skal du følge disse trin for at konfigurere det.</span><span class="sxs-lookup"><span data-stu-id="3767a-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="3767a-136">Gå til **Transportstyring \> Opsætning \> Programmer \> Satsprogram**.</span><span class="sxs-lookup"><span data-stu-id="3767a-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="3767a-137">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="3767a-138">Angiv følgende felter i den nye række:</span><span class="sxs-lookup"><span data-stu-id="3767a-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="3767a-139">**Vurderingsprogram** – Angiv et entydigt navn til satsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3767a-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="3767a-140">Hvis du bruger demosatsprogrammet, skal du angive *Demosatsprogram*.</span><span class="sxs-lookup"><span data-stu-id="3767a-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="3767a-141">**Navn** – Angiv en kort beskrivelse af satsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="3767a-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="3767a-142">Hvis du bruger demosatsprogrammet, skal du angive *Demosatsprogram*.</span><span class="sxs-lookup"><span data-stu-id="3767a-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="3767a-143">**Vurderingsmetadata-id** – Vælg det grundlag, der skal bruges til at beregne din sats.</span><span class="sxs-lookup"><span data-stu-id="3767a-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="3767a-144">Din sats kan f.eks. beregnes ud fra afstand.</span><span class="sxs-lookup"><span data-stu-id="3767a-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="3767a-145">Hvis du bruger demosatsprogrammet, kan du lade dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="3767a-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="3767a-146">**Programsamling** – Angiv filnavnet på den DLL-pakke, du har implementeret.</span><span class="sxs-lookup"><span data-stu-id="3767a-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="3767a-147">Hvis du bruger demosatsprogrammet, skal du angive *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="3767a-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="3767a-148">**Programklasse** – Angiv det klassenavn, der blev oprettet for dit satsprogram.</span><span class="sxs-lookup"><span data-stu-id="3767a-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="3767a-149">Hvis du bruger demosatsprogrammet, skal du angive *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="3767a-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3767a-150">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="3767a-150">Example scenario</span></span>

<span data-ttu-id="3767a-151">I dette eksempelscenarie vises, hvordan du konfigurerer og bruger SPS, når du har forberedt systemet som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="3767a-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="3767a-152">I dette scenarie bruges det tidligere nævnte demosatsprogram.</span><span class="sxs-lookup"><span data-stu-id="3767a-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="3767a-153">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="3767a-153">Make demo data available</span></span>

<span data-ttu-id="3767a-154">Hvis du vil arbejde gennem dette scenarie ved hjælp af de demoposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="3767a-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="3767a-155">Derudover skal du vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="3767a-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="3767a-156">Konfigurere scenariet</span><span class="sxs-lookup"><span data-stu-id="3767a-156">Set up the scenario</span></span>

<span data-ttu-id="3767a-157">I dette eksempelscenarie skal du have en demofragtmand, fragtmandsgruppe, pakkepolitik og pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="3767a-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="3767a-158">I følgende underafsnit forklares, hvordan du kan forberede de poster, der kræves til scenariet.</span><span class="sxs-lookup"><span data-stu-id="3767a-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="3767a-159">I et produktionsscenarie ligner opsætningsprocessen typisk den proces, der er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="3767a-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="3767a-160">Du skal dog angive forskellige værdier.</span><span class="sxs-lookup"><span data-stu-id="3767a-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="3767a-161">Konfigurere fragtmænd</span><span class="sxs-lookup"><span data-stu-id="3767a-161">Set up carriers</span></span>

<span data-ttu-id="3767a-162">Følg disse trin for at konfigurere en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3767a-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="3767a-163">Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.</span><span class="sxs-lookup"><span data-stu-id="3767a-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="3767a-164">Vælg **Ny** i handlingsruden for at tilføje en fragtmand.</span><span class="sxs-lookup"><span data-stu-id="3767a-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="3767a-165">Angiv følgende værdier på hoveddelen:</span><span class="sxs-lookup"><span data-stu-id="3767a-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="3767a-166">**Fragtmand:** *Demofragtmand*</span><span class="sxs-lookup"><span data-stu-id="3767a-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="3767a-167">**Navn:** *Demofragtmand*</span><span class="sxs-lookup"><span data-stu-id="3767a-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="3767a-168">**Tilstand:** *Fragt*</span><span class="sxs-lookup"><span data-stu-id="3767a-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="3767a-169">I oversigtspanelet **Oversigt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3767a-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3767a-170">**Aktivere fragtmand:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3767a-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="3767a-171">**Aktivere fragtmandsvurdering:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3767a-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="3767a-172">Gå til oversigtspanelet **Tjenester**, og vælg **Ny** for at føje en tjeneste til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="3767a-173">Angiv følgende værdier for den nye tjeneste:</span><span class="sxs-lookup"><span data-stu-id="3767a-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="3767a-174">**Fragttjeneste:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="3767a-175">**Navn:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="3767a-176">**Transportmetode:** *Fragt*</span><span class="sxs-lookup"><span data-stu-id="3767a-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="3767a-177">Angiv tilfældige værdier for alle de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="3767a-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="3767a-178">(Når du gemmer den nye fragtmandspost, oprettes der en ny leveringsmåde, og Feltet **Leveringsmåde** angives automatisk).</span><span class="sxs-lookup"><span data-stu-id="3767a-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="3767a-179">I oversigtspanelet **Vurderingsprofiler** skal du vælge **Ny** for at føje en vurderingsprofil til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="3767a-180">Angiv følgende værdier for den nye profil:</span><span class="sxs-lookup"><span data-stu-id="3767a-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="3767a-181">**Vurderingsprofil:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="3767a-182">**Navn:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="3767a-183">**Satsprogram:** *Demosatsprogram*</span><span class="sxs-lookup"><span data-stu-id="3767a-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="3767a-184">Angiv tilfældige værdier for alle de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="3767a-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="3767a-185">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="3767a-186">Du kan finde flere oplysninger om at konfigurere fragtmænd under [Konfigurere fragtmænd](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="3767a-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="3767a-187">Konfigurere fragttjenestekonti</span><span class="sxs-lookup"><span data-stu-id="3767a-187">Set up carrier service accounts</span></span>

<span data-ttu-id="3767a-188">Følg disse trin for at konfigurere en fragttjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="3767a-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="3767a-189">Gå til **Transportstyring \> Opsætning \> Klassificering \> Fragttjenestekonto**.</span><span class="sxs-lookup"><span data-stu-id="3767a-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="3767a-190">Gå til handlingsruden, og vælg **Ny** for at tilføje en fragttjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="3767a-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="3767a-191">Angiv følgende værdier for den nye konto:</span><span class="sxs-lookup"><span data-stu-id="3767a-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="3767a-192">**Fragtmand:** *Demofragtmand*</span><span class="sxs-lookup"><span data-stu-id="3767a-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="3767a-193">**Fragttjeneste:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="3767a-194">**Debitorkontonummer for fragtmand:** Det debitorkontonummer for fragtmanden, der bruges til at kontrollere og godkende forbindelsen til fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="3767a-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="3767a-195">Din fragtmand angiver denne værdi.</span><span class="sxs-lookup"><span data-stu-id="3767a-195">Your carrier will provide this value.</span></span> <span data-ttu-id="3767a-196">Hvis du bruger demotjenesten, kan du angive en tilfældig værdi.</span><span class="sxs-lookup"><span data-stu-id="3767a-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="3767a-197">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="3767a-197">**Site:** *6*</span></span>
    - <span data-ttu-id="3767a-198">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="3767a-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="3767a-199">Ofte er værdien **Debitorkontonummer for fragtmand** den eneste værdi, der kræves for at godkende forbindelsen.</span><span class="sxs-lookup"><span data-stu-id="3767a-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="3767a-200">Men hvis fragtmanden kræver yderligere godkendelsesparametre, skal din organisation tilpasse denne side for at tilføje ekstra felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="3767a-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="3767a-201">Konfigurere en politik for containerpakning</span><span class="sxs-lookup"><span data-stu-id="3767a-201">Set up a container packing policy</span></span>

<span data-ttu-id="3767a-202">Følg disse trin for at konfigurere en politik for containerpakning:</span><span class="sxs-lookup"><span data-stu-id="3767a-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="3767a-203">Hvis du ikke allerede har konfigureret en ZPL-printerdefinition, skal du bruge programmet Dokumentets ruteplanlægningsagent til at konfigurere den.</span><span class="sxs-lookup"><span data-stu-id="3767a-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="3767a-204">Yderligere oplysninger finder du i [Oversigt over udskrivning af dokumenter](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og relaterede emner.</span><span class="sxs-lookup"><span data-stu-id="3767a-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="3767a-205">Gå til **Lokationsstyring \> Konfiguration \> Containere \> Politikker for containerpakning**.</span><span class="sxs-lookup"><span data-stu-id="3767a-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="3767a-206">Gå til handlingsruden, og vælg **Ny** for at tilføje en politik for containerpakning.</span><span class="sxs-lookup"><span data-stu-id="3767a-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="3767a-207">Angiv følgende værdier på hoveddelen for den nye politik:</span><span class="sxs-lookup"><span data-stu-id="3767a-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="3767a-208">**Politik for containerpakning:** *Politik for demopakning*</span><span class="sxs-lookup"><span data-stu-id="3767a-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="3767a-209">**Beskrivelse:** En beskrivelse af politikken</span><span class="sxs-lookup"><span data-stu-id="3767a-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="3767a-210">I oversigtspanelet **Oversigt** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3767a-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3767a-211">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="3767a-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3767a-212">**Standardlokation til endelig forsendelse:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="3767a-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="3767a-213">**Vægtenhed:** *KG*</span><span class="sxs-lookup"><span data-stu-id="3767a-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="3767a-214">**Politik for containerlukning:** *Automatisk frigivelse*</span><span class="sxs-lookup"><span data-stu-id="3767a-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="3767a-215">**Politik for containerfrigivelse:** *Gør disponibel ved endelig afsendelseslokation*</span><span class="sxs-lookup"><span data-stu-id="3767a-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="3767a-216">I oversigtspanelet **Containermanifest** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3767a-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3767a-217">**Automatisk manifest ved containerlukning:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="3767a-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="3767a-218">**Manifestkrav til container:** *Transportstyring*</span><span class="sxs-lookup"><span data-stu-id="3767a-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="3767a-219">**Udskriv containerindhold:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="3767a-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="3767a-220">I oversigtspanelet **Udskrivning af fragtetiket** skal du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3767a-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3767a-221">**Udskriv forsendelsesetiket til containere:** *Altid*</span><span class="sxs-lookup"><span data-stu-id="3767a-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="3767a-222">**Printernavn:** Navnet på den ZPL-printer, der skal udskrive forsendelsesetiketter</span><span class="sxs-lookup"><span data-stu-id="3767a-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="3767a-223">Konfigurere en pakningsprofil</span><span class="sxs-lookup"><span data-stu-id="3767a-223">Set up a packing profile</span></span>

<span data-ttu-id="3767a-224">Følg disse trin for at konfigurere en pakningsprofil.</span><span class="sxs-lookup"><span data-stu-id="3767a-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="3767a-225">Gå til **Lokationsstyring \> Konfiguration \> Pakning \> Pakningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="3767a-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="3767a-226">Gå til handlingsruden, og vælg **Ny** for at føje en pakningsprofil til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="3767a-227">Angiv følgende værdier for den nye profil:</span><span class="sxs-lookup"><span data-stu-id="3767a-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="3767a-228">**Pakkeprofil-id:** *Demopakningsprofil*</span><span class="sxs-lookup"><span data-stu-id="3767a-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="3767a-229">**Beskrivelse:** En beskrivelse af profilen</span><span class="sxs-lookup"><span data-stu-id="3767a-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="3767a-230">**Politik for containerpakning:** *Politik for demopakning*</span><span class="sxs-lookup"><span data-stu-id="3767a-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="3767a-231">**Container-id-tilstand:** *Auto*</span><span class="sxs-lookup"><span data-stu-id="3767a-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="3767a-232">**Containertype:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="3767a-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="3767a-233">Konfigurere en debitor til at bruge SPS-fragtmanden</span><span class="sxs-lookup"><span data-stu-id="3767a-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="3767a-234">Følg disse trin for at konfigurere en kunde, så denne kan bruge den fragtmand, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="3767a-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="3767a-235">Gå til **Debitor \> Debitorer \> Alle debitorer**.</span><span class="sxs-lookup"><span data-stu-id="3767a-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="3767a-236">Find og vælg debitor *US-027* i gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="3767a-237">Vælg **Debitorkonti for fragtmand** i gruppen **Konfiguration** på fanen **Generelt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="3767a-238">Vælg **Ny** på siden **Debitorkonti for fragtmand** i handlingsruden for at føje en konto til gitteret.</span><span class="sxs-lookup"><span data-stu-id="3767a-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="3767a-239">Angiv følgende værdier for den nye konto:</span><span class="sxs-lookup"><span data-stu-id="3767a-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="3767a-240">**Fragtmand:** *Demofragtmand*</span><span class="sxs-lookup"><span data-stu-id="3767a-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="3767a-241">**Debitorkontonummer for fragtmand:** *12345* (værdien er ikke vigtig for dette scenarie, men der vil blive henvist til den i næste afsnit).</span><span class="sxs-lookup"><span data-stu-id="3767a-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="3767a-242">Gennemgå eksempelscenariet</span><span class="sxs-lookup"><span data-stu-id="3767a-242">Go through the example scenario</span></span>

<span data-ttu-id="3767a-243">Når du har konfigureret alle eksempeldataene som beskrevet i forrige afsnit, er du klar til at gennemgå eksempelscenariet.</span><span class="sxs-lookup"><span data-stu-id="3767a-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="3767a-244">Oprette en salgsordre og behandle arbejdet</span><span class="sxs-lookup"><span data-stu-id="3767a-244">Create a sales order and process the work</span></span>

<span data-ttu-id="3767a-245">Følg disse trin for at oprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3767a-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="3767a-246">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="3767a-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3767a-247">Vælg **Ny** for at oprette en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="3767a-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="3767a-248">Gå til dialogboksen **Opret salgsordre**, og angiv **US-027** i feltet *Debitorkonto*.</span><span class="sxs-lookup"><span data-stu-id="3767a-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="3767a-249">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3767a-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="3767a-250">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="3767a-250">The new sales order is opened.</span></span> <span data-ttu-id="3767a-251">I oversigtspanelet **Salgsordrehoved** skal du angive feltet **Debitorkontonummer for fragtmand** til den værdi, du valgte for denne debitor tidligere (*12345*).</span><span class="sxs-lookup"><span data-stu-id="3767a-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="3767a-252">Tilføj en salgslinje i sektionen **Salgsordrelinjer**, og angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="3767a-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="3767a-253">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="3767a-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="3767a-254">**Antal:** *1*</span><span class="sxs-lookup"><span data-stu-id="3767a-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="3767a-255">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="3767a-255">**Site:** *6*</span></span>
    - <span data-ttu-id="3767a-256">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="3767a-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="3767a-257">Skift til **overskriftsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="3767a-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="3767a-258">I oversigtspanelet **Levering** kan du angive følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="3767a-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3767a-259">**Fragtmand:** *Demofragtmand*</span><span class="sxs-lookup"><span data-stu-id="3767a-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="3767a-260">**Fragttjeneste:** *Demofragtmandstjeneste*</span><span class="sxs-lookup"><span data-stu-id="3767a-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="3767a-261">Skift tilbage til visningen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="3767a-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="3767a-262">Hvis du bliver bedt om at opdatere leveringsmåden for salgslinjerne, skal du vælge **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3767a-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="3767a-263">I sektionen **Salgsordrelinjer** skal du vælge den ordrelinje, du konfigurerede tidligere, og derefter vælge **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="3767a-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="3767a-264">På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="3767a-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="3767a-265">Luk siden **Reservation** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3767a-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="3767a-266">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="3767a-267">Der oprettes arbejde for at flytte varer fra pluklokationen til pakkestationen.</span><span class="sxs-lookup"><span data-stu-id="3767a-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="3767a-268">I sektionen **Salgsordrelinjer** skal du vælge **Lagersted \> Forsendelsesoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="3767a-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="3767a-269">Notér forsendelses-id'et på siden **Forsendelsesoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="3767a-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="3767a-270">Du skal bruge det, når du pakker forsendelsen på pakkestationen.</span><span class="sxs-lookup"><span data-stu-id="3767a-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="3767a-271">Luk siden **Forsendelsesoplysninger** for at vende tilbage til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="3767a-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="3767a-272">Notér salgsordrenummeret, og gå derefter til **Lokationsstyring \> Arbejde \> Alt arbejde**.</span><span class="sxs-lookup"><span data-stu-id="3767a-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="3767a-273">Brug salgsordrenummeret til at finde og vælge det arbejde, der er oprettet for ordren.</span><span class="sxs-lookup"><span data-stu-id="3767a-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="3767a-274">I handlingsruden skal du på fanen **Arbejde** vælge **Fuldfør arbejde**.</span><span class="sxs-lookup"><span data-stu-id="3767a-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="3767a-275">Vælg et bruger-id i feltet **Bruger-id** på siden **Færdiggørelse af arbejde**.</span><span class="sxs-lookup"><span data-stu-id="3767a-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="3767a-276">Vælg derefter **Valider arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="3767a-277">Hvis arbejdet består valideringen du vælge **Fuldfør arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="3767a-278">Arbejdet er markeret som fuldført for at simulere bevægelsen af varer til pakkestationen.</span><span class="sxs-lookup"><span data-stu-id="3767a-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="3767a-279">Pakke forsendelsen</span><span class="sxs-lookup"><span data-stu-id="3767a-279">Pack the shipment</span></span>

<span data-ttu-id="3767a-280">Følg disse trin for at pakke forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="3767a-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="3767a-281">Gå til **Lokationsstyring \> Konfiguration \> Arbejder**, og kontrollér, at din brugerkonto er knyttet til en arbejderkonto til lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="3767a-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="3767a-282">Gå til **Lokationsstyring \> Pluk og containerisering \> Pakke**.</span><span class="sxs-lookup"><span data-stu-id="3767a-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="3767a-283">Angiv følgende værdier i dialogboksen **Vælg pakkestation**:</span><span class="sxs-lookup"><span data-stu-id="3767a-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3767a-284">**Lokation:** *6*</span><span class="sxs-lookup"><span data-stu-id="3767a-284">**Site:** *6*</span></span>
    - <span data-ttu-id="3767a-285">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="3767a-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="3767a-286">**Lokation:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="3767a-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="3767a-287">**Pakkeprofil-id:** *Demopakningsprofil*</span><span class="sxs-lookup"><span data-stu-id="3767a-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="3767a-288">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3767a-288">Select **OK**.</span></span>
1. <span data-ttu-id="3767a-289">Siden **Pakke** vises.</span><span class="sxs-lookup"><span data-stu-id="3767a-289">The **Pack** page appears.</span></span> <span data-ttu-id="3767a-290">I et produktionsscenarie scanner en arbejder en nummerplade eller et forsendelses-id.</span><span class="sxs-lookup"><span data-stu-id="3767a-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="3767a-291">I dette scenarie skal du dog åbne siden **Alle forsendelser** og slå forsendelsesnummeret op for den forsendelse, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="3767a-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="3767a-292">Angiv derefter denne værdi i feltet **Nummerplade eller forsendelse** på siden **Pakke**.</span><span class="sxs-lookup"><span data-stu-id="3767a-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="3767a-293">Du kan alternativt angive det forsendelses-id, du har noteret tidligere.</span><span class="sxs-lookup"><span data-stu-id="3767a-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="3767a-294">Gå til handlingsruden, og vælg **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="3767a-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="3767a-295">I den dialogboks, der vises, vises detaljer om den nye container.</span><span class="sxs-lookup"><span data-stu-id="3767a-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="3767a-296">Behold standardværdierne, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="3767a-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="3767a-297">På siden **Pakke** skal du i handlingsruden **Varepakning** i feltet **Identifikator** vælge *A0002* for at pakke denne vare.</span><span class="sxs-lookup"><span data-stu-id="3767a-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="3767a-298">Varen føjes til containeren.</span><span class="sxs-lookup"><span data-stu-id="3767a-298">The item is added to the container.</span></span>
1. <span data-ttu-id="3767a-299">Vælg **Containere til forsendelse** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3767a-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="3767a-300">Siden **Containere til forsendelse**, der vises, indeholder en række for den container, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="3767a-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="3767a-301">Feltet **Containermanifest-id** i denne række er dog tomt i øjeblikket, da du endnu ikke har modtaget forsendelsesetiketten og sporingsnummeret fra fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="3767a-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="3767a-302">Gå til handlingsruden, og vælg **Luk container**.</span><span class="sxs-lookup"><span data-stu-id="3767a-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="3767a-303">I dialogboksen **Luk container** skal du angive feltet **Bruttovægt** til *1 kg* og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="3767a-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="3767a-304">Forsendelsesetiketten skal nu udskrives på den ZPL-printer, du valgte tidligere.</span><span class="sxs-lookup"><span data-stu-id="3767a-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="3767a-305">Den skulle ligne følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="3767a-305">It should resemble the following example.</span></span>

    <span data-ttu-id="3767a-306">![Eksempel på forsendelsesetiket](media/sps-label-example.png "Eksempel på forsendelsesetiket")</span><span class="sxs-lookup"><span data-stu-id="3767a-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="3767a-307">Bemærk, at værdierne **Containermanifest-id** og **Samlet fragt** er tilføjet som modtaget fra fragtmanden.</span><span class="sxs-lookup"><span data-stu-id="3767a-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]