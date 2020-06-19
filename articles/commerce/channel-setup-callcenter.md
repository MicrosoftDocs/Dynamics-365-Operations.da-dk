---
title: Konfigurere en callcenter-kanal
description: Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
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
ms.openlocfilehash: bdaabad39484cb12537bc5f94c34dcb2575a5b2f
ms.sourcegitcommit: ef27189efc15ce79c3c31ce2e41ef8a606fc5429
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410407"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="00e25-103">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="00e25-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="00e25-104">Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="00e25-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="00e25-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="00e25-105">Overview</span></span>


<span data-ttu-id="00e25-106">I Dynamics 365 Commerce er et callcenter en slags Commerce-kanal, som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="00e25-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="00e25-107">Hvis du definerer en kanal til dit callcenter, kan systemet binde specifikke data og ordrebehandlingstandarder til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="00e25-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="00e25-108">Mens en virksomhed kan definere flere callcenter-kanaler i Commerce, er det vigtigt at bemærke, at en individuel bruger kun kan knyttes til én callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="00e25-109">Før du opretter en ny callcenter-kanal, skal du sikre dig, at du har fuldført [Forudsætningerne for kanalopsætning](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="00e25-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="00e25-110">Oprette og konfigurere en ny callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="00e25-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="00e25-111">Følg disse trin for at oprette en ny callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="00e25-112">Gå til **Retail og Commerce \> Kanaler \> Call centre \> Alle call centre** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="00e25-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="00e25-113">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00e25-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="00e25-114">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="00e25-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="00e25-115">Vælg den relevante **Juridisk enhed** fra rullelisten.</span><span class="sxs-lookup"><span data-stu-id="00e25-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="00e25-116">Vælg placeringen af det relevante **Lagersted** fra rullelisten.</span><span class="sxs-lookup"><span data-stu-id="00e25-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="00e25-117">Dette sted bruges som standard på salgsordrer, som oprettes for denne call centerkanal, medmindre der er defineret andre standarder på kunde- eller vareniveau.</span><span class="sxs-lookup"><span data-stu-id="00e25-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="00e25-118">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="00e25-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="00e25-119">Disse data bruges til automatisk udfyldelse af standarder, når der oprettes nye kundeposter.</span><span class="sxs-lookup"><span data-stu-id="00e25-119">This data is used to assist in auto-populating defaults when new customer records are created.</span></span> <span data-ttu-id="00e25-120">Når du opretter call center-ordrer, er det ikke tilrådeligt at oprette ordrer til standardkunden.</span><span class="sxs-lookup"><span data-stu-id="00e25-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="00e25-121">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="00e25-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="00e25-122">Når der oprettes og behandles call center-ordrer, bruges profilen til mailbeskeder for at udløse automatiske mailpåmindelser til kunder med oplysninger om deres ordrestatus.</span><span class="sxs-lookup"><span data-stu-id="00e25-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="00e25-123">Angiv en oplysningskode for **Prisændring**.</span><span class="sxs-lookup"><span data-stu-id="00e25-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="00e25-124">Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="00e25-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="00e25-125">Denne oplysningskode indeholder de sæt årsagskoder, som brugeren vil blive bedt om at vælge mellem, når hun/han bruger funktionaliteten for prisændring på en call center-ordre.</span><span class="sxs-lookup"><span data-stu-id="00e25-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="00e25-126">Angiv en oplysningskode for **Venteposition**.</span><span class="sxs-lookup"><span data-stu-id="00e25-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="00e25-127">Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="00e25-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="00e25-128">Denne oplysningskode indeholder de sæt valgfrie årsagskoder, som brugeren vil blive bedt om at vælge mellem, når hun/han sætter en ordre på hold.</span><span class="sxs-lookup"><span data-stu-id="00e25-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="00e25-129">Angiv en oplysningskode for **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="00e25-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="00e25-130">Du skal måske oprette en oplysningskode til dette først.</span><span class="sxs-lookup"><span data-stu-id="00e25-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="00e25-131">Denne oplysningskode indeholder det sæt årsagskoder, som brugeren kan vælge imellem, når hun/han bruger call centerets ordrekreditfunktion for at give kunden diverse refunderinger for årsagen til kundeservice.</span><span class="sxs-lookup"><span data-stu-id="00e25-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="00e25-132">Valgfrit: Konfigurer økonomiske dimensioner på oversigtspanelet **Økonomiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="00e25-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="00e25-133">De dimensioner, der angives her, vil som standard være i en salgsordre, der er oprettet i denne call center-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="00e25-134">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="00e25-134">Click **Save**.</span></span>

<span data-ttu-id="00e25-135">Følgende billede viser oprettelsen af en ny callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-135">The following image shows the creation of a new call center channel.</span></span>

![Ny callcenter-kanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="00e25-137">Følgende billede viser et eksempel på en callcenter-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-137">The following image shows an example call center channel.</span></span>

![Eksempel på call center-kanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="00e25-139">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="00e25-139">Additional channel setup</span></span>

<span data-ttu-id="00e25-140">Yderligere opgaver, der kræves til konfiguration af callcenter-kanalen, omfatter opsætning af betalingsmetoder og leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="00e25-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="00e25-141">I følgende billede vises konfigurationsindstillinger til **Leveringsmetoder** og **Betalingsmetoder** under fanen **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="00e25-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Yderligere handlinger til konfiguration af callcenter-kanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="00e25-143">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="00e25-143">Set up payment methods</span></span>

<span data-ttu-id="00e25-144">Hvis du vil oprette betalingsmetoder, skal du følge disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="00e25-145">Brugerne skal vælge fra foruddefinerede betalingsmetoder for at kæde dem sammen med call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="00e25-146">Før du konfigurerer dine call center-betalingsmetoder, skal du først konfigurere dine stambetalingsmåder i **Retail og Commerce \> Konfiguration af kanal \> Betalingsmetoder \> Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="00e25-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="00e25-147">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="00e25-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="00e25-148">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00e25-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="00e25-149">I navigationsruden skal du vælge en betalingsmetode fra de foruddefinerede tilgængelige betalinger.</span><span class="sxs-lookup"><span data-stu-id="00e25-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="00e25-150">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="00e25-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="00e25-151">Ved kreditkort, gavekort eller fordelskundekort skal du udføre yderligere opsætning ved at vælge funktionen **Opsætning af kort**.</span><span class="sxs-lookup"><span data-stu-id="00e25-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="00e25-152">Konfigurer korrekte bogføringskonti for betalingstypen i afsnittet **Bogføring**.</span><span class="sxs-lookup"><span data-stu-id="00e25-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="00e25-153">Klik på **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00e25-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="00e25-154">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="00e25-154">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="00e25-156">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="00e25-156">Set up modes of delivery</span></span>

<span data-ttu-id="00e25-157">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="00e25-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="00e25-158">Hvis du vil ændre eller tilføje en leveringsmåde, der skal knyttes til call center-kanalen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="00e25-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="00e25-159">Vælg **Administrer leveringsmåder** i formularen Call centerets leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="00e25-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="00e25-160">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.</span><span class="sxs-lookup"><span data-stu-id="00e25-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="00e25-161">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="00e25-162">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="00e25-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="00e25-163">Sørg for, at leveringsmåden er konfigureret med data i oversigtspanelet **Produkter** og oversigtspanelet **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="00e25-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="00e25-164">Hvis ingen produkter eller leveringsadresser er gyldige i forbindelse med leveringsmåden, vil der opstå fejl, hvis du vælger den under ordreindtastning.</span><span class="sxs-lookup"><span data-stu-id="00e25-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="00e25-165">Når der er foretaget ændringer i call center-tilstanden for leveringskonfigurationer, skal jobbet **Behandling af leveringsmåder** køres for at udfolde ændringsmatrixen.</span><span class="sxs-lookup"><span data-stu-id="00e25-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="00e25-166">Dette job kan findes ved at navigere til **Retail og Commerce \> Retail og Commerce IT \> Behandling af leveringsmåder**.</span><span class="sxs-lookup"><span data-stu-id="00e25-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="00e25-167">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="00e25-167">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="00e25-169">Konfigurer kanalbrugere</span><span class="sxs-lookup"><span data-stu-id="00e25-169">Set up channel users</span></span>

<span data-ttu-id="00e25-170">Hvis en bruger vil oprette en salgsordre, der er knyttet til call center-kanalen fra Commerce Headquarters, skal denne bruger, der opretter salgsordren, være knyttet til call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="00e25-171">Brugeren kan ikke manuelt sammenkæde en salgsordre, der er oprettet i Commerce Headquarters, til call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-171">The user can not manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="00e25-172">Sammenkædningen er systematisk og baseret på brugeren og brugerens forhold til call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="00e25-173">En bruger kan kun være knyttet til én call center-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="00e25-174">Vælg fanen **Kanal** i handlingsruden, og vælg derefter **Kanalbrugere**.</span><span class="sxs-lookup"><span data-stu-id="00e25-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="00e25-175">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="00e25-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="00e25-176">Vælg et eksisterende **Bruger-id** på rullelisten for at knytte denne bruger til call center-kanalen</span><span class="sxs-lookup"><span data-stu-id="00e25-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="00e25-177">Når kanabrugeren er konfigureret, og brugeren opretter en ny salgsordre i Commerce Headquarters, vil denne salgsordre blive sammenkædet med brugerens tilknyttede call center-kanal.</span><span class="sxs-lookup"><span data-stu-id="00e25-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="00e25-178">Eventuelle konfigurationer til denne kanal anvendes systematisk på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="00e25-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="00e25-179">En bruger kan bekræfte, hvilken call center-kanal salgsordren er knyttet til, ved at få vist referencen til kanalnavnet i salgsordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="00e25-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="00e25-180">Konfigurer prisgrupper</span><span class="sxs-lookup"><span data-stu-id="00e25-180">Set up price groups</span></span>

<span data-ttu-id="00e25-181">Prisgrupper er valgfrie, men hvis de bruges, kan man styre, hvilke salgspriser der tilbydes til kunder, som placerer ordrer i call center-kanalen.</span><span class="sxs-lookup"><span data-stu-id="00e25-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="00e25-182">Hvis der ikke er konfigureret en prisgruppe for kunden, eller hvis der ikke anvendes katalogprisgrupper på salgsordren (ved hjælp af feltet **Kildekode-id** i call center-ordrens overskrift), bruges kanalens prisgruppe til at finde varepriser.</span><span class="sxs-lookup"><span data-stu-id="00e25-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="00e25-183">Hvis der ikke findes en prisgruppe på call center-kanalen, bruges standardvarens stampriser.</span><span class="sxs-lookup"><span data-stu-id="00e25-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="00e25-184">Gør følgende for at oprette en prisgruppe.</span><span class="sxs-lookup"><span data-stu-id="00e25-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="00e25-185">Klik på fanen **Kanal** i handlingsruden, og vælg derefter **Prisgrupper**.</span><span class="sxs-lookup"><span data-stu-id="00e25-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="00e25-186">Klik på **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="00e25-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="00e25-187">Vælg en **Detailprisgruppe** på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="00e25-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00e25-188">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="00e25-188">Additional resources</span></span>

[<span data-ttu-id="00e25-189">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="00e25-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="00e25-190">Funktionalitet til callcenter-salg</span><span class="sxs-lookup"><span data-stu-id="00e25-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="00e25-191">Konfigurere indstillinger for callcenter-ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="00e25-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="00e25-192">Callcenter-kataloger</span><span class="sxs-lookup"><span data-stu-id="00e25-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="00e25-193">Konfigurere og arbejde med advarsler om svindel</span><span class="sxs-lookup"><span data-stu-id="00e25-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="00e25-194">Oprette kontinuitetsprogrammer for callcentre</span><span class="sxs-lookup"><span data-stu-id="00e25-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
