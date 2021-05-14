---
title: Konfigurer en detailkanal
description: Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937528"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="81bdb-103">Konfigurere en detailkanal</span><span class="sxs-lookup"><span data-stu-id="81bdb-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="81bdb-104">Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="81bdb-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="81bdb-105">Dynamics 365 Commerce understøtter flere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="81bdb-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="81bdb-106">Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="81bdb-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="81bdb-107">Hver detailbutikskanal kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="81bdb-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="81bdb-108">Du skal oprette alle disse elementer, for at du kan oprette en detailbutikskanal.</span><span class="sxs-lookup"><span data-stu-id="81bdb-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="81bdb-109">Før du opretter en detailkanal, skal du sikre dig, at du følger [kanalens forudsætninger](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="81bdb-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="81bdb-110">Oprette og konfigurere en ny detailkanal</span><span class="sxs-lookup"><span data-stu-id="81bdb-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="81bdb-111">Gå til **Moduler \> Kanaler \> Butikker \> Onlinebutikker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="81bdb-112">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-113">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="81bdb-114">Angiv et entydigt butiksnummer i feltet **Butiksnummer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="81bdb-115">Nummeret kan være alfanumerisk med højst 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="81bdb-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="81bdb-116">Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="81bdb-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="81bdb-117">Angiv det relevante **Lagersted** på rullelisten Lagersted.</span><span class="sxs-lookup"><span data-stu-id="81bdb-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="81bdb-118">Vælg den relevante tidszone i feltet **Lagertidszone**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="81bdb-119">Vælg en relevant for momsgruppe butikken på rullelisten **Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="81bdb-120">Vælg den relevante valuta i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="81bdb-121">Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="81bdb-122">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="81bdb-123">Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="81bdb-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="81bdb-124">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="81bdb-125">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="81bdb-126">Følgende billede viser oprettelsen af en ny detailkanal.</span><span class="sxs-lookup"><span data-stu-id="81bdb-126">The following image shows the creation of a new retail channel.</span></span>

![Ny detailkanal](media/channel-setup-retail-1.png)

<span data-ttu-id="81bdb-128">Følgende billede viser et eksempel på en detailkanal.</span><span class="sxs-lookup"><span data-stu-id="81bdb-128">The following image shows an example retail channel.</span></span>

![Eksempel på detailkanal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="81bdb-130">Andre indstillinger</span><span class="sxs-lookup"><span data-stu-id="81bdb-130">Other settings</span></span>

<span data-ttu-id="81bdb-131">Der er adskillige andre valgfrie indstillinger, du kan angive i sektionerne **Opgørelse/ultimo** og **Diverse**, afhængigt af behovene i detailbutikken.</span><span class="sxs-lookup"><span data-stu-id="81bdb-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="81bdb-132">Du kan også se [Skærmlayout til POS](pos-screen-layouts.md) for at få oplysninger om, hvordan du konfigurerer standardskærmlayoutet, i afsnittet **Skærmlayout** og [Konfigurerer og installerer Retail hardware Station](retail-hardware-station-configuration-installation.md) for at få oplysninger om installation af afsnittet **Hardwarestationer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="81bdb-133">Følgende billede viser et eksempel på konfiguration af en detailkanal.</span><span class="sxs-lookup"><span data-stu-id="81bdb-133">The following image shows an example retail channel setup configuration.</span></span>

![Eksempel på detailkanalkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="81bdb-135">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="81bdb-135">Additional channel set up</span></span>

<span data-ttu-id="81bdb-136">Der er flere elementer, der skal konfigureres for en kanal, som findes i handlingsruden under sektionen **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="81bdb-137">Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, kontantopgørelse, leveringsmetoder, indtægts/udgiftskonto, sektioner gruppetildeling for opfyldelse og pengeskabe.</span><span class="sxs-lookup"><span data-stu-id="81bdb-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="81bdb-138">I følgende billede vises de yderligere indstillinger for opsætning af detailkanal under fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Konfigurer kanal](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="81bdb-140">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="81bdb-140">Set up payment methods</span></span>

<span data-ttu-id="81bdb-141">Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="81bdb-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="81bdb-142">Vælg fanen **Konfigurer** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="81bdb-143">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-144">Vælg den ønskede betalingsmetode i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="81bdb-145">Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.</span><span class="sxs-lookup"><span data-stu-id="81bdb-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="81bdb-146">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="81bdb-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="81bdb-147">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="81bdb-148">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="81bdb-148">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="81bdb-150">Opsætning af kontantopgørelse</span><span class="sxs-lookup"><span data-stu-id="81bdb-150">Set up cash declaration</span></span>

1. <span data-ttu-id="81bdb-151">Vælg fanen **Konfigurer** i handlingsruden, og vælg derefter **Kontantopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="81bdb-152">Vælg **Ny** i handlingsruden, og opret derefter alle relevante betegnelser for **Mønt** og **Pengeseddel**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="81bdb-153">Følgende billede viser et eksempel på en kontantopgørelse.</span><span class="sxs-lookup"><span data-stu-id="81bdb-153">The following image shows an example of a cash declaration.</span></span>

![Opsætning af kontantopgørelser](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="81bdb-155">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="81bdb-155">Set up modes of delivery</span></span>

<span data-ttu-id="81bdb-156">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmåder** under fanen **Konfigurer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="81bdb-157">Udfør følgende trin for at ændre eller tilføje en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="81bdb-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="81bdb-158">Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="81bdb-159">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmåde, eller vælg en eksisterende måde.</span><span class="sxs-lookup"><span data-stu-id="81bdb-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="81bdb-160">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen.</span><span class="sxs-lookup"><span data-stu-id="81bdb-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="81bdb-161">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="81bdb-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="81bdb-162">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="81bdb-162">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="81bdb-164">Konfigurer indtægts/udgiftskonto</span><span class="sxs-lookup"><span data-stu-id="81bdb-164">Set up income/expense account</span></span>

<span data-ttu-id="81bdb-165">Gør følgende for at konfigurere en indtægts/udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="81bdb-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="81bdb-166">Vælg fanen **Konfigurer** i handlingsruden, og vælg derefter **Indtægts/udgiftskonto**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="81bdb-167">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-168">Angiv et navn under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="81bdb-169">Angiv et søgenavn under **Søgenavn**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="81bdb-170">Angiv kontotypen under **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="81bdb-171">Angiv tekst for **Meddelelseslinje 1**, **Meddelelseslinje 2**, **Bilag 1** og **Bilag 2** efter behov.</span><span class="sxs-lookup"><span data-stu-id="81bdb-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="81bdb-172">Angiv bogføringsoplysninger under **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="81bdb-173">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="81bdb-174">Følgende billede viser et eksempel på en indtægts/udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="81bdb-174">The following image shows an example of an income/expense account.</span></span>

![Konfigurer indtægts/udgiftskonti](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="81bdb-176">Konfigurere sektioner</span><span class="sxs-lookup"><span data-stu-id="81bdb-176">Set up sections</span></span>

<span data-ttu-id="81bdb-177">Gør følgende for at konfigurere sektioner.</span><span class="sxs-lookup"><span data-stu-id="81bdb-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="81bdb-178">I handlingsruden skal du vælge **Sektioner** under **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="81bdb-179">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-180">Angiv et sektionsnummer under **Sektionsnummer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="81bdb-181">Indtast en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="81bdb-182">Angiv en sektionsstørrelse under **Sektionsstørrelse**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="81bdb-183">Konfigurer yderligere indstillinger for **Generelt** og **Salgsstatistik** efter behov.</span><span class="sxs-lookup"><span data-stu-id="81bdb-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="81bdb-184">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="81bdb-185">Konfigurer en gruppetildeling for opfyldelse</span><span class="sxs-lookup"><span data-stu-id="81bdb-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="81bdb-186">Gør følgende for at konfigurere en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="81bdb-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="81bdb-187">Vælg fanen **Konfigurer** i handlingsruden, og vælg derefter **Tildeling af opfyldelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="81bdb-188">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-189">Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="81bdb-190">Indtast en beskrivelse i rullelisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="81bdb-191">Vælg **Gem** i handlingsruden</span><span class="sxs-lookup"><span data-stu-id="81bdb-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="81bdb-192">Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="81bdb-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Konfigurer gruppetildelinger for opfyldelse](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="81bdb-194">Konfigurer pengeskabe</span><span class="sxs-lookup"><span data-stu-id="81bdb-194">Set up safes</span></span>

<span data-ttu-id="81bdb-195">Gør følgende for at konfigurere pengeskabe.</span><span class="sxs-lookup"><span data-stu-id="81bdb-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="81bdb-196">I handlingsruden skal du vælge **Pengeskabe** under **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="81bdb-197">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="81bdb-198">Angiv et navn til pengeskabet.</span><span class="sxs-lookup"><span data-stu-id="81bdb-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="81bdb-199">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81bdb-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="81bdb-200">Sikre entydige transaktions-id'er</span><span class="sxs-lookup"><span data-stu-id="81bdb-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="81bdb-201">Fra Commerce-version 10.0.18 er de transaktions-id'er der genereres for POS, fortløbende og omfatter følgende dele:</span><span class="sxs-lookup"><span data-stu-id="81bdb-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="81bdb-202">En fast del, der er en sammenkædning af butiks-id og terminal-id.</span><span class="sxs-lookup"><span data-stu-id="81bdb-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="81bdb-203">En fortløbende del, der er en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="81bdb-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="81bdb-204">Formatet er specifikt *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="81bdb-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="81bdb-205">Da transaktions-id'er kan genereres i offline- og onlinetilstand, er der genereret forekomster af identiske transaktions-id'er.</span><span class="sxs-lookup"><span data-stu-id="81bdb-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="81bdb-206">Eliminering af identiske transaktions-id'er kræver mange manuelle datarettelser.</span><span class="sxs-lookup"><span data-stu-id="81bdb-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="81bdb-207">Med Commerce version 10.0.19 er formatet for transaktions-id'et opdateret, så den fortløbende del er fjernet, og der i stedet anvendes et 13-cifret nummer, der genereres ved at beregne tiden i millisekunder siden 1970.</span><span class="sxs-lookup"><span data-stu-id="81bdb-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="81bdb-208">Med denne ændring er det nye transaktions-id-format *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="81bdb-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="81bdb-209">Denne opdatering betyder, at transaktions-id'et ikke er fortløbende, og sikrer, at transaktions-id'er altid er entydige.</span><span class="sxs-lookup"><span data-stu-id="81bdb-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="81bdb-210">Transaktions-id'er er kun beregnet til brug i det interne system, så de behøver ikke være fortløbende.</span><span class="sxs-lookup"><span data-stu-id="81bdb-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="81bdb-211">Mange lande/områder kræver dog, at kvitterings-id'er er fortløbende.</span><span class="sxs-lookup"><span data-stu-id="81bdb-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="81bdb-212">Det nye formatfunktion for transaktions-id'er kan aktiveres fra arbejdsområdet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="81bdb-213">Benyt følgende fremgangsmåde, hvis du vil aktivere brugen af de nye transaktions-id'er:</span><span class="sxs-lookup"><span data-stu-id="81bdb-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="81bdb-214">I Commerce-hovedkvarteret skal du gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="81bdb-215">Filtrer efter modulet "Retail og Commerce".</span><span class="sxs-lookup"><span data-stu-id="81bdb-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="81bdb-216">Søg efter funktionsnavnet **Aktiver nyt transaktions-id for at undgå identiske transaktions-id'er**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="81bdb-217">Vælg funktionen, og vælg derefter **Aktiver nu** i højre rude.</span><span class="sxs-lookup"><span data-stu-id="81bdb-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="81bdb-218">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="81bdb-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="81bdb-219">Kør jobbene **Konfiguration af 1070-kanal** og **1170 POS-opgaveoptager** for at synkronisere den aktiverede funktion med butikkerne.</span><span class="sxs-lookup"><span data-stu-id="81bdb-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="81bdb-220">Når ændringerne er sendt til butikkerne, skal POS-terminaler lukkes og åbnes igen for at bruge det nye transaktions-id-format.</span><span class="sxs-lookup"><span data-stu-id="81bdb-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="81bdb-221">Når den nye funktion til transaktions-id-format er aktiveret, kan du ikke deaktivere denne funktion.</span><span class="sxs-lookup"><span data-stu-id="81bdb-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="81bdb-222">Hvis den skal deaktiveres, skal du kontakte Commerce Support.</span><span class="sxs-lookup"><span data-stu-id="81bdb-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81bdb-223">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="81bdb-223">Additional resources</span></span>

[<span data-ttu-id="81bdb-224">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="81bdb-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="81bdb-225">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="81bdb-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="81bdb-226">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="81bdb-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="81bdb-227">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="81bdb-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
