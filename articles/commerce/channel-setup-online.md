---
title: Konfigurere en onlinekanal
description: Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107224"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="aca68-103">Konfigurere en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="aca68-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="aca68-104">Dette emne beskriver, hvordan du opretter en ny onlinekanal i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aca68-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aca68-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="aca68-105">Overview</span></span>

<span data-ttu-id="aca68-106">Dynamics 365 Commerce understøtter flere detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="aca68-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="aca68-107">Disse detailkanaler omfatter onlinebutikker, call centre og detailbutikker (også kaldet fysiske butikker).</span><span class="sxs-lookup"><span data-stu-id="aca68-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="aca68-108">Onlinebutikker giver kunderne mulighed for at købe produkter fra detailhandlerens onlinebutik ud over fra detailhandlerens fysiske butik.</span><span class="sxs-lookup"><span data-stu-id="aca68-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="aca68-109">Hvis du vil oprette en onlinebutik i Commerce, skal du først oprette en onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="aca68-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="aca68-110">Før du opretter en ny onlinekanal, skal du sikre dig, at du har fuldført [forudsætningerne for kanalopsætning](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="aca68-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="aca68-111">Før du kan oprette et nyt websted, skal der oprettes mindst én onlinebutik i Commerce.</span><span class="sxs-lookup"><span data-stu-id="aca68-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="aca68-112">Du kan finde flere oplysninger under [Oprette et websted for e-handel](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="aca68-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="aca68-113">Oprette og konfigurere en ny onlinekanal</span><span class="sxs-lookup"><span data-stu-id="aca68-113">Create and configure a new online channel</span></span>

<span data-ttu-id="aca68-114">Følg disse trin for at oprette en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="aca68-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="aca68-115">Gå til **Moduler \> Kanaler \> Onlinebutikker** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="aca68-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="aca68-116">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aca68-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aca68-117">Skriv et navn til den nye kanal i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="aca68-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="aca68-118">Angiv den relevante **Juridiske enhed** på rullelisten Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="aca68-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="aca68-119">Angiv det relevante **Lagersted** på rullelisten Lagersted.</span><span class="sxs-lookup"><span data-stu-id="aca68-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="aca68-120">Vælg den relevante tidszone i feltet **Lagertidszone**.</span><span class="sxs-lookup"><span data-stu-id="aca68-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="aca68-121">Vælg den relevante valuta i feltet **Valuta**.</span><span class="sxs-lookup"><span data-stu-id="aca68-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="aca68-122">Angiv en gyldig standardkunde i feltet **Standardkunde**.</span><span class="sxs-lookup"><span data-stu-id="aca68-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="aca68-123">Angiv et gyldigt adressekartotek i feltet **Kundeadressekartotek**.</span><span class="sxs-lookup"><span data-stu-id="aca68-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="aca68-124">Vælg en funktionalitetsprofil i feltet **Funktionalitetsprofil** , hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="aca68-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="aca68-125">Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="aca68-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="aca68-126">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aca68-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aca68-127">Følgende billede viser oprettelsen af en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="aca68-127">The following image shows the creation of a new online channel.</span></span>

![Ny onlinekanal](media/channel-setup-online-1.png)

<span data-ttu-id="aca68-129">Følgende billede viser et eksempel på en onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="aca68-129">The following image shows an example online channel.</span></span>

![Eksempel på onlinekanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="aca68-131">Konfigurer sprog</span><span class="sxs-lookup"><span data-stu-id="aca68-131">Set up languages</span></span>

<span data-ttu-id="aca68-132">Hvis dit e-handels-websted skal understøtte flere sprog, skal du udvide afsnittet **Sprog** og tilføje flere sprog efter behov.</span><span class="sxs-lookup"><span data-stu-id="aca68-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="aca68-133">Konfigurere betalingskonto</span><span class="sxs-lookup"><span data-stu-id="aca68-133">Set up payment account</span></span>

<span data-ttu-id="aca68-134">Du kan tilføje en tredjepartsbetalingsudbyder i sektionen **Betalingskonto**.</span><span class="sxs-lookup"><span data-stu-id="aca68-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="aca68-135">Du kan få oplysninger om konfiguration af en Adyen-betalingsconnector i [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="aca68-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="aca68-136">Yderligere kanalopsætning</span><span class="sxs-lookup"><span data-stu-id="aca68-136">Additional channel setup</span></span>

<span data-ttu-id="aca68-137">Yderligere opgaver, der kræves til konfiguration af onlinekanalen, omfatter konfiguration af betalingsmetoder, leveringsmetoder og gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="aca68-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="aca68-138">Følgende billede viser opsætningsindstillinger til **Leveringsmetoder** , **Betalingsmetoder** og **Gruppetildeling for opfyldelse** under fanen **Opsætning** .</span><span class="sxs-lookup"><span data-stu-id="aca68-138">The following image shows **Modes of delivery** , **Payment methods** , and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Yderligere handlinger til konfiguration af onlinekanal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="aca68-140">Oprette betalingsmåder</span><span class="sxs-lookup"><span data-stu-id="aca68-140">Set up payment methods</span></span>

<span data-ttu-id="aca68-141">Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.</span><span class="sxs-lookup"><span data-stu-id="aca68-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="aca68-142">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.</span><span class="sxs-lookup"><span data-stu-id="aca68-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="aca68-143">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aca68-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aca68-144">Vælg den ønskede betalingsmetode i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="aca68-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="aca68-145">Angiv et **Handlingsnavn** i sektionen **Generelt** , og konfigurer evt. andre ønskede indstillinger.</span><span class="sxs-lookup"><span data-stu-id="aca68-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="aca68-146">Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.</span><span class="sxs-lookup"><span data-stu-id="aca68-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="aca68-147">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aca68-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aca68-148">Følgende billede viser et eksempel på en metode til kontantbetaling.</span><span class="sxs-lookup"><span data-stu-id="aca68-148">The following image shows an example of a cash payment method.</span></span>

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="aca68-150">Konfigurer leveringsmåder</span><span class="sxs-lookup"><span data-stu-id="aca68-150">Set up modes of delivery</span></span>

<span data-ttu-id="aca68-151">Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="aca68-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="aca68-152">Udfør følgende trin for at ændre eller tilføje en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="aca68-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="aca68-153">Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="aca68-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="aca68-154">Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.</span><span class="sxs-lookup"><span data-stu-id="aca68-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="aca68-155">Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen.</span><span class="sxs-lookup"><span data-stu-id="aca68-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="aca68-156">Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.</span><span class="sxs-lookup"><span data-stu-id="aca68-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="aca68-157">Følgende billede viser et eksempel på en leveringsmetode.</span><span class="sxs-lookup"><span data-stu-id="aca68-157">The following image shows an example of a mode of delivery.</span></span>

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="aca68-159">Konfigurer en gruppetildeling for opfyldelse</span><span class="sxs-lookup"><span data-stu-id="aca68-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="aca68-160">Gør følgende for at konfigurere en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="aca68-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="aca68-161">Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Gruppetildeling for opfyldelse**.</span><span class="sxs-lookup"><span data-stu-id="aca68-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="aca68-162">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aca68-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="aca68-163">Vælg en opfyldelsesgruppe på rullelisten **Opfyldelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="aca68-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="aca68-164">Indtast en beskrivelse i rullelisten **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="aca68-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="aca68-165">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="aca68-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="aca68-166">Følgende billede viser et eksempel på en opsætning af en gruppetildeling for opfyldelse.</span><span class="sxs-lookup"><span data-stu-id="aca68-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Konfigurer Gruppetildeling for opfyldelse](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="aca68-168">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="aca68-168">Additional resources</span></span>

[<span data-ttu-id="aca68-169">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="aca68-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="aca68-170">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="aca68-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="aca68-171">Konfigurer en detailkanal</span><span class="sxs-lookup"><span data-stu-id="aca68-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="aca68-172">Konfigurere en callcenter-kanal</span><span class="sxs-lookup"><span data-stu-id="aca68-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="aca68-173">Dynamics 365-betalingsconnector til Adyen</span><span class="sxs-lookup"><span data-stu-id="aca68-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
