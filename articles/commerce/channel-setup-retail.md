---
title: Konfigurer en detailkanal
description: Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411042"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="a469d-103">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="a469d-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a469d-104">Dette emne beskriver, hvordan du opretter en ny detailkanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a469d-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a469d-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="a469d-105">Overview</span></span>

<span data-ttu-id="a469d-106">Dynamics 365 Commerce understøtter flere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="a469d-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="a469d-107">Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="a469d-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="a469d-108">Hver detailbutikskanal kan have sine egne betalingsmetoder, prisgrupper, POS-kasseapparater, indtægtskonti og udgiftskonti samt medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="a469d-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="a469d-109">Du skal oprette alle disse elementer, for at du kan oprette en detailbutikskanal.</span><span class="sxs-lookup"><span data-stu-id="a469d-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="a469d-110">Før du opretter en detailkanal, skal du sikre dig, at du følger [kanalens forudsætninger](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a469d-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="a469d-111">Oprette og konfigurere en ny detailkanal</span><span class="sxs-lookup"><span data-stu-id="a469d-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="a469d-112">Gå til **Moduler \> Kanaler \> Butikker \> Onlinebutikker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="a469d-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="a469d-113">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-114">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a469d-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="a469d-115">Angiv et entydigt butiksnummer i feltet **Butiksnummer**.</span><span class="sxs-lookup"><span data-stu-id="a469d-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="a469d-116">Nummeret kan være alfanumerisk med højst 10 tegn.</span><span class="sxs-lookup"><span data-stu-id="a469d-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="a469d-117">Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="a469d-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="a469d-118">Angiv det relevante **Lagersted** på rullelisten Lagersted.</span><span class="sxs-lookup"><span data-stu-id="a469d-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="a469d-119">Vælg den relevante tidszone i feltet **Lagertidszone**.</span><span class="sxs-lookup"><span data-stu-id="a469d-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="a469d-120">Vælg en relevant for momsgruppe butikken på rullelisten **Momsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="a469d-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="a469d-121">Vælg den relevante valuta i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="a469d-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="a469d-122">Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="a469d-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="a469d-123">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="a469d-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="a469d-124">Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil**, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="a469d-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="a469d-125">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="a469d-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="a469d-126">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a469d-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a469d-127">Følgende billede viser oprettelsen af en ny detailkanal.</span><span class="sxs-lookup"><span data-stu-id="a469d-127">The following image shows the creation of a new retail channel.</span></span>

![Ny detailkanal](media/channel-setup-retail-1.png)

<span data-ttu-id="a469d-129">Følgende billede viser et eksempel på en detailkanal.</span><span class="sxs-lookup"><span data-stu-id="a469d-129">The following image shows an example retail channel.</span></span>

![Eksempel på detailkanal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="a469d-131">Andre indstillinger</span><span class="sxs-lookup"><span data-stu-id="a469d-131">Other settings</span></span>

<span data-ttu-id="a469d-132">Der er adskillige andre valgfrie indstillinger, du kan angive i sektionerne **Opgørelse/ultimo** og **Diverse**, afhængigt af behovene i detailbutikken.</span><span class="sxs-lookup"><span data-stu-id="a469d-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="a469d-133">Du kan også se [Skærmlayout til POS](pos-screen-layouts.md) for at få oplysninger om, hvordan du konfigurerer standardskærmlayoutet, i afsnittet **Skærmlayout** og [Konfigurerer og installerer Retail hardware Station](retail-hardware-station-configuration-installation.md) for at få oplysninger om installation af afsnittet **Hardwarestationer**.</span><span class="sxs-lookup"><span data-stu-id="a469d-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="a469d-134">Følgende billede viser et eksempel på konfiguration af en detailkanal.</span><span class="sxs-lookup"><span data-stu-id="a469d-134">The following image shows an example retail channel setup configuration.</span></span>

![Eksempel på detailkanalkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="a469d-136">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="a469d-136">Additional channel set up</span></span>

<span data-ttu-id="a469d-137">Der er flere elementer der skal konfigureres for en kanal, som kan findes i **Handlingsrude** under sektionen **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="a469d-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="a469d-138">Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, kontantopgørelse, leveringsmetoder, indtægts/udgiftskonto, sektioner gruppetildeling for opfyldelse og pengeskabe.</span><span class="sxs-lookup"><span data-stu-id="a469d-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="a469d-139">I følgende billede vises de yderligere indstillinger for opsætning af detailkanal under fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="a469d-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Konfigurer kanal](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="a469d-141">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="a469d-141">Set up payment methods</span></span>

<span data-ttu-id="a469d-142">Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="a469d-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="a469d-143">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="a469d-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="a469d-144">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-145">Vælg den ønskede betalingsmetode i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="a469d-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="a469d-146">Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.</span><span class="sxs-lookup"><span data-stu-id="a469d-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="a469d-147">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="a469d-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="a469d-148">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a469d-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a469d-149">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="a469d-149">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="a469d-151">Opsætning af kontantopgørelse</span><span class="sxs-lookup"><span data-stu-id="a469d-151">Set up cash declaration</span></span>

1. <span data-ttu-id="a469d-152">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Kontantopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="a469d-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="a469d-153">Vælg **Ny** i handlingsruden, og opret derefter alle relevante **Mønter** og **Pengesedler**.</span><span class="sxs-lookup"><span data-stu-id="a469d-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="a469d-154">Følgende billede viser et eksempel på en kontantopgørelse.</span><span class="sxs-lookup"><span data-stu-id="a469d-154">The following image shows an example of a cash declaration.</span></span>

![Opsætning af kontantopgørelser](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="a469d-156">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="a469d-156">Set up modes of delivery</span></span>

<span data-ttu-id="a469d-157">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="a469d-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="a469d-158">Udfør følgende trin for at ændre eller tilføje en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="a469d-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="a469d-159">Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="a469d-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="a469d-160">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.</span><span class="sxs-lookup"><span data-stu-id="a469d-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="a469d-161">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen.</span><span class="sxs-lookup"><span data-stu-id="a469d-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="a469d-162">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="a469d-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="a469d-163">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="a469d-163">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="a469d-165">Konfigurer indtægts/udgiftskonto</span><span class="sxs-lookup"><span data-stu-id="a469d-165">Set up income/expense account</span></span>

<span data-ttu-id="a469d-166">Gør følgende for at konfigurere en indtægts/udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="a469d-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="a469d-167">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Indtægts/udgiftskonto**.</span><span class="sxs-lookup"><span data-stu-id="a469d-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="a469d-168">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-169">Angiv et navn under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a469d-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="a469d-170">Angiv et søgenavn under **Søgenavn**.</span><span class="sxs-lookup"><span data-stu-id="a469d-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="a469d-171">Angiv kontotypen under **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="a469d-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="a469d-172">Angiv tekst for **Meddelelseslinje 1**, **Meddelelseslinje 2**, **Bilag 1** og **Bilag 2** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a469d-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="a469d-173">Angiv bogføringsoplysninger under **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="a469d-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="a469d-174">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a469d-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a469d-175">Følgende billede viser et eksempel på en indtægts/udgiftskonto.</span><span class="sxs-lookup"><span data-stu-id="a469d-175">The following image shows an example of an income/expense account.</span></span>

![Konfigurer indtægts/udgiftskonti](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="a469d-177">Konfigurere sektioner</span><span class="sxs-lookup"><span data-stu-id="a469d-177">Set up sections</span></span>

<span data-ttu-id="a469d-178">Gør følgende for at konfigurere sektioner.</span><span class="sxs-lookup"><span data-stu-id="a469d-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="a469d-179">I handlingsruden skal du vælge **Sektioner** under **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="a469d-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="a469d-180">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-181">Angiv et sektionsnummer under **Sektionsnummer**.</span><span class="sxs-lookup"><span data-stu-id="a469d-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="a469d-182">Indtast en beskrivelse under **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a469d-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="a469d-183">Angiv en sektionsstørrelse under **Sektionsstørrelse**.</span><span class="sxs-lookup"><span data-stu-id="a469d-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="a469d-184">Konfigurer yderligere indstillinger for **Generelt** og **Salgsstatistik** efter behov.</span><span class="sxs-lookup"><span data-stu-id="a469d-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="a469d-185">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a469d-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="a469d-186">Konfigurer en gruppetildeling for opfyldelse</span><span class="sxs-lookup"><span data-stu-id="a469d-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="a469d-187">Gør følgende for at konfigurere en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="a469d-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="a469d-188">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.</span><span class="sxs-lookup"><span data-stu-id="a469d-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="a469d-189">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-190">Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="a469d-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="a469d-191">Indtast en beskrivelse i rullelisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a469d-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="a469d-192">Gå til handlingsruden, og vælg **Gem**</span><span class="sxs-lookup"><span data-stu-id="a469d-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="a469d-193">Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="a469d-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Konfigurer gruppetildelinger for opfyldelse](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="a469d-195">Konfigurer pengeskabe</span><span class="sxs-lookup"><span data-stu-id="a469d-195">Set up safes</span></span>

<span data-ttu-id="a469d-196">Gør følgende for at konfigurere pengeskabe.</span><span class="sxs-lookup"><span data-stu-id="a469d-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="a469d-197">I handlingsruden skal du vælge **Pengeskabe** under **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="a469d-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="a469d-198">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a469d-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a469d-199">Angiv et navn til pengeskabet.</span><span class="sxs-lookup"><span data-stu-id="a469d-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="a469d-200">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a469d-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a469d-201">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a469d-201">Additional resources</span></span>

[<span data-ttu-id="a469d-202">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="a469d-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a469d-203">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="a469d-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a469d-204">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="a469d-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="a469d-205">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="a469d-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

